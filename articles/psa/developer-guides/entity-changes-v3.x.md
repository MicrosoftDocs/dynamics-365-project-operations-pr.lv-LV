---
title: Entītijas, vadīklas un lietotāja saskarnes izmaiņas (Project Service Automation 3.x)
description: Šajā tēmā ir aprakstītas izmaiņas risinājuma Microsoft Dynamics Project Service Automation 3.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 48062eda1f524dd3ca0d5feccf11fd5577521275
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148742"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a>Entītijas, vadīklas un lietotāja saskarnes izmaiņas (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]


Izlaižot Microsoft Dynamics Project Service Automation (PSA) 3.x, entītijām, vadīklām, skatiem un lietotāja saskarnei ir veiktas daudzas izmaiņas. Šajā dokumentā ir sniegta svarīga informācija par tālāk norādītajām produkta versijām.

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a>Primārā un pakārtotā attiecību pārdošanas dokumentam, pārdošanas dokumenta rindai, pārdošanas dokumenta rindas detalizētajām entītijām
Pēc versijas Dynamics 365 Project Service Automation (PSA), kas tika izlaista pirms versijas 3.0, dažas attiecības starp pārdošanas dokumentiem, pārdošanas dokumentu rindām un pārdošanas dokumentu rindu detaļām tika ieviestas, izmantojot virkņu laukus, kas saturēs virknes attēlojumu saistīto entītiju. Tas bija saistīts ar platformas ierobežojumiem, kam nepieciešami nozīmīgi pasūtījuma kodi serverī un klienta puses risinājumā, lai šīs attiecības darbotos līdzīgi kā tipiskas Dynamics CRM entītiju attiecības un panāktu, lai virkņu lauki darbojas kā uzmeklēšanas lauki.

PSA 3.0 tika atjaunināts, lai izmantotu jaunas entītiju attiecības starp pārdošanas dokumentu un pārdošanas dokumentu rindu entītijām.

Tā kā uzmeklēšanas laukus tagad var izmantot, lai norādītu atsauces uz entītijām, lauki, kas uzturēja saistītās entītijas GUID vērtību iepriekšējās versijās, vairs nav nepieciešami un tāpēc ir novecojuši. Pielāgotais klients un servera blakuskods, kas apstrādā mantoto virkņu laukos definētās attiecības, arī ir novecojis.

### <a name="entity-schema-changes"></a>Entītijas shēmas izmaiņas
Tālāk sniegtajā tabulā ir sniegts viens pret vienu novecojuši virkņu lauku saraksts, kā arī jauni entītiju uzmeklēšanas lauki. 

 Entītija |   Novecojis lauks (virkne) | Jauns lauks (uzmeklēšana)
--- | --- | ---
invoicedetail (rēķina rinda) |  msdyn_contractline |    msdyn_contractlineid
msdyn_actual (faktiskais) | msdyn_contractline |   msdyn_salescontractlineid
msdyn_contractlineinvoiceschedule (Project Contract rindas rēķina grafiks) |    msdyn_contractline |    msdyn_contractlineid
msdyn_contractlinescheduleofvalue (Project Contract rindas galotne) |   msdyn_contractline |    msdyn_contractlineid
msdyn_fact (faktiskais) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_invoicelinetransaction (rēķina rindas informācija) | msdyn_invoiceline <br> msdyn_salescontractline | msdyn_invoiceline <br> msdyn_salescontractlineid
msdyn_journalline (žurnāla rinda) |  msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlineresourcecategory (Project Contract rindas resursa kategorija) | msdyn_salescontractline |   msdyn_contractlineid
msdyn_orderlinetransaction (projekta līguma rindas detaļa) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlinetransactioncategory (Project Contract rindas transakciju kategorija) |   msdyn_contractline |    msdyn_contractlineid
msdyn_orderlinetransactionclassification (Project Contract rindas transakciju klasifikācija) |   msdyn_contractline |    msdyn_contractlineid
msdyn_quotelineinvoiceschedule (piedāvājumu rindas rēķina grafiks) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelineresourcecategory (piedāvājumu rindas resursu kategorija) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinescheduleofvalue (piedāvājuma rindas virsotne) | msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransaction (piedāvājuma rindas informācija) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactioncategory (piedāvājumu rindas transakciju kategorija) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactionclassification (piedāvājumu rindas transakciju klasifikācija) |  msdyn_quoteline |   msdyn_quotelineid
SalesOrderDetail (pasūtījuma rinda) | msdyn_quotelineid | msdyn_quoteline 

### <a name="deprecated-custom-views-and-controls"></a>Novecojuši pielāgotie skati un vadīklas
Šie pielāgotie skati un vadīklas, kā arī ar tām saistītie artefakti, ir novecojuši.

- Iekasēšanas skats.
- Pielāgotas režģa vadīklas, kas parāda piedāvājuma rindas detalizēto informāciju piedāvājuma rindas lapā **Projekta informācija**.
- Pielāgotas režģa vadīklas, kas parāda projekta līguma rindas detalizēto informāciju piedāvājuma rindas lapā **Projekta informācija**.

> [!NOTE]
> Pilnu novecojušo resursu sarakstu skatiet sadaļā [Novecojušie tīmekļa resursi Project Service Automation versijai v3.x](../developer-guides/web-resources-deprecated-v3.x.md)

## <a name="unified-client-interface-app-module"></a>Vienotās klienta saskarnes lietotnes modulis
Ieviešot vienotās klienta saskarnes (UCI) programmu moduļus, PSA vietnes kartes ieraksti ir noņemti no sistēmas.  
Funkcionalitāte, kas saistīta ar veidlapu pārslēgšanu iespējai, piedāvājumam, pasūtījumam un rēķinam, ir novecojusi, jo tā vairs nav vajadzīga, jo UCI programmas modulī ir iekļautas tikai veidlapu PSA versijas.  

Ir novecojuši šādi tīmekļa resursi:

- msdyn_\SalesDocument\SalesDocumentFormLoader.js
- msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js

> [!NOTE]
> Pilnu novecojušo resursu sarakstu skatiet sadaļā [Novecojušie tīmekļa resursi Project Service Automation versijai v3.x](../developer-guides/web-resources-deprecated-v3.x.md)


