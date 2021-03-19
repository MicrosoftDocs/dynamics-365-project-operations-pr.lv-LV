---
title: Dienasnauda
description: Šajā tēmā ir sniegta informācija par dienasnaudas kārtulām, kas tiek izmantotas izdevumu pārvaldībā.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 70e26a5e0f9a06730a2166318006429195335d4d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276312"
---
# <a name="per-diems"></a><span data-ttu-id="27756-103">Dienasnauda</span><span class="sxs-lookup"><span data-stu-id="27756-103">Per diems</span></span>

<span data-ttu-id="27756-104">_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="27756-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="27756-105">Dienasnauda ir pabalsts, ko maksā darba ņēmējam, kurš dodas komandējumā.</span><span class="sxs-lookup"><span data-stu-id="27756-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="27756-106">Izdevumu pārvaldībā varat izveidot dienasnaudas kārtulas dažādām ceļošanas situācijām.</span><span class="sxs-lookup"><span data-stu-id="27756-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="27756-107">Dienasnaudas likmes var būt atkarīgas no gada laika, ceļojuma galamērķa vai abiem.</span><span class="sxs-lookup"><span data-stu-id="27756-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="27756-108">Kad izveidojat dienasnaudas kārtulu, varat norādīt, ka noteikta procentuālā dienasnaudas likme tiek ieturēta, ja darbinieks saņem bezmaksas maltītes vai pakalpojumus.</span><span class="sxs-lookup"><span data-stu-id="27756-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="27756-109">Varat iestatīt arī minimālo un maksimālo stundu skaitu, kam var piemērot darba ņēmēja komandējuma dienasnaudas likmi.</span><span class="sxs-lookup"><span data-stu-id="27756-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="27756-110">Konfigurācija</span><span class="sxs-lookup"><span data-stu-id="27756-110">Configuration</span></span> 

1. <span data-ttu-id="27756-111">Lai pievienotu dienasnaudas atrašanās vietas, ejiet uz **Iestatīšana** > **Aprēķini un kodi** > **Dienasnaudas atrašanās vietas**.</span><span class="sxs-lookup"><span data-stu-id="27756-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="27756-112">Katrai no iepriekš pievienotajām atrašanās vietām atlasiet dienasnaudas likmi un valūtu, kas ir derīga starp noteiktu sākuma un beigu datumu viesnīcas, maltīšu vai citu izdevumu segšanai.</span><span class="sxs-lookup"><span data-stu-id="27756-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="27756-113">Dienasnaudas likmes un valūtas tiek konfigurētas sadaļā **Iestatīšana** > **Aprēķini un kodi** > **Dienasnaudas**.</span><span class="sxs-lookup"><span data-stu-id="27756-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="27756-114">Lapā **Dienasnaudas atrašanās vieta** konfigurējiet dienasnaudas likmju līmeņus.</span><span class="sxs-lookup"><span data-stu-id="27756-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="27756-115">Dienasnaudas likmju līmeņi ļauj definēt ikdienas pabalsta procentuālo sadalījumu attiecībā uz viesnīcas, maltīšu un citiem izdevumiem.</span><span class="sxs-lookup"><span data-stu-id="27756-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="27756-116">Lai norādītu maltīšu procentuālo atskaitījumu brokastīm, pusdienām vai vakariņām, atjauniniet laukus lapā **Izdevumu pārvaldības parametri** cilnē **Dienasnauda**.</span><span class="sxs-lookup"><span data-stu-id="27756-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="27756-117">Izdevumu iesniegšana, izmantojot dienasnaudu</span><span class="sxs-lookup"><span data-stu-id="27756-117">Submit expenses using per diem</span></span>
<span data-ttu-id="27756-118">Lai iesniegtu izdevumus, kas attiecas uz dienasnaudu, izmantojiet izdevumu kategoriju **Dienasnauda**, kad veidojat izdevumu atskaiti.</span><span class="sxs-lookup"><span data-stu-id="27756-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="27756-119">Ievadiet **Dienasnauda no datuma**, **Dienasnauda līdz datumam** un **Dienasnaudas atrašanās vieta**.</span><span class="sxs-lookup"><span data-stu-id="27756-119">Enter the **Per diem from date**, **Per diem to date**,  and the **Per diem location**.</span></span> <span data-ttu-id="27756-120">Summu aprēķina, par pamatu izmantojot dienasnaudas likmes izvēlētajai atrašanās vietai, un atskaitījums par maltītēm tiek aprēķināts, par pamatu izmantojot dienasnaudas likmju līmeņus.</span><span class="sxs-lookup"><span data-stu-id="27756-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]