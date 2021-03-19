---
title: Zamknij ofertę
description: Ta temat zawiera informacje na temat zamykania ofert w Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a2c752ba6395ed4bf025092219350dc245f7428f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277261"
---
# <a name="close-a-quote"></a><span data-ttu-id="df3a5-103">Zamknij ofertę</span><span class="sxs-lookup"><span data-stu-id="df3a5-103">Close a quote</span></span>

<span data-ttu-id="df3a5-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="df3a5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="df3a5-105">Ofertę projektu można zamknąć jako wykorzystaną lub utraconą.</span><span class="sxs-lookup"><span data-stu-id="df3a5-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="df3a5-106">Ponieważ funkcje Aktywuj i Popraw nie są obsługiwane w Microsoft Dynamics 365 Project Operations, możesz zamknąć wersję roboczą oferty.</span><span class="sxs-lookup"><span data-stu-id="df3a5-106">Because the functions Activate and Revise are not supported on quotes in Microsoft Dynamics 365 Project Operations, you can close a draft quote.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="df3a5-107">Zamknięcie oferty jako wykorzystaną</span><span class="sxs-lookup"><span data-stu-id="df3a5-107">Close a quote as Won</span></span>

<span data-ttu-id="df3a5-108">Zamknięcie oferty projektu jako wykorzystanej spowoduje zamknięcie oferty z ustawionym stanem **Zamknięty** i przyczyną stanu ustawiona na **Wygrana**.</span><span class="sxs-lookup"><span data-stu-id="df3a5-108">Closing a project quote as Won will set the status of the quote to **Closed** and status reason to **Won**.</span></span> <span data-ttu-id="df3a5-109">Zamknięcie oferty spowoduje, że projekt stanie się tylko do odczytu i utworzony zostanie kontakt w wersji roboczej, który zawierać będzie wszystkie informacje z oferty.</span><span class="sxs-lookup"><span data-stu-id="df3a5-109">Closing the quotes makes it read-only and creates a draft project contract with all the quote information.</span></span> <span data-ttu-id="df3a5-110">Ponieważ nie można ponownie otworzyć zamkniętej oferty, przed zamknięciem oferty zostanie wyświetlone okno dialogowe potwierdzenia zmian.</span><span class="sxs-lookup"><span data-stu-id="df3a5-110">Because a closed quote can't be reopened, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="df3a5-111">Kontrakt utworzony na podstawie oferty projektu jest udostępniany również w module Zarządzanie projektami i księgowości w Project Operations.</span><span class="sxs-lookup"><span data-stu-id="df3a5-111">The project contract created from a project quote is also made available in the Project management and accounting module of Project Operations.</span></span> <span data-ttu-id="df3a5-112">Jeśli kontrakt projektu nie jest zamapowany do projektu w żadnym z jego wierszy, ten kontrakt jest udostępniany jako nieaktywny kontrakt projektu i będzie aktywny zaraz po zamapowaniu projektu do co najmniej jednej z pozycji kontraktu.</span><span class="sxs-lookup"><span data-stu-id="df3a5-112">If a project contract is not mapped to a project on any of its lines, this project contract is made available as an inactive project contract and becomes active as soon as a project is mapped to at least one of its contract lines.</span></span>

<span data-ttu-id="df3a5-113">Jeśli oferta jest powiązana z szansą sprzedaży, wszystkie inne oferty projektu w szansie sprzedaży są automatycznie zamykane jako utracone.</span><span class="sxs-lookup"><span data-stu-id="df3a5-113">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="df3a5-114">Wpływ finansowy zamknięcia oferty jako wykorzystanej</span><span class="sxs-lookup"><span data-stu-id="df3a5-114">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="df3a5-115">W przypadku istnienia wartości rzeczywistych dla czasu zapisanego w projekcie w czasie, gdy jest on wciąż zapisany w formie wersji roboczej, rejestrowana jest tylko koszt czasu lub wydatku.</span><span class="sxs-lookup"><span data-stu-id="df3a5-115">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="df3a5-116">Po zamknięciu oferty jako wykorzystanej aplikacja przeliczy koszty odwracając starsze koszty w wartościach rzeczywistych i tworząc nowe wartości rzeczywiste kosztów.</span><span class="sxs-lookup"><span data-stu-id="df3a5-116">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="df3a5-117">Aplikacja będzie przetwarzać te same koszty według metody rozliczania w skojarzonej pozycji kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="df3a5-117">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="df3a5-118">Jeśli koszt odwołuje się do cz pozycji kontraktu czasu i materiałów, system automatycznie utworzy odpowiednie niezafakturowane wartości rzeczywiste przy zamykaniu oferty i utworzeniu kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="df3a5-118">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="df3a5-119">Jeśli referencyjne koszty są odwołaniami do pozycji kontraktu o stałej cenie, aplikacja zatrzyma przetwarzanie wartości rzeczywistych kosztów na podstawie reguł podziału fakturowania dla klientów kontraktów projektów.</span><span class="sxs-lookup"><span data-stu-id="df3a5-119">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

<span data-ttu-id="df3a5-120">Wszystkie ponownie przetworzone wartości rzeczywiste są dostępne w module Zarządzanie projektami i ich księgowanie dla konta projektu, które można przejrzeć, zaktualizować i wysłać do księgi głównej.</span><span class="sxs-lookup"><span data-stu-id="df3a5-120">All reprocessed actuals are available in the Project management and accounting module for the Project accountant to review, update, and post to the General ledger.</span></span> 

## <a name="close-a-quote-as-lost"></a><span data-ttu-id="df3a5-121">Zamknięcie oferty jako utraconej</span><span class="sxs-lookup"><span data-stu-id="df3a5-121">Close a quote as Lost</span></span>

<span data-ttu-id="df3a5-122">Zamknięcie oferty projektu jako utraconej spowoduje ustawienie stanu na **Zamknięty** i nada przyczynę stanu **Utracona**.</span><span class="sxs-lookup"><span data-stu-id="df3a5-122">Closing a project quote as Lost will set the status to **Closed** and status reason to **Lost**.</span></span> <span data-ttu-id="df3a5-123">Zamknięcie oferty powoduje, że wejdzie ona w tryb tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="df3a5-123">Closing the quote makes it read-only.</span></span> <span data-ttu-id="df3a5-124">Ponieważ nie można ponownie otworzyć zamkniętej oferty, przed zamknięciem oferty zostanie wyświetlone okno dialogowe potwierdzenia zmian.</span><span class="sxs-lookup"><span data-stu-id="df3a5-124">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="df3a5-125">Jeśli oferta projektu, która zostanie zamknięta jako utracona zawiera projekt, do którego odwołuje się dowolny z tych wierszy, projekt jest również oznaczony jako zamknięty, a rezerwacje wszystkich zaksięgowań począwszy od danego dnia są anulowane.</span><span class="sxs-lookup"><span data-stu-id="df3a5-125">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="df3a5-126">W Project Operations zamknięcie oferty jako wykorzystanej lub utraconej nie wpłynie na stan szansy sprzedaży, który pozostanie otwarty do momentu jego ręcznego zamknięcia.</span><span class="sxs-lookup"><span data-stu-id="df3a5-126">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]