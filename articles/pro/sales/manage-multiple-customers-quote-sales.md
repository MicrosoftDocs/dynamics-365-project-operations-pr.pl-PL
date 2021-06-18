---
title: Zarządzanie wieloma klientami w ofertach projektu - wersja uproszczona
description: W tym temacie zamieszczono informacje dotyczące pracy z ofertami wielu klientów, którzy będą finansować dany projekt. (Sales)
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 02a05de28a92d98b58245a70f456a9b144c8d5a1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994959"
---
# <a name="manage-multiple-customers-on-project-quotes---lite"></a>Zarządzanie wieloma klientami w ofertach projektu - wersja uproszczona

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Oferty projektów obsługują scenariusz polegający na tym, że dana oferta obejmuje wielu klientów, którzy będą finansować transakcję. Na karcie **Podsumowanie** oferty znajduje się pole **Potencjalni klienci**, który identyfikuje podstawowego klienta transakcji. Innych klientów w ramach transakcji można skonfigurować na karcie **Klienci** w ofercie projektu.

Wszyscy klienci oferty na karcie **Klienci** w ofercie projektu domyślnie stają się klientami wiersza oferty dla wszystkich **nowych** wierszy oferty opartej na projekcie tworzonych dla oferty projektu. Żadne istniejące wiersze oferty opartej na projekcie nie odziedziczą nowych rekordów klientów oferty utworzonych po ich utworzeniu.

Wiersze oferty opartej na produkcie są automatycznie kojarzone z podstawowym klientem, który jest także klientem w polu **Potencjalny klient** na karcie **Podsumowanie** oferty.

Można dodawać klientów oferty i klientów wierszy oferty, a także aktualizować, dodawać i usuwać te dane przed zamknięciem oferty.

## <a name="concept-of-a-primary-customer"></a>Koncept podstawowego klienta

Klient będący na karcie Podsumowanie oferty projektu, to potencjalny klient, czyli główny klient oferty. Podczas próby usunięcia klienta podstawowego z listy klientów w ofercie jest wyświetlany komunikat o błędzie informujący, że nie można usunąć rekordu podstawowego klienta w ofercie.

Podstawowy klient nie powinien być aktualizowany na liście klientów w ofercie. Użytkownik może jednak zmienić podstawowego klienta, zmieniając potencjalnego klienta na karcie **Podsumowanie** oferty. Jeśli to pole jest aktualizowane w ramach **Podsumowania** oferty, nowo wybrani potencjalni klienci zostaną dodani jako nowy klient oferty z ustawioną flagą **Podstawowy**. Stary potencjalny klient będzie nadal klientem w ofercie.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Tworzenie, aktualizowanie i usuwanie rekordu klienta w wierszu oferty

Klienta oferty można utworzyć, aktualizować i usuwać z poziomu karty **Klienci oferty** na stronie **Oferta**. W poniższej tabeli przedstawiono pola rekordu klienta w wierszu oferty opartej na projekcie.

| **Pole** | **Lokalizacja** | **Opis** | **Wpływ zmian w dalszych etapach** |
| --- | --- | --- | --- |
| Konto | Edytowalna siatka na karcie **Klienci oferty**, formularz **główny** i formularze **szybkiego tworzenia** dla klienta wiersza oferty. | Lista wszystkich aktywnych kont. To pole jest zablokowane po utworzeniu rekordu. Jeśli chcesz przeprowadzić aktualizację, usuń rekord i utwórz go ponownie. Jeśli rekord został zarejestrowany z wartościami rzeczywistymi lub rekord klienta oferty to klient podstawowy, użytkownik będzie mógł usunąć rekord. | Po wykorzystaniu oferty klienci wiersza oferty są kopiowani jako klienci w pozycji kontraktu projektu. Po wykorzystaniu oferty klienci wiersza oferty są także kopiowani jako klienci w pozycji kontraktu projektu. |
| Procent podziału rozliczeń | Edytowalna siatka na karcie **Klienci oferty**, formularz **główny** i formularze **szybkiego tworzenia** dla klienta wiersza oferty. | Reprezentuje procent każdej niezafakturowanej transakcji sprzedaży, która będzie przypisywana do tego klienta oferty. | Po wygraniu oferty ta wartość jest kopiowana do klienta kontraktu oraz nowych wierszy oferty. |
| Nazwa kontaktu u płatnika | Edytowalna siatka na karcie **Klienci oferty**, formularz **główny** i formularze **szybkiego tworzenia** dla klienta wiersza oferty. | Jest to pole tekstowe, które ma służyć do identyfikowania osoby kontaktowej dla faktury u danego klienta. Te elementy są domyślnie pobierane z rekordu pokrewnego konta | Skopiowane do klienta kontraktu dotyczącego projektu podczas potwierdzenia oferty i do pola Nazwa płatnika kontraktu na fakturze wygenerowanej dla danego klienta. |
| Nazwa płatnika | Edytowalna siatka na karcie **Klienci oferty**, formularz **główny** i formularze **szybkiego tworzenia** dla klienta wiersza oferty. | To pole tekstowe ma służyć do identyfikowania osoby kontaktowej dla faktury u danego klienta. | Skopiowane do klienta kontraktu dotyczącego projektu podczas potwierdzenia oferty i do pola **Nazwa płatnika kontraktu** na fakturze wygenerowanej dla danego klienta. |
| Warunki płatności | Edytowalna siatka na karcie **Klienci oferty**, formularz **główny** i formularze **szybkiego tworzenia** dla klienta wiersza oferty. | Jest to zestaw opcji z wartościami domyślnymi dla rekordu konta pokrewnego. | Skopiowane do klienta kontraktu dotyczącego projektu podczas potwierdzenia oferty i do pola **Nazwa płatnika kontraktu** na fakturze wygenerowanej dla danego klienta. |
| Zaokrągla | Edytowalna siatka na karcie **Klienci oferty**, formularz **główny** i formularze **szybkiego tworzenia** dla klienta wiersza oferty. | Wskazuje, czy ten klient jest domyślnym klientem do zaokrąglania dla danej transakcji. | Po wygraniu oferty ta wartość jest kopiowana do klienta oferty. |
| Nieprzekraczalny limit | Edytowalna siatka na karcie **Klienci oferty**, formularz **główny** i formularze **szybkiego tworzenia** dla klienta wiersza oferty. | Wskazuje, czy istnieje limit negocjacyjny lub blokada ogólnej kwoty, która będzie zafakturowana dla tego klienta w tej interakcji | Po wygraniu oferty ta wartość jest kopiowana do klienta oferty. |

## <a name="editing-billing-split-percentages"></a>Edytowanie procentu podziału rozliczeń

Zawartość procentową podziału rozliczeń na fakturze można edytować przy użyciu funkcji edycji siatki w wierszu. Jeśli procent podziału rozliczenia nie sumuje się do 100%, wystąpi błąd. Po aktualizacji procentów podziału na fakturze odśwież stronę, aby usunąć błąd.

Można również spróbować wybrać **Rozłóż równomiernie** w podsiatce klientów z ofertą. Ta akcja spowoduje alokowanie podziału procentowego na fakturze dla wszystkich klientów oferty. Jeśli istnieje współczynnik zaokrąglenia, zostanie dodany do klienta zaokrąglającego. Jeden z klientów korzystających z oferty jest zawsze oznakowany jako klient do zaokrąglenia. oznacza to, że dany rekord klienta oferty ma ustawioną flagę **Tak** w opcji **Zaokrąglanie**. Zazwyczaj jest to główny klient oferty, ale można to zmienić.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]