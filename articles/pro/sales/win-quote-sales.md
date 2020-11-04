---
title: Zamykanie ofert
description: Ta temat zawiera informacje na temat zamykania ofert w Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081933"
---
# <a name="close-quotes"></a>Zamykanie ofert 

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Ofertę projektu można zamknąć jako wykorzystaną lub utraconą. Operacje aktywowania i zmiany oferty nie są obsługiwane w ramach Microsoft Dynamics 365 Project Operations, więc roboczą ofertę można zamknąć.

## <a name="close-a-quote-as-won"></a>Zamknięcie oferty jako wykorzystaną

Zamknięcie oferty projektu jako wykorzystanej spowoduje zamknięcie oferty z ustawionym stanem „Zamknięty” i przyczyną stanu ustawiona na „Wygrana”. Zamknięcie oferty spowoduje, że projekt stanie się tylko do odczytu i utworzony zostanie kontakt w wersji roboczej, który zawierać będzie informacje z oferty. Ponieważ nie można ponownie otworzyć zamkniętej oferty, przed wprowadzeniem zmian w okienku powiadomień jest dostępne okno dialogowe potwierdzenia. Nie można ponownie otworzyć zamkniętej oferty, a zmiana jest nieodwracalna.

Jeśli oferta jest powiązana z szansą sprzedaży, wszystkie inne oferty projektu w szansie sprzedaży są automatycznie zamykane jako utracone.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Wpływ finansowy zamknięcia oferty jako wykorzystanej

W przypadku istnienia wartości rzeczywistych dla czasu zapisanego w projekcie w czasie, gdy jest on wciąż zapisany w formie wersji roboczej, rejestrowana jest tylko koszt czasu lub wydatku. Po zamknięciu oferty jako wykorzystanej aplikacja przeliczy koszty odwracając starsze koszty w wartościach rzeczywistych i tworząc nowe wartości rzeczywiste kosztów. Aplikacja będzie przetwarzać te same koszty według metody rozliczania w skojarzonej pozycji kontraktu projektu. Jeśli koszt odwołuje się do cz pozycji kontraktu czasu i materiałów, system automatycznie utworzy odpowiednie niezafakturowane wartości rzeczywiste przy zamykaniu oferty i utworzeniu kontraktu projektu. Jeśli referencyjne koszty są odwołaniami do pozycji kontraktu o stałej cenie, aplikacja zatrzyma przetwarzanie wartości rzeczywistych kosztów na podstawie reguł podziału fakturowania dla klientów kontraktów projektów.

## <a name="closing-a-quote-as-lost"></a>Zamykanie oferty jako utraconej:

Zamknięcie oferty projektu jako utraconej spowoduje ustawienie stanu na „Zamknięty” i nada przyczynę stanu „Utracona”. Zamknięcie oferty powoduje, że projekt przejdzie w tryb tylko do odczytu. Ponieważ nie można ponownie otworzyć zamkniętej oferty, przed zamknięciem oferty zostanie wyświetlone okno dialogowe potwierdzenia zmian.

Jeśli oferta projektu, która zostanie zamknięta jako utracona zawiera projekt, do którego odwołuje się dowolny z tych wierszy, projekt jest również oznaczony jako zamknięty, a rezerwacje wszystkich zaksięgowań począwszy od danego dnia są anulowane.

> [!NOTE]
> W Project Operations zamknięcie oferty jako wykorzystanej lub utraconej nie wpłynie na stan szansy sprzedaży, który pozostanie otwarty do momentu jego ręcznego zamknięcia.
