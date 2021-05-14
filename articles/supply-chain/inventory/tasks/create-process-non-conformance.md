---
title: Niet-conformeringen maken en verwerken
description: In dit onderwerp wordt het beheer van niet-conformeringen, op basis van een bestaande kwaliteitsorder, beschreven.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 06a56a694f7a80d65cb46d08744e78d8361cee3b
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956201"
---
# <a name="create-and-process-nonconformances"></a><span data-ttu-id="e0dce-103">Niet-conformeringen maken en verwerken</span><span class="sxs-lookup"><span data-stu-id="e0dce-103">Create and process nonconformances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e0dce-104">In dit onderwerp wordt het beheer van niet-conformeringen, op basis van een bestaande kwaliteitsorder, beschreven.</span><span class="sxs-lookup"><span data-stu-id="e0dce-104">This topic describes how to perform nonconformance management based on an existing quality order.</span></span> <span data-ttu-id="e0dce-105">Het beheer van niet-conformeringen wordt meestal uitgevoerd door een kwaliteitbewakingsmedewerker.</span><span class="sxs-lookup"><span data-stu-id="e0dce-105">Typically, nonconformance management is done by a quality clerk.</span></span> <span data-ttu-id="e0dce-106">Een voorwaarde hiervoor is dat een kwaliteitsorder beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="e0dce-106">As a prerequisite, you must have a quality order available.</span></span> <span data-ttu-id="e0dce-107">(Zie voor informatie over het maken van een kwaliteitsorder [De kwaliteit van goederen inspecteren](inspect-quality-goods.md).)</span><span class="sxs-lookup"><span data-stu-id="e0dce-107">(For information about how to create a quality order, see [Inspect the quality of goods](inspect-quality-goods.md).)</span></span>

<span data-ttu-id="e0dce-108">Voordat een gebruiker de goedkeuring van een niet-conformering kan verwerken, moet een medewerker aan deze gebruiker zijn toegewezen in het veld **Persoon** op de pagina **Gebruikers**.</span><span class="sxs-lookup"><span data-stu-id="e0dce-108">Before a user can process the approval of a nonconformance, a worker must be assigned to them in the **Person** field on the **Users** page.</span></span> <span data-ttu-id="e0dce-109">Voordat de gebruiker de documentnotities kan gebruiken, moet bovendien de optie **Documentverwerking inschakelen** zijn ingesteld op *Ja* in diens gebruikersopties.</span><span class="sxs-lookup"><span data-stu-id="e0dce-109">Additionally, before the user can use the document notes, the **Enable document handling** option must be set to *Yes* in their user options.</span></span>

## <a name="create-a-nonconformance"></a><span data-ttu-id="e0dce-110">Een non-conformiteit maken</span><span class="sxs-lookup"><span data-stu-id="e0dce-110">Create a nonconformance</span></span>

<span data-ttu-id="e0dce-111">Volg deze stappen om een niet-conformering te maken.</span><span class="sxs-lookup"><span data-stu-id="e0dce-111">To create a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="e0dce-112">Ga naar **Voorraadbeheer \> Periodieke taken \> Kwaliteitsbeheer \> Niet-conformeringen**.</span><span class="sxs-lookup"><span data-stu-id="e0dce-112">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="e0dce-113">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="e0dce-113">On the Action pane, select **New**.</span></span>
1. <span data-ttu-id="e0dce-114">Selecteer in het dialoogvenster **Niet-conformering maken** in het veld **Probleemtype** het type probleem dat is gevonden tijdens het inspectieproces.</span><span class="sxs-lookup"><span data-stu-id="e0dce-114">In the **Create non conformance** dialog box, in **Problem type** field, select the type of problem that was found during the inspection process.</span></span>
1. <span data-ttu-id="e0dce-115">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0dce-115">Select **OK**.</span></span>

## <a name="approve-or-reject-a-nonconformance"></a><span data-ttu-id="e0dce-116">Een niet-conformering goedkeuren of afwijzen</span><span class="sxs-lookup"><span data-stu-id="e0dce-116">Approve or reject a nonconformance</span></span>

