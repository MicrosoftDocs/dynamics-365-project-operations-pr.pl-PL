---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 29.5, poprawka, wer. 3
description: W tym temacie wymieniono funkcje i poprawki, które są dostępne w aktualizacji Project Service Automation, wydanie 29.5, poprawka wersja 3.
author: ruhercul
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
ms.openlocfilehash: d5050945c4ab7c1da61b07ec08bed20f32e166b9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999189"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-295-v3"></a><span data-ttu-id="e7044-103">Nowości i zmiany w aplikacji Project Service Automation, wydanie 29.5, wer. 3</span><span class="sxs-lookup"><span data-stu-id="e7044-103">What's new or changed in Project Service Automation Update Release 29.5, V3</span></span>

<span data-ttu-id="e7044-104">Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="e7044-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="e7044-105">To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności.</span><span class="sxs-lookup"><span data-stu-id="e7044-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="e7044-106">To wydanie jest zgodne z systemem Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="e7044-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e7044-107">Aby zaktualizować do tej wersji, odwiedź centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację.</span><span class="sxs-lookup"><span data-stu-id="e7044-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="e7044-108">By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution.md).</span><span class="sxs-lookup"><span data-stu-id="e7044-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution.md).</span></span>

<span data-ttu-id="e7044-109">W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wer. 3, aktualizacja 29.5.</span><span class="sxs-lookup"><span data-stu-id="e7044-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.5.</span></span> <span data-ttu-id="e7044-110">Numer tej kompilacji to V3.10.47.150 i jest on zazwyczaj dostępny za pośrednictwem samoaktualizacji w styczniu 2021 r.</span><span class="sxs-lookup"><span data-stu-id="e7044-110">This version has a build number of V3.10.47.150 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-295"></a><span data-ttu-id="e7044-111">Wydanie 29.5</span><span class="sxs-lookup"><span data-stu-id="e7044-111">Update Release 29.5</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="e7044-112">Poprawki błędów</span><span class="sxs-lookup"><span data-stu-id="e7044-112">Bug fixes</span></span>


<span data-ttu-id="e7044-113">**Sprzedaż**</span><span class="sxs-lookup"><span data-stu-id="e7044-113">**Sales**</span></span>

<span data-ttu-id="e7044-114">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="e7044-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="e7044-115">W przypadku zamknięcia oferty jako wygranej i bez cennika w encji **ContractLineMapHelper.UpdateContractLineDetailPriceListReference** pojawia się możliwy zerowy wyjątek odwołania.</span><span class="sxs-lookup"><span data-stu-id="e7044-115">A possible null reference exception occurs in **ContractLineMapHelper.UpdateContractLineDetailPriceListReference** when you close a quote as won and the quote has no price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
