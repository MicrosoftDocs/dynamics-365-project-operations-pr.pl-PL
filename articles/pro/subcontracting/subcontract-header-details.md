---
title: Szczegóły nagłówka dla podumów
description: W tym artykule objaśniono funkcje w nagłówku kontraktu podrzędnego dostępne w aplikacji Project Operations.
author: rumant
ms.date: 09/14/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ce16b7a968bc7e6904411ae9e021a5ca1839d02e
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261431"
---
# <a name="header-details-for-subcontracts"></a>Szczegóły nagłówka dla podumów

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

W tym artykule objaśniono funkcje w nagłówku kontraktu podrzędnego dostępne w aplikacji Dynamics 365 Project Operations.

Menedżer projektu planuje i wykonuje projekty, może zatrudniać podwykonawców oraz zakupić produkty i usługi od dostawców. Gdy menedżer projektu musi zakupić produkty lub usługi, może utworzyć podwykonawcę w aplikacji Project Operations.

Aby utworzyć podumowę, wykonaj następujące kroki.

1. W okienku nawigacji wybierz opcję **Podwykonawcy**, a następnie na stronie **Podumowa** wybierz opcję **Nowy**.
2. Wprowadź wymagane informacje, a następnie wybierz **Zapisz**.

    W poniższej tabeli przedstawiono informacje o polach na stronie **Nagłówek podumowy**.

    | Pole | Opis |Wpływ funkcjonalny |
    |---|------|---| 
    | Imię i nazwisko/nazwa | Nazwa podumowy. | Na wszystkich listach rozwijanych podwykonawców nazwa podumowy jest wymieniona w pierwszej kolumnie, by pomóc w zidentyfikowaniu podumowy. | 
    | Opis | Krótki opis usług i produktów zakupionych w ramach podumowy. | Brak |
    | Dostawca (sprzedawca) | Nazwa firmy, w której są nabywane produkty i usługi. Ten rekord dostawcy ma typ relacji **Dostawca** lub **Dostawca (producent)**. | W zależności od wybranego dostawcy wartości domyślne są automatycznie wprowadzane dla następujących pól:<br/> **• Waluta** </br> **• Cenniki** </br> **• Warunki płatności**</br> **• Adres płatności**</br> **• Adres płatnika**</br> **• Nazwa płatnika** </br>**• Menedżer ds. konta dostawcy**|
    | Data podumowy | Data utworzenia podumowy. | Data podumowy służy do wybierania prawidłowego cennika zakupu z cenników dołączonych do pokrewnego dostawcy lub z parametrów projektu. |
    | Przyczyna stanu | Stan podumowy. | Stan określa miejsce podumowy w procesie biznesowym i czy możliwe jest jego edytowanie. <br/>Wartości są następujące:<br>• **Wersja robocza**: podumowa może być edytowana. Podumowy można edytować tylko ze stanem **Wersja robocza**.<br/>• **Potwierdzona**: negocjacje z dostawcą zostały zakończone, a podumowa została zatwierdzona do dostarczenia. <br/>• **Zamknięta**: dostarczenie podumowy jest zakończone.<br/>• **Anulowana**: podumowa została anulowana i nie jest planowana żadna dostawa.  | 
    | Waluta | Waluta, w jakiej są nabywane produkty i usługi. Wartość domyślna jest wprowadzana automatycznie z konta dostawcy, ale można ją zmienić. | Waluta podumowy służy do wybierania cennika zakupu z cenników dołączonych do pokrewnego dostawcy lub z parametrów projektu. Z podumową nie można skojarzyć cenników w innej walucie. Koszt czasu, wydatki i materiały zapewniane przez zasoby dostawcy na podstawie tej podumowy są rejestrowane w tej walucie w projekcie. Po zapisaniu rekordu podumowy nie można zmienić waluty dla podumowy.|
    | Jednostka kontraktująca | Oddział firmy, który zawiera kontrakt dotyczący zakupu lub podumowę z dostawcą. | Brak |
    | Warunki płatności | Warunki płatności na fakturze od dostawcy wystawiane na tej podumowie. Wartość domyślna jest wprowadzana automatycznie z rekordu konta dostawcy. | Warunki płatności z podumowy są kopiowane do wszystkich faktur od dostawców powiązanych z tą podumową. Warunki płatności można zaktualizować, jeśli podumowa ma stan **Wersja robocza**. | 
    | Adres płatności | Adres dostawcy, na który należy wysłać płatności. Wartość domyślna jest wprowadzana automatycznie z rekordu konta dostawcy. | Adres płatności z podumowy jest kopiowany jako adres płatności na wszystkie faktury od dostawcy utworzone dla tej podumowy. Adres płatności można zaktualizować, jeśli podumowa ma stan **Wersja robocza**.|
    | Nazwa płatnika | Nazwa osoby lub działu w firmie dostawcy, która wyśle fakturę. Wartość domyślna jest wprowadzana automatycznie z rekordu konta dostawcy. | Wartość **Nazwa płatnika** z podumowy jest kopiowana do wszystkich faktur od dostawców powiązanych z tą podumową. To pole można zaktualizować, jeśli podumowa ma stan **Wersja robocza**.|
    | Adres płatnika | Adres używany na fakturach od dostawcy. Wartość domyślna jest wprowadzana automatycznie z rekordu konta dostawcy. | Ten adres jest adresem „faktura od” na fakturach od dostawcy, które są tworzone dla tej podumowy. |
    | Suma częściowa | Jeśli podumowa nie ma wierszy, wprowadź sumę częściową zamówienia przed opodatkowaniem. Jeśli podumowa ma wiersze, to pole jest tylko do odczytu. Wyświetlana kwota jest kwotą częściową ze wszystkich wierszy podumowy. | Brak |
    | Łączny podatek | Jeśli podumowa nie ma wierszy, wprowadź całkowite opodatkowanie od tej podumowy. Jeśli podumowa ma wiersze, to pole jest tylko do odczytu. Wyświetlana kwota jest kwotą opodatkowania ze wszystkich wierszy podumowy. | Brak |
    | Łączna kwota | To pole obliczane zawiera łączną kwotę podumowy po uwzględnieniu podatków. | Brak |
    | Potwierdzona data | Data, gdy podumowa została potwierdzona. | Brak |
    | Żądane przez | W tym polu jest domyślnie ustawiona nazwa użytkownika, który tworzy podumowę. Twórca podumowy może jednak zmienić wartość w celu wskazania osoby, w imieniu której tworzona jest podumowa. | Brak |
    | Menedżer ds. konta dostawcy | Nazwa podstawowego kontaktu dla konta dostawcy. Wartość domyślna jest wprowadzana automatycznie z rekordu konta dostawcy. Można wybrać inny kontakt jako menedżera konta dostawcy dla podumowy. | Można skonfigurować alerty poczty e-mail, aby powiadomić kontakt o zmianach wykonywanych w podumowie w wyniku negocjacji cen. |
