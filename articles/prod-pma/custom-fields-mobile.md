---
title: Pielāgoto lauku ieviešana Microsoft Dynamics 365 Project Timesheet mobilajā programmā operētājsistēmā iOS un Android
description: Šajā rakstā ir sniegti bieži sastopami paplašinājumu izmantošanas modeļi pielāgotu lauku ieviešanai.
author: Yowelle
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 03b79d58d1f91e07034b8c9efb408e6d7a9c29a8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913721"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Pielāgoto lauku ieviešana Microsoft Dynamics 365 Project Timesheet mobilajā programmā operētājsistēmā iOS un Android

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegti bieži sastopami paplašinājumu izmantošanas modeļi pielāgotu lauku ieviešanai. Ir ietverti šādi raksti:

- Dažādie datu tipi, kurus atbalsta pielāgotā lauku struktūra
- Kā laika uzskaites tabulās parādīt tikai lasāmus vai rediģējamus ierakstus un saglabāt lietotāja sniegtās vērtības atpakaļ datu bāzē
- Kā rādīt tikai lasāmus laukus laika uzskaites tabulas galvenē
- Kā integrēt citu pielāgoto biznesa loģiku, lai laukos ievadītu noklusējuma vērtības un veiktu papildu validāciju

## <a name="audience"></a>Auditorija

Šis raksts ir paredzēts izstrādātājiem, kuri integrē savus pielāgotos laukus mobilajā lietojumprogrammā Microsoft Dynamics 365 Project Timesheet, kas ir pieejama Apple iOS un Google Android. Tiek pieņemts, ka lasītāji pārzina X++ izstrādi un projekta laika uzskaites tabulu funkcionalitāti.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Datu līgums — TSTimesheetCustomField X++ klase

**TSTimesheetCustomField** klase ir X++ datu līguma klase, kas atspoguļo informāciju par pielāgotu laika uzskaites tabulas funkcionalitātes lauku. Pielāgoto lauku objektu saraksti tiek nodoti gan TSTimesheetDetails datu līgumam, gan TSTimesheetEntry datu līgumam, lai rādītu pielāgotos laukus mobilajā programmā.

- **TSTimesheetDetails** — laika uzskaites tabulas galvenes līgums.
- **TSTimesheetEntry** — laika uzskaites tabulas transakcijas līgums. Šo objektu grupas, kurām ir vienāda projekta informācija un **timesheetLineRecId** vērtība, veido rindu.

### <a name="fieldbasetype-types"></a>fieldBaseType (Types)

Rekvizīts **FieldBaseType** objektā **TsTimesheetCustom** nosaka tā lauka veidu, kas tiek parādīts programmā. Tiek atbalstītas tālāk norādītās **Types** vērtības.

| Types vērtība | Veids              | Piezīmes |
|-------------|-------------------|-------|
| 0           | Virkne (un uzskaitījums) | Lauks tiek parādīts kā teksta lauks. |
| 1           | Integer           | Šī vērtība tiek parādīta kā skaitlis bez decimāldaļām. |
| 2           | Real              | Šī vērtība tiek parādīta kā skaitlis ar decimāldaļām.<p>Lai programmā parādītu faktisko vērtību kā valūtu, izmantojiet rekvizītu **fieldExtenededType**. Varat izmantot rekvizītu **numberOfDecimals**, lai iestatītu parādāmo decimāldaļu skaitu.</p> |
| 3           | Datums              | Datuma formātus nosaka lietotāja iestatījums **Datuma, laika un ciparu formāts**, kas ir norādīts iestatījumos **Valodas un valsts/reģiona reference** sadaļā **Lietotāja opcijas**. |
| 4           | Boolean           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Ja rekvizīts **stringOptions** nav norādīts objektā **TSTimesheetCustomField**, lietotājam tiek nodrošināts brīva teksta lauks.

    Rekvizītu **stringLength** var izmantot, lai iestatītu maksimālo virknes garumu, ko lietotāji var ievadīt.

