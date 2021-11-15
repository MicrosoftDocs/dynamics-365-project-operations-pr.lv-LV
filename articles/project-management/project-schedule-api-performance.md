---
title: Projektu plānošanas API veiktspēja
description: Šajā tēmā ir sniegta informācija par projektu plānošanas API veiktspējas kritērijiem un paraugprakses piemēri optimālai izmantošanai.
author: ruhercul
ms.date: 11/03/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a1abadbae044ccbd40077c6937262f0f17387bad
ms.sourcegitcommit: 5c536cf05e2cbfc1d15982e4695d726064a074da
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/04/2021
ms.locfileid: "7750611"
---
# <a name="project-schedule-api-performance"></a>Projektu plānošanas API veiktspēja

_**Attiecas uz:** Project Operations resursu balstītiem / krājumu nebalstītiem scenārijiem, Lite izvietošana — darījums ar proformas rēķinu izrakstīšanu Project for the web_

Šajā tēmā ir sniegta informācija par projektu plānošanas lietojumprogrammu programmēšanas interfeisu (API) veiktspējas kritērijiem un paraugprakses piemēri optimālai izmantošanai.

## <a name="project-scheduling-service"></a>Projektu plānošanas pakalpojums
Projektu plānošanas pakalpojums ir vairāku nomnieku pakalpojums, kas tiek izpildīts platformā Microsoft Azure. Šī platforma ir izstrādāta, lai uzlabotu mijiedarbību, nodrošinot ātru un ērtu lietošanu darbā ar projektiem. Uzlabojums tiek sasniegts, pieņemot izmaiņu pieprasījumus, apstrādājot tos un pēc tam nekavējoties atgriežot rezultātus. Pakalpojums asinhroni pastāv platformā Dataverse un nebloķē lietotājus citu operāciju veikšanai.

Projektu plānošanas API izmanto projektu plānošanas pakalpojumu, lai izpildītu pieprasījumus, kas detalizētāk aprakstīti šīs tēmas turpmākajās sadaļās.

Projektu plānošanas API ir izstrādāti darbam ar šādām darba sadalījuma struktūras (WBS) entītijām:

  - Project
  - Projekta uzdevums
  - Projekta uzdevuma atkarība
  - Projekta grupas dalībnieks
  - Resursu piešķiršana
  
Tiek atbalstīti gan iepriekš aizpildīti lauki, gan pielāgoti lauki. Ja vien nav norādīts citādi, tiek atbalstītas visas bieži lietotās operācijas, piemēram, izveide, atjaunināšana un dzēšana. Papildinformāciju skatiet sadaļā [Projektu plānošanas API izmantošana operāciju veikšanai un entītiju plānošanai](schedule-api-preview.md).

Kā daļa no projektu plānošanas API ir pievienots darba vienības modelis. Šo shēmu sauc par OperationSet, un to var izmantot, kad vairāki pieprasījumi ir jāapstrādā vienā transakcijā.

Nākamajā ilustrācijā parādīta plūsma, kas partnerim būs pieejama šī līdzekļa lietošanas laikā.

![Dataverse un projektu plānošanas pakalpojuma plūsma.](./media/dataverse-project-scheduling-service-flow.png)

**1. darbība**: klients veic API izsaukumu atvērto datu protokola (OData) galapunktā platformā Dataverse, lai izveidotu OperationSet.

**2. darbība**: pēc jauna OperationSet izveides tiek atgriezta vērtība **OperationSetId**.

**3. darbība**: klients izmanto **OperationSetId** vērtību, lai veiktu citu projektu plānošanas API pieprasījumu. Rezultāts ir izveides, atjaunināšanas vai dzēšanas pieprasījums plānošanas entītijai. Pēc šī pieprasījuma iesniegšanas tiek veikta metadatu validācija. Ja validācija neizdodas, pieprasījums tiek pabeigts un tiek atgriezta kļūda.

**4.a–4.c** darbība: šīs darbības apzīmē posmu ACCEPT. Klients izsauc **ExecuteOperationSetV1** API, kas nosūta visas projektu plānošanas pakalpojuma izmaiņas vienā partijā. Projektu plānošanas pakalpojums veic validāciju partijas pieprasījumiem. Validācijas kļūmes atsauc partiju un izsaucējam atgriež izņēmumu. Ja projektu plānošanas pakalpojums sekmīgi akceptē partiju, OperationSet statuss tiek atjaunināts, lai atspoguļotu to, ka OperationSet tiek apstrādāts projekta plānošanas pakalpojumā.

