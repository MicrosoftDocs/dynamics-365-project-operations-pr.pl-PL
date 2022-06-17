---
title: Zamówienie materiałów niemagazynowanych dla projektu przy użyciu zamówień zakupu projektu
description: Ten artykuł objaśnia, jak można zamówić materiały niemagazynowane dla projektu przy użyciu zamówień zakupu projektu.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fe24faa143869af2396f3b0f28aae31417cadda7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929825"
---
# <a name="order-procurement-categories-or-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Zamów kategorie zaopatrzenia lub materiały nie będące w magazynie dla projektu za pomocą zamówień zakupu projektu

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Dział zakupów w organizacji może użyć [zamówień zakupu](/dynamics365/supply-chain/procurement/purchase-order-overview) do śledzenia zamówień towarów i usług. Zamówienia zakupu dla kategorii zaopatrzenia lub materiałów niemagazynowych można przypisać do projektu. Fakturowanie tych zamówień zapisuje koszt w ramach projektu.

## <a name="prerequisites"></a>Wymagania wstępne
Aby włączyć funkcję zamówień zakupu projektu, wykonaj następujące kroki.

1. W programie Dynamics 365 Finance przejdź do obszaru roboczego **Zarządzanie funkcjami**.
2. Na liście funkcji znajdź wybierz funkcję **Włącz zamówienia zakupu projektu w rozwiązaniu Project Operations dla scenariuszy opartych na zasobach/niemagazynowanych**.
3. Wybierz opcję **Włącz**.
4. Konfigurowanie materiałów niemagazynowanych i oczekujących faktur od dostawcy zgodnie z opisem [Konfigurowanie materiałów niemagazynowych i oczekujących faktur od dostawcy](configure-materials-nonstocked.md).
5. Skonfigurowanie kategorii kategorii kategorii w sposób opisany w [Korzystanie z kategorii w zamówieniach zakupu projektu i oczekujących na fakturach od dostawców](configure-procurement-categories.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Tworzenie zamówienia zakupu projektu z listy zamówień zakupu projektu

1. W rozwiązaniu Finance przejdź do opcji **Zarządzanie projektami i ich księgowanie** > **Projekty** > **Wszystkie projekty** i wybierz projekt.
2. W okienku akcji, na karcie **Zarządzaj**, w grupie **Nowe** wybierz **Zadanie pozycji** > **Zamówienie zakupu**.
3. Na stronie **Utwórz zamówienia zakupu** wybierz dostawcę, u którego chcesz złożyć zamówienie, wprowadź odpowiednie informacje, a następnie wybierz przycisk **OK**.
4. Na stronie **Zamówienie zakupu** w siatce **Wiersze zamówienia zakupu** wybierz **Dodaj wiersz**.
5. Wprowadź numer pozycji lub kategorię zaopatrzenia, ilość, jednostkę, cenę jednostkową i inne informacje, stosownie do potrzeb.

    > [!NOTE]
    > Z zamówieniami zakupu projektu można używać tylko kategorii zaopatrzenia, towarów niemagazynowanych i usług. Elementy stockowane nie są obsługiwane.

6. Kontynuuj dodawanie towarów lub kategorii zaopatrzenia zgodnie z wymaganiami i potwierdź zamówienie zakupu.

    Potwierdzenia otrzymania towarów i usług można zarejestrować, tworząc i księgując potwierdzenie otrzymania produktu.

    > [!NOTE]
    > Dokumenty dostawy produktów nie są rejestrowane dla wartości rzeczywistych w programie Microsoft Dataverse i nie mają wpływu na księgę podrzędną projektu.

    Po wysłaniu przez dostawcę faktury za pozycje i usługi w zamówieniu zakupu dział zakupów może wygenerować fakturę dla zamówienia zakupu, przechodząc do okienka akcji **Faktura** > **Generuj** > **Faktura**. Aby uzyskać więcej informacji o oczekujących fakturach od dostawcy, zobacz temat [Zakup materiałów niemagazynowych przy użyciu oczekujących faktur od dostawcy](pending-vendor-invoices.md).
