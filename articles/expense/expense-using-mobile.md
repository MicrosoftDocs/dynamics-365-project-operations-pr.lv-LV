---
title: Izdevumu mobilā programma
description: Šajā tēmā ir sniegta informācija par to, kā izmantot izdevumu pārvaldības mobilo darbvietu.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 88251552a937f0a3a066e08b87dbd5f7b73c46c69776fbc788d37cc21fe73541
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993205"
---
# <a name="mobile-expense-app"></a>Izdevumu mobilā programma

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Šajā tēmā ir sniegta informācija par to, kā izmantot **Izdevumu pārvaldības** mobilo darbvietu. Šī darbvieta ļauj lietotājiem tvert un augšupielādēt kvīti, lai to varētu vēlāk pievienot izdevumu atskaitei. Lietotāji var arī ātri izveidot izdevumu rindu, izmantojot pievienoto kvīti, un izveidot un pārvaldīt savas izdevumu atskaites. Turklāt apstiprinātāji var izmantot **Izdevumu pārvaldības** mobilo darbvietu, lai skatītu sev piešķirtās izdevumu atskaites un tās vai nu apstiprināt vai noraidīt.

Šo mobilo darbvietu ir paredzēts izmantot kopā ar Dynamics 365 Unified OPS mobilo programmu.

Daudzām organizācijām ir nepieciešams brauciena vai biznesa izdevumu atskaitei pievienot kvīts kopiju, kuru darba ņēmējs iesniedz, lai saņemtu atlīdzinājumu. **Izmaksu pārvaldības** mobilā darbvieta ļauj lietotājiem ātri izveidot jaunas izmaksu rindas sevis izvēlētajā mobilajā ierīcē, izmantoto pievienoto kvīts fotoattēlu. Lietotājs var arī tvert kvīts fotoattēlu un to pievienot izdevumu atskaitei vēlāk. Darbinieki var arī izveidot un pārvaldīt izdevumu atskaites un pēc tam tās iesniegt apstiprināšanai un atlīdzināšanai, izmantojot mobilās ierīces.

Konkrēti **Izmaksu pārvaldības** mobilā darbvieta ļauj lietotājiem veikt šādus uzdevumus:

- Uzņemt kvīts fotoattēlu. Augšupielādēt kvīts fotoattēlu un to vēlāk pievienot izdevumu atskaitei.
- Augšupielādēt failu kā tverto kvīti. Pēc tam šo failu varat vēlāk pievienot izdevumu atskaitei.
- Izveidot jaunu izdevumu rindu, izmantojot pievienoto kvīti. Pēc tam varat vēlāk izdevumu atskaitei pievienot rindas vienumu un to iesniegt apstiprināšanai un atlīdzināšanai.

Varat arī izmantot šos līdzekļus:

- Izveidot jaunu izdevumu atskaiti.
- Pievienot izdevumu atskaitei kredītkaršu darījumus un citus iepriekš radušos izdevumus.
- Izveidot jaunus izdevumus izdevumu atskaitei.
- Pievienot kvīti jebkādiem izdevumiem izdevumu atskaitē, vai nu nofotografējot kvīti vai augšupielādējot failu kā tverto kvīti.
- Atkarībā no uzņēmuma izdevumu politikas, varat izdevumiem pievienot viesu sarakstu.
- Atkarībā no uzņēmuma izdevumu politikas, varat uzskaitīt pa punktiem izdevumus.
- Iesniegt izdevumu atskaiti apstiprināšanai un atlīdzināšanai.
- Apstiprināt vai noraidīt izdevumu atskaites, kurām esat piešķirts kā apstiprinātājs.

## <a name="prerequisites"></a>Priekšnosacījumi
Priekšnosacījumi atšķiras atkarībā no tā, kāda versija ir izvietota jūsu organizācijā.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Priekšnosacījumi, ja izmantojat Dynamics 365 Finance 
Ja jūsu organizācijai ir izvietots Finance, sistēmas administratoram ir jāpublicē **Izdevumu pārvaldības** mobilajai darbvietai. 

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Priekšnosacījumi, ja izmantojat versiju 1611 ar platformas atjauninājumu 3 vai jaunāku versiju
Ja jūsu organizācijai ir izvietota versija 1611 ar platformas atjauninājumu 3 vai jaunāku versiju, sistēmas administratoram ir jāizpilda tālāk minētie priekšnosacījumi. 

