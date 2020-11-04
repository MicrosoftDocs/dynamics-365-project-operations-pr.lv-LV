---
title: Starpuzņēmumu rēķinu izrakstīšana
description: Šajā rakstā ir sniegta informācija un piemēri saistībā ar starpuzņēmumu rēķinu izrakstīšanu projektiem.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4604708dbd7c835c8df1cf48f67e645952f49774
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080470"
---
# <a name="intercompany-invoicing"></a>Starpuzņēmumu rēķinu izrakstīšana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija un piemēri saistībā ar starpuzņēmumu rēķinu izrakstīšanu projektiem.

Jūsu organizācijā var būt vairākas nodaļas, meitasuzņēmumi un citas juridiskas personas, kas pārsūta produktus un pakalpojumus cita citai projektu ietvaros. Juridiskā persona, kas nodrošina pakalpojumu vai produktu, tiek saukta par *aizdodošo juridisko personu* , un juridiskā persona, kas saņem pakalpojumu vai produktu, tiek saukta par *aizņemošo juridisko personu*. 

Šajā ilustrācijā ir parādīts tipisks scenārijs, kurā divas juridiskas personas, SI FR (aizņemošā juridiskā persona) un SI USA (aizdodošā juridiskā persona) koplieto resursus, lai izpildītu klientam A projektu. Šajā scenārijā uzņēmums SI FR ir nolīgts, lai izpildītu darbu klienta A labā. 

