---
title: Projektowanie szablonów projektów przy użyciu narzędzia kopiowania projektów
description: W tym temacie zamieszczono informacje dotyczące sposobu tworzenia szablonów projektów przy użyciu niestandardowej akcji kopiowania projektów.
author: stsporen
manager: Annbe
ms.date: 01/21/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cc17df0c73b276048f7c4b04bd9dc6644e828dc0
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949827"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="05866-103">Projektowanie szablonów projektów przy użyciu narzędzia kopiowania projektów</span><span class="sxs-lookup"><span data-stu-id="05866-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="05866-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="05866-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="05866-105">Aplikacja Dynamics 365 Project Operations obsługuje kopiowanie projektów i przywracanie przypisań z powrotem do zasobów ogólnych reprezentujących rolę.</span><span class="sxs-lookup"><span data-stu-id="05866-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="05866-106">Dzięki tej funkcji użytkownicy mogą tworzyć podstawowe szablony projektów.</span><span class="sxs-lookup"><span data-stu-id="05866-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="05866-107">Po wybraniu opcji **Kopiowania projektów** status projektu docelowego jest aktualizowany.</span><span class="sxs-lookup"><span data-stu-id="05866-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="05866-108">Pole **Powód statusu** jest wykorzystywane do określenia, czy zadanie kopiowania jest zakończone.</span><span class="sxs-lookup"><span data-stu-id="05866-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="05866-109">Wybranie opcji **Kopiowania projektu** powoduje zaktualizowanie daty rozpoczęcia projektu do bieżącej daty rozpoczęcia, jeśli nie zostanie wykryta data docelowa w encji projektu docelowego.</span><span class="sxs-lookup"><span data-stu-id="05866-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="05866-110">Niestandardowa akcja kopiowania projektu</span><span class="sxs-lookup"><span data-stu-id="05866-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="05866-111">Nazwa/nazwisko</span><span class="sxs-lookup"><span data-stu-id="05866-111">Name</span></span> 

<span data-ttu-id="05866-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="05866-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="05866-113">Parametry wejściowe</span><span class="sxs-lookup"><span data-stu-id="05866-113">Input parameters</span></span>
<span data-ttu-id="05866-114">Istnieją 3 parametry wejściowe:</span><span class="sxs-lookup"><span data-stu-id="05866-114">There are three input parameters:</span></span>

| <span data-ttu-id="05866-115">Parametr</span><span class="sxs-lookup"><span data-stu-id="05866-115">Parameter</span></span>          | <span data-ttu-id="05866-116">Pisz</span><span class="sxs-lookup"><span data-stu-id="05866-116">Type</span></span>   | <span data-ttu-id="05866-117">Wartości</span><span class="sxs-lookup"><span data-stu-id="05866-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="05866-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="05866-118">ProjectCopyOption</span></span>  | <span data-ttu-id="05866-119">String</span><span class="sxs-lookup"><span data-stu-id="05866-119">String</span></span> | <span data-ttu-id="05866-120">**{"removeNamedResources":true}** lub **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="05866-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="05866-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="05866-121">SourceProject</span></span>      | <span data-ttu-id="05866-122">Odwołanie do encji</span><span class="sxs-lookup"><span data-stu-id="05866-122">Entity Reference</span></span> | <span data-ttu-id="05866-123">Projekt źródłowy</span><span class="sxs-lookup"><span data-stu-id="05866-123">Source Project</span></span> |
| <span data-ttu-id="05866-124">Język docelowy</span><span class="sxs-lookup"><span data-stu-id="05866-124">Target</span></span>             | <span data-ttu-id="05866-125">Odwołanie do encji</span><span class="sxs-lookup"><span data-stu-id="05866-125">Entity Reference</span></span> | <span data-ttu-id="05866-126">Projekt docelowy</span><span class="sxs-lookup"><span data-stu-id="05866-126">Target Project</span></span> |


- <span data-ttu-id="05866-127">**{"clearTeamsAndAssignments":true}**: domyślne zachowanie projektu sieciowego, usunie wszystkie przypisania i członków zespołu.</span><span class="sxs-lookup"><span data-stu-id="05866-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="05866-128">**{"removeNamedResources":true}** domyślne zachowanie Project Operations powoduje przywrócenie przydziałów do zasobów ogólnych.</span><span class="sxs-lookup"><span data-stu-id="05866-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="05866-129">Aby uzyskać więcej informacji na temat Akcji, zobacz [Korzystanie z akcji Web API](/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="05866-129">For more defaults on actions, see [Use Web API actions](/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="05866-130">Określ pola do skopiowania</span><span class="sxs-lookup"><span data-stu-id="05866-130">Specify fields to copy</span></span> 
<span data-ttu-id="05866-131">Po wywołaniu akcji **Kopiowanie projektu** zostanie wyświetlony widok projektu **Kopiuj kolumny projektu**, Aby określić, które pola zostaną skopiowane podczas kopiowania projektu.</span><span class="sxs-lookup"><span data-stu-id="05866-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>


### <a name="example"></a><span data-ttu-id="05866-132">Przykład</span><span class="sxs-lookup"><span data-stu-id="05866-132">Example</span></span>
<span data-ttu-id="05866-133">W poniższym przykładzie pokazano, jak wywołać akcję niestandardową **CopyProject** przy użyciu zestawu parametru **removeNamedResources**.</span><span class="sxs-lookup"><span data-stu-id="05866-133">The following example shows how to call the **CopyProject** custom action with the **removeNamedResources** parameter set.</span></span>
```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    [DataContract]
    public class ProjectCopyOption
    {
        /// <summary>
        /// Clear teams and assignments.
        /// </summary>
        [DataMember(Name = "clearTeamsAndAssignments")]
        public bool ClearTeamsAndAssignments { get; set; }

        /// <summary>
        /// Replace named resource with generic resource.
        /// </summary>
        [DataMember(Name = "removeNamedResources")]
        public bool ReplaceNamedResources { get; set; }
    }

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project";
            targetProject.Id = organizationService.Create(targetProject);

            ProjectCopyOption copyOption = new ProjectCopyOption();
            copyOption.ReplaceNamedResources = true;

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, ProjectCopyOption projectCopyOption)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV2");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;
            req["ProjectCopyOption"] = JsonConvert.SerializeObject(projectCopyOption);
            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```


[!INCLUDE[footer-include](../includes/footer-banner.md)]