<span data-ttu-id="e0dce-117">Om een niet-conformering goed te keuren of af te wijzen, volgt u deze stappen:</span><span class="sxs-lookup"><span data-stu-id="e0dce-117">To approve or reject a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="e0dce-118">Ga naar **Voorraadbeheer \> Periodieke taken \> Kwaliteitsbeheer \> Niet-conformeringen**.</span><span class="sxs-lookup"><span data-stu-id="e0dce-118">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="e0dce-119">Zoek en selecteer in de lijst de niet-conformering die u wilt bijwerken.</span><span class="sxs-lookup"><span data-stu-id="e0dce-119">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e0dce-120">U kunt alleen een correctie toevoegen aan niet-conformeringen die zijn goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="e0dce-120">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="e0dce-121">Selecteer in het actievenster de optie **Functies \> Niet-conformering goedkeuren** om de niet-conformering goed te keuren of **Functies \> Niet-conformering weigeren** om deze af te wijzen.</span><span class="sxs-lookup"><span data-stu-id="e0dce-121">On the Action Pane, select **Functions \> Approve non conformance** to approve the nonconformance or **Functions \> Refuse non conformance** to reject it.</span></span> <span data-ttu-id="e0dce-122">U kunt goedgekeurde niet-conformeringen aan [gerelateerde bewerkingen](../quality-operations.md) koppelen.</span><span class="sxs-lookup"><span data-stu-id="e0dce-122">You can associate approved nonconformances with [related operations](../quality-operations.md).</span></span> <span data-ttu-id="e0dce-123">Op deze manier kunt u werk registreren dat wordt uitgevoerd als onderdeel van de niet-conformeringsverwerking en de verwerking van correctieafhandeling.</span><span class="sxs-lookup"><span data-stu-id="e0dce-123">In this way, you can record work that is done as part of the nonconformance handling and the processing of correction handling.</span></span>
1. <span data-ttu-id="e0dce-124">U wordt gevraagd om de selectie te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="e0dce-124">You're prompted to confirm your selection.</span></span> <span data-ttu-id="e0dce-125">Selecteer **Ja** om door te gaan.</span><span class="sxs-lookup"><span data-stu-id="e0dce-125">Select **Yes** to continue.</span></span>

## <a name="add-operations-and-other-details-to-nonconformances"></a><span data-ttu-id="e0dce-126">Bewerkingen en andere details toevoegen aan niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="e0dce-126">Add operations and other details to nonconformances</span></span>

<span data-ttu-id="e0dce-127">Nadat u een niet-conformering hebt gemaakt, kunt u gerelateerde bewerkingen gaan toevoegen en extra informatie over die bewerkingen opgeven.</span><span class="sxs-lookup"><span data-stu-id="e0dce-127">After you've created a nonconformance, you can start to add related operations and specify additional information about those operations.</span></span> <span data-ttu-id="e0dce-128">U kunt alleen gerelateerde bewerkingen toevoegen aan niet-conformeringen die zijn goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="e0dce-128">You can add related operations only to nonconformances that are approved.</span></span>

<span data-ttu-id="e0dce-129">Naast de basisgegevens kunt u de volgende details toevoegen aan een bewerking:</span><span class="sxs-lookup"><span data-stu-id="e0dce-129">Besides the basic information, you can add the following details to an operation:</span></span>

- <span data-ttu-id="e0dce-130">**Artikelen**: U kunt een lijst met artikelen maken die worden verbruikt bij het uitvoeren van de correctie.</span><span class="sxs-lookup"><span data-stu-id="e0dce-130">**Items** – You can create a list of items that are consumed to perform the correction.</span></span> <span data-ttu-id="e0dce-131">De artikelen kunnen bijvoorbeeld producten zijn die vereist zijn om apparatuur te repareren of ingrediënten die nodig zijn om een eindproduct bij te werken.</span><span class="sxs-lookup"><span data-stu-id="e0dce-131">For example, the items might be products that are required to repair equipment or ingredients that are required to rework a finished product.</span></span>
- <span data-ttu-id="e0dce-132">**Kwaliteitstoeslagen**: U kunt een lijst met toeslagen maken die worden gemaakt of naar externe bronnen worden gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="e0dce-132">**Quality charges** – You can create a list of charges that are incurred or billed out to external sources.</span></span>
- <span data-ttu-id="e0dce-133">**Urenstaat**: U kunt een logboek maken waarind de tijd wordt vastgelegd die elke werknemer besteedt aan de bewerking.</span><span class="sxs-lookup"><span data-stu-id="e0dce-133">**Timesheet** – You can create a log of the time that each worker spends on the operation.</span></span>

<span data-ttu-id="e0dce-134">De overige instellingen zijn optioneel.</span><span class="sxs-lookup"><span data-stu-id="e0dce-134">The remaining settings are optional.</span></span> <span data-ttu-id="e0dce-135">De kosten voor elk artikel, kwaliteitstoeslagen en de urenstaten worden opgeteld en weergegeven in de bewerking.</span><span class="sxs-lookup"><span data-stu-id="e0dce-135">The cost for each item, quality charges, and the timesheet are summed and shown on the operation.</span></span> <span data-ttu-id="e0dce-136">U kunt het veld **Kosten** van de bewerking niet direct bewerken.</span><span class="sxs-lookup"><span data-stu-id="e0dce-136">You can't directly edit the **Cost** field on the operation.</span></span>

