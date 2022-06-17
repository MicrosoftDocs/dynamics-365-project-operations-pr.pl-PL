---
title: Obsługa członków zespołu
description: Ten artykuł zawiera informacje o rezerwowaniu nazwanych zasobów dla zespołów projektów oraz o przypisywaniu ich do zadań.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 6ab1541cc79870fcab9dbce45073e6b5a7bb0133
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933459"
---
# <a name="maintain-team-members"></a>Obsługa członków zespołu

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Nazwany zasób można dodać do zespołu projektu, rezerwując go bezpośrednio dla zespołu.

1. W programie Dynamics 365 Project Operations wybierz opcję **Projekty** i zaznacz otwarty projekt, dla którego chcesz dokonać rezerwacji.
2. Na stronie **Projekt** na karcie **Zespół** wybierz opcję **Nowy**. 
3. W oknie dialogowym **Szybkie tworzenie członka zespołu projektu** zaznacz zasób możliwy do zarezerwowania. W polu **Rola** zostanie wstawiona domyślna rola zasobu, jeśli jest ona przypisana. Można zmienić rolę. 
4. Wybierz daty początku i końca okresu, w którym zasób będzie potrzebny, oraz wybierz metodę alokacji dyspozycyjności zasobu. 
5. Jeśli chcesz, aby członek zespołu był osobą zatwierdzającą projekt, wybierz opcję **Tak** w polu **Osoba zatwierdzająca projekt**. Ten członek zespołu może zatwierdzać wpisy czasu i wydatków przesłane dla tego projektu. 
6. Wybierz pozycję **Zapisz**.

Teraz zarezerwowany zasób można przypisywać do zadań w projekcie. Na stronie **Projekt** kliknij kartę **Harmonogram**, aby przypisać zadania nowemu zasobowi. Selektor zasobów, który zostanie uruchomiony z pola **Zasoby** w siatce zadań, będzie przedstawiał członków zespołu, których można wybrać.


W Project Operations nie są ściśle sprzężone rezerwacje zasobów i przydziały zadań. Podczas korzystania z selektora zasobów w harmonogramie można przypisywać zadania członkom zespołu na więcej godzin, niż określają ich rezerwacje w projekcie.

Różnice między rezerwacjami członków zespołu i przydziałami są widoczne na kartach **Zespół** oraz **Uzgadnianie zasobów**. Istnieje również możliwość uzgodnienia różnic między zaksięgowaniem a przydziałami dla zasobów na bardziej szczegółowym poziomie.

Użyj selektora zasobów na karcie **Harmonogram** w celu wyszukiwania i zaznaczania zasobów możliwych do zarezerwowania, które jeszcze nie wchodzą w skład zespołu projektu. Zasoby są wyświetlane w selektorze zasobów jako **Inne zasoby**.

Po dokonaniu wyboru zasób zostanie dodany do zespołu projektu i przypisany do zadania, ale nie zostaną wygenerowane żadne rezerwacje.

Aby zarezerwować dyspozycyjność zasobu dla projektu, można użyć funkcji rozszerzania rezerwacji dostępnej na stronie **Uzgadnianie** albo okna **Tablica harmonogramu**.

Gdy członek zespołu jest zarezerwowany dla Twojego projektu, do **zarządzania jego rezerwacjami** możesz używać funkcji **Obsługa rezerwacji** albo bezpośrednio tablicy harmonogramu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]