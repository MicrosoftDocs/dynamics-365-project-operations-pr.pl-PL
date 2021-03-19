---
title: Typy okresów
description: Ten temat zawiera informacje dotyczące sposobów konfigurowania typów okresów na potrzeby szacowania przychodów.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 107cecbc1dabdf13147d847bf1816f44cc2703c5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287296"
---
# <a name="period-types"></a><span data-ttu-id="6893a-103">Typy okresów</span><span class="sxs-lookup"><span data-stu-id="6893a-103">Period types</span></span>

<span data-ttu-id="6893a-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="6893a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6893a-105">Typ okresu określa, jak często szacowany jest przychód w projekcie.</span><span class="sxs-lookup"><span data-stu-id="6893a-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="6893a-106">Ten temat zawiera informacje dotyczące sposobów konfigurowania typów okresów na potrzeby szacowania przychodów.</span><span class="sxs-lookup"><span data-stu-id="6893a-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="6893a-107">Tworzenie typów okresów i praca z nimi</span><span class="sxs-lookup"><span data-stu-id="6893a-107">Create and work with period types</span></span>
<span data-ttu-id="6893a-108">Aby utworzyć typy okresów i pracować z nimi, wykonaj następujące czynności:</span><span class="sxs-lookup"><span data-stu-id="6893a-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="6893a-109">W środowisku aplikacji Dynamics 365 Finance przejdź do pozycji **Zarządzanie projektami i księgowanie** > **Konfiguracja** > **Szacowania** > **Typy okresów**.</span><span class="sxs-lookup"><span data-stu-id="6893a-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="6893a-110">Wybierz pozycję **Nowy**, aby utworzyć nowy typ okresu.</span><span class="sxs-lookup"><span data-stu-id="6893a-110">Select **New** to create new period type.</span></span> <span data-ttu-id="6893a-111">Wprowadź nazwę i opis.</span><span class="sxs-lookup"><span data-stu-id="6893a-111">Enter a name and description.</span></span>
3. <span data-ttu-id="6893a-112">W polu **Częstotliwość** wybierz wartość:</span><span class="sxs-lookup"><span data-stu-id="6893a-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="6893a-113">W przypadku wybrania opcji **Tydzień**, **Co dwa tygodnie**, **Co pół miesiąca**, **Miesiąc**, **Dzień**, **Kwartał** lub **Rok** kalendarz będzie używany do generowania okresów.</span><span class="sxs-lookup"><span data-stu-id="6893a-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="6893a-114">Jeśli wybierzesz opcję **Okres księgi**, okresy księgi z konfiguracji księgi głównej będą używane do generowania okresów.</span><span class="sxs-lookup"><span data-stu-id="6893a-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="6893a-115">W przypadku wybrania opcji **Nieograniczone** można wskazać okresy niestandardowe.</span><span class="sxs-lookup"><span data-stu-id="6893a-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="6893a-116">Wybierz rekord typu okresu, a następnie wybierz pozycję **Generuj okresy**, aby utworzyć okresy dla typu okresu.</span><span class="sxs-lookup"><span data-stu-id="6893a-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="6893a-117">Na podstawie wybranej częstotliwości okresu może być dostępna opcja określenia daty rozpoczęcia lub liczby okresów do wygenerowania.</span><span class="sxs-lookup"><span data-stu-id="6893a-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="6893a-118">Wybierz pozycję **Okresy**, aby przejrzeć wygenerowane okresy.</span><span class="sxs-lookup"><span data-stu-id="6893a-118">Select **Periods** to review generated periods.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]