---
title: Rēķinu izveidošanas papildu līgumi, pamatojoties uz norisi
description: Šajā tēmā izskaidrots, kā izveidot projekta līgumus, lai varētu ģenerēt klientiem rēķinus, par pamatu izmantojot pabeigtā darba procentus.
author: RadhikaRS
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: bdafc2ed2398054d8b0bf42bdd96dfe0eccee93b
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683172"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Rēķinu izveidošanas papildu līgumi, pamatojoties uz norisi
[!include [banner](../includes/banner.md)]

Šajā tēmā izskaidrots, kā izveidot projekta līgumus, lai varētu izveidot klientiem rēķinus, par pamatu izmantojot pabeigtā darba procentus. Rēķina summas automātiski tiek aprēķinātas budžeta darba kategorijām, kas ir iestatītas projektam. Rēķina laiks tiek iestatīts, vienojoties par projekta līgumu ar klientu.

Izmantojiet šajā tēmā norādītās darbības, lai iestatītu līgumu, saistīto projektu un rēķinu noteikumus, kas aprēķina rēķinu summas projektam iestatītajām budžeta kategorijām.

Pēc tam, kad esat izveidojis līgumu un projektu, varat iestatīt detalizētu informāciju par projektu. Piemēram, var definēt aktivitātes un piešķirt darbiniekiem projektu.

## <a name="example"></a>Piemērs

Jūsu organizācija ir programmatūras izstrādes uzņēmums. Jūs piekrītat izveidot algu uzskaites pakotni klientam par kopējo maksu 20 000 ASV dolāri (USD). Jūsu uzņēmums piekrīt izrakstīt rēķinu klientam, kad pabeigsit noteiktu projekta procentuālo daļu. Darbam iestatiet tālāk norādītās projekta kategorijas, lai tās varētu izmantot norēķinu procesā.

- Vairumtirdzniecība un mazumtirdzniecība; automobiļu un motociklu remonts
- Dizains
- Instalēšana

Jūs iestatāt arī norēķinu kārtulas, kuras automātiski aprēķina rēķina summas par katrai kategorijai izpildīto projekta daļu.

Budžeta pārvaldnieks izveido budžetu projekta kategorijām. Pabeigtā darba apjoms automātiski tiek aprēķināts procentos no faktiskā darba apjoma salīdzinājumā ar budžetā paredzētajām summām.

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms izveidojat projektu, kurā tiek izmantotas norēķinu kārtulas, iestatiet numuru sērijas norēķinu kārtulām un maksas žurnālu, kas tiek izmantots, lai grāmatotu progresa rēķinus.

1. Dodieties uz **Projekta pārvaldība un uzskaite** \> **Iestatīšana** \> **Projekta pārvaldības un grāmatvedības parametri**.
2. Lapas **Projekta pārvaldība un uzskaites parametri** cilnē **Numuru sērijas** iestatiet to numuru sēriju, ko vēlaties izmantot, veidojot rēķina kārtulas.
3. Dodieties uz **Projekta pārvaldība un uzskaite** \> **Žurnāli** \> **Izmaksas**.
4. Lapā **Izmaksu žurnāls** atlasiet **Jauns** un ievadiet žurnāla nosaukumu.

## <a name="create-a-contract-for-progress-billings"></a>Līgumu par norises rēķinu izpildi izveide

Veiciet šīs darbības, lai izveidotu projekta līgumu fiksētas cenas projektam. Projekta rēķins tiek veidots, kad projektā pabeigtais darbs sasniedz norādīto procentuālo vērtību.

1. Dodieties uz **Projekta pārvaldība un uzskaite** \> **Projekti** \> **Projekta līgumi**.
2. Lapā **Projekta līgumi** atlasiet **Jauns**.
3. Dialoglodziņā **Jauns projekta līgums** iestatiet tālāk norādītos laukus.

    - **Nosaukums**
    - **Finansēšanas veids**
    - **Finansējuma avots**
    - **Pārdošanas valūta** — pēc noklusējuma šī valūta tiek izmantota klienta rēķiniem, kas saistīti ar šo projekta līgumu. Taču pārdošanas valūtu var mainīt noteiktam klienta rēķinam.

