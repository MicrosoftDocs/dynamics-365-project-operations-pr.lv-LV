---
title: Kā pielāgot projekta posmu biznesa procesa plūsmu?
description: Pārskats par to, kā pielāgot projekta posmu biznesa procesa plūsmu.
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: 15540f524fb8fca8f69a2249f783289ba683cad7dabbf58ecbf620d147e5d491
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002970"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a>Kā pielāgot projekta posmu biznesa procesa plūsmu?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

Ir zināms ierobežojums iepriekšējās Project Service versijās — posmu nosaukumiem projekta posmu biznesa procesa plūsmā ir precīzi jāatbilst paredzētajiem nosaukumiem angļu valodā (**Quote**, **Plan**, **Close**). Pretējā gadījumā biznesa loģika, kuras pamatā ir posmu nosaukumi angļu valodā, nedarbojas, kā paredzēts. Tāpēc projekta formā jūs neredzat pazīstamas darbības kā **Pārslēgt procesu** vai **Rediģēt procesu**, kā arī nav ieteicams pielāgot biznesa procesa plūsmu. 

Šis ierobežojums ir novērsts versijā 2.4.5.48 un jaunākās versijās. Šajā raksta tiek sniegti ieteicamie risinājumi, ja jums ir nepieciešams pielāgot noklusējuma biznesa procesa plūsmu agrākām versijām.  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a>Biznesa loģikai ir nepieciešama precīza atbilstība ar posmu nosaukumiem angļu valodā

Projekta posmu biznesa procesa plūsma ietver biznesa loģiku, kas programmā vada šādas darbības:
- Ja projekts ir saistīts ar piedāvājumu, kods iestata biznesa procesa plūsmu posmā **Quote** (Piedāvajums).
- Ja projekts ir saistīts ar līgumu, kods iestata biznesa procesa plūsmu posmā **Plan** (Plāns).
- Kad biznesa procesa plūsma tiek iestatīta posmā **Close** (Aizvērt), projekta ieraksts ir deaktivizēts. Kad projekts tiek deaktivizēts, projekta veidlapa un darba sadalījuma struktūra (WBS) tiek iestatītas kā tikai lasāmas, tiek izlaistas nosaukto resursu rezervācijas un deaktivizēti visi saistītie cenrāži.

Šī biznesa loģika ir balstīta uz projekta posmu nosaukumiem angļu valodā. Šī atkarība no posma nosaukumiem angļu valodā ir galvenais iemesls, kāpēc nav ieteicams pielāgot projekta posmu biznesa procesa plūsmu, kā arī kāpēc projekta entītijā neredzat bieži izmantotās biznesa procesa plūsmas darbības, piemēram, **Pārslēgt procesu** vai **Rediģēt procesu**.

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a>Kas notiek, ja posmu nosaukumi neatbilst nosaukumiem angļu valodā?

Ja Project Service versijā 1.x platformā 8.2 posmu nosaukumi biznesa procesa plūsmā precīzi neatbilst posmu nosaukumiem angļu valodā, biznesa loģika, kas iestata pareizo posmu piedāvājumiem vai līgumiem vai aizver projektu, tiek izlaista. Netiek parādīti kļūdu ziņojumi. Tāpēc šķiet, ka varat pielāgot projekta posmus biznesa procesa plūsmā. Tomēr nedarbosies automātiskie procesi piedāvājumiem, līgumiem un projektu aizvēršanai.

Project Service versijā 2.4.4.30 vai vecākā versijā platformā 9.0 bija nozīmīgas arhitektūras izmaiņas biznesa procesa plūsmās, kuru dēļ bija jāpārraksta biznesa procesa plūsmas biznesa loģika. Ja procesa posmu nosaukumi neatbilst paredzētajiem nosaukumiem angļu valodā, šī iemesla dēļ netiek parādīts kļūdas ziņojums. 

Ja vēlaties pielāgot projekta posmus projekta entītijai biznesa procesa plūsmā, varat tikai pievienot jaunus posmus projekta entītijas noklusējuma biznesa procesa plūsmā, saglabājot posmus **Piedāvājums**, **Plāns** un **Aizvēršana** tādus, kādi tie ir. Šis ierobežojums nodrošina, ka netiek rādītas kļūdas no biznesa loģikas, kas biznesa procesa plūsmā sagaida posmu nosaukumus angļu valodā.

Versijā 2.4.5.48 un jaunākās versijās biznesa loģika, kas ir aprakstīta šajā rakstā, ir noņemta no projekta entītijas noklusējuma biznesa procesa plūsmas. Jauninot uz šo versiju vai jaunāku versiju, varēsiet pielāgot vai aizstāt noklusējuma biznesa procesa plūsmu ar savu. 

