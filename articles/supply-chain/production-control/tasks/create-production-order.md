---
title: Een productieorder maken
description: Deze procedure laat zien hoe u een productieorder maakt.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdTable, ProdBOM, ProdRoute, ProdJournalCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 81caa6693d86c797d8565270094556ae4e103e6a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998673"
---
# <a name="create-a-production-order"></a><span data-ttu-id="9b45d-103">Een productieorder maken</span><span class="sxs-lookup"><span data-stu-id="9b45d-103">Create a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9b45d-104">Deze procedure laat zien hoe u een productieorder maakt.</span><span class="sxs-lookup"><span data-stu-id="9b45d-104">This procedure shows how to create a production order.</span></span> <span data-ttu-id="9b45d-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="9b45d-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="9b45d-106">Dit is de eerste procedure van zeven die de productieorderlevenscyclus beschrijven.</span><span class="sxs-lookup"><span data-stu-id="9b45d-106">This is the first procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="9b45d-107">Een productieorder maken</span><span class="sxs-lookup"><span data-stu-id="9b45d-107">Create a production order</span></span>
1. <span data-ttu-id="9b45d-108">Ga naar Productiebeheer > Productieorders > Alle productieorders.</span><span class="sxs-lookup"><span data-stu-id="9b45d-108">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="9b45d-109">Klik op Nieuwe productieorder.</span><span class="sxs-lookup"><span data-stu-id="9b45d-109">Click New production order.</span></span>
3. <span data-ttu-id="9b45d-110">Typ in het veld Artikelnummer de waarde 'D0001'.</span><span class="sxs-lookup"><span data-stu-id="9b45d-110">In the Item number field, type 'D0001'.</span></span>
4. <span data-ttu-id="9b45d-111">Geef een datum op in het veld Levering.</span><span class="sxs-lookup"><span data-stu-id="9b45d-111">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="9b45d-112">De leveringsdatum geeft aan wanneer de productieorder moet eindigen om op tijd te leveren.</span><span class="sxs-lookup"><span data-stu-id="9b45d-112">The delivery date indicates when the production order should end in order to deliver on time.</span></span> <span data-ttu-id="9b45d-113">Deze datum kan in het planningsproces worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="9b45d-113">This date can be used in the scheduling process.</span></span> <span data-ttu-id="9b45d-114">Bijvoorbeeld: u kunt de order terug in de tijd plannen vanaf de leveringsdatum.</span><span class="sxs-lookup"><span data-stu-id="9b45d-114">For example, you can schedule the order backward from the delivery date.</span></span>  
5. <span data-ttu-id="9b45d-115">Stel Hoeveelheid in op '20'.</span><span class="sxs-lookup"><span data-stu-id="9b45d-115">Set Quantity to '20'.</span></span>
    * <span data-ttu-id="9b45d-116">Opmerking: Het veld voor het stuklijstnummer bevat automatisch het nummer van een actieve stuklijst voor het huidige artikel, maar u kunt de stuklijst voor de productieorder wijzigen door een actieve stuklijst in de lijst met goedgekeurde stuklijstversies te selecteren.</span><span class="sxs-lookup"><span data-stu-id="9b45d-116">Note: The BOM number field automatically displays the number of any active BOM for the current item, but you can change the BOM for the production order by selecting an active BOM from the list of approved BOM versions.</span></span>    <span data-ttu-id="9b45d-117">Het veld voor het routenummer bevat automatisch het nummer van een actieve route voor het huidige artikel, maar u kunt de route voor de productieorder wijzigen door een actieve route in de lijst met goedgekeurde routeversies te selecteren.</span><span class="sxs-lookup"><span data-stu-id="9b45d-117">The Route number field automatically displays the number of any active Route for the current item, but you can change the Route for the production order by selecting an active Route from the list of approved Route versions.</span></span>  
6. <span data-ttu-id="9b45d-118">Klik op Maken.</span><span class="sxs-lookup"><span data-stu-id="9b45d-118">Click Create.</span></span>

