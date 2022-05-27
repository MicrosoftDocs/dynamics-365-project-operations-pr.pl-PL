---
title: Podział wydatków na pozycje
description: W tym temacie wyjaśniono sposób podziału wydatków na pozycje za pomocą nowej wersji obszaru roboczego Wydatki.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 34b11c6bd8be729957973a60fccccc2dd32c2669
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574535"
---
# <a name="expense-itemization"></a>Podział wydatków na pozycje

[!include [banner](../includes/banner.md)]

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

W organizacjach często jest wymagane podanie szczegółowych informacji o wydatkach poniesionych podczas podróży. Na przykład folio hotelu może zawierać kilka wierszy podzielonych na pozycje, takie jak pokój, podatek, parking i różne wydatki ponoszone każdego dnia w czasie pobytu w hotelu. Wydatek związany z posiłkiem może też wymagać podania bardziej szczegółowego podziału na śniadanie, lunch lub obiad. Zgodnie z potrzebami organizacji każdą kategorię wydatków można skonfigurować w celu odzwierciedlenia podkategoria lub pozycji wiersza stanowiącej część wydatku. Chociaż opcja podziału na pozycje od zawsze jest obsługiwana w **zarządzaniu wydatkami**, obszar roboczy **wydatków w nowej wersji** pozwala na efektywniejszy podział na pozycje, gdy funkcja **Możliwość szybkiego dzielenia cyklicznych wydatków na pozycje** jest włączona.  

## <a name="enable-quick-itemization"></a>Włączanie szybkiego podziału na pozycje 

Funkcji **Możliwość szybkiego dzielenia cyklicznych wydatków na pozycje** można używać do szybkiego dzielenie cyklicznych wydatków na pozycje, jednocześnie unikając wprowadzania wydatków dziennych za każdym razem w czasie pobytu w hotelu. Wykonaj następujące kroki, aby włączyć szybki podział na pozycje.

1. Przejdź do obszaru roboczego **Zarządzanie funkcjami** i na liście funkcji znajdź i wybierz opcję **Raporty wydatków w nowej wersji**. 
2. Wybierz opcję **Włącz teraz**. 
3. Na liście funkcji znajdź i wybierz opcję **Możliwość szybkiego dzielenia cyklicznych wydatków na pozycje**.
4. Wybierz opcję **Włącz teraz**. 

## <a name="itemization-grid"></a>Siatka podziału na pozycje 

Jeśli kategoria wydatków ma podkategorie lub różne składniki tworzące ten wydatek, można podzielić ją na pozycje. Aby podzielić wydatek na pozycje, wybierz wiersz wydatku w raporcie wydatków i w okienku **Szczegóły wydatku** wybierz opcję **Akcje** > **Podziel na pozycje**. Suwak **Podział na pozycje** ujawnia siatkę z polami. W poniższej tabeli przedstawiono przykłady poszczególnych pól w siatce oraz sposób renderowania pola w raporcie wydatków. 

|     Pole          |     Description                                                                                  |     Przykład              |
|--------------------|--------------------------------------------------------------------------------------------------|--------------------------|
|     Podkategoria    |     Lista podkategorii skonfigurowanych w obszarze typu kategorii wydatków **Hotel**.             |     Cena pokoju za dzień      |
|     Data rozpoczęcia     |     Data, gdy po raz pierwszy poniesiono pozycję wydatku.                                           |     13.09.2021           |
|     Stawka dzienna     |     Kwota poniesionej pozycji wydatku.                                                    |     200                  |
|     Ilość       |     Liczba powtarzających się opłat w ciągłym okresie.                       |     3                    |

![Podziel wydatek na pozycje.](media/Itemization%20screen%201.png)

Podczas zapisywania podziału na pozycje zobaczysz pojedynczy wiersz z podziałem na pozycje dla ilości określonej w siatce podziału na pozycje. Każdy wiersz rozpoczyna się w dniu określonym w siatce.

![Raport z podziałem na pozycje.](media/Itemization%20screen%202.png)

