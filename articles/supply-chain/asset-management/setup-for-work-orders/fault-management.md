---
title: Foutbeheer
description: In dit onderwerp wordt foutbeheer in Activabeheer uitgelegd.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetFaultArea, EntAssetFaultDesigner, EntAssetFaultCopyFromObjectType, EntAssetFaultRemedy, EntAssetObjectFaultRelationRequestInfoPart, EntAssetObjectFaultRelationWorkOrderInfoPart, EntAssetFaultCreateCombinations, EntAssetObjectFaultSymptom, EntAssetObjectFaultSymptomListPage, EntAssetFaultType, EntAssetFaultSymptom, EntAssetFaultCause
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 176fbebcf88e7557bf2bafc56524cd2ec015220e
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020959"
---
# <a name="fault-management"></a><span data-ttu-id="90794-103">Foutbeheer</span><span class="sxs-lookup"><span data-stu-id="90794-103">Fault management</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="90794-104">In Activabeheer kunt u de foutontwerper gebruiken om foutsymptomen, foutgebieden en foutsoorten in te stellen voor typen activa.</span><span class="sxs-lookup"><span data-stu-id="90794-104">In Asset Management, you can use the fault designer to set up fault symptoms, fault areas, and fault types on asset types.</span></span> <span data-ttu-id="90794-105">Op deze manier kunt u fouten beheren die op activa zijn gedetecteerd.</span><span class="sxs-lookup"><span data-stu-id="90794-105">In this way, you can manage faults that are detected on assets.</span></span> <span data-ttu-id="90794-106">Bovendien kunnen de foutoorzaken en suggesties voor het corrigeren van fouten op een werkorder worden geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="90794-106">Additionally, fault causes and suggestions for fixing faults can be registered on a work order.</span></span>

<span data-ttu-id="90794-107">Het proces voor foutregistratie en -beheer bestaat uit de volgende stappen.</span><span class="sxs-lookup"><span data-stu-id="90794-107">The process for fault registration and management consists of these steps.</span></span>

1. <span data-ttu-id="90794-108">Een lijst met foutsymptomen, foutgebieden en foutsoorten maken die mogelijk voorkomen op uw typen activa.</span><span class="sxs-lookup"><span data-stu-id="90794-108">Create a list of fault symptoms, fault areas, and fault types that might occur on your asset types.</span></span>
2. <span data-ttu-id="90794-109">In de foutontwerper stelt u symptomen, foutgebieden en fouttypen in.</span><span class="sxs-lookup"><span data-stu-id="90794-109">In the fault designer, set up symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="90794-110">Hier volgen enkele voorbeelden om u te helpen het verschil te begrijpen tussen foutsymptomen, foutgebieden en fouttypen.</span><span class="sxs-lookup"><span data-stu-id="90794-110">Here are some examples to help you understand the difference between fault symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="90794-111">**Foutsymptomen:**</span><span class="sxs-lookup"><span data-stu-id="90794-111">**Fault symptoms:**</span></span>

- <span data-ttu-id="90794-112">Onevenwichtige spanningen</span><span class="sxs-lookup"><span data-stu-id="90794-112">Unbalanced voltages</span></span>
- <span data-ttu-id="90794-113">Kortsluiting</span><span class="sxs-lookup"><span data-stu-id="90794-113">Short circuit</span></span>
- <span data-ttu-id="90794-114">Lawaai</span><span class="sxs-lookup"><span data-stu-id="90794-114">Noise</span></span>
- <span data-ttu-id="90794-115">Lek</span><span class="sxs-lookup"><span data-stu-id="90794-115">Leak</span></span>
- <span data-ttu-id="90794-116">Trillingen</span><span class="sxs-lookup"><span data-stu-id="90794-116">Vibrations</span></span>

<span data-ttu-id="90794-117">**Foutgebieden:**</span><span class="sxs-lookup"><span data-stu-id="90794-117">**Fault areas:**</span></span>

- <span data-ttu-id="90794-118">Elektrisch</span><span class="sxs-lookup"><span data-stu-id="90794-118">Electrical</span></span>
- <span data-ttu-id="90794-119">Mechanisch</span><span class="sxs-lookup"><span data-stu-id="90794-119">Mechanical</span></span>
- <span data-ttu-id="90794-120">Hydraulisch</span><span class="sxs-lookup"><span data-stu-id="90794-120">Hydraulic</span></span>
- <span data-ttu-id="90794-121">Pneumatisch</span><span class="sxs-lookup"><span data-stu-id="90794-121">Pneumatic</span></span>

