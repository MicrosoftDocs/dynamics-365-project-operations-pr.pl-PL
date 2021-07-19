---
title: Project Operations — integracja podwójnego zapisu
description: Ten temat umożliwia omówienie integracji podwójnego zapisu w Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: 540b6f74d8e79116e5fdb2ceffaa4bbb487ff08f
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368444"
---
# <a name="project-operations-dual-write-integration-overview"></a>Omówienie: Project Operations — integracja podwójnego zapisu

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Project Operations używa [funkcji podwójnego zapisu](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) do synchronizowania danych między Microsoft Dataverse i Dynamics 365 Finance.

Na poniższym rysunku pokazano, jak są synchronizowane dane w ramach integracji między Dataverse a Finance.

![Omówienie przepływów danych Project Operations](./media/ProjectOperationsFlows.jpg)

Project Operations w Dataverse zapewnia nowoczesny interfejs użytkownika (UI) i łatwą rozszerzalność bez kodu/niskokodowo z wykorzystaniem możliwości Power Platform. Menedżerowie projektów, menedżerowie zasobów, członkowie zespołu projektu i inne osoby front office mogą wykonywać swoje działania Project Operations w Dataverse.

Project Operations w Finanse umożliwia obsługę księgowych projektów i rozpoznawanie przychodów. Project Operations włącza się do struktury finansowej w Finance na potrzeby obliczania podatku, kursów wymiany walut, raportowania rozmiarów finansowych itp. Środowisko obsługi klienta projektu w większości jest oparte na Finance.

Integracja Project Operations składa się z następującej integracji składników:


- [Integracja danych instalacji i konfiguracji aplikacji Project Operations](resource-dual-write-setup-integration.md) 
- [Szacowania projektu i wartości rzeczywistych](resource-dual-write-estimates-actuals.md)
- [Faktury projektu](resource-dual-write-project-invoice.md)
- [Zarządzanie wydatkami](resource-dual-write-expense.md)
- [Faktura od dostawcy](resource-dual-write-vendor-invoice.md)
