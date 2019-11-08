---
title: Boekhoudingsverdelingen en journaalposten in de subadministratie voor leveranciersfacturen
description: Boekhoudingsverdelingen worden gebruikt om te bepalen hoe een bedrag zal worden verwerkt, zoals hoe de onkosten, BTW of heffingen zullen worden verwerkt op een leveranciersfactuur. Elk bedrag dat moet worden verwerkt wanneer de leveranciersfactuur in het boekhoudingsjournaal wordt vastgelegd, heeft een of meerdere boekhoudingsverdelingen.
author: abruer
manager: AnnBe
ms.date: 08/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f8e38e6a571bb7f08b32548bcb4af823807a4340
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177241"
---
# <a name="accounting-distributions-and-subledger-journal-entries-for-vendor-invoices"></a><span data-ttu-id="e348e-104">Boekhoudingsverdelingen en journaalposten in de subadministratie voor leveranciersfacturen</span><span class="sxs-lookup"><span data-stu-id="e348e-104">Accounting distributions and subledger journal entries for vendor invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e348e-105">Boekhoudingsverdelingen worden gebruikt om te bepalen hoe een bedrag zal worden verwerkt, zoals hoe de onkosten, BTW of heffingen zullen worden verwerkt op een leveranciersfactuur.</span><span class="sxs-lookup"><span data-stu-id="e348e-105">Accounting distributions are used to define how an amount will be accounted for, such as how the expense, tax, or charges will be accounted for on a vendor invoice.</span></span> <span data-ttu-id="e348e-106">Elk bedrag dat moet worden verwerkt wanneer de leveranciersfactuur in het boekhoudingsjournaal wordt vastgelegd, heeft een of meerdere boekhoudingsverdelingen.</span><span class="sxs-lookup"><span data-stu-id="e348e-106">Every amount that must be accounted for when the vendor invoice is journalized will have one or more accounting distributions.</span></span> 

<a name="accounting-distributions"></a><span data-ttu-id="e348e-107">Boekhoudingsverdelingen</span><span class="sxs-lookup"><span data-stu-id="e348e-107">Accounting distributions</span></span> 
-------------------------

<span data-ttu-id="e348e-108">U kunt de volgende knoppen op de pagina Leveranciersfactuur gebruiken voor het weergeven en mogelijk wijzigen van de boekhoudingsverdelingen voor elk bedrag op de leveranciersfactuur.</span><span class="sxs-lookup"><span data-stu-id="e348e-108">You can use the following buttons in the Vendor invoice page to view, and possibly modify, the accounting distributions for each amount on the vendor invoice.</span></span>
-   <span data-ttu-id="e348e-109">**Bedragen verdelen** – De boekhoudingsverdelingen weergeven en wijzigen voor een afzonderlijke regel en alle onderliggende regels, zoals belastingen of heffingen.</span><span class="sxs-lookup"><span data-stu-id="e348e-109">**Distribute amounts** – View and modify the accounting distributions for an individual line and any child lines, such as taxes or charges.</span></span> <span data-ttu-id="e348e-110">U kunt de boekhoudingsverdeling voor de onderliggende regel rechtstreeks weergeven en wijzigen op de pagina Btw-transacties of de pagina Transacties met toeslagen transacties.</span><span class="sxs-lookup"><span data-stu-id="e348e-110">You can also view and modify the accounting distributions for the child line directly from the Sales tax transactions page or the Charges transactions page.</span></span>
    -   <span data-ttu-id="e348e-111">Bedragen in de koptekst van leveranciersfacturen wijzigen, zoals heffingen of valuta-afrondingsbedragen.</span><span class="sxs-lookup"><span data-stu-id="e348e-111">Modify vendor invoice header amounts, such as charges or currency rounding amounts.</span></span>
    -   <span data-ttu-id="e348e-112">Bedragen op factuurregels van leveranciersfacturen wijzigen.</span><span class="sxs-lookup"><span data-stu-id="e348e-112">Modify vendor invoice line amounts.</span></span>
