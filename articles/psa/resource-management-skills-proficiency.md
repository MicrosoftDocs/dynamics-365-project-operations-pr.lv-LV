---
title: Prasmes un kvalifikācijas modeļi
description: Šajā tēmā ir sniegta informācija par to, kā izmantot prasmes un kvalifikācijas modeļus.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: cd243544df062e5801bbfa0a3bd75c4d9a116a6f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080664"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="08013-103">Prasmes un kvalifikācijas modeļi</span><span class="sxs-lookup"><span data-stu-id="08013-103">Skills and proficiency models</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="08013-104">Prasmes ir resursu īpašības, kas tiek kopīgotas programmā Dynamics 365 Project Service Automation un attiecīgajos gadījumos programmā Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="08013-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="08013-105">Lai uzturētu prasmju krātuvi programmā Project Service Automation, atveriet sadaļu **Resursi** \> **Resursu prasmes**.</span><span class="sxs-lookup"><span data-stu-id="08013-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![Resursu prasmes](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="08013-107">Kvalifikācijas modeļu izmantošana, lai vērtētu resursus</span><span class="sxs-lookup"><span data-stu-id="08013-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="08013-108">Resursu prasmes vērtē atbilstoši kvalifikācijas modeļiem.</span><span class="sxs-lookup"><span data-stu-id="08013-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="08013-109">Atsevišķi vērtējumi ir iekļauti kvalifikācijas modelī.</span><span class="sxs-lookup"><span data-stu-id="08013-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="08013-110">Lai izveidotu kvalifikācijas modeli, atveriet sadaļu **Resurss** \> **Kvalifikācijas modeļi** un pēc tam atlasiet vienumu **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="08013-110">To create a proficiency model, go to **Resources** \> **Proficiency Models** , and then select **New**.</span></span>
2. <span data-ttu-id="08013-111">Jaunajā vērtējuma modelī norādiet minimālo vērtējuma vērtību, maksimālo novērtējuma vērtību un novērtēto entītiju.</span><span class="sxs-lookup"><span data-stu-id="08013-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="08013-112">Apakšrežģī **Vērtējuma vērtības** var definēt dažādas vērtējuma vērtības no minimālās līdz maksimālajai.</span><span class="sxs-lookup"><span data-stu-id="08013-112">In the **Rating Values** sub-grid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![Definētie minimālie un maksimālie vērtējumi](media/Resource-Management-image85.png)

<span data-ttu-id="08013-114">Šīs vērtējuma vērtības tiek rādītas vienumu **Resursu prasības** , **Plānošanas panelis** un **Plānošanas palīgs** filtros.</span><span class="sxs-lookup"><span data-stu-id="08013-114">These rating values are shown on the **Resource Requirements** , **Schedule Board** , and **Schedule Assistant** filters.</span></span>
