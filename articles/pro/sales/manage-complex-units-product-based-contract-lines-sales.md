---
title: Produktu līgumu rindu kompleksu vienību pārvaldīšana — Lite
description: Šajā tēmā ir sniegta informācija par to, kā atbalstīt uz abonementu balstītu produktu pārdošanu.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 029d2aa4fd20fc036a34ae6136fe12454f3b7703
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273342"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a><span data-ttu-id="7eb93-103">Produktu līgumu rindu kompleksu vienību pārvaldīšana — Lite</span><span class="sxs-lookup"><span data-stu-id="7eb93-103">Manage complex units for product-based contract lines - lite</span></span>

<span data-ttu-id="7eb93-104">_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_</span><span class="sxs-lookup"><span data-stu-id="7eb93-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7eb93-105">Dynamics 365 Project Operations, lai atbalstītu uz abonēšanu balstītu produktu pārdošanu, izmanto daudzuma koeficientus.</span><span class="sxs-lookup"><span data-stu-id="7eb93-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="7eb93-106">Uz abonēšanu balstītiem produktiem daudzums līgumā vai projekta līguma rindā tiek izteikts kā lietotāju mēnešu skaits.</span><span class="sxs-lookup"><span data-stu-id="7eb93-106">For subscription-based products, the quantity on the contract or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="7eb93-107">Abonējamas programmatūras cena katalogā tiek glabāta kā cena vienam lietotājam vienā mēnesī.</span><span class="sxs-lookup"><span data-stu-id="7eb93-107">The price of subscription software is stored in the catalog as the price per-user, per-month.</span></span> <span data-ttu-id="7eb93-108">Pārdošanas procesa laikā cena līguma rindā parasti ir vienam lietotājam, viena mēneša cena, par kuru notika pārrunas un kuras atlaidi noteica IT pārdošanas aģents.</span><span class="sxs-lookup"><span data-stu-id="7eb93-108">During the sales process, the price on the contract line is usually the per-user, per-month price that was negotiated and discounted by the sales agent.</span></span> <span data-ttu-id="7eb93-109">Katram darījumam ir atšķirīgs lietotāju skaits un atšķirīgs abonēšanas mēnešu skaits.</span><span class="sxs-lookup"><span data-stu-id="7eb93-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="7eb93-110">Daudzums, kas tiek izmantots līguma rindas summas aprēķināšanai, ir lietotāju skaita un abonēšanas mēnešu skaita reizinājums.</span><span class="sxs-lookup"><span data-stu-id="7eb93-110">The quantity used to calculate the amount of the contract line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="7eb93-111">Lai atbalstītu šāda tipa pārdošanu, Project Operations atbalsta *daudzuma koeficientu* jēdzienu.</span><span class="sxs-lookup"><span data-stu-id="7eb93-111">To support this type of sale, Project Operations supports the concept of *quantity factors*.</span></span> <span data-ttu-id="7eb93-112">Daudzuma faktori izmanto produktu atribūtus.</span><span class="sxs-lookup"><span data-stu-id="7eb93-112">Quantity factors rely on product attributes.</span></span> <span data-ttu-id="7eb93-113">Kad kādam produktam konfigurējat konkrētus rekvizītus, jūs varat atzīmēt šo rekvizītu apakškopu vai visus rekvizītus kā daudzuma faktorus.</span><span class="sxs-lookup"><span data-stu-id="7eb93-113">When you configure specific properties for a product, you can flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="7eb93-114">Project Operations pārliecinās, ka kā daudzuma koeficienti ir atzīmēti tikai skaitliskie rekvizīti vai produktu rekvizīti, kuriem ir skaitlisks datu tips.</span><span class="sxs-lookup"><span data-stu-id="7eb93-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="7eb93-115">Kad prece ar konfigurētu daudzuma koeficientu tiek pievienota līguma rindai, lauks **Daudzums** kļūst tikai lasāms.</span><span class="sxs-lookup"><span data-stu-id="7eb93-115">When a product with configured quantity factors is added to a contract line, the **Quantity** field  becomes read-only.</span></span> <span data-ttu-id="7eb93-116">Kad produktu rekvizītiem ir ievadītas vērtības, kas ir daudzuma koeficienti, Project Operations aprēķina līguma rindas daudzumu.</span><span class="sxs-lookup"><span data-stu-id="7eb93-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the contract line.</span></span>

