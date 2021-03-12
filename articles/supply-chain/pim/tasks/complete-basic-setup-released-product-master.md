---
title: Basisinstellingen voor een vrijgegeven productmodel voltooien
description: In dit onderwerp ziet u hoe u de minimuminstelling voltooit die is vereist voordat het productmodel in stuklijstversies kan worden gebruikt.
author: ShylaThompson
manager: tfehr
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 668b60efa55fa553cf308d5bfc5da7e23f460366
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987024"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="916d8-103">Basisinstellingen voor een vrijgegeven productmodel voltooien</span><span class="sxs-lookup"><span data-stu-id="916d8-103">Complete basic setup of a released product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="916d8-104">In dit onderwerp ziet u hoe u de minimuminstelling voltooit die is vereist voordat het productmodel in stuklijstversies kan worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="916d8-104">This topic shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="916d8-105">Dit is de derde van acht procedures waarin wordt uitgelegd hoe u combinaties maakt voor een op dimensies gebaseerde configuratie.</span><span class="sxs-lookup"><span data-stu-id="916d8-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="916d8-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="916d8-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="916d8-107">Ga naar **Navigatievenster > Modules > Productgegevensbeheer > Producten > Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="916d8-107">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="916d8-108">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="916d8-108">In the list, find and select the desired record.</span></span> <span data-ttu-id="916d8-109">Selecteer het productmodel dat u in de tweede procedure hebt vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="916d8-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="916d8-110">Dit productmodel wordt gemaakt met de op dimensies gebaseerde configuratietechnologie.</span><span class="sxs-lookup"><span data-stu-id="916d8-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="916d8-111">Selecteer **Product** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="916d8-111">On the Action Pane, select **Product**.</span></span>
4. <span data-ttu-id="916d8-112">Selecteer **Dimensiegroepen** om het uitklapvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="916d8-112">Select **Dimension groups** to open the drop dialog.</span></span>
5. <span data-ttu-id="916d8-113">Selecteer in het veld **Opslagdimensiegroep** de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="916d8-113">In the **Storage dimension group** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="916d8-114">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="916d8-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="916d8-115">De opslagdimensiegroep bepaalt welke opslagdimensies voor de producttransactie worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="916d8-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="916d8-116">Selecteer **Vestiging** voor deze procedure.</span><span class="sxs-lookup"><span data-stu-id="916d8-116">Select **Site** for this procedure.</span></span>  
7. <span data-ttu-id="916d8-117">Selecteer in het veld **Traceringsdimensiegroep** de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="916d8-117">In the **Tracking dimension group** field, select the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="916d8-118">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="916d8-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="916d8-119">De trackingdimensiegroep bepaalt welke trackingdimensies voor de producttransactie worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="916d8-119">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="916d8-120">Selecteer **Geen** voor deze procedure.</span><span class="sxs-lookup"><span data-stu-id="916d8-120">Select **None** for this procedure.</span></span>  
9. <span data-ttu-id="916d8-121">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="916d8-121">Click **OK**.</span></span>
10. <span data-ttu-id="916d8-122">Klik op **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="916d8-122">Click **Edit**.</span></span>
11. <span data-ttu-id="916d8-123">Selecteer in het veld **Artikelmodelgroep** de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="916d8-123">In the **Item model group** field, select the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="916d8-124">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="916d8-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="916d8-125">Artikelmodelgroepen bevatten instellingen waarmee wordt bepaald hoe artikelen worden beheerd en verwerkt op artikelontvangsten en artikeluitgiften.</span><span class="sxs-lookup"><span data-stu-id="916d8-125">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="916d8-126">Hiermee wordt ook bepaald hoe het artikelverbruik wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="916d8-126">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="916d8-127">Selecteer **FIFO** voor deze procedure.</span><span class="sxs-lookup"><span data-stu-id="916d8-127">Select **FIFO** for this procedure.</span></span>  
13. <span data-ttu-id="916d8-128">Vouw de sectie **Kosten beheren** uit.</span><span class="sxs-lookup"><span data-stu-id="916d8-128">Expand the **Manage costs** section.</span></span>
14. <span data-ttu-id="916d8-129">Selecteer in het veld **Artikelgroep** de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="916d8-129">In the **Item group** field, select the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="916d8-130">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="916d8-130">In the list, find and select the desired record.</span></span> <span data-ttu-id="916d8-131">Artikelengroepen worden gebruikt voor het beheren van de voorraad door de voorraadartikelen in groepen te verdelen.</span><span class="sxs-lookup"><span data-stu-id="916d8-131">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="916d8-132">Selecteer **CarAudio** voor deze procedure.</span><span class="sxs-lookup"><span data-stu-id="916d8-132">Select **CarAudio** for this procedure.</span></span>  
16. <span data-ttu-id="916d8-133">Selecteer **Plan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="916d8-133">On the Action Pane, select **Plan**.</span></span>
17. <span data-ttu-id="916d8-134">Standaard **Standaardorderinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="916d8-134">Select **Default order settings**.</span></span>
18. <span data-ttu-id="916d8-135">Selecteer een optie in het veld **Standaardordertype**.</span><span class="sxs-lookup"><span data-stu-id="916d8-135">In the **Default order type field**, select an option.</span></span> <span data-ttu-id="916d8-136">Selecteer **Productie** om op te geven dat de standaardleveringsoptie voor dit productmodel is om het te produceren.</span><span class="sxs-lookup"><span data-stu-id="916d8-136">Select **Production** to specify that the default supply option for this product master is to produce it.</span></span>  
19. <span data-ttu-id="916d8-137">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="916d8-137">Select **Save**.</span></span>
20. <span data-ttu-id="916d8-138">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="916d8-138">Close the page.</span></span>
21. <span data-ttu-id="916d8-139">Sluit het formulier **Vrijgegeven productdetails**.</span><span class="sxs-lookup"><span data-stu-id="916d8-139">Close the **Released product details** form.</span></span>

