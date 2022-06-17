---
title: Utwórz i zaktualizuj projekt
description: W tym artykule przedstawiono informacje na temat aktualizowania aplikacji Project Operations.
author: ruhercul
ms.date: 10/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: dcb822a726f94a7e8e8621dc7a04f9051168d361
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911103"
---
# <a name="create-and-update-a-project"></a>Utwórz i zaktualizuj projekt

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Poniżej znajduje się podsumowanie pól, które można zaktualizować w projekcie po jego utworzeniu. Obejmuje to również wszelkie stosowne konsekwencje wynikające z tych aktualizacji.

## <a name="project-detail-fields"></a>Pola szczegółów projektu

- **Nazwa**: Nazwa projektu.
- **Opis**: Opis projektu.
- **Klient**: firma, której będzie dostarczony projekt.
- **Szablon kalendarza**: godziny pracy projektu. Po zmianie pola nastąpi ponowne obliczenie całego harmonogramu.
- **Waluta**: Waluta projektu. Domyślna wartość tego pola jest oparta na walucie zdefiniowanej w jednostce umowy. Po zaktualizowaniu jednostki zamawiającej to pole jest również aktualizowane.
- **Jednostka zamawiająca**: jednostka organizacyjna reprezentująca grupę lub oddział firmy, która jest głównie odpowiedzialna za sprzedaż i zarządzanie dostawą pracy i usług do klienta.  Jeśli jednostka organizacyjna kierownika projektu nie jest zdefiniowana, to pole domyślnie przyjmuje wartość zdefiniowaną w parametrach projektu.
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
