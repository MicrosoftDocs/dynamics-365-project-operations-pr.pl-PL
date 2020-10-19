---
title: Interpretacja stanu projektu
description: W tym temacie zamieszczono informacje statusie przypisanym do projektu w Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 336e479ad39653af14cca7930fe63e906b7de489
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965689"
---
# <a name="understand-project-status"></a><span data-ttu-id="03f95-103">Interpretacja stanu projektu</span><span class="sxs-lookup"><span data-stu-id="03f95-103">Understand project status</span></span>

<span data-ttu-id="03f95-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="03f95-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="03f95-105"> **Sekcja stan** na stronie **Encja projektu** zawiera podsumowanie stanu środowiska projektu na podstawie kosztów i nakładu pracy.</span><span class="sxs-lookup"><span data-stu-id="03f95-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="03f95-106">Pola podsumowania stanu</span><span class="sxs-lookup"><span data-stu-id="03f95-106">Status summary fields</span></span>

- <span data-ttu-id="03f95-107">Pole **Stan całkowitego projektu** jest polem edytowalnym, które zawiera ogólny stan projektu.</span><span class="sxs-lookup"><span data-stu-id="03f95-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="03f95-108">Pole to korzysta z kodowania kolorów, takiego jak kolor zielony, żółty i czerwony, aby wskazywać większe ryzyko.</span><span class="sxs-lookup"><span data-stu-id="03f95-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="03f95-109">Pole **Komentarze** umożliwia menedżerowi projektu wprowadzenie określonych komentarzy dotyczących stanu.</span><span class="sxs-lookup"><span data-stu-id="03f95-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="03f95-110">Wyświetlany w polu **Stan zaktualizowany** nie jest edytowalny.</span><span class="sxs-lookup"><span data-stu-id="03f95-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="03f95-111">Wartość w tym polu to znacznik czasowy wskazujący, że stan został ostatnio zaktualizowany.</span><span class="sxs-lookup"><span data-stu-id="03f95-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="03f95-112">Pola **Wydajność planowania** oraz **Wydajność kosztów** są ustawiane na podstawie siatki śledzenia.</span><span class="sxs-lookup"><span data-stu-id="03f95-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="03f95-113">Jeśli odchylenie względem harmonogramu i kosztu dla węzła głównego w widoku **śledzenia nakładu pracy** jest dodatnie, pola te zostaną zaktualizowane do **mieści się**.</span><span class="sxs-lookup"><span data-stu-id="03f95-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="03f95-114">Kiedy Odchylenie względem harmonogramu i kosztu dla węzła głównego są ujemne,te pola otrzymają wartość **nie mieści się**.</span><span class="sxs-lookup"><span data-stu-id="03f95-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>
