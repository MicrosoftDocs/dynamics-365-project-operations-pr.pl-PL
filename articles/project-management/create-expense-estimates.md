---
title: Szacowanie wydatków
description: W tym temacie zamieszczono informacje dotyczące definiowania lub szacowania kosztów opartych na projektach.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 10872366453985561bda0c07e50cff7f5f6d333e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131716"
---
# <a name="expense-estimates"></a><span data-ttu-id="f4c30-103">Szacowanie wydatków</span><span class="sxs-lookup"><span data-stu-id="f4c30-103">Expense estimates</span></span>
<span data-ttu-id="f4c30-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="f4c30-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f4c30-105">Oprócz definiowania oszacowań opartych na zasobach Dynamics 365 Project Operations umożliwia menedżerom projektów definiowanie kosztów opartych na projekcie dla każdego projektu.</span><span class="sxs-lookup"><span data-stu-id="f4c30-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="f4c30-106">Każdy element wydatków może być skojarzony z określoną kategorią zadania lub wydatku projektu.</span><span class="sxs-lookup"><span data-stu-id="f4c30-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="f4c30-107">Kategorie wydatków są zwykle definiowane na poziomie organizacji.</span><span class="sxs-lookup"><span data-stu-id="f4c30-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="f4c30-108">Kalkulacja cen dla każdej kategorii wydatków jest zwykle definiowane w poniższej hierarchii:</span><span class="sxs-lookup"><span data-stu-id="f4c30-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="f4c30-109">Organizacja</span><span class="sxs-lookup"><span data-stu-id="f4c30-109">Organization</span></span>
- <span data-ttu-id="f4c30-110">Klient</span><span class="sxs-lookup"><span data-stu-id="f4c30-110">Customer</span></span>
- <span data-ttu-id="f4c30-111">Oferta / kontrakt</span><span class="sxs-lookup"><span data-stu-id="f4c30-111">Quote/contract</span></span>

<span data-ttu-id="f4c30-112">Wykonaj poniższe kroki, aby wyświetlić, dodać lub usunąć koszty projektu.</span><span class="sxs-lookup"><span data-stu-id="f4c30-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="f4c30-113">Przejdź do obszaru **Projekty** i wybierz projekt, który chcesz edytować.</span><span class="sxs-lookup"><span data-stu-id="f4c30-113">Go to **Projects**, and select the project you want to work on.</span></span>
2. <span data-ttu-id="f4c30-114">Wybierz **Oszacowania projektów** i wyświetl listę wydatków projektowych.</span><span class="sxs-lookup"><span data-stu-id="f4c30-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="f4c30-115">Wybierz opcję **Nowe koszty**, aby dodać wydatek.</span><span class="sxs-lookup"><span data-stu-id="f4c30-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="f4c30-116">Możesz też wybrać wydatek, który ma zostać usunięty, a następnie wybrać pozycję **Usuń wydatek**.</span><span class="sxs-lookup"><span data-stu-id="f4c30-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="f4c30-117">Dla każdego elementu wiersza wydatków są definiowane następujące atrybuty:</span><span class="sxs-lookup"><span data-stu-id="f4c30-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="f4c30-118">**Kategoria**: wspólne zgrupowania używane do opisywania wszystkich kosztów poniesionych w związku z projektem.</span><span class="sxs-lookup"><span data-stu-id="f4c30-118">**Category**: The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="f4c30-119">**Data rozpoczęcia**: data, kiedy zakłada się, że wydatek zostanie poniesiony.</span><span class="sxs-lookup"><span data-stu-id="f4c30-119">**Start Date**: The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="f4c30-120">**Ilość**: szacowana liczba pozycji wydatku dla określonej kategorii.</span><span class="sxs-lookup"><span data-stu-id="f4c30-120">**Quantity**: The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="f4c30-121">**Jednostkowy koszt własny**: cena jednostkowa użyta do obliczenia kosztu wydatku.</span><span class="sxs-lookup"><span data-stu-id="f4c30-121">**Unit Cost Price**: The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="f4c30-122">**Jednostkowa cena sprzedaży**: cena jednostkowa użyta do obliczenia ceny sprzedaży danego wydatku.</span><span class="sxs-lookup"><span data-stu-id="f4c30-122">**Unit Sales Price**: The unit price used to calculate the sale prices of the expense.</span></span>

