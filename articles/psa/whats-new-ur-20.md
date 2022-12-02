---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 20, V3
description: Šajā rakstā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 20, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: 7265f4999ee9c584450efcf444621c00acd65920
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913077"
---
# <a name="project-service-automation-update-release-20-v3"></a>Project Service Automation atjauninājumu izlaidums 20, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Šis laidiens ir saderīgs ar Dynamics 365 9. x. Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).

Šajā rakstā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājuma izlaidumā 20. Šīs versijas būvējuma numurs ir V 3.10.31.37, un tā ir vispārīgi pieejama, izmantojot 2020. gada jūnija pašatjauninājumu.

## <a name="update-release-20"></a>Atjauninājumu izlaidums 20

### <a name="bug-fixes"></a>Kļūdu labojumi

**Projekta pārvaldība**

Ir novērstas tālāk norādītās problēmas.

- Projekta darba grupas dalībnieku importēšana ar piešķiršanas metodi, kurai ir nepieciešamas stundas, izraisa neskaidru kļūdas ziņojumu, kad noteiktās stundas ir nulle.
- Lietotāji saņem nepareiza kļūda, ja projekta uzdevuma laukā **Apraksts** ir ievadīti maksimālais rakstzīmju skaits.
- **Microsoft Dynamics 365 Project Service Automation pievienojumprogrammas lejupielādes** lapa novirza uz angļu valodas lejupielādes lapu, kad lietotāja valodas iestatījumi ir iestatīti japāņu valodā.
- Kad rodas servera kļūda, dažreiz paliek sinhronizācijas etiķete, kas atrodas veidlapas **Projekti** cilnē **Grafiks**.
- Kad uzdevums tiek modificēts, uz serveri tiek nosūtīti lieki uzdevuma atjauninājumi.

**Sales**

Ir novērstas tālāk norādītās problēmas.

- Veidlapā **Līgums** veicot dubultklikšķi uz **Izveidot rēķinu**, tiek izveidoti divi rēķinus vienam faktiskajam ierakstam.
- Lietotāji nevar izveidot izdevumu ierakstus programmā Internet Explorer 11.
- Izmaksu apvērse un rēķinā neiekļauto pārdošanas datu apvērse nav saistītas.
- POga **Atsvaidzināt faktiskos datus** veidlapā **Projekts** neatsvaidzina **Uzdevuma faktisko stundu skaits**.
- Spraudnis **PreValidateProjectTeamMemberCreate** var izveidot dublikātus vispārējiem rezervējamiem resursiem, ja atribūts **msdyn_isgenericresourceprojectscoped** ir iestatīts uz **Aplams**.
- **Pārrēķināt** notīra ar produktiem saistītu piedāvājumu rindas detalizētas informācijas un līgumu rindu detalizētas informācijas rēķinā iekļaujamās izmaksas.
- Noteiktos scenārijos spraudnis **PostEstimateLineUpdate** rāda nulles atsauces kļūdas ziņojumu.
- Laika fāzes ilgums **Rentabilitātes analīzes diagrammā** neatbilst izmaksu ilgumam piedāvājuma fiksētas cenas piedāvājuma rindas detalizētajā informācijā.
- Vienību un vienību grupu vērtības izmaksu kategorijām veidlapās **Līguma rindu informācija** un **Piedāvājumu rindu informācija** netiek pareizi iestatītas uz noklusējumu.
- Saraksts **Organizācijas vienību izmaksu cenrādis** ļauj pārklāties spēkā esamības datumiem.
- Lietotājiem nav atļauts mainīt **OrgUnit**, ja pasūtījuma tips ir neatkarīgs no darba, jo tas izraisa nulles atsauces izņēmumu kļūdu.
- Mēģinot naviģēt no veidlapas **Piedāvājuma rindu informācija** atpakaļ uz cilni **Piedāvājums**, veidlapa tiek atsvaidzināta un parāda cilni **Kopsavilkums**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
