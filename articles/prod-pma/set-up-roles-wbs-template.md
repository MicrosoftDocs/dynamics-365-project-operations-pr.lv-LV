---
title: Lomu iestatīšana darba sadalījuma struktūras veidnēs
description: Šajā tēmā ir sniegta informācija par lomas informācijas iestatīšanu darba sadalījuma struktūras veidnēs.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec952021f9da4d83520d29d68d040675f7933df7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997610"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Lomu iestatīšana darba sadalījuma struktūras veidnēs

[!include [banner](../includes/banner.md)]

Projekta vadītāji var iestatīt darba sadalījuma struktūras (WBS) veidnes, kuras viņi var lietot, veidojot WBS jauniem projektiem. Veidnes izveides laikā projektu vadītāji var pievienot lomas. Lai WBS veidnei piešķirtu lomu, izmantojiet šādu procedūru.

1. Atlasiet **Projekta pārvaldība un uzskaite** > **Iestatīšana** > **Projekti** > **Darba sadalījuma struktūras veidnes**.
2. Atlasiet atlasītās WBS veidnes **Informāciju**.
3. Sarakstā atlasiet uzdevumu un pēc tam laukā **Loma** atlasiet lomu, kuru piešķirt uzdevumam.

## <a name="work-with-a-wbs"></a>Darbs ar WBS

Varat izveidot jaunu WBS vai varat nokopēt WBS no esošas WBS veidnes. Projekta vadītājs var viegli pārvaldīt resursus, piešķirot lomas jauniem WBS uzdevumiem. Lomas var aizstāt vai nu pēc tam, kas resurss ir iegūts, vai pēc tam, kad darbam ar uzdevumu ir identificēts apstiprināts resurss. Šāda elastība ļauj projektu vadītājiem veikt šādus uzdevumus:

- Identificēt to resursu skaitu, kuri ir nepieciešami WBS darba pakotnēm.
- Aprēķināt projekta izmaksas.
- Noteikt provizorisko budžetu.
- Aprēķināt darbības ilgumu, pamatojoties uz lomām un resursiem.
- Izstrādāt projekta vadības plānus, pamatojoties uz pieejamo projekta informāciju.

WBS ir pievienotas papildu opcijas, lai labāk izmantotu resursu plānošanas funkcionalitāti.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opcija</th>
<th>Apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Resursu piešķīrumi</td>
<td>Skatiet WBS uzdevumiem piešķirtos resursus, datumus, stundu skaitu un rezervācijas veidu.</td>
</tr>
<tr class="even">
<td>Darba grupas automātiska ģenerēšana</td>
<td>Automātiski pievienojiet plānotos resursus, izmantojot lomas, kas ir saistītas ar uzdevumu. Finance automātiski iesaka plānotos resursu, izmantojot daudzkritēriju lēmumu analīzi, kas ir balstīta lomās. Pēc tam, kad WBS uzdevumiem ir iestatītas lomas un darbs (stundās) un pēc struktūras izlaišanas atlasiet <strong>Automātiski ģenerēt darba grupu</strong>. Nepieciešamais plānoto resursu skaits tiek pievienots WBS un cilnei <strong>Projekta un darba grupas plānošana</strong>.</td>
</tr>
<tr class="odd">
<td>Resurss (nolaižamais saraksts)</td>
<td>Lapā <strong>Palaist resursu piešķiri</strong> varat atlasīt resursus stingrajai vai vieglajai rezervēšanai, pamatojoties uz norādīto ilgumu. Varat pielāgot skatīšanas iestatījumus, lai redzētu un iestatītu resursu darbību ilgumu. Varat atlasīt un piešķirt resursus darba pakotnes līmenī, izmantojot šādas opcijas:
<ul>
<li><strong>Piekrist</strong> – Apstipriniet uzdevumam piešķirta resursa izmaiņas.</li>
<li><strong>Atcelt</strong> – Atceliet uzdevumam piešķirta resursa izmaiņas.</li>
<li><strong>Piešķirt automātiski</strong> — Pieejamais personāla resurss, kuram ir atbilstoša loma, tiek automātiski atlasīts un piešķirts atlasītajam uzdevumam.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Lapā **Visi projekti** atlasiet projektu **XYZ Jaunināšanas fāze 2**.
2. Atlasiet **Plāns** > **Darbības** > **Darba sadalījuma struktūra**.
3. Atlasiet **Jauns**, lai WBS pievienotu šādas pirmā līmeņa darbības:

    - Uzsākšana
    - Plānošana
    - Tiek izpildīts
    - Pārraudzība un vadība
    - Slēgt

4. Iestatiet datumus un darbu (stundās), kā parādīts šajā ilustrācijā.

    [![Datumu un darba iestatīšana](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Atlasiet **Uzsākšanas** uzdevuma rindu un pēc tam laukā **Loma** atlasiet **Vecākais projekta vadītājs**.
6. Atlasiet **Publicēt**.
7. Šīs pašas rindas laukā **Resurss** atlasiet **Daniels Goldšmits** un pēc tam atlasiet **Piekrist**.
8. Atlasiet **Plānošanas** uzdevuma rindu un pēc tam laukā **Loma** atlasiet **Biznesa analītiķis**.
9. Atlasiet **Publicēt** un pēc tam atlasiet **Automātiski ģenerēt komandu**.
10. Parādītajā ziņojuma lodziņā atlasiet **Jā**.
11. Laukā **Resurss** apstipriniet, ka vērtība ir **Biznesa analītiķis 1**.
12. Resursam **Biznesa analītiķis 1** atveriet uzmeklēšanu un atlasiet **Palaist resursu piešķires**. Pēc tam atlasiet uzdevuma darbinieku.
13. Atlasiet **Vieglā piešķire** &gt; **Pilnā noslodze**.

    > [!NOTE] 
    > Jūs nesaņemat brīdinājumu, ka norādītais resurss tagad ir 2, jo resursa numurs joprojām ir 1.

14. **Darba sadalījuma struktūras** lapā pārbaudiet resursa piešķiri WBS un pēc tam atlasiet **Saglabāt**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]