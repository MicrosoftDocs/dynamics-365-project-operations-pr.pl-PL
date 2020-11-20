---
title: Zachowanie interfejsu użytkownika wpisów czasu
description: Ten temat zawiera informacje na temat interfejsu użytkownika wpisów czasu.
author: stsporen
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 8719e2f9ee4867f17ed75142eca2115f61e37999
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124516"
---
# <a name="time-entry-ui-behavior"></a>Zachowanie interfejsu użytkownika wpisów czasu

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_


**Tygodniowa siatka wpisów czasu** jest niestandardową kontrolką, która ma pasek narzędzi i dwie główne sekcje, **Wymiary** oraz **Czas trwania**.

## <a name="dimensions"></a>Wymiary
Sekcja **Wymiary** zawiera wymiary, które mogą być wprowadzane względem danego czasu. Poniższe wymiary są obsługiwane standardowo:

  - Project
  - Zadanie projektu
  - Rola
  - Pisz
  - Stan wpisu

W sekcji **Wymiary** niedozwolona jest edycja w tekście. Ta sekcja jest oparta na widoku, który umożliwia dodawanie niestandardowych pól do tygodniowej siatki wpisów czasu.

## <a name="duration"></a>Czas trwania
Sekcja Czas trwania pokazuje dni tygodnia jako nagłówki kolumn. Ta sekcja zezwala na edycję w tekście. Po utworzeniu wiersza wpisu o odpowiednich wymiarach użytkownicy mogą szybko wprowadzić oraz edytować w tekście czas spędzony na tych wymiarach.

## <a name="create-a-new-time-entry"></a>Tworzenie nowego wpisu czasu

1. W tej siatce wpisu czasu wybierz opcję **Nowa**. 
2. W oknie dialogowym **Szybkie tworzenie wpisu czasu** wybierz datę wpisu czasu.
3. Wprowadź dane dla wymiarów **Projekt**, **Zadania projektu**, **Rola** i **Czas trwania**. Informacje należy dodać w minutach, godzinach lub dniach, wpisując odpowiednio **h**, **m** lub **d** wraz z liczbą. 
4. Wprowadź opis i komentarze dotyczące wpisu, które mogą być udostępniane zewnętrznie dla danego wpisu czasu. 

Przy zapisywaniu wpisu wprowadzone wartości są wyświetlane w sekcji **Wymiary**. Informacje wprowadzone w polu **Czas trwania** są wyświetlane w dniu, w którym utworzono wpis czasu.

Pola wyszukiwania są obsługiwane w widokach systemowych. Na przykład po wejściu do projektu, pole **Zadanie projektu** jest domyślnie ustawione na widok **Kopia**. Aby utworzyć wpisy czasu dla zadań, które nie są przypisane do użytkownika, wybierz **Zmień widok** w oknie dialogowym wyszukiwania i wybierz widok **Wszystkie aktywne zadania projektu**.

## <a name="edit-a-time-entry"></a>Edycja wpisu czasu 
Szczegóły z niektórych pól na stronie wprowadzania godzin, takie jak **Opis** i **Komentarze zewnętrzne**, nie są wyświetlane w siatce zapisu czasu tygodniowego. Zamiast tego w komórkach **czasu trwania** jest wyświetlany niewielki trójkątny wskaźnik, który zawiera te dodatkowe informacje. 

1. Aby przeprowadzić edycję wpisu czasu, wybierz komórkę, do zaktualizowania.
2. Wybierz pozycję **Edytuj szczegóły**, aby zaktualizować dane w okienku **Formularz główny wpisu czasu**. 

## <a name="copy-a-time-entry-row"></a>Kopiowanie wiersza wpisu czasu
Po utworzeniu wiersza można wybrać opcję **Kopiuj wiersz**, aby skopiować cały wiersz do nowego wiersza. Po skopiowaniu wiersza w ten sposób, wymiary i czas trwania również są kopiowane. Można również wybrać opcję **Edytuj wiersz**, w celu zaktualizowania wartości wymiarów i czasów trwania w sekcji **Czas trwania**.