-   <span data-ttu-id="e348e-113">**Verdelingen weergeven** – Voor alle regels op het document de boekhoudingsverdelingen weergeven.</span><span class="sxs-lookup"><span data-stu-id="e348e-113">**View distributions** – View the accounting distributions for all lines on the document.</span></span> <span data-ttu-id="e348e-114">Vanuit deze weergave kunt u de boekhoudingsverdelingen niet wijzigen.</span><span class="sxs-lookup"><span data-stu-id="e348e-114">You cannot modify the accounting distributions from this view.</span></span>
    -   <span data-ttu-id="e348e-115">Bedragen in de koptekst en op de regel weergeven.</span><span class="sxs-lookup"><span data-stu-id="e348e-115">View header and line amounts.</span></span>

<span data-ttu-id="e348e-116">Als de leveranciersfactuur naar een inkooporder verwijst, kunt u de boekhoudingsverdelingen splitsen en wijzigen voor regels met een item dat niet is opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="e348e-116">If the vendor invoice references a purchase order, you can split and modify the accounting distributions for lines that contain an item that is not stocked.</span></span> <span data-ttu-id="e348e-117">Indien de leveranciersfactuurregel niet verwijst naar een inkooporderregel, kunt u ook een boekhoudingsverdeling verwijderen.</span><span class="sxs-lookup"><span data-stu-id="e348e-117">If the vendor invoice line does not reference a purchase order line, you can also delete an accounting distribution.</span></span> <span data-ttu-id="e348e-118">U kunt geen regels splitsen of verwijderen voor heffingen, belastingen en regelkortingen.</span><span class="sxs-lookup"><span data-stu-id="e348e-118">You cannot split or delete lines for charges, taxes, and line discounts.</span></span> <span data-ttu-id="e348e-119">U kunt de grootboekrekening wijzigen, maar niet bedragen of percentages.</span><span class="sxs-lookup"><span data-stu-id="e348e-119">You can modify the ledger account, but you cannot change the amounts or percentages.</span></span>
> [!NOTE]                                                                                                                                 
> <span data-ttu-id="e348e-120">Indien de bovenliggende regel een artikel bevat dat niet in voorraad wordt opgeslagen en de boekhoudingsverdelingen worden gesplitst, wordt de onderliggende regel automatisch gesplitst om overeen te komen met de financiële dimensies van de bovenliggende regel.</span><span class="sxs-lookup"><span data-stu-id="e348e-120">If the parent line contains an item that is not stocked and the accounting distributions are split, the child line will be split automatically to match the financial dimensions of the parent line.</span></span> <span data-ttu-id="e348e-121">De boekhoudingsverdelingen voor de onderliggende regel kunnen niet aanvullend worden gesplitst of verwijderd, maar afhankelijk van de instelling van de onderliggende regel kunt u mogelijk de grootboekrekening voor de boekhoudingsverdelingen van de onderliggende regel wijzigen.</span><span class="sxs-lookup"><span data-stu-id="e348e-121">The accounting distributions for the child line cannot be additionally split or deleted, but depending on the setup of the child line, you might be able to modify the ledger account for the accounting distributions of the child line.</span></span>

