---
title: Reparatiebeheer
description: U kunt problemen systematisch groeperen, zodat oplossingen worden voorgesteld die bij eerdere problemen hebben gewerkt.
author: ShylaThompson
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAConditionTable, SMASymptomArea, SMADiagnosisArea, SMAResolutionTable, SMARepairStage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 32202344f77352cd3f9c1a807d14192a9bf0d9e6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "349280"
---
# <a name="repair-management"></a><span data-ttu-id="6523c-103">Reparatiebeheer</span><span class="sxs-lookup"><span data-stu-id="6523c-103">Repair management</span></span>       

[!include [banner](../includes/banner.md)]


<span data-ttu-id="6523c-104">Bij reparatiebeheer kunt u problemen systematisch groeperen.</span><span class="sxs-lookup"><span data-stu-id="6523c-104">For repair management you can group problems systematically.</span></span> <span data-ttu-id="6523c-105">Hierdoor worden oplossingen voorgesteld die bij eerdere problemen hebben gewerkt.</span><span class="sxs-lookup"><span data-stu-id="6523c-105">This is to help with the suggestion of solutions that have been successful in the past.</span></span>

<span data-ttu-id="6523c-106">U geeft instellingen voor de symptomen, diagnose en oplossing op.</span><span class="sxs-lookup"><span data-stu-id="6523c-106">You set up symptoms, diagnosis, and resolution settings.</span></span> <span data-ttu-id="6523c-107">Deze instellingen kunnen later worden toegepast wanneer u een vergelijkbaar artikel ontvangt voor reparatie.</span><span class="sxs-lookup"><span data-stu-id="6523c-107">All these can later be applied when you receive a similar item for repair.</span></span> <span data-ttu-id="6523c-108">U kunt ook reparatiefasen instellen, zodat u de voortgang van een reparatie kunt volgen.</span><span class="sxs-lookup"><span data-stu-id="6523c-108">You can also set up repair stages that can follow the progress of a repair issue.</span></span>

## <a name="setting-up-repair-management"></a><span data-ttu-id="6523c-109">Reparatiebeheer instellen</span><span class="sxs-lookup"><span data-stu-id="6523c-109">Setting up repair management</span></span>

<span data-ttu-id="6523c-110">Met de volgende instellingsformulieren kunt u gegevens invoeren waarmee de symptomen, diagnose en oplossing voor de reparatie worden ingesteld.</span><span class="sxs-lookup"><span data-stu-id="6523c-110">Use the following setup forms to enter information that will be used to specify the symptoms, the diagnosis, and the resolution, of the repair.</span></span>

1.  <span data-ttu-id="6523c-111">Klik op **Servicebeheer** \> **Instellen** \> **Repareren** \> **Voorwaarden**.</span><span class="sxs-lookup"><span data-stu-id="6523c-111">Click **Service management** \> **Setup** \> **Repair** \> **Conditions**.</span></span>

2.  <span data-ttu-id="6523c-112">Klik op **Servicebeheer** \> **Instellen** \> **Repareren** \> **Symptoomgebieden**.</span><span class="sxs-lookup"><span data-stu-id="6523c-112">Click **Service management** \> **Setup** \> **Repair** \> **Symptom areas**.</span></span>

3.  <span data-ttu-id="6523c-113">Klik op **Servicebeheer** \> **Instellen** \> **Repareren** \> **Diagnosegebieden**.</span><span class="sxs-lookup"><span data-stu-id="6523c-113">Click **Service management** \> **Setup** \> **Repair** \> **Diagnosis areas**.</span></span>

4.  <span data-ttu-id="6523c-114">Klik op **Servicebeheer** \> **Instellen** \> **Repareren** \> **Oplossingen**.</span><span class="sxs-lookup"><span data-stu-id="6523c-114">Click **Service management** \> **Setup** \> **Repair** \> **Resolutions**.</span></span>

5.  <span data-ttu-id="6523c-115">Klik op **Servicebeheer** \> **Instellen** \> **Repareren** \> **Reparatiefasen**.</span><span class="sxs-lookup"><span data-stu-id="6523c-115">Click **Service management** \> **Setup** \> **Repair** \> **Repair stages**.</span></span>

## <a name="symptoms-and-conditions"></a><span data-ttu-id="6523c-116">Symptomen en voorwaarden</span><span class="sxs-lookup"><span data-stu-id="6523c-116">Symptoms and conditions</span></span>

