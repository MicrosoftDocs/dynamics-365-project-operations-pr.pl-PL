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
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Nowości i zmiany w programie Project Service Automation w wersji 3, wydanie 1 w 2020 r.
Temat wyróżnia podstawowe kwestie dotyczące uaktualniania podczas przechodzenia do najnowszej wersji programu Project Service Automation (PSA) w wersji 3.x, wydanie 1 w 2020 r.

## <a name="time-entry"></a>Wpis czasu
Sposób obsługi wpisu godziny został rozszerzony w celu dostarczenia funkcji umożliwiających wydłużenie wpisu godziny do dalszych scenariuszy klientów. Obejmuje to możliwość dodawania typów wpisów, które teraz dotyczą konkretnego zachowania w zależności od nazwy schematu pola **Ustawienia wpisu czasu** , wyświetlanych jako **źródło czasu**. Dodano nowe rozwiązanie, takie jak godzina, wydatek, ustawianie stanu i zatwierdzenia (TESA) w celu obsługi tej funkcji.

### <a name="upgrade-consideration"></a>Zagadnienie dotyczące uaktualniania
W celu zapewnienia obsługi tej funkcjonalności role w usłudze PSA zostały zaktualizowane w celu uwzględnienia nowych uprawnień. Te uprawnienia umożliwiają dostęp do odczytu do nowej encji , czyli **ustawień wpisu czasu**.

Użytkownikom, którzy wymagają możliwości logowania, powinna zostać przyznana rola użytkownika **Użytkownik wprowadzający czas** w dodatku do istniejących ról. Ta rola obejmuje nowe funkcje, dzięki czemu będzie można kontynuować pracę z wpisem czasowym.

Ponadto w przypadku dowolnych niestandardowych modułów aplikacji, które zawierają wszystkie formularze dla encji wpisu godzin, konieczne będzie usunięcie z modułu **Formularza szybkiego tworzenia wpisu czasu TESA**.

### <a name="currently-extended-time-entry-changes"></a>Zmiany aktualnie przedłużonych wpisów czasowych
Aby zminimalizować wpływ wpisu czasowego na bieżących użytkowników, ta zmiana roli jest jedynym wymogiem podstawowym koniecznym do kontynuowania korzystania z wpisu czasowego. Jeśli zostały utworzone widoki niestandardowe lub odrębny czas wprowadzenia, należy ustawić prawidłową wartość PSA w polach **ustawienia wpisu czasowego**.
