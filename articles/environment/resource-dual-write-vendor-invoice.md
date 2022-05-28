---
title: Integracja faktury od dostawcy
description: Ten temat zawiera informacje o integracji faktur od dostawcy w Project Operations.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8650eed2230b99b821c1635fdc88252bb65c5583
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591188"
---
# <a name="vendor-invoice-integration"></a>Integracja faktury od dostawcy

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Zamówienia związane z projektem w Dynamics 365 Project Operations można rejestrować, przechodząc do **Rozrachunki z dostawcami** > **Faktury** > **Oczekujące faktury od dostawców** i używając dokumentu oczekującej faktury sprzedawcy. Aby uzyskać więcej informacji, zobacz [jak zakupić materiały niebędące na stanie magazynowym za pomocą oczekującej faktury dostawcy](../procurement/pending-vendor-invoices.md).

> [!IMPORTANT]
> Przed użyciem funkcji opisanych w tym temacie należy przejrzeć i zastosować wymagane konfiguracje. Aby uzyskać więcej informacji, zobacz [jak włączyć obsługę materiałów niebędących na stanie magazynowym i oczekujących na faktury dostawcy](../procurement/configure-materials-nonstocked.md).

W Project Operations wiersze raportu dotyczące faktur dostawcy są publikowane przy użyciu specjalnych reguł publikowania:

- Koszty związane z projektem (w tym podatek niepodlegający zwrotowi) nie są natychmiast księgowane na koncie kosztów projektu w księdze głównej. Zamiast tego koszt jest księgowany na **koncie integracyjnym zamówień**. To konto jest skonfigurowane w **Zarządzanie projektami i księgowanie** > **Konfiguracja** > **Zarządzanie parametrami projektów i księgowania**, **Project Operations w Dynamics 365 Customer engagement**.
- Podwójny zapis umożliwia synchronizację szczegółów faktury dostawcy z Microsoft Dataverse, za pomocą następujących mapowań tabeli:

     - **Integracja encji eksportu faktur dostawcy w Project Operations (msdyn_projectvendorinvoices)**: Ta mapa tabeli synchronizuje informacje nagłówka faktury sprzedawcy. Z programem Dataverse są synchronizowane tylko faktury dostawców zawierające co najmniej jeden wiersz identyfikatora projektu.
     - **Integracja encji eksportu wiersza faktury dostawcy w Project Operations (msdyn_projectvendorinvoicelines)**: Ta mapa tabeli synchronizuje informacje wiersza faktury sprzedawcy. Z Dataverse są synchronizowane tylko wiersze zawierające identyfikator projektu.

     > [!NOTE]
     > Nie można edytować szczegółów faktury dostawcy w Dataverse.

Podrzędna księga podatkowa, podrzędna księga dostawcy i inne księgowania finansowe są rejestrowane odpowiednio w Dynamics 365 Finance podczas księgowania faktury od dostawcy.

![Integracja faktury od dostawcy.](media/DW7VendorInvoice.png)

Podczas tworzenia rekordów w encji **Faktury dostawcy** w Dataverse rozpoczyna się zautomatyzowany proces zatwierdzania rekordów. W razie potrzeby można przejrzeć stan procesu zautomatyzowanego zatwierdzania w Dataverse, przechodząc do strony **Zaawansowane ustawienia** > **System** > **Zadania systemowe**. Po zakończeniu zatwierdzania rekordy klasy transakcji są tworzone przez system w encji **Wartości rzeczywiste**.

Wartości rzeczywiste związane z materiałami są następnie przetwarzane przy użyciu podwójnego zapisu tabeli mapowania **Wartości rzeczywistych integracji z Project Operations (msdynactuals)**. Aby uzyskać więcej informacji, zobacz [Szacunki projektowe i wartości rzeczywiste](resource-dual-write-estimates-actuals.md).

Proces okresowy **Import z etapów** tworzy wiersze dziennika integracji w Project Operations związane z fakturą dostawcy. Konto rozliczeniowe jest domyślnie ustawione na konto integracji zamówień. Po zaksięgowaniu dziennika integracji saldo konta zostaje wyczyszczone dla transakcji faktury sprzedawcy, a kwota wiersza zostaje przeniesiona na konto kosztów projektu. Transakcje księgi podrzędnej projektu są również tworzone dla celów dalszego fakturowania i rozpoznawania przychodów.