- Ja rekvizīts **stringOptions** ir norādīts objektā **TSTimesheetCustomField**, šie saraksta elementi ir vienīgās vērtības, ko lietotāji var atlasīt, izmantojot opciju pogas (radiopogas).

    Šajā gadījumā virknes lauks var darboties kā uzskaitījuma vērtība lietotāja ieraksta vajadzībām. Lai saglabātu vērtību datu bāzē kā uzskaitījumu, pirms saglabāšanas datu bāzē manuāli kartējiet virknes vērtību atpakaļ uz uzskaitījuma vērtību, izmantojot komandķēdi (piemēram, skatiet sadaļu "Izmantot komandķēdi TSTimesheetEntryService klasē, lai saglabātu darba laika uzskaites tabulas ierakstu no programmas atpakaļ uz datu bāzi" tālāk šajā rakstā).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Šo rekvizītu var izmantot, lai formatētu reālas vērtības kā valūtu. Šī pieeja ir piemērojama tikai tad, ja **fieldBaseType** vērtība ir **Real**.

- **TSCustomFieldExtendedType:None** — formatējums netiek lietots.
- **TSCustomFieldExtendedType::Currency** — vērtības formatēšana valūtā.

    Ja valūtas formatēšana ir aktīva, lauku **stringValue** var lietot, lai nodotu valūtas kodu, kas jārāda programmā. Šī vērtība ir tikai lasāma.

    Lauks **realValue** satur naudas summu, kas jāsaglabā datu bāzē.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Šo rekvizītu var izmantot, lai norādītu, kur programmā jārāda pielāgotais lauks.

- **TSCustomFieldSection::Header** — lauks tiks parādīts programmas sadaļā **Skatīt detalizētu informāciju**. Šie vienmēr ir tikai lasāmie lauki.
- **TSCustomFieldSection::Line** — lauks tiks parādīts pēc visiem iebūvētajiem rindu laukiem laika uzskaites tabulas ierakstos. Šie lauki var būt rediģējami vai tikai lasāmi.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Šis rekvizīts identificē lauku, kad programmas nodrošinātās vērtības tiek saglabātas atpakaļ datu bāzē.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Šis rekvizīts identificē lauku, kad programmas nodrošinātās vērtības tiek saglabātas atpakaļ datu bāzē.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Iestatiet šo rekvizītu uz **Yes**, lai norādītu, ka lauku laika uzskaites tabulas ierakstu sadaļā lietotāji var rediģēt. Iestatiet rekvizītu uz **No**, lai padarītu lauku tikai lasāmu.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Iestatiet šo rekvizītu uz **Yes**, lai norādītu, ka laukam laika uzskaites tabulas ierakstu sadaļā jābūt obligātam.

### <a name="label-str"></a>label (str)

Šajā rekvizītā ir norādīta etiķete, kas tiek parādīta blakus laukam programmā.

### <a name="stringoptions-list-of-strings"></a>stringOptions (List of Strings)

Šis rekvizīts ir lietojams tikai tad, ja **fieldBaseType** ir iestatīts uz **String**. Ja **stringOptions** ir iestatīts, virkņu vērtības, kas ir pieejamas atlasei, izmantojot opciju pogas (radiopogas), tiek norādītas pēc virknēm sarakstā. Ja virknes netiek nodrošinātas, brīvā teksta ievade virknes laukā ir atļauta (skatiet piemēru tālāk šajā rakstā sadaļā "Izmantot komandas ķēdi TSTimesheetEntryService klasē, lai saglabātu darba laika uzskaites tabulas ierakstu no programmas atpakaļ datu bāzē").

### <a name="stringlength-int"></a>stringLength (int)

Šajā rekvizītā ir norādīts virknes lauka maksimālais garums. Tas ir lietojams tikai tad, ja **fieldBaseType** ir iestatīts uz **String**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Šis rekvizīts norāda decimāldaļu skaitu, kas tiek rādīts reālo skaitļu laukam. Tas ir lietojams tikai tad, ja **fieldBaseType** ir iestatīts uz **Real**.

### <a name="ordersequence-int"></a>orderSequence (int)

Šis rekvizīts nosaka secību, kādā pielāgotie lauki tiek rādīti programmā, ja ir norādīti vairāki pielāgotie lauki. Lauki, kuros ir mazāki skaitļi, tiek parādīti vispirms.

### <a name="booleanvalue-boolean"></a>booleanValue (boolean)

**Boolean** veida laukiem šis rekvizīts nodod lauka Būla vērtību starp serveri un programmu.

### <a name="guidvalue-guid"></a>guidValue (guid)

**GUID** veida laukiem šis rekvizīts nodod lauka vispārēji unikālā identifikatora (GUID) vērtību starp serveri un programmu.

### <a name="int64value-int64"></a>int64Value (int64)

**Int64** veida laukiem šis rekvizīts nodod lauka Int64 vērtību starp serveri un programmu.

