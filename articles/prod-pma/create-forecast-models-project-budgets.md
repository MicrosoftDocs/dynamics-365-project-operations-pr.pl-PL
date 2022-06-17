---
title: Tworzenie modeli prognoz dla budżetów projektów
description: W tym artykule opisano sposób tworzenia modelu prognozy dla pozostałych budżetów.
author: Yowelle
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: e6b1419c41124d2062595f7346efb7538e50ee33
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916715"
---
# <a name="create-forecast-models-for-project-budgets"></a>Tworzenie modeli prognoz dla budżetów projektów 

[!include [banner](../includes/banner.md)]

W tym artykule opisano sposób tworzenia modelu prognozy dla pozostałych budżetów. W projekcie, który jest objęty kontrolą budżetu, są używane dwa typy budżetów: początkowy i pozostały. Podczas tworzenia budżetu projektu należy określić modele prognoz budżetu pierwotnego i pozostałego utworzone na stronie **Modele prognozy**. Budżety projektu oparte na określonych modelach są tworzone podczas zatwierdzania budżetu projektu.

> [!NOTE]
> Model prognozy używany w przypadku kontroli budżetu nie może mieć pod-modelu ani być używanym w ramach pod-modelu.

1. Wybierz **Zarządzanie projektem i księgowanie** > **Konfiguracja** > **Prognozy**  > **Modele prognozowania**.
2. Wybierz opcję **Nowy**, aby utworzyć nowy model prognozy, a następnie wprowadź numer identyfikatora i nazwę nowego modelu. 
3. Ustawienie opcji **Zatrzymane** na **Tak** powoduje, że nie są wprowadzane żadne zmiany w wierszach prognozy dla modelu prognozy. 
4. Jeśli wiersze prognozy, z którymi jest skojarzony model, powinny generować prognozy przepływów pieniężnych w księdze głównej, należy ustawić pole **Dodaj do prognoz przepływów pieniężnych** na wartość **Tak**. 
5. Aby użyć daty projektu jako daty faktury, ustaw wartość w polu **Prognozowanie daty faktury** na **Tak**. 
6. W polu **Typ budżetu** wybierz jeden z następujących typów modeli:

   - **Budżet początkowy**: Użyj kwot z budżetu początkowego podanych podczas tworzenia i zatwierdzania budżetu początkowego.
   - **Pozostały budżet**: Użyj kwot z pozostałego budżetu w czasie trwania projektu. Salda w tym modelu prognozy są redukowane o rzeczywiste transakcje, zwiększane lub zmniejszane na podstawie korekt budżetu.
   - **Przeniesienie na następny okres**: Użyj kwot budżetu przeniesienia na następny okres w projekcie. Przeniesienie na następny okres jest procesem opcjonalnym, który można uruchomić w celu przeniesienia niewykorzystanych kwot budżetu z jednego roku obrachunkowego do innego.

7. W razie potrzeby określ następujące opcje:

   - Aby użyć daty projektu jako daty faktury, włącz **Prognozowanie daty faktury**.
   - Włącz **Prognozę PWT** na podstawie pracy w toku (PWT), a następnie wybierz typ PWT. 
   - Można zachować domyślny **Typ budżetu** jako **Brak** lub wprowadzić nowy typ. Nie można zmienić typu budżetu po zmianie rekordu.     
    > [!NOTE]
    > Zmiana domyślnego typu budżetu spowoduje, że wszystkie pozostałe opcje staną się niedostępne do aktualizacji i nie będzie można korzystać z tego modelu prognozy. 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]