<span data-ttu-id="6523c-117">Symptomen zijn de manier waarop de klant het probleem beschrijft.</span><span class="sxs-lookup"><span data-stu-id="6523c-117">Symptoms are how the customer characterizes the problem.</span></span> <span data-ttu-id="6523c-118">Symptomen omvatten de opmerkingen van de klant waarmee wordt aangegeven dat het artikel moet worden gerepareerd.</span><span class="sxs-lookup"><span data-stu-id="6523c-118">Symptoms include the customer observations that indicate the need for repair.</span></span>

<span data-ttu-id="6523c-119">U kunt symptoomgebieden, symptoomcodes en voorwaarden instellen.</span><span class="sxs-lookup"><span data-stu-id="6523c-119">You can set up symptom areas, symptom codes, and conditions.</span></span> <span data-ttu-id="6523c-120">Het symptoomgebied geeft het gebied van het defect aan en met de symptoomcode wordt het defectsymptoom aangeduid.</span><span class="sxs-lookup"><span data-stu-id="6523c-120">The symptom area covers the area of malfunction, and the symptom code covers the malfunction symptom.</span></span> <span data-ttu-id="6523c-121">De voorwaarde geeft de situatie of de omgeving aan die aanwezig is wanneer het probleem optreedt.</span><span class="sxs-lookup"><span data-stu-id="6523c-121">The condition describes the situation or environment that is present when the problem occurs.</span></span>

<span data-ttu-id="6523c-122">**Voorbeeld**</span><span class="sxs-lookup"><span data-stu-id="6523c-122">**Example**</span></span>

<span data-ttu-id="6523c-123">Een computer wordt teruggebracht voor reparatie omdat de vaste schijf telkens vastloopt na langdurig gebruik.</span><span class="sxs-lookup"><span data-stu-id="6523c-123">A computer is brought in for repair because the hard drive fails after an extended period of use.</span></span> <span data-ttu-id="6523c-124">Als de vaste schijf vastloopt, verschijnt er een blauw scherm.</span><span class="sxs-lookup"><span data-stu-id="6523c-124">The hard drive failure causes a blue screen error.</span></span> <span data-ttu-id="6523c-125">De technisch medewerker die de computer ontvangt, voert de volgende symptomen en voorwaarden in:</span><span class="sxs-lookup"><span data-stu-id="6523c-125">The technician who receives the computer enters the following symptoms and conditions:</span></span>

1.  <span data-ttu-id="6523c-126">Het symptoomgebied is de vaste schijf</span><span class="sxs-lookup"><span data-stu-id="6523c-126">The symptom area is the hard drive</span></span>

2.  <span data-ttu-id="6523c-127">De symptoomcode is de fout met het blauwe scherm</span><span class="sxs-lookup"><span data-stu-id="6523c-127">The symptom code is the blue screen error</span></span>

3.  <span data-ttu-id="6523c-128">De voorwaarde is dat de vaste schijf vastloop na langdurig gebruik</span><span class="sxs-lookup"><span data-stu-id="6523c-128">The condition is that the hard drive fails after extended use</span></span>

## <a name="diagnosis-and-resolutions"></a><span data-ttu-id="6523c-129">Diagnose en oplossingen</span><span class="sxs-lookup"><span data-stu-id="6523c-129">Diagnosis and resolutions</span></span>

<span data-ttu-id="6523c-130">De diagnose- en oplossingsvelden zijn verklaringen vanuit reparatieperspectief.</span><span class="sxs-lookup"><span data-stu-id="6523c-130">The diagnosis and resolution fields are statements from the repair perspective.</span></span> <span data-ttu-id="6523c-131">Dit zijn de stappen die zijn uitgevoerd door een technische werknemer om het probleem te onderzoeken.</span><span class="sxs-lookup"><span data-stu-id="6523c-131">These are the steps that a technician went through to investigate the problem.</span></span>

