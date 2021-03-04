---
title: Tworzenie rozwiązania dla niestandardowych wymiarów kalkulacji cen
description: W tym temacie zamieszczono informacje dotyczące sposobu tworzenia rozwiązań obsługujących niestandardowe wymiary kalkulacji cen.
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 441501dff23d16960381b3f9fb4b2cceba2b3ba5
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/12/2020
ms.locfileid: "4514011"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a>Tworzenie rozwiązania dla niestandardowych wymiarów kalkulacji cen

 _**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_ 

>[!IMPORTANT]
>Wszystkie zmiany wymiarów niestandardowych cen są dostępne w odrębnym rozwiązaniu. Ta ważna najlepsza praktyka umożliwia elastyczne wprowadzanie aktualizacji lub usuwanie zmian w razie potrzeby, pomaga wykorzystywać utworzoną pracę do innych celów oraz ułatwia przenoszenie zmian do innych wystąpień. Po wprowadzeniu wszystkich wymaganych zmian należy wyeksportować to rozwiązanie jako rozwiązanie **zarządzane**, a następnie je zaimportować do innych wystąpień w celu ponownego używania.

## <a name="create-a-solution-for-custom-pricing-dimensions"></a>Tworzenie rozwiązania dla niestandardowych wymiarów kalkulacji cen

1.  Wybierz przycisk **Ustawienia** > **Rozwiązania**, a następnie wybierz pozycję **Nowe**.
2.  Nazwij rozwiązanie *Wymiary kalkulacji cen organizacji <your organization name>*.
3. Wprowadź pozostałe wymagane informacje, a następnie wybierz **Zapisz**.

  ![Tworzenie rozwiązania do obsługi niestandardowych wymiarów kalkulacji cen](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Dodawanie wszystkich wymaganych encji i pokrewnych składników do rozwiązania wymiarami cen

Dodaj następujące encje aplikacji Project Service do rozwiązania obsługującego kalkulację cen, aby wprowadzić ważne zmiany schematu w rozwiązaniu obsługującym kalkulację cen. Po zakończeniu tej procedury encje będą rozpoznawać nowe wymiary kalkulacji cen.

1.  Wybierz pozycje **Ustawienia** > **Rozwiązania**, a następnie kliknij dwukrotnie pozycję **<*nazwa Twojej organizacji*> — wymiary kalkulacji cen**.
2.  W Eksploratorze rozwiązań w lewym okienku nawigacji kliknij kolejno opcje **Dodaj istniejący** > **Encje**.
3.  W oknie dialogowym **Składniki rozwiązania** zaznacz następujące encje:
 
   - **Rzeczywiste**
   - **Zasób, który można zarezerwować**
   - **Wiersz szacowania**
   - **Zadanie projektu**
   - **Szczegóły wiersza faktury**
   - **Wiersz arkusza**
   - **Szczegóły pozycji kontraktu projektu**
   - **Członek zespołu projektu**
   - **Szczegóły wiersza oferty**
   - **Narzut na cenę dla roli**
   - **Cena roli**
   - **Wpis czasu**
 
   ![Dodawanie istniejących encji do rozwiązania do obsługi niestandardowych wymiarów kalkulacji cen](./media/Existing-entities-to-PD-solution.png)
 
 4. Dla każdej encji przejrzyj dodawane składniki i ostateczną listę zasobów dla każdej encji. 

   >[!NOTE]
   > Uwzględnij wszystkie formularze i widoki dla każdej wybranej encji.

  ![Dodano encje](./media/solution-component-selection.png)


5.  Po wyświetleniu monitu o uwzględnienie dowolnych encji zależnych dla wybranych encji wybierz opcję **Nie, nie należy dołączać składników wymaganych.**

    ![Z uwzględnieniem encji zależnych](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]