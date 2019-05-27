---
title: Een hiërarchie van aanschaffingscategorieën instellen
description: Deze procedure laat zien hoe u nieuwe knooppunten in een hiërarchie van aanschaffingscategorieën maakt en hoe u een aanschaffingscategorie configureert die in een aanschaffingsproces moet worden gebruikt.
author: mkirknel
manager: AnnBe
ms.date: 11/06/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 01809a8a3256342682d8a9cfb296a355310fe4ed
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569886"
---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="3303a-103">Een hiërarchie van aanschaffingscategorieën instellen</span><span class="sxs-lookup"><span data-stu-id="3303a-103">Set up a procurement category hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3303a-104">Deze procedure laat zien hoe u nieuwe knooppunten in een hiërarchie van aanschaffingscategorieën maakt en hoe u een aanschaffingscategorie configureert die in een aanschaffingsproces moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="3303a-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="3303a-105">Deze taken worden meestal uitgevoerd door een inkoopmanager.</span><span class="sxs-lookup"><span data-stu-id="3303a-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="3303a-106">Voordat u deze procedure kunt starten, moet er een categoriehiërarchie van het type Inkoop zijn.</span><span class="sxs-lookup"><span data-stu-id="3303a-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="3303a-107">Als u een demobedrijf gebruikt, kunt u deze procedure in het bedrijf USMF uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="3303a-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="3303a-108">Een nieuwe inkoopcategorie toevoegen</span><span class="sxs-lookup"><span data-stu-id="3303a-108">Add a new procurement category</span></span>
1. <span data-ttu-id="3303a-109">Ga naar Inkoop en sourcing > Inkoopcategorieën.</span><span class="sxs-lookup"><span data-stu-id="3303a-109">Go to Procurement and sourcing > Procurement categories.</span></span>
2. <span data-ttu-id="3303a-110">Klik op Categoriehiërarchie bewerken.</span><span class="sxs-lookup"><span data-stu-id="3303a-110">Click Edit category hierarchy.</span></span>
    * <span data-ttu-id="3303a-111">De huidige hiërarchie van aanschaffingscategorieën wordt weergegeven aan de linkerkant van de pagina.</span><span class="sxs-lookup"><span data-stu-id="3303a-111">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="3303a-112">U gaat de hiërarchie wijzigen.</span><span class="sxs-lookup"><span data-stu-id="3303a-112">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="3303a-113">Klik op Nieuw categorieknooppunt.</span><span class="sxs-lookup"><span data-stu-id="3303a-113">Click New category node.</span></span>
    * <span data-ttu-id="3303a-114">Het systeem selecteert standaard het bovenste knooppunt.</span><span class="sxs-lookup"><span data-stu-id="3303a-114">The system selects the top node by default.</span></span> <span data-ttu-id="3303a-115">Als u deze procedure als taakbegeleiding uitvoert, kunt u op de knop Ontgrendelen klikken en een ander bovenliggend knooppunt selecteren om uw nieuw knooppunt in te plaatsen.</span><span class="sxs-lookup"><span data-stu-id="3303a-115">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="3303a-116">Zodra dat is gedaan, vergrendelt u de taakbegeleiding opnieuw en klikt u op het categorieknooppunt Nieuw.</span><span class="sxs-lookup"><span data-stu-id="3303a-116">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="3303a-117">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="3303a-117">In the Name field, type a value.</span></span>
5. <span data-ttu-id="3303a-118">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="3303a-118">In the Description field, type a value.</span></span>
6. <span data-ttu-id="3303a-119">Typ een waarde in het veld Beschrijvende naam.</span><span class="sxs-lookup"><span data-stu-id="3303a-119">In the Friendly name field, type a value.</span></span>
    * <span data-ttu-id="3303a-120">De beschrijvende naam is optioneel.</span><span class="sxs-lookup"><span data-stu-id="3303a-120">The friendly name is optional.</span></span> <span data-ttu-id="3303a-121">Deze wordt in categoriezoekopdrachten met de categorienaam weergegeven.</span><span class="sxs-lookup"><span data-stu-id="3303a-121">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="3303a-122">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="3303a-122">Click Save.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="3303a-123">Producten aan uw nieuwe aanschaffingscategorie toevoegen</span><span class="sxs-lookup"><span data-stu-id="3303a-123">Add products to your new procurement category</span></span>
