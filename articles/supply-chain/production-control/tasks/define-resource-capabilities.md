---
title: Bronmogelijkheden definiëren
description: Resourcecapaciteiten beschrijven wat resources voor bedrijfsactiviteiten kunnen doen.
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrCapability
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6bd3f2b1efc1e6a883ad2a25d127e74a8925de8f
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146785"
---
# <a name="define-resource-capabilities"></a><span data-ttu-id="f66c6-103">Bronmogelijkheden definiëren</span><span class="sxs-lookup"><span data-stu-id="f66c6-103">Define resource capabilities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f66c6-104">Resourcecapaciteiten beschrijven wat resources voor bedrijfsactiviteiten kunnen doen.</span><span class="sxs-lookup"><span data-stu-id="f66c6-104">Resource capabilities describe what operations resources can do.</span></span> <span data-ttu-id="f66c6-105">Tijdens het plannen worden de vereisten van elke taak en bewerking vergeleken met de capaciteiten van de beschikbare resources.</span><span class="sxs-lookup"><span data-stu-id="f66c6-105">During scheduling, the requirements of each job and operation are matched against the capabilities of the available resources.</span></span> <span data-ttu-id="f66c6-106">Deze taakbegeleiding helpt u een resourcecapaciteit te maken en deze toe te wijzen aan een resource.</span><span class="sxs-lookup"><span data-stu-id="f66c6-106">This task guide will help you create a resource capability and assign it to a resource.</span></span> <span data-ttu-id="f66c6-107">Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="f66c6-107">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-resource-capability"></a><span data-ttu-id="f66c6-108">Een resourcecapaciteit maken</span><span class="sxs-lookup"><span data-stu-id="f66c6-108">Create a resource capability</span></span>
1. <span data-ttu-id="f66c6-109">Ga naar Bronmogelijkheden.</span><span class="sxs-lookup"><span data-stu-id="f66c6-109">Go to Resource capabilities.</span></span>
2. <span data-ttu-id="f66c6-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="f66c6-110">Click New.</span></span>
3. <span data-ttu-id="f66c6-111">Typ in het veld Mogelijkheid de ID van de bronmogelijkheid.</span><span class="sxs-lookup"><span data-stu-id="f66c6-111">In the Capability field, type the ID of the resource capability.</span></span>
    * <span data-ttu-id="f66c6-112">Voor een bepaalde bewerking gebruikt u de capaciteits-id om de resources op te geven die deze capaciteit moeten hebben om de bewerking uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="f66c6-112">For a given operation, you use the capability ID to specify that resources must have this capability to perform the operation.</span></span>  
4. <span data-ttu-id="f66c6-113">Voer in het veld Omschrijving een omschrijving van de mogelijkheid in.</span><span class="sxs-lookup"><span data-stu-id="f66c6-113">In the Description field, enter a description of the capability.</span></span>

## <a name="assign-capability-to-a-resource"></a><span data-ttu-id="f66c6-114">Capaciteit aan een resource toewijzen</span><span class="sxs-lookup"><span data-stu-id="f66c6-114">Assign capability to a resource</span></span>
1. <span data-ttu-id="f66c6-115">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="f66c6-115">Click Add.</span></span>
2. <span data-ttu-id="f66c6-116">Typ in het veld Bron de ID van de bron.</span><span class="sxs-lookup"><span data-stu-id="f66c6-116">In the Resource field, type the ID of the resource.</span></span>
    * <span data-ttu-id="f66c6-117">Een resourcecapaciteit kan aan een of meer resources zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="f66c6-117">A resource capability can be assigned to one or more resources.</span></span>  
3. <span data-ttu-id="f66c6-118">Voer in het veld Vervaldatum een datum in.</span><span class="sxs-lookup"><span data-stu-id="f66c6-118">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="f66c6-119">U kunt dit veld gebruiken om te specificeren dat een resource de capaciteit voor een beperkte tijd heeft.</span><span class="sxs-lookup"><span data-stu-id="f66c6-119">You can use this field to specify that a resource has the capability for only a limited time.</span></span>  
4. <span data-ttu-id="f66c6-120">Voer een getal in het veld Prioriteit in.</span><span class="sxs-lookup"><span data-stu-id="f66c6-120">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="f66c6-121">Wanneer u taken en bewerkingen plant, kunt u opgeven of u resources op prioriteit wilt selecteren.</span><span class="sxs-lookup"><span data-stu-id="f66c6-121">When you schedule jobs and operations, you can specify whether to select resources by priority.</span></span> <span data-ttu-id="f66c6-122">Als u dit kiest, en er meer dan één resource de taak of de bewerking op de gevraagde datum kan uitvoeren, wordt de resource met de laagste prioriteit met betrekking tot de vereiste capaciteit geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="f66c6-122">If you choose to do this, and more than one resource can perform the job or operation by the requested date, the resource that has the lowest priority with respect to the required capability is selected.</span></span>  
5. <span data-ttu-id="f66c6-123">Voer een nummer in het veld Niveau in.</span><span class="sxs-lookup"><span data-stu-id="f66c6-123">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="f66c6-124">Wanneer u opgeeft dat een taak of bewerking een bepaalde capaciteit vereist, kunt u ook het minimum niveau opgeven dat nodig is.</span><span class="sxs-lookup"><span data-stu-id="f66c6-124">When you specify that a job or operation requires a particular capability, you can also specify the minimum level that is required.</span></span> <span data-ttu-id="f66c6-125">Gebruik het capaciteitsniveau om resources te onderscheiden die dezelfde taak kunnen uitvoeren, maar met verschillende snelheden, sterke punten, grootte, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="f66c6-125">Use the capability level to differentiate resources that can perform the same job, but at different speeds, strengths, sizes, and so on.</span></span>  

