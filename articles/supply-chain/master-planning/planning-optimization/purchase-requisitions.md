---
title: Opdrachten tot inkoop
description: In dit onderwerp wordt beschreven hoe opdrachten tot inkoop worden ondersteund in Planningsoptimalisatie.
author: ChristianRytt
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqPlanSched, ReqGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 564f87fe78e79107feb103f953ed4769e4734aa1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808035"
---
# <a name="purchase-requisitions"></a><span data-ttu-id="770ca-103">Opdrachten tot inkoop</span><span class="sxs-lookup"><span data-stu-id="770ca-103">Purchase requisitions</span></span>

<span data-ttu-id="770ca-104">Via de hoofdplanning kunnen goedgekeurde opdrachten tot inkoop worden aangevuld.</span><span class="sxs-lookup"><span data-stu-id="770ca-104">Master planning can replenish approved purchase requisitions.</span></span> <span data-ttu-id="770ca-105">Daarom hoeven gebruikers voor het uitvoeren van opdrachten tot inkoop geen werkstroom te gebruiken om inkooporders te maken.</span><span class="sxs-lookup"><span data-stu-id="770ca-105">Therefore, to cover purchase requisitions, users don't have to use a workflow to create purchase orders.</span></span> <span data-ttu-id="770ca-106">In plaats daarvan kunnen opdrachten tot inkoop worden uitgevoerd door de hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="770ca-106">Instead, purchase requisitions can be covered by master planning.</span></span> <span data-ttu-id="770ca-107">Dankzij deze functionaliteit kan een opdracht tot inkoop een inkooporder, een overboekingsorder of een productieorder produceren, afhankelijk van de waarde van het **Geplande ordertype** die is ingesteld voor het gerelateerde product.</span><span class="sxs-lookup"><span data-stu-id="770ca-107">Because of this functionality, a purchase requisition can produce a purchase order, a transfer order, or a production order, depending on the **Planned order type** value that is set for the related product.</span></span>

## <a name="enable-master-plans-to-include-requisitions"></a><span data-ttu-id="770ca-108">Hoofdplannen inschakelen om opdrachten tot inkoop op te nemen</span><span class="sxs-lookup"><span data-stu-id="770ca-108">Enable master plans to include requisitions</span></span>

<span data-ttu-id="770ca-109">Voer de volgende stappen uit om tijdens de behoefteplanningsberekening voor een hoofdplan opdrachten tot inkoop op te nemen.</span><span class="sxs-lookup"><span data-stu-id="770ca-109">To include requisitions during the coverage calculation for a master plan, follow these steps.</span></span>

1. <span data-ttu-id="770ca-110">Ga naar **Hoofdplanning** \> **Instellingen** \> **Plannen** \> **Hoofdplannen**.</span><span class="sxs-lookup"><span data-stu-id="770ca-110">Go to **Master planning** \> **Setup** \> **Plans** \> **Master plans**.</span></span>
1. <span data-ttu-id="770ca-111">Maak of selecteer een hoofdplan.</span><span class="sxs-lookup"><span data-stu-id="770ca-111">Create or select a master plan.</span></span>
1. <span data-ttu-id="770ca-112">Stel op het sneltabblad **Algemeen** de optie **Bestelaanvragen opnemen** in op *Ja*.</span><span class="sxs-lookup"><span data-stu-id="770ca-112">On the **General** FastTab, set the **Include requisitions** option to *Yes*.</span></span>
1. <span data-ttu-id="770ca-113">Herhaal stap 2 en 3 voor elk extra hoofdplan waarin u opdrachten tot inkoop wilt opnemen.</span><span class="sxs-lookup"><span data-stu-id="770ca-113">Repeat steps 2 and 3 for each additional master plan where you want to include requisitions.</span></span>

## <a name="approved-requisitions-time-fence"></a><span data-ttu-id="770ca-114">Time fence goedgekeurde bestelaanvragen</span><span class="sxs-lookup"><span data-stu-id="770ca-114">Approved requisitions time fence</span></span>

<span data-ttu-id="770ca-115">Met de *time fence goedgekeurde bestelaanvragen* legt u vast hoe ver terug (in dagen) een hoofdplan de vraag omvat van goedgekeurde bestelaanvragen voor aanvulling.</span><span class="sxs-lookup"><span data-stu-id="770ca-115">The *approved requisitions time fence* establishes how far back (in days) a master plan will include demand from approved replenishment requisitions.</span></span> <span data-ttu-id="770ca-116">U kunt een time fence voor goedgekeurde bestelaanvragen instellen op zowel het niveau van de behoefteplanningsgroep als het niveau van het hoofdplan.</span><span class="sxs-lookup"><span data-stu-id="770ca-116">You can set an approved requisitions time fence at both the coverage group level and the master plan level.</span></span>

