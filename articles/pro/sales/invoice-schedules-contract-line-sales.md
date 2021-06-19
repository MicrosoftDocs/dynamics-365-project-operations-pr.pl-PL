---
title: Tworzenie harmonogramów fakturowania w pozycji kontraktu opartego na projekcie - wersja uproszczona
description: W tym temat zamieszczono informacje dotyczące tworzenia harmonogramów faktur i punktów kontrolnych.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 548858f6d2257343a632657ca386da03f1f330a9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003244"
---
# <a name="create-invoice-schedules-on-a-project-based-contract-line---lite"></a>Tworzenie harmonogramów fakturowania w pozycji kontraktu opartego na projekcie - wersja uproszczona

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Można dołączyć harmonogram fakturowania w pozycji kontraktu opartego na projekcie. Fakturowanie jest dozwolone tylko po wykorzystaniu kontraktu, aby utworzyć kontrakt dotyczący projektu. Harmonogramy faktur umożliwiają automatyczne tworzenie faktur na podstawie projektów dla wierszy kontraktu opartego na projektach. Jeśli są planowane ręczne tworzenie faktur, można pominąć tworzenie harmonogramów faktur w pozycji kontraktu opartej na projekcie lub pozycji kontraktu.

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-contract-line"></a>Utwórz harmonogram faktur czasowych i materiałowych dla pozycji umowy opartej na projekcie

Kiedy metoda fakturowania w wierszu kontraktu opartego na projekcie to czas i materiały, można wygenerować harmonogram fakturowania opartego na datach. Aby automatycznie wygenerować harmonogram faktur zależnych od dat, należy wykonać następujące kroki.

1. Przejdź do **Ustawienia** > **Częstotliwości fakturowania**, aby skonfigurować częstotliwość faktur.
2. Otwórz kontrakt projektu i na karcie **Podsumowanie** ustaw żądaną datę dostawy.
3. Otwórz wiersz kontraktu typu czas i materiały, dla którego chcesz utworzyć harmonogram fakturowania opartego na datach. 
4. Na karcie **Harmonogram faktur** wybierz datę rozpoczęcia fakturowania i częstotliwość faktur. 
5. W podsiatce wybierz pozycję **Utwórz harmonogram fakturowania**.

    System wygeneruje harmonogram faktur z informacjami o następujących polach:

    - W polu **Data przebiegu fakturowania** jest ustawiana data oparta na częstotliwości faktur.
    - **Ostateczny termin transakcji** jest ustawiany na dzień wcześniej niż **Data przebiegu fakturowania**.
    - **Stan przebiegu** jest automatycznie ustawiany jako **Nie uruchomiony**. Kiedy zadanie automatycznego tworzenia faktury jest uruchamiane na określoną **Data przebiegu fakturowania**, spowoduje to zaktualizowanie tego pola na wartość **Przebieg pomyślny** albo **Przebieg nieudany**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-contract-line"></a>Utwórz harmonogram faktur ze stałą ceną dla wiersza umowy opartego na projekcie

Kiedy pozycja kontraktu oparta na projektach ma metodę fakturowania przy ustalonej cenie, można utworzyć harmonogram faktur według punktów kontrolnych. Wykonaj poniższe kroki, aby automatycznie wygenerować harmonogram faktur oparty na punktach kontrolnych dla ustalonego zestawu punktów kontrolnych, które będą dystrybuowane równo za dany okres kalendarzowy.

