---
title: Konfigurowanie integracji aplikacji Project Operations według firm
description: W tym artykule przedstawiono informacje dotyczące konfigurowania integracji według firmy w aplikacji Project Operations.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3f33e641ee0932655282618c99a26e2603660059
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914691"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Konfigurowanie integracji aplikacji Project Operations według firm 

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

W tym artykule opisano kroki wymagane do skonfigurowania aplikacji Dynamics 365 Project Operations według firmy.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Włącz funkcję kluczy w Dynamics 365 Finance

Wykonaj poniższe kroki w celu włączenia wymaganych funkcji.

1. W programie Dynamics 365 Finance przejdź do obszaru roboczego **Zarządzanie funkcjami**.
2. Na liście **Funkcji** znajdź i włącz następujące funkcje:
  
    - **Włączanie wielu pozycji kontraktu dla projektu**
    - **Włączanie Project Operations w u klientach usługi Dynamics 365 Customer Engagement**

> [!NOTE]
> Jeśli nie są widoczne **Klawisze funkcji**, należy sprawdzić, czy wersja Finance spełnia minimalne wymagania dotyczące wersji (wersja aplikacji 10.0.13 wraz ze wszystkimi zastosowanymi aktualizacjami lub wyższa). Wybierz opcję **Wyszukaj aktualizacje** aby odświeżyć listę funkcji.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Definiowanie scenariusza wdrażania Project Operations dla podmiotu prawnego

Project Operations można włączać na poziomie encji prawnej w u klientach usługi Dynamics 365 Customer Engagement. W przypadku scenariuszy opartych na zasobach i niedosyłanych zasobach można utworzyć jedną encję prawną przy użyciu funkcji Project Operations w u klientach usługi Dynamics 365 Customer Engagement. W tym samym środowisku inna firma może korzystać z Project Operations na potrzeby scenariuszy opartych na zaopatrzeniu / scenariuszy zamówień produkcyjnych.

1. W układzie Dynamics 365 Finance przejdź do **strony Zarządzanie projektami i rozliczeniami** > **Ustawienia** > **Parametry zarządzania projektami i księgowymi**.
2. Z listy dostępnych encji prawnej wybierz encje, w których będzie włączona obsługa wielu wierszy kontraktu i Project Operations w programie Dynamics 365 Customer Engagement. Pozostaw osoby prawne, które będą używać Project Operations dla scenariuszy magazynowych/zleceń produkcyjnych, jako niezaznaczone.

> [!NOTE]
> Podmiot prawny można wybrać tylko wtedy, gdy nie ma dla niego żadnych istniejących projektów.

## <a name="configure-project-management-and-accounting-parameters"></a>Konfiguracja zarządzania projektem i parametrów księgowania

Każda encja prawnie korzystająca z funkcji Project Operations w u klientach Dynamics 365 Customer Engagement musi mieć zestaw parametrów domyślnych. Te parametry są konfigurowane na karcie **Project Operations** na stronie **Zarządzanie projektami i parametry księgowania**. Te parametry to:

  - **Domyślne ustawienia typu fakturowania**: Project Operations korzysta ze stałego zestawu wartości domyślnych typu fakturowania, które muszą być mapowane na właściwości wierszy Finance. Utwórz rekord dla każdego typu fakturowania: **nieokreślony**, **odpłatny**, **nieodpłatny**, **bezpłatny** i **niedostępny**.
  - **Wartości domyślne kategorii projektów**: należy wybrać domyślne kategorie projektów, które mają być używane dla poszczególnych typów transakcji. Te wartości domyślne będą używane w **Arkuszu integracji Project Operations** i w oszacowaniach, w których kategoria transakcji nie jest określona dla wartości rzeczywistej projektu.
  - **Prognozy**: należy wybrać model prognozy, który ma być używana na potrzeby oszacowań czasu i wydatków.


[!INCLUDE[footer-include](../includes/footer-banner.md)]