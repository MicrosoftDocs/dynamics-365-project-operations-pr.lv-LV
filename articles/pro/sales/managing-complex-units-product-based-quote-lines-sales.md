---
title: Sarežģītu vienību, piemēram, viena lietotāja, pārvaldība, uz vienu mēnesi produktu piedāvājuma rindām — Lite
description: Šajā tēmā ir sniegta informācija par sarežģītu vienību pārvaldību produktu piedāvājumu rindām.
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 78bdb64d901cf68ce02c168987c2386e1416f6ee
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994775"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a><span data-ttu-id="ca21f-103">Sarežģītu vienību, piemēram, viena lietotāja, pārvaldība, uz vienu mēnesi produktu piedāvājuma rindām — Lite</span><span class="sxs-lookup"><span data-stu-id="ca21f-103">Managing complex units such as per-user, per-month for product-based quote lines - lite</span></span>

<span data-ttu-id="ca21f-104">_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_</span><span class="sxs-lookup"><span data-stu-id="ca21f-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ca21f-105">Dynamics 365 Project Operations, lai atbalstītu uz abonēšanu balstītu produktu pārdošanu, izmanto daudzuma koeficientus.</span><span class="sxs-lookup"><span data-stu-id="ca21f-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="ca21f-106">Uz abonēšanu balstītiem produktiem daudzums piedāvājumā vai projekta līguma rindā tiek izteikts kā lietotāju mēnešu skaits.</span><span class="sxs-lookup"><span data-stu-id="ca21f-106">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="ca21f-107">Parasti abonējamas programmatūras cena katalogā tiek glabāta kā cena vienam lietotājam vienā mēnesī.</span><span class="sxs-lookup"><span data-stu-id="ca21f-107">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="ca21f-108">Pārdošanas procesa laikā cena piedāvājuma rindā parasti ir vienam lietotājam, viena mēneša cena, par kuru notika pārrunas un kuras atlaidi noteica IT pārdošanas aģents.</span><span class="sxs-lookup"><span data-stu-id="ca21f-108">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="ca21f-109">Katram darījumam ir atšķirīgs lietotāju skaits un atšķirīgs abonēšanas mēnešu skaits.</span><span class="sxs-lookup"><span data-stu-id="ca21f-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="ca21f-110">Daudzums, kas tiek izmantots piedāvājuma rindas aprēķināšanai, ir lietotāju skaita un abonēšanas mēnešu skaita reizinājums.</span><span class="sxs-lookup"><span data-stu-id="ca21f-110">The quantity used to compute the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="ca21f-111">Lai atbalstītu šāda tipa pārdošanu, Project Operations ieviesa daudzuma koeficientu jēdzienu.</span><span class="sxs-lookup"><span data-stu-id="ca21f-111">To support this type of sale, Project Operations introduced the concept of quantity factors.</span></span> <span data-ttu-id="ca21f-112">Daudzuma koeficienti izmanto produkta atribūtus programmā Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="ca21f-112">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="ca21f-113">Kad kādam produktam konfigurējat konkrētus rekvizītus, Project Operations ļauj jums atzīmēt apakškopu vai visus rekvizītus kā daudzuma faktorus.</span><span class="sxs-lookup"><span data-stu-id="ca21f-113">When you configure specific properties for a product, Project Operations lets you flag a subset, or all of the properties, as quantity factors.</span></span>

<span data-ttu-id="ca21f-114">Project Operations pārliecinās, ka kā daudzuma koeficienti ir atzīmēti tikai skaitliskie rekvizīti vai produktu rekvizīti, kuriem ir skaitlisks datu tips.</span><span class="sxs-lookup"><span data-stu-id="ca21f-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="ca21f-115">Kad pievienojat produktu ar daudzuma koeficientiem piedāvājuma rindai, lauks **Daudzums** kļūst tikai lasāms.</span><span class="sxs-lookup"><span data-stu-id="ca21f-115">When you add a product with quantity factors to a quote line, the **Quantity** field becomes read-only.</span></span> <span data-ttu-id="ca21f-116">Kad produktu rekvizītiem ir ievadītas vērtības, kas ir daudzuma koeficienti, Project Operations aprēķināta piedāvājuma rindas daudzumu.</span><span class="sxs-lookup"><span data-stu-id="ca21f-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the quote line.</span></span>

