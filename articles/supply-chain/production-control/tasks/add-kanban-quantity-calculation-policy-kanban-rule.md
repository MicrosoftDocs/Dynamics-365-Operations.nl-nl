---
title: Een kanbanberekeningsbeleid aan een kanbanregel toevoegen
description: Deze procedure is gericht op het maken van een beleid voor berekening van de kanbanhoeveelheid en het toevoegen hiervan aan een kanbanregel om de grootte en hoeveelheden van de kanban te optimaliseren.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanQuantityPolicy, KanbanRules
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fffd623104dc403e230128c9234521ad1e39c7bb
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568323"
---
# <a name="add-a-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="d2642-103">Een kanbanberekeningsbeleid aan een kanbanregel toevoegen</span><span class="sxs-lookup"><span data-stu-id="d2642-103">Add a kanban quantity calculation policy to a kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d2642-104">Deze procedure is gericht op het maken van een beleid voor berekening van de kanbanhoeveelheid en het toevoegen hiervan aan een kanbanregel om de grootte en hoeveelheden van de kanban te optimaliseren.</span><span class="sxs-lookup"><span data-stu-id="d2642-104">This procedure focuses on creating a kanban quantity calculation policy and adding it to a kanban rule to optimize the kanban size and quantities.</span></span> <span data-ttu-id="d2642-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="d2642-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="d2642-106">Deze procedure is bedoeld voor de waardestroombeheerder.</span><span class="sxs-lookup"><span data-stu-id="d2642-106">This procedure is intended for the value stream manager.</span></span> <span data-ttu-id="d2642-107">Deze procedure is een vereiste voor het maken van de procedure Suggesties voor kanbanhoeveelheid berekenen.</span><span class="sxs-lookup"><span data-stu-id="d2642-107">This procedure is a prerequisite for creating the procedure Calculate kanban quantity suggestions.</span></span> 


## <a name="create-a-kanban-quantity-calculation-policy"></a><span data-ttu-id="d2642-108">Een beleid voor het berekenen van de kanbanhoeveelheid maken</span><span class="sxs-lookup"><span data-stu-id="d2642-108">Create a kanban quantity calculation policy</span></span>
1. <span data-ttu-id="d2642-109">Ga naar Productiebeheer > Periodieke taken > Berekening kanbanhoeveelheid > Beleid voor berekenen kanbanhoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="d2642-109">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban quantity calculation policies.</span></span>
2. <span data-ttu-id="d2642-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="d2642-110">Click New.</span></span>
3. <span data-ttu-id="d2642-111">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="d2642-111">In the Name field, type a value.</span></span>
    * <span data-ttu-id="d2642-112">Typ bijvoorbeeld Speaker2016.</span><span class="sxs-lookup"><span data-stu-id="d2642-112">For example, type Speaker2016.</span></span>  
4. <span data-ttu-id="d2642-113">Klik in het veld Hoofdplan op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="d2642-113">In the Master plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="d2642-114">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="d2642-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d2642-115">Selecteer StaticPlan om de vraag te berekenen.</span><span class="sxs-lookup"><span data-stu-id="d2642-115">Select StaticPlan to calculate demand.</span></span>  
6. <span data-ttu-id="d2642-116">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="d2642-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="d2642-117">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="d2642-117">Click Save.</span></span>
8. <span data-ttu-id="d2642-118">Voer in het veld Minimale kanbanhoeveelheid "1" in.</span><span class="sxs-lookup"><span data-stu-id="d2642-118">In the Minimum kanban quantity field, enter '1'.</span></span>
    * <span data-ttu-id="d2642-119">Dit is het aanvullende aantal kanbans dat in de berekening van kanbanhoeveelheid is opgenomen.</span><span class="sxs-lookup"><span data-stu-id="d2642-119">This is the additional number of kanbans that is included in the kanban quantity calculation.</span></span>  