<span data-ttu-id="6523c-132">Het diagnosegebied bestaat uit de bewerking die moet worden uitgevoerd om het probleem op te lossen.</span><span class="sxs-lookup"><span data-stu-id="6523c-132">The diagnosis area covers the operation that must occur to solve the issue.</span></span> <span data-ttu-id="6523c-133">Met de diagnosecode wordt aangegeven hoe het probleem is afgehandeld en de oplossing kan zijn dat het artikel is gerepareerd, vervangen of dat de order is geannuleerd door de klant.</span><span class="sxs-lookup"><span data-stu-id="6523c-133">The diagnosis code is how the problem was handled, and the resolution could be that the item was repaired, replaced, or the order was canceled by the customer.</span></span> <span data-ttu-id="6523c-134">Als de computer bijvoorbeeld is gerepareerd, kan het diagnosegebied 'defect onderdeel' zijn, de diagnosecode 'nieuwe videokaart geïnstalleerd' en de oplossing 'vervangen'.</span><span class="sxs-lookup"><span data-stu-id="6523c-134">For example, if the computer is repaired, the diagnosis area could be "defective part," the diagnosis code could be "new video card installed," and the resolution could be "replaced."</span></span>

## <a name="repair-stages"></a><span data-ttu-id="6523c-135">Reparatiefasen</span><span class="sxs-lookup"><span data-stu-id="6523c-135">Repair stages</span></span>

<span data-ttu-id="6523c-136">Met reparatiefasen wordt de voortgang van het reparatieproces aangegeven.</span><span class="sxs-lookup"><span data-stu-id="6523c-136">Repair stages state the progress of the repair process.</span></span> <span data-ttu-id="6523c-137">De reparatiefase heeft de afmeldingsparameter **Voltooid**, waarmee wordt aangegeven dat de reparatieregel is voltooid en de voltooiingsdatum en -tijd zijn vastgelegd.</span><span class="sxs-lookup"><span data-stu-id="6523c-137">The repair stage has a **Finished** sign-off parameter that indicates that the repair line has been completed, and the finishing date and time has been recorded.</span></span>

## <a name="applying-repair-management"></a><span data-ttu-id="6523c-138">Reparatiebeheer toepassen</span><span class="sxs-lookup"><span data-stu-id="6523c-138">Applying repair management</span></span>

<span data-ttu-id="6523c-139">Als u reparatiebeheer wilt toepassen op een artikel, moet het artikel op een serviceorder worden ingesteld met een serviceobjectrelatie.</span><span class="sxs-lookup"><span data-stu-id="6523c-139">To apply repair management to an item, the item must be set up with a service object relation on a service order.</span></span> <span data-ttu-id="6523c-140">Via de serviceorder kunt u vervolgens een reparatieregel maken met informatie over het huidige probleem.</span><span class="sxs-lookup"><span data-stu-id="6523c-140">From the service order you can then create a repair line with information about the current issue.</span></span> <span data-ttu-id="6523c-141">Op de reparatieregel definieert u het serviceobject dat moet worden gerepareerd en informatie over symptomen, de diagnose en uitvoering.</span><span class="sxs-lookup"><span data-stu-id="6523c-141">On the repair line you define the service object that is in repair and information about symptoms, diagnosis, and execution.</span></span> <span data-ttu-id="6523c-142">U kunt ook een notitie maken voor de reparatieregel.</span><span class="sxs-lookup"><span data-stu-id="6523c-142">You can also create a note for the repair line.</span></span>

<span data-ttu-id="6523c-143">U kunt voor elke stap in het reparatieproces reparatieregels maken.</span><span class="sxs-lookup"><span data-stu-id="6523c-143">You can create repair lines for each step in the repair process.</span></span>

## <a name="create-a-repair-line-on-a-service-order"></a><span data-ttu-id="6523c-144">Een reparatieregel maken in een serviceorder</span><span class="sxs-lookup"><span data-stu-id="6523c-144">Create a repair line on a service order</span></span>

1.  <span data-ttu-id="6523c-145">Klik op **Servicebeheer** \> **Algemeen** \> **Serviceorders** \> **Serviceorders**.</span><span class="sxs-lookup"><span data-stu-id="6523c-145">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="6523c-146">Selecteer de serviceorder met het serviceobject dat moet worden gerepareerd.</span><span class="sxs-lookup"><span data-stu-id="6523c-146">Select the service order with the service object that needs repair.</span></span>

3.  <span data-ttu-id="6523c-147">Klik op **Repareren** \> **Reparatieregels** om het formulier **Reparatieregels** te openen.</span><span class="sxs-lookup"><span data-stu-id="6523c-147">Click **Repair** \> **Repair lines** to open the **Repair lines** form.</span></span>

