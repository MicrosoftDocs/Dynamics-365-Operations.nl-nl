---
title: Probleemoplossing voor positiebudgettering
description: Dit artikel bevat beantwoorden op vragen die u kunt hebben wanneer u positiebudgettering configureert. Het behandelt vaak gestelde vragen over hoe u budgetkostenelementen, compensatiegroepen en compensatierasters maakt.
author: panolte
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmBudgetPurposeType, HcmPositionForecast
audience: Application User
ms.reviewer: roschlom
ms.custom: 88253
ms.assetid: c44df01b-8700-4022-b4c6-c4b1cb84d31d
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f03ab1437d7b4af38b3594892310e27771c829d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241437"
---
# <a name="position-budgeting-troubleshooting"></a><span data-ttu-id="6b2e9-104">Probleemoplossing voor positiebudgettering</span><span class="sxs-lookup"><span data-stu-id="6b2e9-104">Position budgeting troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6b2e9-105">Dit artikel bevat beantwoorden op vragen die u kunt hebben wanneer u positiebudgettering configureert.</span><span class="sxs-lookup"><span data-stu-id="6b2e9-105">This article provides answers to questions that you might have when you configure position budgeting.</span></span> <span data-ttu-id="6b2e9-106">Het behandelt vaak gestelde vragen over hoe u budgetkostenelementen, compensatiegroepen en compensatierasters maakt.</span><span class="sxs-lookup"><span data-stu-id="6b2e9-106">It addresses frequently asked questions about how to create budget cost elements, compensation groups, and compensation grids.</span></span> 

<a name="why-cant-i-find-the-forecast-position-page-in-human-resources"></a><span data-ttu-id="6b2e9-107">Waarom kan ik de prognosepositiepagina in Human resources niet vinden?</span><span class="sxs-lookup"><span data-stu-id="6b2e9-107">Why can’t I find the forecast position page in Human resources?</span></span>
---------------------------------------------------------------

<span data-ttu-id="6b2e9-108">Prognoseposities zijn verplaatst naar Budgettering.</span><span class="sxs-lookup"><span data-stu-id="6b2e9-108">Forecast positions have been moved to Budgeting.</span></span>

## <a name="why-cant-i-delete-a-budget-cost-element"></a><span data-ttu-id="6b2e9-109">Waarom kan ik geen budgetkostenelement verwijderen?</span><span class="sxs-lookup"><span data-stu-id="6b2e9-109">Why can’t I delete a budget cost element?</span></span>
<span data-ttu-id="6b2e9-110">U kunt geen budgetkostenelement verwijderen dat aan een prognosepositie is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="6b2e9-110">You can’t delete a budget cost element that is assigned to a forecast position.</span></span> <span data-ttu-id="6b2e9-111">Voordat u een budgetkostenelement kunt verwijderen, moet u het uit alle prognoseposities verwijderen.</span><span class="sxs-lookup"><span data-stu-id="6b2e9-111">Before you can delete a budget cost element, you must remove it from all forecast positions.</span></span> <span data-ttu-id="6b2e9-112">**Tip:** als u alle posities wilt zoeken waaraan een budgetkostenelement is toegewezen, selecteert u het kostenelement op de pagina **Budgetkostenelementen** en klikt u vervolgens op **Posities bijwerken**</span><span class="sxs-lookup"><span data-stu-id="6b2e9-112">**Tip:** To find all the positions that a budget cost element is assigned to, select the cost element on the **Budget cost elements** page, and then click **Update positions**.</span></span> <span data-ttu-id="6b2e9-113">De posities die het kostenelement gebruiken, worden in het bovenste raster weergegeven.</span><span class="sxs-lookup"><span data-stu-id="6b2e9-113">The positions that use the cost element are listed in the upper grid.</span></span>

