---
title: Przejścia stanu podumowy
description: W tym artykule wyjaśniono przejścia stanu dla podumowy w aplikacji Microsoft Dynamics 365 Project Operations podczas tworzenia, wykonywania oraz zamykania podumowy.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b41e3d44a17c51778dd850c7d4a48351a5d44554
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919751"
---
# <a name="state-transitions-on-a-subcontract"></a>Przejścia stanu podumowy 

[!include [banner](../../includes/dataverse-preview.md)]

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

W tym artykule wyjaśniono przejścia stanu podumowy w aplikacji Microsoft Dynamics 365 Project Operations. Każdy stan jest reprezentowany jako wersja robocza, podumowa potwierdzona, zamknięta lub anulowana. Poniższy obraz przedstawia przejścia stanu.

![Model stanu podumowy](../media/SubconStates.png)  

W poniższej tabeli przedstawiono opis poszczególnych stanów w cyklu życia podumowy w aplikacji Project Operations.

| State | Description | Dozwolone przejścia |
| --- | --- | --- |
| Wersja robocza | Reprezentuje stan początkowy podumowy. Trwają negocjacje z dostawcą. Wiersze i ceny podlegają modyfikacji. Podumowa w tym stanie może być używana do szacowania i obsadzania wymagań dotyczących projektu dla zasobów i materiałów. Można również odwoływać się do niej w zakresie czasu, wydatków i użycia materiałów związanych z projektem. Podumowę w tym stanie można edytować i usuwać. | Potwierdzone |
| Potwierdzone | Reprezentuje etap podumowy po zakończeniu negocjacji z dostawcą w sprawie kalkulacji cen i kupowanych pozycji. Jednak rzeczywista dostawa materiałów i/lub praca podwykonawców nadal trwa. Podumowa w tym stanie może być używana do szacowania i obsadzania wymagań dotyczących projektu dla zasobów i materiałów. Można również odwoływać się do niej w zakresie czasu, wydatków i użycia materiałów związanych z projektem. Podumowy w tym stanie nie można edytować ani usuwać. Przycisk **Anuluj** umożliwia anulowanie potwierdzonej podumowy. Przycisk **Otwórz ponownie** umożliwia ponowne otwarcie podumowy w celu powrotu do stanu **Wersja robocza**. Użyj przycisku **Zamknij**, aby zamknąć potwierdzoną podumowę. | Zamknięcie <br> Anulowane <br> Wersja robocza |
| Zamknięcie | Ten stan reprezentuje etap podumowy, na którym zakończy się rzeczywista dostawa materiałów lub praca zasobów podwykonawców. Podumowa w tym stanie nie może być już używana do szacowania i obsadzania wymagań dotyczących projektu dla zasobów i materiałów. Nie można już również odwoływać się do niej w zakresie czasu, wydatków i użycia materiałów związanych z projektem. Podumowy w tym stanie nie można edytować ani usuwać. | None |
| Anulowane | Ten stan reprezentuje etap podumowy, na którym rzeczywista dostawa materiałów lub praca zasobów podwykonawców nie jest już potrzebna. Podumowy w tym stanie nie można używać do szacowania i obsadzania wymagań związanych z projektem dla zasobów i materiałów ani też nie można się do niej odwoływać się w zakresie czasu, wydatków i użycia materiałów w projekcie. Podumowy w tym stanie nie można edytować ani usuwać. | None |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
