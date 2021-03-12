---
title: Problemen met productontvangstbonnen en -facturering oplossen
description: In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden terwijl u werkt met productontvangstbonnen en -facturering.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 22b1abec0c6dd5f571e604c5c07379b397b8bdaa
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999048"
---
# <a name="troubleshoot-product-receipts-and-invoicing"></a><span data-ttu-id="bdc12-103">Problemen met productontvangstbonnen en -facturering oplossen</span><span class="sxs-lookup"><span data-stu-id="bdc12-103">Troubleshoot product receipts and invoicing</span></span>

<span data-ttu-id="bdc12-104">In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden terwijl u werkt met productontvangstbonnen en -facturering.</span><span class="sxs-lookup"><span data-stu-id="bdc12-104">This topic describes how to fix issues that you might encounter while you work with product receipts and invoicing.</span></span>

## <a name="i-cant-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a><span data-ttu-id="bdc12-105">Ik kan niet meer dan één factuur boeken voor een inkooporderregel die op categorieën gebaseerde artikelen bevat.</span><span class="sxs-lookup"><span data-stu-id="bdc12-105">I can't post more than one invoice for a purchase order line that has category-based items.</span></span>

<span data-ttu-id="bdc12-106">Een hoeveelheid is verplicht als u facturen wilt boeken.</span><span class="sxs-lookup"><span data-stu-id="bdc12-106">A quantity is mandatory if you want to post invoices.</span></span> <span data-ttu-id="bdc12-107">Als de volledige hoeveelheid van een regel slechts voor een gedeeltelijk bedrag is gefactureerd, kunt u het resterende bedrag niet op een andere factuur factureren.</span><span class="sxs-lookup"><span data-stu-id="bdc12-107">Therefore, if the full quantity of a line has been invoiced for only a partial amount, you won't be able to invoice the remaining amount on another invoice.</span></span>

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a><span data-ttu-id="bdc12-108">Tijdens een inkooporderbevestiging wordt het foutbericht weergegeven dat de objectverwijzing niet is ingesteld of er wordt een uitzondering gegenereerd door het doel van een aanroep. Tijdens het boeken van leveranciersfacturen treedt er een uitzondering op.</span><span class="sxs-lookup"><span data-stu-id="bdc12-108">I receive an "Object reference not set" error during purchase order confirmation, or an "Exception has been thrown by the target of an invocation" exception occurs during vendor invoice posting.</span></span>

<span data-ttu-id="bdc12-109">Dit probleem kan optreden vanwege inconsistenties in inkooporderdistributies.</span><span class="sxs-lookup"><span data-stu-id="bdc12-109">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="bdc12-110">Als u dit probleem wilt verhelpen en de inkooporder wilt terugzetten op de status *Concept*, gaat u naar **Inkoopbeheer \> Periodieke taken \> Opschonen \> Distributie van inkooporder opnieuw instellen**.</span><span class="sxs-lookup"><span data-stu-id="bdc12-110">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="bdc12-111">Zie het volgende blogbericht voor meer informatie: [Fouten met IO-distributie in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/) oplossen.</span><span class="sxs-lookup"><span data-stu-id="bdc12-111">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="i-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a><span data-ttu-id="bdc12-112">Ik kan niet meerdere productontvangstbonnen in één inkooporder consolideren.</span><span class="sxs-lookup"><span data-stu-id="bdc12-112">I can't consolidate multiple product receipts into a single purchase order.</span></span>

<span data-ttu-id="bdc12-113">U kunt niet meerdere productontvangstbonnen consolideren in één inkooporder als de verschillende productontvangstbonregels verschillende boekingsdatums hebben.</span><span class="sxs-lookup"><span data-stu-id="bdc12-113">You can't consolidate multiple product receipts into a single purchase order if the different product receipt lines have different accounting dates.</span></span>

<span data-ttu-id="bdc12-114">In eerdere versies van Microsoft Dynamics 365 Supply Chain Management was consolidatie in deze situatie toegestaan.</span><span class="sxs-lookup"><span data-stu-id="bdc12-114">In earlier versions of Microsoft Dynamics 365 Supply Chain Management, consolidation was allowed in this situation.</span></span> <span data-ttu-id="bdc12-115">Dit bleek is echter foutgevoelig te zijn.</span><span class="sxs-lookup"><span data-stu-id="bdc12-115">However, the practice is prone to error.</span></span> <span data-ttu-id="bdc12-116">De boekhoudingsdatum op de gemaakte inkooporderregels mag niet verschillen van de boekhoudingsdatum op de productontvangstbonregels waarop deze inkooporderregels zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="bdc12-116">The accounting date on the purchase order lines that are created should not differ from the accounting date on the product receipt lines that those purchase order lines were created from.</span></span> <span data-ttu-id="bdc12-117">(De boekhoudingsdatum op de inkooporderregels komt overeen met de boekhoudingsdatum in de koptekst van de inkooporder.) De consolidatie van meerdere productontvangstbonnen in één inkooporder is daarom niet meer toegestaan.</span><span class="sxs-lookup"><span data-stu-id="bdc12-117">(The accounting date on the purchase order lines matches the accounting date on the purchase order header.) Therefore, the consolidation of multiple product receipts into a single purchase orders is no longer allowed.</span></span>

