---
title: Producten uit Finance and Operations synchroniseren met producten in Sales
description: In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van producten tussen Microsoft Dynamics 365 for Finance and Operations, Enterprise edition en Microsoft Dynamics 365 for Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 07/03/2017
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
ms.author: ChristianRytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 2f14b06b57930256f9211f2085512aa589df083e
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-products-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="c8ed3-103">Producten uit Finance and Operations synchroniseren met producten in Sales</span><span class="sxs-lookup"><span data-stu-id="c8ed3-103">Synchronize products from Finance and Operations to products in Sales</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="c8ed3-104">Voordat u de oplossing Prospect naar contant geld kunt gebruiken, moet u vertrouwd zijn met de functie [Dynamics 365 Gegevensintegratie](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="c8ed3-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="c8ed3-105">In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van producten tussen Microsoft Dynamics 365 for Finance and Operations, Enterprise edition en Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="c8ed3-105">This topic discusses the templates and underlying tasks that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="template-and-task"></a><span data-ttu-id="c8ed3-106">Sjabloon en taak</span><span class="sxs-lookup"><span data-stu-id="c8ed3-106">Template and task</span></span>

<span data-ttu-id="c8ed3-107">De volgende sjablonen en onderliggende taken worden gebruikt voor het synchroniseren van producten tussen Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations) en Microsoft Dynamics 365 for Sales (Sales).</span><span class="sxs-lookup"><span data-stu-id="c8ed3-107">The following templates and underlying tasks are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations) to Microsoft Dynamics 365 for Sales (Sales).</span></span>

-   <span data-ttu-id="c8ed3-108">Naam van de sjabloon: Producten (Fin and Ops naar Sales)</span><span class="sxs-lookup"><span data-stu-id="c8ed3-108">Name of template: Products (Fin and Ops to Sales)</span></span>

-   <span data-ttu-id="c8ed3-109">Naam van taak in project: Producten</span><span class="sxs-lookup"><span data-stu-id="c8ed3-109">Name of task in project: Products</span></span>

<span data-ttu-id="c8ed3-110">Taken die nodig zijn voor het synchroniseren van product: geen</span><span class="sxs-lookup"><span data-stu-id="c8ed3-110">Sync tasks required prior to Product sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="c8ed3-111">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="c8ed3-111">Entity set</span></span>

| <span data-ttu-id="c8ed3-112">**Finance and Operations**</span><span class="sxs-lookup"><span data-stu-id="c8ed3-112">**Finance and Operations**</span></span> | <span data-ttu-id="c8ed3-113">**CDS**</span><span class="sxs-lookup"><span data-stu-id="c8ed3-113">**CDS**</span></span> | <span data-ttu-id="c8ed3-114">**Verkoop**</span><span class="sxs-lookup"><span data-stu-id="c8ed3-114">**Sales**</span></span>  |
|----------------------------|---------|------------|
| <span data-ttu-id="c8ed3-115">Verkoopbare vrijgegeven producten</span><span class="sxs-lookup"><span data-stu-id="c8ed3-115">Sellable released products</span></span> | <span data-ttu-id="c8ed3-116">Artikel</span><span class="sxs-lookup"><span data-stu-id="c8ed3-116">Product</span></span> | <span data-ttu-id="c8ed3-117">Producten</span><span class="sxs-lookup"><span data-stu-id="c8ed3-117">Products</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="c8ed3-118">Entiteitstroom</span><span class="sxs-lookup"><span data-stu-id="c8ed3-118">Entity flow</span></span>

