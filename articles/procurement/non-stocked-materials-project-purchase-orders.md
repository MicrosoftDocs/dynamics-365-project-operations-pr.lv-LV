---
title: Pasūtiet uz krājumiem nebalstītu projektu materiālus, izmantojot projekta pirkšanas pasūtījumus
description: Šajā sadaļā ir paskaidrots, kā jūs varat pasūtīt uz krājumiem nebalstītu projektu materiālus, izmantojot projekta pirkšanas pasūtījumus.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6e0307ad6474feef96fc8080877eccbbbc7259db
ms.sourcegitcommit: 2d96345fb3afc3b174530285f95271b5ccbdea03
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7563031"
---
# <a name="order-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Pasūtiet uz krājumiem nebalstītu projektu materiālus, izmantojot projekta pirkšanas pasūtījumus

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Lai izsekotu preču un pakalpojumu pasūtījumus, jūsu organizācijas sagādes nodaļa var izmantot [pirkšanas pasūtījumus](/dynamics365/supply-chain/procurement/purchase-order-overview). Pirkšanas pasūtījumus uz krājumiem nebalstītiem materiāliem var saistīt ar projektu. Izrakstot rēķinu šiem pirkšanas pasūtījumiem, tiek reģistrētas projekta izmaksas.

## <a name="prerequisites"></a>Priekšnosacījumi
Lai iespējotu projekta pirkuma pasūtījumu funkcionalitāti, veiciet tālāk norādītās darbības.

1. Risinājumā Dynamics 365 Finance dodieties uz darbvietu **Līdzekļu pārvaldība**.
2. Līdzekļu sarakstā atrodiet un atlasiet līdzekli **Iespējot projekta iegādes pasūtījumus Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem**.
3. Atlasiet **Iespējot**.
4. Konfigurējiet uz krājumiem nebalstītus materiālus un gaidošus piegādātāju rēķinus, kā aprakstīts sadaļā [Konfigurēt uz krājumiem nebalstītus materiālus, un gaidošus piegādātāju rēķinus](configure-materials-nonstocked.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Izveidojiet projekta pirkuma pasūtījumu no projekta pirkuma pasūtījumu saraksta

1. Sadaļā Finance dodieties uz **Projektu pārvaldība un grāmatvedība** > **Projekti** > **Visi projekti** un atlasiet projektu.
2. Darbību rūts cilnes **Pārvaldīt** grupā **Jauns** atlasiet **vienuma uzdevumu** > **Pirkšanas pasūtījums**.
3. Lapā **Izveidot pirkuma pasūtījumu** atlasiet piegādātāju, kuru vēlaties ievietot pirkuma pasūtījumā, ja nepieciešams, ievadiet papildu informāciju un atlasiet **Labi**.
4. Lapā **Pirkums pasūtījums** režģī **Pirkuma pasūtījuma rindas** atlasiet **Pievienot rindu**.
5. Pēc vajadzības ievadiet elementa numuru, daudzumu, vienību, vienības cenu un citu informāciju.

    > [!NOTE]
    > Projekta pirkuma pasūtījumos var izmantot tikai noliktavā neesošus krājumus un pakalpojumus. Netiek atbalstītas uzkrāto krājumu kategorijas un sagādes kategorijas.

6. Pēc vajadzības turpiniet pievienot elementus un apstipriniet pirkuma pasūtījumu.

    Preču un pakalpojumu kvītis var ierakstīt, izveidojot un iegrāmatojot produkta kvīti.

    > [!NOTE]
    > Produktu kvītis netiek ierakstītas Microsoft Dataverse projekta faktiskajos datos, un tās neietekmē projekta apakšgrāmatas.

    Pēc tam, kad piegādātājs ir nosūtījis rēķinu par precēm un pakalpojumiem pirkuma pasūtījumā, sagādes nodaļa par pirkuma pasūtījumu var ģenerēt rēķinu, dodoties uz darbību rūts sadaļu **Rēķins** > **Ģenerēt** > **Rēķinu**. Papildinformāciju par gaidošiem piegādātāja rēķiniem skatiet sadaļā [Uz krājumiem nebalstītu materiālu iegāde, izmantojot gaidošu piegādātāja rēķinu](pending-vendor-invoices.md).