## <a name="distributing-amounts"></a><span data-ttu-id="e348e-122">Bedragen verdelen</span><span class="sxs-lookup"><span data-stu-id="e348e-122">Distributing amounts</span></span>
<span data-ttu-id="e348e-123">Wanneer u een leveranciersfactuur invoert, wordt elk bedrag als volgt verdeeld.</span><span class="sxs-lookup"><span data-stu-id="e348e-123">When you enter a vendor invoice, each amount will be distributed as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e348e-124">Soort leveranciersfactuurregel</span><span class="sxs-lookup"><span data-stu-id="e348e-124">Type of vendor invoice line</span></span></th>
<th><span data-ttu-id="e348e-125">Volgorde van prioriteit die bepaalt waar de hoofdrekening uit wordt weergegeven</span><span class="sxs-lookup"><span data-stu-id="e348e-125">Order of priority that determines where the main account is displayed from</span></span></th>
<th><span data-ttu-id="e348e-126">Volgorde van prioriteit die bepaalt welke standaard financiële dimensie wordt weergegeven</span><span class="sxs-lookup"><span data-stu-id="e348e-126">Order of priority that determines which default financial dimension is displayed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e348e-127">Product in voorraad</span><span class="sxs-lookup"><span data-stu-id="e348e-127">Stocked product</span></span></td>
<td><ol>
<li><span data-ttu-id="e348e-128">De boekhoudingsverdeling voor de inkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-128">The accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="e348e-129">Het veld Hoofdrekening wanneer Inkoopuitgave voor product is geselecteerd op de pagina Boeking.</span><span class="sxs-lookup"><span data-stu-id="e348e-129">The Main account field when Purchase expenditure for product is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="e348e-130">Als de factuurregel verwijst naar een inkooporderregel, gebruikt u de boekhoudingsverdeling voor de inkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-130">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="e348e-131">De standaard financiële dimensiewaarden gebruiken op de leveranciersfactuur.</span><span class="sxs-lookup"><span data-stu-id="e348e-131">Use the default financial dimension values on the vendor invoice.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e348e-132">Een aanschaffingscategorie of een product dat niet op voorraad is</span><span class="sxs-lookup"><span data-stu-id="e348e-132">A procurement category or a product that is not stocked</span></span></td>
<td><ol>
<li><span data-ttu-id="e348e-133">De boekhoudingsverdeling voor de inkooporderregel indien de leveranciersfactuurregel verwijst naar een inkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-133">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="e348e-134">Het veld Hoofdrekening wanneer Inkoopuitgave voor onkosten is geselecteerd op de pagina Boeking.</span><span class="sxs-lookup"><span data-stu-id="e348e-134">The Main account field when Purchase expenditure for expense is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="e348e-135">Als de factuurregel verwijst naar een inkooporderregel, gebruikt u de boekhoudingsverdeling voor de inkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-135">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="e348e-136">Indien de hoofdrekening een toewijzingsrekening is, gebruikt u de standaardwaarde van de definitie van de toewijzingsrekening.</span><span class="sxs-lookup"><span data-stu-id="e348e-136">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="e348e-137">De standaard financiële dimensiewaarden gebruiken op de leveranciersfactuur.</span><span class="sxs-lookup"><span data-stu-id="e348e-137">Use the default financial dimension values on the vendor invoice.</span></span></li>
<li><span data-ttu-id="e348e-138">De financiële dimensiewaarden gebruiken van de leveranciersfactuurregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-138">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="e348e-139">De standaard financiële dimensiewaarden gebruiken van de hoofdrekening op de pagina Rekeningschema.</span><span class="sxs-lookup"><span data-stu-id="e348e-139">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e348e-140">Vaste activa</span><span class="sxs-lookup"><span data-stu-id="e348e-140">Fixed asset</span></span></td>
<td><ol>
<li><span data-ttu-id="e348e-141">De boekhoudingsverdeling voor de inkooporderregel indien de leveranciersfactuurregel verwijst naar een inkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-141">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="e348e-142">Als Verwerving is geselecteerd in het veld Transactietype in het formulier Leveranciersfactuur, wordt het veld Hoofdrekening geselecteerd op de pagina Boekingsprofielen voor vaste activa.</span><span class="sxs-lookup"><span data-stu-id="e348e-142">If Acquisition is selected in the Transaction type field in the Vendor invoice form, the Main account field when Acquisition is selected in the Fixed asset posting profiles page.</span></span></li>
<li><span data-ttu-id="e348e-143">Als Verwervingscorrectie is geselecteerd in het veld Transactietype, wordt het veld Verwervingscorrectie geselecteerd op de pagina Boekingsprofielen voor vaste activa.</span><span class="sxs-lookup"><span data-stu-id="e348e-143">If Acquisition adjustment is selected in the Transaction type field, the Main account field when Acquisition adjustment is selected in the Fixed asset posting profiles page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="e348e-144">Gebruik de boekhoudingsverdeling voor de inkooporderregel als de factuurregel verwijst naar een inkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-144">Use the account distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="e348e-145">De financiële dimensiewaarden gebruiken van de leveranciersfactuurregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-145">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="e348e-146">De standaard financiële dimensiewaarden gebruiken van de hoofdrekening op de pagina Rekeningschema.</span><span class="sxs-lookup"><span data-stu-id="e348e-146">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e348e-147">Project gedefinieerd op de leveranciersfactuurregel</span><span class="sxs-lookup"><span data-stu-id="e348e-147">Project defined on the vendor invoice line</span></span></td>
<td><ol>
<li><span data-ttu-id="e348e-148">De boekhoudingsverdeling voor de inkooporderregel als de factuurregel verwijst naar een inkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-148">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="e348e-149">Als Saldo is geselecteerd in het veld Kosten boeken - Artikel op de pagina Projectgroep, wordt het veld Hoofdrekening geselecteerd op de pagina Instellingen boeking in grootboek.</span><span class="sxs-lookup"><span data-stu-id="e348e-149">If Balance is selected in the Post costs - item field in the Project groups page, the Main account field when Cost is selected in the Ledger posting setup page.</span></span></li>
<li><span data-ttu-id="e348e-150">Als Verlies-en-winstrekening is geselecteerd in het veld Kosten boeken - Artikel op de pagina Projectgroep, wordt het veld Kosten - artikel geselecteerd op de pagina Instellingen boeking in grootboek.</span><span class="sxs-lookup"><span data-stu-id="e348e-150">If Profit and loss is selected in the Post costs - item field in the Project groups page, the Main account field when Cost - item is selected in the Ledger posting setup page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="e348e-151">Als de factuurregel verwijst naar een inkooporderregel, gebruikt u de boekhoudingsverdeling voor de inkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-151">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e348e-152">Regelkorting</span><span class="sxs-lookup"><span data-stu-id="e348e-152">Line discount</span></span></td>
<td><ol>
<li><span data-ttu-id="e348e-153">De boekhoudingsverdeling voor de inkooporderregel als de factuurregel verwijst naar een inkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-153">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="e348e-154">Het veld Hoofdrekening wanneer Korting is geselecteerd op de pagina Boeking.</span><span class="sxs-lookup"><span data-stu-id="e348e-154">The Main account field when Discount is selected in the Posting page.</span></span></li>
<li><span data-ttu-id="e348e-155">Als een hoofdrekening voor een korting niet is gedefinieerd in het boekingsprofiel, de boekhoudingsverdeling van de totaalprijs op de inkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-155">If a main account for a discount is not defined on the posting profile, the accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="e348e-156">Als de factuurregel verwijst naar een inkooporderregel, gebruikt u de boekhoudingsverdeling voor de inkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-156">If the invoice line references a purchase order line, use the accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="e348e-157">De financiële dimensies gebruiken voor de boekhoudingsverdelingen voor de totaalprijs van de leveranciersfactuurregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-157">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="e348e-158">De financiële dimensiewaarden voor de leveranciersfactuurregel gebruiken.</span><span class="sxs-lookup"><span data-stu-id="e348e-158">Use the financial dimension values for the vendor invoice line.</span></span></li>
<li><span data-ttu-id="e348e-159">De standaard financiële dimensiewaarden gebruiken van de hoofdrekening op de pagina Rekeningschema.</span><span class="sxs-lookup"><span data-stu-id="e348e-159">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e348e-160">Aankooptoeslag, ingevoerd op het tabblad Prijs en korting van de inkooporderregel</span><span class="sxs-lookup"><span data-stu-id="e348e-160">Purchase charge, which is entered on the Price and discount tab of the purchase order line</span></span></td>
<td><ol>
<li><span data-ttu-id="e348e-161">De boekhoudingsverdeling voor de inkooporderregel als de factuurregel verwijst naar een inkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-161">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="e348e-162">De boekhoudingsverdeling van de totaalprijs op de inkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-162">The accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="e348e-163">Als de factuurregel verwijst naar een inkooporderregel, gebruikt u de boekhoudingsverdeling voor de inkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-163">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="e348e-164">De financiële dimensies gebruiken voor de boekhoudingsverdelingen voor de totaalprijs van de leveranciersfactuurregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-164">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e348e-165">Regeltoeslag</span><span class="sxs-lookup"><span data-stu-id="e348e-165">Line charge</span></span></td>
<td><ol>
<li><span data-ttu-id="e348e-166">De boekhoudingsverdeling voor de inkooporderregel als de factuurregel verwijst naar een inkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-166">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="e348e-167">Als Grootboekrekening is geselecteerd in het veld Debettype in het formulier Toeslagcode, het veld Debetrekening op de pagina Toeslagcode.</span><span class="sxs-lookup"><span data-stu-id="e348e-167">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="e348e-168">Als Artikel is geselecteerd in het veld Debettype in het formulier Toeslagcode, de boekhoudingsverdeling voor de totaalprijs op de inkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-168">If Item is selected in the debit Type field in the Charges code form, the accounting distribution for the extended price on the purchase order line.</span></span></li>
<li><span data-ttu-id="e348e-169">Als Klant/leverancier is geselecteerd in het veld Debettype in het formulier Toeslagcode, het veld Creditrekening op de pagina Toeslagcode.</span><span class="sxs-lookup"><span data-stu-id="e348e-169">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="e348e-170">Als de factuurregel verwijst naar een inkooporderregel, gebruikt u de boekhoudingsverdeling voor de inkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-170">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="e348e-171">De financiële dimensies gebruiken voor de boekhoudingsverdelingen voor de totaalprijs van de leveranciersfactuurregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-171">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="e348e-172">De financiële dimensiewaarden gebruiken van de leveranciersfactuurregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-172">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="e348e-173">De standaard financiële dimensiewaarden gebruiken van de hoofdrekening op de pagina Rekeningschema.</span><span class="sxs-lookup"><span data-stu-id="e348e-173">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e348e-174">BTW, met de volgende status:</span><span class="sxs-lookup"><span data-stu-id="e348e-174">Tax, with the following condition:</span></span>
<ul>
<li><span data-ttu-id="e348e-175">De optie Amerikaanse belastingregels toepassen wordt geselecteerd op de pagina Grootboekparameters.</span><span class="sxs-lookup"><span data-stu-id="e348e-175">The Apply U.S. taxation rules option is selected in the General ledger parameters page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="e348e-176">De boekhoudingsverdeling voor de inkooporderregel als de factuurregel verwijst naar een inkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-176">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="e348e-177">De boekhoudingsverdelingen van de totaalprijs of de toeslag.</span><span class="sxs-lookup"><span data-stu-id="e348e-177">The accounting distribution of the extended price or charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="e348e-178">Als de factuurregel verwijst naar een inkooporderregel, gebruikt u de boekhoudingsverdeling voor de inkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-178">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="e348e-179">De financiële dimensies gebruiken voor de boekhoudingsverdelingen voor de totaalprijs van de leveranciersfactuurregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-179">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="e348e-180">De financiële dimensiewaarden gebruiken van de leveranciersfactuurregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-180">Use the financial dimension values from the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e348e-181">BTW, met de volgende status:</span><span class="sxs-lookup"><span data-stu-id="e348e-181">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="e348e-182">De optie Amerikaanse belastingregels wordt uitgeschakeld op de pagina Grootboekparameters.</span><span class="sxs-lookup"><span data-stu-id="e348e-182">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="e348e-183">Het veld Gebruiksbelasting voor de btw-groep wordt uitgeschakeld op de pagina Btw-groepen.</span><span class="sxs-lookup"><span data-stu-id="e348e-183">The Use tax field for the sales tax group is cleared in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="e348e-184">Als het btw-percentage terug te vorderen is, het veld Te ontvangen btw op de pagina Groepen boekingen in grootboek.</span><span class="sxs-lookup"><span data-stu-id="e348e-184">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="e348e-185">Als het btw-bedrag niet recupereerbaar is, de totaalprijs of de boekhoudingsverdeling voor de toeslag.</span><span class="sxs-lookup"><span data-stu-id="e348e-185">If the tax amount is not recoverable, the extended price or the accounting distribution for the charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="e348e-186">Als de factuurregel verwijst naar een inkooporderregel, gebruikt u de boekhoudingsverdeling voor de inkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-186">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="e348e-187">De financiële dimensies gebruiken voor de totaalprijs of de boekhoudingsverdelingen voor de kost van de leveranciersfactuurregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-187">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="e348e-188">De financiële dimensiewaarden gebruiken van de leveranciersfactuurregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-188">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="e348e-189">De standaard financiële dimensiewaarden gebruiken van de hoofdrekening op de pagina Rekeningschema.</span><span class="sxs-lookup"><span data-stu-id="e348e-189">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e348e-190">BTW, met de volgende status:</span><span class="sxs-lookup"><span data-stu-id="e348e-190">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="e348e-191">De optie Amerikaanse belastingregels wordt uitgeschakeld op de pagina Grootboekparameters.</span><span class="sxs-lookup"><span data-stu-id="e348e-191">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="e348e-192">Het veld Gebruiksbelasting voor de btw-groep wordt ingeschakeld op de pagina Btw-groepen.</span><span class="sxs-lookup"><span data-stu-id="e348e-192">The Use tax field for the sales tax group is selected in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="e348e-193">Als het btw-percentage terug te vorderen is, het veld Te ontvangen btw op de pagina Groepen boekingen in grootboek.</span><span class="sxs-lookup"><span data-stu-id="e348e-193">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="e348e-194">Als het btw-percentage niet terug te vorderen is, het veld Gebruiksbelastinguitgave op de pagina Groepen boekingen in grootboek.</span><span class="sxs-lookup"><span data-stu-id="e348e-194">If the tax amount is not recoverable, the Use tax expense field in the Ledger posting groups page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="e348e-195">Als de factuurregel verwijst naar een inkooporderregel, gebruikt u de boekhoudingsverdeling voor de inkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-195">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="e348e-196">De financiële dimensies gebruiken voor de totaalprijs of de boekhoudingsverdelingen voor de kost van de leveranciersfactuurregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-196">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="e348e-197">De financiële dimensiewaarden gebruiken van de leveranciersfactuurregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-197">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="e348e-198">De standaard financiële dimensiewaarden gebruiken van de hoofdrekening op de pagina Rekeningschema.</span><span class="sxs-lookup"><span data-stu-id="e348e-198">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e348e-199">Kopteksttoeslag</span><span class="sxs-lookup"><span data-stu-id="e348e-199">Header charge</span></span></td>
<td><ol>
<li><span data-ttu-id="e348e-200">Als Grootboekrekening is geselecteerd in het veld Debettype in het formulier Toeslagcode, het veld Debetrekening op de pagina Toeslagcode.</span><span class="sxs-lookup"><span data-stu-id="e348e-200">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="e348e-201">Als Klant/leverancier is geselecteerd in het veld Debettype in het formulier Toeslagcode, het veld Creditrekening op de pagina Toeslagcode.</span><span class="sxs-lookup"><span data-stu-id="e348e-201">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="e348e-202">Als de factuurregel verwijst naar een inkooporderregel, gebruikt u de boekhoudingsverdeling voor de inkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-202">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="e348e-203">Indien de hoofdrekening een toewijzingsrekening is, gebruikt u de standaardwaarde van de definitie van de toewijzingsrekening.</span><span class="sxs-lookup"><span data-stu-id="e348e-203">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="e348e-204">De standaardsjabloon gebruiken van de financiële dimensie van de leveranciersfactuurtitel.</span><span class="sxs-lookup"><span data-stu-id="e348e-204">Use the financial dimension default template values from the vendor invoice header.</span></span></li>
<li><span data-ttu-id="e348e-205">De financiële dimensiewaarden gebruiken van de leveranciersfactuurregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-205">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="e348e-206">De standaard financiële dimensiewaarden gebruiken van de hoofdrekening op de pagina Rekeningschema.</span><span class="sxs-lookup"><span data-stu-id="e348e-206">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e348e-207">Kortingtitel</span><span class="sxs-lookup"><span data-stu-id="e348e-207">Header discount</span></span></td>
<td><ol>
<li><span data-ttu-id="e348e-208">Het veld Hoofdrekening voor het boekingstype Korting op leveranciersfactuur op de pagina Rekeningen voor automatische transacties.</span><span class="sxs-lookup"><span data-stu-id="e348e-208">The Main account field for the Vendor invoice discount posting type in the Accounts for automatic transactions page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="e348e-209">Als de factuurregel verwijst naar een inkooporderregel, gebruikt u de boekhoudingsverdeling voor de inkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-209">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="e348e-210">De financiële dimensies gebruiken voor de boekhoudingsverdelingen voor de totaalprijs van de leveranciersfactuurregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-210">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="e348e-211">De financiële dimensiewaarden gebruiken van de leveranciersfactuurregel.</span><span class="sxs-lookup"><span data-stu-id="e348e-211">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="e348e-212">De standaard financiële dimensiewaarden gebruiken van de hoofdrekening op de pagina Rekeningschema.</span><span class="sxs-lookup"><span data-stu-id="e348e-212">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>


