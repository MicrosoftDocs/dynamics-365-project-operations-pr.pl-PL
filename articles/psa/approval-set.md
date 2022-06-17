---
title: Zestawy zatwierdzeń w rozwiązaniu Project Service Automation
description: W tym artykule przedstawiono informacje na temat zestawu zatwierdzeń, żądań i podzbiorów tych operacji.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 568815967b909d2a5ee9bf40b4fee97e0ad4d295
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927065"
---
# <a name="approval-sets-in-project-service-automation"></a>Zestawy zatwierdzeń w rozwiązaniu Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Zestawy zatwierdzeń grupują żądania zatwierdzenia w mniejsze podzbiory operacji. Takie grupowanie pozwala na przetwarzanie zatwierdzeń w kolejności według Projektu oraz umożliwia ponawianie prób i sekwencjonowanie. Grupowanie poprawia niezawodność i identyfikowalność przetwarzania zatwierdzeń w przypadku dużych ilości zatwierdzeń.

Zestawy zatwierdzeń wskazują ogólny stan przetwarzania powiązanych z nimi rekordów. Po przetworzeniu rekordu zatwierdzenia przy użyciu zestawu zatwierdzeń, rekord zostaje przeniesiony z **Zatwierdzony** do **Zatwierdzony** i zostaje usunięty z zestawu zatwierdzeń. Jeśli zapis nie powiedzie się podczas przekazywania go do zatwierdzenia, zapis pozostaje w statusie **Przesłany**, a zestaw zatwierdzający jest oznaczony jako nieudany. Zestaw zatwierdzający rejestruje komunikat błędu o niepowodzeniu.

## <a name="processing-approvals-and-approval-sets"></a>Przetwarzanie zatwierdzeń i zestawów zatwierdzeń
Zatwierdzenia oczekujące w kolejce do przetwarzania widoczne są w widoku **Opracowywanie zatwierdzeń**. System próbuje przetworzyć wszystkie wpisy wiele razy asynchronicznie, w tym ponowić próbę zatwierdzenia, jeśli poprzednie próby zakończyły się niepowodzeniem.

Pole **Próby zatwierdzenia ogółem** określa ilość prób, które pozostały do przetworzenia zestawu, zanim zostanie on oznaczony jako nieudany.

## <a name="failed-approvals-and-approval-sets"></a>Nieudane zatwierdzenia i zestawy zatwierdzeń
Widok **Nieudane zatwierdzenia** zawiera listę wszystkich zatwierdzeń, które wymagają interwencji użytkownika. Otwórz dzienniki powiązanych zestawów zatwierdzeń, aby zidentyfikować przyczynę niepowodzenia.
Wybranie opcji **Ponów próbę** dodaje wartość do licznika prób zestawu zatwierdzeń, przywraca zestawowi zatwierdzeń status **Przetwarzanie** i próbuje przetworzyć pozostałe rekordy.

## <a name="configure-approval-sets"></a>Konfiguracja zestawów zatwierdzeń

###  <a name="enable-the-approval-sets-feature"></a>Włączanie funkcji Zestawów zatwierdzających
Przed włączeniem funkcji Zestawy zatwierdzeń należy sprawdzić, czy nie są aktualnie przetwarzane żadne zatwierdzenia.

- Przejdź na stronę **Parametry projektu** i wybierz **Kontrola właściwości** > **Włącz nowe zatwierdzenia**.

### <a name="turn-off-the-approval-sets-feature"></a>Wyłączanie funkcji Zestawów zatwierdzających
Przed wyłączeniem funkcji Zestawy zatwierdzeń należy sprawdzić, czy nie są aktualnie przetwarzane żadne zatwierdzenia.

- Przejdź na stronę **Parametry projektu** i wybierz **Kontrola właściwości** > **Wyłącz nowe zatwierdzenia**.

### <a name="configuring-the-asynchronous-threshold"></a>Konfiguracja progu asynchronicznego 
Podczas tworzenia zestawów zatwierdzeń przetwarzanie przechodzi na drugi plan, gdy wybrana liczba rekordów do zatwierdzenia przekroczy wskazany próg. Użyj pola **Próg asynchroniczności**, aby ustalić, czy przetwarzanie zatwierdzeń ma się odbywać synchronicznie czy asynchronicznie.
Prawidłowe wartości:

  - Zero: Wszystkie żądania powinny być przetwarzane asynchronicznie. 
  - Wartość większa od zera: Zatwierdzenia są przetwarzane asynchronicznie tylko wtedy, gdy przesłana liczba zatwierdzeń przekracza tę wartość.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
