---
title: Usunięte lub przestarzałe funkcje w aplikacji Dynamics 365 Project Operations
description: W tym temacie opisano funkcje, które zostały usunięte lub są przeznaczone do usunięcia z aplikacji Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 61bb84b94274762636eb8532f09634db1109e969
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601583"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Usunięte lub przestarzałe funkcje w aplikacji Dynamics 365 Project Operations

_**Ma zastosowanie do:** Project Operations dla scenariuszy opartych na zasobach / braku zapasów, wdrożenie w wersji uproszczonej - zajmuj się fakturowaniem proforma i Project Operations dla scenariuszy magazynowych / opartych na produkcji_

W tym temacie opisano funkcje, które zostały usunięte lub są przeznaczone do usunięcia z aplikacji Dynamics 365 Project Operations.

- *Usunięta* funkcja nie jest już dostępna w produkcie.
- *Przestarzała* funkcja nie znajduje się w aktywnym planowaniu i może zostać usunięta w przyszłej aktualizacji.

Ta lista ma na celu ułatwienie rozważenia tych usunięć i wycofań we własnym planowaniu.

> [!NOTE]
> Szczegółowe informacje o obiektów w aplikacji finansowych i operacyjnych można znaleźć w [**raportach z wykazami parametrów technicznych**](/dynamics/s-e/global/axtechrefrep_61). Można porównać różne wersje tych raportów, aby dowiedzieć się więcej o obiektach, które zostały zmienione lub usunięte w poszczególnych wersjach aplikacji finansowych i operacyjnych.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Funkcje usunięte lub przestarzałe w wydaniu Project Operations z marca 2022

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Parametr "Zawsze twórz transakcje korekty" w zarządzaniu projektami i księgowości

| &nbsp; | &nbsp; |
|--------|--------|
| **Przyczyna wycofania/usunięcia** | Do celów inspekcji wymagane są transakcje korekty. Po dez macji parametr ten zostanie ukryty. System zawsze tworzy transakcje korekty, tak jak obecnie, kiedy parametr jest ustawiony na **Tak**. |
| **Zastąpienie przez inną funkcję?** | Nie. |
| **Obszary produktów, których to dotyczy** | Aplikacja |
| **Opcja wdrożenia** | Project Operations dla scenariuszy obejmujących produkcję/magazynowanie |
| **Status** | Przestarzały: do 1 marca 2023 roku ukryć parametr i zmienić zachowanie systemu, aby transakcje korekty zawsze były tworzone. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Parametr "Użyj daty dostosowania jako nowej daty projektu" w zarządzaniu projektami i księgowości

| &nbsp; | &nbsp; |
|--------|--------|
| **Przyczyna wycofania/usunięcia** | Parametr został pierwotnie użyty w celu umożliwienia użytkownikom okres obrachunkowy zamknięcia listy. Jednak nie jest to już konieczne, ponieważ datę księgowyą transakcji można zmienić na pierwszą datę otwartego okresu, jeśli została skonfigurowana. Nie można zmieniać daty projektu, ponieważ reprezentuje ona datę, w która wystąpiła transakcja. |
| **Zastąpienie przez inną funkcję?** | Nie. |
| **Obszary produktów, których to dotyczy** | Aplikacja |
| **Opcja wdrożenia** | Project Operations dla scenariuszy obejmujących produkcję/magazynowanie |
| **Status** | Przestarzałe: do 1 marca 2023 r. ukryjemy parametr i zmienimy zachowanie systemu, aby data projektu nigdy nie uległa zmianie podczas korekt. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Przepływ pracy żądania zasobów w Project Operations dla scenariuszy magazynowych/produkcyjnych

| &nbsp; | &nbsp; |
|--------|--------|
| **Przyczyna wycofania/usunięcia** | Przestarzały z powodu niskiej liczby użycia i ograniczeń liczby transakcji. |
| **Zastąpienie przez inną funkcję?** | Nie. |
| **Obszary produktów, których to dotyczy** | Aplikacja |
| **Opcja wdrożenia** | Project Operations dla scenariuszy obejmujących produkcję/magazynowanie |
| **Status** | Przestarzały: do 1 marca 2023 roku wyłączymy opcję żądania zasobów dla projektu przy użyciu przepływu pracy. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Strona propozycje projektu na fakturze bez widoków Nagłówek i Wiersze

| &nbsp; | &nbsp; |
|--------|--------|
| **Przyczyna wycofania/usunięcia** | Przestarzałe z powodu udoskonaleń strony wprowadzonej razem z formularzami **użyj faktury i faktur projektu wraz z kluczem funkcji widoku Nagłówek i Wiersze**. |
| **Zastąpienie przez inną funkcję?** | Tak |
| **Obszary produktów, których to dotyczy** | Aplikacja |
| **Opcja wdrożenia** | Project Operations dla scenariuszy produkcyjnych/magazynowych; Project Operations dla scenariuszy niezabędowych |
| **Status** | Przestarzały: 1 marca 2023 r. zostanie wyłączona wcześniejsza strona (starsza) i zostanie domyślnie wyłączona funkcja **użyj faktur i faktur zafakturowanych z kluczem widoku Nagłówek i Wiersze**. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Funkcje usunięte lub przestarzałe w aplikacji Project Operations, wydanie z grudnia 2021 r.

### <a name="collaboration-workspaces"></a>Obszary robocze współpracy

[Tworzenie obszaru roboczego współpracy lub łączenie się z nim (projekt)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Przyczyna wycofania/usunięcia** | Funkcja uznana za przestarzałą z powodu niskiego użycia. Klienci używający aplikacji Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu mogą korzystać z funkcji [Współpraca z grupami pakietu Office](../project-management/collaboration-groups.md). |
| **Zastąpienie przez inną funkcję?** | Nie. |
| **Obszary produktów, których to dotyczy** | Aplikacja  |
| **Opcja wdrożenia** | Project Operations dla scenariuszy obejmujących produkcję/magazynowanie |
| **Status** | Przestarzała: planujemy zakończenie obsługi obszarów roboczych współpracy do 1 grudnia 2022 r. |
