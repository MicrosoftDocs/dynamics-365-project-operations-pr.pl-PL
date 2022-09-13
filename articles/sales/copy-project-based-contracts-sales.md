---
title: Kopiowanie kontraktów opartych na projektach
description: W tym artykule przedstawiono informacje na temat kopiowania kontraktów projektu w aplikacji Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 21994ef6d8f6e6cdf321599d107cc80368c96ecc
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410337"
---
# <a name="copy-project-based-contracts"></a>Kopiowanie kontraktów opartych na projektach

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Nowe kontrakty projektów można łatwo utworzyć, kopiując istniejące kontrakty na dwa sposoby:

- Na stronie listy **Kontrakty projektów** wybierz kontrakt projektu, a następnie wybierz pozycję **Kopiuj**.
- Na stronie szczegółów **Kontraktu projektu** wybierz opcję **Kopiuj**.

W obydwu przypadkach spowoduje to wyświetlenie okna dialogowego, w którym można ustawić parametry kopiowanego kontraktu. Okno dialogowe zawiera następujące pola. W zależności od wybranych wartości proces kopiowania może się zmienić.

| Pole | opis | Wpływ zmian w dalszych etapach |
| --- | --- | --- |
| Temat | Wprowadź temat docelowego kontraktu. Po otwarciu okna dialogowego platforma ustawi nazwę tego pola na nazwę kontraktu źródłowego, z dołączonym słowem „copy”. | W tym polu nie ma wpływu zmian na dalsze etapy. |
| kliencie | Odwołanie do rekordu firmy lub konta klienta. Po otwarciu okna dialogowego platforma ustawia to pole na konto z kontraktu źródłowego. | To pole to główny klient kontraktu. |
| Firma będąca właścicielem | Firma odpowiedzialna za realizację projektów skojarzonych z tą transakcją. Po otwarciu okna dialogowego platforma ustawia to pole na firmę będącą właścicielem z kontraktu źródłowego. | Firma będąca właścicielem to osoba prawna, która będzie realizować projektu po sfinalizowaniu transakcji. Waluta firmy będącej właścicielem musi być zgodna z walutą jednostki kontraktującej. |
| Jednostka kontraktująca | Jednostka organizacyjna odpowiedzialna za realizację projektów skojarzonych z tą transakcją. Po otwarciu okna dialogowego platforma ustawia to pole na jednostkę kontraktującą z kontraktu źródłowego. | Jednostka zamawiająca to wydział firmy, który będzie odpowiedzialny za wykonanie projektu po zamknięciu transakcji. Każda jednostka zamawiająca ma walutę. Waluta jest używana do raportowania szacowanych i rzeczywistych kosztów, które poniesiono podczas projektu. |
| Waluta | Waluta, w jakiej obliczana jest kwota oferty. Po otwarciu okna dialogowego platforma ustawia pole na walutę z kontraktu źródłowego. Nie można zmienić waluty. Jeśli tak jest, to pole **Kopiuj kalkulację cen** jest zawsze ustawione na wartość **Nie**, ponieważ cenniki w kontrakcie źródłowym nie są już potrzebne. | Waluta ta jest używana to utworzenia domyślnego cennika, aby wygenerować szacowaną wartość finansową w kontrakcie i tworzyć faktury dla klienta, kiedy oferta przejdzie w fazę realizacji. |
| Żądana data dostawy | Data dostarczenia, której zażądał klient. | Ta wartość jest używana jako data zakończenia podczas tworzenia faktury z wybraną częstotliwością. |
| Kopiuj kalkulację cen | Wartość, która wskazuje, czy wycena z kontraktu powinna zostać skopiowana z kontraktu źródłowego. | Jeśli w polu zostanie wybrana opcja **Tak**, lista produktów i odwołań do cennika projektu jest kopiowana z kontraktu źródłowego do kontaktu docelowego. W przypadku ustawienia wartości **Nie** używane są cenniki na podstawie najnowszych cenników ustawionych dla parametrów projektu. |

Po wybraniu opcji **OK** w oknie dialogowym platforma tworzy kopię kontraktu na podstawie ustawionych wartości parametrów. Następnie zostanie otwarty nowy kontrakt.

Następujące informacje nie **nie** są kopiowane z kontraktu źródłowego do kontraktu docelowego, ponieważ są specyficzne dla każdego kontraktu:

- Harmonogram fakturowania
- Klienci pozycji kontraktów oraz kontraktów
- Odwołanie do projektu w wierszach kontraktu opartego na projekcie
- Informacje o budżecie klienta

Kopiowane są wiersze oferty dotyczące projektów i produktów, szacowania dotyczące szczegółów pozycji kontraktu oraz wartości graniczne nie do przekroczenia na poziomie kontraktu. Wprowadzanie domyślnych cen i stawek kosztów zależy od wartości w polu **Kopiuj kalkulację cen** w oknie dialogowym **Kopiowanie parametrów**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
