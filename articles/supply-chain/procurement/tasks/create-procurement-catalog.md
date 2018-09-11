--- 
title: Een inkoopcatalogus maken
description: Deze handleiding laat zien hoe u een aanschaffingscatalogus maakt.
author: mkirknel
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 071b73b3498bdb346f5916a770a43174ef896568
ms.contentlocale: nl-nl
ms.lasthandoff: 09/11/2018

---
# <a name="create-a-procurement-catalog"></a><span data-ttu-id="867cb-103">Een inkoopcatalogus maken</span><span class="sxs-lookup"><span data-stu-id="867cb-103">Create a procurement catalog</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="867cb-104">Deze handleiding laat zien hoe u een aanschaffingscatalogus maakt.</span><span class="sxs-lookup"><span data-stu-id="867cb-104">This guide shows you how to create a procurement catalog.</span></span> <span data-ttu-id="867cb-105">Deze taak wordt gewoonlijk uitgevoerd door een inkoopmedewerker.</span><span class="sxs-lookup"><span data-stu-id="867cb-105">This task would typically be carried out by a procurement professional.</span></span> <span data-ttu-id="867cb-106">U komt ook te weten hoe werknemers de catalogus kunnen gebruiken wanneer zij een bestelopdracht maken.</span><span class="sxs-lookup"><span data-stu-id="867cb-106">You will also learn how employees can use the catalog when they create a requisition.</span></span> <span data-ttu-id="867cb-107">Voordat u een catalogus kunt maken, moet er een hiërarchie van aanschaffingscategorieën in uw systeem worden ingesteld.</span><span class="sxs-lookup"><span data-stu-id="867cb-107">Before you can create a catalog, there must be a procurement category hierarchy in your system.</span></span> <span data-ttu-id="867cb-108">De hiërarchie wordt overgenomen door de nieuwe catalogus, samen met alle producten in de hiërarchie.</span><span class="sxs-lookup"><span data-stu-id="867cb-108">The hierarchy is inherited by the new catalog, along with all the products that are in the hierarchy.</span></span> <span data-ttu-id="867cb-109">U kunt deze handleiding in het demobedrijf USMF gebruiken waar de hiërarchie van aanschaffingscategorieën beschikbaar is, evenals de voorbeelden die zijn gebruikt in de procedurestappen.</span><span class="sxs-lookup"><span data-stu-id="867cb-109">You can use this guide in demo data company USMF where the procurement category hierarchy is available, as well as the examples used in the procedure steps.</span></span>


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a><span data-ttu-id="867cb-110">Controleren of er een hiërarchie van aanschaffingscategorieën bestaat</span><span class="sxs-lookup"><span data-stu-id="867cb-110">Ensure that a procurement category hierarchy exists</span></span>
1. <span data-ttu-id="867cb-111">Ga naar Inkoop en sourcing > Inkoopcategorieën.</span><span class="sxs-lookup"><span data-stu-id="867cb-111">Go to Procurement and sourcing > Procurement categories.</span></span>
    * <span data-ttu-id="867cb-112">In het USMF-demobedrijf is een hiërarchie van aanschaffingscategorieën beschikbaar en er zijn producten toegevoegd aan de categorie Kantoormachines/Computers.</span><span class="sxs-lookup"><span data-stu-id="867cb-112">A procurement category hierarchy is available in the USMF demo data company and products have been added to the Office machines/Computers category.</span></span> <span data-ttu-id="867cb-113">Als u deze procedure uitvoert als taakbegeleiding, moet u de taakbegeleiding ontgrendelen als u door de categorie wilt bladeren.</span><span class="sxs-lookup"><span data-stu-id="867cb-113">If you’re running this procedure as a task guide, you’ll need to unlock the guide if you want to browse through the category.</span></span> <span data-ttu-id="867cb-114">Als er geen hiërarchie beschikbaar was, zou u deze maken door op Nieuw te klikken.</span><span class="sxs-lookup"><span data-stu-id="867cb-114">If a hierarchy was not available, you’d create it by clicking New.</span></span> <span data-ttu-id="867cb-115">Dit kan slechts één keer worden gedaan.</span><span class="sxs-lookup"><span data-stu-id="867cb-115">This can only be done once.</span></span>  
2. <span data-ttu-id="867cb-116">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="867cb-116">Close the page.</span></span>

