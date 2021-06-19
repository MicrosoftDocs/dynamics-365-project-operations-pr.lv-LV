---
title: Finanšu dimensiju noklusējumi
description: Šajā tēmā ir sniegta informācija par to, kā iestatīt finanšu dimensiju noklusējumus.
author: sigitac
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d2509f74d34ac3dce4c6915ca860283750eb50b1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013315"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="c808b-103">Finanšu dimensiju noklusējumi</span><span class="sxs-lookup"><span data-stu-id="c808b-103">Financial dimension defaults</span></span>

<span data-ttu-id="c808b-104">_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="c808b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c808b-105">Dynamics 365 Project Operations izmanto [Finanšu dimensiju](/dynamics365/finance/general-ledger/financial-dimensions) struktūru programmā Dynamics 365 Finance, lai sniegtu papildu ieskatus projekta apakšgrāmatas un virsgrāmatas darbībās.</span><span class="sxs-lookup"><span data-stu-id="c808b-105">Dynamics 365 Project Operations uses the [Financial dimensions](/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="c808b-106">Noklusējuma finanšu dimensijas var iestatīt klientam, projekta finansējuma avotam, atskaites punktam, projekta līguma rindai vai projektam.</span><span class="sxs-lookup"><span data-stu-id="c808b-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="c808b-107">Debitora noklusējuma finanšu dimensiju definēšana</span><span class="sxs-lookup"><span data-stu-id="c808b-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="c808b-108">Debitoru dimensiju noklusējuma iestatījumi ir norādīti finanšu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="c808b-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="c808b-109">Lai iestatītu dimensiju noklusējuma iestatījumus, paveiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="c808b-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="c808b-110">Dodieties uz **Debitori** > **Klienti** > **Visi klienti**.</span><span class="sxs-lookup"><span data-stu-id="c808b-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="c808b-111">Lapas **Klienti** cilnē **Finanšu dimensijas** iestatiet finanšu dimensiju vērtības noteiktajam klientam.</span><span class="sxs-lookup"><span data-stu-id="c808b-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="c808b-112">Projekta līguma noklusējuma finanšu dimensiju definēšana</span><span class="sxs-lookup"><span data-stu-id="c808b-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="c808b-113">Projekta līgumi tiek izveidoti un uzturēti pakalpojumā Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="c808b-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="c808b-114">Projekta līgumu uzskaites atribūti tiek iestatīti Finanšu modulī **Projekta pārvaldība un uzskaite**.</span><span class="sxs-lookup"><span data-stu-id="c808b-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="c808b-115">Finanšu dimensiju iestatīšana projekta finansējuma avotam</span><span class="sxs-lookup"><span data-stu-id="c808b-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="c808b-116">Dodieties uz **Projekta pārvaldība un uzskaite** > **Projekti** > **Projekta līgumi**.</span><span class="sxs-lookup"><span data-stu-id="c808b-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="c808b-117">Atlasiet ierakstu, kuru vēlaties atjaunināt, un cilnē **Projekta līgums** atlasiet **Rādīt noklusējuma uzskaiti**.</span><span class="sxs-lookup"><span data-stu-id="c808b-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="c808b-118">Izvērsiet sadaļu **Saistītā informācija** un atlasiet cilni **Finansējuma avoti**.</span><span class="sxs-lookup"><span data-stu-id="c808b-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="c808b-119">Iestatiet finanšu dimensijas noklusējumus.</span><span class="sxs-lookup"><span data-stu-id="c808b-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="c808b-120">Ņemiet vērā, ka finanšu dimensiju noklusējuma vērtība ir no klienta uzņēmuma.</span><span class="sxs-lookup"><span data-stu-id="c808b-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="c808b-121">Finanšu dimensiju iestatīšana projekta līguma rindai</span><span class="sxs-lookup"><span data-stu-id="c808b-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="c808b-122">Dodieties uz **Projekta pārvaldība un uzskaite** > **Projekti** > **Projekta līgumi**.</span><span class="sxs-lookup"><span data-stu-id="c808b-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="c808b-123">Atlasiet ierakstu, kuru vēlaties atjaunināt, un cilnē **Projekta līgums** atlasiet **Rādīt noklusējuma uzskaiti**.</span><span class="sxs-lookup"><span data-stu-id="c808b-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="c808b-124">Izvērsiet sadaļu **Saistītā informācija** un atlasiet cilni **Līguma rindas**.</span><span class="sxs-lookup"><span data-stu-id="c808b-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="c808b-125">Iestatiet finanšu dimensijas noklusējumus.</span><span class="sxs-lookup"><span data-stu-id="c808b-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="c808b-126">Finanšu dimensiju noklusējumi ir piemērojami un tos var izmantot tikai ar fiksētas cenas (atskaites punkta) līguma rindām.</span><span class="sxs-lookup"><span data-stu-id="c808b-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="c808b-127">Šie noklusējumi tiek izmantoti saistītā projekta uzņēmuma transakcijās un rēķina rindās.</span><span class="sxs-lookup"><span data-stu-id="c808b-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="c808b-128">Projektu noklusējuma finanšu dimensiju definēšana</span><span class="sxs-lookup"><span data-stu-id="c808b-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="c808b-129">Projekti tiek izveidoti un uzturēti pakalpojumā CDS.</span><span class="sxs-lookup"><span data-stu-id="c808b-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="c808b-130">Projektu uzskaites atribūti tiek iestatīti Finanšu modulī **Projekta pārvaldība un uzskaite**.</span><span class="sxs-lookup"><span data-stu-id="c808b-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="c808b-131">Dodieties uz **Projekta pārvaldība un uzskaite** > **Projekti** > **Visi projekti**.</span><span class="sxs-lookup"><span data-stu-id="c808b-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="c808b-132">Atlasiet ierakstu, kuru vēlaties atjaunināt, un cilnē **Projekts** atlasiet **Rādīt noklusējuma uzskaiti**.</span><span class="sxs-lookup"><span data-stu-id="c808b-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="c808b-133">Izvērsiet sadaļu **Saistītā informācija** un atlasiet cilni **Iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="c808b-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="c808b-134">Iestatiet finanšu dimensijas noklusējumus.</span><span class="sxs-lookup"><span data-stu-id="c808b-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="c808b-135">Ņemiet vērā, ka finanšu dimensiju noklusējuma vērtība ir no klienta uzņēmuma.</span><span class="sxs-lookup"><span data-stu-id="c808b-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="c808b-136">Ja projekts ir saistīts ar līguma rindu ar vairākiem projekta līguma klientiem, primārais klients tiek izmantots noklusējuma finanšu dimensijās.</span><span class="sxs-lookup"><span data-stu-id="c808b-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="c808b-137">Projektu noklusējuma finanšu dimensijas izmanto, lai iestatītu žurnāla rindas noklusējuma vērtības laika, izdevumu un maksu darbībām **Project Operations integrācijas žurnālā** un ar to saistītajās projekta rēķina rindās.</span><span class="sxs-lookup"><span data-stu-id="c808b-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]