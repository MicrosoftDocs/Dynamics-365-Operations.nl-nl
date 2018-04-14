--- 
title: Een productmodel maken
description: Maak een productmodel voor de vooraf gedefinieerde varianten.
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 1cf621b0fad72ad8785a0c9cb35fbf1964ee3b0d
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-product-master"></a><span data-ttu-id="c5722-103">Een productmodel maken</span><span class="sxs-lookup"><span data-stu-id="c5722-103">Create a product master</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c5722-104">Maak een productmodel voor de vooraf gedefinieerde varianten.</span><span class="sxs-lookup"><span data-stu-id="c5722-104">Create a product master for the predefined variants.</span></span> <span data-ttu-id="c5722-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="c5722-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="c5722-106">Deze procedure is bedoeld voor de productontwerper.</span><span class="sxs-lookup"><span data-stu-id="c5722-106">This procedure is intended for the product designer.</span></span>


## <a name="create-a-new-product-master"></a><span data-ttu-id="c5722-107">Een nieuw productmodel maken</span><span class="sxs-lookup"><span data-stu-id="c5722-107">Create a new product master</span></span>
1. <span data-ttu-id="c5722-108">Ga naar Productgegevensbeheer > Producten > Productmodellen.</span><span class="sxs-lookup"><span data-stu-id="c5722-108">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="c5722-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="c5722-109">Click New.</span></span>
3. <span data-ttu-id="c5722-110">Typ een waarde in het veld Productnummer.</span><span class="sxs-lookup"><span data-stu-id="c5722-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="c5722-111">Het nummer moet uniek zijn.</span><span class="sxs-lookup"><span data-stu-id="c5722-111">The number must be unique.</span></span> <span data-ttu-id="c5722-112">Er kan een nummerreeks worden ingesteld voor het veld Productnummer.</span><span class="sxs-lookup"><span data-stu-id="c5722-112">A number sequence can be set for the Product number field.</span></span> <span data-ttu-id="c5722-113">In dit geval hoeft de gebruiker geen waarde in te voeren.</span><span class="sxs-lookup"><span data-stu-id="c5722-113">In this case, the user doesn't have to enter a value.</span></span>  
4. <span data-ttu-id="c5722-114">Typ een waarde in het veld Productnaam.</span><span class="sxs-lookup"><span data-stu-id="c5722-114">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="c5722-115">Voer een omschrijvende naam van het product in.</span><span class="sxs-lookup"><span data-stu-id="c5722-115">Enter a descriptive product name.</span></span> <span data-ttu-id="c5722-116">Voor de waarde wordt standaard de zoeknaam gebruikt, maar deze kan door de gebruiker worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="c5722-116">The value defaults to the search name, but this can be changed by the user.</span></span>  
5. <span data-ttu-id="c5722-117">Klik in het veld Productdimensiegroep op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c5722-117">In the Product dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c5722-118">De productdimensiegroep bepaalt van de 4 productdimensies kunnen worden gebruikt voor het maken van productvarianten.</span><span class="sxs-lookup"><span data-stu-id="c5722-118">The product dimension group determines which of the 4 product dimensions that can be used to create product variants.</span></span> <span data-ttu-id="c5722-119">In dit voorbeeld wordt een groep met kleur en maat gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c5722-119">This example uses a group with color and size.</span></span>  
6. <span data-ttu-id="c5722-120">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="c5722-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="c5722-121">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c5722-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c5722-122">De standaard configuratietechnologie is Vooraf gedefinieerde variant.</span><span class="sxs-lookup"><span data-stu-id="c5722-122">The default configuration technology is Predefined variant.</span></span> <span data-ttu-id="c5722-123">Deze wordt gebruikt voor dit voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="c5722-123">This will be used for this example.</span></span>  
8. <span data-ttu-id="c5722-124">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c5722-124">Click OK.</span></span>

## <a name="select-product-dimension-groups"></a><span data-ttu-id="c5722-125">Productdimensiegroepen selecteren</span><span class="sxs-lookup"><span data-stu-id="c5722-125">Select product dimension groups</span></span>
1. <span data-ttu-id="c5722-126">Klik in het veld Kleurgroep op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c5722-126">In the Color group field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="c5722-127">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="c5722-127">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c5722-128">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c5722-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c5722-129">Klik in het veld Formaatgroep op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c5722-129">In the Size group field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="c5722-130">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="c5722-130">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="c5722-131">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c5722-131">In the list, click the link in the selected row.</span></span>

## <a name="add-dimension-groups"></a><span data-ttu-id="c5722-132">Dimensiegroepen toevoegen</span><span class="sxs-lookup"><span data-stu-id="c5722-132">Add dimension groups</span></span>
1. <span data-ttu-id="c5722-133">Klik in het actievenster op Product.</span><span class="sxs-lookup"><span data-stu-id="c5722-133">On the Action Pane, click Product.</span></span>
2. <span data-ttu-id="c5722-134">Klik op Dimensiegroepen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="c5722-134">Click Dimension groups to open the drop dialog.</span></span>
3. <span data-ttu-id="c5722-135">Klik in het veld Opslagdimensiegroep op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c5722-135">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c5722-136">De opslagdimensies helpen u bij het beheer over de opslag en het verwijderen van artikelen in de voorraad.</span><span class="sxs-lookup"><span data-stu-id="c5722-136">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="c5722-137">Zo kan bijvoorbeeld een opslagdimensie Locatie en Magazijn bevatten.</span><span class="sxs-lookup"><span data-stu-id="c5722-137">For example, a storage dimension can include Site and Warehouse.</span></span>  
4. <span data-ttu-id="c5722-138">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="c5722-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="c5722-139">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c5722-139">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="c5722-140">Klik in het veld Traceringsdimensiegroep op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c5722-140">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c5722-141">De traceringsdimensiegroep bepaalt welke traceringsdimensies u kunt toevoegen aan een product.</span><span class="sxs-lookup"><span data-stu-id="c5722-141">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="c5722-142">Het batchnummer en serienummer worden bijvoorbeeld gebruikt om voorraadartikelen te traceren.</span><span class="sxs-lookup"><span data-stu-id="c5722-142">For example, the batch number and serial number are used to track inventory items.</span></span>  
7. <span data-ttu-id="c5722-143">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="c5722-143">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="c5722-144">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c5722-144">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="c5722-145">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c5722-145">Click OK.</span></span>
10. <span data-ttu-id="c5722-146">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="c5722-146">Click Save.</span></span>
11. <span data-ttu-id="c5722-147">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="c5722-147">Close the page.</span></span>