### <a name="set-the-approved-requisitions-time-fence-for-a-coverage-group"></a><span data-ttu-id="770ca-117">De time fence voor goedgekeurde bestelaanvragen voor een behoefteplanningsgroep instellen</span><span class="sxs-lookup"><span data-stu-id="770ca-117">Set the approved requisitions time fence for a coverage group</span></span>

1. <span data-ttu-id="770ca-118">Ga naar **Hoofdplanning** \> **Instellen** \> **Behoefteplanning** \> **Behoefteplanningsgroepen**.</span><span class="sxs-lookup"><span data-stu-id="770ca-118">Go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage groups**.</span></span>
1. <span data-ttu-id="770ca-119">Maak of selecteer een behoefteplanningsgroep.</span><span class="sxs-lookup"><span data-stu-id="770ca-119">Create or select a coverage group.</span></span>
1. <span data-ttu-id="770ca-120">Stel in het veld **Time fence goedgekeurde bestelaanvragen (dagen)** op het sneltabblad **Overig** het aantal dagen in dat in de time fence moet worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="770ca-120">On the **Other** FastTab, set the **Approved requisitions time fence (days)** field to the number of days to include in the time fence.</span></span>
1. <span data-ttu-id="770ca-121">Herhaal stap 2 en 3 voor elke aanvullende behoefteplanningsgroep waarin u een time fence voor goedgekeurde bestelaanvragen wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="770ca-121">Repeat steps 2 and 3 for each additional coverage group where you want to set an approved requisitions time fence.</span></span>

### <a name="set-the-approved-requisitions-time-fence-for-individual-master-plans"></a><span data-ttu-id="770ca-122">De time fence voor goedgekeurde bestelaanvragen voor afzonderlijke hoofdplannen instellen</span><span class="sxs-lookup"><span data-stu-id="770ca-122">Set the approved requisitions time fence for individual master plans</span></span>

<span data-ttu-id="770ca-123">Wanneer u een time fence voor goedgekeurde bestelaanvragen wilt instellen voor een afzonderlijk hoofdplan, wordt daarmee de instelling van de time fence voor elke toepasselijke behoefteplanningsgroep overschreven.</span><span class="sxs-lookup"><span data-stu-id="770ca-123">When you set an approved requisitions time fence for an individual master plan, the setting overrides the time fence setting for any applicable coverage group.</span></span>

1. <span data-ttu-id="770ca-124">Ga naar **Hoofdplanning** \> **Instellingen** \> **Plannen** \> **Hoofdplannen**.</span><span class="sxs-lookup"><span data-stu-id="770ca-124">Go to **Master planning** \> **Setup** \> **Plans** \> **Master plans**.</span></span>
1. <span data-ttu-id="770ca-125">Maak of selecteer een hoofdplan.</span><span class="sxs-lookup"><span data-stu-id="770ca-125">Create or select a master plan.</span></span>
1. <span data-ttu-id="770ca-126">Stel in het veld **Time fence goedgekeurde bestelaanvragen (dagen)** op het sneltabblad **Time fences in dagen** het aantal dagen in dat in de time fence moet worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="770ca-126">On the **TIme fences in days** FastTab, set the **Approved requisitions time fence (days)** field to the number of days to include in the time fence.</span></span>
1. <span data-ttu-id="770ca-127">Herhaal stap 2 en 3 voor elk aanvullend hoofdplan waarin u een time fence voor goedgekeurde bestelaanvragen wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="770ca-127">Repeat steps 2 and 3 for each additional master plan where you want to set an approved requisitions time fence.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="770ca-128">**Binnenkort:** times fences voor goedgekeurde bestelaanvragen worden nog niet ondersteund voor Planningsoptimalisatie.</span><span class="sxs-lookup"><span data-stu-id="770ca-128">**Coming soon:** Approved requisitions time fences aren't yet supported for Planning Optimization.</span></span> <span data-ttu-id="770ca-129">Tot die tijd worden alle waarden die u invoert in het veld **Time fence goedgekeurde bestelaanvragen (dagen)** genegeerd.</span><span class="sxs-lookup"><span data-stu-id="770ca-129">Until they are supported, all values that you enter in the **Approved requisitions time fence (days)** field will be ignored.</span></span>

