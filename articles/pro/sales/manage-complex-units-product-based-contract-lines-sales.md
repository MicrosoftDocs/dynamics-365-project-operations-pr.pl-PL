---
title: Zarządzanie złożonymi jednostkami dla pozycji kontraktu opartej na produkcie - wersja uproszczona
description: W tym temat zamieszczono informacje dotyczące sprzedaży produktów opartych na subskrypcji.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6bd4e11bf96d9f7d77c77fe081fde02b421c3139915150480a8d1a4d812887f6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003379"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a>Zarządzanie złożonymi jednostkami dla pozycji kontraktu opartej na produkcie - wersja uproszczona

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Do obsługi sprzedaży produktów opartych na subskrypcji program Dynamics 365 Project Operations używa współczynników ilościowych. W przypadku produktów opartych na subskrypcji liczba w kontrakcie lub pozycji kontraktu projektu jest wyrażona liczbą użytkowników w miesiącu.

Cena subskrybowanego oprogramowania jest przechowywana w katalogu jako cena za jednego użytkownika za jeden miesiąc. W trakcie procesu sprzedaży cena w wierszu kontraktu to zazwyczaj cena na użytkownika na miesiąc, która została wynegocjowana i uzupełniona o rabat przez przedstawiciela handlowego. Każda transakcja ma inną liczbę użytkowników i inną liczbę miesięcy subskrypcji. Ilość użyta do obliczenia kwoty pozycji umowy to iloczyn liczby użytkowników i liczby miesięcy abonamentowych.

W celu zapewnienia obsługi tego typu sprzedaży w rozwiązaniu Project Operations wprowadzono koncepcję *współczynników ilościowych*. Współczynniki ilościowe opierają się na atrybutach produktów. Podczas konfigurowania konkretnych właściwości produktu można oznaczyć podzbiór tych właściwości albo wszystkich właściwości jako współczynników ilościowych.

Project Operations weryfikuje, czy tylko właściwości liczbowe lub właściwości produktu mające liczbowy typ danych są flagowane jako współczynniki ilościowe. Kiedy produkt z skonfigurowanymi współczynnikami ilościowymi jest dodawany do pozycji kontraktu, pole **Ilość** jest dostępne jako tylko do odczytu. Po wprowadzeniu wartości właściwości produktu będących współczynnikami ilościowymi rozwiązanie Project Operations obliczy ilość w pozycji kontraktu.

Na przykład system Dynamics 365 Sales może mieć następujące właściwości:

- **Liczba użytkowników**: liczba użytkowników.
- **Liczba miesięcy**: liczba miesięcy subskrypcji.
- **SKU produktu**: jednostka magazynowa (SKU) danego produktu.

Właściwości **Liczba użytkowników** i **Liczba miesięcy** można oflagować jako współczynniki ilościowe, odpowiednio modyfikując właściwości wiersza produktu.

Aby utworzyć współczynnik ilościowy z poziomu właściwości produktu, należy wykonać następujące kroki.

1. W przypadku **Project Operations** wybierz **Sprzedaż-Produkty**.
2. Otwórz produkt, dla którego chcesz skonfigurować wskaźniki ilościowe. Upewnij się, że w produkcie zdefiniowano już właściwości.
3. Na stronie **Informacje o projekcie** wybierz kartę **Współczynnik ilościowy**.
4. W podsiatce wybierz **+ Nowe obliczanie pola**.
5. Wprowadź nazwę **Współczynnika ilościowego** i wybierz wartość właściwości, która ma być mapowana na obliczenia pola.
6. Zapisz i zamknij formularz.
7. Powtórz kroki 2-6 dla wszystkich właściwości, które będą składają się na ilość w wierszu kontraktu opartego na produkcie.

W przypadku, gdy użytkownik tworzy wiersz kontraktu dla tego produktu, ilość pozycji kontraktu jest zablokowana. Ilość jest następnie obliczana jako iloczyn wartości właściwości dla danej pozycji kontraktu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]