---
title: Een bestaande activiteit toevoegen aan een productiestroomversie
description: Bij het maken van nieuwe versies van productiestromen, kunt u kiezen om activiteiten die voor de oudere versies zijn gemaakt, aan de nieuwe versie toe te voegen.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityAddExisting, PlanActivityAddExistingLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ff549fd6ed526eefc5514ce2013cc31a700510f8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006936"
---
# <a name="add-an-existing-activity-to-a-production-flow-version"></a><span data-ttu-id="8baf3-103">Een bestaande activiteit toevoegen aan een productiestroomversie</span><span class="sxs-lookup"><span data-stu-id="8baf3-103">Add an existing activity to a production flow version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8baf3-104">Bij het maken van nieuwe versies van productiestromen, kunt u kiezen om activiteiten die voor de oudere versies zijn gemaakt, aan de nieuwe versie toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="8baf3-104">When creating new versions of production flows, you can choose to add activities created for the older versions, to the new version.</span></span> <span data-ttu-id="8baf3-105">Deze procedure laat zien hoe een nieuwe versie voor een bestaande productiestroom wordt gemaakt, zonder de activiteiten te kopiëren.</span><span class="sxs-lookup"><span data-stu-id="8baf3-105">This procedure shows how a new version is created for an existing production flow, without copying the activities.</span></span> <span data-ttu-id="8baf3-106">In de volgende stap wordt een bestaande activiteit toegevoegd aan de nieuwe versie.</span><span class="sxs-lookup"><span data-stu-id="8baf3-106">In the next step, an existing activity is added to the new version.</span></span> 

<span data-ttu-id="8baf3-107">Deze taak vereist dat er al een productiestroom met versie en activiteiten is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="8baf3-107">This task requires production flow with version and activities already created.</span></span>


## <a name="create-a-new-production-flow-version"></a><span data-ttu-id="8baf3-108">Een nieuwe productiestroomversie maken</span><span class="sxs-lookup"><span data-stu-id="8baf3-108">Create a new production flow version</span></span>
1. <span data-ttu-id="8baf3-109">Ga naar Productiebeheer > Instellingen > Lean productiestroom > Productiestromen.</span><span class="sxs-lookup"><span data-stu-id="8baf3-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="8baf3-110">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="8baf3-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="8baf3-111">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="8baf3-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="8baf3-112">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="8baf3-112">Click Edit.</span></span>
5. <span data-ttu-id="8baf3-113">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="8baf3-113">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="8baf3-114">Voer in het veld Vervaldatum een datum en tijd in.</span><span class="sxs-lookup"><span data-stu-id="8baf3-114">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="8baf3-115">Let op dat voordat u een nieuwe productiestroomversie maakt, u de vervaldatum en -tijd van de actieve versie moet controleren.</span><span class="sxs-lookup"><span data-stu-id="8baf3-115">Note that before you create a new production flow version, make sure to check the expiration date and time of the active version.</span></span> <span data-ttu-id="8baf3-116">De nieuwe versie wordt gemaakt met een ingangsdatum, die aan de vervaldatum van de geselecteerde versie is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="8baf3-116">The new version will be created with an effective start date, which connects to the expiry date of the selected version.</span></span>  
7. <span data-ttu-id="8baf3-117">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="8baf3-117">Click Add.</span></span>
8. <span data-ttu-id="8baf3-118">Selecteer Nee in het veld Kopiëren uit versie.</span><span class="sxs-lookup"><span data-stu-id="8baf3-118">Select No in the Copy from version field.</span></span>
    * <span data-ttu-id="8baf3-119">Selecteer Nee om met een lege versie te starten als de meeste activiteiten van de gekopieerde versie door nieuwe activiteiten worden vervangen.</span><span class="sxs-lookup"><span data-stu-id="8baf3-119">Select No to start with an empty version if most of the activities of the copied version will be replaced by new activities.</span></span> <span data-ttu-id="8baf3-120">Voeg de onveranderde activiteiten handmatig toe aan het formulier Bestaande functie toevoegen in de activiteit.</span><span class="sxs-lookup"><span data-stu-id="8baf3-120">Add the unchanged activities to the Add existing function in the activity form manually.</span></span>  
9. <span data-ttu-id="8baf3-121">Selecteer Nee in het veld Dubbele kanbanregels.</span><span class="sxs-lookup"><span data-stu-id="8baf3-121">Select No in the Duplicate kanban rules field.</span></span>
    * <span data-ttu-id="8baf3-122">Wanneer de activiteiten niet naar de nieuwe versie worden gekopieerd, is het niet mogelijk om de kanbanregels op het moment van aanmaken van de nieuwe versie te kopiëren.</span><span class="sxs-lookup"><span data-stu-id="8baf3-122">When the activities are not copied to the new version, it is not possible to copy the kanban rules at the time of creation of the new version.</span></span>   <span data-ttu-id="8baf3-123">In plaats daarvan gebruikt u de functie om later een vervangende kanban te maken in het kanbanregelformulier om kanbanregels van de oude productiestroomversie te vervangen door kanbanregels met de activiteiten van de nieuwe versie.</span><span class="sxs-lookup"><span data-stu-id="8baf3-123">Instead you will use the create replacement kanban function later in the kanban rule form, to replace kanban rules of the old production flow version with kanban rules using the activities of the new version.</span></span>  
10. <span data-ttu-id="8baf3-124">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="8baf3-124">Click OK.</span></span>
11. <span data-ttu-id="8baf3-125">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="8baf3-125">In the list, find and select the desired record.</span></span>

## <a name="add-an-existing-activity"></a><span data-ttu-id="8baf3-126">Een bestaande activiteit toevoegen</span><span class="sxs-lookup"><span data-stu-id="8baf3-126">Add an existing activity</span></span>
1. <span data-ttu-id="8baf3-127">Klik op Activiteiten.</span><span class="sxs-lookup"><span data-stu-id="8baf3-127">Click Activities.</span></span>
2. <span data-ttu-id="8baf3-128">Klik op Bestaand toevoegen om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="8baf3-128">Click Add existing to open the drop dialog.</span></span>
    * <span data-ttu-id="8baf3-129">Zoek en selecteer een bestaande activiteit die moet worden toegevoegd aan de nieuwe productiestroomversie.</span><span class="sxs-lookup"><span data-stu-id="8baf3-129">Find and select an existing activity to be added to the new production flow version.</span></span>  <span data-ttu-id="8baf3-130">Merk op dat de lijst alle activiteiten weergeeft die voor deze productiestroom zijn gemaakt voor alle vorige versies van de stroom.</span><span class="sxs-lookup"><span data-stu-id="8baf3-130">Note that the list shows all activities that have been created for this production flow for all previous versions of the flow.</span></span>  
3. <span data-ttu-id="8baf3-131">Typ of selecteer een waarde in het veld Activiteit.</span><span class="sxs-lookup"><span data-stu-id="8baf3-131">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="8baf3-132">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="8baf3-132">Click OK.</span></span>

