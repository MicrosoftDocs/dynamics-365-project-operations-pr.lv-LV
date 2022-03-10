---
title: Finanšu dimensiju noklusējumi
description: Šajā tēmā ir sniegta informācija par to, kā iestatīt finanšu dimensiju noklusējumus.
author: sigitac
ms.date: 12/14/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8c1eb71d13ca7fc59118d15fef7ac914577b3b0e
ms.sourcegitcommit: fe5610464fdb5be756aa6a6a5b3c9a991dea0ed8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/15/2021
ms.locfileid: "7922947"
---
# <a name="financial-dimension-defaults"></a>Finanšu dimensiju noklusējumi

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations izmanto [Finanšu dimensiju](/dynamics365/finance/general-ledger/financial-dimensions) struktūru programmā Dynamics 365 Finance, lai sniegtu papildu ieskatus projekta apakšgrāmatas un virsgrāmatas darbībās.

Noklusējuma finanšu dimensijas var iestatīt klientam, projekta finansējuma avotam, atskaites punktam, projekta līguma rindai vai projektam.

## <a name="define-default-financial-dimensions-for-a-customer"></a>Debitora noklusējuma finanšu dimensiju definēšana

Debitoru dimensiju noklusējuma iestatījumi ir norādīti finanšu sistēmā. Lai iestatītu dimensiju noklusējuma iestatījumus, paveiciet tālāk norādītās darbības.

1. Dodieties uz **Debitori** > **Klienti** > **Visi klienti**.
2. Lapas **Klienti** cilnē **Finanšu dimensijas** iestatiet finanšu dimensiju vērtības noteiktajam klientam.

## <a name="define-default-financial-dimensions-for-project-contracts"></a>Projekta līguma noklusējuma finanšu dimensiju definēšana

Projekta līgumi tiek izveidoti un uzturēti pakalpojumā Common Data Service (CDS). Projekta līgumu uzskaites atribūti tiek iestatīti Finanšu modulī **Projekta pārvaldība un uzskaite**.

### <a name="set-financial-dimensions-for-a-project-funding-source"></a>Finanšu dimensiju iestatīšana projekta finansējuma avotam

1. Dodieties uz **Projekta pārvaldība un uzskaite** > **Projekti** > **Projekta līgumi**.
2. Atlasiet ierakstu, kuru vēlaties atjaunināt, un cilnē **Projekta līgums** atlasiet **Rādīt noklusējuma uzskaiti**.
3. Izvērsiet sadaļu **Saistītā informācija** un atlasiet cilni **Finansējuma avoti**.
4. Iestatiet finanšu dimensijas noklusējumus. Ņemiet vērā, ka finanšu dimensiju noklusējuma vērtība ir no klienta uzņēmuma.

### <a name="set-financial-dimensions-for-a-project-contract-line"></a>Finanšu dimensiju iestatīšana projekta līguma rindai

1. Dodieties uz **Projekta pārvaldība un uzskaite** > **Projekti** > **Projekta līgumi**.
2. Atlasiet ierakstu, kuru vēlaties atjaunināt, un cilnē **Projekta līgums** atlasiet **Rādīt noklusējuma uzskaiti**.
3. Izvērsiet sadaļu **Saistītā informācija** un atlasiet cilni **Līguma rindas**.
4. Iestatiet finanšu dimensijas noklusējumus. Finanšu dimensiju noklusējumi ir piemērojami un tos var izmantot tikai ar fiksētas cenas (atskaites punkta) līguma rindām.

Šie noklusējumi tiek izmantoti saistītā projekta uzņēmuma transakcijās un rēķina rindās.

## <a name="define-default-financial-dimensions-for-projects"></a>Projektu noklusējuma finanšu dimensiju definēšana

Projekti tiek izveidoti un uzturēti pakalpojumā CDS. Projektu uzskaites atribūti tiek iestatīti Finanšu modulī **Projekta pārvaldība un uzskaite**.

1. Dodieties uz **Projekta pārvaldība un uzskaite** > **Projekti** > **Visi projekti**.
2. Atlasiet ierakstu, kuru vēlaties atjaunināt, un cilnē **Projekts** atlasiet **Rādīt noklusējuma uzskaiti**.
3. Izvērsiet sadaļu **Saistītā informācija** un atlasiet cilni **Iestatīšana**.
4. Iestatiet finanšu dimensijas noklusējumus. Ņemiet vērā, ka finanšu dimensiju noklusējuma vērtība ir no klienta uzņēmuma. Ja projekts ir saistīts ar līguma rindu ar vairākiem projekta līguma klientiem, primārais klients tiek izmantots noklusējuma finanšu dimensijās.

Projektu noklusējuma finanšu dimensijas izmanto, lai iestatītu žurnāla rindas noklusējuma vērtības laika, izdevumu un maksu darbībām **Project Operations integrācijas žurnālā** un ar to saistītajās projekta rēķina rindās.

## <a name="apply-financial-dimensions-for-project-time-entries"></a>Attiecināt projekta laika ierakstu finanšu dimensijas
Lai attiecinātu projekta laika ierakstiem finanšu dimensijas, ņemiet vērā, ka noklusējuma dimensijas vērtība ir balstīta uz šādu secību:

1. Resursa
2. Project
3. Finansējuma avots

Piemēram, ja resursam ir norādīta noklusējuma dimensija, tā tiks lietota projektā norādītajā noklusējumā. Tāpat noklusējuma projekta dimensija tiks lietota noklusējuma, kas norādīta finansējuma avotā.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
