---
title: Wydajność propozycji faktury projektu
description: Ten temat zawiera informacje o ulepszeniach wydajności propozycji faktur projektu.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5a14acf51d277b16896d64c4b12ee00bfb326910
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269803"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="5374c-103">Wydajność propozycji faktury projektu</span><span class="sxs-lookup"><span data-stu-id="5374c-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5374c-104">Podczas tworzenia nowej propozycji faktury możesz napotkać problemy z wydajnością, ponieważ wzrasta liczba projektów i podprojektów.</span><span class="sxs-lookup"><span data-stu-id="5374c-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="5374c-105">Aby poprawić wydajność, dostępna jest funkcja, która skraca czas potrzebny do utworzenia nowej propozycji faktury dla zaksięgowanych transakcji projektu.</span><span class="sxs-lookup"><span data-stu-id="5374c-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="5374c-106">Włącz poprawę wydajności propozycji faktury za projekt</span><span class="sxs-lookup"><span data-stu-id="5374c-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="5374c-107">Aby włączyć funkcję poprawy wydajności propozycji faktury za projekt, wykonaj następujące kroki.</span><span class="sxs-lookup"><span data-stu-id="5374c-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="5374c-108">Przejdź do opcji **Zarządzanie funkcjami** > **Wszystkie**.</span><span class="sxs-lookup"><span data-stu-id="5374c-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="5374c-109">Na liście funkcji znajdź **Poprawa wydajności propozycji faktury za projekt**.</span><span class="sxs-lookup"><span data-stu-id="5374c-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="5374c-110">Wybierz opcję **Włącz teraz**.</span><span class="sxs-lookup"><span data-stu-id="5374c-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="5374c-111">Odśwież przeglądarkę i utwórz nową fakturę.</span><span class="sxs-lookup"><span data-stu-id="5374c-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="5374c-112">Wyłącz poprawę wydajności propozycji faktury za projekt</span><span class="sxs-lookup"><span data-stu-id="5374c-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="5374c-113">Wykonaj następujące kroki, aby wyłączyć poprawę wydajności propozycji faktury za projekt.</span><span class="sxs-lookup"><span data-stu-id="5374c-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="5374c-114">Przejdź do opcji **Zarządzanie funkcjami** > **Wszystkie**.</span><span class="sxs-lookup"><span data-stu-id="5374c-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="5374c-115">Na liście funkcji znajdź **Poprawa wydajności propozycji faktury za projekt**.</span><span class="sxs-lookup"><span data-stu-id="5374c-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="5374c-116">Wybierz opcję **Wyłącz**.</span><span class="sxs-lookup"><span data-stu-id="5374c-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="5374c-117">Odśwież przeglądarkę.</span><span class="sxs-lookup"><span data-stu-id="5374c-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="5374c-118">Wydajności propozycji faktury nie można zastosować, jeśli włączono reguły fakturowania.</span><span class="sxs-lookup"><span data-stu-id="5374c-118">Invoice proposal performance can't be applied when billing rules are enabled.</span></span>
> 
> <span data-ttu-id="5374c-119">Podczas procesu przetwarzania wsadowego w celu utworzenia propozycji faktury liczba zadań podrzędnych będzie dzielić zadania na maksymalną liczbę w zależności od liczby kontraktów z transakcjami możliwymi do zafakturowania, niezależnie od tego, co wprowadzono.</span><span class="sxs-lookup"><span data-stu-id="5374c-119">During the batch process to create invoice proposals, the number of subtasks will split the tasks to a maximum number based on the number of contracts with invoiceable transactions, regardless of what you have entered.</span></span> <span data-ttu-id="5374c-120">Jeśli na przykład wprowadzisz wartość **3** dla liczby zadań podrzędnych na potrzeby tworzenia propozycji faktury w partii i istnieją tylko dwa kontrakty z transakcjami do fakturowania, tworzone są tylko dwa zadania podrzędne.</span><span class="sxs-lookup"><span data-stu-id="5374c-120">For example, if you enter **3** for the number of subtasks for invoice proposal creation in batch, and there are only two contracts with invoiceable transactions, only two subtasks are created.</span></span>