<span data-ttu-id="c8ed3-119">Producten worden beheerd in Finance and Operations en gesynchroniseeerd met Sales</span><span class="sxs-lookup"><span data-stu-id="c8ed3-119">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="c8ed3-120">De gegevensentiteit **Verkoopbare vrijgegeven producten** in Finance and Operations exporteert alleen producten die verkoopbaar zijn, wat betekent dat de producten de informatie bevatten die nodig is om te worden gebruikt op een verkooporder.</span><span class="sxs-lookup"><span data-stu-id="c8ed3-120">The data entity **Sellable released products** in Finance and Operations only exports products that are sellable, which means that products have the information required to be used on a sales order.</span></span> <span data-ttu-id="c8ed3-121">Dezelfde regels zijn van toepassing wanneer een product wordt gevalideerd met de functie **Valideren** op de pagina **Vrijgegeven product**.</span><span class="sxs-lookup"><span data-stu-id="c8ed3-121">The same rules apply when a product is validated with the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="c8ed3-122">Het **Productnummer** wordt gebruikt als sleutel, wat betekent dat productvarianten met CDS en Sales worden gesynchroniseerd met afzonderlijke **product-id's** per **productvariant**.</span><span class="sxs-lookup"><span data-stu-id="c8ed3-122">The **Product number** is used as key, meaning that product variants are synchronized to CDS and Sales with individual **Product IDs** per **Product variant**.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="c8ed3-123">Oplossing Prospect naar contant geld voor Sales</span><span class="sxs-lookup"><span data-stu-id="c8ed3-123">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="c8ed3-124">In Sales wordt een nieuw veld **Wordt extern beheerd** voor de producten toegevoegd om aan te geven dat een bepaald product extern wordt beheerd.</span><span class="sxs-lookup"><span data-stu-id="c8ed3-124">In Sales, a new field on the products **Is Externally Maintained** is added to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="c8ed3-125">De waarde wordt standaard ingesteld op **Ja** tijdens het importeren in Sales.</span><span class="sxs-lookup"><span data-stu-id="c8ed3-125">The value is set to **Yes** by default during import to Sales.</span></span>

-   <span data-ttu-id="c8ed3-126">**Wordt extern beheerd = Ja**: product is afkomstig uit Finance and Operations en kan niet worden bewerkt in Sales.</span><span class="sxs-lookup"><span data-stu-id="c8ed3-126">**Is Externally Maintained = Yes**: Product originates from Finance and Operations and will not be editable in Sales.</span></span>

-   <span data-ttu-id="c8ed3-127">**Wordt extern beheerd = Nee**: product wordt rechtstreeks ingevoerd in Sales.</span><span class="sxs-lookup"><span data-stu-id="c8ed3-127">**Is Externally Maintained = No**: Product is entered directly in Sales.</span></span>

-   <span data-ttu-id="c8ed3-128">**Wordt extern beheerd = blanco**: product bestaat in Sales vóór het inschakelen van de oplossing Prospect naar contant geld.</span><span class="sxs-lookup"><span data-stu-id="c8ed3-128">**Is Externally Maintained = Blank**: Product exists in Sales prior to enabling the Prospect to cash solution.</span></span>

<span data-ttu-id="c8ed3-129">De gegevens van **Wordt extern beheerd** worden gebruikt om ervoor te zorgen dat alleen **offertes** en **verkooporders** met **extern onderhouden producten** worden gesynchroniseerd met Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c8ed3-129">The **Is Externally Maintained** information is used to ensure that only **Quotes** and **Sales orders** with **Externally maintained products** will sync to Finance and Operations.</span></span>

<span data-ttu-id="c8ed3-130">**Extern onderhouden producten** worden automatisch toegevoegd aan de eerste geldige **prijslijst** met dezelfde valuta.</span><span class="sxs-lookup"><span data-stu-id="c8ed3-130">**Externally maintained products** are automatically added to the first valid **Price list** with the same currency.</span></span> <span data-ttu-id="c8ed3-131">Houd er rekening mee dat de lijst alfabetisch is ingedeeld op **Naam**.</span><span class="sxs-lookup"><span data-stu-id="c8ed3-131">Note that the list is organized alphabetically by **Name**.</span></span> <span data-ttu-id="c8ed3-132">De verkoopprijs van het product van Finance and Operations wordt gebruikt als prijs op de **prijslijst**.</span><span class="sxs-lookup"><span data-stu-id="c8ed3-132">The product sales price from Finance and Operations is used as price on the **Price list**.</span></span> <span data-ttu-id="c8ed3-133">Dit houdt in dat er in Sales een **prijslijst** moet zijn voor elke **productverkoopvaluta** in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c8ed3-133">This means that it is required to have a **Price list** in Sales for each **Product sales currency** in Finance and Operations.</span></span> <span data-ttu-id="c8ed3-134">Valuta op de vrijgegeven verkoopbare producten wordt ingesteld op de boekhoudvaluta van de rechtspersoon, waaruit het product wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="c8ed3-134">Currency on the released sellable products is set to the accounting currency in the legal entity, from which the product is exported.</span></span>

