---
title: Projekta veidnes izveide
description: Projekta veidnes izveide programmā Project Service
author: ruhercul
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
ms.openlocfilehash: 148bf1d42b640ff7b58b13bb0c30c7e583d803c8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997250"
---
# <a name="create-a-project-template-project-service"></a><span data-ttu-id="c85fb-103">Projekta veidnes izveide (Project Service)</span><span class="sxs-lookup"><span data-stu-id="c85fb-103">Create a project template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="c85fb-104">Projekta veidnes ietaupa jūsu laiku, ja jūsu uzņēmums regulāri iesniedz piedāvājumus līdzīga veida projektos.</span><span class="sxs-lookup"><span data-stu-id="c85fb-104">Project templates save you time if your company regularly bids on similar types of projects.</span></span> <span data-ttu-id="c85fb-105">Tie nodrošina standartu noteikumu kopumu un aplēsto stundu skaitu projekta tipam.</span><span class="sxs-lookup"><span data-stu-id="c85fb-105">They provide a standard set of roles and estimated hours for a type of project.</span></span> <span data-ttu-id="c85fb-106">Uzņēmumu vadītāji un projektu vadītāji var izveidot projektus, balstoties uz projekta veidni, vai nokopēt veidni un pārveidot to paši.</span><span class="sxs-lookup"><span data-stu-id="c85fb-106">Account managers and project managers can create projects based on a project template, or they can copy the template and make one of their own.</span></span>  
  
## <a name="components-of-project-template"></a><span data-ttu-id="c85fb-107">Projekta veidnes komponenti</span><span class="sxs-lookup"><span data-stu-id="c85fb-107">Components of project template</span></span>
 <span data-ttu-id="c85fb-108">Projekta veidne sastāv no trim komponentiem.</span><span class="sxs-lookup"><span data-stu-id="c85fb-108">A project template consists of three components:</span></span>  
  
- <span data-ttu-id="c85fb-109">**Darba sadalījuma struktūra**: darba sadalījuma struktūrai projekta veidnē ir tāds pats elementu kopums kā projektā.</span><span class="sxs-lookup"><span data-stu-id="c85fb-109">**Work breakdown structure**: A work breakdown structure in a project template has the same set of elements as in the project.</span></span> <span data-ttu-id="c85fb-110">Varat izveidot uzdevumu hierarhiju, piesaistīt lomas uzdevumam, noteikt plānošanas atribūtus, iestatīt atkarības un skatīt visus datus Ganta shēmā.</span><span class="sxs-lookup"><span data-stu-id="c85fb-110">You can create a task hierarchy, associate roles to task, define schedule attributes, set dependencies and view all the data in the Gantt.</span></span> <span data-ttu-id="c85fb-111">Darba sadalījuma struktūra projekta veidnēs atbalsta arī uzdevumu režīmus katram uzdevumam.</span><span class="sxs-lookup"><span data-stu-id="c85fb-111">The work breakdown structure in project templates also support task modes for each task.</span></span> <span data-ttu-id="c85fb-112">Nav nekādas atšķirības starp projekta veidni un projektu, veidojot darba grafiku.</span><span class="sxs-lookup"><span data-stu-id="c85fb-112">There is no difference between a project template and a project when creating work schedule.</span></span>  
  
