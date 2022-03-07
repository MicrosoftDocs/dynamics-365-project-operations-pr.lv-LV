---
title: Projekta izdevumu pārskats
description: Šajā tēmā ir sniegta informācija par novērtējumiem risinājumā Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4ff73c6efd5b21b91a7772c3733734d8008e00a3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286887"
---
# <a name="estimate-projects-overview"></a>Projekta izdevumu pārskats

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Projekta piedāvājumā var izmantot **Piedāvājuma rindas informācijas** entītiju, lai novērtētu darbu, kas nepieciešams projekta nodrošināšanai. Pēc tam šo novērtējumu var koplietot ar klientu.

Projekta piedāvājuma rindām var būt neviena vai daudzas piedāvājuma rindas detaļas. Piedāvājuma rindu detalizētā informācija tiek izmantota, lai novērtētu laiku, izdevumus vai maksas. Microsoft Dynamics 365 Project Operations nenodrošina materiālu aprēķinus piedāvājuma rindas informācijā. Tos sauc par transakciju klasēm. Novērtētās nodokļu summas var ievadīt arī transakciju klasē.

Papildus transakciju klasēm piedāvājuma rindu informācijā ir iekļauts transakcijas tips. Piedāvājuma rindas informācijai tiek atbalstīti divi transakciju veidi: **Izmaksas** un **Projekta līgums**.

## <a name="estimate-by-using-a-contract"></a>Novērtējums, izmantojot līgumu

Ja izmantojāt piedāvājumu, kad izveidojāt ar projektiem pamatotu līgumu, tad novērtējums, ko veicāt katrai piedāvājuma rindai, tiek kopēts projekta līgumā. Projekta līguma uzbūve ir tāda pati kā projekta piedāvājuma struktūra, kurā ir rindas, rindu dati un rēķinu grafiki.

Novērtējumus var veikt tieši projekta līgumā, kā tas ir projekta piedāvājumā. Projekta piedāvājumam novērtējumi tiek veikti, izmantojot līguma rindas un informāciju par līgumu rindu. Līguma rindu informāciju var ģenerēt arī no projekta plāna, kas izveidots, izmantojot augšupējo aprēķina metodi.

Līguma rindu detalizētā informācija tiek izmantota, lai novērtētu laiku, izdevumus vai maksas. Novērtētās nodokļu summas var ievadīt arī līguma rindas informācijā.

Līguma rindas informācijā nav atļauti materiālu aprēķini.

Ar projekta līgumu atbalstītie procesi ir rēķinu izveide un apstiprināšana. Rēķina izveide veido projekta rēķina melnrakstu, kurā ir iekļauti visi nepārdotie pārdošanas darījumi, līdz pašreizējam datumam.

Apstiprināšana padara līgumu par tikai lasāmu un maina tā statusu no **Melnraksts** uz **Apstiprināts**. Pēc šīs darbības veikšanas to nevar atsaukt. Tā kā šī darbība ir neatgriezeniska, ieteicams līgumu uzturēt statusā **Melnraksts**.

Vienīgā atšķirība starp līgumu projektiem un apstiprinātajiem līgumiem ir to statuss un tas, ka līgumu melnrakstus var rediģēt, taču apstiprinātos līgumus nevar. Rēķinu izveidi un izsekošanu faktiski var veikt gan līgumu projektiem, gan apstiprinātajiem līgumiem.

Project Operations neatbalsta līgumu vai projektu pasūtījumu maiņu.

## <a name="estimating-projects"></a>Projektu novērtēšana

Projektiem var novērtēt laiku un izdevumus. Project Operations neļauj aprēķināt projektu materiālus vai maksas.

Laika novērtējumi tiek ģenerēti, kad izveidojat uzdevumu un identificējat vispārēja resursa atribūtus, kas nepieciešami, lai izpildītu šo uzdevumu. Laika aprēķini tiek ģenerēti, izmantojot grafika uzdevumus. Laika aprēķini netiek izveidoti, ja veidojat vispārējus darba grupas dalībniekus ārpus grafika konteksta.

Izmaksu novērtējumi tiek ievadīti lapas **Novērtējumi** režģī.

## <a name="understanding-estimation"></a>Izpratne par novērtējumu

Izmantojiet šo tabulu kā ceļvedi, lai izprastu biznesa loģiku novērtēšanas fāzē.

