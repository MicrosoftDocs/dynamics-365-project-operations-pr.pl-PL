---
title: Integracja faktury projektu
description: Ten temat zawiera informacje na temat integracji funkcji podwójnego zapisu w programie Project Operations na potrzeby fakturowania klientów.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7407c98aad79806dcbaf25e81ff3e08397b41ffe
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996579"
---
# <a name="project-invoice-integration"></a>Integracja faktury projektu

Ten temat zawiera informacje na temat integracji funkcji podwójnego zapisu w programie Project Operations na potrzeby fakturowania klientów.

W programie Project Operations menedżer projektu zarządza zaległościami w rozliczaniu projektu i tworzy fakturę proforma dla klienta w Microsoft Dataverse. Na podstawie tej faktury proforma klient, pracownik biurowy lub klient projektu tworzy fakturę dostępną dla klienta. Dzięki integracji podwójnego zapisu szczegóły faktury proforma są synchronizowane z aplikacjami Finance and Operations. Po zaksięgowaniu faktury dla klienta system aktualizuje odpowiednie wartości rzeczywiste księgowania dla projektu w Dataverse. Następująca ilustracja przedstawia koncepcję na wysokim poziomie — omówienie tej integracji.

   ![Integracja faktury projektu](./media/DW5Invoicing.png)

Po potwierdzenia przez menedżera projektu faktury proforma w Dataverse, informacje nagłówka faktury proforma są synchronizowane z aplikacjami Finance and Operations, używając podwójnego zapisu mapy tabeli, czyli **Propozycji faktury projektu V2 (faktury)**. Jest to jednokierunkowa integracja — Dataverse z aplikacjami Finance and Operations. Tworzenie lub usuwanie ofert faktur projektów bezpośrednio w aplikacjach Finance and Operations nie jest obsługiwane.

Potwierdzenie faktury w Dataverse powoduje również wyzwolenie logiki biznesowej do tworzenia rekordów dotyczących rozliczeń w encji **Wartości rzeczywiste**. Te wartości rzeczywiste są synchronizowane z aplikacjami Finance and Operations przy użyciu podwójnego zapisu mapowania tabeli w ramach **Wartości rzeczywistych Project Operations (msdyn\_actuals)** dla późniejszego księgowania. Aby uzyskać więcej informacji, zobacz [Szacunki projektowe i wartości rzeczywiste](resource-dual-write-estimates-actuals.md). 

Wiersze propozycji faktury projektu są tworzone przez proces okresowy **Tworzenia etapów importowania formularzy**. Ten proces jest oparty na fakturowanych szczegółach wartości rzeczywistych sprzedaży w tabeli **Etapów wartości rzeczywistych**. Aby uzyskać więcej informacji, zobacz temat [Zarządzanie ofertami faktury projektowej ](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
