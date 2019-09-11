---
title: Foutbeheer
description: In dit onderwerp wordt foutbeheer in Activabeheer uitgelegd.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 48c90a8b776cc16804de8e20ada7d8ca347fa5b9
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874734"
---
# <a name="fault-management"></a><span data-ttu-id="c0e96-103">Foutbeheer</span><span class="sxs-lookup"><span data-stu-id="c0e96-103">Fault management</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="c0e96-104">In Activabeheer kunt u de foutontwerper gebruiken om foutsymptomen, foutgebieden en foutsoorten in te stellen voor typen activa.</span><span class="sxs-lookup"><span data-stu-id="c0e96-104">In Asset Management, you can use the fault designer to set up fault symptoms, fault areas, and fault types on asset types.</span></span> <span data-ttu-id="c0e96-105">Op deze manier kunt u fouten beheren die op activa zijn gedetecteerd.</span><span class="sxs-lookup"><span data-stu-id="c0e96-105">In this way, you can manage faults that are detected on assets.</span></span> <span data-ttu-id="c0e96-106">Bovendien kunnen de foutoorzaken en suggesties voor het corrigeren van fouten op een werkorder worden geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="c0e96-106">Additionally, fault causes and suggestions for fixing faults can be registered on a work order.</span></span>

<span data-ttu-id="c0e96-107">Het proces voor foutregistratie en -beheer bestaat uit de volgende stappen.</span><span class="sxs-lookup"><span data-stu-id="c0e96-107">The process for fault registration and management consists of these steps.</span></span>

1. <span data-ttu-id="c0e96-108">Een lijst met foutsymptomen, foutgebieden en foutsoorten maken die mogelijk voorkomen op uw typen activa.</span><span class="sxs-lookup"><span data-stu-id="c0e96-108">Create a list of fault symptoms, fault areas, and fault types that might occur on your asset types.</span></span>
2. <span data-ttu-id="c0e96-109">In de foutontwerper stelt u symptomen, foutgebieden en fouttypen in.</span><span class="sxs-lookup"><span data-stu-id="c0e96-109">In the fault designer, set up symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="c0e96-110">Hier volgen enkele voorbeelden om u te helpen het verschil te begrijpen tussen foutsymptomen, foutgebieden en fouttypen.</span><span class="sxs-lookup"><span data-stu-id="c0e96-110">Here are some examples to help you understand the difference between fault symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="c0e96-111">**Foutsymptomen:**</span><span class="sxs-lookup"><span data-stu-id="c0e96-111">**Fault symptoms:**</span></span>

- <span data-ttu-id="c0e96-112">Onevenwichtige spanningen</span><span class="sxs-lookup"><span data-stu-id="c0e96-112">Unbalanced voltages</span></span>
- <span data-ttu-id="c0e96-113">Kortsluiting</span><span class="sxs-lookup"><span data-stu-id="c0e96-113">Short circuit</span></span>
- <span data-ttu-id="c0e96-114">Lawaai</span><span class="sxs-lookup"><span data-stu-id="c0e96-114">Noise</span></span>
- <span data-ttu-id="c0e96-115">Lek</span><span class="sxs-lookup"><span data-stu-id="c0e96-115">Leak</span></span>
- <span data-ttu-id="c0e96-116">Trillingen</span><span class="sxs-lookup"><span data-stu-id="c0e96-116">Vibrations</span></span>

<span data-ttu-id="c0e96-117">**Foutgebieden:**</span><span class="sxs-lookup"><span data-stu-id="c0e96-117">**Fault areas:**</span></span>

- <span data-ttu-id="c0e96-118">Elektrisch</span><span class="sxs-lookup"><span data-stu-id="c0e96-118">Electrical</span></span>
- <span data-ttu-id="c0e96-119">Mechanisch</span><span class="sxs-lookup"><span data-stu-id="c0e96-119">Mechanical</span></span>
- <span data-ttu-id="c0e96-120">Hydraulisch</span><span class="sxs-lookup"><span data-stu-id="c0e96-120">Hydraulic</span></span>
- <span data-ttu-id="c0e96-121">Pneumatisch</span><span class="sxs-lookup"><span data-stu-id="c0e96-121">Pneumatic</span></span>

<span data-ttu-id="c0e96-122">**Foutsoorten:**</span><span class="sxs-lookup"><span data-stu-id="c0e96-122">**Fault types:**</span></span>

