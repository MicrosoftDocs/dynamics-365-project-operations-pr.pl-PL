---
title: Kalendarz wpisów czasu
description: W tym temacie zamieszczono informacje dotyczące używania kalendarza wpisów czasu.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0188258a7d3c0e1644ae6db051995e6e02bcbf58
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282121"
---
# <a name="time-entry-calendar"></a><span data-ttu-id="381aa-103">Kalendarz wpisów czasu</span><span class="sxs-lookup"><span data-stu-id="381aa-103">Time entry calendar</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="381aa-104">Na stronie **Wpisy czasu** można przeglądać wpisy czasu istniejące w kalendarzu, wybierając kolejno opcje **Zapisz jako** \> **Formant kalendarza**.</span><span class="sxs-lookup"><span data-stu-id="381aa-104">On the **Time Entries** page, you can view the time entries on the calendar by selecting **Show as** \> **Calendar Control**.</span></span>

## <a name="updated-calendar-control"></a><span data-ttu-id="381aa-105">Zaktualizowana kontrolka kalendarza</span><span class="sxs-lookup"><span data-stu-id="381aa-105">Updated calendar control</span></span>

<span data-ttu-id="381aa-106">Program Dynamics 365 Project Service Automation oferuje nowy, rozszerzalny mechanizm obsługi wpisów czasu.</span><span class="sxs-lookup"><span data-stu-id="381aa-106">Dynamics 365 Project Service Automation offers a new and extensible time entry experience.</span></span> <span data-ttu-id="381aa-107">Ten nowy mechanizm zastępuje kontrolkę kalendarza niestandardowego, która była używana we wcześniejszych wersjach.</span><span class="sxs-lookup"><span data-stu-id="381aa-107">This new experience replaces the Custom Calendar Control that was used in earlier versions.</span></span> <span data-ttu-id="381aa-108">Można jednak nadal wyświetlać wpisy czasu za pośrednictwem kontrolki kalendarza tylko do odczytu, którą struktura ujednoliconego interfejsu udostępnia dla widoków dziennych, tygodniowych i miesięcznych.</span><span class="sxs-lookup"><span data-stu-id="381aa-108">However, you can still view time entries through a read-only calendar control that the Unified Interface Framework provides for daily, weekly, or monthly views.</span></span>

<span data-ttu-id="381aa-109">Kalendarz nie obsługuje akcji na poszczególnych elementach kalendarza i nie można zaznaczyć jednego lub więcej elementów kalendarza do przesłania lub usunięcia.</span><span class="sxs-lookup"><span data-stu-id="381aa-109">The calendar doesn't support actions on individual calendar items, and you can't select one or more calendar items for submission or deletion.</span></span> <span data-ttu-id="381aa-110">Zamiast tego należy zaznaczyć element kalendarza, aby otworzyć stronę encji **Wpis czasu**, gdzie można wykonać wymagane czynności.</span><span class="sxs-lookup"><span data-stu-id="381aa-110">Instead, select a calendar item to open the **Time Entry** entity page, where you can complete the required actions.</span></span>

## <a name="extensibility"></a><span data-ttu-id="381aa-111">Możliwości rozszerzania</span><span class="sxs-lookup"><span data-stu-id="381aa-111">Extensibility</span></span>

<span data-ttu-id="381aa-112">Na stronie **Wpisy czasu** zawierającej siatkę godzin można dodać pola niestandardowe, skonfigurować pola wyszukiwania i utworzyć widoki niestandardowe.</span><span class="sxs-lookup"><span data-stu-id="381aa-112">On the **Time Entries** page that has the time entry grid, you can add custom fields, set up lookup fields, and create custom views.</span></span> <span data-ttu-id="381aa-113">Istnieje również możliwość skonfigurowania niestandardowej logiki biznesowej, która jest oparta na wartościach wybranych lub wprowadzonych w polach niestandardowych.</span><span class="sxs-lookup"><span data-stu-id="381aa-113">You can also set up custom business logic that is based on the values that are selected or entered in custom fields.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]