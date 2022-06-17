---
title: Zarządzanie wieloma klientami w ofercie projektu
description: W tym artykule przedstawiono informacje na temat pracy z ofertami obejmującymi wielu klientów, którzy będą finansować projekt.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 16cd07527fddd093748a18c1f7c900c8b32be85d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928215"
---
# <a name="manage-multiple-customers-on-a-project-quote"></a>Zarządzanie wieloma klientami w ofercie projektu

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Oferty projektów obsługują scenariusz polegający na tym, że dana oferta obejmuje wielu klientów, którzy będą finansować transakcję. Na karcie **Podsumowanie** oferty znajduje się pole **Potencjalni klienci**, które identyfikuje podstawowego klienta transakcji. Innych klientów w ramach transakcji można skonfigurować na karcie **Klienci** w ofercie projektu.

Wszyscy klienci oferty na karcie **Klienci** w ofercie projektu domyślnie stają się klientami wiersza oferty dla wszystkich **nowych** wierszy oferty opartej na projekcie tworzonych dla oferty projektu. Żadne istniejące wiersze oferty opartej na projekcie nie odziedziczą nowych rekordów klientów oferty utworzonych po ich utworzeniu.

Można dodawać klientów oferty i klientów wierszy oferty, a także aktualizować, dodawać i usuwać te dane przed zamknięciem oferty. Prawidłowa identyfikacja klienta w ofercie projektu musi zostać ustawiona na stronie **Klienci** na firmę będącą właścicielem lub osobę prawną. Podmioty prawne są konfigurowane w module **Zarządzanie projektami i księgowanie w aplikacji** rozwiązania Dynamics 365 Project Operations i są dostępne jako firmy w modułach **Sprzedaż i dostawa projektu** w aplikacji Project Operations.

## <a name="concept-of-a-primary-customer"></a>Koncept podstawowego klienta

Klient wymieniony na karcie **Podsumowanie** oferty projektu, to potencjalny klient, czyli główny klient oferty. Jeśli zostanie podjęta próba usunięcia klienta podstawowego z listy klientów, w ofercie jest wyświetlany komunikat o błędzie informujący, że nie można usunąć rekordu podstawowego klienta w ofercie.

Podstawowy klient nie powinien być aktualizowany na liście klientów w ofercie. Użytkownik może jednak zmienić podstawowego klienta, zmieniając potencjalnego klienta na karcie **Podsumowanie** oferty. Jeśli to pole jest aktualizowane w ramach **Podsumowania** oferty, nowo wybrani potencjalni klienci zostaną dodani jako nowy klient oferty z ustawioną flagą **Podstawowy**. Stary potencjalny klient będzie nadal klientem w ofercie.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Tworzenie, aktualizowanie i usuwanie rekordu klienta w wierszu oferty

Klienta oferty można utworzyć, aktualizować i usuwać z poziomu karty **Klienci oferty** na stronie **Oferta**. W poniższej tabeli przedstawiono pola rekordu klienta w wierszu oferty opartej na projekcie.

