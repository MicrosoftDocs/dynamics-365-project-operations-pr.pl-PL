---
title: Określenie typu wdrażania
description: W tym temacie zamieszczono informacje pozwalające wybrać odpowiedni typ wdrożenia Project Operations dla Twojej firmy.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082016"
---
# <a name="determine-your-deployment-type"></a>Określenie typu wdrażania

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

> [!IMPORTANT]
> Po zakupieniu licencji, zacznij tutaj, aby określić najlepszy model wdrażania Dynamics 365 Project Operations przy użyciu [Przepływu instalacji nadzorowanej](https://aka.ms/provisionprojectoperations).
> Po zakończeniu przepływu instalacji nadzorowanej, aby ją zakończyć, nastąpi przekierowanie do odpowiedniego portalu zarządzania. Więcej informacji na ten temat można znaleźć w części dotyczącej wdrożenia programu.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Istniejący klienci systemu Dynamics — korzystając z Dynamics 365 Project Service Automation
Project Operations obejmuje funkcje dostarczone z automatyzacją usługi Project Service Automation. W przyszłości dla tych klientów zostanie wydana ścieżka uaktualniania.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Obecni klienci Dynamics 365 Finance korzystający z programu Project Management and Accounting 

Istniejący użytkownicy Finance, którzy korzystają z Project Management and Accounting mogą dalej korzystać z programu w taki sam sposób, jak dotychczas. Zobacz [Project Operations — scenariusze obejmujące magazynowanie / zlecenia produkcyjne](#pma).


## <a name="deployment-types"></a>Typy wdrożenia
Project Operations obsługuje wiele opcji wdrażania spełniających wymagania użytkownika. Niezależnie od tego, czy jesteś nowym, czy istniejącym klientem Dynamics 365, Project Operations pomoże Ci w Twojej pracy.

Nasz [kwestionariusz wdrażania](https://aka.ms/provisionprojectoperations) pomoże Ci w określeniu odpowiednich wdrożeń. Wyniki pozwolą CI wybrać jeden z następujących typów wdrożeń:

- [Wdrożenie uproszczone — od okazji do faktury pro forma](#lite)
- [Project Operations — zasoby / scenariusze nieobejmujące magazynowania](#integrated)
- [Project Operations — scenariusze obejmujące magazynowanie / zlecenia produkcyjne](#pma)

Project Operations obsługuje scenariusze dotyczące zleceń magazynowania / zlecenia produkcyjnego i scenariusze oparte na zasobach / zasobach niemagazynowanych w tym samym środowisku za pośrednictwem konfiguracji na poziomie firmy. Firma Contoso może na przykład użyć funkcji zarządzania stanami magazynowymi/zleceniami produkcyjnymi swojej placówki w Stanach Zjednoczonych (osoba prawna = Contoso Manufacturing United States). Firma Contoso może użyć funkcji zarządzania stanami magazynowymi/zleceniami produkcyjnymi swojej placówki w Wielkiej Brytanii (osoba prawna = Contoso Robotics United Kingdom).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Wdrożenie uproszczone — od okazji do faktury pro forma

We wdrożeniu uproszczonym dostępne są następujące możliwości:

- Planowanie projektów przy użyciu programu Microsoft Project dla sieci Web
- Wielowymiarowe ceny
- Zunifikowane zarządzanie zasobami
- Śledzenie czasu
- Podstawowe wydatki
- Propozycja faktury

#### <a name="deployment-steps"></a>Kroki wdrażania
Wyznaczanie najlepszego modelu wdrażania Project Operations przy użyciu [kwestionariusza rozmieszczenia](https://aka.ms/provisionprojectoperations).

W tym wdrożeniu zobacz [Tworzenie konta dla subskrypcji w wersji zapoznawczej](lite-preview-subscription-sign-up.md) i [Ustanowienie nowego środowiska](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations — zasoby / scenariusze nieobejmujące magazynowania
Project Operations dotyczące scenariuszy zasobów i zasobów niemagazynowanych oferują następujące możliwości:
  
- Planowanie projektów przy użyciu programu Microsoft Project dla sieci Web
- Wielowymiarowe ceny
- Zunifikowane zarządzanie zasobami
- Śledzenie czasu
- Podstawowe wydatki
- Wydatek pełny
- OCR paragonów
- Pełne fakturowanie
- Ujmowanie przychodów

#### <a name="deployment-steps"></a>Kroki wdrażania
Wyznaczanie najlepszego modelu wdrażania Project Operations przy użyciu [kwestionariusza rozmieszczenia](https://aka.ms/provisionprojectoperations).

W tym wdrożeniu zobacz [Tworzenie konta dla subskrypcji w wersji zapoznawczej](resource-sign-up-preview-subscription.md) i [Ustanowienie nowego środowiska](resource-provision-new-environment.md). 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations — scenariusze obejmujące magazynowanie / zlecenia produkcyjne

- Planowanie projektu za pomocą WBS
- Zarządzanie zasobami
- Śledzenie czasu
- Wydatek pełny
- OCR paragonów
- Pełne fakturowanie
- Ujmowanie przychodów
- Zlecenia produkcyjne
- Obsługa materiałów

#### <a name="deployment-steps"></a>Kroki wdrażania
Wyznaczanie najlepszego modelu wdrażania Project Operations przy użyciu [kwestionariusza rozmieszczenia](https://aka.ms/provisionprojectoperations).

W tym wdrożeniu zobacz [Tworzenie konta dla subskrypcji w wersji zapoznawczej](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) i [Ustanowienie nowego środowiska](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json). 

