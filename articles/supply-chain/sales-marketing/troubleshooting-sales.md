---
title: Problemen met verkooporders oplossen
description: In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met verkooporders.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 346ebee598e282abfe01a399793cc259aff3c22d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232225"
---
# <a name="troubleshoot-sales-orders"></a><span data-ttu-id="95524-103">Problemen met verkooporders oplossen</span><span class="sxs-lookup"><span data-stu-id="95524-103">Troubleshoot sales orders</span></span>

<span data-ttu-id="95524-104">In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met verkooporders.</span><span class="sxs-lookup"><span data-stu-id="95524-104">This topic describes how to fix issues that you might encounter while you work with sales orders.</span></span>

## <a name="the-tax-information-isnt-updated-if-i-change-the-location-on-a-sales-order-header"></a><span data-ttu-id="95524-105">De belastinggegevens worden niet bijgewerkt als ik de locatie in de kop van een verkooporder wijzig.</span><span class="sxs-lookup"><span data-stu-id="95524-105">The tax information isn't updated if I change the location on a sales order header.</span></span>

### <a name="issue-description"></a><span data-ttu-id="95524-106">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="95524-106">Issue description</span></span>

<span data-ttu-id="95524-107">Als de locatie, het magazijn of het afleveradres wordt gewijzigd in de koptekst van een verkooporder of op het regelniveau, wordt de belastinginformatie voor de aanvraag niet automatisch bijgewerkt voor de regels.</span><span class="sxs-lookup"><span data-stu-id="95524-107">If the site, warehouse, or delivery address is changed either on a sales order header or at the line level, the case tax information isn't automatically updated for the lines.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="95524-108">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="95524-108">Issue resolution</span></span>

<span data-ttu-id="95524-109">Dit is zo ontworpen.</span><span class="sxs-lookup"><span data-stu-id="95524-109">This behavior is by design.</span></span> <span data-ttu-id="95524-110">Het probleem doet zich voor omdat het afleveradres, de locatie en het magazijn niet automatisch op regelniveau worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="95524-110">The issue occurs because the delivery address, site, and warehouse aren't automatically changed at the line level either.</span></span> <span data-ttu-id="95524-111">U moet ze handmatig bijwerken.</span><span class="sxs-lookup"><span data-stu-id="95524-111">You must update them manually.</span></span>

## <a name="if-there-are-two-trade-agreements-for-the-same-period-or-overlapping-periods-the-same-agreement-line-is-always-selected"></a><span data-ttu-id="95524-112">Als er twee handelsovereenkomsten zijn voor dezelfde periode of overlappende perioden, wordt altijd dezelfde overeenkomstregel geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="95524-112">If there are two trade agreements for the same period or overlapping periods, the same agreement line is always selected.</span></span>

### <a name="issue-description"></a><span data-ttu-id="95524-113">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="95524-113">Issue description</span></span>

<span data-ttu-id="95524-114">Als twee handelsovereenkomsten zijn gedefinieerd voor dezelfde periode of overlappende perioden, lijkt telkens dezelfde handelsovereenkomst te worden geselecteerd wanneer u verkooporderregels maakt die die artikelen bevatten.</span><span class="sxs-lookup"><span data-stu-id="95524-114">If two trade agreements are defined for the same period or overlapping periods, the same trade agreement seems to be selected every time when you create sales order lines that contain those items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="95524-115">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="95524-115">Issue resolution</span></span>

<span data-ttu-id="95524-116">Als er meer dan één handelsovereenkomst voor een bepaalde datum is, wordt altijd de handelsovereenkomst met de laagste prijs geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="95524-116">If there is more than one trade agreement for a given date, the trade agreement that has the lowest price is always selected.</span></span> <span data-ttu-id="95524-117">Download het volgende technische document voor meer informatie: [Handelsovereenkomsten in Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).</span><span class="sxs-lookup"><span data-stu-id="95524-117">For more information, download the following white paper: [Trade agreements in Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).</span></span>

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a><span data-ttu-id="95524-118">Kan ik een inkooporder aan een verkooporder koppelen om aan de vraag te voldoen?</span><span class="sxs-lookup"><span data-stu-id="95524-118">Can I link a purchase order to a sales order to fulfill demand?</span></span>

