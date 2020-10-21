---
title: Zarządzanie wieloma klientami w wierszach oferty opartej na projekcie
description: W tym temacie opisano sposób zarządzania wieloma klientami w wierszach oferty opartej na projekcie.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6a509fcf8d1fa11b4ce1ba1493d9c3cc64b4f22f
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965859"
---
# <a name="managing-multiple-customers-on-project-based-quote-lines"></a>Zarządzanie wieloma klientami w wierszach oferty opartej na projekcie

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Wiersze oferty oparte na projekcie obsługują scenariusze, w których każdy wiersz oferty zawiera listę klientów, którzy za niego płacą. Ta lista klientów w wierszu oferty opartej na projekcie może być identyczna z listą klientów z oferty. Można również zmienić listę klientów, aby się różniła. Po wykorzystaniu oferty projektu lista klientów w wierszu oferty opartej na projekcie jest kopiowana do odpowiedniego wiersza kontraktu opartego na projekcie w celu utworzenia ostatecznego kontraktu dotyczącego projektu. Klienci z oferty opartej na projekcie są kopiowani do kontraktu dotyczącego projektu.

Po zafakturowaniu ostatecznego kontraktu dotyczącego projektu lista klientów w pozycji kontraktu opartej na projekcie ma priorytet nad listą w kontrakcie projektu. Lista klientów w kontrakcie dotyczącym projektu jest używana tylko w przypadku wartości domyślnych w nowych pozycjach kontraktu projektu.

Wszyscy klienci oferty na karcie **Klienci** w ofercie projektu domyślnie stają się klientami wiersza oferty dla wszystkich nowych wierszy oferty opartej na projekcie tworzonych dla oferty projektu. Żadne istniejące wiersze oferty opartej na projekcie nie dziedziczą nowych rekordów klientów oferty utworzonych po ich utworzeniu.

## <a name="create-update-or-delete-a-quote-line-customer-record"></a>Tworzenie, aktualizowanie i usuwanie rekordu klienta w wierszu oferty

Użytkownik może tworzyć, aktualizować i usuwać klienta wiersza oferty na karcie **Klient wiersza oferty** na stronie **Wiersz oferty opartej na projekcie**. Po dodaniu nowego klienta do wiersza oferty opartej na projekcie klient jest także dodawany do ogólnej oferty jako jej klient, przy czym domyślny procent przydziału faktury wynosi dla niego 0%. Procent podziału na fakturze dla oferty łącznej jest kopiowany do nowych wierszy oferty oraz do ostatecznego kontraktu dotyczącego projektu. Jednak podczas fakturowania na poziomie kontraktu jest używany procent podziału na fakturę z poziomu wiersza oferty, a nie procent podziału na fakturze na ogólnym poziomie kontraktu. 

W poniższej tabeli przedstawiono pola rekordu nabywcy w wierszu oferty opartej na projekcie.

| Pole | Lokalizacja | Opisy i wskazówki | Wpływ zmian w dalszych etapach |
| --- | --- | --- | --- |
| **Klient** | Edytowalna siatka na karcie **Kontrahenci wiersza oferty**, formularz główny i formularze szybkiego tworzenia dla klienta wiersza oferty. | Lista wszystkich aktywnych kont. To pole jest zablokowane po utworzeniu rekordu. Jeśli zachodzi konieczność zaktualizowania pola, należy usunąć rekord i utworzyć go ponownie. W przypadku zapisania jakichkolwiek wartości rzeczywistych rekord nie jest usuwany. | W przypadku wybrania do dodania konta z głównej listy klientów, klient z wiersza oferty jest dodawany również jako klient oferty po zapisaniu. Po wykorzystaniu oferty klienci wiersza oferty są kopiowani jako klienci w pozycji kontraktu projektu. |
| **Procent podziału rozliczeń** | Edytowalna siatka na karcie **Kontrahenci wiersza oferty**, formularz główny i formularze szybkiego tworzenia dla klienta wiersza oferty. | Reprezentuje procent każdej niezafakturowanej transakcji sprzedaży, która będzie przypisywana do tego klienta. | Kopiowane do klientów pozycji kontraktu projektu. |
| **Nieprzekraczalny limit** | Edytowalna siatka na karcie **Kontrahenci wiersza oferty**, formularz główny i formularze szybkiego tworzenia dla klienta wiersza oferty. | Wskazuje, czy istnieje limit negocjacyjny lub blokada ogólnej kwoty, która będzie zafakturowana dla tego klienta w tym wierszu oferty. | Po wygraniu oferty ta wartość jest kopiowana do klienta wiersza oferty. |
| **Zaokrągla** | Edytowalna siatka na karcie **Kontrahenci wiersza oferty**, formularz główny i formularze szybkiego tworzenia dla klienta wiersza oferty. | Wskazuje, czy ten klient jest domyślnym klientem zaokrąglającym w ramach danego wiersza oferty opartej na projekcie. | Po wygraniu oferty ta wartość jest kopiowana do klienta oferty. |

## <a name="edit-billing-split-percentages"></a>Edytowanie procentu podziału rozliczeń

Procent podziału rozliczeń można edytować w wierszu. Jeśli procent podziału rozliczenia nie sumuje się do 100%, wystąpi błąd. Po wyedytowaniu procentów podziału na fakturze odśwież stronę w wierszu oferty, aby usunąć błąd.

Skorzystaj z siatki rozdzielenia równomiernego pomiędzy klientami wiersza oferty, aby przydzielić wszystkie procenty podziału rozliczeń pomiędzy wszystkich klientów wiersza. Jeśli istnieje współczynnik zaokrąglenia, zostanie dodany do klienta zaokrąglającego. Jeden z klientów wierszy oferty jest zawsze oznakowany jako klient zaokrąglający, co oznacza, że rekord klienta wiersza oferty ma ustawioną flagę zaokrąglania równą **Tak**. 
