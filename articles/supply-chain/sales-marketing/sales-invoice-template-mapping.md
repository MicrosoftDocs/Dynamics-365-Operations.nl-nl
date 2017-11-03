---
title: Kopteksten en regels in verkoopfacturen synchroniseren vanuit Finance and Operations naar Sales
description: In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van kopteksten en regels van verkoopfacturen tussen Microsoft Dynamics 365 for Finance and Operations, Enterprise edition en Microsoft Dynamics 365 for Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
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
ms.openlocfilehash: 22ab02555dcac850b18aac9564af41d6c627eade
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-invoice-headers-and-lines-from-finance-and-operations-to-sales"></a><span data-ttu-id="e2635-103">Kopteksten en regels in verkoopfacturen synchroniseren vanuit Finance and Operations naar Sales</span><span class="sxs-lookup"><span data-stu-id="e2635-103">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e2635-104">In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van kopteksten en regels van verkoopfacturen tussen Microsoft Dynamics 365 for Finance and Operations, Enterprise edition en Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="e2635-104">The topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="e2635-105">Sjablonen en taken</span><span class="sxs-lookup"><span data-stu-id="e2635-105">Templates and tasks</span></span>

<span data-ttu-id="e2635-106">De volgende sjablonen en onderliggende taken worden gebruikt voor het synchroniseren van de kopteksten en regels van verkoopfacturen tussen Finance and Operations en Sales:</span><span class="sxs-lookup"><span data-stu-id="e2635-106">The following templates and underlying tasks are used to synchronize sales invoice headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="e2635-107">**Naam van de sjabloon in Gegevensintegratie**</span><span class="sxs-lookup"><span data-stu-id="e2635-107">**Name of the template in Data integration**</span></span> 

     - <span data-ttu-id="e2635-108">Verkoopfacturen (Fin en Ops naar Sales)</span><span class="sxs-lookup"><span data-stu-id="e2635-108">Sales Invoices (Fin and Ops to Sales)</span></span>

- <span data-ttu-id="e2635-109">**Namen van de taken in het project Gegevensintegratie**</span><span class="sxs-lookup"><span data-stu-id="e2635-109">**Names of the tasks in the Data integration project**</span></span>

    - <span data-ttu-id="e2635-110">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="e2635-110">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="e2635-111">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="e2635-111">SalesInvoiceLine</span></span>

<span data-ttu-id="e2635-112">Taken die nodig zijn voor het synchroniseren van koptekst en regels van verkoopfacturen:</span><span class="sxs-lookup"><span data-stu-id="e2635-112">Sync tasks required prior to Sales invoice header and lines synchronization:</span></span>
-   <span data-ttu-id="e2635-113">Producten (Fin en Ops naar Sales)</span><span class="sxs-lookup"><span data-stu-id="e2635-113">Products (Fin and Ops to Sales)</span></span>
-   <span data-ttu-id="e2635-114">Rekeningen (Sales naar Fin and Ops) (indien gebruikt)</span><span class="sxs-lookup"><span data-stu-id="e2635-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
-   <span data-ttu-id="e2635-115">Contactpersonen (Sales naar Fin and Ops) (indien gebruikt)</span><span class="sxs-lookup"><span data-stu-id="e2635-115">Contacts (Sales to Fin and Ops) (if used)</span></span>
-   <span data-ttu-id="e2635-116">Koptekst en regels van verkooporder (Fin and Ops naar Sales)</span><span class="sxs-lookup"><span data-stu-id="e2635-116">Sales order header and lines (Fin and Ops to Sales)</span></span>

## <a name="entity-set"></a><span data-ttu-id="e2635-117">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="e2635-117">Entity set</span></span>

