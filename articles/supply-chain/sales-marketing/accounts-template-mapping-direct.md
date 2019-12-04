---
title: Rekeningen rechtstreeks vanuit Sales synchroniseren met klanten in Supply Chain Management
description: Dit onderwerp bespreekt de sjablonen en onderliggende taken die worden gebruikt om rekeningen rechtstreeks te synchroniseren van Dynamics 365 Sales naar Supply Chain Management.
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: ebca416e94f44d0448a4f4d0be08f13e30e749e9
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813219"
---
# <a name="synchronize-accounts-directly-from-sales-to-customers-in-supply-chain-management"></a><span data-ttu-id="a6d8a-103">Rekeningen rechtstreeks vanuit Sales synchroniseren met klanten in Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="a6d8a-103">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="a6d8a-104">Voordat u de oplossing Prospect naar contant geld kunt gebruiken, moet u vertrouwd zijn met [Gegevens integreren in Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="a6d8a-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="a6d8a-105">Dit onderwerp bespreekt de sjablonen en onderliggende taken die worden gebruikt om rekeningen rechtstreeks te synchroniseren van Dynamics 365 Sales naar Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-105">This topic discusses the templates and underlying tasks that are used to synchronize accounts directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="a6d8a-106">Gegevensstroom in Prospect naar contant geld</span><span class="sxs-lookup"><span data-stu-id="a6d8a-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="a6d8a-107">De oplossing Prospect naar contant geld gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Supply Chain Management en Sales.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span>  <span data-ttu-id="a6d8a-108">De Prospect naar contant geld-sjablonen die beschikbaar zijn in de functie Gegevensintegratie activeren de stroom van gegevens over rekeningen, contactpersonen, producten, verkoopoffertes en verkoopfacturen tussen Supply Chain Management en Sales.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="a6d8a-109">De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Supply Chain Management en Sales.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="a6d8a-110">[![Gegevensstroom in Prospect naar contant geld](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="a6d8a-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="a6d8a-111">Sjablonen en taken</span><span class="sxs-lookup"><span data-stu-id="a6d8a-111">Templates and tasks</span></span>

