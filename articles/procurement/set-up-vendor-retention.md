---
title: Konfigurowanie przechowywania dostawców
description: W tym temacie opisano sposób konfigurowania przechowywania dostawców.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e0cd7669c7d6b916261e2c85cce0f24ff241a075
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583717"
---
# <a name="set-up-vendor-retention"></a>Konfigurowanie przechowywania dostawców

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

W tym temacie podano informacje dotyczące konfigurowania przechowywania dostawców.

## <a name="set-up-a-vendor-retention-account-in-general-ledger"></a>Konfigurowanie konta przechowywania dostawców w księdze głównej

1. W Dynamics 365 Finance przejdź do **Księga główna** > **Konfiguracja księgowania** > **Konta dla transakcji automatycznych**.
2. Dodaj nowy wiersz.
3. W polu **Typ publikowania** wybierz pozycję **Przechowywanie dostawcy**.
4. Wybierz konto główne dla księgowania przechowywania dostawcy.

## <a name="create-vendor-retention-terms"></a>Utwórz postanowienia przechowywania dostawcy

Korzystanie ze strony **Postanowienia przechowywania dostawcy** w celu skonfigurowania i zachowania warunków przechowywania dostawców. Wprowadź procent płatności dla dostawcy, jaki ma być zatrzymany oraz procent poprzednio zatrzymanych kwot, jakie mają być zwolnione. Kwoty na fakturach dostawców są automatycznie zatrzymywane , dopóki kontrakt nie osiągnie określonego stanu wykonania. Po skonfigurowaniu postanowień przechowywania dostawcy można zastosować je do dowolnego projektu, nad którym pracuje dostawca.

1. W rozwiązaniu Finance przejdź do **Zarządzanie projektami i ich księgowanie** > **Konfiguracja** > **Przechowywanie** > **Warunki zatrzymania płatności u dostawcy**.
2. Wybierz opcję **Nowy**, aby dodać nowy warunek zatrzymania dla dostawcy. Wartość w polu **Identyfikator reguły** dla nowego warunku zostanie wprowadzona automatycznie. 
3. W polu **Opis** wprowadź nazwę opisową nowego postanowienia.
4. Na karcie **Warunki** wybierz opcję **Dodaj wiersz**, aby wprowadzić termin przechowywania dostawcy.
5. W polu **Procent dostarczonych jednostek** wprowadź procent ukończenia dla reguły. Stosowne kwoty zostają automatycznie zatrzymane na fakturach od dostawcy do czasu ukończenia etapu projektu odpowiadającego wprowadzonej wartości procentowej. Na przykład po wprowadzeniu wartości 50,00 kwoty zostaną zatrzymane, dopóki projekt nie będzie ukończony w 50%.
6. W polu **Procent do zatrzymania** wprowadź procent kwoty z faktury dostawcy, jaki ma być zatrzymany. Na przykład, jeśli zostanie wprowadzona wartość 10,00, to zatrzymywaniu będzie podlegało 10 procent kwoty na fakturach od dostawcy do momentu, gdy projekt nie osiągnie etapu ukończenia ustawionego w polu **Procent dostarczonych jednostek**.
7. W polu **Procent do zwolnienia** wprowadź procent jakichkolwiek wcześniej zatrzymanych kwot, jaki ma być zwolniony po osiągnięciu określonego poziomu ukończenia projektu.

> [!NOTE]
> Jeśli projekt obejmuje więcej niż jeden kamień milowy dla różnych poziomów ukończenie projektu, wprowadź osobny wiersz warunku zatrzymania płatności dla dostawcy dla każdej reguły zatrzymania. Każdy wiersz może określać inną wartość procentową zatrzymania i inny procent do zwolnienia dla każdego wyznaczonego poziomu ukończenia projektu.

## <a name="set-up-a-vendor-agreement-for-the-project"></a>Konfigurowanie umowy dostawcy dla projektu

Konfigurowanie postawień przechowywania dostawcy, które mają zastosowanie do projektu. Warunki zatrzymania dotyczącego dostawcy są również wyświetlane w zamówieniach zakupu tworzonych dla danego dostawcy.

1. W rozwiązaniu Finance przejdź do opcji **Zarządzanie projektami i ich księgowanie** > **Projekty** > **Wszystkie projekty**. 
2. Wybierz projekt i w okienku akcji wybierz opcje **Grupa projektów** > **Umowy dostawców**.
3. Na stronie **Umowy dostawców** dodaj nowy wiersz.
4. W polu **Kod konta** wybierz jedną z następujących opcji:
   - **Tabela**: warunki zatrzymania dotyczące dostawcy stosuje się do jednego dostawcy.
   - **Grupa**: warunki zatrzymania dotyczące dostawcy stosuje się do wszystkich dostawców w grupie.
   - **Wszyscy**: warunki zatrzymania dotyczące dostawcy stosuje się do wszystkich dostawców.
5. W polu **Dostawca / Grupa dostawców** wybierz dostawcę lub grupę, do których mają mieć zastosowanie warunki zatrzymania. Jeśli wybrano opcję **Wszyscy**, wtedy to pole jest niedostępne.
6. W polu **Postanowienia przechowywania dostawcy** wybierz identyfikator reguły dla postanowień przechowywania, które mają być stosowane względem tego dostawcy.

