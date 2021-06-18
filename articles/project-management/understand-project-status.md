---
title: Interpretacja stanu projektu
description: Ten temat zawiera informacje o stanie przypisania do projektów w rozwiązaniu Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ad8c012b93bc65595dca33df1770562916c557e0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993429"
---
# <a name="understand-project-status"></a><span data-ttu-id="159d4-103">Interpretacja stanu projektu</span><span class="sxs-lookup"><span data-stu-id="159d4-103">Understand project status</span></span>

<span data-ttu-id="159d4-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="159d4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="159d4-105">Sekcja **Stan** na stronie **Encja projektu** zawiera podsumowanie stanu środowiska projektu na podstawie kosztów i nakładu pracy.</span><span class="sxs-lookup"><span data-stu-id="159d4-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="159d4-106">Pola podsumowania stanu</span><span class="sxs-lookup"><span data-stu-id="159d4-106">Status summary fields</span></span>

- <span data-ttu-id="159d4-107">Pole **stan całkowitego projektu** jest polem edytowalnym, które zawiera ogólny stan projektu.</span><span class="sxs-lookup"><span data-stu-id="159d4-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="159d4-108">Pole to korzysta z kodowania kolorów, takiego jak kolor zielony, żółty i czerwony, aby wskazywać większe ryzyko.</span><span class="sxs-lookup"><span data-stu-id="159d4-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="159d4-109">Pole **Komentarze** umożliwia menedżerowi projektu wprowadzenie określonych komentarzy dotyczących stanu.</span><span class="sxs-lookup"><span data-stu-id="159d4-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="159d4-110">Pole **Stan zaktualizowany dnia** jest edytowalny.</span><span class="sxs-lookup"><span data-stu-id="159d4-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="159d4-111">Wartość w tym polu to znacznik czasowy wskazujący, że stan został ostatnio zaktualizowany.</span><span class="sxs-lookup"><span data-stu-id="159d4-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="159d4-112">Pola **Wydajność planowania** i **Wydajność kosztów** są ustawiane na podstawie siatki śledzenia.</span><span class="sxs-lookup"><span data-stu-id="159d4-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="159d4-113">Jeśli odchylenie względem harmonogramu i kosztu dla węzła głównego w widoku **śledzenia nakładu** pracy jest dodatnie, te pola są zaktualizowane na **Wyprzedza**.</span><span class="sxs-lookup"><span data-stu-id="159d4-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="159d4-114">Kiedy Odchylenie względem harmonogramu i kosztu dla węzła głównego są ujemne,te pola otrzymają wartość **Opóźnienie**.</span><span class="sxs-lookup"><span data-stu-id="159d4-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]