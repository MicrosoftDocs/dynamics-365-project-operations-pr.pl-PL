---
title: Omówienie przetwarzania faktur
description: Ten temat zawiera omówienie procesu fakturowania w Project Operations dla scenariuszy opartych na zasobach / braku zapasów.
author: sigitac
manager: Annbe
ms.date: 01/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fbc1519b6cbcf231cfa89df8b7843d11a8904e49
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089283"
---
# <a name="invoicing-process-overview"></a>Omówienie przetwarzania faktur

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Project Operations dla scenariuszy opartych na zasobach / braku zapasów oferują wszechstronne możliwości dostosowane do potrzeb zarówno kierownika projektu, jak i księgowego / księgowego projektu. W procesie fakturowania kierownik projektu zarządza zaległościami rozliczeniowymi projektu, a księgowy / księgowy projektu tworzy zgodny i dokładny dokument faktury skierowany do klienta.

![Diagram przepływu fakturowania](./media/invoicing-flow.png)

Wiersz umowy dotyczącej projektu definiuje metodę fakturowania dla powiązanych transakcji projektu. Gdy kierownik projektu zatwierdzi transakcje dotyczące czasu i wydatków, system rejestruje transakcje w encji **Wartości rzeczywiste** i wysyła informacje do modułu **Zarządzanie projektami i księgowość** w Dynamics 365 Finance. Księgowy projektu następnie przegląda i publikuje rekordy przy użyciu [arkusza integracji aplikacji Project Operations](../project-accounting/project-operations-integration-journal.md). Ten arkusz zawiera ważne szczegóły księgowe dotyczące wartości rzeczywistych projektu, takie jak fakturowanie, grupa podatków, grupa podatków pozycji fakturowania i wymiary finansowe.

Menedżer projektu może przeglądać niezafakturowane transakcje sprzedaży przy użyciu metody rozliczania za czas i materiały w [Zaległość rozliczania czasu i materiałów](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) oraz fakturowania po stałej cenie w [punktach kontrolnych z ustalonymi cenami](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Te widoki umożliwiają filtrowanie i wybieranie transakcji, które mają zostać uwzględnione w następnym cyklu rozliczeniowym, a następnie oznaczanie ich jako **Przygotowane do fakturowania**.

Można ręcznie [utworzyć fakturę proforma](../proforma-invoicing/create-manual-proforma-invoice.md) lub skorzystać z [procesu okresowego](../proforma-invoicing/configure-automated-invoice-creation.md). Menedżer projektu może w razie potrzeby [dostosować roboczą fakturę proforma](../proforma-invoicing/manage-proforma-invoice.md), a następnie potwierdzić ją.

Potwierdzona faktura proforma jest wysyłana do modułu **Zarządzanie projektami i księgowanie** w Finance. Księgowy projektu formatuje i aktualizuje propozycję faktury za projekt, a następnie księguje i drukuje dokument. Zaksięgowane faktury projektu są rejestrowane w księdze głównej oraz w podksięgach Klient i Projekt.
