---
title: Co nowego w sierpniu 2021 r. — wdrażanie wersji uproszczonej aplikacji Project Operations
description: Ten artykuł zawiera informacje o aktualizacjach jakości dostępnych w wydaniu Project Operations — wersja uproszczona w sierpniu 2021 r.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 84318a26d97355fe56794e1d1532576cde4af661
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922051"
---
# <a name="whats-new-august-2021---project-operations-lite-deployment"></a>Co nowego w sierpniu 2021 r. — wdrażanie wersji uproszczonej aplikacji Project Operations

_Zastosowane do: Wdrażanie uproszczone — od okazji do faktury pro forma_

Ten artykuł dotyczy następujących składników i wersji oprogramowania Dynamics 365 Project Operations:

  - Project Operations w środowisku Dataverse w wersji 4.13.0.152

## <a name="features-included-in-this-release"></a>Funkcje uwzględnione w tym wydaniu

To wydanie zawiera następujące funkcje:

- **Zestawy zatwierdzeń**: zestawy zatwierdzeń grupują żądania zatwierdzenia użycia czasu, wydatków i materiałów razem w mniejsze podzestawy operacji. Takie grupowanie umożliwia przetwarzanie zatwierdzeń w określonej kolejności w ramach projektu oraz umożliwia ponowne przetwarzanie i sekwencjonowanie. Grupowanie żądań poprawia niezawodność i możliwość śledzenia przetwarzania zatwierdzeń w przypadku dużej liczby zatwierdzeń. Aby uzyskać więcej informacji, zobacz [Zestawy zatwierdzeń](../../approvals/approval-sets.md).

## <a name="quality-updates"></a>Aktualizacje dotyczące jakości

### <a name="project-operations-on-dataverse"></a>Project Operations w usłudze Dataverse

| **Obszar funkcji** | **Numer referencyjny** | **Aktualizacja dotycząca jakości** |
| --- | --- | --- |
| Rozliczenia i ceny | 2295625 | Nazwa punktu kontrolnego musi być skopiowana z harmonogramu faktur do szczegółów wiersza faktury. |
| Rozliczenia i ceny | 2316323 | Nie można edytować rabatu na fakturze proforma w aplikacji Project Operations w scenariuszach opartych na zasobach. |
|   Zarządzanie szansami sprzedaży | 2338619 | Reguły biznesowe **Szansa sprzedaży** i **Oferta** muszą być wywoływane tylko na stronach. |
| Zarządzanie zasobami | 2316523 | Użycie polecenia **Wyślij żądanie** z poziomu wymagania zasobu, który ma załączona rolę, nie powinno powodować wyświetlenia błędu. |
| Zarządzanie zasobami | 2326885 | Utworzenie wymagania zasobu w ramach projektu nie powinno powodować wyświetlenia błędu. |
| Czas i wydatek | 2335584 | Przestarzałe przepływy zadań są przepływami we wpisie czasu. |
| Czas i wydatek | 2336884 | Przycisk wpisu czasu **Kopiuj tydzień** musi działać dla więcej niż tylko bieżącego użytkownika. |