## <a name="create-a-catalog"></a><span data-ttu-id="867cb-117">Een catalogus maken</span><span class="sxs-lookup"><span data-stu-id="867cb-117">Create a catalog</span></span>
1. <span data-ttu-id="867cb-118">Ga naar Inkoopbeheer > Catalogi > Inkoopcatalogi.</span><span class="sxs-lookup"><span data-stu-id="867cb-118">Go to Procurement and sourcing > Catalogs > Procurement catalogs.</span></span>
2. <span data-ttu-id="867cb-119">Klik op Nieuwe aanschaffingscatalogus om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="867cb-119">Click New procurement catalog to open the drop dialog.</span></span>
3. <span data-ttu-id="867cb-120">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="867cb-120">In the Name field, type a value.</span></span>
4. <span data-ttu-id="867cb-121">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="867cb-121">Click OK.</span></span>
5. <span data-ttu-id="867cb-122">Vouw in de structuur 'CORP-AANSCHAFFINGSCATEGORIEËN' uit.</span><span class="sxs-lookup"><span data-stu-id="867cb-122">In the tree, expand 'CORP PROCUREMENT CATEGORIES'.</span></span>
6. <span data-ttu-id="867cb-123">Vouw 'KANTOORMACHINES' uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="867cb-123">In the tree, expand 'OFFICE MACHINES'.</span></span>
7. <span data-ttu-id="867cb-124">Selecteer 'Computers' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="867cb-124">In the tree, select 'Computers'.</span></span>
    * <span data-ttu-id="867cb-125">De producten uit de aanschaffingscategorie worden weergegeven in de lijst.</span><span class="sxs-lookup"><span data-stu-id="867cb-125">The products from the procurement category are displayed in the list.</span></span> <span data-ttu-id="867cb-126">Als u een product aan de categorie wilt toevoegen, moet u dit doen op de pagina Hiërarchie van inkoopcategorieën of op de pagina Artikelgegevens.</span><span class="sxs-lookup"><span data-stu-id="867cb-126">If you want to add a product to the category you need to do this on the Procurement category hierarchy page or on the Item details page.</span></span>  
    * <span data-ttu-id="867cb-127">Het standaard bijwerktype bepaalt of nieuwe producten die aan de hiërarchie van aanschaffingscategorieën zijn toegevoegd direct zichtbaar zijn in de catalogus.</span><span class="sxs-lookup"><span data-stu-id="867cb-127">The Default update type determines whether new products that have been added to the procurement category hierarchy are immediately visible in the catalog.</span></span> <span data-ttu-id="867cb-128">Als het bijwerktype is ingesteld op Dynamisch, zijn wijzigingen direct zichtbaar.</span><span class="sxs-lookup"><span data-stu-id="867cb-128">If the update type is set to Dynamic, changes are visible immediately.</span></span> <span data-ttu-id="867cb-129">Als het bijwerktype Statisch is, zijn nieuwe producten alleen zichtbaar voor mensen die de catalogus gebruiken nadat de catalogus opnieuw is uitgegeven.</span><span class="sxs-lookup"><span data-stu-id="867cb-129">If the update type is Static, new products are only visible to people using the catalog after the catalog has been re-published.</span></span> <span data-ttu-id="867cb-130">De actie Publiceren is beschikbaar in het actievenster boven aan de pagina.</span><span class="sxs-lookup"><span data-stu-id="867cb-130">The Publish action is available on the Action Pane at the top of the page.</span></span> <span data-ttu-id="867cb-131">Als producten worden verwijderd uit de hiërarchie van aanschaffingscategorieën, is de wijziging direct zichtbaar, ongeacht de waarde in het Veld het Standaard bijwerktype.</span><span class="sxs-lookup"><span data-stu-id="867cb-131">If products are removed from the procurement category hierarchy, the change is immediately visible, regardless of the value in the Default update type field.</span></span>  
8. <span data-ttu-id="867cb-132">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="867cb-132">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="867cb-133">Klik op Verbergen.</span><span class="sxs-lookup"><span data-stu-id="867cb-133">Click Hide.</span></span>
10. <span data-ttu-id="867cb-134">Klik in het actievenster op Categorienavigatie.</span><span class="sxs-lookup"><span data-stu-id="867cb-134">On the Action Pane, click Category navigation.</span></span>
11. <span data-ttu-id="867cb-135">Klik op Uitschakelen.</span><span class="sxs-lookup"><span data-stu-id="867cb-135">Click Disable.</span></span>
12. <span data-ttu-id="867cb-136">Klik in het actievenster op Categorienavigatie.</span><span class="sxs-lookup"><span data-stu-id="867cb-136">On the Action Pane, click Category navigation.</span></span>
13. <span data-ttu-id="867cb-137">Klik op Inschakelen.</span><span class="sxs-lookup"><span data-stu-id="867cb-137">Click Enable.</span></span>
14. <span data-ttu-id="867cb-138">Klik op Catalogus activeren.</span><span class="sxs-lookup"><span data-stu-id="867cb-138">Click Activate catalog.</span></span>
15. <span data-ttu-id="867cb-139">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="867cb-139">Close the page.</span></span>

