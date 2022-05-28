---
title: Wdrożenie aplikacji Project Operations — wersja uproszczona
description: W tym temacie zamieszczono informacje dotyczące sposobu instalowania programu Project Operations lite deployment — od oferty do faktury pro forma.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: e33506504665f2e7ef7ad48469082f9f64a2a44b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580745"
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
