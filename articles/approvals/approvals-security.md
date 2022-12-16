---
title: Zabezpieczenia i zatwierdzenia
description: Ten artykuł zawiera informacje o ustawieniach zabezpieczeń dla pracy z zatwierdzeniami w Microsoft Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: conceptual
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 88186485dff43c3011095b267640151948b4d77c
ms.sourcegitcommit: 0d11377bf3ac74c80afbd2013775fcc9869f926a
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/10/2022
ms.locfileid: "9841937"
---
# <a name="security-and-approvals"></a>Zabezpieczenia i zatwierdzenia

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Microsoft Dynamics 365 Project Operations używa dwóch ról zabezpieczeń, aby umożliwić zatwierdzanie wpisów dotyczących czasu, wydatków i materiałów:

- Osoba zatwierdzająca projekt
- Administrator zatwierdzający projekt

## <a name="project-approver"></a>Osoba zatwierdzająca projekt

Aby zatwierdzać wpisy dotyczące czasu, wydatków i materiałów w projekcie, musisz mieć rolę **osoby zatwierdzającej projekt**. Trzeba mieć również dostęp do odpowiednich encji pokrewnych, takich jak **Projekt**. Ten dostęp może przypisać ktoś, kto ma rolę **Menedżer projektu**. Ponadto musisz być członkiem zespołu w projekcie i być zaznaczonym jako osoba zatwierdzająca.

Aby zatwierdzić wpisy niebędące projektami, musisz być przełożonym osoby zgłaszającej.

## <a name="project-approver-admin"></a>Administrator zatwierdzający projekt

> [!NOTE]
> Funkcja [Zestawy zatwierdzeń](approval-sets.md) musi być włączona, zanim będziesz mógł korzystać z funkcji Administratora projektu.

Rola bezpieczeństwa **Zatwierdzający projekt administrator** pozwala użytkownikom na omijanie zasad i umożliwia zatwierdzanie wpisów we wszystkich projektach. Przypisanie tej roli ominie logikę walidacji, która wymaga członkostwa w zespole i oznaczenia jako zatwierdzającego. Trzeba mieć dostęp do odpowiednich tabel pokrewnych, takich jak **Projekt**, za pośrednictwem przypisanych ról zabezpieczeń.

Kontekst użytkownika SYSTEM omija walidację w taki sam sposób, jak rola bezpieczeństwa Administrator zatwierdzający projekt.
