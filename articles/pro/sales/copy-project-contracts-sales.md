---
title: Kopiowanie kontraktów projektu
description: W tym temacie zamieszczono informacje o kopiowaniu kontraktów projektu w Project Operations.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6da8e3ba8e062f3e06dc7f440caebdd93e496c65
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081917"
---
# <a name="copying-project-contracts"></a>Kopiowanie kontraktów projektu

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Nowe kontrakty projektów można łatwo utworzyć, tworząc kopie istniejących kontraktów na dwa sposoby: 

  - Na stronie listy **Kontrakty projektów** wybierz kontrakt projektu, a następnie wybierz pozycję **Kopiuj**.
  - Na stronie szczegółów **Kontraktu projektu** wybierz opcję **Kopiuj**.

Spowoduje to otwarcie okna dialogowego, w którym można wprowadzić parametry kopiowanego kontraktu. W oknie dialogowym zawarte są następujące pola. W zależności od wybranych wartości w tym oknie proces kopiowania może ulec zmianie.

| **Pole** | **Stopień zgodności, cel i wskazówki** | **Wpływ zmian w dalszych etapach** |
| --- | --- | --- |
| Temat | Wprowadź temat docelowego kontraktu. Po otwarciu okna dialogowego program ustawi nazwę tego pola na nazwę kontraktu źródłowego z dołączonym elementem **-kopia**. | W tym polu nie ma wpływu zmian na dalsze etapy. |
| Klient | Odwołanie do rekordu firmy lub konta klienta. Po otwarciu okna dialogowego system ustawi to pole na konto z kontraktu źródłowego. | To pole to główny klient kontraktu. |
| Jednostka kontraktująca | Jednostka organizacyjna odpowiedzialna za realizację projektów skojarzonych z tą transakcją. Po otwarciu okna dialogowego system wyświetli jednostkę zamawiającą ze źródłowego kontraktu. | Jednostka zamawiająca to wydział firmy, który będzie odpowiedzialny za wykonanie projektu po zamknięciu transakcji. Każda jednostka zamawiająca ma walutę. Waluta jest używana do raportowania szacowanych i rzeczywistych kosztów poniesionych podczas projektu. |
| Waluta | Waluta, w jakiej obliczana jest kwota oferty. Po otwarciu okna dialogowego system ustawi pole na walutę ze źródłowego kontraktu. Nie można zmienić waluty. Jeśli tak jest, to pole **Kopiuj kalkulację cen** jest zawsze ustawione na wartość **Nie** ponieważ cenniki w kontrakcie źródłowym nie są już potrzebne. | Waluta jest używana to utworzenia domyślnego cennika, aby utworzyć szacowaną wartość finansową w kontrakcie i zafakturować klienta, kiedy oferta przejdzie w fazę realizacji. |
| Żądana data dostawy | Data dostarczenia zażądana przez klienta. | Ta wartość jest używana jako data zakończenia podczas tworzenia faktury w ramach odpowiedniego interwału. |
| Kopiuj kalkulację cen | Wskazuje, czy wycena z kontraktu powinna zostać skopiowana z kontraktu źródłowego. | Jeśli w polu zostanie wybrana opcja **Tak** , lista produktów i odwołań do cennika projektu jest kopiowana z kontaktu źródłowego do kontaktu docelowego. Jeśli wybrana jest opcja **Nie** , cenniki są domyślnie ustawiane na podstawie najnowszych cenników ustawionych dla parametrów projektu. |

Po wybraniu opcji **OK** na stronie dialogu system tworzy kopię kontraktu projektu na podstawie wybranych parametrów. Zostanie otwarty nowy kontrakt.

Poniższe informacje nie są kopiowane z lokalizacji **źródłowej** do **kontraktu docelowego** :

  - Harmonogram fakturowania
  - Klienci pozycji kontraktów oraz kontraktów
  - Odwołanie do projektu w wierszach kontraktu opartego na projekcie
  - Informacje o budżecie klienta

Ponieważ te informacje są specyficzne dla danego kontraktu, te pola i rekordy nie są kopiowane. Kopiowane są wiersze oferty dotyczące projektów i produktów, oszacowania dotyczące szczegółów wierszy kontraktu oraz wartości graniczne nie do przekroczenia na poziomie kontraktu. Domyślne ustawienia cen i stawek kosztów zależą od wartości w polu **Kopiuj kalkulację cen** wybranej na stronie **Kopiowania parametrów**.