- <span data-ttu-id="c0e96-123">Defecte hoofdstatorwikkeling</span><span class="sxs-lookup"><span data-stu-id="c0e96-123">Faulty main stator winding</span></span>
- <span data-ttu-id="c0e96-124">Defecte diode</span><span class="sxs-lookup"><span data-stu-id="c0e96-124">Faulty diode</span></span>
- <span data-ttu-id="c0e96-125">Vervuilde wikkelingen</span><span class="sxs-lookup"><span data-stu-id="c0e96-125">Dirty windings</span></span>
- <span data-ttu-id="c0e96-126">Defecte generator</span><span class="sxs-lookup"><span data-stu-id="c0e96-126">Defective generator</span></span>
- <span data-ttu-id="c0e96-127">Defecte sensor</span><span class="sxs-lookup"><span data-stu-id="c0e96-127">Defective sensor</span></span>

## <a name="create-fault-symptoms"></a><span data-ttu-id="c0e96-128">Foutsymptomen maken</span><span class="sxs-lookup"><span data-stu-id="c0e96-128">Create fault symptoms</span></span>

<span data-ttu-id="c0e96-129">Voer de volgende stappen uit om een lijst met symptomen te maken die kunnen worden gebruikt in de foutontwerper.</span><span class="sxs-lookup"><span data-stu-id="c0e96-129">Follow these steps to create a list of symptoms that can be used in the fault designer.</span></span>

1. <span data-ttu-id="c0e96-130">Selecteer **Activabeheer** \> **Instellingen** \> **Fout** \> **Foutsymptomen**.</span><span class="sxs-lookup"><span data-stu-id="c0e96-130">Select **Asset management** \> **Setup** \> **Fault** \> **Fault symptoms**.</span></span>
2. <span data-ttu-id="c0e96-131">Selecteer **Nieuw** om een record te maken.</span><span class="sxs-lookup"><span data-stu-id="c0e96-131">Select **New** to create a record.</span></span>
3. <span data-ttu-id="c0e96-132">Voer in het veld **Foutsymptoom** een naam in voor het foutsymptoom.</span><span class="sxs-lookup"><span data-stu-id="c0e96-132">In the **Fault symptom** field, enter a name for the fault symptom.</span></span>
4. <span data-ttu-id="c0e96-133">Voer in het veld **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="c0e96-133">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="c0e96-134">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c0e96-134">Select **Save**.</span></span>

## <a name="create-fault-areas"></a><span data-ttu-id="c0e96-135">Foutgebieden maken</span><span class="sxs-lookup"><span data-stu-id="c0e96-135">Create fault areas</span></span>

<span data-ttu-id="c0e96-136">Voer de volgende stappen uit om een lijst met gebieden of locaties te maken die kunnen worden gebruikt in de foutontwerper.</span><span class="sxs-lookup"><span data-stu-id="c0e96-136">Follow these steps to create a list of areas or locations that can be used in the fault designer.</span></span>

1. <span data-ttu-id="c0e96-137">Selecteer **Activabeheer** \> **Instellingen** \> **Fout** \> **Foutsymptomen**.</span><span class="sxs-lookup"><span data-stu-id="c0e96-137">Select **Asset management** \> **Setup** \> **Fault** \> **Fault areas**.</span></span>
2. <span data-ttu-id="c0e96-138">Selecteer **Nieuw** om een record te maken.</span><span class="sxs-lookup"><span data-stu-id="c0e96-138">Select **New** to create a record.</span></span>
3. <span data-ttu-id="c0e96-139">Voer in het veld **Foutsymptoom** een naam in voor het foutsymptoom.</span><span class="sxs-lookup"><span data-stu-id="c0e96-139">In the **Fault area** field, enter a name for the fault area.</span></span>
4. <span data-ttu-id="c0e96-140">Voer in het veld **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="c0e96-140">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="c0e96-141">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c0e96-141">Select **Save**.</span></span>

## <a name="create-fault-types"></a><span data-ttu-id="c0e96-142">Foutsoorten maken</span><span class="sxs-lookup"><span data-stu-id="c0e96-142">Create fault types</span></span>

