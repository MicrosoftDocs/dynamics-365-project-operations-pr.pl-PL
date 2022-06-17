---
title: Konfigurowanie kategorii projektów
description: W tym artykule przedstawiono informacje na temat konfigurowania kategorii projektów.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 440fc712750c07e8426d54e3a1f994f506879e3c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933597"
---
# <a name="configure-project-categories"></a>Konfigurowanie kategorii projektów

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Project Operations oferuje niezawodne funkcje służące do kategoryzowania przychodów i kosztów projektów. Kategorie umożliwiają raportowanie i analizowanie transakcji projektów oraz przesyłanie księgowości do księgi głównej.

Na poniższym diagramie przedstawiono korelację między kategoriami transakcji, wspólnymi kategoriami i kategoriami projektów. 

Kategorie transakcji są podstawowymi grupami transakcji projektów. W ramach tego pogrupowania istnieje zestaw wspólnych kategorii, które mogą być współużytkowane w aplikacjach i modułach. Kategorie projektów to najmniejsze i najdokładniejsze poziomy kategorii. Kategorie projektów są specyficzne dla encji prawnej, modułu i aplikacji.

![Korelacja między kategoriami transakcji, wspólnymi kategoriami i kategoriami projektów.](media/project-categories.png)

## <a name="transaction-categories"></a>Kategorie transakcji

Kategorie transakcji reprezentują podstawowe pogrupowanie transakcji projektu. Nie są specyficzne dla firmy lub typu transakcji. Na przykład firma Contoso Robotics używa kategorii „projektowanie”, „podróże”, „instalacja” i „transakcja usług” do grupowania transakcji projektów.

Kategorie transakcji są definiowane w module Project Operations. 
1. Przejdź do **Ustawienia** \> **Kategorie transakcji**, aby otworzyć formularz. 
2. Aby utworzyć nową kategorię transakcji, należy wybrać opcję **Nowa** lub wybrać **Import z szablonu Excel**.

## <a name="shared-categories"></a>Udostępnione kategorie

Usługa Dynamics 365 używa pojęcia Kategorie udostępnione w celu kategoryzowania wydatków w różnych aplikacjach, takich jak Dynamics 365 Finance, Dynamics 365 Supply Chain i Dynamics 365 Project Operations. W przypadku każdej utworzonej kategorii transakcji w ramach Project Operations są automatycznie tworzone cztery powiązane kategorie wspólne: godziny, wydatek, opłaty i przedmiot. Udostępnione kategorie można przejrzeć i dopasować, przechodząc kolejno do **Zarządzania projektem i księgowania** \> **Konfiguracji** \> **Kategorii** \> **Kategorii wspólnych**.

## <a name="project-categories"></a>Kategorie projektu

Kategorie projektu reprezentują najniższy, najbardziej dokładny poziom szczegółowości konfiguracji kategorii i muszą zostać skonfigurowane oddzielnie dla każdej firmy — przez księgowego projektu.

1. Przejdź do sekcji **Zarządzenie projektem i księgowanie** \> **Konfiguracja** \> **Kategorie** \> **Kategorie projektów**.
2. Wybierz **Nowy**.
3. Wybierz **Identyfikator kategorii** współużytkowanej kategorii utworzonej w poprzedniej sekcji. Project Operations umożliwia skorzystanie z wyłącznie tylko udostępnionych kategorii skojarzonych z kategoriami transakcji.
4. Wybierz grupę kategorii.

## <a name="category-groups"></a>Grupy kategorii

Grupy kategorii umożliwiają udostępnianie właściwości, głównie profilom księgowania, między pokrewnymi kategoriami projektów. Dla każdego typu transakcji musi istnieć co najmniej jedna grupa kategorii, a do każdej kategorii projektu jest przypisana grupa.

Specyfikacje księgowania w Project Operations są definiowane przez reguły profilu koszt projektu i przychód, kategorie projektów i grupy kategorii. Grupy kategorii można skonfigurować, przechodząc do **Zarządzenie projektem i księgowanie** \> **Konfiguracja** \> **Kategorie** \> **Grupy kategorii**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]