---
title: Nowości i zmiany w programie Project Service Automation, wydanie 12, wer. 3
description: W tym temacie przedstawiono informacje na temat nowości w aktualizacji usługi Project Service Automation, wydanie 12, wer. 3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: af8dbfe3-7ce9-4374-9c03-17b2e1d6ac32
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 758717562c12a72848f1a874fa8b1171139ebb0c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754326"
---
# <a name="project-service-automation-v3-update-release-12"></a>Project Service Automation, wer. 3, wydanie 12
Mamy przyjemność przedstawić najnowszą aktualizację dotyczącą aplikacji Dynamics 365 Project Service Automation (PSA). To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. To wydanie jest zgodne z systemem Dynamics 365 9.x. Aby zaktualizować do tej wersji, odwiedź Centrum administracyjne programu Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wer. 3, aktualizacja 14. Numer tej kompilacji to V3.10.2.34 i jest on zazwyczaj dostępny za pośrednictwem samoaktualizacji w październiku 2019.

## <a name="update-release-12"></a>Wydanie 12

### <a name="bug-fixes"></a>Poprawki błędów

- Czas i wydatek

    - Naprawione: błąd zapisu godziny został zaktualizowany w celu uzyskania odpowiedniego kontekstu.
    - Naprawione: Siatka wprowadzania godziny i harmonogram poprawnie wyświetlają pasek przewijania w pionie, gdy to konieczne.
    - Naprawione: przesłane wpisy wydatków i czasu mogą być zatwierdzone.
    - Naprawione: okno dialogowe anulowania zatwierdzania zostało poprawione w celu odzwierciedlenia stanu zatwierdzenia po zmianie z **zatwierdzonego** na **przesłane**.
    - Naprawione: pola **Cena**, **Jednostka** i **ilość** są teraz zablokowane w rekordzie wydatków po jego zatwierdzeniu.

- Zarządzanie projektem

    - Naprawione: Czynność **Nowe** w głównym formularzu **członka zespołu** została usunięta.
    - Naprawione: przydziały zasobów zostały zaktualizowane w celu brania pod uwagę niedokładnych błędów zaokrąglania, które prowadzą do zmiany daty zakończenia zadania.
    - Naprawione: w siatce zadań powiązane błędy po stronie serwera zostaną ukazane użytkownikowi.
    - Naprawione: Nazwa członka zespołu jest teraz renderowana w selektorze osób zadania zamiast nazwy pozycji.

- Zarządzanie zasobami

    - Naprawione: szczegóły wymagania dotyczące zasobów dla projektów utworzonych na podstawie szablonu są realizowane za pomocą kalendarza projektu.
    - Naprawione: umiejętności i kompetencje są obecnie domyślne na podstawie danych głównych ról w zapotrzebowaniu na zasoby utworzonemu dla tej roli.

- Sales

    - Naprawione: w formularzu **głównym kontraktu** znaleziono zduplikowane identyfikatory obiektów.
    - Naprawione: logika została zaktualizowana tak, by karta **Analiza oferty** była wyświetlana w celu ukazania konfiguracji metadanych karty.
    - Naprawione: Data księgowania w aktualnym rekordzie zaczyna się od daty wprowadzenia godzin/wydatku, a nie daty zatwierdzenia.
