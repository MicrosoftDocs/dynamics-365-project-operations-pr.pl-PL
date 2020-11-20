---
title: Interpretacja stanu projektu
description: W tym temacie zamieszczono informacje statusie przypisanym do projektu w Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: bc5bc174518e46b32cf88ea7231bb2df10fde292
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127306"
---
# <a name="understand-project-status"></a><span data-ttu-id="297e0-103">Interpretacja stanu projektu</span><span class="sxs-lookup"><span data-stu-id="297e0-103">Understand project status</span></span>

<span data-ttu-id="297e0-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="297e0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="297e0-105">Sekcja **Stan** na stronie **Encja projektu** zawiera podsumowanie stanu środowiska projektu na podstawie kosztów i nakładu pracy.</span><span class="sxs-lookup"><span data-stu-id="297e0-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="297e0-106">Pola podsumowania stanu</span><span class="sxs-lookup"><span data-stu-id="297e0-106">Status summary fields</span></span>

- <span data-ttu-id="297e0-107">Pole **stan całkowitego projektu** jest polem edytowalnym, które zawiera ogólny stan projektu.</span><span class="sxs-lookup"><span data-stu-id="297e0-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="297e0-108">Pole to korzysta z kodowania kolorów, takiego jak kolor zielony, żółty i czerwony, aby wskazywać większe ryzyko.</span><span class="sxs-lookup"><span data-stu-id="297e0-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="297e0-109">Pole **Komentarze** umożliwia menedżerowi projektu wprowadzenie określonych komentarzy dotyczących stanu.</span><span class="sxs-lookup"><span data-stu-id="297e0-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="297e0-110">Pole **Stan zaktualizowany dnia** jest edytowalny.</span><span class="sxs-lookup"><span data-stu-id="297e0-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="297e0-111">Wartość w tym polu to znacznik czasowy wskazujący, że stan został ostatnio zaktualizowany.</span><span class="sxs-lookup"><span data-stu-id="297e0-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="297e0-112">Pola **Wydajność planowania** i **Wydajność kosztów** są ustawiane na podstawie siatki śledzenia.</span><span class="sxs-lookup"><span data-stu-id="297e0-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="297e0-113">Jeśli odchylenie względem harmonogramu i kosztu dla węzła głównego w widoku **śledzenia nakładu** pracy jest dodatnie, te pola są zaktualizowane na **Wyprzedza**.</span><span class="sxs-lookup"><span data-stu-id="297e0-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="297e0-114">Kiedy Odchylenie względem harmonogramu i kosztu dla węzła głównego są ujemne,te pola otrzymają wartość **Opóźnienie**.</span><span class="sxs-lookup"><span data-stu-id="297e0-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>
