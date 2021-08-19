---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 18, wer. 3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostępne w programie Project Service Automation, aktualizacja 18, wer. 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: 43491a3820d84e9d2a43e678f2604e234e18794d9e28889429debc0b991bbfac
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "7004369"
---
# <a name="project-service-automation-update-release-18-v3"></a>Project Service Automation, wydanie 18, wer. 3

[!include [banner](../includes/psa-now-project-operations.md)]

Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365. To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. To wydanie jest zgodne z systemem Dynamics 365 9.x. Aby zaktualizować do tej wersji, odwiedź Centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).

W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wer. 3, aktualizacja 18. Ta wersja ma numer kompilacji V3.10.8.12 i zazwyczaj jest dostępna za pośrednictwem samoaktualizacji w kwietniu 2020 r.

## <a name="update-release-18"></a>Wydanie 18

### <a name="bug-fixes"></a>Poprawki błędów

**Czas i wydatek**

- Naprawione: Przepływy **Odwołaj**, **Żądaj** i **Anuluj zatwierdzenie** powodują wyjątki z niejasnymi komunikatami o błędach.
- Naprawione: Kiedy **Anuluj zatwierdzenie** nie powiedzie się dla wydatku, nie jest wywoływany stosowny błąd wyjątku.
- Naprawione: Siatka wpisu czasu nieprawidłowo obsługuje dni wolne od pracy w Australii po zmianie z czasu letniego (DST) w październiku.
- Naprawione: Nieprawidłowa domyślna logika uniemożliwia przesłanie kosztów.
- Naprawione: Kiedy zatwierdzanie zapisu czasu kończyło się niepowodzeniem, zatwierdzenie pozostało w stanie **Oczekującym**.
- Naprawione: Błędy SQL w zatwierdzeniach zbiorczych (zakleszczenie/przekroczenie limitu czasu).
- Naprawione: Znaczne problemy z wydajnością, które wynikają z aktualizowania członków zespołu podczas zatwierdzania wpisów czasu.

**Zarządzanie projektem**

- Stałe: Powiadomienie strefy czasowej przeniesione z widoku **Uzgadnianie** do głównego formularza **Projektu**.
- Naprawione: Szablon kalendarza nie jest poprawnie ustawiony jako domyślny po otwarciu nowego formularza projektu.
- Naprawione: W przypadku przeglądarek opartych na chromium użytkownicy nie mogą łatwo wybrać zadań poprzedników do usunięcia.
- Naprawione: Tworzenie lub kopiowanie **Projektu z pustego szablonu** pobiera niepokrewne przypisania.
- Naprawione: W określonych skrajnych przypadkach tworzenie nowego przypisania z siatki zadań powoduje utworzenie zduplikowanych rekordów.
- Naprawione: W trybie ręcznym użytkownicy nie mogą aktualizować dat rozpoczęcia zadania, tak aby były późniejsze niż bieżąca data zapisana.

**Zarządzanie zasobami**

- Stałe: Wiersz podsumy widoku **Uzgodnienie** nieprawidłowo oblicza wariancję księgowania po rozszerzeniu księgowania.
- Naprawione: Widok **uzgadniania** powoduje nieprawidłowe wyświetlenie przydziałów zasobów, gdy zasób obsługujący rezerwacje jest kalendarzem niezgodnym z kalendarzem projektu.

**Sales**

- Naprawione: Czas ponownego zatwierdzania wpisów (**Zatwierdzanie > Anulowanie >** Ponowne zatwierdzanie) powoduje utworzenie zduplikowanych wartości rzeczywistych, które nie są odliczane.


[!INCLUDE[footer-include](../includes/footer-banner.md)]