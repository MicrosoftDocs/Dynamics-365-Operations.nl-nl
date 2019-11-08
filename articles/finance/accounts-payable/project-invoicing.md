---
title: Projectfacturering
description: Dit artikel biedt een overzicht van projectfacturen voor tijd- en materiaalprojecten en projecten met een vaste prijs. Het bevat informatie over factuurvoorstellen (voorlopige facturen), factuurbeheer, a conto-facturering, leveranciersfacturering en creditnota's.
author: ShylaThompson
manager: AnnBe
ms.date: 10/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjInvoiceCashFlow, ProjInvoiceControl, ProjInvoiceListPage, ProjInvoiceProposalDetail, ProjInvoiceProposalListPage
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23111
ms.assetid: 1812d6f2-8b34-4258-8f5f-dcf12281547f
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a68ed1cf21039ec1077bae428dea242f19514b51
ms.sourcegitcommit: 574309903f15eeab7911091114885b5c7279d22a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/24/2019
ms.locfileid: "2658615"
---
# <a name="project-invoicing"></a><span data-ttu-id="f77c0-104">Projectfacturering</span><span class="sxs-lookup"><span data-stu-id="f77c0-104">Project invoicing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f77c0-105">Dit artikel biedt een overzicht van projectfacturen voor tijd- en materiaalprojecten en projecten met een vaste prijs.</span><span class="sxs-lookup"><span data-stu-id="f77c0-105">This article provides an overview of project invoicing for Time and material projects and Fixed-price projects.</span></span> <span data-ttu-id="f77c0-106">Het bevat informatie over factuurvoorstellen (voorlopige facturen), factuurbeheer, a conto-facturering, leveranciersfacturering en creditnota's.</span><span class="sxs-lookup"><span data-stu-id="f77c0-106">It includes information about invoice proposals (preliminary invoices), invoice control, on-account invoicing, vendor invoicing, and credit notes.</span></span>

<span data-ttu-id="f77c0-107">Aan de hand van het projecttype wordt bepaald welke factureringsmethode moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="f77c0-107">The project type determines which invoicing procedure should be applied.</span></span> <span data-ttu-id="f77c0-108">Alleen de twee externe projecttypen, Tijd en materiaal en Vaste prijs, kunnen worden gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="f77c0-108">Only the two external project types, Time and material and Fixed-price, can be invoiced.</span></span> <span data-ttu-id="f77c0-109">Tijd- en materiaalprojecten en Projecten met een vaste prijs zijn altijd aan een projectcontract gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="f77c0-109">Time and material projects and Fixed-price projects are always attached to a project contract.</span></span>

-   <span data-ttu-id="f77c0-110">**Projecten met een vaste prijs**: het bedrag van de klantfactuur is gebaseerd op factureringsschema's.</span><span class="sxs-lookup"><span data-stu-id="f77c0-110">**Fixed-price projects** – The customer invoice amount is based on invoice billing schedules.</span></span> <span data-ttu-id="f77c0-111">Facturering wordt uitgevoerd via een a conto-instelling, ook wel een factureringsschema genoemd.</span><span class="sxs-lookup"><span data-stu-id="f77c0-111">Invoicing is done through an on-account setup, which is also referred to as a billing schedule.</span></span> <span data-ttu-id="f77c0-112">Projecten met een vaste prijs kunnen per project of per projectcontract worden gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="f77c0-112">Fixed-price projects can be invoiced per project or per project contract.</span></span>
-   <span data-ttu-id="f77c0-113">**Tijd- en materiaalprojecten**: het bedrag van de klantfactuur is gebaseerd op transactieregels die voor projecten zijn ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="f77c0-113">**Time and material projects** – The customer invoice amount is based on transaction lines that are entered on projects.</span></span> <span data-ttu-id="f77c0-114">Transacties kunnen per project of per projectcontract worden gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="f77c0-114">Transactions can be invoiced per project or per project contract.</span></span>

