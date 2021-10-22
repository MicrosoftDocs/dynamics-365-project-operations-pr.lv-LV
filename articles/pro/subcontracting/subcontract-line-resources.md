---
title: Apakšlīguma rindas resursi
description: Šajā tēmā ir paskaidrots, kā norādīt īpašos resursus, ko piegādātājs nodrošina konkrētai apakšlīguma laika rindai.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4a929b985a51ab49d3e34ce4a5c277af4c05c216
ms.sourcegitcommit: d507a75a19c992a9421e4f3605162a2faa84a445
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2021
ms.locfileid: "7558466"
---
# <a name="subcontract-line-resources"></a>Apakšlīguma rindas resursi

[!include [banner](../../includes/dataverse-preview.md)]

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Programmā Dynamics 365 Project Operations piegādātājs var norādīt resursus, kas tiks izmantoti, lai nodrošinātu resursu noslodzi, kas tiek iegādāta apakšlīguma laika rindā.

## <a name="create-subcontract-line-resources"></a>Apakšlīguma rindas resursu izveide

Lai izveidotu apakšlīguma rindas resursus, veiciet tālāk norādītās darbības.

1. Navigācijas rūtī atlasiet **Apakšlīgumi** un atveriet apakšlīgumu, ar kuru vēlaties strādāt.
2. Atveriet apakšlīguma laika rindu, kurā vēlaties norādīt piegādātāja resursus.
3. Cilnes **Apakšlīguma rindas resursi** apakšrežģī atlasiet **+ Jauns apakšlīguma rindas resurss**.
4. Lapā **Jauns apakšuzņēmēja līguma rindas resurss** ievadiet nepieciešamo informāciju un pēc tam atlasiet **Saglabāt un aizvērt**.

Tālāk redzamajā tabulā ir paskaidroti apakšlīguma rindas resursu lauki.

| Lauks | Apraksts | Funkcionālā ietekme |
| ----- | ----------- | ----------------- |
| Rezervējamais resurssss | Atlasiet rezervējamu **Līguma darbinieka** tipa resursu, kuru vēlaties izmantot, kā resursu apakšuzņēmēja līguma rindā.| Ja līguma darbiniekam neesat izveidojis rezervējamu resursu, atstājiet šo lauku tukšu. Saglabājot ierakstu, tiks izveidots rezervējams resurss.  |
| Kontaktpersona | Apakšuzņēmēja līguma rindas resursu var izveidot no esošas kontaktpersonas. Izmantojiet uzmeklēšanu, lai sistēmā skatītu aktīvo kontaktpersonu sarakstu. Atlasiet šī apakšlīguma piegādātāja kontaktpersonu. Ja atlasītā kontaktpersona nav derīga pārdevēja kontaktpersona apakšuzņēmēja līgumā, tad apakšuzņēmēja līguma rindas resursa ieraksts netiks saglabāts.| Ja atlasītajai kontaktpersonai nav rezervējamu resursu, sistēma izveido atlasītajai kontaktpersonai rezervējamu resursu pirms apakšlīguma rindas resursa izveides. |
| Lietotājs | Apakšuzņēmēja līguma rindas resursu var izveidot, atlasot aktīvu lietotāju. Izmantojiet uzmeklēšanu, lai sistēmā skatītu aktīvo lietotāju sarakstu.| Ja atlasītajam lietotājam nav rezervējamu resursu, sistēma izveido atlasītajam lietotājam rezervējamu resursu pirms apakšlīguma rindas resursa izveides. |
| Sākuma datums | Datums, kad sāksies apakšlīguma darbinieka piešķire.| Ja šis resurss ir rezervēts uz laiku, kas ir pirms šī datumu diapazona, tiks parādīts brīdinājums. |
| Beigu datums | Datums, kad beigsies apakšlīguma darbinieka piešķire.| Ja šis resurss ir rezervēts uz laiku, kas ir pēc šī datumu diapazona, tiks parādīts brīdinājums. |
| Panākumi | Kopējais darba stundu skaits, ko darbinieks patērēs šajā apakšuzņēmēja līguma rindā, par kuru ir noslēgts līgums.| Ja šis resurss tiek rezervēts, pārsniedzot šajā apakšuzņēmēja līgumā piešķirto stundu skaitu, tad tiks parādīts brīdinājums. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