**5. darbība**. Šī darbība norāda uz posmu PERSIST. Projektu plānošanas pakalpojums asinhroni raksta partiju platformas Dataverse transakcijā. Ja rakstīšanas operācija ir sekmīga, OperationSet tiek atzīmēta kā **Pabeigta**. Jebkādu kļūdu gadījumā transakcija un partija netiek izpildīta, un OperationSet ir atzīmēts kā **Neizdevās**.

## <a name="performance-methodology"></a>Veiktspējas metodoloģija
Izpildes laiks tiek definēts kā laiks no **ExecuteOperationSetV1** API izsaukšanas līdz projektu plānošanas pakalpijuma datu ievades pabeigšanai platformā Dataverse. Visas operācijas tiek veiktas 2200 reizes, un tiek ziņots par P99 izpildes laiku. Tiek mērītas viena ieraksta un lielapjoma operācijas.

Viena ieraksta operācijai OperationSet ietver vienu pieprasījumu. Lielapjoma operācijas ietver 20, 50 vai 100 pieprasījumu. Katra lielapjoma operācija tiek ziņota atsevišķi.

Šīs operācijas tiek palaistas, izmantojot UR 15 Project Operations Lite izvietojumu Ziemeļamerikā.

## <a name="results"></a>Rezultāti
### <a name="create-operations"></a>Operāciju izveide
#### <a name="single-record-create-operations"></a>Viena ieraksta izveides operācijas
Tālāk sniegtajā tabulā ir norādīti atsevišķa ieraksta izveides izpildes laiki. Laiks ir norādīti sekundēs.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Ieraksta&nbsp;&nbsp;&nbsp;tips</th>
    <th class="tg-0lax" colspan="2">Laiks</th>
  </tr>
  <tr>
    <th class="tg-0lax">Obligātie lauki</th>
    <th class="tg-0lax">Visi atbalstītie lauki</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">2.5</td>
    <td class="tg-0lax">3.78</td>
  </tr>
  <tr>
    <td class="tg-0lax">Uzdevums</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Piešķiršana</td>
    <td class="tg-0lax">9.19</td>
    <td class="tg-0lax">9.19</td>
  </tr>
  <tr>
    <td class="tg-0lax">Darba grupas dalībnieks</td>
    <td class="tg-0lax">0.84</td>
    <td class="tg-0lax">4.2</td>
  </tr>
  <tr>
    <td class="tg-0lax">Atkarība</td>
    <td class="tg-0lax">8.84</td>
    <td class="tg-0lax">8.84</td>
  </tr>
</tbody>
</table>

#### <a name="bulk-create-operations"></a>Lielapjoma izveides operācijas
Tālāk sniegtajā tabulā ir norādīti daudzu ierakstu izveides izpildes laiki. Korporācija Microsoft vienā OperationSet noteica izpildes laikus 20,50 un 100 ierakstu izveidei. Laiks ir norādīti sekundēs.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Ieraksta&nbsp;&nbsp;&nbsp;tips</th>
    <th class="tg-0lax" colspan="6">Laiks</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 ierakstu</th>
    <th class="tg-0lax" colspan="2">50 ierakstu</th>
    <th class="tg-0lax" colspan="2">100 ierakstu</th>
  </tr>
  <tr>
    <th class="tg-0lax">Obligātie lauki</th>
    <th class="tg-0lax">Visi atbalstītie lauki</th>
    <th class="tg-0lax">Obligātie lauki</th>
    <th class="tg-0lax">Visi atbalstītie lauki</th>
    <th class="tg-0lax">Obligātie lauki</th>
    <th class="tg-0lax">Visi atbalstītie lauki</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Uzdevums</td>
    <td class="tg-0lax">19.92</td>
    <td class="tg-0lax">38.35</td>
    <td class="tg-0lax">36.67</td>
    <td class="tg-0lax">99.13</td>
    <td class="tg-0lax">116.77</td>
    <td class="tg-0lax">174.06</td>
  </tr>
  <tr>
    <td class="tg-0lax">Piešķiršana</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">69.38</td>
    <td class="tg-0lax">69.38</td>
  </tr>
  <tr>
    <td class="tg-0lax">Atkarība</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">176.89</td>
    <td class="tg-0lax">176.89</td>
  </tr>
</tbody>
</table>

> [!NOTE] 
> Šajā tabulā nav ietvertas lielapjoma izveides operācijas entītijām **Project** un **Team Member**, jo to izpildes laiks ataino izpildes laiku, kad API veido vienu ierakstu un ir izsaukts vairākas reizes. Šie API tiek palaisti nekavējoties platformā Dataverse.