<span data-ttu-id="7eb93-117">Programmatūrā Dynamics 365 Sales varētu būt, piemēram, tālāk norādītie rekvizīti.</span><span class="sxs-lookup"><span data-stu-id="7eb93-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="7eb93-118">**Lietotāju skaits**: lietotāju skaits.</span><span class="sxs-lookup"><span data-stu-id="7eb93-118">**No of users**: The number of users.</span></span>
- <span data-ttu-id="7eb93-119">**Mēnešu skaits**: abonēšanas mēnešu skaits.</span><span class="sxs-lookup"><span data-stu-id="7eb93-119">**No of Months**: The number of subscription months.</span></span>
- <span data-ttu-id="7eb93-120">**Produkta SKU** : produkta krājumu uzturēšanas vienība (SKU).</span><span class="sxs-lookup"><span data-stu-id="7eb93-120">**Product SKU**: The stock keeping unit (SKU) for the product.</span></span>

<span data-ttu-id="7eb93-121">Rekvizītus **Lietotāju skaits** un **Mēnešu skaits** var atzīmēt kā daudzuma koeficientus, rediģējot produkta rindas rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="7eb93-121">The **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="7eb93-122">Lai no produkta rekvizītiem izveidotu daudzuma koeficientus, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="7eb93-122">To create quantity factors from product properties, complete the following steps.</span></span>

1. <span data-ttu-id="7eb93-123">Līdzeklī **Project Operations** atlasiet **Pārdošana — produkti**.</span><span class="sxs-lookup"><span data-stu-id="7eb93-123">On the **Project Operations**, select **Sales-Products**.</span></span>
2. <span data-ttu-id="7eb93-124">Atveriet produktu, kuram ir nepieciešams iestatīt daudzuma koeficientus.</span><span class="sxs-lookup"><span data-stu-id="7eb93-124">Open the product for which you need to set up quantity factors.</span></span> <span data-ttu-id="7eb93-125">Pārliecinieties, vai produktam jau ir iestatīti rekvizīti.</span><span class="sxs-lookup"><span data-stu-id="7eb93-125">Make sure that the product has properties already set up.</span></span>
3. <span data-ttu-id="7eb93-126">Lapā **Projekta informācija** atlasiet cilni **Daudzuma koeficienti**.</span><span class="sxs-lookup"><span data-stu-id="7eb93-126">On the **Project Information** page, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="7eb93-127">Apakšrežģī atlasiet **+ Jauns lauka aprēķins**.</span><span class="sxs-lookup"><span data-stu-id="7eb93-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="7eb93-128">Ievadiet **Daudzuma koeficienta** nosaukumu un atlasiet rekvizīta vērtību, kas ir kartēta uz lauka aprēķinu.</span><span class="sxs-lookup"><span data-stu-id="7eb93-128">Enter the name of the **Quantity Factor** and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="7eb93-129">Saglabāt un aizvērt formu.</span><span class="sxs-lookup"><span data-stu-id="7eb93-129">Save and close the form.</span></span>
7. <span data-ttu-id="7eb93-130">Atkārtojiet 2.–6. darbību visiem rekvizītiem, kas kopā veido produkta līguma rindai atbilstošo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="7eb93-130">Repeat steps 2-6 for all the properties that together will make up the quantity for the product-based contract line.</span></span>

<span data-ttu-id="7eb93-131">Ja ir iestatīti daudzuma koeficienti, tad, kad lietotājs veido līguma rindu šim produktam, līguma rindas daudzums ir slēgts.</span><span class="sxs-lookup"><span data-stu-id="7eb93-131">With quantity factors set up, when the user creates a contract line for this product, the quantity of the contract line is locked.</span></span> <span data-ttu-id="7eb93-132">Pēc tam daudzums tiek aprēķināts kā šīs līguma rindas rekvizītu vērtību produkts.</span><span class="sxs-lookup"><span data-stu-id="7eb93-132">The quantity is then calculated as a product of the property values for that contract line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]