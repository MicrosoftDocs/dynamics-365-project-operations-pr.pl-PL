---
title: Co nowego w lutym 2022 r. — Wdrożenie Project Operations lite
description: Ten artykuł zawiera informacje o aktualizacjach jakości, które są dostępne w wydaniu z lutego 2022 r. wdrożenia uproszczonego Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1203faa2dd53a8fb82cff0857a1725426ebff19a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922833"
---
# <a name="whats-new-february-2022---project-operations-lite-deployment"></a>Co nowego w lutym 2022 r. — Wdrożenie Project Operations lite

_Zastosowane do: Wdrażanie uproszczone — od okazji do faktury pro forma_

Ten artykuł dotyczy następujących składników i wersji oprogramowania Microsoft Dynamics 365 Project Operations:

- Project Operations w środowisku Dataverse w wersji 4.28.0.120

## <a name="features-included-in-this-release"></a>Funkcje uwzględnione w tym wydaniu

W tym wydaniu można dodać do 300 członków zespołu do jednego projektu. Wcześniej limit liczby członków zespołu wynosi 150. Aby uzyskać więcej informacji, zobacz [Ograniczenia projektu](../../project-management/create-wbs.md#project-limitations).

## <a name="quality-updates"></a>Aktualizacje dotyczące jakości

| Obszar funkcji | Numer referencyjny | Aktualizacja dotycząca jakości |
| --- | --- | --- |
| Rozliczenia i ceny | 2497369 | Poprawianie materiałów musi być zgodne z wartością daty w parametrach **Poprawianie**. |
| Rozliczenia i ceny | 2498697 | Poprawiono konfigurację zabezpieczeń dla czasowego **wpisu**. |
| Rozliczenia i ceny | 2517455 | W **przypadku tej samej faktury nie** można wyzwalać jednoczesnego aktywowania akcji Odświeżony wiersz faktury. |
| Rozliczenia i ceny | 2517465 | Akcja **Dezaktywowanie szczegółów wiersza** faktury jest blokowana, ponieważ nie jest obsługiwana. |
| Rozliczenia i ceny | 2556660 | Stałe sprawdzenie czeków efektowalności dat, które są wykonywane w cenniku dołączonym do rekordu parametrów projektu. |
|   Zarządzanie szansami sprzedaży | 2369202 | Poprawiono logikę biznesową, która pozwala sprawdzić, czy cenniki z nakładającymi się datami ważności można dołączyć do tego samego kontraktu projektu. |
|   Zarządzanie szansami sprzedaży | 2385965 | Poprawiono zachowanie na karcie **Klienci** na stronie **Kontraktu Projektu** po wybraniu opcji **Zapisz i zamknij**. |
