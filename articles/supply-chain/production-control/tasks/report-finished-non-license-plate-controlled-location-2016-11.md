---
title: Gereedmelden bij een locatie waar nummerplaten niet worden gecontroleerd (toepassing, mei 2016)
description: Deze taakbegeleiding toont een voorbeeld van gereedmelding bij een locatie waar geen nummerplaten worden gecontroleerd.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdParmCostEstimation, ProdParmStartUp, ProdParmReportFinished, WHSWorkTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fdb24238bf8c0cfea0006aa0aa0217de9d3f1bc2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831933"
---
# <a name="report-as-finished-to-a-non-license-plate-controlled-location--application-may-2016"></a><span data-ttu-id="d8a6e-103">Gereedmelden bij een locatie waar nummerplaten niet worden gecontroleerd (toepassing, mei 2016)</span><span class="sxs-lookup"><span data-stu-id="d8a6e-103">Report as finished to a non-license plate controlled location  (Application, May 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d8a6e-104">Deze taakbegeleiding toont een voorbeeld van gereedmelding bij een locatie waar geen nummerplaten worden gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="d8a6e-104">This task guide shows an example of reporting as finished to a location that isn't license plate–controlled.</span></span> <span data-ttu-id="d8a6e-105">Een toepasselijk werkbeleid is de vereiste voor deze taak.</span><span class="sxs-lookup"><span data-stu-id="d8a6e-105">An applicable work policy is the prerequisite for this task.</span></span> <span data-ttu-id="d8a6e-106">Een vorige taakbegeleiding liet zien hoe het werkbeleid wordt ingesteld.</span><span class="sxs-lookup"><span data-stu-id="d8a6e-106">A previous task guide showed the setup of the work policy.</span></span> <span data-ttu-id="d8a6e-107">Voor deze taakbegeleiding is de toepassing Dynamics AX 7.0.1 of hoger vereist.</span><span class="sxs-lookup"><span data-stu-id="d8a6e-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>




## <a name="set-up-an-output-location"></a><span data-ttu-id="d8a6e-108">Een uitvoerlocatie instellen</span><span class="sxs-lookup"><span data-stu-id="d8a6e-108">Set up an output location</span></span>
1. <span data-ttu-id="d8a6e-109">Ga naar Organisatiebeheer > Resources > Resourcegroepen.</span><span class="sxs-lookup"><span data-stu-id="d8a6e-109">Go to Organization administration > Resources > Resource groups.</span></span>
2. <span data-ttu-id="d8a6e-110">Selecteer resourcegroep '5102' in de lijst.</span><span class="sxs-lookup"><span data-stu-id="d8a6e-110">In the list, select resource group '5102'.</span></span>
3. <span data-ttu-id="d8a6e-111">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="d8a6e-111">Click Edit.</span></span>
4. <span data-ttu-id="d8a6e-112">Voer '51' in het veld Uitvoermagazijn in.</span><span class="sxs-lookup"><span data-stu-id="d8a6e-112">In the Output warehouse field, enter '51'.</span></span>
5. <span data-ttu-id="d8a6e-113">Voer '001' in het veld Uitvoerlocatie in.</span><span class="sxs-lookup"><span data-stu-id="d8a6e-113">In the Output location field, enter '001'.</span></span>
    * <span data-ttu-id="d8a6e-114">Locatie 001 is geen locatie waar nummerplaten worden gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="d8a6e-114">Location 001 isn't a license plate–controlled location.</span></span> <span data-ttu-id="d8a6e-115">U kunt een uitvoerlocatie waar geen nummerplaten worden gecontroleerd alleen instellen als er een toepasselijk werkbeleid voor de locatie bestaat.</span><span class="sxs-lookup"><span data-stu-id="d8a6e-115">You can set up a non–license plate output location only if an applicable work policy exists for the location.</span></span>  

