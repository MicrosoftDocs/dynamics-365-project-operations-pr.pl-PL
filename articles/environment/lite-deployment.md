---
title: Wdrożenie aplikacji Project Operations — wersja uproszczona
description: W tym temacie zamieszczono informacje dotyczące sposobu instalowania programu Project Operations lite deployment — od oferty do faktury pro forma.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2470d573f4537cb22de4dbd98caff148cbe0bda3
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950277"
---
# <a name="deploy-project-operations---lite"></a><span data-ttu-id="4ae80-103">Wdrożenie aplikacji Project Operations — wersja uproszczona</span><span class="sxs-lookup"><span data-stu-id="4ae80-103">Deploy Project Operations - lite</span></span>

<span data-ttu-id="4ae80-104">_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_</span><span class="sxs-lookup"><span data-stu-id="4ae80-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="4ae80-105">Project Operations obsługuje wiele modeli wdrożeń.</span><span class="sxs-lookup"><span data-stu-id="4ae80-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="4ae80-106">Aby wybrać najlepszy model wdrażania, zobacz artykuł [typy wdrożeń](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="4ae80-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="4ae80-107">To wdrożenie polega na wdrożeniu w wersji uproszczonej — oferta do faktury proforma, co powoduje jednoczesne wdrożenie **Project Operations tylko w Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="4ae80-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="4ae80-108">Wdrażanie usługi Project Operations w nowym środowisku usługi CDS</span><span class="sxs-lookup"><span data-stu-id="4ae80-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="4ae80-109">Instalacja programu w istniejącym CDS</span><span class="sxs-lookup"><span data-stu-id="4ae80-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="4ae80-110">Wdrażanie usługi Project Operations w nowym środowisku usługi CDS</span><span class="sxs-lookup"><span data-stu-id="4ae80-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="4ae80-111">Jako [administrator globalny lub administrator Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) z licencją Project Operations utwórz nowe CDS w [centrum administracyjnym PowerPlatform](https://admin.powerplatform.com).</span><span class="sxs-lookup"><span data-stu-id="4ae80-111">As the [Global or Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="4ae80-112">Upewnij się, że **Baza danych** oraz **Aplikacje Dynamics 365** są włączone.</span><span class="sxs-lookup"><span data-stu-id="4ae80-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="4ae80-113">Aby uzyskać więcej informacji zobacz [Tworzenie środowisk i zarządzanie nimi w centrum administracyjnym usługi Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="4ae80-113">For more information, see [Create and manage environments in the Power Platform admin center](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="4ae80-114">Wybierz pozycję **Microsoft Dynamics 365 Project Operations** z listy wdrożeń aplikacji Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="4ae80-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="4ae80-115">Wdrażanie usługi Project Operations w istniejącym środowisku usługi CDS</span><span class="sxs-lookup"><span data-stu-id="4ae80-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="4ae80-116">Jako [administrator globalny lub administrator Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) z licencją Project Operations znajdź środowisko w [centrum administracyjnym PowerPlatform](https://admin.powerplatform.com), w którym chcesz zainstalować Project Operations.</span><span class="sxs-lookup"><span data-stu-id="4ae80-116">As the [Global or Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="4ae80-117">Zainstaluj aplikację **Microsoft Dynamics 365 Project Operations** z listy wdrożeń aplikacji Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="4ae80-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="4ae80-118">Aby uzyskać więcej informacji, zobacz temat [Zarządzanie aplikacjami Dynamics 365](/power-platform/admin/manage-apps).</span><span class="sxs-lookup"><span data-stu-id="4ae80-118">For more information, see [Manage Dynamics 365 apps](/power-platform/admin/manage-apps).</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]