<span data-ttu-id="f77c0-115">Er zijn drie manieren om Tijd- en materiaalprojecten en Projecten met een vaste prijs te koppelen aan de factuurprojecten:</span><span class="sxs-lookup"><span data-stu-id="f77c0-115">There are three ways to attach Time and material projects and Fixed-price projects to the invoice projects:</span></span>

-   <span data-ttu-id="f77c0-116">**A conto-facturering**: Tijd- en materiaalprojecten en Projecten met een vaste prijs kunnen op rekening worden gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="f77c0-116">**On-account invoicing** – Time and material projects and Fixed-price projects can be invoiced on account.</span></span> <span data-ttu-id="f77c0-117">Voor elk projecttype zijn twee verschillende a conto-instellingen vereist.</span><span class="sxs-lookup"><span data-stu-id="f77c0-117">Two types of on-account setup are required, one for each project type.</span></span>
-   <span data-ttu-id="f77c0-118">**Facturering in de sectie periodiek**: via de periodieke functies kunnen transacties in projecten worden gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="f77c0-118">**Invoicing in the periodic section** – Through the periodic functions, transactions can be invoiced across projects.</span></span> <span data-ttu-id="f77c0-119">De periodieke functies geven een overzicht van transacties die moeten worden gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="f77c0-119">The periodic functions provide an overview of transactions that must be invoiced.</span></span>
-   <span data-ttu-id="f77c0-120">**Door creditnota's in de facturering te gebruiken**: voor zowel tijd- en materiaalprojecten als projecten met een vaste prijs kan een creditnota worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="f77c0-120">**By using credit notes in invoicing** – A credit note can be created for both Time and material projects and Fixed-price projects.</span></span>

## <a name="invoice-proposals"></a><span data-ttu-id="f77c0-121">Factuurvoorstellen</span><span class="sxs-lookup"><span data-stu-id="f77c0-121">Invoice proposals</span></span>
<span data-ttu-id="f77c0-122">Voordat u een klantfactuur voor een project maakt, kunt u een voorlopige factuur of factuurvoorstel maken.</span><span class="sxs-lookup"><span data-stu-id="f77c0-122">Before you create a customer invoice for a project, you can create a preliminary invoice, or invoice proposal.</span></span> <span data-ttu-id="f77c0-123">In een factuurvoorstel kunt u projecttransacties selecteren die in een projectfactuur moeten worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="f77c0-123">In an invoice proposal, you can select project transactions to include in a project invoice.</span></span> <span data-ttu-id="f77c0-124">U kunt de factuurdetails vervolgens controleren voordat u de projectfactuur boekt en het naar de klant of andere financieringsbron verstuurt.</span><span class="sxs-lookup"><span data-stu-id="f77c0-124">You can then review the invoice details before you post the project invoice and send it to the customer or other funding source.</span></span>

### <a name="creating-invoice-proposals"></a><span data-ttu-id="f77c0-125">Factuurvoorstellen maken</span><span class="sxs-lookup"><span data-stu-id="f77c0-125">Creating invoice proposals</span></span>

<span data-ttu-id="f77c0-126">U kunt factuurvoorstellen maken door handmatig te kiezen uit een lijst met transacties voor een opgegeven project.</span><span class="sxs-lookup"><span data-stu-id="f77c0-126">You can create invoice proposals by manually selecting from a list of transactions for a specified project.</span></span> <span data-ttu-id="f77c0-127">U kunt tevens factureringsregels instellen die opgeven wanneer automatisch een factuurvoorstel wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="f77c0-127">You can also set up billing rules that specify when to automatically create an invoice proposal.</span></span> <span data-ttu-id="f77c0-128">U kunt bijvoorbeeld een factureringsregel maken om een factuurvoorstel te maken wanneer het werk aan een project 25 procent, 50 procent, 75 procent, en 100 procent is voltooid.</span><span class="sxs-lookup"><span data-stu-id="f77c0-128">For example, you can create a billing rule to create an invoice proposal when work on a project is 25 percent, 50 percent, 75 percent, and 100 percent completed.</span></span> 

