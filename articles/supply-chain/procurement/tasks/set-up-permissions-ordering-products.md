---
title: Machtigingen instellen voor het bestellen van producten namens iemand anders
description: Dit onderwerp laat zien hoe u medewerkers machtigingen kunt verlenen om opdrachten tot inkoop voor te bereiden namens andere medewerkers.
author: mkirknel
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqAuthorization, HcmWorkerLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fe8ad0540febcc703554e2451f7f644338e4d57b
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149453"
---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a><span data-ttu-id="478e2-103">Machtigingen instellen voor het bestellen van producten namens iemand anders</span><span class="sxs-lookup"><span data-stu-id="478e2-103">Set up permissions for ordering products on behalf of someone else</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="478e2-104">Dit onderwerp laat zien hoe u medewerkers machtigingen kunt verlenen om opdrachten tot inkoop voor te bereiden namens andere medewerkers.</span><span class="sxs-lookup"><span data-stu-id="478e2-104">This topic explains how to grant workers permission to prepare purchase requisitions on behalf of other workers.</span></span> <span data-ttu-id="478e2-105">Met andere woorden, een opdracht tot inkoop voor voorbereider kan een opdracht tot inkoop maken voor een andere aanvrager.</span><span class="sxs-lookup"><span data-stu-id="478e2-105">In other words, a purchase requisition "preparer" can create a requisition for another "requester."</span></span> <span data-ttu-id="478e2-106">De procedure laat ook zien hoe u een werknemer kunt machtigen om artikelen en diensten in verschillende rechtspersonen of operationele eenheden te bestellen.</span><span class="sxs-lookup"><span data-stu-id="478e2-106">The procedure also shows how to grant a worker permission to order items and services in different legal entities or operating units.</span></span> <span data-ttu-id="478e2-107">Deze taken worden gewoonlijk uitgevoerd door een inkoopmanager.</span><span class="sxs-lookup"><span data-stu-id="478e2-107">Typically, these tasks are performed by a purchasing manager.</span></span> <span data-ttu-id="478e2-108">U kunt deze procedure gebruiken voor gegevens voor het USMF-demobedrijf of voor uw eigen gegevens.</span><span class="sxs-lookup"><span data-stu-id="478e2-108">You can use this procedure either on data for the USMF demo company or on your own data.</span></span>


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a><span data-ttu-id="478e2-109">Machtiging verlenen om opdrachten tot inkoop in te voeren namens een andere medewerker</span><span class="sxs-lookup"><span data-stu-id="478e2-109">Grant permission to enter purchase requisitions on behalf of another worker</span></span>
1. <span data-ttu-id="478e2-110">Ga in het navigatievenster naar **Modules > Inkoopbeheer > Instellingen > Beleid > Machtigingen voor inkoopbestelopdrachten**.</span><span class="sxs-lookup"><span data-stu-id="478e2-110">In the navigation pane, go to **Modules > Procurement and sourcing > Setup > Policies > Purchase requisition permissions**.</span></span> <span data-ttu-id="478e2-111">Controleer of het veld **Huidige weergave** is ingesteld op **Op voorbereider**.</span><span class="sxs-lookup"><span data-stu-id="478e2-111">Make sure that the **Current view** field is set to **By preparer**.</span></span> <span data-ttu-id="478e2-112">De lijst in het linkerdeelvenster laat de personen zien die kunnen worden gemachtigd om opdrachten namens andere mensen voor te bereiden.</span><span class="sxs-lookup"><span data-stu-id="478e2-112">The list in the left pane shows the people who can be granted permission to prepare requisitions on behalf of other people.</span></span>  
2. <span data-ttu-id="478e2-113">Selecteer de persoon die u wilt machtigen (de voorbereider).</span><span class="sxs-lookup"><span data-stu-id="478e2-113">Select the person to grant permission to (the preparer).</span></span>
3. <span data-ttu-id="478e2-114">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="478e2-114">Select **Add**.</span></span>
4. <span data-ttu-id="478e2-115">Zoek en selecteer de persoon die u als aanvrager wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="478e2-115">Find and select the person to add as a requester.</span></span>
    - <span data-ttu-id="478e2-116">De aanvrager is de persoon namens wie de voorbereider bestelopdrachten kan maken.</span><span class="sxs-lookup"><span data-stu-id="478e2-116">The requester is the person that the preparer can create requisitions on behalf of.</span></span>  
    - <span data-ttu-id="478e2-117">Selecteer in het veld **Autorisatie** de optie **Specifiek** als de voorbereider opdrachten tot inkoop moet kunnen maken namens de geselecteerde medewerker.</span><span class="sxs-lookup"><span data-stu-id="478e2-117">In the **Authorization** field, select **Specific** if the preparer should be able to create purchase requisitions on behalf of the selected worker.</span></span> <span data-ttu-id="478e2-118">Selecteer **Rapportage** als de voorbereider ook opdrachten tot inkoop moet kunnen maken namens alle medewerkers die aan die medewerker rapporteren.</span><span class="sxs-lookup"><span data-stu-id="478e2-118">Select **Reporting** if the preparer should also be able to create purchase requisitions on behalf of all workers who report to that worker.</span></span>  
