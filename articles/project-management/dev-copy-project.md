---
title: Projektowanie szablonów projektów przy użyciu narzędzia kopiowania projektów
description: W tym temacie zamieszczono informacje dotyczące sposobu tworzenia szablonów projektów przy użyciu niestandardowej akcji kopiowania projektów.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 22976730ef3c8c22ea028b27a6eb5f14fb88993e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642421"
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
