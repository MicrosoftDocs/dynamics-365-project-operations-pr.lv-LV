---
title: Iestatīt piegādātāju ieturēšanu
description: Šajā rakstā paskaidrots, kā iestatīt kreditora ieturējumu.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f30e8829d8d5d99c81fce730cb93cd7ce31913fe
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929775"
---
# <a name="set-up-vendor-retention"></a>Iestatīt piegādātāju ieturēšanu

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Šajā rakstā ir sniegta informācija par to, kā iestatīt piegādātāja ieturējumu.

## <a name="set-up-a-vendor-retention-account-in-general-ledger"></a>Piegādātāja ieturēšanas konta iestatīšana vispārējā virsgrāmatā

1. Sadaļā Dynamics 365 Finance dodieties uz **Virsgrāmatas** > **grāmatošanas uzstādījumu** > **konti automātiskām darbībām**.
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

