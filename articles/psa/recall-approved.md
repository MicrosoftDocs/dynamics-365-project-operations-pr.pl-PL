---
title: Odwoływanie zatwierdzonych wpisów czasu lub wydatku
description: Ten temat zawiera informacje o sposobie odwoływania uprzednio zatwierdzonej transakcji rozliczanej według czasu lub transakcji wydatku.
author: rumant
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 71f75c1c516ca6e652baf311aa14e0c3fd4ba81e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998199"
---
# <a name="recall-approved-time-or-expense-entries"></a>Odwoływanie zatwierdzonych wpisów czasu lub wydatku

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Członek zespołu projektu lub inna osoba, która prześle wpis czasu lub wydatku, może odwołać ten wpis po jego zatwierdzeniu. Proces odwoływania zatwierdzanego wpisu czasu lub wydatku ma dwa etapy:

1. Osoba przesyłająca prosi o odwołanie.
2. Osobna zatwierdzająca akceptuje odwołanie.

## <a name="request-a-recall"></a>Wnioskowanie o odwołanie

Wykonaj te kroki, aby poprosić o odwołanie zatwierdzonego wpisu czasu lub wydatku.

1. W przypadku wpisów czasu wybierz kolejno opcje **Projekty** \> **Moja praca** \> **Wpis czasu**.

    –lub–

    W przypadku wpisów wydatku wybierz kolejno opcje **Projekty** \> **Moja praca** \> **Wydatki**.

2. W przypadku wpisów czasu zaznacz wszystkie wpisy czasu dla określonej kombinacji projektu i zadania. Alternatywnie w siatce zaznacz poszczególne komórki czasu w określonym dniu określonego projektu.

    –lub–

    W przypadku wpisów wydatków zaznacz wiersz wpisu wydatku, który ma zostać odwołany.

3. Wybierz pozycję **Odwołaj**. Pojawia się okno dialogowe potwierdzenia. Jeśli zaznaczone wpisy czasu i wydatku były już zatwierdzone, zostanie wyświetlony monit o podanie przyczyny odwołania.
4. Wprowadź przyczynę odwołania, a następnie wybierz przycisk **OK**, aby potwierdzić operację. System wyśle do użytkownika, który zatwierdził wpisy, prośbę o zatwierdzenie odwołania.

> [!NOTE]
> Mimo że zatwierdzone wpisy czasu i wydatków można odwoływać, to jeśli za zatwierdzony czas lub wydatek już wystawiono odbiorcy fakturę, nie można utworzyć żądania odwołania. Użytkownik próbujący utworzyć żądanie odwołania zobaczy komunikat informujący o tym, że nie można odwołać wpisu czasu lub wydatku, ponieważ został on już zafakturowany.

## <a name="approve-or-reject-a-recall-request"></a>Zatwierdzanie lub odrzucanie żądania odwołania

Wykonaj te kroki, aby zatwierdzić lub odrzucić żądanie odwołania.

1. Wybierz kolejno opcje **Projekty** \> **Moja praca** \> **Zatwierdzenia**.
2. Na stronie listy **Zatwierdzenia** zmień widok na **Żądania odwołania do zatwierdzenia**. Zostanie wyświetlona lista przesłanych żądań odwołania.
3. Zaznacz jeden lub więcej wpisów, a następnie kliknij przycisk **Zatwierdź** lub **Odrzuć**.
4. W przypadku wybrania opcji **Zatwierdź** zostanie wyświetlony komunikat ostrzegawczy zawierający opis skutków zatwierdzenia. Wybierz pozycję **OK**, aby potwierdzić operację. Żądanie odwołania zostanie zatwierdzone.

    –lub–

    W przypadku wybrania opcji **Odrzuć** żądanie odwołania zostanie odrzucone.

> [!NOTE]
> Podobnie jak w przypadku wnioskowania o odwołanie, podczas zatwierdzania odwołania system sprawdza wszelkie ewentualne czynności fakturowania wpisów czasu lub wydatku. Jeśli wpis został już zafakturowany lub jeśli znajduje się on w wersji roboczej faktury, osoba zatwierdzająca zobaczy komunikat o błędzie z informacją, że nie można zatwierdzić odwołania czasu lub wydatku, ponieważ został on już zafakturowany.

## <a name="impact-of-a-recall-request"></a>Wpływ żądania odwołania

Odwołanie zatwierdzonego wpisu ma wpływ na stronę operacyjną i finansową.

### <a name="operational-impact"></a>Wpływ operacyjny

Jeśli żądanie odwołania zostanie zatwierdzone, rekord zatwierdzenia jest oznaczany jako **Odrzucono**. Stan wpisu zmieni się na **Zwrócono** lub **Odrzucono**, w zależności od tego, czy jest to wpis czasu, czy wpis wydatku.

Członek zespołu projektu może wyświetlać wpisy, edytować je i ponownie wysyłać albo całkowicie usuwać.

Jeśli żądanie odwołania zostanie odrzucone, wpis zachowuje stan **Zatwierdzono**, a wpisu nie może edytować członek zespołu projektu ani osoba zatwierdzająca w projekcie.

### <a name="financial-impact"></a>Wpływ finansowy

Jeśli żądanie odwołania zostanie zatwierdzane, odnośne wartości rzeczywiste dotyczące kosztu i sprzedaży są aktualizowane w następujący sposób:

- Pole **Stan korekty** zmienia wartość na **Skorygowano**.
- Pole **Stan rozliczania** zmienia wartość na **Anulowano**.

Następnie w tabeli Wartości rzeczywiste są tworzone wpisy wycofania. Aby utworzyć wpisy wycofania, system kopiuje wartości pól z pierwotnych wartości rzeczywistych. Jedyne wartości, które nie są kopiowane, to wartości ilości. Zamiast tego te wartości są wycofywane. Wycofane wartości rzeczywiste są tworzone dla wartości rzeczywistych **Koszt** i **Nierozliczona sprzedaż**. Pole **Stan korekty** w wycofanych wartościach rzeczywistych otrzymuje wartość **Nie można skorygować**, a pole **Stan rozliczania** otrzymuje wartość **Anulowano**. Ze względu na te zmiany zarejestrowane wydatki oraz zaległości przychodów w projekcie nie będą już uwzględniały kwot reprezentowanych przez te wartości rzeczywiste.

Jeśli żądanie odwołania zostanie odrzucone, nie ma żadnego wpływu finansowego na projekt.

## <a name="changes-to-time-entry-records"></a>Zmiany w rekordach wpisów czasu

Na poniższej ilustracji pokazano zmiany występujące w zatwierdzonych wpisach czasu po ich odwołaniu.

![Zmiany stanu wpisu czasu](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a>Zmiany w rekordach wpisu wydatku

Na poniższej ilustracji pokazano zmiany występujące w zatwierdzonych wpisach wydatków po ich odwołaniu.

![Zmiany stanu wpisu wydatku](media/ExpenseEntryStateTransitions.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]