---
title: " Een hardwarestation maken en koppelen"
description: Deze procedure doorloopt hoe u een nieuw hardwarestation maakt.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailHardwareStation, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 305308b0e4ba99aae4bf6f8f94041db570a25893
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141032"
---
# <a name="create-and-associate-a-hardware-station"></a><span data-ttu-id="e1281-103"> Een hardwarestation maken en koppelen</span><span class="sxs-lookup"><span data-stu-id="e1281-103">Create and associate a hardware station</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1281-104">Deze procedure doorloopt hoe u een nieuw hardwarestation maakt.</span><span class="sxs-lookup"><span data-stu-id="e1281-104">This procedure walks through how to create a new hardware station.</span></span> <span data-ttu-id="e1281-105">Een nieuw hardwareprofiel wordt gemaakt en gebruikt om nieuwe hardwarestations toe te voegen aan een vooraf gedefinieerde winkel (kanaal).</span><span class="sxs-lookup"><span data-stu-id="e1281-105">A new hardware profile will be created and used to add new hardware stations to a pre-defined store (channel).</span></span> <span data-ttu-id="e1281-106">Deze procedure gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="e1281-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="e1281-107">Ga naar Hoofdzaken van Commerce > Kanalen >...</span><span class="sxs-lookup"><span data-stu-id="e1281-107">Go to Commerce essentials > Channels > ..</span></span> <span data-ttu-id="e1281-108">> ..</span><span class="sxs-lookup"><span data-stu-id="e1281-108">> ..</span></span> <span data-ttu-id="e1281-109">> ..</span><span class="sxs-lookup"><span data-stu-id="e1281-109">> ..</span></span> <span data-ttu-id="e1281-110">> Profielen van hardwarestation.</span><span class="sxs-lookup"><span data-stu-id="e1281-110">> Hardware station profiles.</span></span>
2. <span data-ttu-id="e1281-111">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="e1281-111">Click New.</span></span>
3. <span data-ttu-id="e1281-112">Typ in het veld Hardwarestation-id 'TestHWProfile'.</span><span class="sxs-lookup"><span data-stu-id="e1281-112">In the Hardware station ID field, type 'TestHWProfile'.</span></span>
4. <span data-ttu-id="e1281-113">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="e1281-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="e1281-114">Voer een getal in het veld Poortnummer in.</span><span class="sxs-lookup"><span data-stu-id="e1281-114">In the Port number field, enter a number.</span></span>
6. <span data-ttu-id="e1281-115">Klik in het veld Hardwareprofiel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="e1281-115">In the Hardware profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="e1281-116">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="e1281-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="e1281-117">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e1281-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="e1281-118">Klik in het veld Pakketnaam op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="e1281-118">In the Package name field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="e1281-119">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e1281-119">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e1281-120">Dit is het standaardpakket dat met een nieuwe omgeving wordt geleverd.</span><span class="sxs-lookup"><span data-stu-id="e1281-120">This is the standard package that comes with a new environment.</span></span> <span data-ttu-id="e1281-121">Het versienummer kan variëren.</span><span class="sxs-lookup"><span data-stu-id="e1281-121">The version number may vary.</span></span>  
11. <span data-ttu-id="e1281-122">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="e1281-122">Click Save.</span></span>
12. <span data-ttu-id="e1281-123">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e1281-123">Close the page.</span></span>
13. <span data-ttu-id="e1281-124">Ga naar Retail en Commerce > Kanalen > Alle winkels.</span><span class="sxs-lookup"><span data-stu-id="e1281-124">Go to Retail and Commerce > Channels > All stores.</span></span>
14. <span data-ttu-id="e1281-125">Selecteer rij 17 in de lijst.</span><span class="sxs-lookup"><span data-stu-id="e1281-125">In the list, select row 17.</span></span>
    * <span data-ttu-id="e1281-126">Als u het demobedrijf USRT gebruikt, is dit de Houston-winkel.</span><span class="sxs-lookup"><span data-stu-id="e1281-126">If you are using the USRT demo data company, this is the Houston store.</span></span>  
15. <span data-ttu-id="e1281-127">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e1281-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="e1281-128">Schakel de uitbreiding van de sectie Hardwarestations om.</span><span class="sxs-lookup"><span data-stu-id="e1281-128">Toggle the expansion of the Hardware stations section.</span></span>
17. <span data-ttu-id="e1281-129">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e1281-129">Click Add.</span></span>
18. <span data-ttu-id="e1281-130">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e1281-130">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="e1281-131">Klik in het veld Profiel-id op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="e1281-131">In the Profile ID field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="e1281-132">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="e1281-132">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e1281-133">Dit moet het nieuwe hardwarestationprofiel zijn dat in de vorige stappen is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e1281-133">This must be the new hardware station profile that was created in the previous steps.</span></span>  
21. <span data-ttu-id="e1281-134">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e1281-134">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="e1281-135">Typ een waarde in het veld Hostnaam.</span><span class="sxs-lookup"><span data-stu-id="e1281-135">In the Host name field, type a value.</span></span>
23. <span data-ttu-id="e1281-136">Typ een waarde in het veld EFT-terminal-id.</span><span class="sxs-lookup"><span data-stu-id="e1281-136">In the EFT terminal ID field, type a value.</span></span>
24. <span data-ttu-id="e1281-137">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="e1281-137">Click Save.</span></span>

