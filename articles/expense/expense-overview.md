---
title: Izdevumu pārskats
description: Šajā tēmā ir sniegta informācija par izdevumu funkcionalitāti risinājumā Project Operations.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 6da831fef5dba060b8019d7689645405c7ebdbed
ms.sourcegitcommit: 0874b3d89e1dc0e65a51cedb82bf8f80831ca0bb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/06/2020
ms.locfileid: "3967375"
---
# <a name="expense-home-page"></a><span data-ttu-id="520d2-103">Sākumlapas izdevumi</span><span class="sxs-lookup"><span data-stu-id="520d2-103">Expense home page</span></span>

<span data-ttu-id="520d2-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="520d2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="520d2-105">Dynamics 365 Project Operations atbalsta iespēju apstrādāt izdevumus.</span><span class="sxs-lookup"><span data-stu-id="520d2-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="520d2-106">Izdevumu apstrāde notiek ar vai bez projektiem, izmantojot pielāgojamu politiku, darījumu kategoriju un apstiprinājumu darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="520d2-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="520d2-107">Risinājumā Project Operations ir divi atbalstīti Izdevumu izvietošanas modeļi:</span><span class="sxs-lookup"><span data-stu-id="520d2-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="520d2-108">**Pilna**: pilna izvietošana ir pieejama **Project Operations scenārijiem, kas balstīti uz resursiem/nav balstīti uz krājumiem**, vai **Project Operations scenārijiem, kas balstīti uz ražošanas pasūtījumiem**.</span><span class="sxs-lookup"><span data-stu-id="520d2-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order based scenarios**.</span></span>
- <span data-ttu-id="520d2-109">**Pamata**: pamata izvietošana ir pieejama **Project Operations scenārijiem, kas balstīti uz resursiem/nav balstīti uz krājumiem** un **Lite izvietošanai — pārejai uz proforma rēķina izrakstīšanu**.</span><span class="sxs-lookup"><span data-stu-id="520d2-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="520d2-110">Pilntiesīgs</span><span class="sxs-lookup"><span data-stu-id="520d2-110">Full</span></span> 
<span data-ttu-id="520d2-111">Pilna Izdevumu izvietošana nodrošina pilnīgu politikas izpildi, kas ietver iespēju izveidot politikas, piemēram:</span><span class="sxs-lookup"><span data-stu-id="520d2-111">Full Expense deployment provides a complete policy enforcement which includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="520d2-112">Izdevumu kategorijas ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="520d2-112">Expense category limits</span></span>
  - <span data-ttu-id="520d2-113">Ceļš</span><span class="sxs-lookup"><span data-stu-id="520d2-113">Travel</span></span>
  - <span data-ttu-id="520d2-114">Dienasnauda</span><span class="sxs-lookup"><span data-stu-id="520d2-114">Per diem</span></span>
  - <span data-ttu-id="520d2-115">Kredītkartes importēšana</span><span class="sxs-lookup"><span data-stu-id="520d2-115">Credit card imports</span></span>
  - <span data-ttu-id="520d2-116">Rakstzīmju optiskā atpazīšana kvītīs</span><span class="sxs-lookup"><span data-stu-id="520d2-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="520d2-117">Pamatiespējas</span><span class="sxs-lookup"><span data-stu-id="520d2-117">Basic</span></span> 
<span data-ttu-id="520d2-118">Pamata Izmaksu izvietošanas scenārijs ļauj tikai ierakstīt pamata izmaksas saistībā ar projektu.</span><span class="sxs-lookup"><span data-stu-id="520d2-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="520d2-119">Papildinformāciju skatiet šeit: [Izdevumu ievade (Lite)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="520d2-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="520d2-120">Nosakiet savu Izdevumu izvietošanu</span><span class="sxs-lookup"><span data-stu-id="520d2-120">Determine your Expense deployment</span></span>
<span data-ttu-id="520d2-121">Lai noteiktu, vai darbināt Pamata izmaksu pārvaldības izvietošanu, pārbaudiet, vai adreses URL vietrādis beidzas ar **. crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="520d2-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 
