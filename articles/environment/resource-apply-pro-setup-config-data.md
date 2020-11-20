---
title: Skonfiguruj i zastosuj dane konfiguracyjne w usłudze Common Data Service
description: W tym temacie zamieszczono informacje dotyczące ustawienia i zastosowania danych konfiguracyjnych Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7de8db5e91265c77c79f34a513bf27d9a55b789a
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401141"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a>Skonfiguruj i zastosuj dane konfiguracyjne w usłudze Common Data Service 

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

## <a name="prerequisites"></a>Wymagania wstępne

Przed przystąpieniem do konfigurowania danych z Common Data Service (CDS) muszą spełnione następujące wymagania wstępne:

1.  Udostępnij środowisko CDS i środowisko Dynamics 365 Finance na potrzeby Project Operations.
2.  Informacje o osobach prawnych z Dynamics 365 Finance są udostępniane środowisku CDS. Oznacza to, że **Firma** z CDS zawiera następujące rekordy firm:
  - THPM
  - USPM
  - GBPM

## <a name="install-setup-and-configuration-data"></a>Zainstaluj konfigurację i dane konfiguracyjne

1. Pobierz, odblokuj i rozpakuj [pakiet danych instalacyjnych i konfiguracyjnych](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).
2. Przejdź do wyodrębnionego folderu, a następnie uruchom plik wykonywalny *DataMigrationUtility*.
3. Na stronie 1 Kreatora migracji konfiguracji Common Data Service (CMT) wybierz pozycję **Importuj dane**, a następnie wybierz pozycję **Kontynuuj**.

![Migracja konfiguracji](./media/1ConfigurationMigration.png)

4. Na stronie 2 kreatora CMT wybierz **Microsoft 365** jako **Typ wdrożenia**.
5. Wybierz pola wyboru **Wyświetl listę dostępnych organizacji** i **Wyświetl zaawansowane**.
6. Wybierz region dzierżawy, wprowadź swoje poświadczenia, a następnie wybierz pozycję **Zaloguj**.

![Konfiguracja logowania](./media/2ConfigurationSignin.png)

7. Na stronie 3 z poziomu listy organizacji w dzierżawie wybierz nazwę organizacji, do której chcesz zaimportować dane demonstracyjne, a następnie wybierz pozycję **Zaloguj**.
8. Na stronie 4 wybierz plik zip *SampleSetupAndConfigData*, który znajduje się w rozpakowanym folderze.

![Wybieranie pliku zip](./media/3ZipFile.png)

![Wybierz plik](./media/4SelectAFile.png)

9. Po zaznaczeniu pliku zip wybierz pozycję **Importuj dane**.

![Importuj dane](./media/5ImportData.png)

10. Importowanie potrwa około dwóch sekund, w zależności od szybkości sieci. Po zakończeniu importu zakończ działanie kreatora CMT. 
11. Należy sprawdzić w ramach organizacji dane z następujących 19 encji:

  - Waluta
  - Jednostka organizacyjna
  - Kontakt biznesowy
  - Grupa podatku
  - Grupa klientów
  - Jednostka
  - Grupa jednostek
  - Cennik
  - Cennik parametrów projektu
  - Częstotliwość faktur
  - Kategoria zasobów, które można zarezerwować
  - Kategoria transakcji
  - Kategoria wydatków
  - Cena roli
  - Cena kategorii transakcji
  - Charakterystyka
  - Zasób, który można zarezerwować
  - Skojarzenie kategorii zasobów, które można zarezerwować
  - Charakterystyka zasobu, który można zarezerwować

![Zakończ importowanie](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a>Aktualizowanie konfiguracji Project Operations

1. Przejdź do środowiska CE. Można je znaleźć otwierając [centrum administracyjne Power Platform](https://admin.powerplatform.microsoft.com/environments), wybierając środowisko i wybierając pozycję **Otwórz środowisko**. 

![Otwórz środowisko](./media/7OpenEnvironment.png)

2. Przejdź do obszaru **Projekty** > **Zasoby** i wybierz opcję **Nowy**, aby utworzyć zasób zaksięgowany dla użytkownika.

![Zasoby, które można zarezerwować](./media/8BookableResources.png)

3. Na karcie **Ogólne** wybierz użytkownika administracyjnego. Sprawdź, czy strefa czasowa jest zgodna z strefą, w której się znajdujesz. 

![Nowy zasób, który można zarezerwować](./media/9NewBookableResource.png)

4. Na karcie **Planowanie**, w polu **Firma** wybierz firmę **USPM**, a następnie wybierz pozycję **Zapisz**. 

![Karta planowania](./media/10SchedulingTab.png)

5. Wybierz kartę **Godziny pracy**.  

![Godziny pracy](./media/11WorkHours.png)

6. Kliknij dwukrotnie dowolną wartość w kalendarzu i wybierz pozycję **Edytuj** > **Wszystkie zdarzenia z serii**. 

![Kalendarz pracy](./media/12WorkCalendar.png)

7. Zmień godziny pracy na osiem (8) godzin w trakcie dnia pracy i zaznacz weekendy jako dni wolne od pracy i upewnij się, że strefa czasowa odpowiada Twojej. 
8. Wybierz **Zapisz i zamknij**.

![Aktualizacja kalendarza](./media/13UpdateCalendar.png)

9. Wybierz kolejno pozycje **Ustawienia** > **Szablony kalendarza** i utwórz **Nowy**.
 
 ![Szablony kalendarzy](./media/14CalendarTemplates.png)
 
 10. Wprowadź nazwę, zaznacz utworzony szablon zasobu, a następnie wybierz pozycję **Zapisz**. 
 
 ![Zapisz szablon kalendarza](./media/15SaveCalendarTemplate.png)
 
 11. Przejdź do obszaru **Parametry** i kliknij dwukrotnie rekord. 
 
 ![Parametry projektu](./media/16ProjectParameters.png)
 
12. Zaktualizuj następujące pola:

 - **Domyślna firma**: USPM
 - **Domyślna jednostka organizacyjna**: Contoso Robotics Global
 - **Częstotliwość fakturowania**: siódmy i ostatni dzień
 - **Szablon godzin pracy**: Zmień na utworzony szablon.

13. Wybierz pozycję **Zapisz**. 

![Zaktualizowane parametry projektu](./media/17UpdatedProjectParameters.png)