## <a name="validate-the-production-order"></a><span data-ttu-id="9b45d-119">De productieorder valideren</span><span class="sxs-lookup"><span data-stu-id="9b45d-119">Validate the production order</span></span>
1. <span data-ttu-id="9b45d-120">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="9b45d-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9b45d-121">Klik op de koppeling voor het productieordernummer dat u zojuist hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="9b45d-121">Click the link for the production order number that you have just created.</span></span> <span data-ttu-id="9b45d-122">Hiermee wordt de detailspagina voor de order geopend.</span><span class="sxs-lookup"><span data-stu-id="9b45d-122">This will open the details page for the order.</span></span>  
2. <span data-ttu-id="9b45d-123">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="9b45d-123">Click Edit.</span></span>
3. <span data-ttu-id="9b45d-124">Geef een datum op in het veld Levering.</span><span class="sxs-lookup"><span data-stu-id="9b45d-124">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="9b45d-125">Bijvoorbeeld: u kunt de leveringsdatum voor de productieorder wijzigen.</span><span class="sxs-lookup"><span data-stu-id="9b45d-125">For example, you can change the delivery date for the production order.</span></span>  
4. <span data-ttu-id="9b45d-126">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="9b45d-126">Click Save.</span></span>
5. <span data-ttu-id="9b45d-127">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="9b45d-127">Close the page.</span></span>

## <a name="update-the-bom"></a><span data-ttu-id="9b45d-128">De stuklijst bijwerken</span><span class="sxs-lookup"><span data-stu-id="9b45d-128">Update the BOM</span></span>
1. <span data-ttu-id="9b45d-129">Klik in het actievenster op Productieorder.</span><span class="sxs-lookup"><span data-stu-id="9b45d-129">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="9b45d-130">Klik op Stuklijst.</span><span class="sxs-lookup"><span data-stu-id="9b45d-130">Click BOM.</span></span>
    * <span data-ttu-id="9b45d-131">Open de stuklijstpagina om de stuklijstgegevens te valideren die van de standaardgegevens zijn gekopieerd toen de productieorder werd gemaakt.</span><span class="sxs-lookup"><span data-stu-id="9b45d-131">Open the BOM page to validate the BOM data that was copied from the default data when the production order was created.</span></span> <span data-ttu-id="9b45d-132">In deze procedure moet u de hoeveelheid voor een stuklijst bijwerken.</span><span class="sxs-lookup"><span data-stu-id="9b45d-132">In this procedure, you need to update the quantity for a BOM.</span></span>  
3. <span data-ttu-id="9b45d-133">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="9b45d-133">Click Edit.</span></span>
4. <span data-ttu-id="9b45d-134">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="9b45d-134">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="9b45d-135">Het wijzigen van de hoeveelheid op de stuklijstregel is van invloed op de kostenraming van materiaalverbruik voor de productieorder.</span><span class="sxs-lookup"><span data-stu-id="9b45d-135">Changing the quantity on the BOM line affects the cost estimate of material consumption for the production order.</span></span>  
5. <span data-ttu-id="9b45d-136">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="9b45d-136">Click Save.</span></span>
6. <span data-ttu-id="9b45d-137">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="9b45d-137">Close the page.</span></span>

## <a name="update-the-production-route"></a><span data-ttu-id="9b45d-138">De productieroute bijwerken</span><span class="sxs-lookup"><span data-stu-id="9b45d-138">Update the production route</span></span>
1. <span data-ttu-id="9b45d-139">Klik in het actievenster op Productieorder.</span><span class="sxs-lookup"><span data-stu-id="9b45d-139">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="9b45d-140">Klik op Route.</span><span class="sxs-lookup"><span data-stu-id="9b45d-140">Click Route.</span></span>
    * <span data-ttu-id="9b45d-141">Open de routepagina om de gegevens van de productieroute te valideren die van de standaardgegevens zijn gekopieerd toen de order werd gemaakt.</span><span class="sxs-lookup"><span data-stu-id="9b45d-141">Open the Route page to validate the data of the production route that was copied from the default data when the order was created.</span></span> <span data-ttu-id="9b45d-142">In deze procedure moet u de hoeveelheid voor een van de bewerkingen in de productieroute bijwerken.</span><span class="sxs-lookup"><span data-stu-id="9b45d-142">In this procedure, you need to update the quantity for one of the operations in the production route.</span></span>  
3. <span data-ttu-id="9b45d-143">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="9b45d-143">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="9b45d-144">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="9b45d-144">Click Edit.</span></span>
5. <span data-ttu-id="9b45d-145">Voer in het veld Verwerkingshoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="9b45d-145">In the Process qty. field, enter a number.</span></span>
    * <span data-ttu-id="9b45d-146">Het wijzigen van de verwerkingstijd is van invloed op het geraamde routeverbruik en de kosten van de productieorder.</span><span class="sxs-lookup"><span data-stu-id="9b45d-146">Changing the process time affects the estimated route consumption and the cost of the production order.</span></span>  
6. <span data-ttu-id="9b45d-147">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="9b45d-147">Click Save.</span></span>
7. <span data-ttu-id="9b45d-148">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="9b45d-148">Close the page.</span></span>

