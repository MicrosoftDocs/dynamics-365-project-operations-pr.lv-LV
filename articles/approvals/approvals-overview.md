---
title: Apstiprinājumu pārskats
description: Šajā tēmā ir sniegta informācija par darbu ar apstiprinājumiem programmā Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080304"
---
# <a name="approvals-overview"></a><span data-ttu-id="8ecce-103">Apstiprinājumu pārskats</span><span class="sxs-lookup"><span data-stu-id="8ecce-103">Approvals overview</span></span>

<span data-ttu-id="8ecce-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="8ecce-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8ecce-105">Iesniegtajiem Laika un Izdevumu datiem tiek veikta apstiprinājumu darbplūsma.</span><span class="sxs-lookup"><span data-stu-id="8ecce-105">Time and Expense submissions move through an approval workflow.</span></span> <span data-ttu-id="8ecce-106">Pēc ievadīto datu apstiprināšanas darījumi tiek reģistrēti faktiskajos datos vai laika grafikā tiek rezervēts laiks.</span><span class="sxs-lookup"><span data-stu-id="8ecce-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="8ecce-107">Apstiprinājumu darbplūsma</span><span class="sxs-lookup"><span data-stu-id="8ecce-107">Approvals workflow</span></span>
<span data-ttu-id="8ecce-108">Kad izveidojat un iesniedzat laika vai izdevumu ierakstu, tiek izveidots apstiprinājuma ieraksts.</span><span class="sxs-lookup"><span data-stu-id="8ecce-108">When you create and submit a time or expense entry, an approval entry is created.</span></span> <span data-ttu-id="8ecce-109">Projekta apstiprinātājs vai jūsu vadītājs izskata un apstiprina jūsu ierakstu.</span><span class="sxs-lookup"><span data-stu-id="8ecce-109">The Project approver or your manager reviews and approves your entry.</span></span> <span data-ttu-id="8ecce-110">Ja ieraksts apstiprināšanas brīdī ir saistīts ar projektu, tiek izveidoti faktiskie dati.</span><span class="sxs-lookup"><span data-stu-id="8ecce-110">If the entry is related to a project, when it's approved, the actuals will be created.</span></span> <span data-ttu-id="8ecce-111">Tādējādi var izsekot izmaksām un norēķiniem.</span><span class="sxs-lookup"><span data-stu-id="8ecce-111">This allows the cost and billing to be tracked.</span></span> 

## <a name="approve-an-entry"></a><span data-ttu-id="8ecce-112">Ieraksta apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="8ecce-112">Approve an entry</span></span>
<span data-ttu-id="8ecce-113">Veidlapa **Apstiprinājumi** jums ļauj pārslēgt dažādus skatus, lai jūs varētu skatīt dažādos apstiprinājumu veidus.</span><span class="sxs-lookup"><span data-stu-id="8ecce-113">The **Approvals** form allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="8ecce-114">Dodieties uz veidlapu **Apstiprinājumi** un atlasiet vienumu **Izdevumi** , **Laiks** vai **Atsaukšanas**.</span><span class="sxs-lookup"><span data-stu-id="8ecce-114">Go to the **Approvals** form and select **Expenses** , **Time** , or **Recalls**.</span></span>
2. <span data-ttu-id="8ecce-115">Pārskatiet katru apstiprinājumu un atlasiet tos, ko vēlaties apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="8ecce-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="8ecce-116">Lai apstiprinātu atlasītos ierakstus, atlasiet **Apstiprināt**.</span><span class="sxs-lookup"><span data-stu-id="8ecce-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="8ecce-117">Sistēma apstrādās šos ierakstus un izveidos faktiskos datus vai rezervāciju.</span><span class="sxs-lookup"><span data-stu-id="8ecce-117">The system will process these entries and create actuals or a booking.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="8ecce-118">Ieraksta noraidīšana</span><span class="sxs-lookup"><span data-stu-id="8ecce-118">Reject an entry</span></span>
<span data-ttu-id="8ecce-119">Jums kā Projekta apstiprinātājam var nākties sūtīt ierakstu atpakaļ lietotājam, lai tas veiktu labojumus.</span><span class="sxs-lookup"><span data-stu-id="8ecce-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="8ecce-120">Dodieties uz veidlapu **Apstiprinājumi** un atlasiet noraidāmo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="8ecce-120">Go to the **Approvals** form and select the entry to reject.</span></span> 
2. <span data-ttu-id="8ecce-121">Atlasiet vienumu **Noraidīt**.</span><span class="sxs-lookup"><span data-stu-id="8ecce-121">Select **Reject**.</span></span>
3. <span data-ttu-id="8ecce-122">Pēc izvēles – pievienojiet komentāru dialogā **Noraidīšanas komentāri** , lai informētu lietotāju par ieraksta noraidīšanas iemesliem.</span><span class="sxs-lookup"><span data-stu-id="8ecce-122">Optional - Add a comment in the **Rejection Comments** dialog to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="8ecce-123">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="8ecce-123">Select **OK**.</span></span> <span data-ttu-id="8ecce-124">Ieraksts tiks atgriezts lietotājam.</span><span class="sxs-lookup"><span data-stu-id="8ecce-124">The entry will be returned to the user.</span></span>
  
