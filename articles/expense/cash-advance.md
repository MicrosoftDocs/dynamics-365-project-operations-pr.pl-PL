---
title: Zaliczka gotówkowa
description: Ten temat zawiera informacje o zaliczkach gotówkowych.
author: suvaidya
manager: AnnBe
ms.date: 02/01/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6da50ac5611fcbd54aef8d8591ee112200468177
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276721"
---
# <a name="cash-advance"></a>Zaliczka gotówkowa

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Zaliczka gotówkowa umożliwia pracownikom pożyczanie pieniędzy z firmy przed poniesieniem kosztów. Po zatwierdzeniu i zapłaceniu zaliczki gotówkowej pracownik może użyć tych pieniędzy do opłacenia poniesionych kosztów prowadzenia działalności. 

## <a name="create-and-submit-a-cash-advance-request"></a>Tworzenie i złożenie prośby o zaliczkę gotówkową
Aby utworzyć nową zaliczkę z góry i złożyć wniosek o zaliczkę, wykonaj następujące czynności: 

1. W obszarze **Moje koszty** wybierz **Zaliczki gotówkowe** > **Nowe**. 
2. Na **Nowy wniosek o zaliczkę gotówkową** wprowadź cel wydatku i wybierz lokalizację, w której koszty będą ponoszone.
3. Wprowadź wnioskowaną kwotę i walutę, a następnie wybierz pozycję **Zapisz**. 
4. Kiedy przygotowana prośba o zaliczkę gotówkową będzie gotowa, na stronie **Wniosek o zaliczkę gotówkową** wybierz pozycję **Przepływ pracy** > **Prześlij**.

## <a name="modify-a-cash-advance-request"></a>Modyfikowanie wniosku o zaliczkę gotówkową

Wniosek o zaliczkę gotówkową można modyfikować, jeśli nie został jeszcze przesłany do akceptacji.

1. W obszarze **Moje koszty: Zaliczki gotówkowe** i wybierz zaliczki gotówkowe do edycji.
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

Po utworzeniu i przesłaniu raportu z wydatków dla zaliczki gotówkowej, którą już otrzymałeś, wydatki zostaną automatycznie skorygowane o tę zaliczkę. Jeśli zaliczka gotówkowa jest większa od wydanej kwoty konieczne jest zwrócenie pozostałej kwoty korzystając z kategorii wydatków **Zwrot gotówki**. Jeśli zaliczka gotówkowa opłacona przez firmę jest mniejsza niż kwota, którą wydałeś, firma musi zwrócić Ci saldo. 

### <a name="example"></a>Przykład
Planujesz podróż z Seattle do Nowego Jorku na konferencję. Tworzysz żądanie zaliczki na kwotę 3000,00 USD na podstawie szacunkowego kosztu biletu konferencyjnego, przelotów, hotelu, posiłków i taksówki. Nie otrzymasz zapłaty, dopóki Twój menedżer nie zatwierdzi tej prośby. Po otrzymaniu zatwierdzenia zaliczka w wysokości 3000 USD trafia na Twój rachunek. Bierzesz udział w konferencji. Po zakończeniu podróży okazuje się, że łączna liczba wydatków wyniosła 2790.00 USD. Wybierz opcję **Gotówka** w polu **Metoda płatności** i prześlij koszt o wartości 2790,00 USD. Przesłana kwota wydatków jest automatycznie porównywana z kwotą zaliczki gotówkowej (3000 USD), która została Ci wcześniej udzielona. Teraz jesteś winien saldo w wysokości 210,00 USD (3000,00 - 2790,00), które możesz zwrócić firmie za pomocą kategorii **Zwrot gotówki**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]