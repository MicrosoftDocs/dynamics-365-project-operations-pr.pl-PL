---
title: Proces konwersji planowania rozwiązania Project Service Automation do Project Operations
description: Ten artykuł zawiera omówienie zmian funkcji z rozwiązania dla Microsoft Dynamics 365 Project Service Automation do Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/07/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 84a40fcc9a8561c4ade0be175b08f701f3196508
ms.sourcegitcommit: 28004d38800782540fa5642d41f8fe0f6e2d9fa5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2022
ms.locfileid: "9642582"
---
# <a name="project-service-automation-to-project-operations-project-scheduling-conversion-process"></a>Proces konwersji planowania rozwiązania Project Service Automation do Project Operations

Po pomyślnym uaktualnieniu projektu Microsoft Dynamics 365 Project Service Automation z wersji 3.X do Dynamics 365 Project Operations w wersji uproszczonej nie jest możliwa edycja zadań projektu w strukturze struktury organizacyjnej pracy siatki zadań (WBS). Klienci będą mogli przeglądać pola WBS w siatce śledzenia, gdzie dodano nowe pola, aby podać wszystkie szczegóły dotyczące zadania. W przypadku projektów, w których wymagane są modyfikacje WBS, można wybiórczo konwertować zakwalifikowane projekty na nowy Project for the Web.

## <a name="project-conversion-process"></a>Proces konwersji projektu

Wykonaj poniższe czynności, aby konwertować projekt.

1. Otwórz stronę główną projektu i wybierz opcję **Konwertuj** w okienku akcji.
1. W oknie z komunikatem potwierdzenia wybierz przycisk **OK**, aby rozpocząć konwersję projektu. Występują następujące akcje:

    1. Pasek komunikatów wyświetlany na stronie głównej projektu zawiera komunikat „Harmonogram projektu jest konwertowany. Do momentu ukończenia konwersji nie można wprowadzać zmian w projekcie”.
    1. Nastąpi przekierowanie do listy projektów.

    Po zakończeniu konwersji projektu nastąpią następujące akcje:

    1. Przypisany menedżer projektu otrzyma powiadomienie po prawej stronie aplikacji.
    1. Pasek komunikatów informujący o tym, że konwersja jest w trakcie realizacji, jest usuwany.
    1. Na karcie **Harmonogram** można wyświetlać nowe funkcje planowania przy użyciu funkcji Project for the Web. Każdy użytkownik, który ma odpowiednie licencje i role zabezpieczeń, może edytować WBS.
    1. Pole **Aparat planowania** zostanie zaktualizowane do wersji **Project for the Web**.
    1. Przycisk **Konwertuj** jest usuwany z okienka akcja.

> [!IMPORTANT]
> Zbiorcze konwersje projektów są niedozwolone. Zaktualizowanie wielu projektów jednocześnie zostanie stłumione. To ograniczenie pomaga zapewnić wysoką wydajność dla wszystkich klientów.

## <a name="manual-tasks-vs-automatic-tasks"></a>Zadania ręczne a zadania automatyczne

W przypadku uaktualnienia środowiska z rozwiązania Project Service Automation do Project Operations wszystkie zadania w WBS są traktowane jako zaplanowane automatycznie. Pojęcie ręcznie zaplanowanych zadań jest niedostępne w aplikacji Project for the Web. Można jednak zdefiniować preferowane zachowanie planowania dla projektów, używając ustawienia [trybu planowania](/project-management/scheduling-modes.md) podczas tworzenia nowych projektów.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Operacje ograniczone w ramach projektów przed konwersją

W tej sekcji określono różnice funkcjonalne, których można się spodziewać, jeśli projekty nie zostały skonwertowane.

### <a name="copy-project"></a>Kopiuj projekt

Operacja **kopiowania** jest obsługiwana tylko w przypadku przekonwertowanych projektów. Uaktualnionych projektów nie można kopiować przed konwersją.

### <a name="move-project"></a>Przenieś projekt

Zmiana daty rozpoczęcia projektu nie spowoduje w sposób odpowiedni przeniesienia rozpoczęcia zadań, o ile projekt nie zostanie przekonwertowany.

## <a name="frequently-asked-questions"></a>Często zadawane pytania

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Jakie są różnice między przekonwertowanymi projektami a nowymi projektami, które utworzono po zakończeniu uaktualniania?

W przypadku projektów przekonwertowanych po uaktualnieniu środowiska zostanie ustawiony nowa flaga, która instruuje harmonogram, aby przestrzegał tylko kalendarza projektu. To zachowanie jest takie samo, jak w przypadku rozwiązania Project Service Automation. Jednocześnie nie będzie można ustawić nowych projektów utworzonych po uaktualnieniu. Z tego powodu harmonogram będzie przestrzegał godzin pracy zasobów przypisanych do zadania.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Co zrobić, jeśli konwersja projektu nie powiedzie się?

Jeśli konwersja projektu nie powiedzie się, pierwszym krokiem jest przejrzenie dzienników błędów w celu zidentyfikowania typowych problemów dotyczących WBS. Jeśli dzienniki nie wskazują na konkretny błąd, na podstawie którego można podjąć działanie, skontaktuj z pomocą techniczną, aby sprawa mogła być głębiej zbadana.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>W jaki sposób aplikacja Project for the Web obsługuje zamknięcie biznesu?

Project for the Web nie przestrzega zamknięcia dni biznesowych zdefiniowanych przez przedsiębiorstwo na poziomie organizacji. Będzie jednak przestrzegać innych typów dni wolnych zdefiniowanych w szablonie podanych godzin pracy.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Jakie są ograniczenia funkcji Project for the Web?

Zobacz [Utwórz strukturę podziału pracy: ograniczenia projektu](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Czy mogę oczekiwać zmian w szacowanych kosztach i sprzedaży?

W rzadkich przypadkach, gdy przydziałów zasobów są ponownie obliczanie lub gdy termin ich realizacji jest inny niż projekt źródłowy, mogą wystąpić różnice w szacowaniu sprzedaży i kosztów. W ramach procesu uaktualnienia klienci powinni przetestować przykładowy zestaw projektów, aby zrozumieć potencjalne zmiany w harmonogramie.
