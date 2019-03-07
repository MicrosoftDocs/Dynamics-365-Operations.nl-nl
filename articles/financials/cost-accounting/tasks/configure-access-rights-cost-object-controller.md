---
title: Toegangsrechten configureren voor een controller voor kostenobjecten
description: Gebruik deze procedure om toegangsrechten te configureren voor een controller voor kostenobjecten.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6b7018f9d4926321341af94efd13911e2c69f5f5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "351166"
---
# <a name="configure-access-rights-for-a-cost-object-controller"></a><span data-ttu-id="4884b-103">Toegangsrechten configureren voor een controller voor kostenobjecten</span><span class="sxs-lookup"><span data-stu-id="4884b-103">Configure access rights for a cost object controller</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4884b-104">Gebruik deze procedure om toegangsrechten te configureren voor een controller voor kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="4884b-104">Use this procedure to configure access rights for a cost object controller.</span></span> <span data-ttu-id="4884b-105">Deze registratie gebruikt het USP2-demogegevensbedrijf.</span><span class="sxs-lookup"><span data-stu-id="4884b-105">This recording uses the USP2 demo data company.</span></span>


## <a name="assign-the-cost-object-controller-role"></a><span data-ttu-id="4884b-106">De rol van controller voor kostenobjecten toewijzen</span><span class="sxs-lookup"><span data-stu-id="4884b-106">Assign the cost object controller role</span></span>
1. <span data-ttu-id="4884b-107">Ga naar Systeembeheer > Gebruikers > Gebruikers.</span><span class="sxs-lookup"><span data-stu-id="4884b-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="4884b-108">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="4884b-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="4884b-109">Filter bijvoorbeeld op het veld Gebruikers met een waarde van 'alicia'.</span><span class="sxs-lookup"><span data-stu-id="4884b-109">For example, filter on the User name field with a value of 'alicia'.</span></span>
3. <span data-ttu-id="4884b-110">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="4884b-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="4884b-111">Klik op Rollen toewijzen.</span><span class="sxs-lookup"><span data-stu-id="4884b-111">Click Assign roles.</span></span>
5. <span data-ttu-id="4884b-112">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="4884b-112">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="4884b-113">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="4884b-113">Click OK.</span></span>

## <a name="enable-access-list-security"></a><span data-ttu-id="4884b-114">Toegangslijstbeveiliging inschakelen</span><span class="sxs-lookup"><span data-stu-id="4884b-114">Enable access list security</span></span>
1. <span data-ttu-id="4884b-115">Ga naar Kostprijsboekhouding > Dimensies > Dimensiehiërarchieën.</span><span class="sxs-lookup"><span data-stu-id="4884b-115">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="4884b-116">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="4884b-116">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4884b-117">Selecteer Organisatie.</span><span class="sxs-lookup"><span data-stu-id="4884b-117">Select Organization.</span></span>  
3. <span data-ttu-id="4884b-118">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="4884b-118">Click Edit.</span></span>
4. <span data-ttu-id="4884b-119">Selecteer Ja in het veld Hiërarchie van toegangslijsten.</span><span class="sxs-lookup"><span data-stu-id="4884b-119">Select Yes in the Access list hierarchy field.</span></span>
5. <span data-ttu-id="4884b-120">Klik op Hiërarchie weergeven.</span><span class="sxs-lookup"><span data-stu-id="4884b-120">Click View hierarchy.</span></span>

## <a name="assign-access-rights-to-user"></a><span data-ttu-id="4884b-121">Toegangsrechten toewijzen aan gebruiker</span><span class="sxs-lookup"><span data-stu-id="4884b-121">Assign access rights to user</span></span>
1. <span data-ttu-id="4884b-122">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="4884b-122">Click New.</span></span>
2. <span data-ttu-id="4884b-123">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="4884b-123">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="4884b-124">Typ of selecteer een waarde in het veld Gebruikers-id.</span><span class="sxs-lookup"><span data-stu-id="4884b-124">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="4884b-125">Selecteer Beheer.</span><span class="sxs-lookup"><span data-stu-id="4884b-125">Select Admin.</span></span>  
4. <span data-ttu-id="4884b-126">Selecteer in de structuur 'Organisatie\CEO\CFO\FIM'.</span><span class="sxs-lookup"><span data-stu-id="4884b-126">In the tree, select 'Organization\CEO\CFO\FIM'.</span></span>
5. <span data-ttu-id="4884b-127">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="4884b-127">Click New.</span></span>
6. <span data-ttu-id="4884b-128">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="4884b-128">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="4884b-129">Typ of selecteer een waarde in het veld Gebruikers-id.</span><span class="sxs-lookup"><span data-stu-id="4884b-129">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="4884b-130">Selecteer Alicia.</span><span class="sxs-lookup"><span data-stu-id="4884b-130">Select Alicia.</span></span>  
8. <span data-ttu-id="4884b-131">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="4884b-131">Click Save.</span></span>

## <a name="enable-access-rights-in-cost-accounting"></a><span data-ttu-id="4884b-132">Toegangsrechten inschakelen in kostprijsboekhouding</span><span class="sxs-lookup"><span data-stu-id="4884b-132">Enable access rights in Cost accounting</span></span>
1. <span data-ttu-id="4884b-133">Ga naar Kostprijsboekhouding > Instellen > Parameters.</span><span class="sxs-lookup"><span data-stu-id="4884b-133">Go to Cost accounting > Setup > Parameters.</span></span>
2. <span data-ttu-id="4884b-134">Klik op het tabblad Algemeen.</span><span class="sxs-lookup"><span data-stu-id="4884b-134">Click the General tab.</span></span>
3. <span data-ttu-id="4884b-135">Selecteer Ja in het veld Weergavetoegang voor dimensieleden voor kostenobject inschakelen.</span><span class="sxs-lookup"><span data-stu-id="4884b-135">Select Yes in the Enable view access for cost object dimension members field.</span></span>
4. <span data-ttu-id="4884b-136">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="4884b-136">Click Save.</span></span>
5. <span data-ttu-id="4884b-137">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4884b-137">Close the page.</span></span>
6. <span data-ttu-id="4884b-138">Ga naar Kostprijsboekhouding > Instellen > Configuratie van werkgebied voor kostenbeheer.</span><span class="sxs-lookup"><span data-stu-id="4884b-138">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
7. <span data-ttu-id="4884b-139">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="4884b-139">Click Edit.</span></span>
8. <span data-ttu-id="4884b-140">Selecteer Ja in het veld Gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="4884b-140">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="4884b-141">Als u Ja selecteert, kan een gebruiker die aan een van de volgende vier rollen is toegewezen, de rapporten zien in het werkgebied voor kostenbeheer: accounting manager, kostenaccountant, assistent kostenaccountant en controller voor kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="4884b-141">If you select Yes, a user who is assigned one of the following four roles can see the reports in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, and cost object controller.</span></span> <span data-ttu-id="4884b-142">Als u Nee selecteert, kan alleen een gebruiker die aan een van de volgende rollen is toegewezen, de rapporten zien: manager van kostprijsboekhouding, kostenaccountant en assistent kostenaccountant.</span><span class="sxs-lookup"><span data-stu-id="4884b-142">If you select No, only a user who is assigned one of the following roles can see the reports: cost accounting manager, cost accountant, and cost accountant clerk.</span></span>    
9. <span data-ttu-id="4884b-143">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="4884b-143">Click Save.</span></span>

