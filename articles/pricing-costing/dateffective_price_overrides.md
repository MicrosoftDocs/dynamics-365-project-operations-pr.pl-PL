---
title: Zastąpienia ceny z datą wejścia w życie
description: W tym artykule wyjaśniono, jak skonfigurować zastąpienia cen dla określonych cen w cenniku.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 41af5176c0809c9621fc0fa946a04492da7d152b
ms.sourcegitcommit: 37293b0b28f072deafc00112ddbbea91c48a7802
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/08/2022
ms.locfileid: "9445976"
---
# <a name="date-effective-price-overrides"></a>Zastąpienia ceny z datą wejścia w życie 

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

*Zastąpienia ceny z datą wejścia w życie* stanowi sposób zastępowania lub zmieniania określonych cen w cenniku. Na przykład cennik standardowy obowiązuje od 1 stycznia 2022 r. do 31 grudnia 2022 r. Cennik ma ceny wielu ról. Cena skonfigurowania dla roli **Technik sieciowy** wynosi 100 dolarów (USD) za godzinę. Kiedy technik sieciowy rejestruje czas między 1 stycznia 2022 r. a 31 grudnia 2022 r., godzina jest wyceniona na 100 USD. 1 października 2022 r. trzeba dostosować cenę *tylko* dla roli **Technik sieciowy** ze 100 USD za godzinę do 110 USD za godzinę. Funkcja **Zastąpienia ceny z datą wejścia w życie** umożliwia skonfigurowanie tej zmiany jako zastąpienia wiersza dla danej ceny roli. Dlatego nie trzeba kopiować całego cennika ani zmieniać ceny tego wiersza.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Zastąpienia ceny z datą wejścia w życie dla cen robocizny

Proces konfigurowania zastąpień ceny z datą wejścia w życie dla cen robocizny w projekcie składa się z dwóch podstawowych kroków.

1. Włączenie funkcji **Zastąpienia ceny z datą wejścia w życie**.
1. Konfigurowanie zastąpienia ceny z datą wejścia w życie.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Włączenie funkcji Zastąpienia ceny z datą wejścia w życie

> [!NOTE]
> Po włączeniu funkcji **Zastąpienia ceny z datą wejścia w życie** nie można jej wyłączyć.

Aby włączyć funkcję **Zastąpienia ceny z datą wejścia w życie**, wykonaj następujące kroki.

1. Przejdź do pozycji **Ustawienia** \> **Parametry**.
1. Otwórz rekord **Parametry**.
1. W okienku Akcje na karcie **Kontrola funkcji** wybierz **Włącz zastąpienia ceny z datą wejścia w życie**.
1. W oknie dialogowym z monitem o potwierdzenie wybierz **OK**.
1. Po kilku chwilach odśwież przeglądarkę. Funkcje zastępowania ceny z datą wejścia w życie powinny być teraz dostępne. Zobaczysz, że te funkcje zostały włączone, jeśli przycisk **Włącz zastąpienia ceny z datą wejścia w życie** nie jest już wyświetlany w okienku akcji.

### <a name="set-up-a-date-effective-price-override"></a>Konfigurowanie zastąpienia ceny z datą wejścia w życie

Zastąpienia ceny z datą wejścia w życie można skonfigurować w cennikach **Koszt**, **Sprzedaż** lub **Zakup**.

> [!NOTE]
>Zachowanie funkcji **Zastąpienia ceny z datą wejścia w życie** jest obecnie ograniczone w następujący sposób:
>
> - Tylko ceny ról i narzuty cenowe ról obsługują funkcję **Zastąpienia ceny z datą wejścia w życie** w Project Operations.
> - Podczas kopiowania cennika za pomocą akcji **Kopiuj** na stronie **Szczegóły cennika** oraz podczas tworzenia cennika projektu z cennika standardowego lub niestandardowego podczas tworzenia umowy, nadpisania cen efektywnych z datą są **nie** kopiowane z cennika źródłowego.

Aby ustawić zastąpienie ceny z datą wejścia w życie dla ceny roli lub narzutu na cenę dla roli, wykonaj następujące kroki.

