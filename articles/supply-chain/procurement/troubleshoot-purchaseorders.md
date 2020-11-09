---
title: Problemen met inkooporders oplossen
description: In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met inkooporders.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 234458f865e37a2d962aee8ab218b9521847081d
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018555"
---
# <a name="troubleshoot-purchase-orders"></a><span data-ttu-id="dec55-103">Problemen met inkooporders oplossen</span><span class="sxs-lookup"><span data-stu-id="dec55-103">Troubleshoot purchase orders</span></span>

<span data-ttu-id="dec55-104">In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met inkooporders.</span><span class="sxs-lookup"><span data-stu-id="dec55-104">This topic describes how to fix issues that you might encounter while you work with purchase orders.</span></span>

## <a name="an-action-can-be-completed-only-after-the-line-number-is-fully-distributed"></a><span data-ttu-id="dec55-105">Een actie kan pas worden voltooid nadat het regelnummer volledig is verdeeld.</span><span class="sxs-lookup"><span data-stu-id="dec55-105">An action can be completed only after the line number is fully distributed.</span></span>

<span data-ttu-id="dec55-106">Dit probleem kan optreden vanwege inconsistenties in inkooporderdistributies.</span><span class="sxs-lookup"><span data-stu-id="dec55-106">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="dec55-107">Als u dit probleem wilt verhelpen en de inkooporder wilt terugzetten op de status *Concept* , gaat u naar **Inkoopbeheer \> Periodieke taken \> Opschonen \> Distributie van inkooporder opnieuw instellen**.</span><span class="sxs-lookup"><span data-stu-id="dec55-107">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="dec55-108">Zie het volgende blogbericht voor meer informatie: [Fouten met IO-distributie in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/) oplossen.</span><span class="sxs-lookup"><span data-stu-id="dec55-108">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="when-purchase-orders-are-imported-through-data-management-purchase-order-line-numbers-dont-follow-the-increment-that-defined-in-system-parameters"></a><span data-ttu-id="dec55-109">Wanneer inkooporders worden geïmporteerd via gegevensbeheer, volgen de nummers van de inkooporderregels niet de verhoging die is gedefinieerd in de systeemparameters.</span><span class="sxs-lookup"><span data-stu-id="dec55-109">When purchase orders are imported through data management, purchase order line numbers don't follow the increment that defined in system parameters.</span></span>

### <a name="issue-description"></a><span data-ttu-id="dec55-110">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="dec55-110">Issue description</span></span>

<span data-ttu-id="dec55-111">Automatisch gegenereerde regelnummers voor inkooporderregels die worden geïmporteerd via de gegevensentiteit *Inkooporderregels V2* gebruiken niet de systeemregelnummerverhoging die is opgegeven in systeemparameters.</span><span class="sxs-lookup"><span data-stu-id="dec55-111">By default, automatically generated line numbers for purchase order lines that are imported through the *Purchase order lines V2* data entity don't use the system line number increment that is specified in system parameters.</span></span> <span data-ttu-id="dec55-112">Als u handmatig een inkooporder maakt en regels toevoegt via de gebruikersinterface (UI), worden de regelnummers juist verhoogd.</span><span class="sxs-lookup"><span data-stu-id="dec55-112">If you manually create a purchase order and add lines through the user interface (UI), the line numbers are incremented correctly.</span></span> <span data-ttu-id="dec55-113">Als u echter het DMF (Data Management Framework) gebruikt, worden ze niet op de juiste wijze verhoogd.</span><span class="sxs-lookup"><span data-stu-id="dec55-113">However, if you use the Data management framework (DMF), they aren't incremented correctly.</span></span>