> [!NOTE]
> <span data-ttu-id="c8ed3-135">Productsynchronisatie mislukt zonder een **prijslijst** met de overeenkomende valuta.</span><span class="sxs-lookup"><span data-stu-id="c8ed3-135">Product sync will not succeed without a **Price list** with the matching currency.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="c8ed3-136">Voorwaarden en instellingen voor toewijzing</span><span class="sxs-lookup"><span data-stu-id="c8ed3-136">Preconditions and mapping setup</span></span>

-   <span data-ttu-id="c8ed3-137">Voordat u de allereerste synchronisatie uitvoert, vult u de **tabel Verschillend product** voor bestaande producten in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c8ed3-137">Before you run the very first sync, you must populate the **Distinct product table** for existing products in Finance and Operations.</span></span> <span data-ttu-id="c8ed3-138">Bestaande producten worden niet gesynchroniseerd totdat deze taak is voltooid.</span><span class="sxs-lookup"><span data-stu-id="c8ed3-138">Existing products will not be synchronized until this job is completed.</span></span>

    -   <span data-ttu-id="c8ed3-139">Gebruik in Finance and Operations de zoekfunctie om te zoeken naar **Tabel met verschillende producten vullen**.</span><span class="sxs-lookup"><span data-stu-id="c8ed3-139">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>

    -   <span data-ttu-id="c8ed3-140">Klik op **Tabel met verschillende producten vullen** om de taak uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="c8ed3-140">Click the **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="c8ed3-141">Deze taak hoeft slechts één keer te worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="c8ed3-141">This job only needs to be run once.</span></span>

-   <span data-ttu-id="c8ed3-142">Controleer of de benodigde **ValueMap** voor **Maateenheid** voor verkopen voorkomt in Finance and Operations in **Bron \> CDS-toewijzing SalesUnitSymbol / DefaultSellingUnitOfMeasure**.</span><span class="sxs-lookup"><span data-stu-id="c8ed3-142">Ensure that the needed **ValueMap** for selling **Unit of measure** (UOM) in Finance and Operations exists in the **Source -\> CDS mapping SalesUnitSymbol / DefaultSellingUnitOfMeasure**.</span></span>

-   <span data-ttu-id="c8ed3-143">Controleer of **Ondersteunde decimalen** voor maateenheid overeenkomen met uw vereisten in **CDS \> Bestemming**.</span><span class="sxs-lookup"><span data-stu-id="c8ed3-143">Ensure that **Decimals supported** for UOM match your requirements in **CDS -\> Destination**.</span></span> <span data-ttu-id="c8ed3-144">Als u verschillende waarden per maateenheid nodig hebt, kunt u dit doen met **ValueMap** van Eenheid, bijvoorbeeld [Elk: 0] & [Pond: 2].</span><span class="sxs-lookup"><span data-stu-id="c8ed3-144">If you require different values per UOM, this can be done with **ValueMap** from Unit, for example, [Each : 0] & [Pound : 2].</span></span>

    -   <span data-ttu-id="c8ed3-145">De standaardsjabloonwaarde is 0.</span><span class="sxs-lookup"><span data-stu-id="c8ed3-145">Template value is defaulted to 0.</span></span>