<span data-ttu-id="90794-122">**Foutsoorten:**</span><span class="sxs-lookup"><span data-stu-id="90794-122">**Fault types:**</span></span>

- <span data-ttu-id="90794-123">Defecte hoofdstatorwikkeling</span><span class="sxs-lookup"><span data-stu-id="90794-123">Faulty main stator winding</span></span>
- <span data-ttu-id="90794-124">Defecte diode</span><span class="sxs-lookup"><span data-stu-id="90794-124">Faulty diode</span></span>
- <span data-ttu-id="90794-125">Vervuilde wikkelingen</span><span class="sxs-lookup"><span data-stu-id="90794-125">Dirty windings</span></span>
- <span data-ttu-id="90794-126">Defecte generator</span><span class="sxs-lookup"><span data-stu-id="90794-126">Defective generator</span></span>
- <span data-ttu-id="90794-127">Defecte sensor</span><span class="sxs-lookup"><span data-stu-id="90794-127">Defective sensor</span></span>

## <a name="create-fault-symptoms"></a><span data-ttu-id="90794-128">Foutsymptomen maken</span><span class="sxs-lookup"><span data-stu-id="90794-128">Create fault symptoms</span></span>

<span data-ttu-id="90794-129">Voer de volgende stappen uit om een lijst met symptomen te maken die kunnen worden gebruikt in de foutontwerper.</span><span class="sxs-lookup"><span data-stu-id="90794-129">Follow these steps to create a list of symptoms that can be used in the fault designer.</span></span>

1. <span data-ttu-id="90794-130">Selecteer **Activabeheer** \> **Instellingen** \> **Fout** \> **Foutsymptomen**.</span><span class="sxs-lookup"><span data-stu-id="90794-130">Select **Asset management** \> **Setup** \> **Fault** \> **Fault symptoms**.</span></span>
2. <span data-ttu-id="90794-131">Selecteer **Nieuw** om een record te maken.</span><span class="sxs-lookup"><span data-stu-id="90794-131">Select **New** to create a record.</span></span>
3. <span data-ttu-id="90794-132">Voer in het veld **Foutsymptoom** een naam in voor het foutsymptoom.</span><span class="sxs-lookup"><span data-stu-id="90794-132">In the **Fault symptom** field, enter a name for the fault symptom.</span></span>
4. <span data-ttu-id="90794-133">Voer in het veld **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="90794-133">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="90794-134">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="90794-134">Select **Save**.</span></span>

## <a name="create-fault-areas"></a><span data-ttu-id="90794-135">Foutgebieden maken</span><span class="sxs-lookup"><span data-stu-id="90794-135">Create fault areas</span></span>

<span data-ttu-id="90794-136">Voer de volgende stappen uit om een lijst met gebieden of locaties te maken die kunnen worden gebruikt in de foutontwerper.</span><span class="sxs-lookup"><span data-stu-id="90794-136">Follow these steps to create a list of areas or locations that can be used in the fault designer.</span></span>

1. <span data-ttu-id="90794-137">Selecteer **Activabeheer** \> **Instellingen** \> **Fout** \> **Foutsymptomen**.</span><span class="sxs-lookup"><span data-stu-id="90794-137">Select **Asset management** \> **Setup** \> **Fault** \> **Fault areas**.</span></span>
2. <span data-ttu-id="90794-138">Selecteer **Nieuw** om een record te maken.</span><span class="sxs-lookup"><span data-stu-id="90794-138">Select **New** to create a record.</span></span>
3. <span data-ttu-id="90794-139">Voer in het veld **Foutsymptoom** een naam in voor het foutsymptoom.</span><span class="sxs-lookup"><span data-stu-id="90794-139">In the **Fault area** field, enter a name for the fault area.</span></span>
4. <span data-ttu-id="90794-140">Voer in het veld **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="90794-140">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="90794-141">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="90794-141">Select **Save**.</span></span>

## <a name="create-fault-types"></a><span data-ttu-id="90794-142">Foutsoorten maken</span><span class="sxs-lookup"><span data-stu-id="90794-142">Create fault types</span></span>

