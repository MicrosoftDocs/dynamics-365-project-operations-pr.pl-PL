---
title: Każdego dnia
description: Ta temat zawiera informacje na temat reguł na dzień, które są używane w zarządzaniu wydatkami.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: e537d6c6112eb4baf38229e3e40897eacdf21983
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578307"
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]