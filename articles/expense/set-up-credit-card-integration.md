---
title: Konfigurowanie integracji z kartą kredytową
description: W tym temacie wyjaśniono, jak pracować z transakcjami kartą kredytową związanymi z wydatkami.
author: suvaidya
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3555e894e206c2aafb30b0df1e52efadd69b0713
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001842"
---
# <a name="set-up-credit-card-integration"></a>Konfigurowanie integracji z kartą kredytową

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Transakcje związane z kartą kredytową związane z wydatkami można skonfigurować w taki sposób, aby były automatycznie importowane w harmonogramie cyklicznym. Można także importować transakcje ręcznie, zależnie od potrzeb. Transakcje kartą kredytową są importowane za pośrednictwem obiektu danych o nazwie transakcje kartą kredytową.

## <a name="import-credit-card-transactions"></a>Importowanie transakcji kartą kredytową

Aby zaimportować transakcje kartą kredytową, wykonaj następujące kroki:

1. Na stronie **Transakcje kartą kredytową** wybierz opcję **Import transakcji**. W przypadku korzystania z zarządzania danymi po raz pierwszy, przed kontynuowaniem system musi zaktualizować listę encji danych.
2. W polu **Nazwa** wprowadź unikatowy opis zadania importu.
3. W polu **Format danych źródłowych** wybierz format pliku zawierającego transakcje kartą kredytową do zaimportowania.
4. Wybierz opcję **Prześlij**, a następnie znajdź i wybierz plik do zaimportowania.
5. Po przekazaniu pliku należy sprawdzić poprawność mapowania pliku transakcji kartą kredytową i kolumnę obiektu dane transakcji kartą kredytową, wybierając łącze **Mapa widoku** na kafelku. Jeśli występują błędy mapowania lub konieczne będzie jego zmodyfikowanie, można to zrobić na karcie **Wizualizacja** lub **Szczegóły mapowania**.
6. W celu zautomatyzowania transakcji kartą kredytową wybierz opcję **Utwórz cykliczne zadanie danych**. Następnie można ustawić cykliczność definiującą częstotliwość importowania transakcji kartą kredytową. Kiedy skończysz, wybierz **OK**.
7. Aby zaimportować wybrany plik teraz, wybierz pozycję **Importuj**.
8. Jeśli podczas importu wystąpią błędy, możesz przejrzeć dziennik wykonywania lub dane przemieszczania, aby zobaczyć błędy, które należy naprawić, aby zapewnić pomyślny import.

> [!NOTE]
> Jeśli chcesz zaimportować więcej niż jeden format pliku, musisz utworzyć osobne zadania importu dla każdego typu formatu.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Ponowne przypisywanie transakcji kartą kredytową dla zakończonych pracowników

Po zakończeniu rekordu pracownika, jego konto Active Directory Domain Services (AD DS) jest wyłączane. Jednakże mogą istnieć aktywne transakcje kartą, które nadal trzeba rozliczyć lub zwrócić. Na stronie **Transakcje kartą kredytową** możesz ponownie przypisać pracownika do dowolnej transakcji kartą kredytową, w przypadku której powiązany pracownik został zwolniony.

Wybierz jedną lub kilka transakcji kartą kredytową, a następnie wybierz opcję **Ponowne przypisanie transakcji**. Następnie można wybrać innego pracownika, do którego ma zostać przypisana transakcja kartą kredytową. Po zmianie przypisania transakcji kartą kredytową można ją wybrać z poziomu raportu z wydatków i zapłacić korzystając z normalnego procesu zwrotu kosztu wydatków.

## <a name="delete-credit-card-transactions"></a>Usuwanie transakcji kartą kredytową 

Czasami po zaimportowaniu transakcji kartą kredytową niektóre transakcje mogą wymagać usunięcia. Może tak być, jeśli transakcje są duplikatami lub ponieważ dane mogą być niedokładne. Administratorzy mogą używać funkcji **Usuwanie transakcji kart kredytowych**, aby wybierać i usuwać transakcje kartą kredytową, które **nie są dołączone** do raportu wydatków. 

1. Przejdź do **Zadania okresowe** > **Usuń transakcje kartą kredytową**.
2. Wybierz opcję **Filtruj** i podaj informacje służące do identyfikacji uwzględnianych rekordów.
3. Wybierz **OK**, aby usunąć rekordy. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
