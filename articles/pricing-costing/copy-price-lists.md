---
title: Kopiowanie cenników
description: W tym artykule zamieszczono informacje dotyczące sposobu kopiowania cenników w aplikacji Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3fce3a362fe6326e362c3f77054c10281a9c146c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921177"
---
# <a name="copy-price-lists"></a>Kopiowanie cenników

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

W rozwiązaniu Dynamics 365 Project Operations można tworzyć kopie cenników. Na przykład można utworzyć cenniki dla nadchodzącego roku, korzystając z cennika z bieżącego roku.  Istnieje również możliwość skopiowania cennika stawek rozliczania i cen sprzedaży z cenników dla kosztu. 

Aby utworzyć kopię cennika, należy wykonać następujące kroki.

1. Otwórz cennik, dla którego chcesz utworzyć kopię programu, a następnie wybierz pozycję **Kopiuj**.
2. Wprowadź niezbędne informacje, aby skopiować cennik. W poniższej tabeli przedstawiono kwestie, o których warto pamiętać przy wprowadzaniu informacji.

| Pole | Opis | Wpływ zmian w dalszych etapach |
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

1. Na kartach **Cennik**, **Kategoria** i **Pozycja cennika** można wybrać opcję **Uaktualnij ceny**, aby zastosować adiustację dla wszystkich cen w podsiatce. 
2. W otwartym oknie dialogowym, wprowadź narzut. Istnieje również możliwość wprowadzenia ujemnego narzutu procentowego w celu obniżenia cen o daną wartość procentową. 
3. Na stronie dialogu wybierz przycisk **OK**, a następnie sprawdź, czy ceny w podsiatce odzwierciedlają wprowadzone zmiany.


[!INCLUDE[footer-include](../includes/footer-banner.md)]