## <a name="recall-entries"></a><span data-ttu-id="8ecce-125">Ierakstu atsaukšana</span><span class="sxs-lookup"><span data-stu-id="8ecce-125">Recall entries</span></span>
<span data-ttu-id="8ecce-126">Jums var rasties vajadzība atsaukt iesniegtu ierakstu.</span><span class="sxs-lookup"><span data-stu-id="8ecce-126">At some point, you might need to recall a submitted entry.</span></span> <span data-ttu-id="8ecce-127">Ja ieraksts vēl nav apstiprināts, tas tiek atgriezts nekavējoties.</span><span class="sxs-lookup"><span data-stu-id="8ecce-127">If the entry has not been approved, it will be returned immediately.</span></span> <span data-ttu-id="8ecce-128">Taču apstiprinātam ierakstam var būt būtiska ietekme.</span><span class="sxs-lookup"><span data-stu-id="8ecce-128">An approved entry however, may have a material impact.</span></span> <span data-ttu-id="8ecce-129">Projekta apstiprinātājam jāapstiprina atsaukšana, lai darījums tiktu atsaukts Faktiskajos datos.</span><span class="sxs-lookup"><span data-stu-id="8ecce-129">The Project approver is required to approve the recall in order to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="8ecce-130">Projekta apstiprinātāju norādīšana</span><span class="sxs-lookup"><span data-stu-id="8ecce-130">Specify Project approvers</span></span>
<span data-ttu-id="8ecce-131">Katram projektam ir vairāki projekta darba grupas dalībnieki/</span><span class="sxs-lookup"><span data-stu-id="8ecce-131">Each project has a number of project team members.</span></span> <span data-ttu-id="8ecce-132">Varat norādīt, kuri darba grupas dalībnieki ir arī Projekta apstiprinātāji.</span><span class="sxs-lookup"><span data-stu-id="8ecce-132">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="8ecce-133">Dodieties uz veidlapu **Projekti** un atveriet projektu no saraksta.</span><span class="sxs-lookup"><span data-stu-id="8ecce-133">Go to the **Projects** form and open the project from the list.</span></span>
2. <span data-ttu-id="8ecce-134">Cilnē **Darba grupa** atlasiet darba grupas dalībnieku, kurš būs Projekta apstiprinātājs, un pēc tam atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="8ecce-134">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="8ecce-135">Iestatiet lauku **Projekta apstiprinātājs** stāvoklī **Jā**.</span><span class="sxs-lookup"><span data-stu-id="8ecce-135">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="8ecce-136">Atlasiet vienumu **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="8ecce-136">Select **Save**.</span></span>
5. <span data-ttu-id="8ecce-137">Lai pievienotu papildu Projekta apstiprinātājus, atkārtojiet 2. līdz 4. darbību.</span><span class="sxs-lookup"><span data-stu-id="8ecce-137">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="8ecce-138">Lietotāja pārvaldnieka konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="8ecce-138">Configure the user's manager</span></span>

1. <span data-ttu-id="8ecce-139">Atveriet sadaļu **Iestatījumi** > **Drošība** > **Lietotāji**.</span><span class="sxs-lookup"><span data-stu-id="8ecce-139">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="8ecce-140">Atlasiet lietotāju, kam piešķirat pārvaldnieku, un zonā **Organizācijas informācija** no saraksta atlasiet pārvaldnieku.</span><span class="sxs-lookup"><span data-stu-id="8ecce-140">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="8ecce-141">Atlasiet vienumu **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="8ecce-141">Select **Save**.</span></span>