[![Starpuzņēmumu rēķinu izrakstīšanas piemērs](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

Mērķis ir padarīt izmaksu kontroli, ieņēmumu atzīšanu, nodokļu pārvaldību un pārdošanas cenu starpuzņēmumu projekta transakcijām elastīgāku un efektīvāku. Turklāt ir pieejamas tālāk norādītās iespējas.

-   Klientu rēķinu izveidošana par projektiem pie aizņemošās juridiskās personas, izmantojot starpuzņēmumu laika uzskaites tabulas, izdevumus un piegādātāju rēķinus no aizdodošās juridiskās personas.
-   Nodokļu aprēķinu un netiešo izmaksu atbalsts.
-   Ieņēmumu atzīšanas atlikšana aizdodošajai juridiskajai personai un ja aizņemošajai juridiskajai personai ir jāatzīst izmaksas.
-   Uzkrājiet nepabeigtā darba (WIP) ieņēmumus aizdodošajā juridiskajā personā.
-   Iestatiet pārsūtīšanas cenas, kuru pamatā var būt dažādi cenu noteikšanas modeļi. Lūk, daži piemēri:
    -   **Daudzums**  — summa, ko ievadāt laukā **Cenas noteikšana** , ir faktiskās izmaksas par daudzumu vai vienību.
    -   **Izmaksu summa**  — cenas/izmaksas par transakciju un izmaksu summa, ko ievadāt laukā **Cenas noteikšana**.
    -   **Izmaksu procentuālā daļa**  — pārsūtīšanas cena ir cena/izmaksas par transakciju, kas reizinātas ar izmaksu procentuālo daļu, ko ievadāt laukā **Cenu noteikšana**.
    -   **Pārdošanas cenas procentuālā daļa**  — tās pārdošanas cenas procentuālā daļa, kas tiek pārsūtīta aizdodošajai juridiskajai personai.
    -   **Summa zem pārdošanas cenas**  — summa, ko aizņemošā juridiskā persona aiztur no pārdošanas cenas pirms pārskaitīšanas aizdodošajai juridiskajai personai.
    -   **Seguma summas likme**  — skaitlis, ko ievadāt laukā **Cenas noteikšana** , ir seguma summas likme, kas ir izteikta procentos no pārdošanas cenas.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>1. piemērs: parametru iestatīšana starpuzņēmumu rēķinu izrakstīšanai
Šajā piemērā USSI ir aizdodošā juridiskā persona, un tās resursi ir atskaišu izveides laiks attiecībā pret aizņemošo juridisku personu, FRSI, kam pieder līgums ar gala klientu. Stundas un izdevumi, par ko USSI darbinieku atskaiti var iekļaut projekta rēķinā, ko ģenerē FRSI. Turklāt pastāv arī trešais transakciju avots, kas var nākt no aizdodošās juridiskās personas (USSI šajā piemērā), kad tas nodrošina dalītus piegādātāju pakalpojumus meitasuzņēmumiem (piemēram, FRSI) un pēc tam nodod šīs izmaksas projektiem šajos meitasuzņēmumos. Visus atbilstošos rēķinu dokumentus un nodokļu aprēķinus pabeidz risinājums Finance. 

Šajā piemērā FRSI ir jābūt klientam USSI juridiskajā personā, un USSI jābūt pakalpojumu sniedzējam FRSI juridiskajā personā. Pēc tam varat iestatīt starpuzņēmumu attiecības starp abām juridiskajām personām. Nākamajā procedūrā ir parādīts, kā iestatīt parametrus, lai abas juridiskās personas varētu piedalīties starpuzņēmumu rēķinu izrakstīšanā.

1. Iestatiet FRSI kā klientu USSI juridiskajā personā un iestatiet USSI kā pakalpojumu sniedzēju FRSI juridiskajā personā. Šim uzdevumam nepieciešamajām darbībām ir trīs ievades punkti.

   | Darbība |                                                       Ievades punkts                                                        |                                                                                                                                                                                               Apraksts                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  A   | USSI noklikšķiniet uz <strong>Debitori</strong> &gt; <strong>Klienti</strong> &gt; <strong>Visi klienti</strong>. |                                                                                                                                                                  Izveidojiet jaunu klienta ierakstu FRSI un atlasiet klientu grupu.                                                                                                                                                                  |
   |  T   |    FRSI noklikšķiniet uz <strong>Kreditori</strong> &gt; <strong>Piegādātāji</strong> &gt; <strong>Visi piegādātāji</strong>.     |                                                                                                                                                                    Izveidojiet jaunu piegādātāja ierakstu USSI un atlasiet piegādātāju grupu.                                                                                                                                                                    |
   |  C   |                                  FRSI atveriet tikko izveidoto piegādātāja ierakstu.                                  | Darbību rūts cilnes <strong>Vispārīgi</strong> grupā <strong>Iestatīšana</strong> noklikšķiniet uz <strong>Starpuzņēmumu</strong>. Lapas <strong>Starpuzņēmumu</strong> cilnē <strong>Tirdzniecības attiecības</strong> iestatiet slīdni <strong>Aktīvas</strong> uz <strong>Jā</strong>. Laukā <strong>Klienta uzņēmums</strong> atlasiet klienta ierakstu, ko izveidojāt A darbībā. |


2. Noklikšķiniet uz **Projektu pārvaldība un grāmatvedība** &gt; **Iestatīšana** &gt; **Projektu pārvaldības uzskaites parametri** un pēc tam noklikšķiniet uz cilnes **Starpuzņēmumu**. Parametru iestatīšanas veids ir atkarīgs no tā, vai jūs esat aizņemošā juridiskā persona vai aizdodošā juridiskā persona.
   -   Ja jūs esat aizņemošā juridiskā persona, atlasiet sagādes kategoriju, kas jāizmanto, lai atbilstu piegādātāju rēķiniem, kas tiek ģenerēti automātiski.
   -   Ja esat aizdodošā juridiskā persona, katrai aizņemošajai personai atlasiet noklusējuma projekta kategoriju katram transakcijas tipam. Projekta kategorijas tiek izmantotas nodokļu konfigurēšanai, ja starpuzņēmumu transakcijās iekļautā kategorija, par kuru izrakstīts rēķins, pastāv tikai aizņemošajā juridiskajā personā. Varat izvēlēties, vai jāuzkrāj ieņēmumi no starpuzņēmumu transakcijām. Šī uzkrāšana tiek veikta, grāmatojot transakcijas, un pēc tam, kad ir iegrāmatots starpuzņēmumu rēķins, tā tiek atsaukta.

3. Noklikšķiniet uz **Projekta pārvaldība un grāmatvedība** &gt; **Iestatīšana** &gt; **Cenas noteikšana** &gt; **Pārsūtīšanas cena**.
4. Atlasiet valūtu, transakcijas tipu un pārsūtīšanas cenas modeli. Rēķinā izmantojamā valūta ir valūta, kas tiek konfigurēta aizņemošās juridiskās personas klienta ierakstā aizdodošajā juridiskajā personā. Valūta tiek izmantota, lai salīdzinātu ierakstus pārsūtīšanas cenu tabulā.
5. Noklikšķiniet uz **Virsgrāmata** &gt; **Publicēšanas iestatīšana** &gt; **Starpuzņēmumu uzskaite** un iestatiet USSI un FRSI attiecības.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>2. piemērs: starpuzņēmumu laika uzskaites tabulas izveide un publicēšana
USSI, aizdodošajai juridiskajai personai ir jāizveido un jāpublicē projekta laika uzskaites tabula no FRSI, aizņemošās juridiskās personas. Šim uzdevumam nepieciešamajām darbībām ir divi ievades punkti.

| Darbība | Ievades punkts                                                                       | Apraksts                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Projekta vadība un grāmatvedība** &gt; **Laika uzskaites tabulas** &gt; **Visas laika uzskaites tabulas** | Izveidojiet jaunu laika uzskaites tabulu. Laika uzskaites tabulas rindas laukā **Juridiskā persona** atlasiet **FRSI**. Laukā **Projekta ID** atlasiet projektu FRSI. Ievadiet stundas katrai nedēļas dienai. |
| T    | Lapa **Laika uzskaties tabula**                                                                | Pēc darbplūsmas izpildes publicējiet laika uzskaites tabulu un norādiet dokumenta numuru.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>3. piemērs: starpuzņēmumu piegādātāja rēķina izveide un publicēšana
USSI, aizdodošajai juridiskajai personai, ir jāizveido un jāpublicē starpuzņēmumu piegādātāja rēķins no FRSI, aizņemošās juridiskās personas. Šis piegādātāja rēķins atspoguļo ārpakalpojuma darbu un izdevumus, ko veica piegādātāji, kuriem maksā USSI. Šim uzdevumam nepieciešamajām darbībām ir divi ievades punkti.

| Darbība | Ievades punkts                                                                                      | Apraksts                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Kreditori** &gt; **Rēķini** &gt; **Atvērt piegādātāju rēķinus** &gt; **Jauns piegādātāja rēķins** | Izveidojiet jaunu piegādātāja rēķinu un ievadiet pakalpojumus, kas tika iepirkti FRSI projekta vārdā.                                                                                                                                                                                  |
| T    | Lapa **Piegādātāja rēķins**                                                                      | Ievadiet rindas, kas atspoguļo ārpakalpojumu pakalpojumus FRSI vārdā. FastTab cilnes **Rindas detaļas** rēķina rindas cilnē **Projekts** , laukā **Projekta uzņēmums** ievadiet **FRSI**. Ievadiet projektu un atbilstošo informāciju. Pēc tam publicējiet piegādātāja rēķinu. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>4. piemērs: starpuzņēmumu rēķina izveide un publicēšana
USSI, aizdodošajai juridiskajai personai ir jāizveido un jāpublicē starpuzņēmumu rēķins. Šim uzdevumam nepieciešamajām darbībām ir divi ievades punkti.

| Darbība | Ievades punkts                                                                                             | Apraksts                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Projektu pārvaldība un grāmatvedība** &gt; **Projekta rēķini** &gt; **Starpuzņēmumu klienta rēķins**  | Noklikšķiniet uz **Jauns** , lai atvērtu lapu **Izveidot starpuzņēmumu rēķinu**.                                                                                  |
| T    | **Projektu pārvaldība un grāmatvedība** &gt; **Projekta rēķini** &gt; **Starpuzņēmumu klientu rēķini** | Lapā **Izveidot starpuzņēmumu rēķinu** ievadiet juridisko personu, norādiet darbību, kas ir jāiekļauj, un pēc tam noklikšķiniet uz **Meklēt**. |
| C    | **Projektu pārvaldība un grāmatvedība** &gt; **Projekta rēķini** &gt; **Starpuzņēmumu klientu rēķini** | Atlasiet rēķinā iekļaujamās transakcijas vai noklikšķiniet **Atlasīt visu** , lai publicētu visas sarakstā iekļautās transakcijas, un pēc tam noklikšķiniet uz **Labi**.                  |
| D    | Lapa **Starpuzņēmumu rēķins**                                                                       | Tiek parādīts starpuzņēmumu klienta rēķina priekšlikums.                                                                                             |
| E    | Lapa **Starpuzņēmumu rēķins**                                                                       | Noklikšķiniet uz **Publicēt**.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>5. piemērs: piegādātāja rēķina publicēšana un rēķina izrakstīšana klientam
Ja aizdodošā juridiskā persona, USSI, iegrāmato starpuzņēmumu klienta rēķinu, aizņemošajā juridiskajā personā, FRSI, tiek izveidots atbilstošs gaidošs piegādātāja rēķins. Pēc tam, kad šis kreditora rēķins ir publicēts, FRSI arī izraksta rēķinu projekta klientam par USSI ievadītajām stundām. Šim uzdevumam nepieciešamajām darbībām ir trīs ievades punkti.

| Darbība | Ievades punkts                                                                                        | Apraksts                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A    | **Kreditori** &gt; **Rēķini** &gt; **Gaidoši piegādātāju rēķini**                            | Pārskatiet rēķinu, lai pārbaudītu, vai ir ietvertas laika uzskaites tabulas vērtības, un pēc publicējiet piegādātāja rēķinu.                  |
| T    | **Projektu pārvaldība un grāmatvedība** &gt; **Projekta rēķini** &gt; **Projektu rēķinu priekšlikumi** | Izveidojiet jaunu projekta rēķina projektu un pārbaudiet, vai tiek rādītas publicētās stundu transakcijas.            |
| C    | Lapa **Projekta rēķins**                                                                       | Atlasiet projekta rēķinu un pēc tam noklikšķiniet uz **Skatīt detalizētu informāciju** , lai pārskatītu izmaksu un pārdošanas summu. Pēc tam publicējiet rēķinu. |


Papildinformāciju skatiet sadaļā [Starpuzņēmumu projektu rēķinu izrakstīšanas konfigurēšana](tasks/configure-intercompany-project-invoicing.md).