<a name="distributing-taxes"></a><span data-ttu-id="e348e-213">Belastingen verdelen</span><span class="sxs-lookup"><span data-stu-id="e348e-213">Distributing taxes</span></span>
------------------

<span data-ttu-id="e348e-214">Boekhoudingsverdelingen voor belastingen kunnen pas worden gemaakt nadat belastingen zijn berekend.</span><span class="sxs-lookup"><span data-stu-id="e348e-214">Accounting distributions for taxes cannot be created until taxes are calculated.</span></span> <span data-ttu-id="e348e-215">Voor het berekenen van de btw moet u een van de volgende taken uitvoeren op de pagina Leveranciersfactuur:</span><span class="sxs-lookup"><span data-stu-id="e348e-215">To calculate sales taxes, you must complete one of the following tasks in the Vendor invoice page:</span></span>
-   <span data-ttu-id="e348e-216">Het factuurtotaal weergeven.</span><span class="sxs-lookup"><span data-stu-id="e348e-216">View the invoice total.</span></span>
-   <span data-ttu-id="e348e-217">De btw weergeven.</span><span class="sxs-lookup"><span data-stu-id="e348e-217">View the sales tax.</span></span>
-   <span data-ttu-id="e348e-218">De subadministratie bekijken.</span><span class="sxs-lookup"><span data-stu-id="e348e-218">View the subledger journal.</span></span>
-   <span data-ttu-id="e348e-219">Boekhoudingsverdelingen voor de totale leveranciersfactuur weergeven.</span><span class="sxs-lookup"><span data-stu-id="e348e-219">View accounting distributions for the complete vendor invoice.</span></span>
-   <span data-ttu-id="e348e-220">Een leveranciersfactuur in wachtstand zetten.</span><span class="sxs-lookup"><span data-stu-id="e348e-220">Place the vendor invoice on hold.</span></span>
-   <span data-ttu-id="e348e-221">De leveranciersfactuur boeken.</span><span class="sxs-lookup"><span data-stu-id="e348e-221">Post the vendor invoice.</span></span>