1. Otwórz stronę cennika, dla którego chcesz ustawić zastąpienie ceny z datą wejścia w życie.
1. Wybierz kartę **Ceny dla roli**. Na karcie tej znajduje się lista wszystkich rekordów **Ceny dla roli** w cenniku.
1. Wybierz rekord **Cena dla roli**, dla którego chcesz ustawić nową cenę z datą wejścia w życie, a następnie dwukrotnie dotknij (lub kliknij dwukrotnie) **Cena dla roli**, aby otworzyć stronę **Szczegóły ceny dla roli**.
1. Wybierz kartę **Zastąpienia daty wejścia w życie**. Siatka na tej karcie zawiera listę wszystkich zastąpień daty wejścia w życie ceną dla wybranego rekordu **Cena dla roli**.
1. Na pasku narzędzi nad siatką wybierz **Nowe zastąpienie ceny dla roli**. Zostanie otwarty suwak **Nowe zastąpienie ceny dla roli**.
1. Określ datę wejścia w życie, jednostkę i nową cenę dla zastąpienia ceny. Następnie wybierz **Zapisz** i zamknij formularz.

> [!NOTE]
> - Zastąpienie ceny z datą wejścia w życie dla ceny roli lub narzutu na cenę dla roli ma zastosowanie do tej samej kombinacji wartości wymiaru cenowego, która istnieje w nadrzędnym wierszu **Cena dla roli** lub **Narzut na cenę dla roli**.
> - Data, która jest wybierana w polu **Obowiązuje od** powinna mieścić się w datach obowiązywania cennika nadrzędnego. Zastąpienie ceny zacznie obowiązywać w dniu, który został wybrany w polu **Obowiązuje od** i będzie obowiązywać do daty końcowej cennika nadrzędnego. Jeśli ustawisz kolejne zastąpienie ceny z datą wejścia w życie dla tej samej ceny roli, pierwsze zastąpienie ceny zacznie obowiązywać w dniu wybranym w polu **Obowiązuje od** i będzie obowiązywać do momentu rozpoczęcia drugiego zastąpienia.

## <a name="examples"></a>Przykłady

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>Przykład 1: Określanie daty wejścia w życie dla ceny roli, która ma zastąpienia ceny dla roli.

Poniższy przykład pokazuje, w jaki sposób określana jest data wejścia w życie dla określonej ceny roli, dla której ustawione są zastąpienia ceny dla roli.

**Cennik A: Od 1 stycznia do 30 czerwca**

*Cena dla roli*

| Cena dla roli | Jednostka | Cena | Wpływ na ustalanie cen dla transakcji przychodzących |
|---|---|---|---|
| Pracownik serwisu sieciowego | Godzina | 100 | Cena ta będzie stosowana na wszelkich transakcjach, w których data transakcji przypada pomiędzy 1 stycznia a 14 marca. |

*Zastąp cenę dla roli*

| Obowiązuje od | Jednostka | Cena | Wpływ na ustalanie cen dla transakcji przychodzących |
|---|---|---|---|
| Marzec 15 | Godzina | 110 | Cena ta będzie stosowana na wszelkich transakcjach, w których data transakcji przypada pomiędzy 15 marca a 30 marca. |
| Kwiecień 1 | Godzina | 120 | Cena ta będzie stosowana na wszelkich transakcjach, w których data transakcji przypada pomiędzy 1 kwietnia a 30 czerwca. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>Przykład 2: Określanie daty wejścia w życie dla narzutu na cenę dla roli, która ma zastąpienia narzutu ceny dla roli.

Poniższy przykład pokazuje, w jaki sposób określana jest data wejścia w życie dla określonego narzutu na cenę dla roli, dla której ustawione są zastąpienia narzutu na cenę dla roli.

**Cennik A: Od 1 stycznia do 30 czerwca**

*Cena dla roli*

| Cena dla roli | Godziny pracy | Jednostka | Cena | Wpływ na ustalanie cen dla transakcji przychodzących |
|---|---|---|---|---|
| Technik sieciowy | Zwykły | Godzina | 100 | Cena ta będzie stosowana na wszelkich transakcjach, w których data transakcji przypada pomiędzy 1 stycznia a 14 marca. |

*Narzut na cenę dla roli*

| Jednostka organizacyjna | Godziny pracy | Narzut (%) |
|---|---|---|
| Contoso US | Nadgodziny | 10% |

*Zastąpienie narzutu na cenę dla roli*

| Obowiązuje od | Cena | Wpływ na ustalanie cen dla transakcji przychodzących |
|---|---|---|
| Marzec 15 | 20% | Ten procent narzutu będzie stosowany na wszelkich transakcjach, w których data transakcji przypada pomiędzy 15 marca a 30 marca. |
| Kwiecień 1 | 25% | Ten narzut będzie stosowany na wszelkich transakcjach, w których data transakcji przypada pomiędzy 1 kwietnia a 30 czerwca. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
