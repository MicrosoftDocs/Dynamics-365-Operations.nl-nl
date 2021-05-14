---
title: Typen problemen voor niet-conformeringen
description: In dit onderwerp wordt beschreven hoe u probleemtypen voor niet-conformeringen maakt en gebruikt.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventProblemType, InventProblemTypeSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df509365f5c900898921acfbda380b5e20c7a251
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956614"
---
# <a name="problem-types-for-nonconformances"></a><span data-ttu-id="266c4-103">Typen problemen voor niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="266c4-103">Problem types for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="266c4-104">In dit onderwerp wordt beschreven hoe u probleemtypen voor niet-conformeringen maakt en gebruikt.</span><span class="sxs-lookup"><span data-stu-id="266c4-104">This topic describes how to create and use problem types for nonconformances.</span></span>

<span data-ttu-id="266c4-105">U kunt de pagina **Probleemtypen** gebruiken om een classificatie te definiëren van de kwaliteitsproblemen die zich kunnen voordoen voor de verschillende typen niet-conformeringen.</span><span class="sxs-lookup"><span data-stu-id="266c4-105">You use the **Problem types** page to define a classification of the quality problems that might occur for the various nonconformance types.</span></span> <span data-ttu-id="266c4-106">Voor elk probleemtype dat u maakt, moet u de typen van niet-conformeringen opgeven waarmee het probleemtype kan worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="266c4-106">For each problem type that you create, you must specify the types of nonconformances that the problem type can be used with.</span></span> <span data-ttu-id="266c4-107">U kunt de volgende typen niet-conformeringen instellen:</span><span class="sxs-lookup"><span data-stu-id="266c4-107">You can set up the following nonconformance types:</span></span>

- <span data-ttu-id="266c4-108">**Intern**: niet-conformeringen van dit type zijn gerelateerd aan voorhanden voorraad (bijvoorbeeld kwaliteitsorders of quarantaineorders).</span><span class="sxs-lookup"><span data-stu-id="266c4-108">**Internal** – Nonconformances of this type are related to on-hand inventory (for example, quality orders or quarantine orders).</span></span>
- <span data-ttu-id="266c4-109">**Klant**: niet-conformeringen van dit type zijn gerelateerd aan verkooporders.</span><span class="sxs-lookup"><span data-stu-id="266c4-109">**Customer** – Nonconformances of this type are related to sales orders.</span></span>
- <span data-ttu-id="266c4-110">**Leverancier**: niet-conformeringen van dit type zijn gerelateerd aan inkooporders.</span><span class="sxs-lookup"><span data-stu-id="266c4-110">**Vendor** – Nonconformances of this type are related to purchase orders.</span></span>
- <span data-ttu-id="266c4-111">**Serviceaanvraag**: niet-conformeringen van dit type zijn gerelateerd aan serviceorders.</span><span class="sxs-lookup"><span data-stu-id="266c4-111">**Service request** – Nonconformances of this type are related to service orders.</span></span>
- <span data-ttu-id="266c4-112">**Productie**: niet-conformeringen van dit type zijn gerelateerd aan batchorders of productieorders.</span><span class="sxs-lookup"><span data-stu-id="266c4-112">**Production** – Nonconformances of this type are related to batch orders or production orders.</span></span>
- <span data-ttu-id="266c4-113">**Productie van coproducten**: niet-conformeringen van dit type zijn gerelateerd aan batchorders voor coproducten.</span><span class="sxs-lookup"><span data-stu-id="266c4-113">**Co-product production** – Nonconformances of this type are related to batch orders for co-products.</span></span>

<span data-ttu-id="266c4-114">Wanneer u een nieuw probleemtype maakt, selecteert u **Niet-conformeringstypen** in het actievenster om een lijst te maken met een of meer niet-conformeringstypen die zijn geautoriseerd voor het probleemtype.</span><span class="sxs-lookup"><span data-stu-id="266c4-114">When you create a new problem type, select **Non conformance types** on the Action Pane to create a list of one or more nonconformance types that are authorized for the problem type.</span></span> <span data-ttu-id="266c4-115">Het probleemtype bijvoorbeeld dat is gerelateerd aan een defectcode, kan mogelijk van toepassing zijn op alle niet-conformeringstypen.</span><span class="sxs-lookup"><span data-stu-id="266c4-115">For example, a problem type that is related to a defect code might apply to all nonconformance types.</span></span> <span data-ttu-id="266c4-116">Een probleemtype dat gerelateerd is aan klachten van klanten, kan echter alleen van toepassing zijn op de niet-conformeringstypen **Klanten** en **Serviceverzoeken**.</span><span class="sxs-lookup"><span data-stu-id="266c4-116">However, a problem type that is related to customer complaints might apply only to the **Customer** and **Service request** nonconformance types.</span></span>

## <a name="examples-of-problem-types"></a><span data-ttu-id="266c4-117">Voorbeelden van probleemtypen</span><span class="sxs-lookup"><span data-stu-id="266c4-117">Examples of problem types</span></span>

<span data-ttu-id="266c4-118">Hieronder vindt u enkele voorbeelden van scenario's voor probleemtypen die kunnen worden gebruikt met de verschillende niet-conformeringstypen:</span><span class="sxs-lookup"><span data-stu-id="266c4-118">Here are some examples of scenarios for problem types that can be used with the different nonconformance types:</span></span>