<span data-ttu-id="dec55-114">Dit probleem treedt op omdat het systeem bij het importeren van regels via DMF de methode van het DMF gebruikt voor het toewijzen van regels als regelnummers nog niet zijn toegewezen in de geïmporteerde entiteit.</span><span class="sxs-lookup"><span data-stu-id="dec55-114">This issue occurs because, when you import lines via DMF, if line numbers aren't already assigned in the imported entity, the system uses DMF's method for assigning them.</span></span> <span data-ttu-id="dec55-115">Met deze methode worden regelnummers altijd met één verhoogd.</span><span class="sxs-lookup"><span data-stu-id="dec55-115">That method always increments line numbers by one.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="dec55-116">Tijdelijke oplossing voor probleem</span><span class="sxs-lookup"><span data-stu-id="dec55-116">Issue workaround</span></span>

<span data-ttu-id="dec55-117">Zorg ervoor dat de gewenste regelnummers al zijn opgegeven in de regelnummervelden van de entiteit wanneer u de inkooporderregels importeert.</span><span class="sxs-lookup"><span data-stu-id="dec55-117">Make sure that the desired line numbers are already given in the data entity line number fields when you import the purchase order lines.</span></span> <span data-ttu-id="dec55-118">In dit geval worden de regelnummers niet overschreven door DMF.</span><span class="sxs-lookup"><span data-stu-id="dec55-118">In this case, DMF won't overwrite the line numbers.</span></span>

## <a name="a-default-tax-group-and-a-default-cash-discount-arent-filled-in-from-the-invoice-account"></a><span data-ttu-id="dec55-119">Een standaardbelastinggroep en een standaardcontantkorting worden niet ingevuld op basis van de factuurrekening.</span><span class="sxs-lookup"><span data-stu-id="dec55-119">A default tax group and a default cash discount aren't filled in from the invoice account.</span></span>

<span data-ttu-id="dec55-120">Als u een factuurrekening gebruikt die verschilt van de klantrekening, worden er geen standaardbelastinggroep en standaardcontantkorting ingevuld op basis van de factuurrekening wanneer er een inkooporder wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="dec55-120">If you're using an invoice account that differs from the customer account, a default tax group and a default cash discount aren't filled in from the invoice account when a purchase order is created.</span></span>

<span data-ttu-id="dec55-121">Dit is zo ontworpen.</span><span class="sxs-lookup"><span data-stu-id="dec55-121">This behavior is by design.</span></span> <span data-ttu-id="dec55-122">De standaardwaarden voor de belastinggroep, contantkortingen en andere prijsgegevens zijn gebaseerd op de klantrekening, niet op de factuurrekening.</span><span class="sxs-lookup"><span data-stu-id="dec55-122">The default values for the tax group, cash discounts, and other price information are based on the customer account, not the invoice account.</span></span>

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a><span data-ttu-id="dec55-123">Tijdens een inkooporderbevestiging wordt het foutbericht weergegeven dat de objectverwijzing niet is ingesteld of er wordt een uitzondering gegenereerd door het doel van een aanroep. Tijdens het boeken van leveranciersfacturen treedt er een uitzondering op.</span><span class="sxs-lookup"><span data-stu-id="dec55-123">I receive an "Object reference not set" error during purchase order confirmation, or an "Exception has been thrown by the target of an invocation" exception occurs during vendor invoice posting.</span></span>

<span data-ttu-id="dec55-124">Dit probleem kan optreden vanwege inconsistenties in inkooporderdistributies.</span><span class="sxs-lookup"><span data-stu-id="dec55-124">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="dec55-125">Als u dit probleem wilt verhelpen en de inkooporder wilt terugzetten op de status *Concept* , gaat u naar **Inkoopbeheer \> Periodieke taken \> Opschonen \> Distributie van inkooporder opnieuw instellen**.</span><span class="sxs-lookup"><span data-stu-id="dec55-125">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="dec55-126">Zie het volgende blogbericht voor meer informatie: [Fouten met IO-distributie in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/) oplossen.</span><span class="sxs-lookup"><span data-stu-id="dec55-126">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a><span data-ttu-id="dec55-127">Een of meer boekhoudingsverdelingen is te veel of te weinig verdeeld.</span><span class="sxs-lookup"><span data-stu-id="dec55-127">One or more accounting distributions are either over-distributed or under-distributed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="dec55-128">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="dec55-128">Issue description</span></span>

