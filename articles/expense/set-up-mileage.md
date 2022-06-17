---
title: Konfigurowanie przebiegu używającego warstw współczynnika przebiegu
description: W tym artykule podane są informacje o stawkach za przebieg oraz warstw stawek za przebieg.
author: suvaidya
ms.date: 05/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 03ca18c8fef6228f2ba553ebe50447beda5a857c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930147"
---
# <a name="set-up-mileage-using-mileage-rate-tiers"></a>Konfigurowanie przebiegu używającego warstw współczynnika przebiegu

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Gdy zgłaszany jest wydatek, a wybraną kategorią wydatku jest **Milowy**, kwota dla tej linii wydatku jest obliczana zgodnie z *stawką za kilometr*. Kwota ta jest określana na podstawie zdefiniowanych poziomów stawek milowych lub, jeśli nie ma zdefiniowanych poziomów stawek milowych, na podstawie standardowej stawki milowej. 

Poziomy stawek milowych można ustawić przechodząc do **Zarządzanie wydatkami** > **Ustawienia** > **Ogólne** > **Kategorie wydatków** > **Milowy** > **Ustawienia kategorii**.

Po aktualizacji do wersji 10.0.18, jeśli Twoja organizacja korzysta z kategorii wydatków na kilometry, rozważ włączenie funkcji mil po zapoznaniu się z poniższymi zmianami projektowymi. 

Nowy wygląd poziomów stawek milowych wpływa na sposób przetwarzania wartości w polu **Ilość**. Przed wydaniem wersji 10.0.18, wartość w polu **Ilość** była uważana za dolną granicę. Gdy akumulacja przekraczała tę wartość, stosowano odpowiednią stawkę.  Od wersji 10.0.18 wartość w polu **Ilość** jest uważana za górną granicę. Odpowiednia stawka jest stosowana, gdy kumulacja przebiegu jest mniejsza niż wartość w polu **Ilość**.  Nowy model poziomów milowych zapewnia spójność pomiędzy poziomami milowymi i lepszą użyteczność.   

Wszystkie zatwierdzone raporty wydatków zostaną przeliczone podczas księgowania zgodnie z nowym wzorem.

## <a name="example"></a>Przykład
 
### <a name="before-version-10018"></a>Przed wersją 10.0.18
W przypadku dwóch poziomów stawek milowych, pole **Ilość** w każdym poziomie oznacza dolny limit kilometrów. Obecnie poziom 1 ma wartość zero (0) i stawkę 0,45, a poziom 2 ma wartość 1000 i stawkę 0,25. Jeśli skumulowana liczba mil lub kilometrów przekracza wartość w polu, używana jest odpowiednia stawka. Jeśli nie ma linii z zerową ilością, system używa stawki kilometrowej, która jest zdefiniowana w Zarządzaniu wydatkami. 
 
Jeśli pracownik złoży raport wydatków z 1500 milami, dwie linie milowe na zaksięgowanym raporcie wydatków wyniosłyby: 1000 (stawka 0,45) + 500 (stawka 0,25) = 575,00.

### <a name="after-version-10018"></a>Po wersji 10.0.18
W wersji 10.0.18 pole **Ilość** w każdej warstwie reprezentuje górną granicę warstwy. Obecnie poziom 1 ma wartość zero 999 i stawkę 0,45, a poziom 2 ma wartość 999 999 999,00 i stawkę 0,25. Jeśli skumulowana liczba mil lub kilometrów przekracza wartość w polu **Ilość**, używana jest odpowiednia stawka. Jeśli wszystkie górne limity zostaną przekroczone, system stosuje stawkę kilometrażową zdefiniowaną w Zarządzaniu wydatkami. 
 
Aby poprawnie obliczyć ten sam scenariusz, należy zmienić ustawienie poziomów dokładności. Pole **Ilość** w warstwie pierwszej ma wartość 999,00, a w warstwie drugiej 999 999 999,00. Jeśli pracownik przekroczy łączną ilość mil lub kilometrów na poziomie pierwszym, system stosuje stawkę kilometrową, która jest zdefiniowana w Zarządzaniu wydatkami. 
  
Jeśli pracownik złoży raport wydatków z 1,500 milami, dwie linie milowe na zaksięgowanym raporcie wydatków wyniosłyby: 1000 (stawka 0,45) + 500 (stawka 0,25) = 575

## <a name="enable-the-mileage-amount-calculation-for-multiple-mileage-tiers-with-same-rate-feature"></a>Włącz obliczanie kwoty kilometrowej dla wielu poziomów kilometrowych z tą samą stawką

Funkcja **Obliczanie kwoty kilometrowej dla wielu poziomów kilometrowych z tą samą stawką** usprawnia obliczanie stawek kilometrowych. Wykonaj następujące kroki, aby włączyć tę funkcję.

1. Wybierz kolejno pozycje **Obszary robocze** > **Zarządzanie funkcjami**. 
2. Na liście odszukaj i wybierz **Obliczanie kwoty kilometra dla wielu poziomów kilometrowych z tą samą stawką**, a następnie wybierz **Włącz teraz**.

Po włączeniu funkcji należy zresetować poziomy milowe, aby prawidłowo odzwierciedlały wartość pola **Ilość**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
