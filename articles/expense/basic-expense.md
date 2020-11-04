---
title: Wpis wydatków (lekkich)
description: W tym temat zamieszczono informacje na temat pracy z wpisem wydatków w ramach wdrożenia w wersji uproszczonej.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 746d5d9ff56222e7d6b9b6e264db75d5814365c7
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081896"
---
# <a name="expense-entry-lite"></a>Wpis wydatków (lekkich)

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Podstawowe lub uproszczone zarządzanie wydatkami polega na zarejestrowaniu prostych kosztów. Istnieje możliwość rejestrowania kosztów w stosunku do projektu, a następnie analizy i zatwierdzenia ich przez osobę zatwierdzającą w projekcie.

Aby uzyskać więcej informacji o możliwościach wydatkowych w Dynamics 365 Project Operations zobacz temat [Informacje o wydatkach](expense-overview.md).

## <a name="capture-a-basic-expense"></a>Rejestrowanie podstawowego wydatku

Wydatki można rejestrować, aby można było przesłać je do osoby zatwierdzającej.

1. Przejdź do obszaru **Wydatki** i wybierz pozycję **Nowy**.
2. Na stronie **Nowy wydatek** wprowadź wymagane informacje o wydatkach, a następnie wybierz pozycję **Zapisz**.

## <a name="submit-a-basic-expense"></a>Przesyłanie podstawowego wydatku

Po zakończeniu przechwytywania wszystkich kosztów i przygotowaniu ich do zatwierdzenia należy je przesłać.

1. Przejdź do obszaru **Wydatki** i wybierz wydatek. Można też wybrać wszystkie wydatki, korzystając z pola wyboru w nagłówku.
2. Wybierz **Prześlij**. System przetwarza wybrane wpisy, a następnie tworzy żądania zatwierdzeń wydatków.

## <a name="recall-a-basic-expense"></a>Wycofanie podstawowego wydatku

Jeśli wydatek został przesłany przez pomyłkę, można go wycofać. Czas wymagany do wycofania wpisu wydatku zależy od etapu zatwierdzania, na którym się znajduje.  Jeśli osoba zatwierdzająca jeszcze nie zatwierdziła wpisu, odwołanie może nastąpić natychmiast. Jeśli jednak wpis został już zatwierdzony, należy poprosić osobę zatwierdzającą o zatwierdzenie wycofania i odwrócenie transakcji.

1. Przejdź do obszaru **Koszty** , a następnie na liście wydatków wybierz koszty, które chcesz wycofać.
2. Wybierz pozycję **Odwołaj**. Jeśli pozycja wydatku nie została jeszcze zatwierdzona, system natychmiast ją wycofa. Jeśli zapis wydatków został już zatwierdzony, jest tworzone żądanie wycofania umożliwiające powiadomienie osoby zatwierdzającej o chęci odwrócenia wydatku. Osoba zatwierdzająca potwierdzi również, że można dokonać odwrócenia, a wpis zostanie cofnięty.

## <a name="delete-a-basic-expense"></a>Usunięcie podstawowego wydatku

Wydatki które nie zostały jeszcze przesłane, można usunąć. Aby usunąć wydatek, który został już przesłany, należy go najpierw wycofać.

## <a name="see-also"></a>Zobacz także

- [Omówienie zatwierdzeń](../approvals/approvals-overview.md)
