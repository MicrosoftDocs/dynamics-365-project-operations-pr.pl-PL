---
title: Tworzenie wpisów czasu
description: W tym temacie zamieszczono informacje dotyczące tworzenia wpisów czasu.
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
ms.openlocfilehash: 520d3a6e6cc3d486d778c66c2ef7fd3ff20cd582
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149691"
---
# <a name="create-time-entries"></a><span data-ttu-id="c3231-103">Tworzenie wpisów czasu</span><span class="sxs-lookup"><span data-stu-id="c3231-103">Create time entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c3231-104">W poprzednich wersjach programu Dynamics 365 Project Service Automation wpisy czasu były wprowadzane tygodniowo.</span><span class="sxs-lookup"><span data-stu-id="c3231-104">In previous versions of Dynamics 365 Project Service Automation, time entries were entered on a weekly basis.</span></span> <span data-ttu-id="c3231-105">W wersji 3 rozwiązania Project Service Automation wpisy czasu są wprowadzane codziennie.</span><span class="sxs-lookup"><span data-stu-id="c3231-105">In version 3 of Project Service Automation, time entries are entered on a daily basis.</span></span> <span data-ttu-id="c3231-106">Jednak po utworzeniu kilku wpisów czasu można je tworzyć lub kopiować zbiorczo.</span><span class="sxs-lookup"><span data-stu-id="c3231-106">However, after a few time entries have been created, you can bulk create or copy them.</span></span>

## <a name="create-a-time-entry"></a><span data-ttu-id="c3231-107">Tworzenie wpisu czasu</span><span class="sxs-lookup"><span data-stu-id="c3231-107">Create a time entry</span></span>

<span data-ttu-id="c3231-108">Aby utworzyć wpis czasu, wykonaj następujące czynności.</span><span class="sxs-lookup"><span data-stu-id="c3231-108">Follow these steps to create a time entry.</span></span>

1. <span data-ttu-id="c3231-109">Na stronie **Wpisy czasu** kliknij przycisk **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="c3231-109">On the **Time Entries** page, select **New**.</span></span>
2. <span data-ttu-id="c3231-110">W oknie dialogowym **Szybkie tworzenie: Wpis czasu** wprowadź czas trwania wpisu czasu w minutach, godzinach lub dniach.</span><span class="sxs-lookup"><span data-stu-id="c3231-110">In the **Quick Create: Time Entry** dialog box, enter the duration of the time entry in minutes, hours, or days.</span></span> <span data-ttu-id="c3231-111">Czas trwania musi być wprowadzony w następującym formacie: *x* minut, *x* godzin lub *x* dni.</span><span class="sxs-lookup"><span data-stu-id="c3231-111">The duration must be entered in the following format: *x* minutes, *x* hours, or *x* days.</span></span> <span data-ttu-id="c3231-112">Godziny i dni można również wprowadzać jako wartości dziesiętne, na przykład *x,x* godzin lub *x,x* dni.</span><span class="sxs-lookup"><span data-stu-id="c3231-112">Hours and days can also be entered as decimal values, such as *x.x* hours or *x.x* days.</span></span>
3. <span data-ttu-id="c3231-113">Wybierz typ wpisu czasu oraz projekt, dla którego wprowadzasz ten wpis czasu.</span><span class="sxs-lookup"><span data-stu-id="c3231-113">Select the type of time entry and the project that you're entering the time entry for.</span></span>
4. <span data-ttu-id="c3231-114">W polu **Zadanie projektu** znajdź zadanie dla tego wpisu czasu.</span><span class="sxs-lookup"><span data-stu-id="c3231-114">In the **Project Task** field, find the task for this time entry.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c3231-115">W przypadku tworzenia wpisu czasu dla zadania, które nie jest przypisane do użytkownika, w polu **Zadanie projektu** kliknij przycisk **Wyszukaj**, wybierz pozycję **Zmień widok**, a następnie wybierz pozycję **Wszystkie aktywne zadania projektu**, a zostanie wyświetlona lista wszystkich zadań.</span><span class="sxs-lookup"><span data-stu-id="c3231-115">If you're creating a time entry for a task that isn't assigned to a user, in the **Project Task** field, select the **Search** button, select **Change View**, and then select **All Active Project Tasks** to list all tasks.</span></span>

