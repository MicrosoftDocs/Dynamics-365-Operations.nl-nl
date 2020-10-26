---
title: Een organisatierapporthiërarchie maken
description: Gebruik deze procedure om een rapporthiërarchie te maken voor organisatierapportage.
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 57203a7ddbacd631cbf800fb3a98e35a485cb74f
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976254"
---
# <a name="create-an-organization-report-hierarchy"></a><span data-ttu-id="d1dfe-103">Een organisatierapporthiërarchie maken</span><span class="sxs-lookup"><span data-stu-id="d1dfe-103">Create an organization report hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d1dfe-104">Gebruik deze procedure om een rapporthiërarchie te maken voor organisatierapportage.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-104">Use this procedure to create a report hierarchy for organization reporting.</span></span> <span data-ttu-id="d1dfe-105">Het doel van deze registratie is u te helpen door de dimensiehiërarchie, zodat u door kunt gaan totdat de hele organisatierapportagestructuur is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-105">The purpose of this recording is to guide you through the dimension hierarchy so that you can continue until the whole organization reporting structure is created.</span></span> <span data-ttu-id="d1dfe-106">Deze registratie gebruikt het USP2-demogegevensbedrijf.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="d1dfe-107">Ga naar Kostprijsboekhouding > Dimensies > Dimensiehiërarchieën.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-107">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="d1dfe-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-108">Click New.</span></span>
3. <span data-ttu-id="d1dfe-109">Selecteer in het veld HierarchyTypeComboBox 'Hiërarchie dimensieclassificatie'.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-109">In the HierarchyTypeComboBox field, select 'Dimension classification hierarchy'.</span></span>
    * <span data-ttu-id="d1dfe-110">Selecteer Hiërarchie dimensieclassificatie.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-110">Select Dimension classification hierarchy.</span></span> <span data-ttu-id="d1dfe-111">Het type Hiërarchie dimensieclassificatie wordt gebruikt om regels voor rapportagedoeleinden te definiëren.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-111">The Dimension classification hierarchy type is used to define rules and for reporting purposes.</span></span> <span data-ttu-id="d1dfe-112">Het biedt ondersteuning voor alle dimensies, zoals kostenobjecten, kostenelementen en statistische dimensies.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-112">It supports all dimensions, such as cost objects, cost elements, and statistical dimensions.</span></span>  
