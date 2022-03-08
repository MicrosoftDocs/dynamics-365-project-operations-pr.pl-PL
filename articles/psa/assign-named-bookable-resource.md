---
title: Rezerwowanie nazwanych zasobów możliwych do zarezerwowania dla zespołu projektu i przypisywanie zadań
description: Ten temat zawiera informacje na temat rezerwowania nazwanych zasobów dla zespołów projektów oraz o przypisywaniu ich do zadań.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8568921dd16472f10a7043c5fe3f58b9f5cd3989ad39e3a3bdf269b0c7203ae2
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998654"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a>Rezerwowanie nazwanych zasobów możliwych do zarezerwowania dla zespołu projektu i przypisywanie zadań 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Nazwany zasób można dodać do zespołu projektu, rezerwując go bezpośrednio dla zespołu. W tym celu wykonaj następujące kroki.

1. W programie Project Service Automation wybierz opcję **Projekty** i zaznacz otwarty projekt, dla którego chcesz dokonać rezerwacji.
2. Na stronie **Projekt** na karcie **Zespół** kliknij opcję **Nowy**. 

![Dodawanie członka zespołu z poziomu karty Zespół.](media/RM-how-to-1.png)

3. W oknie dialogowym **Szybkie tworzenie członka zespołu projektu** zaznacz zasób możliwy do zarezerwowania. W polu **Rola** zostanie wstawiona domyślna rola zasobu, jeśli jest ona przypisana. W razie potrzeby można zmienić rolę. 
4. Wybierz daty początku i końca okresu, w którym zasób będzie potrzebny, oraz wybierz metodę alokacji dyspozycyjności zasobu. 
5. Jeśli chcesz, aby członek zespołu był osobą zatwierdzającą projekt, wybierz opcję **Tak** w polu **Osoba zatwierdzająca projekt**. Oznacza to, że członek zespołu może zatwierdzać wpisy czasu i wydatków przesłane dla tego projektu. 
6. Kliknij przycisk **Zapisz**.

![Dodawanie członka zespołu w formularzu szybkiego tworzenia.](media/RM-how-to-2.png)


Teraz zarezerwowany zasób można przypisywać do zadań w projekcie. Na stronie **Projekt** kliknij kartę **Harmonogram**, aby przypisać zadania nowemu zasobowi. Selektor zasobów, który zostanie uruchomiony z pola **Zasoby** w siatce zadań, będzie przedstawiał członków zespołu, których można wybrać.

![Przypisywanie członka zespołu do zadania na karcie Harmonogram.](media/RM-how-to-3.png)

W wersji 3 programu Project Service Automation (PSA) rezerwacje zasobów i przypisania zadań nie są ściśle powiązane. Oznacza to, że podczas korzystania z selektora zasobów w harmonogramie można przypisywać zadania członkom zespołu na więcej godzin, niż określają ich rezerwacje w projekcie.
Różnice między rezerwacjami członków zespołu i ich przypisaniami można zobaczyć na karcie **Zespół** lub na karcie **Uzgadnianie zasobów**. Istnieje również możliwość uzgadniania różnic między rezerwacjami i przypisaniami zasobów na bardziej szczegółowym poziomie.

![Karta Uzgadnianie zasobów.](media/RM-how-to-4.png)

Można również użyć selektora zasobów na karcie **Harmonogram** w celu wyszukiwania i zaznaczania zasobów możliwych do zarezerwowania, które jeszcze nie wchodzą w skład zespołu projektu. Są one wyświetlane w selektorze zasobów jako **Inne zasoby**.

![Przypisywanie zasobu niebędącego członkiem zespołu do zadania.](media/RM-how-to-5.png)

Po wykonaniu tej czynności zasób zostanie dodany do zespołu projektu i przypisany do zadania, ale nie zostaną wygenerowane żadne rezerwacje.

![Członek zespołu z przypisaniami, ale bez rezerwacji.](media/RM-how-to-6.png)

Aby zarezerwować dyspozycyjność zasobu dla projektu, można użyć funkcji rozszerzania rezerwacji dostępnej na stronie **Uzgadnianie** albo okna **Tablica harmonogramu**.

![Rozszerzanie rezerwacji dla członka zespołu na karcie Uzgadnianie zasobów.](media/RM-how-to-7.png)

Gdy członek zespołu jest zarezerwowany dla Twojego projektu, do zarządzania jego rezerwacjami możesz używać funkcji Obsługa rezerwacji albo bezpośrednio tablicy harmonogramu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]