<span data-ttu-id="dec55-129">Het volgende foutbericht wordt weergegeven: Een of meer boekhoudingsverdelingen is te veel of te weinig verdeeld.</span><span class="sxs-lookup"><span data-stu-id="dec55-129">You receive the following error: "One or more accounting distributions is either over-distributed or under-distributed."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="dec55-130">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="dec55-130">Issue resolution</span></span>

<span data-ttu-id="dec55-131">Dit probleem kan optreden vanwege inconsistenties in inkooporderdistributies.</span><span class="sxs-lookup"><span data-stu-id="dec55-131">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="dec55-132">Als u dit probleem wilt verhelpen en de inkooporder wilt terugzetten op de status *Concept* , gaat u naar **Inkoopbeheer \> Periodieke taken \> Opschonen \> Distributie van inkooporder opnieuw instellen**.</span><span class="sxs-lookup"><span data-stu-id="dec55-132">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="dec55-133">Zie het volgende blogbericht voor meer informatie: [Fouten met IO-distributie in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/) oplossen.</span><span class="sxs-lookup"><span data-stu-id="dec55-133">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="can-i-show-only-purchase-orders-that-i-created"></a><span data-ttu-id="dec55-134">Kan ik alleen inkooporders weergeven die ik heb gemaakt?</span><span class="sxs-lookup"><span data-stu-id="dec55-134">Can I show only purchase orders that I created?</span></span>

<span data-ttu-id="dec55-135">Deze functionaliteit is momenteel niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="dec55-135">This functionality isn't currently available.</span></span>

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a><span data-ttu-id="dec55-136">Kan ik voorraad reserveren en transacties maken voor geregistreerde voorraad op een inkooporder?</span><span class="sxs-lookup"><span data-stu-id="dec55-136">Can I reserve inventory and create transactions against registered inventory on a purchase order?</span></span>

### <a name="issue-description"></a><span data-ttu-id="dec55-137">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="dec55-137">Issue description</span></span>

<span data-ttu-id="dec55-138">Zelfs wanneer artikelen de status *Geregistreerd* in een inkooporder hebben, kunt u nog steeds de voorraad reserveren.</span><span class="sxs-lookup"><span data-stu-id="dec55-138">Even when items are in a *Registered* state on a purchase order, you can still reserve the inventory.</span></span> <span data-ttu-id="dec55-139">Met andere woorden, u kunt transacties maken voor de geregistreerde voorraad.</span><span class="sxs-lookup"><span data-stu-id="dec55-139">In other words, you can create transactions against the registered inventory.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="dec55-140">Het probleem reproduceren</span><span class="sxs-lookup"><span data-stu-id="dec55-140">Reproduce the issue</span></span>

<span data-ttu-id="dec55-141">In de volgende procedure wordt één manier weergegeven om het probleem te reproduceren.</span><span class="sxs-lookup"><span data-stu-id="dec55-141">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="dec55-142">Inkooporder maken.</span><span class="sxs-lookup"><span data-stu-id="dec55-142">Create a purchase order.</span></span>
2. <span data-ttu-id="dec55-143">Registreer de inkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="dec55-143">Register the purchase order line.</span></span>
3. <span data-ttu-id="dec55-144">U ziet dat u reserveringen of transacties voor de geregistreerde voorraad kunt genereren.</span><span class="sxs-lookup"><span data-stu-id="dec55-144">Notice that you can generate reservations or transactions against the registered inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="dec55-145">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="dec55-145">Issue resolution</span></span>