4. <span data-ttu-id="d1dfe-113">Klik op Maken.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-113">Click Create.</span></span>
5. <span data-ttu-id="d1dfe-114">Typ 'Oganisatie USP2' in het veld Naam van dimensiehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-114">In the Dimension hierarchy name field, type 'Oganization USP2'.</span></span>
6. <span data-ttu-id="d1dfe-115">Typ of selecteer een waarde in het veld Dimensie.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-115">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="d1dfe-116">Selecteer Kostenplaatsen.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-116">Select Cost centers.</span></span>  
7. <span data-ttu-id="d1dfe-117">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-117">Click Save.</span></span>
8. <span data-ttu-id="d1dfe-118">Klik op Hiërarchie weergeven.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-118">Click View hierarchy.</span></span>
9. <span data-ttu-id="d1dfe-119">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-119">Click New.</span></span>
10. <span data-ttu-id="d1dfe-120">Typ 'CEO' in het veld Knooppunt.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-120">In the Node name field, type 'CEO'.</span></span>
11. <span data-ttu-id="d1dfe-121">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-121">Click Save.</span></span>
12. <span data-ttu-id="d1dfe-122">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-122">Click New.</span></span>
13. <span data-ttu-id="d1dfe-123">Typ 'CEO kostenplaatsen' in het veld Naam knooppunt.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-123">In the Node name field, type 'CEO cost centers'.</span></span>
14. <span data-ttu-id="d1dfe-124">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-124">Click Save.</span></span>
15. <span data-ttu-id="d1dfe-125">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-125">Click New.</span></span>
16. <span data-ttu-id="d1dfe-126">Typ 'Oostelijke regio' in het veld Naam knooppunt.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-126">In the Node name field, type 'Region East'.</span></span>
17. <span data-ttu-id="d1dfe-127">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-127">Click Save.</span></span>
18. <span data-ttu-id="d1dfe-128">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-128">Click New.</span></span>
19. <span data-ttu-id="d1dfe-129">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-129">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="d1dfe-130">Typ of selecteer een waarde in het veld Van dimensielid.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-130">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="d1dfe-131">Selecteer het dimensielid dat met het knooppunt overeenkomt.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-131">Select the dimension member that corresponds to the node.</span></span>  
21. <span data-ttu-id="d1dfe-132">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-132">Click Save.</span></span>
22. <span data-ttu-id="d1dfe-133">Selecteer in de structuur 'Organisatie USP2\CEO\CEO kostenplaatsen'.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-133">In the tree, select 'Oganization USP2\CEO\CEO cost centers'.</span></span>
23. <span data-ttu-id="d1dfe-134">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-134">Click New.</span></span>
24. <span data-ttu-id="d1dfe-135">Typ 'Westelijke regio' in het veld Naam knooppunt.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-135">In the Node name field, type 'Region West'.</span></span>
25. <span data-ttu-id="d1dfe-136">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-136">Click Save.</span></span>
26. <span data-ttu-id="d1dfe-137">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-137">Click New.</span></span>
27. <span data-ttu-id="d1dfe-138">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-138">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="d1dfe-139">Typ of selecteer een waarde in het veld Van dimensielid.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-139">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="d1dfe-140">Selecteer het dimensielid dat met het knooppunt overeenkomt.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-140">Select the dimension member that corresponds to the node.</span></span>  
29. <span data-ttu-id="d1dfe-141">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-141">Click Save.</span></span>
30. <span data-ttu-id="d1dfe-142">Selecteer in de structuur 'Organisatie USP2\CEO'.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-142">In the tree, select 'Oganization USP2\CEO'.</span></span>
31. <span data-ttu-id="d1dfe-143">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-143">Click New.</span></span>
32. <span data-ttu-id="d1dfe-144">Typ 'CFO kostenplaatsen' in het veld Naam knooppunt.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-144">In the Node name field, type 'CFO cost centers'.</span></span>
33. <span data-ttu-id="d1dfe-145">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-145">Click Save.</span></span>
34. <span data-ttu-id="d1dfe-146">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-146">Click New.</span></span>
35. <span data-ttu-id="d1dfe-147">Typ 'Marketingcampagne' in het veld Naam knooppunt.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-147">In the Node name field, type 'Marketing campa'.</span></span>
36. <span data-ttu-id="d1dfe-148">Typ 'Marketingcampagne' in het veld Naam knooppunt.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-148">In the Node name field, type 'Marketing campaign'.</span></span>
37. <span data-ttu-id="d1dfe-149">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-149">Click Save.</span></span>
38. <span data-ttu-id="d1dfe-150">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-150">Click New.</span></span>
39. <span data-ttu-id="d1dfe-151">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-151">In the list, mark the selected row.</span></span>
40. <span data-ttu-id="d1dfe-152">Typ of selecteer een waarde in het veld Van dimensielid.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-152">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="d1dfe-153">Selecteer het dimensielid dat met het knooppunt overeenkomt.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-153">Select the dimension member that corresponds to the node.</span></span>  
41. <span data-ttu-id="d1dfe-154">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-154">Click Save.</span></span>
42. <span data-ttu-id="d1dfe-155">Selecteer in de structuur Organisatie USP2\CEO\CFO kostenplaatsen.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-155">In the tree, select 'Organization USP2\CEO\CFO cost centers'.</span></span>
43. <span data-ttu-id="d1dfe-156">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-156">Click New.</span></span>
44. <span data-ttu-id="d1dfe-157">Typ 'Handelsbeurzen' in het veld Naam knooppunt.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-157">In the Node name field, type 'Trade shows'.</span></span>
45. <span data-ttu-id="d1dfe-158">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-158">Click Save.</span></span>
46. <span data-ttu-id="d1dfe-159">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-159">Click New.</span></span>
47. <span data-ttu-id="d1dfe-160">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-160">In the list, mark the selected row.</span></span>
48. <span data-ttu-id="d1dfe-161">Typ of selecteer een waarde in het veld Van dimensielid.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-161">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="d1dfe-162">Selecteer het dimensielid dat met het knooppunt overeenkomt.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-162">Select the dimension member that corresponds to the node.</span></span>  
49. <span data-ttu-id="d1dfe-163">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-163">Click Save.</span></span>
50. <span data-ttu-id="d1dfe-164">Selecteer in de structuur 'Organisatie USP2\CEO'.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-164">In the tree, select 'Oganization USP2\CEO'.</span></span>
51. <span data-ttu-id="d1dfe-165">Typ 'CIO kostenplaatsen' in het veld Naam knooppunt.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-165">In the Node name field, type 'CIO cost centers'.</span></span>
52. <span data-ttu-id="d1dfe-166">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-166">Click Save.</span></span>
53. <span data-ttu-id="d1dfe-167">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-167">Click New.</span></span>
54. <span data-ttu-id="d1dfe-168">Typ 'Callcenters' in het veld Naam knooppunt.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-168">In the Node name field, type 'Call centers'.</span></span>
55. <span data-ttu-id="d1dfe-169">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-169">Click Save.</span></span>
56. <span data-ttu-id="d1dfe-170">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-170">Click New.</span></span>
57. <span data-ttu-id="d1dfe-171">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-171">In the list, mark the selected row.</span></span>
58. <span data-ttu-id="d1dfe-172">Typ of selecteer een waarde in het veld Van dimensielid.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-172">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="d1dfe-173">Selecteer het dimensielid dat met het knooppunt overeenkomt.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-173">Select the dimension member that corresponds to the node.</span></span>  
59. <span data-ttu-id="d1dfe-174">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-174">Click Save.</span></span>

