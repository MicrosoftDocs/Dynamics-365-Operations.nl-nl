---
title: Contactpersonen vanuit Sales direct synchroniseren naar contactpersonen of klanten in Finance and Operations
description: In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van de entiteiten in Contactpersoon (contactpersonen) en Contactpersoon (klanten) vanuit Microsoft Dynamics 365 for Sales naar Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.
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
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 6e0c95618377685b9c27cf693f5553cf515ce6b1
ms.contentlocale: nl-nl
ms.lasthandoff: 01/17/2018

---

# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-finance-and-operations"></a><span data-ttu-id="1b69f-103">Contactpersonen vanuit Sales direct synchroniseren naar contactpersonen of klanten in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1b69f-103">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="1b69f-104">Voordat u de oplossing Prospect naar contant geld kunt gebruiken, moet u vertrouwd zijn met [Dynamics 365 Gegevensintegratie](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="1b69f-104">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

<span data-ttu-id="1b69f-105">In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het direct synchroniseren van de entiteiten in Contactpersoon (contactpersonen) en Contactpersoon (klanten) vanuit Microsoft Dynamics 365 for Sales naar Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span><span class="sxs-lookup"><span data-stu-id="1b69f-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) and Contact (Customers) entities directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="1b69f-106">Gegevensstroom in Prospect naar contant geld</span><span class="sxs-lookup"><span data-stu-id="1b69f-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="1b69f-107">De oplossing Prospect naar contant geld gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Finance and Operations en Sales.</span><span class="sxs-lookup"><span data-stu-id="1b69f-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="1b69f-108">De Prospect naar contant geld-sjablonen die beschikbaar zijn in de functie Gegevensintegratie activeren de stroom van gegevens over rekeningen, contactpersonen, producten, verkoopoffertes en verkoopfacturen tussen Finance and Operations en Sales.</span><span class="sxs-lookup"><span data-stu-id="1b69f-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="1b69f-109">De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Finance and Operations en Sales.</span><span class="sxs-lookup"><span data-stu-id="1b69f-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="1b69f-110">[![Gegevensstroom in Prospect naar contant geld](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="1b69f-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="1b69f-111">Sjablonen en taken</span><span class="sxs-lookup"><span data-stu-id="1b69f-111">Templates and tasks</span></span>

