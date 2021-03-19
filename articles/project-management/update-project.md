---
title: Aktualizowanie projektu
description: W tym temacie zamieszczono informacje o aktualizowaniu projektu w Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27444b072bdf7de55d6b38c30c1ea5fe66ed46ac
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286396"
---
# <a name="update-a-project"></a>Aktualizowanie projektu

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Poniżej zamieszczono podsumowanie pól, które mogą być aktualizowane po utworzeniu projektu oraz wszystkich odpowiednich skutków aktualizacji.

## <a name="project-detail-fields"></a>Pola szczegółów projektu

- **Nazwa**: Nazwa projektu.
- **Opis**: Opis projektu.
- **Klient**: firma, której będzie dostarczony projekt.
- **Szablon kalendarza**: godziny pracy projektu. Po zmianie pola nastąpi ponowne obliczenie całego harmonogramu.
- **Waluta**: Waluta projektu. Wartość domyślna tego pola jest określana na podstawie waluty określonej w obszarze jednostki zamawiającej. Po zaktualizowaniu jednostki zamawiającej to pole jest również aktualizowane.
- **Jednostka zamawiająca**: jednostka organizacyjna reprezentująca grupę lub oddział firmy, która jest głównie odpowiedzialna za sprzedaż i zarządzanie dostawą pracy i usług do klienta. 
- **Menedżer projektu**: członek zespołu projektu, który ma uprawnienia do przeglądania i zatwierdzania wpisów czasu oraz wydatków.

## <a name="estimate-fields"></a>Pola oszacowań

- **Szacowana data rozpoczęcia**: Data rozpoczęcia projektu. Po zaktualizowaniu tego pola wszelkie zadania w projekcie będą proporcjonalnie przesunięte względem nowej daty rozpoczęcia.
- **Data zakończenia**: planowana data zakończenia projektu.
- **Nakład pracy**: szacowany nakład pracy w projekcie. W przypadku dodawania zadań do projektu to pole nie jest już dostępne do edycji.
- **Szacowany koszt pracy**: szacowany koszt pracy w projekcie. W przypadku dodawania kosztów pracy do projektu to pole nie jest już dostępne do edycji.
- **Szacowane wydatki**: szacowane wydatki w projekcie. W przypadku dodawania wydatków do projektu to pole nie jest już dostępne do edycji.

## <a name="project-actual-fields"></a>Pola wartości rzeczywistych projektu
- **Rzeczywisty początek**: Data rozpoczęcia projektu.
- **Rzeczywisty koniec**: do zaktualizowania po zakończeniu projektu.

## <a name="project-status-fields"></a>Pole stanu projektu

- **Ogólny stan projektu**: ogólna kondycja projektu podana przez menedżera projektu.
- **Komentarze**: Opis aktualnej kondycji projektu dostarczony przez menedżera projektu.



[!INCLUDE[footer-include](../includes/footer-banner.md)]