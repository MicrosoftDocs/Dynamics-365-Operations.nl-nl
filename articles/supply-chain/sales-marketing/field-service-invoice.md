---
title: Overeenkomstfacturen in Field Service synchroniseren met vrije-tekstfacturen in Finance and Operations
description: In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van overeenkomstfacturen in Microsoft Dynamics 365 for Field Service met vrije-tekstfacturen in Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
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
ms.sourcegitcommit: 08cfd2cfa24bef0f0c92126f5d1052a12ceba37a
ms.openlocfilehash: 1863814d6dd645da8602495858d024fbad2e7149
ms.contentlocale: nl-nl
ms.lasthandoff: 04/11/2018

---

# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-finance-and-operations"></a><span data-ttu-id="afac0-103">Overeenkomstfacturen in Field Service synchroniseren met vrije-tekstfacturen in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="afac0-103">Synchronize agreement invoices in Field Service to free text invoices in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="afac0-104">In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van overeenkomstfacturen in Microsoft Dynamics 365 for Field Service met vrije-tekstfacturen in Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="afac0-104">This topic discusses the templates and underlying tasks that are used to synchronize agreement invoices in Microsoft Dynamics 365 for Field Service to free text invoices in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="afac0-105">Sjablonen en taken</span><span class="sxs-lookup"><span data-stu-id="afac0-105">Templates and tasks</span></span>

<span data-ttu-id="afac0-106">De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van overeenkomstfacturen in Field Service met vrije-tekstfacturen in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="afac0-106">The following template and underlying tasks are used to run synchronization of agreement invoices from Field Service to free text invoices in Finance and Operations.</span></span>

