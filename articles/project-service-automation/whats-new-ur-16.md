---
title: Nowości i zmiany w Project Service Automation, wydanie aktualizacji 16, wer. 3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostepne w programie Project Service Automation, aktualizacja 16, wer. 3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: b890a7b6-1664-4812-8732-fed77653cc05
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 0f4c206fd5b7a36d940e966b28c2437525812a98
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754322"
---
# <a name="project-service-automation-v3-update-release-16"></a>Project Service Automation, wer. 3, aktualizacja wydania 16
Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365. To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności.

To wydanie jest zgodne z systemem Dynamics 365 9.x. Aby zaktualizować do tej wersji, odwiedź Centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie Preferowanego rozwiązania](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page). W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie PSA, wer. 3, aktualizacja 16. Numer tej kompilacji to V3.10.6.34 i jest on zazwyczaj dostępny za pośrednictwem samoaktualizacji w styczniu 2020 r.

## <a name="update-release-16"></a>Wydanie 16

### <a name="bug-fixes"></a>Poprawki błędów

-   Czas i wydatek

    -   Naprawione: Użytkownicy próbujący przesłać usunięte wpisy czasu i wydatków na potrzeby zatwierdzenia będą otrzymywać odpowiednie komunikaty o błędach.

-   Zarządzanie projektem

    -   Poprawione: Jednostki zasobów zdefiniowane dla członków zespołu w szablonach są przestrzegane wraz z szablonami stosowanymi w nowym projekcie.

    -   Naprawione: poprawiono sposób obsługi ponownego przypisywania własności rekordu.

    -   Naprawione: Projekty, które są w trakcie procesu kopiowania, nie będą dozwolone do skopiowania do momentu ukończenia wszystkich operacji kopiowania.

-   Zarządzanie zasobami

    -   Naprawione: Rozszerz rezerwacje teraz poprawnie obsługuje krótkie czasy trwania i nie tworzy już zero godzin dla przedłużonych rezerwacji.

    -   Naprawione: Widok uzgadniania jest teraz renderowany, gdy strefa czasowa projektu będzie wynosić +5:30 GMT, a tylko czas użytkownika jest inny.

-   Sales

    -   Naprawione: Po usunięciu projektu zamapowanego do pozycji kontraktu i zamapowaniu nowego projektu nie można ponownie oszacować rzeczywistych rekordów w nowym projekcie na podstawie reguł fakturowania i kalkulacji cen zdefiniowanych w pozycji kontraktu. Ta funkcja została naprawiona w tym wydaniu. Zmiana cen i rzeczywistych rekordów w nowym zamapowanym projekcie zostanie zmieniona i poprawnie odtworzona na podstawie reguł kalkulacji cen i fakturowania w pozycji kontraktu. Rzeczywista liczba rekordów zamapowanego projektu będzie również wyznaczona ponownie i w konsekwencji ponownie utworzona.

    -   Naprawione: Dodano dodatkowe sprawdzanie w polu **Kwota** wiersza oszacowania, aby mieć pewność, że wartości puste nie będą utrwalone.

    -   Naprawione: Po zaktualizowaniu wartości rzeczywistych w projekcie w głównym formularzu projektu dodano przycisk Odśwież, który umożliwia użytkownikom ponowne zsynchronizowanie wartości rzeczywistych.

    -   Naprawione: Kiedy użytkownicy uaktualnią wersję z od 2.X do 3.X, dozwolone będą projekty o wartości PUSTEJ dla nazwy projektu.