<span data-ttu-id="95524-119">U kunt een inkooporder maken op basis van een verkooporder.</span><span class="sxs-lookup"><span data-stu-id="95524-119">You can create a purchase order from a sales order.</span></span> <span data-ttu-id="95524-120">Meer informatie vindt u in [Een inkooporder maken op basis van een verkooporder](tasks/create-purchase-order-sales-order.md).</span><span class="sxs-lookup"><span data-stu-id="95524-120">For more information, see [Create a purchase order from a sales order](tasks/create-purchase-order-sales-order.md).</span></span>

## <a name="i-cant-cancel-or-delete-a-return-order-or-a-sales-order"></a><span data-ttu-id="95524-121">Ik kan een retourorder of een verkooporder niet annuleren of verwijderen.</span><span class="sxs-lookup"><span data-stu-id="95524-121">I can't cancel or delete a return order or a sales order.</span></span>

<span data-ttu-id="95524-122">U kunt alleen verkooporders en retourorders annuleren die de status *Gemaakt* hebben.</span><span class="sxs-lookup"><span data-stu-id="95524-122">You can cancel only sales orders and return orders that are in a *Created* state.</span></span> <span data-ttu-id="95524-123">Zie voor meer informatie [Een retourorder annuleren](../service-management/cancel-return-order.md).</span><span class="sxs-lookup"><span data-stu-id="95524-123">For more information, see [Cancel a return order](../service-management/cancel-return-order.md).</span></span>

## <a name="when-i-try-to-cancel-a-sales-order-i-receive-a-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations-error"></a><span data-ttu-id="95524-124">Wanneer ik een verkooporder wil annuleren, krijg ik het bericht "Reserveringen kunnen niet worden verwijderd omdat er werk is gemaakt dat afhankelijk is van de reserveringen".</span><span class="sxs-lookup"><span data-stu-id="95524-124">When I try to cancel a sales order, I receive a "Reservations cannot be removed because there is work created which relies on the reservations" error.</span></span>

<span data-ttu-id="95524-125">Foutcode: WAX4661</span><span class="sxs-lookup"><span data-stu-id="95524-125">Error code: WAX4661</span></span>

<span data-ttu-id="95524-126">Als werk aan een verkooporder is gekoppeld, kunt u de verkooporder pas annuleren als het werk is geannuleerd en omgekeerd.</span><span class="sxs-lookup"><span data-stu-id="95524-126">If work is associated with a sales order, you can't cancel the sales order until the work is canceled and reversed.</span></span> <span data-ttu-id="95524-127">Deze vereiste geldt ook als het werk dat aan de verkooporder is gekoppeld, is afgesloten.</span><span class="sxs-lookup"><span data-stu-id="95524-127">This requirement applies even if the work that is associated with the sales order is closed.</span></span>

<span data-ttu-id="95524-128">Volg deze stappen om dit probleem op te lossen.</span><span class="sxs-lookup"><span data-stu-id="95524-128">To fix this issue, follow these steps.</span></span>

1. <span data-ttu-id="95524-129">Annuleer het werk en plaats voorraad terug op de gewenste locatie.</span><span class="sxs-lookup"><span data-stu-id="95524-129">Cancel the work, and put inventory back into the desired location.</span></span> <span data-ttu-id="95524-130">Ga naar de desbetreffende belasting van de verkooporder en selecteer **Opgenomen hoeveelheid reduceren** op de ladingsregel of **Werk omkeren** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="95524-130">Go to the relevant load of the sales order, and select either **Reduce picked quantity** on the load line or **Reverse work** on the Action Pane.</span></span>

    <span data-ttu-id="95524-131">Het werk heeft nu de status *Geannuleerd* en er wordt automatisch werk voor een nieuwe voorraadverplaatsing gemaakt en verwerkt om de voorraad terug te zetten op de locatie die op het moment van de omkering is beschreven.</span><span class="sxs-lookup"><span data-stu-id="95524-131">The work now has a status of *Canceled*, and new inventory movement work is automatically created and processed to put inventory back into the location that was described at the time of reversal.</span></span>

