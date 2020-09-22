---
title: Nowości i zmiany w programie Project Service Automation w wersji 3.x, wydanie 1 w 2020 r.
description: Niniejszy temat zawiera informacje dotyczące nowości i zmian w programie Project Service Automation w wersji 3, wydanie 1 z 2020 r.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754321"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="8c998-103">Nowości i zmiany w programie Project Service Automation w wersji 3, wydanie 1 w 2020 r.</span><span class="sxs-lookup"><span data-stu-id="8c998-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>
<span data-ttu-id="8c998-104">Temat wyróżnia podstawowe kwestie dotyczące uaktualniania podczas przechodzenia do najnowszej wersji programu Project Service Automation (PSA) w wersji 3.x, wydanie 1 w 2020 r.</span><span class="sxs-lookup"><span data-stu-id="8c998-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="8c998-105">Wpis czasu</span><span class="sxs-lookup"><span data-stu-id="8c998-105">Time entry</span></span>
<span data-ttu-id="8c998-106">Sposób obsługi wpisu godziny został rozszerzony w celu dostarczenia funkcji umożliwiających wydłużenie wpisu godziny do dalszych scenariuszy klientów.</span><span class="sxs-lookup"><span data-stu-id="8c998-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="8c998-107">Obejmuje to możliwość dodawania typów wpisów, które teraz dotyczą konkretnego zachowania w zależności od nazwy schematu pola **Ustawienia wpisu czasu**, wyświetlanych jako **źródło czasu**.</span><span class="sxs-lookup"><span data-stu-id="8c998-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="8c998-108">Zagadnienie dotyczące uaktualniania</span><span class="sxs-lookup"><span data-stu-id="8c998-108">Upgrade consideration</span></span>
<span data-ttu-id="8c998-109">W celu zapewnienia obsługi tej funkcjonalności role w usłudze PSA zostały zaktualizowane w celu uwzględnienia nowych uprawnień.</span><span class="sxs-lookup"><span data-stu-id="8c998-109">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="8c998-110">Te uprawnienia umożliwiają dostęp do odczytu do nowej encji , czyli **ustawień wpisu czasu**.</span><span class="sxs-lookup"><span data-stu-id="8c998-110">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="8c998-111">Użytkownikom, którzy wymagają możliwości logowania, powinna zostać przyznana rola użytkownika **Użytkownik wprowadzający czas** w dodatku do istniejących ról.</span><span class="sxs-lookup"><span data-stu-id="8c998-111">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="8c998-112">Ta rola obejmuje nowe funkcje, dzięki czemu będzie można kontynuować pracę z wpisem czasowym.</span><span class="sxs-lookup"><span data-stu-id="8c998-112">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="8c998-113">Zmiany aktualnie przedłużonych wpisów czasowych</span><span class="sxs-lookup"><span data-stu-id="8c998-113">Currently extended time entry changes</span></span>
<span data-ttu-id="8c998-114">Aby zminimalizować wpływ wpisu czasowego na bieżących użytkowników, ta zmiana roli jest jedynym wymogiem podstawowym koniecznym do kontynuowania korzystania z wpisu czasowego.</span><span class="sxs-lookup"><span data-stu-id="8c998-114">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="8c998-115">Jeśli zostały utworzone widoki niestandardowe lub odrębny czas wprowadzenia, należy ustawić prawidłową wartość PSA w polach **ustawienia wpisu czasowego**.</span><span class="sxs-lookup"><span data-stu-id="8c998-115">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
