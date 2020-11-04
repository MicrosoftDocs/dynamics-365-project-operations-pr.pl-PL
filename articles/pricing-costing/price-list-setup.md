---
title: Konfigurowanie cenników
description: Ten temat zawiera informacje na temat konfiguracji cenników kosztów i sprzedaży.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 578f5641659a5d05785781afe7055fe4449cf799
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088048"
---
# <a name="set-up-price-lists"></a>Konfigurowanie cenników

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Cenniki w Dynamics 365 Project Operations są odzwierciedleniem katalogu stawek. Stawki wyrażają koszty, sprzedaż i stawki rozliczeń. W zależności od tego, czy cennik zawiera stawki kosztów lub stawki sprzedaży i stawki rozliczeń, kontekstem cennika jest **Sprzedaż** lub **Koszt**.

Poniższe rozszerzenia są specyficzne dla Project Operations i są stosowane do cenników z Dynamics 365 Sales.

- **Kontekst** : w tym polu są obsługiwane wartości **Koszt** i **Sprzedaż**. Wartość **Zakup** jest nieobsługiwana. Ustaw kontekst na **Koszt** , co spowoduje stworzenie listy kosztów własnych lub ustaw kontekst na **Sprzedaż** , aby stworzyć cennik sprzedaży. Listy kosztów własnych służą do rozróżniania ceny według typu kosztu na rekordach szacunkowych i rzeczywistych. Cenniki sprzedaży służą do rozpoznawania ceny na oszacowanych i rzeczywistych rekordach typów sprzedaży niezafakturowanych i rozliczonych.
- **Jednostka czasu** : jest to domyślna jednostka czasu, dla której jest ustawiana cena w pokrewnej tabeli **Cena roli** dla danego cennika.
- **Encja cennika** : w tym ukrytym polu Project Operations dokonuje rozróżniania cenników, które są ofertami lub kontraktami, od tych, które są stosowane w sposób standardowy i globalny.

## <a name="price-list-header"></a>Nagłówek cennika

Poniższa tabela zawiera pola na karcie **Ogólne** cennika, które są unikatowe dla Project Operations lub mogą mieć znaczące zmiany w zachowaniu w stosunku do cenników z Sales.

| Pole | Lokalizacja | Stopień zgodności, cel i wskazówki | Wpływ zmian w dalszych etapach |
| --- | --- | --- | --- |
| Nazwa/nazwisko | Karta **Ogólne** i formularze **Szybkie tworzenie** | Tożsamość cennika. | Cennik jest wyświetlany wraz z wartością na wszystkich stronach list oraz w opcjach rozwijanych.|
| Kontekst | Karta **Ogólne** i formularze **Szybkie tworzenie** | To pole można ustawić jako **Koszt** lub **Sprzedaż**. | Cennik ustawiony na **Koszt** jest używany do wyszukiwania ceny w oszacowaniach kosztów i kosztach rzeczywistych. Cennik ustawiony na **Sprzedaż** jest używany do wyszukiwania ceny w oszacowaniach sprzedaży i wartościach rzeczywistych sprzedaży. Tylko cenniki z ustawionym kontekstem na **Sprzedaż** mogą być dołączane do cenników dla klienta, oferty lub kontraktu projektu. |
| Data rozpoczęcia | Karta **Ogólne** i formularze **Szybkie tworzenie** | Data rozpoczęcia okresu, w którym znajduje się cennik, obowiązuje. | Wraz z polem **Data końcowa** to pole jest używane w celu określenia cennika, który ma zastosowanie do określonego oszacowania lub konkretnego wiersza. |
| Data zakończenia | Karta **Ogólne** i formularze **Szybkie tworzenie** | Data zakończenia okresu, w którym znajduje się cennik, obowiązuje. | Wraz z polem **Data startowa** to pole jest używane w celu określenia cennika, który ma zastosowanie do określonego oszacowania lub konkretnego wiersza. |
| Waluta | Karta **Ogólne** i formularze **Szybkie tworzenie** | To pole jest używane jako domyślna waluta w poszczególnych wierszach roli, kategorii lub cennika powiązanych z tym cennikiem. | Nie można tworzyć cenników, roli, kategorii lub wierszy pozycji cennika w **Sprzedaży** w walutach innych niż podana waluta. W przypadku cenników **Koszt** można utworzyć wiersz ceny roli w dowolnej walucie. Waluta zdefiniowana w tym miejscu jest używana jako domyślna. Zależne od konfiguracji użytkownika ceny ról mogą zastąpić tę wartość w celu włączenia konfiguracji stawki kosztów pracy w dowolnej walucie. Stawki kosztów kategorii i koszty pozycji cennika można skonfigurować wyłącznie w walucie zdefiniowanej w tym miejscu. |
| Jednostka czasu | Karta **Ogólne** i formularze **Szybkie tworzenie** | To pole jest używane jako domyślna jednostka czasu w poszczególnych wierszach roli cennika. | Ta wartość pola jest używana tylko w pokrewnych ustawieniach cen ról. W przypadku cenników **Koszt** oraz **Sprzedaż** można utworzyć wiersz ceny w dowolnej jednostce czasu. Jednostka czasu zdefiniowana w tym miejscu jest używana jako domyślna. Zależne od konfiguracji użytkownika ceny ról mogą zastąpić tę wartość w celu włączenia konfiguracji stawki kosztów pracy i rozliczania w dowolnej jednostce czasu. |
| Opis | Karta **Ogólne** i formularze **Szybkie tworzenie** | Jest to pole tekstowe umożliwiające wyświetlanie wielowierszowego opisu cennika. | To pole jest wyświetlane w widokach **Skojarzonych** z cennikiem w różnych encjach, w których znajdują się pokrewne cenniki. |
