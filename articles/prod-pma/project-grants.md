---
title: Projekta dotācijas
description: Šajā tēmā ir paskaidrots, kā izveidot vai modificēt dotāciju.
author: RadhikaRS
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 89801696d6a2924d78c85f6e9b4281409222dbb0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080625"
---
# <a name="project-grants"></a>Projekta dotācijas

[!include [banner](../includes/banner.md)]

Dotācija ir naudas dāvana konkrētam nolūkam vai projektam. Parasti pastāv ierobežojumi attiecībā uz to, kā var tērēt dotāciju. Projektu pārvaldībā un grāmatvedībā varat ievadīt un izsekot dotācijas un definēt to attiecības ar projektiem un projekta līgumiem. Piemēram, var veikt šādus uzdevumus:

- Saistiet dotācijas ar projektiem un finansējuma avotiem, izmantojot saites uz lapām **Projekts** un **Projekta līguma detalizētās informācija**.
- Ievadiet un izsekojiet izmaiņas dotācijā, kad tās pārvietojas no viena statusa uz citu.
- Ievadiet un izsekojiet izmaksas, pieprasītās summas un piešķirtās summas.
- Veidojiet galvenās dotācijas un saistiet tās ar apakšdotācijām.

Dotāciju var izveidot, ievadot visu informāciju jaunā ierakstā, vai arī var kopēt detaļas no esošas dotācijas un pēc tam tās atjaunināt.

## <a name="create-a-new-grant"></a>Jaunas dotācijas izveide

1. Dodieties uz **Projekta pārvaldība un uzskaite** \> **Dotācijas** \> **Dotācijas**.
2. Atlasiet **Jauna** \> **Dotācija**.
3. Dotāciju informācijas lapas kopsavilkuma cilnē **Vispārēji**, laukā **Dotācijas ID** ievadiet dotācijas burtciparu identifikatoru.
4. Laukā **Dotācijas nosaukums** ievadiet unikālu dotācijas nosaukumu.
5. Laukā **Apraksts** pievienojiet detalizētu informāciju par jauno dotāciju.

    Lielākā daļa citu lapas lauku nav obligāti, un jūs varat ievadīt tik daudz informācijas, cik vēlaties.

    Tālāk sniegtajā sarakstā ir aprakstīta informācija, kas ir norādīta katrā kopsavilkuma cilnes lapas dotāciju detalizētās informācijas lapā.

    - **Vispārīgi** — ievadiet dotācijas nosaukumu, statusu, aprakstu, mērķi un summu.
    - **Kontaktinformācija** — ievadiet detalizētu informāciju par personāla locekļiem, departamentu, kas pārvalda dotāciju, un dotācijas klientu vai organizācijas avotu. Varat arī norādīt, vai jūsu organizācija ir tranzīta entītija, kas saņem dotāciju, un pēc tam to nodod citam adresātam. Atlasiet **Pievienot**, lai pievienotu kontaktinformāciju, piemēram, tālruņu numurus un e-pasta adreses organizācijai, kas nodrošina dotāciju.
    - **Datumi un termiņi** — ievadiet datumus, kas ir saistīti ar dotāciju un dotācijas pieteikumu. Piemēri iekļauj pieteikuma izpildes datumu, iesniegšanas datumu un dotācijas apstiprināšanas vai noraidīšanas datumu.
    - **Saistītie projekti un projekta līgumi** — informāciju šajā kopsavilkuma cilnē var ievadīt tikai tad, ja lauks **Dotācijas statuss** kopsavilkuma cilnē **Vispārīgi** ir iestatīts kā **Aktīvs** vai **Piešķirts**. Lai izpildītu saistīto uzdevumu, atlasiet vienu no šīm opcijām:

        - **Pievienot finansējuma avotu** — pievienojiet jaunu finansējuma avotu dotācijai. Tagad var ievadīt visu informāciju vai arī izmantot noklusēto informāciju un pēc tam to vēlāk atjaunināt.
        - **Pievienot projekta līgumu** — pievienojiet vai atjauniniet projekta līguma informāciju.
        - **Pievienot projektu** — pievienojiet vai atjauniniet detalizētu informāciju par projektu.

    - **Iestatīt** — ievadiet detalizētu informāciju par atbilstošām dotācijām, ja šī informācija ir vajadzīga. Daudzas organizācijas, kas piešķir dotācijas, pieprasa, lai saņēmēji iztērētu konkrētu savas naudas vai resursu summu, kas atbilst dotācijā piešķirtajai summai. Laukā **Lokālais projekts vai izsekošanas ID** var ievadīt identifikatoru, kas atšķiras no projekta identifikatora.

        > [!NOTE]
        > Ja daļa no dotācijas tiks piešķirta citai organizācijai, iestatiet opciju **Apakšdotētais** uz **Jā**. Attiecībā uz dotācijām, kas tiek piešķirtas Amerikas Savienotajās Valstīs, varat norādīt, vai dotācija tiks piešķirta saskaņā ar valsts mandātu vai federālo mandātu.

    - **Informācija par izgūšanu** — pievienojiet vai atjauniniet informāciju par to, cik bieži piešķirt dotāciju līdzekļus var atsaukt, izrakstīt rēķinu par tiem vai tērēt.

## <a name="create-a-new-grant-from-a-copy"></a>Jaunas dotācijas izveide no kopijas

1. Dodieties uz **Projekta pārvaldība un uzskaite** \> **Dotācijas** \> **Dotācijas**.
2. Atlasiet **Jauna** \> **Dotācijas kopija**.
3. Ievadiet jaunās dotācijas burtciparu identifikatoru un nosaukumu un pēc tam atlasiet **Labi**.
4. Dotāciju datu lapā pārskatiet informāciju par kopēto dotāciju un veiciet vajadzīgās izmaiņas. Lielākā daļa lapas lauku ir neobligāti.

## <a name="view-or-modify-grant-details"></a>Dotācijas informācijas skatīšana vai modificēšana

1. Dodieties uz **Projekta pārvaldība un uzskaite** \> **Dotācijas** \> **Dotācijas**.
2. Atlasiet dotāciju modificēšanai.
3. Darbību rūts cilnes **Dotācija** grupā **Uzturēt** atlasiet opciju **Rediģēt**.
4. Pārskatiet dotācijas informāciju un veiciet vajadzīgās izmaiņas.
