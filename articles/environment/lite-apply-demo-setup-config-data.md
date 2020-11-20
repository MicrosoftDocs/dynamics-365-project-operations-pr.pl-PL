---
title: Zastosowanie konfiguracji demonstracyjnej i danych konfiguracyjnych — wersja uproszczona
description: W tym temacie zamieszczono informacje dotyczące sposobu stosowania konfiguracji demonstracyjnej i danych konfiguracyjnych Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5cfc270c07a568d692f6cd180b9c367ae185044c
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401276"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Zastosowanie konfiguracji demonstracyjnej i danych konfiguracyjnych dla Project Operations — wersja uproszczona 

_**Wdrażanie uproszczone — od oferty do faktury pro forma_

## <a name="prerequisites"></a>Wymagania wstępne

Przed rozpoczęciem konfiguracji należy dysponować środowiskiem Common Data Service (CDS) dla Dynamics 365 Project Operations.


## <a name="instructions"></a>Instrukcje

1. Pobierz [pakiet Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip). 
2. Przejdź do folderu *ProjOpsDemoDataSetupAndMaster - Integrated CMT*, a następnie uruchom plik wykonywalny *DataMigrationUtility*.
3. Na stronie 1 Kreatora migracji konfiguracji Common Data Service (CMT) wybierz pozycję **Importuj dane**, a następnie wybierz pozycję **Kontynuuj**.

![Migracja konfiguracji](./media/1ConfigurationMigration.png)

4. Na stronie 2 kreatora CMT wybierz **Microsoft 365** jako **Typ wdrożenia**.
5. Wybierz pola wyboru **Wyświetl listę dostępnych organizacji** i **Wyświetl zaawansowane**.
6. Wybierz region dzierżawy, wprowadź swoje poświadczenia, a następnie wybierz pozycję **Zaloguj**.

![Konfiguracja logowania](./media/2ConfigurationSignin.png)

7. Na stronie 3 z poziomu listy organizacji w dzierżawie wybierz nazwę organizacji, do której chcesz zaimportować dane demonstracyjne, a następnie wybierz pozycję **Zaloguj**.
8. Na stronie 4 wybierz plik zip *MasterAndSetupData*, który znajduje się w rozpakowanym folderze *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.

![Plik ZIP](./media/3ZipFile.png)

![Wybierz plik](./media/4SelectAFile.png)

9. Po zaznaczeniu pliku zip wybierz pozycję **Importuj dane**.

![Importuj dane](./media/5ImportData.png)

10. Importowanie potrwa około dwóch sekund, w zależności od szybkości sieci. Po zakończeniu pracy zakończ działanie kreatora CMT. 
11. Należy sprawdzić w ramach organizacji dane z następujących 20 encji:

-   Waluta
-   Konto
-   Jednostka organizacyjna
-   Kontakt biznesowy
-   Grupa podatku
-   Grupa klientów
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

![Zakończ importowanie](./media/6CompleteImport.png)
