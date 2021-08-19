---
title: Integracja faktury od dostawcy
description: Ten temat zawiera informacje o integracji faktur od dostawcy w Project Operations.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 538a2694591f1d0d368ee0ffeed9bdf12cb47420c3d0571f75185fe433f23436
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986504"
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

Księgi pomocnicze podatkowe, księgi pomocnicze sprzedawcy oraz inne księgowania finansowe są rejestrowane odpowiednio w Dynamics 365 Finance w momencie zaksięgowania faktury sprzedawcy.

![Integracja faktury od dostawcy.](media/DW7VendorInvoice.png)

Podczas tworzenia rekordów w encji **Faktury dostawcy** w Dataverse rozpoczyna się zautomatyzowany proces zatwierdzania rekordów. W razie potrzeby można przejrzeć stan procesu zautomatyzowanego zatwierdzania w Dataverse, przechodząc do strony **Zaawansowane ustawienia** > **System** > **Zadania systemowe**. Po zakończeniu zatwierdzania rekordy klasy transakcji są tworzone przez system w encji **Wartości rzeczywiste**.

Wartości rzeczywiste związane z materiałami są następnie przetwarzane przy użyciu podwójnego zapisu tabeli mapowania **Wartości rzeczywistych integracji z Project Operations (msdynactuals)**. Aby uzyskać więcej informacji, zobacz [Szacunki projektowe i wartości rzeczywiste](resource-dual-write-estimates-actuals.md).

Proces okresowy **Import z etapów** tworzy wiersze dziennika integracji w Project Operations związane z fakturą dostawcy. Konto rozliczeniowe jest domyślnie ustawione na konto integracji zamówień. Po zaksięgowaniu dziennika integracji saldo konta zostaje wyczyszczone dla transakcji faktury sprzedawcy, a kwota wiersza zostaje przeniesiona na konto kosztów projektu. Transakcje księgi podrzędnej projektu są również tworzone dla celów dalszego fakturowania i rozpoznawania przychodów.