<span data-ttu-id="afac0-107">**Naam van de sjabloon in Gegevensintegratie:**</span><span class="sxs-lookup"><span data-stu-id="afac0-107">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="afac0-108">Overeenkomstfacturen (Field Service met Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="afac0-108">Agreement invoices (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="afac0-109">**Namen van de taken in het project Gegevensintegratie:**</span><span class="sxs-lookup"><span data-stu-id="afac0-109">**Names of the tasks in the Data integration project:**</span></span>

- <span data-ttu-id="afac0-110">Factuurkopteksten</span><span class="sxs-lookup"><span data-stu-id="afac0-110">Invoice headers</span></span>
- <span data-ttu-id="afac0-111">Factuurregels</span><span class="sxs-lookup"><span data-stu-id="afac0-111">Invoice lines</span></span>

<span data-ttu-id="afac0-112">De volgende synchronisatietaak is vereist voordat de synchronisatie van de overeenkomstfacturen kan plaatsvinden:</span><span class="sxs-lookup"><span data-stu-id="afac0-112">The following synchronization is required before synchronization of agreement invoices can occur:</span></span>

- <span data-ttu-id="afac0-113">Rekeningen (Sales naar Fin and Ops) - Direct</span><span class="sxs-lookup"><span data-stu-id="afac0-113">Accounts (Sales to Fin and Ops) – Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="afac0-114">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="afac0-114">Entity set</span></span>

| <span data-ttu-id="afac0-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="afac0-115">Field Service</span></span>  | <span data-ttu-id="afac0-116">Finance en Operations</span><span class="sxs-lookup"><span data-stu-id="afac0-116">Finance and Operations</span></span>                 |
|----------------|----------------------------------------|
| <span data-ttu-id="afac0-117">facturen</span><span class="sxs-lookup"><span data-stu-id="afac0-117">invoices</span></span>       | <span data-ttu-id="afac0-118">Kopteksten voor vrije-tekstfacturen van CDS-klanten</span><span class="sxs-lookup"><span data-stu-id="afac0-118">CDS customer free text invoice headers</span></span> |
| <span data-ttu-id="afac0-119">factuurdetails</span><span class="sxs-lookup"><span data-stu-id="afac0-119">invoicedetails</span></span> | <span data-ttu-id="afac0-120">Regels voor vrije-tekstfacturen van CDS-klanten</span><span class="sxs-lookup"><span data-stu-id="afac0-120">CDS customer free text invoice lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="afac0-121">Entiteitstroom</span><span class="sxs-lookup"><span data-stu-id="afac0-121">Entity flow</span></span>

<span data-ttu-id="afac0-122">Facturen die zijn gemaakt op basis van een overeenkomst in Field Service kunnen worden gesynchroniseerd met Finance and Operations via een Common Data Service-gegevensintegratieproject (CDS).</span><span class="sxs-lookup"><span data-stu-id="afac0-122">Invoices that are created from an agreement in Field Service can be synchronized to Finance and Operations via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="afac0-123">Updates voor deze facturen worden gesynchroniseerd met de vrije-tekstfacturen in Finance and Operations als de boekhoudstatus van de vrije-tekstfacturen **onderhanden** is.</span><span class="sxs-lookup"><span data-stu-id="afac0-123">Updates to these invoices will be synchronized to the free text invoices in Finance and Operations if the accounting status of the free text invoices is **In process**.</span></span> <span data-ttu-id="afac0-124">Nadat de vrije-tekstfacturen zijn geboekt in Finance and Operations en de boekhoudstatus is bijgewerkt naar **voltooid**, kunt u de updates van Field Service niet meer synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="afac0-124">After the free text invoices are posted in Finance and Operations, and the accounting status is updated to **Completed**, you can no longer synchronize updates from Field Service.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="afac0-125">Field Service CRM-oplossing</span><span class="sxs-lookup"><span data-stu-id="afac0-125">Field Service CRM solution</span></span>

<span data-ttu-id="afac0-126">Het veld **Heeft regels met oorsprong overeenkomst** is toegevoegd aan de entiteit **Factuur**.</span><span class="sxs-lookup"><span data-stu-id="afac0-126">The **Has Lines With Agreement Origin** field has been added to the **Invoice** entity.</span></span> <span data-ttu-id="afac0-127">Dit veld zorgt ervoor dat alleen facturen die zijn gemaakt op basis van een overeenkomst, worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="afac0-127">This field helps guarantee that only invoices that are created from an agreement are synchronized.</span></span> <span data-ttu-id="afac0-128">De waarde is **true** als de factuur ten minste één factuurregel bevat die afkomstig is van een overeenkomst.</span><span class="sxs-lookup"><span data-stu-id="afac0-128">The value is **true** if the invoice contains at least one invoice line that originates from an agreement.</span></span>

<span data-ttu-id="afac0-129">Het veld **Heeft oorsprong overeenkomst** is toegevoegd aan de entiteit **Factuurregel**.</span><span class="sxs-lookup"><span data-stu-id="afac0-129">The **Has Agreement Origin** field has been added to the **Invoice Line** entity.</span></span> <span data-ttu-id="afac0-130">Dit veld zorgt ervoor dat alleen factuurregels die zijn gemaakt op basis van een overeenkomst, worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="afac0-130">This field helps guarantee that only invoice lines that are created from an agreement are synchronized.</span></span> <span data-ttu-id="afac0-131">De waarde **true** als de factuurregel afkomstig is uit een overeenkomst.</span><span class="sxs-lookup"><span data-stu-id="afac0-131">The value is **true** if the invoice line originates from an agreement.</span></span>

<span data-ttu-id="afac0-132">**Factuurdatum** is een verplicht veld in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="afac0-132">**Invoice date** is a mandatory field in Finance and Operations.</span></span> <span data-ttu-id="afac0-133">Het veld moet daarom een waarde in Field Service hebben voordat de synchronisatie wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="afac0-133">Therefore, the field must have a value in Field Service before synchronization occurs.</span></span> <span data-ttu-id="afac0-134">Om te voldoen aan deze vereiste wordt de volgende logica toegevoegd:</span><span class="sxs-lookup"><span data-stu-id="afac0-134">To meet this requirement, the following logic is added:</span></span>

- <span data-ttu-id="afac0-135">Als het veld **Factuurdatum** leeg is op de entiteit **Factuur** (dat wil zeggen er is geen waarde), wordt deze ingesteld op de huidige datum wanneer een factuurregel afkomstig uit een overeenkomst wordt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="afac0-135">If the **Invoice Date** field is blank on the **Invoice** entity (that is, if it has no value), it's set to the current date when an invoice line that originates from an agreement is added.</span></span>
- <span data-ttu-id="afac0-136">De gebruiker kan het veld **Factuurdatum** wijzigen.</span><span class="sxs-lookup"><span data-stu-id="afac0-136">The user can change the **Invoice Date** field.</span></span> <span data-ttu-id="afac0-137">Wanneer de gebruiker een factuur wil opslaan die afkomstig is uit een overeenkomst, verschijnt een bedrijfsprocesfout als het veld **Factuurdatum** leeg is op de factuur.</span><span class="sxs-lookup"><span data-stu-id="afac0-137">However, when the user tries to save an invoice that originates from an agreement, he or she receives a business process error if the **Invoice Date** field is blank on the invoice.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="afac0-138">Vereisten en instellingen voor toewijzing</span><span class="sxs-lookup"><span data-stu-id="afac0-138">Prerequisites and mapping setup</span></span>

### <a name="in-finance-and-operations"></a><span data-ttu-id="afac0-139">In Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="afac0-139">In Finance and Operations</span></span>

<span data-ttu-id="afac0-140">De oorsprong van een factuur moet worden ingesteld voor de integratie om vrije-tekstfacturen te herkennen in Finance and Operations die zijn gemaakt op basis van overeenkomstfacturen in Field Service.</span><span class="sxs-lookup"><span data-stu-id="afac0-140">An invoice origin must be set up for the integration, to distinguish the free text invoices in Finance and Operations that are created from agreement invoices in Field Service.</span></span> <span data-ttu-id="afac0-141">Wanneer een factuur een factuuroorsprong heeft van het type **Factuurintegratie van overeenkomst**, wordt het veld **Extern factuurnummer** weergegeven in de koptekst van de **verkoopfactuur**.</span><span class="sxs-lookup"><span data-stu-id="afac0-141">When an invoice has an invoice origin of the **Agreement invoice integration** type, the **External invoice number** field is shown on the **Sales invoice** header.</span></span>

<span data-ttu-id="afac0-142">Behalve op de factuurkop worden de gegvevens van het **externe factuurnummer** gebruikt om te garanderen dat facturen die zijn gemaakt op basis van Field Service-overeenkomstfacturen, eruit worden gefilterd tijdens de factuursynchronisatie tussen Finance and Operations en Field Service.</span><span class="sxs-lookup"><span data-stu-id="afac0-142">Besides appearing on the invoice header, the **External invoice number** information can be used to help guarantee that invoices that are created from Field Service agreement invoices are filtered out during invoice synchronization from Finance and Operations to Field Service.</span></span>

1. <span data-ttu-id="afac0-143">Ga naar **Klanten** \> **Instellen** \> **Oorsprongcodes voor factuur**.</span><span class="sxs-lookup"><span data-stu-id="afac0-143">Go to **Accounts receivable** \> **Setup** \> **Invoice origin codes**.</span></span>
2. <span data-ttu-id="afac0-144">Selecteer **Nieuw** om een nieuwe factuuroorsprong te maken.</span><span class="sxs-lookup"><span data-stu-id="afac0-144">Select **New** to create a new invoice origin.</span></span>
3. <span data-ttu-id="afac0-145">Voer in het veld **Factuuroorsprong** een naam in voor de factuuroorsprong, zoals **FS**.</span><span class="sxs-lookup"><span data-stu-id="afac0-145">In the **Invoice origin** field, enter a name for the invoice origin, such as **FS**.</span></span>
4. <span data-ttu-id="afac0-146">Voer in het veld **Omschrijving** een omschrijving in zoals **Field Service-overeenkomstfactuur**.</span><span class="sxs-lookup"><span data-stu-id="afac0-146">In the **Description** field, enter a description, such as **Field Service Agreement Invoice**.</span></span>
5. <span data-ttu-id="afac0-147">Schakel het selectievakje **Toewijzing van oorsprongtype** in.</span><span class="sxs-lookup"><span data-stu-id="afac0-147">Select the **Origin type assignment** check box.</span></span>
6. <span data-ttu-id="afac0-148">Stel het veld **Type factuuroorsprong** in op **Factuurintegratie van overeenkomst**.</span><span class="sxs-lookup"><span data-stu-id="afac0-148">Set the **Invoice origin type** field to **Agreement invoice integration**.</span></span>
7. <span data-ttu-id="afac0-149">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="afac0-149">Select **Save**.</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="afac0-150">In het project Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="afac0-150">In the Data Integration project</span></span>

<span data-ttu-id="afac0-151">Taak: **Factuurregels**</span><span class="sxs-lookup"><span data-stu-id="afac0-151">Task: **Invoice lines**</span></span>  

<span data-ttu-id="afac0-152">Zorg dat de standaardwaarde voor het veld **Weergegeven waarde hoofdrekening** in Finance and Operations wordt bijgewerkt naar de gewenste waarde.</span><span class="sxs-lookup"><span data-stu-id="afac0-152">Make sure that the default value for the Finance and Operations field **Main Account Display Value** is updated to match the desired value.</span></span>

<span data-ttu-id="afac0-153">De standaardsjabloonwaarde is **401100**.</span><span class="sxs-lookup"><span data-stu-id="afac0-153">The default template value is **401100**.</span></span>

