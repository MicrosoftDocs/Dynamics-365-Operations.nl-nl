---
title: Kopteksten en regels in verkoopoffertes rechtstreeks synchroniseren vanuit Sales naar Supply Chain Management
description: In dit onderwerp worden de sjablonen en onderliggende taken besproken die worden gebruikt voor het rechtstreeks synchroniseren van kopteksten en regels van verkoopoffertes van Dynamics 365 Sales naar Dynamics 365 Supply Chain Management.
author: ChristianRytt
ms.date: 10/25/2018
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
ms.openlocfilehash: 848464cbc62623502b9b87b9b41dcc17150e85ba
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839000"
---
# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-supply-chain-management"></a><span data-ttu-id="51a0c-103">Kopteksten en regels in verkoopoffertes rechtstreeks synchroniseren vanuit Sales naar Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="51a0c-103">Synchronize sales quotation headers and lines directly from Sales to Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="51a0c-104">In dit onderwerp worden de sjablonen en onderliggende taken besproken die worden gebruikt voor het rechtstreeks synchroniseren van kopteksten en regels van verkoopoffertes van Dynamics 365 Sales naar Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="51a0c-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

> [!NOTE]
> <span data-ttu-id="51a0c-105">Voordat u de oplossing Prospect naar contant geld kunt gebruiken, moet u vertrouwd zijn met [Gegevens integreren in Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="51a0c-105">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="51a0c-106">Gegevensstroom in Prospect naar contant geld</span><span class="sxs-lookup"><span data-stu-id="51a0c-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="51a0c-107">De oplossing Prospect naar contant geld gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Supply Chain Management en Sales.</span><span class="sxs-lookup"><span data-stu-id="51a0c-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="51a0c-108">De Prospect naar contant geld-sjablonen die beschikbaar zijn in de functie Gegevensintegratie activeren de stroom van gegevens voor rekeningen, contactpersonen, producten, verkoopoffertes en verkoopfacturen tussen Supply Chain Management en Sales.</span><span class="sxs-lookup"><span data-stu-id="51a0c-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="51a0c-109">De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Supply Chain Management en Sales.</span><span class="sxs-lookup"><span data-stu-id="51a0c-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="51a0c-110">[![Gegevensstroom in Prospect naar contant geld](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="51a0c-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="51a0c-111">Sjabloon en taken</span><span class="sxs-lookup"><span data-stu-id="51a0c-111">Template and tasks</span></span>

<span data-ttu-id="51a0c-112">De volgende sjabloon en onderliggende taken worden gebruikt voor het direct synchroniseren van kopteksten en regels van verkoopoffertes vanuit Sales naar Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="51a0c-112">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Supply Chain Management:</span></span>

- <span data-ttu-id="51a0c-113">**Naam van de sjabloon in Gegevensintegratie:** Verkoopoffertes (Sales naar Supply Chain Management) - Direct</span><span class="sxs-lookup"><span data-stu-id="51a0c-113">**Name of the template in Data integration:** Sales Quotes (Sales to Supply Chain Management) - Direct</span></span>
- <span data-ttu-id="51a0c-114">**Namen van de taken in het project Gegevensintegratie:**</span><span class="sxs-lookup"><span data-stu-id="51a0c-114">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="51a0c-115">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="51a0c-115">QuoteHeader</span></span>
    - <span data-ttu-id="51a0c-116">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="51a0c-116">QuoteLine</span></span>

<span data-ttu-id="51a0c-117">De volgende synchronisatietaken zijn vereist voordat de synchronisatie van de kopteksten en regels van verkoopoffertes kan plaatsvinden:</span><span class="sxs-lookup"><span data-stu-id="51a0c-117">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="51a0c-118">Producten (Supply Chain Management naar Sales) - Direct</span><span class="sxs-lookup"><span data-stu-id="51a0c-118">Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="51a0c-119">Rekeningen (Supply Chain Management naar Sales) - Direct (wanneer gebruikt)</span><span class="sxs-lookup"><span data-stu-id="51a0c-119">Accounts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="51a0c-120">Contactpersonen naar klanten (Sales naar Supply Chain Management) - Direct (indien gebruikt)</span><span class="sxs-lookup"><span data-stu-id="51a0c-120">Contacts to Customers (Sales to Supply Chain Management) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="51a0c-121">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="51a0c-121">Entity set</span></span>

| <span data-ttu-id="51a0c-122">Verkopen</span><span class="sxs-lookup"><span data-stu-id="51a0c-122">Sales</span></span>        | <span data-ttu-id="51a0c-123">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="51a0c-123">Supply Chain Management</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="51a0c-124">Citaten</span><span class="sxs-lookup"><span data-stu-id="51a0c-124">Quotes</span></span>       | <span data-ttu-id="51a0c-125">Dataverse-verkoopoffertekoptekst</span><span class="sxs-lookup"><span data-stu-id="51a0c-125">Dataverse sales quotation header</span></span> |
| <span data-ttu-id="51a0c-126">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="51a0c-126">QuoteDetails</span></span> | <span data-ttu-id="51a0c-127">Dataverse-verkoopofferteregels</span><span class="sxs-lookup"><span data-stu-id="51a0c-127">Dataverse sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="51a0c-128">Entiteitstroom</span><span class="sxs-lookup"><span data-stu-id="51a0c-128">Entity flow</span></span>

<span data-ttu-id="51a0c-129">Verkoopoffertes worden gemaakt in Sales en gesynchroniseerd met Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="51a0c-129">Sales quotations are created in Sales and synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="51a0c-130">Verkoopoffertes uit Sales worden alleen gesynchroniseerd als aan de volgende voorwaarden is voldaan:</span><span class="sxs-lookup"><span data-stu-id="51a0c-130">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="51a0c-131">Alle offerteproducten in de verkoopofferte worden extern beheerd.</span><span class="sxs-lookup"><span data-stu-id="51a0c-131">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="51a0c-132">Als u op **Offerte activeren** klikt, wordt de verkoopofferte actief.</span><span class="sxs-lookup"><span data-stu-id="51a0c-132">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="51a0c-133">Oplossing Prospect naar contant geld voor Sales</span><span class="sxs-lookup"><span data-stu-id="51a0c-133">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="51a0c-134">Het veld **Heeft alleen extern onderhouden producten** is toegevoegd aan de entiteit **Offerte** om consistent bij te houden of de verkoopofferte geheel bestaat uit extern beheerde producten.</span><span class="sxs-lookup"><span data-stu-id="51a0c-134">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="51a0c-135">Als een verkoopofferte alleen extern beheerde producten heeft, worden de producten beheerd in Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="51a0c-135">If a sales quotation has only externally maintained products, the products are maintained in Supply Chain Management.</span></span> <span data-ttu-id="51a0c-136">Zo garandeert u dat u niet verkoopofferteregels probeert te synchroniseren voor producten die onbekend zijn bij Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="51a0c-136">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Supply Chain Management.</span></span>

<span data-ttu-id="51a0c-137">Alle offerteproducten in de verkoopofferte worden bijgewerkt met de informatie **Heeft alleen extern onderhouden producten** uit de verkoopoffertekoptekst.</span><span class="sxs-lookup"><span data-stu-id="51a0c-137">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="51a0c-138">Deze informatie vindt u in het veld **Offerte heeft alleen extern onderhouden producten** voor de entiteit **QuoteDetails**.</span><span class="sxs-lookup"><span data-stu-id="51a0c-138">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="51a0c-139">Er kan een korting worden toegevoegd aan het offerteproduct en deze wordt gesynchroniseerd naar Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="51a0c-139">A discount can be added to the quote product and will be synchronized to Supply Chain Management.</span></span> <span data-ttu-id="51a0c-140">De velden **Korting**, **Toeslagen** en **Btw** in de koptekst worden bepaald door een configuratie in Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="51a0c-140">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Supply Chain Management.</span></span> <span data-ttu-id="51a0c-141">Deze configuratie biedt momenteel geen ondersteuning voor integratietoewijzing.</span><span class="sxs-lookup"><span data-stu-id="51a0c-141">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="51a0c-142">In het huidige ontwerp worden de velden **Prijs**, **Korting**, **Toeslagen** en **Btw** beheerd en verwerkt in Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="51a0c-142">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in FSupply Chain Management.</span></span>

<span data-ttu-id="51a0c-143">In Sales worden de volgende velden alleen-lezen gemaakt, omdat de waarden niet worden gesynchroniseerd met Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="51a0c-143">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Supply Chain Management:</span></span>

- <span data-ttu-id="51a0c-144">Alleen-lezenvelden in de koptekst van de verkoopofferte: **Kortingspercentage**, **Korting** en **Vrachtkosten**</span><span class="sxs-lookup"><span data-stu-id="51a0c-144">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="51a0c-145">Alleen-lezenvelden voor offerteproducten: **Btw**</span><span class="sxs-lookup"><span data-stu-id="51a0c-145">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="51a0c-146">Voorwaarden en instellingen voor toewijzing</span><span class="sxs-lookup"><span data-stu-id="51a0c-146">Preconditions and mapping setup</span></span>

<span data-ttu-id="51a0c-147">Voordat u verkoopoffertes synchroniseert, is het belangrijk de volgende instellingen bij te werken.</span><span class="sxs-lookup"><span data-stu-id="51a0c-147">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="51a0c-148">Instellingen in Sales</span><span class="sxs-lookup"><span data-stu-id="51a0c-148">Setup in Sales</span></span>

- <span data-ttu-id="51a0c-149">Zorg ervoor dat er machtigingen zijn ingesteld voor het team waaraan de gebruiker uit uw verbindingsset in Sales is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="51a0c-149">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="51a0c-150">Als u voorbeeldgegevens gebruikt, heeft de gebruiker meestal beheerderstoegang, maar het team niet.</span><span class="sxs-lookup"><span data-stu-id="51a0c-150">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="51a0c-151">Als het team geen beheerderstoegang heeft wanneer u het project uitvoert vanuit Gegevensintegratie, wordt een foutbericht weergegeven waarin wordt aangegeven dat het hoofdteam ontbreekt.</span><span class="sxs-lookup"><span data-stu-id="51a0c-151">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="51a0c-152">Als u machtigingen voor het team wilt instellen, gaat u naar **instellingen** &gt; **Beveiliging** &gt; **Teams** en selecteert u het gewenste team.</span><span class="sxs-lookup"><span data-stu-id="51a0c-152">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="51a0c-153">Selecteer **Rollen beheren** en selecteer vervolgens een rol met de gewenste machtigingen, zoals **Systeembeheerder**.</span><span class="sxs-lookup"><span data-stu-id="51a0c-153">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="51a0c-154">Ga naar **Instellingen** &gt; **Beheer** &gt; **Systeeminstellingen** &gt; **Sales** en zorg ervoor dat de volgende instellingen worden gebruikt:</span><span class="sxs-lookup"><span data-stu-id="51a0c-154">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="51a0c-155">De optie **Systeem voor berekenen van systeemprijzen gebruiken** is ingesteld op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="51a0c-155">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="51a0c-156">Het veld **Berekeningsmethode korting** is ingesteld op **Regelartikel**.</span><span class="sxs-lookup"><span data-stu-id="51a0c-156">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="51a0c-157">Instellingen in het project Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="51a0c-157">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="51a0c-158">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="51a0c-158">QuoteHeader</span></span>

- <span data-ttu-id="51a0c-159">Zorg ervoor dat de vereiste toewijzing bestaat voor **Shipto\_country** naar **DeliveryAddressCountryRegionISOCode**.</span><span class="sxs-lookup"><span data-stu-id="51a0c-159">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="51a0c-160">In de waardetoewijzing kunt u een standaardwaarde opgeven die moet worden gebruikt als de waarde leeg wordt gelaten.</span><span class="sxs-lookup"><span data-stu-id="51a0c-160">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="51a0c-161">Laat de linkerkant leeg laat en stel de rechterkant in op het gewenste land of de gewenste regio.</span><span class="sxs-lookup"><span data-stu-id="51a0c-161">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="51a0c-162">Op deze manier hoeft u geen land of regio op te geven voor nationale orders.</span><span class="sxs-lookup"><span data-stu-id="51a0c-162">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="51a0c-163">De sjabloonwaarde is een toewijzingswaarde waarbij verschillende landen of regio's worden toegewezen en waarbij een lege waarde gelijk is aan de waarde **VS**.</span><span class="sxs-lookup"><span data-stu-id="51a0c-163">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="51a0c-164">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="51a0c-164">QuoteLine</span></span>

- <span data-ttu-id="51a0c-165">Zorg ervoor dat de vereiste waardetoewijzing voor **SalesUnitSymbol** in Supply Chain Management bestaat.</span><span class="sxs-lookup"><span data-stu-id="51a0c-165">Make sure that the required value map exists for **SalesUnitSymbol** in Supply Chain Management.</span></span>
- <span data-ttu-id="51a0c-166">Zorg ervoor dat de vereiste eenheden zijn gedefinieerd in Sales.</span><span class="sxs-lookup"><span data-stu-id="51a0c-166">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="51a0c-167">Er wordt een sjabloonwaarde met een waardetoewijzing gedefinieerd voor **oumid.name** naar **SalesUnitSymbol**.</span><span class="sxs-lookup"><span data-stu-id="51a0c-167">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="51a0c-168">U kunt desgewenst de volgende toewijzingen toevoegen om te garanderen dat verkoopofferteregels worden geïmporteerd in Supply Chain Management als er geen standaardgegevens over de klant of het product zijn:</span><span class="sxs-lookup"><span data-stu-id="51a0c-168">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Supply Chain Management if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="51a0c-169">**SiteId**: een site is vereist voor het genereren van offertes en verkooporderregels in Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="51a0c-169">**SiteId** – A site is required in order to generate quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="51a0c-170">Er is geen standaardwaarde van de sjabloon voor **SiteId**.</span><span class="sxs-lookup"><span data-stu-id="51a0c-170">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="51a0c-171">**WarehouseId**: een magazijn is vereist voor het verwerken van offertes en verkooporderregels in Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="51a0c-171">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="51a0c-172">Er is geen standaardwaarde van de sjabloon voor **WarehouseId**.</span><span class="sxs-lookup"><span data-stu-id="51a0c-172">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="51a0c-173">Sjabloontoewijzing in gegevensintegrator</span><span class="sxs-lookup"><span data-stu-id="51a0c-173">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="51a0c-174">De velden **Korting**, **Toeslagen** en **Btw** in de koptekst worden bepaald door een complexe configuratie in Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="51a0c-174">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Supply Chain Management.</span></span> <span data-ttu-id="51a0c-175">Deze configuratie biedt momenteel geen ondersteuning voor integratietoewijzing.</span><span class="sxs-lookup"><span data-stu-id="51a0c-175">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="51a0c-176">In het huidige ontwerp worden de velden **Prijs**, **Korting**, **Toeslagen** en **Btw** verwerkt door Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="51a0c-176">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Supply Chain Management.</span></span>
> - <span data-ttu-id="51a0c-177">De velden **Betalingsvoorwaarden**, **Leveringscondities**, **Leveringsvoorwaarden**, **Verzendmethode** en **Leveringsmethode** maken geen deel uit van de standaardtoewijzingen.</span><span class="sxs-lookup"><span data-stu-id="51a0c-177">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="51a0c-178">Als u deze velden wilt toewijzen, moet u een waardetoewijzing instellen die specifiek is voor de gegevens in de organisaties waartussen de entiteit wordt gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="51a0c-178">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="51a0c-179">In de volgende afbeeldingen ziet u een voorbeeld van de toewijzing van een sjabloon in gegevensintegrator.</span><span class="sxs-lookup"><span data-stu-id="51a0c-179">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="51a0c-180">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="51a0c-180">QuoteHeader</span></span>

![Sjabloontoewijzing in gegevensintegrator](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="51a0c-182">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="51a0c-182">QuoteLine</span></span>

![Sjabloontoewijzing in gegevensintegrator](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="51a0c-184">Verwante onderwerpen</span><span class="sxs-lookup"><span data-stu-id="51a0c-184">Related topics</span></span>

[<span data-ttu-id="51a0c-185">Prospect naar contant geld</span><span class="sxs-lookup"><span data-stu-id="51a0c-185">Prospect to cash</span></span>](prospect-to-cash.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]