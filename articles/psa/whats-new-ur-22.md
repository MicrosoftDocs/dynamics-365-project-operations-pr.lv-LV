---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 22, V3
description: Šajā rakstā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation Update Release 22, V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 733ee6e0d3583f21d0f58f9651920be3e3fd8cb0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930649"
---
# <a name="project-service-automation-update-release-22-v3"></a>Project Service Automation atjauninājumu izlaidums 22, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Šis laidiens ir saderīgs ar Dynamics 365 9. x. Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).

Šajā rakstā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti project service automation V3, Update Release 22. Šīs versijas būvējuma numurs ir V 3.10.33.48, un tā ir vispārīgi pieejama, izmantojot 2020. gada jūnija pašatjauninājumu.

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
- Pēc pogas **Apstiprināt** atlases rēķina statuss netiek mainīts uz **Apstiprināts**, ja vien rēķins netiek atsvaidzināts.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
