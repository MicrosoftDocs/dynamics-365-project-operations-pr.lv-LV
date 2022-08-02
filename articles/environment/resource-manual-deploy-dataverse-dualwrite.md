---
title: Manuāla programmas Project Operations Dataverse ar duālās rakstīšanas atbalstu izvietošana
description: Šajā rakstā ir paskaidrots, kā manuāli izvietot programmu Project Operations Dataverse, lai tā atbalstītu dubultrakstīšanu.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: a25e2a59f1c069057c6689825ce52b13d842af71
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028573"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a>Manuāla programmas Project Operations Dataverse ar duālās rakstīšanas atbalstu izvietošana

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Šajā rakstā ir paskaidrots, kā manuāli izvietot Microsoft Dynamics 365 Project Operations Microsoft Dataverse, lai tā atbalstītu dubultrakstīšanu. Project Operations konstatē vides konfigurāciju un pievieno papildu atbalstu attiecībā duālajai rakstīšanai, ja tiek izpildīti priekšnosacījumi.

Izvietošanas laikā, izmantojot Microsoft Dynamics Lifecycle Services (LCS), ja esat izpildījis šajā rakstā sniegtos norādījumus, varat izlaist integrācijas izvietošanu Microsoft Power Platform (iepriekš zināma kā Common Data Service vide).

Project Operations izvietošanas procesam Dataverse, lai tas atbalstītu duālo rakstīšanu, jāveic četras galvenās darbības.

1. [Jaunas vides izveide programmā Dataverse, kurā tiek atbalstīta duālā rakstīšana](#create).
2. [Duālās rakstīšanas priekšnosacījumu pievienošana videi](#prerequisites).
3. [Programmas Project Operations Dataverse pievienošana](#dataverse).
4. [Vižu saistīšana](#link).

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a>Izveidojiet jaunu vidi programmā Dataverse, kurā tiek atbalstīta duālā rakstīšana.

Lai pabeigtu šo procedūru, jāpiesakās kā administratoram.

1. Atveriet [Power Platform administrēšanas centru](https://admin.powerplatform.com) un piesakieties kā administrators.
2. Izveidojiet jaunu vidi un piešķiriet tai nosaukumu.
3. Atlasiet vides tipu. Ja reģistrējāties izmēģinājumversijas piedāvājumam, atlasiet **Izmēģinājumversija (abonementa)**.
4. Apstipriniet izvietošanas reģionu.
5. Iespējojiet opciju **Izveidot datu bāzi šai videi**. 
6. Apstipriniet valodu un pēc tam apstipriniet, vai valūta atbilst jūsu finanšu un operāciju lietotņu valūtai.
7. Iespējojiet opciju **Dynamics 365 programmas** un pārliecinieties, ka lauks **Automātiski izvietot šīs programmas** ir iestatīts kā **Neviens**.
8. Ja ir nepieciešama drošības grupa, pievienojiet to.
9. Atlasiet **Saglabāt**, lai izveidotu vidi.
10. Uzgaidiet, līdz izvietošana ir pabeigta un vide sasniedz statusu **Gatavs**.

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a>Duālās rakstīšanas priekšnosacījumu pievienošana videi

Duālās rakstīšanas atbalsts ietver papildu laukus, kas tiek pievienoti galvenajām entītijām, piemēram, entītijai **Uzņēmums**. Ja pievienojat satura rakstīšanas atbalstu esošai videi, iespējams, būs jāatjaunina dati, lai iespējotu atbalstu. Informāciju par to, kā veikt datu palaišanu, skatiet sadaļā [Uzņēmuma datu palaišana](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data). Papildinformāciju par duālo rakstīšanu skatiet sadaļā [Duālās rakstīšanas sistēmas prasības](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).

Izpildiet šo procedūru, lai pievienotu videi duālās rakstīšanas priekšnosacījumus.

1. Atveriet tikko izveidoto vidi un pēc tam atveriet **Resurss** \> **Dynamics 365 programmas**.
2. Programmu sarakstā atlasiet **Duālās rakstīšanas pamata risinājums** un instalējiet to.
3. Uzgaidiet, līdz instalēšana ir pabeigta. Pēc tam programmu sarakstā atlasiet **Duālās rakstīšanas saskaņotais risinājums** un instalējiet to.

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a>Programmas Project Operations Dataverse pievienošana

Šo procedūru var izpildīt tikai tad, ja pirms Project Operations instalēšanas ir izpildītas iepriekšējās procedūras. Instalācijas laikā sistēma analizē vides konfigurāciju un pievieno atbalstu duālajai rakstīšanai, ja tā ir nepieciešama.

1. Atveriet iepriekš izveidoto vidi un pēc tam atveriet **Resurss** \> **Dynamics 365 programmas**.
2. Programmu sarakstā atlasiet **Microsoft Dynamics 365 Project Operations** un instalējiet to.

## <a name="link-your-environments"></a><a name="link"></a>Vižu saistīšana

Dataverse Kad vide ir izvietota, varat iestatīt saiti savās finanšu un operāciju programmās. Izpildiet darbības, kas norādītas sadaļā [Duālās rakstīšanas vedņa izmantošana vižu saistīšanai](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).