## <a name="subledger-journals-for-vendor-invoices"></a><span data-ttu-id="e348e-222">Subgrootboekrekening voor leveranciersfacturen</span><span class="sxs-lookup"><span data-stu-id="e348e-222">Subledger journals for vendor invoices</span></span>
<span data-ttu-id="e348e-223">Voordat u een leveranciersfactuur boekt, kunt u het volledige boekhoudingsjournaal van de factuur bekijken, inclusief debet- en creditbedragen, om te controleren of de factuur naar de juiste rekeningen wordt geboekt.</span><span class="sxs-lookup"><span data-stu-id="e348e-223">Before you post a vendor invoice, you can view the full accounting entry of the invoice, which includes debits and credits, to verify that the invoice is being posted to the correct accounts.</span></span> <span data-ttu-id="e348e-224">Deze weergave van het volledige boekhoudingsjournaal heet een subadministratie.</span><span class="sxs-lookup"><span data-stu-id="e348e-224">This view of the full accounting entry is called a subledger journal.</span></span> 

<span data-ttu-id="e348e-225">Indien het journaal in de subadministratie onjuist is wanneer u een afdrukvoorbeeld bekijkt voordat u de leveranciersfactuur boekt, kunt u het journaal in de subadministratie niet wijzigen.</span><span class="sxs-lookup"><span data-stu-id="e348e-225">If the subledger journal entry is incorrect when you preview it before you journalize the vendor invoice, you cannot modify the subledger journal entry.</span></span> <span data-ttu-id="e348e-226">In plaats daarvan moet u de boekhoudingsverdelingen of het boekingsprofiel wijzigen.</span><span class="sxs-lookup"><span data-stu-id="e348e-226">Instead, you must modify the accounting distributions or the posting profile.</span></span> <span data-ttu-id="e348e-227">De boekhoudingsverdelingen worden gebruikt om één kant van de boekhoudingspost, de debit- of de creditzijde, te definiëren.</span><span class="sxs-lookup"><span data-stu-id="e348e-227">The accounting distributions are used to define one side of the accounting entry, the debit or the credit.</span></span> <span data-ttu-id="e348e-228">De compenserende journaalregel in de subadministratie wordt gemaakt van de boekingsprofielen, zoals van de leveranciersrekening of de belasting.</span><span class="sxs-lookup"><span data-stu-id="e348e-228">The offsetting subledger journal account entry is created by using the posting profiles, such as from the vendor account or tax.</span></span>




