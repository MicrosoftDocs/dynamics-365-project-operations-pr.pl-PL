---
title: Ustal koszty projektu i szacowania przychodów
description: Ustalanie kosztów projektu i szacowania przychodów w Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 1652b39b6c8a703bf198a990eb9047eff9dc9f4c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082020"
---
# <a name="determine-project-cost-and-revenue-estimates"></a>Ustal koszty projektu i szacowania przychodów 

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Szacowania projektu zapewniają widok finansowy dla prac oszacowanych i zaplanowanych w strukturze podziału pracy projektu. Widok szacowań informuje Cię o wpływie kosztów i przychodów planowanych prac. Widok szacowań zapewnia narzędzie pozwalające wyświetlić informacje o szeregu wstępnie zdefiniowanych wymiarów, aby najlepiej poinformować o finansowym wpływie projektu.  
  
## <a name="cost-and-sales-value-of-the-project"></a>Koszt i wartość sprzedaży projektu  
Cenniki usług [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] określają stawki kosztów i rachunków dla ról używanych przez projekty. Na podstawie ról związanych z zadaniami w strukturze podziału pracy projektu, możesz określić wpływ kosztów i przychodów na wymagane prace.  
  
## <a name="cost-price-defaulting"></a>Domyślne koszty własne  
Każdy projekt należy do organizacji (wskazane w **Jednostka będąca właścicielem** w projekcie). Cennik skojarzony z jednostką będącą właścicielem określa jednostkowy koszt własny. [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] określa koszty własne dla ról dzięki wyszukiwaniu kombinacji roli, jednostki i jednostki organizacyjnej na liście kosztów własnych, aby uzyskać właściwy koszt własny dla daty obowiązującej na wierszach szacowania.  
  
Jeśli kombinacja roli, jednostki. i jednostki organizacyjnej, nie skutkuje kosztem własnym z cennika należącego do właściciela jednostki, jednostka nie jest uwzględniana na rzecz połączenia roli i jednostki organizacyjnej. W przypadku kosztu własnego cena ta jest konwertowana do jednostki wybranej w wierszu szacowania.  
  
Jeżeli kombinacja roli i jednostki organizacyjnej nie skutkuje kosztem własnym, jednostka organizacyjna nie jest uwzględniana na rzecz kombinacji roli i jednostki, a cena jest ustawiana domyślnie po zastosowaniu dowolnej konwersji, jeśli jest to wymagane.  
  
 Jeśli nie ma ceny dla roli, koszt własny w wierszu szacowanie wynosi domyślnie 0,00.  
  
 Wszystkie kwoty sumowane w wierszach szacowania kosztów projektu są wyrażone w walucie jednostki organizacyjnej będącej właścicielem.  
  
## <a name="sales-price-defaulting"></a>Domyślne ceny sprzedaży  
Cennik sprzedaży bazuje na encji sprzedaży do której dołączony jest projekt. Cennik sprzedaży skojarzony z ofertą lub umową określa jednostkową cenę sprzedaży. Jeśli oferta lub umowa posiadają cennik niestandardowy, będzie to domyślny cennik sprzedaży dla oszacowań projektu. Jeśli nie ma skojarzenia z encjami sprzedaży, domyślny cennik sprzedaży skonfigurowany w ustawieniach parametrów będzie domyślnym cennikiem sprzedaży dla projektu. Każdy wiersz szacowania jest skojarzony z jednostką organizacyjną zasobu, aby wskazać jednostkę organizacyjną, z której zasoby będą rezerwowane w celu realizacji tego zadania. Cena sprzedaży dla skojarzonych ról jest określana przez wyszukiwanie kombinacji roli, jednostki i jednostki organizacyjnej zasobu w cenniku sprzedaży, aby uzyskać właściwą cenę sprzedaży dla daty wprowadzenia w wierszach szacowania.  
  
Jeżeli kombinacja roli, jednostki i jednostki organizacyjnej zasobów nie skutkuje ceną sprzedaży z cennika sprzedaży, system zignoruje jednostkę i poszuka kombinacji roli i jednostki organizacyjnej zasobów. Jeśli znaleziona zostaje cena sprzedaży, zostanie ona przekonwertowana do jednostki wybranej w wierszu szacowania sprzedaży.  
  
Jeśli system nie znajdzie ceny dla roli, cena sprzedaży musi wynosić domyślnie 0,00 w wierszu szacowania.  
  
Widok szacunków ma widok siatki wyświetlający płaską siatkę wierszy szacowania z jednostką i całkowitym kosztem i ceną sprzedaży.  
  
