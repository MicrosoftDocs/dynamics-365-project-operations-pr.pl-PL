---
title: Aktualizowanie atrybutów dodatków plug-in przy użyciu nowych wymiarów kalkulacji cen
description: W tym temacie zamieszczono informacje dotyczące sposobu aktualizowania atrybutów dodatków plug-in o wymiary kalkulacji cen.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b3b441b9ea0418e10db80a86613b2c41ea2c4673
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575041"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Aktualizowanie atrybutów dodatków plug-in przy użyciu nowych wymiarów kalkulacji cen

W tym temacie zamieszczono informacje dotyczące sposobu aktualizowania atrybutów dodatków plug-in o wymiary kalkulacji cen.

> [!NOTE]
> Ta temat ma zastosowanie wyłącznie do funkcji ofert i kontraktów w aplikacji Dynamics 365 Project Operations.

## <a name="prerequisites"></a>Wymagania wstępne
Przed wykonaniem czynności opisanych w tym temacie należy wykonać procedury opisane w następujących tematach:

  - [Tworzenie niestandardowych pól i encji](create-custom-fields-entities-pricing-dimensions.md) 
  - [Dodawanie pól niestandardowych do ustawień cen i encji transakcyjnych ](add-custom-fields-price-setup-transactional-entities.md)
  - [Konfigurowanie pól niestandardowych jako wymiarów kalkulacji cen](set-up-custom-fields-pricing-dimensions.md). 
  
Jeśli tych procedur jeszcze nie wykonano, wykonaj je, a następnie wróć do tego tematu.

## <a name="register-a-plug-in"></a>Rejestrowanie dodatku plug-in
W przypadku tworzenia szczegółów wiersza oferty na stronie **Wiersz oferty** dla wiersza oferty projektu system tworzy dwa wiersze szacowania. Jeden wiersz to szacowanie po stronie kosztów, a drugi wiersz — po stronie sprzedaży. To samo dzieje się dla pozycji kontraktu projektu.

Po dokonaniu zmiany w ilości lub w polu po stronie kosztu zmiana jest również dokonywania po stronie sprzedaży. Jest to możliwe, ponieważ dodatki plug-in PreOperations w encjach szczegółów wiersza oferty i szczegółów wiersza kontraktu łączą określone atrybuty po stronie kosztów ze stroną sprzedaży transakcji. Jeśli zmiany wartości wymiarów kalkulacji cen wprowadzone po stronie sprzedaży mają zostać zastosowane również po stronie kosztów, należy ponownie zarejestrować następujące dodatki plug-in po wprowadzeniu zmian wymiaru kalkulacji cen.

Oto dodatki plug-in do zaktualizowania i ponownego zarejestrowania:

- PreOperationContractLineDetailUpdate — **aktualizuje obiekt msdyn_orderlinetransaction**
- PreOperationQuoteLineDetailUpdate — **aktualizuje obiekt msdyn_quotelinetransaction**

Wykonaj poniższe kroki, aby zaktualizować i ponownie zarejestrować dodatki plug-in.

1. Otwórz narzędzie **PluginRegistrationTool** i połącz się ze środowiskiem usługi Project Operations Dataverse.
2. Wybierz opcję **Wyszukaj** i wpisz kilka pierwszych liter dodatku plug-in, który ma zostać zaktualizowany.
3. Po znalezieniu dodatku plug-in zaznacz go, a następnie wybierz opcję **Zaznacz w formularzu głównym**.
4. Wybierz krok **Aktualizuj obiekt msdyn_orderlinetransaction**, kliknij go prawym przyciskiem myszy, a następnie wybierz opcję **Aktualizuj**.
5. W oknie dialogowym **Aktualizowanie** wybierz wielokropek (**...**) w atrybutach filtrowania.
6. Zostanie otwarte okno atrybutów filtrowania z listę wszystkich atrybutów encji i wymiarów kalkulacji cen. Zaznacz pola wyboru dla atrybutów wymiarów kalkulacji cen.
7. Wybierz przycisk **OK**, aby zamknąć stronę, a następnie wybierz pozycję **Aktualizuj krok**.
8. Powtórz kroki 2–7 dla drugiego dodatku plug-in, **PreOperationQuoteLineDetail**. Dla tego dodatku plug-in musisz zaktualizować krok **Aktualizuj obiekt msdyn_quotelinetransaction**.
9. Zamknij narzędzie **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]