<span data-ttu-id="f77c0-129">U kunt factuurvoorstellen maken voor de volgende transacties:</span><span class="sxs-lookup"><span data-stu-id="f77c0-129">You can create invoice proposals for the following transactions:</span></span>

-   <span data-ttu-id="f77c0-130">Uren, onkosten en andere projecttransacties</span><span class="sxs-lookup"><span data-stu-id="f77c0-130">Hours, expenses, and other project transactions</span></span>
-   <span data-ttu-id="f77c0-131">Bedragen die door klanten op eerdere projectfacturen zijn ingehouden.</span><span class="sxs-lookup"><span data-stu-id="f77c0-131">Amounts that are withheld by customers on previous project invoices</span></span>
-   <span data-ttu-id="f77c0-132">Creditnota's</span><span class="sxs-lookup"><span data-stu-id="f77c0-132">Credit notes</span></span>
-   <span data-ttu-id="f77c0-133">Bedragen die een klant aan u heeft betaald voordat een project wordt gestart.</span><span class="sxs-lookup"><span data-stu-id="f77c0-133">Amounts that a customer paid to you before a project is started</span></span>

> [!NOTE]
> <span data-ttu-id="f77c0-134">Met de functie **Sorteren op resources inschakelen tijdens het maken van een projectfactuurvoorstel** kan de projectaccountant bij het maken van een nieuw projectfactuurvoorstel de projecttransacties die beschikbaar zijn voor facturering op resource sorteren.</span><span class="sxs-lookup"><span data-stu-id="f77c0-134">The **Enable sorting by resource during project invoice proposal creation** feature enables the project accountant to sort the project transactions available for billing by the resource when creating a new project invoice proposal.</span></span> <span data-ttu-id="f77c0-135">Het raster waarin de beschikbare projecttransacties worden weergegeven, heeft een afzonderlijk veld voor Resource-id en Resource, zodat de gebruiker op resourcenaam kan filteren en sorteren.</span><span class="sxs-lookup"><span data-stu-id="f77c0-135">The grid displaying the available project transactions will have a separate field for Resource ID and Resource, allowing the user to filter and sort on the resource name.</span></span> <span data-ttu-id="f77c0-136">Deze functie is standaard uitgeschakeld en kan worden ingeschakeld in **Werkgebieden > Functiebeheer**.</span><span class="sxs-lookup"><span data-stu-id="f77c0-136">This feature is disabled by default and can be enabled in **Workspaces > Feature management**.</span></span> <span data-ttu-id="f77c0-137">Neem contact op met uw systeembeheerder voor hulp bij het inschakelen van deze functie.</span><span class="sxs-lookup"><span data-stu-id="f77c0-137">Contact your system administrator for help in enabling this feature.</span></span>

<span data-ttu-id="f77c0-138">U kunt kostentransacties in een factuurvoorstel maken.</span><span class="sxs-lookup"><span data-stu-id="f77c0-138">You can create fee transactions in an invoice proposal.</span></span> <span data-ttu-id="f77c0-139">U kunt ook de verkoopprijs wijzigen voor uur-, onkosten-, artikel- en bijzondere-kostentransacties.</span><span class="sxs-lookup"><span data-stu-id="f77c0-139">You can also modify the sales price on hour, expense, item, and fee transactions.</span></span> <span data-ttu-id="f77c0-140">Als u een factuurvoorstel boekt, worden de bijgewerkte prijzen en transacties toegevoegd aan projectrapporten en de transactiehistorie.</span><span class="sxs-lookup"><span data-stu-id="f77c0-140">When you post an invoice proposal, the updated prices and transactions are added to project reports and the transaction history.</span></span> 

