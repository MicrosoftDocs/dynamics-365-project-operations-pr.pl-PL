---
title: Ręczne wdrażanie aplikacji Project Operations usługi Dataverse z obsługą podwójnego zapisu
description: W tym temacie opisano sposób ręcznego wdrażania aplikacji Project Operations Dataverse, która obsługuje podwójny zapis.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 06325a9a9f9084d1f506f2493c32565fe7b7c52ae6fe22c81339b9c1d632e688
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986459"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a>Ręczne wdrażanie aplikacji Project Operations usługi Dataverse z obsługą podwójnego zapisu

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

W tym temacie opisano sposób ręcznego wdrażania aplikacji Microsoft Dynamics 365 Project Operations w usłudze Microsoft Dataverse, co ma umożliwić obsługę podwójnego zapisu. Aplikacja Project Operations wykrywa konfigurację środowiska i dodaje dodatkową obsługę podwójnego zapisu, jeśli zostaną spełnione wymagania wstępne.

Podczas wdrażania w ramach usług Microsoft Dynamics Lifecycle Services (LCS), jeśli wykonano instrukcje z tego tematu, można pominąć wdrożenie integracji platformy Microsoft Power Platform (wcześniej znanej jako środowisko Common Data Service).

Proces wdrażania aplikacji Project Operations w usłudze Dataverse w celu włączenia podwójnego zapisu ma cztery podstawowe kroki:

1. [Tworzenie w usłudze Dataverse nowego środowiska obsługującego podwójny zapis](#create).
2. [Dodawanie wymagań wstępnych dotyczących podwójnego zapisu do środowiska](#prerequisites).
3. [Dodawanie aplikacji Project Operations Dataverse](#dataverse).
4. [Łączenie środowisk](#link).

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a>Tworzenie w usłudze Dataverse nowego środowiska obsługującego podwójny zapis

Aby wykonać tę procedurę, należy zalogować się jako administrator.

1. Otwórz [centrum administracyjne platformy Power Platform](https://admin.powerplatform.com) i zaloguj się jako administrator.
2. Utwórz nowe środowisko i nadaj mu nazwę.
3. Wybierz typ środowiska. Jeśli utworzono konto oferty wersji próbnej, wybierz **Wersja próbna (oparta na subskrypcji)**.
4. Potwierdź region wdrożenia.
5. Włącz opcję **Utwórz bazę danych dla tego środowiska**. 
6. Potwierdź język, a następnie potwierdź, że waluta odpowiada walucie w Twoich aplikacjach Finance and Operations.
7. Włącz opcję **Aplikacje Dynamics 365** i sprawdź, czy pole **Automatycznie wdrażaj te aplikacje** ma wartość **Brak**.
8. Jeśli jest wymagana grupa zabezpieczeń, dodaj tę grupę.
9. Wybierz **Zapisz**, aby utworzyć nowe środowisko.
10. Poczekaj na ukończenie wdrożenia i osiągnięciu stanu **Gotowe** przez środowisko.

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a>Dodawanie wymagań wstępnych dotyczących podwójnego zapisu do środowiska

Obsługa podwójnego zapisu obejmuje dodatkowe pola, które zostały dodane do encji kluczowych, takich jak encja **Firma**. Jeśli dodajesz obsługę podwójnego zapisu do istniejącego środowiska, być może trzeba będzie zaktualizować dane, aby włączyć tę obsługę. Aby uzyskać informacje na temat ładowania początkowego danych, zobacz [Ładowanie początkowe danych firmy](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data). Aby uzyskać więcej informacji na temat podwójnego zapisu, zobacz [Wymagania systemowe dotyczące podwójnego zapisu](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).

Wykonaj tę procedurę, aby dodać do środowiska wymagania wstępne dotyczące podwójnego zapisu.

1. Otwórz środowisko, które właśnie utworzono, a następnie przejdź do pozycji **Zasób** \> **Aplikacje Dynamics 365**.
2. Wybierz z listy aplikacji **Rozwiązanie podstawowe Podwójny zapis** i zainstaluj je.
3. Poczekaj na ukończenie instalacji. Następnie wybierz z listy aplikacji **Rozwiązanie do aranżacji Podwójny zapis** i zainstaluj je.

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a>Dodawanie aplikacji Project Operations Dataverse

Tę procedurę można wykonać tylko wtedy, gdy zostały wykonane poprzednie procedury przed zainstalowaniem aplikacji Project Operations. Podczas instalacji system analizuje konfigurację środowiska i dodaje obsługę podwójnego zapisu, jeśli jest ona wymagana.

1. Otwórz środowisko, które wcześniej utworzono, a następnie przejdź do pozycji **Zasób** \> **Aplikacje Dynamics 365**.
2. Wybierz z listy aplikacji **Microsoft Dynamics 365 Project Operations** i zainstaluj ją.

## <a name="link-your-environments"></a><a name="link"></a>Łączenie środowisk

Po wdrożeniu środowiska usługi Dataverse można skonfigurować link w swoich aplikacjach Finance and Operations. Wykonaj kroki z tematu [Łączenie środowisk za pomocą kreatora podwójnego zapisu](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).