| Scenārijs                                                                                                                                                                                                                                                                                                                                          | Entītijas ieraksts                                                                                                                                                                                                       | Transakcijas tips | Transakcijas klase | Papildinformācija                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Ja ir jānovērtē piedāvājuma laika pārdošanas vērtība piedāvājumā                                                                                                                                                                                                                                                                                    | Piedāvājuma rindas informācijas (QLD) ieraksts ir izveidots                                                                                                                                                                               | Projekta līgums | Time        | Pārdošanas puses lauks transakcijas sākumpunkts norāda izmaksu puses QLD |
|                                                                                                                                                                                                                                                                                     | Sistēmā tiek izveidots otrs QLD ieraksts, lai saglabātu atbilstošās izmaksu vērtības. Visus beznaudas laukus sistēma kopē no pārdošanas QLD uz izmaksu QLD.                                                                                                                                                                               | Izmaksas | Time        | Pārdošanas puses lauks transakciju sākumpunkts (QLD) norāda izmaksu puses QLD |
| Ja jānovērtē līgumā norādītā laika pārdošanas vērtība                                                                                                                                                                                                                                                                                 | Piedāvājuma rindas informācijas (CLD) ieraksts ir izveidots                                                                                                                                                                    | Projekta līgums | Time        | Pārdošanas puses lauks Transakciju sākumpunkts norāda izmaksu puses CLD      |
|                                                                                                                                                                                                                                                                                  | Sistēmā tiek izveidots otrs CLD ieraksts, lai saglabātu atbilstošās izmaksu vērtības. Visus beznaudas laukus sistēma kopē no pārdošanas CLD uz izmaksu CLD.                                                                                                                                                                    | Izmaksas | Time        | Pārdošanas puses lauks Transakciju sākumpunkts norāda izmaksu puses CLD      |
| Ja lietotājs projekta uzdevumam apraksta resursu                                                                                                                                                                                                                                                                                            | Ja uzdevums ir izveidots ar visām nepieciešamajām pārdošanas dimensijām, tiek izveidots uzdevuma pārdošanas vērtības ieraksta novērtējuma rindas ieraksts. Lomas un organizācijas vienības ir cenu noteikšanas dimensijas | Projekta līgums | Laiks        |                                                                                   |
|     | Ja uzdevums ir izveidots ar visām nepieciešamajām cenu dimensijām, tiek izveidots uzdevuma pārdošanas vērtības ieraksta novērtējuma rindas ieraksts. Visus beznaudas laukus sistēma kopē no pārdošanas novērtējuma rindas uz izmaksu novērtējuma rindu. Lomas un organizācijas vienība ir cenu noteikšanas dimensijas gan izmaksu, gan rēķinu likmēm.                                                                                                                                                                                                                | izdevumi             | Laiks           |                                                                                   |



## <a name="customize-the-quote-line-detail-and-contract-line-detail-entities"></a>Piedāvājuma rindas informācijas un līgumu rindu informācijas entītiju pielāgošana

Ja pievienojāt pielāgotu lauku piedāvājuma rindu informācijai un vēlaties, lai sistēma lauka vērtību ievadītu kā noklusējuma vērtību saistītajā izmaksu rindā, ko tā izveido, izmantojiet spraudņa **PreOperationContractLineDetailUpdate** un **PreOperationQuoteLineDetailUpdate** reģistrēšanas rīkus. Šie spraudņi ir jāreģistrē atkārtoti pēc tam, kad ir mainīta piedāvājuma rindas informācija vai līguma rindu informācija. Lai pabeigtu procesu, rīkojieties šādi:

1. Atveriet PluginRegistrationTool un izveidojiet savienojumu ar tiešsaistes instanci.
2. Atlasiet vienumu **Meklēt** un meklējiet spraudni, lai veiktu atjaunināšanu.
3. Atlasiet spraudni un pēc tam galvenajā lapā noklikšķiniet vienumu **Atlasīt**.
4. Atlasiet spraudņa darbību, lai atjauninātu, ar peles labo pogu noklikšķiniet un pēc tam atlasiet vienumu **Atjaunināt**.
5. Dialoglodziņa **Esošas darbības atjaunināšana** laukā **Filtrēšanas atribūti** atlasiet vienumu atlasiet daudzpunktes pogu (**...**):
6. Dialoglodziņā **Atribūtu atlase** atzīmējiet pielāgotu atribūtu izvēles rūtiņas.
7. Noklikšķiniet uz vienuma **Labi**, lai aizvērtu dialoglodziņu, un pēc tam uz **Atjaunināt darbību**.
8. Otrajā spraudnī atkārtojiet 1.–7. darbību.
9. Aizveriet **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]