<span data-ttu-id="f77c0-141">Als u meerdere klantfacturen wilt maken voor een project, moet u een factuurvoorstel maken voor elke factuur.</span><span class="sxs-lookup"><span data-stu-id="f77c0-141">To create multiple customer invoices for a project, you must create an invoice proposal for each invoice.</span></span> <span data-ttu-id="f77c0-142">U kunt bijvoorbeeld, facturen maken op basis van transactietype.</span><span class="sxs-lookup"><span data-stu-id="f77c0-142">For example, you can create invoices based on transaction type.</span></span> <span data-ttu-id="f77c0-143">Als u uren op één klantfactuur wilt opgeven en artikelen op een andere, moet u afzonderlijke factuurvoorstellen maken voor uurtransacties en een kostentransacties.</span><span class="sxs-lookup"><span data-stu-id="f77c0-143">To specify hours on one customer invoice and items on another, you must create separate invoice proposals for hour transactions and fee transactions.</span></span> 

<span data-ttu-id="f77c0-144">U kunt een afzonderlijk factuurvoorstel maken voor elke financieringsbron als een project meer dan één financieringsbron heeft.</span><span class="sxs-lookup"><span data-stu-id="f77c0-144">If a project has more than one funding source, you can create a separate invoice proposal for each funding source.</span></span> <span data-ttu-id="f77c0-145">Op de pagina **Toewijzingen financieringsregels** kunt u het percentage definiëren van het transactiebedrag dat moet worden toegewezen aan elke financieringsbron, en u kunt de bron definiëren voor het boeken van afrondingsverschillen.</span><span class="sxs-lookup"><span data-stu-id="f77c0-145">On the **Funding rule allocations** page, you can define the percentage of the transaction amount to allocate to each funding source, and the source to post rounding differences.</span></span>

### <a name="creating-customer-invoices-from-invoice-proposals"></a><span data-ttu-id="f77c0-146">Klantfacturen maken van factuurvoorstellen</span><span class="sxs-lookup"><span data-stu-id="f77c0-146">Creating customer invoices from invoice proposals</span></span>

<span data-ttu-id="f77c0-147">Wanneer u een factuurvoorstel maakt en boekt, wordt automatisch een klantfactuur gemaakt voor de transacties die zijn opgenomen in het factuurvoorstel.</span><span class="sxs-lookup"><span data-stu-id="f77c0-147">After you create and post an invoice proposal, a customer invoice is automatically created for the transactions that are included in the invoice proposal.</span></span> 

<span data-ttu-id="f77c0-148">Voordat u een factuurvoorstel boekt, kunt u er transacties aan toevoegen of er transacties uit verwijderen.</span><span class="sxs-lookup"><span data-stu-id="f77c0-148">Before you post an invoice proposal, you can add transactions to it or delete transactions from it.</span></span> <span data-ttu-id="f77c0-149">U kunt bijvoorbeeld onkostentransacties verwijderen die voor een project zijn geboekt maar niet aan de klant kunnen worden toegerekend.</span><span class="sxs-lookup"><span data-stu-id="f77c0-149">For example, you can remove expense transactions that were posted to a project, but that are not chargeable to the customer.</span></span> 

<span data-ttu-id="f77c0-150">Als uw organisatie vereist dat factuurvoorstellen worden gecontroleerd voordat ze worden geboekt, moet het factuurvoorstel mogelijk worden goedgekeurd via de werkstroom "Projectfactuurvoorstellen controleren" voordat deze wordt geboekt.</span><span class="sxs-lookup"><span data-stu-id="f77c0-150">If your organization requires that invoice proposals be reviewed before they are posted, the invoice proposal might need to be approved through the "Review project invoice proposals" workflow before it is posted.</span></span>

