---
title: Zarządzanie zaległością rozliczenia - wersja uproszczona
description: W tym temat zamieszczono informacje dotyczące różnych widoków dostępnych podczas zarządzania zaległościami na fakturę.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 77c4df8c4370017b9199eec3a21cd07dd0343fd9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274111"
---
# <a name="manage-the-billing-backlog---lite"></a>Zarządzanie zaległością rozliczenia - wersja uproszczona

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Rozwiązanie Dynamics 365 Project Operations ma dedykowane widoki ułatwiające zarządzanie zaległościami na fakturę. Aby zarządzać zaległościami na fakturę, należy wybrać łącza w obszarze **Sprzedaż** w obszarze **Fakturowanie**. 

Dostępne są następujące widoki:

- Zatrzymania i zaliczki
- Dostępne zatrzymania i zaliczki
- Punkty kontrolne dotyczące stałej ceny
- Zaległość rozliczania produktów
- Zaległość rozliczania czasu i materiałów

## <a name="retainers-and-advances"></a>Zatrzymania i zaliczki

W widoku **Zatrzymania i zaliczki** są wyświetlane wszystkie zatrzymujące i założone postępy we wszystkich kontraktach projektów w systemie. Po zafakturowaniu zatrzymanego lub zaliczki na fakturę można skorzystać z kwoty zaliczki.

## <a name="available-retainers-and-advances"></a>Dostępne zatrzymania i zaliczki

W widoku **Dostępne zatrzymania i zaliczki** są wyświetlane wszystkie dostępne zatrzymujące i założone postępy we wszystkich kontraktach projektów w systemie. Po zafakturowaniu zaliczki lub zaliczki kwota zaliczki staje się dostępna do wykorzystania i zostaje dodana do listy. Po całkowitym zastosowaniu kwoty zatrzymania lub wypłaty z góry jest ona usuwana z listy.

## <a name="fixed-price-milestones"></a>Punkty kontrolne dotyczące stałej ceny

W widoku **Punkty kontrolne dotyczące stałej ceny** są wyświetlane wszystkie punkty kontrolne dotyczące ustalonych cen we wszystkich pozycjach kontraktu projektu w systemie. Jeden lub wiele punktów kontrolnych można oznaczyć jako **Gotowy do zafakturowania** lub **Niegotowy do zafakturowania** w tym widoku. Oznaczenie punktów kontrolnych jako **Przygotowane do fakturowania** spowoduje, że będzie on dostępny do sporządzenia na fakturze.

W przypadku wierszy kontraktu z wieloma klientami mających metodę fakturowania za cenę ustaloną dla każdego klienta w pozycji kontraktu jest tworzony punkt kontrolny. Punkt kontrolny można utworzyć i podzielić na poszczególne specyficzne dla klienta rekordy punktów kontrolnych. Podział jest określany wewnętrznie i zgodnie z rozbiciem procentu naliczenia dla każdego klienta w pozycji kontraktu. W widoku **Punkty kontrolne dotyczące stałej ceny** zobaczysz informacje o rekordach punktów kontrolnych poszczególnych klientów. Każdy z tych rekordów punktów kontrolnych może być oznaczony jako **Gotowy do fakturowania**, z poziomu tego widoku. Jeśli co najmniej jeden z pokrewnych podział punktów kontrolnych jest oznaczony jako **Przygotowane do fakturowania**, stan nagłówka jest aktualizowany do stanu **W toku** ze stanu **Nie rozpoczęto**. Po zafakturowaniu wszystkich podziałów punktów kontrolnych w nagłówku jest aktualizowane pole stan na **Zakończone**.

Punkt kontrolny w wersji roboczej faktury jest wyświetlany w tym widoku wraz ze stanem fakturowania w **Faktura klienta utworzona**. Po potwierdzeniu wersji roboczej faktury stan fakturowania rekordu jest aktualizowany na **Zaksięgowaną fakturę dla odbiorcy**. Nie należy aktualizować tej wartości stanu przy użyciu kodu niestandardowego. Project Operations nie funkcjonują poprawnie, gdy te wartości stanu są aktualizowane za pomocą kodu niestandardowego.

## <a name="product-billing-backlog"></a>Zaległość rozliczania produktów

W widoku **Zaległość rozliczania produktów** są wyświetlane wszystkie pozycje kontraktu oparte na produktach we wszystkich kontraktach projektów systemu. Jeden lub wiele pozycji kontraktu opartego na produkcie można oznaczyć jako **Gotowy do zafakturowania** lub **Niegotowy do zafakturowania** w tym widoku. Oznaczenie pozycji kontraktu opartego na produkcie jako **Przygotowane do fakturowania** spowoduje, że będzie on dostępny do sporządzenia na fakturze.

Pozycja kontraktu oparta na produktach znajdująca się na wersji roboczej faktury jest wyświetlana w tym widoku wraz ze stanem fakturowania **Utworzono fakturę dla klienta**. Po potwierdzeniu wersji roboczej faktury stan fakturowania w tym rekordzie jest aktualizowany na **Faktura klienta zaksięgowana**. Nie należy aktualizować tej wartości stanu przy użyciu kodu niestandardowego. Project Operations nie funkcjonują poprawnie, gdy te wartości stanu są aktualizowane za pomocą kodu niestandardowego.

## <a name="time-and-material-billing-backlog"></a>Zaległość rozliczania czasu i materiałów

W widoku **Zaległość rozliczania czasu i materiałów** są wyświetlane wszystkie wartości rzeczywiste niezafakturowanej sprzedaży we wszystkich kontraktach projektów w systemie, które nie zostały zafakturowane. Jedną lub wiele nierozliczonych wartości rzeczywistych sprzedaży można oznaczyć jako **Gotowy do zafakturowania** lub **Niegotowy do zafakturowania** w tym widoku. Oznaczenie niezafakturowanej wartości rzeczywistej sprzedaży jako **Gotowej do zafakturowania** sprawia, że jest ona dostępna w fakturze roboczej.

Nie można oznaczyć stanu **Nieprzekraczalny** wynoszącego **Niepowodzenie** nieobsłużonych wartości rzeczywistych sprzedaży jako **Przygotowane do fakturowania**. Jeśli wartość rzeczywista musi być oznaczona jako **Przygotowane do fakturowania**, zresetuj stan na innych wartościach rzeczywistych w zatwierdzonym wierszu kontraktu. a następnie ponownie oceń stan **Nieprzekraczalny**.

Jeśli istnieje metoda fakturowania dla wielu klientów, podczas zatwierdzania typu czasu i wydatku dla każdego klienta w pozycji kontraktu jest tworzona jedna niefakturowana wartość sprzedaży w zależności od podziału procentowego rozliczenia określonego dla każdego z klientów. W widoku **Zaległości dotyczące rozliczeń czasu i materiału** będą widoczne poszczególne specyficzne dla konkretnego klienta informacje o niefakturowanych wartościach sprzedaży. Każdy z tych nierozliczonych rekordów rzeczywistych wartości sprzedaży może być oznaczony jako **Gotowy do fakturowania**, z poziomu tego widoku.

W tym widoku jest wyświetlana niezafakturowana faktyczna sprzedaż, która znajduje się na roboczej fakturze wraz ze stanem fakturowania **Utworzono fakturę dla klienta**. Po potwierdzeniu wersji roboczej faktury stan fakturowania w tym rekordzie jest aktualizowany na **Faktura klienta zaksięgowana**. Nie należy aktualizować tej wartości stanu przy użyciu kodu niestandardowego. Project Operations nie funkcjonują poprawnie, gdy te wartości stanu są aktualizowane za pomocą kodu niestandardowego.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]