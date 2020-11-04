---
title: Omówienie zatwierdzeń
description: Ta temat zawiera informacje na temat pracy z zatwierdzeniami w Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081872"
---
# <a name="approvals-overview"></a>Omówienie zatwierdzeń

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Przepływy pracy i czasu są przenoszone do etapu zatwierdzania. Po zatwierdzeniu wpisów transakcje są rejestrowane w wartościach rzeczywistych lub czasu zaksięgowanych w harmonogramie.

## <a name="approvals-workflow"></a>Przepływ pracy zatwierdzenia
Podczas tworzenia i przesyłania wpisu godziny lub wydatku zostaje utworzony wpis zatwierdzania. Osoba zatwierdzająca lub menedżer projektu przegląda i zatwierdza Twój wpis. Jeśli wpis jest powiązany z projektem, to po jego zatwierdzeniu zostaną utworzone wartości rzeczywiste. Pozwala to na śledzenie kosztów i rozliczania fakturowania. 

## <a name="approve-an-entry"></a>Zatwierdzanie wpisu
Formularz **Zatwierdzania** umożliwia przełączanie między różnymi widokami, dzięki czemu można wyświetlać różne typy zatwierdzeń.
  
1. Przejdź do formularza **Zatwierdzenia** i wybierz **Koszty** , **Czas** lub **Odwołania**.
2. Przejrzyj każde zatwierdzenie i wybierz te, które chcesz zatwierdzić.
3. Wybierz przycisk **Zatwierdź** , aby zatwierdzić wybrane wpisy.
System będzie przetwarzać te wpisy i tworzyć wartości rzeczywiste lub rezerwację.

## <a name="reject-an-entry"></a>Odrzucanie wpisu
Jako osoba zatwierdzająca, być może będziesz musiał przesłać wpis z powrotem do użytkownika w celu dokonania poprawek.
  
1. Przejdź do formularza **Zatwierdzanie** i wybierz wpis do odrzucenia. 
2. Wybierz pozycję **Odrzuć**.
3. Opcjonalne — dodaj komentarz w oknie dialogowym **Powód odrzucenia** , aby użytkownik wiedział, dlaczego dane wpis został odrzucony.
4. Wybierz pozycję **OK**. Wpis zostanie zwrócony użytkownikowi.
  
## <a name="recall-entries"></a>Odwołanie wpisów
W pewnym momencie może zaistnieć konieczność odwołania złożonego wpisu. Jeśli wpis nie został zatwierdzony, będzie on natychmiast zwrócony. Zatwierdzony wpis może jednak mieć istotny wpływ materialny. Aby zatwierdzić odwołanie w celu wystornowania transakcji w wartościach rzeczywistych, osoba zatwierdzająca projekt jest zobowiązana do zaakceptowania odwołania.

## <a name="specify-project-approvers"></a>Określenie osób zatwierdzających projekt
Każdy projekt ma wielu członków zespołu projektu. Użytkownik może określić, którzy członkowie zespołu mogą zatwierdzać projekty.

1. W tym celu należy przejść do formularza **Projekty** i otworzyć projekt z listy.
2. Na karcie **Zespół** wybierz członka zespołu, który będzie osobą zatwierdzającą w projekcie, a następnie wybierz pozycję **Edytuj**.
3. Ustaw pole **Osoba zatwierdzająca w projekcie** na **Tak**.
4. Wybierz pozycję **Zapisz**.
5. Powtórz kroki od 2 do 4, aby dodać kolejne osoby.

## <a name="configure-the-users-manager"></a>Konfigurowanie menedżera użytkownika

1. Przejdź do **Ustawienia** > **Zabezpieczenia** > **Użytkownicy**.
2. Wybierz użytkownika, któremu chcesz przypisać menedżera i w obszarze **Informacje o organizacji** wybierz menedżera z listy. 
3. Wybierz pozycję **Zapisz**.


