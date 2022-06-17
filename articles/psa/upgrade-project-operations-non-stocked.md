---
title: Uaktualnianie rozwiązania Project Service Automation do Project Operations
description: Ten artykuł zawiera omówienie procesu uaktualniania z aplikacji Microsoft Dynamics 365 Project Service Automation do Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/13/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 30eb02240de6617d4c550ce59db2a454eee36f5b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912989"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Uaktualnianie rozwiązania Project Service Automation do Project Operations

Z przyjemnością ogłaszamy rozpoczęcie pierwszej z trzech faz uaktualnienia z aplikacji Microsoft Dynamics 365 Project Service Automation do Dynamics 365 Project Operations. Ten artykuł zawiera przegląd procesu dla klientów, którzy chcą rozpocząć tę ekscytującą podróż. Przyszłe artykuły będą zawierać zagadnienia dla deweloperów i szczegółowe informacje na temat ulepszeń funkcji. Będą nie tylko zawierać wskazówki pomocne przy przygotowywaniu do uaktualnienia do wersji Project Operations, ale także wyjaśnienia, czego można się spodziewać po uaktualnieniu.

Program dostarczania uaktualnienia zostanie podzielony na trzy fazy.

| Dostarczanie uaktualnienia | Faza 1 (styczeń 2022 r.) | Faza 2 (kwiecień 2022 r) | Faza 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Brak zależności od struktury podziału pracy (WBS) dla projektów | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| SPP w ramach obsługiwanych obecnie limitów aplikacji Project Operations | | :heavy_check_mark: | :heavy_check_mark: |
| SPP poza obsługiwanymi obecnie limitami aplikacji Project Operations, w tym obsługa funkcji Project Desktop Client | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Funkcje procesu uaktualniania 

W ramach procesu uaktualniania do mapy witryny dodano dzienniki uaktualnienia, aby administratorzy mogli łatwiej diagnozować błędy. Oprócz nowego interfejsu zostaną dodane nowe reguły walidacji, które zapewnią integralność danych po uaktualnieniu. Do procesu uaktualniania zostaną dodane następujące walidacje.