### <a name="create-an-operation-for-a-nonconformance"></a><span data-ttu-id="e0dce-137">Een bewerking maken voor een niet-conformering</span><span class="sxs-lookup"><span data-stu-id="e0dce-137">Create an operation for a nonconformance</span></span>

<span data-ttu-id="e0dce-138">Volg deze stappen om een bewerking voor een niet-conformering te maken.</span><span class="sxs-lookup"><span data-stu-id="e0dce-138">To create an operation for a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="e0dce-139">Ga naar **Voorraadbeheer \> Periodieke taken \> Kwaliteitsbeheer \> Niet-conformeringen**.</span><span class="sxs-lookup"><span data-stu-id="e0dce-139">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="e0dce-140">Zoek en selecteer in de lijst de niet-conformering die u wilt bijwerken.</span><span class="sxs-lookup"><span data-stu-id="e0dce-140">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e0dce-141">U kunt alleen bewerkingen toevoegen aan of bijwerken voor niet-conformeringen die zijn goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="e0dce-141">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="e0dce-142">Selecteer in het actievenster **Gerelateerde bewerkingen**.</span><span class="sxs-lookup"><span data-stu-id="e0dce-142">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="e0dce-143">Selecteer op de pagina **Gerelateerde bewerkingen** in het actievenster **Nieuw** om een rij aan het raster toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="e0dce-143">On the **Related operations** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="e0dce-144">Stel daarna de volgende velden in voor de nieuwe rij:</span><span class="sxs-lookup"><span data-stu-id="e0dce-144">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="e0dce-145">**Bewerking**: selecteer de code van de bewerking die voor de niet-conformering wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="e0dce-145">**Operation** – Select the code of the operation that will be performed for the nonconformance.</span></span>
    - <span data-ttu-id="e0dce-146">**Reden**: voer een gedetailleerde omschrijving in waarin u duidelijk maakt waarom de bewerking vereist is.</span><span class="sxs-lookup"><span data-stu-id="e0dce-146">**Reason** – Enter a detailed description that explains why the operation is required.</span></span>
    - <span data-ttu-id="e0dce-147">**Verkooporder**: als de geselecteerde bewerkingscode is gerelateerd aan het verkoopordertype, selecteert u de verkooporder die u aan de bewerking koppelt.</span><span class="sxs-lookup"><span data-stu-id="e0dce-147">**Sales order** – If the selected operation code is related to the sales order type, select the sales order that you're linking the operation to.</span></span>
    - <span data-ttu-id="e0dce-148">**Inkooporder**: als de geselecteerde bewerkingscode is gerelateerd aan het inkoopordertype, selecteert u de inkooporder die u aan de bewerking koppelt.</span><span class="sxs-lookup"><span data-stu-id="e0dce-148">**Purchase order** – If the selected operation code is related to the purchase order type, select the purchase order that you're linking the operation to.</span></span>

1. <span data-ttu-id="e0dce-149">Sluit de pagina's.</span><span class="sxs-lookup"><span data-stu-id="e0dce-149">Close the pages.</span></span>

### <a name="add-items-to-an-operation"></a><span data-ttu-id="e0dce-150">Artikelen aan een bewerking toevoegen</span><span class="sxs-lookup"><span data-stu-id="e0dce-150">Add items to an operation</span></span>

<span data-ttu-id="e0dce-151">Volg deze stappen om artikelen aan een bewerking toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="e0dce-151">To add items to an operation, follow these steps.</span></span>

