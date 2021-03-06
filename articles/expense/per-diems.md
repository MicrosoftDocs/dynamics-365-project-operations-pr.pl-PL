---
title: Każdego dnia
description: Ta temat zawiera informacje na temat reguł na dzień, które są używane w zarządzaniu wydatkami.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 7d1c4ac7781cb711e2cc0d09606d422b4dd554f3
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908454"
---
# <a name="per-diems"></a>Każdego dnia

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_


Stawka dzienna jest przyznawana pracownikowi, który podróżuje do pracy. W przypadku zarządzania wydatkami można tworzyć reguły na diety dzienne dla różnych typów podróży. Stawki dzienne mogą być oparte na porze roku, miejscu podróży lub obydwu tych danych. Podczas tworzenia reguły diety dziennej można określić, że procent stawki diety będzie wstrzymany, jeśli pracownik otrzymuje dodatkowe posiłki lub usługi. Można również ustawić minimalną i maksymalną liczbę godzin, w przypadku których stawka dzienna może być zastosowana do kosztów podróży pracownika.

## <a name="configuration"></a>Konfiguracja 

1. Aby dodać lokalizacje diety, przejdź do **Ustawienia** > **Obliczeń i kody** > **Lokalizacje diety na dzień**.
2. W przypadku każdej z dodanych wcześniej lokalizacji wybierz stawkę diety i walutę, która obowiązuje między określoną datą początkową i końcową dla hotelu, dań i innych kosztów. Stawki za diety i waluty konfiguruje się w obszarze **Konfigurowanie** > **Obliczenia i kody** > **Stawki na dzień**.
3. Na stronie **Lokalizacje z dietą na dzień** skonfiguruj warstwy stawek diet na dzień. Poziomy stawki diety na dzień umożliwiają zdefiniowanie procentowego podziału dziennego wydatku na hotel, posiłki i inne koszty. 
4. Aby określić redukcję procentową za śniadanie, obiad lub kolację, należy zaktualizować pola na stronie **Parametry zarządzania wydatkami** na karcie **Na dzień**. 
    
## <a name="submit-expenses-using-per-diem"></a>Prześlij koszty przy użyciu diety na dzień
Aby przesyłać wydatki umożliwiające korzystanie z diet na dzień, należy skorzystać z kategorii wydatków **Na dzień** podczas tworzenia raportu z wydatków. Wprowadź **Datę diety na dzień**, **Datę końcową diety na dzień** i **Lokalizację diety na dzień**. Kwota będzie obliczana na podstawie stawek diety na dzień dla wybranej lokalizacji, a redukcja za posiłki będzie obliczana na podstawie warstw stawek diety.
