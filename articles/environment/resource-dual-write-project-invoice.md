---
title: Integracja faktury projektu
description: Ten temat zawiera informacje na temat integracji funkcji podwójnego zapisu w programie Project Operations na potrzeby fakturowania klientów.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 102a7cdba467a2071119c5b32d2e75e48170c783
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955807"
---
# <a name="project-invoice-integration"></a>Integracja faktury projektu

Ten temat zawiera informacje na temat integracji funkcji podwójnego zapisu w programie Project Operations na potrzeby fakturowania klientów.

W programie Project Operations menedżer projektu zarządza zaległościami w rozliczaniu projektu i tworzy fakturę proforma dla klienta w Microsoft Dataverse. Na podstawie tej faktury proforma klient, pracownik biurowy lub klient projektu tworzy fakturę dostępną dla klienta. Dzięki integracji podwójnego zapisu szczegóły faktury proforma są synchronizowane z aplikacjami Finance and Operations. Po zaksięgowaniu faktury dla klienta system aktualizuje odpowiednie wartości rzeczywiste księgowania dla projektu w Dataverse. Następująca ilustracja przedstawia koncepcję na wysokim poziomie — omówienie tej integracji.

   ![Integracja faktury projektu](./media/DW5Invoicing.png)

Po potwierdzenia przez menedżera projektu faktury proforma w Dataverse, informacje nagłówka faktury proforma są synchronizowane z aplikacjami Finance and Operations, używając podwójnego zapisu mapy tabeli, czyli **Propozycji faktury projektu V2 (faktury)**. Jest to jednokierunkowa integracja — Dataverse z aplikacjami Finance and Operations. Tworzenie lub usuwanie ofert faktur projektów bezpośrednio w aplikacjach Finance and Operations nie jest obsługiwane.

Potwierdzenie faktury w Dataverse powoduje również wyzwolenie logiki biznesowej do tworzenia rekordów dotyczących rozliczeń w encji **Wartości rzeczywiste**. Te wartości rzeczywiste są synchronizowane z aplikacjami Finance and Operations przy użyciu podwójnego zapisu mapowania tabeli w ramach **Wartości rzeczywistych Project Operations (msdyn\_actuals)** dla późniejszego księgowania. Aby uzyskać więcej informacji, zobacz [Szacunki projektowe i wartości rzeczywiste](resource-dual-write-estimates-actuals.md). 

Wiersze propozycji faktury projektu są tworzone przez proces okresowy **Tworzenia etapów importowania formularzy**. Ten proces jest oparty na fakturowanych szczegółach wartości rzeczywistych sprzedaży w tabeli **Etapów wartości rzeczywistych**. Aby uzyskać więcej informacji, zobacz temat [Zarządzanie ofertami faktury projektowej ](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
