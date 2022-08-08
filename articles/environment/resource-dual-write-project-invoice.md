---
title: Integracja faktury projektu
description: W tym artykule przedstawiono informacje dotyczące integracji podwójnego zapisu w aplikacji Project Operations na potrzeby fakturowania klientów.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 61f16ebdbabd6545c09d8d7bd82d99b85dc09975
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029037"
---
# <a name="project-invoice-integration"></a>Integracja faktury projektu

W tym artykule przedstawiono informacje dotyczące integracji podwójnego zapisu w aplikacji Project Operations na potrzeby fakturowania klientów.

W programie Project Operations menedżer projektu zarządza zaległościami w rozliczaniu projektu i tworzy fakturę proforma dla klienta w Microsoft Dataverse. Na podstawie tej faktury proforma klient, pracownik biurowy lub klient projektu tworzy fakturę dostępną dla klienta. Integracja typu podwujny zapis zapewnia synchronizację danych z faktury proforma z aplikacjami finansowymi i operacyjnymi. Po zaksięgowaniu faktury dla klienta system aktualizuje odpowiednie wartości rzeczywiste księgowania dla projektu w Dataverse. Następująca ilustracja przedstawia koncepcję na wysokim poziomie — omówienie tej integracji.

   ![Integracja faktury projektu.](./media/DW5Invoicing.png)

Po zatwierdzeniu faktury proforma przez kierownika projektu w Dataverse informacje nagłówkowe faktury proforma są synchronizowane z aplikacjami finansowymi i operacyjnymi za pomocą mapy tabeli podwójnego zapisu, **Propozycja faktury projektowej V2 (faktury)**. Jest to jednokierunkowa integracja z Dataverse do aplikacji finansowych i operacyjnych. Tworzenie i usuwanie propozycji faktur projektu bezpośrednio w aplikacjach finansowych i operacyjnych nie jest obsługiwane.

Potwierdzenie faktury w Dataverse powoduje również wyzwolenie logiki biznesowej do tworzenia rekordów dotyczących rozliczeń w encji **Wartości rzeczywiste**. Te rekordy są synchronizowane z aplikacjami finansowymi i operacyjnymi przy użyciu mapy tabeli podwójnego zapisu, **wartości rzeczywistych integracji Project Operations (msdynactuals\_).** Aby uzyskać więcej informacji, zobacz [Szacunki projektowe i wartości rzeczywiste](resource-dual-write-estimates-actuals.md). 

Wiersze propozycji faktury projektu są tworzone przez proces okresowy **Tworzenia etapów importowania formularzy**. Ten proces jest oparty na fakturowanych szczegółach wartości rzeczywistych sprzedaży w tabeli **Etapów wartości rzeczywistych**. Aby uzyskać więcej informacji, zobacz temat [Zarządzanie ofertami faktury projektowej ](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
