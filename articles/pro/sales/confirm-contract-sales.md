---
title: Potwierdzenie kontraktu projektu
description: Ten temat zawiera informacje na temat potwierdzenia kontraktu projektu w Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d807d3631f40a93ec7dbd918b64c287fd4875c79
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273841"
---
# <a name="confirm-a-project-contract"></a><span data-ttu-id="ed91d-103">Potwierdzenie kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="ed91d-103">Confirm a project contract</span></span>

<span data-ttu-id="ed91d-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="ed91d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ed91d-105">Kontrakt projektu w Dynamics 365 Project Operations może być aktywny z powodem **Potwierdzone** lub zamknięty z powodem **Utrata**.</span><span class="sxs-lookup"><span data-stu-id="ed91d-105">A project contract in Dynamics 365 Project Operations can be active with a reason of **Confirmed**, or closed with a reason of **Lost**.</span></span> <span data-ttu-id="ed91d-106">Podczas potwierdzania kontraktu projektu, jego stan zmienia się z **Wersji roboczej** na **Aktywna**, a przyczyna stanu to **Potwierdzony**.</span><span class="sxs-lookup"><span data-stu-id="ed91d-106">When you confirm a project contract, the status updates from **Draft** to **Active** and the status reason is **Confirmed**.</span></span> <span data-ttu-id="ed91d-107">Nie można edytować ani ponownie otworzyć aktywnego lub zamkniętego kontraktu.</span><span class="sxs-lookup"><span data-stu-id="ed91d-107">An active or closed contract can't be edited or reopened.</span></span> 

### <a name="financial-impact-of-confirming-a-project-contract"></a><span data-ttu-id="ed91d-108">Finansowy wpływ potwierdzenia kontraktu dotyczącego projektu</span><span class="sxs-lookup"><span data-stu-id="ed91d-108">Financial impact of confirming a project contract</span></span>

<span data-ttu-id="ed91d-109">Po potwierdzeniu projektu kontraktu aplikacja przeliczy koszty odwracając starsze koszty w wartościach rzeczywistych i tworząc nowe wartości rzeczywiste kosztów.</span><span class="sxs-lookup"><span data-stu-id="ed91d-109">After a project contract is confirmed, the application recalculates the costs by reversing the older cost actuals and creating new cost actuals.</span></span> <span data-ttu-id="ed91d-110">Nowe koszty rzeczywiste zostaną przetworzone na podstawie metody rozliczeń powiązanej z projektem w skojarzonej pozycji kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="ed91d-110">The new cost actuals are then processed based on the billing method of the associated project contract line.</span></span> <span data-ttu-id="ed91d-111">Jeśli koszt rzeczywisty odnosi się do wierszu kontraktu Czas i materiały, aplikacja automatycznie ponownie tworzy odpowiednie niezafakturowane wartości rzeczywiste dotyczące sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="ed91d-111">If the cost actuals reference a Time and Material contract line, the application automatically re-creates corresponding unbilled sales actuals.</span></span> <span data-ttu-id="ed91d-112">Jeśli koszty rzeczywiste odwołują się do pozycji kontraktu o stałej cenie, aplikacja zatrzymuje przetwarzanie wartości rzeczywistych kosztów.</span><span class="sxs-lookup"><span data-stu-id="ed91d-112">If the cost actuals reference a Fixed Price contract line, the application stops reprocessing the cost actuals.</span></span>

<span data-ttu-id="ed91d-113">Limity nie do przekroczenia, konfiguracja obciążeń oraz koszty i ceny w wartościach rzeczywistych są oceniane i potem aktualizowane w ramach procesu potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="ed91d-113">Not-to-exceed limits, chargeability setup, and pricing and costing on the actuals is evaluated and then updated as part of the confirmations process.</span></span>

## <a name="close-a-project-contract-as-lost"></a><span data-ttu-id="ed91d-114">Zamykanie kontraktu jako utraconego</span><span class="sxs-lookup"><span data-stu-id="ed91d-114">Close a project contract as lost</span></span>

<span data-ttu-id="ed91d-115">Po zamknięciu kontraktu projektu jako utraconego stan kontraktu jest aktualizowany na **Zamknięty** i przyczyna stanu zostaje ustawiona na **Utracony**.</span><span class="sxs-lookup"><span data-stu-id="ed91d-115">When you close a project contract as lost, the contract status is updated to **Closed** and the status reason is **Lost**.</span></span> <span data-ttu-id="ed91d-116">Kontrakt dotyczący projektu staje się dostępny tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="ed91d-116">The project contract becomes read-only.</span></span> <span data-ttu-id="ed91d-117">Przed ukończeniem zmian dostępne jest okno dialogowe potwierdzenia, ponieważ nie będzie można ponownie otworzyć zamkniętego kontraktu dotyczącego projektu.</span><span class="sxs-lookup"><span data-stu-id="ed91d-117">A confirmation dialog is provided before the changes are complete because you can't reopen a closed project contract.</span></span>

<span data-ttu-id="ed91d-118">Jeśli kontrakt projektu, który został zamknięty jako utracony, odwołuje się do wierszy projektu, projekt jest również oznaczony jako zamknięty.</span><span class="sxs-lookup"><span data-stu-id="ed91d-118">If the project contract that is closed as lost references a project on its lines, that project is also marked as closed.</span></span> <span data-ttu-id="ed91d-119">Wszystkie rezerwacje zasobów począwszy od danego dnia są anulowane.</span><span class="sxs-lookup"><span data-stu-id="ed91d-119">Any resource bookings from that day forward are canceled.</span></span> <span data-ttu-id="ed91d-120">Wszelkie nierozliczone wartości rzeczywiste dotyczące sprzedaży w kontrakcie projektu, które nie są jeszcze zawarte w fakturze, zostaną anulowane.</span><span class="sxs-lookup"><span data-stu-id="ed91d-120">Any unbilled sales actuals on the project contract that aren't already on an invoice, will be reversed.</span></span>

> [!NOTE]
> <span data-ttu-id="ed91d-121">W programie Dynamics 365 Project Operations zamknięcie kontraktu projektu jako utraconego nie wpłynie na ten stan skojarzonej szansy sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="ed91d-121">In Dynamics 365 Project Operations, closing a project contract as lost will not impact that status of the associated opportunity.</span></span> <span data-ttu-id="ed91d-122">Szansa sprzedaży pozostanie otwarta i należy ją zamknąć ręcznie.</span><span class="sxs-lookup"><span data-stu-id="ed91d-122">The opportunity will remain open and must be manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]