## <a name="open-a-time-entry-behavior"></a>Zachowanie otwierania wpisu czasu
Aby zapewnić optymalne i szybkie wpisywanie w najbardziej widocznych polach, siatka tygodniowego wpisu czasu pokazuje podzbiór wybranych wymiarów i czasów trwania. Aby wyświetlić wszystkie szczegółowe informacje dotyczące pojedynczego wpisu czasu, w obszarze **Edytuj wpis** wybierz polecenie **Otwórz.**

## <a name="submit-a-time-entry"></a>Przesyłanie wpisu czasu
Można przesyłać pojedyncze wpisy czasu lub jako grupy wpisów czasu, wybierając blok komórek lub cały wiersz wpisu czasu, a następnie wybierając opcję **Prześlij**. Przesłane wpisy czasu pojawiają się jako wpisy oczekujące na zatwierdzenie na stronie **Zatwierdzenie** osób zatwierdzających. Po pomyślnym przesłaniu wpisów czasu nie one mogą być edytowane.

## <a name="recall-a-time-entry"></a>Odwoływanie wpisu czasu
Przesłane wpisy czasu można odwoływać. Możesz odwołać pojedynczy wpis czasu, blok wpisów czasu lub cały wiersz wpisów czasu. Wycofane wpisy czasu można edytować.

## <a name="time-entry-status"></a>Stan wpisu czasu

- **Wersja robocza**: Nowe wpisy czasu automatycznie otrzymują status **Wersja robocza**. Usunąć można tylko wpisy czasu ze stanem **Wersja robocza**.
- **Przesłany**: Po przesłaniu wpisu czasu status jest aktualizowany na **Przesłany**. 
- **Zatwierdzony**: Po zatwierdzeniu przesłanego wpisu czasu status jest aktualizowany na **Zatwierdzony**. 
- **Zwrócony**: W przypadku odrzucenia wpisu czasu stan zostanie zaktualizowany na **Zwrócony**, a wpis będzie dostępny do poprawiania i ponownego wysyłania. 

## <a name="view-rejection-comments"></a>Wyświetlanie komentarzy dotyczących odrzucenia
Po odrzuceniu przez osobę zatwierdzającą wpisu czasu osoba zatwierdzająca może dodać komentarze , aby ułatwić zasobowi zrozumienie przyczyny odrzucenia. Aby wyświetlić komentarze dotyczące odrzucenia dla wpisu czasu, wybierz **Otwórz wpis**. Komentarze dotyczące odrzucenia będą widoczne na osi czasu. Użytkownik może odpowiedzieć na komentarze dotyczące odrzucenia, zanim ponownie prześle dany wpis.

## <a name="copy-week"></a>Kopiuj tydzień
Po utworzeniu kilku zapisów czasowych użytkownicy mogą tworzyć wiele wpisów czasu w tym samym czasie.

1. W formularzu **Wpisy czasu** wybierz opcję **Kopiowania tygodnia**, aby zbiorczo utworzyć dodatkowe wpisy czasu. 
2. W oknie dialogowym **Kopia**, w sekcji **Z okresu** użyj pól **Data rozpoczęcia** i **Data zakończenia**, aby zdefiniować zakres dat, z którego mają zostać skopiowane wpisy czasu. 
3. W sekcji **Do okresu** w polu **Data rozpoczęcia** określ dzień, dla którego mają zostać utworzone wpisy czasu. 
4. Wybierz **Kopiuj**. Dla określonej daty w okresie **do** tworzona jest kopia wpisów czasu dla odpowiadającego dnia tygodnia w okresie **od**. Na przykład wpis czasu dla poniedziałku z poprzedniego tygodnia jest kopiowany do poniedziałku tygodnia określonego w grupie pól okresu **do**.

## <a name="import"></a>Import
Ten sam podstawowy proces jest przeznaczony do importowania z rezerwacji, przypisań i wymian. Można określić zakres dat dla rezerwacji, które mają zostać zaimportowane, a następnie po prostu wybrać rezerwacje, które mają zostać utworzone jako wpisy czasu w wersji roboczej. 
