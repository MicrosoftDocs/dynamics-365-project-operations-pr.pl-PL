---
title: Przeprojektowane raporty z wydatków
description: W tym temacie zamieszczono informacje dotyczące zmienionej i ulepszonej funkcji tworzenia raportów wydatków w Microsoft Dynamics 365 Finance. Nowe środowisko upraszcza proces tworzenia raportów o wydatkach i skraca wymagany czas.
author: ryansandness
manager: AnnBe
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: f2acd9eab52629b0baeb82a399993fbc6337c722
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650152"
---
# <a name="redesigned-expense-reports"></a>Przeprojektowane raporty z wydatków
[!include[banner](../includes/banner.md)]

Wpis raportu wydatków został przeprojektowany w celu uproszczenia pracy i zmniejszenia czasu wymaganego do wykonania raportów o wydatkach. Oto najważniejsze składniki nowego doświadczenia raportowania wydatków:

- Nowy obszar roboczy Zarządzanie wydatkami, który umożliwia uzyskanie dostępu do wydatków pełnomocnika.
- Nowy system dopasowywania paragonów w celu lepszego pokazywania nagłówków paragonów i uproszczenia procesu dołączania paragonów do wierszy wydatków.
- Nowa siatka tylko do odczytu, która umożliwia wyświetlenie wielu dodatkowych wierszy i dodatkowych kolumn z danymi. Teraz można wyświetlać wszystkie wyszczególnione i podzielone wiersze oraz koszty nadrzędne.
- Uproszczone okienko do edycji kosztów.
- Przeprojektowane komunikaty o błędach, ostrzeżeniach i zasadach w celu ułatwienia zrozumienia prawidłowego kontekstu i zrozumienia problemu oraz sposobu jego rozwiązywania. Firma Microsoft usunęła wiele komunikatów, które wcześniej wyświetlane były użytkownikom, zanim mieli oni możliwość wykonania swoich zadań i rozwiązania problemów, takich jak niekompletny komunikat dotyczący podziału na pozycje.
- Nowa strona określająca pola, które są wymagane w organizacji, opcjonalne pola i pola, które nie powinny być przechwycone. Ta strona umożliwia zmniejszenie liczby pól, które użytkownicy muszą określić.
- Nowy wygląd i działanie raportów wydatków, dzięki czemu raporty nie będą wyglądać tak, jakby były projektowane tylko dla księgowych.

Aby włączyć nowe środowisko, w obszarze roboczym **Zarządzanie funkcjami** można włączyć **Przetworzone raporty wydatków**. Po włączeniu tej funkcji zostaną wykonane następujące akcje:

- Istniejący obszar roboczy Zarządzania wydatkami zostanie zastąpiony nowym obszarem roboczym.
- Dodawany jest nowy element menu z widocznością pola wydatku.
- Nie są usuwane żadne istniejące pozycje menu dla raportów wydatków (istniejąca strona) ani z pól raportu wydatków.
- Przepływy pracy i wszelkie zatwierdzenia wciąż przenoszą użytkownika na stronę istniejących raportów z wydatków.

## <a name="getting-started-video-for-new-users"></a>Wideo wprowadzające do rozwiązania dla nowych użytkowników

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Y7gO]

[Wydatkowanie w Dynamics 365 for Finance and Operations](https://youtu.be/Ocy-MsTvEE0) — film (pokazany powyżej) jest częścią [Listy odtwarzania Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) dostępnej na YouTube.

## <a name="new-features"></a>Nowe funkcje

| Nowe funkcje | Opis |
|---|----|
| Widoczność pola wydatków | Nowa strona ustawień umożliwia wskazanie, które pola powinny być wyłączone w organizacji, jakie pola powinny być wymagane i które pola są zalecane. |
| Pola wymagane | Nowa prosta konfiguracja umożliwia udostępnienie niektórych pól bez konieczności korzystania ze środowiska zasad. |
| Pola opcjonalne | Pola opcjonalne są teraz na drugiej stronie. W ten sposób pracownicy nie będą czuć, że muszą wypełnić pola, ale nadal będą one łatwo dostępne. |
| Dodawanie niepowiązanych paragonów | Możliwość dodawania niedołączonych paragonów do raportu wydatków jest widoczna w obszarze roboczym i w raporcie wydatków. |
| Lepsza obsługa wiadomości | Lepszy wgląd w wiersze wydatków z ostrzeżeniami lub błędami. |
| Redukcja komunikatów na pasku komunikatów| Liczba komunikatów na pasku informacyjnym została zmniejszona i uniemożliwiono wyświetlanie zduplikowanych komunikatów w wielu przypadkach. |
| Połączono razem wspólne akcje | Interfejs został oczyszczony wraz z dodaniem nowych akcji dla większości typowych akcji na poziomie wiersza i dodaniem przycisku wielokropka (...) w celu wyszukania nagłówków i innych rzadziej występujących akcji. |
| Nowy obszar roboczy, aby zwiększyć widoczność | Nowy obszar roboczy łączy funkcje i łącza umożliwiające użytkownikom poruszanie się po różnych obszarach. |
| Dodawanie istniejących kosztów i paragonów podczas tworzenia wydatku | Tworząc raporty o wydatkach, można dodać do niego wszystkie lub wybrane wydatki i paragony. |
| Kalkulator wymiany walut | Dodano kalkulator kursów wymiany walut, który umożliwia obliczenie kursu wymiany dla kosztów w ramach fakturowania wielowalutowego. |
| Zapisywanie i dodawanie nowych wierszy wydatku | Przyciski **Zapisz** i **Nowe** są dostępne po wprowadzeniu nowych wydatków w celu szybkiego wprowadzenia wierszy wydatków. |
| Lepsza widoczność podzielonych i wyszczególnionych wierszy | Wyszczególnione i podzielone wiersze są dodawane bezpośrednio do listy wydatków w celu zwiększenia widoczności i ułatwienia sprawdzania, czy występują jakiekolwiek problemy związane z zasadami lub inne. |
| Pokazywanie paragonów podczas podziału na pozycje | Wyświetlanie paragonów podczas podziału na pozycje jest teraz możliwe. |

Początkowa wersja koncentruje się na scenariuszach wydatków. Scenariusz, w którym użytkownik sprawdza lub zatwierdza raporty wydatków będzie działał na bazie istniejącej strony wydatków.

Następujące funkcje są dostępne na obecnej stronie ale nie są jeszcze dostępne na nowej stronie. Te funkcje zostaną wprowadzone ponownie w ciągu kilku kolejnych wersji:

- Zatwierdzenia
- Zatwierdzanie rachunków z dostawcami i możliwość edytowania księgowania
- Wiele punktów wejścia
- Integracja wniosków wyjazdowych
- Encja danych dla widoczności pola wydatku
- Wpis dla wydatków w ramach diet na dzień
- Przepływ pracy na poziomie wiersza
- Wsparcie tymczasowych osób zatwierdzających
- Wyszczególnianie zaawansowane