<span data-ttu-id="ca21f-117">Programmatūrā Dynamics 365 Sales varētu būt, piemēram, tālāk norādītie rekvizīti.</span><span class="sxs-lookup"><span data-stu-id="ca21f-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="ca21f-118">**Lietotāju skaits**: Lietotāju skaits</span><span class="sxs-lookup"><span data-stu-id="ca21f-118">**No of users**: The number of users</span></span>
- <span data-ttu-id="ca21f-119">**Mēnešu skaits**: Abonēšanas mēnešu skaits</span><span class="sxs-lookup"><span data-stu-id="ca21f-119">**No of Months**: The number of subscription months</span></span>
- <span data-ttu-id="ca21f-120">**Produkta SKU**</span><span class="sxs-lookup"><span data-stu-id="ca21f-120">**Product SKU**</span></span>

<span data-ttu-id="ca21f-121">Rekvizītus **Lietotāju skaits** un **Mēnešu skaits** varat atzīmēt kā daudzuma koeficientus, rediģējot produkta rindas rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="ca21f-121">You can flag the **No of Users** and **No of Months** properties as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="ca21f-122">Lai no produkta rekvizītiem izveidotu daudzuma koeficientus, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="ca21f-122">To create Quantity factors from Product properties, follow these steps:</span></span>

1. <span data-ttu-id="ca21f-123">Project Operations kreisajā navigācijas rūtī pārejiet uz **Sales** > **Products**.</span><span class="sxs-lookup"><span data-stu-id="ca21f-123">On the Project Operations left navigation pane, go to **Sales** > **Products**.</span></span>
2. <span data-ttu-id="ca21f-124">Atveriet produktu, kuram nepieciešams konfigurēt daudzuma koeficientus.</span><span class="sxs-lookup"><span data-stu-id="ca21f-124">Open the product for which you need to configure quantity factors.</span></span> <span data-ttu-id="ca21f-125">Pārliecinieties, vai produktam ir jau konfigurēti rekvizīti.</span><span class="sxs-lookup"><span data-stu-id="ca21f-125">Make sure the product has properties already configured.</span></span>
3. <span data-ttu-id="ca21f-126">Produkta lapā **Projekta informācija** atlasiet **Daudzuma koeficienti**.</span><span class="sxs-lookup"><span data-stu-id="ca21f-126">On the **Project Information** page for the Product, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="ca21f-127">Apakšrežģī atlasiet **+ Jauns lauka aprēķins**.</span><span class="sxs-lookup"><span data-stu-id="ca21f-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="ca21f-128">Ievadiet daudzuma koeficienta nosaukumu un atlasiet rekvizīta vērtību, kas ir kartēta uz lauka aprēķinu.</span><span class="sxs-lookup"><span data-stu-id="ca21f-128">Enter the name of the Quantity factor and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="ca21f-129">Saglabāt un aizvērt formu.</span><span class="sxs-lookup"><span data-stu-id="ca21f-129">Save and close the form.</span></span> <span data-ttu-id="ca21f-130">Atkārtojiet šīs darbības visiem rekvizītiem, kas jāizmanto produkta piedāvājuma rindas daudzuma aprēķināšanai.</span><span class="sxs-lookup"><span data-stu-id="ca21f-130">Repeat these steps for all properties to use for computing the quantity for the product-based quote line.</span></span>

<span data-ttu-id="ca21f-131">Kad produktam tiek izveidota produkta piedāvājuma rinda, piedāvājuma rindas daudzums tiek slēgts.</span><span class="sxs-lookup"><span data-stu-id="ca21f-131">When you create a product-based quote line for a product, the quantity of the quote line will be locked.</span></span> <span data-ttu-id="ca21f-132">Daudzums tiek aprēķināts kā to rekvizītu vērtību reizinājums, kas ievadīts šajā piedāvājuma rindā.</span><span class="sxs-lookup"><span data-stu-id="ca21f-132">The quantity will be computed as a product of the property values that you input for that quote line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]