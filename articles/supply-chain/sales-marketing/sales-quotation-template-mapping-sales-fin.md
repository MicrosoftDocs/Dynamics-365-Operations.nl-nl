---
title: Kopteksten en regels in verkoopoffertes vanuit Sales direct synchroniseren naar Finance and Operations
description: In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van kopteksten en regels van verkoopoffertes tussen Microsoft Dynamics 365 for Sales en Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: efe943f5c874ed041ce7984272ebc19f57cca6ef
ms.contentlocale: nl-nl
ms.lasthandoff: 11/01/2018

---

# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-finance-and-operations"></a><span data-ttu-id="2abfd-103">Kopteksten en regels in verkoopoffertes vanuit Sales direct synchroniseren naar Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2abfd-103">Synchronize sales quotation headers and lines directly from Sales to Finance and Operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2abfd-104">In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van kopteksten en regels van verkoopoffertes tussen Microsoft Dynamics 365 for Sales en Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2abfd-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="2abfd-105">Voordat u de oplossing Prospect naar contant geld kunt gebruiken, moet u vertrouwd zijn met [Gegevens integreren in Common Data Service voor Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="2abfd-105">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="2abfd-106">Gegevensstroom in Prospect naar contant geld</span><span class="sxs-lookup"><span data-stu-id="2abfd-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="2abfd-107">De oplossing Prospect naar contant geld gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Finance and Operations en Sales.</span><span class="sxs-lookup"><span data-stu-id="2abfd-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="2abfd-108">De Prospect naar contant geld-sjablonen die beschikbaar zijn in de functie Gegevensintegratie activeren de stroom van gegevens voor rekeningen, contactpersonen, producten, verkoopoffertes en verkoopfacturen tussen Finance and Operations en Sales.</span><span class="sxs-lookup"><span data-stu-id="2abfd-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="2abfd-109">De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Finance and Operations en Sales.</span><span class="sxs-lookup"><span data-stu-id="2abfd-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="2abfd-110">[![Gegevensstroom in Prospect naar contant geld](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="2abfd-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="2abfd-111">Sjabloon en taken</span><span class="sxs-lookup"><span data-stu-id="2abfd-111">Template and tasks</span></span>

