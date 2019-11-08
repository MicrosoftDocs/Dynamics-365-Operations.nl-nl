---
title: Factuurvereffening en intercompany-inkooporders
description: De aankopende rechtspersoon die bij een intercompany-transactie betrokken is, kan worden ingesteld om factuurvereffening voor leveranciers te gebruiken. In dit geval moet aan de boekingsvereisten worden voldaan voor zowel intercompany-handel en factuurvereffening voor leveranciers voordat IC-leveranciersfacturen kunnen worden geboekt.
author: abruer
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchLineMatchingPolicy
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3101
ms.assetid: 9c7c2e44-45f8-4325-b6de-a09fe790f9cf
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aaa4a08f65e4a3452782cf2b928464dff27ed59b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189655"
---
# <a name="invoice-matching-and-intercompany-purchase-orders"></a><span data-ttu-id="af1a9-104">Factuurvereffening en intercompany-inkooporders</span><span class="sxs-lookup"><span data-stu-id="af1a9-104">Invoice matching and intercompany purchase orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="af1a9-105">De aankopende rechtspersoon die bij een intercompany-transactie betrokken is, kan worden ingesteld om factuurvereffening voor leveranciers te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="af1a9-105">The purchasing legal entity that is involved in an intercompany trade transaction might be set up to use accounts payable invoice matching.</span></span> <span data-ttu-id="af1a9-106">Als het veld **Factuur met verschillen boeken** in het formulier **Parameters van module Leveranciers** is ingesteld op **Goedkeuring vereisen**, wordt factuurvereffeningsvalidatie uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="af1a9-106">When the **Post invoice with discrepancies** field in the **Accounts payable parameters** form is set to **Require approval**, invoice matching validation will be performed.</span></span> <span data-ttu-id="af1a9-107">In dit geval moet aan de boekingsvereisten worden voldaan voor zowel intercompany-handel en factuurvereffening voor leveranciers voordat IC-leveranciersfacturen kunnen worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="af1a9-107">In this case, the posting requirements for both intercompany trade and accounts payable invoice matching must be met before intercompany vendor invoices can be posted.</span></span>

<span data-ttu-id="af1a9-108">Het voorbeeld in dit onderwerp gebruikt de volgende instellingen IC-handel:</span><span class="sxs-lookup"><span data-stu-id="af1a9-108">The examples in this topic use the following setup for intercompany trade:</span></span>
-   <span data-ttu-id="af1a9-109">Fabrikam Inkoop is de aankopende rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="af1a9-109">Fabrikam Purchase is the purchasing legal entity.</span></span>
-   <span data-ttu-id="af1a9-110">Fabrikam Verkoop is de verkopende rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="af1a9-110">Fabrikam Sales is the selling legal entity.</span></span>
-   <span data-ttu-id="af1a9-111">Fabrikam Sales bevat klant 4020.</span><span class="sxs-lookup"><span data-stu-id="af1a9-111">Customer 4020 exists in Fabrikam Sales.</span></span>
-   <span data-ttu-id="af1a9-112">Fabrikam Purchase bevat leverancier 3024.</span><span class="sxs-lookup"><span data-stu-id="af1a9-112">Vendor 3024 exists in Fabrikam Purchase.</span></span>
-   <span data-ttu-id="af1a9-113">Intercompany-informatie wordt opgegeven in Fabrikam Purchase voor leverancier 3024.</span><span class="sxs-lookup"><span data-stu-id="af1a9-113">In Fabrikam Purchase, intercompany information is specified for vendor 3024.</span></span> <span data-ttu-id="af1a9-114">Fabrikam Sales wordt opgegeven als het klantbedrijf en klant 4020 wordt opgegeven als de klantrekening die met de rechtspersoon Fabrikam Purchase overeenkomt.</span><span class="sxs-lookup"><span data-stu-id="af1a9-114">Fabrikam Sales is specified as the customer company, and customer 4020 is specified as the customer account that corresponds to the Fabrikam Purchase legal entity.</span></span>
-   <span data-ttu-id="af1a9-115">Intercompany-informatie wordt opgegeven in Fabrikam Sales voor klant 4020.</span><span class="sxs-lookup"><span data-stu-id="af1a9-115">In Fabrikam Sales, intercompany information is specified for customer 4020.</span></span> <span data-ttu-id="af1a9-116">Fabrikam Purchase wordt opgegeven als het leveranciersbedrijf en leverancier 3024 wordt opgegeven als de leveranciersrekening die met de rechtspersoon Fabrikam Sales overeenkomt.</span><span class="sxs-lookup"><span data-stu-id="af1a9-116">Fabrikam Purchase is specified as the vendor company, and vendor 3024 is specified as the vendor account that corresponds to the Fabrikam Sales legal entity.</span></span>

