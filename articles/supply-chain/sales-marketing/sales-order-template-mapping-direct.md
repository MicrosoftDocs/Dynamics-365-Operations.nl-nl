---
title: Kopteksten en regels in verkooporders direct vanuit Finance and Operations synchroniseren naar Sales
description: In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het direct synchroniseren van kopteksten en regels van verkooporders vanuit Microsoft Dynamics 365 for Finance and Operations, Enterprise edition naar Microsoft Dynamics 365 for Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: cc0be50552ae680ba5291e72b7c482ee67e1e70e
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="5675c-103">Kopteksten en regels in verkooporders direct vanuit Finance and Operations synchroniseren naar Sales</span><span class="sxs-lookup"><span data-stu-id="5675c-103">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5675c-104">In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het direct synchroniseren van kopteksten en regels van verkooporders vanuit Microsoft Dynamics 365 for Finance and Operations, Enterprise edition naar Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="5675c-104">This topic discusses the templates and underlying tasks that are used to synchronize sales order headers and lines directly from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="5675c-105">Gegevensstroom in Prospect naar contant geld</span><span class="sxs-lookup"><span data-stu-id="5675c-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="5675c-106">De oplossing Prospect naar contant geld gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Finance and Operations en Sales.</span><span class="sxs-lookup"><span data-stu-id="5675c-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="5675c-107">De Prospect naar contant geld-sjablonen die beschikbaar zijn in de functie Gegevensintegratie activeren de stroom van gegevens over rekeningen, contactpersonen, producten, verkoopoffertes en verkoopfacturen tussen Finance and Operations en Sales.</span><span class="sxs-lookup"><span data-stu-id="5675c-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="5675c-108">De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Finance and Operations en Sales.</span><span class="sxs-lookup"><span data-stu-id="5675c-108">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="5675c-109">[![Gegevensstroom in Prospect naar contant geld](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="5675c-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="5675c-110">Sjablonen en taken</span><span class="sxs-lookup"><span data-stu-id="5675c-110">Templates and tasks</span></span>

<span data-ttu-id="5675c-111">Open het [PowerApps-beheercentrum](https://preview.admin.powerapps.com/dataintegration) om toegang te krijgen tot de beschikbare sjablonen.</span><span class="sxs-lookup"><span data-stu-id="5675c-111">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="5675c-112">Selecteer **Projecten** en selecteer vervolgens in de rechterbovenhoek de optie **Nieuw project** om openbare sjablonen te selecteren.</span><span class="sxs-lookup"><span data-stu-id="5675c-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="5675c-113">De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van de kopteksten en regels van verkooporders vanuit Finance and Operations naar Sales:</span><span class="sxs-lookup"><span data-stu-id="5675c-113">The following template and underlying tasks are used to synchronize sales order headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="5675c-114">**Naam van de sjabloon in Gegevensintegratie:** Verkooporders (Fin and Ops naar Sales) - Direct</span><span class="sxs-lookup"><span data-stu-id="5675c-114">**Name of the template in Data integration:** Sales Orders (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="5675c-115">**Namen van de taken in het project Gegevensintegratie:**</span><span class="sxs-lookup"><span data-stu-id="5675c-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="5675c-116">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="5675c-116">OrderHeader</span></span>
    - <span data-ttu-id="5675c-117">OrderLine</span><span class="sxs-lookup"><span data-stu-id="5675c-117">OrderLine</span></span>

<span data-ttu-id="5675c-118">De volgende synchronisatietaken zijn vereist voordat de synchronisatie van de kopteksten en regels van verkoopfacturen kan plaatsvinden:</span><span class="sxs-lookup"><span data-stu-id="5675c-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="5675c-119">Producten (Fin and Ops naar Sales) - Direct</span><span class="sxs-lookup"><span data-stu-id="5675c-119">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="5675c-120">Rekeningen (Sales naar Fin and Ops) - Direct (indien gebruikt)</span><span class="sxs-lookup"><span data-stu-id="5675c-120">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="5675c-121">Contactpersonen naar klanten (Sales naar Fin and Ops) - Direct (indien gebruikt)</span><span class="sxs-lookup"><span data-stu-id="5675c-121">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="5675c-122">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="5675c-122">Entity set</span></span>

| <span data-ttu-id="5675c-123">Finance en Operations</span><span class="sxs-lookup"><span data-stu-id="5675c-123">Finance and Operations</span></span>  | <span data-ttu-id="5675c-124">Verkoop</span><span class="sxs-lookup"><span data-stu-id="5675c-124">Sales</span></span>             |
|-------------------------|-------------------|
| <span data-ttu-id="5675c-125">CDS-verkooporderkoppen</span><span class="sxs-lookup"><span data-stu-id="5675c-125">CDS sales order headers</span></span> | <span data-ttu-id="5675c-126">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="5675c-126">SalesOrders</span></span>       |
| <span data-ttu-id="5675c-127">CDS-verkooporderregels</span><span class="sxs-lookup"><span data-stu-id="5675c-127">CDS sales order lines</span></span>   | <span data-ttu-id="5675c-128">SalesOrderDetails</span><span class="sxs-lookup"><span data-stu-id="5675c-128">SalesOrderDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="5675c-129">Entiteitstroom</span><span class="sxs-lookup"><span data-stu-id="5675c-129">Entity flow</span></span>

<span data-ttu-id="5675c-130">Verkooporders worden gemaakt in Finance and Operations en gesynchroniseerd met Sales.</span><span class="sxs-lookup"><span data-stu-id="5675c-130">Sales orders are created in Finance and Operations and synchronized to Sales.</span></span>

<span data-ttu-id="5675c-131">Filters in de sjabloon zorgen ervoor dat alleen relevante verkooporders worden opgenomen in de synchronisatie:</span><span class="sxs-lookup"><span data-stu-id="5675c-131">Filters in the template help guarantee that only relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="5675c-132">Als zowel de bestellende als de facturerende klant op de verkooporder uit Sales afkomstig is, worden beide opgenomen in de synchronisatie.</span><span class="sxs-lookup"><span data-stu-id="5675c-132">On the sales order, both the ordering customer and the invoicing customer that originate from Sales will be included in the synchronization.</span></span> <span data-ttu-id="5675c-133">In Finance and Operations worden de velden **OrderingCustomerIsExternallyMaintained** en **InvoiceCustomerIsExternallyMaintained** gebruikt om de synchronisatie in de gegevensentiteiten bij te houden.</span><span class="sxs-lookup"><span data-stu-id="5675c-133">In Finance and Operations, the **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** fields are used to track the synchronization in the data entities.</span></span>
- <span data-ttu-id="5675c-134">De verkooporder in Finance and Operations moet worden bevestigd.</span><span class="sxs-lookup"><span data-stu-id="5675c-134">The sales order in Finance and Operations must be confirmed.</span></span> <span data-ttu-id="5675c-135">Alleen bevestigde verkooporders of verkooporders met een hogere verwerkingsstatus, bijvoorbeeld met de status **Verzonden** of **Gefactureerd**, worden gesynchroniseerd naar Sales.</span><span class="sxs-lookup"><span data-stu-id="5675c-135">Only confirmed sales orders or sales orders that have a higher processing status, such as **Shipped** or **Invoiced**, are synchronized to Sales.</span></span>
- <span data-ttu-id="5675c-136">Na het maken of wijzigen van een verkooporder moet de batchtaak **Verkooptotalen berekenen** in Finance and Operations worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="5675c-136">After a sales order is created or modified, the **Calculate sales totals** batch job in Finance and Operations must be run.</span></span> <span data-ttu-id="5675c-137">Alleen verkooporders waarvoor verkooptotalen zijn berekend, worden gesynchroniseerd naar Sales.</span><span class="sxs-lookup"><span data-stu-id="5675c-137">Only sales orders where sales totals are calculated will be synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="5675c-138">Momenteel worden belastingen met betrekking tot toeslagen in de koptekst van de verkooporder niet opgenomen bij de synchronisatie van Finance and Operations naar Sales.</span><span class="sxs-lookup"><span data-stu-id="5675c-138">Currently, tax that is related to charges on the sales order header isn't included in the synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="5675c-139">Sales biedt geen ondersteuning voor belastinggegevens op koptekstniveau.</span><span class="sxs-lookup"><span data-stu-id="5675c-139">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="5675c-140">Belastingen gerelateerd aan toeslagen op regelniveau worden echter wel opgenomen in de synchronisatie.</span><span class="sxs-lookup"><span data-stu-id="5675c-140">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="5675c-141">Oplossing Prospect naar contant geld voor Sales</span><span class="sxs-lookup"><span data-stu-id="5675c-141">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="5675c-142">Nieuwe velden zijn toegevoegd aan de entiteit **Order** en worden weergegeven op de pagina:</span><span class="sxs-lookup"><span data-stu-id="5675c-142">New fields have been added to the **Order** entity and appear on the page:</span></span>

- <span data-ttu-id="5675c-143">**Wordt extern beheerd**: stel deze optie in op **Ja** wanneer de order afkomstig is uit Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5675c-143">**Is Maintained Externally** – Set this option to **Yes** when the order is coming from Finance and Operations.</span></span>
- <span data-ttu-id="5675c-144">**Verwerkingsstatus**: in dit veld wordt de verwerkingsstatus weergegeven van de order in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5675c-144">**Processing status** – This field shows the processing status of the order in Finance and Operations.</span></span> <span data-ttu-id="5675c-145">De volgende waarden zijn beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="5675c-145">The following values are available:</span></span>

    - <span data-ttu-id="5675c-146">Actief</span><span class="sxs-lookup"><span data-stu-id="5675c-146">Active</span></span>
    - <span data-ttu-id="5675c-147">Bevestigd</span><span class="sxs-lookup"><span data-stu-id="5675c-147">Confirmed</span></span>
    - <span data-ttu-id="5675c-148">Pakbon</span><span class="sxs-lookup"><span data-stu-id="5675c-148">Packing Slip</span></span>
    - <span data-ttu-id="5675c-149">Gefactureerd</span><span class="sxs-lookup"><span data-stu-id="5675c-149">Invoiced</span></span>
    - <span data-ttu-id="5675c-150">Opgenomen</span><span class="sxs-lookup"><span data-stu-id="5675c-150">Picked</span></span>
    - <span data-ttu-id="5675c-151">Gedeeltelijk opgenomen</span><span class="sxs-lookup"><span data-stu-id="5675c-151">Partially Picked</span></span>
    - <span data-ttu-id="5675c-152">Gedeeltelijk ingepakt</span><span class="sxs-lookup"><span data-stu-id="5675c-152">Partially Packed</span></span>
    - <span data-ttu-id="5675c-153">Verzonden</span><span class="sxs-lookup"><span data-stu-id="5675c-153">Shipped</span></span>
    - <span data-ttu-id="5675c-154">Gedeeltelijk verzonden</span><span class="sxs-lookup"><span data-stu-id="5675c-154">Partially Shipped</span></span>
    - <span data-ttu-id="5675c-155">Gedeeltelijk gefactureerd</span><span class="sxs-lookup"><span data-stu-id="5675c-155">Partially Invoiced</span></span>
    - <span data-ttu-id="5675c-156">Geannuleerd</span><span class="sxs-lookup"><span data-stu-id="5675c-156">Cancelled</span></span>

<span data-ttu-id="5675c-157">De instelling **Heeft alleen extern onderhouden producten** wordt gebruikt in andere verkooporderscenario's (bijvoorbeeld voor de synchronisatie van Sales naar Finance and Operations) om consequent bij te houden of een verkooporder geheel uit extern onderhouden producten bestaat.</span><span class="sxs-lookup"><span data-stu-id="5675c-157">The **Has Externally Maintained Products Only** setting is used in other sales order scenarios (for example, synchronization from Sales to Finance and Operation) to consistently track whether a sales order consists entirely of externally maintained products.</span></span> <span data-ttu-id="5675c-158">Als een verkooporder alleen uit extern beheerde producten bestaat, worden de producten beheerd in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5675c-158">If a sales order consists entirely of externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="5675c-159">Met deze instelling garandeert u dat u geen verkooporderregels probeert te synchroniseren die producten bevatten die onbekend zijn in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5675c-159">This setting helps guarantee that you don't try to synchronize sales order lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="5675c-160">Voor extern beheerde orders zijn de knoppen **Factuur maken**, **Order annuleren**, **Opnieuw berekenen**, **Producten ophalen** en **Adres opzoeken** op de pagina **Verkooporder** verborgen omdat facturen worden gemaakt in Finance and Operations en vervolgens worden gesynchroniseerd naar Sales.</span><span class="sxs-lookup"><span data-stu-id="5675c-160">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products**, and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders, because invoices will be created in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="5675c-161">De bestelpagina kan niet worden bewerkt omdat verkoopordergegevens vanuit Finance and Operations worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="5675c-161">The order page can't be edited, because sales order information will be synchronized from Finance and Operations.</span></span>

<span data-ttu-id="5675c-162">De status van een verkooporder blijft **Actief** om ervoor te zorgen dat wijzigingen vanuit Finance and Operations naar de verkooporder in Sales kunnen stromen.</span><span class="sxs-lookup"><span data-stu-id="5675c-162">The status of a sales order will remain **Active** to help guarantee that changes from Finance and Operations can flow to the sales order in Sales.</span></span> <span data-ttu-id="5675c-163">U stelt dit gedrag in door de standaardwaarde voor **Statuscode \[Status\]** op **Actief** in te stellen in het project Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="5675c-163">To control this behavior, set the default **Statecode \[Status\]** value to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="5675c-164">Voorwaarden en instellingen voor toewijzing</span><span class="sxs-lookup"><span data-stu-id="5675c-164">Preconditions and mapping setup</span></span>

<span data-ttu-id="5675c-165">Voordat u verkooporders synchroniseert, is het belangrijk de volgende instellingen in de systemen bij te werken.</span><span class="sxs-lookup"><span data-stu-id="5675c-165">Before you synchronize sales orders, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="5675c-166">Instellingen in Sales</span><span class="sxs-lookup"><span data-stu-id="5675c-166">Setup in Sales</span></span>

- <span data-ttu-id="5675c-167">Zorg ervoor dat er machtigingen zijn ingesteld voor het team waaraan de gebruiker uit uw verbindingsset in Sales is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="5675c-167">Make sure that permissions are set up for the team that the user from your Sales connection set is assigned to.</span></span> <span data-ttu-id="5675c-168">Als u voorbeeldgegevens gebruikt, heeft de gebruiker meestal beheerderstoegang, maar het team niet.</span><span class="sxs-lookup"><span data-stu-id="5675c-168">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="5675c-169">Als het team niet ook beheerderstoegang heeft wanneer u het project uitvoert vanuit Gegevensintegratie, wordt een foutbericht weergegeven waarin wordt aangegeven dat het hoofdteam ontbreekt.</span><span class="sxs-lookup"><span data-stu-id="5675c-169">If the team doesn't also have admin access, when you run the project from Data integration, you will receive an error message that states that Principal team is missing.</span></span>

    <span data-ttu-id="5675c-170">Ga naar **Instellingen** > **Beveiliging** > **Teams**, selecteer het relevante team, selecteer **Rollen beheren** en selecteer een rol met de gewenste machtigingen, bijvoorbeeld **Systeembeheerder**.</span><span class="sxs-lookup"><span data-stu-id="5675c-170">Go to **Settings** > **Security** > **Teams**, select the relevant team, select **Manage Roles**, and select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="5675c-171">Ga naar **Instellingen** > **Beheer** > **Systeeminstellingen** > **Sales** en zorg ervoor dat de volgende instellingen worden gebruikt:</span><span class="sxs-lookup"><span data-stu-id="5675c-171">Go to **Settings** > **Administration** > **System settings** > **Sales**, and makes sure that the following settings are used:</span></span>

    - <span data-ttu-id="5675c-172">De optie **Systeem voor berekenen van systeemprijzen gebruiken** is ingesteld op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="5675c-172">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="5675c-173">Het veld **Berekeningsmethode korting** is ingesteld op **Regelartikel**.</span><span class="sxs-lookup"><span data-stu-id="5675c-173">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="5675c-174">Instellingen In Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5675c-174">Setup in Finance and Operations</span></span>

<span data-ttu-id="5675c-175">Ga naar **Verkoopbeheer en marketing** > **Periodieke taken** > **Verkooptotalen berekenen** en stel de taak zo in dat deze wordt uitgevoerd als batchtaak.</span><span class="sxs-lookup"><span data-stu-id="5675c-175">Go to **Sales and marketing** > **Periodic tasks** > **Calculate sales totals**, and set the job to run as a batch job.</span></span> <span data-ttu-id="5675c-176">Stel de optie **Totalen berekenen voor verkooporders** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="5675c-176">Set the **Calculate totals for sales orders** option to **Yes**.</span></span> <span data-ttu-id="5675c-177">Deze stap is belangrijk omdat alleen verkooporders waarvoor verkooptotalen zijn berekend, worden gesynchroniseerd naar Sales.</span><span class="sxs-lookup"><span data-stu-id="5675c-177">This step is important, because only sales orders where sales totals are calculated will be synchronized to Sales.</span></span> <span data-ttu-id="5675c-178">De frequentie van de batchtaak moet worden uitgelijnd met de frequentie van de verkoopordersynchronisatie.</span><span class="sxs-lookup"><span data-stu-id="5675c-178">The frequency of the batch job should be aligned with the frequency of sales order synchronization.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="5675c-179">Instellingen in het project Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="5675c-179">Setup in the Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="5675c-180">Taak SalesHeader</span><span class="sxs-lookup"><span data-stu-id="5675c-180">SalesHeader task</span></span>

- <span data-ttu-id="5675c-181">Zorg ervoor dat de vereiste toewijzing bestaat voor **InvoiceCountryRegionId** naar **BillingAddress\_Country** en voor **DeliveryCountryRegionId** naar **DeliveryAddress\_Country**.</span><span class="sxs-lookup"><span data-stu-id="5675c-181">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country** and for **DeliveryCountryRegionId** to **DeliveryAddress\_Country**.</span></span>

    <span data-ttu-id="5675c-182">De sjabloonwaarde is een toewijzingswaarde waarbij verschillende landen of regio's worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="5675c-182">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="5675c-183">Een prijslijst is vereist voor het maken van orders in Sales.</span><span class="sxs-lookup"><span data-stu-id="5675c-183">A price list is required in order to create orders in Sales.</span></span> <span data-ttu-id="5675c-184">Werk de waardetoewijzing voor **pricelevelid.name \[Price List Name\]** per valuta bij naar de gebruikte prijslijst in Sales.</span><span class="sxs-lookup"><span data-stu-id="5675c-184">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="5675c-185">U kunt de standaardprijslijst gebruiken voor één valuta.</span><span class="sxs-lookup"><span data-stu-id="5675c-185">You can use the default price list for a single currency.</span></span> <span data-ttu-id="5675c-186">Als u prijslijsten in meerdere valuta's hebt, kunt u een waardetoewijzing gebruiken.</span><span class="sxs-lookup"><span data-stu-id="5675c-186">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="5675c-187">De standaardsjabloonwaarde van de sjabloon voor **pricelevelid.name \[Price List Name\]** is **CRM Service USA (voorbeeld)**.</span><span class="sxs-lookup"><span data-stu-id="5675c-187">The default template value for **pricelevelid.name \[Price list name\]** is **CRM Service USA (sample)**.</span></span>

#### <a name="salesline-task"></a><span data-ttu-id="5675c-188">Taak SalesLine</span><span class="sxs-lookup"><span data-stu-id="5675c-188">SalesLine task</span></span>

- <span data-ttu-id="5675c-189">Zorg ervoor dat de vereiste toewijzing bestaat voor **DeliveryCountryRegionId** naar **DeliveryAddress\_Country**.</span><span class="sxs-lookup"><span data-stu-id="5675c-189">Make sure that the required mapping exists for **DeliveryCountryRegionId** to **DeliveryAddress\_Country**.</span></span>

    <span data-ttu-id="5675c-190">De sjabloonwaarde is een toewijzingswaarde waarbij verschillende landen of regio's worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="5675c-190">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="5675c-191">Zorg ervoor dat de vereiste waardetoewijzing voor **SalesUnitSymbol** in Finance and Operations bestaat.</span><span class="sxs-lookup"><span data-stu-id="5675c-191">Make sure that the required value map for **SalesUnitSymbol** in Finance and Operations exists.</span></span>

    <span data-ttu-id="5675c-192">Er wordt een sjabloonwaarde met een waardetoewijzing voor **SalesUnitSymbol** naar **Quantity\_UOM** gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="5675c-192">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="5675c-193">Sjabloontoewijzing in Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="5675c-193">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="5675c-194">De velden **Vetalingsvoorwaarden**, **Leveringscondities**, **Leveringsvoorwaarden**, **Verzendmethode** en **Leveringsmethode** maken geen deel uit van de standaardtoewijzingen.</span><span class="sxs-lookup"><span data-stu-id="5675c-194">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="5675c-195">Als u deze velden wilt toewijzen, moet u een waardetoewijzing instellen die specifiek is voor de gegevens in de organisaties waartussen de entiteit wordt gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="5675c-195">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="5675c-196">In de volgende afbeeldingen ziet u een voorbeeld van sjabloontoewijzing in Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="5675c-196">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="5675c-197">Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Sales naar Finance and Operations worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="5675c-197">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="orderheader"></a><span data-ttu-id="5675c-198">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="5675c-198">OrderHeader</span></span>

![Sjabloontoewijzing in Gegevensintegrator](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="orderline"></a><span data-ttu-id="5675c-200">OrderLine</span><span class="sxs-lookup"><span data-stu-id="5675c-200">OrderLine</span></span>

![Sjabloontoewijzing in Gegevensintegrator](./media/sales-order-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="5675c-202">Verwante onderwerpen</span><span class="sxs-lookup"><span data-stu-id="5675c-202">Related topics</span></span>

[<span data-ttu-id="5675c-203">Prospect naar contant geld</span><span class="sxs-lookup"><span data-stu-id="5675c-203">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="5675c-204">Rekeningen in Sales direct synchroniseren naar klanten in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5675c-204">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="5675c-205">Producten vanuit Finance and Operations direct synchroniseren met producten in Sales</span><span class="sxs-lookup"><span data-stu-id="5675c-205">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="5675c-206">Contactpersonen vanuit Sales direct synchroniseren naar contactpersonen of klanten in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5675c-206">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="5675c-207">Kopteksten en regels in verkoopfacturen direct vanuit Finance and Operations synchroniseren naar Sales</span><span class="sxs-lookup"><span data-stu-id="5675c-207">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)




