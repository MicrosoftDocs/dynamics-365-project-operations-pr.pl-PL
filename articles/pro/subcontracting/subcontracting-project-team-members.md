---
title: Podwykonawstwo — członkowie zespołu projektu
description: W tym temacie wyjaśniono, jak uwzględniać członków zespołu projektu jako podwykonawców w aplikacji Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: b98fc356d7de77fa7f05667acaa5569a7053e4d1
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903494"
---
# <a name="subcontracting-project-team-members"></a>Podwykonawstwo — członkowie zespołu projektu

[!include [banner](../../includes/dataverse-preview.md)]

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

W aplikacji Microsoft Dynamics 365 Project Operations można wybrać opcję obsługi podwykonawstwa dla obsadzonych lub nieobsadzonych członków zespołu projektu.

- Nieobsadzeni członkowie zespołu projektu mają przypisany zasób ogólny.
- Obsadzeni członkowie zespołu projektu mają przypisany zasób nazwany.

Po połączeniu członka zespołu projektu z pozycją podumowy wszelkie przypisania do zadań, które przypisano do tego członka zespołu, zostaną ponownie wycenione przy użyciu cennika zakupu dołączonego do podumowy.  Na karcie **Szacowania** na stronie **Szczegóły projektu** wybierz przycisk **Aktualizuj ceny**, aby wyświetlić zaktualizowane ceny i/lub wycenę kosztów wynikających z podjęcia decyzji o zleceniu podwykonawcy. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Podwykonawstwo dla nieobsadzonego członka zespołu projektu
Na stronie **szczegółów członka zespołu** znajdują się pola podumowy i pozycji podumowy, które umożliwiają menedżerowi projektu wyrażanie potrzeby wykorzystywania wymaganej dyspozycyjności w ramach podumowy. Aby uwzględnić członka zespołu projektu jako podwykonawcę w postaci zasobu ogólnego, wykonaj następujące kroki:

1.  Wybierz podumowę na stronie **szczegółów członka zespołu**.

2.  Można wybrać tylko podumowy ze stanem **Wersja robocza** lub **Potwierdzona**. Nie można wybierać podumów **zamkniętych** ani **anulowanych**. 

3.  Pole **Pozycja podumowy** stanie się widoczne po wybraniu podumowy.

4.  W polu **Pozycja podumowy** można wybrać tylko pozycje podumowy powiązane z czasem. Nie można wybrać pozycji podumowy dla wydatków ani materiałów.

5.  Rola rekordu członka zespołu projektu musi być dopasowana do roli w pozycji podumowy. Dzięki temu czas dla roli szacowany w projekcie będzie dotyczyć tej samej roli, którą zakupiono w pozycji podumowy. 

Gdy ogólny członek zespołu jest skojarzony z podumową i pozycją podumowy, pole **Typ pracownika** w wierszu członka zespołu ogólnego zostanie zaktualizowane do wartości **Pracownik kontraktowy**, a wartość **Ważność podumowy** będzie ustawiona na **Ważna**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Podwykonawstwo dla obsadzonego członka zespołu projektu
Podobnie jak ogólni lub nieobsadzeni członkowie zespołu, dyspozycyjność obsadzonych członków zespołu wymaganych w projekcie może być również powiązana z podumową. Aby uwzględnić nazwanego członka zespołu projektu jako podwykonawcę, wykonaj następujące kroki:

1.  Upewnij się, że nazwany zasób jest skonfigurowany jako typ pracownika kontraktowego dla zasobu, który można zarezerwować. Należy się także upewnić, że pole **Dostawca** w zasobie, który można zarezerwować, odpowiada dostawcy w wybieranej podumowie. 

2.  Można wybrać tylko podumowy o stanie **Wersja robocza** lub **Potwierdzona**. Nie można wybierać podumów **zamkniętych** ani **anulowanych**. 

3.  Pole **Pozycja podumowy** stanie się widoczne po wybraniu podumowy.

4.  W polu **Pozycja podumowy** można wybrać tylko pozycje podumowy powiązane z czasem. Nie można wybrać pozycji podumowy dla wydatków ani materiałów.

5.  Rola rekordu członka zespołu projektu musi być dopasowana do roli w pozycji podumowy. Dzięki temu czas dla roli szacowany w projekcie będzie dotyczyć tej samej roli, którą zakupiono w pozycji podumowy. 

Nazwani członkowie zespołu projektu skonfigurowani jako typ pracownika kontraktowego **Zasób, który można zarezerwować** będą mieli stan **nieważny** dla podwykonawcy, jeśli nie zostaną powiązani z podumową. Gdy nazwany członek zespołu jest skojarzony z podumową i pozycją podumowy, pole **Typ pracownika** w wierszu członka zespołu zostanie zaktualizowane do wartości **Pracownik kontraktowy**, a wartość **Ważność podumowy** będzie ustawiona na **Ważna**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