1. <span data-ttu-id="e0dce-152">Ga naar **Voorraadbeheer \> Periodieke taken \> Kwaliteitsbeheer \> Niet-conformeringen**.</span><span class="sxs-lookup"><span data-stu-id="e0dce-152">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="e0dce-153">Zoek en selecteer in de lijst de niet-conformering die u wilt bijwerken.</span><span class="sxs-lookup"><span data-stu-id="e0dce-153">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e0dce-154">U kunt alleen bewerkingen toevoegen aan of bijwerken voor niet-conformeringen die zijn goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="e0dce-154">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="e0dce-155">Selecteer in het actievenster **Gerelateerde bewerkingen**.</span><span class="sxs-lookup"><span data-stu-id="e0dce-155">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="e0dce-156">Selecteer op de pagina **Gerelateerde bewerkingen** de bewerking waaraan u artikelen wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e0dce-156">On the **Related operations** page, select the operation that you want to add items to.</span></span>
1. <span data-ttu-id="e0dce-157">Selecteer **Artikelen** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="e0dce-157">On the Action Pane, select **Items**.</span></span>
1. <span data-ttu-id="e0dce-158">Selecteer op de pagina **Gerelateerde bewerkingen** in het actievenster **Nieuw** om een rij aan het raster toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="e0dce-158">On the **Related operations** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="e0dce-159">Stel daarna de volgende velden in voor de nieuwe rij:</span><span class="sxs-lookup"><span data-stu-id="e0dce-159">Then set the following fields for new row:</span></span>

    - <span data-ttu-id="e0dce-160">**Artikelnummer**: selecteer het product dat wordt verbruikt als onderdeel van de geselecteerde bewerking.</span><span class="sxs-lookup"><span data-stu-id="e0dce-160">**Item number** – Select the product that will be consumed as part of the selected operation.</span></span>
    - <span data-ttu-id="e0dce-161">**Hoeveelheid**: voer het aantal artikelen in dat wordt verbruikt.</span><span class="sxs-lookup"><span data-stu-id="e0dce-161">**Quantity** – Enter the number of items that will be consumed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e0dce-162">U kunt de kosten voor het artikel zien in het veld **Kosten** op het tabblad **Algemeen**. De kosten die hier worden weergegeven, zijn afkomstig van de kosten die zijn ingesteld op de pagina **Vrijgegeven product**.</span><span class="sxs-lookup"><span data-stu-id="e0dce-162">You can view the cost for the item in the **Cost** field on the **General** tab. The cost that is shown there comes from the cost that is set up on the **Released product** page.</span></span> <span data-ttu-id="e0dce-163">De kosten kunnen niet rechtstreeks worden bijgewerkt op de pagina **Artikelen voor gerelateerde bewerking**.</span><span class="sxs-lookup"><span data-stu-id="e0dce-163">The cost can't be updated directly on the **Related operation item** page.</span></span> <span data-ttu-id="e0dce-164">De kosten van alle artikelen die zijn toegevoegd op de pagina **Artikelen voor gerelateerde bewerking** worden automatisch toegevoegd aan het veld **Kosten** op de pagina **Gerelateerde bewerkingen**.</span><span class="sxs-lookup"><span data-stu-id="e0dce-164">The cost of all items that are added on the **Related operation items** page is automatically added to the **Cost** field on the **Related operations** page.</span></span>

1. <span data-ttu-id="e0dce-165">Herhaal de vorige stap voor elk extra artikel dat u moet toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e0dce-165">Repeat the previous step for each additional item that you must add.</span></span>
1. <span data-ttu-id="e0dce-166">Sluit de pagina's.</span><span class="sxs-lookup"><span data-stu-id="e0dce-166">Close the pages.</span></span>

### <a name="add-quality-charges-to-an-operation"></a><span data-ttu-id="e0dce-167">Kwaliteitstoeslagen aan een bewerking toevoegen</span><span class="sxs-lookup"><span data-stu-id="e0dce-167">Add quality charges to an operation</span></span>

<span data-ttu-id="e0dce-168">Volg deze stappen om kwaliteitstoeslagen aan een bewerking toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="e0dce-168">To add quality charges to an operation, follow these steps.</span></span>

1. <span data-ttu-id="e0dce-169">Ga naar **Voorraadbeheer \> Periodieke taken \> Kwaliteitsbeheer \> Niet-conformeringen**.</span><span class="sxs-lookup"><span data-stu-id="e0dce-169">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="e0dce-170">Zoek en selecteer in de lijst de niet-conformering die u wilt bijwerken.</span><span class="sxs-lookup"><span data-stu-id="e0dce-170">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e0dce-171">U kunt alleen bewerkingen toevoegen aan of bijwerken voor niet-conformeringen die zijn goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="e0dce-171">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="e0dce-172">Selecteer in het actievenster **Gerelateerde bewerkingen**.</span><span class="sxs-lookup"><span data-stu-id="e0dce-172">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="e0dce-173">Selecteer op de pagina **Gerelateerde bewerkingen** de bewerking waaraan u kwaliteitstoeslagen wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e0dce-173">On the **Related operations** page, select the operation that you want to add quality charges to.</span></span>
1. <span data-ttu-id="e0dce-174">Selecteer in het actievenster **Kwaliteitstoeslagen**.</span><span class="sxs-lookup"><span data-stu-id="e0dce-174">On the Action Pane, select **Quality charges**.</span></span>
1. <span data-ttu-id="e0dce-175">Selecteer op de pagina **Gerelateerde kwaliteitstoeslagen** in het actievenster **Nieuw** om een rij aan het raster toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="e0dce-175">On the **Related operation charges** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="e0dce-176">Stel daarna de volgende velden in voor de nieuwe rij:</span><span class="sxs-lookup"><span data-stu-id="e0dce-176">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="e0dce-177">**Toeslagcode**: selecteer de kwaliteitstoeslagen die u wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e0dce-177">**Charges code** – Select the quality charge that you want to add.</span></span>
    - <span data-ttu-id="e0dce-178">**Beschrijving**: voer een gedetailleerde beschrijving van de toeslag in.</span><span class="sxs-lookup"><span data-stu-id="e0dce-178">**Description** – Enter a detailed description of the charge.</span></span>
    - <span data-ttu-id="e0dce-179">**Waarde van toeslagen**: Voer het bedrag van de toeslag in.</span><span class="sxs-lookup"><span data-stu-id="e0dce-179">**Charges value** – Enter the amount of the charge.</span></span>

