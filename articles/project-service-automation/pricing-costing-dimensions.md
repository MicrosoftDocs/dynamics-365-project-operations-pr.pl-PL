---
title: Strona główna wymiarów kalkulacji cen i kosztów
description: Ta temat zawiera omówienie funkcjonalności wymiarów kalkulacji cen.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754307"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Strona główna wymiarów kalkulacji cen i kosztów

Wymiary używane w modułach kadrowych do konfigurowania kalkulacji cen i kosztów są podzielone na dwie kategorie:

- Osoby
- Zaplanowana praca

Z tego powodu w programie Project Service Automation (PSA) są dostępne dwa typy wartości wymiarów kalkulacji cen: 

- **Zestawy opcji** — wymiary, które są ustalonymi elementami stałotekstowymi dla zbioru wartości.
- **Wartości oparte na encjach** — wymiary, które mogą być różnymi zbiorami wartości.

## <a name="pricing-dimensions"></a>Wymiary kalkulacji cen

Program PSA zawiera fabrycznie domyślny zestaw wymiarów kalkulacji cen. Można je obejrzeć po wybraniu kolejno opcji **Project Service** > **Parametry**. W rekordzie parametru na karcie **Wymiary kalkulacji cen oparte na kwocie** upewnij się, że rola **msdyn_resourcecategory** oraz jednostka organizacyjna zasobów **msdyn_organizationalunit** mają w polach **Ma zastosowanie do sprzedaży** i **Ma zastosowanie do kosztu** ustawioną wartość **Tak**. Pozwoli to skonfigurować cenę i koszt dla każdej kombinacji roli i jednostki organizacyjnej.

![Zrzut ekranu z parametrami usługi Project Service z wyróżnioną opcją „Ma zastosowanie do sprzedaży”](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Jeżeli w wersji programu PSA sprzed 3 używano gotowych pól roli i jednostki organizacyjnej jako wymiarów kalkulacji cen, nie będzie żadnych zauważalnych zmian. Można nadal korzystać z usługi Project Service w zwykły sposób. 

Jeśli trzeba określić ceny lub koszty zasobów przy użyciu dodatkowych atrybutów, można utworzyć niestandardowe pola, encje i wymiary. Aby uzyskać więcej informacji, zobacz następujące tematy. Należy jednak pamiętać, że procedury trzeba wykonywać w poniższej kolejności:

- [Tworzenie niestandardowych pól i encji](create-custom-fields-entities.md)
- [Dodawanie pól niestandardowych do ustawień cen i encji transakcyjnych](field-references.md)
- [Konfigurowanie pól niestandardowych jako wymiarów kalkulacji cen](set-up-pricing-dimensions.md)
- [Aktualizowanie atrybutów dodatków plug-in w celu dołączenia nowych wymiarów kalkulacji cen](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Wycena pracy personelu
Sposób wyceny czasu pracy personelu w organizacji jest często ważnym strategicznym aspektem, który wpływa na rentowność organizacji. Gdy organizacja jest gotowa do określenia, jak chce skonfigurować stawki rozliczania i kosztów dla czasu pracy ludzi, administrator systemu informatycznego powinien to zrobić wspólnie z zespołami finansowymi i szefami działów.

Inne kryteria wyceny to na przykład określenie, czy mają zostać wykorzystane pola i encje, które obecnie nie są wymiarami kalkulacji cen, ale nadają się do takiej funkcji w organizacji. Pola takie jak **Kategoria transakcji** (**msdyn_transactioncategory**) i **Zasób, który można zarezerwować** (**bookableresource**) to przykłady kandydatów na wymiary. 

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
