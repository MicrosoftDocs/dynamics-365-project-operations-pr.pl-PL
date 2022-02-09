---
title: Wiersze podumowy dla czasu
description: W tym temacie wyjaśniono, jak rejestrować wiersze podumowy dla czasu i rejestrować zakup czasu od dostawców.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 29b38ec9124502e4283b71d13434b1e0420bc413
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547257"
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

| **Pole** | **Opis** | **Wpływ funkcjonalny** |
| --- | --- | --- |
| Imię i nazwisko/nazwa | Nazwa wiersza podumowy, który ma pomóc w identyfikacji. | Ta kolumna będzie wyświetlana jako pierwsza we wszystkich wyszukiwaniach na podstawie wierszy podumów. |
| Opis | Krótki opis usług kupowanych w ramach wiersza podumowy. |Brak |
| Typ linii |   Wartość domyślna tego pola to **Na podstawie ilości**.| Brak |
| Metoda rozliczania | Jest to zestaw opcji reprezentujący dwa główne modele umów obsługiwane przez program Project Operations: **Stała cena** i **Czas i materiały**. | Na podstawie wybranej formy rozliczenia zostanie udostępniony harmonogram faktur opartych na punktach kontrolnych dla wierszy podumowy ze stałą ceną formy rozliczenia. |
| Klasa transakcji | Wartość domyślna to **Czas**. | Oznacza to, że wiersz podumowy jest używany do rejestrowania zakupu czasu podwykonawcy. |
| Rola | Wybierz rolę zasobów podumowy, których czas jest nabywany. | Rola wykonana przez zasoby podumowy określa koszt zakupu. |
| Żądane rozpoczęcie | Wprowadź datę rozpoczęcia pracy zasobów podwykonawcy. | Służy to do wyboru cennika projektu z cenników projektu dołączonych do podumowy. Koszt roli w wierszu podumowy pochodzi z tego cennika. |
| Żądane zakończenie | Wprowadź datę zakończenia przypisania zasobu podwykonawcy. | Będzie on używany do pokazywania ostrzeżeń, gdy menedżer projektu będzie pobierać z pojemności wymagań zasobów występujących po tej dacie. |
| Ilość zamówiona | Wprowadź liczbę godzin roli zakupionych od dostawcy. | Będzie on używany do pokazywania ostrzeżeń, gdy menedżer projektu będzie pobierać zbyt wiele z tej pojemności wymagań zasobów. |
| Grupa jednostek | Domyślna wartość to **Grupa jednostek czasu**, której nie można zmienić. | Brak|
| Jednostka | Domyślną jednostką tego pola jest podstawowa jednostka godzin z **Grupy jednostek czasu**. Można zmienić tę wartość, aby kupić dowolną jednostkę z **Grupy jednostek czasu**, na przykład dzień lub tydzień. | Kombinacja **Roli** i **Jednostki** zostanie użyta jako domyślna lub obliczona dla ceny jednostkowej dla wiersza podumowy. |
| Cena jednostkowa | Domyślna cena jednostkowa wykorzystuje kombinację **Roli** i **Jednostki** z cennika projektu, który ma zastosowanie do dany **Żądanego rozpoczęcia** wiersza podumowy. | Jeśli dla odpowiedniego cennika projektu cena jest ustawiona w innej jednostce niż jednostka z wiersza podumowy, system używa konwersji jednostek do obliczenia ceny jednostkowej. |
| Suma częściowa |    Jest to pole tylko do odczytu obliczane jako cena jednostkowa x ilość, jeśli wprowadzono zarówno wartość jednostkową, jak i ilość. Jeśli pole ilości, ceny jednostkowej lub oba te pola są puste, można wprowadzić wartość w polu. | Brak|
| Podatek |   Wprowadź kwotę podatku. |Brak |
| Łączna kwota | Łączna kwota pozycji podumowy z uwzględnieniem podatku. To pole jest obliczane jako Suma częściowa + Podatek.|Brak |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]