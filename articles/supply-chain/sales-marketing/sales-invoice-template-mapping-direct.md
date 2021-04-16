---
title: Kopteksten en regels in verkoopfacturen rechtstreeks synchroniseren vanuit Supply Chain Management naar Sales
description: In dit onderwerp worden de sjablonen en onderliggende taken besproken die worden gebruikt voor het rechtstreeks synchroniseren van kopteksten en regels van verkoopfacturen van Dynamics 365 Supply Chain Management naar Dynamics 365 Sales.
author: ChristianRytt
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 69f497ed8efff9aa18dedbce65d88e3b2d5168a6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839024"
---
# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="14193-103">Kopteksten en regels in verkoopfacturen rechtstreeks synchroniseren vanuit Finance and Operations naar Sales</span><span class="sxs-lookup"><span data-stu-id="14193-103">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14193-104">In dit onderwerp worden de sjablonen en onderliggende taken besproken die worden gebruikt voor het rechtstreeks synchroniseren van kopteksten en regels van verkoopfacturen van Dynamics 365 Supply Chain Management naar Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="14193-104">This topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines directly from Dynamics 365 Supply Chain Management to Dynamics 365 Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="14193-105">Gegevensstroom in Prospect naar contant geld</span><span class="sxs-lookup"><span data-stu-id="14193-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="14193-106">De oplossing Prospect naar contant geld gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Supply Chain Management en Sales.</span><span class="sxs-lookup"><span data-stu-id="14193-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="14193-107">De Prospect naar contant geld-sjablonen die beschikbaar zijn in de functie Gegevensintegratie activeren de stroom van gegevens over rekeningen, contactpersonen, producten, verkoopoffertes en verkoopfacturen tussen Supply Chain Management en Sales.</span><span class="sxs-lookup"><span data-stu-id="14193-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="14193-108">De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Supply Chain Management en Sales.</span><span class="sxs-lookup"><span data-stu-id="14193-108">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="14193-109">[![Gegevensstroom in Prospect naar contant geld](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="14193-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="14193-110">Sjablonen en taken</span><span class="sxs-lookup"><span data-stu-id="14193-110">Templates and tasks</span></span>

