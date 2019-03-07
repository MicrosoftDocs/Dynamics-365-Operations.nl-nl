---
title: Automatische vrachtafstemming instellen
description: Deze procedure laat zien hoe u gegevens instelt voor automatische vrachtafstemming.
author: ShylaThompson
manager: AnnBe
ms.date: 10/16/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSFreightBillType, TMSFreightBillTypeAssignment, TMSCarrierCodeLookup, DefaultDashboard, TMSAuditMaster
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b7772ad779495b36941a3dc86cc456d80a964467
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "357468"
---
# <a name="set-up-automatic-freight-reconciliation"></a><span data-ttu-id="a123a-103">Automatische vrachtafstemming instellen</span><span class="sxs-lookup"><span data-stu-id="a123a-103">Set up automatic freight reconciliation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a123a-104">Deze procedure laat zien hoe u gegevens instelt voor automatische vrachtafstemming.</span><span class="sxs-lookup"><span data-stu-id="a123a-104">This procedure shows how to set up data for automatic freight reconciliation.</span></span> <span data-ttu-id="a123a-105">Dit wordt gewoonlijk uitgevoerd door een magazijnmanager.</span><span class="sxs-lookup"><span data-stu-id="a123a-105">This is typically done by a warehouse manager.</span></span> <span data-ttu-id="a123a-106">U kunt deze procedure gebruiken in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="a123a-106">You can use this procedure in demo data company USMF.</span></span>


## <a name="set-up-the-freight-bill-type"></a><span data-ttu-id="a123a-107">Stel het vrachtfactuurtype in</span><span class="sxs-lookup"><span data-stu-id="a123a-107">Set up the freight bill type</span></span>
1. <span data-ttu-id="a123a-108">Ga naar Transportbeheer > Instellen > Vrachtafstemming > Type vrachtfactuur.</span><span class="sxs-lookup"><span data-stu-id="a123a-108">Go to Transportation management > Setup > Freight reconciliation > Freight bill type.</span></span>
    * <span data-ttu-id="a123a-109">Het type vrachtrekening bepaalt hoe de vrachtrekeningen en vervoerderfacturen moeten worden afgestemd.</span><span class="sxs-lookup"><span data-stu-id="a123a-109">The freight bill type defines how freight bills and carrier invoices  should be matched.</span></span>  
2. <span data-ttu-id="a123a-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="a123a-110">Click New.</span></span>
3. <span data-ttu-id="a123a-111">Typ een waarde in het veld Vrachtfactuur.</span><span class="sxs-lookup"><span data-stu-id="a123a-111">In the Freight bill type field, type a value.</span></span>
4. <span data-ttu-id="a123a-112">Typ in het veld Engine-assembly 'Microsoft.Dynamics.Ax.Tms.dll'.</span><span class="sxs-lookup"><span data-stu-id="a123a-112">In the Engine assembly field, type 'Microsoft.Dynamics.Ax.Tms.dll'.</span></span>
    * <span data-ttu-id="a123a-113">Dit is de standaardcodebibliotheek voor de afstemmingsengine Transportbeheer.</span><span class="sxs-lookup"><span data-stu-id="a123a-113">This is the standard Transportation management matching engine code library.</span></span>  
5. <span data-ttu-id="a123a-114">Typ in het veld Engineklasse 'Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer'.</span><span class="sxs-lookup"><span data-stu-id="a123a-114">In the Engine class field, type 'Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer'.</span></span>
    * <span data-ttu-id="a123a-115">Dit is de standaardklasse voor de afstemmingsengine Transportbeheer.</span><span class="sxs-lookup"><span data-stu-id="a123a-115">This is the standard Transportation management matching engine class.</span></span>  
6. <span data-ttu-id="a123a-116">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="a123a-116">Click New.</span></span>
7. <span data-ttu-id="a123a-117">Kies in het veld Omschrijving de waarde die moet overeenkomen op de vrachtrekening en de vervoerderfactuur.</span><span class="sxs-lookup"><span data-stu-id="a123a-117">In the Description field, choose the value that should match on the freight bill and the carrier invoice.</span></span>  
8. <span data-ttu-id="a123a-118">Selecteer Ja in het veld Overeenkomst vereist.</span><span class="sxs-lookup"><span data-stu-id="a123a-118">In the Match required field, select 'Yes'.</span></span>
    * <span data-ttu-id="a123a-119">Als u dit veld instelt op Ja, betekent dit dat de geselecteerde waarde in het veld Omschrijving overeen moet komen met de vrachtfactuur en de vervoerderfactuur.</span><span class="sxs-lookup"><span data-stu-id="a123a-119">If you set this field to Yes this means that the value selected in the Description field needs to match on both the freight bill and the carrier invoice.</span></span> <span data-ttu-id="a123a-120">Als u dit instelt op Nee, kan het veld in een van deze leeg zijn.</span><span class="sxs-lookup"><span data-stu-id="a123a-120">If you set it to No, the field can be blank on one of these.</span></span>  
9. <span data-ttu-id="a123a-121">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="a123a-121">Click Save.</span></span>

