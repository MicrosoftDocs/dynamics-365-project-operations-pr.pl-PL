---
title: Tworzenie niestandardowych rozwiązań dla wymiarów kalkulacji cen
description: W tym temat wyjaśniono sposób tworzenia niestandardowego rozwiązania podczas tworzenia niestandardowych wymiarów kalkulacji cen.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3e437fce5b9f1fb330a713788e24100a4fe02948
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082021"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>Tworzenie niestandardowych rozwiązań dla wymiarów kalkulacji cen

> [!IMPORTANT]
> Wszystkie zmiany wymiarów niestandardowych cen są dostępne w odrębnym rozwiązaniu. Ta ważna najlepsza praktyka zapewnia elastyczność umożliwiającą w przyszłości wprowadzanie aktualizacji lub usuwanie zmian w razie potrzeby, pomaga wykorzystywać utworzone obiekty do innych celów oraz ułatwia przenoszenie zmian do innych wystąpień. Po wprowadzeniu wymaganych zmian należy wyeksportować rozwiązanie jako **Rozwiązanie zarządzane** , a następnie je zaimportować do innych wystąpień i tam wykorzystywać.

1. Wybierz przycisk **Ustawienia** > **Rozwiązania** , a następnie wybierz pozycję **Nowe**. 
2. Nazwij rozwiązanie **\<your organization name>nazwa Twojej organizacji> — wymiary kalkulacji cen** , wprowadź pozostałe wymagane informacje, a następnie wybierz **Zapisz**.

> ![Tworzenie niestandardowego rozwiązania dla wymiarów kalkulacji cen](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Dodawanie wszystkich wymaganych encji i pokrewnych składników do rozwiązania wymiarami cen
Następujące encje usługi Project Service trzeba będzie dodać do rozwiązania do zarządzania wymiarami kalkulacji cen. Czynności opisane w tej procedurze umożliwiają wprowadzenie pewnych istotnych zmian w schemacie rozwiązania do zarządzania kalkulacjami cen, tak aby encje dowiedziały się o nowych wymiarach kalkulacji cen.

1. Wybierz **Ustawienia** > **Rozwiązania** , a następnie kliknij dwukrotnie opcję **Wymiary kalkulacji cen \<your organization name>**. 
2. W Eksploratorze rozwiązań w lewym okienku nawigacji kliknij kolejno opcje **Dodaj istniejący** > **Encje**.
3. W oknie dialogowym **Składniki rozwiązania** zaznacz następujące encje:

- Rzeczywiste
- Zasób, który można zarezerwować
- Wiersz szacowania
- Zadanie projektu
- Szczegóły wiersza faktury
- Wiersz arkusza
- Szczegóły pozycji kontraktu projektu
- Członek zespołu projektu
- Szczegóły wiersza oferty
- Narzut na cenę dla roli
- Cena roli 
- Wpis czasu 

> ![Dodawanie istniejących encji do rozwiązania do zarządzania wymiarami kalkulacji cen](media/Existing-entities-to-PD-solution.png)

> ![Wybieranie składników rozwiązania](media/Dimension-Components.png)

> [!NOTE]
> Upewnić się, dla każdej wybranej encji dołączono wszystkie formularze i widoki.

4. Gdy zobaczysz monit o dodanie wszelkich encji zależnych od zaznaczonych encji, wybierz opcję **Nie**.

> ![Opcja niedołączania pokrewnych składników](media/Do-not-include-required.png)


