---
title: Harmonogramy fakturowania w wierszach oferty opartej na projekcie
description: W tym artykule przedstawiono informacje na temat tworzenia harmonogramów i punktów kontrolnych faktur dla wierszy oferty.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b1e431bc3586f9fef7a01348555e4ee4e06cc66c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918325"
---
# <a name="invoice-schedules-on-project-based-quote-lines"></a>Harmonogramy fakturowania w wierszach oferty opartej na projekcie

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Pozycja oferty opartej na projekcie daje możliwość wyrażenia planu fakturowania. Ta funkcja jest opcjonalna podczas fazy oferty, ponieważ aplikacja nie obsługuje fakturowania projektu, jeśli jest on powiązany z wierszem oferty. Fakturowanie jest dozwolone tylko po wykorzystaniu oferty. Podczas fazy oferty jedyny wpływ zmian w dalszych etapach związany z tworzeniem harmonogramu fakturowania polega na tym, że harmonogram faktury jest kopiowany do pozycji kontraktu opartej na projekcie. Jeśli nie utworzysz harmonogramu fakturowania podczas fazy oferty, będzie można wykonać tę czynność w pozycji kontraktu opartej na projekcie.

Generalnie harmonogramy fakturowania umożliwiają automatyczne tworzenie projektów faktur dla pozycji kontraktu opartego na projektach. 

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-quote-line"></a>Tworzenie harmonogramu fakturowania typu czas i materiały dla wiersza oferty opartej na projekcie

Kiedy metoda fakturowania w wierszu oferty opartej na projekcie to czas i materiały, system generuje harmonogram fakturowania opartego na datach. Aby automatycznie wygenerować harmonogram faktur zależnych od dat, należy wykonać następujące kroki.

1. Przejdź do sekcji **Ustawienia** > **Częstotliwości faktur** i ustaw częstotliwość fakturowania.
2. Na stronie **Oferty** otwórz ofertę projektu i na karcie **Podsumowanie** ustaw żądaną datę dostarczenia.
3. Otwórz wiersz oferty typu czas i materiały, dla którego chcesz utworzyć harmonogram fakturowania opartego na datach. 
4. Na karcie **Harmonogram fakturowania** wybierz wartości w polach **Rozpoczęcie fakturowania** i **Częstotliwość fakturowania**. 
5. W podsiatce wybierz pozycję **Utwórz harmonogram fakturowania**.
6. Aplikacja generuje harmonogram faktur dla pól **Data przebiegu fakturowania**, **Ostateczny termin transakcji** oraz **Stan przebiegu** w następujący sposób:

    - **Data przebiegu fakturowania** jest ustawiana na datę określoną na bazie częstotliwości faktur.
    - **Ostateczny termin transakcji** jest ustawiany na dzień wcześniej niż **Data przebiegu fakturowania**.
    - **Stan przebiegu** jest automatycznie ustawiany jako **Nie uruchomiony**. Kiedy zadanie automatycznego tworzenia faktury jest uruchamiane na określoną datę rozpoczęcia fakturowania, spowoduje to zaktualizowanie tego pola na wartość **Przebieg pomyślny** albo **Przebieg nieudany**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-quote-line"></a>Tworzenie harmonogramu fakturowania o stałej cenie dla wiersza oferty opartej na projekcie

Kiedy wiersz oferty opartej na projekcie ma **Stałą** metodę fakturowania, system tworzy harmonogram faktur według typu punktu kontrolnego. Wykonaj poniższe kroki, aby automatycznie wygenerować harmonogram dla ustalonych zestawów punktów kontrolnych, które są równo dystrybuowane za dany okres kalendarzowy.

1. Przejdź do sekcji **Ustawienia** > **Częstotliwości faktur** i ustaw częstotliwość fakturowania.
2. Na stronie **Oferty** otwórz ofertę projektu i na karcie **Podsumowanie** ustaw żądaną datę dostarczenia.
3. Otwórz wiersz oferty o stałej cenie, dla którego chcesz utworzyć harmonogram punktów kontrolnych. 
4. Na karcie **Harmonogram fakturowania** wybierz wartości w polach **Rozpoczęcie fakturowania** i **Częstotliwość fakturowania**. 
5. W podsiatce wybierz pozycję **Utwórz okresowe punkty kontrolne**.
6. Aplikacja generuje harmonogram fakturowania zawierający nazwę, datę i kwotę punktu kontrolnego.

    - Nazwa punktu kontrolnego jest ustawiana na datę określoną na bazie częstotliwości faktur.
    - Data punktu kontrolnego jest ustawiana na datę określoną na bazie częstotliwości faktur.
    - Kwota punktów kontrolnych jest obliczana jako iloraz kwoty oferty w wierszu oferty opartej na projekcie przez liczbę punktów kontrolnych zgodnie z częstotliwością rozpoczęcia i początkiem rozliczenia oraz wymaganych dat dostawy.
    - Jeśli wiersz oferty ma również szacowaną kwotę podatku, ta wartość jest dzielona między poszczególne punkty kontrolne po równo podczas generowania okresowych punktów kontrolnych.

### <a name="manually-create-milestones"></a>Ręczne tworzenie okresowych punktów kontrolnych

Punkty kontrolne ze stałymi cenami mogą również zostać wygenerowane ręcznie, kiedy nie są okresowo dzielone. Aby ręcznie utworzyć okresowy punkt kontrolny:

Otwórz wiersz oferty o stałej cenie, dla którego chcesz utworzyć punkt kontrolny. Na karcie **Harmonogram faktur** w podsiatce wybierz pozycję **+ Utwórz nowy punkt kontrolny wiersza oferty** i wprowadź wymagane informacje na podstawie poniższej tabeli.

| **Pole** | **Lokalizacja** | **Opis** | **Wpływ zmian w dalszych etapach** |
| --- | --- | --- | --- |
| Nazwa punktu kontrolnego | Szybkie tworzenie | Nazwa punktu kontrolnego. | Następuje skopiowanie punktów kontrolnych do pozycji kontraktu projektu i do faktury |
| Zadanie projektu | Szybkie tworzenie | Jeśli punkt kontrolny jest związany z zadaniem projektu, można użyć tego odwołania w celu dodania logiki niestandardowej, a stan punktów kontrolnych zostanie ustawiony na podstawie stanu zadania. | W takim przypadku aplikacja nie ma wpływu na to odwołanie do zadania. |
| Data punktu kontrolnego | Szybkie tworzenie | Ustaw datę, od której będzie wyszukiwany stan tego punktu kontrolnego przy automatycznym tworzeniu faktur, aby wziąć go pod uwagę na potrzeby fakturowania. | Następuje skopiowanie punktów kontrolnych do pozycji kontraktu projektu i do faktury. |
| Stan faktury | Szybkie tworzenie | Po utworzeniu punktu kontrolnego jego stan jest zawsze ustawiony jako **Niegotowy do fakturowania**. | Następuje skopiowanie punktów kontrolnych do pozycji kontraktu projektu i do faktury. |
| Kwota pozycji | Szybkie tworzenie | Kwota lub wartość punktów kontrolnych, która zostanie zafakturowana klientowi. | Następuje skopiowanie punktów kontrolnych do pozycji kontraktu projektu i do faktury. |
| Podatek | Szybkie tworzenie | Kwota podatku, która zostanie zastosowana względem punktu kontrolnego. | Następuje skopiowanie punktów kontrolnych do pozycji kontraktu projektu i do faktury. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]