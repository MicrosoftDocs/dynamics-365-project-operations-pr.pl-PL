---
title: Wiersze podumowy dla czasu
description: W tym temacie wyjaśniono, jak rejestrować wiersze podumowy dla czasu i rejestrować zakup czasu od dostawców.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 10ebe0fcc86b4652ac01e28108361df1f768b61d
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323879"
---
# <a name="subcontract-lines-for-time"></a>Wiersze podumowy dla czasu

[!include [banner](../../includes/dataverse-preview.md)]

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Podumowa w aplikacji Dynamics 365 Project Operations może mieć pozycję podumowy dla czasu. Wiersze podumowy dla czasu umożliwiają menedżerowi projektu zakup czasu zasobu dostawcy na potrzeby zadań związanych z projektem i wymagań dotyczących zasobów.

Aby utworzyć pozycję podumowy dla czasu w aplikacji Project Operations, wykonaj następujące kroki.

1. W okienku nawigacji wybierz opcję **Podumowy**, a następnie otwórz podumowę.
2. Na karcie **Wiersze podumowy** wybierz opcję **Nowy**, aby utworzyć nowy wiersz podumowy.
3. Na stronie **Szybkie tworzenie** w polu **Klasa transakcji** wybierz pozycję **Czas**.
4. Wprowadź pozostałe informacje w polach, a następnie wybierz przycisk **Zapisz**.

  W poniższej tabeli przedstawiono informacje o polach na stronie **wiersza podumowy** oraz na stronie **Szybkie tworzenie**.

| **Pole** | **Opis** |
| --- | --- |
| Imię i nazwisko/nazwa | Nazwa wiersza podumowy. |
| Opis | Krótki opis usług kupowanych w ramach wiersza podumowy. | 
| Typ linii | To pole jest wartością domyślną.  |
| Metoda rozliczania | Wybierz metodę rozliczania. W oparciu o metodę rozliczania przywoływanego wiersza podumowy dla metody rozliczania o stałej cenie jest dostępny harmonogram faktur oparty na punktach kontrolnych. |
| Klasa transakcji | To pole jest wartością domyślną wskazującą, czy wiersz podumowy jest używany do rejestrowania zakupu czasu podwykonawcy. |
| Rola | Rola zasobów podwykonawcy, których czas jest kupowany. Rola przypisana do zasobów podwykonawcy określa koszt zakupu. |
| Żądane rozpoczęcie | Wymagana data rozpoczęcia pracy zasobów podwykonawcy. Żądana data rozpoczęcia służy do wyboru cennika projektu z cenników projektu dołączonych do podumowy. Koszt roli w pozycji umowy jest następnie domyślny dla danego cennika. |
| Żądane zakończenie | Data zakończenia przypisania zasobów podwykonawcy. Ta data służy do pokazywania ostrzeżeń, gdy menedżer projektu przekracza tę wydajność dla wymagań zasobów występujących po tej dacie. |
| Ilość zamówiona | Liczba godzin roli kupowana od dostawcy. Ta wartość służy do pokazywania ostrzeżeń, gdy menedżer projektu przekracza tę wydajność dla wymagań zasobów. |
| Grupa jednostek | Wartość tego pola jest domyślnie ustawiana na grupę jednostek czasu i nie można tego zmienić.  |
| Jednostka | To pole jest domyślnie ustawiane na jednostkę podstawową z grupy jednostek czasu. Można zmienić tę wartość, aby kupić dowolną jednostkę z grupy jednostek czasu, na przykład dzień lub tydzień. Kombinacja roli i jednostki jest używana w celu obliczenia ceny jednostkowej w pozycji podumowy. |
| Cena jednostkowa | Domyślne ceny jednostkowe są stosowane na podstawie kombinacji roli i jednostki z cennika projektu, który ma zastosowanie w przypadku żądanej daty rozpoczęcia dla wiersza podumowy. Jeśli dla odpowiedniego cennika projektu cena jest ustawiona w innej jednostce niż jednostka z wiersza podumowy, system używa konwersji jednostek do obliczenia ceny jednostkowej. |
| Suma częściowa | To jest pole tylko do odczytu, automatycznie obliczane jako **ilość x cena jednostkowa**, jeśli zostanie wprowadzona zarówno wartość ilości, jak i ceny jednostkowej. Jeśli pole ilości, ceny jednostkowej lub oba te pola są puste, można wprowadzić wartość w polu. |
| Podatek |  Wprowadź kwotę podatku. |
| Łączna kwota | Łączna kwota pozycji podumowy po uwzględnieniu podatków. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