4.  <span data-ttu-id="6523c-148">Druk op Ctrl+N om een nieuwe regel te definiëren.</span><span class="sxs-lookup"><span data-stu-id="6523c-148">Press CTRL+N to create a new line.</span></span>

5.  <span data-ttu-id="6523c-149">Selecteer een serviceobject.</span><span class="sxs-lookup"><span data-stu-id="6523c-149">Select a service object.</span></span> <span data-ttu-id="6523c-150">U kunt elk serviceobject selecteren dat op de serviceorder is ingesteld met een objectrelatie.</span><span class="sxs-lookup"><span data-stu-id="6523c-150">You can select any service object that has been set up with an object relation on the service order.</span></span>

6.  <span data-ttu-id="6523c-151">Selecteer op de reparatieregel de vooraf ingestelde waarden voor de symptomen, diagnose en uitvoering die relevant zijn en klik zo nodig op het tabblad **Opmerking** om een notitie te maken voor de reparatieregel.</span><span class="sxs-lookup"><span data-stu-id="6523c-151">Select any of the preset symptoms, diagnosis, and execution values that are relevant in the repair line and then click the **Note** tab to create a note on the repair line, if needed.</span></span>

7.  <span data-ttu-id="6523c-152">Druk op CTRL+S om de nieuwe reparatieregel op te slaan.</span><span class="sxs-lookup"><span data-stu-id="6523c-152">Press CTRL+S to save the new repair line.</span></span> <span data-ttu-id="6523c-153">Het veld **Aanmaakdatum en -tijd** op het tabblad **Algemeen** van het formulier **Reparatieregels** wordt bijgewerkt met het tijdstip waarop de regel is opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="6523c-153">The **Created date and time** field in the **General** tab of the **Repair lines** form is updated with the time of saving.</span></span>

## <a name="tracking-progress-and-resolving-a-repair-issue"></a><span data-ttu-id="6523c-154">De voortgang bijhouden en een reparatieprobleem oplossen</span><span class="sxs-lookup"><span data-stu-id="6523c-154">Tracking progress and resolving a repair issue</span></span>

<span data-ttu-id="6523c-155">U kunt de reparatiefasen van een reparatieregel zo instellen dat de voortgang van de reparatie wordt bijgehouden.</span><span class="sxs-lookup"><span data-stu-id="6523c-155">You can set the repair stages of a repair line to track the progress of the repair.</span></span>

<span data-ttu-id="6523c-156">Als een reparatieprobleem is opgelost, kunt u de reparatieregel afsluiten.</span><span class="sxs-lookup"><span data-stu-id="6523c-156">When a repair issue is resolved, you can close the repair line.</span></span> <span data-ttu-id="6523c-157">Stel de reparatiefase in op een fase waarvoor de eigenschap **Voltooid** is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="6523c-157">Set the repair stage to a stage with a **Finished** property enabled.</span></span> <span data-ttu-id="6523c-158">De huidige datum en tijd worden op de regel vastgelegd als de voltooiingstijd.</span><span class="sxs-lookup"><span data-stu-id="6523c-158">The current date and time is registered as the finish time on the line.</span></span>

## <a name="close-a-repair-line-for-a-resolved-issue"></a><span data-ttu-id="6523c-159">Een reparatieregel voor een opgelost probleem afsluiten</span><span class="sxs-lookup"><span data-stu-id="6523c-159">Close a repair line for a resolved issue</span></span>

1.  <span data-ttu-id="6523c-160">Open het formulier **Reparatieregels**.</span><span class="sxs-lookup"><span data-stu-id="6523c-160">Open the **Repair lines** form.</span></span> <span data-ttu-id="6523c-161">Volg de procedure voor het maken van een reparatieregel die eerder in dit onderwerp is beschreven.</span><span class="sxs-lookup"><span data-stu-id="6523c-161">Follow the procedure earlier in this topic to create a repair line.</span></span>

2.  <span data-ttu-id="6523c-162">Selecteer de reparatieregel met de reparatie die u wilt afsluiten.</span><span class="sxs-lookup"><span data-stu-id="6523c-162">Select the repair line with the repair issue that you want to close.</span></span>

3.  <span data-ttu-id="6523c-163">Selecteer in het veld **Reparatiefase** een fase waarvoor de eigenschap **Voltooid** is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="6523c-163">In the **Repair stage** field, select a stage with the **Finished** property enabled.</span></span>

  


