---
title: Zarządzanie zasobami — często zadawane pytania
description: Ten artykuł zawiera odpowiedzi na często zadawane pytania dotyczące zarządzania zasobami.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 6610098737b79d76b38c3d467135b9118c2a8ec7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913357"
---
# <a name="resource-management-faq"></a>Zarządzanie zasobami — często zadawane pytania

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a>Jaka jest różnica między członkiem zespołu a wymaganiem zasobu?

Członka zespołu projektu można przypisywać do zadań, rezerwować lub rezerwować nadmiarowo oraz ustawiać jako osobę zatwierdzającą. Wymaganie zasobu może istnieć bez członka zespołu projektu, jako wersja robocza uwagi o wymaganiu. 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a>Jaka jest różnica między godzinami proponowanymi a godzinami zarezerwowanymi wstępnie?

Godziny proponowane i godziny zarezerwowane wstępnie różnią się widocznością. Godziny proponowane są widoczne tylko dla menedżerów zasobów i menedżera projektu, który zainicjował wymaganie za pomocą żądania zasobu. Godziny zarezerwowane wstępnie są widoczne dla każdego, kto ma dostęp do tablicy harmonogramu.

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a>Jak wyświetlić wstępnie zarezerwowane godziny dla zasobów w zespole?

Wstępnej rezerwacji można dokonać podczas rezerwowania wymagania zasobu. Zasoby, które wstępnie zarezerwowano w zespole projektu, są wyświetlane jako członkowie zespołu mający wstępnie zarezerwowane godziny. Są one również widoczne na tablicy harmonogramu.

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a>Jak zmienić wymagane godziny oraz daty rozpoczęcia i zakończenia dla zasobu (ogólnego lub nazwanego) zarezerwowanego przeze mnie?

Po zarezerwowaniu zasobów wybierz opcję **Obsługa rezerwacji**, aby wprowadzić wszelkie wymagane zmiany.

## <a name="what-resources-types-does-project-service-automation-support"></a>Jakie typy zasobów obsługuje program Project Service Automation?

**Użytkownik** i **Kontakt** są jedynymi typami zasobów obsługiwanymi w programie Dynamics 365 Project Service Automation. Mimo iż można tworzyć inne typy zasobów (np. **Sprzęt** i **Grupa**), nie są dla nich obsługiwane żadne kompleksowe przypadki użycia.

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a>Jaka jest różnica między przypisaniem a rezerwacją?

Przypisania to przydziały zasobów do zadań projektu w harmonogramie projektu. Zasoby mogą być rzeczywiste lub ogólne. Rezerwacje to ostateczne lub wstępne przydzielenie zasobów do projektu. Rezerwacje ostateczne zużywają dyspozycyjność zasobu. W przypadku zasobów rzeczywistych najlepiej, aby rezerwacje i przypisania były zgodne, ponieważ technicznie nie różnią się od siebie. Jednak program PSA nie wymusza takiej zgodności. Widok Uzgadnianie pokazuje menedżerowi projektu miejsca, w których rezerwacje i przypisania zasobów są niezgodne.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
