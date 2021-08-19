---
title: Przeniesienie budżetów projektu na koniec roku obrachunkowego
description: W tym artykule podano informacje o sposobie przeniesienia pozostałych w budżecie kwot na przyszłe lata oraz utworzenia szczegółowych informacji na temat rejestru budżetu.
author: Yowelle
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 74b2831a19688636f5c4863036adf7043c80d49829737b56c131abb6998d6cb3
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007384"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Przeniesienie budżetów projektu na koniec roku obrachunkowego

[!include [banner](../includes/banner.md)]

Podczas pracy w ramach projektu wieloletniego może się zdarzyć, że w budżecie na końcu roku obrachunkowego pozostały jakieś środki. Pozostałe w budżecie kwoty można przenieść na następny rok i utworzyć szczegółowe informacje dotyczące rejestru budżetu dotyczące kwot w powiązanych kontach księgi głównej. Przed przeniesieniem pozostałej kwoty należy przejrzeć się i zanalizować pozostałe kwoty.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Przegląd i analiza pozostałych w budżecie kwot

Wykonaj poniższe kroki, aby przejrzeć kwoty w budżecie na koniec roku dla projektów, ale nie przenosić kwot na następny okres.

1. Przejdź do **Zarządzania projektami i księgowania** > **Okresowe** > **Budżety** > **Przeniesienie budżetów na następny okres**. 
2. Na stronie **Proces przeniesienia budżetu projektu na następny okres**, na karcie **Opcje końca roku** potwierdź, że pole **Przenoś pozostałe w budżecie kwoty na następny okres** nie jest włączone.
3. Na karcie **Parametry** w polu **Rok budżetowy projektu** zaznacz rok obrachunkowy, dla którego ma zostać wyświetlona pozostała kwota budżetu. 
4. W polu **Rok budżetowy otwarcia** zaznacz rok obrachunkowy, dla którego ma zostać wyświetlona pozostała kwota budżetu. 
5. W polu **Model prognozy** wybierz **Pozostały budżet**. 
6. Aby uwzględnić projekty spełniające wybrane kryteria, które nie mają środków w budżecie, wybierz pozycję **Pokaż pozostałe z zero**.  
7. Na karcie **Wybierz budżety** wybierz pozycję **Pobierz wszystkie budżety**, aby załadować wszystkie budżety spełniające wybrane kryteria, a następnie wybierz pozycję **Przetwórz**. 
8. Aby zaprojektować kwerendę bazy danych zawierającą dany zestaw budżetów w panelu, wybierz pozycję **Pobierz wybrane budżety**.

Aby uzyskać więcej informacji na temat konkretnego wiersza w okienku, zaznacz wiersz i wybierz opcję **Wyświetl szczegóły budżetu** lub **Wyświetl konta**.

## <a name="carry-forward-remaining-budget-amounts"></a>Przenieś na następny okres pozostałe kwoty budżetu 