5. <span data-ttu-id="c3231-116">Wprowadź opis, jeśli jest wymagany, a następnie wybierz pozycję **Zapisz i zamknij**.</span><span class="sxs-lookup"><span data-stu-id="c3231-116">Enter a description, if a description is required, and then select **Save and Close**.</span></span>

<span data-ttu-id="c3231-117">Po utworzeniu i zapisaniu wpisu czasu można go edytować w siatce wpisów czasu.</span><span class="sxs-lookup"><span data-stu-id="c3231-117">After the time entry is created and saved, you can edit it in the time entry grid.</span></span> <span data-ttu-id="c3231-118">Siatka wpisów czasu obsługuje dwa formaty:</span><span class="sxs-lookup"><span data-stu-id="c3231-118">The time entry grid supports two formats:</span></span>

- <span data-ttu-id="c3231-119">Wpisy czasu można wprowadzać w formacie **gg:mm**.</span><span class="sxs-lookup"><span data-stu-id="c3231-119">You can enter time entries in **hh:mm** format.</span></span> <span data-ttu-id="c3231-120">Ten format jest następnie konwertowany na godziny i ułamki.</span><span class="sxs-lookup"><span data-stu-id="c3231-120">This format is then converted to hours and fractions.</span></span>
- <span data-ttu-id="c3231-121">Godziny i ułamki można wprowadzać bezpośrednio.</span><span class="sxs-lookup"><span data-stu-id="c3231-121">You can enter hours and fractions directly.</span></span>

<span data-ttu-id="c3231-122">Zauważ, że ułamki godziny nie są minutami.</span><span class="sxs-lookup"><span data-stu-id="c3231-122">Note that the fractions of an hour aren't minutes.</span></span> <span data-ttu-id="c3231-123">Innymi słowy zapis 1,5 godziny oznacza 1 godzinę i 30 minut.</span><span class="sxs-lookup"><span data-stu-id="c3231-123">Therefore, 1.5 hours represents 1 hour and 30 minutes.</span></span> <span data-ttu-id="c3231-124">Ta sama reguła ma zastosowanie do ułamków dnia.</span><span class="sxs-lookup"><span data-stu-id="c3231-124">The same rule applies to fractions of a day.</span></span> <span data-ttu-id="c3231-125">Jeden dzień to 24 godziny, a 0,5 dnia oznacza 12 godzin.</span><span class="sxs-lookup"><span data-stu-id="c3231-125">One day is 24 hours, and 0.5 days represents 12 hours.</span></span>

## <a name="bulk-create-time-entries"></a><span data-ttu-id="c3231-126">Zbiorcze tworzenie wpisów czasu</span><span class="sxs-lookup"><span data-stu-id="c3231-126">Bulk create time entries</span></span>

<span data-ttu-id="c3231-127">Po utworzeniu kilku wpisów czasu można je kopiować i w ten sposób tworzyć dodatkowe wpisy czasu zbiorczo.</span><span class="sxs-lookup"><span data-stu-id="c3231-127">After a few time entries have been created, you can copy them to create additional time entries in bulk.</span></span>

