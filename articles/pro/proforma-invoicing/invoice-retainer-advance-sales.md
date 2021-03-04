---
title: Fakturowanie płatności opartej na zatrzymaniu lub zaliczce
description: Ten temat zawiera informacje na temat fakturowania zatrzymania lub zaliczki w Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 12bf3822227badcf8c83d84d6aef6c0fdc7a972a
ms.sourcegitcommit: 250270409412ba4cad95fbd4c345a80d3d2b3e53
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/21/2020
ms.locfileid: "4596205"
---
# <a name="invoice-a-retainer-or-an-advance"></a>Fakturowanie płatności opartej na zatrzymaniu lub zaliczce

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Aplikacja Dynamics 365 Project Operations obsługuje kontrakty oparte na zatrzymaniach i zaliczkach jednorazowych. W kontrakcie projektu można zarejestrować harmonogramy zatrzymań lub jednorazowe zaliczki. Jednak rejestrowanie na poziomie kontraktu projektu nie powoduje natychmiastowego udostępnienia takiego zatrzymania lub zaliczki. Aby można było skorzystać z zatrzymania lub zaliczki na fakturze, należy najpierw zafakturować zatrzymanie lub zaliczkę.

Wykonaj poniższe kroki, aby skonfigurować fakturowanie zatrzymania lub zaliczki.

1. Wybierz pozycję **Sprzedaż** > **Fakturowanie** > **Zatrzymania i zaliczki**. 
2. Na stronie **Zatrzymania i zaliczki** użyj filtru w celu wybrania określonego zatrzymania lub zaliczki do fakturowania, a następnie oznacz wybór jako **Gotowy do zafakturowania**.
3. Utwórz fakturę ręcznie na liście **Kontraktów projektu** lub na stronie szczegółów. Zatrzymanie lub zaliczka będą wyświetlane w wersji roboczej faktury w sekcji **Zaliczki i zatrzymania** na stronie **Faktura**.
4. Potwierdź fakturę. Spowoduje to, że zatrzymanie lub udostępnienie będzie gotowe do użycia. Fakturę można sprawdzić na stronie z **Zaliczki i zatrzymania**. W przypadku zafakturowanej zaliczki lub zatrzymania, dostępna kwota jest widoczna w siatce.

## <a name="create-a-retainer-or-advance-from-the-invoice-grid"></a>Tworzenie zatrzymania lub zaliczki z poziomu siatki Faktury

Istnieje możliwość utworzenia zatrzymania lub zaliczki bezpośrednio na fakturze.

1. Na wersji roboczej faktury, w podsiatce **Zaliczki i zatrzymania** wybierz opcję **Nowe**, aby utworzyć nowe zatrzymanie lub zaliczkę. 
2. Na stronie **Szybkie tworzenie** dodaj wymagane informacje, a następnie wybierz pozycję **Zapisz**. W kontrakcie związanym z fakturą jest tworzone zatrzymanie lub zaliczka powiązana z fakturą. Na stronie **Zatrzymania i zaliczki** zaliczka lub zatrzymanie są automatycznie oznaczane jako **Gotowe do zafakturowania**, a następnie dodawane do podsiatki strony **Faktura**.

## <a name="reconcile-an-invoiced-retainer-or-advance"></a>Uzgadnianie fakturowanej zaliczki lub zatrzymania

Po zafakturowaniu zatrzymania lub zaliczki można ich używać lub uzgodnić na fakturze z godzinami, wydatkami, punktami kontrolnymi lub innymi opłatami opartymi na projektach. Klient zobaczy kwotę faktury pomniejszoną o kwoty zatrzymane lub kwoty zaliczki użytej w tej fakturze.

Na wszystkich fakturach wygenerowanych dla kontraktu dotyczącego projektu z zafakturowanymi zaliczeniami lub zaliczkami na fakturze w projekcie automatycznie jest stosowane zatrzymanie lub zaliczka.

Można to zobaczyć na siatce **Zastosowane zaliczki i zatrzymania** na stronie **Faktura**. Poniższa tabela zawiera informacje na temat pól w siatce **Zastosowane zaliczki i zatrzymania** na stronie **Faktura projektu**.

| Pole | Lokalizacja | Opis | Wpływ zmian w dalszych etapach |
| --- | --- | --- | --- |
| Opis | Siatka **Zastosowane zaliczki i zatrzymania** na stronie **Faktura projektu** |To pole jest tylko do odczytu i zawiera opis zatrzymania lub zaliczki użytych na tej fakturze. Nie można zmienić tej wartości na fakturze. Tę wartość można zaktualizować w podsiatce na stronie **Kontraktu projektu**. | To pole może być wyświetlane klientowi na wydrukowanej fakturze w celu wskazania, które z tych zatrzymań lub zaliczek zostało zastosowane do faktury. |
| Data dostarczenia | Siatka **Zastosowane zaliczki i zatrzymania** na stronie **Faktura projektu**  | To pole jest tylko do odczytu i zawiera datę faktury dla zatrzymania lub zaliczki. Nie można zmienić tej wartości na fakturze. Tę wartość można zaktualizować w podsiatce na stronie **Kontraktu projektu**. | To pole może być wyświetlane klientowi na wydrukowanej fakturze w celu wskazania daty zastosowania po raz pierwszy zatrzymania lub zaliczki. |
| Kwota | Siatka **Zastosowane zaliczki i zatrzymania** na stronie **Faktura projektu**  | To pole jest tylko do odczytu i zawiera kwotę zatrzymania lub zaliczki na fakturze. Nie można zmienić tej wartości na fakturze. Tę wartość można zaktualizować w podsiatce na stronie **Kontraktu projektu**. | To pole może być wyświetlane klientowi na wydrukowanej fakturze w celu wskazania oryginalnej kwoty zatrzymania lub zaliczki, którą zapłacił klient. |
| Kwota użyta | Siatka **Zastosowane zaliczki i zatrzymania** na stronie **Faktura projektu**  | To pole przeznaczone tylko do odczytu zawiera obliczoną wartość, która podsumowuje ilość wykorzystanego zatrzymania lub zaliczki. | To pole może być wyświetlane klientowi na wydrukowanej fakturze w celu wskazania kwoty tego zatrzymania lub zaliczki, która już została użyta. |
| Kwota rozszerzona | Siatka **Zastosowane zaliczki i zatrzymania** na stronie **Faktura projektu**  | To edytowalne pole zawiera kwotę zatrzymania lub zaliczki używanych na tej fakturze projektu. Nie może być to więcej, niż dostępne w zaliczce. System automatycznie oblicza, jako różnicę pomiędzy polami siatki **Kwota** i **Kwota użyta**. Można zmniejszyć tę kwotę, aby użyć mniej niż jest dostępnych środków, ale nie można zwiększyć kwoty, która ma być używana ponad dostępną wartość. | To pole może być wyświetlane klientowi na wydrukowanej fakturze w celu wskazania kwoty tego zatrzymania lub zaliczki, która jest użyta na tej fakturze. |
| Kwota salda na zatrzymaniu. | Siatka **Zastosowane zaliczki i zatrzymania** na stronie **Faktura projektu**  | To pole jest tylko do odczytu i wskazuje, jaka część danego zatrzymania lub zaliczki pozostanie do użycia po potwierdzeniu faktury. | To pole może być wyświetlane klientowi na wydrukowanej fakturze w celu wskazania kwoty tego zatrzymania lub zaliczki, która zostanie do użycia po potwierdzeniu i zapłaceniu faktury. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]