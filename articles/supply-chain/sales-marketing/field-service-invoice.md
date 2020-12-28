---
title: Overeenkomstfacturen in Field Service synchroniseren met vrije-tekstfacturen in Supply Chain Management
description: Dit onderwerp bespreekt de sjablonen en onderliggende taken die worden gebruikt voor het synchroniseren van overeenkomstfacturen in Dynamics 365 Field Service voor vrije-tekstfacturen in Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 04/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: c2d0f671d4b824cb5d38a5d11c4b06b2e97bd0c8
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528240"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-supply-chain-management"></a><span data-ttu-id="4764c-103">Overeenkomstfacturen in Field Service synchroniseren met vrije-tekstfacturen in Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="4764c-103">Synchronize agreement invoices in Field Service to free text invoices in Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="4764c-104">Dit onderwerp bespreekt de sjablonen en onderliggende taken die worden gebruikt voor het synchroniseren van facturen in Dynamics 365 Field Service voor vrije-tekstfacturen in Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4764c-104">This topic discusses the templates and underlying tasks that are used to synchronize agreement invoices in Dynamics 365 Field Service to free text invoices in Dynamics 365 Supply Chain Management.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="4764c-105">Sjablonen en taken</span><span class="sxs-lookup"><span data-stu-id="4764c-105">Templates and tasks</span></span>

<span data-ttu-id="4764c-106">De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van overeenkomstfacturen in Field Service met vrije-tekstfacturen in Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4764c-106">The following template and underlying tasks are used to run synchronization of agreement invoices from Field Service to free text invoices in Supply Chain Management.</span></span>

