--- 
title: "Een hiërarchie van aanschaffingscategorieën instellen"
description: "Deze procedure laat zien hoe u nieuwe knooppunten in een hiërarchie van aanschaffingscategorieën maakt en hoe u een aanschaffingscategorie configureert die in een aanschaffingsproces moet worden gebruikt."
author: mkirknel
manager: AnnBe
ms.date: 11/06/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 767fbe69eb918b6e37842ad1c393d08d11346e71
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="92ede-103">Een hiërarchie van aanschaffingscategorieën instellen</span><span class="sxs-lookup"><span data-stu-id="92ede-103">Set up a procurement category hierarchy</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="92ede-104">Deze procedure laat zien hoe u nieuwe knooppunten in een hiërarchie van aanschaffingscategorieën maakt en hoe u een aanschaffingscategorie configureert die in een aanschaffingsproces moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="92ede-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="92ede-105">Deze taken worden meestal uitgevoerd door een inkoopmanager.</span><span class="sxs-lookup"><span data-stu-id="92ede-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="92ede-106">Voordat u deze procedure kunt starten, moet er een categoriehiërarchie van het type Inkoop zijn.</span><span class="sxs-lookup"><span data-stu-id="92ede-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="92ede-107">Als u een demobedrijf gebruikt, kunt u deze procedure in het bedrijf USMF uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="92ede-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="92ede-108">Een nieuwe inkoopcategorie toevoegen</span><span class="sxs-lookup"><span data-stu-id="92ede-108">Add a new procurement category</span></span>
1. <span data-ttu-id="92ede-109">Ga naar Inkoop en sourcing > Inkoopcategorieën.</span><span class="sxs-lookup"><span data-stu-id="92ede-109">Go to Procurement and sourcing > Procurement categories.</span></span>
2. <span data-ttu-id="92ede-110">Klik op Categoriehiërarchie bewerken.</span><span class="sxs-lookup"><span data-stu-id="92ede-110">Click Edit category hierarchy.</span></span>
    * <span data-ttu-id="92ede-111">De huidige hiërarchie van aanschaffingscategorieën wordt weergegeven aan de linkerkant van de pagina.</span><span class="sxs-lookup"><span data-stu-id="92ede-111">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="92ede-112">U gaat de hiërarchie wijzigen.</span><span class="sxs-lookup"><span data-stu-id="92ede-112">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="92ede-113">Klik op Nieuw categorieknooppunt.</span><span class="sxs-lookup"><span data-stu-id="92ede-113">Click New category node.</span></span>
    * <span data-ttu-id="92ede-114">Het systeem selecteert standaard het bovenste knooppunt.</span><span class="sxs-lookup"><span data-stu-id="92ede-114">The system selects the top node by default.</span></span> <span data-ttu-id="92ede-115">Als u deze procedure als taakbegeleiding uitvoert, kunt u op de knop Ontgrendelen klikken en een ander bovenliggend knooppunt selecteren om uw nieuw knooppunt in te plaatsen.</span><span class="sxs-lookup"><span data-stu-id="92ede-115">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="92ede-116">Zodra dat is gedaan, vergrendelt u de taakbegeleiding opnieuw en klikt u op het categorieknooppunt Nieuw.</span><span class="sxs-lookup"><span data-stu-id="92ede-116">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="92ede-117">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="92ede-117">In the Name field, type a value.</span></span>
5. <span data-ttu-id="92ede-118">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="92ede-118">In the Description field, type a value.</span></span>
6. <span data-ttu-id="92ede-119">Typ een waarde in het veld Beschrijvende naam.</span><span class="sxs-lookup"><span data-stu-id="92ede-119">In the Friendly name field, type a value.</span></span>
    * <span data-ttu-id="92ede-120">De beschrijvende naam is optioneel.</span><span class="sxs-lookup"><span data-stu-id="92ede-120">The friendly name is optional.</span></span> <span data-ttu-id="92ede-121">Deze wordt in categoriezoekopdrachten met de categorienaam weergegeven.</span><span class="sxs-lookup"><span data-stu-id="92ede-121">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="92ede-122">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="92ede-122">Click Save.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="92ede-123">Producten aan uw nieuwe aanschaffingscategorie toevoegen</span><span class="sxs-lookup"><span data-stu-id="92ede-123">Add products to your new procurement category</span></span>
