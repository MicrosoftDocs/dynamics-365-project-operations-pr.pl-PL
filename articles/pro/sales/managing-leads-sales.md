---
title: Zarządzaj potencjalnymi klientami (pro)
description: Ten temat zawiera informacje na temat zarządzania potencjalnymi klientami (pro).
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 005e36811643b0b1e98a686792cf39125ae97949
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896339"
---
# <a name="manage-leads-pro"></a>Zarządzaj potencjalnymi klientami (pro)

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Potencjalni klienci oparci na projekcie mogą być zarządzani i kwalifikowani w Project Operations. Proces zarządzania potencjalnymi klientami obejmuje tworzenie potencjalnych klientów i kwalifikowanie ich. 

## <a name="list-of-project-sales-leads"></a>Lista potencjalnych klientów projektu

W sekcji **Sprzedaż** w lewym okienku nawigacji otwórz stronę listy **Potencjalni klienci**, aby wyświetlić listę wszystkich rekordów potencjalnych klientów w systemie. Lista wyświetlanych potencjalnych klientów jest oparta na pracach i innych typach potencjalnych klientów, których można utworzyć w przypadku, gdy użytkownik ma także dostęp do Dynamics 365 Sales i Dynamics 365 Field Service.

Można utworzyć widok filtrowany, aby wyświetlić tylko potencjalnych klientów opartych na projektach, tworząc filtr dla wartości **Typu**. Można na przykład wybrać opcję, aby byli wyświetlani tylko potencjalni klienci w danym miejscu.

## <a name="creating-a-new-lead-for-a-project-based-deal"></a>Tworzenie nowego potencjalnego klienta dla transakcji opartej na projekcie

Zakwalifikowanie potencjalnego klienta opartego na projekcie powoduje utworzenie szansy sprzedaży i konta. Szansa sprzedaży oparta na projekcie jest punktem początkowym wykonywania działań dotyczących sprzedaży w fazie szansy sprzedaży. Szanse sprzedaży na podstawie projektu są unikatowe, wymagane do sprzedaży pracy nad projektem. Dostępne są następujące możliwości:

- Metoda rozliczania transakcji czasu i materiałów
- Wiele dat wejścia w życie cenników dla zasobów ludzkich, wydatków i materiałów wprowadzonych do projektów.

W przypadku zakwalifikowanego potencjalnego klienta, aby automatycznie utworzyć szansę sprzedaży, należy ustawić atrybut **Typ** na **Oparte na pracy**. W przypadku wybrania innego typu potencjalny klient nie będzie tworzył szansy sprzedaży opartej na projekcie, gdy zostanie zakwalifikowany. Jeśli szansa sprzedaży oparta na projekcie nie jest utworzona, funkcje specyficzne dla projektu nie będą dostępne w procesach niższego rzędu.

Poniższa tabela zawiera ważne informacje dotyczące potencjalnego klienta oraz efekty podrzędne tych pól.

| **Pole** | **Lokalizacja** | **Stopień zgodności, cel i wskazówki** | **Wpływ zmian w dalszych etapach** |
| --- | --- | --- | --- |
| Temat | Karta Ogólne | To pole tekstowe powinno zawierać krótki opis transakcji. | Temat potencjalnego klienta będzie domyślnie ustawiony jako szansa sprzedaży, nazwy oferty i kontraktu projektu. |
| Pisz | Karta Ogólne | To pole zestawu opcji zawiera następujące opcje:</br>- Na podstawie pracy (dostępne tylko wtedy, gdy Project Operations jest zainstalowane)</br>- Na podstawie towaru (dostępne tylko wtedy, gdy jest zainstalowane Project Operations i Sales)</br>- Na podstawie wykonania usługi (dostępne po zainstalowaniu Field Service) | Jeśli wartość tego pola jest ustawiona na **Na podstawie pracy** dla potencjalnego klienta, potencjalny klient jest kwalifikowany do utworzenia szansy sprzedaży opartej na projekcie. Szansa sprzedaży oparta na projekcie jest wymagana do włączenia wszystkich rozszerzeń specyficznych dla danego projektu i funkcji w ramach procesu sprzedaży na niższym szczeblu w zakresie omawianej transakcji. |
| Imię | Karta Ogólne | Wprowadź imię dla kontaktu potencjalnego klienta | Zakwalifikowanie potencjalnego klienta opartego na projekcie powoduje utworzenie konta, kontaktu i szansy sprzedaży. Imię kontaktu jest tutaj zapisaną wartością. |
| Nazwisko | Karta Ogólne | Nazwisko dla kontaktu potencjalnego klienta | Zakwalifikowanie potencjalnego klienta opartego na projekcie powoduje utworzenie konta, kontaktu i szansy sprzedaży. Nazwisko kontaktu jest tutaj zapisaną wartością. |
| Firma | Karta Ogólne | Nazwa firmy potencjalnego klienta | Zakwalifikowanie potencjalnego klienta opartego na projekcie powoduje utworzenie konta, kontaktu i szansy sprzedaży. Nazwisko dla utworzonego konta jest tutaj zapisane. |
| Waluta | Karta Szczegóły | Waluta potencjalnego klienta | Zakwalifikowanie potencjalnego klienta opartego na projekcie powoduje utworzenie konta, kontaktu i szansy sprzedaży. Waluta dla utworzonego konta jest tutaj zapisana. |

## <a name="qualify-a-new-project-based-lead"></a>Zakwalifikowanie nowego potencjalnego klienta opartego na projekcie

Potencjalni klienci, dla których ustawiono wartość **Typ** na **Oparty na pracy** nazywani są potencjalnymi klientami opartymi na projektach. W przypadku kwalifikowania potencjalnego klienta opartego na projekcie są tworzone następujące elementy:

- Konto, które korzysta z pola **Firma** potencjalnego klienta.
- Rekord kontaktu skojarzony z kontem na podstawie wartości w polach **Imię** i **Nazwisko** w potencjalnego klienta.
- Szansa sprzedaży oparta na projekcie z polem **Typ** ustawionym na wartość &quot;**Oparte na pracy**.

Aby uzyskać bardziej szczegółowe informacje na temat kwalifikowania potencjalnych klientów, zobacz [kwalifikowanie i konwertowanie potencjalnych klientów](https://docs.microsoft.com/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

## <a name="business-process-flow-for-project-based-deals"></a>Przepływ procesów biznesowych w transakcjach opartych na projektach

Poniższe przepływy procesów biznesowych są obsługiwane w przypadku transakcji opartych na projektach w Project Operations:

- Proces biznesowy Od potencjalnego klienta do szansy sprzedaży
- Proces sprzedaży w ramach szansy sprzedaży

Proces biznesowy Od potencjalnego klienta do szansy sprzedaży obsługuje następujące etapy:

| Nazwa etapu | Mapowana encja | Funkcje |
| --- | --- | --- |
| Kwalifikuj | Potencjalny klient | Kwalifikowanie potencjalnego klienta tworzy konto, kontakt oraz szansę sprzedaży. |
| Opracuj | Szansa sprzedaży | Rozwijanie szansy sprzedaży w celu dodania informacji o związanej pracy, kluczowych udziałowcach i konkurencji. |
| Zaproponuj | Szansa sprzedaży | Opracowanie i uzyskanie zgody zespołu na przegląd wewnętrzny. |
| Zamykanie | Szansa sprzedaży | Wykorzystaj szansę sprzedaży, aby zamknąć ofertę. |