<span data-ttu-id="4764c-107">**Naam van de sjabloon in Gegevensintegratie**</span><span class="sxs-lookup"><span data-stu-id="4764c-107">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="4764c-108">Overeenkomstfacturen (Field Service naar Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="4764c-108">Agreement invoices (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="4764c-109">**Namen van de taken in het project Gegevensintegratie**</span><span class="sxs-lookup"><span data-stu-id="4764c-109">**Names of the tasks in the Data integration project**</span></span>

- <span data-ttu-id="4764c-110">Factuurkopteksten</span><span class="sxs-lookup"><span data-stu-id="4764c-110">Invoice headers</span></span>
- <span data-ttu-id="4764c-111">Factuurregels</span><span class="sxs-lookup"><span data-stu-id="4764c-111">Invoice lines</span></span>

<span data-ttu-id="4764c-112">De volgende synchronisatietaak is vereist voordat de synchronisatie van de overeenkomstfacturen kan plaatsvinden:</span><span class="sxs-lookup"><span data-stu-id="4764c-112">The following synchronization is required before synchronization of agreement invoices can occur:</span></span>

- <span data-ttu-id="4764c-113">Accounts (Sales naar Supply Chain Management) - Direct</span><span class="sxs-lookup"><span data-stu-id="4764c-113">Accounts (Sales to Supply Chain Management) – Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="4764c-114">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="4764c-114">Entity set</span></span>

| <span data-ttu-id="4764c-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="4764c-115">Field Service</span></span>  | <span data-ttu-id="4764c-116">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="4764c-116">Supply Chain Management</span></span>                 |
|----------------|----------------------------------------|
| <span data-ttu-id="4764c-117">facturen</span><span class="sxs-lookup"><span data-stu-id="4764c-117">invoices</span></span>       | <span data-ttu-id="4764c-118">Kopteksten voor vrije-tekstfacturen van CDS-klanten</span><span class="sxs-lookup"><span data-stu-id="4764c-118">CDS customer free text invoice headers</span></span> |
| <span data-ttu-id="4764c-119">factuurdetails</span><span class="sxs-lookup"><span data-stu-id="4764c-119">invoicedetails</span></span> | <span data-ttu-id="4764c-120">Regels voor vrije-tekstfacturen van CDS-klanten</span><span class="sxs-lookup"><span data-stu-id="4764c-120">CDS customer free text invoice lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="4764c-121">Entiteitstroom</span><span class="sxs-lookup"><span data-stu-id="4764c-121">Entity flow</span></span>

<span data-ttu-id="4764c-122">Facturen die zijn gemaakt op basis van een overeenkomst in Field Service kunnen worden gesynchroniseerd met Supply Chain Management via een Common Data Service-gegevensintegratieproject.</span><span class="sxs-lookup"><span data-stu-id="4764c-122">Invoices that are created from an agreement in Field Service can be synchronized to Supply Chain Management via a Common Data Service Data integration project.</span></span> <span data-ttu-id="4764c-123">Updates voor deze facturen worden gesynchroniseerd met de vrije-tekstfacturen in Supply Chain Management als de boekhoudstatus van de vrije-tekstfacturen **Onderhanden** is.</span><span class="sxs-lookup"><span data-stu-id="4764c-123">Updates to these invoices will be synchronized to the free text invoices in Supply Chain Management if the accounting status of the free text invoices is **In process**.</span></span> <span data-ttu-id="4764c-124">Nadat de vrije-tekstfacturen zijn geboekt in Supply Chain Management en de boekhoudstatus is bijgewerkt naar **Voltooid**, kunt u de updates van Field Service niet meer synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="4764c-124">After the free text invoices are posted in Supply Chain Management, and the accounting status is updated to **Completed**, you can no longer synchronize updates from Field Service.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="4764c-125">Field Service CRM-oplossing</span><span class="sxs-lookup"><span data-stu-id="4764c-125">Field Service CRM solution</span></span>

<span data-ttu-id="4764c-126">Het veld **Heeft regels met oorsprong overeenkomst** is toegevoegd aan de entiteit **Factuur**.</span><span class="sxs-lookup"><span data-stu-id="4764c-126">The **Has Lines With Agreement Origin** field has been added to the **Invoice** entity.</span></span> <span data-ttu-id="4764c-127">Dit veld zorgt ervoor dat alleen facturen die zijn gemaakt op basis van een overeenkomst, worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="4764c-127">This field helps guarantee that only invoices that are created from an agreement are synchronized.</span></span> <span data-ttu-id="4764c-128">De waarde is **true** als de factuur ten minste één factuurregel bevat die afkomstig is van een overeenkomst.</span><span class="sxs-lookup"><span data-stu-id="4764c-128">The value is **true** if the invoice contains at least one invoice line that originates from an agreement.</span></span>

<span data-ttu-id="4764c-129">Het veld **Heeft oorsprong overeenkomst** is toegevoegd aan de entiteit **Factuurregel**.</span><span class="sxs-lookup"><span data-stu-id="4764c-129">The **Has Agreement Origin** field has been added to the **Invoice Line** entity.</span></span> <span data-ttu-id="4764c-130">Dit veld zorgt ervoor dat alleen factuurregels die zijn gemaakt op basis van een overeenkomst, worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="4764c-130">This field helps guarantee that only invoice lines that are created from an agreement are synchronized.</span></span> <span data-ttu-id="4764c-131">De waarde **true** als de factuurregel afkomstig is uit een overeenkomst.</span><span class="sxs-lookup"><span data-stu-id="4764c-131">The value is **true** if the invoice line originates from an agreement.</span></span>

<span data-ttu-id="4764c-132">**Factuurdatum** is een verplicht veld in Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4764c-132">**Invoice date** is a mandatory field in Supply Chain Management.</span></span> <span data-ttu-id="4764c-133">Het veld moet daarom een waarde in Field Service hebben voordat de synchronisatie wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="4764c-133">Therefore, the field must have a value in Field Service before synchronization occurs.</span></span> <span data-ttu-id="4764c-134">Om te voldoen aan deze vereiste wordt de volgende logica toegevoegd:</span><span class="sxs-lookup"><span data-stu-id="4764c-134">To meet this requirement, the following logic is added:</span></span>

- <span data-ttu-id="4764c-135">Als het veld **Factuurdatum** leeg is op de entiteit **Factuur** (dat wil zeggen er is geen waarde), wordt deze ingesteld op de huidige datum wanneer een factuurregel afkomstig uit een overeenkomst wordt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="4764c-135">If the **Invoice Date** field is blank on the **Invoice** entity (that is, if it has no value), it's set to the current date when an invoice line that originates from an agreement is added.</span></span>
- <span data-ttu-id="4764c-136">De gebruiker kan het veld **Factuurdatum** wijzigen.</span><span class="sxs-lookup"><span data-stu-id="4764c-136">The user can change the **Invoice Date** field.</span></span> <span data-ttu-id="4764c-137">Wanneer de gebruiker een factuur wil opslaan die afkomstig is uit een overeenkomst, verschijnt een bedrijfsprocesfout als het veld **Factuurdatum** leeg is op de factuur.</span><span class="sxs-lookup"><span data-stu-id="4764c-137">However, when the user tries to save an invoice that originates from an agreement, he or she receives a business process error if the **Invoice Date** field is blank on the invoice.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="4764c-138">Vereisten en instellingen voor toewijzing</span><span class="sxs-lookup"><span data-stu-id="4764c-138">Prerequisites and mapping setup</span></span>

### <a name="in-supply-chain-management"></a><span data-ttu-id="4764c-139">In Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="4764c-139">In Supply Chain Management</span></span>

<span data-ttu-id="4764c-140">De oorsprong van een factuur moet worden ingesteld voor de integratie om vrije-tekstfacturen te herkennen in Supply Chain Management die zijn gemaakt op basis van overeenkomstfacturen in Field Service.</span><span class="sxs-lookup"><span data-stu-id="4764c-140">An invoice origin must be set up for the integration, to distinguish the free text invoices in Supply Chain Management that are created from agreement invoices in Field Service.</span></span> <span data-ttu-id="4764c-141">Wanneer een factuur een factuuroorsprong heeft van het type **Factuurintegratie van overeenkomst**, wordt het veld **Extern factuurnummer** weergegeven in de koptekst van de **verkoopfactuur**.</span><span class="sxs-lookup"><span data-stu-id="4764c-141">When an invoice has an invoice origin of the **Agreement invoice integration** type, the **External invoice number** field is shown on the **Sales invoice** header.</span></span>

<span data-ttu-id="4764c-142">Behalve op de factuurkop worden de gegevens van het **Externe factuurnummer** gebruikt om te garanderen dat facturen die zijn gemaakt op basis van Field Service-overeenkomstfacturen, eruit worden gefilterd tijdens de factuursynchronisatie tussen Supply Chain Management en Field Service.</span><span class="sxs-lookup"><span data-stu-id="4764c-142">Besides appearing on the invoice header, the **External invoice number** information can be used to help guarantee that invoices that are created from Field Service agreement invoices are filtered out during invoice synchronization from Supply Chain Management to Field Service.</span></span>

1. <span data-ttu-id="4764c-143">Ga naar **Klanten** \> **Instellen** \> **Oorsprongcodes voor factuur**.</span><span class="sxs-lookup"><span data-stu-id="4764c-143">Go to **Accounts receivable** \> **Setup** \> **Invoice origin codes**.</span></span>
2. <span data-ttu-id="4764c-144">Selecteer **Nieuw** om een nieuwe factuuroorsprong te maken.</span><span class="sxs-lookup"><span data-stu-id="4764c-144">Select **New** to create a new invoice origin.</span></span>
3. <span data-ttu-id="4764c-145">Voer in het veld **Factuuroorsprong** een naam in voor de factuuroorsprong, zoals **FS**.</span><span class="sxs-lookup"><span data-stu-id="4764c-145">In the **Invoice origin** field, enter a name for the invoice origin, such as **FS**.</span></span>
4. <span data-ttu-id="4764c-146">Voer in het veld **Omschrijving** een omschrijving in zoals **Field Service-overeenkomstfactuur**.</span><span class="sxs-lookup"><span data-stu-id="4764c-146">In the **Description** field, enter a description, such as **Field Service Agreement Invoice**.</span></span>
5. <span data-ttu-id="4764c-147">Schakel het selectievakje **Toewijzing van oorsprongtype** in.</span><span class="sxs-lookup"><span data-stu-id="4764c-147">Select the **Origin type assignment** check box.</span></span>
6. <span data-ttu-id="4764c-148">Stel het veld **Type factuuroorsprong** in op **Factuurintegratie van overeenkomst**.</span><span class="sxs-lookup"><span data-stu-id="4764c-148">Set the **Invoice origin type** field to **Agreement invoice integration**.</span></span>
7. <span data-ttu-id="4764c-149">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="4764c-149">Select **Save**.</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="4764c-150">In het project Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="4764c-150">In the Data Integration project</span></span>

<span data-ttu-id="4764c-151">Taak: **Factuurregels**</span><span class="sxs-lookup"><span data-stu-id="4764c-151">Task: **Invoice lines**</span></span>  

<span data-ttu-id="4764c-152">Zorg dat de standaardwaarde voor het veld **Weergegeven waarde hoofdrekening** in Supply Chain Management wordt bijgewerkt naar de gewenste waarde.</span><span class="sxs-lookup"><span data-stu-id="4764c-152">Make sure that the default value for the Supply Chain Management field **Main Account Display Value** is updated to match the desired value.</span></span>

<span data-ttu-id="4764c-153">De standaardsjabloonwaarde is **401100**.</span><span class="sxs-lookup"><span data-stu-id="4764c-153">The default template value is **401100**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="4764c-154">Sjabloontoewijzing in Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="4764c-154">Template mapping in Data integration</span></span>

<span data-ttu-id="4764c-155">In de volgende afbeeldingen ziet u de sjabloontoewijzing in Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="4764c-155">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-headers"></a><span data-ttu-id="4764c-156">Overeenkomstfacturen (Field Service naar Supply Chain Management): Factuurkopteksten</span><span class="sxs-lookup"><span data-stu-id="4764c-156">Agreement invoices (Field Service to Supply Chain Management): Invoice headers</span></span>

<span data-ttu-id="4764c-157">[![Sjabloontoewijzing in Gegevensintegratie](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span><span class="sxs-lookup"><span data-stu-id="4764c-157">[![Template mapping in Data integration](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span></span>

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-lines"></a><span data-ttu-id="4764c-158">Overeenkomstfacturen (Field Service naar Supply Chain Management): Factuurregels</span><span class="sxs-lookup"><span data-stu-id="4764c-158">Agreement invoices (Field Service to Supply Chain Management): Invoice lines</span></span>

<span data-ttu-id="4764c-159">[![Sjabloontoewijzing in Gegevensintegratie](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span><span class="sxs-lookup"><span data-stu-id="4764c-159">[![Template mapping in Data integration](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span></span>