2. <span data-ttu-id="95524-132">Verwijder de lading.</span><span class="sxs-lookup"><span data-stu-id="95524-132">Delete the load.</span></span> <span data-ttu-id="95524-133">De verzending wordt ook verwijderd.</span><span class="sxs-lookup"><span data-stu-id="95524-133">The shipment is also deleted.</span></span>
3. <span data-ttu-id="95524-134">U moet nu naar de verkooporder kunnen gaan en deze kunnen annuleren.</span><span class="sxs-lookup"><span data-stu-id="95524-134">You should now be able to go to the sales order and cancel it.</span></span>

## <a name="i-cant-cancel-an-intercompany-purchase-order-that-is-linked-to-a-sales-order"></a><span data-ttu-id="95524-135">Ik kan een intercompany-inkooporder die aan een verkooporder is gekoppeld, niet annuleren.</span><span class="sxs-lookup"><span data-stu-id="95524-135">I can't cancel an intercompany purchase order that is linked to a sales order.</span></span>

### <a name="issue-description"></a><span data-ttu-id="95524-136">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="95524-136">Issue description</span></span>

<span data-ttu-id="95524-137">Als u probeert een intercompany-inkooporder te annuleren die aan een verkooporder is gekoppeld, wordt mogelijk het volgende foutbericht weergegeven: 'Hoeveelheid kan niet worden verminderd omdat de resterende bijwerkhoeveelheid van teken verandert'.</span><span class="sxs-lookup"><span data-stu-id="95524-137">If you try to cancel an intercompany purchase order that is linked to a sales order, you might receive the following error message: "Quantity cannot be reduced because the remaining update quantity changes sign."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="95524-138">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="95524-138">Issue resolution</span></span>

<span data-ttu-id="95524-139">Dit probleem is verholpen in Microsoft Dynamics 365 Supply Chain Management versie 10.0.13.</span><span class="sxs-lookup"><span data-stu-id="95524-139">This issue was fixed in Microsoft Dynamics 365 Supply Chain Management version 10.0.13.</span></span> <span data-ttu-id="95524-140">In deze versie en latere versies kunt u nu een intercompany-inkooporder annuleren die aan een verkooporder is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="95524-140">In that version and later versions, you can now cancel an intercompany purchase order that is linked to a sales order.</span></span>

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a><span data-ttu-id="95524-141">Kan ik een gefactureerde verkooporder terugzetten als die is verwijderd?</span><span class="sxs-lookup"><span data-stu-id="95524-141">Can I restore an invoiced sales order that was deleted?</span></span>

### <a name="issue-description"></a><span data-ttu-id="95524-142">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="95524-142">Issue description</span></span>

<span data-ttu-id="95524-143">Een gefactureerde verkooporder is per ongeluk verwijderd en u wilt deze herstellen of de details weergeven.</span><span class="sxs-lookup"><span data-stu-id="95524-143">An invoiced sales order was deleted by mistake, and you want to restore it or view its details.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="95524-144">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="95524-144">Issue resolution</span></span>

<span data-ttu-id="95524-145">Als de verwijderde verkooporder al is gefactureerd, gaat u naar **Klantaccount \> Transacties \> Oorspronkelijke document \> Details weergeven**.</span><span class="sxs-lookup"><span data-stu-id="95524-145">If the deleted sales order has already been invoiced, go to **Customer account \> Transactions \> Original document \> View details**.</span></span> <span data-ttu-id="95524-146">Zoek de factuur waarnaar u op zoek bent en selecteer deze om de details weer te geven.</span><span class="sxs-lookup"><span data-stu-id="95524-146">Find the invoice that you're looking for, and select it to view its details.</span></span> <span data-ttu-id="95524-147">Deze gegevens omvatten de verkooporderverwijzing.</span><span class="sxs-lookup"><span data-stu-id="95524-147">These details include the sales order reference.</span></span> <span data-ttu-id="95524-148">Op die pagina hebt u ook toegang tot de verkoopordergegevens.</span><span class="sxs-lookup"><span data-stu-id="95524-148">You should also be able to access the sales order details from that page.</span></span>

## <a name="the-deadline-of-a-sales-order-header-cant-be-found-in-the-salesorderheaderv2entity-data-entity"></a><span data-ttu-id="95524-149">De deadline van een verkooporderkoptekst staat niet in de gegevensentiteit SalesOrderHeaderV2Entity.</span><span class="sxs-lookup"><span data-stu-id="95524-149">The deadline of a sales order header can't be found in the SalesOrderHeaderV2Entity data entity.</span></span>

