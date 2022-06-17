---
title: Zarządzanie zaległością rozliczenia
description: W tym artykule przedstawiono informacje na temat sposobu wyświetlania zaległych rozliczeń i pracy z nimi w aplikacji Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5be05639650bb5b9d646067e8d83bada60824081
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929391"
---
# <a name="manage-billing-backlog"></a>Zarządzanie zaległością rozliczenia

**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu

Rozwiązanie Dynamics 365 Project Operations ma dedykowane widoki ułatwiające zarządzanie zaległościami na fakturę. Aby zarządzać zaległościami na fakturę, należy wybrać łącza w obszarze **Sprzedaż** w obszarze **Fakturowanie**. 

Dostępne są następujące widoki:

- Zatrzymania i zaliczki
- Dostępne zatrzymania i zaliczki
- Punkty kontrolne dotyczące stałej ceny
- Zaległość rozliczania czasu i materiałów

## <a name="retainers-and-advances"></a>Zatrzymania i zaliczki

Widok **Zatrzymania i zaliczki** zawiera listę wszystkich zatrzymań i zaliczek we wszystkich umowach projektów. Po zafakturowaniu zatrzymanego lub zaliczki na fakturę można skorzystać z kwoty zaliczki.

## <a name="available-retainers-and-advances"></a>Dostępne zatrzymania i zaliczki

Widok **Dostępne zatrzymania i zaliczki** zawiera listę wszystkich zatrzymań i zaliczek we wszystkich umowach projektów. Po zafakturowaniu zaliczki lub zaliczki kwota zaliczki staje się dostępna do wykorzystania i zostaje dodana do listy. Po całkowitym wykorzystaniu kwoty zatrzymania lub zaliczki zostaje ona usunięta z listy.

## <a name="fixed-price-milestones"></a>Punkty kontrolne dotyczące stałej ceny

Widok **Punktów kontrolnych stałej ceny** zawiera listę wszystkich punktów kontrolnych stałej ceny we wszystkich wierszach kontraktu projektu. Z tego widoku jeden lub wiele punktów kontrolnych można oznaczać jako **Gotowe do fakturowania** lub **Nie można zafakturować**. Oznaczenie punktów kontrolnych jako **Przygotowane do fakturowania** spowoduje, że będzie on dostępny do sporządzenia na fakturze.

W przypadku wierszy kontraktu z wieloma klientami mających metodę fakturowania za cenę ustaloną dla każdego klienta w pozycji kontraktu jest tworzony punkt kontrolny. Punkt kontrolny można utworzyć i podzielić na poszczególne specyficzne dla klienta rekordy punktów kontrolnych. Podział jest określany wewnętrznie i zgodnie z rozbiciem procentu naliczenia dla każdego klienta w pozycji kontraktu. W widoku **Punkty kontrolne dotyczące stałej ceny** zobaczysz informacje o rekordach punktów kontrolnych poszczególnych klientów. Każdy z tych rekordów punktów kontrolnych może być oznaczony jako **Gotowy do fakturowania**, z poziomu tego widoku. Gdy co najmniej jeden z powiązanych podziałów punktów kontrolnych jest oznaczony jako **Przygotowane do fakturowania**, stan nagłówka jest aktualizowany do **W trakcie wykonywania** z **Nierozpoczęte**. Po zafakturować wszystkie podziały punktów kontrolnych stan nagłówka punktów kontrolnych jest aktualizowany do stanu **Zakończono**.

Punkt kontrolny w wersji roboczej faktury jest wyświetlany w tym widoku wraz ze stanem fakturowania w **Faktura klienta utworzona**. Po potwierdzeniu wersji roboczej faktury stan fakturowania rekordu jest aktualizowany na **Zaksięgowaną fakturę dla odbiorcy**. 

> [!NOTE] 
> Nie aktualizuj tej wartości stanu przy użyciu kodu niestandardowego. Project Operations nie funkcjonują poprawnie, gdy te wartości stanu są aktualizowane za pomocą kodu niestandardowego.

## <a name="time-and-material-billing-backlog"></a>Zaległość rozliczania czasu i materiałów

W widoku **Zaległość rozliczania czasu i materiałów** są wyświetlane wszystkie wartości rzeczywiste niezafakturowanej sprzedaży we wszystkich kontraktach projektów w systemie, które nie zostały zafakturowane. Jedną lub wiele nierozliczonych wartości rzeczywistych sprzedaży można oznaczyć jako **Gotowy do zafakturowania** lub **Niegotowy do zafakturowania** w tym widoku. Oznaczenie niezafakturowanej wartości rzeczywistej sprzedaży jako **Gotowej do zafakturowania** sprawia, że jest ona dostępna w fakturze roboczej.

Nie można oznaczyć stanu **Nieprzekraczalny** wynoszącego **Niepowodzenie** nieobsłużonych wartości rzeczywistych sprzedaży jako **Przygotowane do fakturowania**. Jeśli wartości rzeczywiste muszą być oznaczone jako **Gotowe do zafakturowania**, należy zresetować stan innych wartości rzeczywistych dla danego kontraktu, a następnie ponownie oceniać stan **Nieprzekraczalny**.

Jeśli istnieje metoda fakturowania dla wielu klientów, podczas zatwierdzania typu czasu i wydatku dla każdego klienta w pozycji kontraktu jest tworzona jedna niefakturowana wartość sprzedaży w zależności od podziału procentowego rozliczenia określonego dla każdego z klientów. W widoku **Zaległości dotyczące rozliczeń czasu i materiału** będą widoczne poszczególne specyficzne dla konkretnego klienta informacje o niefakturowanych wartościach sprzedaży. Każdy z tych nierozliczonych rekordów rzeczywistych wartości sprzedaży może być oznaczony jako **Gotowy do fakturowania**, z poziomu tego widoku.

Niezafakturowana rzeczywista sprzedaż, która znajduje się na roboczej wersji faktury, jest pokazana w tym widoku ze stanem rozliczenia **Utworzono fakturę dla klienta**. Po potwierdzeniu wersji roboczej faktury stan fakturowania w tym rekordzie jest aktualizowany na **Faktura klienta zaksięgowana**. 

> [!NOTE] 
> Nie aktualizuj tej wartości stanu przy użyciu kodu niestandardowego. Project Operations nie funkcjonują poprawnie, gdy te wartości stanu są aktualizowane za pomocą kodu niestandardowego.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
