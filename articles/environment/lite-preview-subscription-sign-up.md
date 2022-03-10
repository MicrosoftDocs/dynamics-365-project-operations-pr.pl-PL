---
title: Tworzenie konta dla subskrypcji w wersji zapoznawczej — wersja uproszczona
description: W tym temacie zamieszczono informacje dotyczące sposobu subskrypcji programu Project Operations w wersji okrojonej— od oferty do faktury pro forma.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5ba43ba9f917da068415fb62067ab73433b701139ee07014b6bd8c02612008ce
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991544"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Tworzenie konta dla subskrypcji w wersji zapoznawczej — wersja uproszczona 

Ten temat wyjaśnia, jak subskrybować ofertę wersji próbnej i przeprowadzić uproszczone wdrożenie aplikacji Dynamics 365 Project Operations — od transakcji do faktury proforma.

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

1. Aprowizuj nowe środowisko wdrożenia usługi Project Operations Dataverse dzięki instrukcjom w temacie [Model wdrożenia usługi Dataverse](lite-deployment.md). Podczas wybierania typu środowiska należy pamiętać o użyciu **wersji próbnej (opartej na subskrypcji)**.

  ![Nowe środowisko.](./media/19CreateEnvironment.png)

2. Zaznacz ustawienie **Włącz aplikacje Dynamics 365** i pozostaw pole **Automatycznie wdrażaj te aplikacje** pustym.  
3. Wybierz **Zapisz**, aby utworzyć nowe środowisko.

  ![Dodaj bazę danych.](./media/20CreateEnvironment1.png)

4. Po utworzeniu środowiska zainstaluj rozwiązanie **Microsoft Dynamics 365 Project Operations**. 

![Instalacja rozwiązania.](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Zainstaluj konfigurację CDS i dane wersji demonstracyjnej

Zainstaluj konfigurację CDS i skonfiguruj dane demonstracyjne, wykonując poniższe instrukcje opisane w temacie [zastosowanie konfiguracji demonstracyjnej i danych konfiguracyjnych](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
