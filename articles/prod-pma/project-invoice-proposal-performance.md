---
title: Wydajność propozycji faktury projektu
description: Ten temat zawiera informacje o ulepszeniach wydajności propozycji faktur projektu.
author: Yowelle
ms.date: 04/20/2021
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
ms.openlocfilehash: 0e7a9eedc80a88e80b7788be4fe4b2f969be8ba1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999504"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="d9183-103">Wydajność propozycji faktury projektu</span><span class="sxs-lookup"><span data-stu-id="d9183-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9183-104">Podczas tworzenia nowej propozycji faktury możesz napotkać problemy z wydajnością, ponieważ wzrasta liczba projektów i podprojektów.</span><span class="sxs-lookup"><span data-stu-id="d9183-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="d9183-105">Aby poprawić wydajność, dostępna jest funkcja, która skraca czas potrzebny do utworzenia nowej propozycji faktury dla zaksięgowanych transakcji projektu.</span><span class="sxs-lookup"><span data-stu-id="d9183-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="d9183-106">Włącz poprawę wydajności propozycji faktury za projekt</span><span class="sxs-lookup"><span data-stu-id="d9183-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="d9183-107">Aby włączyć funkcję poprawy wydajności propozycji faktury za projekt, wykonaj następujące kroki.</span><span class="sxs-lookup"><span data-stu-id="d9183-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="d9183-108">Przejdź do opcji **Zarządzanie funkcjami** > **Wszystkie**.</span><span class="sxs-lookup"><span data-stu-id="d9183-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="d9183-109">Na liście funkcji znajdź **Poprawa wydajności propozycji faktury za projekt**.</span><span class="sxs-lookup"><span data-stu-id="d9183-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="d9183-110">Wybierz opcję **Włącz teraz**.</span><span class="sxs-lookup"><span data-stu-id="d9183-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="d9183-111">Odśwież przeglądarkę i utwórz nową fakturę.</span><span class="sxs-lookup"><span data-stu-id="d9183-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="d9183-112">Wyłącz poprawę wydajności propozycji faktury za projekt</span><span class="sxs-lookup"><span data-stu-id="d9183-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="d9183-113">Wykonaj następujące kroki, aby wyłączyć poprawę wydajności propozycji faktury za projekt.</span><span class="sxs-lookup"><span data-stu-id="d9183-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="d9183-114">Przejdź do opcji **Zarządzanie funkcjami** > **Wszystkie**.</span><span class="sxs-lookup"><span data-stu-id="d9183-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="d9183-115">Na liście funkcji znajdź **Poprawa wydajności propozycji faktury za projekt**.</span><span class="sxs-lookup"><span data-stu-id="d9183-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="d9183-116">Wybierz opcję **Wyłącz**.</span><span class="sxs-lookup"><span data-stu-id="d9183-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="d9183-117">Odśwież przeglądarkę.</span><span class="sxs-lookup"><span data-stu-id="d9183-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="d9183-118">Nie można zastosować wydajności propozycji faktury, gdy są włączone reguły rozliczeniowe lub są uruchomione procesy wsadowe.</span><span class="sxs-lookup"><span data-stu-id="d9183-118">Invoice proposal performance can't be applied when billing rules are enabled or batch processes are running.</span></span>
