---
title: Rekeningen uit Sales synchroniseren met klanten in Finance and Operations
description: In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van rekeningen tussen Microsoft Dynamics 365 for Sales en Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.
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
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: f322c5b273c29d863c059092bf1a41c424c19a7d
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-accounts-from-sales-to-customers-in-finance-and-operations"></a><span data-ttu-id="afd5d-103">Rekeningen uit Sales synchroniseren met klanten in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="afd5d-103">Synchronize accounts from Sales to customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="afd5d-104">Voordat u de oplossing Prospect naar contant geld kunt gebruiken, moet u vertrouwd zijn met de functie [Dynamics 365 Gegevensintegratie](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="afd5d-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="afd5d-105">In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van rekeningen tussen Microsoft Dynamics 365 for Sales (Sales) en Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="afd5d-105">The topic discusses the templates and underlying tasks that are used to synchronize accounts from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span>

## <a name="template-and-task"></a><span data-ttu-id="afd5d-106">Sjabloon en taak</span><span class="sxs-lookup"><span data-stu-id="afd5d-106">Template and task</span></span>

<span data-ttu-id="afd5d-107">De volgende sjablonen en onderliggende taken worden gebruikt voor het synchroniseren van rekeningen tussen Sales en Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="afd5d-107">The following templates and underlying tasks are used to synchronize accounts from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="afd5d-108">**Naam van de sjabloon:** Rekeningen (Sales naar Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="afd5d-108">**Name of the template:** Accounts (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="afd5d-109">**Naam van de taak in het project:** Rekeningen - Rekening - Klanten</span><span class="sxs-lookup"><span data-stu-id="afd5d-109">**Name of the task in the project:** Accounts - Account - Customers</span></span>

<span data-ttu-id="afd5d-110">Taken die nodig zijn voor het synchroniseren van rekening/klant: geen</span><span class="sxs-lookup"><span data-stu-id="afd5d-110">Sync tasks required prior to Account / Customer sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="afd5d-111">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="afd5d-111">Entity set</span></span>

| <span data-ttu-id="afd5d-112">Verkoop</span><span class="sxs-lookup"><span data-stu-id="afd5d-112">Sales</span></span>    | <span data-ttu-id="afd5d-113">CDS</span><span class="sxs-lookup"><span data-stu-id="afd5d-113">CDS</span></span>     | <span data-ttu-id="afd5d-114">Finance en Operations</span><span class="sxs-lookup"><span data-stu-id="afd5d-114">Finance and Operations</span></span> |
|----------|---------|------------------------|
| <span data-ttu-id="afd5d-115">Rekeningen</span><span class="sxs-lookup"><span data-stu-id="afd5d-115">Accounts</span></span> | <span data-ttu-id="afd5d-116">Rekening</span><span class="sxs-lookup"><span data-stu-id="afd5d-116">Account</span></span> | <span data-ttu-id="afd5d-117">Klanten    </span><span class="sxs-lookup"><span data-stu-id="afd5d-117">Customers</span></span>              |

## <a name="entity-flow"></a><span data-ttu-id="afd5d-118">Entiteitstroom</span><span class="sxs-lookup"><span data-stu-id="afd5d-118">Entity flow</span></span>

<span data-ttu-id="afd5d-119">Rekeningen worden beheerd in Sales en gesynchroniseeerd met klanten in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="afd5d-119">Accounts are managed in Sales and synchronized to Finance and Operations as Customers.</span></span> <span data-ttu-id="afd5d-120">De eigenschap **Wordt extern beheerd** is voor deze klanten ingesteld op **Ja** voor het bijhouden van klanten die afkomstig zijn uit Sales.</span><span class="sxs-lookup"><span data-stu-id="afd5d-120">The **Is Externally Maintained** property on these Customers is set to **Yes** to track Customers that originate from Sales.</span></span> <span data-ttu-id="afd5d-121">Bij het factureren wordt deze informatie gebruikt voor het filteren van facturen die worden gesynchroniseerd met Sales.</span><span class="sxs-lookup"><span data-stu-id="afd5d-121">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="afd5d-122">Oplossing Prospect naar contant geld voor Sales</span><span class="sxs-lookup"><span data-stu-id="afd5d-122">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="afd5d-123">Het veld **Rekeningnummer** is beschikbaar op de pagina **Rekening**.</span><span class="sxs-lookup"><span data-stu-id="afd5d-123">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="afd5d-124">Het is een natuurlijke en unieke sleutel voor de ondersteuning van de integratie.</span><span class="sxs-lookup"><span data-stu-id="afd5d-124">It has been made a natural and unique key to support the integration.</span></span> <span data-ttu-id="afd5d-125">De functie van de natuurlijke sleutel in de oplossing Customer Relationship Management (CRM) kan van invloed zijn op klanten die al gebruikmaken van het veld **Rekeningnummer**, maar die geen unieke waarden voor **Rekeningnummer** per rekening gebruiken.</span><span class="sxs-lookup"><span data-stu-id="afd5d-125">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="afd5d-126">De integratie-oplossing ondersteunt op dit moment dit geval niet.</span><span class="sxs-lookup"><span data-stu-id="afd5d-126">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="afd5d-127">Wanneer een nieuwe rekening wordt gemaakt, als een **rekeningnummer** waarde nog niet bestaat, wordt deze automatisch gegenereerd met behulp van een nummerreeks.</span><span class="sxs-lookup"><span data-stu-id="afd5d-127">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="afd5d-128">De waarde bestaat uit **ACC**, gevolgd door een stijgende nummerreeks en vervolgens een achtervoegsel van zes tekens.</span><span class="sxs-lookup"><span data-stu-id="afd5d-128">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="afd5d-129">Bijvoorbeeld: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="afd5d-129">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="afd5d-130">Wanneer de integratie-oplossing voor Sales wordt toegepast, stelt een upgradescript het veld **Rekeningnummer** in voor bestaande rekeningen in Sales.</span><span class="sxs-lookup"><span data-stu-id="afd5d-130">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="afd5d-131">Als er geen **rekeningnummer** waarden zijn, wordt de eerder beschreven nummerreeks gebruikt.</span><span class="sxs-lookup"><span data-stu-id="afd5d-131">If there are no **Account Number** values, the number sequence that was described earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="afd5d-132">Voorwaarden en instellingen voor toewijzing</span><span class="sxs-lookup"><span data-stu-id="afd5d-132">Preconditions and mapping setup</span></span>

- <span data-ttu-id="afd5d-133">De toewijzing **CustomerGroupId** vanuit **CDS &gt; Bestemming** moet worden bijgewerkt naar een geldige waarde in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="afd5d-133">**CustomerGroupId** mapping from **CDS &gt; Destination** must be updated to a valid value in Finance and Operations.</span></span> <span data-ttu-id="afd5d-134">U kunt een standaardwaarde opgeven of u kunt de waarde instellen met behulp van een waardetoewijzing.</span><span class="sxs-lookup"><span data-stu-id="afd5d-134">You can specify a default value, or you can set the value by using a value map.</span></span> <span data-ttu-id="afd5d-135">De standaardsjabloonwaarde is **10**.</span><span class="sxs-lookup"><span data-stu-id="afd5d-135">The default template value is **10**.</span></span>
- <span data-ttu-id="afd5d-136">**Land-regiocode adres** is vereist in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="afd5d-136">**Address country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="afd5d-137">Om synchronisatiefouten te voorkomen kunt u een standaardwaarde opgeven in de toewijzing vanuit **CDS &gt; Bestemming**.</span><span class="sxs-lookup"><span data-stu-id="afd5d-137">To avoid synchronization errors, you can specify a default value in the mapping from **CDS &gt; Destination**.</span></span> <span data-ttu-id="afd5d-138">De standaardwaarde wordt vervolgens gebruikt als het veld is leeg in Sales.</span><span class="sxs-lookup"><span data-stu-id="afd5d-138">That default value is then used if the field is left blank in Sales.</span></span>

    - <span data-ttu-id="afd5d-139">De standaardwaarde van de sjabloon voor **AddressCountryRegionISOCode** is **USA**.</span><span class="sxs-lookup"><span data-stu-id="afd5d-139">The default template value for **AddressCountryRegionISOCode** is **USA**.</span></span>
    - <span data-ttu-id="afd5d-140">De standaardwaarde in de sjabloon voor **DeliveryAddressCountryRegionISOCode** is **USA**.</span><span class="sxs-lookup"><span data-stu-id="afd5d-140">The default template value for **DeliveryAddressCountryRegionISOCode** is **USA**.</span></span>

- <span data-ttu-id="afd5d-141">Door het toevoegen van de volgende toewijzingen uit **CDS &gt; Bestemming**, verkleint u het aantal vereiste handmatige updates in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="afd5d-141">By adding the following mappings from **CDS &gt; Destination**, you can help reduce the number of manual updates that are required in Finance and Operations.</span></span> <span data-ttu-id="afd5d-142">U kunt een standaardwaarde of een waardetoewijzing gebruiken, bijvoorbeeld: **land/regio** of **plaats**.</span><span class="sxs-lookup"><span data-stu-id="afd5d-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="afd5d-143">**SiteId**: een site is vereist voor het genereren van offertes en verkooporderregels in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="afd5d-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="afd5d-144">Een standaardsite kan afkomstig zijn uit het product of uit de orderkoptekst van de klant.</span><span class="sxs-lookup"><span data-stu-id="afd5d-144">A default site can be taken either from the product, or from the customer from the order header.</span></span> <span data-ttu-id="afd5d-145">De standaardwaarde in de sjabloon voor **SiteId** is **1**.</span><span class="sxs-lookup"><span data-stu-id="afd5d-145">The default template value for **SiteId** is **1**.</span></span>
    - <span data-ttu-id="afd5d-146">**WarehouseId**: een magazijn is vereist voor het verwerken van offertes en verkooporderregels in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="afd5d-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="afd5d-147">Een standaardmagazijn kan afkomstig zijn uit het product of uit de orderkoptekst van de klant in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="afd5d-147">A default warehouse can be taken either from the product, or from the customer from the order header in Finance and Operations.</span></span> <span data-ttu-id="afd5d-148">De standaardwaarde in de sjabloon voor **WarehouseId** is **13**.</span><span class="sxs-lookup"><span data-stu-id="afd5d-148">The default template value for **WarehouseId** is **13**.</span></span>
    - <span data-ttu-id="afd5d-149">**LanguageId**: een taal is vereist voor het genereren van offertes en verkooporders in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="afd5d-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="afd5d-150">Standaard wordt de taal uit de orderkoptekst van de klant gebruikt.</span><span class="sxs-lookup"><span data-stu-id="afd5d-150">By default, the language from the order header from the customer is used.</span></span> <span data-ttu-id="afd5d-151">De standaardwaarde van de sjabloon voor **LanguageId** is **en-us**.</span><span class="sxs-lookup"><span data-stu-id="afd5d-151">The default template value for **LanguageId** is **en-us**.</span></span>

- <span data-ttu-id="afd5d-152">Werk de CDS-organisatie-id (**Organization_OrganizationId**) bij in de toewijzing **Bron &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="afd5d-152">Update the CDS organization ID (**Organization_OrganizationId**) in the **Source &gt; CDS** mapping.</span></span> <span data-ttu-id="afd5d-153">De standaardsjabloonwaarde is **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="afd5d-153">The default template value is **ORG001**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="afd5d-154">Sjabloontoewijzing in gegevensintegrator</span><span class="sxs-lookup"><span data-stu-id="afd5d-154">Template mapping in data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="afd5d-155">De velden **Vetalingsvoorwaarden**, **Leveringscondities**, **Leveringsvoorwaarden**, **Verzendmethode** en **Leveringsmethode** maken geen deel uit van de standaardtoewijzingen.</span><span class="sxs-lookup"><span data-stu-id="afd5d-155">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="afd5d-156">Als u deze velden wilt toewijzen, moet u een waardetoewijzing instellen.</span><span class="sxs-lookup"><span data-stu-id="afd5d-156">To map these fields, you must set up a value mapping.</span></span> <span data-ttu-id="afd5d-157">Waardetoewijzingen zijn specifiek voor de gegevens in de organisaties waartussen de entiteit wordt gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="afd5d-157">Value mappings are specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="afd5d-158">In de volgende afbeeldingen ziet u een voorbeeld van de toewijzing van een sjabloon in gegevensintegrator.</span><span class="sxs-lookup"><span data-stu-id="afd5d-158">The following illustrations show an example of a template mapping in data integrator.</span></span>

![Sjabloontoewijzing in gegevensintegrator](./media/accounts-template-mapping-data-integrator-1.png)

![Sjabloontoewijzing voor Rekeningen in gegevensintegrator](./media/accounts-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="afd5d-161">Verwante onderwerpen</span><span class="sxs-lookup"><span data-stu-id="afd5d-161">Related topics</span></span>

[<span data-ttu-id="afd5d-162">Producten uit Finance and Operations synchroniseren met producten in Sales</span><span class="sxs-lookup"><span data-stu-id="afd5d-162">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="afd5d-163">Contactpersonen synchroniseren tussen Sales met contactpersonen of klanten in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="afd5d-163">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="afd5d-164">Kopteksten en regels in verkoopoffertes vanuit Sales synchroniseren naar Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="afd5d-164">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="afd5d-165">Kopteksten en regels in verkooporders synchroniseren vanuit Finance and Operations naar Sales</span><span class="sxs-lookup"><span data-stu-id="afd5d-165">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="afd5d-166">Kopteksten en regels in verkoopfacturen synchroniseren vanuit Finance and Operations naar Sales</span><span class="sxs-lookup"><span data-stu-id="afd5d-166">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)




