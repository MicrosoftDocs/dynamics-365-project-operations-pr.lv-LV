---
title: Finanšu dimensiju noklusējumi
description: Šajā tēmā ir sniegta informācija par to, kā iestatīt finanšu dimensiju noklusējumus.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: eec85b83cad4cd8fb6e0ec9c026c6a571bccf7f2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287382"
---
# <a name="financial-dimension-defaults"></a>Finanšu dimensiju noklusējumi

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations izmanto [Finanšu dimensiju](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) struktūru programmā Dynamics 365 Finance, lai sniegtu papildu ieskatus projekta apakšgrāmatas un virsgrāmatas darbībās.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]