### <a name="intvalue-int"></a>intValue (int)

**Int** veida laukiem šis rekvizīts nodod lauka Int vērtību starp serveri un programmu.

### <a name="realvalue-real"></a>realValue (real)

**Real** veida laukiem šis rekvizīts nodod lauka reālo vērtību starp serveri un programmu.

### <a name="stringvalue-str"></a>stringValue (str)

**String** veida laukiem šis rekvizīts nodod lauka virknes vērtību starp serveri un programmu. Tas tiek izmantots arī **Real** veida laukiem, kas formatēti kā valūta. Šiem laukiem rekvizīts tiek izmantots, lai nodotu valūtas kodu programmai.

### <a name="datevalue-date"></a>dateValue (date)

**Date** veida laukiem šis rekvizīts nodod lauka datuma vērtību starp serveri un programmu.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Pielāgota lauka rādīšana un saglabāšana laika uzskaites tabulas ierakstu sadaļā

Tālāk ir redzams izveidotās laika uzskaites tabulas ieraksta ekrānuzņēmums mobilajā programmā. Tajā ir redzami iebūvētie lauki un pielāgots lauks sadaļā “Laika ieraksts”, kura nosaukums ir “Testa virkne”, un uzskaitījuma vērtība “Otrā opcija” jau ir iestatīta.

![Testa virknes pielāgotais lauks programmā.](media/timesheet-entry.jpg)



Tālāk ir redzams mobilās programmas ekrānuzņēmums, kur lietotājs atlasa vienu no uzskaitījuma opcijām, kas pieejamas pielāgotajam laukam “Testa virkne”.  Šīs divas opcijas ir “Pirmais variants” un “Otrā opcija”, kas tiek rādītas kā radiopogas. Pašlaik ir atlasīta otrā opcija.