## <a name="how-can-i-remove-a-cost-element-from-multiple-forecast-positions-without-opening-each-one"></a><span data-ttu-id="6b2e9-114">Hoe kan ik een kostenelement verwijderen uit meerdere prognoseposities zonder elke positie te openen?</span><span class="sxs-lookup"><span data-stu-id="6b2e9-114">How can I remove a cost element from multiple forecast positions without opening each one?</span></span>
<span data-ttu-id="6b2e9-115">U kunt een kostenelement niet verwijderen.</span><span class="sxs-lookup"><span data-stu-id="6b2e9-115">You can’t remove a cost element.</span></span> <span data-ttu-id="6b2e9-116">U kunt echter wel de begin- en einddatum wijzigen, zodat deze vallen buiten de datums van de budgetplanningscyclus. Het kostenelement wordt dan niet meer toegewezen aan prognoseposities in die budgetplanningscyclus.</span><span class="sxs-lookup"><span data-stu-id="6b2e9-116">However, if you change the start and end dates so that they are outside the budget planning cycle dates, the cost element will no longer be assigned to the forecast positions in that budget planning cycle.</span></span> <span data-ttu-id="6b2e9-117">Als u deze wijziging wilt aanbrengen, opent u het budgetkostenelement, klikt u op het sneltabblad **Kostenberekening** op **Datums wijzigen** en wijzigt u de ingangsdatum of de vervaldatum.</span><span class="sxs-lookup"><span data-stu-id="6b2e9-117">To make this change, open the budget cost element, and then, on the **Cost calculation** FastTab, click **Change dates**, and change the effective date or expiration date.</span></span> <span data-ttu-id="6b2e9-118">Klik op **OK** om automatisch alle prognoseposities bij te werken waaraan het kostenelement is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="6b2e9-118">Then click **OK** to automatically update all forecast positions that the cost element is assigned to.</span></span> <span data-ttu-id="6b2e9-119">**Tip:** als u deze methode gebruikt, moet u er rekening mee houden dat het budgetkostenelement uit **alle** prognoseposities wordt verwijderd waarin de begin- en de einddatum niet meer binnen het juiste bereik liggen.</span><span class="sxs-lookup"><span data-stu-id="6b2e9-119">**Tip:** If you use this method, be aware that it removes the budget cost element from **all** forecast positions where the start and end dates are no longer within the appropriate range.</span></span> <span data-ttu-id="6b2e9-120">Als dit niet is wat u wilt, moet u elke prognosepositie openen waaruit u het budgetkostenelement wilt verwijderen en de wijziging handmatig aanbrengen.</span><span class="sxs-lookup"><span data-stu-id="6b2e9-120">If this effect isn't what you intend, you must open each forecast position that you want to remove the budget cost element from and manually make the change.</span></span>

## <a name="why-cant-i-enter-an-annual-amount-on-the-cost-calculation-fasttab-for-the-budget-cost-element"></a><span data-ttu-id="6b2e9-121">Waarom kan ik geen jaarlijks bedrag invoeren op het sneltabblad Kostenberekening voor het budgetkostenelement?</span><span class="sxs-lookup"><span data-stu-id="6b2e9-121">Why can’t I enter an annual amount on the Cost calculation FastTab for the budget cost element?</span></span>
<span data-ttu-id="6b2e9-122">U kunt geen jaarlijks bedrag invoeren als er budgetkostenelementen op het sneltabblad **Berekeningsbasis** staan, omdat het systeem een percentage vereist om de waarde te berekenen.</span><span class="sxs-lookup"><span data-stu-id="6b2e9-122">You can’t enter an annual amount if there are budget cost elements on the **Calculation basis** FastTab, because the system requires a percentage in order to calculate the value.</span></span> <span data-ttu-id="6b2e9-123">Als u de waarde wilt wijzigen, verwijdert u alle budgetkostenelementen uit het sneltabblad **Berekeningsbasis**.</span><span class="sxs-lookup"><span data-stu-id="6b2e9-123">To change the value, remove all budget cost elements from the **Calculation basis** FastTab.</span></span>

## <a name="why-cant-i-change-the-budget-cost-type-from-earning-to-another-budget-cost-type"></a><span data-ttu-id="6b2e9-124">Waarom kan ik het budgetkostentype niet wijzigen van inkomsten in een ander budgetkostentype?</span><span class="sxs-lookup"><span data-stu-id="6b2e9-124">Why can’t I change the budget cost type from earning to another budget cost type?</span></span>
<span data-ttu-id="6b2e9-125">Sommige budgetkostenelementen gebruiken het kostenelement inkomsten als berekeningsbasis.</span><span class="sxs-lookup"><span data-stu-id="6b2e9-125">Some budget cost elements use the earning cost element as a calculation basis.</span></span> <span data-ttu-id="6b2e9-126">Als u het veld **Budgetkostentype** wilt wijzigen, verwijdert u het kostenelement inkomsten uit het sneltabblad **Berekeningsbasis** van alle budgetkostenelementen.</span><span class="sxs-lookup"><span data-stu-id="6b2e9-126">To change the **Budget cost type** field, remove the earning cost element from the **Calculation basis** FastTab of all budget cost elements.</span></span>