- <span data-ttu-id="266c4-119">**Klant**: een klant heeft een klacht ingediend, een klant heeft iets geretourneerd of er is niet voldaan aan de kwaliteitsspecificaties.</span><span class="sxs-lookup"><span data-stu-id="266c4-119">**Customer:** A customer filed a complaint, a customer made a return, or quality specifications weren't met.</span></span>
- <span data-ttu-id="266c4-120">**Leverancier:** het product is beschadigd, er is niet voldaan aan de kwaliteitsspecificaties of het verkeerde product is ontvangen.</span><span class="sxs-lookup"><span data-stu-id="266c4-120">**Vendor:** The product was damaged, quality specifications weren't met, or the wrong product was received.</span></span>
- <span data-ttu-id="266c4-121">**Serviceaanvraag**: er is niet voldaan aan de kwaliteitsspecificaties, een klant heeft een klacht ingediend of er is machineonderhoud vereist.</span><span class="sxs-lookup"><span data-stu-id="266c4-121">**Service request:** Quality specifications weren't met, a customer filed a complaint, or machine maintenance is required.</span></span>
- <span data-ttu-id="266c4-122">**Productie**: er is niet voldaan aan de kwaliteitsspecificaties, er is machineonderhoud vereist of het product is beschadigd geraakt.</span><span class="sxs-lookup"><span data-stu-id="266c4-122">**Production:** Quality specifications weren't met, machine maintenance is required, or the product was damaged.</span></span>
- <span data-ttu-id="266c4-123">**Productie van coproducten**: er is niet voldaan aan de kwaliteitsspecificaties, er is machineonderhoud vereist of het product is beschadigd geraakt.</span><span class="sxs-lookup"><span data-stu-id="266c4-123">**Co-product production:** Quality specifications weren't met, machine maintenance is required, or the product was damaged.</span></span>

## <a name="create-a-problem-type-and-assign-it-to-nonconformance-types"></a><span data-ttu-id="266c4-124">Een probleemtype maken en dit toewijzen aan niet-conformeringstypen</span><span class="sxs-lookup"><span data-stu-id="266c4-124">Create a problem type and assign it to nonconformance types</span></span>

1. <span data-ttu-id="266c4-125">Ga naar **Voorraadbeheer \> Instellen \> Kwaliteitsbeheer \> Probleemtypen**.</span><span class="sxs-lookup"><span data-stu-id="266c4-125">Go to **Inventory management \> Setup \> Quality management \> Problem types**.</span></span>
1. <span data-ttu-id="266c4-126">Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="266c4-126">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="266c4-127">Stel daarna de volgende velden in voor de nieuwe rij:</span><span class="sxs-lookup"><span data-stu-id="266c4-127">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="266c4-128">**Probleemtype**: voer een unieke id of naam voor het probleemtype in.</span><span class="sxs-lookup"><span data-stu-id="266c4-128">**Problem type** – Enter a unique ID or name for the problem type.</span></span>
    - <span data-ttu-id="266c4-129">**Beschrijving**: voer een gedetailleerde beschrijving van het probleemtype in.</span><span class="sxs-lookup"><span data-stu-id="266c4-129">**Description** – Enter a detailed description of the problem type.</span></span>

1. <span data-ttu-id="266c4-130">Selecteer, terwijl de nieuwe rij nog steeds is geselecteerd, de optie **Niet-conformeringstypen** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="266c4-130">While the new row is still selected, select **Non conformance types** on the Action Pane.</span></span>
1. <span data-ttu-id="266c4-131">Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="266c4-131">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="266c4-132">Vervolgens stelt u voor de nieuwe rij het veld **Niet-conformeringstype** in op het niet-conformeringstype dat u voor het probleemtype wilt toestaan.</span><span class="sxs-lookup"><span data-stu-id="266c4-132">Then, for the new row, set the **Non conformance type** field to the nonconformance type that you want to allow for the problem type.</span></span>
1. <span data-ttu-id="266c4-133">Herhaal de vorige stap voor elk extra niet-conformeringstype dat u voor het probleemtype wilt autoriseren.</span><span class="sxs-lookup"><span data-stu-id="266c4-133">Repeat the previous step for each additional nonconformance type that you want to authorize for the problem type.</span></span>
1. <span data-ttu-id="266c4-134">Sluit de pagina's.</span><span class="sxs-lookup"><span data-stu-id="266c4-134">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="266c4-135">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="266c4-135">Additional resources</span></span>

- [<span data-ttu-id="266c4-136">Overzicht van kwaliteitsbeheer</span><span class="sxs-lookup"><span data-stu-id="266c4-136">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="266c4-137">Beheer van kwaliteit en niet-conformeringen inschakelen</span><span class="sxs-lookup"><span data-stu-id="266c4-137">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="266c4-138">Medewerkers die verantwoordelijk zijn voor het goedkeuren van niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="266c4-138">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="266c4-139">Quarantainezones voor niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="266c4-139">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="266c4-140">Typen diagnosen voor niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="266c4-140">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="266c4-141">Kwaliteitstoeslagen voor niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="266c4-141">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="266c4-142">Bewerkingen voor niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="266c4-142">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="266c4-143">Kwaliteitsbeheer voor magazijnprocessen</span><span class="sxs-lookup"><span data-stu-id="266c4-143">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
