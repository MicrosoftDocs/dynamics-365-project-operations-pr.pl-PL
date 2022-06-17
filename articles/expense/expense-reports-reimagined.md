---
title: Raporty wydatków w nowej wersji (zawiera wideo)
description: W tym artykule objaśniono nowo zaprojektowane, udoskonalone środowisko wprowadzania raportu wydatków.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c74b4b70722af72bc66dba0662813c29d3d1df04
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930285"
---
# <a name="expense-reports-reimagined"></a>Przebudowane raporty wydatków

Zapis raportu z wydatków został przeprojektowany w celu uproszczenia procesu i skrócenia czasu potrzebnego do utworzenia raportu. Oto najważniejsze składniki nowego doświadczenia raportowania wydatków:

- Nowy obszar roboczy Zarządzanie wydatkami, który umożliwia uzyskanie dostępu do wydatków pełnomocnika.
- Nowy system dopasowywania paragonów w celu lepszego pokazywania nagłówków paragonów i uproszczenia procesu dołączania paragonów do wierszy wydatków.
- Nowa siatka tylko do odczytu, która umożliwia wyświetlanie wielu dodatkowych wierszy wydatków i innych kolumn danych. Teraz można wyświetlać wszystkie wyszczególnione i podzielone wiersze oraz koszty nadrzędne.
- Uproszczone okienko do edycji kosztów.
- Przeprojektowane komunikaty o błędach, ostrzeżeniach i zasadach w celu uzyskania prawidłowego kontekstu i zrozumienia problemu oraz sposobu jego rozwiązywania. Usunięto kilka komunikatów, które były wyświetlane przed zakończeniem przez użytkowników swoich zadań i rozwiązać problemy.
- Nowa strona określająca wymagane pola, opcjonalne pola i pola, które nie powinny być uwzględnione. Ta strona umożliwia zmniejszenie liczby pól, które należy określić.
- Nowy wygląd i działanie raportów wydatków, dzięki czemu raporty nie będą wyglądać tak, jakby były projektowane tylko dla księgowych.

Aby włączyć nową funkcję, użyj obszaru roboczego **Zarządzanie funkcjami** w celu włączenia funkcji **Obszar roboczy przeprojektowanych raportów wydatków**. Po włączeniu tej funkcji zostaną wykonane następujące akcje:

- Istniejący obszar roboczy Zarządzania wydatkami zostanie zastąpiony nowym obszarem roboczym.
- Dodawany jest nowy element menu z widocznością pola wydatku.
- Nie są usuwane żadne istniejące pozycje menu dla raportów wydatków (istniejąca strona) ani z pól raportu wydatków.
- Przepływy pracy i wszelkie zatwierdzenia wciąż przenoszą użytkownika na stronę istniejących raportów z wydatków.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4IQFM]

## <a name="new-features"></a>Nowe funkcje

| Nowe funkcje | Opis |
|---|----|
| Widoczność pola wydatków | Nowa strona konfiguracji umożliwia określenie pól, które mają być wyłączone dla organizacji. Można również określić pola, które mają być wymagane, oraz pola, które są zalecane. |
| Pola wymagane | Nowa prosta konfiguracja umożliwia udostępnienie niektórych pól bez konieczności korzystania ze środowiska zasad. |
| Pola opcjonalne | Pola opcjonalne są teraz na drugiej stronie. W ten sposób pracownicy nie będą czuć, że muszą wypełnić pola, ale nadal będą one łatwo dostępne. |
| Dodawanie niepowiązanych paragonów | Możliwość dodawania niedołączonych paragonów do raportu wydatków jest widoczna w obszarze roboczym i w raporcie wydatków. |
| Lepsza obsługa wiadomości | Lepszy wgląd w wiersze wydatków z ostrzeżeniami lub błędami. |
| Redukcja komunikatów na pasku komunikatów| Liczba komunikatów na pasku informacyjnym została zmniejszona i uniemożliwiono wyświetlanie zduplikowanych komunikatów w wielu przypadkach. |
| Połączono razem wspólne akcje | Interfejs został oczyszczony wraz z dodaniem nowych akcji dla większości typowych akcji na poziomie wiersza i dodaniem przycisku wielokropka (...) w celu wyszukania nagłówków i innych rzadziej występujących akcji. |
| Nowy obszar roboczy, aby zwiększyć widoczność | Nowy obszar roboczy łączy funkcje i łącza umożliwiające użytkownikom poruszanie się po różnych obszarach. |
| Dodawanie istniejących kosztów i paragonów podczas tworzenia wydatku | Podczas tworzenia raportów z wydatków można dodać wszystkie wydatki lub wybrać wydatki niezwiązane. Niezwiązane wydatki to wydatki, które zostały zaimportowane z firmowego kanału informacyjnego karty kredytowej lub wydatki, które zostały ręcznie utworzone przez użytkownika, ale nie zostały dołączone do raportu z wydatków.|
| Kalkulator wymiany walut | Dodano kalkulator kursów wymiany walut, który umożliwia obliczenie kursu wymiany dla kosztów w ramach fakturowania wielowalutowego. |
| Zapisywanie i dodawanie nowych wierszy wydatku | Przyciski **Zapisz** i **Nowe** są dostępne po wprowadzeniu nowych wydatków w celu szybkiego wprowadzenia wierszy wydatków. |
| Lepsza widoczność podzielonych i wyszczególnionych wierszy | Wyszczególnione i podzielone wiersze są dodawane bezpośrednio do listy wydatków w celu zwiększenia widoczności i ułatwienia sprawdzania, czy występują jakiekolwiek problemy. |
| Wyświetlanie szczegółów podkategorii w wierszach pozycjach | Poszczególne wiersze wydatku nadrzędnego pokazują etykiety podkategorii w raporcie z wydatków. Podział na pozycje pozwala szybko przejrzeć szczegółowe szczegóły.|
|Szybki podział wydatków cyklicznych na pozycje | Obszar roboczy wydatków w nowej wersji umożliwia szybkie dzielenie wydatków cyklicznych na pozycje przez dodanie podkategorii, daty rozpoczęcia i ilości. Ilość odnosi się do liczby powtarzających się opłat w ciągłym okresie. |
| Pokazywanie paragonów podczas podziału na pozycje | Wyświetlanie paragonów podczas podziału na pozycje jest teraz możliwe. |
| Wybór zaliczki gotówkowej | Wybierz jedną lub więcej zaliczek gotówkowych do realizacji pojedynczej transakcji wydatków. |
| Saldo zaliczki gotówkowej | Przejrzyj saldo zaliczki gotówkowej w czasie rzeczywistym podczas tworzenia wpisu wydatków względem zatwierdzonych i zapłaconych zaliczek gotówkowych. |

Początkowa wersja koncentruje się na scenariuszach wydatków. Scenariusz, w którym użytkownik sprawdza lub zatwierdza raporty wydatków będzie działał na bazie istniejącej strony wydatków.


Następujące funkcje nie są obsługiwane w obszarze roboczym przeprojektowanych raportów wydatków, ale są planowane w przyszłych wydaniach: 

- Integracja wniosków wyjazdowych
- Wpis wydatku na dzień
- Wsparcie tymczasowych osób zatwierdzających
- Możliwość wyświetlania historii przepływu pracy


[!INCLUDE[footer-include](../includes/footer-banner.md)]
