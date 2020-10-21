---
title: Zaliczka gotówkowa
description: Ten temat zawiera informacje o zaliczkach gotówkowych.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 209fe0b8a79b2c0689c458c423664cb292da249b
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908444"
---
# <a name="cash-advance"></a>Zaliczka gotówkowa

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Zaliczka gotówkowa umożliwia pracownikom pożyczanie pieniędzy z firmy przed poniesieniem kosztów. Po zatwierdzeniu i zapłaceniu zaliczki gotówkowej pracownik może użyć tych pieniędzy do opłacenia poniesionych kosztów prowadzenia działalności. 

## <a name="create-and-submit-a-cash-advance-request"></a>Tworzenie i złożenie prośby o zaliczkę gotówkową

1. W sekcji **Moje wydatki** wybierz opcję **Zaliczki gotówkowe** > **Nowa**, aby utworzyć nową zaliczkę gotówkową. 
2. Na **Nowy wniosek o zaliczkę gotówkową** wprowadź cel wydatku i wybierz lokalizację, w której koszty będą ponoszone.
3. Wprowadź wnioskowaną kwotę i walutę, a następnie wybierz pozycję **Zapisz**. 
4. Kiedy przygotowana prośba o zaliczkę gotówkową będzie gotowa, na stronie **Wniosek o zaliczkę gotówkową** wybierz pozycję **Przepływ pracy** > **Prześlij**.

## <a name="modify-a-cash-advance-request"></a>Modyfikowanie wniosku o zaliczkę gotówkową

Wniosek o zaliczkę gotówkową można modyfikować, jeśli nie został jeszcze przesłany do akceptacji.

1. W obszarze **Moje wydatki: zaliczki gotówkowe** odnajdź i zaznacz zaliczkę gotówkową, która ma być edytowana.
2. Wybierz **Edytuj** i wprowadź wymagane zmiany we wniosku o zaliczkę gotówkową. 
3. Wybierz **Zapisz i zamknij**.


## <a name="view-cash-advance-requests"></a>Wyświetlanie wniosków o zaliczki gotówkowe
Możesz przejrzeć listę wszystkich zaliczek gotówkowych dostępnych w wersji roboczej, przesłanych lub wypłaconych w ramach sekcji **Moje wydatki: zaliczki gotówkowe**. 

## <a name="approve-cash-advance-requests"></a>Zatwierdzanie wniosków o zaliczki gotówkowe

Menedżerowie lub użytkownicy skonfigurowani jako osoby akceptujące w przepływie pracy będą mogli zatwierdzać zaliczki gotówkowe, które zostały przesłane do przeglądu. 

1. Aby zatwierdzić zaliczkę gotówkową, w obszarze **Przetwarzanie zaliczek gotówkowych** wybierz pozycję **Zaliczki gotówkowe do oceny**.
2. Zaznacz zaliczkę, którą chcesz ocenić i wybierz pozycję **Zatwierdź**.  

## <a name="pay-cash-advances"></a>Wypłata zaliczek gotówkowych 
Poniższa procedura jest zwykle wykonywana przez księgowego lub osobę z uprawnieniami do księgowania.

1. W celu zaksięgowania zatwierdzonych zaliczek gotówkowych wybierz opcję **Zaakceptowane zaliczki gotówkowe**, a następnie wybierz pozycję **Wypłata i transfer**.  
2. Wprowadź szczegóły dziennika dotyczące zaliczek gotówkowych, a następnie kliknij przycisk **OK**. 

## <a name="submit-an-expense-report-against-a-paid-cash-advance"></a>Wysyłanie raportu wydatków względem płatnej zaliczki gotówkowej 

Podczas tworzenia i przesyłania raportu wydatków dotyczącego już otrzymanej zaliczki, koszty zostaną automatycznie skorygowane w stosunku do tej zaliczki. Jeśli zaliczka gotówkowa jest większa od wydanej kwoty konieczne jest zwrócenie pozostałej kwoty korzystając z kategorii wydatków **Zwrot gotówki**. Jeśli zaliczka gotówkowa jest mniejsza niż wydana kwota, firma musi zwrócić różnicę. 

### <a name="example"></a>Przykład
Zamierzasz podróżować na konferencję z Seattle do Nowego Jorku. Tworzysz wniosek o zaliczkę w wys. 3000 USD, gdyż tyle będzie szacunkowo kosztować będą bilety na konferencję, przeloty, hotel, posiłki oraz taksówki. Nie otrzymasz środków, chyba że Menedżer zatwierdzi tę prośbę. Po otrzymaniu zatwierdzenia zaliczka w wysokości 3000 USD trafia na Twój rachunek. Bierzesz udział w konferencji. Po zakończeniu podróży okazuje się, że łączna liczba wydatków wyniosła 2790.00 USD. W polu **Metoda płatności** wybierz **Gotówka** i prześlij koszt w wysokości 2790 USD. Przesłana kwota wydatków jest automatycznie porównywana z kwotą zaliczki gotówkowej (3000 USD), która została Ci wcześniej udzielona. Różnicę w wysokości 210 USD (3000 - 2790) musisz zwrócić firmie. Możesz to zrobić za pomocą kategorii wydatków pt. **Zwrot gotówki**. 
