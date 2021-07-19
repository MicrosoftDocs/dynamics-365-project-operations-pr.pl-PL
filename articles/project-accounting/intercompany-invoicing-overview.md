---
title: Omówienie faktury międzyfirmowej
description: W tym temacie przedstawiono informacje i przykłady dotyczące fakturowania międzyfirmowego dla projektów.
author: sigitac
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: c1dcf642f79ce64cb83285ac6dc6d7eaf815145c
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369389"
---
# <a name="intercompany-invoicing-overview"></a>Omówienie faktury międzyfirmowej

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Organizacja może dysponować wieloma oddziałami, podmiotami zależnymi i innymi firmami, które przekazują sobie produkty i usługi do projektów. Podmiot prawny, który dostarcza usługę lub produkt, nosi nazwę *firmy wypożyczającej*. Podmiot prawny, który otrzymuje usługę lub produkt, nosi nazwę *firmy pożyczającej*.

Poniższa ilustracja przedstawia typowy scenariusz, w którym dwa podmioty prawne, Contoso Robotics USA (podmiot prawny pożyczający) i Contoso Robotics UK (podmiot prawny wypożyczający) dzielą się zasobami w celu realizacji projektu dla klienta, firmy Adventure works. W tym scenariuszu firma Contoso Robotics USA została zakontraktowana na dostawę robót do Adventure Works.

![Faktura międzyfirmowa](./media/IntercompanyScenario.png) 

W aplikacji Dynamics 365 Project Operations do przetwarzania transakcji międzyfirmowych jest używany następujący przepływ:

1. Zasoby z firmy wypożyczającej rejestrują międzyfirmowe transakcje dotyczące czasu lub wydatków, rezerwując czas i wydatki względem projektów w firmie pożyczającej.
2. Koszty związane z czasem i wydatkami są rejestrowane w firmie wypożyczającej przy użyciu listy kosztów własnych firmy pożyczającej.
3. Międzyfirmowe transakcje niezafakturowanej sprzedaży są rejestrowane w firmie wypożyczającej przy użyciu listy kosztów własnych firmy pożyczającej.
4. Przychód niezafakturowany jest rejestrowany w firmie pożyczającej przy użyciu cennika sprzedaży z kontraktu dotyczącego projektu. Klienta można fakturować podczas rejestrowania niezafakturowanego przychodu. Klient nie musi czekać na zakończenie przetwarzania faktury międzyfirmowej.
5. Międzyfirmowe faktury dla klientów są tworzone w sposób okresowy w firmie wypożyczającej. Faktury są tworzone ręcznie lub przy użyciu zautomatyzowanego procesu okresowego. Można utworzyć jedną fakturę dla każdej firmy pożyczającej lub oddzielne faktury mogą być tworzone w ramach projektu.
6. Gdy międzyfirmowa faktura dla klienta jest księgowana w firmie wypożyczającej, równocześnie w firmie pożyczającej jest tworzona odpowiadająca jej oczekująca faktura od dostawcy. Koszty na oczekującej fakturze od dostawcy będą rejestrowane w księdze podrzędnej projektu podczas księgowania faktury.

Na poniższym diagramie przedstawiono fakturowanie międzyfirmowe w zależności od zdarzeń księgowania oraz oczekiwane zapisy księgowe w księdze głównej.

![Przepływ międzyfirmowy](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>Dodatkowe zasoby

- [Konfigurowanie faktury międzyfirmowej](configure-intercompany-invoicing.md)
- [Rejestrowanie transakcji międzyfirmowych](create-intercompany-transactions.md)
- [Tworzenie faktur międzyfirmowych dla klienta i dostawcy](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]