---
title: Zamykanie ofert
description: Ta temat zawiera informacje na temat zamykania ofert w Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896204"
---
# <a name="close-quotes"></a><span data-ttu-id="b3642-103">Zamykanie ofert</span><span class="sxs-lookup"><span data-stu-id="b3642-103">Close quotes</span></span> 

<span data-ttu-id="b3642-104">_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_</span><span class="sxs-lookup"><span data-stu-id="b3642-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b3642-105">Ofertę projektu można zamknąć jako wykorzystaną lub utraconą.</span><span class="sxs-lookup"><span data-stu-id="b3642-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="b3642-106">Operacje aktywowania i zmiany oferty nie są obsługiwane w ramach Microsoft Dynamics 365 Project Operations, więc roboczą ofertę można zamknąć.</span><span class="sxs-lookup"><span data-stu-id="b3642-106">The Activate and Revise operations on quotes is not supported in Microsoft Dynamics 365 Project Operations, so a draft quote can be closed.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="b3642-107">Zamknięcie oferty jako wykorzystaną</span><span class="sxs-lookup"><span data-stu-id="b3642-107">Close a quote as Won</span></span>

<span data-ttu-id="b3642-108">Zamknięcie oferty projektu jako wykorzystanej spowoduje zamknięcie oferty z ustawionym stanem „Zamknięty” i przyczyną stanu ustawiona na „Wygrana”.</span><span class="sxs-lookup"><span data-stu-id="b3642-108">Closing a project quote as Won will close the quote with the status set to Closed and the status reason set to Won.</span></span> <span data-ttu-id="b3642-109">Zamknięcie oferty spowoduje, że projekt stanie się tylko do odczytu i utworzony zostanie kontakt w wersji roboczej, który zawierać będzie informacje z oferty.</span><span class="sxs-lookup"><span data-stu-id="b3642-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="b3642-110">Ponieważ nie można ponownie otworzyć zamkniętej oferty, przed wprowadzeniem zmian w okienku powiadomień jest dostępne okno dialogowe potwierdzenia. Nie można ponownie otworzyć zamkniętej oferty, a zmiana jest nieodwracalna.</span><span class="sxs-lookup"><span data-stu-id="b3642-110">Because a closed quote can't be reopened, a confirmation dialog There is a confirmation dialog before the changes are done since a closed quote cannot be re-opened and the changes are irreversible.</span></span>

<span data-ttu-id="b3642-111">Jeśli oferta jest powiązana z szansą sprzedaży, wszystkie inne oferty projektu w szansie sprzedaży są automatycznie zamykane jako utracone.</span><span class="sxs-lookup"><span data-stu-id="b3642-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="b3642-112">Wpływ finansowy zamknięcia oferty jako wykorzystanej</span><span class="sxs-lookup"><span data-stu-id="b3642-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="b3642-113">W przypadku istnienia wartości rzeczywistych dla czasu zapisanego w projekcie w czasie, gdy jest on wciąż zapisany w formie wersji roboczej, rejestrowana jest tylko koszt czasu lub wydatku.</span><span class="sxs-lookup"><span data-stu-id="b3642-113">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="b3642-114">Po zamknięciu oferty jako wykorzystanej aplikacja przeliczy koszty odwracając starsze koszty w wartościach rzeczywistych i tworząc nowe wartości rzeczywiste kosztów.</span><span class="sxs-lookup"><span data-stu-id="b3642-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="b3642-115">Aplikacja będzie przetwarzać te same koszty według metody rozliczania w skojarzonej pozycji kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="b3642-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="b3642-116">Jeśli koszt odwołuje się do cz pozycji kontraktu czasu i materiałów, system automatycznie utworzy odpowiednie niezafakturowane wartości rzeczywiste przy zamykaniu oferty i utworzeniu kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="b3642-116">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="b3642-117">Jeśli referencyjne koszty są odwołaniami do pozycji kontraktu o stałej cenie, aplikacja zatrzyma przetwarzanie wartości rzeczywistych kosztów na podstawie reguł podziału fakturowania dla klientów kontraktów projektów.</span><span class="sxs-lookup"><span data-stu-id="b3642-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="b3642-118">Zamykanie oferty jako utraconej:</span><span class="sxs-lookup"><span data-stu-id="b3642-118">Closing a quote as lost:</span></span>

<span data-ttu-id="b3642-119">Zamknięcie oferty projektu jako utraconej spowoduje ustawienie stanu na „Zamknięty” i nada przyczynę stanu „Utracona”.</span><span class="sxs-lookup"><span data-stu-id="b3642-119">Closing a project quote as Lost will set the status to Closed and status reason to Lost.</span></span> <span data-ttu-id="b3642-120">Zamknięcie oferty powoduje, że projekt przejdzie w tryb tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="b3642-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="b3642-121">Ponieważ nie można ponownie otworzyć zamkniętej oferty, przed zamknięciem oferty zostanie wyświetlone okno dialogowe potwierdzenia zmian.</span><span class="sxs-lookup"><span data-stu-id="b3642-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="b3642-122">Jeśli oferta projektu, która zostanie zamknięta jako utracona zawiera projekt, do którego odwołuje się dowolny z tych wierszy, projekt jest również oznaczony jako zamknięty, a rezerwacje wszystkich zaksięgowań począwszy od danego dnia są anulowane.</span><span class="sxs-lookup"><span data-stu-id="b3642-122">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="b3642-123">W Project Operations zamknięcie oferty jako wykorzystanej lub utraconej nie wpłynie na stan szansy sprzedaży, który pozostanie otwarty do momentu jego ręcznego zamknięcia.</span><span class="sxs-lookup"><span data-stu-id="b3642-123">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
