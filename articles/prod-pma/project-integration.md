---
title: Integracja klienta programu Microsoft Project
description: Planowanie i utrzymywanie harmonogramu projektu może być skomplikowane, więc kierownicy projektów muszą używać narzędzi, które pomagają im zarządzać tym zadaniem. Integracja z Microsoft Project Client zapewnia wsparcie dla otwierania i zarządzania strukturą podziału pracy w projekcie.
author: Yowelle
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 032d726bb6206c563b573f30d13fe2697a13c949
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999459"
---
# <a name="microsoft-project-client-integration"></a>Integracja klienta programu Microsoft Project

[!include [banner](../includes/banner.md)]

Planowanie i utrzymywanie harmonogramu projektu może być skomplikowane, więc kierownicy projektów muszą używać narzędzi, które pomagają im zarządzać tym zadaniem. Integracja z Microsoft Project Client zapewnia wsparcie dla otwierania i zarządzania strukturą podziału pracy w projekcie. Kierownik projektu może opublikować wszystkie zmiany wprowadzone z powrotem w strukturze podziału prac projektu Dynamics 365 Finance.

> [!NOTE]
> W przypadku korzystania z aktualizacji z lipca (wersja 10.0.4) należy zainstalować program KB 4054797 i 4055884.

## <a name="configure-the-microsoft-project-client-add-in"></a>Konfigurowanie dodatku Microsoft Project Client
Aby umożliwić integrację z Microsoft Project Client, dodatek Microsoft Dynamics 365 musi być zainstalowany w aplikacji klienta Microsoft Project użytkownika. W tym celu należy otworzyć **Obszar roboczy zarządzanie projektami**.

•   Kliknij opcję **Konfigurowanie dodatku klienta projektu**, korzystając z sekcji **Łącza** > **Ustawienia** w obszarze roboczym.

•   Kliknij przycisk **Otwórz**, a następnie kliknij opcję **Uruchom** po wyświetleniu monitu.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Otwórz i edytuj istniejącą roboczą strukturę podziału pracy w programie Microsoft Project Client
Jeśli projekt w Dynamics 365 Finance ma już utworzoną strukturę podziału pracy, strukturę podziału pracy można otworzyć w aplikacji Microsoft Project Client, jeśli struktura podziału pracy ma status wersji roboczej. Aby otworzyć ze strony **Projektu**, kliknij łącze **Otwórz w programie Microsoft Project** na karcie **Plan**. Tę stronę można również otworzyć z poziomu aplikacji Microsoft Project Client, klikając **Otwórz** na karcie **Microsoft Dynamics 365**. Wybierz **Firma** i **Projekt** z listy.

> [!NOTE]
> Jeśli używasz przeglądarki Internet Explorer jako przeglądarki, musisz kliknąć przycisk **Zapisz**, aby ręcznie otworzyć plik z lokalizacji, do której został pobrany plik. Lub kliknij przycisk **Zapisz i Otwórz**, aby otworzyć plik w programie Microsoft Project Client. Nie zmieniaj nazwy pliku przy zapisywaniu.

Przed wprowadzeniem jakichkolwiek zmian w pliku przy użyciu Microsoft Project Client należy go zaewidencjonować. Kliknij pozycję **Wyewidencjonuj** na karcie **Microsoft Dynamics 365**. Uniemożliwi to innym użytkownikom edytowanie struktury podziału prac z poziomu finansów w tym samym czasie. Aby opublikować strukturę podziału pracy po zakończeniu edycji, kliknij pozycję **Zaewidencjonuj** na karcie **Microsoft Dynamics 365**.

Jeśli zespół projektowy został już dodany do projektu w programie Finance, lista zasobów zostanie wypełniona członkami zespołu. Jeśli zespół projektu nie został jeszcze dodany do projektu, można wybrać zasoby i zbudować zespół w programie Microsoft Project Client, klikając przycisk **Zasoby** na karcie **Microsoft Dynamics 365**. 

Następujące dane będą synchronizowane z powrotem do Finance w ramach procesu ewidencjonowania:

•   Nazwa zadania

•   Data rozpoczęcia

•   Data zakończenia

•   Elementy poprzedzające

•   Nazwy zasobu

•   Kategoria

•   Kategoria zasobów

•   Godziny pracy

•   Notatki

•   Priorytet

> [!NOTE]
> Dodanie innych kolumn do pliku klienta programu Microsoft Project spowoduje, że nie zostaną one zapisane w pliku i nie zostaną wyświetlone po ponownym otwarciu pliku.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Tworzenie struktury podziału pracy dla istniejącego projektu przy użyciu Microsoft Project Client
Aby utworzyć nową strukturę podziału pracy za pomocą Microsoft Project Client, wykonaj następujące kroki:


1.  Otwórz Microsoft Project Client.

2.  Na karcie **Microsoft Dynamics 365** kliknij opcję **Opcje**.

3.  Wybierz **Firma** dla projektu.

4.  Wybierz **Projekt**.

5.  Kliknij pozycję **Zapoznaj się** na karcie **Microsoft Dynamics 365**.

6.  Gdy jest gotowy do opublikowania w Finance, kliknij opcję **Zaewidencjonuj** na karcie **Microsoft Dynamics 365**.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Zastąp istniejącą strukturę podziału pracy dla istniejącego projektu przy użyciu programu Microsoft Project Client
Aby utworzyć nową strukturę podziału pracy przy użyciu programu Microsoft Project Client i zastąpić istniejącą strukturę podziału pracy dla istniejącego projektu, wykonaj następujące kroki:

1.  Otwórz Microsoft Project Client.

2.  Utwórz harmonogram w programie Microsoft Project Client.

3.  Na karcie **Microsoft Dynamics 365** kliknij przycisk **Zapisz zmiany** > **Zastąp istniejący projekt**.

4.  Wybierz **Firma** dla projektu.

5.  Wybierz **Projekt**.

6.  Kliknij przycisk **OK**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Tworzenie nowego projektu z poziomu Microsoft Project Client


1.  Otwórz Microsoft Project Client.

2.  Utwórz harmonogram w programie Microsoft Project Client.

3.  Na karcie **Microsoft Dynamics 365** kliknij przycisk **Zapisz zmiany** > **Zapisz do nowego projektu**.

4.  Wybierz **Firma** dla projektu.

5.  W razie potrzeby wprowadź **Identyfikator projektu**.

6.  Wprowadź **Nazwa projektu**.

7.  Wybierz **Typ projektu**, **Grupę projektów** oraz **Identyfikator kontraktu projektu**. Można również utworzyć nowy kontrakt dotyczący projektu, klikając opcję **Nowy**.

8.  Wybierz **Kalendarz**, który ma być używany do ponownego wyszukania.

11. Kliknij przycisk **OK**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]