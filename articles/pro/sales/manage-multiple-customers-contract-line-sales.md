---
title: Zarządzanie wieloma klientami w pozycjach kontraktu opartego na projekcie - wersja uproszczona
description: Ten temat zawiera informacje o zarządzaniu wieloma klientami w pozycjach kontraktów dotyczących projektu.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f28e7d1363647621f7bd23504aa6d4ea3fc95fc9
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181651"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines---lite"></a>Zarządzanie wieloma klientami w pozycjach kontraktu opartego na projekcie - wersja uproszczona

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Pozycje kontraktu oparte na projektach mogą zawierać listę klientów, którzy są odpowiedzialni za zapłatę. Ta lista klientów w pozycji kontraktu opartego na projekcie może być identyczna z listą klientów w kontrakcie, ale nie jest to wymagane. Po zdobyciu oferty na projekt i utworzeniu umowy dotyczącej projektu lista klientów w wierszu oferty jest kopiowana do odpowiedniego wiersza umowy. Klienci z oferty są kopiowani do kontraktu.

Po zafakturowaniu kontraktu projektu lista klientów w pozycji kontraktu opartej na projekcie ma priorytet nad listą klientów w kontrakcie. Lista klientów w kontrakcie projektu zawiera tylko domyślne nowe pozycje kontraktu.

Wszyscy kontrahenci kontraktów na karcie **Klienci** kontraktu projektu jako domyślny dla wszystkich nowych wierszy kontraktu tworzonych na podstawie projektu, które są tworzone dla kontraktu dotyczącego projektu. Wszystkie istniejące pozycje kontraktu nie będą dziedziczyć nowych rekordów klientów kontraktowych utworzonych po ich utworzeniu.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Tworzenie, aktualizowanie i usuwanie rekordu klienta w wierszu kontraktu

Klienta pozycji kontraktu można tworzyć, aktualizować i usuwać z poziomu karty Klienci pozycji kontraktu na stronie Pozycje kontraktu opartego na projekcie. Po dodaniu nowego klienta w pozycji kontraktu opartej na projekcie są one również dodawane do całościowego kontraktu jako klient kontraktowy z domyślnym procentem podziału fakturowania równym zero procent. Procent podziału rozliczenia na ogólny kontrakt jest kopiowany do nowych pozycji kontraktu i ostatecznego kontraktu dotyczącego projektu. Natomiast podczas fakturowania z poziomu kontraktu jest to wartość procentowa podziału na fakturę na poziomie pozycji kontraktu, a nie wartość podziału na fakturę na poziomie ogólnego kontraktu.

Poniżej znajdują się pola rekordu klienta w wierszu **Kontraktu** opartego na projekcie, który ma mieć swoją uwagę podczas pracy z nim:

| Pole | Lokalizacja | Opis | Wpływ zmian w dalszych etapach |
| --- | --- | --- | --- |
| **Klient** | Edytowana siatka na karcie **Klienci kontraktowi** i formularze **Główny** i **Szybkie tworzenie** dla klienta z pozycjami kontraktu. | Wszystkie aktywne konta. To pole jest zablokowane po utworzeniu rekordu. Aby zaktualizować pole, należy usunąć rekord i utworzyć nowy rekord. W przypadku odnotowania wszystkich wartości rzeczywistych nie można usunąć rekordu. Można jednak oznaczyć procent podziału na fakturę jako zero dla tego konta. Jeśli rekord jest oznaczony jako zero, wpłynie to na wszystkie przyszłe wartości kosztów i przychodów, które są przypisane lub podzielone na klienta. | W przypadku wybrania konta z głównej listy kont w celu dodania i zaoszczędzenia klient pozycja kontraktu jest dodawany jako klient kontraktowy. Kontrahenci z pozycji kontraktu są używani podczas generowania faktur. |
| **Procent podziału rozliczeń** | Edytowana siatka na karcie **Klienci kontraktowi** i formularze **Główny** i **Szybkie tworzenie** dla klienta z pozycjami kontraktu. | To pole reprezentuje procent każdej niezafakturowanej transakcji sprzedaży, która zostanie przypisana do tej pozycji kontraktu klient. | Klienci w pozycji kontraktu i procent podziału fakturowania są używane podczas tworzenia wartości rzeczywistych po zatwierdzeniu i podczas generowania faktury. |
| **Nieprzekraczalny limit** | Edytowana siatka na karcie **Klienci kontraktowi** i formularze **Główny** i **Szybkie tworzenie** dla klienta z pozycjami kontraktu. | Wskazuje, czy w pozycji kontraktu istnieje wynegocjowany limit lub wartość licznika z informacją, która zostanie zafakturowana dla danego klienta. | Limit nieprzekraczania dla klienta wiersza umowy jest używany podczas tworzenia wartości rzeczywistych i generowania faktur. |
| **Zaokrągla** | Edytowana siatka na karcie **Klienci kontraktowi** i formularzami **Główny** i **Szybkie tworzenie** dla klienta z pozycjami kontraktu. | To pole wskazuje, czy dany nabywca jest domyślnym zaokrąglaniem nabywcy dla danego wiersza kontraktu opartego na projektach. | W przypadku generowania wartości rzeczywistej na podstawie procentu podziału rozliczenia mogą się pojawić różnice zaokrągleń. Klientowi przypisywane są różnice zaokrągleń w tym przypadku. |

## <a name="edit-billing-split-percentages"></a>Edytowanie procentu podziału rozliczeń

Podziały procentowe dotyczące rozliczeń można edytować w siatce. Jeśli procent podziału rozliczenia nie ma sumy 100 procent, wystąpi błąd. Po wyedytowaniu procentów podziału na fakturę odśwież stronę, aby usunąć błąd.

Można wybrać **Rozłóż równomiernie** w podsiatce klientów pozycji kontraktu. Ta akcja powoduje równomierne alokowanie podziału na rozliczenia dla wszystkich klientów z pozycji kontraktu. Jeśli istnieje współczynnik zaokrąglania, zostanie on dodany do zaokrąglenia do klienta. Klient z jedną pozycją kontraktu jest zawsze oznakowany jako klient **Zaokrąglający** flagę **Zaokrąglania** ustawioną na **Tak**.
