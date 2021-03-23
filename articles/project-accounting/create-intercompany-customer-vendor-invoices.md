---
title: Starpuzņēmumu klientu un piegādātāju rēķinu izveide
description: Šajā tēmā ir sniegta informācija par to, kā izveidot starpuzņēmumu klientu un piegādātāju rēķinus.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: dd9aa1a4d167d556206a487e79983090b3f4592a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287472"
---
# <a name="create-intercompany-customer-and-vendor-invoices"></a>Starpuzņēmumu klientu un piegādātāju rēķinu izveide

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Aizdevuma juridiskās personas projekta grāmatvedis izveido starpuzņēmumu klienta rēķinu par projekta izmaksām, kas tiek nodotas aizņēmuma juridiskajai personai. Pēc starpuzņēmumu klienta rēķina apstiprināšanas un iegrāmatošanas aizdevuma juridiskā persona nosūta starpuzņēmumu rēķinu aizņēmuma juridiskajai personai.

Aizdevuma juridiskās personas projekta grāmatvedis var iestatīt pakešveida apstrādi, lai starpuzņēmumu rēķini tiktu ģenerēti periodiski. Projekta grāmatvedis norāda kritērijus, piemēram, noteiktus projektus, lai izveidotu starpuzņēmumu rēķinus paketē.

## <a name="manually-create-an-intercompany-customer-invoice-for-project-transactions"></a>Manuāla starpuzņēmumu klienta rēķina izveide par projekta darbībām 

Izmantojiet šo procedūru, lai manuāli izveidotu starpuzņēmumu klienta rēķinu par projekta darbībām. Meklējiet stundas, kuras grāmatoja projektu darbinieki aizņēmuma juridiskajās personās, un izdevumus, kas radās jūsu juridiskajai personai aizņēmuma juridisko personu vārdā. Varat meklēt pēc juridiskās personas nosaukuma, projekta līguma numura, projekta numura, datumu diapazona vai jebkuras šo opciju kombinācijas. Meklēšanas rezultātos atlasiet darbības, kas jāpievieno starpuzņēmumu rēķinam.

1. Programmā Dynamics 365 Finance dodieties uz **Projektu pārvaldība un uzskaite** > **Projektu rēķini** > **Starpuzņēmumu klientu rēķini**. Saraksta lapas **Starpuzņēmumu klientu rēķini** darbību rūtī atlasiet **Jauns.**
2. Lapas **Izveidot starpuzņēmumu rēķinu** laukā **Juridiskā persona** atlasiet aizņēmuma juridisko personu.
3. Neobligāti: ievadiet konkrēta projekta līguma un projekta numuru.
4. Sašauriniet meklēšanu, atlasot datumu diapazonu. Ievadiet konkrētus datumus laukos **Sākuma datums** un **Beigu datums**. Meklēšanas rezultātos tiek rādītas tikai šajā datumu diapazonā grāmatotās starpuzņēmumu darbības.
5. Iestatiet vienumu **Projekta papildu žurnāla rindas parametrs** uz **Jā** un atlasiet **Meklēt**.
6. Meklēšanas rezultātos atlasiet darbības, ko iekļaut starpuzņēmumu rēķina priekšlikumā, un pēc tam atlasiet **Labi**.
7. Lapā **Starpuzņēmumu klienta rēķins** tiek rādītas meklēšanas rezultātos atlasītās starpuzņēmumu projekta darbības. Lai pirms rēķina nosūtīšanas aizņēmuma juridiskajai personai mainītu darbības, veiciet tālāk norādītās darbības.
  
    1. Atveriet lapu **Rēķina priekšlikuma izveide**. Atlasiet pašreizējam rēķinam papildu starpuzņēmumu darbības, pēc tam atlasiet **Pievienot rindu**.
    2. Lai noņemtu rindu, atlasiet to un pēc tam atlasiet **Noņemt**.
    3. Komentārus, iemeslus, finanšu dimensijas un citu informāciju par atlasīto rindu skatiet kopsavilkuma cilnē **Rēķina rindas**.
    
