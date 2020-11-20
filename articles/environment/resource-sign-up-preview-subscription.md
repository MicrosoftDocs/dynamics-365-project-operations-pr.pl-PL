---
title: Rejestracja w przeglądzie subskrypcji Project Operations w ramach scenariuszy zasobów / zasobów niemagazynowanych
description: W tym temacie zamieszczono informacje dotyczące sposobu subskrypcji i wdrożenia Project Operations do obsługi zasobów i zasobów niemagazynowanych.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: dc3b353f19b915f645aed91dc2a8127117027034
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121141"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Rejestracja w przeglądzie subskrypcji Project Operations w ramach scenariuszy zasobów / zasobów niemagazynowanych

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

W tym temacie przedstawiono sposób subskrybowania wersji zapoznawczej / partnerskiej i wdrożenie Project Operations na potrzeby scenariuszy zasobów i zasobów niemagazynowanych.

## <a name="prerequisites"></a>Wymagania wstępne

- Otrzymasz wiadomość e-mail z zaproszeniem do skorzystania z wersji zapoznawczej. O dostęp do wersji zapoznawczej można wystąpić na [stronie internetowej Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Użytkownik wdrażający wersję zapoznawczą musi posiadać prawa administratora globalnego dzierżawy Azure.
- Wdrożenie środowiska Finance wymaga poprawnej subskrypcji Azure, która będzie rozliczana w ramach poszczególnego środowiska. Aby rozpocząć, należy użyć istniejącej subskrypcji lub [wersji próbnej usługi Azure](https://azure.microsoft.com/en-us/free/). Środowisko CDS jest dostępne bezpłatnie przez okres 30 dni.

## <a name="subscribe"></a>Subskrybuj

Po zatwierdzeniu [żądania wersji zapoznawczej](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), otrzymasz 3 wiadomości e-mail z ofertą od firmy Microsoft. Te oferty umożliwiają wdrożenie wersji zapoznawczej Project Operations:

- Dynamics 365 Project Operations (CRM) — próbna wersja zapoznawcza
- Office 365 Project Operations — (wersja zapoznawcza)
- Dynamics 365 Finance — próbna wersja zapoznawcza

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

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance — próbna wersja zapoznawcza

Powtórz te same kroki dla ostatniej oferty z powitalnej wiadomości e-mail.

## <a name="assign-licenses"></a>Przypisywanie licencji

> [!IMPORTANT]
> Aby wykonać poniższe kroki, potrzebny jest dostęp administracyjny do portalu Microsoft 365 swojej organizacji.

1. Przejdź do [Centrum administracyjnego Microsoft 365](https://portal.office.com/), aby przypisać licencje do użytkowników.

![Strona Centrum administracyjnego](./media/14AdminPortal.png)

2. Na stronie **Aktywni użytkownicy** wybierz użytkownika, któremu chcesz przypisać licencję.

![Przypisywanie licencji](./media/15AssignLicenses.png)

3. Sprawdź, czy wybrano licencje **Dynamics 365 Project Operations (CRM) — próbna wersja zapoznawcza** i **Office 365 Project Operations — wersja zapoznawcza**, a następnie wybierz **Zapisz zmiany**.

> [!NOTE]
> Oferta wersji próbnej Finance nie musi być przypisana do użytkownika.

## <a name="start-a-new-project-in-lcs"></a>Rozpoczęcie nowego projektu w LCS

Utwórz nowy projekt LCS, tak jak to opisano w temacie [Rozpoczynanie nowego projektu w LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Dodaj subskrypcję Azure do projektu LCS

Aby wykonać to zadanie, należy wykonać kroki opisane w temacie [Dodawanie subskrypcji Azure do projektu LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Wdrażanie środowiska demonstracyjnego Finance z Project Operations dla scenariuszy zasobów / zasobów niemagazynowanych

Postępuj zgodnie z instrukcjami w temacie [Ustanowienie nowego środowiska](resource-provision-new-environment.md), aby zakończyć wdrażanie. Skorzystaj z typu wdrożenia: [wersja demonstracyjna](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) w celu zapoznania się z funkcjami. 

## <a name="install-cds-setup-and-configuration-data"></a>Zainstaluj konfigurację CDS i dane konfiguracyjne

Zainstaluj konfigurację CDS i dane konfiguracyjne, tak jak to opisano w temacie [Konfiguracja i stosowanie danych konfiguracyjnych w usłudze Common Data Service](resource-apply-pro-setup-config-data.md).
Tę czynność należy wykonać tylko po wdrożeniu środowiska pokazowego Finance i przygotowaniu danych demonstracyjnych w FO.
