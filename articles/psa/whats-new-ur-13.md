---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 13, wer. 3
description: W tym temacie przedstawiono informacje na temat nowości w aktualizacji usługi Project Service Automation, wydanie 13, wer. 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: a4ebc2e6ca3f6be0a05a7240d762d7a8cf92d81b
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949467"
---
# <a name="project-service-automation-update-release-13-v3"></a>Project Service Automation, wydanie 13, wer. 3

[!include [banner](../includes/psa-now-project-operations.md)]

Mamy przyjemność przedstawić najnowszą aktualizację dotyczącą aplikacji Dynamics 365 Project Service Automation (PSA). To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. To wydanie jest zgodne z systemem Dynamics 365 9.x. Aby zaktualizować do tej wersji, odwiedź Centrum administracyjne programu Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).

W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wer. 3, aktualizacja 13. Numer tej kompilacji to V3.10.3.18 i jest on dostępny w następującym harmonogramie:

- **Powszechne udostępnienie (samoaktualizacja):** listopad 2019
- **Automatyczna aktualizacja:** grudzień 2019


## <a name="update-release-13"></a>Wydanie 13 

### <a name="bug-fixes"></a>Poprawki błędów

- Czas i wydatek

     - Naprawione: funkcja wyszukiwania na stronie **zatwierdzania wydatków** nie działa podczas wyszukiwania według przeznaczenia wydatku.

- Zarządzanie zasobami

     - Naprawione: liczby w uzgodnieniu zostały zaktualizowane w celu wyjustowania do prawej.
     - Naprawione: na karcie **harmonogram** nie można przypisywać nazwanych zasobów do zadań.

- Zarządzanie projektem

     - Naprawione: wyjątek odwołania zerowego podczas przypisywania członka zespołu w przypadku braku informacji konfiguracyjnych **TransactionType** dla **Jednostki** i **DefaultGroup**.

- Sales

     - Naprawione: duplikaty rekordów typów transakcji zwracają błąd podczas tworzenia rekordów cen ról.
     - Naprawione: dodatkowe przyciski dla **Nowa szansa sprzedaży**, **Oferta**, **Wiersz zamówienia** i **Dodaj produkt** są widoczne dla poleceń dotyczących szans sprzedaży, ofert, produktów zamówionych i podsiatki wierszy opartych na projekcie.




[!INCLUDE[footer-include](../includes/footer-banner.md)]