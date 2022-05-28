---
title: Dodaj subskrypcję Azure do projektu LCS
description: W tym temat zamieszczono informacje dotyczące sposobu łączenia subskrypcji usługi Azure z projektem LCS.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 839c510838b0bccb718b8ca8a4f71a1c46e7ea3f
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595925"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a>Dodaj subskrypcję Azure do projektu LCS

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Środowiska hostowane w chmurze muszą zostać wdrożone za pomocą istniejącej subskrypcji platformy Azure. W tym temacie zamieszczono informacje dotyczące sposobu łączenia istniejącej subskrypcji usługi Azure z projektem LCS. 

## <a name="grant-admin-consent"></a>Wyrażanie zgody administratora

1. W projekcie LCS, w sekcji **Środowiska** wybierz pozycję **Ustawienia Microsoft Azure**.

![Ustawienia Microsoft Azure.](./media/1MicrosoftAzureSettings.png)

2. Na stronie **Ustawienia projektu** na karcie **Łączniki Azure** wybierz opcję **Autoryzuj**. Pozwala to na wdrażanie środowiska w tym projekcie.

![Łączniki Azure.](./media/2AzureConnectors.png)

3. Wybierz **Autoryzuj**, aby wydać zgodę administratora.

![Wyrażanie zgody administratora.](./media/3GrantAdminConsent.png)

4. Zaakceptuj prośbę o uprawnienia.

![Zaakceptowanie prośby o uprawnienia.](./media/4AcceptPermissionRequest.png)

Autoryzacja jest teraz ukończona. 

![Pomyślna autoryzacja.](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Umożliw dostęp Dynamics Deployment Services do Twojej subskrypcji Azure

1. Przejdź do [Rozliczeń Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) i wybierz swoją subskrypcję. Usługi wdrażania Dynamics Deployment Services muszą mieć dostęp do tej subskrypcji w celu umożliwienia wdrażania środowisk.

![Szczegóły subskrypcji platformy Azure.](./media/6AzureSubscription.png)

2. Wybierz pozycję **Kontrola dostępu (IAM)** w okienku nawigacji, a następnie wybierz pozycję **Dodaj przypisanie roli**.
3. Korzystając z suwaka po prawej stronie wybierz opcję **Rola współautora**, a następnie na liście znajdź i wybierz pozycję **Dynamics Deployment Services**. 
4. Wybierz pozycję **Zapisz**.

![Dostęp do subskrypcji.](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>Dodawanie łącznika subskrypcji Azure do projektu LCS

1. W projekcie LCS na stronie **Ustawień Microsoft Azure** wybierz pozycję **Dodaj**, aby dodać nowy łącznik.
2. Wprowadź identyfikator subskrypcji platformy Azure. Identyfikator subskrypcji platformy Azure można znaleźć w [portalu Azure](https://ms.portal.azure.com/), w obszarze **Ustawienia** w lewej dolnej części ekranu.
3. W polu **Konfiguruj, aby korzystać z Azure Resource Manager** wybierz opcję **Tak**.
4. Upewnij się, że domena dzierżawy subskrypcji Azure usługi AAD pasuje do używanej przez użytkownika domeny subskrypcji platformy Azure i wybierz opcję **Dalej**.
5. Na ekranie **Konfiguracji Microsoft Azure** wybierz pozycję **Dalej**, aby potwierdzić. Jeśli na tym ekranie zostanie wyświetlony komunikat o błędzie, powróć do sekcji [Umożliw dostęp Dynamics Deployment Services do Twojej subskrypcji Azure](#provide) w tym temacie i upewnij się, że zostały zakończone wszystkie opisane czynności.
6. Pobierz Azure Management Certificate do folderu lokalnego na komputerze. Poproś administratora Azure o przesłanie certyfikatu do Azure Management Portal, wybierając subskrypcję i przechodząc do **Ustawienia** > **Certyfikaty zarządzania**. Ten certyfikat umożliwia usługom LCS komunikację z platformą Azure w imieniu użytkownika. Jeśli użytkownik ma dostęp do subskrypcji, można pominąć ten krok.
7. Wybierz **Dalej**.
8. Wybierz obszar Azure, którego wdrożenie ma zostać wdrożone, i wybierz centrum danych, które znajduje się w pobliżu miejsca, w którym zamierzasz używać tego systemu.
9.  Wybierz pozycję **Połącz**.

Pomyślnie połączono Twoją subskrypcję Azure. Teraz możesz wdrożyć środowiska obsługiwane w chmurze przez usługę Dynamics 365 Finance.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