<span data-ttu-id="bdc12-118">De boekhoudingsdatum wordt bijvoorbeeld gebruikt voor budgetreserveringen en vordering.</span><span class="sxs-lookup"><span data-stu-id="bdc12-118">The accounting date is used, for example, for budget reservations and encumbrance.</span></span> <span data-ttu-id="bdc12-119">Daarom moet deze tijdens de overgang van productontvangstbon naar de inkooporder worden bewaard.</span><span class="sxs-lookup"><span data-stu-id="bdc12-119">Therefore, it should be kept during the transition from product receipt to purchase order.</span></span>

## <a name="when-product-receipts-are-canceled-transactions-can-be-posted-to-a-suspended-ledger-account"></a><span data-ttu-id="bdc12-120">Wanneer productontvangstbonnen worden geannuleerd, kunnen transacties naar een uitgestelde grootboekrekening worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="bdc12-120">When product receipts are canceled, transactions can be posted to a suspended ledger account.</span></span>

### <a name="issue-description"></a><span data-ttu-id="bdc12-121">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="bdc12-121">Issue description</span></span>

<span data-ttu-id="bdc12-122">Als een productontvangstbon wordt geannuleerd, kunnen transacties naar uitgestelde grootboekrekeningen worden geboekt, zelfs als de hoofdrekeningen zijn opgeschort.</span><span class="sxs-lookup"><span data-stu-id="bdc12-122">If a product receipt is canceled, the system allows transactions to be posted to suspended ledger accounts, even though the main accounts are suspended.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="bdc12-123">Het probleem reproduceren</span><span class="sxs-lookup"><span data-stu-id="bdc12-123">Reproduce the issue</span></span>

<span data-ttu-id="bdc12-124">In de volgende procedure wordt één manier weergegeven om het probleem te reproduceren.</span><span class="sxs-lookup"><span data-stu-id="bdc12-124">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="bdc12-125">Controleer op de pagina **Parameters van module Leveranciers** op het tabblad **Algemeen** of de optie **Productontvangstbon in grootboek boeken** is ingesteld op *Ja*.</span><span class="sxs-lookup"><span data-stu-id="bdc12-125">On the **Accounts payable parameters** page, on the **General** tab, make sure that the **Post product receipt in ledger** option is set to *Yes*.</span></span>
1. <span data-ttu-id="bdc12-126">Maak een inkooporder en voeg een orderregel toe met een hoeveelheid van *1000* voor een product.</span><span class="sxs-lookup"><span data-stu-id="bdc12-126">Create a purchase order, and add an order line that has a quantity of *1,000* for a product.</span></span>
1. <span data-ttu-id="bdc12-127">Bevestig de inkooporder.</span><span class="sxs-lookup"><span data-stu-id="bdc12-127">Confirm the purchase order.</span></span>
1. <span data-ttu-id="bdc12-128">Boek de productontvangstbon en controleer de boekstukken.</span><span class="sxs-lookup"><span data-stu-id="bdc12-128">Post the product receipt, and check the vouchers.</span></span>
1. <span data-ttu-id="bdc12-129">Schort de relevante hoofdrekeningen, *200140* en *140200*, op.</span><span class="sxs-lookup"><span data-stu-id="bdc12-129">Suspend the relevant main accounts, *200140* and *140200*.</span></span>
1. <span data-ttu-id="bdc12-130">Annuleer de geboekte productontvangstbon.</span><span class="sxs-lookup"><span data-stu-id="bdc12-130">Cancel the posted product receipt.</span></span>
1. <span data-ttu-id="bdc12-131">U ziet dat transacties naar de uitgestelde grootboekrekeningen kunnen worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="bdc12-131">Notice that transactions can be posted to the suspended leger accounts.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="bdc12-132">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="bdc12-132">Issue resolution</span></span>