<table>
<thead>
<tr class="header">
<th>Priekšnosacījums</th>
<th>Loma</th>
<th>Apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>KB 4019015 ieviešana.</td>
<td>Sistēmas administrators</td>
<td>KB 4019015 ir X + + atjaunināšanas vai metadatu labojumfails, kurā ir iekļauts <strong>Izmaksu pārvaldības</strong> mobilajā darbvietā. Lai ieviestu KB 4019015, jūsu sistēmas administratoram ir jāizpilda šīs darbības.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Lejupielādēt atjauninājumus Lifecycle Services</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Instalējiet metadatu labojumfailu</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Izveidojiet izvietojamu pakotni</a>, kurā ir <strong>ApplicationSuite</strong> un <strong>ExpenseMobile</strong> modeļi, un pēc tam augšupielādējiet izvēršamo paku uz LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Izmantojiet izvēršamo pakotni</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Publicēt <strong>Izmaksu pārvaldības</strong> mobilo darbvietu.</td>
<td>Sistēmas administrators</td>
<td>Skatiet <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publicēt mobilo darbvietu</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-unified-ops-mobile-app"></a>Dynamics 365 Unified Ops mobilās programmas lejupielāde un instalēšana
Dynamics 365 Unified Ops mobilās programmas lejupielāde un instalēšana:

- [Android tālruņiem](https://go.microsoft.com/fwlink/?linkid=850662)
- [Tālruņiem iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Pierakstieties mobilajā programmā
1. Startējiet programmu savā mobilajā ierīcē.
2. Ievadiet savu Dynamics 365 URL.
4. Pirmo reizi pierakstoties sistēmā, tiek parādīts aicinājums ievadīt lietotājvārdu un paroli. Ievadiet savus akreditācijas datus.
5. Pēc pierakstīšanās programmā tiek rādītas pieejamās darbvietas jūsu uzņēmumam. Ja sistēmas administrators vēlāk publicēs jaunu darbvietu, būs jāatsvaidzina mobilo darbvietu saraksts.

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Kvīts tveršana, izmantojot Izdevumu pārvaldības mobilo darbvietu

1. Mobilajā ierīcē atveriet **Izdevumu pārvaldības** darbvietu.
2. Atlasiet **Tvert kvīti**.
3. Atlasiet **Uzņemt fotoattēlu** vai **Izvēlieties fotoattēlu**.
4. Veiciet vienu no šīm darbībām:

   - Ja atlasījāt **Uzņemt fotoattēlu**, veiciet šīs darbības:

      1. Jūs pārcels uz kameru jūsu mobilajā ierīcē, lai varat uzņemt kvīts fotoattēlu. 
      2. Pēc fotoattēla uzņemšanas atlasiet **OK**, lai apstiprinātu fotoattēlu.
      3. Pēc izvēles: Ievadiet fotoattēla nosaukumu un ievadiet piezīmes.

    - Ja atlasījāt **Izvēlieties fotoattēlu**, veiciet šīs darbības:

        1. Atlasiet sarakstā attēlu.
        2. Pēc izvēles: Ievadiet attēla nosaukumu un ievadiet piezīmes.

5. Atlasiet **Gatavs**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Ātri ievadiet izdevumus, izmantojot Izdevumu pārvaldības mobilo darbvietu

1. Mobilajā ierīcē atveriet **Izdevumu pārvaldības** darbvietu.
2. Atlasiet **Ātrā izdevumu ievade**.
3. Atlasiet izdevumu kategoriju. Redzēsit sarakstu ar izdevumu kategorijām, kas tiek ielādētas jūsu programmā lietošanai bezsaistē. Pēc noklusējuma tiek ielādēti 50 elementi, taču izstrādātājs šo skaitu var mainīt. Papildinformāciju izstrādātāji var skatīt sadaļā [Mobilā platforma](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Ja jūsu kategorija nav iekļauta sarakstā, atlasiet **Meklēt**, lai veiktu meklēšanu tiešsaistē. Meklējiet pēc izdevumu kategorijas vai pārslēdziet uz meklēšanu pēc izdevumu veida.
4. Ievadiet izdevumu transakcijas datumu.
5. Pēc izvēles: Ievadiet izdevumu tirgotāju.
6. Ievadiet izdevuma apmēru.
7. Atlasiet izdevuma valūtu. Redzēsit valūtu kodu sarakstu, kas tiek ielādēti jūsu programmā lietošanai bezsaistē. Pēc noklusējuma tiek ielādētas 400 valūtas, taču izstrādātājs šo skaitu var mainīt. Papildinformāciju izstrādātāji var skatīt sadaļā [Mobilā platforma](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Ja jūsu valūta nav iekļauta sarakstā, atlasiet **Meklēt**, lai veiktu meklēšanu tiešsaistē. Meklējiet pēc valūtas vai pārslēdzieties uz meklēšanu pēc nosaukuma.
8. Atlasiet **Uzņemt fotoattēlu** vai **Izvēlieties fotoattēlu**.
9. Veiciet vienu no šīm darbībām:

    - Ja atlasāt **Uzņemt fotoattēlu**, jūs pārcels uz mobilās ierīces kameru, lai varat uzņemt kvīts fotoattēlu. Pēc fotoattēla uzņemšanas atlasiet **OK**, lai apstiprinātu fotoattēlu.
    - Ja atlasāt **Izvēlēties attēlu**, atlasiet sarakstā attēlu.

10. Atlasiet **Gatavs**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Apstipriniet izdevumu atskaiti, izmantojot Izdevumu pārvaldības mobilo darbvietu (ja lietojat 2017. gada jūlija atjauninājumu)

1. Mobilajā ierīcē atveriet **Izdevumu pārvaldības** darbvietu.
2. **Izmaksu apstiprinājumos** tiek parādīts jūsu apstiprināšanai piešķirto izdevumu atskaišu skaits. Šis skaitlis tiek atjaunināts aptuveni ik pēc 30 minūtēm. Atlasiet **Izdevumu apstiprinājumi**.

    Tiek rādīts jūsu apstiprināšanai piešķirto izdevumu atskaišu saraksts.
    
3. Atlasiet izdevumu atskaiti, lai skatītu tās izdevumu informāciju.
4. Atlasiet izdevumu, lai skatītu tā informāciju. Informācija, kas tiek rādīta attiecībā uz izdevumu, ietver informāciju par kvīti, viesi un specifikāciju.
5. Atgriežoties **Izdevumu atskaites** lapā atlasiet apstiprināt vai noraidīt izdevumu atskaiti.
6. Ievadiet jebkādus apstiprinājuma darbības komentārus.
7. Atlasiet **Gatavs**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Izveidojiet jaunu izdevumu atskaiti un iesniedziet to apstiprināšanai, izmantojot Izdevumu pārvaldības mobilo darbvietu (ja izmantojat 2017. gada jūlija atjauninājumu)

1. Mobilajā ierīcē atveriet **Izdevumu pārvaldības** darbvietu.
2. Atlasiet **Izdevumu ievade**.
3. Atlasiet **Jauna atskaite** vai sarakstā atlasiet esošu izdevumu atskaiti.
4. Jaunām izdevumu atskaitēm ievadies mērķi un jebkādu pieejamo papildinformāciju. Šī informācija atšķiras atkarībā no veida, kādā izdevumu pārvaldība tiek konfigurēta jūsu uzņēmumam.
5. Atlasiet **Gatavs**.
6. Lai izdevumu atskaitei pievienotu esošus izdevumus, piemēram, kredītkaršu transakcijas, atlasiet **Pievienot**.
7. Sarakstā atlasiet vienu vai vairākus izdevumus.
8. Atlasiet **Gatavs**.
9. Lai izdevumu atskaitei pievienotu jaunu izdevumu, atlasiet **Jauns izdevums**.
10. Atlasiet izdevuma kategoriju. Redzēsit sarakstu ar izdevumu kategorijām, kas tiek ielādētas jūsu programmā lietošanai bezsaistē. Pēc noklusējuma tiek ielādēti 50 elementi, taču izstrādātājs šo skaitu var mainīt. Papildinformāciju izstrādātāji var skatīt sadaļā [Mobilā platforma](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Ja jūsu kategorija nav iekļauta sarakstā, atlasiet **Meklēt**, lai veiktu meklēšanu tiešsaistē. Meklējiet pēc izdevumu kategorijas vai pārslēdziet uz meklēšanu pēc izdevumu veida.
11. Pēc izvēles: Ievadiet izdevumu tirgotāju.
12. Ievadiet izdevumu transakcijas datumu.
13. Ievadiet izdevuma apmēru.
14. Atlasiet izdevuma valūtu. Redzēsit valūtu kodu sarakstu, kas tiek ielādēti jūsu programmā lietošanai bezsaistē. Pēc noklusējuma tiek ielādētas 400 valūtas, taču izstrādātājs šo skaitu var mainīt. Papildinformāciju izstrādātāji var skatīt sadaļā [Mobilā platforma](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Ja jūsu valūta nav iekļauta sarakstā, atlasiet **Meklēt**, lai veiktu meklēšanu tiešsaistē. Meklējiet pēc valūtas vai pārslēdzieties uz meklēšanu pēc nosaukuma.
15. Atlasiet **Gatavs**.
16. Lai izdevumam pievienotu papildinformāciju, atlasiet **Pievienot papildinformāciju**. Pieejamie lauki ir atkarīgi no jūsu uzņēmuma izdevumu pārvaldības konfigurācijas.
17. Ja saskaņā ar uzņēmuma politiku ir nepieciešama izdevumu kvīts, atlasiet **Kvītis** un pēc tam izpildiet šādas darbības:

    1. Atlasiet **Tvert kvīti** vai **Pievienot kvīti**.
    2. Veiciet vienu no šīm darbībām:

        - Ja atlasījāt **Tvert kvīti**, izpildiet šādas darbības:

            1. Atlasiet **Uzņemt fotoattēlu** vai **Izvēlieties fotoattēlu**.
            2. Veiciet vienu no šīm darbībām:

                - Ja atlasījāt **Uzņemt fotoattēlu**, veiciet šīs darbības:

                    1. Jūs pārcels uz kameru jūsu mobilajā ierīcē, lai varat uzņemt kvīts fotoattēlu. Pēc fotoattēla uzņemšanas atlasiet **OK**, lai apstiprinātu fotoattēlu.
                    2. Pēc izvēles: Ievadiet fotoattēla nosaukumu un ievadiet piezīmes.

                - Ja atlasījāt **Izvēlieties fotoattēlu**, veiciet šīs darbības:

                    1. Atlasiet sarakstā attēlu.
                    2. Pēc izvēles: Ievadiet attēla nosaukumu un ievadiet piezīmes.

            3.  Atlasiet **Gatavs**.

        - Ja atlasījāt **Pievienot kvīti**, izpildiet šādas darbības:

            1.  Atlasiet sarakstā vienu vai vairākus attēlus.
            2.  Atlasiet **Gatavs**.

    3. Atlasiet pogu **Atpakaļ**, lai atgrieztos pie izdevumu informācijas.

18. Ja saskaņā ar uzņēmuma politiku ir nepieciešami izdevumu viesi, atlasiet **Viesi** un pēc tam izpildiet šādas darbības:

    1. Atlasiet **Viesis**, **Iepriekšējie viesi** vai **Līdzstrādnieki**.
    2. Veiciet vienu no šīm darbībām:

        - Ja atlasījāt **Viesis**, izpildiet šādas darbības:

            1. Ievadiet viesa vārdu.
            2. Pēc izvēles: Ievadiet viesa organizāciju un/vai valsti.
            3. Pēc izvēles: Ievadiet viesa amatu.
            4. Atlasiet **Gatavs**.

        - Ja atlasījāt **Iepriekšējie viesi**, izpildiet šādas darbības:

            1. Sarakstā atlasiet vienu vai vairākus iepriekšējos viesus. Jūs redzēsit iepriekšējām izdevumu atskaitēm pievienotu iepriekšējo viesu sarakstu, kas tiek ielādētas jūsu programmā lietošanai bezsaistē. Pēc noklusējuma tiek ielādēti 50 elementi, taču izstrādātājs šo skaitu var mainīt. Papildinformāciju izstrādātāji var skatīt sadaļā [Mobilā platforma](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Ja jūsu iepriekšējais viesis nav iekļauts sarakstā, atlasiet **Meklēt**, lai veiktu meklēšanu tiešsaistē. Meklējiet pēc vārda vai pārslēdzieties uz meklēšanu pēc organizācijas, valsts vai amata.
            2. Atlasiet **Gatavs**.

        - Ja atlasījāt **Līdzstrādnieki**, izpildiet šādas darbības:

            1. Sarakstā atlasiet vienu vai vairākus līdzstrādniekus. Redzēsit sarakstu ar līdzstrādniekiem, kas tiek ielādēts jūsu programmā lietošanai bezsaistē. Pēc noklusējuma tiek ielādēti 50 elementi, taču izstrādātājs šo skaitu var mainīt. Papildinformāciju izstrādātāji var skatīt sadaļā [Mobilā platforma](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Ja jūsu līdzstrādnieks nav iekļauts sarakstā, atlasiet **Meklēt**, lai veiktu meklēšanu tiešsaistē. Meklējiet pēc vārda vai pārslēdzieties uz meklēšanu pēc uzņēmuma vai amata.
            2. Atlasiet **Gatavs**.

    3. Atlasiet pogu **Atpakaļ**, lai atgrieztos pie izdevumu informācijas.

19. Ja saskaņā ar uzņēmuma politiku izdevumus nepieciešams uzskaitīt, atlasiet **Uzskaitīt** un pēc tam veiciet šādas darbības:

    1. Atlasiet pirmo uzskaitīšanas datumu.
    2. Atlasiet **Pievienot uzskaitījumu**.
    3. Atlasiet izdevumu uzskaitīšanas apakškategoriju. Redzēsit sarakstu ar izdevumu apakškategorijām, kas tiek ielādētas jūsu programmā lietošanai bezsaistē. Pēc noklusējuma tiek ielādēti 50 elementi, taču izstrādātājs šo skaitu var mainīt. Papildinformāciju izstrādātāji var skatīt sadaļā [Mobilā platforma](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Ja jūsu apakškategorija nav iekļauta sarakstā, atlasiet **Meklēt**, lai veiktu meklēšanu tiešsaistē. Meklējiet pēc izdevuma apakškategorijas nosaukuma.
    4. Ievadiet uzskaites transakcijas apmēru.
    5. Ja nepieciešams rediģējiet transakcijas datumu.
    6. Atlasiet **Gatavs**.
    7. Atkārtojiet iepriekšējās darbības, līdz esat pabeiguši pievienot visus atlasītā datuma uzskaitījumus.
    8. Papildu dienām varat atlasīt **Kopēt uz nākamo dienu**, lai kopētu uzskaitījumus uz nākamo dienu. Varat arī atlasīt datumu, kuru uzskaitīt, un pēc tam pievienot uzskaitījumus tāpat, kā to darījāt pirmajam datumam.
    9. Pēc izdevumu uzskaites pabeigšanas, atlasiet pogu **Atpakaļ**, lai atgrieztos pie izdevumu informācijas.

20. Atlasiet pogu **Atpakaļ**, lai atgrieztos **Izdevumu atskaites** lapā.
21. Atkārtojiet iepriekšējās darbības, līdz ir pievienoti visi izdevumi.
22. Atlasiet **Iesniegt**.
23. Ievadiet jebkādus komentārus apstiprinātājam.
24. Atlasiet **Gatavs**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]