## <a name="set-up-the-freight-bill-type-assignment"></a><span data-ttu-id="a123a-122">Stel de toewijzing van het vrachtfactuurtype in</span><span class="sxs-lookup"><span data-stu-id="a123a-122">Set up the freight bill type assignment</span></span>
1. <span data-ttu-id="a123a-123">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a123a-123">Close the page.</span></span>
2. <span data-ttu-id="a123a-124">Ga naar Transportbeheer > Instellen > Vrachtafstemming > Type toewijzingen van vrachtfractuur.</span><span class="sxs-lookup"><span data-stu-id="a123a-124">Go to Transportation management > Setup > Freight reconciliation > Freight bill type assignments.</span></span>
    * <span data-ttu-id="a123a-125">De toewijzing van de vrachtrekening wordt gebruikt om op te geven welk type vrachtrekening voor een bepaalde vervoerder wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="a123a-125">The freight bill type assignment is used to specify which freight bill type is used for a particular carrier.</span></span>   
3. <span data-ttu-id="a123a-126">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="a123a-126">Click New.</span></span>
4. <span data-ttu-id="a123a-127">Typ of selecteer een waarde in het veld Modus.</span><span class="sxs-lookup"><span data-stu-id="a123a-127">In the Mode field, enter or select a value.</span></span>
5. <span data-ttu-id="a123a-128">Typ of selecteer een waarde in het veld Vervoerder.</span><span class="sxs-lookup"><span data-stu-id="a123a-128">In the Shipping carrier field, enter or select a value.</span></span>
6. <span data-ttu-id="a123a-129">Selecteer in het veld Type vrachtfactuur het type vrachtfactuur dat u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="a123a-129">In the Freight bill type field, select the freight bill type that you created earlier.</span></span>
7. <span data-ttu-id="a123a-130">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a123a-130">Close the page.</span></span>

## <a name="set-up-the-audit-master"></a><span data-ttu-id="a123a-131">Stel het controlemodel in</span><span class="sxs-lookup"><span data-stu-id="a123a-131">Set up the audit master</span></span>
1. <span data-ttu-id="a123a-132">Ga naar Transportbeheer > Instellen > Vrachtafstemming > Controlemodel.</span><span class="sxs-lookup"><span data-stu-id="a123a-132">Go to Transportation management > Setup > Freight reconciliation > Audit master.</span></span>
    * <span data-ttu-id="a123a-133">Het controlemodel bepaalt de tolerantielimieten voor automatische vrachtafstemming.</span><span class="sxs-lookup"><span data-stu-id="a123a-133">The audit master defines the tolerance limits for automatic freight reconciliation.</span></span> <span data-ttu-id="a123a-134">Het specificeert met hoeveel de monetaire bedragen op de vrachtrekening en de vervoerderfactuur kunnen verschillen en toch nog afstemming toestaan.</span><span class="sxs-lookup"><span data-stu-id="a123a-134">It specifies by how much the monetary amounts on the freight bill and the carrier invoice can differ and still allow reconciliation to occur.</span></span> <span data-ttu-id="a123a-135">Het bepaalt ook hoe om verschillen worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="a123a-135">It also defines how to handle discrepancies.</span></span>  
2. <span data-ttu-id="a123a-136">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="a123a-136">Click New.</span></span>
3. <span data-ttu-id="a123a-137">Typ een waarde in het veld Controlemodel-id.</span><span class="sxs-lookup"><span data-stu-id="a123a-137">In the Audit master ID field, type a value.</span></span>
4. <span data-ttu-id="a123a-138">Selecteer in het veld Vervoerder dezelfde vervoerder als eerder.</span><span class="sxs-lookup"><span data-stu-id="a123a-138">In the Shipping carrier  field, select the same shipping carrier as you did earlier.</span></span>
5. <span data-ttu-id="a123a-139">Selecteer in het veld Type vrachtfactuur het type vrachtfactuur dat u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="a123a-139">In the Freight bill type field, select the freight bill type that you created earlier.</span></span>
6. <span data-ttu-id="a123a-140">Vouw de sectie Tolerantie uit.</span><span class="sxs-lookup"><span data-stu-id="a123a-140">Expand the Tolerance section.</span></span>
7. <span data-ttu-id="a123a-141">Typ een getal in het veld Minimumtolerantie.</span><span class="sxs-lookup"><span data-stu-id="a123a-141">In the Minimum tolerance level field, enter a number.</span></span>
8. <span data-ttu-id="a123a-142">Typ een getal in het veld Maximumtolerantie.</span><span class="sxs-lookup"><span data-stu-id="a123a-142">In the Maximum tolerance level field, enter a number.</span></span>
9. <span data-ttu-id="a123a-143">Vouw de sectie Resultaat uit.</span><span class="sxs-lookup"><span data-stu-id="a123a-143">Expand the Result section.</span></span>
10. <span data-ttu-id="a123a-144">Typ of selecteer een waarde in het veld Redencode voor overbetaling.</span><span class="sxs-lookup"><span data-stu-id="a123a-144">In the Overpayment reason code field, enter or select a value.</span></span>
    * <span data-ttu-id="a123a-145">Als de monetaire bedragen op de vrachtrekening en de vervoerderfactuur verschillen, geven de redencodes voor overbetaling en onderbetaling de rekeningen aan waarop het verschil moet worden geregistreerd, zolang het verschil binnen de tolerantieniveaus is.</span><span class="sxs-lookup"><span data-stu-id="a123a-145">If the monetary amounts differ on the freight bill and the carrier invoice, the overpayment and underpayment reason codes specify the accounts that the difference should be registered on, as long as the difference is within the tolerance levels.</span></span>  
11. <span data-ttu-id="a123a-146">Typ of selecteer een waarde in het veld Redencode voor onderbetaling.</span><span class="sxs-lookup"><span data-stu-id="a123a-146">In the Underpayment reason code field, enter or select a value.</span></span>
12. <span data-ttu-id="a123a-147">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a123a-147">Close the page.</span></span>