1. <span data-ttu-id="3303a-124">Ga naar Inkoop en sourcing > Inkoopcategorieën.</span><span class="sxs-lookup"><span data-stu-id="3303a-124">Go to Procurement and sourcing > Procurement categories.</span></span>
    * <span data-ttu-id="3303a-125">Selecteer het knooppunt dat u zojuist hebt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="3303a-125">Select the node you just added.</span></span> <span data-ttu-id="3303a-126">Als u de procedure als taakbegeleiding uitvoert, moet u de taakbegeleiding wellicht ontgrendelen om het knooppunt te selecteren.</span><span class="sxs-lookup"><span data-stu-id="3303a-126">If you’re running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="3303a-127">Schakel de uitbreiding van de sectie Producten om.</span><span class="sxs-lookup"><span data-stu-id="3303a-127">Toggle the expansion of the Products section.</span></span>
3. <span data-ttu-id="3303a-128">Klik op Toevoegen om producten te koppelen aan de aanschaffingscategorie.</span><span class="sxs-lookup"><span data-stu-id="3303a-128">Click Add to associate products with the procurement category.</span></span>
4. <span data-ttu-id="3303a-129">Selecteer het product dat u wilt toevoegen aan de aanschaffingscategorie.</span><span class="sxs-lookup"><span data-stu-id="3303a-129">Select the product you want to add to the procurement category.</span></span>
5. <span data-ttu-id="3303a-130">Klik op de pijl om het product te selecteren.</span><span class="sxs-lookup"><span data-stu-id="3303a-130">Click the arrow to select the product.</span></span>
6. <span data-ttu-id="3303a-131">Selecteer een ander product dat u wilt toevoegen aan de aanschaffingscategorie.</span><span class="sxs-lookup"><span data-stu-id="3303a-131">Select another product to add to the procurement category.</span></span>
7. <span data-ttu-id="3303a-132">Klik op de pijl om het product te selecteren.</span><span class="sxs-lookup"><span data-stu-id="3303a-132">Click the arrow to select the product.</span></span>
8. <span data-ttu-id="3303a-133">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="3303a-133">Click OK.</span></span>

## <a name="add-approved-and-preferred-vendors"></a><span data-ttu-id="3303a-134">Goedgekeurde en voorkeursleveranciers toevoegen</span><span class="sxs-lookup"><span data-stu-id="3303a-134">Add approved and preferred vendors</span></span>
1. <span data-ttu-id="3303a-135">Schakel de uitbreiding van de sectie Leveranciers om.</span><span class="sxs-lookup"><span data-stu-id="3303a-135">Toggle the expansion of the Vendors section.</span></span>
2. <span data-ttu-id="3303a-136">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="3303a-136">Click Add.</span></span>
    * <span data-ttu-id="3303a-137">U kunt nu een leverancier aan een aanschaffingscategorie toevoegen en opgeven of een leverancier de voorkeur heeft of alleen is goedgekeurd voor de categorie.</span><span class="sxs-lookup"><span data-stu-id="3303a-137">You can add a vendor to a procurement category and specify whether a vendor is preferred or just approved for the category.</span></span> <span data-ttu-id="3303a-138">Wanneer u een leverancier uit een categorie verwijdert, worden de historische transacties met de leverancier in de categorie niet verwijderd.</span><span class="sxs-lookup"><span data-stu-id="3303a-138">When you delete a vendor from a category, the historical transactions with the vendor in the category are not deleted.</span></span>   
3. <span data-ttu-id="3303a-139">Zoek de leverancier die u wilt toevoegen aan de categorie.</span><span class="sxs-lookup"><span data-stu-id="3303a-139">Find the vendor you want to add to the category.</span></span>
4. <span data-ttu-id="3303a-140">Klik op de pijl om de leverancier te selecteren.</span><span class="sxs-lookup"><span data-stu-id="3303a-140">Click the arrow to select the vendor.</span></span>
5. <span data-ttu-id="3303a-141">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="3303a-141">Click OK.</span></span>
6. <span data-ttu-id="3303a-142">Selecteer op de leveranciersrij die u wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="3303a-142">Select the vendor row that you want to modify.</span></span>
7. <span data-ttu-id="3303a-143">Selecteer een optie in het veld Leveranciersstatus.</span><span class="sxs-lookup"><span data-stu-id="3303a-143">In the Vendor status field, select an option.</span></span>
    * <span data-ttu-id="3303a-144">De instelling van de leverancierselectie in de categoriebeleidsregel bepaalt of favoriete, goedgekeurde of alle leveranciers beschikbaar zijn voor opdrachten tot inkoop.</span><span class="sxs-lookup"><span data-stu-id="3303a-144">The vendor selection setting in the Category policy rule governs whether preferred, approved, or all vendors are available on purchase requisitions.</span></span>   

