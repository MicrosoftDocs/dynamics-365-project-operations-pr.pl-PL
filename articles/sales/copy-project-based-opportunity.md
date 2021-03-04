---
title: Kopiowanie szans sprzedaży opartych na projekcie
description: W tym temacie zamieszczono informacje dotyczące kopiowania szans sprzedaży opartych na produkcie w Project Operations.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 26ae5cc267bb06f958bbf9cdce2d80ccde9d3d24
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181688"
---
# <a name="copy-project-based-opportunities"></a>Kopiowanie szans sprzedaży opartych na projekcie

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_


Szanse sprzedaży projektu można łatwo kopiować, aby tworzyć nowe szanse sprzedaży projektu. 

1. Przejdź do strony listy **Project Operations** i wybierz szansę sprzedaży z listy. Można też otworzyć stronę szczegółów konkretnej szansy sprzedaży. 
2. Z dowolnej strony wybierz opcję **Kopiuj**. Zostanie otwarte okno dialogowe zawierające poniższe informacje w polach. W zależności od wybranych wartości w tym oknie proces kopiowania może ulec zmianie.

    | **Pole** | **Opis** | **Wpływ zmian w dalszych etapach** |
    | --- | --- | --- |
    | Temat | Wprowadź odpowiedni temat lub nazwę szansy sprzedaży. Po otwarciu okna dialogowego program wyświetli temat dotyczący źródłowej szansy sprzedaży z dołączonym elementem **-kopia**. | W tym polu nie ma wpływu zmian na dalsze etapy. |
    | Konto | Odwołania do rekordu firmy lub konta klienta. Po otwarciu okna dialogowego system wyświetli konto ze źródłowej szansy sprzedaży. | To pole to główny klient szansy sprzedaży. |
    | Jednostka kontraktująca | Jednostka organizacyjna odpowiedzialna za realizację projektów skojarzonych z tą transakcją. Po otwarciu okna dialogowego system wyświetli jednostkę zamawiającą ze źródłowej szansy sprzedaży. | Jednostka zamawiająca to wydział firmy, który wykonuje projekt po zamknięciu transakcji. Każda jednostka zamawiająca korzysta z jakiejś waluty, i ta waluta jest używana do raportowania szacowanych i rzeczywistych kosztów poniesionych podczas projektu. |
    | Waluta | Waluta, w jakiej obliczana jest kwota oferty. Po otwarciu okna dialogowego system wyświetli walutę ze źródłowej szansy sprzedaży. | Waluta jest używana do ustalenia domyślnego cennika i tworzenia oszacowań finansowych w ofercie. Ostatecznie waluta jest używana do fakturowania klienta w momencie wykorzystania szansy sprzedaży. |
    | Kopiuj kalkulację cen | Wartość tak/nie wskazuje, czy cena z szansy sprzedaży powinna być kopiowana z szansy sprzedaży źródłowej. | Jeśli zaznaczona jest opcja **Tak**, cenniki są kopiowane z lokalizacji źródłowej do docelowej szansy sprzedaży. Jeśli wybrana jest opcja **Nie**, cenniki są domyślnie ustawiane na podstawie najnowszych skonfigurowanych cenników. |

3. Wybierz pozycję **OK**. System utworzy kopię szansy sprzedaży projektu na podstawie wybranych parametrów i otworzy się nowa szansa sprzedaży projektu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]