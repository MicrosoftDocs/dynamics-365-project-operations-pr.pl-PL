---
title: Przeglądanie zaległości fakturowania w projektach i kontraktach na projekty
description: W tym temacie zamieszczono informacje dotyczące sposobu przeglądania zaległości dotyczących wpisów czasu, wydatków i projektów oraz ich oznaczania jako gotowych do zafakturowania.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: bcdcc0cae06ce61bd582d56a8398e718051ff564
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123976"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a>Przeglądanie zaległości fakturowania w projektach i kontraktach na projekty

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Kiedy transakcja jest gotowa do utworzenia i przetworzenia dla niej faktury, należy ją oznaczyć jako **Przygotowane do fakturowania**. W tym temacie opisano typy transakcji, które można tworzyć.

## <a name="review-the-time-and-material-billing-backlog"></a>Przeglądanie zaległości rozliczania czasu i materiałów

Gry wpis czasu lub wydatku zostanie przesłany i zatwierdzony dla projektu, program PSA tworzy wartość rzeczywistą projektu. Jeśli kombinacja projektu i klasy transakcji jest mapowana na pozycję kontraktu w projekcie rozliczanym według czasu i materiałów, po zatwierdzeniu wpisu są tworzone dwie wartości rzeczywiste:

- Wartość rzeczywista kosztu 
- Wartość rzeczywista nierozliczonej sprzedaży

Wartości rzeczywiste nierozliczonej sprzedaży reprezentują zaległość rozliczania, a ich stan fakturowania musi mieć wartość **Przygotowane do fakturowania**. Podczas tworzenia faktury projektu nierozliczone wartości rzeczywiste sprzedaży oznaczone jako **Przygotowane do fakturowania** są kopiowane jako szczegóły wierszy faktury.

Aby przejrzeć zaległość rozliczania czasu i materiałów, wybierz kolejno opcje **Sprzedaż** \> **Rozliczenia** \> **Zaległość rozliczania czasu i materiałów**. Zaznacz wszystkie nierozliczone wartości rzeczywiste sprzedaży, które są gotowe do zafakturowania, a następnie wybierz pozycję **Przygotowane do fakturowania**. Stan rozliczania tych wartości rzeczywistych zmieni się na **Przygotowane do fakturowania**.

![Zaległość rozliczania czasu i materiałów](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a>Przeglądanie zaległości rozliczania produktów

W programie PSA jeżeli kontrakt projektu zawiera pozycje kontraktu oparte na produktach, te pozycje (wiersze) są brane pod uwagę podczas fakturowania, ilekroć jest tworzona faktura do kontraktu na projekt. Każdy produkt z pozycjami kontraktu oznaczonym jako **Przygotowane do fakturowania** jest kopiowany do faktury za projekt jako wiersze faktury projektu.

Aby przejrzeć zaległość rozliczania produktów, wybierz kolejno opcje **Sprzedaż** \> **Rozliczenia** \> **Zaległość rozliczania produktów**. Zaznacz wszystkie pozycje kontraktu oparte na produktach, które są gotowe do zafakturowania, a następnie wybierz pozycję **Przygotowane do fakturowania**. Stan rozliczania tych wierszy zmieni się na **Przygotowane do fakturowania**.

![Zaległość rozliczania produktów](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a>Przeglądanie punktów kontrolnych rozliczania w kontraktach o stałej cenie

Każda pozycja kontraktu projektu z metodą rozliczania według stałej ceny musi określać punkty kontrolne kontraktu. Te punkty kontrolne kontraktu można zafakturować tylko wtedy, gdy są oznaczone **Przygotowane do fakturowania**. 

Aby przejrzeć punkty kontrolne rozliczania, wybierz kolejno opcje **Sprzedaż** \> **Rozliczenia** \> **Punkty kontrolne dotyczące stałej ceny**. Zaznacz punkty kontrolne, które są gotowe do zafakturowania, a następnie wybierz pozycję **Przygotowane do fakturowania**. Stan rozliczania tych punktów kontrolnych zmieni się na **Przygotowane do fakturowania**.

![Punkty kontrolne dotyczące stałej ceny](media/FPBacklog.png)