<span data-ttu-id="dec55-146">Dit is zo ontworpen.</span><span class="sxs-lookup"><span data-stu-id="dec55-146">This behavior is by design.</span></span> <span data-ttu-id="dec55-147">De verwachting is dat de geregistreerde artikelen fysiek zijn aangekomen in het magazijn of voorraad en dat ze daarom beschikbaar zijn voor reservering.</span><span class="sxs-lookup"><span data-stu-id="dec55-147">The expectation is that the registered items have physically arrived in the warehouse or inventory, and that they are therefore available for reservation.</span></span>

## <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a><span data-ttu-id="dec55-148">Inkooporders reflecteren niet de taalinstellingen van de rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="dec55-148">Purchase orders don't reflect the language settings of the legal entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="dec55-149">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="dec55-149">Issue description</span></span>

<span data-ttu-id="dec55-150">De productnaam op een inkooporder wordt weergegeven in de systeemtaal in plaats van de taal die is ingesteld voor de rechtspersoon waarvoor de inkooporder is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="dec55-150">The product name on a purchase order is shown in the system language instead of the language that is set for the legal entity where the purchase order was created.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="dec55-151">Het probleem reproduceren</span><span class="sxs-lookup"><span data-stu-id="dec55-151">Reproduce the issue</span></span>

<span data-ttu-id="dec55-152">In de volgende procedure wordt één manier weergegeven om het probleem te reproduceren.</span><span class="sxs-lookup"><span data-stu-id="dec55-152">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="dec55-153">Stel de systeemtaal in op *en-US* (Amerikaans-Engels).</span><span class="sxs-lookup"><span data-stu-id="dec55-153">Set the system language to *EN-US* (US English).</span></span>
1. <span data-ttu-id="dec55-154">Zorg ervoor dat er een product is waarin de talen *en_US* en *de* (Duits) worden onderhouden voor vertalingen van de productnaam.</span><span class="sxs-lookup"><span data-stu-id="dec55-154">Make sure that there is a product where the *EN-US* and *DE* (German) languages are maintained for translations of the product name.</span></span>
1. <span data-ttu-id="dec55-155">De taal van een rechtspersoon wijzigen in *de*.</span><span class="sxs-lookup"><span data-stu-id="dec55-155">Change the language of a legal entity to *DE*.</span></span>
1. <span data-ttu-id="dec55-156">Maak in de rechtspersoon waarvoor de taal *de* is ingesteld een inkooporder die het product bevat.</span><span class="sxs-lookup"><span data-stu-id="dec55-156">In the legal entity where *DE* is set as the language, create a purchase order that includes the product.</span></span>
1. <span data-ttu-id="dec55-157">U ziet dat de productnaam nog steeds wordt weergegeven in Amerikaans Engels (de systeemtaal).</span><span class="sxs-lookup"><span data-stu-id="dec55-157">Notice that the product name is still shown in US English (the system language).</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="dec55-158">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="dec55-158">Issue resolution</span></span>

<span data-ttu-id="dec55-159">Dit is zo ontworpen.</span><span class="sxs-lookup"><span data-stu-id="dec55-159">This behavior is by design.</span></span> <span data-ttu-id="dec55-160">Op inkooporders wordt het product altijd weergegeven in de systeemtaal.</span><span class="sxs-lookup"><span data-stu-id="dec55-160">On purchase orders, the product is always shown in the system language.</span></span> <span data-ttu-id="dec55-161">De taal van de inkooporder wordt gebruikt bij het maken van een bevestigingsjournaal.</span><span class="sxs-lookup"><span data-stu-id="dec55-161">The purchase order language is used when a confirmation journal is created.</span></span>

## <a name="the-approved-vendor-list-by-product-entity-doesnt-allow-the-effective-date-to-be-changed"></a><span data-ttu-id="dec55-162">De ingangsdatum kan niet per productentiteit worden gewijzigd in de lijst met goedgekeurde leveranciers.</span><span class="sxs-lookup"><span data-stu-id="dec55-162">The Approved vendor list by product entity doesn't allow the effective date to be changed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="dec55-163">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="dec55-163">Issue description</span></span>

