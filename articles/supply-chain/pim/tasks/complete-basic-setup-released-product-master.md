---
title: Basisinstellingen voor een vrijgegeven productmodel voltooien
description: Deze procedure laat zien hoe u de minimuminstelling voltooit die is vereist voordat het productmodel in stuklijstversies kan worden gebruikt.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d3a91977c38c0ce0f9fe114bec943c7cb32a5d4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568761"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="96ad8-103">Basisinstellingen voor een vrijgegeven productmodel voltooien</span><span class="sxs-lookup"><span data-stu-id="96ad8-103">Complete basic setup of a released product master</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="96ad8-104">Deze procedure laat zien hoe u de minimuminstelling voltooit die is vereist voordat het productmodel in stuklijstversies kan worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="96ad8-104">This procedure shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="96ad8-105">Dit is de derde van acht procedures waarin wordt uitgelegd hoe u combinaties maakt voor een op dimensies gebaseerde configuratie.</span><span class="sxs-lookup"><span data-stu-id="96ad8-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="96ad8-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="96ad8-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="96ad8-107">Ga naar Productgegevensbeheer > Producten > Vrijgegeven producten.</span><span class="sxs-lookup"><span data-stu-id="96ad8-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="96ad8-108">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="96ad8-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="96ad8-109">Selecteer het productmodel dat u in de tweede procedure hebt vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="96ad8-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="96ad8-110">Dit productmodel wordt gemaakt met de op dimensies gebaseerde configuratietechnologie.</span><span class="sxs-lookup"><span data-stu-id="96ad8-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="96ad8-111">Klik in het actievenster op Product.</span><span class="sxs-lookup"><span data-stu-id="96ad8-111">On the Action Pane, click Product.</span></span>
4. <span data-ttu-id="96ad8-112">Klik op Dimensiegroepen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="96ad8-112">Click Dimension groups to open the drop dialog.</span></span>
5. <span data-ttu-id="96ad8-113">Klik in het veld Opslagdimensiegroep op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="96ad8-113">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="96ad8-114">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="96ad8-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="96ad8-115">De opslagdimensiegroep bepaalt welke opslagdimensies voor de producttransactie worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="96ad8-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="96ad8-116">Selecteer Locatie voor deze procedure.</span><span class="sxs-lookup"><span data-stu-id="96ad8-116">Select Site for this procedure.</span></span>  
7. <span data-ttu-id="96ad8-117">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="96ad8-117">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="96ad8-118">Klik in het veld Traceringsdimensiegroep op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="96ad8-118">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="96ad8-119">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="96ad8-119">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="96ad8-120">De trackingdimensiegroep bepaalt welke trackingdimensies voor de producttransactie worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="96ad8-120">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="96ad8-121">Selecteer Geen voor deze procedure.</span><span class="sxs-lookup"><span data-stu-id="96ad8-121">Select None for this procedure.</span></span>  
10. <span data-ttu-id="96ad8-122">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="96ad8-122">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="96ad8-123">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="96ad8-123">Click OK.</span></span>
12. <span data-ttu-id="96ad8-124">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="96ad8-124">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="96ad8-125">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="96ad8-125">Click Edit.</span></span>
    * <span data-ttu-id="96ad8-126">Open het formulier Vrijgegeven productdetails om door te gaan met de instellingstaak.</span><span class="sxs-lookup"><span data-stu-id="96ad8-126">Open the Released product details form to continue the setup task.</span></span>  
14. <span data-ttu-id="96ad8-127">Klik in het veld Artikelmodelgroep op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="96ad8-127">In the Item model group field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="96ad8-128">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="96ad8-128">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="96ad8-129">Artikelmodelgroepen bevatten instellingen waarmee wordt bepaald hoe artikelen worden beheerd en verwerkt op artikelontvangsten en artikeluitgiften.</span><span class="sxs-lookup"><span data-stu-id="96ad8-129">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="96ad8-130">Hiermee wordt ook bepaald hoe het artikelverbruik wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="96ad8-130">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="96ad8-131">Selecteer FIFO voor deze procedure.</span><span class="sxs-lookup"><span data-stu-id="96ad8-131">Select   FIFO for this procedure.</span></span>  
16. <span data-ttu-id="96ad8-132">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="96ad8-132">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="96ad8-133">Vouw de sectie Kosten beheren uit of samen.</span><span class="sxs-lookup"><span data-stu-id="96ad8-133">Expand or collapse the Manage costs section.</span></span>
18. <span data-ttu-id="96ad8-134">Klik in het veld Artikelgroep op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="96ad8-134">In the Item group field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="96ad8-135">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="96ad8-135">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="96ad8-136">Artikelengroepen worden gebruikt voor het beheren van de voorraad door de voorraadartikelen in groepen te verdelen.</span><span class="sxs-lookup"><span data-stu-id="96ad8-136">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="96ad8-137">Selecteer CarAudio voor deze procedure.</span><span class="sxs-lookup"><span data-stu-id="96ad8-137">Select   CarAudio for this procedure.</span></span>  
20. <span data-ttu-id="96ad8-138">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="96ad8-138">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="96ad8-139">Klik in het actievenster op Plannen.</span><span class="sxs-lookup"><span data-stu-id="96ad8-139">On the Action Pane, click Plan.</span></span>
22. <span data-ttu-id="96ad8-140">Klik op Standaardorderinstellingen.</span><span class="sxs-lookup"><span data-stu-id="96ad8-140">Click Default order settings.</span></span>
23. <span data-ttu-id="96ad8-141">Selecteer een optie in het veld Standaardordertype.</span><span class="sxs-lookup"><span data-stu-id="96ad8-141">In the Default order type field, select an option.</span></span>
    * <span data-ttu-id="96ad8-142">Selecteer Productie om op te geven dat de standaardleveringsoptie voor dit productmodel is om het te produceren.</span><span class="sxs-lookup"><span data-stu-id="96ad8-142">Select Production to specify that the default supply option for this product master is to produce it.</span></span>  
24. <span data-ttu-id="96ad8-143">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="96ad8-143">Close the page.</span></span>
25. <span data-ttu-id="96ad8-144">Sluit het formulier Vrijgegeven productdetails.</span><span class="sxs-lookup"><span data-stu-id="96ad8-144">Close the Released product details form.</span></span>

