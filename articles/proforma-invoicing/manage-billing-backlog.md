---
title: Zarządzanie zaległością rozliczenia
description: W tym temacie zamieszczono informacje dotyczące wyświetlania i pracy z zaległościami w rozliczeniu w Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c3752abd26e760d27320d2b86079d84a967d53cf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287746"
---
# <a name="manage-the-billing-backlog"></a>Zarządzanie zaległością rozliczenia

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Rozwiązanie Dynamics 365 Project Operations ma dwa dedykowane widoki ułatwiające zarządzanie zaległościami na fakturę. Są to **Punkty kontrolne stałych cen** oraz **Zaległości rozliczeniowe w ramach czasu i materiałów**. Aby wybrać widok, w obszarze **Sales** w Project Operations, po lewej stronie nawigacji wybierz pozycję **Rozliczanie**. W tym miejscu są przechowywane łącza do rozliczania zaległości.

## <a name="fixed-price-milestones"></a>Punkty kontrolne dotyczące stałej ceny

W tym widoku są wyświetlane wszystkie pozycje punktów kontrolnych ustalonej ceny we wszystkich pozycjach kontraktu projektu w systemie. Jeden lub wiele punktów kontrolnych można oznaczyć jako **Gotowy do zafakturowania** lub **Niegotowy do zafakturowania** w tym widoku. Gdy punkt kontrolny jest oznaczany jako **Gotowy do zafakturowania**, staje się dostępny w wersji roboczej faktury.

Kiedy pozycje kontraktu wielu klientów mają metodę fakturowania przy stałej cenie, dla każdego klienta w pozycji kontraktu jest tworzony jeden punkt kontrolny. Użytkownik tworzy punkt kontrolny, a punkt kontrolny jest dzielony na klienta = rekordy określonych punktów kontrolnych wewnętrznie, na podstawie podziału procentu rozliczenia określonego dla każdego klienta w pozycji kontraktu. W widoku **Punktów kontrolnych o stałej cenie** zostaną wyświetlone poszczególne rekordy punktów kontrolnych dotyczących konkretnego klienta. Każdy z tych rekordów punktów kontrolnych może być oznaczony jako **Gotowy do fakturowania**, z poziomu tego widoku. Jeśli co najmniej jeden z powiązanych punktów kontrolnych jest oznaczony jako **Gotowy do zafakturowania**, nagłówek przechodzi do stanu **W toku** z **Nierozpoczętego**. Po zafakturowaniu wszystkich podziałów punktów kontrolnych w nagłówku stan zostanie ustawiony na **Zakończony**.

Punkt kontrolny w wersji roboczej faktury jest wyświetlany w tym widoku wraz ze stanem fakturowania w **Faktura klienta utworzona**. Po potwierdzeniu wersji roboczej faktury stan fakturowania w tym rekordzie jest aktualizowany na **Faktura zaksięgowana**. Zaktualizowanie tej wartości stanu przy użyciu kodu niestandardowego nie jest zalecane. Project Operations nie będzie działać poprawnie, jeśli te wartości stanu będą aktualizowane za pomocą kodu niestandardowego.

## <a name="time-and-material-billing-backlog"></a>Zaległość rozliczania czasu i materiałów

Ten widok zawiera listę wszystkich niezaksięgowanych wartości rzeczywistych sprzedaży, które nie zostały zafakturowane we wszystkich kontraktach projektów w systemie. Jedną lub wiele nierozliczonych wartości rzeczywistych sprzedaży można oznaczyć jako **Gotowy do zafakturowania** lub **Niegotowy do zafakturowania** w tym widoku. Oznaczenie niezafakturowanej wartości rzeczywistej sprzedaży jako **Gotowej do zafakturowania** sprawia, że jest ona dostępna w fakturze roboczej.

Nierozliczone wartości rzeczywiste sprzedaży, które mają stan **Nie do przekroczenia** lub **Nieudane** nie mogą być oznaczone jako **Gotowe do zafakturowania**. Jeśli te wartości rzeczywiste muszą zostać oznaczone jako gotowe, zresetuj stan na innych wartościach rzeczywistych w zatwierdzonym wierszu kontraktu, a następnie oceń stan **Nie do przekroczenia**.

W przypadku pozycji z listy kontraktów obejmujących wielu klientów, które zawierają metodę fakturowania typu czas i materiały, podczas zatwierdzania czasu i wydatków dla każdego klienta w pozycji kontraktu jest tworzona wartość rzeczywista sprzedaży niezafakturowanej w zależności od procentu podziału określonego dla każdego klienta w pozycji kontraktu. W widoku **Zaległości rozliczeń czasu i materiałów** będą widoczne poszczególne specyficzne dla konkretnego klienta nierozliczone wartości rzeczywiste. Każdy z tych nierozliczonych rekordów rzeczywistych wartości sprzedaży może być oznaczony jako **Gotowy do fakturowania**, z poziomu tego widoku.

Nierozliczona wartość rzeczywista sprzedaży w wersji roboczej faktury jest wyświetlana w tym widoku wraz ze **stanem fakturowania** w polu **Faktura klienta utworzona**. Po potwierdzeniu wersji roboczej faktury stan fakturowania w tym rekordzie jest aktualizowany na **Faktura klienta zaksięgowana**. Zaktualizowanie tej wartości stanu w tym momencie przy użyciu kodu niestandardowego nie jest zalecane. Project Operations nie będzie działać poprawnie, gdy te wartości stanu będą aktualizowane za pomocą kodu niestandardowego.


[!INCLUDE[footer-include](../includes/footer-banner.md)]