## <a name="why-cant-i-change-the-date-on-budget-cost-element-lines-for-a-budget-cost-element"></a><span data-ttu-id="6b2e9-127">Waarom kan ik de datum op de regels van budgetkostenelementen niet wijzigen voor een budgetkostenelement?</span><span class="sxs-lookup"><span data-stu-id="6b2e9-127">Why can’t I change the date on budget cost element lines for a budget cost element?</span></span>
<span data-ttu-id="6b2e9-128">U kunt de datum in het budgetkostenelement niet wijzigen wanneer een budgetkostenelement door een prognosepositie wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="6b2e9-128">You can’t change the date on the budget cost element line when a budget cost element is used by a forecast position.</span></span> <span data-ttu-id="6b2e9-129">Deze beperking helpt ervoor zorgen dat de prognoseposities altijd binnen de richtlijnen van het budgetkostenelement zijn.</span><span class="sxs-lookup"><span data-stu-id="6b2e9-129">This limitation helps guarantee that the forecast positions are always within the guidelines of the budget cost element.</span></span> <span data-ttu-id="6b2e9-130">Als u de datum wilt wijzigen, klikt u op sneltabblad **Kostenberekening**, klikt u op **Datums wijzigen** en voert u de nieuwe datums in.</span><span class="sxs-lookup"><span data-stu-id="6b2e9-130">To change the date, on the **Cost calculation** FastTab, click **Change dates**, and enter the new dates.</span></span> <span data-ttu-id="6b2e9-131">Klik vervolgens op **OK** om automatisch de posities bij te werken waaraan het kostenelement is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="6b2e9-131">Then click **OK** to update the positions that the cost element is assigned to.</span></span>

## <a name="why-cant-i-change-the-costs-for-a-budget-cost-element-on-the-compensation-group-page"></a><span data-ttu-id="6b2e9-132">Waarom kan ik de kosten voor een budgetkostenelement niet wijzigen op de pagina Compensatiegroep?</span><span class="sxs-lookup"><span data-stu-id="6b2e9-132">Why can’t I change the costs for a budget cost element on the Compensation group page?</span></span>
<span data-ttu-id="6b2e9-133">U kunt budgetkostenelementen alleen wijzigen op de pagina **Budgetkostenelementen**.</span><span class="sxs-lookup"><span data-stu-id="6b2e9-133">You can create and change budget cost elements only on the **Budget cost elements** page.</span></span>

## <a name="why-do-i-receive-an-error-message-when-i-change-the-dates-for-a-cost-element-on-a-forecast-position"></a><span data-ttu-id="6b2e9-134">Waarom krijg ik een foutmelding wanneer ik de datums voor een kostenelement wijzig in een prognosepositie?</span><span class="sxs-lookup"><span data-stu-id="6b2e9-134">Why do I receive an error message when I change the dates for a cost element on a forecast position?</span></span>
<span data-ttu-id="6b2e9-135">De datums op de prognosepositiekostenelementregel moeten binnen de volgende bereiken vallen:</span><span class="sxs-lookup"><span data-stu-id="6b2e9-135">The dates on the forecast position cost element line must be within the following ranges:</span></span>

-   <span data-ttu-id="6b2e9-136">De activerings- en deactiveringsdata van de positie.</span><span class="sxs-lookup"><span data-stu-id="6b2e9-136">The activation and retirement dates of the position.</span></span>
-   <span data-ttu-id="6b2e9-137">De activerings- en de vervaldata van het budgetkostenelement.</span><span class="sxs-lookup"><span data-stu-id="6b2e9-137">The activation and expiration dates of the budget cost element.</span></span>
-   <span data-ttu-id="6b2e9-138">De begin- en einddatums van de budgetcyclus die aan het budgetplanningsproces van de prognosepositie is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="6b2e9-138">The start and end dates of the budget cycle that is associated with the budget planning process of the forecast position.</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]