9. <span data-ttu-id="d2642-120">Stel Veiligheidsfactor in op "1".</span><span class="sxs-lookup"><span data-stu-id="d2642-120">Set Safety factor to '1'.</span></span>
    * <span data-ttu-id="d2642-121">Dit is de factor die wordt gebruikt om aanvullende hoeveelheid van beveiligingsvoorraad te berekenen.</span><span class="sxs-lookup"><span data-stu-id="d2642-121">This is the factor that is used to calculate additional quantity of safety stock.</span></span>  
10. <span data-ttu-id="d2642-122">Voer "30" in het veld Dagen voor in.</span><span class="sxs-lookup"><span data-stu-id="d2642-122">In the Days ahead field, enter '30'.</span></span>
    * <span data-ttu-id="d2642-123">Dit is het aantal dagen vóór de kanbanberekeningsdatum dat vraag in de berekening is opgenomen in de vraagberekening.</span><span class="sxs-lookup"><span data-stu-id="d2642-123">This is the number of days prior to the kanban quantity calculation date that is included in the demand calculation.</span></span>  
11. <span data-ttu-id="d2642-124">Voer "30" in het veld Dagen achter in.</span><span class="sxs-lookup"><span data-stu-id="d2642-124">In the Days behind field, enter '30'.</span></span>
    * <span data-ttu-id="d2642-125">Dit is het aantal dagen vooruit vanaf de kanbanberekeningsdatum dat vraag in de berekening is opgenomen in de vraagberekening.</span><span class="sxs-lookup"><span data-stu-id="d2642-125">This is the number of days forward from the kanban quantity calculation date that is included in the demand calculation.</span></span>  <span data-ttu-id="d2642-126">De formule wordt gebruikt voor de berekening wordt weergegeven met de werkelijke waarden.</span><span class="sxs-lookup"><span data-stu-id="d2642-126">The formula used for the calculation is shown with the actual values.</span></span> <span data-ttu-id="d2642-127">Bijvoorbeeld: Kanbanhoeveelheid = ((Gemiddelde dagelijkse vraag x doorlooptijd x 2,00)/Producthoeveelheid per materiaalverwerkingseenheid) + 1</span><span class="sxs-lookup"><span data-stu-id="d2642-127">For example,  Kanban quantity = ((Average daily demand x lead time x 2.00) / Product quantity per handling unit) + 1</span></span>  
12. <span data-ttu-id="d2642-128">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="d2642-128">Close the page.</span></span>

## <a name="add-the-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="d2642-129">Het beleid voor het toevoegen van de berekening van de kanbanhoeveelheid toevoegen aan de kanbanregel</span><span class="sxs-lookup"><span data-stu-id="d2642-129">Add the kanban quantity calculation policy to a kanban rule</span></span>
1. <span data-ttu-id="d2642-130">Ga naar Productgegevensbeheer > Lean manufacturing > Kanbanregels.</span><span class="sxs-lookup"><span data-stu-id="d2642-130">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="d2642-131">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="d2642-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d2642-132">Selecteer kanbanregel 000020 voor deze procedure.</span><span class="sxs-lookup"><span data-stu-id="d2642-132">Select kanban rule 000020 for this procedure.</span></span>  
3. <span data-ttu-id="d2642-133">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="d2642-133">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="d2642-134">Schakel de uitbreiding van de sectie voor het beleid voor berekening van de kanbanhoeveelheid om.</span><span class="sxs-lookup"><span data-stu-id="d2642-134">Toggle the expansion of the Kanban quantity calculation policies section.</span></span>
5. <span data-ttu-id="d2642-135">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="d2642-135">Click Add.</span></span>
    * <span data-ttu-id="d2642-136">Voeg het berekeningsbeleid voor de kanbanhoeveelheid toe die u zojuist in de vorige deeltaak hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d2642-136">Add the kanban quantity calculation policy that you have just created in the previous sub-task.</span></span>  
6. <span data-ttu-id="d2642-137">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="d2642-137">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="d2642-138">Klik in het veld Naam op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="d2642-138">In the Name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="d2642-139">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="d2642-139">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d2642-140">Selecteer het beleid Speaker2016 dat u zojuist in de vorige deeltaak hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d2642-140">Select the policy Speaker2016 that you have just created in the previous sub-task.</span></span>  

