---
title: Praca z pozycjami kontraktu opartymi na projekcie
description: Ten temat zawiera informacje o pozycjach kontraktów opartych na projektach.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 14d880eccd5547c122ebe37b63022e64fa2fb6fe
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181734"
---
# <a name="work-with-projectbased-contract-lines"></a>Praca z pozycjami kontraktu opartymi na projekcie

Linie umowy oparte na projekcie w Dynamics 365 Project Operations są przeznaczone do przechowywania szacunkowych i rozliczeniowych umów dla określonych komponentów pracy projektowej na zlecenie. Struktura pozycji kontraktu opartej na projekcie jest rozszerzana na oszacowania projektów i scenariusze fakturowania przy użyciu następujących koncepcji:

- Metoda rozliczania
- Mapowanie projektów i zadań
- Dołączone klasy transakcji
- Nieprzekraczalny limit
- Konfiguracja odpłatności
- Oszacowania przy użyciu szczegółów pozycji kontraktu
- Klient pozycji kontraktu

Poniższe pola znajdują się na karcie **Ogólne** w pozycjach kontraktu opartego na projektach. Te pola pomagają w konfigurowaniu podstawy dla konkretnego szacunkowego oszacowania kosztów i sposobu fakturowania przy pracy opartej na projekcie.

| Pole | Opis | Wpływ zmian w dalszych etapach |
| --- | --- | --- |
| **Nazwa/nazwisko** | Nazwa pozycji kontraktu, która identyfikuje dyskretny składnik szacowanego kontraktu. W przypadku kontraktu projektu utworzonego z oferty ta wartość jest kopiowana z odpowiedniej wartości wiersza oferty opartej na projekcie. | Ta wartość pola jest kopiowana do wiersza faktury projektu tworzonego z tej pozycji kontraktu podczas tworzenia faktury. |
| **Metoda rozliczania** | W umowie dotyczącej projektu utworzonej na podstawie oferty ta wartość jest kopiowana z odpowiedniego pola w wierszu oferty. Jest to zestaw opcji reprezentujący dwa główne modele zamawiające, które są obsługiwane przez Project Operations:</br>- **Stała cena**</br>- **Czas i materiał** | Na podstawie metody fakturowania przywoływanego wiersza kontraktu zostanie przetworzona transakcja rzeczywista. Jeśli dana pozycja kontraktu zawiera metodę fakturowania czasu i materiału, tworzone są rekordy kosztów i niezafakturowanego rekordu sprzedaży. Jeśli pozycja kontraktu, do której odwołuje się wartość rzeczywista, ma metodę fakturowania z ceną ustaloną, zostanie utworzona tylko wartość rzeczywista kosztu. |
| **Project** | To pole służy do identyfikowania projektu, który będzie używany do dostarczania pracy nad tym zakontraktowaniem. | Wartość w tym polu jest używana w połączeniu z **Uwzględnione zadania** i **Uwzględnione klasy transakcji** w celu ustalenia odwołania do pozycji kontraktu w rekordzie rzeczywistym lub w wierszu szacowania. |
| **Uwzględnij czas** | Flaga wskazuje, czy w danej pozycji kontraktu znajdują się transakcje czasowe czy koszty robocizny. Wartość **Nie** oznacza, że transakcje godzinowe lub koszty robocizny nie zostaną uwzględnione w tej pozycji kontraktu. Wartość **Tak** oznacza, że będą. | Ta wartość pola jest używana w połączeniu z projektem w celu rozwiązania odniesienia do wiersza kontraktu w rekordzie wiersza rzeczywistego lub szacunkowego. |
| **Uwzględnij wydatek** | Flaga wskazuje, czy koszty wydatków w wybranym projekcie zostaną uwzględnione w tej pozycji kontraktu. Wartość **Nie** oznacza, że koszt wydatków nie zostanie uwzględniony w tej pozycji kontraktu. Wartość **Tak** oznacza, że będzie. | Ta wartość pola jest używana w połączeniu z projektem w celu rozwiązania odniesienia do wiersza kontraktu w rekordzie wiersza rzeczywistego lub szacunkowego. |
| **Uwzględnij opłatę** | Flaga wskazuje, czy opłaty w wybranym projekcie zostaną uwzględnione w tej pozycji kontraktu. Wartość **Nie** oznacza, że opłaty nie będą uwzględnione w tej pozycji kontraktu. Wartość **Tak** oznacza, że będą. | Ta wartość pola jest używana w połączeniu z projektem w celu rozwiązania odniesienia do wiersza kontraktu w rekordzie wiersza rzeczywistego lub szacunkowego. |
| **Zakontraktowana kwota** | W pozycji kontraktu o stałej cenie jest to wartość ustalona, która zostanie zafakturowana klientowi dla wszystkich składników pracy skojarzonych z daną pozycją kontraktu. W pozycji umowy dotyczącej czasu i materiałów kwota ta jest szacunkową wartością tego, co zostanie zafakturowane klientowi za wszystkie składniki pracy związane z tą pozycją kontraktu. W umowie dotyczącej projektu utworzonej na podstawie oferty ta wartość jest kopiowana z odpowiedniego pola w wierszu oferty. Kiedy pozycja kontraktu oparta na projekcie zawiera szczegółowe informacje o wierszach, to pole jest zablokowane do edycji i jest sumowane od kwoty podanej we wszystkich pozycjach kontraktu. | W przypadku, gdy pozycja kontraktu zawiera szczegółowe informacje o wierszach, ta wartość może zostać zmodyfikowana, zmieniając kwoty w szczegółach wiersza. W pozycji kontraktu o stałej cenie ta wartość jest używana do generowania kwoty przed podatkami dotyczącymi okresowych punktów kontrolnych rozliczania. |
| **Szacowany podatek** | Użytkownik może edytować to pole, aby wprowadzić szacowaną kwotę podatku w pozycji kontraktu. Kiedy pozycja kontraktu oparta na projekcie zawiera szczegółowe informacje o wierszach, to pole jest zablokowane do edycji i jest sumowane podatku od kwoty podanej we wszystkich pozycjach kontraktu. | W przypadku, gdy pozycja kontraktu zawiera szczegółowe informacje o wierszach, ta wartość może zostać zmodyfikowana, zmieniając kwoty podatku w szczegółach wiersza. W pozycji kontraktu o stałej cenie ta wartość jest używana do generowania podatków dotyczących okresowych punktów kontrolnych rozliczania. |
| **Zakontraktowana kwota po opodatkowaniu** | Zakontraktowana kwota pozycji kontraktu po opodatkowaniu. To pole jest tylko do odczytu i jest obliczane jako **Kwota w kontrakcie + podatek**. | W pozycji kontraktu o stałej cenie ta wartość jest używana do generowania okresowych punktów kontrolnych fakturowania. |
| **Nieprzekraczalny limit** | Użytkownik może edytować to pole, ale jest dostępne tylko w wierszach kontraktów opartych na projektach, które zawierają metodę fakturowania typu czas i materiały. | Użytkownik może edytować to pole. Gdy rzeczywisty czas lub koszt odnosi się do tej pozycji kontraktu pod względem czasu i materiałów, kwota rzeczywista jest oceniana na podstawie nieprzekraczalnego limitu w tej pozycji umowy po uwzględnieniu już wydanych i zatwierdzonych kwot. |
| **Budżet klienta** | To pole jest edytowalne i jest kopiowane z odpowiedniego pola w wierszu oferty, jeśli umowa została utworzona na podstawie oferty. | To pole jest używane tylko do informowania i nie ma żadnych elementów podrzędnych. |

