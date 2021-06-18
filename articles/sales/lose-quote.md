---
title: Kopiowanie ofert opartych na projekcie
description: W tym temat zamieszczono informacje dotyczące kopiowania wierszy szansy sprzedaży opartych na produkcie w Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4e9009391d33c5dd5988ae65e13ca1ca1ec398bc
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999099"
---
# <a name="copy-project-based-quotes"></a>Kopiowanie ofert opartych na projekcie

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Istnieje możliwość łatwego utworzenia nowej oferty projektu przez skopiowanie istniejącej. 

- Aby skopiować ofertę projektu, na stronie listy **Ofert projektów** lub na stronie szczegółów **Oferty projektu** należy wybrać ofertę projektu, która ma zostać skopiowana, a następnie wybrać opcję **Kopiuj**.

Spowoduje to otwarcie strony dialogu, na której można wprowadzić parametry kopii. W poniższej tabeli wymieniono pola, które są wyświetlane na stronie dialogowej. W zależności od wybranych wartości proces kopiowania może ulec zmianie.

| **Pole** | **Opis** | **Wpływ zmian w dalszych etapach** |
| --- | --- | --- |
| Temat | Wprowadź odpowiedni temat lub nazwę oferty docelowej. Po otwarciu okna dialogowego program wyświetli temat dotyczący kopii z oferty źródłowej z dołączonym elementem **-kopia**. | |
| Ewentualny klient | Odwołanie do rekordu firmy lub konta klienta. Po otwarciu okna dialogowego system wyświetli konto z oferty źródłowej. | To pole jest to główny klient oferty. |
| Jednostka kontraktująca | Jednostka organizacyjna odpowiedzialna za realizację projektów skojarzonych z tą transakcją.
Po otwarciu okna dialogowego system wyświetli jednostkę zamawiającą z oferty źródłowej. | Jednostka zamawiająca to wydział firmy, który wykona projekt po zamknięciu transakcji. Każda jednostka zamawiająca ma walutę. Waluta jest używana do raportowania szacowanych i rzeczywistych kosztów poniesionych podczas wykonywania projektu. |
| Waluta | Jest to waluta, w jakiej obliczana jest kwota oferty. Po otwarciu okna dialogowego system wyświetli walutę z oferty źródłowej. Tę wartość można zmodyfikować, a jeśli jest ona zmieniona, pole **Kopiuj kalkulację cen** jest zawsze ustawione na **nie**. Wynika to z faktu, że cenniki w ofercie źródłowej nie mają już zastosowania. | Waluta jest używana to wybrania domyślnego cennika, aby utworzyć szacowaną wartość finansową oferty i ewentualnie zafakturować klienta, kiedy oferta przejdzie w fazę realizacji. |
| Żądana data dostawy | Jest to data dostarczenia zlecona przez klienta. | Ta wartość jest używana jako data zakończenia podczas tworzenia faktur w ramach odpowiedniego interwału. |
| Kopiuj kalkulację cen | Wartość Tak/Nie wskazuje, czy wycena z oferty powinna zostać skopiowana z oferty źródłowej. | Jeśli zostanie wybrana opcja **Tak**, lista produktów i odwołań do cennika projektu jest kopiowana z oferty źródłowej do oferty docelowej. Jeśli wybrana jest opcja **Nie**, cenniki są ponownie domyślnie ustawiane na podstawie najnowszych cenników ustawionych dla parametrów klienta lub projektu. |

Po wybraniu opcji **OK** na stronie dialogu system tworzy kopię oferty projektu na podstawie parametrów wybranych w oknie dialogowym. Zostanie otwarta nowa oferta projektu. 

> [!NOTE]
> Poniższe informacje nie są kopiowane z lokalizacji źródłowej do oferty docelowej:
>
> - Harmonogram fakturowania
> - Klienci wierszy ofert i ofert
> - Odwołanie do projektu w wierszach oferty opartej na projekcie — informacje o budżecie klienta
>
>Ponieważ te informacje są specyficzne dla danej oferty, te pola i rekordy nie są kopiowane. Kopiowane są wiersze oferty dotyczące projektów i produktów, oszacowania dotyczące szczegółów wiersza oferty oraz wartości graniczne nie do przekroczenia na poziomie oferty. Domyślne ustawienia cen i stawek kosztów zależą od wartości w opcji **Kopiuj kalkulację cen** wybranej na stronie **Kopiowania parametrów**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]