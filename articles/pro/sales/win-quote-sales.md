---
title: Zamknięcie oferty - wersja uproszczona
description: Ta temat zawiera informacje na temat zamykania ofert w Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: bde4794c19dd69b6dd77abf5483c674cd7503d23
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574719"
---
# <a name="close-a-quote---lite"></a>Zamknięcie oferty - wersja uproszczona

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Ofertę projektu można zamknąć jako wykorzystaną lub utraconą. Wersję roboczą oferty można zamknąć, ponieważ operacje Aktywuj i poprawiaj oferty nie są obsługiwane w Microsoft Dynamics 365 Project Operations.

## <a name="close-a-quote-as-won"></a>Zamknięcie oferty jako wykorzystaną

Kiedy zamkniesz wycenę projektu jako Wygrana, stan jest ustawiony na Zamknięty, a przyczyna statusu to Wygrana. Zamknięcie oferty spowoduje, że projekt stanie się tylko do odczytu i utworzony zostanie kontakt w wersji roboczej, który zawierać będzie informacje z oferty. Ponieważ zamkniętej wyceny nie można ponownie otworzyć, okno dialogowe potwierdzenia potwierdzi wprowadzone zmiany.

Jeśli oferta jest powiązana z szansą sprzedaży, wszystkie inne oferty projektu w szansie sprzedaży są automatycznie zamykane jako utracone.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Wpływ finansowy zamknięcia oferty jako wykorzystanej

Jeśli istnieją jakiekolwiek wartości rzeczywiste dotyczące czasu w projekcie, gdy jest on nadal dołączony do projektu wyceny, rejestrowany jest tylko koszt czasu lub wydatków. Po zamknięciu oferty jako wykorzystanej aplikacja przeliczy koszty odwracając starsze koszty w wartościach rzeczywistych i tworząc nowe wartości rzeczywiste kosztów. Aplikacja będzie przetwarzać te same koszty według metody rozliczania w skojarzonej pozycji kontraktu projektu. Jeśli wartości rzeczywiste kosztu odnoszą się do wiersza kontraktu dotyczącego czasu i materiałów, odpowiednie niezafakturowane wartości rzeczywiste sprzedaży są tworzone na czas zamknięcia oferty i utworzenia umowy dotyczącej projektu. Jeśli wartości rzeczywiste kosztu odnoszą się do wiersza umowy o stałej cenie, aplikacja przestanie ponownie przetwarzać wartości rzeczywiste kosztów, które są oparte na regułach rozliczenia podziału dla klientów objętych umową dotyczącą projektu.

## <a name="closing-a-quote-as-lost"></a>Zamykanie oferty jako utraconej:

Kiedy zamkniesz wycenę projektu jako Utracone, stan jest ustawiony na Zamknięty, a przyczyna statusu to Utracone. Zamknięcie oferty powoduje, że projekt przejdzie w tryb tylko do odczytu. Ponieważ nie można ponownie otworzyć zamkniętej oferty, przed zamknięciem oferty zostanie wyświetlone okno dialogowe potwierdzenia zmian.

Jeśli oferta projektu zamknięta jako Utracone odwołuje się do projektu w dowolnym z jego wierszy, ten projekt jest także oznaczony jako Zamknięty. Wszystkie rezerwacje zasobów począwszy od danego dnia są anulowane.

> [!NOTE]
> W Project Operations zamknięcie oferty jako wykorzystanej lub utraconej nie wpłynie na stan szansy sprzedaży, który pozostanie otwarty do momentu jego ręcznego zamknięcia.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]