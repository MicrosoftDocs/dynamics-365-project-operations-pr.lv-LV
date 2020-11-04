---
title: Manuāla proformas rēķina izveide
description: Šajā tēmā ir sniegta informācija par manuāla proforma rēķina izveidi risinājumā Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5e93206737507bf6698a9746815c790d3dfc904
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/20/2020
ms.locfileid: "4080673"
---
# <a name="creating-a-manual-proforma-invoice"></a>Manuāla proformas rēķina izveide

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Risinājumā Dynamics 365 Project Operations proforma rēķinus var izveidot manuāli, ja nepieciešams. Proforma rēķinu manuāli var izveidot no saraksta lapas **Projekta līgumi** vai informācijas lapas **Projekta līgums**.

##  <a name="project-contracts-list-page"></a>Saraksta lapa Projekta līgums

Saraksta lapā **Projekta līgums** atlasiet vienu vai vairākus projekta līgumus un izveidojiet rēķinus visiem atlasītajiem ierakstiem.

Sistēma pārbauda, lai skatītu, kuriem no atlasītajiem projekta līgumiem ir rezerve **Gatavs rēķina izrakstīšanai** ar datumu pirms šodienas datuma. No šiem līgumiem sistēma izveido proforma rēķinu melnrakstus. Ja projekta līgumam ir vairāki klienti, katram klientam var izveidot vienu rēķinu, kā arī vairākus rēķinus katram projekta līgumam.

Visi izveidotie projekta rēķini ir pieejami apgabala **Pārdošana** lapas **Rēķins** sadaļā **Norēķini**.

## <a name="project-contract-details-page"></a>Informācijas lapa Projekta līgums

Proforma rēķinu var izveidot arī no informācijas lapas **Projekta līgums** , kas izveido rēķinu šim konkrētajam projekta līgumam. Sistēma pārbauda, vai projekta līgumam ir rezerve **Gatavs rēķina izrakstīšanai** ar datumu pirms šodienas datuma. No šiem līgumiem sistēma izveido proforma rēķinu melnrakstus, pamatojoties uz klientu skaitu katrā rēķina rindā.

Ja ir izveidots viens proforma rēķins, tiek atvērta lapa **Rēķins**. Ja šim projekta līgumam ir izveidoti vairāki rēķini, tiek atvērta saraksta lapa **Rēķini** , lai parādītu visus izveidotos rēķinus.
