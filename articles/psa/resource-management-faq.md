---
title: Zarządzanie zasobami — często zadawane pytania
description: Ta temat zawiera odpowiedzi na często zadawane pytania dotyczące zarządzania zasobami.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 395aa57d73e5d4a0c9c827c79bf4e7ef229c3981
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082223"
---
# <a name="resource-management-faq"></a>Zarządzanie zasobami — często zadawane pytania

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a>Jaka jest różnica między członkiem zespołu a wymaganiem zasobu?

Członka zespołu projektu można przypisywać do zadań, rezerwować lub rezerwować nadmiarowo oraz ustawiać jako osobę zatwierdzającą. Wymaganie zasobu może istnieć bez członka zespołu projektu, jako wersja robocza uwagi o wymaganiu. 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a>Jaka jest różnica między godzinami proponowanymi a godzinami zarezerwowanymi wstępnie?

Godziny proponowane i godziny zarezerwowane wstępnie różnią się widocznością. Godziny proponowane są widoczne tylko dla menedżerów zasobów i menedżera projektu, który zainicjował wymaganie za pomocą żądania zasobu. Godziny zarezerwowane wstępnie są widoczne dla każdego, kto ma dostęp do tablicy harmonogramu.

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a>Jak wyświetlić wstępnie zarezerwowane godziny dla zasobów w zespole?

Wstępnej rezerwacji można dokonać podczas rezerwowania wymagania zasobu. Zasoby, które wstępnie zarezerwowano w zespole projektu, są wyświetlane jako członkowie zespołu mający wstępnie zarezerwowane godziny. Są one również widoczne na tablicy harmonogramu.

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a>Jak zmienić wymagane godziny oraz daty rozpoczęcia i zakończenia dla zasobu (ogólnego lub nazwanego) zarezerwowanego przeze mnie?

Po zarezerwowaniu zasobów wybierz opcję **Obsługa rezerwacji** , aby wprowadzić wszelkie wymagane zmiany.

## <a name="what-resources-types-does-project-service-automation-support"></a>Jakie typy zasobów obsługuje program Project Service Automation?

**Użytkownik** i **Kontakt** są jedynymi typami zasobów obsługiwanymi w programie Dynamics 365 Project Service Automation. Mimo iż można tworzyć inne typy zasobów (np. **Sprzęt** i **Grupa** ), nie są dla nich obsługiwane żadne kompleksowe przypadki użycia.

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a>Jaka jest różnica między przypisaniem a rezerwacją?

Przypisania to przydziały zasobów do zadań projektu w harmonogramie projektu. Zasoby mogą być rzeczywiste lub ogólne. Rezerwacje to ostateczne lub wstępne przydzielenie zasobów do projektu. Rezerwacje ostateczne zużywają dyspozycyjność zasobu. W przypadku zasobów rzeczywistych najlepiej, aby rezerwacje i przypisania były zgodne, ponieważ technicznie nie różnią się od siebie. Jednak program PSA nie wymusza takiej zgodności. Widok Uzgadnianie pokazuje menedżerowi projektu miejsca, w których rezerwacje i przypisania zasobów są niezgodne.
