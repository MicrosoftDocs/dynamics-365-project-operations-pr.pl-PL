---
title: Zastosowanie konfiguracji demonstracyjnej i danych konfiguracyjnych — wersja uproszczona
description: W tym artykule przedstawiono informacje na temat stosowania pokazowych danych instalacji i konfiguracji w aplikacji Project Operations.
author: sigitac
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8ac8c910ce2d91fa47df08e8fb6efb723c0dc5fa
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811039"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Zastosowanie konfiguracji demonstracyjnej i danych konfiguracyjnych dla Project Operations — wersja uproszczona 

_**Wdrażanie uproszczone — od oferty do faktury pro forma_



## <a name="prerequisites"></a>Wymagania wstępne

Przed rozpoczęciem konfiguracji należy dysponować środowiskiem usługi Dataverse ustanowionym dla aplikacji Dynamics 365 Project Operations.


## <a name="instructions"></a>Instrukcje

1. Pobierz [Pakiet konfiguracji danych](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
1. Przejśdź do folderu *ProjOpsSampleSetupData - CE only CMT* i uruchom plik wykonywalny, *DataMigrationUtility*.
1. Na stronie 1 Kreatora migracji konfiguracji Common Data Service (CMT) wybierz pozycję **Importuj dane**, a następnie wybierz pozycję **Kontynuuj**.

    ![Migracja konfiguracji.](./media/1ConfigurationMigration.png)

1. Na stronie 2 kreatora CMT wybierz **Microsoft 365** jako **Typ wdrożenia**.
1. Wybierz pola wyboru **Wyświetl listę dostępnych organizacji** i **Wyświetl zaawansowane**.
1. Wybierz region dzierżawy, wprowadź swoje poświadczenia, a następnie wybierz pozycję **Zaloguj**.

   ![Konfiguracja logowania.](./media/2ConfigurationSignin.png)

1. Na stronie 3 z poziomu listy organizacji w dzierżawie wybierz nazwę organizacji, do której chcesz zaimportować dane demonstracyjne, a następnie wybierz pozycję **Zaloguj**.
1. Na stronie 4 wybierz plik zip, *SampleSetupAndConfigData* z rozpakowanego folderu, *ProjOpsSampleSetupData - CE only CMT*.

   ![Plik ZIP.](./media/3ZipFile.png)

   ![Wybierz plik.](./media/4SelectAFile.png)

1. Po zaznaczeniu pliku zip wybierz pozycję **Importuj dane**.

   ![Importuj dane.](./media/5ImportData.png)

1. Importowanie potrwa około dwóch sekund, w zależności od szybkości sieci. Po zakończeniu pracy zakończ działanie kreatora CMT. 
1. Należy sprawdzić w ramach organizacji dane z następujących 18 encji:

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
