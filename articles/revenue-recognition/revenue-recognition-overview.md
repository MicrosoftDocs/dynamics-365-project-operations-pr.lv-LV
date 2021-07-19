---
title: Ieņēmumu atpazīšanas pārskats
description: Šajā tēmā ir sniegta informācija par ieņēmumu atpazīšanu risinājumā Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: ab9b36b71223b1bcfe48de5f9b68b6fb6a98f388
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368035"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="51756-103">Ieņēmumu atpazīšanas pārskats</span><span class="sxs-lookup"><span data-stu-id="51756-103">Revenue recognition overview</span></span>

<span data-ttu-id="51756-104">_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="51756-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="51756-105">Risinājumā Dynamics 365 Project Operations ieņēmumu atpazīšanas principi atšķiras atkarībā no atlasītās norēķinu metodes projektam vai projekta daļai.</span><span class="sxs-lookup"><span data-stu-id="51756-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="51756-106">Šajā tēmā ir sniegta informācija par ieņēmumu atpazīšanu risinājumā Project Operations.</span><span class="sxs-lookup"><span data-stu-id="51756-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="51756-107">Transakcijas, kas uzskaitītas, izmantojot laika un materiālu norēķinu metodi</span><span class="sxs-lookup"><span data-stu-id="51756-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="51756-108">Izmaksu un ieņēmumu atpazīšana ir saistīta.</span><span class="sxs-lookup"><span data-stu-id="51756-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="51756-109">Transakciju izmaksas un rēķinā neiekļautās pārdošanas transakcijas tiek grāmatotas, izmantojot [Project Operations integrācijas žurnālu](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="51756-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="51756-110">Projekta izmaksu un ieņēmumu profils nosaka, vai rēķinā neiekļautās pārdošanas transakcijas tiek grāmatotas virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="51756-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="51756-111">Ja atlasīta opcija **Uzkrāt ieņēmumus**, sistēma grāmatošanas laikā izmanto kontus **NP pārdošanas vērtība** un **Uzkrāto ieņēmumu pārdošanas vērtība**.</span><span class="sxs-lookup"><span data-stu-id="51756-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="51756-112">Tālāk sniegts šīs metodes piemērs.</span><span class="sxs-lookup"><span data-stu-id="51756-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="51756-113">Transakcijas veids</span><span class="sxs-lookup"><span data-stu-id="51756-113">Transaction type</span></span> | <span data-ttu-id="51756-114">Debets/kredīts</span><span class="sxs-lookup"><span data-stu-id="51756-114">Debit/Credit</span></span> | <span data-ttu-id="51756-115">Apjoms/summa</span><span class="sxs-lookup"><span data-stu-id="51756-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="51756-116">NP pārdošanas vērtība</span><span class="sxs-lookup"><span data-stu-id="51756-116">WIP Sales value</span></span> | <span data-ttu-id="51756-117">Debets</span><span class="sxs-lookup"><span data-stu-id="51756-117">Debit</span></span> | <span data-ttu-id="51756-118">100</span><span class="sxs-lookup"><span data-stu-id="51756-118">100</span></span> |
  | <span data-ttu-id="51756-119">Uzkrāto ieņēmumu pārdošanas vērtība</span><span class="sxs-lookup"><span data-stu-id="51756-119">Accrued revenue sales value</span></span> | <span data-ttu-id="51756-120">Kredīts</span><span class="sxs-lookup"><span data-stu-id="51756-120">Credit</span></span> | <span data-ttu-id="51756-121">100</span><span class="sxs-lookup"><span data-stu-id="51756-121">100</span></span> |

