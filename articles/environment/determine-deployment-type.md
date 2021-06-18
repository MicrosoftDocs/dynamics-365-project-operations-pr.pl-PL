---
title: Określenie typu wdrażania
description: W tym temacie zamieszczono informacje pozwalające wybrać odpowiedni typ wdrożenia Project Operations dla Twojej firmy.
author: stsporen
ms.date: 03/15/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ad700a84edd6c39609bc5b4f09ca74af3059a0dd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997119"
---
# <a name="determine-your-deployment-type"></a>Określenie typu wdrażania

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

> [!IMPORTANT]
> Po zakupie licencji należy rozpocząć tutaj, aby określić najlepszy model wdrażania rozwiązania Dynamics 365 Project Operations przy użyciu [przepływu instalacji z przewodnikiem](https://aka.ms/provisionprojectoperations).
> Po zakończeniu przepływu instalacji nadzorowanej, aby ją zakończyć, nastąpi przekierowanie do odpowiedniego portalu zarządzania. Więcej informacji na ten temat można znaleźć w części dotyczącej wdrożenia programu.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Istniejący klienci systemu Dynamics — korzystając z Dynamics 365 Project Service Automation
Project Operations obejmuje funkcje dostarczone z automatyzacją usługi Project Service Automation. Ścieżka aktualizacji zostanie wydana dla tych klientów w pierwszej fazie wydania 2021.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Obecni klienci Dynamics 365 Finance korzystający z programu Project Management and Accounting 

Obecni klienci Finance, którzy używają funkcji zarządzania projektami i księgowości, mogą nadal korzystać z niej w obecnej postaci. Zobacz [Project Operations — scenariusze obejmujące magazynowanie / zlecenia produkcyjne](#pma).


## <a name="deployment-regions"></a>Regiony wdrażania
Aby określić, które regiony obsługują wdrażanie rozwiązania Project Operations, zobacz [Dostępność geograficzna systemu Dynamics 365 i raport Power Platform](https://dynamics.microsoft.com/en-us/geographic-availability/). Wybierz pozycję **Wyświetl raport** i rozwiń pozycję **Dynamics 365 > Aplikacje operacji > Dynamics 365 Project Operations**, aby wyświetlić obsługiwane regiony.

## <a name="deployment-types"></a>Typy wdrożenia
Project Operations obsługuje wiele opcji wdrażania spełniających wymagania użytkownika. Niezależnie od tego, czy jesteś nowym, czy istniejącym klientem Dynamics 365, Project Operations pomoże Ci w Twojej pracy.

Nasz [kwestionariusz wdrażania](https://aka.ms/provisionprojectoperations) pomoże Ci w określeniu odpowiednich wdrożeń. Wyniki pozwolą CI wybrać jeden z następujących typów wdrożeń:

- [Wdrożenie uproszczone — od okazji do faktury pro forma](#lite)
- [Project Operations — zasoby / scenariusze nieobejmujące magazynowania](#integrated)
- [Project Operations — scenariusze obejmujące magazynowanie / zlecenia produkcyjne](#pma)

Project Operations obsługuje scenariusze dotyczące zleceń magazynowania / zlecenia produkcyjnego i scenariusze oparte na zasobach / zasobach niemagazynowanych w tym samym środowisku za pośrednictwem konfiguracji na poziomie firmy. Na przykład firma Contoso może korzystać z możliwości magazynowania / zleceń produkcyjnych w swoim zakładzie produkcyjnym w USA (firma = Contoso Manufacturing United States). Firma Contoso może używać niedostępnych / opartych na zasobach możliwości w swoim ośrodku serwisowym Contoso Robotics Arms w Wielkiej Brytanii (firma = Contoso Robotics w Wielkiej Brytanii).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Wdrażanie w wersji uproszczonej — od okazji do faktury pro forma

We wdrożeniu uproszczonym dostępne są następujące możliwości:

- Proces sprzedaży dla projektów, który rozszerza środowisko aplikacji Dynamics 365 Sales
- Planowanie projektów przy użyciu programu Microsoft Project dla sieci Web
- Wielowymiarowe ceny
- Zunifikowane zarządzanie zasobami
- Śledzenie czasu
- Podstawowe wydatki
- Wystawianie faktury Proforma za przegląd i edycję kierownika projektu 

#### <a name="deployment-steps"></a>Kroki wdrażania
Wyznaczanie najlepszego modelu wdrażania Project Operations przy użyciu [kwestionariusza rozmieszczenia](https://aka.ms/provisionprojectoperations).

W tym wdrożeniu zobacz [Tworzenie konta dla subskrypcji w wersji zapoznawczej](lite-preview-subscription-sign-up.md) i [Ustanowienie nowego środowiska](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations — zasoby / scenariusze nieobejmujące magazynowania
Project Operations dotyczące scenariuszy zasobów i zasobów niemagazynowanych oferują następujące możliwości:
 
- Proces sprzedaży dla projektów, który rozszerza aplikację Dynamics 365 Sales
- Planowanie projektów przy użyciu programu Microsoft Project dla sieci Web
- Wielowymiarowe ceny
- Zunifikowane zarządzanie zasobami
- Śledzenie czasu
- Podstawowe wydatki
- Wydatek pełny
- OCR paragonów
- Proforma i fakturowanie dla klientów 
- Rozpoznawanie przychodów dla projektów

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
- Obsługa materiałów magazynowych przy użyciu zapasów

#### <a name="deployment-steps"></a>Kroki wdrażania
Wyznaczanie najlepszego modelu wdrażania Project Operations przy użyciu [kwestionariusza rozmieszczenia](https://aka.ms/provisionprojectoperations).

W tym wdrożeniu zobacz [Tworzenie konta dla subskrypcji w wersji zapoznawczej](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) i [Ustanowienie nowego środowiska](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json). 



[!INCLUDE[footer-include](../includes/footer-banner.md)]