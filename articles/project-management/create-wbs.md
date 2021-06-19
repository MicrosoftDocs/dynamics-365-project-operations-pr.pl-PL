---
title: Tworzenie struktury podziału pracy
description: W tym temacie wyjaśniono, jak utworzyć strukturę podziału pracy (SPP), w tym podstawowe elementy sterujące w nowym interfejsie planowania.
author: ruhercul
ms.date: 01/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ac3facacd95e5e677635cb037d0d3458da612410
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005714"
---
# <a name="create-a-work-breakdown-structure-wbs"></a>Tworzenie struktury podziału pracy (SPP)

Harmonogram projektu komunikuje, co jest niezbędne do wykonania pracy, które zasoby będą za to odpowiedzialne, i w jakich ramach czasowych musi zostać zrealizowana. Harmonogram odzwierciedla wszystkie prace związane z dostarczeniem projektu na czas. W Dynamics 365 Project Operations tworzysz harmonogram projektu poprzez:

  - Podzielenie pracy na łatwe do wykonania zadania.
  - Szacowanie czasu potrzebnego na wykonanie każdego zadania.
  - Ustawianie zależności zadań.
  - Ustawianie czasu trwania zadania.
  - Szacowanie ogólnych zasobów, które będą wykonywać zadania. 

Harmonogram projektu jest tworzony na karcie **Harmonogram** na stronie **Projekt**.

## <a name="tasks"></a>Zadania

Pierwszym krokiem podczas tworzenia harmonogramu projektu jest przerwanie pracy w rozwiązaniu z zarządzanymi porcjami. W harmonogramie Project Operations są obsługiwane następujące funkcje:

- Zadania sumaryczne lub zadania typu kontener
- Zadania węzła liścia

### <a name="summary-tasks"></a>Zadania podsumowujące

Zadania sumaryczne mogą przechowywać inne zadania sumaryczne lub zadania węzłów liści. Nie mają własnych nakładów pracy ani kosztów. Zamiast tego ich nakład pracy i koszt stanowią zestawienie nakładu pracy i kosztu ich zadań kontenera. Data rozpoczęcia zadania sumarycznego to data rozpoczęcia zadań kontenera, a data końcowa to data zakończenia zadań kontenera. Nazwę zadania sumarycznego można edytować, ale nie można edytować właściwości jego planowania, w tym nakład pracy, daty i czas trwania. Usunięcie zadania sumarycznego powoduje również usunięcie wszystkich jego zadań kontenera.

### <a name="leaf-node-tasks"></a>Zadania węzła liścia

Zadania węzła liścia reprezentują najbardziej szczegółowe prace związane z projektem. Mają szacunkowe nakłady pracy, zasoby, planowaną datę rozpoczęcia i zakończenia oraz czas trwania.

## <a name="create-a-task-hierarchy"></a>Tworzenie hierarchii zadań

### <a name="add-a-task"></a>Dodawanie zadania

Wykonaj następujące kroki, aby dodać jedno lub więcej zadań.

1. Wybierz opcję **Projekty** oraz wybierz i otwórz rekord projektu, dla którego chcesz utworzyć harmonogram. 
2. Wybierz kartę **Zadania**. 
3. Wybierz opcję **Dodaj nowe zadanie**, wprowadź nazwę zadania, a następnie naciśnij klawisz Enter.
2. Wprowadź inną nazwę zadania i ponownie naciśnij klawisz Enter, aż uzyskasz pełną listę zadań.

### <a name="manage-hierarchy-of-a-task"></a>Zarządzanie hierarchią zadania

Kiedy zadanie jest wcięte, staje się podrzędne względem zadania, które znajduje się bezpośrednio nad nim. Identyfikator harmonogramu zadania jest następnie przeliczany w taki sposób, aby był oparty na identyfikatorze harmonogramu nowego obiektu nadrzędnego i podążał za schematem numerowania konspektu. Zadanie nadrzędne jest teraz zadaniem podsumowania. Z tego powodu staje się zestawieniem jego zadań podrzędnych. W przypadku podwyższenia poziomu zadania nie jest już ono podrzędne względem zadania, które było dla niego nadrzędne. Identyfikator harmonogramu jest następnie przeliczany w taki sposób, aby odzwierciedlał zaktualizowane wcięcie i pozycję zadania w hierarchii. Nakłady pracy, koszty i daty poprzedniego zadania nadrzędnego są obliczane ponownie, tak aby nie obejmowały tego zadania.

Wykonaj następujące kroki, aby wciąż lub podwyższyć poziom zadania.

1. Na stronie **Projekt** na karcie **Zadania** w obszarze **Zadania sumaryczne**, zaznacz trzy pionowe kropki obok nazwy zadania, a następnie wybierz pozycję **Utwórz podzadanie**. 
2. Wybierz zadanie do dodania lub podwyższenia. Aby zaznaczyć więcej niż jedno zadanie, zaznacz zadanie, naciśnij i przytrzymaj klawisz Ctrl, a następnie wybierz inne zadania.
2. Wybierz **Wcięcie** lub **Podwyższ poziom podzadanie**, aby przenieść zadania do obszaru lub z obszaru Zadania sumaryczne.