## <a name="independent-supply-regardless-of-coverage-code"></a><span data-ttu-id="770ca-130">Onafhankelijke levering, ongeacht behoefteplanningscode</span><span class="sxs-lookup"><span data-stu-id="770ca-130">Independent supply, regardless of coverage code</span></span>

<span data-ttu-id="770ca-131">Opdrachten tot inkoop worden altijd gedekt door onafhankelijke geplande orders, ongeacht de behoefteplanningscode.</span><span class="sxs-lookup"><span data-stu-id="770ca-131">Purchase requisitions are always covered by independent planned orders, regardless of the coverage code.</span></span> <span data-ttu-id="770ca-132">Dit gedrag zorgt voor duidelijke traceerbaarheid en werkstromen tussen opdrachten tot inkoop en aanvullingsorders.</span><span class="sxs-lookup"><span data-stu-id="770ca-132">This behavior ensures clear traceability and workflows between purchase requisitions and replenishment orders.</span></span>

### <a name="example-1"></a><span data-ttu-id="770ca-133">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="770ca-133">Example 1</span></span>

<span data-ttu-id="770ca-134">Een product is zo ingesteld dat het een waarde voor **Behoefteplanningscode** van *Min/max* heeft. Het heeft de volgende statuswaarden voor voorraad en aanvraag:</span><span class="sxs-lookup"><span data-stu-id="770ca-134">A product is set up so that it has a **Coverage code** value of *Min/max*. It has the following inventory and requisition statuses:</span></span>

- <span data-ttu-id="770ca-135">Hoeveelheid voorhanden voorraad = 10.</span><span class="sxs-lookup"><span data-stu-id="770ca-135">Inventory on-hand quantity = 10.</span></span>
- <span data-ttu-id="770ca-136">Minimale voorraadhoeveelheid = 15.</span><span class="sxs-lookup"><span data-stu-id="770ca-136">Minimum inventory quantity = 15.</span></span>
- <span data-ttu-id="770ca-137">Maximale voorraadhoeveelheid = 20.</span><span class="sxs-lookup"><span data-stu-id="770ca-137">Maximum inventory quantity = 20.</span></span>
- <span data-ttu-id="770ca-138">Er bestaat een opdracht tot inkoop voor één stuk.</span><span class="sxs-lookup"><span data-stu-id="770ca-138">A purchase requisition for one piece exists.</span></span> <span data-ttu-id="770ca-139">De aangevraagde datum is vandaag.</span><span class="sxs-lookup"><span data-stu-id="770ca-139">It has a requested date of today.</span></span>

<span data-ttu-id="770ca-140">Bij het uitvoeren van de hoofdplanning worden twee geplande orders gemaakt: een voor 10 stuks om de voorraad aan te vullen tot de maximumhoeveelheid en een voor één stuk om de opdracht tot inkoop aan te vullen.</span><span class="sxs-lookup"><span data-stu-id="770ca-140">When master planning runs, two planned orders are created: one for 10 pieces to replenish inventory to the maximum quantity, and one for one piece to replenish the purchase requisition.</span></span>

### <a name="example-2"></a><span data-ttu-id="770ca-141">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="770ca-141">Example 2</span></span>

<span data-ttu-id="770ca-142">Een product is zo ingesteld dat het een waarde voor **Behoefteplanningscode** van *Min/max* heeft. Het heeft de volgende statuswaarden voor voorraad en aanvraag:</span><span class="sxs-lookup"><span data-stu-id="770ca-142">A product is set up so that it has a **Coverage code** value of *Min/max*. It has the following inventory and requisition statuses:</span></span>

- <span data-ttu-id="770ca-143">Hoeveelheid voorhanden voorraad = 17.</span><span class="sxs-lookup"><span data-stu-id="770ca-143">Inventory on-hand quantity = 17.</span></span>
- <span data-ttu-id="770ca-144">Minimale voorraadhoeveelheid = 15.</span><span class="sxs-lookup"><span data-stu-id="770ca-144">Minimum inventory quantity = 15.</span></span>
- <span data-ttu-id="770ca-145">Maximale voorraadhoeveelheid = 20.</span><span class="sxs-lookup"><span data-stu-id="770ca-145">Maximum inventory quantity = 20.</span></span>
- <span data-ttu-id="770ca-146">Er bestaat een opdracht tot inkoop voor één stuk.</span><span class="sxs-lookup"><span data-stu-id="770ca-146">A purchase requisition for one piece exists.</span></span> <span data-ttu-id="770ca-147">De aangevraagde datum is vandaag.</span><span class="sxs-lookup"><span data-stu-id="770ca-147">It has a requested date of today.</span></span>