## <a name="time-phased-view-of-project-estimates"></a>Widok faz czasowych oszacowań projektu  
W widoku faz czasowych oszacowań projektu dane szacunkowe z widoku siatki są obracane domyślnie przez rolę i ukazują rozkład danych szacowania dla całej osi czasu w wybranej skali czasu.  
  
## <a name="effort-estimate-allocation-based-on-task-mode"></a>Alokacja szacowania nakładu pracy w oparciu o tryb zadania  
W widoku faz czasowych całkowity nakład pracy szacowany dla zadania jest rozkładany przez przydzielenie określonej liczby godzin nakładu pracy na jednostkowy okres czasu wybranej skali czasu. W rozwiązaniu Project Service tryb zadania określa sposób alokacji wysiłku przez czas trwania zadania. Dwa rodzaje alokacji to alokacja równomierna oraz alokacja w oparciu o godziny pracy  
  
## <a name="work-hours-based-allocation"></a>Alokacja w oparciu o godziny pracy  
Tryb automatycznego planowania zadań dla zadania reguluje, że dla liczby zasobów szacowanych dla zadania, szacuje się wykorzystanie ich w czasie pełnych godzin pracy w ciągu dnia. Obowiązuje podczas przydzielania nakładu pracy z rozłożeniem go na czasie trwania zadania również w widoku faz czasowych. Na przykład na skali czasowej "Dzień" dla zadania oszacowanego do zrealizowania przez jeden zasób, nakład pracy przydzielony na dzień nie przekroczy godzin pracy dla tego dnia określonych w kalendarzu projektu. W związku z tym przydział nakładu pracy zawsze gwarantuje, że zasoby zostaną wykorzystane w ciągu pełnego dnia.  
  
## <a name="even-distribution"></a>Równomierna dystrybucja  
Ręcznie zaplanowany tryb zadania nie honoruje godzin pracy, kalendarza projektu ani liczby zasobów określonych dla zadania. Harmonogram zadania bazuje na danych wprowadzonych przez użytkownika. W przypadku tego typu zadań rozdział nakładu pracy na jednostkowy okres czasu wybranej skali czasu nie ma żadnych czynników ograniczających. Całkowity nakład pracy dla zadania jest rozdzielony równomiernie i przydzielony dla każdego jednostkowego okresu czasu na wybranej skali czasu.  
  
W ten sposób tryb zadania określony dla zadania określa rozkład nakładu pracy lub przydział nakładu pracy na jednostkowy okres czasu w szacunkach faz czasowych.  
  
## <a name="grouping-and-time-phasing-options"></a>Opcje grupowania i faz czasowych  
Ten widok pomaga zrozumieć rozkład nakładu pracy, kosztów i szacunków sprzedaży dla dnia, tygodnia, miesiąca lub roku. Opcja Grupuj według pozwala na przestawianie danych szacunkowych w dwóch wymiarach: Kategoria i Zasób. Zarówno w widoku siatki jak i w widoku faz czasowych możesz wybrać pola, które będą wyświetlane. Sumy dla każdego bloku czasu są wyświetlane u dołu, i ukazują całkowity szacunkowy nakład pracy, koszt. i sprzedaż na dzień, tydzień, miesiąc lub rok.  
  
Domyślny koszt oraz cena sprzedaży obowiązują dla dat — kiedy wielkości dla ról zmienią się, będzie to lepiej widoczne w widoku faz czasowych podczas przeglądania danych szacunkowych dla "Zasób" i tygodniowej fazy czasowej.  
  
## <a name="expense-estimates"></a>Szacowanie wydatków  
Wszelkie wydatki, które zostaną poniesione w projekcie, a które nie są bezpośrednio związane z wydatkami na pracę, mogą być rejestrowane w szacunkach projektu w widoku siatki. Można to zrobić za pomocą opcji **Dodaj szacowanie wydatków** w widoku siatki. Szacunki wydatków można rejestrować dla określonego zadania lub dla całego projektu; można wybrać kategorie wydatków w tych wierszach i wybrać wstępną datę, kiedy to przewidywane jest poniesienie tych wydatków. Jeśli na liście kosztów i w cenniku sprzedaży znajdują się ceny domyślne, lub wartości procentowe narzutu zdefiniowane dla kategorii wydatków, zostaną one przedstawione w wierszu szacowania jako domyślne.  
  
### <a name="see-also"></a>Zobacz także  
 [Przewodnik menedżera projektu](../psa/project-manager-guide.md)
