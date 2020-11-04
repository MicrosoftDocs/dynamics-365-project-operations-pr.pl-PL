---
title: Nowości i zmiany w programie Project Service Automation w wersji 3.x, wydanie 1 w 2020 r.
description: Niniejszy temat zawiera informacje dotyczące nowości i zmian w programie Project Service Automation w wersji 3, wydanie 1 z 2020 r.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 16b51995f863d9ee54172625dacbf081c51c8556
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081958"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="9c455-103">Nowości i zmiany w programie Project Service Automation w wersji 3, wydanie 1 w 2020 r.</span><span class="sxs-lookup"><span data-stu-id="9c455-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>
<span data-ttu-id="9c455-104">Temat wyróżnia podstawowe kwestie dotyczące uaktualniania podczas przechodzenia do najnowszej wersji programu Project Service Automation (PSA) w wersji 3.x, wydanie 1 w 2020 r.</span><span class="sxs-lookup"><span data-stu-id="9c455-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="9c455-105">Wpis czasu</span><span class="sxs-lookup"><span data-stu-id="9c455-105">Time entry</span></span>
<span data-ttu-id="9c455-106">Sposób obsługi wpisu godziny został rozszerzony w celu dostarczenia funkcji umożliwiających wydłużenie wpisu godziny do dalszych scenariuszy klientów.</span><span class="sxs-lookup"><span data-stu-id="9c455-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="9c455-107">Obejmuje to możliwość dodawania typów wpisów, które teraz dotyczą konkretnego zachowania w zależności od nazwy schematu pola **Ustawienia wpisu czasu** , wyświetlanych jako **źródło czasu**.</span><span class="sxs-lookup"><span data-stu-id="9c455-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings** , displayed as **Time Source**.</span></span> <span data-ttu-id="9c455-108">Dodano nowe rozwiązanie, takie jak godzina, wydatek, ustawianie stanu i zatwierdzenia (TESA) w celu obsługi tej funkcji.</span><span class="sxs-lookup"><span data-stu-id="9c455-108">A new solution, called Time, Expense, Statusing, and Approvals (TESA) has been added to support this functionality.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="9c455-109">Zagadnienie dotyczące uaktualniania</span><span class="sxs-lookup"><span data-stu-id="9c455-109">Upgrade consideration</span></span>
<span data-ttu-id="9c455-110">W celu zapewnienia obsługi tej funkcjonalności role w usłudze PSA zostały zaktualizowane w celu uwzględnienia nowych uprawnień.</span><span class="sxs-lookup"><span data-stu-id="9c455-110">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="9c455-111">Te uprawnienia umożliwiają dostęp do odczytu do nowej encji , czyli **ustawień wpisu czasu**.</span><span class="sxs-lookup"><span data-stu-id="9c455-111">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="9c455-112">Użytkownikom, którzy wymagają możliwości logowania, powinna zostać przyznana rola użytkownika **Użytkownik wprowadzający czas** w dodatku do istniejących ról.</span><span class="sxs-lookup"><span data-stu-id="9c455-112">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="9c455-113">Ta rola obejmuje nowe funkcje, dzięki czemu będzie można kontynuować pracę z wpisem czasowym.</span><span class="sxs-lookup"><span data-stu-id="9c455-113">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

<span data-ttu-id="9c455-114">Ponadto w przypadku dowolnych niestandardowych modułów aplikacji, które zawierają wszystkie formularze dla encji wpisu godzin, konieczne będzie usunięcie z modułu **Formularza szybkiego tworzenia wpisu czasu TESA**.</span><span class="sxs-lookup"><span data-stu-id="9c455-114">Additionally, if you have any custom app modules that include all forms for the time entry entity, you will be required to remove the **TESA time Entry Quick Create Form** from the module.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="9c455-115">Zmiany aktualnie przedłużonych wpisów czasowych</span><span class="sxs-lookup"><span data-stu-id="9c455-115">Currently extended time entry changes</span></span>
<span data-ttu-id="9c455-116">Aby zminimalizować wpływ wpisu czasowego na bieżących użytkowników, ta zmiana roli jest jedynym wymogiem podstawowym koniecznym do kontynuowania korzystania z wpisu czasowego.</span><span class="sxs-lookup"><span data-stu-id="9c455-116">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="9c455-117">Jeśli zostały utworzone widoki niestandardowe lub odrębny czas wprowadzenia, należy ustawić prawidłową wartość PSA w polach **ustawienia wpisu czasowego**.</span><span class="sxs-lookup"><span data-stu-id="9c455-117">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
