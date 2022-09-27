---
title: Płatności dla sprzedawców w momencie zapłaty
description: Ten temat wyjaśnia, jak korzystać ze scenariusza Płacę, gdy płacę (PWP).
author: mukumarm
ms.date: 08/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: mukumarm
ms.openlocfilehash: d1fe8d92663b31b22dc405fc1f3e06d976e6c5dc
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525343"
---
# <a name="pay-when-paid-vendor-payments"></a>Płatności dla sprzedawców w momencie zapłaty

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Ten temat wyjaśnia, jak korzystać ze scenariusza Płacę, gdy płacę (PWP).

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>Utwórz zamówienie zakupu z warunkami PWP

W przypadku księgowania faktury dostawcy, jeśli dostawcę obowiązują warunki PWP, warunki te są widoczne w wierszach zamówienia zakupu (PO). Aby utworzyć zamówienie zakupu z warunkami PWP wykonaj następujące kroki.

1. W Microsoft Dynamics 365 Finance wykonaj jedną z poniższych czynności:

    - Przejdź do **Zaopatrzenie i sourcing** \> **Zamówienia zakupu** \> **Wszystkie zamówienia zakupu**. W okienku akcji wybierz pozycję **Nowe**. W oknie dialogowym **Utwórz zamówienie** wybierz sprzedawcę, dla którego w projekcie ustawiono warunki PWP, wprowadź inne wymagane informacje, a następnie wybierz **OK**.
    - Przejdź do **Zarządzanie projektami i księgowanie** \> **Projekty** \> **Wszystkie projekty**. W okienku akcji otwórz kartę **Zarządzanie** i wybierz pozycję **Zadanie przedmiotu**. Wybierz zlecenie zakupu. Wybierz sprzedawcę, dla którego ustawiono warunki PWP w projekcie, a następnie wybierz **OK**.

2. Na stronie **Zamówienie zakupu**, na zakładce **Wiersze zamówienia zakupu** wybierz **Dodaj wiersz**, aby utworzyć wiersz zamówienia zakupu.
3. Wybierz numer artykułu lub kategorię zamówienia i wprowadź inne wymagane informacje. Przejrzyj szczegóły wiersza PO dla sprzedawcy.

    Opcja **Zapłać po otrzymaniu zapłaty** jest wybierana automatycznie, a wartość w polu **Procent progu PWP** jest automatycznie kopiowana z pola **Procent progu PWP** ze strony **Projekty**.

4. Jeśli nie chcesz stosować PWP względem dostawcy w wierszu zamówienia zakupu, wyczyść opcję **Płać po otrzymaniu zapłaty**. W tym przypadku **Procent progu PWP** dla wiersza zakupu zostanie zresetowany do wartości **0** (zero).
5. Na stronie **Zlecenie zakupu**, w okienku akcji na karcie **Zakup**, kliknij **Potwierdź**, aby potwierdzić zamówienie zakupu.
6. W okienku akcji, na karcie **Faktura**, w grupie Generuj wybierz pozycję **Faktura**, aby wygenerować fakturę do zlecenia zakupu.

## <a name="create-a-project-invoice-proposal"></a>Tworzenie propozycji faktury za projekt

Propozycje faktur projektowych są używane do tworzenia faktur projektowych dla klienta. W scenariuszu PWP płatności sprzedawców są uzależnione od płatności klientów zgodnie z ustawieniami PWP. Istnieją jednak opcje, które pozwalają na zwolnienie płatności bez płatności klienta, zgodnie z Twoimi potrzebami. Aby utworzyć fakturę za projekt dla klienta, wykonaj następujące kroki.

1. W aplikacjach do obsługi klienta przejdź do **Projekt** \> **Projekt** i wybierz projekt.
2. Na zakładce **Rzeczywiste** wybierz linię rzeczywistą wygenerowaną przez PO, która ma typ transakcji **Sprzedaż niefakturowana**. Następnie wybierz opcję **Gotowe do faktury**.
3. Przejdź do **Sprzedaż** \> **Sprzedaż** \> **Kontrakt projektowy** i wybierz kontrakt projektowy.
4. Na pasku akcji wybierz **fakturę**, aby wygenerować fakturę dla klienta.
5. W programie Finanse przejdź do zakładki **Zarządzanie projektem i księgowość** \> **Okresowe** \> **Importuj z tabeli inscenizacji** i wybierz **OK**, aby wygenerować dziennik integracji Project operations.
6. Przejdź do **Zarządzanie projektem i księgowość** \> **Faktury projektu** \> **Propozycja faktury projektu** i wybierz **Post**, aby umieścić propozycję faktury, która została wygenerowana dla projektu.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Aktualizowanie płatności u klienta i spłata

Gdy dostawca wykona swoją pracę nad projektem i prześle fakturę, należy przejrzeć stan projektu i faktury klienta w celu ustalenia, czy dla danego projektu spełniono warunki PWP. Jeśli zostały spełnione warunki PWP dla danego dostawcy, można ustalić, które wiersze na fakturze opłacić na podstawie płatności z tytułu klienta dla danego projektu. W przypadku wybrania opcji zapłaty dostawcy pomimo braku spełnienia warunków PWP, warunki PWP można zastąpić na stronie **Faktura dostawcy z opcją płać po otrzymaniu zapłaty**.

1. W rozwiązaniu Finanse przejdź do opcji **Zarządzanie projektami i ich księgowanie** \> **Projekty** \> **Wszystkie projekty** i wybierz projekt.
2. Na pasku akcji wybierz **Kontrolę**, a następnie wybierz **Faktury dostawców**, aby pokazać wszystkie faktury dostawców, które zostały wygenerowane dla projektu.
3. Na stronie **Faktura dostawcy z opcją płać po otrzymaniu zapłaty**, w polu wyszukiwania wprowadź wartości, aby znaleźć fakturę zakupu, którą chcesz przejrzeć, a następnie wybierz pozycję **Wyszukaj**.
4. Wybierz opcję **Płać po zapłaceniu**, aby wyświetlić tylko faktury PWP.
5. Na skróconej karcie **Wiersze faktury dostawcy** zaznacz wiersze, które chcesz zwolnić do zapłaty.
6. Wybierz **Zwolnienie płatności dla dostawcy**. Opcja **Zapłać po otrzymaniu zapłaty** jest wyczyszczona, a wartość pola **Gotowe do zapłaty** jest zamieniana na **Tak**.