<span data-ttu-id="1b69f-112">Open het [PowerApps-beheercentrum](https://preview.admin.powerapps.com/dataintegration) om toegang te krijgen tot de beschikbare sjablonen.</span><span class="sxs-lookup"><span data-stu-id="1b69f-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="1b69f-113">Selecteer **Projecten** en selecteer vervolgens in de rechterbovenhoek de optie **Nieuw project** om openbare sjablonen te selecteren.</span><span class="sxs-lookup"><span data-stu-id="1b69f-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="1b69f-114">De volgende sjablonen en onderliggende taken worden gebruikt voor het synchroniseren van entiteiten in Contactpersoon (contactpersonen) in Sales naar entiteiten in Contactpersoon (klanten) in Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="1b69f-114">The following templates and underlying tasks are used to synchronize Contact (Contacts) entities in Sales to Contact (Customers) entities in Finance and Operations:</span></span>

- <span data-ttu-id="1b69f-115">**Namen van de sjablonen in Gegevensintegratie:**</span><span class="sxs-lookup"><span data-stu-id="1b69f-115">**Names of the templates in Data integration:**</span></span>

    - <span data-ttu-id="1b69f-116">Contactpersonen (Sales naar Fin and Ops) - Direct</span><span class="sxs-lookup"><span data-stu-id="1b69f-116">Contacts (Sales to Fin and Ops) - Direct</span></span>
    - <span data-ttu-id="1b69f-117">Contactpersonen met klant (Sales naar Fin and Ops) - Direct</span><span class="sxs-lookup"><span data-stu-id="1b69f-117">Contacts to Customer (Sales to Fin and Ops) - Direct</span></span>

- <span data-ttu-id="1b69f-118">**Namen van de taken in het project Gegevensintegratie:**</span><span class="sxs-lookup"><span data-stu-id="1b69f-118">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="1b69f-119">Contacten</span><span class="sxs-lookup"><span data-stu-id="1b69f-119">Contacts</span></span>
    - <span data-ttu-id="1b69f-120">ContactToCustomer</span><span class="sxs-lookup"><span data-stu-id="1b69f-120">ContactToCustomer</span></span>

<span data-ttu-id="1b69f-121">De volgende synchronisatietaak is vereist voor de synchronisatie van contactpersonen: rekeningen (Sales naar Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="1b69f-121">The following synchronization task is required before contact synchronization can occur: Accounts (Sales to Fin and Ops)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="1b69f-122">Entiteitsets</span><span class="sxs-lookup"><span data-stu-id="1b69f-122">Entity sets</span></span>

| <span data-ttu-id="1b69f-123">Verkoop</span><span class="sxs-lookup"><span data-stu-id="1b69f-123">Sales</span></span>    | <span data-ttu-id="1b69f-124">Finance en Operations</span><span class="sxs-lookup"><span data-stu-id="1b69f-124">Finance and Operations</span></span> |
|----------|------------------------|
| <span data-ttu-id="1b69f-125">Contacten</span><span class="sxs-lookup"><span data-stu-id="1b69f-125">Contacts</span></span> | <span data-ttu-id="1b69f-126">CDS-contactpersonen</span><span class="sxs-lookup"><span data-stu-id="1b69f-126">CDS Contacts</span></span>           |
| <span data-ttu-id="1b69f-127">Contacten</span><span class="sxs-lookup"><span data-stu-id="1b69f-127">Contacts</span></span> | <span data-ttu-id="1b69f-128">Klanten V2</span><span class="sxs-lookup"><span data-stu-id="1b69f-128">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="1b69f-129">Entiteitstroom</span><span class="sxs-lookup"><span data-stu-id="1b69f-129">Entity flow</span></span>

<span data-ttu-id="1b69f-130">Contactpersonen worden beheerd in Sales en gesynchroniseerd naar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1b69f-130">Contacts are managed in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="1b69f-131">Een contactpersoon in Sales kan een contactpersoon of klant worden in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1b69f-131">A contact in Sales can become either a contact or a customer in Finance and Operations.</span></span> <span data-ttu-id="1b69f-132">Om te bepalen of een contactpersoon in Sales als een contactpersoon of klant moet worden gesynchroniseerd met Finance and Operations, wordt in het systeem naar de volgende eigenschappen van de contactpersoon in Sales gekeken:</span><span class="sxs-lookup"><span data-stu-id="1b69f-132">To determine whether a contact in Sales should be synchronized to Finance and Operations as a contact or a customer, the system looks at the following properties on the contact in Sales:</span></span>

- <span data-ttu-id="1b69f-133">**Synchronisatie met een klant in Finance and Operations:** contactpersonen waarvoor **Is actieve klant** is ingesteld op **Ja**</span><span class="sxs-lookup"><span data-stu-id="1b69f-133">**Synchronization to a customer in Finance and Operations:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="1b69f-134">**Synchronisatie met een contactpersoon in Finance and Operations:** contactpersonen waarvoor **Is actieve klant** is ingesteld op **Nee** en **Bedrijf** (bovenliggende rekening/contactpersoon) verwijst naar een rekening (niet een contactpersoon)</span><span class="sxs-lookup"><span data-stu-id="1b69f-134">**Synchronization to a contact in Finance and Operations:** Contacts where **Is Active Customer** is set to **No** and **Company** (parent account/contact) points to an account (not a contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="1b69f-135">Oplossing Prospect naar contant geld voor Sales</span><span class="sxs-lookup"><span data-stu-id="1b69f-135">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="1b69f-136">Er is een nieuw veld **Is actieve klant** toegevoegd aan de contactpersoon.</span><span class="sxs-lookup"><span data-stu-id="1b69f-136">A new **Is Active Customer** field has been added to the contact.</span></span> <span data-ttu-id="1b69f-137">Dit veld wordt gebruikt om onderscheid te maken tussen contactpersonen met verkoopactiviteiten en contactpersonen zonder verkoopactiviteiten.</span><span class="sxs-lookup"><span data-stu-id="1b69f-137">This field is used to differentiate contacts that have sales activity and contacts that don't have sales activity.</span></span> <span data-ttu-id="1b69f-138">**Is actieve klant** is alleen ingesteld op **Ja** voor contactpersonen met gerelateerde offertes, orders of facturen.</span><span class="sxs-lookup"><span data-stu-id="1b69f-138">**Is Active Customer** is set to **Yes** only for contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="1b69f-139">Alleen die contactpersonen worden als klanten gesynchroniseerd met Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1b69f-139">Only those contacts are synchronized to Finance and Operations as customers.</span></span>

<span data-ttu-id="1b69f-140">Er wordt een nieuw veld **IsCompanyAnAccount** toegevoegd aan de contactpersoon.</span><span class="sxs-lookup"><span data-stu-id="1b69f-140">A new **IsCompanyAnAccount** field has been added to the contact.</span></span> <span data-ttu-id="1b69f-141">In dit veld wordt aangegeven of een contactpersoon is gekoppeld aan een bedrijf (bovenliggende rekening/contactpersoon) van het type **Rekening**.</span><span class="sxs-lookup"><span data-stu-id="1b69f-141">This field indicates whether a contact is linked to a company (parent account/contact) of the **Account** type.</span></span> <span data-ttu-id="1b69f-142">Deze informatie wordt gebruikt ter identificatie van contactpersonen die als contactpersonen moeten worden gesynchroniseerd met Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1b69f-142">This information is used to identify contacts that should be synchronized to Finance and Operations as contacts.</span></span>

<span data-ttu-id="1b69f-143">Er is een nieuw veld **Contactnummer** toegevoegd aan de contactpersoon om een natuurlijke en unieke sleutel voor de integratie te garanderen.</span><span class="sxs-lookup"><span data-stu-id="1b69f-143">A new **Contact Number** field has been added to the contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="1b69f-144">Wanneer u een nieuwe contactpersoon maakt, wordt automatisch een waarde voor **Contactnummer** gegenereerd op basis van een nummerreeks.</span><span class="sxs-lookup"><span data-stu-id="1b69f-144">When a new contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="1b69f-145">De waarde bestaat uit **CON**, gevolgd door een stijgende nummerreeks en vervolgens een achtervoegsel van zes tekens.</span><span class="sxs-lookup"><span data-stu-id="1b69f-145">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="1b69f-146">Bijvoorbeeld: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="1b69f-146">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="1b69f-147">Wanneer de integratieoplossing voor Sales wordt toegepast, stelt een upgradescript het veld **Contactnummer** in voor bestaande contactpersonen op basis van de eerder genoemde nummerreeks.</span><span class="sxs-lookup"><span data-stu-id="1b69f-147">When the integration solution for Sales is applied, an upgrade script sets the **Contact Number** field for existing contacts by using the number sequence that was mentioned earlier.</span></span> <span data-ttu-id="1b69f-148">Het upgradescript stelt ook het veld **Is actieve klant** in op **Ja** voor contactpersonen met verkoopactiviteiten.</span><span class="sxs-lookup"><span data-stu-id="1b69f-148">The upgrade script also sets the **Is Active Customer** field to **Yes** for any contacts that have sales activity.</span></span>

## <a name="in-finance-and-operations"></a><span data-ttu-id="1b69f-149">In Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1b69f-149">In Finance and Operations</span></span>

<span data-ttu-id="1b69f-150">Contactpersonen worden gelabeld met de eigenschap **IsContactPersonExternallyMaintained**.</span><span class="sxs-lookup"><span data-stu-id="1b69f-150">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="1b69f-151">Deze eigenschap geeft aan dat een bepaalde contactpersoon extern wordt beheerd.</span><span class="sxs-lookup"><span data-stu-id="1b69f-151">This property indicates that a given contact is maintained externally.</span></span> <span data-ttu-id="1b69f-152">In dit geval worden extern beheerde contactpersonen beheerd in Sales.</span><span class="sxs-lookup"><span data-stu-id="1b69f-152">In this case, externally maintained contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="1b69f-153">Voorwaarden en instellingen voor toewijzing</span><span class="sxs-lookup"><span data-stu-id="1b69f-153">Preconditions and mapping setup</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="1b69f-154">Contactpersoon met klant</span><span class="sxs-lookup"><span data-stu-id="1b69f-154">Contact to customer</span></span>

- <span data-ttu-id="1b69f-155">**Klantgroep** is vereist in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1b69f-155">**CustomerGroup** is required in Finance and Operations.</span></span> <span data-ttu-id="1b69f-156">Om synchronisatiefouten te voorkomen, kunt u een standaardwaarde opgeven in de toewijzing.</span><span class="sxs-lookup"><span data-stu-id="1b69f-156">To help prevent synchronization errors, you can specify a default value in the mapping.</span></span> <span data-ttu-id="1b69f-157">De standaardwaarde wordt vervolgens gebruikt als het veld is leeg in Sales.</span><span class="sxs-lookup"><span data-stu-id="1b69f-157">That default value is then used if the field is left blank in Sales.</span></span>

    <span data-ttu-id="1b69f-158">De standaardsjabloonwaarde is **10**.</span><span class="sxs-lookup"><span data-stu-id="1b69f-158">The default template value is **10**.</span></span>

- <span data-ttu-id="1b69f-159">Door de volgende toewijzingen toe te voegen, verkleint u het aantal vereiste handmatige updates in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1b69f-159">By adding the following mappings, you can help reduce the number of manual updates that are required in Finance and Operations.</span></span> <span data-ttu-id="1b69f-160">U kunt een standaardwaarde of een waardetoewijzing gebruiken, bijvoorbeeld: **land/regio** of **plaats**.</span><span class="sxs-lookup"><span data-stu-id="1b69f-160">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="1b69f-161">**SiteId**: een standaardlocatie kan ook worden gedefinieerd voor producten in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1b69f-161">**SiteId** – A default site can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="1b69f-162">Een site is vereist voor het genereren van offertes en verkooporders in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1b69f-162">A site is required in order to generate quotations and sales orders in Finance and Operations.</span></span>

        <span data-ttu-id="1b69f-163">Er is geen sjabloonwaarde voor **SiteId** gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="1b69f-163">A template value for **SiteId** isn't defined.</span></span>

    - <span data-ttu-id="1b69f-164">**WarehouseId**: een standaardmagazijn kan ook worden gedefinieerd voor producten in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1b69f-164">**WarehouseId** – A default warehouse can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="1b69f-165">Een magazijn is vereist voor het genereren van offertes en verkooporders in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1b69f-165">A warehouse is required in order to generate quotations and sales orders in Finance and Operations.</span></span>

        <span data-ttu-id="1b69f-166">Er is geen sjabloonwaarde voor **WarehouseId** gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="1b69f-166">A template value for **WarehouseId** isn't defined.</span></span>

    - <span data-ttu-id="1b69f-167">**LanguageId**: een taal is vereist voor het genereren van offertes en verkooporders in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1b69f-167">**LanguageId** – A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span>
    
        <span data-ttu-id="1b69f-168">De standaardwaarde van de sjabloon is **en-us**.</span><span class="sxs-lookup"><span data-stu-id="1b69f-168">The default template value for is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="1b69f-169">Sjabloontoewijzing in Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="1b69f-169">Template mapping in Data integration</span></span>

<span data-ttu-id="1b69f-170">In de volgende afbeeldingen ziet u een voorbeeld van sjabloontoewijzing in Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="1b69f-170">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="1b69f-171">Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Sales naar Finance and Operations worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="1b69f-171">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="1b69f-172">Contactpersoon met contactpersoon</span><span class="sxs-lookup"><span data-stu-id="1b69f-172">Contact to contact</span></span>

![Sjabloontoewijzing in Gegevensintegrator](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a><span data-ttu-id="1b69f-174">Contactpersoon met klant</span><span class="sxs-lookup"><span data-stu-id="1b69f-174">Contact to customer</span></span>

![Sjabloontoewijzing in Gegevensintegrator](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a><span data-ttu-id="1b69f-176">Verwante onderwerpen</span><span class="sxs-lookup"><span data-stu-id="1b69f-176">Related topics</span></span>

[<span data-ttu-id="1b69f-177">Prospect naar contant geld</span><span class="sxs-lookup"><span data-stu-id="1b69f-177">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="1b69f-178">Rekeningen in Sales direct synchroniseren naar klanten in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1b69f-178">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="1b69f-179">Producten vanuit Finance and Operations direct synchroniseren met producten in Sales</span><span class="sxs-lookup"><span data-stu-id="1b69f-179">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="1b69f-180">Kopteksten en regels in verkooporders direct vanuit Finance and Operations synchroniseren naar Sales</span><span class="sxs-lookup"><span data-stu-id="1b69f-180">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct.md)

[<span data-ttu-id="1b69f-181">Kopteksten en regels in verkoopfacturen direct vanuit Finance and Operations synchroniseren naar Sales</span><span class="sxs-lookup"><span data-stu-id="1b69f-181">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)



