---
title: Konfigurēt iekšējo projektu uzskaiti
description: Šajā tēmā ir sniegta informācija par to, kā iestatīt uzskaites metodes Project Operations iekšējiem projektiem.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9f1cc75b12fec81d726e46f8d970dcfe030f6b29
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287607"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="398b6-103">Konfigurēt iekšējo projektu uzskaiti</span><span class="sxs-lookup"><span data-stu-id="398b6-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="398b6-104">_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="398b6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="398b6-105">Iekšējie projekti ļauj uzņēmumiem izsekot izmaksas, kas saistītas ar darbībām, par kurām klientam netiek izrakstīts rēķins.</span><span class="sxs-lookup"><span data-stu-id="398b6-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="398b6-106">Iekšējo projektu piemēri ir šādi:</span><span class="sxs-lookup"><span data-stu-id="398b6-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="398b6-107">Projekta, piemēram, mobilās programmas, izstrāde un izmaksu izsekošana saistībā ar izstrādi.</span><span class="sxs-lookup"><span data-stu-id="398b6-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="398b6-108">Pirmspārdošanas laika un izdevumu pārvaldīšana.</span><span class="sxs-lookup"><span data-stu-id="398b6-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="398b6-109">Šo pirmspārdošanas iekšējo projektu vēlāk var pārveidot par rēķinā iekļaujamu projektu, ja piedāvājums tiek iegūts.</span><span class="sxs-lookup"><span data-stu-id="398b6-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="398b6-110">Jebkurš projekts, kas nav saistīts ar līgumu, Dynamics 365 Project Operations tiek uzskatīts par iekšēju.</span><span class="sxs-lookup"><span data-stu-id="398b6-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="398b6-111">Projekta izmaksu un ieņēmumu profili netiek izmantoti, lai noteiktu projekta uzskaites kārtulas.</span><span class="sxs-lookup"><span data-stu-id="398b6-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="398b6-112">Iekšējās projekta izmaksas vienmēr tiek grāmatotas, izmantojot peļņas un zaudējumu principus.</span><span class="sxs-lookup"><span data-stu-id="398b6-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="398b6-113">Grāmatojumu virsgrāmatas konti tiek definēti lapā **Virsgrāmatas publicēšanas iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="398b6-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="398b6-114">Laika darījumi tiek grāmatoti, debitējot **izmaksu** kontu un kreditējot **algu sadalījuma** kontu.</span><span class="sxs-lookup"><span data-stu-id="398b6-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="398b6-115">Izdevumu darījumi tiek grāmatoti, debitējot **izmaksu** kontu un kreditējot **ieskaita kontu izdevumiem**.</span><span class="sxs-lookup"><span data-stu-id="398b6-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>

<span data-ttu-id="398b6-116">Pēc darbību grāmatošanas projektā, ja projekts ir saistīts ar projekta līgumu, sistēma atceļ visus uzkrātos darījumus un izveido jaunus rēķinā iekļaujamus darījumus.</span><span class="sxs-lookup"><span data-stu-id="398b6-116">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="398b6-117">Rēķinā iekļautie darījumi ievēro uzskaites kārtulas, kas definētas atbilstošajā projekta izmaksu un ieņēmumu profilā.</span><span class="sxs-lookup"><span data-stu-id="398b6-117">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]