<span data-ttu-id="90794-143">Voer de volgende stappen uit om een lijst met foutsoorten te maken die kunnen worden gebruikt in de foutontwerper.</span><span class="sxs-lookup"><span data-stu-id="90794-143">Follow these steps to create a list of fault types that can be used in the fault designer.</span></span>

1. <span data-ttu-id="90794-144">Selecteer **Activabeheer** \> **Instellingen** \> **Fout** \> **Type fouten**.</span><span class="sxs-lookup"><span data-stu-id="90794-144">Select **Asset management** \> **Setup** \> **Fault** \> **Fault types**.</span></span>
2. <span data-ttu-id="90794-145">Selecteer **Nieuw** om een record te maken.</span><span class="sxs-lookup"><span data-stu-id="90794-145">Select **New** to create a record.</span></span>
3. <span data-ttu-id="90794-146">Voer in het veld **Type fout** een naam op voor het type fout.</span><span class="sxs-lookup"><span data-stu-id="90794-146">In the **Fault type** field, enter a name for the fault type.</span></span>
4. <span data-ttu-id="90794-147">Voer in het veld **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="90794-147">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="90794-148">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="90794-148">Select **Save**.</span></span>

## <a name="set-up-the-fault-designer"></a><span data-ttu-id="90794-149">De foutontwerper instellen</span><span class="sxs-lookup"><span data-stu-id="90794-149">Set up the fault designer</span></span>

<span data-ttu-id="90794-150">In de foutontwerper stelt u foutgegevens in voor typen activa.</span><span class="sxs-lookup"><span data-stu-id="90794-150">In the fault designer, you set up fault data on asset types.</span></span>

1. <span data-ttu-id="90794-151">Selecteer **Activabeheer** \> **Instellingen** \> **Fout** \> **Foutontwerper**.</span><span class="sxs-lookup"><span data-stu-id="90794-151">Select **Asset management** \> **Setup** \> **Fault** \> **Fault designer**.</span></span>
2. <span data-ttu-id="90794-152">Selecteer in het linkerdeelvenster het type activa waarvoor u een foutrecord wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="90794-152">In the left pane, select the type of asset to set up a fault record for.</span></span>
3. <span data-ttu-id="90794-153">Selecteer in het Sneltabblad **Foutsymptoom** de optie **regel toevoegen** en selecteer vervolgens in het veld **Foutsymptoom** een foutsymptoom.</span><span class="sxs-lookup"><span data-stu-id="90794-153">On the **Fault symptom** FastTab, select **Add line**, and then, in the **Fault symptom** field, select a fault symptom.</span></span>
4. <span data-ttu-id="90794-154">Selecteer in het Sneltabblad **Foutgebied** de optie **Regel toevoegen** en selecteer vervolgens in het veld **Foutgebied** een foutgebied.</span><span class="sxs-lookup"><span data-stu-id="90794-154">On the **Fault area** FastTab, select **Add line**, and then, in the **Fault area** field select a fault area.</span></span>
5. <span data-ttu-id="90794-155">Selecteer in het Sneltabblad **Fouttype** de optie **Regel toevoegen** en selecteer vervolgens in het veld **Fouttype** een fouttype.</span><span class="sxs-lookup"><span data-stu-id="90794-155">On the **Fault type** FastTab, select **Add line**, and then, in the **Fault type** field, select a fault type.</span></span>
6. <span data-ttu-id="90794-156">Om snel combinaties van alle bestaande foutsymptomen, -gebieden en -typen voor het geselecteerde activatype te maken, selecteert u **Foutcombinaties** maken.</span><span class="sxs-lookup"><span data-stu-id="90794-156">To quickly create combinations of all existing fault symptoms, areas, and types for the selected asset type, select **Create fault combinations**.</span></span> <span data-ttu-id="90794-157">Deze functie is handig als u veel foutsymptomen, -gebieden en -typen hebt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="90794-157">This function is useful if you've added many fault symptoms, areas, and types.</span></span> <span data-ttu-id="90794-158">Het is eenvoudiger om de regels te verwijderen voor alle combinaties die niet relevant zijn voor het type activum dan om handmatig nieuwe regels te maken.</span><span class="sxs-lookup"><span data-stu-id="90794-158">It's easier to delete the lines for any combinations that aren't relevant to the asset type than to create new lines manually.</span></span>

    > [!NOTE]
    > <span data-ttu-id="90794-159">Als u de instellingen van foutsymptomen, -gebieden en -typen van het ene type activum naar het geselecteerde type activum wilt kopiëren, selecteert u **Kopiëren vanuit activum type**.</span><span class="sxs-lookup"><span data-stu-id="90794-159">To copy the setup of fault symptoms, areas, and types from one asset type to the selected asset type, select **Copy from asset type**.</span></span>

