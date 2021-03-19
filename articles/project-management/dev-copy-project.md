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
ms.openlocfilehash: 27847575e2d6ec9af77d24f756b13d3aeb0efea7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286936"
---
# <a name="develop-project-templates-with-copy-project"></a>Projektowanie szablonów projektów przy użyciu narzędzia kopiowania projektów

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Aplikacja Dynamics 365 Project Operations obsługuje kopiowanie projektów i przywracanie przypisań z powrotem do zasobów ogólnych reprezentujących rolę. Dzięki tej funkcji użytkownicy mogą tworzyć podstawowe szablony projektów.

Po wybraniu opcji **Kopiowania projektów** status projektu docelowego jest aktualizowany. Pole **Powód statusu** jest wykorzystywane do określenia, czy zadanie kopiowania jest zakończone. Wybranie opcji **Kopiowania projektu** powoduje zaktualizowanie daty rozpoczęcia projektu do bieżącej daty rozpoczęcia, jeśli nie zostanie wykryta data docelowa w encji projektu docelowego.

## <a name="copy-project-custom-action"></a>Niestandardowa akcja kopiowania projektu 

### <a name="name"></a>Nazwa/nazwisko 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Parametry wejściowe
Istnieją 3 parametry wejściowe:

| Parametr          | Pisz   | Wartości                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** lub **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Odwołanie do encji | Projekt źródłowy |
| Język docelowy             | Odwołanie do encji | Projekt docelowy |


- **{"clearTeamsAndAssignments":true}**: domyślne zachowanie projektu sieciowego, usunie wszystkie przypisania i członków zespołu.
- **{"removeNamedResources":true}** domyślne zachowanie Project Operations powoduje przywrócenie przydziałów do zasobów ogólnych.

Aby uzyskać więcej informacji na temat Akcji, zobacz [Korzystanie z akcji Web API](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Określ pola do skopiowania 
Po wywołaniu akcji **Kopiowanie projektu** zostanie wyświetlony widok projektu **Kopiuj kolumny projektu**, Aby określić, które pola zostaną skopiowane podczas kopiowania projektu.


### <a name="example"></a>Przykład
W poniższym przykładzie pokazano, jak wywołać akcję niestandardową **CopyProject** przy użyciu zestawu parametru **removeNamedResources**.
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