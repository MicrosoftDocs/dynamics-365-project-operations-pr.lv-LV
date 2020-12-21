---
title: Maksāt-kad-apmaksāts iestatīšana un izmantošana piegādātāja maksājumiem
description: Šajā tēmā ir paskaidrots, kā izveidot maksāt-kad-apmaksāts (PWP) nosacījumus, lai varētu atbrīvot daļējos piegādātāju maksājumus, pamatojoties uz klientu maksājumiem.
author: RadhikaRS
manager: AnnBe
ms.date: 03/30/2020
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
ms.openlocfilehash: e872c4a2d35cef4cddc6851615c6c4d73b4e9d9a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080423"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a><span data-ttu-id="8d688-103">Maksāt-kad-apmaksāts iestatīšana un izmantošana piegādātāja maksājumiem</span><span class="sxs-lookup"><span data-stu-id="8d688-103">Set up and use pay-when-paid vendor payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8d688-104">Kad apstiprināt, ka piegādātājs darbosies kā apakšuzņēmējs, iespējams, vēlēsities aizturēt maksājumu piegādātājam, līdz klients jums samaksās par projektu.</span><span class="sxs-lookup"><span data-stu-id="8d688-104">When you approve a vendor to work as a subcontractor, you might want to withhold payment to the vendor until your customer pays you for the project.</span></span> <span data-ttu-id="8d688-105">Lai atbalstītu šo scenāriju, uzstādot iepirkuma pasūtījumu (PO) ar piegādātāju, var iestatīt maksāt-kad-apmaksāts (PWP) nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="8d688-105">To support this scenario, you can set up pay-when-paid (PWP) terms when you set up the purchase order (PO) with the vendor.</span></span>

<span data-ttu-id="8d688-106">Piemēram, kad klients samaksā summu projekta rēķinā, varat izlaist daļu vai visu piegādātāja rēķina summu.</span><span class="sxs-lookup"><span data-stu-id="8d688-106">For example, when a customer pays an amount on a project invoice, you can release some or all of the vendor invoice amount.</span></span> <span data-ttu-id="8d688-107">Vienkārši iestatiet PWP nosacījumus, kas norāda, ka piegādātājs tiks apmaksāts pēc tam, kad saņemsit procentuālo daļu no saistītā maksājuma no klienta.</span><span class="sxs-lookup"><span data-stu-id="8d688-107">Just set up PWP terms that specify that the vendor will be paid after you receive a percentage of the related payment from the customer.</span></span> <span data-ttu-id="8d688-108">Ja saņemat daļēju maksājumu no klienta, varat manuāli izlaist dažus saistītos piegādātāju rēķinus apmaksai.</span><span class="sxs-lookup"><span data-stu-id="8d688-108">If you receive partial payment from a customer, you can manually release some of the related vendor invoices for payment.</span></span>

<span data-ttu-id="8d688-109">Šajā piemērā ir izklāstīts process, lietojot PWP nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="8d688-109">The following example outlines the process when PWP terms are used.</span></span>

## <a name="example"></a><span data-ttu-id="8d688-110">Piemērs</span><span class="sxs-lookup"><span data-stu-id="8d688-110">Example</span></span>

<span data-ttu-id="8d688-111">Jūsu organizācija piekrīt nodrošināt klientam 100 datoru, kuros ir instalēta programmatūra, par cenu 150,00 ASV dolāri (USD) par vienu vienību.</span><span class="sxs-lookup"><span data-stu-id="8d688-111">Your organization agrees to provide a customer with 100 computers that have software installed, for a price of 150.00 US dollars (USD) per computer.</span></span> <span data-ttu-id="8d688-112">Pēc tam jūs nolīgstat piegādātāju, kas jums nodrošina datorus, kuros instalēta programmatūra.</span><span class="sxs-lookup"><span data-stu-id="8d688-112">You then hire a vendor to provide you with the computers that have software installed.</span></span> <span data-ttu-id="8d688-113">Saskaņā ar līgumu klientam ir jāapstiprina datoru kvalitāte, pirms tas samaksā jūsu organizācijai.</span><span class="sxs-lookup"><span data-stu-id="8d688-113">According to the agreement, the customer must approve the quality of the computers before it pays your organization.</span></span> <span data-ttu-id="8d688-114">Jūsu organizācijas politika ir ieturēt maksājumu piegādātājiem, līdz klients jums ir samaksājis.</span><span class="sxs-lookup"><span data-stu-id="8d688-114">Your organization's policy is to withhold payment to vendors until the customer has paid you.</span></span> <span data-ttu-id="8d688-115">Tādēļ iestatāt projektu, lai tā PWP procentu 100 procentu.</span><span class="sxs-lookup"><span data-stu-id="8d688-115">Therefore, you set up the project so that it has a PWP percentage of 100 percent.</span></span>

