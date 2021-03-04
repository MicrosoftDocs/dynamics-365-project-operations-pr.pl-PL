---
title: Potwierdzenie kontraktu projektu
description: Ten temat zawiera informacje na temat potwierdzenia kontraktu projektu w Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24da0887c0266d51bddcbbf8efd6f2644b6d0f4f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128296"
---
# <a name="confirm-a-project-contract"></a>Potwierdzenie kontraktu projektu

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Kontrakt projektu w Dynamics 365 Project Operations może być aktywny i mieć powód **Potwierdzony** lub zamknięty z powodem **Utracony**. Podczas potwierdzania kontraktu projektu, jego stan zmienia się z **Wersji roboczej** na **Aktywna**, a przyczyna stanu to **Potwierdzony**. Nie można edytować ani ponownie otworzyć aktywnego lub zamkniętego kontraktu. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Finansowy wpływ potwierdzenia kontraktu dotyczącego projektu

Po potwierdzeniu projektu kontraktu aplikacja przeliczy koszty odwracając starsze koszty w wartościach rzeczywistych i tworząc nowe wartości rzeczywiste kosztów. Nowe koszty rzeczywiste zostaną przetworzone na podstawie metody rozliczeń powiązanej z projektem w skojarzonej pozycji kontraktu projektu. Jeśli koszt rzeczywisty odnosi się do wierszu kontraktu Czas i materiały, aplikacja automatycznie ponownie tworzy odpowiednie niezafakturowane wartości rzeczywiste dotyczące sprzedaży. Jeśli koszty rzeczywiste odwołują się do pozycji kontraktu o stałej cenie, aplikacja zatrzymuje przetwarzanie wartości rzeczywistych kosztów.

Limity nie do przekroczenia, konfiguracja obciążeń oraz koszty i ceny w wartościach rzeczywistych są oceniane i potem aktualizowane w ramach procesu potwierdzenia.

## <a name="close-a-project-contract-as-lost"></a>Zamykanie kontraktu jako utraconego

Po zamknięciu kontraktu projektu jako utraconego stan kontraktu jest aktualizowany na **Zamknięty** i przyczyna stanu zostaje ustawiona na **Utracony**. Kontrakt dotyczący projektu staje się dostępny tylko do odczytu. Przed ukończeniem zmian dostępne jest okno dialogowe potwierdzenia, ponieważ nie będzie można ponownie otworzyć zamkniętego kontraktu dotyczącego projektu.

Jeśli kontrakt projektu, który został zamknięty jako utracony, odwołuje się do wierszy projektu, projekt jest również oznaczony jako zamknięty. Wszystkie rezerwacje zasobów począwszy od danego dnia są anulowane. Wszelkie nierozliczone wartości rzeczywiste dotyczące sprzedaży w kontrakcie projektu, które nie są jeszcze zawarte w fakturze, zostaną anulowane.

> [!NOTE]
> W przypadku Dynamics 365 Project Operations zamknięcie kontraktu dotyczącego projektu jako utraconego nie wpłynie na stan skojarzonej szansy sprzedaży. Szansa sprzedaży pozostanie otwarta i należy ją zamknąć ręcznie.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]