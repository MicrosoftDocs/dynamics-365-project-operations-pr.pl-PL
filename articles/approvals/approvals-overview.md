---
title: Omówienie zatwierdzeń
description: Ta temat zawiera informacje na temat pracy z zatwierdzeniami w Project Operations.
author: stsporen
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 5e30b8a386805faee869f77e695d5ee492d78cdb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996714"
---
# <a name="approvals-overview"></a>Omówienie zatwierdzeń

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Informacje dotyczące czasu, wydatków i materiałów są przepływem pracy zatwierdzania. Po zatwierdzeniu wpisów transakcje są rejestrowane w wartościach rzeczywistych lub czasu zaksięgowanych w harmonogramie.

## <a name="approvals-workflow"></a>Przepływ pracy zatwierdzenia
Podczas tworzenia i przesyłania wpisu czasu, wydatków lub zużycia materiałów tworzony jest rekord zatwierdzenia. Osoba zatwierdzająca projekt lub menedżer przegląda i zatwierdza wpis. Jeśli wpis dotyczy projektu, dane rzeczywiste zostaną utworzone po jego zatwierdzeniu. Pozwala to na śledzenie kosztów i rozliczania fakturowania.

## <a name="approve-an-entry"></a>Zatwierdzanie wpisu
Strona **Zatwierdzenia** umożliwia przełączanie się między różnymi widokami, dzięki czemu można przeglądać różne typy zatwierdzeń.
  
1. Przejdź do strony **Zatwierdzanie** i wybierz opcję **Koszty**, **Czas**, **Użycie materiałów** lub **Wycofania**.
2. Przejrzyj każde zatwierdzenie i wybierz te, które chcesz zatwierdzić.
3. Wybierz przycisk **Zatwierdź**, aby zatwierdzić wybrane wpisy.
System przetwarza te wpisy i tworzy wartości rzeczywiste.

## <a name="reject-an-entry"></a>Odrzucanie wpisu
Jako osoba zatwierdzająca, być może będziesz musiał przesłać wpis z powrotem do użytkownika w celu dokonania poprawek.
  
1. Przejdź do strony **Zatwierdzenia** i wybierz wpis, który chcesz odrzucić. 
2. Wybierz pozycję **Odrzuć**.
3. Opcjonalnie dodaj komentarz w oknie dialogowym **Komentarze odrzucenia**, aby poinformować użytkownika, dlaczego wpis jest odrzucany.
4. Wybierz pozycję **OK**. Wpis zostanie zwrócony użytkownikowi.
  
## <a name="cancel-approval"></a>Anuluj zatwierdzenie
W niektórych przypadkach może być konieczne anulowanie uprzednio zatwierdzonego wpisu. Anulowanie uprzednio zatwierdzonego wpisu będzie miało wpływ na finanse. 

## <a name="approving-recall-requests"></a>Zatwierdzanie próśb o wycofanie
W niektórych przypadkach konsultant może potrzebować przypomnieć wcześniej zatwierdzony wpis. Anulowanie uprzednio zatwierdzonego wpisu będzie miało wpływ na finanse. Osoba zatwierdzająca projekt musi zatwierdzić wycofanie w celu cofnięcia transakcji w danych rzeczywistych.

## <a name="specify-project-approvers"></a>Określenie osób zatwierdzających projekt
Każdy projekt ma wielu członków zespołu projektu. Użytkownik może określić, którzy członkowie zespołu mogą zatwierdzać projekty.

1. Przejdź na stronę **Projekty** i otwórz projekt z listy.
2. Na karcie **Zespół** wybierz członka zespołu, który będzie osobą zatwierdzającą w projekcie, a następnie wybierz pozycję **Edytuj**.
3. Ustaw pole **Osoba zatwierdzająca w projekcie** na **Tak**.
4. Wybierz pozycję **Zapisz**.
5. Powtórz kroki od 2 do 4, aby dodać kolejne osoby.

## <a name="configure-the-users-manager"></a>Konfigurowanie menedżera użytkownika

1. Przejdź do **Ustawienia** > **Zabezpieczenia** > **Użytkownicy**.
2. Wybierz użytkownika, któremu chcesz przypisać menedżera i w obszarze **Informacje o organizacji** wybierz menedżera z listy. 
3. Wybierz pozycję **Zapisz**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
