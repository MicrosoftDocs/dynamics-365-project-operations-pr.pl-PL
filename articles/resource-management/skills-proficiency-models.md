---
title: Kwalifikacje i certyfikacje
description: Ten temat zawiera informacje na temat dodawania charakterystyk kwalifikacji i certyfikacji do zasobów.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4c814754e68b3a1a8bf8784434d45010bf8d0123
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908441"
---
# <a name="skills-and-certifications"></a><span data-ttu-id="f3429-103">Kwalifikacje i certyfikacje</span><span class="sxs-lookup"><span data-stu-id="f3429-103">Skills and certifications</span></span>
<span data-ttu-id="f3429-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="f3429-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f3429-105">Charakterystyki służą do wzbogacenia atrybutów używanych do opisywania możliwości zasobu.</span><span class="sxs-lookup"><span data-stu-id="f3429-105">Characteristics are used to enrich the attributes used to describe the abilities of a resource.</span></span> <span data-ttu-id="f3429-106">Każda charakterystyka zasobu może być opisana jako **Umiejętność** lub **Certyfikat**.</span><span class="sxs-lookup"><span data-stu-id="f3429-106">Each characteristic of a resource can be described as a **Skill** or a **Certification**.</span></span>

<span data-ttu-id="f3429-107">Dodanie charakterystyk do wymagań zasobów pozwala na udokumentowanie umiejętności lub wiedzy fachowej niezbędnych do wykonania różnych zadań w projekcie.</span><span class="sxs-lookup"><span data-stu-id="f3429-107">Adding characteristics to resource requirements lets you document the knowledge or expertise needed by a resource to complete tasks on a project.</span></span> <span data-ttu-id="f3429-108">Charakterystyki pozwalają filtrować listę dostępnych zasobów pod kątem zasobów, które posiadają wymagane charakterystyki w momencie planowania zapotrzebowania na zasoby.</span><span class="sxs-lookup"><span data-stu-id="f3429-108">Characteristics let you filter the list of available resources to those resources that have the required characteristics when scheduling the resource requirement.</span></span>

## <a name="add-characteristics"></a><span data-ttu-id="f3429-109">Dodaj właściwości</span><span class="sxs-lookup"><span data-stu-id="f3429-109">Add characteristics</span></span>

1. <span data-ttu-id="f3429-110">W menu głównym otwórz **Zasoby**, a następnie wybierz sekcję **Zasoby**. Tam wybierz **Umiejętności**.</span><span class="sxs-lookup"><span data-stu-id="f3429-110">From the main menu, open **Resources** and in the **Resources** section, select **Skills**.</span></span>
2. <span data-ttu-id="f3429-111">Wybierz **Nowa**, aby dodać właściwość.</span><span class="sxs-lookup"><span data-stu-id="f3429-111">Select **New** to add characteristics.</span></span>
3. <span data-ttu-id="f3429-112">Wypełnij wymagane pola, a następnie kliknij **Typ charakterystyki**.</span><span class="sxs-lookup"><span data-stu-id="f3429-112">Fill in the required fields and select the **Characteristic Type**.</span></span>

## <a name="assign-characteristics-to-resources"></a><span data-ttu-id="f3429-113">Przypisz właściwości do zasobów</span><span class="sxs-lookup"><span data-stu-id="f3429-113">Assign characteristics to resources</span></span>

1. <span data-ttu-id="f3429-114">Z menu głównego, wybierz **Planowanie zasobów** > **Zasoby możliwe do zarezerwowania**.</span><span class="sxs-lookup"><span data-stu-id="f3429-114">From the main menu, select **Resources** > **Bookable Resources**.</span></span> <span data-ttu-id="f3429-115">Zostanie otwarta strona **Aktywne zasoby możliwe do zarezerwowania** i będzie można wyświetlić listę wszystkich dostępnych zasobów w systemie.</span><span class="sxs-lookup"><span data-stu-id="f3429-115">The **Active Bookable Resources** page opens and you can view a list of all available resources in the system.</span></span>
2. <span data-ttu-id="f3429-116">Wybierz zasób z listy dostępnych zasobów, które można zarezerwować.</span><span class="sxs-lookup"><span data-stu-id="f3429-116">From the list, select the name of a bookable resource.</span></span>
3. <span data-ttu-id="f3429-117">W sekcji **Project Service** wybierz **+Dodaj rekord właściwości zasobu, który można zarezerwować**.</span><span class="sxs-lookup"><span data-stu-id="f3429-117">In the **Project Service** section, select **+Add Bookable Resource Characteristics record**.</span></span>
4. <span data-ttu-id="f3429-118">To spowoduje otworzenie okienka wyskakującego, w którym będziesz mógł wyszukać i wybrać wymagane charakterystyki i dodać **Wartość oceny** dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="f3429-118">In the pop-up window that opens, find and select the required characteristics, and add a **Rating Value** for the resource.</span></span>
5. <span data-ttu-id="f3429-119">Zaznacz **Zapisz i zamknij**.</span><span class="sxs-lookup"><span data-stu-id="f3429-119">Select **Save & Close**.</span></span>

## <a name="assign-characteristics-to-resource-requirements"></a><span data-ttu-id="f3429-120">Przypisz właściwości do wymagań zasobów</span><span class="sxs-lookup"><span data-stu-id="f3429-120">Assign characteristics to resource requirements</span></span>

1. <span data-ttu-id="f3429-121">W siatce członka zespołu znajdź i kliknij dwukrotnie danego członka zespołu ogólnego z parametrami, które wymagają aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="f3429-121">In the team member grid, find and double-click the generic team member with the characteristics that need to be updated.</span></span>
2. <span data-ttu-id="f3429-122">W sekcji **Szczegóły członka zespołu projektu** wybierz kartę **Wymaganie zasobu**.</span><span class="sxs-lookup"><span data-stu-id="f3429-122">In the **Project Team member Detail**, select the **Resource Requirement** tab.</span></span>
3. <span data-ttu-id="f3429-123">W podsiatce **Umiejętność** wybierz pozycję **+ Dodaj nową charakterystykę wymagania.**</span><span class="sxs-lookup"><span data-stu-id="f3429-123">In the **Skills** subgrid, select **+Add new Requirement Characteristic.**</span></span>
4. <span data-ttu-id="f3429-124">W okienku szybkiego tworzenia znajdź i wybierz wymagane charakterystyki i dodaj **Wartość oceny**.</span><span class="sxs-lookup"><span data-stu-id="f3429-124">In the quick create pane, find and select the required characteristics and add a **Rating Value**.</span></span>
5. <span data-ttu-id="f3429-125">Zaznacz **Zapisz i zamknij**.</span><span class="sxs-lookup"><span data-stu-id="f3429-125">Select **Save & Close**.</span></span>