---
title: Apakšlīguma rindas resursi
description: Šajā tēmā ir paskaidrots, kā norādīt īpašos resursus, ko piegādātājs nodrošina konkrētai apakšlīguma laika rindai.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 48440f82170bde7f0a0a45f8f9849d688b232949
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323380"
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
4. Lapā **Jauns apakšlīguma rindas atskaites punkts** ievadiet nepieciešamo informāciju un pēc tam atlasiet **Saglabāt un aizvērt**.

Tālāk redzamajā tabulā ir paskaidroti apakšlīguma rindas resursu lauki.

| Lauks |  Apraksts |
| ----- | ------------ |
| Rezervējamais resurssss | Atlasiet rezervējamu "Līgumdarbinieka" tipa resursu, kuru vēlaties izmantot kā resursu apakšlīguma rindā. Ja vēl neesat izveidojis rezervējamu resursu līgumdarbiniekam, atstājiet šo lauku tukšu. Saglabājot ierakstu, tiek izveidots rezervējams resurss.  |
| Kontaktpersona | Ja lauks **Rezervējams resurss** ir tukšs, apakšlīguma rindas resursu var izveidot no esošas kontaktpersonas. Izmantojiet uzmeklēšanu, lai sistēmā skatītu aktīvo kontaktpersonu sarakstu. Atlasiet šī apakšlīguma piegādātāja kontaktpersonu. Atlasītā kontaktpersona tiek validēta ieraksta saglabāšanas laikā. Ja atlasītā kontaktpersona nav derīga kontaktpersona, ieraksts netiks saglabāts. Ja atlasītajai kontaktpersonai nav rezervējamu resursu, sistēma izveido atlasītajai kontaktpersonai rezervējamu resursu pirms apakšlīguma rindas resursa izveides. |
| Lietotājs | Ja lauks **Rezervējams resurss** ir tukšs, apakšlīguma rindas resursu var izveidot, atlasot aktīvu lietotāju. Izmantojiet uzmeklēšanu, lai sistēmā skatītu aktīvo lietotāju sarakstu. Ja atlasītajam lietotājam nav rezervējamu resursu, sistēma izveido atlasītajam lietotājam rezervējamu resursu pirms apakšlīguma rindas resursa izveides. |
| Sākuma datums | Datums, kad sāksies apakšlīguma darbinieka piešķire. Ja šis resurss ir rezervēts uz laiku, kas ir pirms šī datumu diapazona, tiks parādīts brīdinājums. |
| Beigu datums | Datums, kad beigsies apakšlīguma darbinieka piešķire. Ja šis resurss ir rezervēts uz laiku, kas ir pēc šī datumu diapazona, tiks parādīts brīdinājums. |
| Panākumi | Kopējais darba stundu skaits, ko apakšuzņēmēja darbinieks patērēs šajā apakšlīguma rindā. Ja šis resurss tiek rezervēts, pārsniedzot darbu, kas tam piešķirts šajā apakšlīgumā, tiks parādīts brīdinājums. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
