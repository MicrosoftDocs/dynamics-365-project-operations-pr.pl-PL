---
title: Zastosowanie konfiguracji demonstracyjnej i danych konfiguracyjnych — wersja uproszczona
description: W tym temacie zamieszczono informacje dotyczące sposobu stosowania konfiguracji demonstracyjnej i danych konfiguracyjnych Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ecb5da3bccf35f8ed7e2246f68dd4da2b145c6be
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587001"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Zastosowanie konfiguracji demonstracyjnej i danych konfiguracyjnych dla Project Operations — wersja uproszczona 

_**Wdrażanie uproszczone — od oferty do faktury pro forma_



## <a name="prerequisites"></a>Wymagania wstępne

Przed rozpoczęciem konfiguracji należy dysponować środowiskiem usługi Common Data Service (CDS) ustanowionym dla aplikacji Dynamics 365 Project Operations.


## <a name="instructions"></a>Instrukcje

1. Pobierz [pakiet Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
2. Przejśdź do folderu *ProjOpsSampleSetupData - CE only CMT* i uruchom plik wykonywalny, *DataMigrationUtility*.
3. Na stronie 1 Kreatora migracji konfiguracji Common Data Service (CMT) wybierz pozycję **Importuj dane**, a następnie wybierz pozycję **Kontynuuj**.

    ![Migracja konfiguracji.](./media/1ConfigurationMigration.png)

4. Na stronie 2 kreatora CMT wybierz **Microsoft 365** jako **Typ wdrożenia**.
5. Wybierz pola wyboru **Wyświetl listę dostępnych organizacji** i **Wyświetl zaawansowane**.
6. Wybierz region dzierżawy, wprowadź swoje poświadczenia, a następnie wybierz pozycję **Zaloguj**.

   ![Konfiguracja logowania.](./media/2ConfigurationSignin.png)

7. Na stronie 3 z poziomu listy organizacji w dzierżawie wybierz nazwę organizacji, do której chcesz zaimportować dane demonstracyjne, a następnie wybierz pozycję **Zaloguj**.
8. Na stronie 4 wybierz plik zip, *SampleSetupAndConfigData* z rozpakowanego folderu, *ProjOpsSampleSetupData - CE only CMT*.

   ![Plik ZIP.](./media/3ZipFile.png)

   ![Wybierz plik.](./media/4SelectAFile.png)

9. Po zaznaczeniu pliku zip wybierz pozycję **Importuj dane**.

   ![Importuj dane.](./media/5ImportData.png)

10. Importowanie potrwa około dwóch sekund, w zależności od szybkości sieci. Po zakończeniu pracy zakończ działanie kreatora CMT. 
11. Należy sprawdzić w ramach organizacji dane z następujących 18 encji:

    -   Waluta
    -   Konto
    -   Jednostka organizacyjna
    -   Kontakt
    -   Jednostka
    -   Grupa jednostek
    -   Cennik
    -   Cennik parametrów projektu 
    -   Częstotliwość faktur
    -   Kategoria zasobów, które można zarezerwować
    -   Kategoria transakcji
    -   Kategoria wydatków
    -   Cena roli
    -   Cena kategorii transakcji
    -   Charakterystyka
    -   Zasób, który można zarezerwować
    -   Skojarzenie kategorii zasobów, które można zarezerwować
    -   Charakterystyka zasobu, który można zarezerwować

    ![Zakończ importowanie.](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
