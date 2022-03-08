---
title: Tworzenie konta dla subskrypcji w wersji zapoznawczej
description: W tym temacie zamieszczono informacje dotyczące sposobu subskrypcji programu Project Operations w wersji okrojonej— od oferty do faktury pro forma.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5342466f308ab62a9f73a85fbd838d7c33bb1f47
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081875"
---
# <a name="sign-up-for-a-preview-subscription-for-lite-deployment--deal-to-proforma-invoicing"></a>Tworzenie konta subskrypcji w wersji zapoznawczej wdrożenia uproszczonego — od oferty do faktury pro forma

W tym temacie zamieszczono informacje wyjaśniające wykorzystanie oferty partnerskiej i wdrożenie programu Dynamics 365 Project Operations w wersji okrojonej— od oferty do faktury pro forma.

> [!NOTE]
> Ten proces będzie się zmieniać w nadchodzących wersjach Project Operations.

## <a name="prerequisites"></a>Wymagania wstępne

- Otrzymasz wiadomość e-mail z zaproszeniem do skorzystania z wersji zapoznawczej. O dostęp do wersji zapoznawczej można wystąpić na [stronie internetowej Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Użytkownik wdrażający wersję zapoznawczą musi posiadać prawa administratora globalnego dzierżawy Azure.
- Przejrzyj cały regulamin.

## <a name="subscribe"></a>Subskrybuj

Po zatwierdzeniu żądania [dostępu do wersji zapoznawczej](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), otrzymasz 2 wiadomości e-mail z ofertą od firmy Microsoft. Te oferty umożliwiają wdrożenie wersji zapoznawczej Project Operations:

- Dynamics 365 Project Operations (CRM) — próbna wersja zapoznawcza
- Office 365 Project Operations — (wersja zapoznawcza)

> [!IMPORTANT]
> To zadanie musi wykonać tylko jedna osoba — administrator dzierżawy w organizacji. Jeśli nie jesteś subskrybentem tej wersji, zaczekaj, aż organizacja się zarejestruje i otrzymasz swoje poświadczenia użytkownika.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) — próbna wersja zapoznawcza 

Przed rozpoczęciem pracy należy się upewnić, że użytkownik jest zalogowany w przeglądarce i ma konto pracy użytkownika w dzierżawie, w której ma zostać wyświetlona wersja zapoznawcza Project Operations.

1. Zrealizuj pierwszy kod oferty **Dynamics 365 Project Operations (CRM) — próbna wersja zapoznawcza**, wklejając go do adresu URL przeglądarki.

![Realizacja oferty](./media/16RedeemFirstOfferNew.png)

2. Potwierdź zamówienie.
![Potwierdź zamówienie](./media/17ConfirmOrderNew.png)

Zobaczysz, że oferta potwierdzenia została zrealizowana pomyślnie.

![Potwierdzenie](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations — (wersja zapoznawcza)

Powtórz te kroki, tak jak w przypadku pierwszego kodu oferty. Należy pamiętać, aby dodać drugi kod oferty, korzystając z tego samego konta użytkownika, które zostało użyte za pierwszym razem.

## <a name="assign-licenses"></a>Przypisywanie licencji

> [!IMPORTANT]
> Aby wykonać poniższe kroki, potrzebny jest dostęp administracyjny do portalu Microsoft 365 swojej organizacji.


1. Przejdź do [Centrum administracyjnego Microsoft 365](https://portal.office.com/), aby przypisać licencje do użytkowników.

![Strona Centrum administracyjnego](./media/14AdminPortal.png)

2. Na stronie **Aktywni użytkownicy** wybierz użytkownika, któremu chcesz przypisać licencję.

![Przypisywanie licencji](./media/15AssignLicenses.png)

3. Sprawdź, czy wybrano licencje **Dynamics 365 Project Operations (CRM) — próbna wersja zapoznawcza** i **Office 365 Project Operations — wersja zapoznawcza**. 
4. Wybierz **Zapisz zmiany**.

## <a name="create-a-new-cds-environment"></a>Utwórz nowe środowisko CDS

1. Ustanów nowe środowisko Project Operations CDS dzięki instrukcjom w temacie [model wdrożenia CDS](lite-deployment.md). Podczas wybierania typu środowiska należy pamiętać o użyciu **wersji próbnej (opartej na subskrypcji)**.
![Nowe środowisko](./media/19CreateEnvironment.png)

2. Zaznacz ustawienie **Włącz aplikacje Dynamics 365** i pozostaw pole **Automatycznie wdrażaj te aplikacje** pustym.  
3. Wybierz **Zapisz**, aby utworzyć nowe środowisko.

![Dodaj bazę danych](./media/20CreateEnvironment1.png)

4. Po utworzeniu środowiska zainstaluj rozwiązanie **Microsoft Dynamics Project 365 Operations**. 

![Instalacja rozwiązania](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Zainstaluj konfigurację CDS i dane wersji demonstracyjnej

Zainstaluj konfigurację CDS i skonfiguruj dane demonstracyjne, wykonując poniższe instrukcje opisane w temacie [zastosowanie konfiguracji demonstracyjnej i danych konfiguracyjnych](lite-apply-demo-setup-config-data.md).
