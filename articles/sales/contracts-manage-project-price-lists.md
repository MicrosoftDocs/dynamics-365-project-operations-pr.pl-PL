---
title: Zarządzanie cennikami projektu w kontraktach projektu
description: Ta temat zawiera informacje na temat zarządzania cennikami projektu przy kontraktach dotyczących projektów.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3313eef74b5e7a0624b32d2a336cd986dfdda839
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010394"
---
# <a name="manage-project-price-lists-on-project-contracts"></a>Zarządzanie cennikami projektu w kontraktach projektu

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Kontrakty projektów w rozwiązaniu Dynamics 365 Project Operations są projektowane tak, aby obsługiwały w kontrakcie wiele efektywnych cenników sprzedaży. W operacjach projektu istnieje nowa encja skojarzona o nazwie **Cenniki projektu**. Ta encja jest relacją typu jeden-do-wielu z kontraktem dotyczącym projektu.

Cenniki projektu służą do wyceny transakcji dotyczących czasu, materiałów i wydatków w projekcie. Gdy kontrakt ma co najmniej jeden cennik projektu, cenniki te służą do wyceny czasu, materiałów, szacunków kosztów i wartości rzeczywistych dotyczących projektów, które są skojarzone z kontraktem za pośrednictwem wiersza kontraktu.

Jeśli w umowie dotyczącej projektu nie ma cenników projektu, zostanie wyświetlony komunikat ostrzegawczy, że nie ma cenników projektu, a Twoje szacunki, rzeczywiste prace projektowe, materiały i zarejestrowane wydatki nie zostaną wycenione. Nie będzie ceny na wartości sprzedaży.

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a>Kojarzenie i odkojarzenie cennika projektu względem kontraktu dotyczącego projektu

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-material-and-expenses"></a>Utwórz lub skojarz konkretny cennik w celu oszacowania pracy, materiałów i wydatków związanych z projektem

1. W kontrakcie projektu wybierz kartę **Cenniki projektów**.
2. W podsiatce wybierz pozycję **+ Dodaj nowy Cennik projektu**.
3. Na suwaku **Szybkie tworzenie** wybierz cennik. 

  Lista rozwijana zawiera listę wszystkich cenników, dla których ustawiono zestawienie **Sprzedaż**, w którym waluta na cenniku odpowiada walucie zawartej w kontrakcie.
  
4. Wprowadź opis skojarzenia z cennikiem projektu, wybierz pozycję **Zapisz**, a następnie zamknij suwak **Szybkie tworzenie**.

   Utworzenie skojarzenia cennika projektu.
   
5. Powtórz kroki 1-4, aby skojarzyć z kontraktem projektu więcej niż jeden cennik projektu. Utwórz wiele cenników projektów tylko wtedy, gdy masz różne daty obowiązywania w każdym z powiązanych cenników projektów.

> [!NOTE]
> Project Operations nie obsługują nakładania się obowiązywania dat cenników projektu. Jeśli istnieje wiele cenników projektu dotyczących transakcji z określonym terminem, cena w tej transakcji będzie domyślnie równa zero.

### <a name="remove-a-project-price-list-association"></a>Usuń powiązanie cennika projektu

- Wybierz Cennik projektu i wybierz pozycję **Usuń cennik projektu kontraktu** w podsiatce. 

  Cennik jest usuwany z cenników projektu dotyczących danego kontraktu. Sam cennik nie zostanie usunięty. Usuwany jest tylko skojarzeny z kontraktem.

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a>Konfigurowanie automatycznej konfiguracji domyślnej cenników projektu na kontrakcie

Cennik projektu można ustawić jako cennik domyślny dla projektu. Ta konfiguracja zapewnia, że wszystkie umowy w Twojej organizacji zawsze zaczynają się od standardowego cennika projektu dla tego okresu cenowego.

### <a name="set-up-the-organizational-default-for-project-price-lists"></a>Konfigurowanie ustawień domyślnych organizacyjnych dla cenników projektu

1. Wybierz kolejno pozycje **Ustawienia** > **Ogólne** i **Parametry**.
2. Na stronie lista **Aktywnych parametrów** wybierz rekord, kliknij go dwukrotnie, aby go otworzyć. Kiedy klikasz dwukrotnie opcję, upewnij się, że nie klikasz wartości pola, która jest hiperłączem. 
3. Na stronie **Aktywne parametry** wybierz kartę **Cennik**. W podsiatce jest widoczna lista domyślnych cenników. Jest to lista kosztów standardowych i cenników sprzedaży. Dla każdej sprzedawanej waluty w programie jest dostępna lista cen **Sprzedaży** zawierająca wartość domyślną na wszystkich kontraktach tworzonych dla klientów, którzy są transakcją w tej walucie.

### <a name="set-up-a-customer-specific-project-price-list"></a>Konfigurowanie cennika konkretnego klienta

Po wynegocjowaniu głównej umowy cenowej z klientami można również skonfigurować cenniki projektów dla konkretnych klientów.

1. Wybierz kolejno pozycje **Sprzedaż** > **Klienci**.
2. Z listy aktywnych klientów wybierz klienta, dla którego jest Cennik specjalny.
3. Wybierz rekord klienta, który ma go otworzyć, a następnie wybierz kartę **Cenniki projektu**. W podsiatce jest wyświetlona lista cenników projektu specyficzna dla danego klienta. 
4. W tym miejscu utwórz nowe skojarzenie cennika, aby dysponować cennikiem określonym dla tego klienta.

## <a name="custom-pricing-on-a-project-contract"></a>Niestandardowa kalkulacja cen w kontrakcie dotyczącym projektu

Po utworzeniu organizacji i domyślnych cenników projektu dla konkretnego klienta kontrakty projektów zostaną utworzone automatycznie za pomocą tych skojarzeń z cennikami projektu. Jednak cenniki projektu zawarte w kontrakcie projektu są zawsze kopiowane z datą i nazwą kontraktu dodaną do nich. Menedżerowie kont i projektów mogą następnie rozpocząć edycję cen w tych kopiach. Te zmienione ceny będą dotyczyć wyłącznie tego kontraktu dotyczącego projektu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