Podczas przetwarzania pozostałych kwot budżetu można utworzyć transakcje w księdze głównej na kwotę, która ma być przeniesiona na następny okres. Aby utworzyć transakcje księgi głównej, wykonaj kroki opisane w sekcji [Przenoszenie kwot budżetu na następny okres i tworzenie transakcji w ramach księgi głównej](#carry-forward). 

> [!NOTE]
> Kwoty budżetu przeniesione na następny okres są przenoszone do modelu prognozy wybranego na stronie **Modele prognozy** jako model prognozy przeniesienia na następny okres.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Przenoszenie kwot budżetu na następny okres i tworzenie transakcji w ramach księgi głównej

1.  Wybierz **Zarządzania projektami i księgowania** > **Okresowe** > **Budżety** > **Przeniesienie budżetów na następny okres**. 
2. Na stronie **Przeniesienie budżetu projektu na następny okres** wybierz opcję **Koniec roku**, a następnie włącz **Przenoszenie pozostałych kwot budżetu na następny okres** i **Tworzenie wpisów do rejestru budżetu w księdze głównej**. 
3. Na karcie **Parametry** zaznacz grupę wyboru **Parametry projektu**, a następnie wklej w polu następujący kod:

   - **Rok budżetowy projektu**: zaznacz początek roku obrachunkowego, dla którego ma zostać wyświetlona pozostała kwota budżetu. 
   - **Zyski i straty**: w księdze głównej utwórz transakcje zysków i strat. 
   -  **PWT**: tworzenie transakcji prac w toku (PWT) w księdze głównej.
   -  **Lista płac**: tworzenie transakcji alokacji środków w księdze głównej. 

5. W grupie pól **Księga główna** wprowadź następujące informacje: 

   - W polu **Rok budżetowy otwarcia** zaznacz rok obrachunkowy, na którzy chcesz przenieść pozostałą kwotę budżetu. Wartość domyślna wynosi kolejny rok po wartości znajdującej się w polu **Rok budżetowy projektu**.
   -  W polu **Okres przeniesienia** wybierz okres, w którym mają zostać utworzone szczegóły dotyczące rejestru budżetu w księdze głównej. Zazwyczaj jest to pierwszy okres w otwieranym roku obrachunkowym.

6. W grupie pól **Kopiuj z / do** wprowadź następujące informacje:

   - W polu **Model prognozowania** wybierz model prognozy budżetu projektu skojarzony z pozostałymi kwotami budżetów, które mają zostać przeniesione do projektów. 
   - W polu **Docelowy model księgi budżetowej** wybierz model prognozy księgi budżetu skojarzony z pozostałymi kwotami budżetów, które mają zostać przeniesione do księgi głównej. 
   -  Wybierz opcję **Przenieś walutę sprzedaży**, aby użyć waluty sprzedaży projektu na potrzeby transakcji księgi głównej tworzonych przy przenoszeniu kwot budżetu dla projektów. Jeśli opcja ta nie jest wybrana, transakcje korzystają z waluty rozliczeniowej. 
   -  Wybierz opcję **Pokaż pozostałe zera**, aby uwzględnić projekty, które nie mają pozostałych kwot budżetu, ale spełniają inne kryteria wybrane w projektach wyświetlonych w dolnym okienku.

7. Na karcie **Wybierz budżety** wybierz pozycję **Pobierz wszystkie budżety**, aby załadować wszystkie budżety spełniające wybrane kryteria. Jeśli wolisz zaprojektować kwerendę bazy danych zawierającą dany zestaw budżetów projektu w panelu, wybierz pozycję **Pobierz wybrane budżety**.
8. Dla każdego projektu, który ma zostać przetworzony, wybierz opcję na początku wiersza projektu.

    > [!TIP]
    > Aby zaznaczyć wszystkie lub większość projektów, zaznacz pole wyboru znajdujące się w lewym górnym rogu. Aby wykluczyć przetwarzanie dowolnego projektu, wyczyść znacznik wyboru dla tego projektu.

9. Aby przenieść pozostałe kwoty budżetu dla wybranych projektów do wybranego rok obrachunkowy i utworzyć szczegóły dotyczące rejestru budżetu w księdze głównej, wybierz opcję **Przetwórz**.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Przenoszenie kwot budżetu na następny okres bez tworzenia transakcji w ramach księgi głównej

1. Przejdź do **Zarządzania projektami i księgowania** > **Okresowe** > **Budżety** > **Przeniesienie budżetów na następny okres**.
2. Na stronie **Proces przeniesienia budżetu projektu na następny okres**, w polu **Opcje końca roku** wybierz **Przenoś pozostałe w budżecie kwoty na następny okres**.
3. W grupie **Parametry**, w polu **Rok budżetowy projektu** zaznacz rok obrachunkowy, dla którego mają zostać wyświetlone pozostałe kwoty budżetu.
4. W grupie **Kopiuj z / do** wprowadź następujące informacje:

   - W polu **Model prognozowania** wybierz model prognozy budżetu projektu skojarzony z pozostałymi kwotami budżetów, które mają zostać przeniesione do projektów. 
   - Wybierz pozycję **Pokaż pozostałe z zero**, aby uwzględnić projekty spełniające wybrane kryteria, które nie mają środków w budżecie.
   - W grupie **Wybierz budżety** wybierz pozycję **Pobierz wszystkie budżety**, aby załadować wszystkie budżety spełniające wybrane kryteria. Aby zaprojektować kwerendę bazy danych zawierającą dany zestaw budżetów projektów w panelu, wybierz pozycję **Pobierz wybrane budżety**.

5. Dla każdego projektu, który ma zostać przetworzony, wybierz opcję na początku wiersza projektu. 
6. Wybierz opcję **Przetwórz**, aby przenieść pozostałe kwoty budżetu dla wybranych projektów do wybranego rok obrachunkowy.



[!INCLUDE[footer-include](../includes/footer-banner.md)]