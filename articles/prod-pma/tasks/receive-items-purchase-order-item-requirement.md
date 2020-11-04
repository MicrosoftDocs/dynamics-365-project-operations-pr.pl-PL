---
title: Pobierz towary w zamówieniu zakupu od zapotrzebowania na towary
description: W tym temat przedstawiono sposób przyjmowania zapasów na zamówienie zakupu z zapotrzebowania na towary.
author: Yowelle
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5b3622458da957ed150311f6ea75d5f1444d5f1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082179"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>Pobierz towary w zamówieniu zakupu od zapotrzebowania na towary

[!include [banner](../../includes/banner.md)]

W tym temat przedstawiono sposób przyjmowania zapasów na zamówienie zakupu z zapotrzebowania na towary.

Używając zapotrzebowania na towary zamiast transakcji na towary, można zaplanować dostawę tuż przed faktycznym wykorzystaniem towaru, utworzyć zamówienie zakupu, uwzględnić towar w ramach umowy handlowej i uwzględnić zapotrzebowanie na towary w planowaniu produkcji. 

W tym zadaniu jest używany zestaw danych USSI.

1. W okienku nawigacji wybierz kolejno pozycje **Moduły > Zarządzanie projektami i księgowanie > Projekty > Wszystkie projekty**.
2. Na liście wybierz łącze w żądanym wierszu.
3. W okienku akcji wybierz pozycję **Plan**.
4. Wybierz **Zapotrzebowania na towary**.
5. Wybierz **Nowy**.
6. W nowym wierszu wprowadź lub wybierz wartość w polu **Kod towaru**.
7. W polu **Ilość** wprowadź liczbę.
8. Wybierz pozycję **Zapisz**.
9. W okienku akcji wybierz pozycję **Zarządzaj**.
10. Wybierz **Funkcje**.
11. Wybierz **Utwórz zamówienie zakupu**.
12. Zaznacz pole wyboru **Dołącz wszystkie**.
13. W polu **Konto sprzedawcy** wprowadź lub wybierz wartość.
14. Wybierz pozycję **OK**.
15. W okienku nawigacji wybierz kolejno pozycje **Moduły > Rozrachunki z dostawcami > Zamówienia zakupu > Wszystkie zamówienia zakupu**.
16. Na liście wybierz łącze w żądanym wierszu.
17. W okienku akcji wybierz pozycję **Zakup**.
18. Wybierz pozycję **Potwierdź**.
19. W okienku akcji wybierz pozycję **Otrzymaj**.
20. Wybierz **Odbiór produktu**.
21. Wpisz wartość w polu **Odbiór produktu**.
22. Wybierz pozycję **OK**.

