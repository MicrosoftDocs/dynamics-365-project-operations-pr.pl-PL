---
title: Zarządzanie wieloma klientami w kontraktach projektu
description: W tym artykule przedstawiono informacje na temat zarządzania wieloma klientami w kontraktach projektów.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 001c3c822a5d1cef6bd85164ef5e63e81719dafb
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824546"
---
# <a name="manage-multiple-customers-on-project-contracts"></a>Zarządzanie wieloma klientami w kontraktach projektu

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Umowy dotyczące projektów w Dynamics 365 Project Operations obsługują scenariusz, w którym umowa dotyczy wielu klientów, którzy finansują transakcję. Karta **Podsumowanie** na stronie **Kontrakt projektu** zawiera pole **Klient**. To pole Identyfikuje podstawowego klienta transakcji. Informacje o innych klientach związanych z transakcjami można skonfigurować na karcie **Klienci** na stronie **Kontrakt projektu**.

Wszyscy kontrahenci kontraktów występujący w kontrakcie projektu jako domyślny dla wszystkich nowych wierszy kontraktu tworzonych na podstawie projektu, które są tworzone dla kontraktu dotyczącego projektu. Istniejące pozycje kontraktu oparte na projektach nie dziedziczą nowych klientów kontraktowych podczas tworzenia nowych rekordów.

Pozycje kontraktu oparte na produktach są automatycznie kojarzone z klientem podstawowym.

Klienci kontraktów i pozycje kontraktu mogą być dodani, aktualizowane lub usuwane w dowolnym momencie przed wygraniem kontraktu.

## <a name="primary-customer"></a>Klient podstawowy

Klient, który jest wymieniony na karcie **Podsumowanie** kontraktu projektu jako potencjalny klient, jest głównym klientem kontraktu. Podczas próby usunięcia klienta podstawowego z listy klientów w kontrakcie zostanie wyświetlony komunikat o błędzie informujący, że rekordu podstawowego klienta w kontrakcie nie można usunąć.

Klienta podstawowego nie można zaktualizować z poziomu listy klienci kontraktów. Zamiast tego można zmienić potencjalnego klienta na karcie **Podsumowanie** kontraktu. Po zaktualizowaniu tego pola na stronie **Podsumowanie kontraktu** nowy klient jest dodawany jako nowy klient kontraktowy z ustawioną flagą **Podstawowy**. Poprzedni podstawowy klient nadal będzie klientem kontraktu.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Tworzenie, aktualizowanie i usuwanie rekordu klienta

Klienta kontraktowego można utworzyć, zaktualizować lub usunąć, korzystając z karty **Klienci** na stronie **Kontrakt projektu**. Pola w poniższej tabeli znajdują się w rekordzie kontraktu dotyczącego kontraktu dotyczącego projektu i należy pamiętać o jego zachowaniu podczas pracy z kontraktem.

| Pole | Lokalizacja | Opis | Wpływ zmian w dalszych etapach |
| --- | --- | --- | --- |
| **Klient** | Siatkę można edytować na karcie **Klienci kontraktowi** i formularze **Główny** i **Szybkie tworzenie** dla klienta z pozycjami kontraktu. | Lista wszystkich aktywnych kont. To pole jest zablokowane po utworzeniu rekordu. Aby zaktualizować konto, usuń rekord i utwórz go ponownie. Jeśli zarejestrowano jakiekolwiek dane rzeczywiste lub rekord klienta objętego umową jest klientem głównym, nie można usunąć rekordu. | Podczas tworzenia pozycji kontraktu klienci kontraktowi są kopiowani jako klienci z wiersza kontraktu. |
| **Procent podziału rozliczeń** | Siatkę można edytować na karcie **Klienci kontraktowi** i formularze **Główny** i **Szybkie tworzenie** dla klienta z pozycjami kontraktu. | Reprezentuje odsetek każdej niezafakturowanej transakcji sprzedaży, który jest przypisany do tego klienta objętego umową. | Kopiowany na nowe pozycje kontraktu i do klientów w pozycji kontraktu projektu we wszystkich pozycjach kontraktu projektu. |
| **Nazwa kontaktu u płatnika** | Siatkę można edytować na karcie **Klienci kontraktowi** i formularze **Główny** i **Szybkie tworzenie** dla klienta z pozycjami kontraktu. | To pole tekstowe ma służyć do identyfikowania osoby kontaktowej dla faktury u danego klienta. Wartość domyślna tego pola jest określana na podstawie rekordu konta pokrewnego. | Wartość skopiowana do pola **Nazwa płatnika kontraktu** na fakturze wygenerowanej dla danego klienta. |
| **Nazwa płatnika** | Siatkę można edytować na karcie **Klienci kontraktowi** i formularze **Główny** i **Szybkie tworzenie** dla klienta z pozycjami kontraktu | To pole tekstowe ma służyć do identyfikowania osoby kontaktowej dla faktury u danego klienta. Wartość domyślna tego pola jest określana na podstawie rekordu konta pokrewnego. | Wartość skopiowana do pola **Nazwa płatnika kontraktu** na fakturze wygenerowanej dla danego klienta. |
| **Warunki płatności** | Siatkę można edytować na karcie **Klienci kontraktowi** i formularze **Główny** i **Szybkie tworzenie** dla klienta z pozycjami kontraktu. | Wartości domyślne z powiązanego rekordu konta. | Wartość skopiowana do pola **Nazwa płatnika kontraktu** na fakturze wygenerowanej dla danego klienta. |
| **Zaokrągla** | Siatkę można edytować na karcie **Klienci kontraktowi** i formularze **Główny** i **Szybkie tworzenie** dla klienta z pozycjami kontraktu. | Wskazuje, czy ten klient jest domyślnym klientem do zaokrąglania dla danej transakcji. W kontrakcie projektu może się znajdować tylko jeden klient zaokrąglenia. | W przypadku podziału kosztów i niepodzielonych faktur sprzedaży na ilość ołowiu w odniesieniu do różnicy zaokrągleń ta różnica jest stosowana względem wartości rzeczywistej mapowanej na danego klienta. |
| **Nieprzekraczalny limit** | Siatkę można edytować na karcie **Klienci kontraktowi** i formularze **Główny** i **Szybkie tworzenie** dla klienta z pozycjami kontraktu | Wskazuje, czy istnieje wynegocjowany limit lub limit całkowitej kwoty, która zostanie zafakturowana klientowi za to zlecenie. | **Nieprzekraczający limitu** ustawiony na poziomie klienta kontraktowego będzie oceniany na podstawie **Wartości rzeczywistych niefakturowanych sprzedaży**, które odwołują się do danego klienta kontraktowego. |

## <a name="edit-billing-split-percentages"></a>Edytowanie procentu podziału rozliczeń

Wartości procentowe podziału płatności można edytować za pomocą narzędzia do edycji siatki w linii. Gdy wartości procentowe podziału płatności nie osiągną 100 procent, pojawi się błąd. Po wyedytowaniu procentów podziału na fakturę odśwież stronę, aby odrzucić błąd.

Można również wybrać **Równo rozpowszechnianie** w podsiatce **Klienci kontraktów**, aby podzielić rozliczenia na różne pozycje. Jeśli istnieje współczynnik zaokrąglania, zostanie on dodany do zaokrąglenia do klienta. Jeden z klientów kontraktowych jest zawsze oznakowany jako klient **zaokrąglający**, co oznacza, że flaga zaokrąglania rekordu klienta w kontrakcie jest ustawiona na **Tak**. Zazwyczaj jest to główny klient kontraktu, ale można go również zmienić.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