## <a name="make-the-catalog-visible"></a><span data-ttu-id="867cb-140">De catalogus zichtbaar maken</span><span class="sxs-lookup"><span data-stu-id="867cb-140">Make the catalog visible</span></span>
1. <span data-ttu-id="867cb-141">Ga naar Inkoopbeheer > Instellingen > Beleid > Inkoopbeleid.</span><span class="sxs-lookup"><span data-stu-id="867cb-141">Go to Procurement and sourcing > Setup > Policies > Purchasing policies.</span></span>
2. <span data-ttu-id="867cb-142">Selecteer Aanschaffingsbeleid USMF.</span><span class="sxs-lookup"><span data-stu-id="867cb-142">Select Procurement Policy USMF.</span></span>
    * <span data-ttu-id="867cb-143">U moet het aanschafbeleid selecteren voor de rechtspersoon waarvoor de medewerker die met uw gebruikersprofiel is verbonden producten mag bestellen.</span><span class="sxs-lookup"><span data-stu-id="867cb-143">You need to select the purchasing policy for the legal entity that the worker connected to your user profile is allowed to order products in.</span></span> <span data-ttu-id="867cb-144">In de USMF-demogegevens, is de gebruiker Beheerder gekoppeld aan de medewerker genaamd Julia Funderburk en zij bestelt standaard producten in USMF.</span><span class="sxs-lookup"><span data-stu-id="867cb-144">In the USMF demo data, the Admin user is connected to the worker called Julia Funderburk, and she orders products in USMF by default.</span></span>  
3. <span data-ttu-id="867cb-145">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="867cb-145">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="867cb-146">Selecteer de catalogus die u zojuist hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="867cb-146">Select the catalog that you’ve just created.</span></span>
5. <span data-ttu-id="867cb-147">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="867cb-147">Click OK.</span></span>
6. <span data-ttu-id="867cb-148">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="867cb-148">Close the page.</span></span>
7. <span data-ttu-id="867cb-149">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="867cb-149">Close the page.</span></span>

## <a name="use-the-catalog"></a><span data-ttu-id="867cb-150">De catalogus gebruiken</span><span class="sxs-lookup"><span data-stu-id="867cb-150">Use the catalog</span></span>
1. <span data-ttu-id="867cb-151">Ga naar Inkoopbeheer > Opdrachten tot inkoop > Alle opdrachten tot inkoop.</span><span class="sxs-lookup"><span data-stu-id="867cb-151">Go to Procurement and sourcing > Purchase requisitions > All purchase requisitions.</span></span>
2. <span data-ttu-id="867cb-152">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="867cb-152">Click New.</span></span>
3. <span data-ttu-id="867cb-153">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="867cb-153">In the Name field, type a value.</span></span>
4. <span data-ttu-id="867cb-154">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="867cb-154">Click OK.</span></span>
5. <span data-ttu-id="867cb-155">Klik op Producten toevoegen.</span><span class="sxs-lookup"><span data-stu-id="867cb-155">Click Add products.</span></span>
6. <span data-ttu-id="867cb-156">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="867cb-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="867cb-157">U kunt de categoriehiërarchie aan de linkerkant of het filter boven aan de lijst gebruiken om de producten te filteren.</span><span class="sxs-lookup"><span data-stu-id="867cb-157">You can use the category hierarchy on the left or the filter at the top of the list to filter the products.</span></span>  
7. <span data-ttu-id="867cb-158">Klik op Regels toevoegen.</span><span class="sxs-lookup"><span data-stu-id="867cb-158">Click Add to lines.</span></span>
8. <span data-ttu-id="867cb-159">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="867cb-159">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="867cb-160">Klik op Regels toevoegen.</span><span class="sxs-lookup"><span data-stu-id="867cb-160">Click Add to lines.</span></span>
10. <span data-ttu-id="867cb-161">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="867cb-161">Click OK.</span></span>


