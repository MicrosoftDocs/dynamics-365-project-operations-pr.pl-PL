---
title: Tworzenie harmonogramu fakturowania w pozycji kontraktu opartego na projekcie
description: W tym temacie zamieszczono informacje dotyczące tworzenia harmonogramów faktur i punktów kontrolnych wierszy kontraktów.
author: rumant
manager: Annbe
ms.date: 10/17/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b2fbec567c07d7567f1d133fa3512496039f16a1
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513937"
---
# <a name="create-an-invoice-schedule-on-a-project-based-contract-line"></a>Tworzenie harmonogramu fakturowania w pozycji kontraktu opartego na projekcie 

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Można tworzyć harmonogram fakturowania w pozycji kontraktu opartego na projekcie. Fakturowanie jest dozwolone tylko po wykorzystaniu kontraktu i utworzeniu kontraktu dotyczącego projektu. Harmonogram faktur umożliwia automatyczne tworzenie projektów faktur dla wierszy kontraktu opartego na projektach. Jeśli jednak tylko ręczne tworzenie faktur jest konieczne, można pominąć tworzenie harmonogramów faktur w pozycjach kontraktu.

## <a name="create-a-time-and-material-invoice-schedule-for-a-contract-line"></a>Tworzenie harmonogramu fakturowania typu czas i materiały dla wiersza kontraktu opartego na projekcie

Kiedy metoda fakturowania w wierszu kontraktu opartego na projekcie to czas i materiały, można wygenerować harmonogram fakturowania opartego na datach. Aby automatycznie wygenerować harmonogram faktur zależnych od dat, należy wykonać następujące kroki.

1. Przejdź do sekcji **Ustawienia** > **Częstotliwości faktur** i ustaw częstotliwość fakturowania.
2. Przejdź do rekordu kontraktu projektu i na karcie **Podsumowanie** wybierz **Datę dostawy** w odpowiednim polu.
3. Otwórz wiersz oferty typu **czas i materiały**, dla którego tworzysz harmonogram fakturowania opartego na datach. 
4. Na karcie **Harmonogram fakturowania** wybierz wartości w polach rozpoczęcie fakturowania i częstotliwość fakturowania.
5. W podsiatce wybierz pozycję **Utwórz harmonogram fakturowania**. Aplikacja generuje harmonogram faktur dla pól **Data przebiegu fakturowania**, **Ostateczny termin transakcji** oraz **Stan przebiegu** w następujący sposób:

    - **Data przebiegu fakturowania**: ta data jest ustawiana na datę określoną na bazie częstotliwości faktur.
    - **Ostateczny termin transakcji**: ten termin jest ustawiany na dzień wcześniej niż data przebiegu fakturowania.
    - **Stan przebiegu**: jest automatycznie ustawiany jako **Nie uruchomiony**. Kiedy zadanie automatycznego tworzenia faktury jest uruchamiane na określoną datę rozpoczęcia fakturowania, spowoduje to zaktualizowanie tego pola na wartość **Przebieg pomyślny** albo **Przebieg nieudany**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-contract-line"></a>Tworzenie harmonogramu fakturowania o stałej cenie dla wiersza kontraktu opartego na projekcie

Kiedy wiersz kontraktu opartego na projekcie ma stałą metodę fakturowania, można utworzyć harmonogram faktur według typu punktu kontrolnego. 

> [!NOTE]
> Nie można tworzyć punktów kontrolnych, jeśli w pozycji kontraktu nie ma projektów.

Wykonaj poniższe kroki, aby wygenerować harmonogram dla harmonogramu fakturowania opartego na punktach kontrolnych, które są równo dystrybuowane za dany okres kalendarzowy.

