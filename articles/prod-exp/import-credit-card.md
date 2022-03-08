---
title: Importowanie i zarządzanie transakcjami kartami kredytowymi
description: W tym temat przedstawiono sposób importu i utrzymywania transakcji kartą kredytową związanych z wydatkami. Te transakcje można skonfigurować w taki sposób, aby były automatycznie importowane w harmonogramie cyklicznym, lub mogą też w razie potrzeby zostać zaimportowane ręcznie.
author: KimANelson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: c3a53d2ae4eae411364aaf68ac806b55335c75d4870a24715954ccae327f4358
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995864"
---
# <a name="import-and-maintain-credit-card-transactions"></a>Importowanie i zarządzanie transakcjami kartami kredytowymi

Transakcje związane z kartą kredytową związane z wydatkami można skonfigurować w taki sposób, aby były automatycznie importowane w harmonogramie cyklicznym. Można także importować transakcje ręcznie, zależnie od potrzeb. Transakcje kartą kredytową są importowane za pośrednictwem obiektu danych o nazwie transakcje kartą kredytową.

Aby uzyskać więcej informacji o encjach danych, zobacz [Encje danych](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).

## <a name="import-credit-card-transactions"></a>Importowanie transakcji kartą kredytową

1. Na stronie **Transakcje kartą kredytową** wybierz opcję **Import transakcji**. W przypadku korzystania z zarządzania danymi po raz pierwszy, przed kontynuowaniem system musi zaktualizować listę encji danych.
2. W polu **Nazwa** wprowadź unikatowy opis zadania importu.
3. W polu **Format danych źródłowych** wybierz format pliku zawierającego transakcje kartą kredytową do zaimportowania.
4. Wybierz opcję **Prześlij**, a następnie znajdź i wybierz plik do zaimportowania.
5. Po przekazaniu pliku należy sprawdzić poprawność mapowania pliku transakcji kartą kredytową i kolumnę obiektu dane transakcji kartą kredytową, wybierając łącze **Mapa widoku** na kafelku. Jeśli występują błędy mapowania lub konieczne będzie jego zmodyfikowanie, można to zrobić na karcie **Wizualizacja** lub **Szczegóły mapowania**.
6. W celu zautomatyzowania transakcji kartą kredytową wybierz opcję **Utwórz cykliczne zadanie danych**. Następnie można ustawić cykliczność definiującą częstotliwość importowania transakcji kartą kredytową. Kiedy skończysz, wybierz **OK**.
7. Aby zaimportować wybrany plik teraz, wybierz pozycję **Importuj**.
8. Jeśli podczas importowania wystąpią błędy, można wyświetlić dziennik wykonywania lub dane przemieszczania, aby zobaczyć błędy, które należy rozwiązać w celu zagwarantowania pomyślnego zaimportowania.

> [!NOTE]
> Jeśli zachodzi konieczność zaimportowania więcej niż jednego formatu pliku, należy utworzyć osobne zadania importu dla każdego typu formatu.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Ponowne przypisywanie transakcji kartą kredytową dla zakończonych pracowników

Po zakończeniu rekordu pracownika, jego konto Active Directory Domain Services (AD DS) jest wyłączane. Jednakże mogą istnieć aktywne transakcje kartą, które nadal trzeba rozliczyć lub zwrócić. Na stronie **Transakcji kartą kredytową** można przypisać pracownika do dowolnej transakcji kartą kredytową, nawet pracownika, który już nie jest zatrudniony.

Wybierz jedną lub kilka transakcji kartą kredytową, a następnie wybierz opcję **Ponowne przypisanie transakcji**. Następnie można wybrać innego pracownika, do którego ma zostać przypisana transakcja kartą kredytową. Po zmianie przypisania transakcji kartą kredytową można ją wybrać z poziomu raportu z wydatków i zapłacić korzystając z normalnego procesu zwrotu kosztu wydatków.


[!INCLUDE[footer-include](../includes/footer-banner.md)]