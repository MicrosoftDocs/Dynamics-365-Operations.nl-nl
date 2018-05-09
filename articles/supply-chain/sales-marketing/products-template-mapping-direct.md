---
title: Producten vanuit Finance and Operations direct synchroniseren met producten in Sales
description: In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van producten vanuit Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Sales.
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 821ba4f0957d8bb84fc188c86895700631b46fed
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---

# <a name="synchronize-products-directly-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="5ddc3-103">Producten van Finance and Operations rechtstreeks synchroniseren met producten in Sales</span><span class="sxs-lookup"><span data-stu-id="5ddc3-103">Synchronize products directly from Finance and Operations to products in Sales</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="5ddc3-104">Voordat u de oplossing Prospect naar contant geld kunt gebruiken, moet u vertrouwd zijn met [Dynamics 365 Gegevensintegratie](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="5ddc3-104">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

<span data-ttu-id="5ddc3-105">In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het rechtstreeks synchroniseren van producten vanuit Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-105">This topic discusses the templates and underlying tasks that are used to synchronize products directly from Microsoft Dynamics 365 for Finance and Operations, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="5ddc3-106">Gegevensstroom in Prospect naar contant geld</span><span class="sxs-lookup"><span data-stu-id="5ddc3-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="5ddc3-107">De oplossing Prospect naar contant geld gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Finance and Operations en Sales.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="5ddc3-108">De Prospect naar contant geld-sjablonen die beschikbaar zijn in de functie Gegevensintegratie activeren de stroom van gegevens over rekeningen, contactpersonen, producten, verkoopoffertes en verkoopfacturen tussen Finance and Operations en Sales.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="5ddc3-109">De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Finance and Operations en Sales.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="5ddc3-110">[![Gegevensstroom in Prospect naar contant geld](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="5ddc3-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="5ddc3-111">Sjablonen en taken</span><span class="sxs-lookup"><span data-stu-id="5ddc3-111">Templates and tasks</span></span>

<span data-ttu-id="5ddc3-112">Open het [PowerApps-beheercentrum](https://preview.admin.powerapps.com/dataintegration) om toegang te krijgen tot de beschikbare sjablonen.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="5ddc3-113">Selecteer **Projecten** en selecteer vervolgens in de rechterbovenhoek de optie **Nieuw project** om openbare sjablonen te selecteren.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="5ddc3-114">De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van producten van Finance and Operations naar Sales.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-114">The following template and underlying tasks are used to synchronize products from Finance and Operations to Sales.</span></span>

- <span data-ttu-id="5ddc3-115">**Naam van de sjabloon in Gegevensintegratie:** Producten (Fin and Ops naar Sales) - Direct</span><span class="sxs-lookup"><span data-stu-id="5ddc3-115">**Name of the template in Data integration:** Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="5ddc3-116">**Naam van de taak in het project Gegevensintegratie:** Producten</span><span class="sxs-lookup"><span data-stu-id="5ddc3-116">**Name of the task in the Data integration project:** Products</span></span>

<span data-ttu-id="5ddc3-117">Er hoeven geen synchronisatietaken te worden uitgevoerd voordat productsynchronisatie kan plaatsvinden.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-117">No synchronization tasks are required before product synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="5ddc3-118">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="5ddc3-118">Entity set</span></span>

| <span data-ttu-id="5ddc3-119">Finance en Operations</span><span class="sxs-lookup"><span data-stu-id="5ddc3-119">Finance and Operations</span></span>     | <span data-ttu-id="5ddc3-120">Verkoop</span><span class="sxs-lookup"><span data-stu-id="5ddc3-120">Sales</span></span>    |
|----------------------------|----------|
| <span data-ttu-id="5ddc3-121">Verkoopbare vrijgegeven producten</span><span class="sxs-lookup"><span data-stu-id="5ddc3-121">Sellable released products</span></span> | <span data-ttu-id="5ddc3-122">Producten</span><span class="sxs-lookup"><span data-stu-id="5ddc3-122">Products</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="5ddc3-123">Entiteitstroom</span><span class="sxs-lookup"><span data-stu-id="5ddc3-123">Entity flow</span></span>

<span data-ttu-id="5ddc3-124">Producten worden beheerd in Finance and Operations en gesynchroniseeerd met Sales</span><span class="sxs-lookup"><span data-stu-id="5ddc3-124">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="5ddc3-125">Met de gegevensentiteit **Verkoopbare vrijgegeven producten** in Finance and Operations worden alleen producten geëxporteerd die *verkoopbaar* zijn.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-125">The **Sellable released products** data entity in Finance and Operations exports only products that are *sellable*.</span></span> <span data-ttu-id="5ddc3-126">Verkoopbare producten zijn producten die de informatie bevatten die ze nodig hebben om te kunnen worden gebruikt op een verkooporder.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-126">Sellable products are products that have the information that they require in order to be used on a sales order.</span></span> <span data-ttu-id="5ddc3-127">Dezelfde regels zijn van toepassing wanneer een product wordt gevalideerd met de functie **Valideren** op de pagina **Vrijgegeven product**.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-127">The same rules apply when a product is validated by using the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="5ddc3-128">Het productnummer wordt gebruikt als een sleutel.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-128">The product number is used as a key.</span></span> <span data-ttu-id="5ddc3-129">Dus wanneer productvarianten worden gesynchroniseerd naar Sales, heeft elke productvariant een afzonderlijke product-id.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-129">Therefore, when product variants are synchronized to Sales, each product variant has an individual product ID.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="5ddc3-130">Oplossing Prospect naar contant geld voor Sales</span><span class="sxs-lookup"><span data-stu-id="5ddc3-130">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="5ddc3-131">In Sales is het nieuwe veld **Wordt extern beheerd** voor producten toegevoegd om aan te geven dat een bepaald product extern wordt beheerd.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-131">In Sales, a new **Is Externally Maintained** field has been added on products to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="5ddc3-132">Standaard wordt de waarde ingesteld op **Ja** tijdens het importeren naar Sales.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-132">By default, the value is set to **Yes** during an import to Sales.</span></span> <span data-ttu-id="5ddc3-133">De volgende waarden zijn beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="5ddc3-133">The following values are available:</span></span>

- <span data-ttu-id="5ddc3-134">**Ja**: het product is afkomstig uit Finance and Operations en kan niet worden bewerkt in Sales.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-134">**Yes** – The product originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="5ddc3-135">**Nee**: het product is rechtstreeks in Sales ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-135">**No** – The product was entered directly in Sales.</span></span>
- <span data-ttu-id="5ddc3-136">**(Leeg)**: het product bestond in Sales voordat de oplossing Prospect naar contant geld werd ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-136">**(Blank)** – The product existed in Sales before the Prospect to cash solution was enabled.</span></span>

<span data-ttu-id="5ddc3-137">Met het veld **Wordt extern beheerd** kunt u ervoor zorgen dat alleen offertes en verkooporders met extern onderhouden producten worden gesynchroniseerd naar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-137">The **Is Externally Maintained** field helps guarantee that only quotations and sales orders that have externally maintained products will be synchronized to Finance and Operations.</span></span>

<span data-ttu-id="5ddc3-138">Extern onderhouden producten worden automatisch toegevoegd aan de eerste geldige prijslijst met dezelfde valuta.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-138">Externally maintained products are automatically added to the first valid price list that has the same currency.</span></span> <span data-ttu-id="5ddc3-139">Prijslijsten worden alfabetisch op naam ingedeeld.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-139">Price lists are organized alphabetically by name.</span></span> <span data-ttu-id="5ddc3-140">De verkoopprijs van het product uit Finance and Operations wordt gebruikt als de prijs in de prijslijst.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-140">The product sales price from Finance and Operations is used as the price on the price list.</span></span> <span data-ttu-id="5ddc3-141">Daarom moet er een prijslijst in Sales bestaan voor elke productverkoopvaluta in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-141">Therefore, there must be a price list in Sales for every product sales currency in Finance and Operations.</span></span> <span data-ttu-id="5ddc3-142">De valuta voor de vrijgegeven verkoopbare producten wordt ingesteld op de boekhoudvaluta van de rechtspersoon waaruit het product wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-142">The currency on the released sellable products is set to the accounting currency in the legal entity that the product is exported from.</span></span>

> [!NOTE]
> <span data-ttu-id="5ddc3-143">Productsynchronisatie lukt alleen als er een prijslijst met een overeenkomende valuta is.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-143">Product synchronization won't succeed unless there is a price list that has a matching currency.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="5ddc3-144">Voorwaarden en instellingen voor toewijzing</span><span class="sxs-lookup"><span data-stu-id="5ddc3-144">Preconditions and mapping setup</span></span>

- <span data-ttu-id="5ddc3-145">Voordat u de synchronisatie voor het eerst uitvoert, vult u de tabel Verschillend product voor bestaande producten in Finance and Operations in.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-145">Before you run the synchronization for the first time, you must fill the Distinct product table for existing products in Finance and Operations.</span></span> <span data-ttu-id="5ddc3-146">Bestaande producten worden pas gesynchroniseerd als deze taak is voltooid.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-146">Existing products won't be synchronized until this job is completed.</span></span>

    1. <span data-ttu-id="5ddc3-147">Gebruik in Finance and Operations de zoekfunctie om te zoeken naar **Tabel met verschillende producten vullen**.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-147">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>
    2. <span data-ttu-id="5ddc3-148">Selecteer **Tabel met verschillende producten vullen** om de taak uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-148">Select **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="5ddc3-149">Deze taak moet slechts één keer worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-149">This job must be run only one time.</span></span>

- <span data-ttu-id="5ddc3-150">Zorg ervoor dat de vereiste waardetoewijzing voor de verkoopmaateenheid tussen Finance and Operations en Sales bestaat in de toewijzing van **SalesUnitSymbol** naar **DefaultUnit (Name)**.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-150">Make sure that the required value map for the selling unit of measure (UOM) between Finance and Operations and Sales exists in the mapping of **SalesUnitSymbol** to **DefaultUnit (Name)**.</span></span>
- <span data-ttu-id="5ddc3-151">Werk de waardetoewijzing bij voor **Eenhedengroep** (**defaultuomscheduleid.name**) zodat deze overeenkomt met **Eenhedengroepen** in Sales.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-151">Update the value map for **Unit group** (**defaultuomscheduleid.name**) so that it matches **Unit groups** in Sales.</span></span>

    <span data-ttu-id="5ddc3-152">De standaardsjabloonwaarde is **Standaardmaateenheid**.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-152">The default template value is **Default unit**.</span></span>

- <span data-ttu-id="5ddc3-153">Controleer of de verkoopmaateenheden voor alle producten uit Finance and Operations bestaan in Sales.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-153">Make sure that the selling UOMs for all products from Finance and Operations exist in Sales.</span></span>
- <span data-ttu-id="5ddc3-154">Controleer of prijslijsten bestaan in Sales voor elke productverkoopvaluta in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-154">Make sure that price lists exist in Sales for every product sales currency in Finance and Operations.</span></span>
- <span data-ttu-id="5ddc3-155">Wanneer producten worden gemaakt in Sales, kunnen ze de status **Concept** of **Actief** hebben.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-155">When products are created in Sales, they can have a status of **Draft** or **Active**.</span></span> <span data-ttu-id="5ddc3-156">Het gedrag wordt beheerd via **Instellingen** > **Beheer** > **Systeeminstellingen** > **Sales** in Sales.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-156">The behavior is controlled at **Settings** > **Administration** > **System settings** > **Sales** in Sales.</span></span>

    <span data-ttu-id="5ddc3-157">Producten die de status **Concept** hebben wanneer ze worden gemaakt, moeten worden geactiveerd voordat ze kunnen worden toegevoegd aan offertes of verkooporders.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-157">Products that have **Draft** status when they are created must be activated before they can be added to quotations or sales orders.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="5ddc3-158">Sjabloontoewijzing in Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="5ddc3-158">Template mapping in Data integration</span></span>

<span data-ttu-id="5ddc3-159">In de volgende afbeelding ziet u een voorbeeld van sjabloontoewijzing in Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-159">The following illustration shows an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="5ddc3-160">Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Sales naar Finance and Operations worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-160">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

![Sjabloontoewijzing in Gegevensintegrator](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a><span data-ttu-id="5ddc3-162">Verwante onderwerpen</span><span class="sxs-lookup"><span data-stu-id="5ddc3-162">Related topics</span></span>

[<span data-ttu-id="5ddc3-163">Prospect naar contant geld</span><span class="sxs-lookup"><span data-stu-id="5ddc3-163">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="5ddc3-164">Rekeningen in Sales direct synchroniseren naar klanten in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5ddc3-164">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="5ddc3-165">Contactpersonen vanuit Sales direct synchroniseren naar contactpersonen of klanten in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5ddc3-165">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="5ddc3-166">Kopteksten en regels in verkooporders rechtstreeks synchroniseren vanuit Finance and Operations naar Sales</span><span class="sxs-lookup"><span data-stu-id="5ddc3-166">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="5ddc3-167">Kopteksten en regels in verkoopfacturen direct vanuit Finance and Operations synchroniseren naar Sales</span><span class="sxs-lookup"><span data-stu-id="5ddc3-167">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)




