---
title: Definiowanie zasad wydatków
description: W przypadku wprowadzania i przesyłania raportów o wydatkach i wniosków wyjazdowych można zdefiniować zasady dotyczące kosztów, których pracownicy muszą przestrzegać.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c55cec132649daf9ee08ea4d8db3668860247934
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128431"
---
# <a name="define-expense-policies"></a>Definiowanie zasad wydatków

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

W przypadku wprowadzania i przesyłania raportów o wydatkach i wniosków wyjazdowych można zdefiniować zasady, których pracownicy muszą przestrzegać.         
Wprowadzenie w życie zasad dotyczących kosztów może pomóc w skutecznym zarządzaniu wydatkami.         

Można na przykład ustawić zasadę dotyczącą wydatków na hotele w Nowym Jorku, która stwierdza, że koszty na dzień nie mogą być większe niż 250 USD.       
Jeśli pracownik złoży raport o wydatkach lub zapotrzebowanie wyjazdowe, gdzie koszt pokoju przekroczy tę kwotę, system wyświetli         
użytkownikowi informację o zasadzie i o przekroczeniu kwoty wydatkowej. Użytkownik może skonfigurować wiadomość wyświetlaną użytkownikowi podczas        
określania zasady.      
        
Możesz korzystać z trzech typów zasad:         
        
- **Ostrzeżenie** : Zezwala pracownikowi na przesyłanie raportu z wydatków lub przejazdu na podróż, ale wydatek będzie zaznaczony dla wszystkich osób zatwierdzających i         
  na potrzeby późniejszego raportowania.        

- **Błąd**: wymaga, aby pracownik poprawił koszty w celu zapewnienia zgodności z zasadami przed przesłaniem raportu z wydatków lub wniosku wyjazdowego.        
 
 - **Uzasadnienie**: wymaga, aby pracownik lub kierownik wprowadził uzasadnienie przekroczenia kwoty zasady przed przesłaniem raportu z wydatków lub wniosku wyjazdowego.        

## <a name="policy-tips"></a>Podpowiedzi dot. zasad
Oto kilka sugestii, które mogą pomóc podczas tworzenia nowych zasad zarządzania wydatkami: 

- Zasady wchodzą w życie z datą utworzenia. Oznacza to, że zasady nie będą obowiązywały co do wydatków, które powstały przed utworzeniem zasady. Załóżmy na przykład, że użytkownik utworzył nowe zasady dziś w celu wyegzekwowania maksymalnego kosztu posiłku w wys. 50 USD. Wszelkie istniejące koszty wprowadzone wczoraj nie będą sprawdzane względem tej zasady.
- Tworząc zasadę dla kategorii wydatków, która może być wyświetlona w ramach listy elementów, należy rozważyć dodanie warunku dotyczącego typu wiersza wydatku. Niektóre zasady, na przykład wymaganie paragonu, mogą nie mieć zastosowania względem list elementów. W tym przypadku zasada ma zastosowanie tylko względem wiersza nagłówka lub wiersza bez pozycji. 
- Reguły zarządzania wydatkami są domyślnie oceniane względem encji źródłowej. Zamiast tego, w przypadku scenariuszy międzyfirmowych można skonfigurować zasadę, która będzie oceniana względem encji docelowej (encji pożyczanej). Aby uruchomić zasady w odniesieniu do encji docelowej, należy włączyć funkcję **Oceniaj zasadę dotyczącą kosztów względem pożyczonej encji firmy** w obszarze roboczym **Zarządzanie funkcjami**.

## <a name="when-to-evaluate-policies"></a>Kiedy oceniać przestrzeganie zasad

W ramach parametrów zarządzania wydatkami można wybrać opcję oceny pod kątem przestrzegania zasad dotyczących wydatków na: podczas zapisywania wiersza lub podczas przesyłania raportu z wydatków. W przypadku wybrania opcji oceny w trakcie zapisywania wiersza użytkownicy będą wcześniej widzieli, co należy wykonać, aby wypełnić cały raport. Można także opóźnić ocenę przez zasadę i oszczędzić czas przeprowadzając weryfikację na samym końcu, przed przesłaniem do przepływu pracy.


[!INCLUDE[footer-include](../includes/footer-banner.md)]