<span data-ttu-id="c0e96-143">Voer de volgende stappen uit om een lijst met foutsoorten te maken die kunnen worden gebruikt in de foutontwerper.</span><span class="sxs-lookup"><span data-stu-id="c0e96-143">Follow these steps to create a list of fault types that can be used in the fault designer.</span></span>

1. <span data-ttu-id="c0e96-144">Selecteer **Activabeheer** \> **Instellingen** \> **Fout** \> **Type fouten**.</span><span class="sxs-lookup"><span data-stu-id="c0e96-144">Select **Asset management** \> **Setup** \> **Fault** \> **Fault types**.</span></span>
2. <span data-ttu-id="c0e96-145">Selecteer **Nieuw** om een record te maken.</span><span class="sxs-lookup"><span data-stu-id="c0e96-145">Select **New** to create a record.</span></span>
3. <span data-ttu-id="c0e96-146">Voer in het veld **Type fout** een naam op voor het type fout.</span><span class="sxs-lookup"><span data-stu-id="c0e96-146">In the **Fault type** field, enter a name for the fault type.</span></span>
4. <span data-ttu-id="c0e96-147">Voer in het veld **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="c0e96-147">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="c0e96-148">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c0e96-148">Select **Save**.</span></span>

## <a name="set-up-the-fault-designer"></a><span data-ttu-id="c0e96-149">De foutontwerper instellen</span><span class="sxs-lookup"><span data-stu-id="c0e96-149">Set up the fault designer</span></span>

<span data-ttu-id="c0e96-150">In de foutontwerper stelt u foutgegevens in voor typen activa.</span><span class="sxs-lookup"><span data-stu-id="c0e96-150">In the fault designer, you set up fault data on asset types.</span></span>

1. <span data-ttu-id="c0e96-151">Selecteer **Activabeheer** \> **Instellingen** \> **Fout** \> **Foutontwerper**.</span><span class="sxs-lookup"><span data-stu-id="c0e96-151">Select **Asset management** \> **Setup** \> **Fault** \> **Fault designer**.</span></span>
2. <span data-ttu-id="c0e96-152">Selecteer in het linkerdeelvenster het type activa waarvoor u een foutrecord wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="c0e96-152">In the left pane, select the type of asset to set up a fault record for.</span></span>
3. <span data-ttu-id="c0e96-153">Selecteer in het Sneltabblad **Foutsymptoom** de optie **regel toevoegen** en selecteer vervolgens in het veld **Foutsymptoom** een foutsymptoom.</span><span class="sxs-lookup"><span data-stu-id="c0e96-153">On the **Fault symptom** FastTab, select **Add line**, and then, in the **Fault symptom** field, select a fault symptom.</span></span>
4. <span data-ttu-id="c0e96-154">Selecteer in het Sneltabblad **Foutgebied** de optie **Regel toevoegen** en selecteer vervolgens in het veld **Foutgebied** een foutgebied.</span><span class="sxs-lookup"><span data-stu-id="c0e96-154">On the **Fault area** FastTab, select **Add line**, and then, in the **Fault area** field select a fault area.</span></span>
5. <span data-ttu-id="c0e96-155">Selecteer in het Sneltabblad **Fouttype** de optie **Regel toevoegen** en selecteer vervolgens in het veld **Fouttype** een fouttype.</span><span class="sxs-lookup"><span data-stu-id="c0e96-155">On the **Fault type** FastTab, select **Add line**, and then, in the **Fault type** field, select a fault type.</span></span>
6. <span data-ttu-id="c0e96-156">Om snel combinaties van alle bestaande foutsymptomen, -gebieden en -typen voor het geselecteerde activatype te maken, selecteert u **Foutcombinaties** maken.</span><span class="sxs-lookup"><span data-stu-id="c0e96-156">To quickly create combinations of all existing fault symptoms, areas, and types for the selected asset type, select **Create fault combinations**.</span></span> <span data-ttu-id="c0e96-157">Deze functie is handig als u veel foutsymptomen, -gebieden en -typen hebt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="c0e96-157">This function is useful if you've added many fault symptoms, areas, and types.</span></span> <span data-ttu-id="c0e96-158">Het is eenvoudiger om de regels te verwijderen voor alle combinaties die niet relevant zijn voor het type activum dan om handmatig nieuwe regels te maken.</span><span class="sxs-lookup"><span data-stu-id="c0e96-158">It's easier to delete the lines for any combinations that aren't relevant to the asset type than to create new lines manually.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c0e96-159">Als u de instellingen van foutsymptomen, -gebieden en -typen van het ene type activum naar het geselecteerde type activum wilt kopiëren, selecteert u **Kopiëren vanuit activum type**.</span><span class="sxs-lookup"><span data-stu-id="c0e96-159">To copy the setup of fault symptoms, areas, and types from one asset type to the selected asset type, select **Copy from asset type**.</span></span>