| Walidacje | Faza 1 (styczeń 2022 r.) | Faza 2 (kwiecień 2022 r) | Faza 3  |
|-------------|------------------------|---------------------------|---------------------------|
| SPP zostanie sprawdzona pod kątem typowych naruszeń integralności danych (na przykład przypisania zasobów skojarzone z tym samym zadaniem nadrzędnym, ale które mają różne projekty nadrzędne). | | :heavy_check_mark: | :heavy_check_mark: |
| SPP zostanie sprawdzona pod kątem [znanych limitów rozwiązania Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| SPP zostanie sprawdzona pod kątem znanych limitów rozwiązania Project Desktop Client. | |  | :heavy_check_mark: |
| Możliwe do rezerwacji zasoby i kalendarze projektów będą sprawdzane pod kątem typowych wyjątków polegających na niezgodności z regułami kalendarza. | | :heavy_check_mark: | :heavy_check_mark: |

W fazie 2. projekty klientów, którzy uaktualnią aplikację do wersji Project Operations, zostaną uaktualnione do środowiska tylko do odczytu na potrzeby planowania projektów. W tym środowisku tylko do odczytu pełna SPP będzie widoczna w siatce śledzenia. Aby edytować SPP, menedżerowie projektów mogą wybrać pozycję **Konwertuj** na głównej stronie **Projekty**. Proces w tle zaktualizuje projekt w taki sposób, aby go obsługiwał nowe funkcje planowania projektów z rozwiązania Project for the Web. Ta faza jest odpowiednia dla klientów, którzy mają projekty mieszczące się w znanych limitach rozwiązania [Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

W fazie 3. zostanie dodana obsługa rozwiązania Project Desktop Client z korzyścią dla klientów, którzy chcą nadal edytować swoje projekty z tej aplikacji. Jednak jeśli istniejące projekty zostaną przekonwertowane na nowe środowisko Project for the Web, dostęp do dodatku będzie wyłączony dla każdego przekonwertowanego projektu.

## <a name="prerequisites"></a>Wymagania wstępne

Aby zakwalifikować się do 1. fazy uaktualnienia, klient musi spełniać następujące kryteria:

- Środowisko docelowe nie może zawierać żadnych rekordów w encji **msdyn_projecttask**.
- Prawidłowe licencje aplikacji Project Operations muszą być przypisane do wszystkich aktywnych użytkowników klienta. 
- Klient musi zweryfikować procesu uaktualniania w co najmniej jednym środowisku nieprodukcyjnym, w którym znajduje się reprezentatywny zestaw danych dopasowany do danych produkcyjnych.
- Środowisko docelowe należy zaktualizować do wersji Project Service Automation Update Release 41 (3.10.62.162) lub nowszej.

Wymagania wstępne dla faz 2. i 3. będą aktualizowane w miarę zbliżania się dat ogólnej dostępności.

## <a name="licensing"></a>Licencjonowanie

Jeśli masz aktywne licencje aplikacji Project Service Automation, możesz zainstalować i stosować aplikację Project Operations, która oferuje wszystkie funkcje aplikacji Project Service Automation i inne. W ten sposób można przetestować możliwości aplikacji Project Operations, nadal używając aplikacji Project Service Automation w środowisku produkcyjnym. Po wygaśnięciu licencji rozwiązania Project Service Automation musisz przejść do aplikacji Project Operations. Planując to przejście, trzeba pamiętać o tym, że licencja aplikacji Project Operations nie obejmuje licencji aplikacji Project Service Automation.

## <a name="testing-and-refactoring-customizations"></a>Testowanie i refaktoryzowanie dostosowań

Jako punkt początkowy zaimportuj wszystkie dostosowania do środowiska czystego środowiska Project Operations (w wersji uproszczonej) w celu potwierdzenia, że import zakończył się pomyślnie i że operacje biznesowe działają zgodnie z oczekiwaniami.

Oto zagadnienia, które należy obserwować:

- Importowanie może się nie powieść z powodu brakujących zależności. Innymi słowy, dostosowania odwołują się do pól lub innych składników, które zostały usunięte w aplikacji Project Operations. W tym przypadku należy usunąć te zależności ze środowiska developmentu.
- Jeśli rozwiązania zarządzane i niezarządzane zawierają składniki, które nie są dostosowane, należy je usunąć z rozwiązania. Na przykład podczas dostosowywania encji **Projekt** należy dodać do rozwiązania tylko nagłówek encji. Nie dodawaj wszystkich pól. Jeśli wszystkie składniki zostały wcześniej dodane, może być konieczne ręczne utworzenie nowego rozwiązania i dodanie do niego odpowiednich składników.
- Formularze i widoki mogą nie być wyświetlane zgodnie z oczekiwaniami. W pewnych okolicznościach dostosowanie gotowych formularzy lub widoków może uniemożliwić stosowanie nowych aktualizacji w aplikacji Project Operations. W celu zidentyfikowania tych problemów zaleca się dokładne czystej instalacji aplikacji Project Operations i instalacji aplikacji Project Operations z dostosowaniami. Porównaj formularze najczęściej używane w firmie, aby upewnić się, że wersja formularza nadal ma sens i nie brakuje w niej niczego z czystej wersji formularza. Wykonaj ten sam typ przeglądania strona po stronie dla wszystkich dostosowanych widoków.
- Logika biznesowa może nie działać w czasie wykonywania. Ponieważ odwołania do pól w dodatkach nie są weryfikowane podczas importowania, logika biznesowa może nie zadziałać z powodu odwołań do pól, które już nie istnieją, i może zostać wyświetlony komunikat o błędzie przypominający następujący przykład: „Encja <Projekt> nie zawiera atrybutu Name = „msdyn_plannedhours” ani NameMapping = „Logiczne”. W tym przypadku należy zmodyfikować dostosowania, tak aby wykorzystywały nowe pola. Jeśli w logice dodatku są automatycznie generowane klasy serwera proxy i silne odwołania do typów, rozważ ponowne wygenerowanie tych serwerów proxy z czystej instalacji. W ten sposób można łatwo zidentyfikować wszystkie miejsca, w których dodatki są zależne od przestarzałych pól.

Po zaktualizowaniu dostosowań w celu czystego zaimportowania aplikacji Project Operations przejdź do kolejnych kroków.

## <a name="end-to-end-testing-in-development-environments"></a>Testowanie end-to-end w środowiskach programistycznych

### <a name="initiate-upgrade"></a>Zainicjowanie uaktualnienia 

1. W centrum administracyjnym Power Platform znajdź i wybierz środowisko. Następnie w aplikacjach znajdź i wybierz pozycję **Dynamics 365 Project Operations**.
2. Wybierz pozycję **Zainstaluj**, aby zacząć uaktualnianie. Centrum administracyjne platformy Power Platform przedstawi tę instalację jako nową instalację. Zostanie jednak wykryta obecność wcześniejszej wersji rozwiązania Project Service Automation i istniejąca instalacja zostanie uaktualniona.

    Po zakończeniu uaktualniania środowisko powinno pokazywać zainstalowaną aplikację Project Operations oraz brak zainstalowanej aplikacji Project Service Automation.

    > [!NOTE]
    > W zależności od ilości danych w środowisku uaktualnienie może zająć kilka godzin. Podstawowy zespół zarządzający uaktualnieniem powinien odpowiednio zaplanować i uruchomić uaktualnienie poza godzinami pracy. W niektórych przypadkach, jeśli ilość danych jest duża, uaktualnienie należy przeprowadzić w weekend. Decyzja o planowaniu powinna być oparta na wynikach testowania w środowiskach na niższym poziomie.

3. Uaktualnij odpowiednio rozwiązania niestandardowe. W tym momencie należy wdrożyć wszystkie zmiany wprowadzone w dostosowaniach w sekcji [Testowanie i refaktoryzowanie dostosowań](#testing-and-refactoring-customizations) tego artykułu.
4. Przejdź do pozycji **Ustawienia** \> **Rozwiązania** i wybierz opcję odinstalowania rozwiązania **Przestarzałe składniki aplikacji Project Operations**.

    To rozwiązanie jest rozwiązaniem tymczasowym, które zawiera istniejący model danych i składniki obecne podczas uaktualnienia. Usunięcie tego rozwiązania powoduje usunięcie wszystkich pól i składników, które nie są już używane. Pozwala to uprościć interfejs oraz ułatwić integrację i stosowanie rozszerzeń.
    
### <a name="validate-common-scenarios"></a>Sprawdź poprawność typowych scenariuszy

Po zweryfikowaniu określonych dostosowań zaleca się przejrzenie procesów biznesowych obsługiwanych w aplikacjach. Te procesy biznesowe obejmują między innymi tworzenie encji sprzedaży, takich jak oferty i kontrakty, oraz tworzenie projektów takich jak WBS i zatwierdzenie wartości rzeczywistych.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Główne zmiany między aplikacjami Project Service Automation i Project Operations

W tej sekcji przedstawiono podsumowanie głównych zmian, których można między aplikacjami między Project Service Automation i Project Operations.

### <a name="project-planning"></a>Planowanie projektu

Funkcje planowania projektów w aplikacji Project Operations nie są już zależne od kombinacji logiki po stronie klienta i logiki po stronie serwera. W zamian aplikacja Project Operations używa rozwiązania Project for the Web jako aparatu planowania. Ta zmiana funkcji planowania umożliwia korzystanie z kilku nowych funkcji, takich jak widoki Tablica i Gantt, planowanie na podstawie zasobów, [pozycje listy kontrolnej zadań](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) i tryby planowania projektów. Nowe funkcje planowania są również obsługiwane przez bogaty zestaw nowych [interfejsów programowania aplikacji (API)](../project-management/schedule-api-preview.md). Te interfejsy API mają zagwarantować, że żadna programowa operacja tworzenia, aktualizowania lub usuwania encji w SPP nie uszkodzi pól obliczanych w harmonogramie.

## <a name="billing-and-pricing"></a>Rozliczenia i ceny

W ramach ciągłych inwestycji w aplikację Project Operations w obszarach rozliczeń i cen jest dostępnych kilka nowych funkcji. Oto kilka przykładów:

- [Rejestrowanie użycia materiałów w projektach i zadaniach projektów](../material/material-usage-log.md)
- [Zarządzanie podumowami](../pro/subcontracting/managing-subcontracts-overview.md)
- [Kontrakty oparte na zaliczkach i zatrzymaniach](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Kontraktowanie nieprzekraczalnego stanu i weryfikacji](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Rozliczenia oparte na zadaniach

## <a name="frequently-asked-questions"></a>Często zadawane pytania

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Jakie typy wdrożeń są obecnie obsługiwane przez proces uaktualnienia?

| Lokalizacja źródłowa                                                 | Target                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Automatyzacja usługi projektów                             | Wdrożenie aplikacji Project Operations w wersji uproszczonej                        | Obsługiwane               |
| Zarządzanie projektami i księgowość w Dynamics 365 Finance | Wdrożenie aplikacji Project Operations w wersji uproszczonej                        | Obecnie nieobsługiwane |
| Zarządzanie projektami i księgowanie w aplikacji Finance              | Project Operations — zasoby / scenariusze nieobejmujące magazynowania     | Obecnie nieobsługiwane |
| Project Service Automation 3.x                         | Project Operations — zasoby / scenariusze nieobejmujące magazynowania     | Obecnie nieobsługiwane |
| Project for the Web (środowisko dedykowane)            | Wdrożenie aplikacji Project Operations w wersji uproszczonej                        | Obecnie nieobsługiwane |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Jak mogę zainstalować aplikację Project Operations przed udostępnieniem narzędzi do uaktualniania?

Przed udostępnienie narzędzi do uaktualniania można zainstalować aplikację Project Operations na dwa sposoby:

- Ustanowienie nowego środowiska.
- Wdrożenie aplikacji Project Operations oddzielnie w dowolnej organizacji sprzedaży, w której nie ma aplikacji Project Service Automation.

> [!NOTE]
> Jeśli aplikacja Project Service Automation została zainstalowana w organizacji, ale nie jest używana, można ją odinstalować. Po całkowitym usunięciu aplikacji Project Service Automation aplikację Project Operations można zainstalować w tej samej organizacji.
