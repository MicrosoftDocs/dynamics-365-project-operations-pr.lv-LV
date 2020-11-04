---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 22, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 22, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: badd87a276d68d9959e9cca4220daf61ed570638
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080392"
---
# <a name="project-service-automation-update-release-22-v3"></a>Project Service Automation atjauninājumu izlaidums 22, V3

Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Šis laidiens ir saderīgs ar Dynamics 365 9. x. Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājuma izlaidumā 22. Šīs versijas būvējuma numurs ir V 3.10.33.48, un tā ir vispārīgi pieejama, izmantojot 2020. gada jūnija pašatjauninājumu.

## <a name="update-release-22"></a>Atjauninājumu izlaidums 22

### <a name="bug-fixes"></a>Kļūdu labojumi



**Laiks un izdevumi**

Ir novērstas tālāk norādītās problēmas.

- **Laika ieraksti** pēc importēšanas netiek automātiski pievienoti laika ierakstu grafikā.
- **Laika ieraksts** režģa datuma atlasītājs neatpazīst lietotāja reģionālos iestatījumus.

**Resursu pārvaldība**

Ir novērstas tālāk norādītās problēmas.

- Manuālajā režīmā izmaiņas **Resursu piešķire** kontūros netiek atpazītas, ģenerējot **Resursa prasības**.
- **Resursu pieprasījumi** neatbalsta pielāgotus pieprasījuma statusus.

**Projekta pārvaldība**

Ir novērstas tālāk norādītās problēmas.

- Veicot dubultklikšķi uz EstimateGridControl, netiks pareizi parsēti holandiešu valodas formāta skaitļi.
- Ja piešķires tiek mainītas, izmantojot Microsoft Project darbvirsmas klienta pievienojumprogrammu, piešķirtās stundas netiek pareizi atjauninātas.
- Režģi Projektu izsekošana un Novērtējumi parāda nepareizu pārdošanas valūtas kodu, ja līguma valūta atšķiras no klienta valūtas un organizācija ir konfigurēta rādīt valūtas kodus, nevis valūtas simbolus.
- Darba grupas dalībnieka beigu datums tiks pievienots vienai dienai, ja darba stundu grafiks ir 24 stundas dienā.
- Projekta aprakstā Darbības kategorijas pievienošana uzdevumam neizraisa automātisko saglabāšanu.
- Pievienojot darba grupas dalībnieku projekta veidnei, tiek parādīta šāda kļūda: “Resursa prasības nevar saistīt ar projekta veidnēm”. 
- Lentes kārtulas skripts "“msdyn.Approval.CanApproveOrReject” rāda taimauta kļūdu.

**Sales**

Ir novērstas tālāk norādītās problēmas.

- Validācijas kļūdas ziņojums netiek parādīts, ja Cenu saraksta uzmeklēšanā formā/entītijā tiek atlasīts Izmaksu cenrādis.
- Ja piedāvājums tiek slēgts, nepārvietojieties uz izveidoto līgumu, ja piedāvājumam pievienotais BPF ir beigu stadijā.
- Ja atsaukta **Neiekasētā pārdošana** tiek saistīta ar sākotnējām izmaksām, laika ieraksts tiks atsaukts.
- Pēc pogas **Apstiprināt** atlases rēķina statuss netiek mainīts uz **Apstiprināts** , ja vien rēķins netiek atsvaidzināts.
