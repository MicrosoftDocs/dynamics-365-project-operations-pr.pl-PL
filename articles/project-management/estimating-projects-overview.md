---
title: Omówienie szacowania projektu
description: W tym temacie zamieszczono informacje o szacowaniu w Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8e7ee4888a907b9d8c3ce06c1597f6b05be84477
ms.sourcegitcommit: 6eb26bab511ec09201ab70c3e2808dece3f74c4c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/07/2020
ms.locfileid: "3968056"
---
# <a name="estimate-projects-overview"></a>Omówienie szacowania projektu

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

W ofercie opartej na projekcie można za pomocą encji **Szczegóły wiersza** oferty oszacować pracę wymaganą do zrealizowania projektu. Następnie ten szacunek można udostępnić klientowi.

Wiersze oferty opartej na projekcie mogą mieć zero szczegółów wierszy oferty. Szczegóły wierszy oferty służą do szacowania czasu, wydatków lub opłat. W programie Microsoft Dynamics 365 Project Operations nie są dozwolone oszacowania materiału w szczegółach wierszy oferty. Takie szacunki są nazywane klasami transakcji. W klasach transakcji można również wprowadzać szacowane kwoty podatków.

Oprócz klas transakcji szczegóły wierszy oferty mają także typ transakcji. Istnieją dwa obsługiwane typy transakcji w szczegółach wierszy oferty: **Koszt** i **Kontrakt projektu**.

## <a name="estimate-by-using-a-contract"></a>Szacowanie za pomocą kontraktu

Jeśli podczas tworzenia kontraktu opartego na projekcie użyto oferty z systemu, oszacowanie wykonane dla każdego wiersza oferty w ofercie jest kopiowane do kontraktu na projekt. Struktura kontraktu projektu przypomina strukturę oferty na projekt z wierszami, szczegółami wierszy i harmonogramami fakturowania.

Oszacowania można wykonywać bezpośrednio w kontrakcie na projekt, podobnie jak w ofercie na projekt. W przypadku oferty projektu szacowanie odbywa się za pomocą pozycji kontraktu i szczegółów pozycji kontraktu. Szczegóły pozycji kontraktu można również wygenerować z poziomu planu projektu, który został utworzony przy użyciu metody szacowania oddolnego.

Szczegóły pozycji kontraktu mogą służyć do szacowania czasu, wydatków lub opłat. W szczegółach pozycji kontraktu można również wprowadzać szacowane kwoty podatków.

Nie są dozwolone oszacowania materiału w szczegółach pozycji kontraktu.

W kontrakcie na projekt są obsługiwane procesy tworzenia i potwierdzania faktur. Tworzenie faktury polega na utworzeniu wersji roboczej faktury opartej na projekcie, która obejmuje wszystkie nierozliczone wartości rzeczywiste sprzedaży aż do bieżącego dnia.

Potwierdzenie powoduje, że kontrakt staje się tylko do odczytu i zmienia stan z **Wersja robocza** na **Potwierdzony**. Po wykonaniu tej czynności nie można jej cofnąć. Ponieważ ta operacja jest nieodwracalna, najlepszym rozwiązaniem jest utrzymywanie kontraktu w stanie **Wersja robocza**.

Jedyna różnica między kontraktami w wersji roboczej i potwierdzonymi to ich status oraz fakt, że kontrakty w wersji roboczej można edytować, a kontraktów potwierdzonych nie. Tworzenie faktur i śledzenie wartości rzeczywistych można wykonywać zarówno wobec kontraktów w wersji roboczej, jak i kontraktów potwierdzonych.

Project Operations nie obsługuje zleceń zmian w kontraktach ani projektach.

## <a name="estimating-projects"></a>Szacowanie projektów

W projektach można szacować czas i wydatki. Project Operations nie pozwala na szacowanie materiałów ani opłat w projektach.

Oszacowania czasu są generowane podczas tworzenia zadania i identyfikowania atrybutów standardowego zasobu wymaganego do wykonania zadania. Szacunki czasu są generowane na podstawie zadań planowania. Szacunki czasu nie są tworzone w przypadku tworzenia ogólnych członków zespołu poza kontekstem harmonogramu.

Oszacowania wydatków są wprowadzane w siatce na stronie **Szacunki**.

## <a name="understanding-estimation"></a>Informacje o szacowaniu

Poniższa tabela pomoże zrozumieć logikę biznesową stosowaną w fazie szacowania.

