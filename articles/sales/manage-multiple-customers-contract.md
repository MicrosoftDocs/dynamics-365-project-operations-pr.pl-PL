---
title: Zarządzanie wieloma klientami w kontraktach projektu
description: Ten temat zawiera informacje o sposobach zarządzania wieloma klientami w kontraktach dotyczących projektu.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1adb786c36d43a148e8c5a8b25ded5a997557119f7e6e9e2248935ad4ed211d5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992084"
---
# <a name="manage-multiple-customers-on-project-contracts"></a>Zarządzanie wieloma klientami w kontraktach projektu

Ten temat zawiera informacje o sposobach zarządzania wieloma klientami w kontraktach dotyczących projektu. Kontraktu projektu można użyć, jeśli trzeba zawrzeć umowę kontraktową dotyczącą wielu klientów w celu finansowania transakcji. Na stronie **Kontrakt projektu** na karcie **Podsumowanie** znajdują się informacje dotyczące podstawowego klienta transakcji. Innych klientów uczestniczących w transakcji można dodać do karty **Klienci**.

Wszyscy klienci kontraktu na karcie **Klienci** kontraktu projektu są domyślnie ustawiani jako klienci pozycji kontraktu we wszystkich nowych pozycjach kontraktu tworzonych na podstawie kontraktu dotyczącego projektu. Żadne istniejące pozycje kontraktu oparte na projektach nie dziedziczą rekordów nowych klientów kontraktu, które zostaną utworzone później.

Możesz dodawać, aktualizować lub usuwać klientów kontraktu i pozycji kontraktu w dowolnym momencie przed wygraniem kontraktu. Klient w kontrakcie projektu musi zostać skonfigurowany jako klient w firmie lub podmiocie prawnym będącym właścicielem na stronie **Klienci**. Podmioty prawne są konfigurowane w module **Zarządzanie projektami i księgowanie** w aplikacji Dynamics 365 Project Operations i są dostępne jako firmy w modułach **Sprzedaż wg projektu** i **Dostarczanie** w aplikacji Project Operations.

## <a name="primary-customers"></a>Klienci podstawowi

Potencjalny klient na karcie **Podsumowanie** kontraktu projektu to podstawowy klient kontraktu. Klienta podstawowego nie można aktualizować z poziomu listy klientów kontraktu. Podczas próby usunięcia klienta podstawowego z listy klientów w kontrakcie wystąpi błąd z komunikatem informującym o tym, że rekordu podstawowego klienta w kontrakcie nie można usunąć. W zamian można zmienić klienta w polu **Potencjalny klient** na karcie **Podsumowanie** kontraktu projektu. W przypadku zaktualizowania tego pola nowy wybrany klient jest dodawany jako nowy klient kontraktu z flagą **Podstawowy** ustawioną na **Tak**. Poprzedni podstawowy klient jest nadal klientem w kontrakcie, ale nie jest już klientem podstawowym.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Tworzenie, aktualizowanie i usuwanie rekordu klienta

Klienta kontraktowego można utworzyć, zaktualizować lub usunąć na karcie **Klienci kontraktu** na stronie **Kontrakt**. Poniższe pola znajdują się w rekordzie klienta kontraktu w kontrakcie projektu.

