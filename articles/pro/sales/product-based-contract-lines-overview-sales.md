---
title: Uz produktiem balstītu līgumu rindu pārskats — Lite
description: Šajā tēmā ir sniegta informācija par līguma rindām, kuras ir balstītas uz produktu.
author: rumant
ms.date: 10/07/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8006e90e0d4fdf02042f26b261775a92f87f47ca
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598221"
---
# <a name="product-based-contract-lines-overview---lite"></a>Uz produktiem balstītu līgumu rindu pārskats — Lite

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Programmā Dynamics 365 Project Operations varat izveidot uz produktu balstītas līguma rindas. Uz produktu balstītas līguma rindas var būt manuāli izveidotas rindas, vai tās var būt vienumi no produktu kataloga.

## <a name="product-catalog"></a>Preču katalogs

Produktiem preču katalogā ir noklusējuma vienība un vienību grupa. Ja vairākiem produktiem ir vienāda atribūtu kopa, varat izveidot produktu saimi, kurai arī ir šie atribūti. Visi produkti vienā produktu saimē pārmanto vienādu atribūtu kopu.

Piemēram, uzņēmums pārdod abonementa licences dažādu veidu programmatūrai. Katrai abonējamajai programmatūrai ir divi tālāk norādītie atribūti.

- Lietotāju skaits
- Abonementa ilgums (mēnešos)

Lai uzturētu šāda tipa katalogu, izveidojiet produktu saimi, kuras nosaukums ir **Abonēšanas programmatūra**. Pievienojiet atribūtus **Lietotāju skaits** un **Abonementa ilgums** produktu saimei. Pēc tam pievienojiet **Abonementa programmatūra** produktu saimei atsevišķus produktus.

## <a name="add-product-catalog-items-to-a-project-contract"></a>Produktu kataloga vienumu pievienošana projekta līgumam

Projekta līgumam ir sadaļas divu tipu rindām: uz projektu balstītām rindām un uz produktu balstītām rindām. Produktu bāzētās rindās ir iekļauti visi līguma produktu cenrāža produkti un vienības. Var pievienot produktus, kas nav iekļauti līguma produktu cenrādī.

Varat atlasīt produktus no citiem cenrāžiem vai tieši no preču kataloga. Ja produktus atlasāt tieši no kāda preču kataloga, lai iegūtu produkta pārdošanas cenu, tiek izmantots šī produkta noklusējuma cenrādis. Ja noklusējuma cenrādis nav iestatīts, cena tiek iestatīta uz 0 (nulle).

Ja līguma rinda ir balstīta uz preču katalogu, pārdošanas cenu varat pārlabot tieši rindā. Līguma rindai ir lauks **Cenu noteikšana** ar divām vērtībām:

- **Pārlabot izcenojumu**
- **Izmantot noklusējumu**

Ja iestatāt lauku **Cenu noteikšana** uz **Pārlabot cenu noteikšanu**, noklusējuma cena nav iestatīta. Ievadiet produkta cenu līguma rindā. Ja iestatījāt lauku uz **Izmantotu noklusējumu**, tiek izmantota noklusējuma pārdošanas cena un lauku nevar rediģēt.

Pēc Project Operations instalēšanas noklusētās pārdošanas cenas tiek ievadītas līguma produktu rindās. Lauks **Cenu noteikšana** tiek iestatīts uz **Pārlabot cenu noteikšanu**, lai jūs varētu rediģēt noteiktā cenu līguma rindās. Šī ir Project Operations specifiska pārlabošana uz produktu bāzētu līniju uzvedībai risinājumā Dynamics 365 Sales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]