1. <span data-ttu-id="c3231-128">Na stronie **Wpisy czasu** kliknij przycisk **Kopiuj tydzień**.</span><span class="sxs-lookup"><span data-stu-id="c3231-128">On the **Time Entries** page, select **Copy Week**.</span></span>
2. <span data-ttu-id="c3231-129">W grupie pól **Z okresu** w polach **Data rozpoczęcia** i **Data zakończenia** zdefiniuj zakres dat, z którego mają zostać skopiowane wpisy czasu.</span><span class="sxs-lookup"><span data-stu-id="c3231-129">In the **From Period** field group, in the **Start Date** and **End Date** fields, define the date range to copy time entries from.</span></span>
3. <span data-ttu-id="c3231-130">W grupie pól **Do okresu** w polu **Data rozpoczęcia** określ dzień, dla którego mają zostać utworzone wpisy czasu.</span><span class="sxs-lookup"><span data-stu-id="c3231-130">In the **To Period** field group, in the **Start Date** field, specify the date to create time entries for.</span></span>
4. <span data-ttu-id="c3231-131">Kliknij przycisk **Kopiuj**, aby utworzyć kopię wpisów czasu odpowiadających dniu tygodnia określonemu w grupie pól **Do okresu**.</span><span class="sxs-lookup"><span data-stu-id="c3231-131">Select **Copy** to create a copy of the time entries that correspond to the day of the week that is specified in the **To Period** field group.</span></span> <span data-ttu-id="c3231-132">Na przykład wpis czasu dla poniedziałku poprzedniego tygodnia jest kopiowany do poniedziałku tygodnia określonego w grupie pól **Do okresu**.</span><span class="sxs-lookup"><span data-stu-id="c3231-132">For example, the time entry for Monday of last week is copied to Monday of the week that is specified in the **To Period** field group.</span></span>

## <a name="import-data-for-time-entries"></a><span data-ttu-id="c3231-133">Importowanie danych dla wpisów czasu</span><span class="sxs-lookup"><span data-stu-id="c3231-133">Import data for time entries</span></span>

<span data-ttu-id="c3231-134">Można importować dane z rezerwacji projektów i przypisań.</span><span class="sxs-lookup"><span data-stu-id="c3231-134">You can import data from project bookings and assignments.</span></span> <span data-ttu-id="c3231-135">Podczas importowania danych można określić zakres dat dla rezerwacji, które mają zostać zaimportowane, a następnie jawnie wybrać rezerwacje, które mają zostać utworzone jako wpisy czasu **Wersja robocza**.</span><span class="sxs-lookup"><span data-stu-id="c3231-135">When you import data, you can specify the date range of the bookings to import and then explicitly select the bookings that should be created as **Draft** time entries.</span></span>

## <a name="group-by-sort-search-and-filter-capabilities"></a><span data-ttu-id="c3231-136">Funkcje grupowania według, sortowania, wyszukiwania i filtrowania</span><span class="sxs-lookup"><span data-stu-id="c3231-136">Group by, sort, search, and filter capabilities</span></span>

<span data-ttu-id="c3231-137">Wpisy czasu można grupować i filtrować według wymiarów określonych w kolumnach.</span><span class="sxs-lookup"><span data-stu-id="c3231-137">You can group and filter time entries by the dimensions that are specified in the columns.</span></span> <span data-ttu-id="c3231-138">W polu **Grupuj według** wybierz wymiar, który ma być używany do filtrowania wpisów czasu.</span><span class="sxs-lookup"><span data-stu-id="c3231-138">In the **Group by** field, select the dimension to use to filter time entries.</span></span> <span data-ttu-id="c3231-139">Przy użyciu strzałek sortowania w nagłówkach kolumn można również sortować rekordy wpisów czasu w porządku rosnącym lub malejącym.</span><span class="sxs-lookup"><span data-stu-id="c3231-139">You can also sort the time entry records in ascending or descending order by using the sort arrow on the column headings.</span></span> <span data-ttu-id="c3231-140">Ponadto można wyświetlać lub ukrywać wpisy, klikając przycisk **Filtruj** w nagłówkach kolumn, a następnie w polu **Wyszukaj** wprowadzając tekst, który ma być używany do wyszukiwania wpisów czasu według nazwy projektu, zadania projektu, godziny wpisu lub zasobu.</span><span class="sxs-lookup"><span data-stu-id="c3231-140">Additionally, you can show or hide entries by selecting the **Filter** button on the column headings, and then, in the **Search** box, entering the text that should be used to search for time entries by project name, project task, time entry, or resource.</span></span>