<span data-ttu-id="14193-111">Open het [Power Apps-beheercentrum](https://preview.admin.powerapps.com/dataintegration) om toegang te krijgen tot de beschikbare sjablonen.</span><span class="sxs-lookup"><span data-stu-id="14193-111">To access the available templates, open [Power Apps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="14193-112">Selecteer **Projecten** en selecteer vervolgens in de rechterbovenhoek de optie **Nieuw project** om openbare sjablonen te selecteren.</span><span class="sxs-lookup"><span data-stu-id="14193-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="14193-113">De volgende sjabloon en onderliggende taken worden gebruikt om kopteksten en regels van verkoopfacturen vanuit Supply Chain Management te synchroniseren met Sales:</span><span class="sxs-lookup"><span data-stu-id="14193-113">The following template and underlying tasks are used to synchronize sales invoice headers and lines from Supply Chain Management to Sales:</span></span>

- <span data-ttu-id="14193-114">**Naam van de sjabloon in Gegevensintegratie:** Verkoopfacturen (Fin and Ops naar Sales) - Direct</span><span class="sxs-lookup"><span data-stu-id="14193-114">**Name of the template in Data integration:** Sales Invoices (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="14193-115">**Namen van de taken in het project Gegevensintegratie:**</span><span class="sxs-lookup"><span data-stu-id="14193-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="14193-116">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="14193-116">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="14193-117">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="14193-117">SalesInvoiceLine</span></span>

<span data-ttu-id="14193-118">De volgende synchronisatietaken zijn vereist voordat de synchronisatie van de kopteksten en regels van verkoopfacturen kan plaatsvinden:</span><span class="sxs-lookup"><span data-stu-id="14193-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="14193-119">Producten (Supply Chain Management naar Sales) - Direct</span><span class="sxs-lookup"><span data-stu-id="14193-119">Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="14193-120">Rekeningen (Supply Chain Management naar Sales) - Direct (wanneer gebruikt)</span><span class="sxs-lookup"><span data-stu-id="14193-120">Accounts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="14193-121">Contacten (Sales naar Supply Chain Management) - Direct (wanneer gebruikt)</span><span class="sxs-lookup"><span data-stu-id="14193-121">Contacts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="14193-122">Kopteksten en regels in verkooporders (Supply Chain Management naar Sales) - Direct</span><span class="sxs-lookup"><span data-stu-id="14193-122">Sales order header and lines (Supply Chain Management to Sales) - Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="14193-123">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="14193-123">Entity set</span></span>

| <span data-ttu-id="14193-124">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="14193-124">Supply Chain Management</span></span>                              | <span data-ttu-id="14193-125">Verkoop</span><span class="sxs-lookup"><span data-stu-id="14193-125">Sales</span></span>          |
|------------------------------------------------------|----------------|
| <span data-ttu-id="14193-126">Extern onderhouden kopteksten van klantverkoopfacturen</span><span class="sxs-lookup"><span data-stu-id="14193-126">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="14193-127">Facturen</span><span class="sxs-lookup"><span data-stu-id="14193-127">Invoices</span></span>       |
| <span data-ttu-id="14193-128">Extern onderhouden klantverkoopfactuurregels</span><span class="sxs-lookup"><span data-stu-id="14193-128">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="14193-129">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="14193-129">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="14193-130">Entiteitstroom</span><span class="sxs-lookup"><span data-stu-id="14193-130">Entity flow</span></span>

<span data-ttu-id="14193-131">Verkoopoffertes worden gemaakt in Supply Chain Management en gesynchroniseerd met Sales.</span><span class="sxs-lookup"><span data-stu-id="14193-131">Sales invoices are created in Supply Chain Management and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="14193-132">Momenteel worden belastingen met betrekking tot toeslagen in de koptekst van de verkoopfactuur niet opgenomen bij de synchronisatie van Supply Chain Management naar Sales.</span><span class="sxs-lookup"><span data-stu-id="14193-132">Currently, tax that is related to charges on the sales invoice header isn't included in the synchronization from Supply Chain Managements to Sales.</span></span> <span data-ttu-id="14193-133">Sales biedt geen ondersteuning voor belastinggegevens op koptekstniveau.</span><span class="sxs-lookup"><span data-stu-id="14193-133">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="14193-134">Belastingen gerelateerd aan toeslagen op regelniveau worden echter wel opgenomen in de synchronisatie.</span><span class="sxs-lookup"><span data-stu-id="14193-134">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="14193-135">Oplossing Prospect naar contant geld voor Sales</span><span class="sxs-lookup"><span data-stu-id="14193-135">Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="14193-136">Het veld **Factuurnummer** is aan de entiteit **Factuur** toegevoegd en wordt weergegeven op de pagina.</span><span class="sxs-lookup"><span data-stu-id="14193-136">An **Invoice number** field has been added to the **Invoice** entity and appears on the page.</span></span>
- <span data-ttu-id="14193-137">De knop **Factuur maken** op de pagina **Verkooporder** is verborgen omdat facturen in Supply Chain Management worden gemaakt en worden gesynchroniseerd naar Sales.</span><span class="sxs-lookup"><span data-stu-id="14193-137">The **Create invoice** button on the **Sales order** page is hidden, because invoices will be created in Supply Chain Management and synchronized to Sales.</span></span> <span data-ttu-id="14193-138">De pagina **Factuur** kan niet worden bewerkt omdat facturen vanuit Supply Chain Management worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="14193-138">The **Invoice** page can't be edited, because invoices will be synchronized from Supply Chain Management.</span></span>
- <span data-ttu-id="14193-139">De waarde voor **Verkooporderstatus** wordt automatisch in **Gefactureerd** gewijzigd wanneer de bijbehorende factuur vanuit Supply Chain Management is gesynchroniseerd naar Sales.</span><span class="sxs-lookup"><span data-stu-id="14193-139">The **Sales order status** value is automatically changed to **Invoiced** when the related invoice from Supply Chain Management has been synchronized to Sales.</span></span> <span data-ttu-id="14193-140">Daarnaast wordt de eigenaar van de verkooporder op basis waarvan de factuur is gemaakt, aangewezen als de eigenaar van de factuur.</span><span class="sxs-lookup"><span data-stu-id="14193-140">Additionally, the owner of the sales order that the invoice was created from is assigned as the owner of the invoice.</span></span> <span data-ttu-id="14193-141">De eigenaar van de verkooporder kan de factuur dus weergeven.</span><span class="sxs-lookup"><span data-stu-id="14193-141">Therefore, the owner of the sales order can view the invoice.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="14193-142">Voorwaarden en instellingen voor toewijzing</span><span class="sxs-lookup"><span data-stu-id="14193-142">Preconditions and mapping setup</span></span>

<span data-ttu-id="14193-143">Voordat u verkoopfacturen synchroniseert, is het belangrijk de volgende instellingen in de systemen bij te werken.</span><span class="sxs-lookup"><span data-stu-id="14193-143">Before you synchronize sales invoices, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="14193-144">Instellingen in Sales</span><span class="sxs-lookup"><span data-stu-id="14193-144">Setup in Sales</span></span>

<span data-ttu-id="14193-145">Ga naar **Instellingen** > **Beheer** > **Systeeminstellingen** > **Sales** en zorg ervoor dat de volgende instellingen worden gebruikt:</span><span class="sxs-lookup"><span data-stu-id="14193-145">Go to **Settings** > **Administration** > **System settings** > **Sales**, and make sure that the following settings are used:</span></span>

- <span data-ttu-id="14193-146">De optie **Systeem voor berekenen van systeemprijzen gebruiken** is ingesteld op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="14193-146">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
- <span data-ttu-id="14193-147">Het veld **Berekeningsmethode korting** is ingesteld op **Regelartikel**.</span><span class="sxs-lookup"><span data-stu-id="14193-147">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="14193-148">Instellingen in het project Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="14193-148">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="14193-149">Taak SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="14193-149">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="14193-150">Zorg ervoor dat de vereiste toewijzing bestaat voor **InvoiceCountryRegionId** naar **BillingAddress\_Country**.</span><span class="sxs-lookup"><span data-stu-id="14193-150">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country**.</span></span>

    <span data-ttu-id="14193-151">De sjabloonwaarde is een toewijzingswaarde waarbij verschillende landen of regio's worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="14193-151">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="14193-152">Een prijslijst is vereist voor het maken van facturen in Sales.</span><span class="sxs-lookup"><span data-stu-id="14193-152">A price list is required in order to create invoices in Sales.</span></span> <span data-ttu-id="14193-153">Werk de waardetoewijzing voor **pricelevelid.name \[Price List Name\]** per valuta bij naar de gebruikte prijslijst in Sales.</span><span class="sxs-lookup"><span data-stu-id="14193-153">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="14193-154">U kunt de standaardprijslijst gebruiken voor één valuta.</span><span class="sxs-lookup"><span data-stu-id="14193-154">You can use the default price list for a single currency.</span></span> <span data-ttu-id="14193-155">Als u prijslijsten in meerdere valuta's hebt, kunt u een waardetoewijzing gebruiken.</span><span class="sxs-lookup"><span data-stu-id="14193-155">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="14193-156">De sjabloonwaarde voor **pricelevelid.name \[Prijs List Name\]** is een waardetoewijzing die is gebaseerd op valuta met USD = CRM Service USA (voorbeeld).</span><span class="sxs-lookup"><span data-stu-id="14193-156">The template value for **pricelevelid.name \[Price list name\]** is a value map that is based on currency with USD = CRM Service USA (sample).</span></span>  
    
#### <a name="salesinvoiceline-task"></a><span data-ttu-id="14193-157">Taak SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="14193-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="14193-158">Zorg ervoor dat de vereiste toewijzing bestaat voor **Maateenheid**.</span><span class="sxs-lookup"><span data-stu-id="14193-158">Make sure that the required mapping exists for **Unit of measure**.</span></span>
- <span data-ttu-id="14193-159">Zorg ervoor dat de vereiste waardetoewijzing voor **SalesUnitSymbol** in Supply Chain Management bestaat.</span><span class="sxs-lookup"><span data-stu-id="14193-159">Make sure that the required value map for **SalesUnitSymbol** in Supply Chain Management exists.</span></span>

    <span data-ttu-id="14193-160">Er wordt een sjabloonwaarde met een waardetoewijzing voor **SalesUnitSymbol** naar **Quantity\_UOM** gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="14193-160">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="14193-161">Sjabloontoewijzing in Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="14193-161">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="14193-162">De velden **Vetalingsvoorwaarden**, **Leveringscondities**, **Leveringsvoorwaarden**, **Verzendmethode** en **Leveringsmethode** maken geen deel uit van de standaardtoewijzingen.</span><span class="sxs-lookup"><span data-stu-id="14193-162">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="14193-163">Als u deze velden wilt toewijzen, moet u een waardetoewijzing instellen die specifiek is voor de gegevens in de organisaties waartussen de entiteit wordt gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="14193-163">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="14193-164">In de volgende afbeeldingen ziet u een voorbeeld van sjabloontoewijzing in Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="14193-164">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="14193-165">Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Sales naar Supply Chain Management worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="14193-165">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

### <a name="salesinvoiceheader"></a><span data-ttu-id="14193-166">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="14193-166">SalesInvoiceHeader</span></span>

![Sjabloontoewijzing in Gegevensintegratie](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a><span data-ttu-id="14193-168">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="14193-168">SalesInvoiceLine</span></span>

![Sjabloontoewijzing in Gegevensintegratie](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="14193-170">Verwante onderwerpen</span><span class="sxs-lookup"><span data-stu-id="14193-170">Related topics</span></span>

[<span data-ttu-id="14193-171">Van prospect naar contant geld</span><span class="sxs-lookup"><span data-stu-id="14193-171">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="14193-172">Rekeningen rechtstreeks vanuit Sales synchroniseren met klanten in Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="14193-172">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="14193-173">Producten rechtstreeks vanuit Supply Chain Management synchroniseren met producten in Sales</span><span class="sxs-lookup"><span data-stu-id="14193-173">Synchronize products directly from Supply Chain Management to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="14193-174">Contactpersonen in Sales rechtstreeks synchroniseren met contactpersonen of klanten in Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="14193-174">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="14193-175">Verkooporders rechtstreeks tussen Sales en Supply Chain Management synchroniseren</span><span class="sxs-lookup"><span data-stu-id="14193-175">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]