## <a name="on-account-invoicing"></a><span data-ttu-id="f77c0-151">Facturering op rekening</span><span class="sxs-lookup"><span data-stu-id="f77c0-151">On-account invoicing</span></span>
<span data-ttu-id="f77c0-152">Het bedrag dat u op een a conto-factuur invoert voor een project, hangt af van de uren, het voltooiingspercentage en andere factuurvoorwaarden die in het bijbehorende projectcontract zijn gespecificeerd.</span><span class="sxs-lookup"><span data-stu-id="f77c0-152">The amount that you enter for a project in an on-account invoice is based on the timing, percentage of completion, and other billing conditions that are specified in the related project contract.</span></span> <span data-ttu-id="f77c0-153">Het bedrag wordt niet berekend op basis van de uren, artikelen, kosten of toeslagen die voor een project worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="f77c0-153">The amount is not calculated based on the hours, items, expenses, or fees that are posted to the project.</span></span> 

<span data-ttu-id="f77c0-154">U moet u eerst een a conto-transactie maken voor een Tijd- en materiaalproject of een Project met een vaste prijs voordat u die a conto-transactie aan een projectfactuur kunt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="f77c0-154">You must create an on-account transaction for a Time and material project or a Fixed-price project before you can add that on-account transaction to a project invoice.</span></span> <span data-ttu-id="f77c0-155">Voer op de a conto-transactie het bedrag in dat aan een klant moet worden gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="f77c0-155">On the on-account transaction, enter the amount to invoice a customer.</span></span> <span data-ttu-id="f77c0-156">Om een projectfactuur te maken voor het bedrag maakt u een voorlopige factuur (factuurvoorstel).</span><span class="sxs-lookup"><span data-stu-id="f77c0-156">To create a project invoice for the amount, create a preliminary invoice (invoice proposal).</span></span> <span data-ttu-id="f77c0-157">Selecteer in het factuurvoorstel de a conto-transactie.</span><span class="sxs-lookup"><span data-stu-id="f77c0-157">In the invoice proposal, select the on-account transaction.</span></span> <span data-ttu-id="f77c0-158">U kunt de a-conto-informatie bekijken in het factuurvoorstel voordat u er een projectfactuur voor maakt.</span><span class="sxs-lookup"><span data-stu-id="f77c0-158">You can review the on-account information in the invoice proposal before you create a project invoice for it.</span></span>

### <a name="fixed-price-projects"></a><span data-ttu-id="f77c0-159">Projecten met een vaste prijs</span><span class="sxs-lookup"><span data-stu-id="f77c0-159">Fixed-price projects</span></span>

<span data-ttu-id="f77c0-160">Voor projecten met een vaste prijs, worden a conto transacties gebaseerd op een vooraf overeengekomen mijlpaal, een leveringseenheid, of een facturering naar rato van voortgang zoals bepaald in een projectcontract.</span><span class="sxs-lookup"><span data-stu-id="f77c0-160">For Fixed-price projects, on-account transactions are based on an agreed-upon milestone, unit of delivery, or progress billing arrangement that is specified in a project contract.</span></span> <span data-ttu-id="f77c0-161">Er wordt één regel gemaakt voor elke betaling die van de projectklant moet worden ontvangen.</span><span class="sxs-lookup"><span data-stu-id="f77c0-161">One line is created for each payment that must be received from the project customer.</span></span> <span data-ttu-id="f77c0-162">Geen inhoudingen vereist.</span><span class="sxs-lookup"><span data-stu-id="f77c0-162">No deductions are required.</span></span>

### <a name="time-and-material-projects"></a><span data-ttu-id="f77c0-163">Tijd- en materiaalprojecten</span><span class="sxs-lookup"><span data-stu-id="f77c0-163">Time and material projects</span></span>

