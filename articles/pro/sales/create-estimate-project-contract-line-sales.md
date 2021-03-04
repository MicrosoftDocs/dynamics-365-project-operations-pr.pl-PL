---
title: Szacowanie pozycji kontraktu opartego na projekcie - wersja uproszczona
description: Ta temat zawiera informacje na temat oszacowań w pozycji kontraktu opartej na projekcie.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2d0d8309fcb4300e33ed2f5933259f99ad7e0d6a
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180430"
---
# <a name="estimate-a-projectbased-contract-line---lite"></a>Szacowanie pozycji kontraktu opartego na projekcie - wersja uproszczona

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

W Dynamics 365 Project Operations pozycja kontraktu oparta na projektach zawiera szczegółowe informacje pomocne w oszacowaniu kosztu i potencjalnego przychodu pozostałej pracy związanej z pozycjami kontraktu.

Aby oszacować pozycje kontraktu oparte na projektach, przejdź do karty **Szczegóły pozycji kontraktu** w **Pozycji kontraktu** projektu.  Istnieją dwa sposoby tworzenia oszacowania w pozycji kontraktu opartym na projekcie:

   - Aby utworzyć szacowaną bezpośrednio w pozycji kontraktu, należy ręcznie dodać szczegóły pozycji kontraktu.
   - Utworzenie projektu i planu projektu, a następnie skojarzenie projektu i zadań z pozycją kontraktu projektu. Umożliwia to proces importowania oszacowania planu projektu do pozycji kontraktu na podstawie składników zawartych w pozycji kontraktu.

## <a name="create-an-estimation-directly-on-a-projectbased-contract-line"></a>Tworzenie oszacowania bezpośrednio w pozycji kontraktu opartego na projekcie

1. Przejdź do pozycji kontraktu i wybierz kartę **Szczegóły pozycji kontraktu** . Wiersze utworzone na tej karcie są sumowane i wyświetlane jako **Wartość kontraktu** dla danej **Pozycji kontraktu**. 
2. W podsiatce **Szczegóły pozycji kontraktu** wybierz pozycję **+ Nowe szczegóły pozycji kontraktu**. Zostanie otwarty suwak szybkiego tworzenia. W formularzu **szczegóły pozycji kontraktu** są dostępne następujące pola:

| Pole | Lokalizacja | Opis | Wpływ zmian w dalszych etapach |
| --- | --- | --- | --- |
| **Opis** | **Szybkie tworzenie** | Opis terminu konkretnego oszacowania. | W tym polu są domyślnie wyświetlane szczegóły dotyczące powiązanych wierszy kontraktu dla kosztów, które są automatycznie tworzone. |
| **Klasa transakcji** | **Szybkie tworzenie** | Ta lista rozwijana jest listą klas transakcji uwzględnionych na karcie **Ogólne** w pozycji kontraktu opartej na projektach. | W tym polu są domyślnie wyświetlane szczegóły dotyczące powiązanych wierszy kontraktu dla kosztów, które są automatycznie tworzone. |
| **Rola** | **Szybkie tworzenie** | Rola osoby wykonującej prace lub korzystającej z tego wydatku. | W tym polu są domyślnie wyświetlane szczegóły dotyczące powiązanych wierszy kontraktu dla kosztów, które są automatycznie tworzone. |
| **Kategoria** | **Szybkie tworzenie** | Kategoria pracy lub wydatku. | W tym polu są domyślnie wyświetlane szczegóły dotyczące powiązanych wierszy kontraktu dla kosztów, które są automatycznie tworzone. |
| **Data rozpoczęcia** | **Szybkie tworzenie** | Data rozpoczęcia pracy. | W tym polu są domyślnie wyświetlane szczegóły dotyczące powiązanych wierszy kontraktu dla kosztów, które są automatycznie tworzone. |
| **Data zakończenia** | **Szybkie tworzenie** | Data zakończenia pracy. | W tym polu są domyślnie wyświetlane szczegóły dotyczące powiązanych wierszy kontraktu dla kosztu, który jest automatycznie tworzony. |
| **Jednostka zasobów** | **Szybkie tworzenie** | Jednostka pozyskania, która ponosi koszt i określa zasób, który ma nad nim pracować. | W tym polu są domyślnie wyświetlane szczegóły dotyczące powiązanych wierszy kontraktu dla kosztów, które są automatycznie tworzone. To pole jest również używane podczas pobierania kosztu własnego. |
| **Harmonogram jednostek** | **Szybkie tworzenie** | Grupa jednostek pracy lub kosztów. Jednostki należą do harmonogramu jednostek lub grupy jednostek. Na przykład *mile* i *kilometry (KMS)* to jednostki należące do grupy jednostek, które opisują odległość. | W tym polu są domyślnie wyświetlane szczegóły dotyczące powiązanych wierszy kontraktu dla kosztów, które są automatycznie tworzone. |
| **Jednostka** | **Szybkie tworzenie** | Grupa jednostek pracy lub kosztów. | W tym polu są domyślnie wyświetlane szczegóły dotyczące powiązanych wierszy kontraktu dla kosztów, które są automatycznie tworzone. |
| **Ilość** | **Szybkie tworzenie** | Ilość jednostek pracy lub kosztów. | W tym polu są domyślnie wyświetlane szczegóły dotyczące powiązanych wierszy kontraktu dla kosztów, które są automatycznie tworzone. |
| **Cena jednostkowa** | **Szybkie tworzenie** | Współczynnik sprzedaży roli, która wykonuje pracę, lub cenę zakupu w danej kategorii wydatkowej. To pole jest domyślnie ustawione na **Czas** na podstawie kombinacji roli i jednostki zasobów znajdującej się na cenniku projektu, która obowiązuje w stosunku do daty rozpoczęcia. W przypadku kosztów wartość tego pola jest domyślna określana na podstawie konfiguracji ceny w danej kategorii transakcji w cenniku projektu, która obowiązuje w stosunku do daty rozpoczęcia. Jeśli w kategorii transakcji wybrana jest inna metoda kalkulacji cen niż **cena jednostkowa**, nie zostanie zastosowana wartość domyślna, a to pole pozostanie puste. | Stawka kosztów roli, która wykonuje pracę, lub koszt na jednostkę kategorii wydatków. To pole jest domyślnie ustawiane na **Czas w zależności od roli** oraz kombinacji jednostkowej ponownej sprzedaży w wierszu ceny roli na liście kosztów podanych w polu Data rozpoczęcia załączonym do Umawiającej się jednostki, która obowiązuje. W przypadku wydatków wartość domyślna tego pola jest oparta na wierszu ceny kategorii w cenniku własnym dołączonym do jednostki umownej, która obowiązuje od daty rozpoczęcia. Jeśli w kategorii transakcji wybrana jest inna metoda kalkulacji cen niż cena jednostkowa, nie zostanie zastosowana wartość domyślna, a to pole pozostanie puste. |
| **Szacowany podatek** | **Szybkie tworzenie** | Szacunkowy podatek dla tej pracy lub wydatku wyrażony jako wejściowy przez użytkownika. | Szacunkowy podatek dla tej pracy lub wydatku wyrażony jako wejściowy przez użytkownika. |
| **Kwota** | **Szybkie tworzenie** | Tę wartość w tym polu może dodać użytkownik, jeśli pola **Ilość** i **Cena** pozostaną niewypełnione. Jeśli **ilość** i **Cena** są wypełnione, pole **Kwoty** jest przeznaczone tylko do odczytu i jest obliczane jako **(Ilość \* Cena jednostkowa) + podatek**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Aktualizowanie cen w wierszach kontraktu