<span data-ttu-id="dec55-164">Een product heeft een goedgekeurde leverancier die bijvoorbeeld een ingangsdatum heeft van 11 januari 2018 ( *01/11/2018* ) en de vervaldatum *Nooit*.</span><span class="sxs-lookup"><span data-stu-id="dec55-164">A product has an approved vendor that has, for example, an effective date of January 11, 2018 ( *01/11/2018* ), and an expiration date of *Never*.</span></span> <span data-ttu-id="dec55-165">Als u de ingangsdatum probeert te wijzigen in 10 januari 2018 ( *01/10/2018* ) of 12 januari 2018 ( *01/12/2018* ), wordt het volgende foutbericht weergegeven:</span><span class="sxs-lookup"><span data-stu-id="dec55-165">If you try to change the effective date to January 10, 2018 ( *01/10/2018* ), or January 12, 2018 ( *01/12/2018* ), you receive the following error:</span></span>

> <span data-ttu-id="dec55-166">Kan geen record maken in lijst met goedgekeurde leveranciers (PdsApproveVendorList).</span><span class="sxs-lookup"><span data-stu-id="dec55-166">Cannot create a record in Approved supplier list (PdsApproveVendorList).</span></span> <span data-ttu-id="dec55-167">De waarde voor Vervaldatum moet groter zijn dan of gelijk zijn aan die van de Ingangsdatum.</span><span class="sxs-lookup"><span data-stu-id="dec55-167">The 'Expiration' value needs to be greater than or equal to the 'Effective' value.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="dec55-168">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="dec55-168">Issue resolution</span></span>

<span data-ttu-id="dec55-169">U kunt alleen de periode verlengen waarvoor de leverancier is goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="dec55-169">You can only extend the period that the vendor is approved for.</span></span> <span data-ttu-id="dec55-170">De volgende regels zijn van toepassing:</span><span class="sxs-lookup"><span data-stu-id="dec55-170">The following rules apply:</span></span>

- <span data-ttu-id="dec55-171">Als u de ingangsdatum zo wilt wijzigen dat deze eerder is dan een van de bestaande records (perioden) voor de leverancier van het artikel, moet de vervaldatum van de nieuwe periode eerder zijn dan de vervaldatums in de bestaande records.</span><span class="sxs-lookup"><span data-stu-id="dec55-171">To change the effective date so that it's earlier than any of the existing records (periods) for the item vendor, the expiration date of the new period must be before all the expiration dates in the existing records.</span></span>
- <span data-ttu-id="dec55-172">Als u de vervaldatum zo wilt wijzigen dat deze later is dan een van de bestaande perioden, moet de ingangsdatum na de laatste vervaldatum in een bestaande record vallen.</span><span class="sxs-lookup"><span data-stu-id="dec55-172">To change the expiration date so that it's later than any of the existing periods, the effective date must be after the latest expiration date in any existing record.</span></span>
- <span data-ttu-id="dec55-173">Als u de totale periode waarvoor de leverancier is goedgekeurd, wilt verkorten, moet u bestaande records verwijderen of wijzigen.</span><span class="sxs-lookup"><span data-stu-id="dec55-173">To reduce the overall period that the vendor is approved for, you must delete or modify existing records.</span></span> <span data-ttu-id="dec55-174">U kunt ook de schakeloptie **Afkappen** gebruiken tijdens het importeren.</span><span class="sxs-lookup"><span data-stu-id="dec55-174">Alternatively, you can use the **truncate** switch during import.</span></span> <span data-ttu-id="dec55-175">Met deze schakeloptie verwijdert u alle bestaande records in de tabel voor goedgekeurde leveranciers per artikel.</span><span class="sxs-lookup"><span data-stu-id="dec55-175">This switch deletes all existing records in the table for approved vendors by item.</span></span>

