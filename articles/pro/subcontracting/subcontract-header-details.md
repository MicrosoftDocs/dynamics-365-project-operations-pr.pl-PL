---
title: Szczegóły nagłówka dla podumów
description: W tym temacie wyjaśniono funkcje dostępne w nagłówku podumowy w aplikacji Project Operations.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 49158af1a430033db3a5db57a840512c45bc17e2
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323654"
---
# <a name="header-details-for-subcontracts"></a>Szczegóły nagłówka dla podumów

[!include [banner](../../includes/dataverse-preview.md)]

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

W tym temacie wyjaśniono funkcje dostępne w nagłówku podumowy w aplikacji Dynamics 365 Project Operations.

Menedżer projektu planuje i wykonuje projekty, może zatrudniać podwykonawców oraz zakupić produkty i usługi od dostawców. Gdy menedżer projektu musi zakupić produkty lub usługi, może utworzyć podwykonawcę w aplikacji Project Operations.

Aby utworzyć podumowę, wykonaj następujące kroki.

1. W okienku nawigacji wybierz opcję **Podwykonawcy**, a następnie na stronie **Podumowa** wybierz opcję **Nowy**.
2. Wprowadź wymagane informacje, a następnie wybierz **Zapisz**.

    W poniższej tabeli przedstawiono informacje o polach na stronie nagłówka Podumowa.

    | **Pole** | **Opis** |
    | --- | --- | 
    | Imię i nazwisko/nazwa | Nazwa podumowy. |
    | Opis | Krótki opis usług i produktów zakupionych w ramach podumowy. |
    | Dostawca (sprzedawca) | Nazwa firmy, w której są nabywane produkty i usługi. Ten rekord dostawcy ma typ relacji **Dostawca** lub **Dostawca (producent)**. |
    | Data podumowy | Data utworzenia podumowy. |
    | Przyczyna stanu | Stan podumowy. |
    | Waluta | Waluta, w której są nabywane produkty i usługi. Wartość w tym polu jest domyślnie ustawiana na konto dostawcy, ale można to zmienić. Cenniki projektów używane do kalkulacji cen produktów i usług w ramach podumowy powinny być w tej walucie. Z podumową nie można skojarzyć cenników w innej walucie. Koszt produktów i usług ponoszony w ramach tej podumowy zostanie zarejestrowany w projekcie w tej walucie. |
    | Jednostka kontraktująca | Oddział firmy, który zawiera kontrakt dotyczący zakupu lub podumowę z dostawcą. |
    | Warunki płatności | Warunki płatności za faktury dostawcy wystawiane w odniesieniu do tej podumowy. Wartość w tym polu jest domyślnie ustawiana na rekord konta dostawcy. |
    | Adres płatności | Adres, pod który są wysyłane płatności za faktury dostawcy. Wartość w tym polu jest domyślnie ustawiana na rekord konta dostawcy. |
    | Nazwa płatnika | Nazwa osoby lub działu w firmie dostawcy, która wyśle fakturę. Wartość w tym polu jest domyślnie ustawiana na podstawie rekordu konta dostawcy i będzie używana jako nazwa kontaktu podstawowego dla faktur dostawcy utworzonych dla tej podumowy. |
    | Adres płatnika | Adres używany na fakturach od tego dostawcy. Wartość w tym polu jest domyślnie ustawiana na rekord konta dostawcy. Ten adres jest również używany jako adres źródłowy faktury w fakturach dostawcy utworzonych dla tej podumowy. |
    | Suma częściowa | Jeśli podumowa nie ma wierszy, wprowadź w tym polu wartość oznaczającą sumę częściową zamówienia przed opodatkowaniem. Jeśli podumowa ma wiersze, to pole jest tylko do odczytu. Kwota wyświetlana jest sumą częściową ze wszystkich wierszy podumowy. |
    | Łączny podatek | Jeśli podumowa nie ma wierszy, wprowadź w tym polu wartość oznaczającą podatki od tej podumowy. Jeśli podumowa ma wiersze, to pole jest tylko do odczytu. Kwota wyświetlana jest sumą kwot podatku ze wszystkich wierszy podumowy. |
    | Łączna kwota |  To pole obliczane zawiera łączną kwotę podumowy po uwzględnieniu podatków.  |
    | Potwierdzona data | Data potwierdzenia podumowy.  |
    | Żądane przez | Wartość w tym polu jest domyślnie ustawiana na nazwę użytkownika, który tworzy podumowę. Ta wartość może zostać zmieniona przez twórcę podumowy w celu wskazania osoby, w imieniu której tworzy on podumowę.  |
    | Menedżer ds. konta dostawcy | Nazwa podstawowego kontaktu dla konta dostawcy. Wartość w tym polu jest domyślnie ustawiana na rekord konta dostawcy. Ta wartość pola może zostać zmieniona przez użytkownika, aby mógł wybrać inny kontakt jako menedżer konta dostawcy dla podumowy. Alerty e-mail i negocjacje cen mogą być skonfigurowane i wysyłane przez ten kontakt. |


