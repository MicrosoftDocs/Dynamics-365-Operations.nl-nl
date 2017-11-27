---
title: Kopteksten en regels van verkoopofferte synchroniseren tussen Sales en Finance and Operations
description: In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van kopteksten en regels van verkoopoffertes tussen Microsoft Dynamics 365 for Sales en Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.
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
ms.openlocfilehash: c8cfc484eed02423dbf0c7caaf8ac2337b6ac38d
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-from-sales-to-finance-and-operations"></a><span data-ttu-id="6629a-103">Kopteksten en regels van verkoopofferte synchroniseren tussen Sales en Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6629a-103">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="6629a-104">Voordat u de oplossing Prospect naar contant geld kunt gebruiken, moet u vertrouwd zijn met de functie [Dynamics 365 Gegevensintegratie](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="6629a-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="6629a-105">In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van kopteksten en regels van verkoopoffertes tussen Microsoft Dynamics 365 for Sales en Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span><span class="sxs-lookup"><span data-stu-id="6629a-105">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span> 

## <a name="template-and-tasks"></a><span data-ttu-id="6629a-106">Sjabloon en taken</span><span class="sxs-lookup"><span data-stu-id="6629a-106">Template and tasks</span></span>

<span data-ttu-id="6629a-107">De volgende sjablonen en onderliggende taken worden gebruikt voor het synchroniseren van de kopteksten en regels van verkoopoffertes tussen Sales en Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="6629a-107">The following templates and underlying tasks are used to synchronize sales quotation headers and lines from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="6629a-108">**Naam van de sjabloon:** Verkoopoffertes (Sales naar Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="6629a-108">**Name of the template:** Sales Quotes (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="6629a-109">**Namen van de taken in het project:**</span><span class="sxs-lookup"><span data-stu-id="6629a-109">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="6629a-110">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="6629a-110">QuoteHeader</span></span>
    - <span data-ttu-id="6629a-111">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="6629a-111">QuoteLine</span></span>

<span data-ttu-id="6629a-112">De volgende synchronisatietaken zijn vereist voordat de synchronisatie van de kopteksten en regels van verkoopoffertes kan plaatsvinden:</span><span class="sxs-lookup"><span data-stu-id="6629a-112">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="6629a-113">Producten (Fin en Ops naar Sales)</span><span class="sxs-lookup"><span data-stu-id="6629a-113">Products (Fin and Ops to Sales)</span></span>
- <span data-ttu-id="6629a-114">Rekeningen (Sales naar Fin and Ops) (indien gebruikt)</span><span class="sxs-lookup"><span data-stu-id="6629a-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
- <span data-ttu-id="6629a-115">Contactpersonen naar klanten (Sales naar Fin and Ops) (indien gebruikt)</span><span class="sxs-lookup"><span data-stu-id="6629a-115">Contacts to Customers (Sales to Fin and Ops) (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="6629a-116">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="6629a-116">Entity set</span></span>

| <span data-ttu-id="6629a-117">Verkoop</span><span class="sxs-lookup"><span data-stu-id="6629a-117">Sales</span></span>        | <span data-ttu-id="6629a-118">CDS</span><span class="sxs-lookup"><span data-stu-id="6629a-118">CDS</span></span>           | <span data-ttu-id="6629a-119">Finance en Operations</span><span class="sxs-lookup"><span data-stu-id="6629a-119">Finance and Operations</span></span>    |
|--------------|---------------|---------------------------|
| <span data-ttu-id="6629a-120">Citaten</span><span class="sxs-lookup"><span data-stu-id="6629a-120">Quotes</span></span>       | <span data-ttu-id="6629a-121">Offerte</span><span class="sxs-lookup"><span data-stu-id="6629a-121">Quotation</span></span>     | <span data-ttu-id="6629a-122">Kopteksten van verkoopoffertes</span><span class="sxs-lookup"><span data-stu-id="6629a-122">Sales quotation headers</span></span>   |
| <span data-ttu-id="6629a-123">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="6629a-123">QuoteDetails</span></span> | <span data-ttu-id="6629a-124">QuotationLine</span><span class="sxs-lookup"><span data-stu-id="6629a-124">QuotationLine</span></span> | <span data-ttu-id="6629a-125">Regels van CDS-verkoopofferte</span><span class="sxs-lookup"><span data-stu-id="6629a-125">CDS sales quotation lines</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="6629a-126">Entiteitstroom</span><span class="sxs-lookup"><span data-stu-id="6629a-126">Entity flow</span></span>

<span data-ttu-id="6629a-127">Verkoopoffertes worden gemaakt in Sales en gesynchroniseerd met Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6629a-127">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="6629a-128">Verkoopoffertes uit Sales worden alleen gesynchroniseerd als aan de volgende voorwaarden is voldaan:</span><span class="sxs-lookup"><span data-stu-id="6629a-128">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="6629a-129">Alle producten op de verkoopofferteregels worden extern beheerd.</span><span class="sxs-lookup"><span data-stu-id="6629a-129">All products on the sales quotation lines are externally maintained.</span></span>
- <span data-ttu-id="6629a-130">De verkoopofferte is actief of geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="6629a-130">The sales quotation is active or activated.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="6629a-131">Oplossing Prospect naar contant geld voor Sales</span><span class="sxs-lookup"><span data-stu-id="6629a-131">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="6629a-132">Het veld **Heeft alleen extern onderhouden producten** is toegevoegd aan de offerte-entiteit om consistent bij te houden of de verkoopofferte geheel bestaat uit extern beheerde producten.</span><span class="sxs-lookup"><span data-stu-id="6629a-132">The **Has Externally Maintained Products Only** field has been added to the Quote entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="6629a-133">Als een verkoopofferte alleen extern beheerde producten heeft, worden de producten beheerd in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6629a-133">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="6629a-134">Zo garandeert u dat u niet verkoopofferteregels probeert te synchroniseren voor producten die onbekend zijn in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6629a-134">This behavior helps guarantee that you don't try to synchronize sales quotation lines with products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="6629a-135">Alle producten en regels op de offerte worden bijgewerkt met de informatie **Heeft alleen extern onderhouden producten** uit de offertekoptekst.</span><span class="sxs-lookup"><span data-stu-id="6629a-135">All products and lines on the quotation are updated with the **Has Externally Maintained Products Only** information from the quotation header.</span></span> <span data-ttu-id="6629a-136">Deze informatie vindt u in het veld **Offerte heeft alleen extern onderhouden producten** op de offerteregelentiteit.</span><span class="sxs-lookup"><span data-stu-id="6629a-136">This information can be found in the **Quote Has Externally Maintained Products Only** field on the Quote line entity.</span></span>

<span data-ttu-id="6629a-137">De velden **Korting**, **Toeslagen** en **Btw** worden bepaald door een complexe configuratie in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6629a-137">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="6629a-138">Deze instellingen ondersteunen momenteel geen integratietoewijzing.</span><span class="sxs-lookup"><span data-stu-id="6629a-138">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="6629a-139">In het huidige ontwerp worden de velden **Prijs**, **Korting**, **Toeslagen** en **Btw** beheerd en verwerkt door Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6629a-139">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are mastered and handled by Finance and Operations.</span></span>

<span data-ttu-id="6629a-140">In Sales worden de volgende velden alleen-lezen gemaakt, omdat de waarden niet worden gesynchroniseerd met Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="6629a-140">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="6629a-141">**Alleen-lezen velden in de koptekst van de verkoopofferte:** Kortingspercentage, Korting, Vrachtkosten</span><span class="sxs-lookup"><span data-stu-id="6629a-141">**Read-only fields on the sales quotation header:** Discount %, Discount, Freight Amount</span></span>
- <span data-ttu-id="6629a-142">**Alleen-lezen velden op de verkoopofferteregels:** Btw</span><span class="sxs-lookup"><span data-stu-id="6629a-142">**Read-only fields on sales quotation lines:** Tax</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="6629a-143">Voorwaarden en instellingen voor toewijzing</span><span class="sxs-lookup"><span data-stu-id="6629a-143">Preconditions and mapping setup</span></span>

<span data-ttu-id="6629a-144">Voordat u verkooporders synchroniseert, is het belangrijk de systemen bij te werken met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="6629a-144">Before synchronizing sales orders, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="6629a-145">Instellingen in Sales</span><span class="sxs-lookup"><span data-stu-id="6629a-145">Setup in Sales</span></span>

- <span data-ttu-id="6629a-146">Ga naar **Instellingen** &gt; **Beheer** &gt; **Systeeminstellingen** &gt; **Sales** en controleer of het veld **Berekeningsmethode korting** is ingesteld op **Per eenheid**.</span><span class="sxs-lookup"><span data-stu-id="6629a-146">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the **Discount calculation method** field is set to **Per unit**.</span></span> <span data-ttu-id="6629a-147">Deze instelling zorgt ervoor dat de regelitemkorting uit Sales overeenkomt met de instelling in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6629a-147">This setting helps guarantee that the line item discount from Sales matches the setting in Finance and Operations.</span></span> <span data-ttu-id="6629a-148">Anders is de korting niet juist in Finance and Operations, omdat Finance and Operations de korting leest als korting per eenheid zelfs als dit een korting per regel is in Sales.</span><span class="sxs-lookup"><span data-stu-id="6629a-148">Otherwise, the discount won't be correct in Finance and Operations, because Finance and Operations will read the discount as a per-unit discount even if it was a per-line discount in Sales.</span></span>

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="6629a-149">Instellingen In Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6629a-149">Setup in Finance and Operations</span></span>

- <span data-ttu-id="6629a-150">Ga naar **Klanten** &gt; **Instellingen** &gt; **Parameters van module Klanten**.</span><span class="sxs-lookup"><span data-stu-id="6629a-150">Go to **Accounts receivable** &gt; **Setup** &gt; **Account receivable parameters**.</span></span> <span data-ttu-id="6629a-151">Selecteer op het tabblad **Nummerreeks** de nummerreeks voor verkoopoffertes en klik vervolgens op **Details weergeven**.</span><span class="sxs-lookup"><span data-stu-id="6629a-151">On the **Number sequence** tab, select the number sequence for sales quotations, and then click **View details**.</span></span> <span data-ttu-id="6629a-152">Stel vervolgens onder **Algemene instelling** het veld **Handmatig** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="6629a-152">Then, under **General Setup**, set the **Manual** field to **Yes**.</span></span>
- <span data-ttu-id="6629a-153">Ga naar **Klanten** &gt; **Instellingen** &gt; **Parameters van module Klanten**.</span><span class="sxs-lookup"><span data-stu-id="6629a-153">Go to **Accounts receivable** &gt; **Setup** &gt; **Accounts receivable parameters**.</span></span> <span data-ttu-id="6629a-154">Stel vervolgens op het tabblad **Zendingen** het veld **Controle leveringsdatum** in op **Geen**.</span><span class="sxs-lookup"><span data-stu-id="6629a-154">Then, on the **Shipments** tab, set the **Delivery date control** field to **None**.</span></span> <span data-ttu-id="6629a-155">Met deze instelling voorkomt u dat de synchronisatie voor verkoopoffertes mislukt.</span><span class="sxs-lookup"><span data-stu-id="6629a-155">This setting helps prevent synchronization from failing for sales quotations.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="6629a-156">Instellingen in het project Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="6629a-156">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="6629a-157">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="6629a-157">QuoteHeader</span></span>

- <span data-ttu-id="6629a-158">Het veld **Gevraagde leveringsdatum** is vereist in Finance and Operations en de synchronisatie mislukt als u het veld leeg laat.</span><span class="sxs-lookup"><span data-stu-id="6629a-158">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="6629a-159">Om dit te voorkomen wordt een standaard datum opgehaald uit **Bron &gt; CDS** als het veld leeg is.</span><span class="sxs-lookup"><span data-stu-id="6629a-159">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="6629a-160">De datum moet worden bijgewerkt met een voorkeurswaarde.</span><span class="sxs-lookup"><span data-stu-id="6629a-160">The date should be updated to a preferred value.</span></span> <span data-ttu-id="6629a-161">Momenteel kunt u geen waarde invoeren als **Vandaag** om de datum van vandaag aan te geven.</span><span class="sxs-lookup"><span data-stu-id="6629a-161">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="6629a-162">U moet een specifieke datum opgeven.</span><span class="sxs-lookup"><span data-stu-id="6629a-162">You must enter a specific date.</span></span> <span data-ttu-id="6629a-163">De standaardwaarde van de sjabloon voor **Gevraagde leveringsdatum** is **1/1/2020**.</span><span class="sxs-lookup"><span data-stu-id="6629a-163">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="6629a-164">Het veld **Land-regiocode adres** is vereist in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6629a-164">The **Address Country region code** field is required in Finance and Operations.</span></span> <span data-ttu-id="6629a-165">Om synchronisatiefouten te voorkomen kunt u een standaardwaarde opgeven die wordt gebruikt als het veld is leeg in Sales.</span><span class="sxs-lookup"><span data-stu-id="6629a-165">To help prevent synchronization errors, you can specify a default value that is used if the field is left blank in Sales.</span></span> <span data-ttu-id="6629a-166">Deze standaardwaarde is ook handig, omdat u niet handmatig een waarde hoeft in te voeren in het veld **Land/regio** voor lokale adressen.</span><span class="sxs-lookup"><span data-stu-id="6629a-166">This default value is also useful, because you don't have to manually enter a value in the **Country region** field for local addresses.</span></span> <span data-ttu-id="6629a-167">Er is geen standaardwaarde in de sjabloon voor **DeliveryAddressCountryRegionISOCode**.</span><span class="sxs-lookup"><span data-stu-id="6629a-167">There is no default template value for **DeliveryAddressCountryRegionISOCode**.</span></span>
- <span data-ttu-id="6629a-168">Werk de toewijzing voor **CDS-organisatie-id** bij in **Bron &gt; CDS** zodat deze overeenkomt met **CDS-organisatie** in de Organisatie-eenheid:</span><span class="sxs-lookup"><span data-stu-id="6629a-168">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="6629a-169">De standaardwaarde van de sjabloon voor **Organization_OrganizationId** is **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="6629a-169">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="6629a-170">De standaardwaarde van de sjabloon voor **Account_Organization_OrganizationId** is **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="6629a-170">The default template value for **Account_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="6629a-171">De standaardwaarde van de sjabloon voor **InvoiceAccount_OrganizationId** is **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="6629a-171">The default template value for **InvoiceAccount_OrganizationId** is **ORG001**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="6629a-172">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="6629a-172">QuoteLine</span></span>

- <span data-ttu-id="6629a-173">Werk de toewijzing voor **CDS-organisatie-id** bij in **Bron &gt; CDS** zodat deze overeenkomt met **CDS-organisatie** in de Organisatie-eenheid:</span><span class="sxs-lookup"><span data-stu-id="6629a-173">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="6629a-174">De standaardwaarde van de sjabloon voor **Organization_OrganizationId** is **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="6629a-174">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="6629a-175">De standaardwaarde van de sjabloon voor **Product_Organization_Organization_OrganizationId** is **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="6629a-175">The default template value for **Product_Organization_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="6629a-176">De standaardwaarde van de sjabloon voor **Quotation_Organization_Organization_OrganizationId** is **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="6629a-176">The default template value for **Quotation_Organization_Organization_OrganizationId** is **ORG001**.</span></span>

- <span data-ttu-id="6629a-177">Het veld **Gevraagde leveringsdatum** is vereist in Finance and Operations en de synchronisatie mislukt als u het veld leeg laat.</span><span class="sxs-lookup"><span data-stu-id="6629a-177">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="6629a-178">Om dit te voorkomen wordt een standaard datum opgehaald uit **Bron &gt; CDS** als het veld leeg is.</span><span class="sxs-lookup"><span data-stu-id="6629a-178">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="6629a-179">De datum moet worden bijgewerkt met een voorkeurswaarde.</span><span class="sxs-lookup"><span data-stu-id="6629a-179">The date should be updated to a preferred value.</span></span> <span data-ttu-id="6629a-180">Momenteel kunt u geen waarde invoeren als **Vandaag** om de datum van vandaag aan te geven.</span><span class="sxs-lookup"><span data-stu-id="6629a-180">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="6629a-181">U moet een specifieke datum opgeven.</span><span class="sxs-lookup"><span data-stu-id="6629a-181">You must enter a specific date.</span></span> <span data-ttu-id="6629a-182">De standaardwaarde van de sjabloon voor **Gevraagde leveringsdatum** is **1/1/2020**.</span><span class="sxs-lookup"><span data-stu-id="6629a-182">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="6629a-183">U kunt de volgende toewijzingen uit **CDS &gt; Bestemming** toevoegen om te garanderen dat offerteregels worden geïmporteerd in Finance and Operations als er geen standaardgegevens over de klant of het product zijn:</span><span class="sxs-lookup"><span data-stu-id="6629a-183">You can add the following mappings from **CDS &gt; Destination** to help guarantee that quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="6629a-184">**SiteId**: een site is vereist voor het genereren van offertes en verkooporderregels in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6629a-184">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="6629a-185">Er is geen standaardwaarde van de sjabloon voor **SiteId**.</span><span class="sxs-lookup"><span data-stu-id="6629a-185">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="6629a-186">**WarehouseId**: een magazijn is vereist voor het verwerken van offertes en verkooporderregels in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6629a-186">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="6629a-187">Er is geen standaardwaarde van de sjabloon voor **WarehouseId**.</span><span class="sxs-lookup"><span data-stu-id="6629a-187">There is no default template value for **WarehouseId**.</span></span>

- <span data-ttu-id="6629a-188">Zorg ervoor dat de vereiste waardetoewijzing voor de verkoopmaateenheid in Finance and Operations bestaat in de toewijzing **CDS &gt; Bestemming** voor **Quantity_UOM** naar **SALESUNITSYMBOL**.</span><span class="sxs-lookup"><span data-stu-id="6629a-188">Make sure that the required value map for the selling unit of measure (UOM) in Finance and Operations exists in the **CDS &gt; Destination** mapping for **Quantity_UOM** to **SALESUNITSYMBOL**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="6629a-189">Sjabloontoewijzing in gegevensintegrator</span><span class="sxs-lookup"><span data-stu-id="6629a-189">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="6629a-190">De velden **Korting**, **Toeslagen** en **Btw** worden bepaald door een complexe configuratie in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6629a-190">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="6629a-191">Deze instellingen ondersteunen momenteel geen integratietoewijzing.</span><span class="sxs-lookup"><span data-stu-id="6629a-191">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="6629a-192">In het huidige ontwerp worden de velden **Prijs**, **Korting**, **Toeslagen** en **Btw** verwerkt door Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6629a-192">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="6629a-193">De velden **Betalingsvoorwaarden**, **Leveringscondities**, **Leveringsvoorwaarden**, **Verzendmethode** en **Leveringsmethode** maken geen deel uit van de standaardtoewijzingen.</span><span class="sxs-lookup"><span data-stu-id="6629a-193">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="6629a-194">Als u deze velden wilt toewijzen, moet u een waardetoewijzing instellen die specifiek is voor de gegevens in de organisaties waartussen de entiteit wordt gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="6629a-194">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="6629a-195">In de volgende afbeeldingen ziet u een voorbeeld van de toewijzing van een sjabloon in gegevensintegrator.</span><span class="sxs-lookup"><span data-stu-id="6629a-195">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="6629a-196">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="6629a-196">QuoteHeader</span></span>

![Sjabloontoewijzing in gegevensintegrator](./media/sales-quotation-template-mapping-data-integrator-1.png)

![Sjabloontoewijzing in gegevensintegrator](./media/sales-quotation-template-mapping-data-integrator-2.png)

### <a name="quoteline"></a><span data-ttu-id="6629a-199">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="6629a-199">QuoteLine</span></span>

![Sjabloontoewijzing in gegevensintegrator](./media/sales-quotation-template-mapping-data-integrator-3.png)

![Sjabloontoewijzing in gegevensintegrator](./media/sales-quotation-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a><span data-ttu-id="6629a-202">Verwante onderwerpen</span><span class="sxs-lookup"><span data-stu-id="6629a-202">Related topics</span></span>

[<span data-ttu-id="6629a-203">Producten uit Finance and Operations synchroniseren met producten in Sales</span><span class="sxs-lookup"><span data-stu-id="6629a-203">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="6629a-204">Accounts in Sales synchroniseren met klanten in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6629a-204">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="6629a-205">Contactpersonen synchroniseren tussen Sales met contactpersonen of klanten in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6629a-205">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)