1. Przejdź do **Ustawienia** > **Częstotliwości fakturowania**, aby skonfigurować częstotliwość faktur.
2. Otwórz kontrakt projektu i na karcie **Podsumowanie** ustaw żądaną datę dostawy.
3. Otwórz wiersz kontraktu o stałej cenie, dla którego chcesz utworzyć harmonogram punktów kontrolnych. 
4. Na karcie **Harmonogram faktur (Punkty kontrolne rozliczenia)** wybierz datę rozpoczęcia fakturowania i częstotliwość faktur. 
5. W podsiatce wybierz pozycję **Utwórz okresowe punkty kontrolne**.

    System generuje harmonogram faktur z następującymi informacjami o punktach kontrolnych.

    - W polu **Nazwa punktu kontrolnego** jest ustawiana data, która jest określana na podstawie częstotliwości faktur.
    - W polu **Data punktu kontrolnego** jest ustawiana data, która jest określana na podstawie częstotliwości faktur.
    - **Kwota punktów kontrolnych** jest obliczana jako iloraz kwoty kontraktu w wierszu kontraktu opartej na projekcie przez liczbę punktów kontrolnych zgodnie z częstotliwością, rozpoczęciem rozliczenia i wymaganymi datami dostawy.
    - Jeśli pozycja kontraktu zawiera wartość w polu **Szacowana kwota podatku**, to pole jest również przydzielone do poszczególnych punktów kontrolnych równo podczas generowania okresowych punktów kontrolnych.

Pozycje punktów kontrolnych rozliczania powinny być równe wartości zakontraktowane w pozycji kontraktu opartej na projekcie. Jeśli nie są równe, wystąpi błąd. Korzystając z tego błędu, można sprawdzić, czy suma punktów kontrolnych rozliczania zakontraktowanej wartości w wierszu jest tworzona, edytowana lub usuwana. Po wprowadzeniu zmian Odśwież stronę.

### <a name="manually-create-milestones"></a>Ręczne tworzenie okresowych punktów kontrolnych

Punkty kontrolne z ustalonymi cenami można generować ręcznie, kiedy nie są okresowo dzielone. Aby utworzyć punkt kontrolny ręcznie, należy wykonać następujące kroki.

1. Otwórz wiersz umowy o stałej cenie, w którym chcesz utworzyć kamień milowy. 
2. Na karcie **Harmonogram faktur** w podsiatce wybierz pozycję **+ Utwórz nowy punkt kontrolny pozycja kontraktu**.
3. W formularzu **Tworzenia punktu kontrolnego** wprowadź wymagane informacje na podstawie poniższej tabeli. 

| Pole | Lokalizacja | Opis | Wpływ zmian w dalszych etapach |
| --- | --- | --- | --- |
| Nazwa punktu kontrolnego | Szybkie tworzenie | Pole tekstowe nazwy punktu kontrolnego. | To pole jest dołączone do pola punkt kontrolny pozycji kontraktu projektu oraz na fakturze. |
| Zadanie projektu | Szybkie tworzenie | Jeśli punkt kontrolny jest związany z zadaniem projektu, należy użyć tego odwołania w celu dodania logiki niestandardowej i ustawienia stanu punktów kontrolnych na podstawie stanu zadania. | Brak skutku obniżyć tego odwołania do zadania. |
| Data punktu kontrolnego | Szybkie tworzenie | Dzień, w którym ma być wyszukiwany stan tego punktu kontrolnego podczas automatycznej operacji tworzenia faktury, aby uważać go za fakturowanie. | To jest dołączone do pola punkt kontrolny pozycji kontraktu projektu oraz na fakturze. |
| Stan faktury | Szybkie tworzenie | Po utworzeniu punktu kontrolnego stan jest zawsze ustawiony jako **Nieprzygotowane do fakturowania** lub **Nierozpoczęty**. | To jest dołączone do pola punkt kontrolny pozycji kontraktu projektu oraz na fakturze. |
| Kwota pozycji | Szybkie tworzenie | Kwoty lub wartości punktów kontrolnych, które będą zafakturowane na klientach. | To pole jest dołączone do pola punkt kontrolny pozycji kontraktu projektu oraz na fakturze, |
| Podatek | Szybkie tworzenie | Kwota podatku stosowana względem punktu kontrolnego. | To jest dołączone do pola punkt kontrolny pozycji kontraktu projektu oraz na fakturze. |

4. Wybierz pozycję **Zapisz i zamknij**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]