## <a name="workarounds-for-earlier-versions"></a>Risinājumi iepriekšējām versijām

Ja nevarat veikt jaunināšanu, varat pielāgot projekta posmu biznesa procesa plūsmu projekta entītijai vienā no diviem tālāk minētajiem veidiem.

1. Pievienojiet papildu posmus noklusējuma konfigurācijā, saglabājot **Piedāvājums**, **Plāns** un **Aizvēršana** posmu nosaukumus angļu valodā.


![Ekrānuzņēmums: posmu pievienošana noklusējuma konfigurācijai.](media/FAQ-Customize-BPF-1.png)
 
2. Izveidojiet savu biznesa procesa plūsmu un iestatiet to kā galveno biznesa procesa plūsmu projekta entītijai, kas ļauj izmantot jebkādus posma vārdus. Tomēr, ja vēlaties izmantot tādus pašus standarta projekta posmus **Piedāvājums**, **Plāns** un **Aizvēršana**, ir jāveic daži pielāgojumi, kuru pamatā ir pielāgotie posmu nosaukumi. Sarežģītāka loģika ir projekta aizvēršana, ko joprojām varat aktivizēt, deaktivizējot projekta ierakstu.

![BPF pielāgošana.](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a>Papildu apsvērumi Project Service versijai 2.4.4.30 vai vecākai versijai platformā 9.0

Programmā Project Service 2.4.4.30 vai vecākā versijā platformā 9.0 ar pielāgotu biznesa procesa plūsmu projekta entītijas lauku **Posma nosaukums** izmantojot diagrammā **Projekts pēc posma**, projektu saraksta skati netiek atjaunināti, tas notiek tāpēc, ka tas ir saistīts ar noklusējuma projektu posmu biznesa procesa plūsmu. Šo problēmu varat novērst, veicot tālāk norādītās darbības.

- Pievienojiet pielāgotu lauku, lai tvertu pašreizējo biznesa procesa plūsmas posmu, kas tiek atjaunināts, kad lietotājs no viena pielāgotas biznesa procesa plūsmas posma pāriet uz citu.

- Mainiet diagrammu **Projekts pēc posma** tā, lai tā darbotos ar jūsu pielāgoto lauku, nevis noklusējuma konfigurāciju.

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a>Darbības, lai projekta entītijai izveidotu savu biznesa procesa plūsmu

Lai projekta entītijai izveidotu savu biznesa procesa plūsmu, rīkojieties šādi:

1. Pārejiet uz **Iestatījumi** > **Procesu centrs**. Nekopējiet projekta posmu biznesa procesa plūsmu, jo tādējādi tiek kopēta arī Project Service biznesa loģika.

  ![Procesa izveide.](media/FAQ-Customize-BPF-3.png)

2. Izmantojiet procesu noformētāju, lai izveidotu vēlamos posmu nosaukumus. Ja vēlaties tādu pašu funkcionalitāti kā **Piedāvājums**, **Plāns** un **Aizvēršana** noklusējuma posmiem, jums būs tā jāizveido, pamatojoties uz pielāgotās biznesa procesa plūsmas posmu nosaukumiem.

   ![Ekrānuzņēmums ar procesu noformētāju, kas izmantots BPF pielāgošanai.](media/FAQ-Customize-BPF-4.png) 

3. Procesu noformētājā noklikšķiniet uz **Pasūtījumu procesa plūsma**, lai pielāgotu biznesa procesa plūsmu iestatītu kā galveno biznesa procesa plūsmu projekta entītijai, pārvietojot to virs projekta posmu biznesa procesa plūsmas saraksta sākumā.


   [Pasūtījumu procesa plūsmas izveides ekrānuzņēmums](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a>Tālāk minētās darbības attiecas uz Project Service 2.4.4.30 vai vecākām versijām platformā 9.0

4. Pievienojiet jaunu pielāgotu lauku projekta entītijai, lai iestatītu pielāgotus posmus pielāgotajā biznesa procesa plūsmā. Lai atjauninātu šo lauku, kad tiks atjaunināts pielāgotas biznesa procesa plūsmas posms, būs jāpievieno biznesa loģika (posms/darbplūsma).

   ![Projekta entītijas pielāgošanas ekrānuzņēmums.](media/FAQ-Customize-BPF-6-720.png)

5. Mainiet diagrammu **Projekts pēc posma**, lai posmiem lietotu jūsu jauno pielāgoto lauku.

   ![Ekrānuzņēmums: diagrammas Projekts pēc posma izmantošana.](media/FAQ-Customize-BPF-7-720.png)

6. Mainiet jebkurus projekta entītijas laukus, lai posmiem ietvertu jauno pielāgoto lauku.

   ![Projekta entītijas skatu maiņas ekrānuzņēmums.](media/FAQ-Customize-BPF-8-720.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]