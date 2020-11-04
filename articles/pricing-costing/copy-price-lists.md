---
title: Kopiowanie cenników
description: Ten temat zawiera informacje na temat kopiowania cenników produktów w Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 91ee798a206ea5200780c8ebafc8f99cd9a3e219
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082051"
---
# <a name="copy-price-lists"></a>Kopiowanie cenników

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Użytkownik może tworzyć kopie cenników w Dynamics 365 Project Operations. Na przykład można utworzyć cenniki dla nadchodzącego roku, korzystając z cennika z bieżącego roku.  Istnieje również możliwość skopiowania cennika stawek rozliczania i cen sprzedaży z cenników dla kosztu. 

Aby utworzyć kopię cennika, należy wykonać następujące kroki.

1. Otwórz cennik, dla którego chcesz utworzyć kopię programu, a następnie wybierz pozycję **Kopiuj**.
2. Wprowadź niezbędne informacje, aby skopiować cennik. W poniższej tabeli przedstawiono kwestie, o których warto pamiętać przy wprowadzaniu informacji.

| Pole | Stopień zgodności, cel i wskazówki | Wpływ zmian w dalszych etapach |
| --- | --- | --- |
| Nazwa/nazwisko | Nazwa cennika źródłowego z dołączonym oznaczeniem **-kopia**. | Cennik zawiera tę wartość na wszystkich stronach list oraz w opcjach rozwijanych. |
| Kontekst | Wprowadź kontekst, który ma być cennikiem docelowym. | Cennik z ustawionym zestawieniem **Kosztów** jest używany do wyszukiwania ceny w oszacowaniach kosztów i kosztach rzeczywistych. Cennik z ustawionym zestawieniem **Sprzedaży** jest używany do wyszukiwania ceny w oszacowaniach sprzedaży i rzeczywistych wartościach sprzedaży. Tylko cenniki z ustawionym kontekstem **Sprzedaż** mogą być dołączane do cennika dla klienta, oferty lub kontraktu. |
| Data rozpoczęcia | Data rozpoczęcia okresu, w którym znajduje się cennik, obowiązuje. | Wraz z **Datą końcową** to pole jest używane w celu określenia cennika, który ma zastosowanie do określonego oszacowania lub konkretnego wiersza. |
| Data zakończenia | Data zakończenia okresu, w którym znajduje się cennik, obowiązuje. | Wraz z **Datą rozpoczęcia** to pole jest używane w celu określenia cennika, który ma zastosowanie do określonego oszacowania lub konkretnego wiersza. |
| Waluta | Waluta w cenniku źródłowym. Można to zmienić. | Po zmianie wszystkie powstające ceny dotyczące wykonanej pracy, wydatków i katalogu produktów są przeliczane na walutę docelową cennika podczas kopiowania. |
| Jednostka czasu | Waluta w cenniku źródłowym. Można to zmienić. | Po zmianie wszystkie powstające ceny dotyczące wykonanej pracy są przeliczane na walutę docelową jednostki cennika podczas kopiowania. Zastosowana jest konwersja z jednostki skonfigurowanej dla jednostki czasu w cenniku źródłowym i jednostki czasu w cenniku docelowym. |
| Opis | Opis cennika źródłowego z dołączonym oznaczeniem **-kopia**. Jest to pole tekstowe umożliwiające wyświetlanie wielowierszowego opisu cennika. | To pole jest wyświetlane w widokach **Skojarzonych** z cennikiem w różnych encjach, w których znajdują się pokrewne cenniki. |

3. Zapisz cennik. 

## <a name="update-a-price-list-by-applying-a-mark-up-to-all-the-prices"></a>Aktualizowanie cennika po zastosowaniu narzutu do wszystkich cen

1. Na kartach **Rola** , **Kategoria** i **Pozycja cennika** można wybrać opcję **Aktualizuj ceny** , aby zastosować narzut dla wszystkich cen w podsiatce. 
2. W otwartym oknie dialogowym, wprowadź narzut. Istnieje również możliwość wprowadzenia ujemnego narzutu procentowego w celu obniżenia cen o daną wartość procentową. 
3. Wybierz **OK** na stronie dialogowej, a następnie sprawdź, czy ceny w podsiatce odzwierciedlają wprowadzone zmiany.