## <a name="create-a-production-order-and-report-it-as-finished"></a><span data-ttu-id="d8a6e-116">Een productieorder maken en gereedmelden</span><span class="sxs-lookup"><span data-stu-id="d8a6e-116">Create a production order and report it as finished</span></span>
1. <span data-ttu-id="d8a6e-117">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="d8a6e-117">Close the page.</span></span>
2. <span data-ttu-id="d8a6e-118">Ga naar Productiebeheer > Productieorders > Alle productieorders.</span><span class="sxs-lookup"><span data-stu-id="d8a6e-118">Go to Production control > Production orders > All production orders.</span></span>
3. <span data-ttu-id="d8a6e-119">Klik op Nieuwe productieorder.</span><span class="sxs-lookup"><span data-stu-id="d8a6e-119">Click New production order.</span></span>
4. <span data-ttu-id="d8a6e-120">Voer 'L0101' in het veld Artikelnummer in.</span><span class="sxs-lookup"><span data-stu-id="d8a6e-120">In the Item number field, enter 'L0101'.</span></span>
5. <span data-ttu-id="d8a6e-121">Klik op Maken.</span><span class="sxs-lookup"><span data-stu-id="d8a6e-121">Click Create.</span></span>
6. <span data-ttu-id="d8a6e-122">Klik in het actievenster op Productieorder.</span><span class="sxs-lookup"><span data-stu-id="d8a6e-122">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="d8a6e-123">Klik op Raming.</span><span class="sxs-lookup"><span data-stu-id="d8a6e-123">Click Estimate.</span></span>
8. <span data-ttu-id="d8a6e-124">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="d8a6e-124">Click OK.</span></span>
9. <span data-ttu-id="d8a6e-125">Klik op Start.</span><span class="sxs-lookup"><span data-stu-id="d8a6e-125">Click Start.</span></span>
10. <span data-ttu-id="d8a6e-126">Klik op het tabblad Algemeen.</span><span class="sxs-lookup"><span data-stu-id="d8a6e-126">Click the General tab.</span></span>
11. <span data-ttu-id="d8a6e-127">Selecteer 'Nooit' in het veld Automatisch stuklijstverbruik.</span><span class="sxs-lookup"><span data-stu-id="d8a6e-127">In the Automatic BOM consumption field, select 'Never'.</span></span>
12. <span data-ttu-id="d8a6e-128">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="d8a6e-128">Click OK.</span></span>
13. <span data-ttu-id="d8a6e-129">Klik op Gereedmelden.</span><span class="sxs-lookup"><span data-stu-id="d8a6e-129">Click Report as finished.</span></span>
14. <span data-ttu-id="d8a6e-130">Klik op het tabblad Algemeen.</span><span class="sxs-lookup"><span data-stu-id="d8a6e-130">Click the General tab.</span></span>
15. <span data-ttu-id="d8a6e-131">Selecteer Ja in het veld Fout accepteren.</span><span class="sxs-lookup"><span data-stu-id="d8a6e-131">Select Yes in the Accept error field.</span></span>
16. <span data-ttu-id="d8a6e-132">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="d8a6e-132">Click OK.</span></span>
17. <span data-ttu-id="d8a6e-133">Klik in het actievenster op Magazijn.</span><span class="sxs-lookup"><span data-stu-id="d8a6e-133">On the Action Pane, click Warehouse.</span></span>
18. <span data-ttu-id="d8a6e-134">Klik op Werkdetails.</span><span class="sxs-lookup"><span data-stu-id="d8a6e-134">Click Work details.</span></span>
    * <span data-ttu-id="d8a6e-135">Toen de productieorder gereedgemeld werd, is er geen werk gegenereerd voor wegzetten.</span><span class="sxs-lookup"><span data-stu-id="d8a6e-135">When the production order was reported as finished, no work was generated for put-away.</span></span> <span data-ttu-id="d8a6e-136">Dit komt doordat er een werkbeleid is gedefinieerd waarmee wordt voorkomen dat werk wordt gegenereerd wanneer product L0101 wordt gereedgemeld bij locatie 001.</span><span class="sxs-lookup"><span data-stu-id="d8a6e-136">This occurs because a work policy is defined that prevents work from being generated when product L0101 is reported as finished to location 001.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]