<span data-ttu-id="af1a9-117">Bij deze voorbeelden worden de volgende instellingen voor factuurmatching in leveranciers gebruikt voor Fabrikam Inkoop:</span><span class="sxs-lookup"><span data-stu-id="af1a9-117">The examples use the following setup for accounts payable invoice matching for Fabrikam Purchase:</span></span>
-   <span data-ttu-id="af1a9-118">Op de pagina Parameters van module Leveranciers is de optie Factuurvereffeningsvalidatie inschakelen geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="af1a9-118">On the Accounts payable parameters page, the Enable invoice matching validation option is selected.</span></span>
-   <span data-ttu-id="af1a9-119">Op de pagina Parameters van module Leveranciers is het veld Factuur met verschillen boeken ingesteld op Goedkeuring vereist.</span><span class="sxs-lookup"><span data-stu-id="af1a9-119">On the Accounts payable parameters page, the Post invoice with discrepancies field is set to Require approval.</span></span>
-   <span data-ttu-id="af1a9-120">Het prijstolerantiepercentage voor de rechtspersoon bedraagt 2 procent.</span><span class="sxs-lookup"><span data-stu-id="af1a9-120">The price tolerance percentage for the legal entity is 2 percent.</span></span>

## <a name="example-price-matching-and-intercompany-trade"></a><span data-ttu-id="af1a9-121">Voorbeeld: Prijsmatching en intercompany-handel</span><span class="sxs-lookup"><span data-stu-id="af1a9-121">Example: Price matching and intercompany trade</span></span>
<span data-ttu-id="af1a9-122">De nettobedragen voor de IC-leveranciersfactuur en de IC-klantfactuur moeten gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="af1a9-122">The net amounts for the intercompany vendor invoice and the intercompany customer invoice must be equal.</span></span> <span data-ttu-id="af1a9-123">Deze vereiste vervangt eventuele van toepassing zijnde goedkeuringen voor factuurmatching of prijstolerantiepercentages.</span><span class="sxs-lookup"><span data-stu-id="af1a9-123">This requirement overrides any invoice matching approvals or price tolerance percentages that apply.</span></span> <span data-ttu-id="af1a9-124">U volgt bijvoorbeeld deze stappen.</span><span class="sxs-lookup"><span data-stu-id="af1a9-124">For example, you follow these steps.</span></span>
1.  <span data-ttu-id="af1a9-125">Maak verkooporder SO888 voor klant 4020 in Fabrikam Purchase.</span><span class="sxs-lookup"><span data-stu-id="af1a9-125">In Fabrikam Purchase, create sales order SO888 for customer 4020.</span></span> <span data-ttu-id="af1a9-126">De intercompany-inkooporder ICPO222 wordt automatisch gemaakt voor leverancier 3024 in Fabrikam Inkoop, en verkooporder ICSO888 wordt automatisch gemaakt in Fabrikam Verkoop.</span><span class="sxs-lookup"><span data-stu-id="af1a9-126">Intercompany purchase order ICPO222 is automatically created for vendor 3024 in Fabrikam Purchase, and sales order ICSO888 is automatically created in Fabrikam Sales.</span></span>
2.  <span data-ttu-id="af1a9-127">In Fabrikam Verkoop, registreert u dat de artikelen zijn ontvangen en boekt u een pakbon.</span><span class="sxs-lookup"><span data-stu-id="af1a9-127">In Fabrikam Sales, register that the items have been received, and post a packing slip.</span></span> <span data-ttu-id="af1a9-128">De status van ICSO888 verandert in Geleverd.</span><span class="sxs-lookup"><span data-stu-id="af1a9-128">The status of ICSO888 changes to Delivered.</span></span> <span data-ttu-id="af1a9-129">De status van ICPO222 verandert in Ontvangen.</span><span class="sxs-lookup"><span data-stu-id="af1a9-129">The status of ICPO222 changes to Received.</span></span>
3.  <span data-ttu-id="af1a9-130">Voer in Fabrikam Verkoop een factuurupdate uit voor ICSO888.</span><span class="sxs-lookup"><span data-stu-id="af1a9-130">In Fabrikam Sales, perform an invoice update for ICSO888.</span></span> <span data-ttu-id="af1a9-131">De eenheidsprijs is 0,45 en er worden 100 artikelen bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="af1a9-131">The unit price is 0.45, and 100 items are updated.</span></span>
4.  <span data-ttu-id="af1a9-132">Maak in Fabrikam Inkoop een factuur voor ICPO222.</span><span class="sxs-lookup"><span data-stu-id="af1a9-132">In Fabrikam Purchase, create an invoice for ICPO222.</span></span> <span data-ttu-id="af1a9-133">U wijzigt de nettoprijs onopzettelijk van 45,00 naar 54,00.</span><span class="sxs-lookup"><span data-stu-id="af1a9-133">You accidentally change the net price from 45.00 to 54.00.</span></span> <span data-ttu-id="af1a9-134">Er wordt een pictogram weergegeven om aan te geven dat de prijs hoger is dan de toegestane prijstolerantie van twee procent.</span><span class="sxs-lookup"><span data-stu-id="af1a9-134">An icon is displayed to indicate that the price exceeds the allowable price tolerance of 2 percent.</span></span>
5.  <span data-ttu-id="af1a9-135">Selecteer op de pagina Factuurvereffeningsgegevens de optie om de boeking met vereffeningsverschillen goed te keuren.</span><span class="sxs-lookup"><span data-stu-id="af1a9-135">On the Invoice matching details page, select the option to approve posting with matching discrepancies.</span></span> <span data-ttu-id="af1a9-136">Klik op OK op de pagina Leveranciersfactuur.</span><span class="sxs-lookup"><span data-stu-id="af1a9-136">On the Vendor invoice page, click OK.</span></span> <span data-ttu-id="af1a9-137">Indien de leveranciersfactuur geen IC-leveranciersfactuur was, zou het boeken lukken.</span><span class="sxs-lookup"><span data-stu-id="af1a9-137">If the vendor invoice was not an intercompany vendor invoice, posting would be successful.</span></span> <span data-ttu-id="af1a9-138">Het boeken is echter mislukt omdat u met een IC-leveranciersfactuur werkt.</span><span class="sxs-lookup"><span data-stu-id="af1a9-138">However, because you are working with an intercompany vendor invoice, posting is unsuccessful.</span></span> <span data-ttu-id="af1a9-139">Voor IC-handel moeten de factuurtotalen voor de IC-verkooporder gelijk zijn aan de factuurtotalen voor de bijbehorende IC-inkooporder.</span><span class="sxs-lookup"><span data-stu-id="af1a9-139">For intercompany trade, the invoice totals on the intercompany sales order must equal the invoice totals on the corresponding intercompany purchase order.</span></span> <span data-ttu-id="af1a9-140">Om dit probleem op te lossen, moet u de netto prijs op de factuur corrigeren door de netto prijs te wijzigen in de standaardhoeveelheid 45,00.</span><span class="sxs-lookup"><span data-stu-id="af1a9-140">To resolve this issue, you must correct the net price on the invoice by changing the net price back to the default amount, 45.00.</span></span>

