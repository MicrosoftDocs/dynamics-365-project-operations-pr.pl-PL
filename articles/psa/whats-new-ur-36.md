---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 36, V3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostępne w programie Microsoft Dynamics 365 Project Service Automation, aktualizacja 36, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/06/2021
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
ms.openlocfilehash: 9b85aed79acb7e7784a23f54a2e9af1cc83f5f4d
ms.sourcegitcommit: 6d9fc4dc851814664bf71729904ab4bedd85fe70
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/06/2021
ms.locfileid: "7606800"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-36-v3"></a>Nowości i zmiany w aplikacji Project Service Automation, wydanie 36, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Z zadowoleniem informujemy, że jest to najnowsza aktualizacja aplikacji Microsoft Dynamics 365 Project Service Automation. To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. Jest ona kompatybilna z Dynamics 365 9.x. Aby dokonać aktualizacji do tego wydania, należy odwiedzić stronę Centrum administracyjnego dla rozwiązań Dynamics 365 online i zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).

W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wydanie aktualizacji 36, V3. Numer tej kompilacji to V3.10.57.152 i jest on zazwyczaj dostępny za pośrednictwem samoaktualizacji w październiku 2021.

## <a name="update-release-36"></a>Wydanie 36

### <a name="bug-fixes"></a>Poprawki błędów

Rozwiązano następujące problemy.

**Ogólne**
- Nazwa pola **Domyślny szablon godziny pracy** jest niepoprawnie przetłumaczona na stronie **Parametry projektu**.
- Asynchroniczne dodatki niepoprawnie obsługują wyjątki dotyczące usługi **SharedVariableService**.

**Czas i wydatek**
- Gdy brakuje wierszy arkusza albo użytkownik nie ma odpowiednich uprawnień do odczytu wierszy arkusza, podczas anulowania zatwierdzeń projektu pojawia się nieprawny błąd.
- Użytkownicy nie mogą anulować zatwierdzania, gdy wydatek lub wpis czasu ma ponad jedno skojarzone zatwierdzenie projektu.
- **Nieobecności** i **Urlopy** są niepoprawnie przetłumaczone na język chiński w danych wyszukiwania na stronie szybkiego tworzenia **Wpisów czasu**.

**Zarządzanie zasobami**
- Użytkownik nie może wyszukać zasobów w **Asystencie planowania**, gdy w trybie widoku jest ustawiony **Dzień**, **Tydzień** lub **Miesiąc**.
- Zasoby ogólne niepoprawnie mogą mieć puste nazwy pozycji. 
- Zamknięcie umowy jako utraconej nie anuluje przyszłych rezerwacji.

**Sprzedaż**
- Gdy w środowisku jest duża ilość produktów, w siatce **Szacowania materiałów** obniża się wydajność.
- Podczas tworzenia projektu z szablonu waluta projektu nie jest domyślną dla odpowiedniej jednostki umowy menedżera projektu.
- Kwoty rzeczywiste nie zawsze są zgodne z tym, co jest odzwierciedlane w należnych projektach lub kwoty stają się ujemne w konkretnych scenariuszach odwołania.
- Błąd występuje w momencie skojarzenia z pozycją kontraktu projektu utworzonego z szablonu projektu.
- Użytkownicy mogą usunąć pozycję kontraktu z punktami kontrolnymi, **Gotowe do zafakturowania** i **Utworzone faktury**. Nie powinno to być dozwolone.
- Podczas importowania szacowań z projektu rozliczanie szczegółów wiersza oferty jest ustawiane niepoprawnie, gdy dla wiersza oferty jest włączone rozliczanie oparte na zadaniach.
- Po dodaniu punktów kontrolnych rozliczania o stałej cenie punkt kontrolny nie jest odzwierciedlany w podsiatce punktów kontrolnych, dopóki strona nie zostanie odświeżona.
- Wyjątek odwołania null jest generowany podczas tworzenia umowy projektu o nazwie oferty o wartości null.
- Zadania w trybie ręcznym, w których waluta projektu różni się od waluty zasobu, są powodować nieprawidłowe szacowania cen.
- Użytkownicy nie mogą odwołać transakcji, która została pomyślnie poprawiona za pomocą faktury poprawionej.
- Zdezaktywowane kategorie transakcji są wyświetlane w siatce **Szacowania wydatków**.