<span data-ttu-id="f77c0-164">Voor tijd- en materiaalprojecten, kunt u aan een klant of een andere financieringsbron een vooruitbetalingsbedrag factureren met een a conto-factuurvoorstel.</span><span class="sxs-lookup"><span data-stu-id="f77c0-164">For Time and material projects, you can bill a customer or other funding source for a prepayment amount by using an on-account invoice proposal.</span></span> <span data-ttu-id="f77c0-165">A conto-transacties invoeren als een regel.</span><span class="sxs-lookup"><span data-stu-id="f77c0-165">Enter on-account transactions as one line.</span></span> <span data-ttu-id="f77c0-166">U kunt desgewenst extra regels invoeren als inhoudingen om vooruitbetalingen van de klant te compenseren.</span><span class="sxs-lookup"><span data-stu-id="f77c0-166">You can optionally enter additional lines as deductions to offset any prepayments that the customer has already made.</span></span> <span data-ttu-id="f77c0-167">Om inhoudingsregels te maken moet vóór het bedrag een minteken staan</span><span class="sxs-lookup"><span data-stu-id="f77c0-167">To create deduction lines, precede the amount with a minus sign.</span></span>

## <a name="invoice-control"></a><span data-ttu-id="f77c0-168">Factuurbeheer</span><span class="sxs-lookup"><span data-stu-id="f77c0-168">Invoice control</span></span>
<span data-ttu-id="f77c0-169">Met factuurbeheer kunt u zowel gefactureerde als niet-gefactureerde transacties volgen en die transacties analyseren met behulp van offertes zodat u een beeld krijgt van het verloop van uw projecten, vanaf de offerte tot aan voltooiing.</span><span class="sxs-lookup"><span data-stu-id="f77c0-169">You can use invoice control to track both invoiced and non-invoiced transactions, and to analyze those transactions against quotations for an end-to-end view of your projects from the quotation stage to completion.</span></span> <span data-ttu-id="f77c0-170">U kunt zien welke transacties naar een bepaald project zijn geladen en welke regels zijn gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="f77c0-170">You can see which transactions have been charged to a specific project and which lines have been invoiced.</span></span> <span data-ttu-id="f77c0-171">Het is ook mogelijk om de afzonderlijke transacties weer te geven zodat u deze kunt corrigeren nadat ze zijn geboekt.</span><span class="sxs-lookup"><span data-stu-id="f77c0-171">You can also view individual transactions, so that you can adjust them after they are posted.</span></span>

## <a name="invoicing-fixed-price-projects"></a><span data-ttu-id="f77c0-172">Projecten met een vaste prijs factureren</span><span class="sxs-lookup"><span data-stu-id="f77c0-172">Invoicing Fixed-price projects</span></span>
<span data-ttu-id="f77c0-173">Om Projecten met een vaste prijs te factureren moet u een factureringsschema definiëren en de factureringsprocedure voltooien.</span><span class="sxs-lookup"><span data-stu-id="f77c0-173">To invoice a Fixed-price project, you must define a billing schedule and complete the invoicing procedure.</span></span>

### <a name="billing-schedule"></a><span data-ttu-id="f77c0-174">Factureringsplanning</span><span class="sxs-lookup"><span data-stu-id="f77c0-174">Billing schedule</span></span>

<span data-ttu-id="f77c0-175">U kunt Projecten met een vaste prijs factureren op een factureringsplanning.</span><span class="sxs-lookup"><span data-stu-id="f77c0-175">You can invoice Fixed-price projects on a billing schedule.</span></span> <span data-ttu-id="f77c0-176">Het factureringsschema wordt gedefinieerd in de vorm van één of meer mijlpalen voor het project.</span><span class="sxs-lookup"><span data-stu-id="f77c0-176">The billing schedule is defined in terms of one or more milestones for the project.</span></span> <span data-ttu-id="f77c0-177">Voor elke mijlpaal kunt u een specifieke datum, verkoopvaluta, een verkoopprijs en activiteit definiëren.</span><span class="sxs-lookup"><span data-stu-id="f77c0-177">For each milestone, you can define a specific date, sales currency, sales price, and activity.</span></span> 

<span data-ttu-id="f77c0-178">U kunt bijvoorbeeld het volgende factureringsschema instellen:</span><span class="sxs-lookup"><span data-stu-id="f77c0-178">For example, you can set up the following billing schedule:</span></span>

