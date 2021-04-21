---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 29.5, poprawka, wer. 3
description: W tym temacie wymieniono funkcje i poprawki, które są dostępne w aktualizacji Project Service Automation, wydanie 29.5, poprawka wersja 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/26/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 99ba353236ad88b8bdff2c1b25e1247fa4bf3455
ms.sourcegitcommit: 9ebf7dd501898053bfa824f732adabf3f273613b
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/26/2021
ms.locfileid: "5715695"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-295-v3"></a><span data-ttu-id="d9982-103">Nowości i zmiany w aplikacji Project Service Automation, wydanie 29.5, wer. 3</span><span class="sxs-lookup"><span data-stu-id="d9982-103">What's new or changed in Project Service Automation Update Release 29.5, V3</span></span>

<span data-ttu-id="d9982-104">Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d9982-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="d9982-105">To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności.</span><span class="sxs-lookup"><span data-stu-id="d9982-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="d9982-106">To wydanie jest zgodne z systemem Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="d9982-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d9982-107">Aby zaktualizować do tej wersji, odwiedź centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację.</span><span class="sxs-lookup"><span data-stu-id="d9982-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="d9982-108">By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="d9982-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="d9982-109">W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wer. 3, aktualizacja 29.5.</span><span class="sxs-lookup"><span data-stu-id="d9982-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.5.</span></span> <span data-ttu-id="d9982-110">Numer tej kompilacji to V3.10.47.150 i jest on zazwyczaj dostępny za pośrednictwem samoaktualizacji w styczniu 2021 r.</span><span class="sxs-lookup"><span data-stu-id="d9982-110">This version has a build number of V3.10.47.150 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-295"></a><span data-ttu-id="d9982-111">Wydanie 29.5</span><span class="sxs-lookup"><span data-stu-id="d9982-111">Update Release 29.5</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="d9982-112">Poprawki błędów</span><span class="sxs-lookup"><span data-stu-id="d9982-112">Bug fixes</span></span>


<span data-ttu-id="d9982-113">**Sprzedaż**</span><span class="sxs-lookup"><span data-stu-id="d9982-113">**Sales**</span></span>

<span data-ttu-id="d9982-114">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="d9982-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="d9982-115">W przypadku zamknięcia oferty jako wygranej i bez cennika w encji **ContractLineMapHelper.UpdateContractLineDetailPriceListReference** pojawia się możliwy zerowy wyjątek odwołania.</span><span class="sxs-lookup"><span data-stu-id="d9982-115">A possible null reference exception occurs in **ContractLineMapHelper.UpdateContractLineDetailPriceListReference** when you close a quote as won and the quote has no price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
