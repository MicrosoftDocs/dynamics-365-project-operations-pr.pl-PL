---
title: Przywołaj wcześniej zatwierdzone wpisy
description: W temat wyjaśniono, jak członek zespołu projektu może zażądać ochłody z przesłanych wcześniej i zatwierdzonych rekordów czasu, wydatków i materiałów oraz jak menedżer projektu może zatwierdzić lub odrzucić żądania zatwierdzenia.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 18796e803ff73806aaa60b453048ee3160406b40
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586587"
---
# <a name="recall-previously-approved-entries"></a>Przywołaj wcześniej zatwierdzone wpisy

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Członek zespołu projektowego, który przesyła wpis dotyczący czasu, wydatków lub wykorzystania materiałów, może przywołać ten wpis po jego zatwierdzeniu. Proces wycofania składa się z dwóch głównych etapów:

1. Osoba przesyłająca prosi o odwołanie.
2. Osoba zatwierdzająca zatwierdza wniosek o wycofanie.

## <a name="request-a-recall"></a>Wnioskowanie o odwołanie

Wykonaj poniższe czynności, aby zażądać wycofania zatwierdzonych wpisów dotyczących czasu, wydatków lub zużycia materiałów.

1. Wykonaj jedną z poniższych czynności, w zależności od typu wpisu, który chcesz przywołać:

    - Aby zobaczyć wpisy dotyczące czasu, przejdź do **Projekty** \> **Moja praca** \> **Wpis czasu** i wybierz wszystkie wpisy dotyczące czasu dla określonej kombinacji projektu i zadanie. Alternatywnie w siatce zaznacz poszczególne komórki czasu w określonym dniu określonego projektu.
    - W przypadku wpisów wydatków przejdź do **Projekty** \> **Moja praca** \> **Wydatki** i wybierz wiersz z wpisem wydatków do przywołania.
    - W przypadku wpisów dotyczących zużycia materiałów przejdź do **Projekty** \> **Moja praca** \> **Dziennik użycia materiałów** i wybierz wiersz, w którym wpis dotyczący zużycia materiałów zostanie przywołany.

2. Wybierz pozycję **Odwołaj**. Pojawia się okno dialogowe potwierdzenia. Jeśli wybrane wpisy dotyczące czasu, wydatków lub zużycia materiałów zostały już zatwierdzone, zostanie wyświetlony monit o podanie powodu wycofania.
3. Wprowadź przyczynę odwołania, a następnie wybierz przycisk **OK**, aby potwierdzić operację. System wyśle do użytkownika, który zatwierdził wpisy, prośbę o zatwierdzenie odwołania.

> [!IMPORTANT]
> Nie można utworzyć żądania wycofania dla zatwierdzonego czasu, kosztu lub wpisu zużycia materiałów, który został już zafakturowany na klienta. Jeśli spróbujesz, otrzymasz komunikat z informacją, że nie można odwołać wpisu czasu, kosztu lub zużycia materiałów, ponieważ został on już zafakturowany. W takim przypadku możesz zażądać wycofania wpisu tylko wtedy, gdy faktura korygująca służy do przyznania klientowi pełnego kredytu lub zwrotu pieniędzy na oryginalnej fakturze.

## <a name="approve-or-reject-a-recall-request"></a>Zatwierdzanie lub odrzucanie żądania odwołania

Wykonaj te kroki, aby zatwierdzić lub odrzucić żądanie odwołania.

1. Wybierz kolejno opcje **Projekty** \> **Moja praca** \> **Zatwierdzenia**.
2. Na stronie listy **Zatwierdzenia** zmień widok na **Żądania odwołania do zatwierdzenia**. Zostanie wyświetlona lista przesłanych żądań odwołania.
3. Zaznacz jeden lub więcej wpisów, a następnie kliknij przycisk **Zatwierdź** lub **Odrzuć**.
4. W przypadku wybrania opcji **Zatwierdź** zostanie wyświetlony komunikat ostrzegawczy zawierający opis skutków zatwierdzenia. Wybierz pozycję **OK**, aby potwierdzić operację. Żądanie odwołania zostanie zatwierdzone.

    –lub–

    W przypadku wybrania opcji **Odrzuć** żądanie odwołania zostanie odrzucone.