## <a name="add-additional-information-to-the-category"></a><span data-ttu-id="3303a-145">Extra informatie aan de categorie toevoegen</span><span class="sxs-lookup"><span data-stu-id="3303a-145">Add additional information to the category</span></span>
1. <span data-ttu-id="3303a-146">Schakel de uitbreiding van de sectie Groepen evaluatiecriteria voor leveranciers om.</span><span class="sxs-lookup"><span data-stu-id="3303a-146">Toggle the expansion of the Vendor evaluation criterion groups section.</span></span>
    * <span data-ttu-id="3303a-147">Op dit tabblad kunt u definiëren op basis van welke criteria de leveranciers in de aanschaffingscategorie moeten worden beoordeeld.</span><span class="sxs-lookup"><span data-stu-id="3303a-147">This tab allows you to define which criteria the vendors in the procurement category should be rated against.</span></span> <span data-ttu-id="3303a-148">Om dit te doen moet u klikken op Toevoegen en vervolgens een leverancierevaluatiegroep selecteren die de gewenste criteria bevat.</span><span class="sxs-lookup"><span data-stu-id="3303a-148">To do this you would click Add and then select a vendor evaluation group that contains the criteria you want.</span></span>  
2. <span data-ttu-id="3303a-149">Schakel de sectie Vragenlijsten om.</span><span class="sxs-lookup"><span data-stu-id="3303a-149">Toggle the expansion of the Questionnaires section.</span></span>
    * <span data-ttu-id="3303a-150">Met dit tabblad kunt u vragenlijsten toevoegen die op de bestelaanvraag worden weergegeven, zolang u het activiteittype instelt op 'Bestelaanvraag'.</span><span class="sxs-lookup"><span data-stu-id="3303a-150">This tab allows you to add questionnaires that will appear on the requisition, as long as you set the Activity type to "Requisition".</span></span> <span data-ttu-id="3303a-151">De aanvrager moet vervolgens een vragenlijst invullen voordat hij of zij een aanvraag voor het specifieke producten of producten in de aanschaffingscategorie kan indienen.</span><span class="sxs-lookup"><span data-stu-id="3303a-151">The requester then has to fill out a questionnaire before they submit a requisition for the specific product or products in the procurement category.</span></span>  
3. <span data-ttu-id="3303a-152">Schakel de uitbreiding van de sectie Btw-groepen voor artikel om.</span><span class="sxs-lookup"><span data-stu-id="3303a-152">Toggle the expansion of the Item sales tax groups section.</span></span>
4. <span data-ttu-id="3303a-153">Klik in het veld Btw-groep voor artikel: op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="3303a-153">In the Item sales tax group: field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="3303a-154">Een btw-groep selecteren.</span><span class="sxs-lookup"><span data-stu-id="3303a-154">Select a sales tax group.</span></span>
6. <span data-ttu-id="3303a-155">Schakel de uitbreiding van de sectie Categoriepagina om.</span><span class="sxs-lookup"><span data-stu-id="3303a-155">Toggle the expansion of the Category page section.</span></span>
    * <span data-ttu-id="3303a-156">Categoriepagina's worden gemaakt op de pagina Categoriehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="3303a-156">Category pages are created in the Category hierarchy page.</span></span> <span data-ttu-id="3303a-157">Ze bevatten informatie over de aanschaffingscategorie, zoals informatie over het type producten in een categorie, afbeeldingen van producten in een categorie of aankondigingen, zoals de verkoopkortingen die beschikbaar zijn in een categorie.</span><span class="sxs-lookup"><span data-stu-id="3303a-157">They contain information about the procurement category such as information about the type of products in a category, images of products in a category, or announcements such as the discounts that are available in a category.</span></span> <span data-ttu-id="3303a-158">De informatie op een categoriepagina wordt weergegeven in bestelaanvragen.</span><span class="sxs-lookup"><span data-stu-id="3303a-158">The information in a category page is displayed on purchase requisitions.</span></span>  
7. <span data-ttu-id="3303a-159">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="3303a-159">Close the page.</span></span>

