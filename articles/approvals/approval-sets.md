---
title: Zestawy zatwierdzenia
description: W tym artykule opisano sposób pracy z zestawami zatwierdzeń, żądaniami i podzbiorami tych operacji.
author: stsporen
ms.date: 02/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: ca205073edbce2b399aab3ae273d635c8af96765
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524930"
---
# <a name="approval-sets"></a>Zestawy zatwierdzenia

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Zestawy zatwierdzeń grupują żądania zatwierdzenia w mniejsze podzbiory operacji. Takie grupowanie umożliwia przetwarzanie zatwierdzeń według projektu, w określonej kolejności oraz umożliwia ponowne przetwarzanie i sekwencjonowanie. Grupowanie żądań zatwierdzeń poprawia niezawodność i możliwość śledzenia przetwarzania zatwierdzeń w przypadku dużej liczby zatwierdzeń.

Zestawy zatwierdzeń wskazują ogólny stan przetwarzania powiązanych z nimi rekordów. Kiedy rekord zatwierdzenia jest przetwarzany przy użyciu zestawu zatwierdzeń, rekord zmienia stan z **Przesłany** na **Zatwierdzony** i nie jest już połączony z zestawem zatwierdzeń. Jeśli zapis nie powiedzie się podczas przekazywania go do zatwierdzenia, zapis pozostaje w statusie **Przesłany**, a zestaw zatwierdzający jest oznaczony jako nieudany. Zestaw zatwierdzający rejestruje komunikat błędu o niepowodzeniu.

## <a name="processing-approvals-and-approval-sets"></a>Przetwarzanie zatwierdzeń i zestawów zatwierdzeń
Zatwierdzenia oczekujące w kolejce do przetwarzania widoczne są w widoku **Opracowywanie zatwierdzeń**. W systemie wszystkie wpisy są przetwarzane wiele razy asynchronicznie, co obejmuje ponawianie prób, jeśli poprzednie próby zakończyły się niepowodzeniem.

Pole **Próby zatwierdzenia ogółem** określa ilość prób, które pozostały do przetworzenia zestawu, zanim zostanie on oznaczony jako nieudany.

Zestawy zatwierdzeń są przetwarzane w ramach okresowej aktywacji na podstawie przepływu **w chmurze** o nazwie **Project Service — Recurrently Schedule Project Approval Sets**. Można go znaleźć w **rozwiązaniu** o nazwie **Project Operations**. 

Upewnij się, że przepływ jest aktywowany, wykonując następujące kroki.

1. Jako Administrator zaloguj się do [flow.microsoft.com](https://powerautomate.microsoft.com).
2. W prawym górnym rogu przejdź do środowiska, w którym jest włączana zmiana na Dynamics 365 Project Operations.
3. Wybierz **pozycję** Rozwiązania, aby wyświetlić listę rozwiązań zainstalowanych w środowisku.
4. Z listy rozwiązań wybierz pozycję **Project Operations**.
5. Zmień filtr ze **Wszystkich** na **Przepływy w chmurze**.
6. Sprawdź, czy przepływ **Project Service projektu w usłudze projektów — harmonogram** cyklicznie jest ustawiony na **Wł**. Jeśli nie, wybierz przepływ, a następnie wybierz opcję **Włącz**.
7. Sprawdź, czy przetwarzanie odbywa się co pięć minut, **przeglądając listę Zadań systemowych** w obszarze **Ustawienia** w środowisku Project Operations Dataverse.

## <a name="failed-approvals-and-approval-sets"></a>Nieudane zatwierdzenia i zestawy zatwierdzeń
Widok **Zatwierdzenia zakończone niepowodzeniem** zawiera listę wszystkich zatwierdzeń wymagających interwencji użytkownika. Otwórz dzienniki powiązanych zestawów zatwierdzeń, aby zidentyfikować przyczynę niepowodzenia.
Wybranie opcji **Ponów próbę** dodaje wartość do licznika prób zestawu zatwierdzeń, przywraca zestawowi zatwierdzeń status **Przetwarzanie** i próbuje przetworzyć pozostałe rekordy.

## <a name="configure-approval-sets"></a>Konfiguracja zestawów zatwierdzeń

### <a name="enable-the-approval-sets-feature"></a>Włączanie funkcji Zestawów zatwierdzających
Przed włączeniem funkcji Zestawy zatwierdzeń należy sprawdzić, czy nie są aktualnie przetwarzane żadne zatwierdzenia. Po włączeniu tej funkcji nie można jej wyłączyć.

- Przejdź na stronę **Parametry projektu** i wybierz **Kontrola właściwości** > **Włącz nowe zatwierdzenia**.

### <a name="configuring-the-asynchronous-threshold"></a>Konfiguracja progu asynchronicznego 
Podczas tworzenia zestawów zatwierdzeń przetwarzanie przechodzi na drugi plan, gdy wybrana liczba rekordów do zatwierdzenia przekroczy wskazany próg. Użyj pola **Próg asynchroniczności**, aby ustalić, czy przetwarzanie zatwierdzeń ma się odbywać synchronicznie czy asynchronicznie. Wybierz jedną z poniższych wartości:

  - Zero: Wszystkie żądania powinny być przetwarzane asynchronicznie. 
  - Wartość większa od zera: Zatwierdzenia są przetwarzane asynchronicznie tylko wtedy, gdy przesłana liczba zatwierdzeń przekracza tę wartość.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
