---
title: Zamknij ofertę
description: Ta temat zawiera informacje na temat zamykania ofert w Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3c429fa14b4b95420c67a91a6a59af7db2660f68
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898904"
---
# <a name="close-a-quote"></a>Zamknij ofertę

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Ofertę projektu można zamknąć jako wykorzystaną lub utraconą. Operacje aktywowania i zmiany oferty nie są obsługiwane w ramach Microsoft Dynamics 365 Project Operations, więc roboczą ofertę można zamknąć.

## <a name="close-a-quote-as-won"></a>Zamknięcie oferty jako wykorzystaną

Zamknięcie oferty projektu jako wykorzystanej spowoduje zamknięcie oferty z ustawionym stanem **Zamknięty** i przyczyną stanu ustawiona na **Wygrana**. Zamknięcie oferty spowoduje, że projekt stanie się tylko do odczytu i utworzony zostanie kontakt w wersji roboczej, który zawierać będzie wszystkie informacje z oferty. Ponieważ nie można ponownie otworzyć zamkniętej oferty, przed zamknięciem oferty zostanie wyświetlone okno dialogowe potwierdzenia zmian.

Kontrakt utworzony na podstawie oferty projektu jest udostępniany również w module Zarządzanie projektami i księgowości w Project Operations. Jeśli kontrakt projektu nie jest zamapowany do projektu w żadnym z jego wierszy, ten kontrakt jest udostępniany jako nieaktywny kontrakt projektu i będzie aktywny zaraz po zamapowaniu projektu do co najmniej jednej z pozycji kontraktu.

Jeśli oferta jest powiązana z szansą sprzedaży, wszystkie inne oferty projektu w szansie sprzedaży są automatycznie zamykane jako utracone.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Wpływ finansowy zamknięcia oferty jako wykorzystanej

W przypadku istnienia wartości rzeczywistych dla czasu zapisanego w projekcie w czasie, gdy jest on wciąż zapisany w formie wersji roboczej, rejestrowana jest tylko koszt czasu lub wydatku. Po zamknięciu oferty jako wykorzystanej aplikacja przeliczy koszty odwracając starsze koszty w wartościach rzeczywistych i tworząc nowe wartości rzeczywiste kosztów. Aplikacja będzie przetwarzać te same koszty według metody rozliczania w skojarzonej pozycji kontraktu projektu. Jeśli koszt odwołuje się do cz pozycji kontraktu czasu i materiałów, system automatycznie utworzy odpowiednie niezafakturowane wartości rzeczywiste przy zamykaniu oferty i utworzeniu kontraktu projektu. Jeśli referencyjne koszty są odwołaniami do pozycji kontraktu o stałej cenie, aplikacja zatrzyma przetwarzanie wartości rzeczywistych kosztów na podstawie reguł podziału fakturowania dla klientów kontraktów projektów.

Wszystkie ponownie przetworzone wartości rzeczywiste są dostępne w module Zarządzanie projektami i ich księgowanie dla konta projektu, które można przejrzeć, zaktualizować i wysłać do księgi głównej. 

## <a name="close-a-quote-as-lost"></a>Zamknięcie oferty jako utraconej

Zamknięcie oferty projektu jako utraconej spowoduje ustawienie stanu na **Zamknięty** i nada przyczynę stanu **Utracona**. Zamknięcie oferty powoduje, że wejdzie ona w tryb tylko do odczytu. Ponieważ nie można ponownie otworzyć zamkniętej oferty, przed zamknięciem oferty zostanie wyświetlone okno dialogowe potwierdzenia zmian.

Jeśli oferta projektu, która zostanie zamknięta jako utracona zawiera projekt, do którego odwołuje się dowolny z tych wierszy, projekt jest również oznaczony jako zamknięty, a rezerwacje wszystkich zaksięgowań począwszy od danego dnia są anulowane.

> [!NOTE]
> W Project Operations zamknięcie oferty jako wykorzystanej lub utraconej nie wpłynie na stan szansy sprzedaży, który pozostanie otwarty do momentu jego ręcznego zamknięcia.