1. Przejdź do sekcji **Ustawienia** > **Częstotliwości faktur** i ustaw częstotliwość fakturowania.
2. Przejdź do rekordu kontraktu projektu i na karcie **Podsumowanie** wybierz **Datę dostawy** w odpowiednim polu.
3. Otwórz wiersz **oferty o stałej cenie**, dla którego tworzysz harmonogram punktów kontrolnych. Na karcie **Punkty kontrolne rozliczania** wybierz wartości w polach rozpoczęcie fakturowania i częstotliwość fakturowania. 
4. W podsiatce wybierz pozycję **Utwórz okresowe punkty kontrolne**. Harmonogram faktur jest generowany z polami **Nazwa punktu kontrolnego**, **Data punktu kontrolnego** i **Kwotą punktu kontrolnego** ustawionymi w następujący sposób:

    - **Nazwa punktu kontrolnego**: ta nazwa jest podyktowana przez częstotliwość fakturowania.
    - **Data punktu kontrolnego**: ta data jest ustawiana na datę określoną na bazie częstotliwości faktur.
    - **Kwota punktu kontrolnego**: jest obliczana jako iloraz kwoty kontraktu w wierszu kontraktu opartego na projekcie przez liczbę punktów kontrolnych zgodnie z częstotliwością rozpoczęcia i początkiem rozliczenia oraz wymaganych dat dostawy.

    Jeśli pozycja kontraktu zawiera wartość w polu **Szacowana kwota podatku**, to pole jest również przydzielone do poszczególnych punktów kontrolnych równo podczas generowania okresowych punktów kontrolnych.

Punkty kontrolne powinny być równe wartości kontraktu z pozycji kontraktu. Jeśli tak nie będzie, na stronie **pozycja kontraktu** zostanie wyświetlony komunikat o błędzie. Aby naprawić ten błąd, należy sprawdzić, czy suma punktów kontrolnych rozliczania zakontraktowana dla danego wiersza jest równa wartości zakontraktowanej poprzez tworzenie, edycję lub usuwanie punktów kontrolnych. Po wprowadzeniu zmian odśwież stronę, aby usunąć błąd.

### <a name="manually-create-milestones"></a>Ręczne tworzenie okresowych punktów kontrolnych

Można także tworzyć punkty kontrolne ze stałymi cenami ręcznie, kiedy nie są one okresowo dzielone. Wykonaj poniższe kroki, aby ręcznie utworzyć nowy punkt kontrolny.

1. Otwórz wiersz kontraktu o stałej cenie, dla którego jest tworzony punkt kontrolny, i na karcie **Harmonogram fakturowania** w podsiatce wybierz pozycję **+ Utwórz nowy punkt kontrolny pozycji kontraktu**. 
2. Na stronie **Tworzenie punktów kontrolnych** wprowadź wymagane informacje na podstawie poniższej tabeli.

| Pole | Lokalizacja | Opis | Wpływ zmian w dalszych etapach |
| --- | --- | --- | --- |
| Nazwa punktu kontrolnego | Szybkie tworzenie | Pole tekstowe nazwy punktu kontrolnego. | Następuje skopiowanie punktów kontrolnych do pozycji kontraktu projektu i do faktury. |
| Zadanie projektu | Szybkie tworzenie | Jeśli punkt kontrolny jest związany z zadaniem projektu, można użyć tego odwołania w celu dodania logiki niestandardowej, a stan punktów kontrolnych zostanie ustawiony na podstawie stanu zadania. | W takim przypadku aplikacja nie ma wpływu na to odwołanie do zadania. |
| Data punktu kontrolnego | Szybkie tworzenie | Ustaw datę, od której będzie wyszukiwany stan tego punktu kontrolnego przy automatycznym tworzeniu faktur, aby wziąć go pod uwagę na potrzeby fakturowania. | Następuje skopiowanie punktów kontrolnych do pozycji kontraktu projektu i do faktury. |
| Stan faktury | Szybkie tworzenie | Po utworzeniu punktu kontrolnego jego stan jest zawsze ustawiony jako **Niegotowy do fakturowania** lub **Nierozpoczęty**. | Następuje skopiowanie punktów kontrolnych do pozycji kontraktu projektu i do faktury. |
| Kwota pozycji | Szybkie tworzenie | Kwota lub wartość punktów kontrolnych, która zostanie zafakturowana klientowi. | Następuje skopiowanie punktów kontrolnych do pozycji kontraktu projektu i do faktury. |
| Podatek | Szybkie tworzenie | Kwota podatku stosowana względem punktu kontrolnego. | Następuje skopiowanie punktów kontrolnych do pozycji kontraktu projektu i do faktury. |

3. Wybierz pozycję **Zapisz i zamknij**.