## <a name="validation-rule-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Reguła sprawdzania poprawności opcji na karcie Ogólne w wierszach kontraktu opartego na projektach

Reguła: projekt i określona klasa transakcji może zawierać tylko jeden wiersz kontraktu opartego na projektach w kontrakcie.

| Kontrakt | Pozycja kontraktu | Project | Uwzględnij czas | Uwzględnij wydatek | Uwzględnij opłatę | Prawidłowe/nieprawidłowe | Przyczyna                                                                                                                                                                                                  |
|----------|---------------|---------|--------------|-----------------|-------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| C1       | CL1           | O1      | Tak          | Tak             | Tak         | Nieprawidłowe       | Narusza regułę. Godziny, wydatek i opłaty w projekcie P1 są uwzględnione zarówno na pozycjach kontraktu, jak i CL1 i CL2.                                                                                       |
| C1       | CL2           | O1      | Tak          | Tak             | Tak         | Nieprawidłowe       | Narusza regułę. Godziny, wydatek i opłaty w projekcie P1 są uwzględnione zarówno na pozycjach kontraktu, jak i CL1 i CL2.                                                                                       |
| C1       | CL1           | O1      | Tak          | No              | Tak         | Nieprawidłowe       | Narusza regułę. Godziny i  opłaty w projekcie P1 są uwzględnione zarówno na pozycjach kontraktu, jak i CL1 i CL2.                                                                                                   |
| C1       | CL2           | O1      | Tak          | Tak             | Tak         | Nieprawidłowe       | Narusza regułę. Godziny i  opłaty w projekcie P1 są uwzględnione zarówno na pozycjach kontraktu, jak i CL1 i CL2.                                                                                                   |
| C1       | CL1           | O1      | Tak          | No              | Tak         | Prawidłowe           | Godziny i opłaty z projektu P1 są uwzględnione na CL1. Wydatki projektu P1 są zawarte w CL2. </br>   W każdym wierszu kontraktu nie ma zakładki, która jest więc ważna.  |
| C1       | CL2           | O1      | No           | Tak             | No          | Prawidłowe           | Godziny i opłaty z projektu P1 są uwzględnione na CL1. Wydatki projektu P1 są zawarte w CL2. </br>   W każdym wierszu kontraktu nie ma zakładki, która jest więc ważna.  |
| C1       | CL1           | O1      | Tak          | Tak             | Tak         | Nieprawidłowe       | Narusza regułę. Godziny, wydatek i opłaty w projekcie P1 są uwzględnione w pozycjach obu kontraktów.                                                                                               |
| CL2      | CL2           | O1      | Tak          | Tak             | Tak         | Nieprawidłowe       | Narusza regułę. Godziny, wydatek i opłaty w projekcie P1 są uwzględnione w pozycjach obu kontraktów.                                                                                               |
