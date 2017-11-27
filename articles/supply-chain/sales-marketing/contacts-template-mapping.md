---
title: Contactpersonen synchroniseren tussen Sales met contactpersonen of klanten in Finance and Operations
description: In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van Contactpersoon (contactpersonen) en Contactpersoon (klanten) tussen Microsoft Dynamics 365 for Sales en Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.
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
ms.openlocfilehash: c838fef502f643c764fade9cd79ae770ffc36974
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-contacts-from-sales-to-contacts-or-customers-in-finance-and-operations"></a><span data-ttu-id="ff163-103">Contactpersonen synchroniseren tussen Sales met contactpersonen of klanten in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ff163-103">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="ff163-104">Voordat u de oplossing Prospect naar contant geld kunt gebruiken, moet u vertrouwd zijn met de functie [Dynamics 365 Gegevensintegratie](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="ff163-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="ff163-105">In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van de entiteiten Contactpersoon (contactpersonen) en Contactpersoon (klanten) tussen Microsoft Dynamics 365 for Sales en Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span><span class="sxs-lookup"><span data-stu-id="ff163-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) entities and Contact (Customers) from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="ff163-106">Sjablonen en taken</span><span class="sxs-lookup"><span data-stu-id="ff163-106">Templates and tasks</span></span>

<span data-ttu-id="ff163-107">De volgende sjablonen en onderliggende taken worden gebruikt voor het synchroniseren van Contactpersoon (contactpersonen) in Sales met Contactpersoon (klanten) in Finance en Operations:</span><span class="sxs-lookup"><span data-stu-id="ff163-107">The following templates and underlying tasks are used to synchronize Contact (Contacts) in Sales to Contact (Customers) in Finance and Operations:</span></span>