<span data-ttu-id="bdc12-133">Transacties kunnen worden geboekt naar de opgeschorte grootboekrekeningen wanneer productontvangstbonnen worden geannuleerd, omdat met dit gedrag correcte boekingen mogelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="bdc12-133">Transactions can be posted to the suspended leger accounts when product receipts are canceled, because this behavior allows for correct postings.</span></span>

## <a name="a-product-receipt-voucher-number-is-consumed-even-if-no-financial-voucher-is-generated-during-product-receipt"></a><span data-ttu-id="bdc12-134">Er wordt een boekstuknummer voor de productontvangstbon verbruikt, zelfs als er tijdens de productontvangst geen financieel boekstuk is gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="bdc12-134">A product receipt voucher number is consumed even if no financial voucher is generated during product receipt.</span></span>

<span data-ttu-id="bdc12-135">Als de optie **Toerekening van aansprakelijkheid bij productontvangstbon** is ingesteld op *Nee* voor de artikelmodelgroep, worden er geen boekingen naar het grootboek uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="bdc12-135">If the **Accrue liability on product receipt** option is set to *No* for the item model group, no postings to the general ledger will occur.</span></span> <span data-ttu-id="bdc12-136">Er wordt echter een fysieke gebeurtenis voor de boekhouding in een subadministratie geregistreerd en voor die gebeurtenis is een boekstuknummer vereist.</span><span class="sxs-lookup"><span data-stu-id="bdc12-136">However, a physical event will be recorded for the purpose of accounting in a subledger, and that event requires a voucher number.</span></span> <span data-ttu-id="bdc12-137">Dit boekstuknummer is het boekstuknummer waarnaar in de voorraadtransacties wordt verwezen.</span><span class="sxs-lookup"><span data-stu-id="bdc12-137">This voucher number is the voucher number that is referenced in the inventory transactions.</span></span>

