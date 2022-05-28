---
title: Pasūtiet uz krājumiem nebalstītu projektu materiālus, izmantojot projekta pirkšanas pasūtījumus
description: Šajā sadaļā ir paskaidrots, kā jūs varat pasūtīt uz krājumiem nebalstītu projektu materiālus, izmantojot projekta pirkšanas pasūtījumus.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 2aa8fb94e2f9cbf91182f3f169339284d3eb9f44
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/18/2022
ms.locfileid: "8612712"
---
# <a name="order-procurement-categories-or-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Pasūtīt iepirkuma kategorijas vai neuzkrātos materiālus projektam, izmantojot projekta pirkšanas pasūtījumus

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Lai izsekotu preču un pakalpojumu pasūtījumus, jūsu organizācijas sagādes nodaļa var izmantot [pirkšanas pasūtījumus](/dynamics365/supply-chain/procurement/purchase-order-overview). Iepirkuma kategoriju vai ar krājumiem nesaistītu materiālu pirkšanas pasūtījumus var attiecināt uz projektu. Izrakstot rēķinu šiem pirkšanas pasūtījumiem, tiek reģistrētas projekta izmaksas.

## <a name="prerequisites"></a>Priekšnosacījumi
Lai iespējotu projekta pirkuma pasūtījumu funkcionalitāti, veiciet tālāk norādītās darbības.

1. Programmā Dynamics 365 Finance dodieties uz **līdzekļu pārvaldības** darbvietu.
2. Līdzekļu sarakstā atrodiet un atlasiet līdzekli **Iespējot projekta iegādes pasūtījumus Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem**.
3. Atlasiet **Iespējot**.
4. Konfigurējiet uz krājumiem nebalstītus materiālus un gaidošus piegādātāju rēķinus, kā aprakstīts sadaļā [Konfigurēt uz krājumiem nebalstītus materiālus, un gaidošus piegādātāju rēķinus](configure-materials-nonstocked.md).
5. Konfigurējiet sagādes kategorijas, kā aprakstīts sadaļā [Sagādes kategoriju izmantošana ar projekta pirkšanas pasūtījumiem un gaidošajiem kreditoru rēķiniem](configure-procurement-categories.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Izveidojiet projekta pirkuma pasūtījumu no projekta pirkuma pasūtījumu saraksta

1. Sadaļā Finance dodieties uz **Projektu pārvaldība un grāmatvedība** > **Projekti** > **Visi projekti** un atlasiet projektu.
2. Darbību rūts cilnes **Pārvaldīt** grupā **Jauns** atlasiet **vienuma uzdevumu** > **Pirkšanas pasūtījums**.
3. Lapā **Izveidot pirkuma pasūtījumu** atlasiet piegādātāju, kuru vēlaties ievietot pirkuma pasūtījumā, ja nepieciešams, ievadiet papildu informāciju un atlasiet **Labi**.
4. Lapā **Pirkums pasūtījums** režģī **Pirkuma pasūtījuma rindas** atlasiet **Pievienot rindu**.
5. Ievadiet krājuma kodu vai sagādes kategoriju, daudzumu, vienību, vienības cenu un citu informāciju pēc vajadzības.

    > [!NOTE]
    > Projekta pirkšanas pasūtījumos var izmantot tikai sagādes kategorijas, neuzkrātās preces un pakalpojumus. Uzkrātie vienumi netiek atbalstīti.

6. Turpiniet pievienot vienumus vai sagādes kategorijas pēc vajadzības un apstipriniet pirkšanas pasūtījumu.

    Preču un pakalpojumu kvītis var ierakstīt, izveidojot un iegrāmatojot produkta kvīti.

    > [!NOTE]
    > Produktu kvītis netiek ierakstītas Microsoft Dataverse projekta faktiskajos datos, un tās neietekmē projekta apakšgrāmatas.

    Pēc tam, kad piegādātājs ir nosūtījis rēķinu par precēm un pakalpojumiem pirkuma pasūtījumā, sagādes nodaļa par pirkuma pasūtījumu var ģenerēt rēķinu, dodoties uz darbību rūts sadaļu **Rēķins** > **Ģenerēt** > **Rēķinu**. Papildinformāciju par gaidošiem piegādātāja rēķiniem skatiet sadaļā [Uz krājumiem nebalstītu materiālu iegāde, izmantojot gaidošu piegādātāja rēķinu](pending-vendor-invoices.md).