- <span data-ttu-id="c85fb-113">**Projekta tāmes**: projekta tāmes veidnēs darbojas tāpat kā projektos, izņemot to, ka cenrāži noklusējuma izmaksu cenām un pārdošanas cenām vienmēr ir noklusējuma izmaksu cenu un pārdošanas cenu rāži, kas definēti [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parametros.</span><span class="sxs-lookup"><span data-stu-id="c85fb-113">**Project estimates**: Project estimates in templates work the same way as they do in projects, except the price lists for defaulting the cost and sales prices are always the default cost and sales price lists defined in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parameters.</span></span> <span data-ttu-id="c85fb-114">Pārējās funkcionalitātes ir tādas pašas kā projektā.</span><span class="sxs-lookup"><span data-stu-id="c85fb-114">The rest of the functionality is the same as in a project.</span></span>  
  
- <span data-ttu-id="c85fb-115">**Projekta darba grupas izveide**: kad veidojat projekta komandu projekta veidnei, nevarat rezervēt nosauktu resursu veidnē.</span><span class="sxs-lookup"><span data-stu-id="c85fb-115">**Project team formation**: When forming a project team for a project template, you can’t book a named resource in a template.</span></span> <span data-ttu-id="c85fb-116">Varat izmantot funkciju **Projekta darba grupas ģenerēšana** darba sadalījuma struktūrā, lai ģenerētu vispārējo resursu kopu.</span><span class="sxs-lookup"><span data-stu-id="c85fb-116">You can use **Generate Project Team** in the work breakdown structure to generate a set of generic resources.</span></span> <span data-ttu-id="c85fb-117">Varat norādīt arī vispārīgo resursu vajadzīgās prasmes un pieredzi.</span><span class="sxs-lookup"><span data-stu-id="c85fb-117">You can also specify required skills and proficiencies for generic resources.</span></span> <span data-ttu-id="c85fb-118">Projekta veidnēs nevarat aizstāt vispārīgu resursu ar rezervējamu resursu.</span><span class="sxs-lookup"><span data-stu-id="c85fb-118">You can’t substitute a generic resource with a bookable resource in project templates.</span></span>  
  
## <a name="create-a-project-from-a-template"></a><span data-ttu-id="c85fb-119">Projekta izveidošana no veidnes</span><span class="sxs-lookup"><span data-stu-id="c85fb-119">Create a project from a template</span></span>  
 <span data-ttu-id="c85fb-120">Projektu no veidnes var izveidot šādos veidos.</span><span class="sxs-lookup"><span data-stu-id="c85fb-120">You can create a project from a template in these following ways:</span></span>  
  
-   <span data-ttu-id="c85fb-121">Veidojot projektu no piedāvājuma, varat izvēlēties projekta veidni projekta ātrās izveides veidlapā.</span><span class="sxs-lookup"><span data-stu-id="c85fb-121">When creating a project from the quote, you can choose a project template in the project quick create form.</span></span>  
  
-   <span data-ttu-id="c85fb-122">Veidojot projektu, noklikšķinot uz **Jauns projekts**, tiek parādīta projekta veidlapa, pirms saglabājat ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c85fb-122">When creating a project by clicking **New Project**, the project form displays before you save the record.</span></span> <span data-ttu-id="c85fb-123">Šeit varat noklikšķināt uz lauka **Izvēlēties veidni**, lai izvēlētos no saraksta ar iepriekš definētām projekta veidnēm jūsu organizācijā.</span><span class="sxs-lookup"><span data-stu-id="c85fb-123">From here, you can click **Pick a template** field to choose from the list of pre-defined project templates in your organization.</span></span>  
  
-   <span data-ttu-id="c85fb-124">Noklikšķiniet uz **Izveidot projektu no veidnes** lapā **Projekta veidne**, lai izveidotu projektu no veidnes.</span><span class="sxs-lookup"><span data-stu-id="c85fb-124">Click **Create project from a template** on the **Project Template** page to create a project from the template.</span></span>  
  
## <a name="copying-components-of-a-template-to-a-project"></a><span data-ttu-id="c85fb-125">Veidnes komponentu kopēšana projektā</span><span class="sxs-lookup"><span data-stu-id="c85fb-125">Copying components of a template to a project</span></span>  
 <span data-ttu-id="c85fb-126">Kopējot veidnes komponentus projektu, jāņem vērā dažas lietas.</span><span class="sxs-lookup"><span data-stu-id="c85fb-126">When you copy components of a template into a project, there are a few things you should know about.</span></span>  
  
 <span data-ttu-id="c85fb-127">**Darba sadalījuma struktūras kopēšana**: kopējot darba sadalījuma struktūru no projekta veidnes, ja projektam ir cits projektu kalendārs nekā veidnei, uzdevumu grafikam tiks izmantotas darba stundas no projekta kalendāra.</span><span class="sxs-lookup"><span data-stu-id="c85fb-127">**Copying a work breakdown structure**: When you copy the work breakdown structure from a project template, if the project has a different project calendar than the template, the work hours from the project’s calendar will be applied to the schedule of tasks.</span></span> <span data-ttu-id="c85fb-128">Tā grafiks tiek pielāgots atbalstošajam projekta kalendāram.</span><span class="sxs-lookup"><span data-stu-id="c85fb-128">This adjusts the schedule to the backing project calendar.</span></span> <span data-ttu-id="c85fb-129">Līdzīgi arī pirmajam uzdevumam darba sadalījuma struktūrā tiek paņemts projekta sākuma datums, bet pārējais uzdevumu hierarhiju grafiks tiek atjaunināts, pamatojoties uz ilgumu un atkarībām, kas norādītas veidnes darba sadalījuma struktūrā.</span><span class="sxs-lookup"><span data-stu-id="c85fb-129">Similarly, the first task on the work breakdown structure takes the project’s start date, so the rest of the task hierarchy schedule is updated based on the duration and dependencies specified in the template’s work breakdown structure.</span></span>  
  
 <span data-ttu-id="c85fb-130">**Projekta tāmju kopēšana**: kopējot pa projekta tāmes rindiņām, cenrāži tiek atjaunoti, balstoties uz projekta atbildīgo vienību izmaksu cenrādim un uz klientu pārdošanas cenrādim.</span><span class="sxs-lookup"><span data-stu-id="c85fb-130">**Copying project estimates**: When you copy across project estimate lines, price lists are updated based on the owning unit of the project for the cost price list and customer for the sales price list.</span></span> <span data-ttu-id="c85fb-131">Vienības izmaksu un pārdošanas cenas nosaka no šiem cenrāžiem projektiem, kas saistīti ar pārdošanas vienību.</span><span class="sxs-lookup"><span data-stu-id="c85fb-131">The unit cost and sales prices are determined from these price lists on projects that are associated to a sales entity.</span></span>  
  
 <span data-ttu-id="c85fb-132">**Projekta darba grupas kopēšana**: kopējot projekta darba grupu no veidnes projektā, vispārīgie resursu tiek kopētas līdzi kopā ar veidnē noteiktajām prasmēm un pieredzi.</span><span class="sxs-lookup"><span data-stu-id="c85fb-132">**Copying a project team**: When you copy the project team from the template to a project, the generic resources are copied across, along with the skills and proficiencies defined in the template.</span></span> <span data-ttu-id="c85fb-133">Vispārīgo resursu piešķires arī tiek saglabātas kā projekta veidnē.</span><span class="sxs-lookup"><span data-stu-id="c85fb-133">Generic resource assignments are also maintained as in the project template.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="c85fb-134">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="c85fb-134">See Also</span></span>  
 [<span data-ttu-id="c85fb-135">Projekta vadītāja rokasgrāmata</span><span class="sxs-lookup"><span data-stu-id="c85fb-135">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]