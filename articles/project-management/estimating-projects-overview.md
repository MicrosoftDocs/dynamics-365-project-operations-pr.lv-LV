---
title: Finanšu aprēķinu koncepcijas
description: Šajā tēmā ir sniegta informācija par finanšu aprēķiniem projektiem programmā Project Operations.
author: rumant
manager: AnnBe
ms.date: 03/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a251be995abddba04cee689714d0a8f4e9d9e7d7
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701745"
---
# <a name="financial-estimation-concepts"></a>Finanšu aprēķinu koncepcijas

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Platformā Dynamics 365 Project Operations varat veidot projektu finanšu aprēķinus divos posmos. 
1. Pirms pārdošanas posmā pirms darījuma iegūšanas. 
2. Izpildes posmā pēc projekta līguma izveides. 

Varat izveidot projekta darba finanšu aprēķinu, izmantojot jebkuru no šīm trīs lapām.
- Lapa **Piedāvājuma rinda**, izmantojot piedāvajuma rindas informāciju.  
- Lapa **Projekta līguma rinda**, izmantojot piedāvājuma rindas informāciju. 
- Lapa **Projekts**, izmantojot ciļņu lapu **Uzdevumi** vai **Izdevumu aprēķini**.

## <a name="use-a-project-quote-to-create-an-estimate"></a>Projekta piedāvājuma izmantošana aprēķina izveidei
Projekta piedāvājumā var izmantot **Piedāvājuma rindas informācijas** entītiju, lai novērtētu darbu, kas nepieciešams projekta nodrošināšanai. Pēc tam šo novērtējumu var koplietot ar klientu.

Projekta piedāvājuma rindām var būt neviena vai daudzas piedāvājuma rindas detaļas. Piedāvājuma rindu detalizētā informācija tiek izmantota, lai novērtētu laiku, izdevumus vai maksas. Microsoft Dynamics 365 Project Operations nenodrošina materiālu aprēķinus piedāvājuma rindas informācijā. Tos sauc par transakciju klasēm. Novērtētās nodokļu summas var ievadīt arī transakciju klasē.

Papildus transakciju klasēm piedāvājuma rindu informācijā ir iekļauts transakcijas tips. Piedāvājuma rindas informācijai tiek atbalstīti divi transakciju veidi: **Izmaksas** un **Projekta līgums**.

## <a name="use-a-project-contract-to-create-an-estimate"></a>Projekta līguma izmantošana aprēķina izveidei

Ja izmantojāt piedāvājumu, kad izveidojāt ar projektiem pamatotu līgumu, tad novērtējums, ko veicāt katrai piedāvājuma rindai, tiek kopēts projekta līgumā. Projekta līguma uzbūve ir tāda pati kā projekta piedāvājuma struktūra, kurā ir rindas, rindu dati un rēķinu grafiki.

Novērtējumus var veikt tieši projekta līgumā, kā tas ir projekta piedāvājumā. Projekta piedāvājumam novērtējumi tiek veikti, izmantojot līguma rindas un informāciju par līgumu rindu. Līguma rindu informāciju var ģenerēt arī no projekta plāna, kas izveidots, izmantojot augšupējo aprēķina metodi.

Līguma rindu detalizētā informācija tiek izmantota, lai novērtētu laiku, izdevumus vai maksas. Novērtētās nodokļu summas var ievadīt arī līguma rindas informācijā.

Līguma rindas informācijā nav atļauti materiālu aprēķini.

## <a name="use-a-project-to-create-an-estimate"></a>Projekta izmantošana aprēķina izveidei 

Projektiem var novērtēt laiku un izdevumus. Project Operations neatbalsta materiālu aprēķinus vai projekta maksas.

Laika novērtējumi tiek ģenerēti, kad izveidojat uzdevumu un identificējat vispārēja resursa atribūtus, kas nepieciešami, lai izpildītu šo uzdevumu. Laika aprēķini tiek ģenerēti, izmantojot grafika uzdevumus. Laika aprēķini netiek izveidoti, ja veidojat vispārējus darba grupas dalībniekus ārpus grafika konteksta.

Izdevumu aprēķini tiek ievadīti lapas **Izdevumu aprēķini** režģī.

Projekta aprēķina izveide tiek uzskatīta par labāko praksi, jo varat veidot detalizētus darba vai laika aprēķinus un izdevumus par katru projekta plāna uzdevumu. Pēc tam šo detalizēto aprēķinu var izmantot, lai izveidotu aprēķinus katrai piedāvājuma rindai un izveidotu klientam vēl lielāku uzkrāšanās vērtējumu. Importējot vai izveidojot detalizētu aprēķinu piedāvājuma rindā, izmantojot projekta plānu, Project Operations importē šo aprēķinu pārdošanas vērtības un izmaksu vērtības. Pēc importēšanas projekta piedāvājumā varat apskatīt peļņas, peļņas, starpības un iespējamības rādītājus.

## <a name="understanding-estimates"></a>Izpratne par novērtējumu

Izmantojiet šo tabulu kā ceļvedi, lai izprastu biznesa loģiku aprēķinu fāzē.

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
