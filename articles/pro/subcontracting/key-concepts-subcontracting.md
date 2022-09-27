---
title: Kluczowe pojęcia związane z podwykonawstwem
description: W tym artykule wyjaśniono kilka kluczowych pojęć dotyczących podwykonawstwa w aplikacji Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9577169f12198222e647ed07ae8a1b6c55da4323
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522762"
---
# <a name="key-concepts-in-subcontracting"></a>Kluczowe pojęcia związane z podwykonawstwem


_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

W artykule wyjaśniono kilka kluczowych pojęć, o których należy pamiętać przed rozpoczęciem korzystania z funkcji podwykonawstwa w aplikacji Microsoft Dynamics 365 Project Operations.

## <a name="contracting-unit-on-the-subcontract"></a>Jednostka zawierająca umowę w sprawie kontraktu podrzędnego

Jednostka zamawiająca reprezentuje oddział lub praktykę, która jest właścicielem realizacji ewentualnego projektu. Jednostka zamawiająca to także dział, który wchodzi w relację umową ze sprzedawcą.

## <a name="purchase-currency"></a>Waluta zakupu

W programie Project Operations waluta zakupu to waluta, w której tworzona jest umowa podwykonawcza. Jest to również waluta, w której księgowane są koszty podwykonawcy w projekcie. Waluta zakupu może różnić się od waluty projektu, a waluta projektu może z kolei różnić się od waluty sprzedaży.

## <a name="billing-methods-on-subcontract-lines"></a>Metody fakturowania w wierszach kontraktów podwykonawców

W przypadku projektów istnieją zazwyczaj modele kontraktów oparte na stałej opłacie i zużyciu. Project Operations obsługuje te metody rozliczeń w kontekście sprzedaży i zakupu. W przypadku zakupu metody rozliczeń działają w następujący sposób:

- **Czas i materiał** — Gdy wiersz umowy podwykonawczej korzysta z metody rozliczeń **Czas i materiał**, koszt czasu jest rejestrowany w projekcie, ponieważ podwykonawcy pracują nad tym projektem i rejestrują czas. Te transakcje kosztowe od podwykonawców są następnie dopasowywane do pozycji na fakturach od dostawców. W tym modelu kierownicy projektów, którzy korzystają z Project Operations, mogą dopasowywać i weryfikować wiersze faktur od dostawcy z rejestrowanym i zatwierdzanym czasem podwykonawcy. Po zakończeniu weryfikacji poprzednie rzeczywiste koszty, które zostały zarejestrowane po zatwierdzeniu, są wycofywane, a w projekcie tworzone są nowe rzeczywiste koszty oparte na fakturze od dostawcy.
- **Stała cena** — W tym modelu zawierania umów ze stałą opłatą faktury od dostawców są oparte na stałych kamieniach milowych. Jednak zasoby podwykonawców mogą również raportować czas. Czas jest następnie sprawdzany i zatwierdzany przez kierownika projektu. Po zatwierdzeniu, Project Operations tworzy tymczasowe rzeczywiste koszty w projekcie. Po wysłaniu przez dostawcę faktury za kamień milowy kierownik projektu może dopasować wcześniej zarejestrowane rzeczywiste koszty do kamienia milowego. Po zakończeniu weryfikacji rzeczywiste koszty są odwracane i rejestrowany jest koszt oparty na kamieniach milowych.

## <a name="project-price-lists-on-subcontracts"></a>Cenniki projektów na umowach podwykonawczych

Cenniki projektów to cenniki używane do ustawiania cen zakupu dla czasu, wydatków i innych składników związanych z projektem. Może istnieć wiele cenników, z których każdy może mieć własną podumowę z datą wejścia w życie w rozwiązaniu Project Operations. Project Operations nie obsługuje nakładania się dat wejścia w życie w cennikach projektów dla umowy podwykonawczej.

## <a name="transaction-classes-on-subcontracts"></a>Klasy transakcji na umowach podwykonawczych

W Project Operations są obsługiwane cztery typy klas transakcji:

- Czas
- Wydatek
- Materiał
- Opłata

Koszty zakupu można oceniać i ponosić tylko w klasach transakcji **Czas**, **Koszt** i **Materiały**. **Opłata** jest klasą transakcji tylko do przychodów i nie jest dostępna w zawartości zakupu.

## <a name="purchase-pricing-dimensions"></a>Wymiary cen zakupu

Wymiary cenowe pozwalają decydować, jakie atrybuty są używane do ustalania ceny zakupu i domyślnie terminowych transakcji. W odniesieniu do zakupów, Project Operations obsługuje tylko stałe zestawy wymiarów dla konfiguracji ceny zakupu i ustawienia domyślnego. W przypadku konfigurowania ceny zakupu i domyślnego konfigurowania wierszy kontraktów i transakcji czasu podwykonawcy atrybuty to **Rola** i **Zasób zarezerwowany**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
