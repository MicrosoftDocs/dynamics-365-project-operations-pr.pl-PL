---
title: Omówienie przetwarzania faktur
description: Ten temat zawiera omówienie procesu fakturowania w Project Operations dla scenariuszy opartych na zasobach / braku zapasów.
author: sigitac
ms.date: 01/29/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 0328d5321909bcc17754da4e19d7652b77a665d5
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582723"
---
# <a name="invoicing-process-overview"></a>Omówienie przetwarzania faktur

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Project Operations dla scenariuszy opartych na zasobach / braku zapasów oferują wszechstronne możliwości dostosowane do potrzeb zarówno kierownika projektu, jak i księgowego / księgowego projektu. W procesie fakturowania kierownik projektu zarządza zaległościami rozliczeniowymi projektu, a księgowy / księgowy projektu tworzy zgodny i dokładny dokument faktury skierowany do klienta.

![Diagram przepływu fakturowania.](./media/invoicing-flow.png)

Wiersz umowy dotyczącej projektu definiuje metodę fakturowania dla powiązanych transakcji projektu. Gdy menedżer projektu zatwierdzi transakcje dotyczące czasu i wydatków, system rejestruje transakcje w encji **Wartości rzeczywiste projektu** i wysyła te informacje do modułu **Zarządzanie projektami oraz moduł księgowy** w programie Dynamics 365 Finance. Księgowy projektu następnie przegląda i publikuje rekordy przy użyciu [arkusza integracji aplikacji Project Operations](../project-accounting/project-operations-integration-journal.md). Ten arkusz zawiera ważne szczegóły księgowe dotyczące wartości rzeczywistych projektu, takie jak fakturowanie, grupa podatków, grupa podatków pozycji fakturowania i wymiary finansowe.

Menedżer projektu może przeglądać niezafakturowane transakcje sprzedaży przy użyciu metody rozliczania za czas i materiały w [Zaległość rozliczania czasu i materiałów](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) oraz fakturowania po stałej cenie w [punktach kontrolnych z ustalonymi cenami](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Te widoki umożliwiają filtrowanie i wybieranie transakcji, które mają zostać uwzględnione w następnym cyklu rozliczeniowym, a następnie oznaczanie ich jako **Przygotowane do fakturowania**.

Można ręcznie [utworzyć fakturę proforma](../proforma-invoicing/create-manual-proforma-invoice.md) lub skorzystać z [procesu okresowego](../proforma-invoicing/configure-automated-invoice-creation.md). Menedżer projektu może w razie potrzeby [dostosować roboczą fakturę proforma](../proforma-invoicing/manage-proforma-invoice.md), a następnie potwierdzić ją.

Potwierdzona faktura proforma jest wysyłana do modułu **Zarządzanie projektami i księgowanie** w Finance. Księgowy projektu formatuje i aktualizuje propozycję faktury za projekt, a następnie księguje i drukuje dokument. Zaksięgowane faktury projektu są rejestrowane w księdze głównej oraz w podksięgach Klient i Projekt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]