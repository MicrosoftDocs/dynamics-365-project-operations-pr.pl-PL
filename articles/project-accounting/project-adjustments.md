---
title: Korekty projektu
description: Ten artykuł zawiera informacje o korektach projektu.
author: ryansandness
ms.date: 11/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 52a262adce2bb624bc088e50858e25824f845e5c
ms.sourcegitcommit: bb03ac64e01112c93bb24035a51653a0a88cd5fc
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788306"
---
# <a name="project-adjustments"></a>Korekty projektu

_**Dotyczy:** Project Operations dla scenariuszy obejmujących magazynowanie/zlecenia produkcyjne_

## <a name="adjustments-overview"></a>Omówienie korekt

Można skonfigurować rozwiązanie Microsoft Dynamics 365 Project Operations tak, aby użytkownicy mogą wprowadzać zmiany w opublikowanych transakcjach. Można jednak dostosować pojedynczo transakcje projektów lub zaznaczyć wiele transakcji równocześnie z listy wszystkich transakcji projektu. Korekty projektu są używane na przykład do masowego aktualizowania stanu rozliczeń, ponownego obliczania kosztu po zmianie konfiguracji lub aktualizowania źródeł funduszy.

Użytkownicy mogą uzyskać dostęp do funkcji korekty projektu na kilka sposobów:

- Można to zrobić za pomocą strony **Dostosuj transakcje**, do której można uzyskać dostęp z witryny **Zarządzanie projektami i księgowością** \> **Ustawienia**.
- Używając przycisku **Dostosowania** na stronie **Opublikowany projekt**, do którego można uzyskać dostęp z witryny **Zarządzanie projektami i księgowość** \> **Transakcje**.
- Używając przycisku **Korekta** na stronie **Zaksięgowanie transakcje projektu** w kontekście projektu. Dostęp do tej strony można uzyskać z opcji **Zarządzanie projektem i księgowość** \> **Wszystkie projekty**.

Aby umożliwić korekty, należy włączyć jeden lub więcej stanów transakcji z funkcji **Zarządzanie projektem i księgowość** \> **Zarządzanie projektem i parametry księgowości** na karcie **Ogólne** w obszarze **Zezwalaj na korekty stanu transakcji**. Przykłady stanów transakcji to zaksięgowane transakcje, zafakturowane transakcje lub wykluczone transakcje. Każdy stan transakcji ustawiony na **Nie** będzie miał transakcje w tym stanie, które nie będą widoczne w procesie korekty z możliwością zaznaczenia do korekty.

Opcja konfiguracji o nazwie **Zawsze twórz transakcje korekty** jest obecnie dostępna w Parametrach zarządzania projektami i księgowości. Tę opcję można wyłączyć, aby zaktualizować oryginalną transakcję zamiast utworzenia nowej transakcji podczas korekty w zestawu podrzędnego scenariuszy. Ogłoszono, że parametr ten zostanie ustawiony jako przestarzały dnia 1 marca 2023 r. Po 1 marca 2023 roku system zawsze będzie zachowywać się tak, jakby opcja była włączona.

## <a name="adjustments-process-flow"></a>Przepływ procesów korekty

Poniższe kroki pokazują typowy przepływ przetwarzania korekt.

1. Otwórz stronę **Dostosowania projektu**.
2. Wybierz opcję **Zaznacz**, aby wyszukać transakcje spełniające oczekiwane kryteria korekty.
3. Z listy transakcji wybierz wszystkie transakcje lub podzbiór transakcji do korekty.
4. Wybierz opcję **Dostosuj** i zmodyfikuj atrybuty wiersza. Alternatywnie, jeśli podczas wprowadzania transakcji zostały ręcznie określone wartości, można wybrać opcję wprowadzenia domyślnych wartości systemowych.
5. Lista transakcji zostanie zwrócona, a w kolumnie **Oczekujące na korektę** zostanie wyświetlony znacznik wyboru wskazujący miejsce dokonania zmian. Wszelkie poprawki, które oczekują na zmiany, są wyświetlane w dolnej połowie strony. Można tam wprowadzić dodatkowe szczegółowe zmiany, wykraczające poza to, co przedstawiono na poprzedniej stronie.
6. Wybierz opcję **Księguj**, aby zaksięgować transakcje korekt.

W zależności od konfiguracji dla korekty zwykle są tworzone nowe transakcje.

- Pole **Stan faktury** w oryginalnej transakcji ma wartość **Skorygowane**.
- W celu cofnięcia pierwotnej transakcji jest tworzona transakcja wycofania, a dla pola **Stan** jest ustawiona wartość **Skorygowane**.
- W przypadku nowej transakcji są tworzone zmiany wprowadzone w procesie korekty.

