---
title: Odinstaluj program Dynamics 365 Project Operations
description: Ten temat zawiera informacje o odinstalowaniu Dynamics 365 Project Operations.
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b87c9324b1c95c10ef1e18b0fbf4572bdbe76827
ms.sourcegitcommit: b8b7a59eee7d93638446e93726d270316e45ab3d
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/10/2021
ms.locfileid: "7783656"
---
# <a name="uninstall-dynamics-365-project-operations"></a>Odinstaluj program Dynamics 365 Project Operations 

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Aby odinstalować Dynamics 365 Project Operations, użytkownik musi mieć przypisaną rolę Administrator.

1. Wybierz kolejno pozycje **Ustawienia** > **Rozwiązania**.

    ![Strona ustawień.](./media/uninstall-proj-ops-solutions.png)
  
2. Usuń rozwiązania dokładnie w kolejności, w jakiej są wymienione w poniższej tabeli. 

    | Krok | Nazwa   rozwiązania                                    | Uwaga                                                                                         |
    |------|----------------------------------------------------|----------------------------------------------------------------------------------------------|
    | 1 | msdyn_ProjectServiceUpgrade_managed.cab            | Jeśli nie znaleziono, pomiń to rozwiązanie.                                                            |
    | 2 | ProjectOperations_Anchor                           | Jeśli nie znaleziono, pomiń to rozwiązanie.                                                            |
    | 3 | Dynamics365ProjectOperationsDualWriteEntityMaps    | Jeśli nie znaleziono, pomiń to rozwiązanie.                                                            |
    | 100 | Dynamics365ProjectOperationsDualWrite              | Jeśli nie znaleziono, pomiń to rozwiązanie.                                                            |
    | 5 | ProjectService                                     | Brak dodatkowych uwag.                                                                         |
    | 6 | ProjectServiceCore_Patch                           | Brak dodatkowych uwag.                                                                         |
    | 7 | ProjectServiceCore                                 | Brak dodatkowych uwag.                                                                         |
    | 8 | ProjectServiceDeprecatedComponents                 | Jeśli nie znaleziono, pomiń to rozwiązanie.                                                            |
    | 9 | FieldServiceCommon                                 | Wymagane do podwójnego zapisu z Dynamics 365 Finance lub Dynamics 365 Supply Chain Management.   |
    | 10 | msdyn_AssetCommon                                  | Wymagane do podwójnego zapisu z Dynamics 365 Finance lub Dynamics 365 Supply Chain Management.   |
    | 11 | msdyn_TESA_Anchor                                  | Wymagana dla Dynamics 365 Field Service.                                                     |
    | 12 | msdyn_TESA_Patch                                   | Wymagana dla Dynamics 365 Field Service.                                                     |
    | 13 | msdyn_TESA                                         | Wymagana dla Dynamics 365 Field Service.                                                     |
    | 14 | ResourceSchedulingControls                         | Wymagana dla Dynamics 365 Field Service.                                                     |
    | 15 | MicrosoftDynamicsScheduling3_CumulativePatch       | Wymagana dla Dynamics 365 Field Service.                                                     |
    | 16 | MicrosoftDynamicsScheduling_Patch_xx               | Wymagana dla Dynamics 365 Field Service.                                                     |
    | 17 | MicrosoftDynamicsScheduling                        | Wymagana dla Dynamics 365 Field Service.                                                     |
    | 18 | Dynamics365FinanceAndOperationsAnchor              | Jeśli nie znaleziono, pomiń to rozwiązanie.                                                            |
    | 19 | Dynamics365Notes                                   | Jeśli nie znaleziono, pomiń to rozwiązanie.                                                            |
    | 20 | Dynamics365FinanceAndOperationsDualWriteEntityMaps | Jeśli nie znaleziono, pomiń to rozwiązanie.                                                            |
    | 21 | DualWriteCore                                      | Jeśli nie znaleziono, pomiń to rozwiązanie.                                                            |
    | 22 | Dynamics365AssetManagementApp                      | Jeśli nie znaleziono, pomiń to rozwiązanie.                                                            |
    | 23 | Dynamics365AssetManagement                         | Jeśli nie znaleziono, pomiń to rozwiązanie.                                                            |
    | 24 | Dynamics365SupplyChainExtended                     | Jeśli nie znaleziono, pomiń to rozwiązanie.                                                            |
    | 25 | Dynamics365FinanceExtended                         | Jeśli nie znaleziono, pomiń to rozwiązanie.                                                            |
    | 26 | HCMCommon                                          | Jeśli nie znaleziono, pomiń to rozwiązanie.                                                            |
    | 27 | Dynamics365FinanceAndOperationsCommon              | Jeśli nie znaleziono, pomiń to rozwiązanie.                                                            |
    | 28 | Strona                                              | Jeśli nie znaleziono, pomiń to rozwiązanie.                                                            |
    | 29 | Dynamics365Company                                 | Jeśli nie znaleziono, pomiń to rozwiązanie.                                                            |
    | 30 | CurrencyExchangeRates                              | Jeśli nie znaleziono, pomiń to rozwiązanie.                                                            |
    | 31 | AssetCommon                                        | Jeśli nie znaleziono, pomiń to rozwiązanie.                                                            |
