---
title: Przegląd wymiarów kalkulacji cen
description: Ten temat zawiera informacje o wymiarach kalkulacji cen w aplikacji Dynamics 365 Project Operations.
author: rumant
ms.date: 11/30/2020
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5f1fa83b52c3812f26e3ab75a8b08ebd40d82aa8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579273"
---
# <a name="pricing-dimensions-overview"></a>Przegląd wymiarów kalkulacji cen

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Wymiary używane w modułach kadrowych do konfigurowania kalkulacji cen i kosztów są podzielone na dwie kategorie:

- Osoby
- Zaplanowana praca

Z tego powodu są dostępne dwa typy wartości wymiarów kalkulacji cen:

- **Zestawy opcji**: wymiary, które są ustalonymi elementami stałotekstowymi dla zbioru wartości.
- **Wartości oparte na encjach**: wymiary, które mogą być różnymi zbiorami wartości.

## <a name="pricing-dimensions"></a>Wymiary kalkulacji cen

Aplikacja Dynamics 365 Project Operations oferuje wbudowany domyślny zestaw wymiarów kalkulacji cen. Można obejrzeć te wymiary kalkulacji cen po wybraniu kolejno opcji **Project Operations** > **Parametry**. W rekordzie parametru na karcie **Wymiary kalkulacji cen oparte na kwocie** upewnij się, że rola **msdyn_resourcecategory** oraz jednostka organizacyjna zasobów **msdyn_organizationalunit** mają w polach **Ma zastosowanie do sprzedaży** i **Ma zastosowanie do kosztu** ustawioną wartość **Tak**. Po uruchomieniu tych pól, pozwoli to skonfigurować cenę i koszt dla każdej kombinacji roli i jednostki organizacyjnej.

![Zrzut ekranu z parametrami usługi Project Service z wyróżnioną opcją „Ma zastosowanie do sprzedaży”.](media/PS-OOB-parameters.png)

Jeśli trzeba określić ceny lub koszty zasobów przy użyciu dodatkowych atrybutów, można utworzyć niestandardowe pola, encje i wymiary. Aby uzyskać więcej informacji, zobacz następujące tematy. 
  
  > [!NOTE]
  > Procedury muszą być wykonane w kolejności, w jakiej są umieszczone na liście.

1. [Tworzenie rozwiązania dla niestandardowych wymiarów kalkulacji cen](../sales/create-solution-custompd.md)
2. [Tworzenie niestandardowych pól i encji](create-custom-fields-entities-pricing-dimensions.md)
3. [Dodawanie pól niestandardowych do ustawień cen i encji transakcyjnych ](add-custom-fields-price-setup-transactional-entities.md)
4. [Konfigurowanie pól niestandardowych jako wymiarów kalkulacji cen ](set-up-custom-fields-pricing-dimensions.md)
5. [Aktualizowanie atrybutów dodatków plug-in w celu dołączenia nowych wymiarów kalkulacji cen](update-plugin-attributes-pd.md)


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


[!INCLUDE[footer-include](../includes/footer-banner.md)]