<span data-ttu-id="2abfd-112">De volgende sjabloon en onderliggende taken worden gebruikt voor het direct synchroniseren van kopteksten en regels van verkoopoffertes vanuit Sales naar Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="2abfd-112">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="2abfd-113">**Naam van de sjabloon in Gegevensintegratie:** Verkoopoffertes (Sales naar Fin and Ops) - Direct</span><span class="sxs-lookup"><span data-stu-id="2abfd-113">**Name of the template in Data integration:** Sales Quotes (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="2abfd-114">**Namen van de taken in het project Gegevensintegratie:**</span><span class="sxs-lookup"><span data-stu-id="2abfd-114">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="2abfd-115">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="2abfd-115">QuoteHeader</span></span>
    - <span data-ttu-id="2abfd-116">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="2abfd-116">QuoteLine</span></span>

<span data-ttu-id="2abfd-117">De volgende synchronisatietaken zijn vereist voordat de synchronisatie van de kopteksten en regels van verkoopoffertes kan plaatsvinden:</span><span class="sxs-lookup"><span data-stu-id="2abfd-117">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="2abfd-118">Producten (Fin and Ops naar Sales) - Direct</span><span class="sxs-lookup"><span data-stu-id="2abfd-118">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="2abfd-119">Rekeningen (Sales naar Fin and Ops) - Direct (indien gebruikt)</span><span class="sxs-lookup"><span data-stu-id="2abfd-119">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="2abfd-120">Contactpersonen naar klanten (Sales naar Fin and Ops) - Direct (indien gebruikt)</span><span class="sxs-lookup"><span data-stu-id="2abfd-120">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="2abfd-121">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="2abfd-121">Entity set</span></span>

| <span data-ttu-id="2abfd-122">Verkoop</span><span class="sxs-lookup"><span data-stu-id="2abfd-122">Sales</span></span>        | <span data-ttu-id="2abfd-123">Finance en Operations</span><span class="sxs-lookup"><span data-stu-id="2abfd-123">Finance and Operations</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="2abfd-124">Citaten</span><span class="sxs-lookup"><span data-stu-id="2abfd-124">Quotes</span></span>       | <span data-ttu-id="2abfd-125">CDS-verkoopoffertekoptekst</span><span class="sxs-lookup"><span data-stu-id="2abfd-125">CDS sales quotation header</span></span> |
| <span data-ttu-id="2abfd-126">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="2abfd-126">QuoteDetails</span></span> | <span data-ttu-id="2abfd-127">Regels van CDS-verkoopofferte</span><span class="sxs-lookup"><span data-stu-id="2abfd-127">CDS sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="2abfd-128">Entiteitstroom</span><span class="sxs-lookup"><span data-stu-id="2abfd-128">Entity flow</span></span>

<span data-ttu-id="2abfd-129">Verkoopoffertes worden gemaakt in Sales en gesynchroniseerd met Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2abfd-129">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="2abfd-130">Verkoopoffertes uit Sales worden alleen gesynchroniseerd als aan de volgende voorwaarden is voldaan:</span><span class="sxs-lookup"><span data-stu-id="2abfd-130">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="2abfd-131">Alle offerteproducten in de verkoopofferte worden extern beheerd.</span><span class="sxs-lookup"><span data-stu-id="2abfd-131">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="2abfd-132">Als u op **Offerte activeren** klikt, wordt de verkoopofferte actief.</span><span class="sxs-lookup"><span data-stu-id="2abfd-132">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="2abfd-133">Oplossing Prospect naar contant geld voor Sales</span><span class="sxs-lookup"><span data-stu-id="2abfd-133">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="2abfd-134">Het veld **Heeft alleen extern onderhouden producten** is toegevoegd aan de entiteit **Offerte** om consistent bij te houden of de verkoopofferte geheel bestaat uit extern beheerde producten.</span><span class="sxs-lookup"><span data-stu-id="2abfd-134">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="2abfd-135">Als een verkoopofferte alleen extern beheerde producten heeft, worden de producten beheerd in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2abfd-135">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="2abfd-136">Zo garandeert u dat u niet verkoopofferteregels probeert te synchroniseren voor producten die onbekend zijn in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2abfd-136">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="2abfd-137">Alle offerteproducten in de verkoopofferte worden bijgewerkt met de informatie **Heeft alleen extern onderhouden producten** uit de verkoopoffertekoptekst.</span><span class="sxs-lookup"><span data-stu-id="2abfd-137">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="2abfd-138">Deze informatie vindt u in het veld **Offerte heeft alleen extern onderhouden producten** voor de entiteit **QuoteDetails**.</span><span class="sxs-lookup"><span data-stu-id="2abfd-138">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="2abfd-139">Er kan een korting worden toegevoegd aan het offerteproduct en deze wordt gesynchroniseerd naar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2abfd-139">A discount can be added to the quote product and will be synchronized to Finance and Operations.</span></span> <span data-ttu-id="2abfd-140">De velden **Korting**, **Toeslagen** en **Btw** in de koptekst worden bepaald door een configuratie in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2abfd-140">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Finance and Operations.</span></span> <span data-ttu-id="2abfd-141">Deze configuratie biedt momenteel geen ondersteuning voor integratietoewijzing.</span><span class="sxs-lookup"><span data-stu-id="2abfd-141">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="2abfd-142">In het huidige ontwerp worden de velden **Prijs**, **Korting**, **Toeslagen** en **Btw** beheerd en verwerkt in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2abfd-142">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in Finance and Operations.</span></span>

<span data-ttu-id="2abfd-143">In Sales worden de volgende velden alleen-lezen gemaakt, omdat de waarden niet worden gesynchroniseerd met Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="2abfd-143">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="2abfd-144">Alleen-lezenvelden in de koptekst van de verkoopofferte: **Kortingspercentage**, **Korting** en **Vrachtkosten**</span><span class="sxs-lookup"><span data-stu-id="2abfd-144">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="2abfd-145">Alleen-lezenvelden voor offerteproducten: **Btw**</span><span class="sxs-lookup"><span data-stu-id="2abfd-145">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="2abfd-146">Voorwaarden en instellingen voor toewijzing</span><span class="sxs-lookup"><span data-stu-id="2abfd-146">Preconditions and mapping setup</span></span>

<span data-ttu-id="2abfd-147">Voordat u verkoopoffertes synchroniseert, is het belangrijk de volgende instellingen bij te werken.</span><span class="sxs-lookup"><span data-stu-id="2abfd-147">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="2abfd-148">Instellingen in Sales</span><span class="sxs-lookup"><span data-stu-id="2abfd-148">Setup in Sales</span></span>

- <span data-ttu-id="2abfd-149">Zorg ervoor dat er machtigingen zijn ingesteld voor het team waaraan de gebruiker uit uw verbindingsset in Sales is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="2abfd-149">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="2abfd-150">Als u voorbeeldgegevens gebruikt, heeft de gebruiker meestal beheerderstoegang, maar het team niet.</span><span class="sxs-lookup"><span data-stu-id="2abfd-150">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="2abfd-151">Als het team geen beheerderstoegang heeft wanneer u het project uitvoert vanuit Gegevensintegratie, wordt een foutbericht weergegeven waarin wordt aangegeven dat het hoofdteam ontbreekt.</span><span class="sxs-lookup"><span data-stu-id="2abfd-151">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="2abfd-152">Als u machtigingen voor het team wilt instellen, gaat u naar **instellingen** &gt; **Beveiliging** &gt; **Teams** en selecteert u het gewenste team.</span><span class="sxs-lookup"><span data-stu-id="2abfd-152">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="2abfd-153">Selecteer **Rollen beheren** en selecteer vervolgens een rol met de gewenste machtigingen, zoals **Systeembeheerder**.</span><span class="sxs-lookup"><span data-stu-id="2abfd-153">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="2abfd-154">Ga naar **Instellingen** &gt; **Beheer** &gt; **Systeeminstellingen** &gt; **Sales** en zorg ervoor dat de volgende instellingen worden gebruikt:</span><span class="sxs-lookup"><span data-stu-id="2abfd-154">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="2abfd-155">De optie **Systeem voor berekenen van systeemprijzen gebruiken** is ingesteld op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="2abfd-155">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="2abfd-156">Het veld **Berekeningsmethode korting** is ingesteld op **Regelartikel**.</span><span class="sxs-lookup"><span data-stu-id="2abfd-156">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="2abfd-157">Instellingen in het project Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="2abfd-157">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="2abfd-158">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="2abfd-158">QuoteHeader</span></span>

- <span data-ttu-id="2abfd-159">Zorg ervoor dat de vereiste toewijzing bestaat voor **Shipto\_country** naar **DeliveryAddressCountryRegionISOCode**.</span><span class="sxs-lookup"><span data-stu-id="2abfd-159">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="2abfd-160">In de waardetoewijzing kunt u een standaardwaarde opgeven die moet worden gebruikt als de waarde leeg wordt gelaten.</span><span class="sxs-lookup"><span data-stu-id="2abfd-160">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="2abfd-161">Laat de linkerkant leeg laat en stel de rechterkant in op het gewenste land of de gewenste regio.</span><span class="sxs-lookup"><span data-stu-id="2abfd-161">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="2abfd-162">Op deze manier hoeft u geen land of regio op te geven voor nationale orders.</span><span class="sxs-lookup"><span data-stu-id="2abfd-162">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="2abfd-163">De sjabloonwaarde is een toewijzingswaarde waarbij verschillende landen of regio's worden toegewezen en waarbij een lege waarde gelijk is aan de waarde **VS**.</span><span class="sxs-lookup"><span data-stu-id="2abfd-163">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="2abfd-164">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="2abfd-164">QuoteLine</span></span>

- <span data-ttu-id="2abfd-165">Zorg ervoor dat de vereiste waardetoewijzing voor **SalesUnitSymbol** in Finance and Operations bestaat.</span><span class="sxs-lookup"><span data-stu-id="2abfd-165">Make sure that the required value map exists for **SalesUnitSymbol** in Finance and Operations.</span></span>
- <span data-ttu-id="2abfd-166">Zorg ervoor dat de vereiste eenheden zijn gedefinieerd in Sales.</span><span class="sxs-lookup"><span data-stu-id="2abfd-166">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="2abfd-167">Er wordt een sjabloonwaarde met een waardetoewijzing gedefinieerd voor **oumid.name** naar **SalesUnitSymbol**.</span><span class="sxs-lookup"><span data-stu-id="2abfd-167">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="2abfd-168">U kunt desgewenst de volgende toewijzingen toevoegen om te garanderen dat verkoopofferteregels worden geïmporteerd in Finance and Operations als er geen standaardgegevens over de klant of het product zijn:</span><span class="sxs-lookup"><span data-stu-id="2abfd-168">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="2abfd-169">**SiteId**: een site is vereist voor het genereren van offertes en verkooporderregels in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2abfd-169">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="2abfd-170">Er is geen standaardwaarde van de sjabloon voor **SiteId**.</span><span class="sxs-lookup"><span data-stu-id="2abfd-170">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="2abfd-171">**WarehouseId**: een magazijn is vereist voor het verwerken van offertes en verkooporderregels in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2abfd-171">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="2abfd-172">Er is geen standaardwaarde van de sjabloon voor **WarehouseId**.</span><span class="sxs-lookup"><span data-stu-id="2abfd-172">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="2abfd-173">Sjabloontoewijzing in gegevensintegrator</span><span class="sxs-lookup"><span data-stu-id="2abfd-173">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="2abfd-174">De velden **Korting**, **Toeslagen** en **Btw** worden bepaald door een complexe configuratie in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2abfd-174">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="2abfd-175">Deze configuratie biedt momenteel geen ondersteuning voor integratietoewijzing.</span><span class="sxs-lookup"><span data-stu-id="2abfd-175">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="2abfd-176">In het huidige ontwerp worden de velden **Prijs**, **Korting**, **Toeslagen** en **Btw** verwerkt door Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2abfd-176">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="2abfd-177">De velden **Betalingsvoorwaarden**, **Leveringscondities**, **Leveringsvoorwaarden**, **Verzendmethode** en **Leveringsmethode** maken geen deel uit van de standaardtoewijzingen.</span><span class="sxs-lookup"><span data-stu-id="2abfd-177">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="2abfd-178">Als u deze velden wilt toewijzen, moet u een waardetoewijzing instellen die specifiek is voor de gegevens in de organisaties waartussen de entiteit wordt gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="2abfd-178">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="2abfd-179">In de volgende afbeeldingen ziet u een voorbeeld van de toewijzing van een sjabloon in gegevensintegrator.</span><span class="sxs-lookup"><span data-stu-id="2abfd-179">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="2abfd-180">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="2abfd-180">QuoteHeader</span></span>

![Sjabloontoewijzing in gegevensintegrator](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="2abfd-182">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="2abfd-182">QuoteLine</span></span>

![Sjabloontoewijzing in gegevensintegrator](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="2abfd-184">Verwante onderwerpen</span><span class="sxs-lookup"><span data-stu-id="2abfd-184">Related topics</span></span>

[<span data-ttu-id="2abfd-185">Prospect naar contant geld</span><span class="sxs-lookup"><span data-stu-id="2abfd-185">Prospect to cash</span></span>](prospect-to-cash.md)


