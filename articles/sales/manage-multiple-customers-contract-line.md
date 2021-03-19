---
title: Zarządzanie wieloma klientami w pozycjach kontraktu opartego na projekcie
description: Ten temat zawiera informacje na temat pracy z pozycjami kontraktu i kontraktami zawierającymi wielu klientów.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 205363d2ea5f1f5bf5fa8879cedd5b3e857eb772
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278026"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines"></a>Zarządzanie wieloma klientami w pozycjach kontraktu opartego na projekcie

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Pozycje kontraktu oparte na projektach mogą zawierać listę klientów, którzy są odpowiedzialni za zapłatę. Ta lista klientów w pozycji kontraktu opartego na projekcie może być identyczna z listą klientów w kontrakcie, ale nie jest to wymagane. Po zdobyciu oferty na projekt i utworzeniu umowy dotyczącej projektu lista klientów w wierszu oferty jest kopiowana do odpowiedniego wiersza umowy. Klienci z oferty są kopiowani do kontraktu.

Po zafakturowaniu kontraktu projektu lista klientów w pozycji kontraktu opartej na projekcie ma priorytet nad listą klientów w kontrakcie. Lista klientów w kontrakcie projektu zawiera tylko domyślne nowe pozycje kontraktu.

Wszyscy kontrahenci kontraktów na karcie **Klienci** kontraktu projektu jako domyślny dla wszystkich nowych wierszy kontraktu tworzonych na podstawie projektu, które są tworzone dla kontraktu dotyczącego projektu. Wszystkie istniejące pozycje kontraktu nie będą dziedziczyć nowych rekordów klientów kontraktowych utworzonych po ich utworzeniu.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Tworzenie, aktualizowanie i usuwanie rekordu klienta w wierszu kontraktu

Klienta pozycji kontraktu można tworzyć, aktualizować i usuwać z poziomu karty **Klienci pozycji kontraktu** na stronie **Pozycje kontraktu opartego na projekcie**. Po dodaniu nowego klienta w pozycji kontraktu opartej na projekcie są one również dodawane do całościowego kontraktu jako klient kontraktowy z domyślnym procentem podziału fakturowania równym zero procent. Procent podziału rozliczenia na ogólny kontrakt jest kopiowany do nowych pozycji kontraktu i ostatecznego kontraktu dotyczącego projektu. Natomiast podczas fakturowania z poziomu kontraktu jest to wartość procentowa podziału na fakturę na poziomie pozycji kontraktu, a nie wartość podziału na fakturę na poziomie ogólnego kontraktu. 

Poniżej znajdują się pola rekordu klienta w wierszu kontraktu opartego na projekcie, który ma mieć swoją uwagę podczas pracy z nim:

| Pole | Lokalizacja | Opis | Wpływ zmian w dalszych etapach |
| --- | --- | --- | --- |
| Konto | Edytowana siatka na karcie **Klienci z pozycjami kontraktu** i głównymi i szybkimi formularzami dla klienta z pozycjami kontraktu | Wszystkie aktywne konta. To pole jest zablokowane po utworzeniu rekordu. Aby zaktualizować pole, należy usunąć rekord i utworzyć nowy rekord. W przypadku odnotowania wszystkich wartości rzeczywistych nie można usunąć rekordu. Można jednak oznaczyć procent podziału na fakturę jako zero dla tego konta. Jeśli rekord jest oznaczony jako zero, wpłynie to na wszystkie przyszłe wartości kosztów i przychodów, które są przypisane lub podzielone na klienta. | W przypadku wybrania konta z głównej listy kont w celu dodania i zaoszczędzenia klient pozycja kontraktu jest dodawany jako klient kontraktowy. Kontrahenci z pozycji kontraktu są używani podczas generowania faktur. |
| Procent podziału rozliczeń | Edytowana siatka na karcie **Klienci z pozycjami kontraktu** i głównymi i szybkimi formularzami dla klienta z pozycjami kontraktu | To pole reprezentuje procent każdej niezafakturowanej transakcji sprzedaży, która zostanie przypisana do tej pozycji kontraktu klient. | Klienci w pozycji kontraktu i procent podziału fakturowania są używane podczas tworzenia wartości rzeczywistych po zatwierdzeniu i podczas generowania faktury. |
| Nieprzekraczalny limit | Edytowana siatka na karcie **Klienci z pozycjami kontraktu** i głównymi i szybkimi formularzami dla klienta z pozycjami kontraktu | Wskazuje, czy w pozycji kontraktu istnieje wynegocjowany limit lub wartość licznika z informacją, która zostanie zafakturowana dla danego klienta. | Limit nieprzekraczania dla klienta wiersza umowy jest używany podczas tworzenia wartości rzeczywistych i generowania faktur. |
| Firma będąca właścicielem | Edytowana siatka na karcie **Klienci z wierszami oferty** i głównymi i szybkimi formularzami dla klienta z pozycjami oferty | Podmiot prawny, dla którego jest skonfigurowany dany klient. To pole jest tylko do odczytu i ma ustawioną firmę będącą właścicielem oferty. Lista klientów, która ma zostać dodana w polu **Konto**, jest już filtrowana na listę z tej firmy będącej właścicielem. | Pojęcie przedsiębiorstwa będącego właścicielem jest równe koncepcji podmiotu prawnego. Wszystkie koszty i przychód z danego projektu są uwzględnione w księdze głównej firmy będącej właścicielem. |
| Zaokrągla | Edytowana siatka na karcie **Klienci z pozycjami kontraktu** i głównymi i szybkimi formularzami dla klienta z pozycjami kontraktu | To pole wskazuje, czy dany nabywca jest domyślnym zaokrąglaniem nabywcy dla danego wiersza kontraktu opartego na projektach. | W przypadku generowania wartości rzeczywistej na podstawie procentu podziału rozliczenia mogą się pojawić różnice zaokrągleń. Klientowi przypisywane są różnice zaokrągleń w tym przypadku. |

## <a name="edit-billing-split-percentages"></a>Edytowanie procentu podziału rozliczeń

Podziały procentowe dotyczące rozliczeń można edytować w siatce. Jeśli procent podziału rozliczenia nie ma sumy 100 procent, wystąpi błąd. Po wyedytowaniu procentów podziału na fakturę odśwież stronę, aby usunąć błąd.

Można również spróbować wybrać **Rozłóż równomiernie** w podsiatce klientów pozycji kontraktu. Ta akcja powoduje równomierne alokowanie podziału na rozliczenia dla wszystkich klientów z pozycji kontraktu. Jeśli istnieje współczynnik zaokrąglania, zostanie on dodany do zaokrąglenia do klienta. Klient z jedną pozycją kontraktu jest zawsze oznakowany jako klient **Zaokrąglający** flagę **Zaokrąglania** ustawioną na **Tak**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]