1. <span data-ttu-id="e0dce-180">Herhaal de vorige stap voor elke extra toeslag die u moet toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e0dce-180">Repeat the previous step for each additional charge that you must add.</span></span>
1. <span data-ttu-id="e0dce-181">Sluit de pagina's.</span><span class="sxs-lookup"><span data-stu-id="e0dce-181">Close the pages.</span></span>

> [!NOTE]
> <span data-ttu-id="e0dce-182">Het bedrag in het veld **Waarde van toeslagen** wordt automatisch opgeteld voor alle kwaliteitstoeslagen en opgeteld bij andere bedragen in het veld **Kosten** op de pagina **Gerelateerde bewerkingen**.</span><span class="sxs-lookup"><span data-stu-id="e0dce-182">The amount in the **Charges value** field is automatically summed for all quality charges and added to any other amounts in the **Cost** field on the **Related operations** page.</span></span>

### <a name="create-a-timesheet-on-an-operation"></a><span data-ttu-id="e0dce-183">Een urenstaat maken voor een bewerking</span><span class="sxs-lookup"><span data-stu-id="e0dce-183">Create a timesheet on an operation</span></span>

<span data-ttu-id="e0dce-184">Volg deze stappen om een urenstaat aan een bewerking toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="e0dce-184">To add a timesheet to an operation, follow these steps.</span></span>

1. <span data-ttu-id="e0dce-185">Ga naar **Voorraadbeheer \> Periodieke taken \> Kwaliteitsbeheer \> Niet-conformeringen**.</span><span class="sxs-lookup"><span data-stu-id="e0dce-185">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="e0dce-186">Zoek en selecteer in de lijst de niet-conformering die u wilt bijwerken.</span><span class="sxs-lookup"><span data-stu-id="e0dce-186">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e0dce-187">U kunt alleen bewerkingen toevoegen aan of bijwerken voor niet-conformeringen die zijn goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="e0dce-187">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="e0dce-188">Selecteer in het actievenster **Gerelateerde bewerkingen**.</span><span class="sxs-lookup"><span data-stu-id="e0dce-188">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="e0dce-189">Selecteer op de pagina **Gerelateerde bewerkingen** de bewerking waaraan u een urenstaat wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e0dce-189">On the **Related operations** page, select the operation that you want to add a timesheet to.</span></span>
1. <span data-ttu-id="e0dce-190">Selecteer in het actievenster de optie **Urenstaat**.</span><span class="sxs-lookup"><span data-stu-id="e0dce-190">On the Action Pane, select **Timesheet**.</span></span>
1. <span data-ttu-id="e0dce-191">Selecteer op de pagina **Gerelateerde urenstaten** in het actievenster **Nieuw** om een rij aan het raster toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="e0dce-191">On the **Related operation time sheets** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="e0dce-192">Stel daarna de volgende velden in voor de nieuwe rij:</span><span class="sxs-lookup"><span data-stu-id="e0dce-192">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="e0dce-193">**Datum**: Geef de datum op waarop het werk is uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="e0dce-193">**Date** – Specify the date when work was done.</span></span> <span data-ttu-id="e0dce-194">Dit veld is standaard ingesteld op de huidige datum.</span><span class="sxs-lookup"><span data-stu-id="e0dce-194">By default, this field is set to the current date.</span></span>
    - <span data-ttu-id="e0dce-195">**Medewerker**: Selecteer de medewerker die het werk heeft uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="e0dce-195">**Worker** – Select the worker who did the work.</span></span> <span data-ttu-id="e0dce-196">Dit veld is standaard ingesteld op de medewerker die aan de huidige gebruiker is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="e0dce-196">By default, this field is set to the worker that is assigned to the current user.</span></span>
    - <span data-ttu-id="e0dce-197">**Bewerkingstijd**: voer het aantal uren in dat aan de geselecteerde bewerking is besteed.</span><span class="sxs-lookup"><span data-stu-id="e0dce-197">**Operation hours** – Enter the number of hours that were worked on the selected operation.</span></span>
    - <span data-ttu-id="e0dce-198">**Gefactureerd**: Schakel dit selectievakje in als de tijd op een factuur in rekening is gebracht aan een klant of leverancier.</span><span class="sxs-lookup"><span data-stu-id="e0dce-198">**Invoiced** – Select this check box if the time has been charged to a customer or vendor on an invoice.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e0dce-199">U kunt de kosten bekijken in het veld **Kosten** op het tabblad **Algemeen**. De kosten worden berekend op basis van het tarief dat u definieert op de pagina **Parameters voor voorraadbeheer**.</span><span class="sxs-lookup"><span data-stu-id="e0dce-199">You can view the cost in the **Cost** field on the **General** tab. The cost is calculated by using the rate that you define on the **Inventory management parameters** page.</span></span>

