---
title: Aktualizowanie atrybutów dodatków plug-in w celu dołączenia nowych wymiarów kalkulacji cen
description: W tym temacie zamieszczono informacje dotyczące aktualizowania atrybutów dodatków plug-in o wymiary kalkulacji cen.
author: Rumant
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 0c9ac219dd19cf5dd14d54b199329de0c15fe2ae
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580884"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Aktualizowanie atrybutów dodatków plug-in w celu dołączenia nowych wymiarów kalkulacji cen

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> Użytkownicy, którzy nie korzystają z funkcji sporządzania ofert i zawierania kontraktów dostępnych w programie Project Service Automation, mogą pominąć tę temat.

W tym temacie założono, że przed rozpoczęciem tej procedury użytkownik wykonał procedury opisane w tematach [Tworzenie niestandardowych pól i encji](create-custom-fields-entities.md), [Dodawanie niestandardowych pól do konfiguracji cen i encji transakcyjnych](field-references.md) oraz [Konfigurowanie pól niestandardowych jako wymiarów kalkulacji cen](set-up-pricing-dimensions.md). Jeśli tych procedur jeszcze nie wykonano, wróć, wykonaj je, a następnie wróć do tego tematu.

Podczas tworzenia szczegółów wiersza oferty na stronie **Wiersz oferty** dla wiersza oferty projektu system tworzy w tle dwa wiersze szacowania — jeden dla strony kosztu oszacowania i jeden dla strony sprzedaży. To samo dzieje się dla pozycji kontraktu projektu.

Po dokonaniu zmiany w ilości lub w polu po stronie kosztu zmiana jest rozpowszechniana do strony sprzedaży. Jest to możliwe dzięki następującym dodatkom plug-in, które należy ponownie zarejestrować po modyfikacji wymiarów kalkulacji cen.

- PreOperationContractLineDetailUpdate - aktualizuje obiekt **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate - aktualizuje obiekt **msdyn_quotelinetransaction**.

W poniższych krokach przedstawiono proces rejestrowania dodatków plug-in.

1. Otwórz narzędzie **PluginRegistrationTool** i nawiąż połączenie z wystąpieniem online.
2. Kliknij przycisk **Wyszukaj** i poszukaj dodatku plug-in, który ma zostać zaktualizowany.

 ![Zrzut ekranu drzewa wyszukiwania.](media/PRT-1.png)

3. Po znalezieniu dodatku plug-in zaznacz go, a następnie kliknij opcję **Zaznacz w formularzu głównym**.

4. Zaznacz krok dodatku plug-in, który chcesz zaktualizować, kliknij prawym przyciskiem myszy, a następnie wybierz opcję **Aktualizuj**.

 ![Zrzut ekranu z dodatkiem plug-in, który ma zostać zaktualizowany.](media/PRT-2.png)
 
5. W oknie aktualizowania w atrybutach filtrowania kliknij wielokropek (**...**).

 ![Zrzut ekranu z informacjami konfiguracyjnymi w oknie Aktualizowanie istniejącego kroku.](media/PRT-3.png)
 
6. Zaznacz pola wyboru atrybutów kalkulacji cen.

 ![Zrzut ekranu pokazujący zaznaczenia pól wyboru atrybutów kalkulacji cen.](media/PRT-4.png)

7. Kliknij przycisk **OK**, aby zamknąć stronę, a następnie wybierz pozycję **Aktualizuj krok**.

 ![Zrzut ekranu z widocznym przyciskiem „Aktualizuj krok”.](media/PRT-5.png)
 
8. Powtórz ten proces dla drugiego dodatku plug-in, **PreOperationQuoteLineDetail - aktualizuje obiekt msdyn_quotelinetransaction**.

9. Zamknij narzędzie do rejestrowania dodatków plug-in.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
