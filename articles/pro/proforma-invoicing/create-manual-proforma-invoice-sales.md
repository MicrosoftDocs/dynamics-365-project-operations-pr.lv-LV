---
title: Manuāla proformas rēķina izveide
description: Šajā tēmā ir sniegta informācija par manuāla proforma rēķina izveidi risinājumā Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5e93206737507bf6698a9746815c790d3dfc904
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/20/2020
ms.locfileid: "4080673"
---
# <a name="creating-a-manual-proforma-invoice"></a><span data-ttu-id="57612-103">Manuāla proformas rēķina izveide</span><span class="sxs-lookup"><span data-stu-id="57612-103">Creating a manual proforma invoice</span></span>

<span data-ttu-id="57612-104">_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_</span><span class="sxs-lookup"><span data-stu-id="57612-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="57612-105">Risinājumā Dynamics 365 Project Operations proforma rēķinus var izveidot manuāli, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="57612-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="57612-106">Proforma rēķinu manuāli var izveidot no saraksta lapas **Projekta līgumi** vai informācijas lapas **Projekta līgums**.</span><span class="sxs-lookup"><span data-stu-id="57612-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="57612-107">Saraksta lapa Projekta līgums</span><span class="sxs-lookup"><span data-stu-id="57612-107">Project Contracts list page</span></span>

<span data-ttu-id="57612-108">Saraksta lapā **Projekta līgums** atlasiet vienu vai vairākus projekta līgumus un izveidojiet rēķinus visiem atlasītajiem ierakstiem.</span><span class="sxs-lookup"><span data-stu-id="57612-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="57612-109">Sistēma pārbauda, lai skatītu, kuriem no atlasītajiem projekta līgumiem ir rezerve **Gatavs rēķina izrakstīšanai** ar datumu pirms šodienas datuma.</span><span class="sxs-lookup"><span data-stu-id="57612-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog  dated before today's date.</span></span> <span data-ttu-id="57612-110">No šiem līgumiem sistēma izveido proforma rēķinu melnrakstus.</span><span class="sxs-lookup"><span data-stu-id="57612-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="57612-111">Ja projekta līgumam ir vairāki klienti, katram klientam var izveidot vienu rēķinu, kā arī vairākus rēķinus katram projekta līgumam.</span><span class="sxs-lookup"><span data-stu-id="57612-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="57612-112">Visi izveidotie projekta rēķini ir pieejami apgabala **Pārdošana** lapas **Rēķins** sadaļā **Norēķini**.</span><span class="sxs-lookup"><span data-stu-id="57612-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="57612-113">Informācijas lapa Projekta līgums</span><span class="sxs-lookup"><span data-stu-id="57612-113">Project Contract details page</span></span>

<span data-ttu-id="57612-114">Proforma rēķinu var izveidot arī no informācijas lapas **Projekta līgums** , kas izveido rēķinu šim konkrētajam projekta līgumam.</span><span class="sxs-lookup"><span data-stu-id="57612-114">A proforma invoice can also be created from the **Project Contract** details page, which creates the invoice for that specific project contract.</span></span> <span data-ttu-id="57612-115">Sistēma pārbauda, vai projekta līgumam ir rezerve **Gatavs rēķina izrakstīšanai** ar datumu pirms šodienas datuma.</span><span class="sxs-lookup"><span data-stu-id="57612-115">The system verifies that the project contract has a **Ready to Invoice** backlog that is dated before today's date.</span></span> <span data-ttu-id="57612-116">No šiem līgumiem sistēma izveido proforma rēķinu melnrakstus, pamatojoties uz klientu skaitu katrā rēķina rindā.</span><span class="sxs-lookup"><span data-stu-id="57612-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="57612-117">Ja ir izveidots viens proforma rēķins, tiek atvērta lapa **Rēķins**.</span><span class="sxs-lookup"><span data-stu-id="57612-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="57612-118">Ja šim projekta līgumam ir izveidoti vairāki rēķini, tiek atvērta saraksta lapa **Rēķini** , lai parādītu visus izveidotos rēķinus.</span><span class="sxs-lookup"><span data-stu-id="57612-118">If there are multiple invoices created for that project contract, then the **Invoices** list page opens to show all of the created invoices.</span></span>
