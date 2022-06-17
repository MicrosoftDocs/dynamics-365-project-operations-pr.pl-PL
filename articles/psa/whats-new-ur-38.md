---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 38, V3
description: W tym artykule przedstawiono funkcje i poprawki, które są dostępne w programie Microsoft Dynamics 365 Project Service Automation, aktualizacja 38, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 12/06/2021
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
ms.openlocfilehash: ccc08cd0bc365bd4761424a4c0ceac91985e7c89
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915198"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Nowości i zmiany w aplikacji Project Service Automation, wydanie 38, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Z zadowoleniem informujemy, że jest to najnowsza aktualizacja aplikacji Microsoft Dynamics 365 Project Service Automation. To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. Jest ona kompatybilna z Dynamics 365 9.x. Aby dokonać aktualizacji do tego wydania, należy odwiedzić stronę Centrum administracyjnego dla rozwiązań Dynamics 365 online i zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).

W tym artykule przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wydanie aktualizacji 38, V3. Ta wersja ma numer kompilacji V3.10.59.117 i jest ogólnie dostępna za pośrednictwem samodzielnej aktualizacji w grudniu 2021 r.

## <a name="update-release-38"></a>Wydanie 38

### <a name="bug-fixes"></a>Poprawki błędów

Rozwiązano następujące problemy.

**Czas i wydatek**

- Wyjątek występuje, gdy długość dzienników zestawu zatwierdzeń przekracza 100 000 rekordów.
- Użytkownicy nie mogą uzyskać dostępu do statki **Wpis czasu** ze strony głównej **Wpis czasu**.
- W sesji dialogowym **Importowanie wpisów czasu** nie jest wyświetlany żaden tekst, jeśli nie ma elementów kwalifikujących się do importowania.
- Użytkownicy mogą tworzyć zestawy zatwierdzeń, dla których pole **Stan docelowy** ma wartość **Nieznany**.

**Zarządzanie projektem**

- Wykresy nie są wyświetlane poprawnie w przypisaniach zasobów dla UTC (+09:30) i UTC (+10:00) po rozpoczęciu czasu letniego.
- W przypadku niektórych ustawień regionalnych pole **Dodatkowa kolumna** jest ukryta dla struktur podziału pracy.
- Selektor daty dla kontrolki kalendarza w siatce **Zadanie projektu** nie jest poprawnie zlokalizowany na język chiński.

**Sprzedaż**

- Wartości **Wydajność kontraktu** i **Koszt rzeczywisty projektu** nie pasują, gdy zasoby z możliwością zarezerwowania, które mają różne jednostki kontraktujące i waluty, przesyłają wpisy czasu.
- Niestandardowy przepływ pracy do automatycznego potwierdzania faktur kończy się niepowodzeniem, gdy faktury są importowane jako rozwiązanie zarządzane. Wyświetlany jest następujący komunikat: „Komunikat Microsoft.Xrm.Sdk.InvalidPluginExecutionException: nieprawidłowy stan faktury”.
- Jeśli jako opcja podsumowania zostanie wybrana opcja **Element główny**, a w projekcie zostaną przedstawione szacowania dotyczące kombinacji klas transakcji (na przykład kombinacja szacowań czasu, wydatków i materiałów), system podsumowuje w różnych klasach transakcji w postaci pojedynczego wiersza opłat.
- W scenariuszach, w których wiersz wydatku jest dodawany przed skojarzeniem pozycji kontraktu z projektem, poprawne ceny nie są wprowadzane jako wartość domyślna w polu **Aktualizuj cenę**.
- Ujemne kwoty sprzedaży nie są dozwolone w encjach **Projekt** i **Zadanie**.
