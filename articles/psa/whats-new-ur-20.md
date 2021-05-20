---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 20, wer. 3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostępne w programie Project Service Automation, aktualizacja 20, wer. 3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: 124dad5438f9489d1ddbc952cecaee977b6b7f01
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949107"
---
# <a name="project-service-automation-update-release-20-v3"></a>Project Service Automation, wydanie 20, wer. 3

[!include [banner](../includes/psa-now-project-operations.md)]

Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365. To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. To wydanie jest zgodne z systemem Dynamics 365 9.x. Aby zaktualizować do tej wersji, odwiedź centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).

W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wer. 3, aktualizacja 20. Ta wersja ma numer kompilacji wer. 3.10.31.37 i zazwyczaj jest dostępna za pośrednictwem samoaktualizacji w czerwcu 2020 r.

## <a name="update-release-20"></a>Wydanie 20

### <a name="bug-fixes"></a>Poprawki błędów

**Zarządzanie projektem**

Rozwiązano następujące problemy:

- Importowanie członków zespołu projektu przy użyciu metody alokacji, która wymaga użycia godzin, powoduje wyczyszczenie niejasnych komunikatów o błędach, kiedy określona liczba godzin jest równa zero.
- Podczas wprowadzania przez użytkownika maksymalnej liczby znaków w polu **Opis** dla zadania w projekcie jest wyświetlany nieprawidłowy błąd.
- Strona **Pobierz dodatek Microsoft Dynamics 365 Project Service Automation** przekierowuje do strony pobierania w języku angielskim, gdy ustawienia języka użytkownika są ustawione na japoński.
- Kiedy wystąpi błąd serwera, etykieta synchronizacji na karcie **Harmonogram** w formularzu **Projekty** pozostaje niekiedy w programie.
- Gdy zadanie jest modyfikowane, nadmiarowe aktualizacje zadań są wysyłane na serwer.

**Sales**

Rozwiązano następujące problemy:

- W formularzu **Kontraktu** dwukrotne kliknięcie pozycji **Utwórz fakturę** tworzy dwie faktury dla pojedynczego rekordu wartości rzeczywistych.
- Użytkownicy przeglądarki Internet Explorer 11 nie mają możliwości utworzenia wpisów wydatków.
- Wycofanie kosztów i wycofanie z niezfakturowanych wartości rzeczywistych nie jest powiązane.
- Przycisk **Odśwież rzeczywiste** w formularzu **Projekt** nie powoduje odświeżenia **Godzin rzeczywistych zadania**.
- Dodatek **PreValidateProjectTeamMemberCreate** może tworzyć duplikaty ogólych zasobów możliwych do zarezerwowania, gdy atrybut **msdyn_isgenericresourceprojectscoped** jest ustawiony na **Fałsz**.
- **Ponowne obliczenie** czyści koszty zakupu dotyczące szczegółów wiersza oferty opartej na produkcie i szczegółów pozycji kontraktu.
- W określonych scenariuszach dodatek **PostEstimateLineUpdate** wyświetla wartość null i błąd wyjątków odwołania.
- Czas trwania fazy czasu na **Wykresie analizy wydajności** nie pasuje do czasu trwania kosztów w szczegółach wiersza oferty z ceną ustaloną dla oferty.
- Wartości jednostek i grupy jednostek nie są poprawnie domyślne dla kategorii wydatków w formularzach **Szczegółów pozycji kontraktu** i **Szczegółów wiersza oferty**.
- **Zestawienie kosztów własnych jednostki organizacyjnej** zezwalają na nakładanie się dnia wejścia w życie.
- Użytkownicy nie mogą zmieniać składnika **OrgUnit**, kiedy typ zamówienia nie jest związany z pracą, ponieważ jego wartość powoduje błąd wyjątku odwołania do wartości null.
- Podczas próby przejścia do nawigacji z poziomu formularza **Szczegóły wiersza oferty,** powrót do karty **Oferta** powoduje odświeżenie formularza i wyświetlenie karty **Podsumowanie**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]