---
title: Izveidot manuālu proformas rēķinu — Lite
description: Šajā tēmā ir sniegta informācija par manuāla proforma rēķina izveidi risinājumā Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 104c2f3f7f0ca0682158d0f7fa0f50a4967e6dd0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274197"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="51893-103">Izveidot manuālu proformas rēķinu — Lite</span><span class="sxs-lookup"><span data-stu-id="51893-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="51893-104">_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_</span><span class="sxs-lookup"><span data-stu-id="51893-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="51893-105">Programmā Dynamics 365 Project Operations proformas rēķinus pēc nepieciešamības var izveidot manuāli.</span><span class="sxs-lookup"><span data-stu-id="51893-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="51893-106">Proforma rēķinu manuāli var izveidot no saraksta lapas **Projekta līgumi** vai informācijas lapas **Projekta līgums**.</span><span class="sxs-lookup"><span data-stu-id="51893-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="51893-107">Saraksta lapa Projekta līgums</span><span class="sxs-lookup"><span data-stu-id="51893-107">Project Contracts list page</span></span>

<span data-ttu-id="51893-108">Saraksta lapā **Projekta līgums** atlasiet vienu vai vairākus projekta līgumus un izveidojiet rēķinus visiem atlasītajiem ierakstiem.</span><span class="sxs-lookup"><span data-stu-id="51893-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="51893-109">Sistēma pārbauda, lai skatītu, kuriem no atlasītajiem projekta līgumiem ir rezerve **Gatavs rēķina izrakstīšanai** ar datumu pirms šodienas datuma.</span><span class="sxs-lookup"><span data-stu-id="51893-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="51893-110">No šiem līgumiem sistēma izveido proforma rēķinu melnrakstus.</span><span class="sxs-lookup"><span data-stu-id="51893-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="51893-111">Ja projekta līgumam ir vairāki klienti, katram klientam var izveidot vienu rēķinu, kā arī vairākus rēķinus katram projekta līgumam.</span><span class="sxs-lookup"><span data-stu-id="51893-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="51893-112">Visi izveidotie projekta rēķini ir pieejami apgabala **Pārdošana** lapas **Rēķins** sadaļā **Norēķini**.</span><span class="sxs-lookup"><span data-stu-id="51893-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="51893-113">Informācijas lapa Projekta līgums</span><span class="sxs-lookup"><span data-stu-id="51893-113">Project Contract details page</span></span>

<span data-ttu-id="51893-114">Proformas rēķinu var arī izveidot no **Projekta līguma** informācijas lapas.</span><span class="sxs-lookup"><span data-stu-id="51893-114">A proforma invoice can also be created from the **Project Contract** details page.</span></span> <span data-ttu-id="51893-115">Sistēma pārbauda, vai projekta līgumam ir rezerve **Gatavs rēķina izrakstīšanai** ar datumu pirms šodienas datuma.</span><span class="sxs-lookup"><span data-stu-id="51893-115">The system verifies the project contract has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="51893-116">No šiem līgumiem sistēma izveido proforma rēķinu melnrakstus, pamatojoties uz klientu skaitu katrā rēķina rindā.</span><span class="sxs-lookup"><span data-stu-id="51893-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="51893-117">Ja ir izveidots viens proforma rēķins, tiek atvērta lapa **Rēķins**.</span><span class="sxs-lookup"><span data-stu-id="51893-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="51893-118">Ja šim projektam tiek izveidoti vairāki rēķini, tiek atvērta saraksta lapa **Rēķini**, lai rādītu visus izveidotos rēķinus.</span><span class="sxs-lookup"><span data-stu-id="51893-118">If multiple invoices are created for that project contract, the **Invoices** list page opens to show all of the created invoices.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]