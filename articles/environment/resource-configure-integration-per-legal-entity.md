---
title: Konfigurowanie integracji aplikacji Project Operations według firm
description: W tym temacie zamieszczono informacje dotyczące ustawienia integracji danych dotyczących podmiotu prawnego w Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5d2bb415362a088e01253fbe54f9f06569b4a921
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122896"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Konfigurowanie integracji aplikacji Project Operations według firm 

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Ten temat zapozna użytkownika z krokami wymaganymi do skonfigurowania Dynamics 365 Project Operations dla każdego podmiotu prawnego.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Uruchamianie klawiszy funkcji w Dynamics 365 Finance

Wykonaj poniższe kroki w celu włączenia wymaganych funkcji.

1. W Dynamics 365 Finance przejdź do obszaru roboczego **Zarządzanie danymi**.
2. Na liście **Funkcji** znajdź i włącz następujące funkcje:
  
    - **Włączanie wielu pozycji kontraktu dla projektu**
    - **Włączanie Project Operations w Dynamics 365 Customer Engagement**

> [!NOTE]
> Jeśli nie są widoczne **Klawisze funkcji**, należy sprawdzić, czy wersja Finance spełnia minimalne wymagania dotyczące wersji (wersja aplikacji 10.0.13 wraz ze wszystkimi zastosowanymi aktualizacjami lub wyższa). Wybierz opcję **Wyszukaj aktualizacje** aby odświeżyć listę funkcji.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Definiowanie scenariusza wdrażania Project Operations dla podmiotu prawnego

Project Operations można włączyć na poziomie podmiotu prawnego w Dynamics 365 Customer Engagement. Użytkownik może dysponować jedną firmą korzystającą z Project Operations w Dynamics 365 Customer Engagement na potrzeby scenariuszy dla zasobów/scenariuszy nieopartych na zaopatrzeniu. W tym samym środowisku inna firma może korzystać z Project Operations na potrzeby scenariuszy opartych na zaopatrzeniu / scenariuszy zamówień produkcyjnych.

1. W Dynamics 365 Finance przejdź do **Zarządzanie projektami i księgowanie** > **Ustawienia** > **Parametry zarządzania projektami i księgowania**.
2. Z poziomu listy dostępnych podmiotów prawnych wybierz podmioty, w których będzie włączone wiele pozycji kontraktu i funkcje Project Operations w Dynamics 365 Customer Engagement. Pozostaw osoby prawne, które będą używać Project Operations dla scenariuszy magazynowych/zleceń produkcyjnych, jako niezaznaczone.

> [!NOTE]
> Podmiot prawny można wybrać tylko wtedy, gdy nie ma dla niego żadnych istniejących projektów.

## <a name="configure-project-management-and-accounting-parameters"></a>Konfiguracja zarządzania projektem i parametrów księgowania

Każdy podmiot prawny korzystający z Project Operations w Dynamics 365 Customer Engagement musi mieć zestaw parametrów domyślnych. Te parametry są konfigurowane na karcie **Project Operations** na stronie **Zarządzanie projektami i parametry księgowania**. Te parametry to:

  - **Domyślne ustawienia typu fakturowania**: Project Operations korzysta ze stałego zestawu wartości domyślnych typu fakturowania, które muszą być mapowane na właściwości wierszy Finance. Utwórz rekord dla każdego typu fakturowania: **nieokreślony**, **odpłatny**, **nieodpłatny**, **bezpłatny** i **niedostępny**.
  - **Wartości domyślne kategorii projektów**: należy wybrać domyślne kategorie projektów, które mają być używane dla poszczególnych typów transakcji. Te wartości domyślne będą używane w **Arkuszu integracji Project Operations** i w oszacowaniach, w których kategoria transakcji nie jest określona dla wartości rzeczywistej projektu.
  - **Prognozy**: należy wybrać model prognozy, który ma być używana na potrzeby oszacowań czasu i wydatków.


[!INCLUDE[footer-include](../includes/footer-banner.md)]