<span data-ttu-id="8d688-116">Piegādātājs nosūta jums 100 datoru, kuros ir instalēta programmatūra, kopā ar rēķinu par 10 000,00 ASV dolāriem.</span><span class="sxs-lookup"><span data-stu-id="8d688-116">The vendor sends you the 100 computers that have software installed, together with an invoice for 10,000.00 USD.</span></span> <span data-ttu-id="8d688-117">Tā kā PWP nosacījumi ir iestatīti jūsu projektam, jūs nemaksājat piegādātājam pēc datoru saņemšanas.</span><span class="sxs-lookup"><span data-stu-id="8d688-117">Because PWP terms are set up for your project, you don't pay the vendor upon receipt of the computers.</span></span> <span data-ttu-id="8d688-118">Tā vietā nosūtāt datorus klientam kopā ar rēķinu par 15 000,00.</span><span class="sxs-lookup"><span data-stu-id="8d688-118">Instead, you send the computers to the customer, together with an invoice for 15,000.00.</span></span> <span data-ttu-id="8d688-119">Klients pārbauda datorus un apstiprina pilnu projekta rēķina summu.</span><span class="sxs-lookup"><span data-stu-id="8d688-119">The customer inspects the computers and approves the full amount of the project invoice.</span></span>

<span data-ttu-id="8d688-120">Pēc tam, kad esat saņēmis pilnu maksājumu no klienta, jūs maksājat 10 000,00 rēķinu — pilnu piegādātāja rēķina summu.</span><span class="sxs-lookup"><span data-stu-id="8d688-120">After you receive the full payment from the customer, you pay the vendor 10,000.00, the full amount of the vendor invoice.</span></span>

## <a name="set-up-pwp-terms-for-a-project"></a><span data-ttu-id="8d688-121">PWP nosacījumu iestatīšana projektam</span><span class="sxs-lookup"><span data-stu-id="8d688-121">Set up PWP terms for a project</span></span>

<span data-ttu-id="8d688-122">Iestatot PWP nosacījumus projektam, kā procenti ir jānorāda minimālā summa, kas klientam ir jāmaksā par projektu, pirms maksājat piegādātājam.</span><span class="sxs-lookup"><span data-stu-id="8d688-122">When you set up PWP terms for a project, you must specify, as a percentage, the minimum amount that a customer must pay you for the project before you will pay the vendor.</span></span> <span data-ttu-id="8d688-123">Sliekšņa summa tiek automātiski aprēķināta projekta klienta rēķiniem.</span><span class="sxs-lookup"><span data-stu-id="8d688-123">The threshold amount is automatically calculated on the customer invoices for the project.</span></span> <span data-ttu-id="8d688-124">Veiciet tālāk norādītās darbības, lai iestatītu PWP nosacījumu sliekšņa procentuālo vērtību.</span><span class="sxs-lookup"><span data-stu-id="8d688-124">Follow these steps to set up the threshold percentage for PWP terms.</span></span>

1. <span data-ttu-id="8d688-125">Dodieties uz **Projekta pārvaldība un uzskaite** \> **Projekti** \> **Visi projekti**.</span><span class="sxs-lookup"><span data-stu-id="8d688-125">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="8d688-126">Atrodiet un atveriet projektu, kuram vēlaties iestatīt PWP nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="8d688-126">Find and open the project that you want to set up PWP terms for.</span></span>
3. <span data-ttu-id="8d688-127">Kopsavilkuma cilnē **Piegādātāju līgumi** atlasiet **Pievienot rindu**.</span><span class="sxs-lookup"><span data-stu-id="8d688-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="8d688-128">Laukā **Konta kods** atlasiet vienu no tālāk minētajām opcijām.</span><span class="sxs-lookup"><span data-stu-id="8d688-128">In the **Account code** field, select one of the following options:</span></span>

    - <span data-ttu-id="8d688-129">**Tabula**  — PWP nosacījumi attiecas uz vienu piegādātāju.</span><span class="sxs-lookup"><span data-stu-id="8d688-129">**Table** – The PWP terms apply to a single vendor.</span></span>
    - <span data-ttu-id="8d688-130">**Grupa**  — PWP nosacījumi attiecas uz visiem piegādātāju grupas piegādātājiem.</span><span class="sxs-lookup"><span data-stu-id="8d688-130">**Group** – The PWP terms apply to all vendors in a vendor group.</span></span>
    - <span data-ttu-id="8d688-131">**Visi**  — PWP nosacījumi attiecas uz visiem piegādātājiem.</span><span class="sxs-lookup"><span data-stu-id="8d688-131">**All** – The PWP terms apply to all vendors.</span></span>

