---
title: Przeglądanie zaległości fakturowania w projektach i kontraktach na projekty
description: W tym temacie zamieszczono informacje dotyczące sposobu przeglądania zaległości dotyczących wpisów czasu, wydatków i projektów oraz ich oznaczania jako gotowych do zafakturowania.
author: rumant
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: cec09ca39563e3faf0f3b2c10cf9bde3feb020b0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008549"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="c5d77-103">Przeglądanie zaległości fakturowania w projektach i kontraktach na projekty</span><span class="sxs-lookup"><span data-stu-id="c5d77-103">Review the invoicing backlog on projects and project contracts</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c5d77-104">Kiedy transakcja jest gotowa do utworzenia i przetworzenia dla niej faktury, należy ją oznaczyć jako **Przygotowane do fakturowania**.</span><span class="sxs-lookup"><span data-stu-id="c5d77-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="c5d77-105">W tym temacie opisano typy transakcji, które można tworzyć.</span><span class="sxs-lookup"><span data-stu-id="c5d77-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="c5d77-106">Przeglądanie zaległości rozliczania czasu i materiałów</span><span class="sxs-lookup"><span data-stu-id="c5d77-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="c5d77-107">Gry wpis czasu lub wydatku zostanie przesłany i zatwierdzony dla projektu, program PSA tworzy wartość rzeczywistą projektu.</span><span class="sxs-lookup"><span data-stu-id="c5d77-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="c5d77-108">Jeśli kombinacja projektu i klasy transakcji jest mapowana na pozycję kontraktu w projekcie rozliczanym według czasu i materiałów, po zatwierdzeniu wpisu są tworzone dwie wartości rzeczywiste:</span><span class="sxs-lookup"><span data-stu-id="c5d77-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="c5d77-109">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="c5d77-109">Cost actual</span></span> 
- <span data-ttu-id="c5d77-110">Wartość rzeczywista nierozliczonej sprzedaży</span><span class="sxs-lookup"><span data-stu-id="c5d77-110">Unbilled sales actual</span></span>

<span data-ttu-id="c5d77-111">Wartości rzeczywiste nierozliczonej sprzedaży reprezentują zaległość rozliczania, a ich stan fakturowania musi mieć wartość **Przygotowane do fakturowania**.</span><span class="sxs-lookup"><span data-stu-id="c5d77-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="c5d77-112">Podczas tworzenia faktury projektu nierozliczone wartości rzeczywiste sprzedaży oznaczone jako **Przygotowane do fakturowania** są kopiowane jako szczegóły wierszy faktury.</span><span class="sxs-lookup"><span data-stu-id="c5d77-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="c5d77-113">Aby przejrzeć zaległość rozliczania czasu i materiałów, wybierz kolejno opcje **Sprzedaż** \> **Rozliczenia** \> **Zaległość rozliczania czasu i materiałów**.</span><span class="sxs-lookup"><span data-stu-id="c5d77-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="c5d77-114">Zaznacz wszystkie nierozliczone wartości rzeczywiste sprzedaży, które są gotowe do zafakturowania, a następnie wybierz pozycję **Przygotowane do fakturowania**.</span><span class="sxs-lookup"><span data-stu-id="c5d77-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="c5d77-115">Stan rozliczania tych wartości rzeczywistych zmieni się na **Przygotowane do fakturowania**.</span><span class="sxs-lookup"><span data-stu-id="c5d77-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![Zaległość rozliczania czasu i materiałów](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="c5d77-117">Przeglądanie zaległości rozliczania produktów</span><span class="sxs-lookup"><span data-stu-id="c5d77-117">Review the product billing backlog</span></span>

<span data-ttu-id="c5d77-118">W programie PSA jeżeli kontrakt projektu zawiera pozycje kontraktu oparte na produktach, te pozycje (wiersze) są brane pod uwagę podczas fakturowania, ilekroć jest tworzona faktura do kontraktu na projekt.</span><span class="sxs-lookup"><span data-stu-id="c5d77-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="c5d77-119">Każdy produkt z pozycjami kontraktu oznaczonym jako **Przygotowane do fakturowania** jest kopiowany do faktury za projekt jako wiersze faktury projektu.</span><span class="sxs-lookup"><span data-stu-id="c5d77-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="c5d77-120">Aby przejrzeć zaległość rozliczania produktów, wybierz kolejno opcje **Sprzedaż** \> **Rozliczenia** \> **Zaległość rozliczania produktów**.</span><span class="sxs-lookup"><span data-stu-id="c5d77-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="c5d77-121">Zaznacz wszystkie pozycje kontraktu oparte na produktach, które są gotowe do zafakturowania, a następnie wybierz pozycję **Przygotowane do fakturowania**.</span><span class="sxs-lookup"><span data-stu-id="c5d77-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="c5d77-122">Stan rozliczania tych wierszy zmieni się na **Przygotowane do fakturowania**.</span><span class="sxs-lookup"><span data-stu-id="c5d77-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![Zaległość rozliczania produktów](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="c5d77-124">Przeglądanie punktów kontrolnych rozliczania w kontraktach o stałej cenie</span><span class="sxs-lookup"><span data-stu-id="c5d77-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="c5d77-125">Każda pozycja kontraktu projektu z metodą rozliczania według stałej ceny musi określać punkty kontrolne kontraktu.</span><span class="sxs-lookup"><span data-stu-id="c5d77-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="c5d77-126">Te punkty kontrolne kontraktu można zafakturować tylko wtedy, gdy są oznaczone **Przygotowane do fakturowania**.</span><span class="sxs-lookup"><span data-stu-id="c5d77-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="c5d77-127">Aby przejrzeć punkty kontrolne rozliczania, wybierz kolejno opcje **Sprzedaż** \> **Rozliczenia** \> **Punkty kontrolne dotyczące stałej ceny**.</span><span class="sxs-lookup"><span data-stu-id="c5d77-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="c5d77-128">Zaznacz punkty kontrolne, które są gotowe do zafakturowania, a następnie wybierz pozycję **Przygotowane do fakturowania**.</span><span class="sxs-lookup"><span data-stu-id="c5d77-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="c5d77-129">Stan rozliczania tych punktów kontrolnych zmieni się na **Przygotowane do fakturowania**.</span><span class="sxs-lookup"><span data-stu-id="c5d77-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![Punkty kontrolne dotyczące stałej ceny](media/FPBacklog.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]