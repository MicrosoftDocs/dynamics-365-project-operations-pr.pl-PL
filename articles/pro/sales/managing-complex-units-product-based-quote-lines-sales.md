---
title: Zarządzanie jednostkami złożonymi, takimi jak na użytkownika, na miesiąc dla wierszy oferty opartej na produktach
description: Ten temat zawiera informacje o zarządzaniu jednostkami złożonymi w wierszu oferty opartej na produktach.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 741230e69302138cce8f7379f520f7178e1c80af
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081944"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines"></a>Zarządzanie jednostkami złożonymi, takimi jak na użytkownika, na miesiąc dla wierszy oferty opartej na produktach

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Do obsługi sprzedaży produktów opartych na subskrypcji program Dynamics 365 Project Operations używa współczynników ilościowych. W przypadku produktów opartych na subskrypcji liczba w ofercie lub pozycji kontraktu projektu jest wyrażona liczbą użytkowników w miesiącu.

Zazwyczaj cena subskrybowanego oprogramowania jest przechowywana w katalogu jako cena za jednego użytkownika za jeden miesiąc. W trakcie procesu sprzedaży cena w wierszu oferty to zazwyczaj cena na użytkownika na miesiąc, która została wynegocjowana i uzupełniona o rabat przez przedstawiciela handlowego z działu IT. Każda transakcja ma inną liczbę użytkowników i inną liczbę miesięcy subskrypcji. Ilość użyta do obliczenia kwoty w wierszu oferty jest iloczynem liczby użytkowników i liczby miesięcy subskrypcji.

W celu zapewnienia obsługi tego typu sprzedaży w rozwiązaniu Project Operations wprowadzono koncepcję współczynników ilościowych. Współczynniki ilościowe opierają się na atrybutach produktów w systemie Dynamics 365. Podczas konfigurowania konkretnych właściwości produktu program Project Operations umożliwia oflagowanie podzbioru tych właściwości albo wszystkich właściwości jako współczynników ilościowych.

Project Operations weryfikuje, czy tylko właściwości liczbowe lub właściwości produktu mające liczbowy typ danych są flagowane jako współczynniki ilościowe. W przypadku dodawania do wiersza oferty towaru z współczynnikami ilościowymi, pole **Ilość** staje się polem tylko do odczytu. Po wprowadzeniu wartości właściwości produktu będących współczynnikami ilościowymi Project Operations obliczy ilość w wierszu oferty.

Na przykład system Dynamics 365 Sales może mieć następujące właściwości:

- **Liczba użytkowników** : liczba użytkowników
- **Liczba miesięcy** : liczba miesięcy subskrypcji
- **Kod SKU produktu**

Właściwości **Liczba użytkowników** i **Liczba miesięcy** można oflagować jako współczynniki ilościowe, odpowiednio modyfikując właściwości wiersza produktu.

Aby utworzyć współczynnik ilościowy na podstawie właściwości produktu, wykonaj następujące kroki:

1. W lewym panelu nawigacyjnym Project Operations przejdź do **Sprzedaż** > **Produkty**.
2. Otwórz produkt, dla którego chcesz skonfigurować czynniki ilościowe. Upewnij się, że właściwości produktu zostały już skonfigurowane.
3. Na stronie **Informacje o projekcie** danego produktu wybierz kartę **Czynniki ilościowe**.
4. W podsiatce wybierz **+ Nowe obliczanie pola**.
5. Wprowadź nazwę współczynnika ilościowego i wybierz wartość właściwości, która ma być mapowana na obliczenia pola.
6. Zapisz i zamknij formularz. Powtórz te kroki dla wszystkich właściwości, które mają być używane do obliczania ilości wiersza oferty opartej na produkcie.

W przypadku utworzenia wiersza oferty opartej na produkcie dla danego produktu, ilość w wierszu oferty zostanie zablokowana. Ilość będzie obliczana jako iloczyn wartości właściwości wprowadzonych w danym wierszu oferty.
