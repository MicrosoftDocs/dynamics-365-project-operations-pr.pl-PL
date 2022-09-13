---
title: Tworzenie konta dla subskrypcji w wersji zapoznawczej — wersja uproszczona
description: W tym artykule podano informacje o tym, jak subskrybować i wdrożyć uproszczone wdrożenie aplikacji Project Operations — od okazji do faktury pro forma.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 29bf31cd1bc9c1c5ac757de989154b4c7acc53fe
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410073"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Tworzenie konta dla subskrypcji w wersji zapoznawczej — wersja uproszczona 

W tym artykule wyjaśniono, jak subskrybować ofertę w wersji próbnej i wdrożyć uproszczone wdrożenie aplikacji Dynamics 365 Project Operations — od okazji do faktury pro forma.

> [!NOTE]
> Ten proces będzie się zmieniać w nadchodzących wersjach Project Operations.

## <a name="prerequisites"></a>Wymagania wstępne
- Użytkownik wdrażający wersję zapoznawczą musi posiadać prawa administratora globalnego dzierżawy Azure. Dzierżawcę można utworzyć podczas realizowania pierwszej oferty.

> [!IMPORTANT]
> To zadanie musi wykonać tylko jedna osoba — administrator dzierżawy w organizacji. Jeśli nie jesteś subskrybentem tej wersji, zaczekaj, aż organizacja się zarejestruje i otrzymasz swoje poświadczenia użytkownika.
> 
> Wersje próbne można używać raz w ramach dzierżawcy. Wersję próbną można uruchomić tylko raz. Na potrzeby wersji próbnej zalecamy utworzenie nowego dzierżawcy.

### <a name="dynamics-365-project-operations-trial"></a>Wersja próbna Dynamics 365 Project Operations 

Przed rozpoczęciem pracy należy się upewnić, że użytkownik jest zalogowany w przeglądarce i ma konto pracy użytkownika w dzierżawie, w której ma zostać wyświetlona wersja zapoznawcza Project Operations.

1. Przejdź do tematu [Wersja próbna aplikacji Project Operations](https://aka.ms/try-po), aby zrealizować kod pierwszej oferty, czyli aplikacji **Dynamics 365 Project Operations**.
2. Potwierdź zamówienie.

  Zobaczysz potwierdzenie z informację, że oferta została pomyślnie zrealizowana.

## <a name="assign-licenses"></a>Przypisywanie licencji

> [!IMPORTANT]
> Aby wykonać poniższe kroki, potrzebny jest dostęp administracyjny do portalu Microsoft 365 swojej organizacji.


1. Przejdź do [Centrum administracyjnego Microsoft 365](https://portal.office.com/), aby przypisać licencje do użytkowników.
2. Na stronie **Aktywni użytkownicy** wybierz użytkownika, któremu chcesz przypisać licencję.
3. Sprawdź, czy licencja **Dynamics 365 Project Operations** została wybrana. 
4. Wybierz **Zapisz zmiany**.

## <a name="create-a-new-dataverse-environment"></a>Utwórz nowe środowisko Dataverse

1. Ustanów nowe środowisko wdrażania usługi Project Operations Dataverse zgodnie z instrukcjami podanymi w artykule [Model wdrożenia usługi Dataverse](lite-deployment.md). Podczas wybierania typu środowiska należy pamiętać o użyciu **wersji próbnej (opartej na subskrypcji)**.

  ![Nowe środowisko.](./media/19CreateEnvironment.png)

2. Zaznacz ustawienie **Włącz aplikacje Dynamics 365** i pozostaw pole **Automatycznie wdrażaj te aplikacje** pustym.  
3. Wybierz **Zapisz**, aby utworzyć nowe środowisko.

  ![Dodaj bazę danych.](./media/20CreateEnvironment1.png)

4. Po utworzeniu środowiska zainstaluj rozwiązanie **Microsoft Dynamics 365 Project Operations**. 

![Instalacja rozwiązania.](./media/21InstallSolution.png)

## <a name="set-up-demo-data"></a>Konfigurowanie danych pokazu

Skonfiguruj dane pokazu zgodnie z instrukcjami podanymi w artykule [Zastosowanie pokazowej konfiguracji i danych konfiguracyjnych](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
