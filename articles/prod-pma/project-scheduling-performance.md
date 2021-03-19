---
title: Wydajność planowania zasobów projektu
description: W tym temacie zamieszczono informacje dotyczące zwiększania wydajności planowania zasobów na dużą liczbę projektów.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 34c31570778f9b64c23387112cf56fa1139cd0fd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289022"
---
# <a name="project-resource-scheduling-performance"></a>Wydajność planowania zasobów projektu

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Problemy dotyczące wydajności związanej z planowaniem zasobów mogą mieć znaczenie, gdy liczba jest bardzo duża. Aby poprawić wydajność planowania zasobów, można uzyskać dostęp do funkcji, która pozwoli użytkownikom skrócić czas potrzebny na uruchomienie formularza dostępności zasobów. W szczególności powoduje to usunięcie procesu synchronizacji zestawienia dyspozycyjności zasobów i użycie tabeli **ResProjectResource** w celu przyspieszenia wyszukiwania zasobów. Zauważ, że tabela **ResRollup** nie będzie już używana.

> [!IMPORTANT]
> Jeśli istnieje zależność między procesem synchronizacji zestawienia wydajności zasobów lub tabelą **ResProjectResource**, nie należy korzystać z tej funkcji.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Włączanie zwiększania wydajności planowania zasobów
Aby włączyć podniesienie wydajności planowania zasobów, należy wykonać następujące kroki.

1. Wybierz kolejno opcje **Zarządzanie funkcjami** > **Wszystkie** i na liście funkcji znajdź pozycję **Włącz funkcję zwiększania wydajności planowania zasobów projektu**.
2. Wybierz opcję **Włącz teraz**.

> [!NOTE]
> Jeśli nie można znaleźć tej funkcji na liście, wybierz pozycję **Sprawdź, czy są aktualizacje** w celu odświeżenia listy.

3. Odśwież przeglądarkę, a następnie przejdź do obszaru **Zarządzanie projektami i księgowanie** > **Okresowe** > **Zasoby projektu** > **Synchronizacja kalendarzy zasobów projektu we wszystkich firmach**.
4. Aby usunąć poprzednie dane, należy ustawić opcję **Usuń istniejące rekordy wydajności** na wartość **Tak**. Jeśli chcesz wygenerować przyrostowe dane, ustaw wartość na **Nie**.
5. W polu **Kod okresu** wybierz okres, w którym mają zostać wygenerowane dane. W przypadku wybrania kodu okresu nie jest konieczne zdefiniowanie daty rozpoczęcia i zakończenia.
6. Jeśli pole **Kod okresu** pozostanie puste, wybierz określone daty rozpoczęcia i zakończenia, aby utworzyć dane.
7. Wybierz pozycję **OK**.

 > [!NOTE]
 > Spowoduje to dystrybuowanie danych ogólnych do tabeli **ResCalendarCapacity** we wszystkich firmach w środowisku, więc zadanie wsadowe musi zostać uruchomione tylko w jednej firmie. Dane w tym zadaniu wsadowym są potrzebne do obliczenia wydajności zasobów za pośrednictwem skojarzonego kalendarza.

8. Przejdź do obszaru **Zarządzanie projektami i księgowanie** > **Okresowe** > **Zasoby projektu** > **Wypełnij zasoby projektu we wszystkich firmach**, a następnie kliknij przycisk **OK**. Jest to skrypt uaktualniania danych dla ogólnych danych w tabelach **ResProjectResource**, **ResCalendarDateTimeRange** oraz **ResEffectiveDateTimeRange**. Wartości pola **PSAPRojSchedRole.RootObject** są również aktualizowane. Jeśli nie zostanie uruchomione, zostanie wyświetlone ostrzeżenie podczas próby wykonania operacji planowania zasobów.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Wyłączanie zwiększania wydajności planowania zasobów

1. Wybierz kolejno opcje **Zarządzanie funkcjami** > **Wszystkie** i wyszukaj opcji **Włącz funkcję zwiększania wydajności planowania zasobów projektu**.
2. Zaznacz funkcję, a następnie wybierz przycisk **Wyłącz**.
3. Odśwież przeglądarkę.
4. Przejdź do **Zarządzanie projektami i księgowanie** > **Okresowe** > **Synchronizacja pojemności** > **Synchronizuj podsumowania pojemności zasobów**.
5. Na stronie **Synchronizacja pojemności** wybierz wartość **Tak** w polu **Usuń istniejące rekordy pojemności**. Jeśli chcesz wygenerować przyrostowe dane, ustaw wartość na **Nie**.
6. W polu **Kod okresu** wybierz okres, w którym mają zostać wygenerowane dane. W przypadku wybrania kodu okresu nie jest konieczne zdefiniowanie daty rozpoczęcia i zakończenia.
7. Jeśli pole **Kod okresu** pozostanie puste, wybierz określone daty rozpoczęcia i zakończenia, aby utworzyć dane.
8. Wybierz pozycję **OK**.

> [!NOTE]
> Spowoduje to dystrybuowanie danych ogólnych do tabeli **ResRollup** we wszystkich firmach w środowisku, więc zadanie wsadowe musi zostać uruchomione tylko w jednej firmie. To zadanie wsadowe jest wymagane we wszystkich widokach **Dostępności zasobów**. Jeśli to zadanie wsadowe nie zostanie uruchomione, dane **ResRollup** będą generowane na żywo, co może zajmować czas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]