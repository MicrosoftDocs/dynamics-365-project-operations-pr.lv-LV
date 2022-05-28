---
title: Novērtējumi
description: Šajā tēmā ir sniegta informācija par novērtējumiem risinājumā Dynamics 365 Project Service Automation.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 1/31/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 978af25fb89feb61e3c6fcfeafa212db034ff5cb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590677"
---
# <a name="estimates"></a>Novērtējumi

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projekta piedāvājumā var izmantot piedāvājuma rindas detalizēto entītiju, lai novērtētu darbu, kas nepieciešams projekta nodrošināšanai. Pēc tam šo novērtējumu var koplietot ar klientu.

Piedāvājuma rindām, kuru pamatā ir projekti, nav jābūt piedāvājuma rindu detalizētai informācijai. Vai arī viņiem var būt daudz piedāvājumu rindu detalizētās informācijas. Piedāvājuma rindu detalizētā informācija tiek izmantota, lai novērtētu laiku, izdevumus vai maksas. PSA nenodrošina materiālu aprēķinus piedāvājuma rindas informācijā. Tos sauc par transakciju klasēm. Novērtētās nodokļu summas var ievadīt arī transakciju klasē.

Papildus transakciju klasēm piedāvājuma rindu informācijā ir iekļauts transakcijas tips. PSA atbalsts piedāvājuma rindu detalizētajai informācijai ir divi transakciju tipi: **Izmaksas** un **Projekta līgums**.

## <a name="estimate-by-using-a-contract"></a>Novērtējums, izmantojot līgumu

Ja izmantojāt PSA piedāvājumu, kad izveidojāt ar projektiem pamatotu līgumu, tad novērtējums, ko veicāt katrai piedāvājuma rindai, tiek kopēts projekta līgumā. Projekta līguma uzbūve ir tāda pati kā projekta piedāvājuma struktūra, kurā ir rindas, rindu dati un rēķinu grafiki.

Novērtējumus var veikt tieši projekta līgumā, kā tas ir projekta piedāvājumā. Projekta piedāvājumam novērtējumi tiek veikti, izmantojot līguma rindas un informāciju par līgumu rindu. Līguma rindu informāciju var ģenerēt arī no projekta plāna, kas izveidots, izmantojot augšupējo aprēķina metodi.

Līguma rindu detalizētā informācija tiek izmantota, lai novērtētu laiku, izdevumus vai maksas. Novērtētās nodokļu summas var ievadīt arī līguma rindas informācijā.

PSA nenodrošina materiālu aprēķinus lguma rindas informācijā.

Ar projekta līgumu atbalstītie procesi ir rēķinu izveide un apstiprināšana. Rēķina izveide veido projekta rēķina melnrakstu, kurā ir iekļauti visi nepārdotie pārdošanas darījumi, līdz pašreizējam datumam.

Apstiprināšana padara līgumu par tikai lasāmu un maina tā statusu no **Melnraksts** uz **Apstiprināts**. Pēc šīs darbības veikšanas to nevar atsaukt. Tā kā šī darbība ir neatgriezeniska, ieteicams līgumu uzturēt statusā **Melnraksts**.

Vienīgā atšķirība starp līgumu projektiem un apstiprinātajiem līgumiem ir to statuss un tas, ka līgumu melnrakstus var rediģēt, taču apstiprinātos līgumus nevar. Rēķinu izveidi un izsekošanu faktiski var veikt gan līgumu projektiem, gan apstiprinātajiem līgumiem.

PSA neatbalsta līgumu vai projektu pasūtījuma maiņu.

## <a name="estimating-projects"></a>Projektu novērtēšana

Projektiem var novērtēt laiku un izdevumus. PSA neļauj aprēķināt materiālu vai maksu par projektiem.

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
| Ja lietotājs projekta uzdevumam apraksta resursu                                                                                                                                                                                                                                                                                            | Ja uzdevums ir izveidots ar visām nepieciešamajām pārdošanas dimensijām, tiek izveidots uzdevuma pārdošanas vērtības ieraksta novērtējuma rindas ieraksts. Lomas un organizācijas vienības ir OOB Project Service cenu noteikšanas dimensijas | Projekta līgums | Time        |                                                                                   |
|     | Ja uzdevums ir izveidots ar visām nepieciešamajām cenu dimensijām, tiek izveidots uzdevuma pārdošanas vērtības ieraksta novērtējuma rindas ieraksts. Visus beznaudas laukus sistēma kopē no pārdošanas novērtējuma rindas uz izmaksu novērtējuma rindu. Lomas un organizācijas vienība ir OOB PSA cenu noteikšanas dimensijas gan izmaksu, gan rēķinu likmēm.                                                                                                                                                                                                                | Izmaksas             | Time           |                                                                                   |



## <a name="customizing-the-quote-line-detail-and-contract-line-detail-entities"></a>Piedāvājuma rindas informācijas un līgumu rindu informācijas entītiju pielāgošana

Ja pievienojāt pielāgotu lauku piedāvājuma rindu informācijai un vēlaties, lai sistēma lauka vērtību ievadītu kā noklusējuma vērtību saistītajā izmaksu rindā, ko tā izveido, izmantojiet spraudņa PreOperationContractLineDetailUpdate un PreOperationQuoteLineDetailUpdate reģistrēšanas rīkus. Šie spraudņi ir jāreģistrē atkārtoti pēc tam, kad ir mainīta piedāvājuma rindas informācija vai līguma rindu informācija. Lai pabeigtu procesu, rīkojieties šādi:

1. Atveriet PluginRegistrationTool un izveidojiet savienojumu ar tiešsaistes instanci.
2. Atlasiet vienumu **Meklēt** un meklējiet spraudni, lai veiktu atjaunināšanu.

    ![Dialoglodziņš Meklēšanas koks.](media/basic-guide-19.png)

3. Atlasiet spraudni un pēc tam galvenajā lapā atlasiet vienumu **Atlasīt.**
4. Atlasiet spraudņa darbību, lai atjauninātu, ar peles labo pogu noklikšķiniet un pēc tam atlasiet vienumu **Atjaunināt**.

    ![Darbību atlase spraudnī.](media/basic-guide-20.png)

5. Dialoglodziņa **Esošas darbības atjaunināšana** laukā **Filtrēšanas atribūti** atlasiet vienumu atlasiet daudzpunktes pogu (**...**):
 
    ![Dialoglodziņš Esošās darbības atjaunināšana.](media/basic-guide-21.png)

6. Dialoglodziņā **Atribūtu atlase** atzīmējiet pielāgotu atribūtu izvēles rūtiņas.

    ![Dialoglodziņš Atribūtu atlase.](media/basic-guide-22.png)

7. Noklikšķiniet uz vienuma **Labi**, lai aizvērtu dialoglodziņu, un pēc tam uz **Atjaunināt darbību**.
 
    ![Darbības atjaunināšanas poga.](media/basic-guide-23.png)

8. Otrajā spraudnī atkārtojiet 1.–7. darbību.
9. Aizveriet PluginRegistrationTool.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
