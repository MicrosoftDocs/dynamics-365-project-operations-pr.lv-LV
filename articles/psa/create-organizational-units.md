---
title: Struktūrvienību izveide
description: Struktūrvienību izveide programmā Project Service
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: ebb00b9838773560404a9e3f7a19cc83408d7889
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125097"
---
# <a name="create-organizational-units-project-service"></a><span data-ttu-id="e0ffc-103">Struktūrvienību izveide (Project Service)</span><span class="sxs-lookup"><span data-stu-id="e0ffc-103">Create organizational units (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="e0ffc-104">Iespējams, ka jūsu uzņēmums organizē konsultāciju sniegšanas biznesu pēc ģeogrāfiskās atrašanās vietas, funkcijas vai citām jomām.</span><span class="sxs-lookup"><span data-stu-id="e0ffc-104">Your company probably organizes its consulting business by geography, function, or other areas.</span></span> <span data-ttu-id="e0ffc-105">Var izveidot struktūrvienības, kas atspoguļo konsultāciju sniegšanas biznesu.</span><span class="sxs-lookup"><span data-stu-id="e0ffc-105">You can create organizational units that reflect your consulting business.</span></span> <span data-ttu-id="e0ffc-106">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] struktūrvienība ir profesionālo pakalpojumu uzņēmuma grupa vai nodaļa, kas nodarbina apmaksājamus resursus ar izmaksu likmēm, kas atšķiras no citām šādām uzņēmuma grupām vai nodaļām.</span><span class="sxs-lookup"><span data-stu-id="e0ffc-106">A [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] organizational unit is a group or division in a professional services company that employs billable resources with cost rates that are distinct from other such groups or divisions in the company.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e0ffc-107">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] struktūrvienība ir nodalīta no biznesa vienības pakalpojumā [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="e0ffc-107">A [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] organizational unit is separate from a business unit in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span></span> <span data-ttu-id="e0ffc-108">Biznesa vienības vairāk atbilst drošības struktūrām, kas ietekmē piekļuves [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] informācijai līmeņus un kas parasti ir pakārotas uzņēmuma nodaļām, piemēram, mātes un meitas uzņēmumiem vai nodaļām.</span><span class="sxs-lookup"><span data-stu-id="e0ffc-108">Business units are more of a security structure that affects levels of access to [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] information, and are usually organized around company divisions, like parent company and subsidiaries or divisions.</span></span> <span data-ttu-id="e0ffc-109">Struktūrvienības norāda, pēc kādām kategorijām konsultāciju uzņēmumā tiek grupēti tā dažādie darījumi, vai nu pēc ģeogrāfiskās atrašanās vietas (piemēram, EMEA vai LATAM), pēc funkcijas (piemēram, produkta izstrādes vai IT ārpakalpojumiem), vai pēc citiem parametriem.</span><span class="sxs-lookup"><span data-stu-id="e0ffc-109">Organizational units represent how your consulting company categorizes its different businesses, whether by geographic location (like EMEA or LATAM), by function (like Product Development or IT Outsourcing), or by other parameters.</span></span>  
  
1.  <span data-ttu-id="e0ffc-110">Pārejiet uz sadaļu **Project Service > Struktūrvienības**.</span><span class="sxs-lookup"><span data-stu-id="e0ffc-110">Go to **Project Service > Organizational Units**.</span></span>  
  
2.  <span data-ttu-id="e0ffc-111">Noklikšķiniet uz **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="e0ffc-111">Click **New**.</span></span>  
  
3.  <span data-ttu-id="e0ffc-112">Zonā **Vispārīgi** ievadiet struktūrvienības nosaukumu laukā **Nosaukums** un atbilstoši aizpildiet pārējos laukus.</span><span class="sxs-lookup"><span data-stu-id="e0ffc-112">In the **General** area, enter a name for the organization unit in **Name**, and fill in the other fields as necessary.</span></span>  
  
4.  <span data-ttu-id="e0ffc-113">Noklikšķiniet uz **Saglabāt**, lai izveidotu ierakstu un pēc tam varētu veikt tā rediģēšanu.</span><span class="sxs-lookup"><span data-stu-id="e0ffc-113">Click **Save** to create the record so you can continue editing it.</span></span>  
  
5.  <span data-ttu-id="e0ffc-114">Sadaļā **Izmaksu cenrāži** noklikšķiniet uz **+**, lai pievienotu cenrādi.</span><span class="sxs-lookup"><span data-stu-id="e0ffc-114">Under **Cost Price Lists**, click **+** to add a price list.</span></span> <span data-ttu-id="e0ffc-115">Šajā vietā var pievienot tikai cenrāžus ar kontekstu **Cena**.</span><span class="sxs-lookup"><span data-stu-id="e0ffc-115">You can only add price lists with the **Cost** context here.</span></span>  
  
6.  <span data-ttu-id="e0ffc-116">Laukā **Nosaukums** noklikšķiniet uz pogas **Meklēt** un atlasiet cenrādi, kura pieejamību vēlaties iespējot šai struktūrvienībai.</span><span class="sxs-lookup"><span data-stu-id="e0ffc-116">In the **Name** field, click the **Search** button and select a price list you want to make available to this organizational unit.</span></span> <span data-ttu-id="e0ffc-117">Ja nepieciešams, turpiniet pievienot cenrāžus.</span><span class="sxs-lookup"><span data-stu-id="e0ffc-117">Continue adding price lists as needed.</span></span>  
  
7.  <span data-ttu-id="e0ffc-118">Kad esat pabeidzis, ekrāna apakšējā labajā stūrī noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="e0ffc-118">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="e0ffc-119">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="e0ffc-119">See Also</span></span>  
 [<span data-ttu-id="e0ffc-120">Project Service Automation konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="e0ffc-120">Configure Project Service Automation</span></span>](../psa/configure.md)