1. <span data-ttu-id="92ede-124">Ga naar Inkoop en sourcing > Inkoopcategorieën.</span><span class="sxs-lookup"><span data-stu-id="92ede-124">Go to Procurement and sourcing > Procurement categories.</span></span>
    * <span data-ttu-id="92ede-125">Selecteer het knooppunt dat u zojuist hebt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="92ede-125">Select the node you just added.</span></span> <span data-ttu-id="92ede-126">Als u de procedure als taakbegeleiding uitvoert, moet u de taakbegeleiding wellicht ontgrendelen om het knooppunt te selecteren.</span><span class="sxs-lookup"><span data-stu-id="92ede-126">If you’re running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="92ede-127">Schakel de uitbreiding van de sectie Producten om.</span><span class="sxs-lookup"><span data-stu-id="92ede-127">Toggle the expansion of the Products section.</span></span>
3. <span data-ttu-id="92ede-128">Klik op Toevoegen om producten te koppelen aan de aanschaffingscategorie.</span><span class="sxs-lookup"><span data-stu-id="92ede-128">Click Add to associate products with the procurement category.</span></span>
4. <span data-ttu-id="92ede-129">Selecteer het product dat u wilt toevoegen aan de aanschaffingscategorie.</span><span class="sxs-lookup"><span data-stu-id="92ede-129">Select the product you want to add to the procurement category.</span></span>
5. <span data-ttu-id="92ede-130">Klik op de pijl om het product te selecteren.</span><span class="sxs-lookup"><span data-stu-id="92ede-130">Click the arrow to select the product.</span></span>
6. <span data-ttu-id="92ede-131">Selecteer een ander product dat u wilt toevoegen aan de aanschaffingscategorie.</span><span class="sxs-lookup"><span data-stu-id="92ede-131">Select another product to add to the procurement category.</span></span>
7. <span data-ttu-id="92ede-132">Klik op de pijl om het product te selecteren.</span><span class="sxs-lookup"><span data-stu-id="92ede-132">Click the arrow to select the product.</span></span>
8. <span data-ttu-id="92ede-133">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="92ede-133">Click OK.</span></span>

## <a name="add-approved-and-preferred-vendors"></a><span data-ttu-id="92ede-134">Goedgekeurde en voorkeursleveranciers toevoegen</span><span class="sxs-lookup"><span data-stu-id="92ede-134">Add approved and preferred vendors</span></span>
1. <span data-ttu-id="92ede-135">Schakel de uitbreiding van de sectie Leveranciers om.</span><span class="sxs-lookup"><span data-stu-id="92ede-135">Toggle the expansion of the Vendors section.</span></span>
2. <span data-ttu-id="92ede-136">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="92ede-136">Click Add.</span></span>
    * <span data-ttu-id="92ede-137">U kunt nu een leverancier aan een aanschaffingscategorie toevoegen en opgeven of een leverancier de voorkeur heeft of alleen is goedgekeurd voor de categorie.</span><span class="sxs-lookup"><span data-stu-id="92ede-137">You can add a vendor to a procurement category and specify whether a vendor is preferred or just approved for the category.</span></span> <span data-ttu-id="92ede-138">Wanneer u een leverancier uit een categorie verwijdert, worden de historische transacties met de leverancier in de categorie niet verwijderd.</span><span class="sxs-lookup"><span data-stu-id="92ede-138">When you delete a vendor from a category, the historical transactions with the vendor in the category are not deleted.</span></span>   
3. <span data-ttu-id="92ede-139">Zoek de leverancier die u wilt toevoegen aan de categorie.</span><span class="sxs-lookup"><span data-stu-id="92ede-139">Find the vendor you want to add to the category.</span></span>
4. <span data-ttu-id="92ede-140">Klik op de pijl om de leverancier te selecteren.</span><span class="sxs-lookup"><span data-stu-id="92ede-140">Click the arrow to select the vendor.</span></span>
5. <span data-ttu-id="92ede-141">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="92ede-141">Click OK.</span></span>
6. <span data-ttu-id="92ede-142">Selecteer op de leveranciersrij die u wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="92ede-142">Select the vendor row that you want to modify.</span></span>
7. <span data-ttu-id="92ede-143">Selecteer een optie in het veld Leveranciersstatus.</span><span class="sxs-lookup"><span data-stu-id="92ede-143">In the Vendor status field, select an option.</span></span>
    * <span data-ttu-id="92ede-144">De instelling van de leverancierselectie in de categoriebeleidsregel bepaalt of favoriete, goedgekeurde of alle leveranciers beschikbaar zijn voor opdrachten tot inkoop.</span><span class="sxs-lookup"><span data-stu-id="92ede-144">The vendor selection setting in the Category policy rule governs whether preferred, approved, or all vendors are available on purchase requisitions.</span></span>   