1. <span data-ttu-id="e0dce-200">Herhaal de vorige stap voor elke extra urenstaatregel die u moet toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e0dce-200">Repeat the previous step for each additional timesheet line that you must add.</span></span>
1. <span data-ttu-id="e0dce-201">Sluit de pagina's.</span><span class="sxs-lookup"><span data-stu-id="e0dce-201">Close the pages.</span></span>

> [!NOTE]
> <span data-ttu-id="e0dce-202">Het bedrag in het veld **Kosten** wordt automatisch opgeteld voor alle urenstaatregels en opgeteld bij andere bedragen in het veld **Kosten** op de pagina **Gerelateerde bewerkingen**.</span><span class="sxs-lookup"><span data-stu-id="e0dce-202">The amount in the **Cost** field is summed for all timesheet lines and added to any other amounts in the **Cost** field on the **Related operations** page.</span></span>

## <a name="add-a-correction-to-a-nonconformance"></a><span data-ttu-id="e0dce-203">Een correctie aan een niet-conformering toevoegen</span><span class="sxs-lookup"><span data-stu-id="e0dce-203">Add a correction to a nonconformance</span></span>

<span data-ttu-id="e0dce-204">Om een correctie aan een niet-conformering toe te voegen, volgt u deze stappen.</span><span class="sxs-lookup"><span data-stu-id="e0dce-204">To add a correction to a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="e0dce-205">Ga naar **Voorraadbeheer \> Periodieke taken \> Kwaliteitsbeheer \> Niet-conformeringen**.</span><span class="sxs-lookup"><span data-stu-id="e0dce-205">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="e0dce-206">Zoek en selecteer in de lijst de niet-conformering die u wilt bijwerken.</span><span class="sxs-lookup"><span data-stu-id="e0dce-206">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e0dce-207">U kunt alleen een correctie toevoegen aan niet-conformeringen die zijn goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="e0dce-207">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="e0dce-208">Selecteer in het actievenster de optie **Correcties**.</span><span class="sxs-lookup"><span data-stu-id="e0dce-208">On the Action Pane, select **Corrections**.</span></span>
1. <span data-ttu-id="e0dce-209">Selecteer op de pagina **Correcties** in het actievenster de optie **Nieuw** om een rij aan het raster toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="e0dce-209">On the **Corrections** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="e0dce-210">Stel daarna de volgende velden in voor de nieuwe rij:</span><span class="sxs-lookup"><span data-stu-id="e0dce-210">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="e0dce-211">**Diagnose**: selecteer het type diagnose dat het type correctie aangeeft dat u maakt.</span><span class="sxs-lookup"><span data-stu-id="e0dce-211">**Diagnostic** – Select the diagnostic type that identifies the type of correction that you're creating.</span></span>
    - <span data-ttu-id="e0dce-212">**Medewerker**: selecteer de persoon die verantwoordelijk is voor de correctie.</span><span class="sxs-lookup"><span data-stu-id="e0dce-212">**Worker** – Select the person who is responsible for the correction.</span></span>
    - <span data-ttu-id="e0dce-213">**Correctieprioriteit**: selecteer een optie om aan te geven wat de prioriteit van de correctie is (*Laag*, *Normaal* of *Hoog*).</span><span class="sxs-lookup"><span data-stu-id="e0dce-213">**Correction priority** – Select an option to indicate how the correction should be prioritized (*Low*, *Normal*, or *High*).</span></span>
    - <span data-ttu-id="e0dce-214">**Gevraagde datum**: voer de datum in waarop de corrigerende actie is aangevraagd.</span><span class="sxs-lookup"><span data-stu-id="e0dce-214">**Requested date** – Enter the date when the corrective action was requested.</span></span>
    - <span data-ttu-id="e0dce-215">**Geplande datum**: voer de datum in waarop de correctie naar verwachting is voltooid.</span><span class="sxs-lookup"><span data-stu-id="e0dce-215">**Planned date** – Enter the date when the correction is expected to be completed.</span></span>
    - <span data-ttu-id="e0dce-216">**Kortetermijnoplossing**: schakel dit selectievakje in als de corrigerende actie de niet-conformering slechts voor korte tijd corrigeert.</span><span class="sxs-lookup"><span data-stu-id="e0dce-216">**Short term solution** – Select this check box if the corrective action corrects the nonconformance only for a short time.</span></span>