### <a name="selecting-multiple-posted-project-transactions-at-a-time-for-adjustments-and-credit-notes"></a>Wybieranie wielu zaksięgowanych transakcji projektu jednocześnie do korekty i faktur korygujących

Nowa funkcja wprowadzona w wersji 10.0.30 umożliwia wybór wielu transakcji do korekty równocześnie ze strony **Zaksięgowanych transakcji projektu**.

Aby móc używać tej funkcji, musi zostać włączona w systemie. Administratorzy mogą skorzystać z obszaru roboczego **Zarządzanie funkcjami**, aby sprawdzić stan funkcji i ją włączyć, jeśli istnieje taka potrzeba. W obszarze roboczym **Zarządzanie funkcjami** wyszukaj i wybierz z listy **Wielokrotny wybór zaksięgowanych transakcji projektu dla korekt i faktur korygujących**, a następnie wybierz **Włącz teraz**.

Ta funkcja włącza następującą kluczową funkcjonalność:

- Dostęp do niej można uzyskać ze strony opublikowanej w transakcji w projekcie, używając istniejącego przycisku **Korekta**.
- Umożliwia włączenie formantu wyboru wielu wierszy na stronie **Zaksięgowane transakcje projektu**. Przed rozpoczęciem korekty można zastosować filtry do strony listy i wybrać rekordy.
- Przycisk **Korekta** jest wyłączany, jeśli nie można dostosować pojedynczej transakcji lub jeśli zamiast razem zamiast pojedynczo wybierzesz kombinację faktur korekty i arkuszy.
- Z powodu dodania formantu wyboru wielu wierszy łącze **Koszt zatwierdzony** na wstążce nie jest już wyłączone, jeśli zaznaczono wiele wierszy.
- Dodaje następujący komunikat ostrzegawczy: „Wybrano więcej niż (wybrana liczba) rekordów do korekty. Kontynuowanie tej akcji może zająć trochę czasu. Czy na pewno chcesz kontynuować tę akcję?”

Ta funkcja powoduje również usunięcie kroku 2 z przepływu procesu opisanego wcześniej w tym artykule. Z tego powodu wszystkie transakcje wybrane przed otwarciem strony **Dostosowywanie transakcji** zostaną uwzględnione na liście transakcji do korekty. Do ich wyszukania nie trzeba używać przycisku **Wybierz**.

> [!NOTE] 
> Nawet jeśli ta funkcja jest wyłączona, nadal można wybrać wiele rekordów do korekty. *Pozostanie jednak zaznaczony* tylko jeden rekord, co spowoduje, że zostanie wyświetlone okno dialogowe **Wybór transakcji** natychmiast po wybraniu opcji otwarcia korekt.

## <a name="adjustment-transaction-statuses-that-can-be-enabled-or-disabled-for-adjustments"></a>Stany transakcji korekty, które można włączyć lub wyłączyć w celu przeprowadzenia korekty

Na karcie **Ogólne** na stronie **Zarządzanie projektami i parametry księgowe** można włączyć lub wyłączyć następujące stany:

- Zaksięgowany
- Propozycja faktury
- Zafakturowano
- Szacowane
- Wyeliminowane
- Saldo początkowego (godzina)

## <a name="adjustment-parameters"></a>Parametry korekty

Te parametry są wyświetlane na stronie **Zarządzanie projektami i parametrami księgowymi** na karcie **Ogólne** w grupie **Korekta** i będą modyfikować sposób przetwarzania zmian. 

| Nazwa parametru | opis |
|----------------|-------------
| Zawsze twórz transakcje korekty | Jeśli parametr jest włączony, proces korekty zawsze tworzy nową transakcję cofania i nową skorygowaną transakcję, gdy będzie to miało wpływ na finanse lub raportowanie. Jeśli parametr jest wyłączony, proces korekty spowoduje zaktualizowanie oryginalnej transakcji, a nie utworzenie wycofania i nowej transakcji w scenariuszu, np. zaktualizowania tekstu transakcji. |
| Automatycznie aktualizuj pole | Jeśli parametr jest włączony, w systemie będzie przeliczany koszt i cena sprzedaży. |
| Użycie daty korekty jako nowego projektu | Parametr jest używany do przenoszenia transakcji do przyszłych okresów obrachunkowych zanim system obsługiwał tę funkcję. Nie zaleca się używania go, ponieważ zmienia datę biznesową transakcji i będzie przestarzały w przyszłej wersji. |
| Zezwalaj na zamknięte działania | Zwykle nie można tworzyć transakcji dla zamkniętych działań. Jeśli parametr jest włączony, to zachowanie zostanie zastąpione. Z tego powodu można utworzyć korekty dla zamkniętych działań. |