W przypadku zmiany cen w cenniku projektu, które są dołączone do kontraktu lub cennika kosztów na jednostkę zamawiającą, można odświeżyć ceny w poszczególnych wierszach kontraktu w celu odzwierciedlenia zmian. Na stronie **Kontrakt** wybierz pozycję **Oblicz ponownie**. Zostanie wyświetlone ostrzeżenie informujące o tym, że wszystkie pozycje kontraktu dotyczące kontraktu są resetowane. Wybierz opcję **Tak**, aby odświeżyć ceny zarówno dla sprzedaży, jak i dla wierszy kontraktu kosztowego.

## <a name="access-contract-line-details-for-cost"></a>Dostęp do szczegółów wiersza kontraktu dostępu

Z poziomu karty **Szczegóły pozycji kontraktu** wybierz wiersz w siatce, aby wyświetlić niektóre akcje na pasku narzędzi w podsiatce. Pierwsza akcja na pasku narzędzi w podsiatce powoduje **Otwarcie szczegółów kosztów**. Aby wyświetlić pokrewną stawkę kosztów i kwotę dotyczącą szczegółów danego wiersza kontraktu, wybierz pozycję **Otwarcie szczegółów kosztów**. 

> [!NOTE]
> Zmiana wartości składnika reźródłem, przekroczenie jednostki, ilość, daty, rola lub kategoria w pozycji kontraktu szczegóły dotyczące **Koszt** spowoduje zmianę odpowiednich wartości w szczegółach pozycji kontraktu dotyczącej **Sprzedaży**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Waluta w wierszu kontraktu szczegóły dotyczące kosztów i sprzedaży

Szczegóły wiersza kontraktu dla **Sprzedaży** ustawiają domyślną walutę z cennika projektu, która obowiązuje od daty rozpoczęcia szczegółów wiersza kontraktu.

Szczegóły wiersza kontraktu dla **Kosztu** ustawiają domyślną walutę z cennika jednostki kontraktu, która obowiązuje od daty rozpoczęcia szczegółów wiersza kontraktu dla **Kosztu**.

Obliczenia rentowności konwertują kwoty dla szczegółów pozycji kontraktu dotyczące **Kosztów** i **Sprzedaży** w walutę podstawową środowiska, aby raportować ogólne i szacowane marginesy kontraktu.

> [!NOTE]
> Błędy zaokrąglania walut i zmienione marginesy mogą nastąpić z powodu braku aktualnych kursów wymiany. Te obliczenia są stosowane w kontraktach dotyczących projektów wyłącznie jako przybliżenia, a nie w stosunku do rzeczywistych lub innych raportów, które wymagają wyższego dokładność zaokrąglania i świadomości daty effectivity dla kursów wymiany.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]