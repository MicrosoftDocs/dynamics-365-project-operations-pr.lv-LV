---
title: Konfigurēt iekšējo projektu uzskaiti
description: Šajā tēmā ir sniegta informācija par to, kā iestatīt uzskaites metodes Project Operations iekšējiem projektiem.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ad8b974ef75cb0a4e43af0aa254cec1bbcab154a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012865"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="50ff6-103">Konfigurēt iekšējo projektu uzskaiti</span><span class="sxs-lookup"><span data-stu-id="50ff6-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="50ff6-104">_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="50ff6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="50ff6-105">Iekšējie projekti ļauj uzņēmumiem izsekot izmaksas, kas saistītas ar darbībām, par kurām klientam netiek izrakstīts rēķins.</span><span class="sxs-lookup"><span data-stu-id="50ff6-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="50ff6-106">Iekšējo projektu piemēri ir šādi:</span><span class="sxs-lookup"><span data-stu-id="50ff6-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="50ff6-107">Projekta, piemēram, mobilās programmas, izstrāde un izmaksu izsekošana saistībā ar izstrādi.</span><span class="sxs-lookup"><span data-stu-id="50ff6-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="50ff6-108">Pirmspārdošanas laika un izdevumu pārvaldīšana.</span><span class="sxs-lookup"><span data-stu-id="50ff6-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="50ff6-109">Šo pirmspārdošanas iekšējo projektu vēlāk var pārveidot par rēķinā iekļaujamu projektu, ja piedāvājums tiek iegūts.</span><span class="sxs-lookup"><span data-stu-id="50ff6-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="50ff6-110">Jebkurš projekts, kas nav saistīts ar līgumu, Dynamics 365 Project Operations tiek uzskatīts par iekšēju.</span><span class="sxs-lookup"><span data-stu-id="50ff6-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="50ff6-111">Projekta izmaksu un ieņēmumu profili netiek izmantoti, lai noteiktu projekta uzskaites kārtulas.</span><span class="sxs-lookup"><span data-stu-id="50ff6-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="50ff6-112">Iekšējās projekta izmaksas vienmēr tiek grāmatotas, izmantojot peļņas un zaudējumu principus.</span><span class="sxs-lookup"><span data-stu-id="50ff6-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="50ff6-113">Grāmatojumu virsgrāmatas konti tiek definēti lapā **Virsgrāmatas publicēšanas iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="50ff6-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="50ff6-114">Laika darījumi tiek grāmatoti, debitējot **izmaksu** kontu un kreditējot **algu sadalījuma** kontu.</span><span class="sxs-lookup"><span data-stu-id="50ff6-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="50ff6-115">Izdevumu darījumi tiek grāmatoti, debitējot **izmaksu** kontu un kreditējot **ieskaita kontu izdevumiem**.</span><span class="sxs-lookup"><span data-stu-id="50ff6-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>
- <span data-ttu-id="50ff6-116">Vienību transakcijas tiek grāmatotas, veicot konta **Izmaksas** debetēšanu un konta **Izmaksas — vienība** kreditēšanu.</span><span class="sxs-lookup"><span data-stu-id="50ff6-116">Item transactions are posted by debiting the **Cost** account and crediting the **Cost - Item** account.</span></span>

<span data-ttu-id="50ff6-117">Pēc darbību grāmatošanas projektā, ja projekts ir saistīts ar projekta līgumu, sistēma atceļ visus uzkrātos darījumus un izveido jaunus rēķinā iekļaujamus darījumus.</span><span class="sxs-lookup"><span data-stu-id="50ff6-117">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="50ff6-118">Rēķinā iekļautie darījumi ievēro uzskaites kārtulas, kas definētas atbilstošajā projekta izmaksu un ieņēmumu profilā.</span><span class="sxs-lookup"><span data-stu-id="50ff6-118">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