5. <span data-ttu-id="478e2-119">Voer een datum in het veld **Ingangsdatum** in.</span><span class="sxs-lookup"><span data-stu-id="478e2-119">In the **Effective** field, enter a date.</span></span>
6. <span data-ttu-id="478e2-120">Voer in het veld **Vervaldatum** een datum in.</span><span class="sxs-lookup"><span data-stu-id="478e2-120">In the **Expiration** field, enter a date.</span></span>

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a><span data-ttu-id="478e2-121">Voorbereiders weergeven die zijn gemachtigd om opdrachten tot inkoop te maken voor een geselecteerde medewerker</span><span class="sxs-lookup"><span data-stu-id="478e2-121">View preparers who have permission to create purchase requisitions for a selected worker</span></span>
1. <span data-ttu-id="478e2-122">Selecteer **Op aanvrager** in het veld **Huidige weergave**.</span><span class="sxs-lookup"><span data-stu-id="478e2-122">In the **Current view** field, select **By requester**.</span></span> <span data-ttu-id="478e2-123">Deze weergave laat een lijst zien met voorbereiders aan wie machtiging vis verleend voor het maken van opdrachten tot inkoop namens een geselecteerde medewerker.</span><span class="sxs-lookup"><span data-stu-id="478e2-123">This view shows a list of preparers who have been granted permission to create purchase requisitions on behalf of a selected worker.</span></span>  
2. <span data-ttu-id="478e2-124">Gebruik het snelfilter om de medewerker te zoeken die zojuist als aanvrager hebt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="478e2-124">Use the Quick Filter to find the worker that you just added as the requester.</span></span>
3. <span data-ttu-id="478e2-125">Selecteer de aanvrager.</span><span class="sxs-lookup"><span data-stu-id="478e2-125">Select the requester.</span></span> <span data-ttu-id="478e2-126">De lijst Voorbereider bevat de personen die zijn gemachtigd om artikelen te bestellen namens de aanvrager die is geselecteerd in het linkerdeelvenster.</span><span class="sxs-lookup"><span data-stu-id="478e2-126">The Preparer list shows the people who have permission to order items on behalf of the requester who is selected in the left pane.</span></span>  <span data-ttu-id="478e2-127">U kunt hier extra voorbereiders toevoegen.</span><span class="sxs-lookup"><span data-stu-id="478e2-127">You can add additional preparers here.</span></span> <span data-ttu-id="478e2-128">In deze weergave kunt u ook de aanvrager verlenen machtiging om opdrachten te maken in rechtspersonen en operationele eenheden die niet de primaire rechtspersoon of operationele eenheid van die persoon zijn.</span><span class="sxs-lookup"><span data-stu-id="478e2-128">This view also lets you grant the requester permission to create requisitions in legal entities and operating units that aren't that person's primary legal entity or operating unit.</span></span>  

