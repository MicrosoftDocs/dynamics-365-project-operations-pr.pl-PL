---
title: Wdrożenie aplikacji Project Operations — wersja uproszczona
description: W tym artykule podano informacje o tym, jak zainstalować uproszczone wdrożenie aplikacji Project Operations — od okazji do faktury pro forma.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 86293b725e86db3d4b8bdaf5810b16b7c670e8a3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930331"
---
# <a name="deploy-project-operations---lite"></a>Wdrożenie aplikacji Project Operations — wersja uproszczona

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_



Project Operations obsługuje wiele modeli wdrożeń. Aby wybrać najlepszy model wdrażania, zobacz artykuł [typy wdrożeń](determine-deployment-type.md).


> [!IMPORTANT]
> To wdrożenie polega na wdrożeniu w wersji uproszczonej — oferta do faktury proforma, co powoduje jednoczesne wdrożenie **Project Operations tylko w Dataverse**.

- [Wdrażanie usługi Project Operations w nowym środowisku usługi Dataverse](#new)
- [Instalacja programu w istniejącym Dataverse](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a>Wdrażanie usługi Project Operations w nowym środowisku usługi Dataverse

1. Jako [administrator globalny lub administrator Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) z licencją Project Operations utwórz nowe Dataverse w [centrum administracyjnym PowerPlatform](https://admin.powerplatform.com). Upewnij się, że włączono funkcję **Tworzenie bazy danych dla tego** środowiska i **aplikacji usługi Dynamics 365**. Aby uzyskać więcej informacji zobacz [Tworzenie środowisk i zarządzanie nimi w centrum administracyjnym usługi Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Wybierz pozycję **Microsoft Dynamics 365 Project Operations** z listy wdrożeń aplikacji Dynamics 365.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a>Wdrażanie usługi Project Operations w istniejącym środowisku usługi Dataverse
1. Upewnij się, że środowisko nie zostało skonfigurowane z [dwoma zapisami](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), ponieważ instalacja spowoduje zainstalowanie [Project Operations dla funkcji scenariuszy opartych na zasobach/brakach magazynowych](project-operations-integrated-deployment-overview.md).
2. Jako [administrator globalny lub administrator Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) z licencją Project Operations znajdź środowisko w [centrum administracyjnym PowerPlatform](https://admin.powerplatform.com), w którym chcesz zainstalować Project Operations.
3. Zainstaluj aplikację **Microsoft Dynamics 365 Project Operations** z listy wdrożeń aplikacji Dynamics 365. Aby uzyskać więcej informacji, zobacz temat [Zarządzanie aplikacjami Dynamics 365](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