<span data-ttu-id="770ca-148">Wanneer de hoofdplanning wordt uitgevoerd, wordt één geplande order voor één stuk gemaakt om de opdracht tot inkoop aan te vullen.</span><span class="sxs-lookup"><span data-stu-id="770ca-148">When master planning runs, one planned order for one piece is created to replenish the purchase requisition.</span></span>

### <a name="example-3"></a><span data-ttu-id="770ca-149">Voorbeeld 3</span><span class="sxs-lookup"><span data-stu-id="770ca-149">Example 3</span></span>

<span data-ttu-id="770ca-150">Een product is zo ingesteld dat het een waarde voor **Behoefteplanningscode** van *Periode* heeft en een periodelengte van zeven dagen.</span><span class="sxs-lookup"><span data-stu-id="770ca-150">A product is set up so that it has a **Coverage code** value of *Period* and a period length of seven days.</span></span> <span data-ttu-id="770ca-151">Het heeft de volgende statuswaarden voor voorraad, verkooporder en bestelaanvraag:</span><span class="sxs-lookup"><span data-stu-id="770ca-151">It has the following inventory, sales order, and requisition statuses:</span></span>

- <span data-ttu-id="770ca-152">Hoeveelheid voorhanden voorraad = 0.</span><span class="sxs-lookup"><span data-stu-id="770ca-152">Inventory on-hand quantity = 0.</span></span>
- <span data-ttu-id="770ca-153">Er bestaat een verkooporder voor vijf stuks.</span><span class="sxs-lookup"><span data-stu-id="770ca-153">A sales order for five pieces exists.</span></span> <span data-ttu-id="770ca-154">De verwachte verzenddatum is vandaag plus één dag.</span><span class="sxs-lookup"><span data-stu-id="770ca-154">It has an expected ship date of today plus one day.</span></span>
- <span data-ttu-id="770ca-155">Er bestaat een opdracht tot inkoop voor drie stuks.</span><span class="sxs-lookup"><span data-stu-id="770ca-155">A purchase requisition for three pieces exists.</span></span> <span data-ttu-id="770ca-156">De aangevraagde datum is vandaag plus drie dagen.</span><span class="sxs-lookup"><span data-stu-id="770ca-156">It has a requested date of today plus three days.</span></span>

<span data-ttu-id="770ca-157">Bij het uitvoeren van de hoofdplanning worden twee geplande orders gemaakt: een voor drie stuks om de opdracht tot in koop aan te vullen en een voor vijf stuks om de verkoopordervraag aan te vullen.</span><span class="sxs-lookup"><span data-stu-id="770ca-157">When master planning runs, two planned orders are created: one for three pieces to replenish the purchase requisition and one for five pieces to replenish sales order demand.</span></span>

> [!NOTE]
> <span data-ttu-id="770ca-158">Nadat een geplande order die is vastgelegd voor een opdracht tot inkoop is gefiatteerd, bewaart de planningsengine de behoeftetracering voor de opdracht tot inkoop.</span><span class="sxs-lookup"><span data-stu-id="770ca-158">After a planned order that is pegged to a purchase requisition is firmed, the planning engine keeps the pegging to the purchase requisition.</span></span> <span data-ttu-id="770ca-159">Als later wordt geconstateerd dat in de gefiatteerde order een bepaalde hoeveelheid ontbreekt die nodig is om aan de opdracht tot inkoop te voldoen, wordt een nieuwe geplande order gemaakt voor het verschil.</span><span class="sxs-lookup"><span data-stu-id="770ca-159">If the firmed order is later found to be missing some quantity that is required to fulfill the purchase requisition, the system will create a new planned order for the difference.</span></span>

<span data-ttu-id="770ca-160">Zie [Overzicht van opdrachten tot inkoop](../../procurement/purchase-requisitions-overview.md) voor meer informatie over opdrachten tot inkoop.</span><span class="sxs-lookup"><span data-stu-id="770ca-160">For more information about purchase requisitions, see [Purchase requisition overview](../../procurement/purchase-requisitions-overview.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]