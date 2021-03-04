---
title: Anulowanie zatwierdzonych wcześniej wpisów czasu i wydatku
description: Ten temat zawiera informacje o sposobie anulowania zatwierdzonej transakcji rozliczanej według czasu i wydatku.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ea42c6755b4b48d986e385879607d659c57f483d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150591"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a>Anulowanie zatwierdzonych wcześniej wpisów czasu lub wydatku

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

W najnowszej wersji programu Dynamics 365 Project Service Automation osoby zatwierdzające mogą anulować wpisy czasu lub wydatku, które zostały wcześniej zatwierdzone.

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a>Anulowanie zatwierdzonego wcześniej wpisu czasu lub wydatku

Wykonaj te kroki, aby anulować wpis czasu lub wydatku, który wcześniej został przez Ciebie zaakceptowany.

1. Wybierz kolejno opcje **Projekty** \> **Moja praca** \> **Zatwierdzenia**.
2. Na stronie listy **Zatwierdzenia** zmień widok na **Moje przeszłe zatwierdzenia**. Zostanie wyświetlona lista wpisów czasu i wydatku uprzednio zatwierdzonych przez Ciebie.
3. Zaznacz jeden lub więcej wpisów, a następnie kliknij przycisk **Anuluj zatwierdzenie**. Zostanie wyświetlony komunikat ostrzegawczy.
4. Kliknij przycisk **OK**, aby anulować zatwierdzenie.

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a>Informacje o skutkach anulowania zatwierdzania wpisu czasu lub wydatku

Anulowanie zatwierdzonego wpisu ma wpływ na stronę operacyjną i finansową.

### <a name="operational-impact"></a>Wpływ operacyjny

Pod względem operacyjnym po anulowaniu zatwierdzenia stan rekordu jest resetowany do wartości **Wersja robocza**, a zatwierdzenie nie jest już wyświetlane w widoku **Moje przeszłe zatwierdzenia**. Zamiast tego anulowane zatwierdzenie jest wyświetlane w widoku **Wpisy czasu do zatwierdzenia** lub widoku **Wpisy wydatków do zatwierdzenia**, w zależności od tego, czy był to wpis czasu, czy wydatku. Ponadto stan pokrewnego wpisu czasu lub wydatku zmienia się na **Przesłano**, tak aby ów wpis był spójny z zatwierdzeniami mającymi stan **Wersja robocza**.

Jako osoba zatwierdzająca, możesz edytować niektóre pola zatwierdzania mającego stan **Wersja robocza**. Są to pola **Typ rozliczania** oraz **Godziny podlegające rozliczeniu dla wpisów czasu**. Po dokonaniu zmian możesz ponownie zatwierdzić rekord. Alternatywnie możesz odrzucić wpis. Odrzucenie zatwierdzenia wpisu czasu spowoduje zmianę stanu wpisu na **Zwrócono**. Odrzucenie zatwierdzenia wpisu wydatku spowoduje zmianę stanu wpisu na **Odrzucono**. Pod względem funkcjonalnym wpisy zwrócone i odrzucone zachowują się tak samo, jak wpisy o stanie **Wersja robocza**. Członek zespołu projektu może wprowadzić wszelkie wymagane zmiany we wpisie i ponownie go przesłać do zatwierdzenia albo całkowicie usunąć wpis.

### <a name="financial-impact"></a>Wpływ finansowy

Anulowanie zatwierdzenia wpływa również finansowo na projekt. Najpierw odnośne wartości rzeczywiste dotyczące kosztu i sprzedaży są aktualizowane w następujący sposób:

- Stan korekty jest ustawiany jako **Skorygowano**.
- Stan rozliczania jest ustawiany jako **Anulowano**.

Następnie w tabeli Wartości rzeczywiste są tworzone wpisy wycofania. Aby utworzyć wpisy wycofania, system kopiuje wartości pól z pierwotnych wartości rzeczywistych. Jedyne wartości, które nie są kopiowane, to wartości ilości. Zamiast tego te wartości są wycofywane. Wycofane wartości rzeczywiste są tworzone dla wartości rzeczywistych **Koszt** i **Nierozliczona sprzedaż**. Pole **Stan korekty** w wycofanych wartościach rzeczywistych otrzymuje wartość **Nie można skorygować**, a stan rozliczania otrzymuje wartość **Anulowano**.

Po wprowadzeniu tych zmian kwota zarejestrowana jako wydana w projekcie oraz zaległości przychodów w projekcie nie będą już uwzględniały kwot reprezentowanych przez te wartości rzeczywiste.