| Scenariusz                                                                                                                                                                                                                                                                                                                                          | Rekord encji                                                                                                                                                                                                       | Typ transakcji | Klasa transakcji | Informacje dodatkowe                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Trzeba oszacować wartości sprzedaży dla czasu w ofercie                                                                                                                                                                                                                                                                                    | Jest tworzony rekord szczegółów wiersza oferty (QLD)                                                                                                                                                                               | Kontrakt projektu | Time        | Pole Początkowy rekord transakcji w wierszu QLD po stronie sprzedaży odwołuje się do QLD po stronie kosztu |
|                                                                                                                                                                                                                                                                                     | System tworzy drugi rekord QLD w celu przechowywania odnośnych wartości kosztów. System kopiuje wszystkie pola niepieniężne z QLD sprzedaży do QLD kosztu.                                                                                                                                                                               | Koszt | Time        | Pole Początkowy rekord transakcji w wierszu szczegółów wiersza oferty (QLD) po stronie sprzedaży odwołuje się do QLD po stronie kosztu |
| Trzeba oszacować wartości sprzedaży dla czasu w kontrakcie                                                                                                                                                                                                                                                                                 | Jest tworzony rekord szczegółów pozycji kontraktu projektu (CLD)                                                                                                                                                                    | Kontrakt projektu | Time        | Pole Początkowy rekord transakcji w wierszu CLD po stronie sprzedaży odwołuje się do CLD kosztu      |
|                                                                                                                                                                                                                                                                                  | System tworzy drugi rekord CLD w celu przechowywania odnośnych wartości kosztów. System kopiuje wszystkie pola niepieniężne z CLD sprzedaży do CLD kosztu.                                                                                                                                                                    | Koszt | Time        | Pole Początkowy rekord transakcji w wierszu CLD po stronie sprzedaży odwołuje się do CLD kosztu      |
| Użytkownik opisuje zasób w zadaniu projektu                                                                                                                                                                                                                                                                                            | Podczas tworzenia zadania jest tworzony rekord wiersza szacowania ze wszystkimi wymaganymi wymiarami kalkulacji cen pokazujący wartość sprzedaży dla zadania. Rola i jednostki organizacyjne są gotowymi wymiarami kalkulacji cen | Kontrakt projektu | Czas        |                                                                                   |
|     | Podczas tworzenia zadania jest tworzony rekord wiersza szacowania ze wszystkimi wymaganymi wymiarami kalkulacji cen pokazujący wartość kosztu dla zadania. System kopiuje wszystkie pola niepieniężne z wiersza szacowania sprzedaży do wiersza szacowania kosztu. Rola i jednostka organizacyjna są gotowymi wymiarami kalkulacji cen dla kosztu i stawek rozliczania.                                                                                                                                                                                                                | Koszt             | Czas           |                                                                                   |



## <a name="customize-the-quote-line-detail-and-contract-line-detail-entities"></a>Dostosowywanie encji Szczegóły wiersza oferty i Szczegóły pozycji kontraktu

Jeśli w szczegółach wiersza oferty dodano pole niestandardowe, a chcesz, aby system wprowadził wartość tego pola jako wartość domyślną w tworzonym pokrewnym wierszu kosztu, należy użyć narzędzi do rejestrowania dodatków plug-in **PreOperationContractLineDetailUpdate** i **PreOperationQuoteLineDetailUpdate**. Te dodatki plug-in należy ponownie zarejestrować po zmodyfikowaniu szczegółów wiersza oferty lub szczegółów pozycji kontraktu. Poniżej znajduje się odpowiednia procedura.

1. Otwórz narzędzie PluginRegistrationTool i nawiąż połączenie z wystąpieniem online.
2. Wybierz opcję **Wyszukaj** i poszukaj dodatku plug-in, który ma zostać zaktualizowany.
3. Zaznacz dodatek plug-in, a następnie na stronie głównej wybierz opcję **Wybierz**.
4. Zaznacz krok dodatku plug-in, który chcesz zaktualizować, kliknij prawym przyciskiem myszy, a następnie wybierz opcję **Aktualizuj**.
5. W oknie dialogowym **Aktualizowanie istniejącego kroku** w polu **Atrybuty filtrowania** kliknij przycisk wielokropka (**...**):
6. W oknie dialogowym **Wybieranie atrybutów** zaznacz pola wyboru atrybutów niestandardowych.
7. Kliknij przycisk **OK**, aby zamknąć okno dialogowe, a następnie wybierz pozycję **Aktualizuj krok**.
8. Powtórz kroki od 1 do 7 dla drugiego dodatku plug-in.
9. Zamknij narzędzie **PluginRegistrationTool**.