7. <span data-ttu-id="c0e96-160">Klik op **Opslaan** om uw wijzigingen op te slaan.</span><span class="sxs-lookup"><span data-stu-id="c0e96-160">Select **Save** to save your changes.</span></span>

![Figuur 1](media/21-setup-for-work-orders.png)

## <a name="create-fault-causes"></a><span data-ttu-id="c0e96-162">Foutoorzaken maken</span><span class="sxs-lookup"><span data-stu-id="c0e96-162">Create fault causes</span></span>

<span data-ttu-id="c0e96-163">Volg deze stappen om een lijst met bekende foutoorzaken te maken die kunnen worden toegevoegd aan een werkorder of een onderhoudsaanvraag.</span><span class="sxs-lookup"><span data-stu-id="c0e96-163">Follow these steps to create a list of known fault causes that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="c0e96-164">Selecteer **Activabeheer** \> **Instellingen** \> **Fout** \> **Foutoorzaken**.</span><span class="sxs-lookup"><span data-stu-id="c0e96-164">Select **Asset management** \> **Setup** \> **Fault** \> **Fault causes**.</span></span>
2. <span data-ttu-id="c0e96-165">Selecteer **Nieuw** om een record te maken.</span><span class="sxs-lookup"><span data-stu-id="c0e96-165">Select **New** to create a record.</span></span>
3. <span data-ttu-id="c0e96-166">Voer in het veld **Foutoorzaak** een naam op voor de foutoorzaak.</span><span class="sxs-lookup"><span data-stu-id="c0e96-166">In the **Fault cause** field, enter a name for the fault cause.</span></span>
4. <span data-ttu-id="c0e96-167">Voer in het veld **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="c0e96-167">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="c0e96-168">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c0e96-168">Select **Save**.</span></span>

## <a name="create-fault-remedies"></a><span data-ttu-id="c0e96-169">Foutoplossingen maken</span><span class="sxs-lookup"><span data-stu-id="c0e96-169">Create fault remedies</span></span>

<span data-ttu-id="c0e96-170">Volg deze stappen om een lijst met suggesties voor oplossing en reparatie te maken die kunnen worden toegevoegd aan een werkorder of een onderhoudsaanvraag.</span><span class="sxs-lookup"><span data-stu-id="c0e96-170">Follow these steps to create a list of suggestions for remedy and repair that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="c0e96-171">Selecteer **Activabeheer** \> **Instellingen** \> **Fout** \> **Foutoplossing**.</span><span class="sxs-lookup"><span data-stu-id="c0e96-171">Select **Asset management** \> **Setup** \> **Fault** \> **Fault remedies**.</span></span>
2. <span data-ttu-id="c0e96-172">Selecteer **Nieuw** om een record te maken.</span><span class="sxs-lookup"><span data-stu-id="c0e96-172">Select **New** to create a record.</span></span>
3. <span data-ttu-id="c0e96-173">Voer in het veld **Foutoplossing** een naam in voor de foutoplossing.</span><span class="sxs-lookup"><span data-stu-id="c0e96-173">In the **Fault remedy** field, enter a name for the fault remedy.</span></span>
4. <span data-ttu-id="c0e96-174">Voer in het veld **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="c0e96-174">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="c0e96-175">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c0e96-175">Select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="c0e96-176">U kunt de namen van uw foutsymptomen, -gebieden, -typen, -oorzaken en -oplossingen wijzigen als dat nodig is.</span><span class="sxs-lookup"><span data-stu-id="c0e96-176">You can change the names of your fault symptoms, areas, types, causes, and remedies as you require.</span></span> <span data-ttu-id="c0e96-177">De naamswijzigingen worden automatisch weergegeven in de gerelateerde foutregistraties.</span><span class="sxs-lookup"><span data-stu-id="c0e96-177">The name changes are automatically reflected in the related fault registrations.</span></span>
