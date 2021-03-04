---
title: Strona główna uaktualnienia
description: W tym temacie przedstawiono miejsca, w których można znaleźć ważne informacje dotyczące nowych i zmienionych funkcji w programie Dynamics 365 Project Service Automation, oraz proces uaktualniania do najnowszej wersji.
manager: kfend
ms.prod: ''
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e30da3a5ade6d8bafcdc45801b830196841997bf
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150096"
---
# <a name="upgrade-home-page"></a>Strona główna uaktualnienia

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a>Uaktualnij aplikację PSA z wersji 2.x lub 1.x do wersji 3.x

### <a name="new-instances"></a>Nowe wystąpienia

Od 17 maja 2019 r. po wybraniu programu Project Service Automation podczas inicjowania obsługi administracyjnej nowego wystąpienia domyślnie będzie instalowana wersja 3.x.

### <a name="existing-instances"></a>Istnieją wystąpienia

Wcześniej klienci, którzy mieli wystąpienie programu PSA w wersji 2.x i chcieli uaktualnić do wersji 3.x, która jest wersją programu PSA wyposażoną w ujednolicony interfejs klienta (UCI), musieli się skontaktować z działem pomocy technicznej i przekazać informacje dotyczące posiadanego wystąpienia, tak aby dział pomocy technicznej mógł przygotować uaktualnienie do wersji 3.x. Od 1 marca 2020 r. klienci, którzy mają wystąpienie PSA w wersji 2.xi muszą uaktualnić swoje wystąpienia do wersji 3.x, będą mogli uaktualnić swoje wystąpienia bezpośrednio z portalu administracyjnego bez konieczności kontaktowania się z pomocą techniczną firmy Microsoft.  

> [!NOTE]
> Program PSA w wersji 3.x zawiera istotne zmiany. Został oparty na strukturze ujednoliconego interfejsu w celu ułatwienia obsługi użytkownikom. Przeprojektowana aplikacja oferuje spójny, jednolity interfejs użytkownika, który jest łatwy w obsłudze i zapewnia dobrą widoczność na wszystkich ekranach bez względu na ich wielkość. W całej aplikacji wprowadzono wiele innych zmian. Zmodyfikowane obszary obejmują kalkulację cen, rezerwację i przypisywanie zasobów oraz zarządzanie okresami, wydatkami i zatwierdzeniami.

Zalecamy, aby przed rozpoczęciem procesu uaktualniania wykonać następujące zadania:

- Sprawdź, czy na wybranym urządzeniu są zainstalowane programy Dynamics 365 Field Service i Project Service Automation. Jeśli są zainstalowane oba rozwiązania, należy zaplanować ich uaktualnienie przed wznowieniem regularnego korzystania z wystąpienia.
- Uważnie przejrzyj poniższe tematy. Znajomość i zrozumienie zmian dokonanych między wersjami pomogą w prawidłowym uaktualnieniu. Te tematy zawierają informacje o zasadniczych zmianach w programie PSA oraz uwagi i zalecenia dotyczące planowania uaktualnienia do wersji 3.x.

    - [Nowości i zmiany w programie Project Service Automation w wersji 3](whats-new-changed-v3.md)
    - [Zagadnienia dotyczące uaktualniania — Project Service Automation z wersji 2.x lub 1.x do wersji 3.x](upgrade-v3.md)

- Uaktualnij wystąpienie piaskownicy, aby ocenić zmiany w posiadanej implementacji przed uaktualnieniem wystąpienia produkcyjnego.

Gdy już przejrzysz tematy wspomniane wcześniej i przygotujesz wszystko do uaktualnienia do programu PSA w wersji 3.x lub innej wersji z interfejsem UCI, prześlij do działu pomocy technicznej Microsoft prośbę o dodanie opcji uaktualnienia do Centrum administracyjnego. We wniosku wprowadź szczegółowe informacje o swoim wystąpieniu.

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a>Starsze wersje rozwiązania PSA (PSA 2.x) w nowo utworzonym wystąpieniu

Od 17 maja 2019 r. wszystkie nowe wystąpienia będą domyślnie używały klienta UCI. W celu zapewnienia zgodności z tą zmianą domyślnie będzie inicjowana obsługa administracyjna programów PSA w wersji 3.x i Field Service w wersji 8.x, ponieważ te wersje są przewidziane do współpracy z klientem UCI.

Od 1 marca 2020 r. klienci Dynamics PSA nie będą już mogli tworzyć nowego środowiska ze starszymi wersjami PSA, na przykład PSA w wersji 2.x lub niższej. Każde nowe środowisko będzie wyłącznie w wersji 3.x PSA.

> [!NOTE]
> Aby osiągnąć najlepszy efekt podczas korzystania ze starszych wersji aplikacji Field Service i PSA, przejdź do strony **Ustawienia systemu** i w polu **Używaj tylko nowego ujednoliconego interfejsu (zalecane)** zaznacz wartość **Nie**, ponieważ te wersje nie są zaprojektowane do poprawnego ładowania w interfejsie UCI. Po wyłączeniu interfejsu UCI można otwierać i uruchamiać te wersje programów Field Service i PSA przy użyciu starego klienta sieci Web. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]