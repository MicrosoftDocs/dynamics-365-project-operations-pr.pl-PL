---
title: Ustawianie zasad dotyczących wydatków
description: W przypadku wprowadzania i przesyłania raportów o wydatkach i wniosków wyjazdowych można zdefiniować w Microsoft Dynamics 365 Finance zasady dotyczące kosztów, których pracownicy muszą przestrzegać.
author: suvaidya
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 050e19016edac53ef22764d227d4ef96d89ba298287b10416febbb55bb00973a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005944"
---
# <a name="set-up-expense-policies"></a>Ustawianie zasad dotyczących wydatków

W przypadku wprowadzania i przesyłania raportów o wydatkach i wniosków wyjazdowych można zdefiniować zasady, których pracownicy muszą przestrzegać.         
Wprowadzenie w życie zasad dotyczących kosztów może pomóc w skutecznym zarządzaniu wydatkami.         

Można na przykład ustawić zasadę dotyczącą wydatków na hotele w Nowym Jorku, która stwierdza, że koszty na dzień nie mogą być większe niż 250 USD.       
Jeśli pracownik złoży raport o wydatkach lub zapotrzebowanie wyjazdowe, gdzie koszt pokoju przekroczy tę kwotę, system wyświetli        
użytkownikowi informację o zasadzie i o przekroczeniu kwoty wydatkowej. Użytkownik może skonfigurować wiadomość wyświetlaną użytkownikowi podczas        
określania zasady.      
        
Możesz korzystać z trzech typów zasad:         
        
- Ostrzeżenie — zezwala pracownikowi na przesyłanie raportu z wydatków lub przejazdu na podróż, ale wydatek będzie zaznaczony dla wszystkich osób zatwierdzających i        
  na potrzeby późniejszego raportowania.        

- Błąd — wymaga, aby pracownik poprawił koszty w celu zapewnienia zgodności z zasadami przed przesłaniem raportu z wydatków lub wniosku wyjazdowego.       
 
 - Uzasadnienie — wymaga, aby pracownik lub kierownik wprowadził uzasadnienie przekroczenia kwoty zasady przed przesłaniem raportu z wydatków lub wniosku wyjazdowego.        

## <a name="policy-tips"></a>Podpowiedzi dot. zasad
Oto kilka sugestii, które mogą pomóc podczas tworzenia nowych zasad zarządzania wydatkami. 
* Zasady wchodzą w życie z datą utworzenia. Oznacza to, że zasada nie będzie obowiązywała co do wydatków, które powstały przed utworzeniem zasady. Jeśli na przykład tworzysz nową zasadę na dziś, aby wymusić maksymalne koszty posiłku w wysokości 50 USD, wówczas wszelkie istniejące koszty wprowadzone wczoraj nie będą sprawdzane względem tej zasady.
* Tworząc zasadę dla kategorii wydatków, która może być wyświetlona w ramach listy elementów, należy rozważyć dodanie warunku dotyczącego typu wiersza wydatku. Niektóre zasady, takie jak wymaganie przyjęcia paragonu, mogą nie być zrozumiałe dla wyszczególnionych wierszy i powinny być stosowane tylko w wierszu nagłówka lub w wierszu niewyszczególnionym. 
* Reguły zarządzania wydatkami są domyślnie oceniane względem encji źródłowej. Zamiast tego, w przypadku scenariuszy międzyfirmowych można skonfigurować zasadę, która będzie oceniana względem encji docelowej (encji pożyczanej). Aby uruchomić zasady w odniesieniu do encji docelowej, należy włączyć funkcję „Oceniaj zasadę dotyczącą kosztów względem pożyczonej encji firmy” w obszarze roboczym **Zarządzanie funkcjami**.

## <a name="when-to-evaluate-policies"></a>Kiedy oceniać przestrzeganie zasad

W ramach parametrów zarządzania wydatkami można wybrać opcję oceny pod kątem przestrzegania zasad dotyczących wydatków na: podczas zapisywania wiersza lub podczas przesyłania raportu z wydatków. W przypadku wybrania opcji oceny w trakcie zapisywania wiersza użytkownicy będą wcześniej widzieli, co należy wykonać, aby wypełnić cały raport. Można także opóźnić ocenę przez zasadę i oszczędzić czas przeprowadzając weryfikację na samym końcu, przed przesłaniem do przepływu pracy.


[!INCLUDE[footer-include](../includes/footer-banner.md)]