---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie aktualizacji 26, wer. 3
ms.openlocfilehash: 849e7288ee91d3e9360c0b03f6b8b37ff29338e7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643276"
---
<a name="project-service-automation-update-release-26-v3"></a>Project Service Automation, wydanie aktualizacji 26, wer. 3
================================================

Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365. To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. To wydanie jest zgodne z systemem Dynamics 365 9.x. Aby zaktualizować do tej wersji, odwiedź centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wydanie aktualizacji 26, wer. 3. Ta wersja ma numer kompilacji V3.10.44.59 i jest ogólnie dostępna za pośrednictwem samodzielnej aktualizacji w grudniu 2020 r.

<a name="update-release-26"></a>Wydanie 26
-----------------

### <a name="bug-fixes"></a>Poprawki błędów

**Czas i wydatek**

Rozwiązano następujące problemy:

-   Użytkownicy mogą zmienić zadanie we wpisie czasu, który został zatwierdzony/przesłany.

-   Błąd „Nie ustawiono odwołania do obiektu” podczas zapisywania wpisu czasu.

-   Importowanie wpisów czasu z przydziałów zasobów powoduje utworzenie wpisów czasu o nieprawidłowych wartościach DateTime.

-   Po zainstalowaniu programu Project Service Automation i aplikacji Field Service przycisk **Nowy** jest wyświetlany dwa razy na pasku poleceń dla wpisów czasu w aplikacji Field Service.

-   Aktualizacje komórek typu **Zezwalanie na aktualizacje** i **Grupa jednostek** działają teraz w ramach siatki **Szacunki wydatków**.

-   Formularz **Aktualizowanie wpisu czasu — edytowanie** zawiera obszar **Oś czasu**.

-   Zatwierdzanie czasu dla nieprojektowych wpisów czasu powoduje blokowanie systemu w przypadku wyszukiwania roli osoby zatwierdzającej w projekcie.

**Zarządzanie zasobami**

Rozwiązano następujące problemy:

-   Dodano walidację w dodatku plug-in **PostProjectCreate** w celu wyszukania podstawowego wymagania przed jego utworzeniem.

-   Formularz szybkiego tworzenia **Członek zespołu projektu** zgłasza wyjątek odwołania o wartości null w przypadku usuwania pól z formularza.

-   Generowanie zapotrzebowań na 12 godzin w ciągu 1 roku będzie kończyć się niepowodzeniem.

-   Ulepszono wyjątek odwołania o wartości null dla komunikatu o błędzie podczas tworzenia zapotrzebowania dotyczącego zasobu.

**Zarządzanie projektem**

Rozwiązano następujące problemy:

-   Ulepszono walidację, aby rozwiązać problem dotyczący wyjątku odwołania o wartości null generowanego w dodatku plug-in **PreProjectUpdate**.

-   Projekty publikowane przez dodatek plug-in Microsoft Project dla komputerów stacjonarnych usuwają nieprzypisane przypisania.

-   Dodano nową walidację w przypadku, gdy odwołanie do projektu zadania jest nieprawidłowe z powodu wyjątku odwołania o wartości null w dodatku plug-in **PreValidateProjectTaskUpdate**.

-   W siatce członków zespołu nie są pokazywane żadne unikatowe przypisania dla rekordu członka zespołu.

-   Dodano nowe komunikaty walidacji i komunikaty o błędach wynikające z wyjątku odwołania o wartości null w dodatku plug-in **PreProjectTaskDelete**.

**Sales**

Rozwiązano następujące problemy:

-   W przypadku wybierania wiersza opartego na projekcie w ofercie lub kontrakcie przycisk **Sugestia** powinien być widoczny tylko podczas wybierania wiersza opartego na produkcie skojarzonego z istniejącym produktem.

-   Oddzielono uprawnienie **Create_Product** od uprawnienia **Create_ProjectContract**.

-   Usunięcie wiersza faktury powoduje niepowodzenie odwołania do wartości null w elemencie **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.