> [!IMPORTANT]
> Po zatwierdzeniu wycofania, podobnie jak w przypadku jego żądania, system sprawdza wszelkie działania związane z fakturowaniem dotyczące czasu, wydatków lub wpisów dotyczących zużycia materiałów. Jeśli wpis został już zafakturowany lub jeśli znajduje się on w wersji roboczej faktury, osoba zatwierdzająca zobaczy komunikat o błędzie z informacją, że nie można zatwierdzić odwołania czasu lub wydatku, ponieważ został on już zafakturowany. W takim przypadku osoba zatwierdzająca może zatwierdzić wycofanie tylko wtedy, gdy faktura korygująca jest używana do przyznania klientowi pełnego kredytu lub zwrotu pieniędzy na oryginalnej fakturze.

## <a name="impact-of-a-recall-request"></a>Wpływ żądania odwołania

Odwołanie zatwierdzonego wpisu ma wpływ na stronę operacyjną i finansową.

### <a name="operational-impact"></a>Wpływ operacyjny

Jeśli żądanie odwołania zostanie zatwierdzone, rekord zatwierdzenia jest oznaczany jako **Odrzucono**. Stan wpisu zmieni się na **Zwrócono** lub **Odrzucono**, w zależności od tego, czy jest to wpis dotyczący czasu, czy wpis dotyczący wydatków lub wykorzystania materiałów.

Członek zespołu projektu może wyświetlać wpisy, edytować je i ponownie wysyłać albo całkowicie usuwać.

Jeśli żądanie odwołania zostanie odrzucone, wpis zachowuje stan **Zatwierdzono**, a wpisu nie może edytować członek zespołu projektu ani osoba zatwierdzająca w projekcie.

### <a name="financial-impact"></a>Wpływ finansowy

Jeśli żądanie odwołania zostanie zatwierdzane, odnośne wartości rzeczywiste dotyczące kosztu i sprzedaży są aktualizowane w następujący sposób:

- Pole **Stan korekty** zmienia wartość na **Skorygowano**.
- Pole **Stan rozliczania** zmienia wartość na **Anulowano**.

Następnie w tabeli Wartości rzeczywiste są tworzone wpisy wycofania. Aby utworzyć wpisy wycofania, system kopiuje wartości pól z pierwotnych wartości rzeczywistych. Jedyne wartości, które nie są kopiowane, to wartości ilości. Zamiast tego te wartości są wycofywane. Wycofane wartości rzeczywiste są tworzone dla wartości rzeczywistych **Koszt** i **Nierozliczona sprzedaż**. Pole **Stan korekty** w wycofanych wartościach rzeczywistych otrzymuje wartość **Nie można skorygować**, a pole **Stan rozliczania** otrzymuje wartość **Anulowano**. Ze względu na te zmiany zarejestrowane wydatki oraz zaległości przychodów w projekcie nie będą już uwzględniały kwot reprezentowanych przez te wartości rzeczywiste.

Jeśli żądanie odwołania zostanie odrzucone, nie ma żadnego wpływu finansowego na projekt.

## <a name="changes-to-time-entry-records"></a>Zmiany w rekordach wpisów czasu

Na poniższej ilustracji przedstawiono zmiany, które zachodzą dla zatwierdzonych wpisów czasu i odpowiednich rekordów zatwierdzenia, gdy są one przywracane.

![Zmiany stanu wpisu czasu.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Zmiany w ewidencji wpisów wydatków i zużycia materiałów

Na poniższej ilustracji przedstawiono zmiany, które zachodzą w przypadku zatwierdzonych wpisów wykorzystania wydatków i materiałów oraz odpowiednich rekordów zatwierdzenia po ich wycofaniu.

![Zmiany stanu wpisu wydatku.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
