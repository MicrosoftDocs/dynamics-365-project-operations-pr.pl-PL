---
title: Tworzenie i stosowanie warunków zatrzymania płatności u dostawcy
description: Ten artykuł zawiera informacje dotyczące konfigurowania i obsługiwania warunków zatrzymania płatności dostawcy.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 2cd18375d93e503ac532cb3839c691231ea46681
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916761"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Tworzenie i stosowanie warunków zatrzymania płatności u dostawcy

[!include [banner](../includes/banner.md)] 

Konfigurowanie warunków zatrzymania płatności u dostawcy w ramach projektu jest przydatne w momencie, gdy organizacja chce zachować część płatności dokonanych w ramach danego dostawcy. Jeśli na przykład użytkownik chce wstrzymać płatność dla dostawcy do momentu, aż dostarczany produkt spełniać będzie oczekiwania użytkownika. Warunki zatrzymania płatności dla dostawcy mogą być określone podczas negocjowania kontraktu dostawcy.

## <a name="create-vendor-payment-retention-terms"></a>Tworzenie warunków zatrzymania płatności dla dostawcy

Istnieje możliwość wprowadzenia wartości procentowej płatności dla dostawcy na potrzeby zatrzymania oraz wartości procentowej poprzednio zatrzymanych kwot, które mają zostać zwolnione. Kwoty na fakturach dostawców są automatycznie zatrzymywane , dopóki kontrakt nie osiągnie określonego stanu wykonania. Po skonfigurowaniu warunków zatrzymania można stosować je do wszystkich projektów danego dostawcy.

Wykonaj poniższe kroki, aby skonfigurować warunki zatrzymywania płatności dostawcy i zarządzać nimi. 

1. Przejdź do obszaru **Zarządzanie projektami i księgowanie** > **Zatrzymywanie** > **Warunki zatrzymania płatności u dostawcy**.
2. Wybierz opcję **Nowy**, aby dodać nowy warunek zatrzymania dla dostawcy. Wartość **Identyfikatora reguły** dla nowego terminu jest wprowadzana automatycznie. 
3. Wprowadź krótki opis w polu **Opis**, a następnie na skróconej karcie **Warunki** wybierz opcję **Dodaj wiersz** w celu wprowadzenia wartości terminów dla następujących kryteriów:

   - **Procent dostarczonych jednostek**: wprowadź wartość procentową wykonania. Kwoty na fakturach dostawców są automatycznie zatrzymywane , dopóki kontrakt nie będzie równy określonemu stanowi procentowego wykonania. Na przykład po wprowadzeniu wartości 50,00 kwoty zostaną zatrzymane, dopóki projekt nie będzie ukończony w 50%.
   - **Procent do zatrzymania**: wprowadź wartość procentową kwoty faktury od dostawcy, która ma zostać zatrzymana. Na przykład wprowadzenie wartości 10,00 oznacza, że 10 procent kwoty na fakturze zostanie zatrzymane do momentu, kiedy projekt osiągnie wartość procentową wykonania ustaloną w polu **Procent dostarczonych jednostek**.
   - **Procent do zwolnienia**: wybierz opcję **Dodaj wiersz**, aby wprowadzić wartość procentową wszelkich poprzednio zatrzymywanych kwot do zwolnienia dla wybranego poziomu wykonania projektu.

> [!NOTE]
> Jeśli na różnych poziomach wykonania projektu znajduje się więcej niż jeden punkt kontrolny, dla każdej reguły zatrzymywania wprowadź osobny wiersz warunku zatrzymania. Każdy wiersz może określać inny procent zatrzymania i inny procent zwolnienia dla każdego określonego poziomu wykonania projektu.

Po utworzeniu warunków zatrzymania dla dostawcy, można stosować je do wszystkich warunków danego dostawcy.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Stosowanie warunków zatrzymania do projektu

1. Przejdź do **Zarządzania projektami i księgowania** > **Projekty** > **Wszystkie projekty** i otwórz projekt na stronie listy projektów.
2. Na skróconej karcie **Kontrakty z dostawcami** wybierz pozycję **Dodaj wiersz**.
3. W polu **Wyświetlany kod konta** wybierz jedną z następujących opcji: 

   - **Tabela**: warunki zatrzymania dotyczące dostawcy stosuje się do jednego dostawcy.
   - **Grupa**: warunki zatrzymania dotyczące dostawcy stosuje się do wszystkich dostawców w grupie.
   - **Wszyscy**: warunki zatrzymania dotyczące dostawcy stosuje się do wszystkich dostawców.

4. W polu **Dostawca / Grupa dostawców** wybierz dostawcę lub grupę, do których mają mieć zastosowanie warunki zatrzymania. Jeśli wybrano opcję **Wszyscy**, wtedy to pole jest niedostępne.
5. W polu **Warunki zatrzymania dla dostawcy** wybierz warunki zatrzymania utworzone w poprzedniej procedurze.
6. Jeśli w projekcie zdefiniowano również warunki płatności dla dostawcy po uiszczonej opłacie (PWP) dla danego dostawcy, wprowadź procent wartości progowej dla projektu w polu **Procent wartości progowej PWP**.

Warunki zatrzymania dotyczącego dostawcy są również wyświetlane w zamówieniach zakupu tworzonych dla danego dostawcy.


[!INCLUDE[footer-include](../includes/footer-banner.md)]