<span data-ttu-id="95524-150">Het veld Deadline bestaat niet in de entiteit *SalesOrderHeaderV2Entity*.</span><span class="sxs-lookup"><span data-stu-id="95524-150">The deadline field doesn't exist on the *SalesOrderHeaderV2Entity* entity.</span></span>

## <a name="i-must-delete-orphaned-sales-order-records"></a><span data-ttu-id="95524-151">Ik moet zwevende verkooporderrecords verwijderen.</span><span class="sxs-lookup"><span data-stu-id="95524-151">I must delete orphaned sales order records.</span></span>

<span data-ttu-id="95524-152">Als u zwevende verkooporderrecords wilt opschonen, voert u de periodieke taak *Verkooporders verwijderen* uit door naar een van de volgende locaties te gaan:</span><span class="sxs-lookup"><span data-stu-id="95524-152">To clean up orphaned sales order records, run the *Sales order deletion* periodic job by going to either of the following places:</span></span>

- <span data-ttu-id="95524-153">Verkoop en marketing \> Periodieke taken \> Opschonen \> Verkooporders verwijderen</span><span class="sxs-lookup"><span data-stu-id="95524-153">Sales and marketing \> Periodic tasks \> Clean up \> Delete sales orders</span></span>
- <span data-ttu-id="95524-154">Detailhandel en commerce \> IT detailhandel en commerce \> Opschonen \> Verkooporders verwijderen</span><span class="sxs-lookup"><span data-stu-id="95524-154">Retail and commerce \> Retail and commerce IT \> Clean up \> Delete sales orders</span></span>

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a><span data-ttu-id="95524-155">Is er een manier om commissies te berekenen op facturen die al zijn geboekt?</span><span class="sxs-lookup"><span data-stu-id="95524-155">Is there a way to calculate commissions on invoices that have already been posted?</span></span>

<span data-ttu-id="95524-156">Supply Chain Management biedt momenteel geen ondersteuning voor de berekening van commissies voor geboekte facturen.</span><span class="sxs-lookup"><span data-stu-id="95524-156">Supply Chain Management doesn't currently support the calculation of commissions for posted invoices.</span></span>

## <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a><span data-ttu-id="95524-157">Een bundelartikel wordt niet ondersteund in een intercompany-proces.</span><span class="sxs-lookup"><span data-stu-id="95524-157">A bundle item isn't supported in an intercompany process.</span></span>

<span data-ttu-id="95524-158">Het bundelartikel is niet beschikbaar voor de inkooporder, want als u de verkooporderregels voor het bundelartikel bekijkt, ziet u dat de hoeveelheid *0* (nul) is en de status *Geannuleerd*.</span><span class="sxs-lookup"><span data-stu-id="95524-158">The bundle item isn't available for the purchase order because, if you examine the sales order lines for the bundle item, you will notice that the quantity is *0* (zero) and the status is *Canceled*.</span></span> <span data-ttu-id="95524-159">Dit is zo ontworpen.</span><span class="sxs-lookup"><span data-stu-id="95524-159">This behavior is by design.</span></span> <span data-ttu-id="95524-160">In de verkooporder worden alleen de onderdelen van het bundelartikel gekocht.</span><span class="sxs-lookup"><span data-stu-id="95524-160">The sales order buys only the components of the bundle item.</span></span> <span data-ttu-id="95524-161">In de verkooporder wordt niet het bundelartikel zelf gekocht.</span><span class="sxs-lookup"><span data-stu-id="95524-161">It doesn't buy the bundle item itself.</span></span>

<span data-ttu-id="95524-162">Als u een bundel moet aanschaffen, overweeg dan of u deze als een bundelartikel moet markeren, omdat deze functionaliteit eigenlijk is bedoeld voor opbrengsttoerekeningsscenario's.</span><span class="sxs-lookup"><span data-stu-id="95524-162">If you must buy a bundle, consider whether you have to mark it as bundle item, because this functionality is designed for revenue recognition scenarios.</span></span> <span data-ttu-id="95524-163">Meer informatie over bundelartikelen vindt u in [Bundels](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).</span><span class="sxs-lookup"><span data-stu-id="95524-163">For more information about bundle items, see [Bundles](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]