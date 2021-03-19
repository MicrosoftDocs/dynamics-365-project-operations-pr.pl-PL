---
title: Zarządzanie nieprzekraczalnym stanem i weryfikacjami
description: Ten temat zawiera informacje o sprawdzaniu limitów nieprzekraczania wykonywanych w Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c5c491d4014ffc2568d7df72b542761ec9b1a90b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274042"
---
# <a name="manage-not-to-exceed-status-and-validations"></a>Zarządzanie nieprzekraczalnym stanem i weryfikacjami 

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

## <a name="not-to-exceed-on-approvals"></a>Nie do przekroczenia w zatwierdzeniach

Po przesłaniu godziny lub wpisu wydatku zostaje utworzony rekord zatwierdzania. Jeśli zatwierdzenie jest odpłatne i mapowane na wiersz kontraktu typu czas i materiały, system zakończy sprawdzanie poprawności, które nie przekroczyć interwału, na następujących poziomach:

  - Sprawdzanie zgodności z limitem skonfigurowanym dla klienta w pozycji kontraktu projektu
  - Sprawdź limit ustawiony na pozycji kontraktu
  - Sprawdź limit ustawiony dla klienta
  - Sprawdź limit ustawiony na kontrakcie

Kontrole na każdym poziomie obejmują zapewnienie, że kwota wartości sprzedaży na tym zatwierdzeniu nie naruszy limitu nieprzekraczania na tym poziomie po uwzględnieniu kwoty zaległości rozliczeniowych już zarejestrowanych oraz kwoty zafakturowanej do tej pory na tym poziomie.

Jeśli test zakończy się pomyślnie, zatwierdzenie otrzyma status walidacji **Sukces**.

Jeśli test nie powiedzie się, zatwierdzenie otrzyma status walidacji **Niepowodzenie**. Szczegółowe informacje o pomyślnym sprawdzeniu poprawności będą informować użytkownika, na którym poziomie nie powiodła się walidacja.

W przypadku braku płatnego czasu lub wpisu wydatku, stan nieprzekraczający przekroczenia jest ustawiony na **Brak stosowania** z szczegółami sprawdzania poprawności równą **Brak zastosowania**.

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a>Nie-do-przekroczenia dla wartości rzeczywistych niefakturowanych sprzedaży

Kiedy zatwierdzany jest czas lub zapis wydatku, tworzone są rekordy kosztu i niezfakturowanych wartości sprzedaży. Jeśli faktycznie tworzona niezafakturowana sprzedaż podlega opłacie i jest mapowana do wiersza umowy czasowej i materiałowej, aplikacja przeprowadza weryfikację nieprzekraczalności na następujących poziomach:

  - Sprawdzanie zgodności z limitem skonfigurowanym dla klienta w pozycji kontraktu projektu
  - Sprawdź limit ustawiony na pozycji kontraktu
  - Sprawdź limit ustawiony dla klienta
  - Sprawdź limit ustawiony na kontrakcie

Kontrole na każdym poziomie zapewniają, że kwota wartości sprzedaży na poziomie faktycznym nie naruszy nieprzekraczalnego limitu na tym poziomie po uwzględnieniu kwoty zaległości rozliczeniowych już zarejestrowanych oraz kwoty zafakturowanej do tej pory na tym poziomie.

Jeśli test zakończył się powodzeniem, oznacza to, że niezafakturowane sprzedaż jest przystawiana jako przekroczenie stanu **Zadeklarowany**.

Jeśli test zakończył się niepowodzeniem, oznacza to, że niezafakturowane sprzedaż jest przystawiana jako przekroczenie stanu **Niepowodzenie**. Szczegóły walidacji informują użytkownika, na jakim poziomie walidacja nie powiodła się.

W przypadku niepłatnych lub bezpłatnych wartości rzeczywistych sprzedaży niezafakturowanej w przypadku braku ograniczeń między ustawieniami nie dotyczącymi przekroczenia limitu na poziomie czterech poziomów lub po utworzeniu wartości rzeczywistej koszt, zatrzymanie, ponowne pozyskanie lub sprzedaż między firmami oznacza, że **Stan nieprzekraczalnego limitu**, a nie więcej niż do dłuższego niż **Limit szczegółów sprawdzania poprawności** musi zostać ustawiona na **Brak zastosowania**.

## <a name="reset-the-not-to-exceed-status"></a>Resetuj nieprzekraczalny stan

Można wykonać zbiorcze resetowanie stanu nieprzekraczalnego. Dzięki temu kierownicy projektów mogą dostosować walidację nieprzekraczającą, aby nadać priorytet fakturom za jeden określony zakres pracy, czasu lub wydatków w stosunku do innych, które zostały już zatwierdzone z dostępnej kwoty nieprzekraczalnej.

Po zresetowaniu stanu nieprzekraczalnego w ramach wartości rzeczywistych niefakturowanych sprzedaży kwota ustalona zostaje zmniejszona. Kierownik projektu może wybrać inny zakres pracy, czasu lub wydatków, które poprzednio nie przeszły walidacji nieprzekraczającej, i ponownie je ocenić. Po zmniejszeniu kwoty zadeklarowanej wartości rzeczywiste przejdą teraz walidację. Pomaga to kierownikowi projektu wywierać większy wpływ i kontrolę nad transakcjami podlegającymi fakturowaniu w tym okresie.

Aby zresetować stan nie do przekroczenia, wybierz jeden lub więcej wartości rzeczywistych w widoku **Zaległość rozliczania czasu i materiałów** albo **Wartości rzeczywiste**, a następnie wybierz opcję **Resetuj nieprzekraczalny stan**.

Stan inne niż przekroczenie jest resetowany do **Nieoceniono** na wszystkich właściwych wybranych wartościach rzeczywistych. Wartości rzeczywiste, dla których został zresetowany stan nieprzekraczania, to niezafakturowane wartości rzeczywiste sprzedaży, które nie zostały jeszcze zafakturowane, nie znajdują się na fakturze roboczej i są oznaczone jako wymagalne. Pozostałe wybrane wartości rzeczywiste zostaną zignorowane.

## <a name="reevaluate-not-to-exceed-status"></a>Oblicz ponownie nieprzekraczalny stan

Można wykonać zbiorcze ponowne obliczanie stanu nieprzekraczalnego. Ponowna ocena stanu nieprzekraczalnego jest przydatna w następujących przypadkach:

  - Nastąpiła renegocjacja z klientem limitów nieprzekraczalnych i wartości rzeczywiste będą musiały zostać ponownie oszacowane.
  - Kierownik projektu chce doprecyzować fakturowanie niezafakturowanych zaległości sprzedaży, nadając priorytet jednej pracy nad drugą.

Aby obliczyć ponownie stan nie do przekroczenia, wybierz jeden lub więcej wartości rzeczywistych w widoku **Zaległość rozliczania czasu i materiałów** albo **Wartości rzeczywiste**, a następnie wybierz opcję **Oblicz ponownie nieprzekraczalny stan**.

Wszystkie wybrane wartości rzeczywiste z wartością nieprzekraczalną limitu będą oceniane względem konfiguracji, która nie przekroczy limitu. Wartości rzeczywiste, które są istotne dla ponownej oceny stanu nieprzekraczalności, to niezafakturowane wartości rzeczywiste sprzedaży, które nie zostały zafakturowane, nie znajdują się na wersji roboczej faktury i są oznaczone jako wymagalne. Zaznacz wszystkie wybrane wartości rzeczywiste.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]