4. <span data-ttu-id="8d688-132">Ja iepriekšējā darbībā atlasījāt **Tabula** vai **Grupa** , laukā **Piegādātājs/piegādātāju grupa** piegādātāju vai piegādātāju grupu, uz kuru attiecas PWP nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="8d688-132">If you selected **Table** or **Group** in the previous step, in the **Vendor/Vendor group** field, select the vendor or vendor group that the PWP terms apply to.</span></span> <span data-ttu-id="8d688-133">Ja iepriekšējā darbībā atlasījāt **Visi** , lauku **Piegādātājs/piegādātāju grupa** nevar rediģēt.</span><span class="sxs-lookup"><span data-stu-id="8d688-133">If you selected **All** in the previous step, the **Vendor/Vendor group** field can't be edited.</span></span>
5. <span data-ttu-id="8d688-134">Ja piegādātāja ieturējumu nosacījumi piegādātājam ir iestatīti projektā, laukā **Piegādātāja ieturējumu nosacījumi** atlasiet noteikuma ID saglabāšanas nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="8d688-134">If vendor retention terms are set up for the vendor in the project, in the **Vendor retention terms** field, select the rule ID for the retention terms.</span></span>
6. <span data-ttu-id="8d688-135">Laukā **PWP sliekšņa procentuālā vērtība** ievadiet projekta sliekšņa procentuālo vērtību.</span><span class="sxs-lookup"><span data-stu-id="8d688-135">In the **PWP threshold percentage** field, enter the threshold percentage for the project.</span></span> <span data-ttu-id="8d688-136">Projektam ievadītā procentuālā vērtība nosaka minimālo summu, kas klientam ir jāmaksā pirms samaksas piegādātājam.</span><span class="sxs-lookup"><span data-stu-id="8d688-136">The percentage that you enter for the project defines the minimum amount that the customer must pay you before you will pay the vendor.</span></span>

## <a name="create-a-po-that-has-pwp-terms"></a><span data-ttu-id="8d688-137">PP izveide, kuram ir PWP nosacījumi</span><span class="sxs-lookup"><span data-stu-id="8d688-137">Create a PO that has PWP terms</span></span>

<span data-ttu-id="8d688-138">Grāmatojot rēķinu no piegādātāja, ja uz piegādātāju attiecas PWP nosacījumi, šie nosacījumi tiek parādīti PP rindās.</span><span class="sxs-lookup"><span data-stu-id="8d688-138">When you post an invoice from a vendor, if the vendor is subject to PWP terms, those terms are shown on the PO lines.</span></span> <span data-ttu-id="8d688-139">Lai izveidotu PP, kam ir PWP nosacījumi, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="8d688-139">To create a PO that has PWP terms, follow these steps.</span></span>

1. <span data-ttu-id="8d688-140">Dodieties uz **Sagāde un avoti** \> **Pirkšanas pasūtījumi** \> **Visi pirkšanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="8d688-140">Go to **Procurement and sourcing** \> **Purchase orders** \> **All purchase orders**.</span></span>
2. <span data-ttu-id="8d688-141">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="8d688-141">On the Action Pane, select **New**.</span></span> <span data-ttu-id="8d688-142">Pēc tam dialoglodziņā **Izveidot pirkšanas pasūtījumu** ievadiet nepieciešamo informāciju un atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="8d688-142">Then, in the **Create purchase order** dialog box, enter the required information, and select **OK**.</span></span>

    <span data-ttu-id="8d688-143">Vai arī atveriet esošu PP saraksta lapā **Visi**.</span><span class="sxs-lookup"><span data-stu-id="8d688-143">Alternatively, open an existing PO on the **All purchase orders** list page.</span></span>