## <a name="example-quantity-matching-with-intercompany-trade"></a><span data-ttu-id="af1a9-141">Voorbeeld: Hoeveelheidvereffening bij intercompany-handel</span><span class="sxs-lookup"><span data-stu-id="af1a9-141">Example: Quantity matching with intercompany trade</span></span>
<span data-ttu-id="af1a9-142">De aantallen op de IC-inkooporder en IC-verkooporder moeten gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="af1a9-142">The quantities on the intercompany purchase order and the intercompany sales order must be equal.</span></span> <span data-ttu-id="af1a9-143">Deze vereiste vervangt eventuele van toepassing zijnde goedkeuringen voor factuurmatching.</span><span class="sxs-lookup"><span data-stu-id="af1a9-143">This requirement overrides any invoice matching approvals that apply.</span></span> <span data-ttu-id="af1a9-144">Bij dit voorbeeld worden de volgende aanvullende instellingen voor intercompany-handel gebruikt:</span><span class="sxs-lookup"><span data-stu-id="af1a9-144">This example uses the following additional setup for intercompany trade:</span></span>
-   <span data-ttu-id="af1a9-145">In Fabrikam Inkoop wordt het inkooporder actiebeleid voor leverancier 3024 ingesteld om de oorspronkelijke klantfactuur en de IC-leveranciersfactuur automatisch te boeken.</span><span class="sxs-lookup"><span data-stu-id="af1a9-145">In Fabrikam Purchase, the purchase order action policy for vendor 3024 is set up to automatically post both the original customer invoice and the intercompany vendor invoice.</span></span>