![Opciju pogas (radiopogas) testa virknes pielāgotajam laukam.](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>TSTimesheetLine tabulas paplašināšana, lai tai būtu pielāgotais lauks

Tipiskos scenārijos ir iespējams, ka dati, kas paredzēti pielāgotajam laukam laika uzskaites tabulas ierakstu sadaļā, tiks saglabāti tabulā TSTimesheetLine. Taču var izmantot arī citas tabulas, ja datus var izgūt, pamatojoties uz nodrošinātu TSTimesheetTrans ierakstu vai ja tiem nav konkrēta ieraksta konteksta (piemēram, ja lauks ir iestatīts kā tikai lasāms projekta parametros).

Ņemiet vērā, ka pielāgotajiem laukiem nav nepieciešami nekādi datu bāzes dublējuma ieraksti. Tos var dinamiski ģenerēt, izmantojot X++ loģiku. Šī pieeja var būt noderīga tikai lasāmos scenārijos (dinamiski ģenerētu pielāgoto lauku vērtību piemēru skatiet sadaļā “Komandu ķēdes izmantošana TSTimesheetDetails klasē, buildCustomFieldListForHeader metode, lai ievadītu laika uzskaites tabulas detaļas”).

Zemāk ir Visual Studio ekrānuzņēmums ar programmas objektu koku. Tajā ir redzams TSTimesheetLine tabulas paplašinājums ar TestLineString lauku, kas pievienots kā pielāgots lauks.

![Rindas virkne.](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Komandu ķēdes izmantošana buildCustomFieldList metodei TSTimesheetSettings klasē, lai parādītu lauku laika uzskaites tabulas ierakstu sadaļā

Šis kods kontrolē lauka rādīšanas iestatījumus programmā. Piemēram, tas kontrolē lauka tipu, etiķeti, to, vai lauks ir obligāts, kā arī to, kurā sadaļā šis lauks tiek rādīts.

Nākamajā piemērā i parādīts virknes lauks laika ierakstos. Šim laukam ir divas opcijas, **Pirmā opcija** un **Otrā opcija**, kas pieejamas, izmantojot opciju pogas (radiopogas). Programmas lauks ir saistīts ar lauku **TestLineString**, kas tiek pievienots tabulai TSTimesheetLine.

Ņemiet vērā, ka varat izmantot **TSTimesheetCustomField::newFromMetatdata()** metodi, lai vienkāršotu pielāgoto lauku rekvizītu inicializēšanu: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** un **numberOfDecimals**. Šos parametrus var iestatīt arī manuāli.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Komandu ķēdes izmantošana buildCustomFieldListForEntry metodei TSTimesheetEntry klasē, lai ievadītu vērtības laika uzskaites tabulas ierakstā

Metode **BuildCustomFieldListForEntry** tiek izmantota, lai ievadītu vērtības saglabātajās laika uzskaites tabulas rindās mobilajā programmā. Kā parametrs tiek ņemts TSTimesheetTrans ieraksts. Šī ieraksta laukus var izmantot, lai programmā ievadītu pielāgotā lauka vērtību.

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Komandu ķēdes izmantošana TSTimesheetEntryService klasē, lai saglabātu laika uzskaites tabulas ierakstu no programmas atpakaļ datu bāzē

Lai saglabātu pielāgotu lauku datu bāzē tipiska lietojuma veidā, ir jāpaplašina vairākas metodes:

- Metode **timesheetLineNeedsUpdating** tiek izmantota, lai noteiktu, vai lietotājs programmā ir mainījis rindas ierakstu un vai tas ir jāsaglabā datu bāzē. Ja veiktspēja nerada bažas, šo metodi var vienkāršot, lai tā vienmēr atgrieztu **true**.
- Metodes **populateTimesheetLineFromEntryDuringCreate** un **populateTimesheetLineFromEntryDuringUpdate** var paplašināt tā, lai tās TSTimesheetLine datu bāzes ierakstā ievadītu vērtības no nodrošinātā TSTimesheetEntry datu līguma ieraksta. Turpmāk norādītajā piemērā pievērsiet uzmanību tam, kā datu bāzes lauka un ieraksta lauka kartēšana tiek veikta manuāli, izmantojot X++ kodu.
- Metodi **populateTimesheetWeekFromEntry** var paplašināt arī tad, ja pielāgoto lauku, kas ir kartēts uz **TSTimesheetEntry** objektu, nepieciešams rakstīt atpakaļ uz TSTimesheetLineweek datu bāzes tabulu.

> [!NOTE]
> Šajā piemērā tiek saglabāta **firstOption** vai **secondOption** vērtība, ko lietotājs atlasa datu bāzē kā neapstrādātu virknes vērtību. Ja datu bāzes lauks ir **Enum** veida lauks, šīs vērtības var manuāli kartēt uz uzskaitījuma vērtību un pēc tam saglabāt datu bāzes tabulas uzskaitījuma laukā.

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Pielāgota lauka rādīšana laika uzskaites tabulas galvenes sadaļā

Tālāk ir redzams ekrānuzņēmums, kurā mobilās programmas lietotājs skata laika uzskaites tabulu. Augšējā labējā stūrī ir atlasīta poga “Papildinformācija”, lai parādītu opciju “Skatīt papildinformāciju”.  

![Detalizētas informācijas skatīšanas komanda.](media/show-more.png)

Tālāk ir redzams ekrānuzņēmums, kurā mobilajā programmā redzama laika uzskaites tabulas sadaļa “Vairāk”. Pielāgots lauks, ko dēvē par “Šīs laika uzskaites tabulas izmantošanas biežums (aprēķinātais pielāgotais lauks), ir pievienots laika uzskaites tabulas galvenes sadaļai. Pielāgotajā laukā ir iestatīta tikai lasāma vērtība “0,667”.

![Papildu sadaļa.](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>TSTimesheetTable tabulas paplašināšana, lai tai būtu pielāgotais lauks

Tipiskos scenārijos ir iespējams, ka dati, kas paredzēti pielāgotajam laukam laika uzskaites tabulas galvenes sadaļā, tiks ņemti no tabulas TSTimesheetHeader. Taču var izmantot arī citas tabulas, ja datus var izgūt, pamatojoties uz nodrošinātu TSTimesheetTable ierakstu vai ja tiem nav konkrēta ieraksta konteksta (piemēram, ja lauks ir iestatīts kā tikai lasāms projekta parametros).

Ņemiet vērā, ka pielāgotajiem laukiem nav nepieciešami nekādi datu bāzes dublējuma ieraksti. Tos var dinamiski ģenerēt, izmantojot X++ loģiku. Tālāk parādīts piemērs, kas demonstrē šādu pieeju.

Galvenes sadaļas lauki programmā vienmēr ir tikai lasāmi.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Komandu ķēdes izmantošana buildCustomFieldList metodei TSTimesheetSettings klasē, lai parādītu lauku galvenes sadaļā

Šis kods kontrolē lauka rādīšanas iestatījumus programmā. Piemēram, tas kontrolē lauka tipu, etiķeti, to, vai lauks ir obligāts, kā arī to, kurā sadaļā šis lauks tiek rādīts.

Nākamajā piemērā ir parādīta aprēķinātā vērtība programmas galvenes sadaļā.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Komandu ķēdes izmantošana buildCustomFieldListForHeader metodei TSTimesheetDetails klasē, lai ievadītu laika uzskaites tabulas detaļas

Metode **buildCustomFieldListForHeader** metode tiek izmantota, lai ievadītu laika uzskaites tabulas galvenes detaļas mobilajā programmā. Kā parametrs tiek ņemts TSTimesheetTable ieraksts. Šī ieraksta laukus var izmantot, lai programmā ievadītu pielāgotā lauka vērtību. Nākamajā piemērā netiek lasītas nekādas vērtības no datu bāzes. Tā vietā tiek izmantota X++ loģika, lai ģenerētu aprēķināto vērtību, kas pēc tam tiek parādīta programmā.


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>Citas konfigurēšanas/paplašināšanas iespējas

### <a name="adding-additional-validation-for-the-app"></a>Papildu validācijas pievienošana programmai

Esošā laika uzskaites tabulas funkcionalitātes loģika datu bāzes līmenī joprojām darbosies kā paredzēts. Lai pārtrauktu saglabāšanas vai iesniegšanas operāciju pabeigšanu un parādītu konkrētu kļūdas ziņojumu, varat pievienot kodam **throw error("message to user")**, izmantojot komandu paplašinājuma ķēdi. Tālāk norādīti trīs noderīgi paplašināmo metožu piemēri.

- Ja **validateWrite** tabulā TSTimesheetLine atgriež **false** laika uzskaites rindas saglabāšanas operācijas laikā, mobilajā programmā tiek parādīts kļūdas ziņojums.
- Ja **validateSubmit** tabulā TSTimesheetTable atgriež **false** laika uzskaites rindas iesniegšanas laikā programmā, lietotājam tiek parādīts kļūdas ziņojums.
- Loģika, kas aizpilda laukus (piemēram, **Rindas rekvizīts**), metodes **insert** laikā tabulā TSTimesheetLine joprojām darbosies.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Iebūvēto lauku paslēpšana un atzīmēšana kā tikai lasāmus, izmantojot konfigurēšanu

Izmantojot projekta parametrus, iebūvētos laukus var padarīt tikai lasāmus vai paslēptus mobilajā programmā. Iestatiet opcijas sadaļā **Mobilās laika uzskaites tabulas** cilnē **Laika uzskaites tabula**, kas atrodas lapā **Projekta pārvaldības un grāmatvedības parametri**.

![Projekta parametri.](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>To darbību mainīšana, kas pieejamas atlasei, izmantojot paplašinājumus

Darbības, kas ir pieejamas projekta atlasei, tiek aizpildītas, izmantojot metodes **getActivitiesForProject()** un **getActivityQuery()** klasē **TsTimesheetProjectService**. Varat izmantot komandu ķēdi, lai mainītu šo uzvedību atbilstoši jūsu biznesa scenārijam attiecībā uz darbībām, kas ir pieejamas atlasīšanai noteiktam projektam.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Noklusējuma projekta kategorijas ievadīšana laika uzskaites tabulas ierakstos

Noklusējuma projekta kategorijas ieraksts laika uzskaites tabulas ierakstos notiek trīs līmeņos. Varat izmantot komandu ķēdi, lai izvērstu uzvedību jebkurā vai visos šajos līmeņos un panāktu nepieciešamo uzvedību. Tiek izmantota tālāk norādītā hierarhija.

1. Programma mēģina ievietot noklusējuma kategoriju no projekta resursa. Šī noklusējuma kategorija ir iestatīta metodēs **getCurrentUserResource** un **getDelegatedResourcesForCurrentUser** klasē **TSTimesheetSettingsService**.
2. Ja noklusējuma kategorija netiek nodrošināta projekta resursu līmenī, programma mēģina to izgūt no projekta darbības. Šī noklusējuma kategorija ir iestatīta metodē **getActivitiesForProject** klasē **TSTimesheetProjectService**.
3. Ja noklusējuma kategorija netiek nodrošināta projekta aktivitātes līmenī, noklusējuma kategorija tiek izgūta no projekta parametriem. Šī noklusējuma kategorija ir iestatīta metodē **getProjectDetailsbyRule** klasē **TSTimesheetProjectService**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]