8. Lai grāmatotu starpuzņēmumu klienta rēķinu, darbību rūtī atlasiet **Grāmatot**.

> [!NOTE]
> Ja jūsu organizācijai nepieciešams, lai starpuzņēmumu rēķini pirms grāmatošanas tiktu pārskatīti, sistēmas administrators starpuzņēmumu rēķiniem var iestatīt darbplūsmu. Ja starpuzņēmumu rēķiniem nav iestatīta darbplūsma, varat grāmatot starpuzņēmumu rēķinu.

## <a name="create-a-batch-job-for-intercompany-invoices"></a>Pakešuzdevuma izveide starpuzņēmumu rēķiniem

Vienlaikus var izveidot vairākus starpuzņēmumu rēķinus visām aizņēmuma juridiskajām personām. Izmantojot meklēšanas funkcionalitāti, varat, piemēram, meklēt visas darbības, kuras grāmato piesaistītie darbinieki un ir saistītas ar projektiem, kurus pārvalda citas juridiskās personas. Pēc tam katrai aizņēmuma juridiskajai personai varat izveidot starpuzņēmumu rēķinu par meklēšanas rezultātos norādītajām darbībām.

1. Dodieties uz **Projektu pārvaldība un uzskaite** > **Periodiski** > **Projektu rēķini** > **Izveidot starpuzņēmumu klientu rēķinus**.
2. Lapas **Izveidot starpuzņēmumu klientu rēķinus** laukā **Uzņēmums** atlasiet juridisko personu, kam jāizraksta rēķins. Ja neatlasīsit uzņēmumu, tiks parādītas visas meklēšanas kritērijiem atbilstošās darbības visām aizņēmuma juridiskajām personām.
3. Sadaļā **Izveidot vienu rēķinu katrā:** atlasiet, vai rēķinu par starpuzņēmumu darbībām izveidot, pamatojoties uz projektu vai aizņēmuma juridisko personu.
4. Neobligāti: lai atlasītu konkrētu projektu un projekta līgumu, kam jāizveido starpuzņēmumu rēķini, noklikšķiniet uz **Atlasīt**. Lapas **Pieprasījums** laukā **Kritēriji** atlasiet projekta līgumu, projekta numuru vai abus un pēc tam noklikšķiniet uz **Labi**.
5. Cilnē **Pakešveida apstrāde** iestatiet pakešveida apstrādi, lai periodiski izveidotu starpuzņēmumu rēķinus. Papildinformāciju skatiet sadaļā [Pakešapstrādes uzdevuma iesniegšana no veidlapas](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form).
6. Lai grāmatotu starpuzņēmumu rēķinus, darbību rūtī atlasiet **Grāmatot**.

> [!NOTE]
> Ja jūsu organizācijai nepieciešams, lai starpuzņēmumu rēķini pirms grāmatošanas tiktu pārskatīti, sistēmas administrators starpuzņēmumu rēķiniem var iestatīt darbplūsmu. Ja starpuzņēmumu rēķiniem nav iestatīta darbplūsma, varat grāmatot starpuzņēmumu rēķinus.

## <a name="post-the-intercompany-vendor-invoice"></a>Starpuzņēmumu piegādātāja rēķina grāmatošana

Projekta grāmatvedis aizņēmuma juridiskajā personā var pārskatīt starpuzņēmumu gaidošos piegādātāja rēķinus, kad ir iegrāmatots atbilstošais starpuzņēmumu klienta rēķins. Programmā Finance aizņēmuma juridiskajā personā dodieties uz **Kreditori** > **Rēķini** > **Gaidošais piegādātāja rēķins**. Gaidošā rēķina numurs atbildīs starpuzņēmumu klienta rēķina numuram. Pārbaudiet, vai rēķins ir pareizs, un pēc tam grāmatojiet rēķinu. Grāmatojot starpuzņēmumu piegādātāja rēķinu, tiek izveidota projekta apakšgrāmatas un virsgrāmatas darbība, kas atspoguļo darbības izmaksas aizņēmuma juridiskajā personā.


[!INCLUDE[footer-include](../includes/footer-banner.md)]