---
title: Projektowanie szablonów projektów przy użyciu narzędzia kopiowania projektów
description: W tym temacie zamieszczono informacje dotyczące sposobu tworzenia szablonów projektów przy użyciu niestandardowej akcji kopiowania projektów.
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 72aa2db7c717eeab85ada448c673bf702087baeb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590912"
---
# <a name="develop-project-templates-with-copy-project"></a>Projektowanie szablonów projektów przy użyciu narzędzia kopiowania projektów

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Aplikacja Dynamics 365 Project Operations obsługuje kopiowanie projektów i przywracanie przypisań z powrotem do zasobów ogólnych reprezentujących rolę. Dzięki tej funkcji użytkownicy mogą tworzyć podstawowe szablony projektów.

Po wybraniu opcji **Kopiowania projektów** status projektu docelowego jest aktualizowany. Pole **Powód statusu** jest wykorzystywane do określenia, czy zadanie kopiowania jest zakończone. Wybranie opcji **Kopiowania projektu** powoduje zaktualizowanie daty rozpoczęcia projektu do bieżącej daty rozpoczęcia, jeśli nie zostanie wykryta data docelowa w encji projektu docelowego.

## <a name="copy-project-custom-action"></a>Niestandardowa akcja kopiowania projektu

### <a name="name"></a>Imię i nazwisko/nazwa 

msdyn\_CopyProjectV3

### <a name="input-parameters"></a>Parametry wejściowe

Istnieją 3 parametry wejściowe:

- **ReplaceNamedResources** lub **ClearTeamsAndAssignments** — ustaw tylko jedną z opcji. Nie ustawiaj obu tych jednocześnie.

    - **\{"ReplaceNamedResources":true\}** — domyślne zachowanie Project Operations. Wszelkie nazwane zasoby są zastępowane zasobami ogólnymi.
    - **\{"ClearTeamsAndAssignments":true\}** — domyślne zachowanie Project for the Web. Wszystkie przypisania i członkowie zespołu są usuwane.

- **SourceProject** — odwołanie do encji projektu źródłowego, z który ma być skopiowany. Parametr dostawcy nie może mieć wartości null.
- **Miejsce docelowe** — Odwołanie do encji projektu docelowego do skopiowania. Parametr dostawcy nie może mieć wartości null.

Poniższa tabela zawiera podsumowanie trzech parametrów.

| Parametr                | Type             | Wartość                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | Wartość logiczna          | **True** lub **False** |
| ClearTeamsAndAssignments | Wartość logiczna          | **True** lub **False** |
| SourceProject            | Odwołanie do encji | Wybierz źródło    |
| Target                   | Odwołanie do encji | Wprowadź miejsce docelowe    |

Aby uzyskać więcej informacji na temat Akcji, zobacz [Korzystanie z akcji Web API](/powerapps/developer/common-data-service/webapi/use-web-api-actions).

### <a name="validations"></a>Walidacje

Przeprowadzane są następujące walidacje.

1. Sprawdzanie null i pobieranie projektów źródłowych i docelowych w celu potwierdzenia wsadu obu projektów w organizacji.
2. System sprawdza, czy projekt docelowy można skopiować, sprawdź następujące warunki:

    - W projekcie nie ma poprzedniego działania (w tym wybór **karty Zadania**) i projekt jest nowo tworzony.
    - Brak poprzedniej kopii, nie żądano importu dla tego projektu i projekt nie ma stanu **Niepowodzenie**.

3. Operacja nie jest wywoływana przy użyciu protokołu HTTP.

## <a name="specify-fields-to-copy"></a>Określ pola do skopiowania

Po wywołaniu akcji **Kopiowanie projektu** zostanie wyświetlony widok projektu **Kopiuj kolumny projektu**, Aby określić, które pola zostaną skopiowane podczas kopiowania projektu.

### <a name="example"></a>Przykład

W poniższym przykładzie pokazano, jak wywołać akcję niestandardową **CopyProjectV3** przy użyciu zestawu parametru **removeNamedResources**.

```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

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
            targetProject["msdyn_subject"] = "Example Project - Copy";
            targetProject.Id = organizationService.Create(targetProject);

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption, true, false);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, bool replaceNamedResources = true, bool clearTeamsAndAssignments = false)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV3");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;

            if (replaceNamedResources)
            {
                req["ReplaceNamedResources"] = true;
            }
            else
            {
                req["ClearTeamsAndAssignments"] = true;
            }

            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