## <a name="add-additional-information-to-the-category"></a><span data-ttu-id="92ede-145">Extra informatie aan de categorie toevoegen</span><span class="sxs-lookup"><span data-stu-id="92ede-145">Add additional information to the category</span></span>
1. <span data-ttu-id="92ede-146">Schakel de uitbreiding van de sectie Groepen evaluatiecriteria voor leveranciers om.</span><span class="sxs-lookup"><span data-stu-id="92ede-146">Toggle the expansion of the Vendor evaluation criterion groups section.</span></span>
    * <span data-ttu-id="92ede-147">Op dit tabblad kunt u definiëren op basis van welke criteria de leveranciers in de aanschaffingscategorie moeten worden beoordeeld.</span><span class="sxs-lookup"><span data-stu-id="92ede-147">This tab allows you to define which criteria the vendors in the procurement category should be rated against.</span></span> <span data-ttu-id="92ede-148">Om dit te doen moet u klikken op Toevoegen en vervolgens een leverancierevaluatiegroep selecteren die de gewenste criteria bevat.</span><span class="sxs-lookup"><span data-stu-id="92ede-148">To do this you would click Add and then select a vendor evaluation group that contains the criteria you want.</span></span>  
2. <span data-ttu-id="92ede-149">Schakel de sectie Vragenlijsten om.</span><span class="sxs-lookup"><span data-stu-id="92ede-149">Toggle the expansion of the Questionnaires section.</span></span>
    * <span data-ttu-id="92ede-150">Met dit tabblad kunt u vragenlijsten toevoegen die op de bestelaanvraag worden weergegeven, zolang u het activiteittype instelt op 'Bestelaanvraag'.</span><span class="sxs-lookup"><span data-stu-id="92ede-150">This tab allows you to add questionnaires that will appear on the requisition, as long as you set the Activity type to "Requisition".</span></span> <span data-ttu-id="92ede-151">De aanvrager moet vervolgens een vragenlijst invullen voordat hij of zij een aanvraag voor het specifieke producten of producten in de aanschaffingscategorie kan indienen.</span><span class="sxs-lookup"><span data-stu-id="92ede-151">The requester then has to fill out a questionnaire before they submit a requisition for the specific product or products in the procurement category.</span></span>  
3. <span data-ttu-id="92ede-152">Schakel de uitbreiding van de sectie Btw-groepen voor artikel om.</span><span class="sxs-lookup"><span data-stu-id="92ede-152">Toggle the expansion of the Item sales tax groups section.</span></span>
4. <span data-ttu-id="92ede-153">Klik in het veld Btw-groep voor artikel: op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="92ede-153">In the Item sales tax group: field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="92ede-154">Een btw-groep selecteren.</span><span class="sxs-lookup"><span data-stu-id="92ede-154">Select a sales tax group.</span></span>
6. <span data-ttu-id="92ede-155">Schakel de uitbreiding van de sectie Categoriepagina om.</span><span class="sxs-lookup"><span data-stu-id="92ede-155">Toggle the expansion of the Category page section.</span></span>
    * <span data-ttu-id="92ede-156">Categoriepagina's worden gemaakt op de pagina Categoriehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="92ede-156">Category pages are created in the Category hierarchy page.</span></span> <span data-ttu-id="92ede-157">Ze bevatten informatie over de aanschaffingscategorie, zoals informatie over het type producten in een categorie, afbeeldingen van producten in een categorie of aankondigingen, zoals de verkoopkortingen die beschikbaar zijn in een categorie.</span><span class="sxs-lookup"><span data-stu-id="92ede-157">They contain information about the procurement category such as information about the type of products in a category, images of products in a category, or announcements such as the discounts that are available in a category.</span></span> <span data-ttu-id="92ede-158">De informatie op een categoriepagina wordt weergegeven in bestelaanvragen.</span><span class="sxs-lookup"><span data-stu-id="92ede-158">The information in a category page is displayed on purchase requisitions.</span></span>  
7. <span data-ttu-id="92ede-159">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="92ede-159">Close the page.</span></span>


