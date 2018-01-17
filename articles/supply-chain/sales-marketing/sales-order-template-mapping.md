---
title: Kopteksten en regels in verkooporders synchroniseren vanuit Finance and Operations naar Sales
description: In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van kopteksten en regels van verkooporders tussen Microsoft Dynamics 365 for Finance and Operations, Enterprise edition en Microsoft Dynamics 365 for Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: d7e4c435a3344f6a5d66e1889b633d80cda085eb
ms.contentlocale: nl-nl
ms.lasthandoff: 01/17/2018

---

# <a name="synchronize-sales-order-headers-and-lines-from-finance-and-operations-to-sales"></a><span data-ttu-id="1f898-103">Kopteksten en regels in verkooporders synchroniseren vanuit Finance and Operations naar Sales</span><span class="sxs-lookup"><span data-stu-id="1f898-103">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1f898-104">In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van kopteksten en regels van verkooporders tussen Microsoft Dynamics 365 for Finance and Operations, Enterprise edition en Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="1f898-104">The topic discusses the templates and underlying tasks that are used to synchronize sales order headers and lines from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span> 

## <a name="template-and-tasks"></a><span data-ttu-id="1f898-105">Sjabloon en taken</span><span class="sxs-lookup"><span data-stu-id="1f898-105">Template and tasks</span></span>

<span data-ttu-id="1f898-106">De volgende sjablonen en onderliggende taken worden gebruikt voor het synchroniseren van de kopteksten en regels van verkooporders tussen Finance and Operations en Sales:</span><span class="sxs-lookup"><span data-stu-id="1f898-106">The following templates and underlying tasks are used to synchronize sales order headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="1f898-107">**Naam van sjabloon in Gegevensintegratie**</span><span class="sxs-lookup"><span data-stu-id="1f898-107">**Name of template in Data integration**</span></span> 

    - <span data-ttu-id="1f898-108">Verkooporders (Fin and Ops naar Sales)</span><span class="sxs-lookup"><span data-stu-id="1f898-108">Sales Orders (Fin and Ops to Sales)</span></span>
    
- <span data-ttu-id="1f898-109">**Namen van taken in het project Gegevensintegratie**</span><span class="sxs-lookup"><span data-stu-id="1f898-109">**Names of tasks in Data integration project**</span></span>

    - <span data-ttu-id="1f898-110">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="1f898-110">OrderHeader</span></span>
    - <span data-ttu-id="1f898-111">OrderLine</span><span class="sxs-lookup"><span data-stu-id="1f898-111">OrderLine</span></span>

<span data-ttu-id="1f898-112">Taken die nodig zijn voor het synchroniseren van koptekst en regels van verkoopfacturen:</span><span class="sxs-lookup"><span data-stu-id="1f898-112">Sync tasks required prior to Sales invoice header and lines sync:</span></span>

