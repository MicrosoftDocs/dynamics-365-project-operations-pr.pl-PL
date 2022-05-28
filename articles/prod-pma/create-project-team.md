---
title: Tworzenie zespołu projektu
description: W tym temacie zamieszczono informacje dotyczące tworzenia nowego zespołu projektu i zarządzania nim.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f134d7566954e640eea8ff8af98e184273ad570c
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683045"
---
# <a name="create-a-project-team"></a>Tworzenie zespołu projektu

[!include [banner](../includes/banner.md)]

Aby użyć ról, które zostały wcześniej skonfigurowane w projekcie, kierownik projektu musi skojarzyć role z projektem. Do danego projektu można przypisać wiele ról. W celu uniknięcia niejasności te role są automatycznie oznaczane podczas rezerwacji. Na przykład, jeśli kierownik projektu wymaga trzech inżynierów oprogramowania, trzy role inżyniera oprogramowania, których etykiety mają **inżyniera oprogramowania 1**, **inżyniera oprogramowania 2** i **inżyniera oprogramowania 3**, są generowane automatycznie. Jeśli właściwości roli zostały wcześniej ustawione dla roli, są one stosowane jako filtr podczas wyszukiwania zasobu. Dodatkowe charakterystyki można dodać w zależności od potrzeb, aby dokładniej uściślić wyszukiwanie.

Ustawienia widoku mogą być również dostosowywane w celu lepszego wyświetlenia dostępności zasobów. Dostępne są opcje umożliwiające pokazanie godzinowych, dziennych, tygodniowych, miesięcznych i rocznych oraz rocznej dostępności. Istnieje również możliwość wyświetlenia dostępnej i pozostałej wydajności zasobów. Ta opcja jest przydatna przy szacowaniu czasu dostępności, kiedy oceniany jest dostępny czas na działania lub dostępność zasobów.

Kierownik projektu może wybrać rolę na stronie, a następnie, jeśli dostępny jest zasób, który spełnia wymagania, może zarezerwować zasób do wypełnienia roli. Należy pamiętać, że zasoby nie muszą być rezerwowane w tym punkcie etapu planowania. Podczas tworzenia SPP można zastępować role przy użyciu zasobów pracowniczych dla danego projektu. Jeśli role zostaną zamienione na zasoby służbowe w SPP, konfiguracja zasobu powoduje automatyczne zaktualizowanie listy i harmonogramu planowania zespołu projektu.

[![Lista zespołu projektowego zawierająca zarówno role, jak i rzeczywiste zasoby.](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Menedżer projektu ma różne opcje rezerwacji zasobu, takie jak **Wydajność pozostała**, **Pełna wydajność**, **Procent wydajności** i **Określona liczba godzin**. Te opcje rezerwacji można anulować w dowolnym momencie, jeśli zmienią się przydziały zasobów. Obsługiwane są dwa typy rezerwacji:

- **Rezerwacja ostateczna** — Rezerwacja zasobów została zatwierdzona i potwierdzona do pracy nad zaangażowaniem przez określony czas.
- **Wstępna rezerwacja** — Rezerwacje zasobów zostały wstępnie ustawione do pracy nad zaangażowaniem przez określony czas.

Poniższa procedura wyjaśnia, jak utworzyć zespół projektowy.

## <a name="create-a-project-team"></a>Tworzenie zespołu projektu

1. Na stronie lista **Wszystkie projekty** wybierz projekt, a następnie wybierz pozycję **Edytuj**.
2. Na karcie **Zespół projektowy i planowanie** w polu **Data zakończenia harmonogramu** wprowadź datę rozpoczęcia harmonogramu plus jeden miesiąc. Jeśli na przykład Data rozpoczęcia planowania wynosi 24 czerwca 2017 (24/06/2017), wprowadź **24/07/2017**.
3. Wybierz **Dodaj**.
4. W okienku **Dodaj role do projektu**, w polu **Rola** wybierz pozycję **Starszy kierownik projektu**.
5. Wybierz **Wymagane kompetencje**.
6. Na stronie **Wybierz cechy** cechy, które zostały wcześniej ustawione dla roli starszego kierownika projektu, są zaznaczone domyślnie. Wybierz pozycję **OK**.
7. Na stronie **Dodawanie ról do projektu**, w polu **Liczba zasobów**, wprowadź wartość **1**.
8. W polu **Zasób** jest wyświetlane wszystkie zasoby o wymaganych kwalifikacjach. Wybierz opcję **Daniel Goldschmidt**, a następnie wybierz pozycję **Utwórz**.
9. Na stronie **Projekt** wybierz opcję **Dodaj**.
10. W okienku **Dodaj role do projektu**, w polu **Rola** wybierz pozycję **Członek zespołu**. W polu **Liczba zasobów** wprowadź liczbę **5**.
11. Wybierz pozycję **Utwórz**.
12. Na stronie **Projekty** wybierz pozycję **Spełniaj zasoby**.

## <a name="monitor-project-teams"></a>Monitoruj zespoły projektów
1. Na stronie **Wszystkie projekty** wybierz łącze **Identyfikator projektu** dla projektu **XYZ uaktualnianie faza 2**.
2. Na skróconej karcie **Zespół projektowy i planowanie** sprawdź, czy wymienione zasoby projektu są poprawne.


[!INCLUDE[footer-include](../includes/footer-banner.md)]