Šajā ilustrācijā redzams izpildes laiku secība entītijām **Task**, **Assignment** un **Dependency**, ja tiek veidoti 20, 50 un 100 ieraksti un tiek izmantoti visi atbalstītie lauki.

![Ierakstu izvedes izpildes laika grafiks.](./media/create-record-execution-time.png)

### <a name="update-operations"></a>Operāciju atjaunināšana
#### <a name="single-record-update-operations"></a>Viena ieraksta atjaunināšanas operācijas
Tālāk sniegtajā tabulā ir norādīti atsevišķa ieraksta atjaunināšanas izpildes laiki. Laiks ir norādīti sekundēs.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Ieraksta&nbsp;&nbsp;&nbsp;tips</th>
    <th class="tg-0lax" colspan="2">Laiks</th>
  </tr>
  <tr>
    <th class="tg-0lax">Obligātie lauki </th>
    <th class="tg-0lax">Visi atbalstītie lauki</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">9.53</td>
    <td class="tg-0lax">13.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Uzdevums</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Darba grupas dalībnieks</td>
    <td class="tg-0lax">9</td>
    <td class="tg-0lax">8.96</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Atjaunināšanas operācijas netiek atbalstītas entītijām **Resource Assignments** un **Project Task Dependency**.

#### <a name="bulk-update-operations"></a>Lielapjoma atjaunināšanas operācijas
Tālāk sniegtajā tabulā ir norādīti daudzu ierakstu atjaunināšanas izpildes laiki. Korporācija Microsoft vienā OperationSet noteica izpildes laikus 20,50 un 100 ierakstu atjaunināšanai. Laiks ir norādīti sekundēs.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Ieraksta&nbsp;&nbsp;&nbsp;tips</th>
    <th class="tg-0lax" colspan="6">Laiks</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 ierakstu</th>
    <th class="tg-0lax" colspan="2">50 ierakstu</th>
    <th class="tg-0lax" colspan="2">100 ierakstu</th>
  </tr>
  <tr>
    <th class="tg-0lax">Obligātie lauki</th>
    <th class="tg-0lax">Visi atbalstītie lauki</th>
    <th class="tg-0lax">Obligātie lauki</th>
    <th class="tg-0lax">Visi atbalstītie lauki</th>
    <th class="tg-0lax">Obligātie lauki</th>
    <th class="tg-0lax">Visi atbalstītie lauki</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Uzdevums</td>
    <td class="tg-0lax">8.91</td>
    <td class="tg-0lax">38.71</td>
    <td class="tg-0lax">20.92</td>
    <td class="tg-0lax">87.13</td>
    <td class="tg-0lax">36.68</td>
    <td class="tg-0lax">190.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Darba grupas dalībnieks</td>
    <td class="tg-0lax">20.52</td>
    <td class="tg-0lax">26.06</td>
    <td class="tg-0lax">41.93</td>
    <td class="tg-0lax">44.51</td>
    <td class="tg-0lax">38.63</td>
    <td class="tg-0lax">66.53</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Atjaunināšanas operācijas netiek atbalstītas entītijām **Resource Assignments** un **Project Task Dependency**.

Šajā ilustrācijā redzams izpildes laiku secība entītijām Task un Team Member, ja tiek atjaunināti 20, 50 un 100 ieraksti un tiek izmantoti visi atbalstītie lauki.

![Ierakstu atjaunināšnas izpildes laika grafiks.](./media/update-record-execution-time.png)

### <a name="delete-operations"></a>Dzēšanas operācijas
#### <a name="single-record-delete-operations"></a>Viena ieraksta dzēšanas operācijas
Tālāk sniegtajā tabulā ir norādīti atsevišķa ieraksta dzēšanas izpildes laiki. Laiks ir norādīti sekundēs.

| Ieraksta tips | Laiks  |
|-------------|-------|
| Uzdevums        | 20.12 |
| Piešķiršana  | 10.86 |
| Darba grupas dalībnieks | 12.52 |
| Atkarība  | 20.89 |

> [!NOTE]
> Netiek atbalstītas dzēšanas operācijas entītijai **Project**.