| <span data-ttu-id="e2635-118">Finance en Operations</span><span class="sxs-lookup"><span data-stu-id="e2635-118">Finance and Operations</span></span>                               | <span data-ttu-id="e2635-119">Common Data Service (CDS)</span><span class="sxs-lookup"><span data-stu-id="e2635-119">Common Data Service (CDS)</span></span>              | <span data-ttu-id="e2635-120">Verkoop</span><span class="sxs-lookup"><span data-stu-id="e2635-120">Sales</span></span>          |
|------------------------------------------------------|------------------|----------------|
| <span data-ttu-id="e2635-121">Extern onderhouden kopteksten van klantverkoopfacturen</span><span class="sxs-lookup"><span data-stu-id="e2635-121">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="e2635-122">SalesInvoice</span><span class="sxs-lookup"><span data-stu-id="e2635-122">SalesInvoice</span></span>     | <span data-ttu-id="e2635-123">Facturen</span><span class="sxs-lookup"><span data-stu-id="e2635-123">Invoices</span></span>       |
| <span data-ttu-id="e2635-124">Extern onderhouden klantverkoopfactuurregels</span><span class="sxs-lookup"><span data-stu-id="e2635-124">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="e2635-125">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="e2635-125">SalesInvoiceLine</span></span> | <span data-ttu-id="e2635-126">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="e2635-126">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="e2635-127">Entiteitstroom</span><span class="sxs-lookup"><span data-stu-id="e2635-127">Entity flow</span></span>

<span data-ttu-id="e2635-128">Verkoopfacturen worden gemaakt in Finance and Operations en gesynchroniseerd met Sales.</span><span class="sxs-lookup"><span data-stu-id="e2635-128">Sales invoices are created in Finance and Operations and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="e2635-129">Belastingen met betrekking tot toeslagen in de **koptekst van de verkoopfactuur** worden niet opgenomen bij de synchronisatie van Finance and Operations met Sales.</span><span class="sxs-lookup"><span data-stu-id="e2635-129">Tax related to charges on the **Sales invoice header** is currently not included in synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="e2635-130">Sales biedt namelijk geen ondersteuning voor belastinggegevens op koptekstniveau.</span><span class="sxs-lookup"><span data-stu-id="e2635-130">This is because Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="e2635-131">Belastingen met betrekking tot kosten op het regelniveau worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="e2635-131">Tax related to charges at the line level is included.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="e2635-132">Oplossing Prospect naar contant geld voor Sales</span><span class="sxs-lookup"><span data-stu-id="e2635-132">Prospect to cash solution for Sales</span></span>

-  <span data-ttu-id="e2635-133">Het veld **Factuurnummer** wordt aan de entiteit **Factuur** toegevoegd en weergegeven op de pagina.</span><span class="sxs-lookup"><span data-stu-id="e2635-133">An **Invoice number field** is added to the **Invoice** entity and displayed on the page.</span></span>
 
-  <span data-ttu-id="e2635-134">De knop **Factuur maken** op de pagina **Verkooporder** is verborgen omdat de facturen in Finance and Operations worden gemaakt en worden gesynchroniseerd met Sales.</span><span class="sxs-lookup"><span data-stu-id="e2635-134">The **Create invoice** button on the **Sales order** page is hidden because invoices will be created in Finance and Operations and synced to Sales.</span></span> <span data-ttu-id="e2635-135">De pagina **Factuur** kan niet worden bewerkt omdat facturen vanuit Finance and Operations worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="e2635-135">The **Invoice** page is non-editable because invoices will be synced from Finance and Operations.</span></span>
 
-  <span data-ttu-id="e2635-136">De **verkooporderstatus** wordt automatisch in **Gefactureerd** gewijzigd wanneer de bijbehorende factuur vanuit Finance and Operations is gesynchroniseerd met Sales.</span><span class="sxs-lookup"><span data-stu-id="e2635-136">The **Sales order status** changes automatically to **Invoiced** when the related invoice from Finance and Operations has been  synchronized to Sales.</span></span> <span data-ttu-id="e2635-137">Daarnaast wordt de eigenaar van de verkooporder op basis waarvan de factuur is gemaakt aangewezen als de eigenaar van de factuur.</span><span class="sxs-lookup"><span data-stu-id="e2635-137">Also, the owner of the sales order from which the invoice was created is assigned as the owner of the invoice.</span></span> <span data-ttu-id="e2635-138">Zo kan de eigenaar van de verkooporder de factuur weergeven.</span><span class="sxs-lookup"><span data-stu-id="e2635-138">This gives the owner of the sales order the ability to view the invoice.</span></span>
 
## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="e2635-139">Voorwaarden en instellingen voor toewijzing</span><span class="sxs-lookup"><span data-stu-id="e2635-139">Preconditions and mapping setup</span></span>

