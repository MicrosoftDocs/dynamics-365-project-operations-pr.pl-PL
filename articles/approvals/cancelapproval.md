---
title: Anuluj zatwierdzenie wcześniej zatwierdzonych wpisów
description: W temat wyjaśniono, jak menedżer projektu może anulować zatwierdzenie zatwierdzonych wcześniej wpisów czasu, wydatków lub materiałów.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 03d4511e85e9fc8d596b269274c4a7e10016244c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584793"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Anuluj zatwierdzenie wcześniej zatwierdzonych wpisów

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Kierownik projektu lub osoba zatwierdzająca, która wcześniej zatwierdziła wpisy dotyczące czasu, wydatków lub wykorzystania materiałów, może anulować zatwierdzenie tych wpisów. 

Wykonaj poniższe czynności, aby anulować zatwierdzenie wcześniej zatwierdzonego wpisu dotyczącego czasu, wydatków lub wykorzystania materiałów.

1. Wybierz kolejno opcje **Projekty** \> **Moja praca** \> **Zatwierdzenia**.
2. Na stronie listy **Zatwierdzanie** są wszystkie wpisy dotyczące godzin, które zostały zatwierdzeń. Zmień widok na Moje **zatwierdzeń z przeszłości**.
3. Wybierz czas, koszt lub zatwierdzenie materiałów do anulowania. W okienku akcji wybierz opcję **Anuluj zatwierdzenie**.
4. W oknie z komunikatem potwierdzenia wybierz przycisk **OK**, aby potwierdzić operację.

> [!IMPORTANT]
> Nie można anulować zatwierdzonego wcześniej wpisu czasu, wydatków i użycia materiałów, które zostały już zafakturowane klientowi. Przy próbie zostanie wyświetlony komunikat z komunikatem, że nie można anulować zatwierdzania, ponieważ zostało już zafakturowane. W takim przypadku można anulować zatwierdzenie tylko wtedy, gdy do wydania pełnego kredytu lub umowy dotyczącej pierwotnej faktury zostanie użyta faktura naprawczy.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Wpływ anulowania zatwierdzenia wcześniej zatwierdzonego wpisu

Anulowanie zatwierdzonego wpisu ma wpływ na stronę operacyjną i finansową.

### <a name="operational-impact"></a>Wpływ operacyjny

Jeśli zatwierdzenie wpisu zostanie anulowane, rekord zatwierdzenia zostanie oznaczony jako **Przesłano**. Stan wpisu zostanie zmieniony na **Przesłane**. Na tym etapie członek zespołu projektu może schylić wpis bez przesyłania żądania prośby o zamówienie.

Osoba zatwierdzająca może zmienić wartości **ilości rozliczeniowej** i **typu faktury**, a następnie ponownie zatwierdzić wpis.

### <a name="financial-impact"></a>Wpływ finansowy

Jeśli zatwierdzenie wpisu zostanie anulowane, odpowiednie wartości rzeczywiste kosztów i sprzedaży są aktualizowane w następujący sposób:

- Pole **Stan korekty** zmienia wartość na **Skorygowano**.
- Pole **Stan rozliczania** zmienia wartość na **Anulowano**.

Następnie w tabeli Wartości rzeczywiste są tworzone wpisy wycofania. Aby utworzyć wpisy wycofania, system kopiuje wartości pól z pierwotnych wartości rzeczywistych. Jedyne wartości, które nie są kopiowane, to wartości ilości. Zamiast tego te wartości są wycofywane. Wycofane wartości rzeczywiste są tworzone dla wartości rzeczywistych **Koszt** i **Nierozliczona sprzedaż**. Pole **Stan korekty** w wycofanych wartościach rzeczywistych otrzymuje wartość **Nie można skorygować**, a pole **Stan rozliczania** otrzymuje wartość **Anulowano**. Ze względu na te zmiany zarejestrowane wydatki oraz zaległości przychodów w projekcie nie będą już uwzględniały kwot reprezentowanych przez te wartości rzeczywiste.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