<span data-ttu-id="bdc12-138">Het is raadzaam om de optie **Toerekening van aansprakelijkheid bij productontvangstbon** in te stellen op *Ja*, zoals wordt beschreven in het volgende blogbericht: [Diverse toeslagen boeken op het moment van ontvangst van het product](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span><span class="sxs-lookup"><span data-stu-id="bdc12-138">We recommend that you set the **Accrue liability on product receipt** option to *Yes*, as described in the following blog post: [Post Misc. charges at time of product receipt](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span></span>

## <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a><span data-ttu-id="bdc12-139">De instelling Boeken op toeslagrekening in grootboek is niet ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="bdc12-139">The Post to charge account in ledger setting isn't turned on.</span></span>

### <a name="issue-description"></a><span data-ttu-id="bdc12-140">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="bdc12-140">Issue description</span></span>

<span data-ttu-id="bdc12-141">Dit probleem doet zich voor wanneer een inkooporder wordt gefactureerd, als de optie **Boeken op toeslagrekening in grootboek** is ingesteld *Ja* op het tabblad **Factuur** van de pagina **Parameters van module Leveranciers**.</span><span class="sxs-lookup"><span data-stu-id="bdc12-141">This issue occurs when a purchase order is invoiced, if the **Post to charge account in ledger** option is set to *Yes* on the **Invoice** tab of the **Accounts payable parameters** page.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="bdc12-142">Het probleem reproduceren</span><span class="sxs-lookup"><span data-stu-id="bdc12-142">Reproduce the issue</span></span>

<span data-ttu-id="bdc12-143">In de volgende procedure wordt één manier weergegeven om het probleem te reproduceren.</span><span class="sxs-lookup"><span data-stu-id="bdc12-143">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="bdc12-144">Ga naar **Leveranciers \> Instellen \> Parameters van Leveranciers**.</span><span class="sxs-lookup"><span data-stu-id="bdc12-144">Go to **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
1. <span data-ttu-id="bdc12-145">Stel op het tabblad **Factuur** de optie **Boeken op toeslagrekening in grootboek** in op *Ja*.</span><span class="sxs-lookup"><span data-stu-id="bdc12-145">On the **Invoice** tab, set the **Post to charge account in ledger** option to *Yes*.</span></span>
1. <span data-ttu-id="bdc12-146">Ga naar **Voorraadbeheer \> Instellen \> Boeken \> Boeken**.</span><span class="sxs-lookup"><span data-stu-id="bdc12-146">Go to **Inventory management \> Setup \> Posting \> Posting**.</span></span>
1. <span data-ttu-id="bdc12-147">Controleer op het tabblad **Inkooporder** of u alle regels in de inkoopuitgave voor het product hebt verwijderd.</span><span class="sxs-lookup"><span data-stu-id="bdc12-147">On the **Purchase order** tab, make sure that you've deleted all the lines in the purchase expenditure for the product.</span></span>
1. <span data-ttu-id="bdc12-148">Ga naar **Leveranciers \> Inkooporders \> Alle inkooporders**.</span><span class="sxs-lookup"><span data-stu-id="bdc12-148">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="bdc12-149">Inkooporder maken.</span><span class="sxs-lookup"><span data-stu-id="bdc12-149">Create a purchase order.</span></span> <span data-ttu-id="bdc12-150">Selecteer in het veld **Leveranciersrekening** de optie *1001 Acme Office Supplies*.</span><span class="sxs-lookup"><span data-stu-id="bdc12-150">In the **Vendor account** field, select *1001 Acme Office Supplies*.</span></span>
1. <span data-ttu-id="bdc12-151">Voeg een inkooporderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="bdc12-151">Add a purchase order line that has the following settings:</span></span>

    - <span data-ttu-id="bdc12-152">**Artikelnummer:** *D0011 Laser Projector*</span><span class="sxs-lookup"><span data-stu-id="bdc12-152">**Item number:** *D0011 Laser Projector*</span></span>
    - <span data-ttu-id="bdc12-153">**Locatie:** *1*</span><span class="sxs-lookup"><span data-stu-id="bdc12-153">**Site:** *1*</span></span>
    - <span data-ttu-id="bdc12-154">**Magazijn:** *11*</span><span class="sxs-lookup"><span data-stu-id="bdc12-154">**Warehouse:** *11*</span></span>
    - <span data-ttu-id="bdc12-155">**Hoeveelheid:** *4*</span><span class="sxs-lookup"><span data-stu-id="bdc12-155">**Quantity:** *4*</span></span>

1. <span data-ttu-id="bdc12-156">Selecteer in het actievenster op het tabblad **Inkoop** in de groep **Actie** de optie **Bevestigen**.</span><span class="sxs-lookup"><span data-stu-id="bdc12-156">On the Action Pane, on the **Purchase** tab, in the **Action** group, select **Confirm**.</span></span>
1. <span data-ttu-id="bdc12-157">Selecteer in het Actievenster op het tabblad **Ontvangen** in de groep **Genereren** de optie **Productontvangstbon**.</span><span class="sxs-lookup"><span data-stu-id="bdc12-157">On the Action Pane, on the **Receive** tab, in the **Generate** group, select **Product receipt**.</span></span>
1. <span data-ttu-id="bdc12-158">Voer in het dialoogvenster **Productontvangstbon boeken** in het veld **Productontvangstbon** een willekeurig getal in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="bdc12-158">In the **Posting product receipt** dialog box, in the **Product receipt** field, enter an arbitrary number, and then select **OK**.</span></span>
1. <span data-ttu-id="bdc12-159">Selecteer in het actievenster op het tabblad **Factuur** in de groep **Genereren** de optie **Factuur**.</span><span class="sxs-lookup"><span data-stu-id="bdc12-159">On the Action Pane, on the **Invoice** tab, in the **Generate** group, select **Invoice**.</span></span>
1. <span data-ttu-id="bdc12-160">Voer in het veld **Getal** een willekeurig getal in als het factuurnummer.</span><span class="sxs-lookup"><span data-stu-id="bdc12-160">In the **Number** field, enter an arbitrary number as the invoice number.</span></span>
1. <span data-ttu-id="bdc12-161">Werk de vereffeningsstatus bij en boek.</span><span class="sxs-lookup"><span data-stu-id="bdc12-161">Update the match status, and post.</span></span>
1. <span data-ttu-id="bdc12-162">U ontvangt nu de volgende fout wanneer u een factuur genereert vanuit een inkooporder: 'Rekeningnummer voor inkoopuitgave van het transactietype bestaat niet'.</span><span class="sxs-lookup"><span data-stu-id="bdc12-162">Notice that you now receive the following error when you generate an invoice from a purchase order: "Account number for transaction type Purchase expenditure for product does not exist."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="bdc12-163">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="bdc12-163">Issue resolution</span></span>

<span data-ttu-id="bdc12-164">Dit is afhankelijk van de parameterinstellingen voor facturen en factuurgroepen.</span><span class="sxs-lookup"><span data-stu-id="bdc12-164">This depends on the parameter settings for invoices and invoice groups.</span></span> <span data-ttu-id="bdc12-165">Zie het volgende blogbericht voor meer informatie: [Boekhouding voor inkooptoeslag en voorraadwijziging](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).</span><span class="sxs-lookup"><span data-stu-id="bdc12-165">For more information, see the following blog post: [Accounting for Purchase charge and Stock variation](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).</span></span>