<span data-ttu-id="af1a9-146">Bij dit voorbeeld worden de volgende aanvullende instellingen voor factuurmatching in leveranciers gebruikt voor Fabrikam Inkoop:</span><span class="sxs-lookup"><span data-stu-id="af1a9-146">This example uses the following additional setup for accounts payable invoice matching for Fabrikam Purchase:</span></span>
-   <span data-ttu-id="af1a9-147">Op de pagina Artikelmodelgroepen voor de modelgroep die wordt gebruikt door artikel B-R14, is de optie Ontvangstvereisten geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="af1a9-147">On the Item model groups page for the model group that is used by item B-R14, the Receiving requirements option is selected.</span></span>
-   <span data-ttu-id="af1a9-148">De voorhanden voorraad voor artikel B-R14 is 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="af1a9-148">The on-hand quantity for item B-R14 is 0 (zero).</span></span>

<span data-ttu-id="af1a9-149">U volgt bijvoorbeeld deze stappen.</span><span class="sxs-lookup"><span data-stu-id="af1a9-149">For example, you follow these steps.</span></span>
1.  <span data-ttu-id="af1a9-150">Maak verkooporder SO999 voor klant 4020 in Fabrikam Purchase.</span><span class="sxs-lookup"><span data-stu-id="af1a9-150">In Fabrikam Purchase, create sales order SO999 for customer 4020.</span></span> <span data-ttu-id="af1a9-151">De order bevat één regelartikel: 100 batterijen (artikel B-R14) met een eenheidsprijs van 1,00 per stuk.</span><span class="sxs-lookup"><span data-stu-id="af1a9-151">The order contains one line item: 100 batteries (item B-R14) at a unit price of 1.00 each.</span></span> <span data-ttu-id="af1a9-152">De intercompany-inkooporder ICPO333 wordt automatisch gemaakt voor leverancier 3024 in Fabrikam Inkoop, en verkooporder ICSO999 wordt automatisch gemaakt in Fabrikam Verkoop.</span><span class="sxs-lookup"><span data-stu-id="af1a9-152">Intercompany purchase order ICPO333 is automatically created for vendor 3024 in Fabrikam Purchase, and sales order ICSO999 is automatically created in Fabrikam Sales.</span></span>
2.  <span data-ttu-id="af1a9-153">Voer in Fabrikam Verkoop een factuurupdate uit voor ICSO999.</span><span class="sxs-lookup"><span data-stu-id="af1a9-153">In Fabrikam Sales, perform an invoice update for ICSO999.</span></span> <span data-ttu-id="af1a9-154">Boeken is mislukt, omdat het artikel niet op voorraad is en nog niet is ontvangen.</span><span class="sxs-lookup"><span data-stu-id="af1a9-154">Posting is unsuccessful, because the item is out of stock and has not yet been received.</span></span> <span data-ttu-id="af1a9-155">Daarom kan de financiële informatie kan niet worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="af1a9-155">Therefore, the financial information cannot be updated.</span></span>
3.  <span data-ttu-id="af1a9-156">In Fabrikam Verkoop legt u vast dat de artikelen zijn ontvangen en boekt i een pakbon voor ICSO999.</span><span class="sxs-lookup"><span data-stu-id="af1a9-156">In Fabrikam Sales, register that the items have been received, and post a packing slip for ICSO999.</span></span> <span data-ttu-id="af1a9-157">De productontvangst voor ICPO333 wordt automatisch geboekt in Fabrikam Inkoop.</span><span class="sxs-lookup"><span data-stu-id="af1a9-157">A product receipt for ICPO333 is automatically posted in Fabrikam Purchase.</span></span> <span data-ttu-id="af1a9-158">In Fabrikam Inkoop, verandert het ontvangen aantal voor artikel B-R14 naar 100.</span><span class="sxs-lookup"><span data-stu-id="af1a9-158">In Fabrikam Purchase, the received quantity for item B-R14 changes to 100.</span></span>
4.  <span data-ttu-id="af1a9-159">Voer in Fabrikam Verkoop een factuurupdate uit voor ICSO999.</span><span class="sxs-lookup"><span data-stu-id="af1a9-159">In Fabrikam Sales, perform an invoice update for ICSO999.</span></span> <span data-ttu-id="af1a9-160">Boeking is voltooid in beide rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="af1a9-160">Posting is successful in both legal entities.</span></span> <span data-ttu-id="af1a9-161">In Fabrikam Inkoop verandert het gekochte aantal voor artikel B-R14 naar 100.</span><span class="sxs-lookup"><span data-stu-id="af1a9-161">In Fabrikam Purchase, the quantity that is purchased for item B-R14 changes to 100.</span></span>




