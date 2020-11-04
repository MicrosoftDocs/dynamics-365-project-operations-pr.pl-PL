---
title: Aktualizowanie projektu
description: W tym temacie zamieszczono informacje o aktualizowaniu projektu w Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 5c9cd0c7c6886bd454c5f2ef2ae7f20d1707293f
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081867"
---
# <a name="update-a-project"></a>Aktualizowanie projektu

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Poniżej zamieszczono podsumowanie pól, które mogą być aktualizowane po utworzeniu projektu oraz wszystkich odpowiednich skutków aktualizacji.

## <a name="project-detail-fields"></a>Pola szczegółów projektu

- **Nazwa** : Nazwa projektu.
- **Opis** : Opis projektu.
- **Klient** : firma, której będzie dostarczony projekt.
- **Szablon kalendarza** : godziny pracy projektu. Po zmianie pola nastąpi ponowne obliczenie całego harmonogramu.
- **Waluta** : Waluta projektu. Wartość domyślna tego pola jest określana na podstawie waluty określonej w obszarze jednostki zamawiającej. Po zaktualizowaniu jednostki zamawiającej to pole jest również aktualizowane.
- **Jednostka zamawiająca** : jednostka organizacyjna reprezentująca grupę lub oddział firmy, która jest głównie odpowiedzialna za sprzedaż i zarządzanie dostawą pracy i usług do klienta. 
- **Menedżer projektu** : członek zespołu projektu, który ma uprawnienia do przeglądania i zatwierdzania wpisów czasu oraz wydatków.

## <a name="estimate-fields"></a>Pola oszacowań

- **Szacowana data rozpoczęcia** : Data rozpoczęcia projektu. Po zaktualizowaniu tego pola wszelkie zadania w projekcie będą proporcjonalnie przesunięte względem nowej daty rozpoczęcia.
- **Data zakończenia** : planowana data zakończenia projektu.
- **Nakład pracy** : szacowany nakład pracy w projekcie. W przypadku dodawania zadań do projektu to pole nie jest już dostępne do edycji.
- **Szacowany koszt pracy** : szacowany koszt pracy w projekcie. W przypadku dodawania kosztów pracy do projektu to pole nie jest już dostępne do edycji.
- **Szacowane wydatki** : szacowane wydatki w projekcie. W przypadku dodawania wydatków do projektu to pole nie jest już dostępne do edycji.

## <a name="project-actual-fields"></a>Pola wartości rzeczywistych projektu
- **Rzeczywisty początek** : Data rozpoczęcia projektu.
- **Rzeczywisty koniec** : do zaktualizowania po zakończeniu projektu.

## <a name="project-status-fields"></a>Pole stanu projektu

- **Ogólny stan projektu** : ogólna kondycja projektu podana przez menedżera projektu.
- **Komentarze** : Opis aktualnej kondycji projektu dostarczony przez menedżera projektu.