- <span data-ttu-id="1f898-113">Producten (Fin en Ops naar Sales)</span><span class="sxs-lookup"><span data-stu-id="1f898-113">Products (Fin and Ops to Sales)</span></span>
- <span data-ttu-id="1f898-114">Rekeningen (Sales naar Fin and Ops) (indien gebruikt)</span><span class="sxs-lookup"><span data-stu-id="1f898-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
- <span data-ttu-id="1f898-115">Contactpersonen naar klanten (Sales naar Fin and Ops) (indien gebruikt)</span><span class="sxs-lookup"><span data-stu-id="1f898-115">Contacts to Customers (Sales to Fin and Ops) (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="1f898-116">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="1f898-116">Entity set</span></span>

| <span data-ttu-id="1f898-117">Finance en Operations</span><span class="sxs-lookup"><span data-stu-id="1f898-117">Finance and Operations</span></span> |    <span data-ttu-id="1f898-118">Common Data Service (CDS)</span><span class="sxs-lookup"><span data-stu-id="1f898-118">Common Data Service (CDS)</span></span>         |     <span data-ttu-id="1f898-119">Verkoop</span><span class="sxs-lookup"><span data-stu-id="1f898-119">Sales</span></span>      |
|------------------------|----------------|----------------|
| <span data-ttu-id="1f898-120">CDS-verkooporderkoppen</span><span class="sxs-lookup"><span data-stu-id="1f898-120">CDS sales order headers</span></span>| <span data-ttu-id="1f898-121">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="1f898-121">SalesOrder</span></span>     | <span data-ttu-id="1f898-122">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="1f898-122">SalesOrders</span></span> |
| <span data-ttu-id="1f898-123">CDS-verkooporderregels</span><span class="sxs-lookup"><span data-stu-id="1f898-123">CDS sales order lines</span></span>  | <span data-ttu-id="1f898-124">SalesOrderLine</span><span class="sxs-lookup"><span data-stu-id="1f898-124">SalesOrderLine</span></span> | <span data-ttu-id="1f898-125">SalesOrderDetails</span><span class="sxs-lookup"><span data-stu-id="1f898-125">SalesOrderDetails</span></span>|

## <a name="entity-flow"></a><span data-ttu-id="1f898-126">Entiteitstroom</span><span class="sxs-lookup"><span data-stu-id="1f898-126">Entity flow</span></span>

<span data-ttu-id="1f898-127">Verkooporders worden gemaakt in Finance and Operations en gesynchroniseerd met Sales.</span><span class="sxs-lookup"><span data-stu-id="1f898-127">Sales orders are created in Finance and Operations and synchronized to Sales.</span></span>

<span data-ttu-id="1f898-128">Filters in de sjabloon zorgen ervoor dat alleen relevante verkooporders worden opgenomen in de synchronisatie:</span><span class="sxs-lookup"><span data-stu-id="1f898-128">Filters in the template ensure that only relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="1f898-129">Zowel de bestellende als de facturerende klant op de verkooporder uit Sales wordt opgenomen in de synchronisatie.</span><span class="sxs-lookup"><span data-stu-id="1f898-129">Both ordering and invoicing customer on the sales order that originate from Sales will be included in the synchronization.</span></span> <span data-ttu-id="1f898-130">In Finance and Operations worden de velden **OrderingCustomerIsExternallyMaintained** en **InvoiceCustomerIsExternallyMaintained** gebruikt om de synchronisatie in de gegevensentiteiten bij te houden.</span><span class="sxs-lookup"><span data-stu-id="1f898-130">In Finance and Operations, the fields **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** are used to track the synchronization in the data entities.</span></span>

- <span data-ttu-id="1f898-131">De **verkooporder** in Finance and Operations moet worden bevestigd.</span><span class="sxs-lookup"><span data-stu-id="1f898-131">The **Sales order** in Finance and Operations must be confirmed.</span></span> <span data-ttu-id="1f898-132">Alleen de bevestigde verkooporders of verkooporders met een hogere verwerkingsstatus, bijvoorbeeld met de status Verzonden of Gefactureerd, worden gesynchroniseerd met Sales.</span><span class="sxs-lookup"><span data-stu-id="1f898-132">Only the confirmed sales orders or sales orders with higher processing status, for example, Shipped or Invoiced status, are synchronized to Sales.</span></span>

- <span data-ttu-id="1f898-133">Na het maken of wijzigen van een verkooporder moet de batchtaak **Verkooptotalen berekenen** in Finance and Operations worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="1f898-133">After creating or modifying a sales order, the batch job **Calculate sales totals** in Finance and Operations must be executed.</span></span> <span data-ttu-id="1f898-134">Alleen de verkooporders waarvoor verkooptotalen zijn berekend, worden gesynchroniseerd met CDS en Sales.</span><span class="sxs-lookup"><span data-stu-id="1f898-134">Only the sales orders with sales totals calculated will be synced to CDS and Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="1f898-135">Belastingen met betrekking tot toeslagen in de **koptekst van de verkooporder** worden niet opgenomen bij de synchronisatie van Finance and Operations met Sales.</span><span class="sxs-lookup"><span data-stu-id="1f898-135">Tax related to charges on the **Sales order header** is currently not included in synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="1f898-136">Sales biedt namelijk geen ondersteuning voor belastinggegevens op koptekstniveau.</span><span class="sxs-lookup"><span data-stu-id="1f898-136">This is because Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="1f898-137">Belastingen met betrekking tot kosten op het regelniveau worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="1f898-137">Tax related to charges at the line level is included.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="1f898-138">Oplossing Prospect naar contant geld voor Sales</span><span class="sxs-lookup"><span data-stu-id="1f898-138">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="1f898-139">Nieuwe velden worden toegevoegd aan de entiteit **Order** en weergegeven op de pagina:</span><span class="sxs-lookup"><span data-stu-id="1f898-139">New fields are added to the **Order** entity and displayed on the page:</span></span>

- <span data-ttu-id="1f898-140">**Wordt extern beheerd**: ingesteld op **Ja** wanneer de order afkomstig is van Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1f898-140">**Is Maintained Externally** - Set to **Yes** when the order is coming from Finance and Operations.</span></span>

- <span data-ttu-id="1f898-141">**Verwerkingsstatus**: wordt gebruikt om de verwerkingsstatus weer te geven van de order in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1f898-141">**Processing status** - Used to show the processing status of the order in Finance and Operations.</span></span> <span data-ttu-id="1f898-142">De volgende waarden zijn mogelijk:</span><span class="sxs-lookup"><span data-stu-id="1f898-142">Values are:</span></span>

    - <span data-ttu-id="1f898-143">Actief</span><span class="sxs-lookup"><span data-stu-id="1f898-143">Active</span></span>
    - <span data-ttu-id="1f898-144">Bevestigd</span><span class="sxs-lookup"><span data-stu-id="1f898-144">Confirmed</span></span>
    - <span data-ttu-id="1f898-145">Pakbon</span><span class="sxs-lookup"><span data-stu-id="1f898-145">Packing Slip</span></span>
    - <span data-ttu-id="1f898-146">Gefactureerd</span><span class="sxs-lookup"><span data-stu-id="1f898-146">Invoiced</span></span>
    - <span data-ttu-id="1f898-147">Opgenomen</span><span class="sxs-lookup"><span data-stu-id="1f898-147">Picked</span></span>
    - <span data-ttu-id="1f898-148">Gedeeltelijk opgenomen</span><span class="sxs-lookup"><span data-stu-id="1f898-148">Partially Picked</span></span>
    - <span data-ttu-id="1f898-149">Gedeeltelijk ingepakt</span><span class="sxs-lookup"><span data-stu-id="1f898-149">Partially Packed</span></span>
    - <span data-ttu-id="1f898-150">Verzonden</span><span class="sxs-lookup"><span data-stu-id="1f898-150">Shipped</span></span>
    - <span data-ttu-id="1f898-151">Gedeeltelijk verzonden</span><span class="sxs-lookup"><span data-stu-id="1f898-151">Partially Shipped</span></span>
    - <span data-ttu-id="1f898-152">Gedeeltelijk gefactureerd</span><span class="sxs-lookup"><span data-stu-id="1f898-152">Partially Invoiced</span></span>
    - <span data-ttu-id="1f898-153">Geannuleerd</span><span class="sxs-lookup"><span data-stu-id="1f898-153">Cancelled</span></span>

<span data-ttu-id="1f898-154">De instelling **Heeft alleen extern onderhouden producten** wordt gebruikt in andere verkooporderscenario's (synchronisatie van Sales met Finance and Operation) om consequent bij te houden of de verkooporder geheel uit **extern onderhouden producten** bestaat, in welk geval producten worden onderhouden in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1f898-154">The **Has Externally Maintained Products Only** setting is used in other sales order scenarios (from Sales to Finance and Operation sync) to consistently keep track of whether the sales order is made up entirely of **Externally Maintained Products**, in which case products are maintained in Finance and Operations.</span></span> <span data-ttu-id="1f898-155">Zo garandeert u dat u niet verkooporderregels probeert te synchroniseren met producten die onbekend zijn in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1f898-155">This ensures that you don't try to sync sales order lines with products that are unknown to Finance and Operations.</span></span>
 
<span data-ttu-id="1f898-156">De knoppen **Factuur maken**, **Order annuleren**, **Opnieuw berekenen**, **Producten ophalen** en **Adres opzoeken** op de pagina **Verkooporder** zijn verborgen voor extern onderhouden orders omdat facturen worden gemaakt in Finance and Operations en deze worden gesynchroniseerd met Sales.</span><span class="sxs-lookup"><span data-stu-id="1f898-156">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products** and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders because invoices will be created in Finance and Operations and synced to Sales.</span></span> <span data-ttu-id="1f898-157">De bestelpagina kan niet worden bewerkt omdat verkoopordergegevens vanuit Finance and Operations worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="1f898-157">The order page is non-editable because sales order information will be synced from Finance and Operations.</span></span>
 
<span data-ttu-id="1f898-158">De **verkooporderstatus** blijft actief om ervoor te zorgen dat wijzigingen vanuit Finance and Operations naar de **verkooporder** in Sales kunnen stromen.</span><span class="sxs-lookup"><span data-stu-id="1f898-158">The **Sales order status** will remain active to ensure that changes from Finance and Operations can flow to the **Sales order** in Sales.</span></span> <span data-ttu-id="1f898-159">U doet dit door **Statuscode [Status]** in te stellen op **Actief** in het project Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="1f898-159">This is controlled by setting the default **Statecode [Status]** to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="1f898-160">Voorwaarden en instellingen voor toewijzing</span><span class="sxs-lookup"><span data-stu-id="1f898-160">Preconditions and mapping setup</span></span> 

<span data-ttu-id="1f898-161">Voordat u verkooporders synchroniseert, is het belangrijk de systemen bij te werken met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="1f898-161">Before synchronizing sales orders, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="1f898-162">Instellingen in Sales</span><span class="sxs-lookup"><span data-stu-id="1f898-162">Setup in Sales</span></span>

- <span data-ttu-id="1f898-163">Zorg voor machtigingen voor het team waaraan de gebruiker (vanuit **Verbindingsset** in Sales) is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="1f898-163">Ensure permissions for the team that the user (from your Sales **Connection set**) is assigned to.</span></span> <span data-ttu-id="1f898-164">Als u voorbeeldgegevens gebruikt, heeft de gebruiker meestal beheerderstoegang, maar niet het team.</span><span class="sxs-lookup"><span data-stu-id="1f898-164">If you are using demo data, usually the user has admin access, but not the team.</span></span> <span data-ttu-id="1f898-165">Zonder beheerderstoegang ontvangt u een fout dat het hoofdteam ontbreekt wanneer u het project uitvoert vanuit Gegevensintegrator.</span><span class="sxs-lookup"><span data-stu-id="1f898-165">Without this you will get an error that Principal team is missing when running the project from Data integrator.</span></span> 

    - <span data-ttu-id="1f898-166">Selecteer onder **Instellingen** > **Beveiliging** > **Teams** het relevante team, klik op **Rollen beheren** en selecteer een rol met de gewenste machtigingen, bijvoorbeeld Systeembeheerder.</span><span class="sxs-lookup"><span data-stu-id="1f898-166">Under **Settings** > **Security** > **Teams**, select the relevant team, click **Manage Roles** and select a role with the desired permissions e.g. System Administrator.</span></span>

- <span data-ttu-id="1f898-167">Controleer of onder **Instellingen** > **Beheer** > **Systeeminstellingen** > **Sales** de optie **Systeem voor berekenen van systeemprijzen gebruiken** is ingesteld op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="1f898-167">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Use system prizing calculation system** is set to **Yes**.</span></span> 

- <span data-ttu-id="1f898-168">Controleer of onder **Instellingen** > **Beheer** > **Systeeminstellingen** > **Sales** de optie **Berekeningsmethode korting** is ingesteld op **Regelartikel**.</span><span class="sxs-lookup"><span data-stu-id="1f898-168">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Discount calculation method** is set to **Line item**.</span></span> 

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="1f898-169">Instellingen In Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1f898-169">Setup in Finance and Operations</span></span>

<span data-ttu-id="1f898-170">Stel **Verkoop en marketing** > **Periodieke taken** > **Verkooptotalen berekenen** in om te worden uitgevoerd als batchtaak, met **Totalen berekenen voor verkooporders** ingesteld op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="1f898-170">Set **Sales and marketing** > **Periodic tasks** > **Calculate sales totals** to run as a batch job, with **Calculate totals for sales orders** set to **Yes**.</span></span> <span data-ttu-id="1f898-171">Dit is belangrijk omdat alleen de verkooporders waarvoor verkooptotalen zijn berekend, worden gesynchroniseerd met CDS en Sales.</span><span class="sxs-lookup"><span data-stu-id="1f898-171">This is important because only the sales orders with sales totals calculated will be synced to CDS and Sales.</span></span> <span data-ttu-id="1f898-172">De frequentie van de batchtaak moet worden uitgelijnd met de frequentie van de verkoopordersynchronisatie.</span><span class="sxs-lookup"><span data-stu-id="1f898-172">The frequency of the batch job should be alligned with the frequency of the sales order synchronization.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="1f898-173">Instellingen in het project Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="1f898-173">Setup in the Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="1f898-174">Taak SalesHeader</span><span class="sxs-lookup"><span data-stu-id="1f898-174">SalesHeader task</span></span>

- <span data-ttu-id="1f898-175">Werk de toewijzing voor **CDS-organisatie-id bij in Bron** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="1f898-175">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span>

    - <span data-ttu-id="1f898-176">De standaardsjabloonwaarde voor **Account_Organization_OrganizationId** is ORG001.</span><span class="sxs-lookup"><span data-stu-id="1f898-176">Default template value for **Account_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="1f898-177">De standaardsjabloonwaarde voor **InvoiceAccount_Organization_OrganizationId** is ORG001.</span><span class="sxs-lookup"><span data-stu-id="1f898-177">Default template value for **InvoiceAccount_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="1f898-178">De standaardsjabloonwaarde voor **Organization_OrganizationId** is ORG001.</span><span class="sxs-lookup"><span data-stu-id="1f898-178">Default template value for **Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="1f898-179">Zorg ervoor dat de benodigde toewijzing bestaat in **Bron** > **CDS voor InvoiceCountryRegionId to BillingAddress_Country** en voor **DeliveryCountryRegionId to DeliveryAddress_Country**.</span><span class="sxs-lookup"><span data-stu-id="1f898-179">Ensure that the needed mapping exists in **Source** > **CDS for InvoiceCountryRegionId to BillingAddress_Country** and for **DeliveryCountryRegionId to DeliveryAddress_Country**.</span></span>

    - <span data-ttu-id="1f898-180">De waarde van de sjabloon is **ValueMap** met een aantal landen die zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="1f898-180">Template value is **ValueMap** with a number of countries mapped.</span></span>

- <span data-ttu-id="1f898-181">**Prijslijst** is vereist voor het maken van orders in Sales.</span><span class="sxs-lookup"><span data-stu-id="1f898-181">**Price list** is required to create orders in Sales.</span></span> <span data-ttu-id="1f898-182">Werk **ValueMap** in **CDS** > **Bestemming** voor **pricelevelid.name [Price List Name]** per valuta bij naar de gebruikte **prijslijst** in Sales.</span><span class="sxs-lookup"><span data-stu-id="1f898-182">Update the **ValueMap** in **CDS** > **Destination** for **pricelevelid.name [Price List Name]** to the **Price list** used in Sales per currency.</span></span> <span data-ttu-id="1f898-183">U kunt de gebruikte **prijslijst** voor één valuta of **ValueMap** gebruiken als u **prijslijsten** in meerdere valuta's hebt.</span><span class="sxs-lookup"><span data-stu-id="1f898-183">You can either used the default **Price list** for single currency or use **ValueMap** if you have **Price lists** in multiple currencies.</span></span>
    
    - <span data-ttu-id="1f898-184">De standaardwaarde van de sjabloon voor **pricelevelid.name [Price List Name]** is CRM Service USA (voorbeeld).</span><span class="sxs-lookup"><span data-stu-id="1f898-184">Default template value for **pricelevelid.name [Price List Name]** is CRM Service USA (sample).</span></span> 

#### <a name="salesline-task"></a><span data-ttu-id="1f898-185">Taak SalesLine</span><span class="sxs-lookup"><span data-stu-id="1f898-185">SalesLine task</span></span>

- <span data-ttu-id="1f898-186">Werk de toewijzing voor **CDS-organisatie-id bij in Bron** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="1f898-186">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span> 
    
    - <span data-ttu-id="1f898-187">De standaardsjabloonwaarde voor **SalesOrder_Organization_OrganizationId** is ORG001.</span><span class="sxs-lookup"><span data-stu-id="1f898-187">Default template value for **SalesOrder_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="1f898-188">De standaardsjabloonwaarde voor **Product_Organization_OrganizationId** is ORG001.</span><span class="sxs-lookup"><span data-stu-id="1f898-188">Default template value for **Product_Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="1f898-189">Zorg ervoor dat de benodigde toewijzing aanwezig is in **Bron** > **CDS** voor **DeliveryCountryRegionId** tot **DeliveryAddress_Country**.</span><span class="sxs-lookup"><span data-stu-id="1f898-189">Ensure that the needed mapping exists in **Source** > **CDS** for **DeliveryCountryRegionId** to **DeliveryAddress_Country**.</span></span>

    - <span data-ttu-id="1f898-190">De waarde van de sjabloon is **ValueMap** met een aantal landen die zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="1f898-190">Template value is **ValueMap** with a number of countries mapped.</span></span>
    
- <span data-ttu-id="1f898-191">Controleer of de benodigde **ValueMap** voor **SalesUnitSymbol** in Finance and Operations aanwezig is in **Bron** > **CDS-toewijzing**.</span><span class="sxs-lookup"><span data-stu-id="1f898-191">Ensure that the needed **ValueMap** for **SalesUnitSymbol** in Finance and Operations exists in the **Source** > **CDS mapping**.</span></span>

    - <span data-ttu-id="1f898-192">Waarde van de sjabloon met **ValueMap** is gedefinieerd voor **SalesUnitSymbol naar Quantity_UOM**.</span><span class="sxs-lookup"><span data-stu-id="1f898-192">Template value with **ValueMap** is defined for **SalesUnitSymbol to Quantity_UOM**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="1f898-193">Sjabloontoewijzing in gegevensintegrator</span><span class="sxs-lookup"><span data-stu-id="1f898-193">Template mapping in data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="1f898-194">De velden **Betalingsvoorwaarden**, **Leveringscondities**, **Leveringsvoorwaarden**, **Verzendmethode** en **Leveringsmethode** maken geen deel uit van de standaardtoewijzingen.</span><span class="sxs-lookup"><span data-stu-id="1f898-194">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="1f898-195">Als u deze velden wilt toewijzen, moet u een waardetoewijzing instellen die specifiek is voor de gegevens in de organisaties waartussen de entiteit wordt gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="1f898-195">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="1f898-196">In de volgende afbeeldingen ziet u een voorbeeld van de toewijzing van een sjabloon in gegevensintegrator.</span><span class="sxs-lookup"><span data-stu-id="1f898-196">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="orderheader"></a><span data-ttu-id="1f898-197">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="1f898-197">OrderHeader</span></span>

![Sjabloontoewijzing in gegevensintegrator](./media/sales-order-template-mapping-data-integrator-1.png)

![Sjabloontoewijzing in gegevensintegrator](./media/sales-order-template-mapping-data-integrator-2.png)

### <a name="orderline"></a><span data-ttu-id="1f898-200">OrderLine</span><span class="sxs-lookup"><span data-stu-id="1f898-200">OrderLine</span></span>

![Sjabloontoewijzing in gegevensintegrator](./media/sales-order-template-mapping-data-integrator-3.png)

![Sjabloontoewijzing in gegevensintegrator](./media/sales-order-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="1f898-203">Verwante onderwerpen</span><span class="sxs-lookup"><span data-stu-id="1f898-203">Related topics</span></span>

[<span data-ttu-id="1f898-204">Producten uit Finance and Operations synchroniseren met producten in Sales</span><span class="sxs-lookup"><span data-stu-id="1f898-204">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="1f898-205">Accounts in Sales synchroniseren met klanten in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1f898-205">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="1f898-206">Contactpersonen in Sales synchroniseren naar contactpersonen of klanten in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1f898-206">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="1f898-207">Kopteksten en regels in verkoopoffertes vanuit Sales synchroniseren naar Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1f898-207">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="1f898-208">Kopteksten en regels in verkoopfacturen synchroniseren vanuit Finance and Operations naar Sales</span><span class="sxs-lookup"><span data-stu-id="1f898-208">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)