| **Pole** | **Lokalizacja** | **Opis** | **Wpływ zmian w dalszych etapach** |
| --- | --- | --- | --- |
| Konto | Edytowalna siatka na karcie **Klienci oferty**, formularz **główny** i formularze **szybkiego tworzenia** dla klienta wiersza oferty. | Lista wszystkich aktywnych kont. To pole jest zablokowane po utworzeniu rekordu. Jeśli chcesz przeprowadzić aktualizację, usuń rekord i utwórz go ponownie. Jeśli rekord został zarejestrowany z wartościami rzeczywistymi lub rekord klienta oferty to klient podstawowy, użytkownik będzie mógł usunąć rekord. | Po wykorzystaniu oferty klienci wiersza oferty są kopiowani jako klienci w pozycji kontraktu projektu. Po wykorzystaniu oferty klienci wiersza oferty są także kopiowani jako klienci w pozycji kontraktu projektu. |
| Procent podziału rozliczeń | Edytowalna siatka na karcie **Klienci oferty**, formularz **główny** i formularze **szybkiego tworzenia** dla klienta wiersza oferty. | Reprezentuje procent każdej niezafakturowanej transakcji sprzedaży, która będzie przypisywana do tego klienta oferty. | Po wygraniu oferty ta wartość jest kopiowana do utworzonego klienta kontraktu oraz nowych wierszy oferty. |
| Nazwa kontaktu u płatnika | Edytowalna siatka na karcie **Klienci oferty**, formularz **główny** i formularze **szybkiego tworzenia** dla klienta wiersza oferty. | Jest to pole tekstowe, które ma służyć do identyfikowania osoby kontaktowej dla faktury u danego klienta. Te elementy są domyślnie pobierane z rekordu pokrewnego konta | Skopiowane do klienta kontraktu dotyczącego projektu podczas potwierdzenia oferty i do pola Nazwa płatnika kontraktu na fakturze wygenerowanej dla danego klienta. |
| Nazwa płatnika | Edytowalna siatka na karcie **Klienci oferty**, formularz **główny** i formularze **szybkiego tworzenia** dla klienta wiersza oferty. | To pole tekstowe ma służyć do identyfikowania osoby kontaktowej dla faktury u danego klienta. | Skopiowane do klienta kontraktu dotyczącego projektu podczas potwierdzenia oferty i do pola **Nazwa płatnika kontraktu** na fakturze wygenerowanej dla danego klienta. |
| Warunki płatności | Edytowalna siatka na karcie **Klienci oferty**, formularz **główny** i formularze **szybkiego tworzenia** dla klienta wiersza oferty. | Jest to zestaw opcji z wartościami domyślnymi dla rekordu konta pokrewnego. | Skopiowane do klienta kontraktu dotyczącego projektu podczas potwierdzenia oferty i do pola **Nazwa płatnika kontraktu** na fakturze wygenerowanej dla danego klienta. |
| Zaokrągla | Edytowalna siatka na karcie **Klienci oferty**, formularz **główny** i formularze **szybkiego tworzenia** dla klienta wiersza oferty. | Wskazuje, czy ten klient jest domyślnym klientem do zaokrąglania dla danej transakcji. | Po wygraniu oferty ta wartość jest kopiowana do klienta oferty. |
| Firma będąca właścicielem | Edytowalna siatka na karcie **Klienci oferty**, formularz **główny** i formularze **szybkiego tworzenia** dla klienta wiersza oferty. | Podmiot prawny, który został skonfigurowany przez tego klienta w module **Zarządzanie projektami i ich księgowanie**. To pole jest tylko do odczytu i jest ustawione na firmę będącą właścicielem oferty. Lista klientów do dodania w polu **Konto** jest już filtrowana na listę z tej firmy będącej właścicielem w module **Informacje o zarządzaniu projektami i ich księgowaniu** w Project Operations. | Firma będąca właścicielem to to samo, co koncept osoby prawnej w module **Zarządzanie projektami i księgowaniem** w Project Operations. Wszystkie koszty i przychód powstałe w wyniku tego projektu będą uwzględnione w księdze głównej firmy będącej właścicielem. |
| Nieprzekraczalny limit | Edytowalna siatka na karcie **Klienci oferty**, formularz **główny** i formularze **szybkiego tworzenia** dla klienta wiersza oferty. | Wskazuje, czy istnieje limit negocjacyjny lub blokada ogólnej kwoty, która będzie zafakturowana dla tego klienta w tej interakcji. | Po wygraniu oferty ta wartość jest kopiowana do klienta oferty. |

## <a name="editing-billing-split-percentages"></a>Edytowanie procentu podziału rozliczeń

Zawartość procentową podziału rozliczeń na fakturze można edytować przy użyciu funkcji edycji siatki w wierszu. Jeśli procent podziału rozliczenia nie sumuje się do 100%, wystąpi błąd. Po aktualizacji procentów podziału na fakturze odśwież stronę, aby usunąć błąd.

Można również spróbować wybrać **Rozłóż równomiernie** w podsiatce klientów z ofertą. Ta akcja spowoduje alokowanie podziału procentowego na fakturze dla wszystkich klientów oferty. Jeśli istnieje współczynnik zaokrąglenia, zostanie dodany do klienta zaokrąglającego. Jeden z klientów korzystających z oferty jest zawsze oznakowany jako klient do zaokrąglenia. oznacza to, że dany rekord klienta oferty ma ustawioną flagę **Tak** w opcji **Zaokrąglanie**. Zazwyczaj jest to główny klient oferty, ale można to zmienić.


[!INCLUDE[footer-include](../includes/footer-banner.md)]