| **Pole** | **Lokalizacja** | **Opis** | 
| --- | --- | --- | 
| Konto | Edytowana siatka na karcie **Klienci kontraktu** oraz strona główna i szybkiego tworzenia dla klienta kontraktu. | Lista wszystkich aktywnych kont. To pole jest zablokowane po utworzeniu rekordu. Aby zaktualizować rekord, musisz go usunąć i ponownie utworzyć. Jeśli zarejestrowano jakiekolwiek dane rzeczywiste lub rekord klienta objętego umową jest klientem głównym, nie można usunąć rekordu. Podczas tworzenia pozycji kontraktu klienci kontraktu są kopiowani jako klienci z pozycji kontraktu. |
| Procent podziału rozliczeń | Edytowana siatka na karcie **Klienci kontraktu** oraz strona główna i szybkiego tworzenia dla klienta kontraktu. | Reprezentuje procent każdej niezafakturowanej transakcji sprzedaży przypisany do klienta kontraktu. Podczas tworzenia nowych pozycji kontraktu projektu procent podziału rozliczeń jest kopiowany do wszystkich nowych pozycji kontraktu oraz do klientów w pozycji kontraktu projektu. |
| Nazwa kontaktu u płatnika | Edytowana siatka na karcie **Klienci kontraktu** oraz strona główna i szybkiego tworzenia dla klienta kontraktu. | To pole tekstowe powinno być używane do identyfikowania osoby kontaktowej faktury dla klienta. Wartość domyślna pochodzi z powiązanego rekordu konta. Nazwa kontaktu jest kopiowana do pola **Nazwa płatnika kontraktu** na fakturze wygenerowanej dla klienta. |
| Nazwa płatnika | Edytowana siatka na karcie **Klienci kontraktu** oraz strona główna i szybkiego tworzenia dla klienta kontraktu. | To pole służy do identyfikowania osoby kontaktowej faktury dla klienta. Wartość domyślna pochodzi z powiązanego rekordu konta. Nazwa jest kopiowana do pola **Nazwa płatnika kontraktu** na fakturze wygenerowanej dla klienta. |
| Warunki płatności | Edytowana siatka na karcie **Klienci kontraktu** oraz strona główna i szybkiego tworzenia dla klienta kontraktu. | Wartość domyślna pochodzi z powiązanego rekordu konta. Warunki są kopiowane do pola **Nazwa płatnika kontraktu** na fakturze wygenerowanej dla klienta. |
| Firma będąca właścicielem | Edytowana siatka na karcie **Klienci kontraktu projektu** oraz strona główna i szybkiego tworzenia dla klienta kontraktu projektu. | Podmiot prawny, w którym klient jest konfigurowany w module **Zarządzanie projektami i księgowanie**. To pole jest tylko do odczytu i ma ustawioną firmę będącą właścicielem kontraktu projektu.</br>Lista klientów do dodania w polu **Konto** jest już filtrowana na listę z tej firmy będącej właścicielem w module **Informacje o zarządzaniu projektami i ich księgowaniu** w Project Operations. Firma będąca właścicielem to podmiot prawny w module **Zarządzanie projektami i księgowanie** w aplikacji Project Operations. Wszystkie koszty i przychód z projektu są uwzględnione w księdze głównej firmy będącej właścicielem. |
| Zaokrągla | Edytowana siatka na karcie **Klienci kontraktu** oraz strona główna i szybkiego tworzenia dla klienta kontraktu. | Wskazuje, czy klient jest domyślnym klientem zaokrąglającym na potrzeby transakcji. W kontrakcie projektu może się znajdować tylko jeden klient zaokrąglenia. Jeśli podział kosztów i niezafakturowanej sprzedaży pod kątem ilości prowadzi do różnicy zaokrąglania, ta różnica jest stosowana względem wartości rzeczywistej mapowanej na klienta. |
| Nieprzekraczalny limit | Edytowana siatka na karcie **Klienci kontraktu** oraz strona główna i szybkiego tworzenia dla klienta kontraktu. | Wskazuje, czy istnieje wynegocjowany limit lub limit całkowitej kwoty, która zostanie zafakturowana dla klienta w ramach interakcji. Nieprzekraczalny limit skonfigurowany na poziomie klienta kontraktu jest oceniany na podstawie wartości rzeczywistych niezafakturowanej sprzedaży, które odwołują się do klienta kontraktu. |

## <a name="edit-billing-split-percentages"></a>Edytowanie procentu podziału rozliczeń

Procent podziału rozliczeń można edytować w obrębie siatki. Jeśli suma procentów podziału rozliczeń jest inna niż 100 procent, występuje błąd. Po zmodyfikowaniu procentu podziału rozliczeń odśwież stronę **Kontrakt projektu**, aby usunąć błąd.

Można również wybrać opcję **Rozłóż równomiernie** w podsiatce klientów kontraktu projektu. Podziały rozliczeń są równomiernie alokowane do wszystkich klientów kontraktu projektu. Jeśli istnieje współczynnik zaokrąglania, zostanie on dodany do klienta zaokrąglającego. Jeden z klientów kontraktu ma zawsze flagę **Zaokrąglanie** ustawioną na **Tak**. Jest to klient zaokrąglający. Zazwyczaj klient zaokrąglający jest również podstawowym klientem kontraktu, ale nie jest to wymagane.


[!INCLUDE[footer-include](../includes/footer-banner.md)]