#### <a name="bulk-delete-operations"></a>Lielapjoma dzēšanas operācijas
Tālāk sniegtajā tabulā ir norādīti daudzu ierakstu dzēšanas izpildes laiki. Korporācija Microsoft vienā OperationSet noteica izpildes laikus 20,50 un 100 ierakstu dzēšanai. Laiks ir norādīti sekundēs.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Ieraksta&nbsp;&nbsp;&nbsp;tips</th>
    <th class="tg-0lax" colspan="3">Laiks</th>
  </tr>
  <tr>
    <th class="tg-0lax">20 ierakstu</th>
    <th class="tg-0lax">50 ierakstu</th>
    <th class="tg-0lax">100 ierakstu</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Uzdevums</td>
    <td class="tg-0lax">20.91</td>
    <td class="tg-0lax">67.43</td>
    <td class="tg-0lax">71.96</td>
  </tr>
  <tr>
    <td class="tg-0lax">Piešķiršana</td>
    <td class="tg-0lax">11.75</td>
    <td class="tg-0lax">25.79</td>
    <td class="tg-0lax">47.66</td>
  </tr>
  <tr>
    <td class="tg-0lax">Darba grupas dalībnieks</td>
    <td class="tg-0lax">9.78</td>
    <td class="tg-0lax">39.73</td>
    <td class="tg-0lax">24.33</td>
  </tr>
  <tr>
    <td class="tg-0lax">Atkarība</td>
    <td class="tg-0lax">24.61</td>
    <td class="tg-0lax">54.9</td>
    <td class="tg-0lax">109.16</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Netiek atbalstītas dzēšanas operācijas entītijai **Project**.

Šajā ilustrācijā redzams izpildes laiku secība entītijām **Task**, **Assignment**, **Team Member** un **Dependency**, ja tiek dzēsti 20, 50 un 100 ieraksti.

![Ierakstu dzēšanas izpildes laika grafiks.](./media/delete-record-execution-time.png)

## <a name="observations"></a>Novērojumi
Katrai ierakstu operācijai **ExecuteOperationSet** API aptuveni 800 milisekunžu laikā nosūta pieprasījumu projektu plānošanas pakalpojumam. Projektu plānošanas pakalpojums pēc tam aptuveni piecās sekundēs apstrādā lietderīģo slodzi un izauc Dataverse. Pārējais izpildes laiks tiek pavadīts, izpildot biznesa loģiku un rakstot datus datu bāzē platformā Dataverse.

Izveidojot, atjauninot vai dzēšot 100 ierakstus, **ExecuteOperationSet** API aptuveni trīs sekundēs nosūta pieprasījumu uz projekta plānošanas pakalpojumu. Projektu plānošanas pakalpojums pēc tam aptuveni piecās sekundēs apstrādā pieprasījumus un izauc Dataverse. Lielapjoma operācijām ir vienreiz jāsamaksā **projektu plānošanas pakalpojuma nodoklis** par visiem OperationSet ierakstiem. Tāpēc lielapjoma operāciju vidējais izpildes laiks ir būtiski zemāks nekā viena ieraksta operācijām.

## <a name="scenarios"></a>Scenāriji
Tālāk sniegtajā tabulā ir norādīti izpildes laiki, kad projektu plānošanas API tiek izmantoti, lai izpildītu noteiktus scenārijus. Laiks ir norādīti sekundēs.

| Scenārijs                                                                   | Laiks  |
|----------------------------------------------------------------------------|-------|
| Izveidojiet projektu, kurā ir 40 uzdevumu.                                      | 36.01 |
| Izveidojiet projektu, kurā ir 40 uzdevumu un 20 atkarību.                  | 38.11 |
| Izveidojiet projektu, kurā ir 40 uzdevumu un 30 piešķīrumu.                   | 60.17 |
| Izveidojiet projektu, kurā ir 40 uzdevumu, 20 atkarību un 30 piešķīrumu. | 60.27 |

## <a name="best-practices"></a>Paraugprakse
Pamatojoties uz iepriekšējiem scenārija rezultātiem, API darbojas labāk šādos apstākļos:

  - Grupējiet pēc iespējas vairāk operāciju. Lielapjoma operāciju vidējais izpildlaiks ir labāks par viena ieraksta operāciju vidējo izpildlaiku. Jo mazāks būs izmantotais OperationSets skaits, jo ātrāks būs vidējais izpildes laiks.
  - Iestatiet tikai minimālos atribūtus, kas nepieciešami scenārija pabeigšanai. Esiet atlasīts attiecībā uz to ne nepieciešamo lauku tipiem, kas iekļauti OperationSet pieprasījumā. Lauki, kuros ir pakārtotās atslēgas vai apkopojuma lauki, ietekmēs veiktspēju.
