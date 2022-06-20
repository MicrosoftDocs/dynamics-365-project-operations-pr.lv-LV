---
title: Apsvērumi par jaunināšanu — Microsoft Dynamics 365 Project Service Automation 2.x vai versija 1.x uz 3. versiju
description: Šajā rakstā ir sniegta informācija par apsvērumiem, kas jāveic, jauninot no Project Service Automation versijas 2.x vai 1.x uz 3. versiju.
ms.prod: ''
ms.custom:
- dyn365-projectservice
ms.date: 11/13/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 3f67b2fe39c9d0224207e7c655892318ec7e09b8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918919"
---
# <a name="upgrade-considerations---psa-version-2x-or-1x-to-version-3"></a>Jaunināšanas apsvērumi – no PSA versijas 2.x vai 1.x uz versiju 3.x

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="project-service-automation-and-field-service"></a>Project Service Automation un Field Service
Gan Dynamics 365 Project Service Automation, gan Dynamics 365 Field Service izmanto vispārējo resursu plānošanas (URS) plānošanas risinājumu, kas paredzēts resursu plānošanai. Ja jūsu instancē ir Project Service Automation un Field Service, atjauniniet abus risinājumus uz jaunāko versiju. Programmai Project Service Automation tā ir versija 3.x. Programmai Field Service tā ir versija 8.x. Atjauninot Project Service Automation vai Field Service, tiks instalēta jaunākā URS versija. Ja gan Project Service Automation, gan Field Service risinājumi vienā un tajā pašā instancē netiek atjaunināti uz jaunāko versiju, var notikt neatbilstošas darbības.

## <a name="resource-assignments"></a>Resursu piešķīrumi
Project Service Automation 2. un 1. versijā uzdevumu piešķires tika glabātas kā pakārtotie uzdevumi (saukti arī par rindas uzdevumiem) **Uzdevuma entītijā** un netieši bija saistīti ar **Resursa piešķires** entītiju. Rindas uzdevums bija redzams piešķires uznirstošajā logā darba sadalījuma struktūrā (WBS).

![Rindas uzdevumi risinājumā WBS Project Service Automation 2. versijā un 1. versijā.](media/upgrade-line-task-01.png)

Project Service Automation 3. versijā ir mainījusies pamatshēma rezervējamo resursu piešķiršanai uzdevumiem. Rindas uzdevums ir novecojis un pastāv tieša 1:1 attiecība starp uzdevumu **Uzdevuma entītijā** un darba grupas dalībnieku **Resursu piešķiršanas** entītijā. Projekta darba grupas dalībniekam piešķirtie uzdevumi tagad tiek glabāti tieši Resursu piešķiršanas entītijā.  

Šīs izmaiņas ietekmē tādu esošu projektu jaunināšanu, kuriem ir resursu piešķires norādītajiem rezervējamiem resursiem un vispārēji resursi projekta darba grupai. Šajā rakstā ir sniegti apsvērumi, kas jums būs jāņem vērā projektos, jauninot uz 3. versiju. 

### <a name="tasks-assigned-to-named-resources"></a>Norādītajiem resursiem piešķirtie uzdevumi
Izmantojot pamatā esošo uzdevuma entītiju, uzdevumi 2. un 1. versijā ļāva darba grupas dalībniekiem parādīt citādāku lomu, kas nav pēc noklusējuma definētā loma. Piemēram, Dace Krēsliņa, kura pēc noklusējuma ir nozīmēta Programmu pārvaldnieka lomai, var tikt nozīmēts uzdevumam ar Izstrādātāja lomu. 3. versijā, nosaukta darba grupas dalībnieka loma vienmēr ir noklusējuma loma, tāpēc jebkurš uzdevums, kam Dace Krēsliņa ir norīkota, izmanto Daces Programmu pārvaldnieka noklusējuma lomu.