1. <span data-ttu-id="e0dce-217">Sluit de pagina's.</span><span class="sxs-lookup"><span data-stu-id="e0dce-217">Close the pages.</span></span>

## <a name="mark-a-correction-as-completed"></a><span data-ttu-id="e0dce-218">Een correctie als voltooid markeren</span><span class="sxs-lookup"><span data-stu-id="e0dce-218">Mark a correction as completed</span></span>

<span data-ttu-id="e0dce-219">Om een correctie van een niet-conformering te markeren als voltooid, volgt u deze stappen.</span><span class="sxs-lookup"><span data-stu-id="e0dce-219">To mark a nonconformance correction as completed, follow these steps.</span></span>

1. <span data-ttu-id="e0dce-220">Ga naar **Voorraadbeheer \> Periodieke taken \> Kwaliteitsbeheer \> Niet-conformeringen**.</span><span class="sxs-lookup"><span data-stu-id="e0dce-220">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="e0dce-221">Zoek en selecteer in de lijst de niet-conformering die u wilt bijwerken.</span><span class="sxs-lookup"><span data-stu-id="e0dce-221">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e0dce-222">U kunt alleen een correctie toevoegen aan niet-conformeringen die zijn goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="e0dce-222">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="e0dce-223">Selecteer in het actievenster de optie **Correcties**.</span><span class="sxs-lookup"><span data-stu-id="e0dce-223">On the Action Pane, select **Corrections**.</span></span>
1. <span data-ttu-id="e0dce-224">Selecteer op de pagina **Correcties** in het raster de correctie die u wilt markeren als voltooid.</span><span class="sxs-lookup"><span data-stu-id="e0dce-224">On the **Corrections** page, in the grid, select the correction that you want to mark as completed.</span></span>
1. <span data-ttu-id="e0dce-225">Selecteer in het actievenster **Als voltooid markeren**.</span><span class="sxs-lookup"><span data-stu-id="e0dce-225">On the Action Pane, select **Mark complete**.</span></span>
1. <span data-ttu-id="e0dce-226">U wordt gevraagd om de selectie te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="e0dce-226">You're prompted to confirm your selection.</span></span> <span data-ttu-id="e0dce-227">Selecteer **OK** om door te gaan.</span><span class="sxs-lookup"><span data-stu-id="e0dce-227">Select **OK** to continue.</span></span> <span data-ttu-id="e0dce-228">Het veld **Datum en tijd voltooiing** is ingesteld op de huidige datum en tijd en het selectievakje **Voltooid** is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="e0dce-228">The **Completion date and time** field is set to the current date and time, and the **Completed** check box is selected.</span></span>
1. <span data-ttu-id="e0dce-229">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e0dce-229">Close the page.</span></span>

## <a name="reopen-a-completed-correction"></a><span data-ttu-id="e0dce-230">Een voltooide correctie opnieuw openen</span><span class="sxs-lookup"><span data-stu-id="e0dce-230">Reopen a completed correction</span></span>

<span data-ttu-id="e0dce-231">Om een voltooide correctie opnieuw te openen, volgt u deze stappen.</span><span class="sxs-lookup"><span data-stu-id="e0dce-231">To reopen a completed correction, follow these steps.</span></span>

1. <span data-ttu-id="e0dce-232">Ga naar **Voorraadbeheer \> Periodieke taken \> Kwaliteitsbeheer \> Niet-conformeringen**.</span><span class="sxs-lookup"><span data-stu-id="e0dce-232">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="e0dce-233">Zoek en selecteer in de lijst de niet-conformering die u wilt bijwerken.</span><span class="sxs-lookup"><span data-stu-id="e0dce-233">In the list, select the nonconformance that you want to update.</span></span>
1. <span data-ttu-id="e0dce-234">Selecteer in het actievenster de optie **Correcties**.</span><span class="sxs-lookup"><span data-stu-id="e0dce-234">On the Action pane, select **Corrections**.</span></span>
1. <span data-ttu-id="e0dce-235">Selecteer op de pagina **Correcties** in het raster de correctie die u opnieuw wilt openen.</span><span class="sxs-lookup"><span data-stu-id="e0dce-235">On the **Corrections** page, in the grid, select the correction that you want to reopen.</span></span>
1. <span data-ttu-id="e0dce-236">Selecteer **Opnieuw openen** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="e0dce-236">On the Action Pane, select **Reopen**.</span></span>
1. <span data-ttu-id="e0dce-237">U wordt gevraagd om de selectie te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="e0dce-237">You're prompted to confirm your selection.</span></span> <span data-ttu-id="e0dce-238">Selecteer **OK** om door te gaan.</span><span class="sxs-lookup"><span data-stu-id="e0dce-238">Select **OK** to continue.</span></span> <span data-ttu-id="e0dce-239">De waarde wordt gewist uit het veld **Datum en tijd voltooiing** en het selectievakje **Voltooid** wordt uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="e0dce-239">The value is cleared from the **Completion date and time** field, and the **Completed** check box is cleared.</span></span>
1. <span data-ttu-id="e0dce-240">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e0dce-240">Close the page.</span></span>