<span data-ttu-id="e2635-140">Voordat u verkoopfacturen synchroniseert, is het belangrijk de systemen bij te werken met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="e2635-140">Before synchronizing sales invoices, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="e2635-141">Instellingen in Sales</span><span class="sxs-lookup"><span data-stu-id="e2635-141">Setup in Sales</span></span>

- <span data-ttu-id="e2635-142">Controleer of onder **Instellingen** > **Beheer** > **Systeeminstellingen** > **Sales** de optie **Systeem voor berekenen van systeemprijzen gebruiken** is ingesteld op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e2635-142">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Use system prizing calculation system** is set to **Yes**.</span></span> 

- <span data-ttu-id="e2635-143">Controleer of onder **Instellingen** > **Beheer** > **Systeeminstellingen** > **Sales** de optie **Berekeningsmethode korting** is ingesteld op **Regelartikel**.</span><span class="sxs-lookup"><span data-stu-id="e2635-143">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Discount calculation method** is set to **Line item**.</span></span> 

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="e2635-144">Instellingen in het project Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="e2635-144">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="e2635-145">Taak SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="e2635-145">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="e2635-146">Werk de toewijzing voor **CDS-organisatie-id** bij in **Bron** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="e2635-146">Update the mapping for **CDS Organization ID** in **Source** > **CDS**.</span></span> 

    -  <span data-ttu-id="e2635-147">De standaardsjabloonwaarde voor **SalesOrder_Organization_OrganizationId** is ORG001.</span><span class="sxs-lookup"><span data-stu-id="e2635-147">Default template value for **SalesOrder_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="e2635-148">De standaardsjabloonwaarde voor **Account_Organization_OrganizationId** is ORG001.</span><span class="sxs-lookup"><span data-stu-id="e2635-148">Default template value for **Account_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="e2635-149">De standaardsjabloonwaarde voor **Organization_OrganizationId** is ORG001.</span><span class="sxs-lookup"><span data-stu-id="e2635-149">Default template value for **Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="e2635-150">Zorg ervoor dat de benodigde toewijzing aanwezig is in **Bron** > **CDS voor InvoiceCountryRegionId** tot **BillingAddress_Country**.</span><span class="sxs-lookup"><span data-stu-id="e2635-150">Ensure that the needed mapping exists in **Source** > **CDS for InvoiceCountryRegionId** to **BillingAddress_Country**.</span></span>

    -  <span data-ttu-id="e2635-151">De waarde van de sjabloon is **ValueMap** met een aantal landen die zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="e2635-151">Template value is **ValueMap** with a number of countries mapped.</span></span>

- <span data-ttu-id="e2635-152">**Prijslijst** is vereist voor het maken van facturen in Sales.</span><span class="sxs-lookup"><span data-stu-id="e2635-152">**Price list** is required to create invoices in Sales.</span></span> <span data-ttu-id="e2635-153">Werk **ValueMap** in **CDS** > **Bestemming voor pricelevelid.name [Price List Name]** per valuta bij naar de gebruikte **prijslijst** in Sales.</span><span class="sxs-lookup"><span data-stu-id="e2635-153">Update the **ValueMap** in **CDS** > **Destination for pricelevelid.name [Price List Name]** to the **Price list** used in Sales per currency.</span></span> <span data-ttu-id="e2635-154">U kunt de standaard **prijslijst** voor één valuta of **ValueMap** gebruiken als u **prijslijsten** in meerdere valuta's hebt.</span><span class="sxs-lookup"><span data-stu-id="e2635-154">You can either use the default **Price list** for single currency or use **ValueMap** if you have **Price lists** in multiple currencies.</span></span>

    -  <span data-ttu-id="e2635-155">De waarde van de sjabloon voor **pricelevelid.name [Price List Name]** is **ValueMap** op basis van **Valuta**.</span><span class="sxs-lookup"><span data-stu-id="e2635-155">Template value for **pricelevelid.name [Price List Name]** is **ValueMap** based on **Currency**.</span></span>
    -  <span data-ttu-id="e2635-156">usd: CRM Service USA (voorbeeld).</span><span class="sxs-lookup"><span data-stu-id="e2635-156">usd: CRM Service USA (sample).</span></span> 

