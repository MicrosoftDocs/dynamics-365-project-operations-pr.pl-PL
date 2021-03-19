---
title: Zamknięcie oferty - wersja uproszczona
description: Ta temat zawiera informacje na temat zamykania ofert w Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6214e1b5bec5c9173a6b6e69578de14654da633e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272296"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="1a930-103">Zamknięcie oferty - wersja uproszczona</span><span class="sxs-lookup"><span data-stu-id="1a930-103">Close a quote - lite</span></span>

<span data-ttu-id="1a930-104">_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_</span><span class="sxs-lookup"><span data-stu-id="1a930-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1a930-105">Ofertę projektu można zamknąć jako wykorzystaną lub utraconą.</span><span class="sxs-lookup"><span data-stu-id="1a930-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="1a930-106">Wersję roboczą oferty można zamknąć, ponieważ operacje Aktywuj i poprawiaj oferty nie są obsługiwane w Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="1a930-106">A draft quote can be closed because the Activate and Revise operations on quotes isn't supported in Microsoft Dynamics 365 Project Operations.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="1a930-107">Zamknięcie oferty jako wykorzystaną</span><span class="sxs-lookup"><span data-stu-id="1a930-107">Close a quote as Won</span></span>

<span data-ttu-id="1a930-108">Kiedy zamkniesz wycenę projektu jako Wygrana, stan jest ustawiony na Zamknięty, a przyczyna statusu to Wygrana.</span><span class="sxs-lookup"><span data-stu-id="1a930-108">When you close a project quote as Won, the status is set to Closed and the status reason is Won.</span></span> <span data-ttu-id="1a930-109">Zamknięcie oferty spowoduje, że projekt stanie się tylko do odczytu i utworzony zostanie kontakt w wersji roboczej, który zawierać będzie informacje z oferty.</span><span class="sxs-lookup"><span data-stu-id="1a930-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="1a930-110">Ponieważ zamkniętej wyceny nie można ponownie otworzyć, okno dialogowe potwierdzenia potwierdzi wprowadzone zmiany.</span><span class="sxs-lookup"><span data-stu-id="1a930-110">Because a closed quote can't be reopened, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="1a930-111">Jeśli oferta jest powiązana z szansą sprzedaży, wszystkie inne oferty projektu w szansie sprzedaży są automatycznie zamykane jako utracone.</span><span class="sxs-lookup"><span data-stu-id="1a930-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="1a930-112">Wpływ finansowy zamknięcia oferty jako wykorzystanej</span><span class="sxs-lookup"><span data-stu-id="1a930-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="1a930-113">Jeśli istnieją jakiekolwiek wartości rzeczywiste dotyczące czasu w projekcie, gdy jest on nadal dołączony do projektu wyceny, rejestrowany jest tylko koszt czasu lub wydatków.</span><span class="sxs-lookup"><span data-stu-id="1a930-113">If there are any actuals for time on a project while is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="1a930-114">Po zamknięciu oferty jako wykorzystanej aplikacja przeliczy koszty odwracając starsze koszty w wartościach rzeczywistych i tworząc nowe wartości rzeczywiste kosztów.</span><span class="sxs-lookup"><span data-stu-id="1a930-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="1a930-115">Aplikacja będzie przetwarzać te same koszty według metody rozliczania w skojarzonej pozycji kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="1a930-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="1a930-116">Jeśli wartości rzeczywiste kosztu odnoszą się do wiersza kontraktu dotyczącego czasu i materiałów, odpowiednie niezafakturowane wartości rzeczywiste sprzedaży są tworzone na czas zamknięcia oferty i utworzenia umowy dotyczącej projektu.</span><span class="sxs-lookup"><span data-stu-id="1a930-116">If the cost actuals reference a time and material contract line, corresponding unbilled sales actuals are created for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="1a930-117">Jeśli wartości rzeczywiste kosztu odnoszą się do wiersza umowy o stałej cenie, aplikacja przestanie ponownie przetwarzać wartości rzeczywiste kosztów, które są oparte na regułach rozliczenia podziału dla klientów objętych umową dotyczącą projektu.</span><span class="sxs-lookup"><span data-stu-id="1a930-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals that are based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="1a930-118">Zamykanie oferty jako utraconej:</span><span class="sxs-lookup"><span data-stu-id="1a930-118">Closing a quote as lost:</span></span>

<span data-ttu-id="1a930-119">Kiedy zamkniesz wycenę projektu jako Utracone, stan jest ustawiony na Zamknięty, a przyczyna statusu to Utracone.</span><span class="sxs-lookup"><span data-stu-id="1a930-119">When you close a project quote as Lost, the status is set to Closed and status reason is Lost.</span></span> <span data-ttu-id="1a930-120">Zamknięcie oferty powoduje, że projekt przejdzie w tryb tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="1a930-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="1a930-121">Ponieważ nie można ponownie otworzyć zamkniętej oferty, przed zamknięciem oferty zostanie wyświetlone okno dialogowe potwierdzenia zmian.</span><span class="sxs-lookup"><span data-stu-id="1a930-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="1a930-122">Jeśli oferta projektu zamknięta jako Utracone odwołuje się do projektu w dowolnym z jego wierszy, ten projekt jest także oznaczony jako Zamknięty.</span><span class="sxs-lookup"><span data-stu-id="1a930-122">If the project quote that is closed as Lost references a project on any of its lines, that project is also marked as Closed.</span></span> <span data-ttu-id="1a930-123">Wszystkie rezerwacje zasobów począwszy od danego dnia są anulowane.</span><span class="sxs-lookup"><span data-stu-id="1a930-123">Any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="1a930-124">W Project Operations zamknięcie oferty jako wykorzystanej lub utraconej nie wpłynie na stan szansy sprzedaży, który pozostanie otwarty do momentu jego ręcznego zamknięcia.</span><span class="sxs-lookup"><span data-stu-id="1a930-124">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]