<span data-ttu-id="e0dce-241">U kunt nu extra bewerkingen of updates aan de correctie toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e0dce-241">You can now make additional edits or updates to the correction.</span></span> <span data-ttu-id="e0dce-242">Wanneer u klaar bent, kunt u de correctie opnieuw markeren als voltooid.</span><span class="sxs-lookup"><span data-stu-id="e0dce-242">When you've finished, you can mark the correction as completed again.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="e0dce-243">Een niet-conformering sluiten</span><span class="sxs-lookup"><span data-stu-id="e0dce-243">Close a nonconformance</span></span>

<span data-ttu-id="e0dce-244">Volg deze stappen om een niet-conformering te sluiten.</span><span class="sxs-lookup"><span data-stu-id="e0dce-244">To close a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="e0dce-245">Ga naar **Voorraadbeheer \> Periodieke taken \> Kwaliteitsbeheer \> Kwaliteitsorders**.</span><span class="sxs-lookup"><span data-stu-id="e0dce-245">Go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>
1. <span data-ttu-id="e0dce-246">Selecteer een kwaliteitsorder in het raster.</span><span class="sxs-lookup"><span data-stu-id="e0dce-246">Select a quality order in the grid.</span></span>
1. <span data-ttu-id="e0dce-247">Selecteer **Query's \> Niet-conformeringen** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="e0dce-247">On the Action Pane, select **Inquiries \> Non conformances**.</span></span>
1. <span data-ttu-id="e0dce-248">Selecteer op de pagina **Niet-conformeringen** de gewenste niet-conformering in het raster.</span><span class="sxs-lookup"><span data-stu-id="e0dce-248">On the **Non conformances** page, select the target nonconformance in the grid.</span></span>
1. <span data-ttu-id="e0dce-249">Selecteer in het actievenster **Functies \> Niet-conformering sluiten**.</span><span class="sxs-lookup"><span data-stu-id="e0dce-249">On the Action Pane, select **Functions \> Close non conformance**.</span></span>
1. <span data-ttu-id="e0dce-250">U wordt gevraagd om de selectie te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="e0dce-250">You're prompted to confirm your selection.</span></span> <span data-ttu-id="e0dce-251">Selecteer **Ja** om door te gaan.</span><span class="sxs-lookup"><span data-stu-id="e0dce-251">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="e0dce-252">Sluit de pagina's.</span><span class="sxs-lookup"><span data-stu-id="e0dce-252">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e0dce-253">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="e0dce-253">Additional resources</span></span>

- [<span data-ttu-id="e0dce-254">Overzicht van kwaliteitsbeheer</span><span class="sxs-lookup"><span data-stu-id="e0dce-254">Quality management overview</span></span>](../quality-management-processes.md)
- [<span data-ttu-id="e0dce-255">Beheer van kwaliteit en niet-conformeringen inschakelen</span><span class="sxs-lookup"><span data-stu-id="e0dce-255">Enable quality and nonconformance management</span></span>](../enable-quality-management.md)
- [<span data-ttu-id="e0dce-256">Medewerkers die verantwoordelijk zijn voor het goedkeuren van niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="e0dce-256">Workers responsible for approving nonconformances</span></span>](../quality-responsible-workers.md)
- [<span data-ttu-id="e0dce-257">Quarantainezones voor niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="e0dce-257">Quarantine zones for nonconformances</span></span>](../quality-quarantine-zones.md)
- [<span data-ttu-id="e0dce-258">Typen diagnosen voor niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="e0dce-258">Diagnostic types for nonconformances</span></span>](../quality-diagnostic-types.md)
- [<span data-ttu-id="e0dce-259">Kwaliteitstoeslagen voor niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="e0dce-259">Quality charges for nonconformances</span></span>](../quality-charges.md)
- [<span data-ttu-id="e0dce-260">Bewerkingen voor niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="e0dce-260">Operations for nonconformances</span></span>](../quality-operations.md)
- [<span data-ttu-id="e0dce-261">Kwaliteitsbeheer voor magazijnprocessen</span><span class="sxs-lookup"><span data-stu-id="e0dce-261">Quality management for warehouse processes</span></span>](../quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
