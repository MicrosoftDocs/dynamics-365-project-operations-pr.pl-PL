---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 16, wer. 3
description: W tym artykule przedstawiono funkcje i poprawki dostępne w programie Project Service Automation, wydanie aktualizacji 16, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: e4429ace3d8206369b91917cf87f6968fbb12277
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926513"
---
# <a name="project-service-automation-update-release-16-v3"></a>Project Service Automation, wydanie 16, wer. 3

[!include [banner](../includes/psa-now-project-operations.md)]

Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365. To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności.  To wydanie jest zgodne z systemem Dynamics 365 9.x. Aby zaktualizować do tej wersji, odwiedź Centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie Preferowanego rozwiązania](/dynamics365/project-service/upgrade-psa-home-page).
W tym artykule przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie PSA V3, wydanie aktualizacji 16. Numer tej kompilacji to V3.10.6.34 i jest on zazwyczaj dostępny za pośrednictwem samoaktualizacji w styczniu 2020 r.


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



[!INCLUDE[footer-include](../includes/footer-banner.md)]
