---
title: Kopteksten en regels in verkoopoffertes vanuit Sales direct synchroniseren naar Finance and Operations
description: In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het direct synchroniseren van kopteksten en regels van verkoopoffertes vanuit Microsoft Dynamics 365 for Sales naar Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.
author: ChristianRytt
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 674d2e1f2c5cdbccf43618a9083ca01abed0735a
ms.openlocfilehash: 8a75c6dd91020ab3e676e2bb40d5c822731e244f
ms.contentlocale: nl-nl
ms.lasthandoff: 11/14/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-finance-and-operations"></a><span data-ttu-id="e23b8-103">Kopteksten en regels in verkoopoffertes vanuit Sales direct synchroniseren naar Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e23b8-103">Synchronize sales quotation headers and lines directly from Sales to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e23b8-104">In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het direct synchroniseren van kopteksten en regels van verkoopoffertes vanuit Microsoft Dynamics 365 for Sales naar Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span><span class="sxs-lookup"><span data-stu-id="e23b8-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

> [!NOTE]
> <span data-ttu-id="e23b8-105">Voordat u de oplossing Prospect naar contant geld kunt gebruiken, moet u vertrouwd zijn met [Dynamics 365 Gegevensintegratie](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="e23b8-105">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="e23b8-106">Sjabloon en taken</span><span class="sxs-lookup"><span data-stu-id="e23b8-106">Template and tasks</span></span>

<span data-ttu-id="e23b8-107">De volgende sjabloon en onderliggende taken worden gebruikt voor het direct synchroniseren van kopteksten en regels van verkoopoffertes vanuit Sales naar Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="e23b8-107">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="e23b8-108">**Naam van de sjabloon in Gegevensintegratie:** Verkoopoffertes (Sales naar Fin and Ops) - Direct</span><span class="sxs-lookup"><span data-stu-id="e23b8-108">**Name of the template in Data integration:** Sales Quotes (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="e23b8-109">**Namen van de taken in het project Gegevensintegratie:**</span><span class="sxs-lookup"><span data-stu-id="e23b8-109">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="e23b8-110">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="e23b8-110">QuoteHeader</span></span>
    - <span data-ttu-id="e23b8-111">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="e23b8-111">QuoteLine</span></span>

<span data-ttu-id="e23b8-112">De volgende synchronisatietaken zijn vereist voordat de synchronisatie van de kopteksten en regels van verkoopoffertes kan plaatsvinden:</span><span class="sxs-lookup"><span data-stu-id="e23b8-112">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="e23b8-113">Producten (Fin and Ops naar Sales) - Direct</span><span class="sxs-lookup"><span data-stu-id="e23b8-113">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="e23b8-114">Rekeningen (Sales naar Fin and Ops) - Direct (indien gebruikt)</span><span class="sxs-lookup"><span data-stu-id="e23b8-114">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="e23b8-115">Contactpersonen naar klanten (Sales naar Fin and Ops) - Direct (indien gebruikt)</span><span class="sxs-lookup"><span data-stu-id="e23b8-115">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="e23b8-116">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="e23b8-116">Entity set</span></span>

| <span data-ttu-id="e23b8-117">Verkoop</span><span class="sxs-lookup"><span data-stu-id="e23b8-117">Sales</span></span>        | <span data-ttu-id="e23b8-118">Finance en Operations</span><span class="sxs-lookup"><span data-stu-id="e23b8-118">Finance and Operations</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="e23b8-119">Citaten</span><span class="sxs-lookup"><span data-stu-id="e23b8-119">Quotes</span></span>       | <span data-ttu-id="e23b8-120">CDS-verkoopoffertekoptekst</span><span class="sxs-lookup"><span data-stu-id="e23b8-120">CDS sales quotation header</span></span> |
| <span data-ttu-id="e23b8-121">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="e23b8-121">QuoteDetails</span></span> | <span data-ttu-id="e23b8-122">Regels van CDS-verkoopofferte</span><span class="sxs-lookup"><span data-stu-id="e23b8-122">CDS sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="e23b8-123">Entiteitstroom</span><span class="sxs-lookup"><span data-stu-id="e23b8-123">Entity flow</span></span>

<span data-ttu-id="e23b8-124">Verkoopoffertes worden gemaakt in Sales en gesynchroniseerd met Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e23b8-124">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="e23b8-125">Verkoopoffertes uit Sales worden alleen gesynchroniseerd als aan de volgende voorwaarden is voldaan:</span><span class="sxs-lookup"><span data-stu-id="e23b8-125">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="e23b8-126">Alle offerteproducten in de verkoopofferte worden extern beheerd.</span><span class="sxs-lookup"><span data-stu-id="e23b8-126">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="e23b8-127">Als u op **Offerte activeren** klikt, wordt de verkoopofferte actief.</span><span class="sxs-lookup"><span data-stu-id="e23b8-127">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="e23b8-128">Oplossing Prospect naar contant geld voor Sales</span><span class="sxs-lookup"><span data-stu-id="e23b8-128">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="e23b8-129">Het veld **Heeft alleen extern onderhouden producten** is toegevoegd aan de entiteit **Offerte** om consistent bij te houden of de verkoopofferte geheel bestaat uit extern beheerde producten.</span><span class="sxs-lookup"><span data-stu-id="e23b8-129">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="e23b8-130">Als een verkoopofferte alleen extern beheerde producten heeft, worden de producten beheerd in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e23b8-130">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="e23b8-131">Zo garandeert u dat u niet verkoopofferteregels probeert te synchroniseren voor producten die onbekend zijn in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e23b8-131">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="e23b8-132">Alle offerteproducten in de verkoopofferte worden bijgewerkt met de informatie **Heeft alleen extern onderhouden producten** uit de verkoopoffertekoptekst.</span><span class="sxs-lookup"><span data-stu-id="e23b8-132">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="e23b8-133">Deze informatie vindt u in het veld **Offerte heeft alleen extern onderhouden producten** voor de entiteit **QuoteDetails**.</span><span class="sxs-lookup"><span data-stu-id="e23b8-133">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="e23b8-134">Er kan een korting worden toegevoegd aan het offerteproduct en deze wordt gesynchroniseerd naar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e23b8-134">A discount can be added to the quote product and will be synchronized to Finance and Operations.</span></span> <span data-ttu-id="e23b8-135">De velden **Korting**, **Toeslagen** en **Btw** in de koptekst worden bepaald door een configuratie in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e23b8-135">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Finance and Operations.</span></span> <span data-ttu-id="e23b8-136">Deze configuratie biedt momenteel geen ondersteuning voor integratietoewijzing.</span><span class="sxs-lookup"><span data-stu-id="e23b8-136">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="e23b8-137">In het huidige ontwerp worden de velden **Prijs**, **Korting**, **Toeslagen** en **Btw** beheerd en verwerkt in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e23b8-137">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in Finance and Operations.</span></span>

<span data-ttu-id="e23b8-138">In Sales worden de volgende velden alleen-lezen gemaakt, omdat de waarden niet worden gesynchroniseerd met Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="e23b8-138">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="e23b8-139">Alleen-lezenvelden in de koptekst van de verkoopofferte: **Kortingspercentage**, **Korting** en **Vrachtkosten**</span><span class="sxs-lookup"><span data-stu-id="e23b8-139">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="e23b8-140">Alleen-lezenvelden voor offerteproducten: **Btw**</span><span class="sxs-lookup"><span data-stu-id="e23b8-140">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="e23b8-141">Voorwaarden en instellingen voor toewijzing</span><span class="sxs-lookup"><span data-stu-id="e23b8-141">Preconditions and mapping setup</span></span>

<span data-ttu-id="e23b8-142">Voordat u verkoopoffertes synchroniseert, is het belangrijk de volgende instellingen bij te werken.</span><span class="sxs-lookup"><span data-stu-id="e23b8-142">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="e23b8-143">Instellingen in Sales</span><span class="sxs-lookup"><span data-stu-id="e23b8-143">Setup in Sales</span></span>

- <span data-ttu-id="e23b8-144">Zorg ervoor dat er machtigingen zijn ingesteld voor het team waaraan de gebruiker uit uw verbindingsset in Sales is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="e23b8-144">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="e23b8-145">Als u voorbeeldgegevens gebruikt, heeft de gebruiker meestal beheerderstoegang, maar het team niet.</span><span class="sxs-lookup"><span data-stu-id="e23b8-145">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="e23b8-146">Als het team geen beheerderstoegang heeft wanneer u het project uitvoert vanuit Gegevensintegratie, wordt een foutbericht weergegeven waarin wordt aangegeven dat het hoofdteam ontbreekt.</span><span class="sxs-lookup"><span data-stu-id="e23b8-146">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="e23b8-147">Als u machtigingen voor het team wilt instellen, gaat u naar **instellingen** &gt; **Beveiliging** &gt; **Teams** en selecteert u het gewenste team.</span><span class="sxs-lookup"><span data-stu-id="e23b8-147">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="e23b8-148">Selecteer **Rollen beheren** en selecteer vervolgens een rol met de gewenste machtigingen, zoals **Systeembeheerder**.</span><span class="sxs-lookup"><span data-stu-id="e23b8-148">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="e23b8-149">Ga naar **Instellingen** &gt; **Beheer** &gt; **Systeeminstellingen** &gt; **Sales** en zorg ervoor dat de volgende instellingen worden gebruikt:</span><span class="sxs-lookup"><span data-stu-id="e23b8-149">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="e23b8-150">De optie **Systeem voor berekenen van systeemprijzen gebruiken** is ingesteld op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e23b8-150">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="e23b8-151">Het veld **Berekeningsmethode korting** is ingesteld op **Regelartikel**.</span><span class="sxs-lookup"><span data-stu-id="e23b8-151">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="e23b8-152">Instellingen in het project Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="e23b8-152">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="e23b8-153">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="e23b8-153">QuoteHeader</span></span>

- <span data-ttu-id="e23b8-154">Zorg ervoor dat de vereiste toewijzing bestaat voor **Shipto\_country** naar **DeliveryAddressCountryRegionISOCode**.</span><span class="sxs-lookup"><span data-stu-id="e23b8-154">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="e23b8-155">In de waardetoewijzing kunt u een standaardwaarde opgeven die moet worden gebruikt als de waarde leeg wordt gelaten.</span><span class="sxs-lookup"><span data-stu-id="e23b8-155">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="e23b8-156">Laat de linkerkant leeg laat en stel de rechterkant in op het gewenste land of de gewenste regio.</span><span class="sxs-lookup"><span data-stu-id="e23b8-156">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="e23b8-157">Op deze manier hoeft u geen land of regio op te geven voor nationale orders.</span><span class="sxs-lookup"><span data-stu-id="e23b8-157">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="e23b8-158">De sjabloonwaarde is een toewijzingswaarde waarbij verschillende landen of regio's worden toegewezen en waarbij een lege waarde gelijk is aan de waarde **VS**.</span><span class="sxs-lookup"><span data-stu-id="e23b8-158">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="e23b8-159">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="e23b8-159">QuoteLine</span></span>

- <span data-ttu-id="e23b8-160">Zorg ervoor dat de vereiste waardetoewijzing voor **SalesUnitSymbol** in Finance and Operations bestaat.</span><span class="sxs-lookup"><span data-stu-id="e23b8-160">Make sure that the required value map exists for **SalesUnitSymbol** in Finance and Operations.</span></span>
- <span data-ttu-id="e23b8-161">Zorg ervoor dat de vereiste eenheden zijn gedefinieerd in Sales.</span><span class="sxs-lookup"><span data-stu-id="e23b8-161">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="e23b8-162">Er wordt een sjabloonwaarde met een waardetoewijzing gedefinieerd voor **oumid.name** naar **SalesUnitSymbol**.</span><span class="sxs-lookup"><span data-stu-id="e23b8-162">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="e23b8-163">U kunt desgewenst de volgende toewijzingen toevoegen om te garanderen dat verkoopofferteregels worden geïmporteerd in Finance and Operations als er geen standaardgegevens over de klant of het product zijn:</span><span class="sxs-lookup"><span data-stu-id="e23b8-163">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="e23b8-164">**SiteId**: een site is vereist voor het genereren van offertes en verkooporderregels in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e23b8-164">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="e23b8-165">Er is geen standaardwaarde van de sjabloon voor **SiteId**.</span><span class="sxs-lookup"><span data-stu-id="e23b8-165">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="e23b8-166">**WarehouseId**: een magazijn is vereist voor het verwerken van offertes en verkooporderregels in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e23b8-166">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="e23b8-167">Er is geen standaardwaarde van de sjabloon voor **WarehouseId**.</span><span class="sxs-lookup"><span data-stu-id="e23b8-167">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="e23b8-168">Sjabloontoewijzing in gegevensintegrator</span><span class="sxs-lookup"><span data-stu-id="e23b8-168">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="e23b8-169">De velden **Korting**, **Toeslagen** en **Btw** worden bepaald door een complexe configuratie in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e23b8-169">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="e23b8-170">Deze configuratie biedt momenteel geen ondersteuning voor integratietoewijzing.</span><span class="sxs-lookup"><span data-stu-id="e23b8-170">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="e23b8-171">In het huidige ontwerp worden de velden **Prijs**, **Korting**, **Toeslagen** en **Btw** verwerkt door Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e23b8-171">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="e23b8-172">De velden **Betalingsvoorwaarden**, **Leveringscondities**, **Leveringsvoorwaarden**, **Verzendmethode** en **Leveringsmethode** maken geen deel uit van de standaardtoewijzingen.</span><span class="sxs-lookup"><span data-stu-id="e23b8-172">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="e23b8-173">Als u deze velden wilt toewijzen, moet u een waardetoewijzing instellen die specifiek is voor de gegevens in de organisaties waartussen de entiteit wordt gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="e23b8-173">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="e23b8-174">In de volgende afbeeldingen ziet u een voorbeeld van de toewijzing van een sjabloon in gegevensintegrator.</span><span class="sxs-lookup"><span data-stu-id="e23b8-174">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="e23b8-175">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="e23b8-175">QuoteHeader</span></span>

![Sjabloontoewijzing in gegevensintegrator](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="e23b8-177">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="e23b8-177">QuoteLine</span></span>

![Sjabloontoewijzing in gegevensintegrator](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="e23b8-179">Verwante onderwerpen</span><span class="sxs-lookup"><span data-stu-id="e23b8-179">Related topics</span></span>

[<span data-ttu-id="e23b8-180">Prospect naar contant geld</span><span class="sxs-lookup"><span data-stu-id="e23b8-180">Prospect to cash</span></span>](prospect-to-cash.md)


