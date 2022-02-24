---
title: Typy okresów
description: Ten temat zawiera informacje dotyczące sposobów konfigurowania typów okresów na potrzeby szacowania przychodów.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6bcd988fbd074c66d64f7e327b4329d3de27e950
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531515"
---
# <a name="period-types"></a>Typy okresów

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Typ okresu określa, jak często szacowany jest przychód w projekcie. Ten temat zawiera informacje dotyczące sposobów konfigurowania typów okresów na potrzeby szacowania przychodów. 

## <a name="create-and-work-with-period-types"></a>Tworzenie typów okresów i praca z nimi
Aby utworzyć typy okresów i pracować z nimi, wykonaj następujące czynności:

1. W środowisku aplikacji Dynamics 365 Finance przejdź do pozycji **Zarządzanie projektami i księgowanie** > **Konfiguracja** > **Szacowania** > **Typy okresów**.
2. Wybierz pozycję **Nowy**, aby utworzyć nowy typ okresu. Wprowadź nazwę i opis.
3. W polu **Częstotliwość** wybierz wartość:

    - W przypadku wybrania opcji **Tydzień**, **Co dwa tygodnie**, **Co pół miesiąca**, **Miesiąc**, **Dzień**, **Kwartał** lub **Rok** kalendarz będzie używany do generowania okresów. 
    - Jeśli wybierzesz opcję **Okres księgi**, okresy księgi z konfiguracji księgi głównej będą używane do generowania okresów.
    - W przypadku wybrania opcji **Nieograniczone** można wskazać okresy niestandardowe.
4. Wybierz rekord typu okresu, a następnie wybierz pozycję **Generuj okresy**, aby utworzyć okresy dla typu okresu. Na podstawie wybranej częstotliwości okresu może być dostępna opcja określenia daty rozpoczęcia lub liczby okresów do wygenerowania.
5. Wybierz pozycję **Okresy**, aby przejrzeć wygenerowane okresy.

