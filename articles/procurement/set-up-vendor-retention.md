---
title: Iestatīt piegādātāju ieturēšanu
description: Šajā tēmā ir izskaidrots, kā iestatīt piegādātāja ieturēšanu.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9511da6212aafbf5b173efc6eb1ceaacbc8264a2
ms.sourcegitcommit: 098ea345ecfaf4445520094c32f5511b67e7953c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/02/2021
ms.locfileid: "7594608"
---
# <a name="set-up-vendor-retention"></a>Iestatīt piegādātāju ieturēšanu

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Šajā tēmā ir informācija, kā iestatīt piegādātāja ieturēšanu.

## <a name="set-up-a-vendor-retention-account-in-general-ledger"></a>Piegādātāja ieturēšanas konta iestatīšana vispārējā virsgrāmatā

1. Dodieties uz Dynamics 365 Finance **Vispārējā virsgrāmata** > **Grāmatošanas iestatīšana** > **Automātisko transakciju konti**.
2. Pievienot jaunu rindu.
3. Laukā **Grāmatošanas veids** atlasiet **Piegādātāja ieturēšana**.
4. Atlasiet galveno kontu, lai iegrāmatotu piegādātāja ieturēšanu.

## <a name="create-vendor-retention-terms"></a>Izveidot kreditora ieturēšanas nosacījumus

Izmantojiet lapu **Piegādātāja ieturēšanas nosacījumi**, lai iestatītu un uzturētu ieturēšanas nosacījumus piegādātāja maksājumiem. Ievadiet procentuālo daļu, kas ir jāietur no piegādātāja maksājuma, un iepriekš ieturēto summu procentuālo daļu, kas ir jānodod izpildei. Summas tiek automātiski saglabātas piegādātāja rēķinos, līdz līgums sasniedz norādīto pabeigšanas statusu. Pēc tam, kad ir iestatīti piegādātāja ieturēšanas nosacījumi, tos var pielietot jebkuram projektam, kurā piegādātājs darbojas.

1. Sadaļā Finance dodieties uz **Projektu vadība un grāmatvedība** > **Iestatīšana** > **Ieturēšana** > **Pārdevēja maksājumu ieturējumu nosacījumi**.
2. Atlasiet **Jauns**, lai pievienotu jaunu piegādātāja saglabāšanas nosacījumu. Jaunā nosacījuma vērtība laukā **Kārtulas ID** tiek ievadīta automātiski. 
3. Laukā **Apraksts** ievadiet aprakstošu jaunā nosacījuma nosaukumu.
4. Cilnē **Nosacījumi** atlasiet **Pievienot rindu**, lai ievadītu piegādātāja ieturēšanas nosacījumu.   
5. Laukā **Piegādāto vienību procentuālā daļa** ievadiet procentuālo daļu, kuru sasniedzot noteikums ir jāizpilda. Summas tiek automātiski ieturētas no piegādātāja rēķiniem, līdz projekta pabeigtības posms ir vienāds ar ievadīto procentuālo daļu. Piemēram, ja ievadīsiet 50,00, summas tiek saglabātas, līdz projekta pabeigtība ir 50 procenti.
6. Laukā **Ieturētie procenti** ievadiet procentuālo daļu, kas ir ieturama no piegādātāja rēķina summas. Piemēram, ja jūs šajā laukā ievadāt 10.00, tad 10 procenti no piegādātāja rēķinu summas tiek ieturēti, līdz projektā ir sasniegts procentuāls pabeigtības stāvoklis, ko jūs iestatījāt laukā **Piegādāto vienību procentuālās daļas**.
7. Laukā **Procentuālā daļa, kas jānodod izpildei** ievadiet iepriekš ieturēto summu procentuālo daļu, kas ir jānodod izpildei, kad projektā ir sasniegts pabeigtības stāvoklis.

> [!NOTE]
> Ja dažādos projekta līmeņos ir iestatīti dažādi pabeigtības stāvokļi, katrai ieturējumu kārtulai ievadiet atsevišķu rindu katram piegādātāja ieturēšanas nosacījumam. Katrā rindā var norādīt atšķirīgu ieturamo procentuālo daļu un atšķirīgu procentuālo daļu, kas ir jānodod izpildei, katrā projekta pabeigtības līmenī.

## <a name="set-up-a-vendor-agreement-for-the-project"></a>Piegādātāja projekta līguma iestatīšana

Iestatiet projektam lietotos piegādātāja ieturēšanas nosacījumus. Piegādātāja saglabāšanas nosacījumi tiek rādīti arī pirkšanas pasūtījumos, ko izveidojat šim piegādātājam.

1. Sadaļā Finance dodieties uz **Projektu pārvaldība un grāmatvedība** > **Projekti** > **Visi projekti**. 
2. Atlasiet projektu un darbību rūtī atlasiet **Projekta grupas** > **Piegādātāju līgumi**.
3. Lapā **Piegādātāju līgumi** pievienojiet jaunu rindu.
4. Laukā **Konta kods** atlasiet vienu no tālāk minētajām opcijām.
   - **Tabula**: piegādātāja saglabāšanas nosacījumi attiecas uz vienu piegādātāju.
   - **Grupa**: piegādātāja saglabāšanas nosacījumi attiecas uz visiem grupā esošajiem piegādātājiem.
   - **Visi**: piegādātāju saglabāšanas nosacījumi attiecas uz visiem piegādātājiem.
5. Laukā **Piegādātājs/piegādātāju grupa** atlasiet piegādātāju vai piegādātāju grupu, uz kuru attiecas piegādātāju ieturēšanas nosacījumi. Ja iepriekšējā darbībā atlasījāt **Visi**, tad šis lauks nav pieejams.
6. Laukā **Piegādātāja ieturēšanas nosacījumi** atlasiet kārtulas ID, kas atbilst šī piegādātāja ieturēšanas nosacījumiem. 