-   <span data-ttu-id="c8ed3-146">Werk de **CDS-organisatie-id Organization_OrganizationId** bij in **Bron -\> CDS**.</span><span class="sxs-lookup"><span data-stu-id="c8ed3-146">Update the **CDS Organization ID Organization_OrganizationId** in **Source -\> CDS**.</span></span>

    -   <span data-ttu-id="c8ed3-147">De standaardsjabloonwaarde is ORG001.</span><span class="sxs-lookup"><span data-stu-id="c8ed3-147">Template value is defaulted to ORG001.</span></span>

-   <span data-ttu-id="c8ed3-148">Werk **ValueMap** bij voor **Eenhedengroep** (**defaultuomscheduleid.name**) in **CDS \> Bestemming** zodat deze overenkomt met de **Eenhedengroepen** in Sales.</span><span class="sxs-lookup"><span data-stu-id="c8ed3-148">Update **ValueMap** for **Unit group** (**defaultuomscheduleid.name**) in **CDS -\> Destination** to match the **Unit groups** in Sales.</span></span>

    -   <span data-ttu-id="c8ed3-149">De standaardsjabloonwaarde is ingesteld op **Standaardmaateenheid**.</span><span class="sxs-lookup"><span data-stu-id="c8ed3-149">Template value is defaulted to **Default unit**.</span></span>

-   <span data-ttu-id="c8ed3-150">Controleer of alle verkoopmaateenheden voor producten van Finance and Operations bestaan in Sales met de waarde **CDS-selectielijsten**.</span><span class="sxs-lookup"><span data-stu-id="c8ed3-150">Ensure that all products selling UOMs from Finance and Operations exist in Sales with the **CDS picklists** value.</span></span>

-   <span data-ttu-id="c8ed3-151">Controleer of **Prijslijsten** bestaan in Sales voor elke productverkoopvaluta in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c8ed3-151">Ensure that **Price lists** exist in Sales for each product sales currency in Finance and Operations.</span></span>

-   <span data-ttu-id="c8ed3-152">Producten kunnen worden gemaakt in Sales met de status **Concept** of **Actief**.</span><span class="sxs-lookup"><span data-stu-id="c8ed3-152">Products can be created in Sales with status **Draft** or **Active**.</span></span> <span data-ttu-id="c8ed3-153">Dit wordt bepaald in **Systeeminstellingen** onder **Sales** in Sales.</span><span class="sxs-lookup"><span data-stu-id="c8ed3-153">This is controlled in **System settings** under **Sales** in Sales.</span></span>

    -   <span data-ttu-id="c8ed3-154">Producten die zijn gemaakt met de conceptstatus moeten worden geactiveerd voordat ze kunnen worden toegevoegd aan **Offerte** of **Verkooporder**.</span><span class="sxs-lookup"><span data-stu-id="c8ed3-154">Products created with draft status need to be activated before they can be added to **Quote** or **Sales order**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="c8ed3-155">Sjabloontoewijzing in gegevensintegrator</span><span class="sxs-lookup"><span data-stu-id="c8ed3-155">Template mapping in data integrator</span></span>

<span data-ttu-id="c8ed3-156">In de volgende afbeeldingen ziet u een voorbeeld van de toewijzing van een sjabloon in gegevensintegrator.</span><span class="sxs-lookup"><span data-stu-id="c8ed3-156">The following illustrations show an example of a template mapping in data integrator.</span></span>

![sjabloontoewijzing in gegevensintegrator](./media/products-template-mapping-data-integrator-1.png)

![sjabloontoewijzing voor producten in gegevensintegrator](./media/products-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="c8ed3-159">Verwante onderwerpen</span><span class="sxs-lookup"><span data-stu-id="c8ed3-159">Related topics</span></span>

[<span data-ttu-id="c8ed3-160">Rekeningen uit Sales synchroniseren met klanten in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c8ed3-160">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="c8ed3-161">Contactpersonen synchroniseren tussen Sales met contactpersonen of klanten in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c8ed3-161">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="c8ed3-162">Kopteksten en regels van verkoopofferte synchroniseren tussen Sales en Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c8ed3-162">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)


