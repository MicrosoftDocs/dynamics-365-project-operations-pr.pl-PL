---
title: Błąd niezgodności walut
description: Ten temat zawiera informacje rozwiązywania problemów w przypadku błędu niezgodności walut, który występuje podczas zapisywania określonych typów rekordów.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 52e33ad3728e1a393e8c7e3ca4e0a4b506d0b774
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903503"
---
# <a name="currency-mismatch-error"></a>Błąd niezgodności walut 

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Podczas zapisywania projektu, kontraktu, oferty lub zasobu, który można zarezerwować możesz zobaczyć następujący błąd: **Waluta, której właścicielem jest firma, nie jest zgodna z walutą jednostki kontraktującej. Aby kontynuować, wybierz inną firmę będącą właścicielem lub inną jednostkę kontraktującą dla kontraktu**. Wynika to z niezgodności między walutą jednostki kontraktującej dla rekordu i walutą, której właścicielem jest firma.


## <a name="resolution"></a>Rozwiązywanie

Aby obejść ten problem, wykonaj następujące czynności:
- Sprawdź walutę jednostki kontraktującej dla tego rekordu. Walutę można wyświetlić, otwierając rekord jednostki organizacyjnej i sprawdzając wartość na karcie **Ogólne** w polu **Waluta**.
- Sprawdź walutę, której właścicielem jest firma. Walutę można wyświetlić, przechodząc do obszaru **Pokrewne** > **Arkusze** w rekordzie firmy. Kliknij dwukrotnie rekord rejestru skojarzony z firmą i sprawdź wartość na karcie **Ogólne** w polu **Waluta rozliczeniowa**.

Jeśli waluta ustawiona w jednostce kontraktującym jest inna niż waluta w rekordzie rejestru, dostosuj konfigurację lub wybierz inne wartości podczas zapisywania rekordu. System wymaga, aby te rekordy były zgodne, aby zapewnić poprawne przepływy fakturowania międzyfirmowego. Aby uzyskać więcej informacji o konfiguracjach międzyfirmowych, zobacz temat [Tworzenie transakcji międzyfirmowych](../../project-accounting/create-intercompany-transactions.md).

Jeśli rekord firmy nie ma skojarzonego rekordu rejestru, oznacza to, że podczas konfigurowania środowiska brakuje konfiguracji. Administrator systemu musi poprawić konfigurację. Administrator systemu musi przejść do obszaru **Konfiguracji podwójnego zapisu**, a następnie zatrzymać i ponownie uruchomić **mapę podwójnego zapisu w rejestrach** z początkową synchronizacją tej mapy oraz z jej wstępnymi wymaganiami. Aby uzyskać więcej informacji, zobacz temat [Wersje mapowania podwójnego zapisu w aplikacji Project Operations](../../environment/resource-dual-write-maps.md).