Ja esat nozīmējis resursu uzdevumam, kas neietilpst viņu noklusējuma lomā 2. un 1. versijā, tad veicot jaunināšanu, norādītajam resursam tiks piešķirta noklusējuma loma visām uzdevuma piešķirēm neatkarīgi no piešķirtās lomas 2. versijā. Šīs piešķires rezultātā radīsies atšķirības novērtējumos, kas aprēķināti no 2. vai 1. versijas līdz 3. versijai, jo novērtējumi tiek aprēķināti, pamatojoties uz resursa lomu, nevis uz rindas uzdevuma piešķiršanu. Piemēram, 2. versijā Alisei Kaņepei tika piešķirti divi uzdevumi. Loma rindas uzdevumā 1. uzdevumam ir Izstrādātājs un 2. uzdevumam – Programmu pārvaldnieks. Pēc noklusējuma Alisei Kaņepei ir Programmu pārvaldnieka loma.

![Vienam resursam piešķirtas vairākas lomas.](media/upgrade-multiple-roles-02.png)

Tā kā Izstrādātāja un Programmu pārvaldnieka lomas atšķiras, izmaksu un pārdošanas aprēķini ir šādi:

![Izmaksu aprēķini resursu lomām.](media/upggrade-cost-estimates-03.png)

![Pārdošanas aprēķini resursu lomām.](media/upgrade-sales-estimates-04.png)

Jauninot uz 3. versiju, rindu uzdevumi tiek aizstāti ar resursu piešķirēm attiecībā uz rezervējamā resursa grupas dalībnieka uzdevumiem. Uzdevumam tiks izmantota rezervējamā resursa noklusējuma loma. Šajā attēlā Alise Kaņepe, kam ir Programmu pārvaldnieka loma, ir resurss.

![Resursu piešķīrumi.](media/resource-assignment-v2-05.png)

Tā kā aprēķini ir balstīti uz resursa noklusējuma lomu, pārdošanas un izmaksu aplēses var mainītas. Nākamajā attēlā vairs netiek rādīta **Izstrādātāja** loma, jo loma tagad ir ņemta no rezervējamā resursa noklusējuma lomas.

![Izmaksu aprēķini noklusējuma lomām.](media/resource-assignment-cost-estimate-06.png)
![Pārdošanas aprēķini noklusējuma lomām.](media/resource-assignment-sales-estimate-07.png)

Pēc jaunināšanas pabeigšanas varat rediģēt grupas dalībnieka lomu, lai izmainītu pēc noklusējuma piešķirto lomu. Tomēr, ja mainīsit grupas dalībnieku lomu, tā tiks mainīta visos viņiem piešķirtajos uzdevumos, jo 3. versijā grupas dalībniekiem vairs nevar piešķirt vairākas lomas.

![Resursa lomas atjaunināšana.](media/resource-role-assignment-08.png)

Tas attiecas arī uz rindas uzdevumiem, kas tika piešķirti norādītajiem resursiem, mainot resursa organizācijas struktūrvienību no noklusējuma uz citu organizācijas struktūrvienību. Pēc 3. versijas jaunināšanas pabeigšanas uzdevums izmantos resursa noklusējuma organizācijas vienību, nevis to, kas iestatīts rindas uzdevumam.

### <a name="tasks-assigned-to-generic-resources"></a>Vispārējiem resursiem piešķirtie uzdevumi
2. un 1. versijā uzdevumam varat iestatīt lomu un organizācijas struktūrvienību, un pēc tam izmantot līdzekli **Ģenerēt darba grupu**, lai ģenerētu vispārējus resursus, balstoties uz uzdevumam iestatītajiem atribūtiem. 3. versijā varat izveidot grupas dalībniekus ar lomu un organizācijas struktūrvienību, un pēc tam uzdevumam nozīmēt grupas dalībniekus.

2. un 1. versijā projektiem ar vispārējiem resursiem var būt divi stāvokļi, vai arī to kombinācija uzdevuma līmenī. Piemēram, var būt šādi scenāriji:

- Uzdevumi ar lomām un organizācijas struktūrvienībām, bet nav ģenerēta saistīta resursu piešķire.
- Uzdevumi ar vispārējiem grupas dalībnieku resursu piešķirēm, kas veiktas, izveidojot vispārēju resursu un izmantojot līdzekli **Ģenerēt darba grupu**.

Pirms jaunināšanas sākšanas ieteicams atkārtoti reģenerēt darba grupu katram projektam, kur vispārējiem resursiem ir piešķirti uzdevumi vai kuram ir nepieciešams veikt darba grupas ģenerēšanas procesu.

