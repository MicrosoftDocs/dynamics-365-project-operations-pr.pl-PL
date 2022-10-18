---
title: Co nowego, wrzesień 2022 r. — Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu
description: Ten artykuł zawiera informacje o aktualizacjach jakości, które są dostępne w wydaniu z września 2022 r. wdrożenia Microsoft Dynamics 365 Project Operations dla scenariuszy opartych na zasobach/niemagazynowanych.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 04b5f2f8223cdc80028860dd880dde314be244eb
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634819"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Co nowego, wrzesień 2022 r. — Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Ten artykuł dotyczy następujących składników i wersji oprogramowania Microsoft Dynamics 365 Project Operations:

- Project Operations w środowisku Dataverse w wersji 4.46.0.60
- Zarządzanie projektami i księgowość w środowisku Dynamics 365 Finance w wersji 10.0.29

## <a name="features-included-in-this-release"></a>Funkcje uwzględnione w tym wydaniu

| Obszar funkcji | Nazwa funkcji | Więcej informacji |
| --- | --- | --- |
| Zarządzanie szansami sprzedaży | **Poprawki i aktywacja ofert**<br>Project Operations zapewnia pełną pomoc w procesie sprzedaży. Oferty projektu można aktywować w celu reprezentowania stanu, w którym oferta jest tylko do odczytu i jest przeglądana. Aktywowane oferty można poprawić, aby tworzyć nowe oferty z przyrostem numeru poprawki. Aktywowane oferty projektu lub poprawki ofert można zamknąć jako wykorzystane lub utracone. | [Aktywowanie i poprawianie oferty projektu](/dynamics365/project-operations/sales/activation-and-revision) |
| Rozliczenia i ceny | **Domyślne ceny niezależne od strefy czasowej**<br>W programie Project Operations we wszystkich wartościach rzeczywistych projektu wprowadzono pojęcie daty strefy czasowej. Nowe pole o wartościach **Data transakcji** jest teraz dostępne w wierszach i wartościach rzeczywistych i będzie używane do przechowywania daty wystąpienia transakcji, ale bez konwertowania tej daty na Uniwersalny czas koordynowany. Ta data będzie używana w procesach, takich jak domyślne ceny i tworzenie faktury. | <p>[Określanie stawek kosztów dla oszacowań i wartości rzeczywistych projektu](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Określanie kosztów sprzedaży dla oszacowań i wartości rzeczywistych projektu](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Rozliczenia i ceny | **Zastępowanie cen z datą wejścia w życie w Project Operations**<br>Zastąpienia ceny z datą wejścia w życie stanowi sposób zastępowania lub zmieniania określonych cen w cenniku. | [Zastąpienia ceny z datą wejścia w życie](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Podwykonawstwo | **Uzgodnienie faktury od dostawcy i podwykonawcy**<br>Ta funkcja umożliwia klientom tworzenie podumów na potrzeby zakupu czasu zasobu, kategorii wydatków i materiałów używanych podczas prac związanych z projektem. Umożliwia również klientom rejestrowanie w aplikacjach finansowych i operacyjnych faktur od dostawcy, które będą dostępne dla menedżerów projektów na potrzeby weryfikacji Dataverse. | <p>[Zarządzanie podumowami](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Tworzenie faktur od dostawcy](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Czas i wydatek | **Globalna osoba zatwierdzająca**<br>Funkcja ta włącza niezależnych dostawców oprogramowania (ISV) i scentralizowane zatwierdzanie, niezależnie od stanu członków projektu lub zespołu w projekcie. | [Zabezpieczenia i zatwierdzenia](/dynamics365/project-operations/approvals/approvals-security) |
| Zarządzanie wydatkami | **Możliwość wpisu odpowiedzialności za koszty w walucie dostawcy**<br>Ta funkcja umożliwia księgowanie raportów z wydatków w walucie dostawcy za gotówkowe formy płatności. | [Możliwość wpisu odpowiedzialności za koszty w walucie dostawcy](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Zaopatrzenie projektu | **Płatności dla sprzedawców w momencie zapłaty**<br>Ta funkcja umożliwia korzystanie z funkcji Zapłać po uiszczeniu zapłaty (PWP) w środowiskach niemagazynowych Project Operations. Umożliwia zablokowanie/zachowanie płatności od dostawcy na podstawie warunków przechowywania do momentu otrzymania płatności od klienta. | [Płatności dla sprzedawców w momencie zapłaty](/dynamics365/project-operations/procurement/pay-when-paid) |
| Zaopatrzenie projektu | **Zapotrzebowania zakupu dla projektu**<br>Ta funkcja umożliwia użytkownikom tworzenie zamówień zakupu powiązanych z projektami w encji prawnej, dla których funkcja Project Operations w Dynamics 365 Customer Engagement jest włączona. Zamówień zakupu projektu można użyć do zapisu materiałów niemagazynowych, które nie są przechowane przez osobę działu zasobów projektu. Zamówienia zakupu projektu nie są synchronizowane z usługą Dataverse. Jednak można użyć encji wirtualnej, aby znaleźć w wierszach zamówień projektu w Dataverse dla informacji zarządzania projektem. Koszt faktury od dostawcy związany z projektem jest zintegrowany z encją Wartości rzeczywiste projektu w programie Dataverse. Księgowanie projektu jest rejestrowane w księdze podrzędnej projektu za pomocą arkusza integracji Project Operations. | |
|Planowanie i śledzenie projektu|**Używanie interfejsów API harmonogramu projektu do wykonywania operacji na encji planowania** </br> </br>Interfejs API edytowania rozkładu przypisania zasobów umożliwia deweloperom programowe określenie nakładu pracy osoby przypisanej do zadania dla obsługiwanego zakresu dat w celu bardziej szczegółowego planowania nakładów pracy w poszczególnych fazach.|[Używanie interfejsów API harmonogramu projektu do wykonywania operacji na encji planowania](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations — mapy podwójnego zapisu — aktualizacje

W poniższej tabeli przedstawiono mapowania dwurdzeniowe, które zostały zmodyfikowane lub dodane w wersji programu Project Operations z września 2022 r.

| Mapowanie encji | Wersja zaktualizowana | Komentarze |
| -------------- | ------------------- | ------------|
| Wartości rzeczywiste integracji Project Operations (msdyn_actuals) | 1.0.0.15 | To mapowanie obsługuje przetwarzanie wartości rzeczywistych podumowy w Project Operations w scenariuszach opartych na zasobach. |
| Integracja w Project Operations encji eksportu faktury dostawcy projektu (msdyn_projectvendorinvoices) | 1.0.0.2 | To mapowanie obsługuje przetwarzanie wartości rzeczywistych podumowy w Project Operations w scenariuszach opartych na zasobach. |
| Integracja w Project Operations encji eksportu wiersza faktury dostawcy projektu (msdyn_projectvendorinvoicelines) | 1.0.0.5 | To mapowanie obsługuje przetwarzanie wartości rzeczywistych podumowy w Project Operations w scenariuszach opartych na zasobach. |

Zawsze uruchamiaj najnowszą wersję mapy w środowisku i włącz wszystkie mapowania tabel pokrewnych podczas aktualizowania rozwiązania Project Operations Dataverse i wersji rozwiązania Finance. Niektóre funkcje i możliwości mogą nie działać poprawnie, jeśli nie jest aktywowana najnowsza wersja mapy. Aktywną wersję mapy można zobaczyć w kolumnie **Wersja** na stronie **Zapis podwójny**. Aby uaktywnić nową wersję mapy, wybierz **Wersję mapowania tabeli**, a następnie zapisz wybraną wersję po wybraniu najnowszej wersji. Jeśli dostosowałeś domyślną mapę tabeli, zastosuj zmiany ponownie. Więcej informacji: [Zarządzanie cyklem życia aplikacji](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jeśli wystąpi problem z uruchomieniem mapy, postępuj zgodnie z instrukcjami w sekcji [Problem z brakującymi kolumnami tabeli w mapach](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) przewodnika po rozwiązywaniu problemów z podwójnym zapisem.

## <a name="quality-updates"></a>Aktualizacje dotyczące jakości

### <a name="project-operations-on-dataverse"></a>Project Operations w usłudze Dataverse

| Obszar funkcji | Numer referencyjny | Aktualizacja dotycząca jakości |
| --- | --- | --- |
| Rozliczenia i ceny | 2754422 | Szacowanie materiałów i wydatków nie jest przepływem do usługi Finance podczas kopiowania projektów w programie Dataverse. |
| Czas i wydatek | 2787409 | Nieprawidłowa osoba zatwierdzająca może zatwierdzić wpis niezwiązany z projektem. |
| Zarządzanie szansami sprzedaży | 2788907 | Zaktualizowany komunikat o błędzie informujący o sprawdzaniu poprawności unikatowości wierszy zamówienia, które zawierają flagi. |
| Czas i wydatek | 2842253 | Obsługa wyjątków null dla zatwierdzania czasu. |
| Rozliczenia i ceny | 2844181 | Niepowodzenie uzyskania identyfikatorów korelacji blokuje tworzenie faktur. |
| Rozliczenia i ceny | 2876628 | QLD, CLD — rozwiązanie cennika szacowanego powinno używać starszych pól z zakresu dat cennika. |
| Podwykonawstwo | 2893222 | Jeśli dla wiersza podumowy nie zostanie podana żadna rola, należy wybrać ten wiersz w członkach zespołu dla dowolnej roli. |

### <a name="project-management-and-accounting-in-finance"></a>Zarządzanie projektami i księgowanie w Finance

Aby uzyskać informacje dotyczące poprawek usterek zawartych w tej aktualizacji, należy zalogować się do Microsoft Dynamics Lifecycle Services i wyświetlić [artykuł z bazy wiedzy](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funkcje włączone domyślnie w nadchodzącym wydaniu

Poniższa tabela zawiera listę funkcji, które są domyślnie włączone w wersji 10.0.30. Większość funkcji, które zostały włączone, można wyłączyć w [zarządzaniu funkcjami](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). W przyszłości niektóre funkcje, które zostały automatycznie włączone, mogą zostać usunięte z zarządzania funkcjami i stać się obowiązkowe. Zmiana ta zapewnia, że klienci korzystają z aktualnych funkcji, dzięki czemu ulepszenia mogą opierać się na aktualnych funkcjach w miarę ich dodawania. Funkcje nigdy nie będą automatycznie włączane w okresie krótszym niż jeden rok, chyba że zostaną uznane za istotne.

| Nazwa funkcji | Włącz dane | Funkcja dodana | Stan funkcji | Moduł |
| --- | --- | --- |--- |--- |
| Włącz operację asynchronizacji, gdy użytkownik musi przełączać się między operacjami synchronizacji a asynchronizacji | 21 października 2022 | 9 kwietnia 2021 | Domyślnie włączona | Zarządzanie wydatkami |
| Wymagana ocena zasad wydatków pod paragonów | 21 października 2022 | 20 grudnia 2021 roku | Domyślnie włączona | Zarządzanie wydatkami |
| Widok listy raportów o wydatkach utworzonych przez delegowanych pracowników | 21 października 2022 | 19 lutego 2020 roku | Domyślnie włączona | Zarządzanie wydatkami |
| Obliczanie sum przebiegu według roku obrachunkowego | 21 października 2022 | 10 maja 2022 | Domyślnie włączona | Zarządzanie wydatkami |