-   <span data-ttu-id="f77c0-179">20 procent wanneer het projectcontract wordt ondertekend</span><span class="sxs-lookup"><span data-stu-id="f77c0-179">20 percent when the project contract is signed</span></span>
-   <span data-ttu-id="f77c0-180">30 procent na de eerste levering</span><span class="sxs-lookup"><span data-stu-id="f77c0-180">30 percent on first delivery</span></span>
-   <span data-ttu-id="f77c0-181">15 procent na de tweede levering</span><span class="sxs-lookup"><span data-stu-id="f77c0-181">15 percent on second delivery</span></span>
-   <span data-ttu-id="f77c0-182">35 procent na de laatste levering</span><span class="sxs-lookup"><span data-stu-id="f77c0-182">35 percent on final delivery</span></span>

### <a name="invoicing-procedure"></a><span data-ttu-id="f77c0-183">Factureringsprocedure</span><span class="sxs-lookup"><span data-stu-id="f77c0-183">Invoicing procedure</span></span>

<span data-ttu-id="f77c0-184">Wanneer de mijlpaalbetalingen kunnen worden gefactureerd, gebruikt u de procedure voor de facturering van a conto-bedragen.</span><span class="sxs-lookup"><span data-stu-id="f77c0-184">When the milestone payments are ready to be invoiced, you use the procedure for invoicing on-account amounts.</span></span>

## <a name="vendor-invoicing"></a><span data-ttu-id="f77c0-185">Leveranciersfacturering</span><span class="sxs-lookup"><span data-stu-id="f77c0-185">Vendor invoicing</span></span>
<span data-ttu-id="f77c0-186">Wanneer u een artikel van een leverancier bestelt en het artikel aan een project toewijst, bepaalt de eigenschap die u voor de inkooporderregel voor dat artikel selecteert of het ingekochte artikel aan een klant wordt gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="f77c0-186">When you order an item from a vendor and assign the item to a project, the line property that you select for the purchase order line for that item determines whether the purchased item is invoiced to a customer.</span></span> <span data-ttu-id="f77c0-187">Als u standaardregeleigenschappen instelt, worden deze weergegeven voor het artikel op de inkooporderregel (Regeldetails &gt; Project &gt; Regeleigenschap).</span><span class="sxs-lookup"><span data-stu-id="f77c0-187">If you set up default line properties, they are displayed for the item on the purchase order line (Line details &gt; Project &gt; Line property).</span></span> <span data-ttu-id="f77c0-188">Er zijn twee manieren om de regeleigenschap te wijzigen:</span><span class="sxs-lookup"><span data-stu-id="f77c0-188">There are two ways to modify the line property:</span></span>

-   <span data-ttu-id="f77c0-189">Het factureren van de klant van het project voor het artikel: stel de regeleigenschap voor het artikel in op een toerekenbare waarde op de inkooporder en factureer vervolgens de klant door de juiste projectfactureringsmethode te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="f77c0-189">Invoice the project's customer for the item: Set the line property for the item to a chargeable value on the purchase order, and then invoice the customer by using the correct project invoicing method.</span></span>
-   <span data-ttu-id="f77c0-190">Factureer niet de projectklant voor het artikel: selecteert niet de regeleigenschap **Toerekenbaar** op de inkooporderregel voor het artikel.</span><span class="sxs-lookup"><span data-stu-id="f77c0-190">Don’t invoice the project's customer for the item: Don’t select the **Chargeable** line property on the purchase order line for the item.</span></span> <span data-ttu-id="f77c0-191">U kunt de inkooporder vervolgens factureren en verder hoeft u niets te doen.</span><span class="sxs-lookup"><span data-stu-id="f77c0-191">You can then invoice the purchase order, and no further action is required.</span></span>