Attiecībā uz uzdevumiem, kas ir piešķirti vispārējiem grupas dalībniekiem, kas izveidoti, izmantojot **Ģenerēt darba grupu**, jauninājums atstās vispārēju resursu darba grupā, bet uzdevumu atstās šim vispārējam grupas dalībniekam. Iesakām jums ģenerēt resursu prasību vispārējam grupas dalībniekam pēc jaunināšanas, taču pirms resursa pieprasījuma rezervācijas vai iesniegšanas. Tas saglabās jebkādus organizācijas vienības uzdevumus vispārējiem grupas dalībniekiem, kas nav projekta līgumslēdzēja organizācijas struktūrvienība.

Piemēram, Projektā Z līgumslēdzēja organizācijas struktūrvienība ir Contoso US. Projekta plānā pārbaudes uzdevumi ieviešanas fāzē tika piešķirti lomai Tehniskais konsultants un nozīmētā organizācijas struktūrvienība ir Contoso India.

![Ieviešanas posma organizācijas piešķire.](media/org-unit-assignment-09.png)

Pēc ieviešanas fāzes integrācijas pārbaudes uzdevums ir piešķirts Tehniskajam konsultantam, bet kā organizācija ir iestatīta Contoso US.  

![Integrācijas pārbaudes uzdevuma organizācijas piešķire.](media/org-unit-generate-team-10.png)

Ģenerējot projekta darba grupu, tiek izveidoti divi vispārēji darba grupas dalībnieki, jo uzdevumiem ir dažādas organizācijas struktūrvienības. 1. Tehniskajam konsultantam tiks piešķirti Contoso India uzdevumi, bet 2. Tehniskajam konsultantam – Contoso US uzdevumi.  

![Ģenerētie vispārēji grupas dalībnieki.](media/org-unit-assignments-multiple-resources-11.png)

> [!NOTE]
> Project Service Automation 2. un 1. versijā darba grupas dalībnieks neieņem organizācijas struktūrvienību, kas tiek uzturēta rindas uzdevumā.

![Rindas uzdevumi Project Service Automation 2. versijā un 1. versijā.](media/line-tasks-12.png)

Organizācijas struktūrvienību var skatīt aprēķinu skatā. 

![Organizācijas struktūrvienību aprēķini.](media/org-unit-estimates-view-13.png)
 
Kad jaunināšana ir pabeigta, organizācijas struktūrvienība rindas uzdevumā, kas atbilst vispārējam grupas dalībniekam, tiek pievienota vispārējam grupas dalībniekam, un šis rindas uzdevums tiek noņemts. Tāpēc pirms jaunināšanas ieteicams ģenerēt vai atkārtoti ģenerēt darba grupu katram projektam, kurā ir iekļauti vispārēji resursi.

Uzdevumiem, kas ir piešķirti lomai ar organizācijas struktūrvienību, kas atšķiras no līgumslēdzēja projekta organizācijas struktūrvienības, un darba grupa nav ģenerēta, jaunināšana šai lomai izveidos vispārēju grupas dalībnieku, bet izmantos projekta līgumslēdzēja vienību grupas dalībnieka organizācijas vienībai. Atsaucoties uz piemēru ar Projektu Z, līgumslēdzēja organizācija Contoso US un projekta plāna pārbaudes uzdevumi Ieviešanas fāzē ir piešķirti lomai Tehniskais konsultants, bet par organizācijas struktūrvienību ir nozīmēts Contoso India. Integrācijas pārbaudes uzdevums, kas ir pabeigts pēc Ieviešanas fāzes, ir piešķirts lomai Tehniskais konsultants. Organizācijas vienība ir Contoso US, un darba grupa nav ģenerēta. Veicot jaunināšanu, būs izveidots viens vispārējs grupas dalībnieks, Tehnisks konsultants, kuram ir piešķirtas stundas visiem trim uzdevumiem, un organizācijas struktūrvienība Contoso US, kas ir projekta līgumslēdzēja organizācijas vstruktūrienība.   
 
Dažādu resursu organizācijas vienību noklusējuma vērtību izmaiņa grupas dalībniekiem, kas nav ģenerēti, ir iemesls, kāpēc pirms jaunināšanas ieteicams ģenerēt vai atkārtoti ģenerēt darba grupu katram projektam, kurā ir iekļauti vispārēji resursi, lai nezaudētu organizācijas vienību piešķires.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