#### <a name="salesinvoiceline-task"></a><span data-ttu-id="e2635-157">Taak SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="e2635-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="e2635-158">Controleer of de benodigde toewijzing aanwezig is in **Bron** > **CDS voor maateenheid**.</span><span class="sxs-lookup"><span data-stu-id="e2635-158">Ensure that the needed mapping exists in **Source** > **CDS for Unit of measure**.</span></span>

- <span data-ttu-id="e2635-159">Controleer of de benodigde **ValueMap** voor **SalesUnitSymbol** in Finance and Operations aanwezig is in **Bron** > **CDS-toewijzing**.</span><span class="sxs-lookup"><span data-stu-id="e2635-159">Ensure that the needed **ValueMap** for **SalesUnitSymbol** in Finance and Operations exists in the **Source** > **CDS mapping**.</span></span> 
    
    - <span data-ttu-id="e2635-160">Waarde van de sjabloon met **ValueMap** is gedefinieerd voor **SalesUnitSymbol naar Quantity_UOM**.</span><span class="sxs-lookup"><span data-stu-id="e2635-160">Template value with **ValueMap** is defined for **SalesUnitSymbol to Quantity_UOM**.</span></span>
    
-  <span data-ttu-id="e2635-161">Werk de toewijzing voor **CDS-organisatie-id bij in Bron** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="e2635-161">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span> 

    -  <span data-ttu-id="e2635-162">De standaardsjabloonwaarde voor **SalesInvoicer_Organization_OrganizationId** is ORG001.</span><span class="sxs-lookup"><span data-stu-id="e2635-162">Default template value for **SalesInvoicer_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="e2635-163">De standaardsjabloonwaarde voor **Product_Organization_OrganizationId** is ORG001.</span><span class="sxs-lookup"><span data-stu-id="e2635-163">Default template value for **Product_Organization_OrganizationId** is ORG001.</span></span>
 
## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="e2635-164">Sjabloontoewijzing in Gegevensintegrator</span><span class="sxs-lookup"><span data-stu-id="e2635-164">Template mapping in Data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="e2635-165">**Betalingsvoorwaarden**, **Leveringscondities**, **Leveringsvoorwaarden**, **Verzendmethode** en **Leveringsmethode** maken geen deel uit van de standaardtoewijzingen.</span><span class="sxs-lookup"><span data-stu-id="e2635-165">**Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** are not part of the default mappings.</span></span> <span data-ttu-id="e2635-166">Als u deze velden wilt toewijzen, moet u een waardetoewijzing instellen die specifiek is voor de gegevens in de organisaties waartussen de entiteit wordt gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="e2635-166">Mapping of these fields requires value mapping to be set up, which is specific to the data in the organizations between which the entity is synchronized.</span></span>

<span data-ttu-id="e2635-167">In de volgende afbeeldingen ziet u een voorbeeld van de toewijzing van een sjabloon in gegevensintegrator.</span><span class="sxs-lookup"><span data-stu-id="e2635-167">The following illustrations show an example of a template mapping in data integrator.</span></span>

![Sjabloontoewijzing in gegevensintegrator](./media/sales-invoice-template-mapping-data-integrator-1.png)

![Sjabloontoewijzing in gegevensintegrator](./media/sales-invoice-template-mapping-data-integrator-2.png)

![Sjabloontoewijzing in gegevensintegrator](./media/sales-invoice-template-mapping-data-integrator-3.png)

![Sjabloontoewijzing in gegevensintegrator](./media/sales-invoice-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="e2635-172">Verwante onderwerpen</span><span class="sxs-lookup"><span data-stu-id="e2635-172">Related topics</span></span>

[<span data-ttu-id="e2635-173">Producten uit Finance and Operations synchroniseren met producten in Sales</span><span class="sxs-lookup"><span data-stu-id="e2635-173">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="e2635-174">Accounts in Sales synchroniseren met klanten in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e2635-174">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="e2635-175">Contactpersonen in Sales synchroniseren naar contactpersonen of klanten in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e2635-175">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="e2635-176">Kopteksten en regels in verkoopoffertes vanuit Sales synchroniseren naar Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e2635-176">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="e2635-177">Kopteksten en regels in verkooporders synchroniseren vanuit Finance and Operations naar Sales</span><span class="sxs-lookup"><span data-stu-id="e2635-177">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)


