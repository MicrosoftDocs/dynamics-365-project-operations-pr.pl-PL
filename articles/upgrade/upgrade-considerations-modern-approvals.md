---
title: Uwagi dotyczące uaktualniania nowoczesnych zatwierdzeń
description: Ten artykuł omawia kwestie, które administratorzy powinni uwzględnić podczas włączania funkcji nowoczesnych zatwierdzeń.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 44a933c92d4ef8dff40f20200d74c4bbdf8caa76
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931757"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Uwagi dotyczące uaktualniania nowoczesnych zatwierdzeń 

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

W ramach wydania Wave 1 z kwietnia 2022 r. funkcja Modern Approvals będzie domyślnie włączona. Ta funkcja poprawia niezawodność logiki zatwierdzania i umożliwia ustalenie przyczyny awarii logiki zatwierdzania.

W ramach tej zmiany zmianie zostaną zaktualizowane zmiany stanu zatwierdzeń projektu. Stan jest teraz przejść bezpośrednio z **przesłanej** do **zatwierdzonej**. **Oczekujące** nie ma już stanu zatwierdzeń. Aby określić, czy zatwierdzenie jest oczekujące, należy sprawdzić, czy to zatwierdzenie należy do zestawu zatwierdzeń, a także sprawdzić stan dołączonego zestawu zatwierdzeń.

## <a name="before-you-upgrade"></a>Przed uaktualnieniem

Przed uaktualnieniem do wersji Nowoczesnych zatwierdzeń należy się upewnić, że nie są oczekujące na zatwierdzenie. Nowoczesnych zatwierdzeń nie używa stanu **Oczekujące**. Z tego powodu wszystkie zatwierdzenia, które są nadal oznaczone jako **Oczekujące** po uaktualnieniu, nie zostaną przetworzone.

## <a name="after-you-upgrade"></a>Po uaktualnieniu

Po uaktualnieniu do wersji Nowoczesnych zatwierdzeń Administrator musi sprawdzić, czy został włączony przepływ w chmurze przetwarzany zatwierdzeń.

1. Logowanie do [flow.microsoft.com](https://flow.microsoft.com)
2. W prawym górnym rogu strony przełącz środowisko na uaktualnione środowisko.
3. Wybierz **pozycję** Rozwiązania, aby wyświetlić listę rozwiązań zainstalowanych w środowisku.
4. Z listy rozwiązań wybierz pozycję **Project Operations** lub **Project Service**.
5. Zmień filtr ze **Wszystkich** na **Przepływy w chmurze**.
6. Sprawdź, czy opcja **Project Service projektu w usłudze projektów — harmonogram** cyklicznie jest ustawiony na **Wł**. Jeśli nie, wybierz przepływ, a następnie wybierz opcję **Włącz**.
7. Sprawdź, czy przetwarzanie występuje co pięć minut, przeglądając **listę Zadania systemowe** w **obszarze Ustawienia**.

## <a name="short-term-rollback"></a>Krótkie wycofać

Jeśli nie można cofnąć zmian lub jeśli wystąpią poważne problemy z tą funkcją, można tymczasowo cofnąć oryginalny przepływ zatwierdzania, wykonując następujące kroki:
1. Zaloguj się do środowiska i sprawdź, czy nie oczekują na zatwierdzenie.
2. Przejdź do **Ustawienia** > **Parametry projektu**.
3. Wybierz **opcję Formant funkcji**, a następnie wybierz opcję **Nowoczesnych zatwierdzeń**, aby wyłączyć funkcję.

## <a name="removing-the-feature-flag"></a>Usunięcie funkcji

W aktualizacji z października 2022 roku możliwość wyłączenia tej funkcji zostanie usunięta.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
