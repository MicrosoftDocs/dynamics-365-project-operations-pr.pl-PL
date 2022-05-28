---
title: Błąd niezgodności walut
description: Ten temat zawiera informacje rozwiązywania problemów w przypadku błędu niezgodności walut, który występuje podczas zapisywania określonych typów rekordów.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5bb54a121f0dc22f1c0ea88ada9c922c1d4c6544
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589761"
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