### <a name="move-tasks-up-and-down"></a>Przenieś zadania w górę i w dół

Zadania można przenieść na dowolny poziom struktury podziału pracy na jeden z dwóch sposobów:

- Wybierz jeszcze jedno zadanie i przeciągnij je w wybrane miejsce.
- Wybierz jedno lub więcej zadań, kliknij prawym przyciskiem myszy i wybierz **Wytnij**, wybierz komórkę docelową w harmonogramie, a następnie kliknij prawym przyciskiem myszy i wybierz **Wklej**.

## <a name="task-attributes"></a>Atrybuty zadania

Nazwa zadania opisuje czynności, które należy wykonać. W Project Operations atrybuty skojarzone z zadaniem opisują harmonogram zadania i wymagania dotyczące jego personelu.

## <a name="schedule-attributes"></a>Zaplanuj atrybuty

Atrybuty **nakład pracy**, **Data rozpoczęcia**, **Data zakończenia** i **czas trwania** określają harmonogram zadania.

W poniższej tabeli przedstawiono dodatkowe atrybuty harmonogramu.

| **Ostateczna nazwa wyświetlana** | **Ostateczny opis** |
| --- | --- |
| Wykonany nakład pracy (godziny) | Ukończona praca w zadaniu w godzinach. |
| Czas trwania | Pokazuje czas trwania zadania w dniach. |
| Łączny nakład pracy | Łączna ilość pracy w zadaniu w godzinach. |
| Zakończenie | Data i godzina zakończenia. |
| % ukończenia | Procent wykonania zadania. |
| Zasobnik projektu | Zawartość tablicy zadań można pogrupować według zasobników, tak aby każdy zasobnik miał własną kolumnę. |
| Pozostały nakład pracy (godziny) | Pozostała praca w zadaniu w godzinach. |
| Zostanie uruchomiony | Data i godzina rozpoczęcia. |
| Nazwa/nazwisko | Nazwa zadania. |
| IDENTYFIKATOR | Identyfikator zadania w strukturze podziału pracy. |

Jako administrator można definiować pola niestandardowe w jednostce zadania. Jednak pola nie mogą być wyświetlane w siatce harmonogramu. Aby wyświetlić pola niestandardowe, dodaj je do strony szczegółów **Zadania projektu**.

## <a name="staffing-attributes"></a>Atrybuty personelu

Dostęp do atrybutów obsługi personelu jest możliwy za pośrednictwem pola **zasoby** w harmonogramie. Użytkownik może wyszukać istniejący zasób lub wybrać pozycję **Utwórz**, a następnie w okienku **szybkie tworzenie** dodać członka zespołu projektu jako nowy zasób.

Pola **rola**, **jednostka zasobów** i **nazwa stanowiska** są używane do opisywania wymagań dotyczących personelu dla zadania. Te atrybuty personelu wraz z harmonogramem zadań są używane do znajdowania dostępnych zasobów w celu wykonania tego zadania.

   - **Rola**: określa typ zasobu wymagany do wykonania zadania.
   - **Jednostka zasobów**: należy podać jednostkę, z której mają zostać przypisane zasoby dla zadania. Ten atrybut wpływa na koszt i oszacowania sprzedaży danego zadania, jeśli koszt i stawka za dany zasób są ustawiane na podstawie jednostek, które należy pozyskać.
   - **Nazwa stanowiska**: wprowadź przyjazną nazwę zasobu ogólnego służącą jako symbol zastępczy zasobu, który ostatecznie wykona prace.

W polu **zasoby** znajduje się nazwa pozycji zasobu ogólnego lub nazwanego zasobu.

Pole **Kategoria** zawiera wartości wskazujące szerszy typ pracy, do której może zostać zgrupowane zadanie. To pole nie ma wpływu na planowanie ani na kadrę. Zamiast tego pole będzie używane tylko do raportowania.

## <a name="task-dependencies"></a>Zależności między zadaniami

Harmonogram w Project Operations może służyć do tworzenia relacji poprzedników między zadaniami. Pole **Poprzednik** używa co najmniej jednej wartości do wskazania zadań, od których zależy zadanie. Podczas przypisywania wartości poprzednika do zadania, zadanie może się rozpocząć po zakończeniu wszystkich zadań poprzedników. Z powodu zależności planowana data rozpoczęcia zadania jest ustawiana na dzień, w którym wykonane zostaną zadania poprzednika.

Tryb zadania nie ma wpływu na aktualizacje wprowadzane do dat rozpoczęcia i zakończenia zadań poprzednika/zależnych.

## <a name="accessibility-and-keyboard-shortcuts"></a>Skróty klawiaturowe i ułatwienia dostępu

Siatka **harmonogramu** jest w pełni dostępna i może być używana z czytnikami ekranu, takimi jak Narrator, JAWS lub NVDA. Aby przechodzić między obszarem siatki za pomocą klawiszy strzałek (jak w Microsoft Excel), można użyć klawisza Tab w celu przechodzenia między elementami interaktywnego interfejsu użytkownika i można użyć klawisza strzałki w dół, klawisza Enter lub klawisza spacji w celu wybrania i otwarcia menu rozwijanego.


[!INCLUDE[footer-include](../includes/footer-banner.md)]