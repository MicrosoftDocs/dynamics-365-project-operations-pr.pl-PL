---
title: Wdrożenie aplikacji Project Operations, wersja uproszczona
description: W tym artykule podano informacje o tym, jak zainstalować uproszczone wdrożenie aplikacji Project Operations — od okazji do faktury pro forma.
author: stsporen
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2c508f56b3018b6a86fea78bcf9ee4136e90f385
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/30/2022
ms.locfileid: "9810992"
---
# <a name="deploy-project-operations-lite"></a>Wdrożenie aplikacji Project Operations, wersja uproszczona

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_



Project Operations obsługuje wiele modeli wdrożeń. Aby wybrać najlepszy model wdrażania, zobacz artykuł [typy wdrożeń](determine-deployment-type.md).


> [!IMPORTANT]
> To wdrożenie polega na wdrożeniu w wersji uproszczonej — oferta do faktury proforma, co powoduje jednoczesne wdrożenie **Project Operations tylko w Dataverse**.

- [Wdrażanie usługi Project Operations w nowym środowisku usługi Dataverse](#new)
- [Instalacja programu w istniejącym Dataverse](#existing)
- [Instalacja w istniejącym środowisku Dataverse, w którym są zainstalowane składniki do podwójnego zapisu](#existingdw)



## <a name="install-project-operations-lite-to-a-new-dataverse-environment"></a><a name="new"></a>Wdrażanie usługi Project Operations w wersji uproszczonej w nowym środowisku usługi Dataverse

1. Jako [administrator globalny lub administrator Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) z licencją Project Operations utwórz nowe Dataverse w [centrum administracyjnym PowerPlatform](https://admin.powerplatform.com). Upewnij się, że włączono funkcję **Tworzenie bazy danych dla tego** środowiska i **aplikacji usługi Dynamics 365**. Aby uzyskać więcej informacji zobacz [Tworzenie środowisk i zarządzanie nimi w centrum administracyjnym usługi Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
1. Wybierz pozycję **Microsoft Dynamics 365 Project Operations** z listy wdrożeń aplikacji Dynamics 365.


## <a name="install-project-operations-lite-to-an-existing-dataverse-environment"></a><a name="existing"></a>Wdrażanie usługi Project Operations w wersji uproszczonej w istniejącym środowisku usługi Dataverse 
1. Jako [administrator globalny lub administrator Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) z licencją Project Operations znajdź środowisko w [centrum administracyjnym PowerPlatform](https://admin.powerplatform.com), w którym chcesz zainstalować Project Operations.
1. Zainstaluj aplikację **Microsoft Dynamics 365 Project Operations** z listy wdrożeń aplikacji Dynamics 365. Aby uzyskać więcej informacji, zobacz temat [Zarządzanie aplikacjami Dynamics 365](/power-platform/admin/manage-apps).

## <a name="install-project-operations-lite-to-an-existing-dataverse-environment-where-dual-write-solutions-are-already-present"></a><a name="existingdw"></a>Instalowanie Project Operations w wersji uproszczonej w istniejącym środowisku Dataverse, w którym są już dostępne rozwiązania do podwójnego zapisu

Aby kontynuować uruchamianie Project Operations w trybie wdrażania uproszczonego, należy wykonać następujące kroki:

1. Jako [administrator globalny lub administrator Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) z licencją Project Operations znajdź środowisko w [centrum administracyjnym PowerPlatform](https://admin.powerplatform.com), w którym chcesz zainstalować Project Operations.
1. Zainstaluj aplikację **Microsoft Dynamics 365 Project Operations** z listy wdrożeń aplikacji Dynamics 365. Aby uzyskać więcej informacji, zobacz temat [Zarządzanie aplikacjami Dynamics 365](/power-platform/admin/manage-apps).
1. Ponieważ w środowisku są dostępne składniki do podwójnego zapisu, które ułatwiają integrację z zainstalowanymi aplikacjami finansowymi i operacyjnymi, instalacja Project Operations obejmuje także funkcje i rozszerzenia wymagane do integrowania danych związanych z projektem z aplikacjami finansowymi i operacyjnymi. Ponieważ chcesz uruchomić Project Operations w uproszczonym wdrożeniu, te składniki integracji należy usunąć, ponieważ będą one tworzyły ograniczenia i sufit dla scenariuszy wdrażania uproszczonego. W celu ręcznego usunięcia rozwiązań **Podwójego zapisu Dynamics 365 Project Operations** i **Mapowań encji podwójnego zapisu Dynamics 365 Project Operations** w celu usunięcia tych komponentów.
1. Przejdź do **Project Operations -> Ustawienia -> Parametry**. Otwórz stronę szczegółów **Parametry projektu** i ustaw pole **Zachowanie uaktualniania rozwiązania** na **Tylko wersja uproszczona**. Dzięki temu żadne kolejne uaktualnienia Project Operations nie będą co jakiś czas wprowadzać składników integracji do Project Operations.  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
