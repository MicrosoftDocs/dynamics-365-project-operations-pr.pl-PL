---
title: Wstępne rezerwowanie wymagań
description: W tym temacie zamieszczono informacje dotyczące wstępnego rezerwowania wymagań.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 97323b73-c6de-4a7f-b889-19d4c42cf17a
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 08a8b46ee03fb93b30d178756e38c3086880f774
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754403"
---
# <a name="soft-book-requirements"></a><span data-ttu-id="99de7-103">Wstępne rezerwowanie wymagań</span><span class="sxs-lookup"><span data-stu-id="99de7-103">Soft-book requirements</span></span>

<span data-ttu-id="99de7-104">Wymaganie zasobu może być zarezerwowane ostatecznie.</span><span class="sxs-lookup"><span data-stu-id="99de7-104">A resource requirement can be hard-booked.</span></span> <span data-ttu-id="99de7-105">Rezerwacja ostateczna powoduje utworzenie propozycji zużywającej dyspozycyjność zasobu.</span><span class="sxs-lookup"><span data-stu-id="99de7-105">A hard booking creates a proposal that consumes a resource's capacity.</span></span> <span data-ttu-id="99de7-106">Następnie propozycja jest odsyłana z powrotem do wnioskodawcy w celu zatwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="99de7-106">The proposal is then sent back to the requester for approval.</span></span> <span data-ttu-id="99de7-107">Wstępna rezerwacja powoduje wstępne dodanie zasobu do zespołu projektu i ma inny status na tablicy harmonogramu, ale nie zużywa dyspozycyjności zasobu.</span><span class="sxs-lookup"><span data-stu-id="99de7-107">A soft booking tentatively adds a resource to a project team and has a different status on the Schedule Board, but it doesn't consume the resource's capacity.</span></span> <span data-ttu-id="99de7-108">Aby wstępnie zarezerwować zasób z tablicy harmonogramu, w polu **Stan rezerwacji** ustaw wartość **Wstępna**.</span><span class="sxs-lookup"><span data-stu-id="99de7-108">To soft-book a resource from the Schedule Board, set the **Booking Status** field to **Soft**.</span></span>

![Stan rezerwacji ustawiony na Wstępna](media/Resource-Management-image77.png)

<span data-ttu-id="99de7-110">Gdy karta **Zespół** jest wyświetlana w widoku **Nazwani członkowie zespołu**, zasób jest tam widoczny.</span><span class="sxs-lookup"><span data-stu-id="99de7-110">When the **Team** tab is in the **Named Team Members** view, the resource appears there.</span></span> <span data-ttu-id="99de7-111">Wstępnie zarezerwowane godziny są raportowane w kolumnie **Wstępnie zarezerwowane godziny**.</span><span class="sxs-lookup"><span data-stu-id="99de7-111">The soft-booked hours are reported in the **Soft Booked Hours** column.</span></span>

![Wstępnie zarezerwowane godziny w widoku Nazwani członkowie zespołu](media/Resource-Management-image78.png)

<span data-ttu-id="99de7-113">Wstępnie zarezerwowani członkowie zespołu mogą być przypisywani do zadań.</span><span class="sxs-lookup"><span data-stu-id="99de7-113">Soft-booked team members can be assigned to tasks.</span></span>

![Wstępnie zarezerwowany członek zespołu przypisany do zadania](media/Resource-Management-image79.png)

<span data-ttu-id="99de7-115">Na karcie **Uzgadnianie** nie są widoczne żadne rezerwacje dla wstępie zarezerwowanego zasobu, ponieważ karta **Uzgadnianie** bierze pod uwagę tylko rezerwacje ostateczne.</span><span class="sxs-lookup"><span data-stu-id="99de7-115">On the **Reconciliation** tab, no bookings are shown for a soft-book resource, because the **Reconciliation** tab considers only hard-bookings.</span></span>

![Wstępnie zarezerwowany zasób bez rezerwacji na karcie Uzgadnianie](media/Resource-Management-image80.png)

> [!NOTE]
> <span data-ttu-id="99de7-117">Nie można dokonać wstępnej rezerwacji zasobu z wymagania wygenerowanego przez ogólnego członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="99de7-117">You can't soft-book a resource from a requirement that was generated from a generic team member.</span></span>

<span data-ttu-id="99de7-118">W tablicy harmonogramu do wstępnych rezerwacji zasobu są używane inne kolory.</span><span class="sxs-lookup"><span data-stu-id="99de7-118">On the Schedule Board, a different coloring is used for soft bookings for a resource.</span></span>

![Wstępne rezerwacje na tablicy harmonogramu](media/Resource-Management-image81.png)

<span data-ttu-id="99de7-120">Aby przekonwertować rezerwację wstępną na rezerwację ostateczną, na tablicy harmonogramu kliknij prawym przyciskiem rezerwację wstępną, a następnie wybierz kolejno polecenia **Zmień stan** \> **Zarezerwuj ostatecznie** \> **Ostateczna**.</span><span class="sxs-lookup"><span data-stu-id="99de7-120">To convert a soft booking to a hard booking, on the Schedule Board, right-click the soft booking, and then select **Change Status** \> **Hard Book** \> **Hard**.</span></span>

![Zmiana stanu rezerwacji na Ostateczna](media/Resource-Management-image82.png)

<span data-ttu-id="99de7-122">Rezerwacja zostanie zmieniona, a stan zmieni się w tablicy harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="99de7-122">The booking is changed, and the status is changed on the Schedule Board.</span></span> <span data-ttu-id="99de7-123">Ze względu na fakt, że stanem rezerwacji jest teraz **Ostateczna**, zasób jest pokazany jako zarezerwowany, a jego dyspozycyjność i dostępność są skorygowane.</span><span class="sxs-lookup"><span data-stu-id="99de7-123">Because the booking status is now **Hard**, the resource is shown as booked, and its capacity and availability are adjusted.</span></span>

<span data-ttu-id="99de7-124">Korzystając z tej samej metody, można anulować rezerwację ostateczną lub wstępną z tablicy harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="99de7-124">You can use the same method to cancel a hard booking or a soft booking from the Schedule Board.</span></span>

<span data-ttu-id="99de7-125">Aby przekonwertować wstępnie zarezerwowany zasób na ostatecznie zarezerwowany zasób na karcie **Zespół** dla projektu, zaznacz zasób i kliknij przycisk **Potwierdź**.</span><span class="sxs-lookup"><span data-stu-id="99de7-125">To convert a resource that is soft-booked to hard-booked on the project's **Team** tab, select the resource, and then select **Confirm**.</span></span>

![Polecenie Potwierdź](media/Resource-Management-image83.png)