- <span data-ttu-id="51756-122">Ieņēmumi tiek atpazīti, izrakstot rēķinus.</span><span class="sxs-lookup"><span data-stu-id="51756-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="51756-123">Grāmatošanas laikā sistēma izmanto kontu **Rēķinā iekļautie ieņēmumi**.</span><span class="sxs-lookup"><span data-stu-id="51756-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="51756-124">Tālāk sniegts šīs metodes piemērs.</span><span class="sxs-lookup"><span data-stu-id="51756-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="51756-125">Transakcijas veids</span><span class="sxs-lookup"><span data-stu-id="51756-125">Transaction type</span></span> | <span data-ttu-id="51756-126">Debets/kredīts</span><span class="sxs-lookup"><span data-stu-id="51756-126">Debit/Credit</span></span> | <span data-ttu-id="51756-127">Apjoms/summa</span><span class="sxs-lookup"><span data-stu-id="51756-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="51756-128">Klienta bilance</span><span class="sxs-lookup"><span data-stu-id="51756-128">Customer balance</span></span> | <span data-ttu-id="51756-129">Debets</span><span class="sxs-lookup"><span data-stu-id="51756-129">Debit</span></span> | <span data-ttu-id="51756-130">120</span><span class="sxs-lookup"><span data-stu-id="51756-130">120</span></span> |
  | <span data-ttu-id="51756-131">Maksājamais PVN</span><span class="sxs-lookup"><span data-stu-id="51756-131">Sales tax payable</span></span> | <span data-ttu-id="51756-132">Kredīts</span><span class="sxs-lookup"><span data-stu-id="51756-132">Credit</span></span> | <span data-ttu-id="51756-133">20</span><span class="sxs-lookup"><span data-stu-id="51756-133">20</span></span> |
  | <span data-ttu-id="51756-134">Ieņēmumi, par ko izrakstīts rēķins</span><span class="sxs-lookup"><span data-stu-id="51756-134">Invoiced Revenue</span></span> | <span data-ttu-id="51756-135">Kredīts</span><span class="sxs-lookup"><span data-stu-id="51756-135">Credit</span></span> | <span data-ttu-id="51756-136">100</span><span class="sxs-lookup"><span data-stu-id="51756-136">100</span></span> |

- <span data-ttu-id="51756-137">Ja ieņēmumi tika uzkrāti, grāmatojot rēķinā neiekļautās pārdošanas transakcijas, sistēma atsauc uzkrātos ieņēmumus rēķina izrakstīšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="51756-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="51756-138">Transakcijas veids</span><span class="sxs-lookup"><span data-stu-id="51756-138">Transaction type</span></span> | <span data-ttu-id="51756-139">Debets/kredīts</span><span class="sxs-lookup"><span data-stu-id="51756-139">Debit/Credit</span></span> | <span data-ttu-id="51756-140">Apjoms/summa</span><span class="sxs-lookup"><span data-stu-id="51756-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="51756-141">NP pārdošanas vērtība</span><span class="sxs-lookup"><span data-stu-id="51756-141">WIP Sales value</span></span> | <span data-ttu-id="51756-142">Kredīts</span><span class="sxs-lookup"><span data-stu-id="51756-142">Credit</span></span> | <span data-ttu-id="51756-143">100</span><span class="sxs-lookup"><span data-stu-id="51756-143">100</span></span> |
  | <span data-ttu-id="51756-144">Uzkrāto ieņēmumu pārdošanas vērtība</span><span class="sxs-lookup"><span data-stu-id="51756-144">Accrued revenue sales value</span></span> | <span data-ttu-id="51756-145">Debets</span><span class="sxs-lookup"><span data-stu-id="51756-145">Debit</span></span> | <span data-ttu-id="51756-146">100</span><span class="sxs-lookup"><span data-stu-id="51756-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="51756-147">Transakcijas, kas uzskaitītas, izmantojot fiksētas cenas norēķinu metodi</span><span class="sxs-lookup"><span data-stu-id="51756-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="51756-148">Izmaksu un ieņēmumu atpazīšana ir atdalīta.</span><span class="sxs-lookup"><span data-stu-id="51756-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="51756-149">Transakciju izmaksas tiek grāmatotas, izmantojot [Project Operations integrācijas žurnālu](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="51756-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="51756-150">Netiek izveidotas rēķinā neiekļautas pārdošanas transakcijas.</span><span class="sxs-lookup"><span data-stu-id="51756-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="51756-151">Ieņēmumus var atpazīt rēķinu izrakstīšanas laikā, ja projekta izmaksu un ieņēmumu profila opcija **Projekta pabeigšanas aprēķiniem izmantotais princips** ir iestatīta uz **Bez NP**.</span><span class="sxs-lookup"><span data-stu-id="51756-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="51756-152">Izmantojiet šo metodi tikai vienkāršiem īstermiņa projektiem.</span><span class="sxs-lookup"><span data-stu-id="51756-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="51756-153">Ieņēmumus var atpazīt, izmantojot fiksētas cenas ieņēmumu novērtējumus ar metodi **Pabeigts līgums** vai **Ieņēmumu atpazīšana, izmantojot pabeigšanas procentuālo vērtību**.</span><span class="sxs-lookup"><span data-stu-id="51756-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="51756-154">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="51756-154">Additional resources</span></span>
[<span data-ttu-id="51756-155">Raksts Apmaksājamo projektu uzskaites konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="51756-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="51756-156">Fiksētas cenas ieņēmumu novērtējumu projekti</span><span class="sxs-lookup"><span data-stu-id="51756-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="51756-157">Ieņēmumu novērtējumu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="51756-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="51756-158">Pabeigšanas izmaksu metodes</span><span class="sxs-lookup"><span data-stu-id="51756-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]