- <span data-ttu-id="ff163-108">**De namen van de sjablonen:**</span><span class="sxs-lookup"><span data-stu-id="ff163-108">**Names of the templates:**</span></span>

    - <span data-ttu-id="ff163-109">Contactpersonen (Sales met Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="ff163-109">Contacts (Sales to Fin and Ops)</span></span>
    - <span data-ttu-id="ff163-110">Contactpersonen met klant (Sales met Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="ff163-110">Contacts to Customer (Sales to Fin and Ops)</span></span>

- <span data-ttu-id="ff163-111">**Namen van de taken in het project:**</span><span class="sxs-lookup"><span data-stu-id="ff163-111">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="ff163-112">Contacten</span><span class="sxs-lookup"><span data-stu-id="ff163-112">Contacts</span></span>
    - <span data-ttu-id="ff163-113">ContactToCustomer</span><span class="sxs-lookup"><span data-stu-id="ff163-113">ContactToCustomer</span></span>

<span data-ttu-id="ff163-114">De volgende synchronisatietaak is vereist voor de synchronisatie van contactpersonen: rekeningen (Sales met Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="ff163-114">The following synchronization task is required before Contact synchronization: Accounts (Sales to Fin and Ops)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="ff163-115">Entiteitsets</span><span class="sxs-lookup"><span data-stu-id="ff163-115">Entity sets</span></span>

| <span data-ttu-id="ff163-116">Verkoop</span><span class="sxs-lookup"><span data-stu-id="ff163-116">Sales</span></span>    | <span data-ttu-id="ff163-117">CDS</span><span class="sxs-lookup"><span data-stu-id="ff163-117">CDS</span></span>     | <span data-ttu-id="ff163-118">Finance en Operations</span><span class="sxs-lookup"><span data-stu-id="ff163-118">Finance and Operations</span></span> |
|----------|---------|------------------------|
| <span data-ttu-id="ff163-119">Contacten</span><span class="sxs-lookup"><span data-stu-id="ff163-119">Contacts</span></span> | <span data-ttu-id="ff163-120">Contactpersoon</span><span class="sxs-lookup"><span data-stu-id="ff163-120">Contact</span></span> | <span data-ttu-id="ff163-121">CDS-contactpersonen</span><span class="sxs-lookup"><span data-stu-id="ff163-121">CDS Contacts</span></span>           |
| <span data-ttu-id="ff163-122">Contacten</span><span class="sxs-lookup"><span data-stu-id="ff163-122">Contacts</span></span> | <span data-ttu-id="ff163-123">Rekening</span><span class="sxs-lookup"><span data-stu-id="ff163-123">Account</span></span> | <span data-ttu-id="ff163-124">Klanten V2</span><span class="sxs-lookup"><span data-stu-id="ff163-124">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="ff163-125">Entiteitstroom</span><span class="sxs-lookup"><span data-stu-id="ff163-125">Entity flow</span></span>

<span data-ttu-id="ff163-126">Contactpersonen worden beheerd in Sales en gesynchroniseerd met Common Data Service (CDS) en Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ff163-126">Contacts are managed in Sales, and are synchronized to Common Data Service (CDS) and Finance and Operations.</span></span>

<span data-ttu-id="ff163-127">Een contactpersoon in Sales wordt een contactpersoon in CDS en Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ff163-127">A Contact in Sales can become a Contact in CDS and Finance and Operations.</span></span> <span data-ttu-id="ff163-128">Het kan ook een rekening worden in CDS en een klant Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ff163-128">Alternatively, it can become an Account in CDS and a Customer in Finance and Operations.</span></span> <span data-ttu-id="ff163-129">Om te bepalen of een contactpersoon moet worden opgehaald in Sales voor synchronisatie met CDS en Finance and Operations (bijvoorbeeld contactpersonen in Sales &gt; Contactpersoon in CDS &gt; Contactpersonen in Finance and Operations), controleert het systeem de volgende eigenschappen van de contactpersoon in Sales:</span><span class="sxs-lookup"><span data-stu-id="ff163-129">To determine whether a contact should be picked up in Sales for synchronization to CDS and Finance and Operations (for example, Contacts in Sales &gt; Contact in CDS &gt; Contacts in Finance and Operations), the system looks at the following properties on Contact in Sales:</span></span>

- <span data-ttu-id="ff163-130">**Synchroniseren met Rekening in CDS en Klant in Finance and Operations:** Contactpersonen waarvoor **Is actieve klant** is ingesteld op **Ja**</span><span class="sxs-lookup"><span data-stu-id="ff163-130">**Sync to Account in CDS and Customer in Finance and Operations:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="ff163-131">**Synchroniseren met Contactpersoon in CDS en Contactpersoon in Finance and Operations:** Contactpersonen waarvoor **Is actieve klant** is ingesteld op **Nee** en **Bedrijf** (Bovenliggende rekening/contactpersoon) verwijst naar een rekening (niet een contactpersoon)</span><span class="sxs-lookup"><span data-stu-id="ff163-131">**Sync to Contact in CDS and Contact in Finance and Operations:** Contacts where **Is Active Customer** is set to **No** and **Company** (Parent Account/Contact) points to an Account (not a Contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="ff163-132">Oplossing Prospect naar contant geld voor Sales</span><span class="sxs-lookup"><span data-stu-id="ff163-132">Prospect to cash solution for Sales</span></span> 

<span data-ttu-id="ff163-133">Er wordt een nieuw veld **Is actieve klant** toegevoegd aan de contactpersoon.</span><span class="sxs-lookup"><span data-stu-id="ff163-133">A new **Is Active Customer** field has been added to the Contact.</span></span> <span data-ttu-id="ff163-134">Dit veld wordt gebruikt om onderscheid te maken tussen contactpersonen met verkoopactiviteit en contacten zonder verkoopactiviteiten.</span><span class="sxs-lookup"><span data-stu-id="ff163-134">This field is used to differentiate Contacts that have sales activity and Contacts that don't have sales activity.</span></span> <span data-ttu-id="ff163-135">**Is actieve klant** is alleen ingesteld op **Ja** voor contactpersonen met gerelateerde offertes, orders of facturen.</span><span class="sxs-lookup"><span data-stu-id="ff163-135">**Is Active Customer** is set to **Yes** only for Contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="ff163-136">Alleen die contactpersonen worden als klanten gesynchroniseerd met Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ff163-136">Only those Contacts are synchronized to Finance and Operations as Customers.</span></span>

<span data-ttu-id="ff163-137">Er wordt een nieuw veld **IsCompanyAnAccount** toegevoegd aan de contactpersoon.</span><span class="sxs-lookup"><span data-stu-id="ff163-137">A new **IsCompanyAnAccount** field has been added to the Contact.</span></span> <span data-ttu-id="ff163-138">Dit veld wordt gebruikt om aan te geven of een contactpersoon is gekoppeld aan een bedrijf (bovenliggende rekening/contactpersoon) van het type **rekening**.</span><span class="sxs-lookup"><span data-stu-id="ff163-138">This field is used to indicate whether a Contact is linked to a Company (Parent Account/Contact) of the **Account** type.</span></span> <span data-ttu-id="ff163-139">Deze informatie wordt gebruikt ter identificatie van de contactpersonen die als contactpersonen moeten worden gesynchroniseerd met Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ff163-139">This information is used to identify Contacts that should be synchronized to Finance and Operations as Contacts.</span></span>

<span data-ttu-id="ff163-140">Er wordt een nieuw veld **Contactnummer** toegevoegd aan de Contactpersoon om een natuurlijke en unieke sleutel voor de integratie te garanderen.</span><span class="sxs-lookup"><span data-stu-id="ff163-140">A new **Contact Number** field has been added to the Contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="ff163-141">Wanneer u een nieuwe contactpersoon maakt, wordt automatisch een waarde voor **Contactnummer** gegenereerd met behulp van een nummerreeks.</span><span class="sxs-lookup"><span data-stu-id="ff163-141">When a new Contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="ff163-142">De waarde bestaat uit **CON**, gevolgd door een stijgende nummerreeks en vervolgens een achtervoegsel van zes tekens.</span><span class="sxs-lookup"><span data-stu-id="ff163-142">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="ff163-143">Bijvoorbeeld: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="ff163-143">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="ff163-144">Wanneer de integratie-oplossing voor Sales wordt toegevoegd aan Sales, stelt een upgradescript het veld **Contactnummer** in voor bestaande contactpersonen met behulp van de vermelde nummerreeks.</span><span class="sxs-lookup"><span data-stu-id="ff163-144">When the integration solution for Sales is added to Sales, an upgrade script sets the **Contact Number** field for existing Contacts by using the number sequence that was discussed earlier.</span></span> <span data-ttu-id="ff163-145">Het upgradescript stelt ook het veld **Is actieve klant** in op **Ja** voor contactpersonen met verkoopactiviteiten.</span><span class="sxs-lookup"><span data-stu-id="ff163-145">The upgrade script also sets the **Is Active Customer** field to **Yes** for any Contacts that have sales activity.</span></span>

## <a name="in-finance-and-operations"></a><span data-ttu-id="ff163-146">In Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ff163-146">In Finance and Operations</span></span> 

<span data-ttu-id="ff163-147">Contactpersonen worden gelabeld met de eigenschap **IsContactPersonExternallyMaintained**.</span><span class="sxs-lookup"><span data-stu-id="ff163-147">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="ff163-148">Deze eigenschap geeft aan dat een bepaalde contactpersoon extern wordt beheerd.</span><span class="sxs-lookup"><span data-stu-id="ff163-148">This property indicates that a given Contact is maintained externally.</span></span> <span data-ttu-id="ff163-149">In dit geval worden extern beheerde contactpersonen onderhouden in Sales.</span><span class="sxs-lookup"><span data-stu-id="ff163-149">In this case, externally maintained Contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="ff163-150">Voorwaarden en instellingen voor toewijzing</span><span class="sxs-lookup"><span data-stu-id="ff163-150">Preconditions and mapping setup</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="ff163-151">Contact met Contact</span><span class="sxs-lookup"><span data-stu-id="ff163-151">Contact to Contact</span></span>

- <span data-ttu-id="ff163-152">Werk **CDS-organisatie-id** bij in de toewijzing **Bron &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="ff163-152">Update **CDS Organization ID** in the **Source &gt; CDS** mapping.</span></span>

    - <span data-ttu-id="ff163-153">De standaardwaarde van de sjabloon voor **Organization_OrganizationId [Organization ID]** is **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="ff163-153">The default template value for **Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>
    - <span data-ttu-id="ff163-154">De standaardwaarde van de sjabloon voor **PrimaryAccount_Organization_OrganizationId [Organization ID]** is **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="ff163-154">The default template value for **PrimaryAccount_Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>

- <span data-ttu-id="ff163-155">**Land-regiocode adres** is vereist in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ff163-155">**Address Country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="ff163-156">Om synchronisatiefouten te voorkomen kunt u een standaardwaarde opgeven in de toewijzing **CDS &gt; Operations**.</span><span class="sxs-lookup"><span data-stu-id="ff163-156">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Operations** mapping.</span></span> <span data-ttu-id="ff163-157">De standaardwaarde wordt vervolgens gebruikt als het veld is leeg in Sales.</span><span class="sxs-lookup"><span data-stu-id="ff163-157">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="ff163-158">De standaardwaarde in de sjabloon voor **PrimaryAddressCountryRegionISOCode** is **USA**.</span><span class="sxs-lookup"><span data-stu-id="ff163-158">The default template value for **PrimaryAddressCountryRegionISOCode** is **USA**.</span></span>
- <span data-ttu-id="ff163-159">Zorg ervoor dat er een waarde voor het volgende veld bestaat in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ff163-159">Make sure that a value for the following field exists in Finance and Operations.</span></span> <span data-ttu-id="ff163-160">Als de informatie niet is vereist in Finance and Operations, kunt u de toewijzing verwijderen uit de toewijzing **CDS &gt; bestemming**.</span><span class="sxs-lookup"><span data-stu-id="ff163-160">If the information isn't required in Finance and Operations, you can remove the mapping from the **CDS &gt; Destination** mapping.</span></span>

    - <span data-ttu-id="ff163-161">**De naam in Finance and Operations.:** Beslissing</span><span class="sxs-lookup"><span data-stu-id="ff163-161">**Field name in Finance and Operations:** Decision</span></span>
    - <span data-ttu-id="ff163-162">**Toewijzing:** PrimaryAccountRole = DecisionMakingRole</span><span class="sxs-lookup"><span data-stu-id="ff163-162">**Mapping:** PrimaryAccountRole = DecisionMakingRole</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="ff163-163">Contactpersoon met klant</span><span class="sxs-lookup"><span data-stu-id="ff163-163">Contact to Customer</span></span>

- <span data-ttu-id="ff163-164">Werk **CDS-organisatie-id** bij in de toewijzing **Bron &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="ff163-164">Update **CDS Organization ID** in the **Source &gt; CDS** mapping.</span></span> <span data-ttu-id="ff163-165">De standaardwaarde van de sjabloon voor **Organization_OrganizationId [Organization ID]** is **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="ff163-165">The default template value for **Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>
- <span data-ttu-id="ff163-166">**Land-regiocode adres** is vereist in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ff163-166">**Address Country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="ff163-167">Om synchronisatiefouten te voorkomen kunt u een standaardwaarde opgeven in de toewijzing **CDS &gt; Bestemming**.</span><span class="sxs-lookup"><span data-stu-id="ff163-167">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Destination** mapping.</span></span> <span data-ttu-id="ff163-168">De standaardwaarde wordt vervolgens gebruikt als het veld is leeg in Sales.</span><span class="sxs-lookup"><span data-stu-id="ff163-168">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="ff163-169">De standaardwaarde in de sjabloon voor **PrimaryAddressCountryRegionISOCode** is **USA**.</span><span class="sxs-lookup"><span data-stu-id="ff163-169">The default template value for **PrimaryAddressCountryRegionISOCode** is **USA**.</span></span>
- <span data-ttu-id="ff163-170">**Klantgroep** is vereist in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ff163-170">**CustomerGroup** is required in Finance and Operations.</span></span> <span data-ttu-id="ff163-171">Om synchronisatiefouten te voorkomen kunt u een standaardwaarde opgeven in de toewijzing **CDS &gt; Bestemming**.</span><span class="sxs-lookup"><span data-stu-id="ff163-171">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Destination** mapping.</span></span> <span data-ttu-id="ff163-172">De standaardwaarde wordt vervolgens gebruikt als het veld is leeg in Sales.</span><span class="sxs-lookup"><span data-stu-id="ff163-172">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="ff163-173">De standaardwaarde in de sjabloon voor **CustomerGroupId** is **10**.</span><span class="sxs-lookup"><span data-stu-id="ff163-173">The default template value for **CustomerGroupId** is **10**.</span></span>
- <span data-ttu-id="ff163-174">Door het toevoegen van de volgende toewijzingen uit **CDS &gt; Bestemming**, verkleint u het aantal handmatige updates in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ff163-174">By adding the following mappings from **CDS &gt; Destination**, you can help reduce the number of manual updates that are in Finance and Operations.</span></span> <span data-ttu-id="ff163-175">U kunt een standaardwaarde of een waardetoewijzing gebruiken, bijvoorbeeld: **land/regio** of **plaats**.</span><span class="sxs-lookup"><span data-stu-id="ff163-175">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="ff163-176">**SiteId**: een standaardlocatie kan ook worden gedefinieerd voor producten in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ff163-176">**SiteId** - A default site can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="ff163-177">Een site is vereist voor het genereren van offertes en verkooporders in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ff163-177">A site is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="ff163-178">Er is geen sjabloonwaarde voor **SiteId** gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="ff163-178">A template value for **SiteId** isn't defined.</span></span>
    - <span data-ttu-id="ff163-179">**WarehouseId**: een standaardmagazijn kan ook worden gedefinieerd voor producten in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ff163-179">**WarehouseId** - A default warehouse can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="ff163-180">Een magazijn is vereist voor het genereren van offertes en verkooporders in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ff163-180">A warehouse is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="ff163-181">Er is geen sjabloonwaarde voor **WarehouseId** gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="ff163-181">A template value for **WarehouseId** isn't defined.</span></span>
    - <span data-ttu-id="ff163-182">**LanguageId**: een taal is vereist voor het genereren van offertes en verkooporders in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ff163-182">**LanguageId** - A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="ff163-183">De standaardwaarde van de sjabloon voor **LanguageId** is **en-us**.</span><span class="sxs-lookup"><span data-stu-id="ff163-183">The default template value for **LanguageId** is **en-us**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="ff163-184">Sjabloontoewijzing in gegevensintegrator</span><span class="sxs-lookup"><span data-stu-id="ff163-184">Template mapping in data integrator</span></span>

<span data-ttu-id="ff163-185">In de volgende afbeeldingen ziet u een voorbeeld van de toewijzing van een sjabloon in gegevensintegrator.</span><span class="sxs-lookup"><span data-stu-id="ff163-185">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="ff163-186">Contact met Contact</span><span class="sxs-lookup"><span data-stu-id="ff163-186">Contact to Contact</span></span>

![Sjabloontoewijzing in gegevensintegrator](./media/contacts-template-mapping-data-integrator-1.png)

![Sjabloontoewijzing voor Contactpersonen in gegevensintegrator](./media/contacts-template-mapping-data-integrator-2.png)

### <a name="contact-to-customer"></a><span data-ttu-id="ff163-189">Contactpersoon met klant</span><span class="sxs-lookup"><span data-stu-id="ff163-189">Contact to Customer</span></span>

![Sjabloontoewijzing in gegevensintegrator](./media/contacts-template-mapping-data-integrator-3.png)

![Sjabloontoewijzing voor Contactpersonen in gegevensintegrator](./media/contacts-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="ff163-192">Verwante onderwerpen</span><span class="sxs-lookup"><span data-stu-id="ff163-192">Related topics</span></span>

[<span data-ttu-id="ff163-193">Producten uit Finance and Operations synchroniseren met producten in Sales</span><span class="sxs-lookup"><span data-stu-id="ff163-193">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="ff163-194">Rekeningen uit Sales synchroniseren met klanten in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ff163-194">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="ff163-195">Kopteksten en regels in verkoopoffertes vanuit Sales synchroniseren naar Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ff163-195">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="ff163-196">Kopteksten en regels in verkooporders synchroniseren vanuit Finance and Operations naar Sales</span><span class="sxs-lookup"><span data-stu-id="ff163-196">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="ff163-197">Kopteksten en regels in verkoopfacturen synchroniseren vanuit Finance and Operations naar Sales</span><span class="sxs-lookup"><span data-stu-id="ff163-197">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)