7. <span data-ttu-id="90794-160">Klik op **Opslaan** om uw wijzigingen op te slaan.</span><span class="sxs-lookup"><span data-stu-id="90794-160">Select **Save** to save your changes.</span></span>

![Pagina Foutontwerper](media/21-setup-for-work-orders.png)

## <a name="create-fault-causes"></a><span data-ttu-id="90794-162">Foutoorzaken maken</span><span class="sxs-lookup"><span data-stu-id="90794-162">Create fault causes</span></span>

<span data-ttu-id="90794-163">Volg deze stappen om een lijst met bekende foutoorzaken te maken die kunnen worden toegevoegd aan een werkorder of een onderhoudsaanvraag.</span><span class="sxs-lookup"><span data-stu-id="90794-163">Follow these steps to create a list of known fault causes that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="90794-164">Selecteer **Activabeheer** \> **Instellingen** \> **Fout** \> **Foutoorzaken**.</span><span class="sxs-lookup"><span data-stu-id="90794-164">Select **Asset management** \> **Setup** \> **Fault** \> **Fault causes**.</span></span>
2. <span data-ttu-id="90794-165">Selecteer **Nieuw** om een record te maken.</span><span class="sxs-lookup"><span data-stu-id="90794-165">Select **New** to create a record.</span></span>
3. <span data-ttu-id="90794-166">Voer in het veld **Foutoorzaak** een naam op voor de foutoorzaak.</span><span class="sxs-lookup"><span data-stu-id="90794-166">In the **Fault cause** field, enter a name for the fault cause.</span></span>
4. <span data-ttu-id="90794-167">Voer in het veld **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="90794-167">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="90794-168">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="90794-168">Select **Save**.</span></span>

## <a name="create-fault-remedies"></a><span data-ttu-id="90794-169">Foutoplossingen maken</span><span class="sxs-lookup"><span data-stu-id="90794-169">Create fault remedies</span></span>

<span data-ttu-id="90794-170">Volg deze stappen om een lijst met suggesties voor oplossing en reparatie te maken die kunnen worden toegevoegd aan een werkorder of een onderhoudsaanvraag.</span><span class="sxs-lookup"><span data-stu-id="90794-170">Follow these steps to create a list of suggestions for remedy and repair that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="90794-171">Selecteer **Activabeheer** \> **Instellingen** \> **Fout** \> **Foutoplossing**.</span><span class="sxs-lookup"><span data-stu-id="90794-171">Select **Asset management** \> **Setup** \> **Fault** \> **Fault remedies**.</span></span>
2. <span data-ttu-id="90794-172">Selecteer **Nieuw** om een record te maken.</span><span class="sxs-lookup"><span data-stu-id="90794-172">Select **New** to create a record.</span></span>
3. <span data-ttu-id="90794-173">Voer in het veld **Foutoplossing** een naam in voor de foutoplossing.</span><span class="sxs-lookup"><span data-stu-id="90794-173">In the **Fault remedy** field, enter a name for the fault remedy.</span></span>
4. <span data-ttu-id="90794-174">Voer in het veld **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="90794-174">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="90794-175">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="90794-175">Select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="90794-176">U kunt de namen van uw foutsymptomen, -gebieden, -typen, -oorzaken en -oplossingen wijzigen als dat nodig is.</span><span class="sxs-lookup"><span data-stu-id="90794-176">You can change the names of your fault symptoms, areas, types, causes, and remedies as you require.</span></span> <span data-ttu-id="90794-177">De naamswijzigingen worden automatisch weergegeven in de gerelateerde foutregistraties.</span><span class="sxs-lookup"><span data-stu-id="90794-177">The name changes are automatically reflected in the related fault registrations.</span></span>