4. <span data-ttu-id="8d688-144">Lapas **Pirkšanas pasūtījums** kopsavilkuma cilnē **Pirkšanas pasūtījuma rindas** pārskatiet detalizētu informāciju par piegādātāja PP rindu.</span><span class="sxs-lookup"><span data-stu-id="8d688-144">On the **Purchase order** page, on the **Purchase order lines** FastTab, review the details of the PO line for the vendor.</span></span> <span data-ttu-id="8d688-145">Automātiski tiek atlasīta opcija **Maksāt-kad-apmaksāts** , un lauks **PWP sliekšņa procentuālā vērtība** automātiski tiek kopēts no lauka **PWP sliekšņa procentuālā vērtība** lapā **Projekti**.</span><span class="sxs-lookup"><span data-stu-id="8d688-145">The **Pay when paid** option is automatically selected, and the value in the **PWP threshold percentage** field is automatically copied from the **PWP threshold percentage** field on the **Projects** page.</span></span>
6. <span data-ttu-id="8d688-146">Ja nevēlaties lietot PWP nosacījumus piegādātājam PP rindai, notīriet opciju **Maksāt-kad-apmaksāts**.</span><span class="sxs-lookup"><span data-stu-id="8d688-146">If you don't want to apply PWP terms to the vendor for a PO line, clear the **Pay when paid** option.</span></span> <span data-ttu-id="8d688-147">Šādā gadījumā PP rinda laukā **PWP sliekšņa procentuālā vērtība** tiks atiestatīta uz 0 (nulle).</span><span class="sxs-lookup"><span data-stu-id="8d688-147">In this case, the **PWP threshold percentage** field for the PO line will be reset to 0 (zero).</span></span>

## <a name="update-a-customer-payment-and-pay-the-vendor"></a><span data-ttu-id="8d688-148">Klienta maksājumu un piegādātāja apmaksu atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="8d688-148">Update a customer payment and pay the vendor</span></span>

<span data-ttu-id="8d688-149">Kad piegādātājs pabeidz darbu ar projektu un nosūta jums rēķinu, ir jāpārskata projekta statuss un klientu rēķini, lai noteiktu, vai projektam ir izpildīti PWP nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="8d688-149">When a vendor completes its work on a project and sends you an invoice, you must review the project status and customer invoices to determine whether the PWP terms have been met for the project.</span></span> <span data-ttu-id="8d688-150">Ja tika izpildīti piegādātāja PWP nosacījumi, varat noteikt, kuras rindas piegādātāja rēķinā ir jāmaksā, pamatojoties uz klienta maksājumiem par projektu.</span><span class="sxs-lookup"><span data-stu-id="8d688-150">If the PWP terms for the vendor were met, you can determine which lines on the vendor invoice to pay, based on the customer payments for the project.</span></span> <span data-ttu-id="8d688-151">Ja nolemjat maksāt piegādātājam pat tad, ja PWP nosacījumi nav izpildīti, varat ignorēt PWP nosacījumus lapā **Piegādātāja rēķins ar apmaksāto summu**.</span><span class="sxs-lookup"><span data-stu-id="8d688-151">If you decide to pay the vendor even though the PWP terms weren't met, you can override the PWP terms on the **Vendor invoice with pay when paid** page.</span></span>

1. <span data-ttu-id="8d688-152">Dodieties uz **Projekta pārvaldība un uzskaite** \> **Pieprasījumi un atskaites** \> **Ieturējumu pieprasījumi** \> **Piegādātāja rēķins ar apmaksāto summu**.</span><span class="sxs-lookup"><span data-stu-id="8d688-152">Go to **Project management and accounting** \> **Inquiries and reports** \> **Retention inquiries** \> **Vendor invoice with pay when paid**.</span></span>
2. <span data-ttu-id="8d688-153">Lapas **Piegādātāja rēķins ar apmaksāto summu** meklēšanas laukā ievadiet vērtības, lai atrastu piegādātāja rēķinu, kuru vēlaties pārskatīt, un pēc tam atlasiet **Meklēt**.</span><span class="sxs-lookup"><span data-stu-id="8d688-153">On the **Vendor invoices with pay when paid** page, in the search field, enter values to find the vendor invoice that you want to review, and then select **Search**.</span></span>
3. <span data-ttu-id="8d688-154">Kopsavilkuma cilnē **Piegādātāja rēķina rindas** atlasiet rindas, kuras vēlaties mainīt.</span><span class="sxs-lookup"><span data-stu-id="8d688-154">On the **Vendor invoice lines** FastTab, select the lines that you want to change.</span></span>
4. <span data-ttu-id="8d688-155">Ja rēķina rindai **Maksāt-kad-apmaksāts** ir izpildīti nosacījumi, atlasiet **Izpildīt piegādātāja maksājumu**.</span><span class="sxs-lookup"><span data-stu-id="8d688-155">If the **Pay when paid** conditions are met for the invoice line, select **Release vendor payment**.</span></span> <span data-ttu-id="8d688-156">Opcija **Maksāt-kad-apmaksāts** tiek notīrīta, un lauka **Gatavs apmaksai** vērtība tiek mainīta uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="8d688-156">The **Pay when paid** option is cleared, and the value of the **Ready for payment** field is changed to **Yes**.</span></span>