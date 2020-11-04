---
title: Przegląd wymiarów kalkulacji cen
description: W tym temacie zamieszczono informacje na temat wymiarów kalkulacji cen w Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6b1ebdc97ec4704ba256acb521c0f2e7c474940b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082119"
---
# <a name="pricing-dimensions-overview"></a>Przegląd wymiarów kalkulacji cen

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Wymiary używane w modułach kadrowych do konfigurowania kalkulacji cen i kosztów są podzielone na dwie kategorie:

- Osoby
- Zaplanowana praca

Z tego powodu są dostępne dwa typy wartości wymiarów kalkulacji cen:

- **Zestawy opcji** : wymiary, które są ustalonymi elementami stałotekstowymi dla zbioru wartości.
- **Wartości oparte na encjach** : wymiary, które mogą być różnymi zbiorami wartości.

## <a name="pricing-dimensions"></a>Wymiary kalkulacji cen

Dynamics 365 Project Operations zawiera domyślny zestaw wymiarów kalkulacji cen. Można obejrzeć te wymiary kalkulacji cen po wybraniu kolejno opcji **Project Operations** > **Parametry**. W rekordzie parametru na karcie **Wymiary kalkulacji cen oparte na kwocie** upewnij się, że rola **msdyn_resourcecategory** oraz jednostka organizacyjna zasobów **msdyn_organizationalunit** mają w polach **Ma zastosowanie do sprzedaży** i **Ma zastosowanie do kosztu** ustawioną wartość **Tak**. Po uruchomieniu tych pól, pozwoli to skonfigurować cenę i koszt dla każdej kombinacji roli i jednostki organizacyjnej.

Jeśli trzeba określić ceny lub koszty zasobów przy użyciu dodatkowych atrybutów, można utworzyć niestandardowe pola, encje i wymiary.

## <a name="pricing-human-resource-time"></a>Wycena pracy personelu
Sposób wyceny czasu pracy personelu w organizacji jest często ważnym strategicznym aspektem, który wpływa na rentowność organizacji. Gdy organizacja jest gotowa do określenia, jak chce skonfigurować stawki rozliczania i kosztów dla czasu pracy ludzi, administrator systemu informatycznego powinien to zrobić wspólnie z zespołami finansowymi i szefami działów.

Inne kryteria wyceny to na przykład określenie, czy mają zostać wykorzystane pola i encje, które obecnie nie są wymiarami kalkulacji cen, ale nadają się do takiej funkcji w organizacji. Pola takie jak **Kategoria transakcji** ( **msdyn_transactioncategory** ) i **Zasób, który można zarezerwować** ( **bookableresource** ) to przykłady kandydatów na wymiary. 

Należy także rozważyć, czy wymiar kalkulacji cen powinien być tabelą, czy zestawem opcji. Jeśli przewidujesz zmiany wartości wymiaru w liczbie przekraczającej 10 lub 12, w związku z czym będziesz potrzebować dodatkowych atrybutów w takich wymiarach, lepiej utworzyć encję, a nie zestaw opcji. Zarządzanie zestawem opcji, czyli na przykład dodawanie lub usuwanie wartości, wymaga udziału administratora lub programisty, podczas nowe wiersze do tabeli może dodawać większość użytkowników.

W przykładzie pod spodem przedstawiono stawki rozliczania skonfigurowane na podstawie roli oraz jednostki organizacyjnej zasobów, do której należy zasób. Stawki kosztów są zwykle oparte na paśmie wynagrodzenia pracownika i na jednostce organizacyjnej, do której pracownik należy. W tym przykładzie tabele stawek rozliczania i stawek kosztów wyglądają następująco:

**Przykładowe stawki rozliczania**

| Rola        | Jednostka organizacyjna    |Jednostka      |Cena      |Waluta  |
| ------------|-------------|----------|----------:|----------|
| Dla deweloperów   | Contoso US  |Hour | 200|USD     |
| Dla deweloperów   | Contoso India |Hour|   112|USD     |


**Przykładowe stawki kosztów**

| Pasmo wynagrodzenia     | Jednostka organizacyjna    |Jednostka      |Cena      |Waluta  |
| ----------------|-------------|----------|----------:|----------|
| Moja firma_pasmo1 | Contoso US  |Hour | 145|USD     |
| Moja firma_pasmo2 | Contoso India |Hour|   67|USD     |