## <a name="credit-notes"></a><span data-ttu-id="f77c0-192">Creditnota's</span><span class="sxs-lookup"><span data-stu-id="f77c0-192">Credit notes</span></span>
<span data-ttu-id="f77c0-193">Als een bedrag op een klantfactuur een negatieve waarde heeft, wordt de factuur geclassificeerd als creditnota.</span><span class="sxs-lookup"><span data-stu-id="f77c0-193">When an amount on a customer invoice has a negative value, the invoice is classified as a credit note.</span></span> <span data-ttu-id="f77c0-194">Wanneer het document wordt afgedrukt, heeft het de titel "Creditnota".</span><span class="sxs-lookup"><span data-stu-id="f77c0-194">When the document is printed, it has the title "Credit note."</span></span> 

<span data-ttu-id="f77c0-195">Als u een creditnota maakt om een bedrag te crediteren dat eerder is gefactureerd, moet u dit bedrag eerst voor creditering selecteren.</span><span class="sxs-lookup"><span data-stu-id="f77c0-195">When you create a credit note to credit an amount that was previously invoiced, you must first select the invoiced amount for crediting.</span></span> <span data-ttu-id="f77c0-196">Vervolgens maakt u een creditnota. Hiervoor geldt dezelfde methode als voor het maken van een gewone klantfactuur.</span><span class="sxs-lookup"><span data-stu-id="f77c0-196">You then create a credit note by following the same procedure that you would use to create an ordinary customer invoice.</span></span> <span data-ttu-id="f77c0-197">U moet dus de transacties selecteren die eerder op een klantfactuur zijn geboekt en vervolgens een creditnotavoorstel maken en boeken.</span><span class="sxs-lookup"><span data-stu-id="f77c0-197">In other words, you select the transactions that were previously posted on a customer invoice, and then create and post a credit note proposal.</span></span> 

<span data-ttu-id="f77c0-198">Hetzelfde document kan transacties bevatten die zijn geselecteerd voor creditering, credittransacties en transacties die zijn geboekt.</span><span class="sxs-lookup"><span data-stu-id="f77c0-198">The same document can include transactions that are selected for crediting, credit transactions, and transactions that have been posted.</span></span> <span data-ttu-id="f77c0-199">Afhankelijk van of het totale bedrag positief of negatief is, wordt het document geclassificeerd als een factuur of creditnota.</span><span class="sxs-lookup"><span data-stu-id="f77c0-199">The document is classified as either an invoice or a credit note, depending on whether the total amount is positive or negative.</span></span> 

<span data-ttu-id="f77c0-200">Als u een gefactureerd bedrag wilt crediteren, moet u dit bedrag eerst voor creditering selecteren en vervolgens een creditnota maken.</span><span class="sxs-lookup"><span data-stu-id="f77c0-200">To credit an invoiced amount, you first select the invoiced amount to credit and then create a credit note.</span></span> <span data-ttu-id="f77c0-201">U maakt een creditnota met dezelfde methode als voor het maken van een klantfactuur.</span><span class="sxs-lookup"><span data-stu-id="f77c0-201">You create a credit note by following the same procedure that you would use to generate a customer invoice.</span></span> 

<span data-ttu-id="f77c0-202">U kunt een klantfactuur met een negatieve waarde maken. Dit wordt een factuur die wordt geclassificeerd als creditnota.</span><span class="sxs-lookup"><span data-stu-id="f77c0-202">You can create an invoice that has a negative amount, which becomes an invoice that is classified as a credit note.</span></span> <span data-ttu-id="f77c0-203">Om een creditnota te maken en af te drukken moet u de transacties selecteren die eerder voor een klantfactuur zijn geboekt en vervolgens de transacties bewerken.</span><span class="sxs-lookup"><span data-stu-id="f77c0-203">To create and print a credit note, you must select the transactions that were previously posted for a customer invoice, and then modify the transactions.</span></span> <span data-ttu-id="f77c0-204">Tenzij het primaire adres van de rechtspersoon Duitsland is, wordt de titel van de factuur "Correctiefactuur".</span><span class="sxs-lookup"><span data-stu-id="f77c0-204">Unless the primary address of the legal entity is in Germany, the title of the invoice will be "Corrective invoice."</span></span>


