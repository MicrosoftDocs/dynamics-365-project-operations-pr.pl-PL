---
title: Rejestracja w przeglądzie subskrypcji Project Operations w ramach scenariuszy zasobów / zasobów niemagazynowanych
description: W tym temacie zamieszczono informacje dotyczące sposobu subskrypcji i wdrożenia Project Operations do obsługi zasobów i zasobów niemagazynowanych.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949012"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Rejestracja w przeglądzie subskrypcji Project Operations w ramach scenariuszy zasobów / zasobów niemagazynowanych

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

W tym temacie przedstawiono sposób subskrybowania wersji zapoznawczej / partnerskiej i wdrożenie Project Operations na potrzeby scenariuszy zasobów i zasobów niemagazynowanych.

## <a name="prerequisites"></a>Wymagania wstępne

- Otrzymasz wiadomość e-mail z zaproszeniem do skorzystania z wersji zapoznawczej. O dostęp do wersji zapoznawczej można wystąpić na [stronie internetowej Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Użytkownik wdrażający wersję zapoznawczą musi posiadać prawa administratora globalnego dzierżawy Azure.
- Wdrożenie środowiska Finance wymaga poprawnej subskrypcji Azure, która będzie rozliczana w ramach poszczególnego środowiska. Aby rozpocząć, należy użyć istniejącej subskrypcji lub [wersji próbnej usługi Azure](https://azure.microsoft.com/en-us/free/). Środowisko CDS jest dostępne bezpłatnie przez okres 30 dni.

## <a name="subscribe"></a>Subskrybuj

Po zatwierdzeniu [żądania wersji zapoznawczej](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), otrzymasz 2 wiadomości e-mail z ofertą od firmy Microsoft. Te oferty umożliwiają wdrożenie wersji zapoznawczej Project Operations:

- Dynamics 365 Project Operations — próbna wersja zapoznawcza
- Dynamics 365 for Finance and Operations — próbna wersja zapoznawcza.

> [!IMPORTANT]
> To zadanie musi wykonać tylko jedna osoba — administrator dzierżawy w organizacji. Jeśli nie jesteś subskrybentem tej wersji, zaczekaj, aż organizacja się zarejestruje i otrzymasz swoje poświadczenia użytkownika.

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations — próbna wersja zapoznawcza

1. Zrealizuj pierwszą ofertę o nazwie **Dynamics 365 Project Operations — wersja próbna**, używając adresu URL podanego w powitalnej wiadomości e-mail.

![Pierwsza oferta](./media/1FirstOffer.png)

2. Sprawdź, czy nastąpiło zalogowanie jako użytkownika należącego do organizacji, która będzie subskrybowała tę usługę.
3. Kontynuuj realizowanie oferty. 
4. Wybierz opcję **Tak, dodajesz do mojego konta**.

![Realizacja oferty](./media/2RedeemFirstOffer.png)

![Potwierdzenie oferty](./media/3ConfirmFirstOffer.png)

![Oferta zrealizowana](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance — próbna wersja zapoznawcza

Powtórz te same kroki dla drugiej oferty z powitalnej wiadomości e-mail.

## <a name="assign-licenses"></a>Przypisywanie licencji

> [!IMPORTANT]
> Aby wykonać poniższe kroki, potrzebny jest dostęp administracyjny do portalu Office 365 swojej organizacji.

1. Przejdź do [Centrum administracyjnego Microsoft 365](https://portal.office.com/), aby przypisać licencje do użytkowników.

![Portal administracyjny usługi Office](./media/5OfficeAdminPortal.png)

2. Na stronie **Aktywni użytkownicy** wybierz użytkownika, któremu chcesz przypisać licencję.

![Przypisywanie licencji](./media/6AssignLicenses.png)

3. Sprawdź, czy wybrano licencję na Project Operations i wybierz pozycję **Zapisz zmiany**. 

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