<span data-ttu-id="a6d8a-112">Open het [Power Apps-beheercentrum](https://preview.admin.powerapps.com/dataintegration) om toegang te krijgen tot de beschikbare sjablonen.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-112">To access the available templates, open [Power Apps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="a6d8a-113">Selecteer **Projecten** en selecteer vervolgens in de rechterbovenhoek de optie **Nieuw project** om openbare sjablonen te selecteren.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="a6d8a-114">De volgende sjabloon en onderliggende taak worden gebruikt voor het synchroniseren van rekeningen van Sales naar Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-114">The following template and underlying task are used to synchronize accounts from Sales to Supply Chain Management:</span></span>

- <span data-ttu-id="a6d8a-115">**Naam van de sjabloon in Gegevensintegratie:** Rekeningen (Sales naar Fin and Ops) - Direct</span><span class="sxs-lookup"><span data-stu-id="a6d8a-115">**Name of the template in Data integration:** Accounts (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="a6d8a-116">**Naam van de taak in het project:** Rekeningen - Klanten</span><span class="sxs-lookup"><span data-stu-id="a6d8a-116">**Name of the task in the project:** Accounts - Customers</span></span>

<span data-ttu-id="a6d8a-117">Er hoeven geen synchronisatietaken te worden uitgevoerd voordat de synchronisatie van rekening/klant kan plaatsvinden.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-117">No synchronization tasks are required before Account/Customer synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="a6d8a-118">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="a6d8a-118">Entity set</span></span>

| <span data-ttu-id="a6d8a-119">Verkoop</span><span class="sxs-lookup"><span data-stu-id="a6d8a-119">Sales</span></span>    | <span data-ttu-id="a6d8a-120">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="a6d8a-120">Supply Chain Management</span></span> |
|----------|------------------------|
| <span data-ttu-id="a6d8a-121">Rekeningen</span><span class="sxs-lookup"><span data-stu-id="a6d8a-121">Accounts</span></span> | <span data-ttu-id="a6d8a-122">Klanten V2</span><span class="sxs-lookup"><span data-stu-id="a6d8a-122">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="a6d8a-123">Entiteitstroom</span><span class="sxs-lookup"><span data-stu-id="a6d8a-123">Entity flow</span></span>

<span data-ttu-id="a6d8a-124">Accounts worden beheerd in Sales en als klanten gesynchroniseerd met Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-124">Accounts are managed in Sales and synchronized to Supply Chain Management as customers.</span></span> <span data-ttu-id="a6d8a-125">De eigenschap **Wordt extern beheerd** is voor deze klanten ingesteld op **Ja** voor het volgen van klanten die afkomstig zijn uit Sales.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-125">The **Is Externally Maintained** property on these customers is set to **Yes** to track customers that originate from Sales.</span></span> <span data-ttu-id="a6d8a-126">Bij het factureren wordt deze informatie gebruikt voor het filteren van facturen die worden gesynchroniseerd met Sales.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-126">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="a6d8a-127">Oplossing Prospect naar contant geld voor Sales</span><span class="sxs-lookup"><span data-stu-id="a6d8a-127">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="a6d8a-128">Het veld **Rekeningnummer** is beschikbaar op de pagina **Rekening**.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-128">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="a6d8a-129">Het is een natuurlijke en unieke sleutel voor de ondersteuning van de integratie.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-129">It has been made a natural and unique key in order to support the integration.</span></span> <span data-ttu-id="a6d8a-130">De functie van de natuurlijke sleutel in de oplossing Customer Relationship Management (CRM) kan van invloed zijn op klanten die al gebruikmaken van het veld **Rekeningnummer**, maar die geen unieke waarden voor **Rekeningnummer** per rekening gebruiken.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-130">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="a6d8a-131">De integratie-oplossing ondersteunt op dit moment dit geval niet.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-131">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="a6d8a-132">Wanneer een nieuwe rekening wordt gemaakt, als een **rekeningnummer** waarde nog niet bestaat, wordt deze automatisch gegenereerd met behulp van een nummerreeks.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-132">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="a6d8a-133">De waarde bestaat uit **ACC**, gevolgd door een stijgende nummerreeks en vervolgens een achtervoegsel van zes tekens.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-133">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="a6d8a-134">Bijvoorbeeld: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="a6d8a-134">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="a6d8a-135">Wanneer de integratie-oplossing voor Sales wordt toegepast, stelt een upgradescript het veld **Rekeningnummer** in voor bestaande rekeningen in Sales.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-135">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="a6d8a-136">Als er geen waarden zijn voor **Rekeningnummer**, wordt de eerder beschreven nummerreeks gebruikt.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-136">If there are no **Account Number** values, the number sequence that was mentioned earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="a6d8a-137">Voorwaarden en instellingen voor toewijzing</span><span class="sxs-lookup"><span data-stu-id="a6d8a-137">Preconditions and mapping setup</span></span>

- <span data-ttu-id="a6d8a-138">De toewijzing **CustomerGroupId** moet worden bijgewerkt naar een geldige waarde in Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-138">The **CustomerGroupId** mapping must be updated to a valid value in Supply Chain Management.</span></span> <span data-ttu-id="a6d8a-139">U kunt een standaardwaarde opgeven of u kunt de waarde instellen met behulp van een waardetoewijzing.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-139">You can specify a default value, or you can set the value by using a value map.</span></span>

    <span data-ttu-id="a6d8a-140">De standaardsjabloonwaarde is **10**.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-140">The default template value is **10**.</span></span>

- <span data-ttu-id="a6d8a-141">Door de volgende toewijzingen toe te voegen, verkleint u het aantal vereiste handmatige updates in Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-141">By adding the following mappings, you can help reduce the number of manual updates that are required in Supply Chain Management.</span></span> <span data-ttu-id="a6d8a-142">U kunt een standaardwaarde of een waardetoewijzing gebruiken, bijvoorbeeld: **land/regio** of **plaats**.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="a6d8a-143">**SiteId**: een site is vereist voor het genereren van offertes en verkooporderregels in Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="a6d8a-144">Een standaardsite kan afkomstig zijn uit het product of uit de orderkoptekst van de klant.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-144">A default site can be taken either from the product, or from the customer from the order header.</span></span>

        <span data-ttu-id="a6d8a-145">De standaardsjabloonwaarde is **1**.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-145">The default template value is **1**.</span></span>

    - <span data-ttu-id="a6d8a-146">**WarehouseId**: een magazijn is vereist voor het verwerken van offertes en verkooporderregels in Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="a6d8a-147">Een standaardmagazijn kan afkomstig zijn uit het product of uit de orderkoptekst van de klant in Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-147">A default warehouse can be taken either from the product, or from the customer from the order header in Supply Chain Management.</span></span>

        <span data-ttu-id="a6d8a-148">De standaardsjabloonwaarde is **13**.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-148">The default template value is **13**.</span></span>

    - <span data-ttu-id="a6d8a-149">**LanguageId**: een taal is vereist voor het genereren van offertes en verkooporders in Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Supply Chain Management.</span></span> <span data-ttu-id="a6d8a-150">Standaard wordt de taal uit de orderkoptekst van de klant gebruikt.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-150">By default, the language from the order header from the customer is used.</span></span>

        <span data-ttu-id="a6d8a-151">De standaardwaarde van de sjabloon is **en-us**.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-151">The default template value is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="a6d8a-152">Sjabloontoewijzing in Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="a6d8a-152">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="a6d8a-153">De velden **Vetalingsvoorwaarden**, **Leveringscondities**, **Leveringsvoorwaarden**, **Verzendmethode** en **Leveringsmethode** maken geen deel uit van de standaardtoewijzingen.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-153">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="a6d8a-154">Als u deze velden wilt toewijzen, moet u een waardetoewijzing instellen die specifiek is voor de gegevens in de organisaties waartussen de entiteit wordt gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-154">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="a6d8a-155">In de volgende afbeeldingen ziet u een voorbeeld van sjabloontoewijzing in Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-155">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="a6d8a-156">Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Sales naar Supply Chain Management worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="a6d8a-156">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

![Sjabloontoewijzing in Gegevensintegratie](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a><span data-ttu-id="a6d8a-158">Verwante onderwerpen</span><span class="sxs-lookup"><span data-stu-id="a6d8a-158">Related topics</span></span>


[<span data-ttu-id="a6d8a-159">Van prospect naar contant geld</span><span class="sxs-lookup"><span data-stu-id="a6d8a-159">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="a6d8a-160">Rekeningen rechtstreeks vanuit Sales synchroniseren met klanten in Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="a6d8a-160">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="a6d8a-161">Contactpersonen in Sales rechtstreeks synchroniseren met contactpersonen of klanten in Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="a6d8a-161">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="a6d8a-162">Verkooporders rechtstreeks tussen Sales en Supply Chain Management synchroniseren</span><span class="sxs-lookup"><span data-stu-id="a6d8a-162">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="a6d8a-163">Kopteksten en regels in verkoopfacturen rechtstreeks synchroniseren vanuit Supply Chain Management naar Sales</span><span class="sxs-lookup"><span data-stu-id="a6d8a-163">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)

