---
title: Zarządzanie podumowami w rozwiązaniu Project Operations
description: W tym artykule przedstawiono omówienie całego procesu zarządzania podwykonawcami, zwykle w organizacjach opartych na projektach.
author: rumant
ms.date: 09/14/2022
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b2e4518f77b2099f9818ea56623be9efb20b01f4
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522339"
---
# <a name="subcontract-management-in-project-operations"></a>Zarządzanie podumowami w rozwiązaniu Project Operations


_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

W tym artykule przedstawiono omówienie całego procesu zarządzania podwykonawcami w organizacjach opartych na projektach. Podwykonawcy usług zwykle działają zgodnie z przepływem procesów biznesowych, który przedstawiono na poniższym diagramie.

![Przepływ procesu podrzędnego](../media/SubcontractingProcessFlow.png)

Poniższa lista zawiera szczegółowy opis procesu podwykonawstwa.

1. Kierownik projektu tworzy umowę podwykonawczą z dostawcą. Domyślnie dla umowy podwykonawczej używane są cenniki dołączone do rekordu dostawcy. Konto dostawcy ma typ relacji **Dostawca** lub **Dostawca (producent)**.
2. Kierownik projektu może wyszczególnić wszystkie zakupy jako pozycje w umowie podwykonawczej. Wiersze podwykonawstwa mogą dotyczyć czasu, wydatków lub produktów. Klasa transakcji w pozycji podumowy określa, do czego służy wiersz.
3. Menedżer klienta dostawcy i kierownik projektu mogą iterować po umowie podwykonawczej. Ceny można dostosować w cennikach zakupu dołączonych do umowy podwykonawczej.
4. Na tym lub późniejszym etapie procesu, jeśli pozycja podumowy dotyczy czasu, kierownik ds. klienta dostawcy kojarzy kontakty dostawcy z każdą pozycją podumowy. To stowarzyszenie dostarcza informacji kierownikowi projektu, który pracuje nad umową podwykonawczą. Gdy kontakt dostawcy jest skojarzony z pozycją podumowy, system automatycznie tworzy zasób, który można zarezerwować, na podstawie kontaktu, jeśli zasób, który można zarezerwować, jeszcze nie istnieje.
5. Metodą rozliczania dla każdego wiersza podwykonawcy może być **Cena stała** lub **Godziny i Materiały**. W przypadku pozycji podumowy o stałej cenie jest konfigurowany harmonogram faktur oparty na kamieniach milowych.
6.  Po skonfigurowaniu podumowy i zakończeniu negocjacji następuje potwierdzenie. Nie można edytować potwierdzonych podumów, ale jeśli wystąpią zmiany, można ponownie otworzyć podumowę do edycji, co powoduje zmianę stanu z **Potwierdzono** z powrotem na **Wersja robocza** i można ponownie otworzyć negocjacje. 
7.  Podczas tworzenia ogólnego członka zespołu w projekcie można powiązać go z pozycją podumowy. Wskazuje to na konieczność posiadania personelu ogólnego, który może pracować w charakterze podwykonawcy.
8.  Nazwani członkowie zespołu mogą być tworzeni bezpośrednio w projekcie lub przez rezerwację przy użyciu funkcji planowania zasobów. Jeśli nazwany członek zespołu projektu jest pracownikiem kontraktowym, można go skojarzyć z pozycją podumowy. Spowoduje to skorzystanie z dostępnej wydajności w pozycji podumowy.
9.  Zasoby podwykonawców mogą rejestrować czas, koszty i użycie materiałów w projektach i zadaniach projektów, a następnie przesyłać je do zatwierdzenia. Odbywa się to podobnie w przypadku pracowników. Podczas rejestrowania czasu pracownik kontraktowy może wybrać określoną podumowę i pozycję podumowy.
10. Po zatwierdzeniu czas zatwierdzony przez podwykonawców będzie służyć do rejestrowania wartości rzeczywistych kosztów projektu na podstawie ceny zakupu powiązanej z pracownikiem kontraktowym lub roli, którą pełnił on w projekcie.
11. Faktury dostawcy i pozycje faktur dostawcy mogą być rejestrowane w systemie dla pracy wykonywanej przez zasoby dostawcy lub produktów dostarczonych przez dostawcę. Pozycje faktury dostawcy muszą być specyficzne dla projektu i następującej klasy transakcji: czas, wydatek, produkt/materiał, punkt kontrolny lub opłata. Opcjonalnie pozycje faktury dostawcy mogą odwoływać się do pozycji podumowy.
12. System automatycznie skojarzy wszystkie wartości rzeczywiste kosztów, które odpowiadają pozycji podumowy i projektowi, z fakturą dostawcy. Pomoże to przeprowadzić 3-kierunkowy proces dopasowywania i weryfikacji.
13. Menedżer projektu może następnie przejrzeć automatycznie dopasowane wartości rzeczywiste projektu, usunąć lub dodać inne wartości rzeczywiste kosztów projektu, a także zakończyć proces weryfikacji.
14. Zakończenie procesu weryfikacji we wszystkich wierszach spowoduje oznaczenie faktury dostawcy jako **gotowej do płatności**. Na tym etapie fakturę i pozycje dostawcy można przenieść do systemu księgowego lub zobowiązań, aby przetworzyć płatność dla dostawcy. Wcześniej zarejestrowane koszty projektu zostaną wycofane, a koszty rzeczywiste z pozycji faktury dostawcy zostaną zarejestrowane w projekcie.

## <a name="quantity-based-subcontract-lines-and-work-based-subcontract-lines"></a>Pozycje podumowy oparte na ilości i pozycje podumowy oparte na pracy

Pozycja podumowy może opierać się na ilości lub na pracy. 

Gdy pozycja podumowy jest **oparta na ilości**, ilość zakupiona w pozycji podumowy dla czasu, wydatku lub materiałów może być wykorzystana w dowolnym projekcie.

Jeśli pozycja podumowy jest **oparta na pracy**, jest ona mapowana na treść pracy reprezentowaną przez węzeł w planie projektu. Wartość pozycji podumowy jest sumą wszystkich składników wymaganych do dostarczenia wymaganej pracy. Są one modelowane jako szczegóły pozycji podumowy i mogą być kolekcją czasu, wydatków lub materiałów. W przypadku pozycji podumowy opartej na pracy pozycja podumowy jest także dedykowana dla pojedynczego projektu. Te typy kontraktów nie są obsługiwane przez Project Operations.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