4. Atlasiet **Labi**. Šī informācija tiek kopēta lapā **Projekta līgumi**.
5. Lapā **Projekta līgumi** aizpildiet visu nepieciešamo projekta informāciju.

## <a name="create-a-project-for-progress-billings"></a>Projektu par norises rēķinu izpildi izveide

Veiciet šīs darbības, lai izveidotu projektu un visus apakšprojektus, kas saistīti ar projekta līgumu.

1. Dodieties uz **Projekta pārvaldība un uzskaite** \> **Projekti** \> **Visi projekti**.
2. Lapā **Visi projekti** atlasiet **Jauns**.
3. Dialoglodziņa **Jauns projekts** laukā **Projekta tips** atlasiet **Laiks un materiāls**.
4. Atlasiet projekta grupu. Projekta grupa definē grāmatošanas informāciju grupai piešķirtajiem projektiem.
5. Atlasiet **Izveidot projektu**.
6. Kad projekts ir izveidots, iestatiet projekta posmu **Notiek apstrāde**.

## <a name="create-a-budget-for-a-project"></a>Budžeta izveide projektam

Budžeta kategorijas tiek izmantotas, lai automātiski aprēķinātu rēķina summas katrai kategorijai pabeigtā darba procentuālajai daļai. Lai izveidotu budžeta kategorijas paredzamajām izmaksām, veiciet tālāk norādītās darbības.

1. Dodieties uz **Projekta pārvaldība un uzskaite** \> **Projekti** \> **Visi projekti**.
2. Lapā **Visi projekti** atlasiet vajadzīgo projektu un atveriet to.
3. Lapas **Projekti** darbību rūts cilnē **Plāns**, grupā **Budžets** atlasiet vienumu **Projekta budžets**.
4. Lapā **Projekta budžets** ievadiet prognozējamās izmaksas katrai projekta kategorijai.

## <a name="create-billing-rules-for-progress-billings"></a>Norēķinu kārtulu izveide progresa aprēķinam

1. Dodieties uz **Projekta pārvaldība un uzskaite** \> **Projekti** \> **Projekta līgumi**.
2. Lapā **Projekta līgumi** atlasiet un atveriet projekta līgumu.
3. Projekta līguma lapā, kopsavilkuma cilnē **Norēķinu kārtulas** atlasiet **Pievienot**.
4. Lapas **Norēķinu kārtulas** laukā **Rindas tips** atlasiet **Norise**.
5. Kopsavilkuma cilnes **Rēķina kārtulas rindas informācijā** laukā **Līguma vērtība** ievadiet līguma kopējo vērtību.
6. Laukā **Kategorija** atlasiet kategoriju, uz kuru grāmatot maksājuma darbību.
7. Laukā **Projekts** atlasiet projektu, kas izmanto šo norēķinu kārtulu.
8. Neobligāti: piešķiriet norēķinu kārtulu papildu projektiem. Kopsavilkuma cilnes **Projekts** sadaļā **Pieejamie projekti** atlasiet projektu un pēc tam noklikšķiniet uz labās puses bultiņas, lai pievienotu projektu sadaļā **Atlasītie projekti**.
9. Neobligāti: aprēķiniet procentu summu, ko klients ietur no maksājuma rēķinā. Attiecībā uz kopsavilkuma cilnes **Maksājuma saglabāšanas nosacījumi** atlasiet finansējuma avotu un pēc tam laukā **Ieturējuma procentuālā vērtība** ievadiet saglabāšanas procentus.
10. Lai projekta līgumam izveidotu papildu norēķinu kārtulas, atkārtojiet šīs darbības.


[!INCLUDE[footer-include](../includes/footer-banner.md)]