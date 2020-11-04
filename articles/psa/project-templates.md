---
title: Projektu veidnes
description: Šajā tēmā ir sniegta informācija par to, kā ātrai projekta iestatīšanai var izmantot projektu veidnes.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 1bb82a312114e9814f5ce65a1698455582fd252e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080606"
---
# <a name="project-templates"></a>Projektu veidnes 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projekta veidne ir iepriekš definēta struktūra, kas palīdz ātri un ērti uzsākt projektu. Iepriekš definētu veidni varat izmantot, lai jaunu projektu izveidotu ar vienu klikšķi. Attiecībā uz projektiem jums ir jādefinē projektu veidņu priekšnosacījumi. Katrai projekta veidnei jums ir jādefinē projekta kalendārs, un organizācijā ir jābūt iepriekš definētām lomām un cenrāžiem, lai veidnes komponentiem būtu noderīgi dati.

Projekta veidne sastāv no trīs komponentiem: grafika, projekta tāmēm un projekta darba grupas dalībniekiem.

## <a name="schedule"></a>Plānot

Grafikam projekta veidnē ir tāda pati elementu kopa kā grafikam projektā. Varat izveidot uzdevumu hierarhiju, saistīt lomas uzdevumiem, noteikt grafika atribūtus un iestatīt atkarības. Grafiks projekta veidnē atbalsta arī uzdevumu režīmus katram uzdevumam. Līdz ar to tas atbalsta plānošanas programmu. Jums ir nepieciešams projektu sasaistīt ar kādu projekta kalendāru. Kad veidojat darbu grafiku, nav nekādas atšķirības starp projekta veidni un projektu.

## <a name="project-estimates"></a>Projekta tāmes

Projekta tāmes projekta veidnē darbojas tāpat kā projekta tāmes projektā. Taču izmaksu un pārdošanas cenas tiek izgūtas no noklusējuma izmaksu un pārdošanas cenrāžiem, kas ir definēti parametros.

## <a name="creating-a-project-from-a-template"></a>Projekta izveidošana no veidnes
 
Projektu var izveidot no projekta veidnes vairākos tālāk norādītajos veidos.

- Kad veidojat projektu no piedāvājuma, varat atlasīt projekta veidni dialoglodziņā **Ātrā izveide: Projekts**.

> ![Dialoglodziņš Ātrā izveide: Projekts](media/project-11.png)

- Kad projektu veidojat, atlasot vienumu **Jauns projekts** , pirms ieraksta saglabāšanas tiek parādīta lapa **Projekts**. Laukā **Izvēlēties veidni** atlasiet vienu no organizācijā esošajām iepriekš definētajām veidnēm.
- Izmantojiet vienumu **Izveidot projektu no veidnes** lapā **Veidnes entītija**.

## <a name="copying-components-of-template-to-project"></a>Veidnes komponentu kopēšana uz projektu

Kad projekta veidnes komponentus kopējat uz projektu, atkarībā no projektā izmantotajiem iestatījumiem var rasties dažas pārlabošanas.

### <a name="copying-the-schedule"></a>Grafika kopēšana

Kad grafiku kopējat no projekta veidnes, ja projektam ir citāds projekta kalendārs nekā veidnei, uzdevumu grafikam tiek izmantotas darba stundas no projekta kalendāra. Šādi grafiks tiek pielāgots atbalstoši pamatā izmantotajam projekta kalendāram. Līdzīgi arī pirmajam uzdevumam grafikā tiek izmantots projekta sākuma datums, bet pārējās hierarhijas grafiks tiek atjaunināts, pamatojoties uz veidnē norādīto ilgumu un atkarībām. 

### <a name="copying-project-estimates"></a>Projekta tāmju kopēšana 

Kad kopēšanu veicat starp projekta tāmju rindām, cenrāži tiek atjaunināti. Izmaksu cenrādim šie atjauninājumi ir balstīti uz projekta īpašnieka struktūrvienību. Pārdošanas cenrādim tie ir balstīti uz klientu. Projektiem, kas ir saistīti ar pārdošanas entītiju, vienības izmaksu un pārdošanas cenas tiek noteiktas, pamatojoties uz šiem cenrāžiem.

### <a name="copying-a-project-team"></a>Projekta darba grupas kopēšana

Kad projekta darba grupa tiek kopēta no projekta veidnes uz projektu, tiek kopēti vispārējie resursi kopā ar veidnē definētajām prasmēm un kvalifikācijām. Arī vispārējo resursu piešķires tiek paturētas tādas, kādas tās bija projekta veidnē. Nosauktie resursi projektu veidnēs netiek atbalstīti.