<span data-ttu-id="dec55-176">Voor het voorbeeldscenario dat in de beschrijving van het probleem wordt beschreven, waarbij een record de ingangsdatum *01/11/2018* en de vervaldatum van *Nooit* heeft, kunt u een nieuwe record importeren met de ingangsdatum *01/10/2018* en de vervaldatum *Nooit*.</span><span class="sxs-lookup"><span data-stu-id="dec55-176">For the example scenario that is described in the issue description, where a record has an effective date of *01/11/2018* and an expiration date of *Never* , you can import a new record that has an effective date of *01/10/2018* and an expiration date of *Never*.</span></span> <span data-ttu-id="dec55-177">Het is echter niet mogelijk om via gegevensbeheer de periode zo te verkleinen dat de ingangsdatum wordt bijgewerkt naar *01/12/2018*.</span><span class="sxs-lookup"><span data-stu-id="dec55-177">However, you can't reduce the period so that the effective date is updated to *01/12/2018* via data management.</span></span> <span data-ttu-id="dec55-178">U moet deze wijziging aanbrengen in de gebruikersinterface.</span><span class="sxs-lookup"><span data-stu-id="dec55-178">You must make this change through the UI.</span></span>

## <a name="after-i-change-the-delivery-address-on-a-purchase-order-header-the-delivery-nameisnt-synced"></a><span data-ttu-id="dec55-179">Nadat ik het afleveradres in een inkooporderkop heb gewijzigd, wordt de leveringsnaam niet gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="dec55-179">After I change the delivery address on a purchase order header, the delivery name isn't synced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="dec55-180">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="dec55-180">Issue description</span></span>

<span data-ttu-id="dec55-181">Het adres in de koptekst van een inkooporder wordt bijgewerkt naar een adres dat geen afleveradres is.</span><span class="sxs-lookup"><span data-stu-id="dec55-181">The address on the header of a purchase order is updated to an address that isn't a delivery address.</span></span> <span data-ttu-id="dec55-182">Hoewel het adres op de inkooporder wordt bijgewerkt, wordt de leveringsnaam niet bijgewerkt op basis van het bijgewerkte adres.</span><span class="sxs-lookup"><span data-stu-id="dec55-182">Although the address is updated on the purchase order, the delivery name isn't updated based on the updated address.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="dec55-183">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="dec55-183">Issue resolution</span></span>

<span data-ttu-id="dec55-184">Dit is zo ontworpen.</span><span class="sxs-lookup"><span data-stu-id="dec55-184">This behavior is by design.</span></span> <span data-ttu-id="dec55-185">Het geselecteerde adres moet worden geclassificeerd als afleveradres.</span><span class="sxs-lookup"><span data-stu-id="dec55-185">The selected address must be classified as a delivery address.</span></span> <span data-ttu-id="dec55-186">Anders wordt de leveringsnaam niet bijgewerkt op basis van het geselecteerde adres.</span><span class="sxs-lookup"><span data-stu-id="dec55-186">Otherwise, the delivery name isn't updated based on the selected address.</span></span>

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a><span data-ttu-id="dec55-187">Kan ik de gebruiker vinden die een inkooporder heeft geannuleerd?</span><span class="sxs-lookup"><span data-stu-id="dec55-187">Can I find the user who canceled a purchase order?</span></span>

<span data-ttu-id="dec55-188">Deze informatie wordt alleen bijgehouden als de inkooporder onder wijzigingsbeheer valt.</span><span class="sxs-lookup"><span data-stu-id="dec55-188">This information is tracked only if the purchase order is subject to change management.</span></span> <span data-ttu-id="dec55-189">Als u wijzigingsbeheer gebruikt, kunt u zien wie de wijziging heeft ingediend (de annulering) en wie deze heeft goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="dec55-189">If you use change management, you can see who submitted the change (the cancellation), and who approved it.</span></span>
