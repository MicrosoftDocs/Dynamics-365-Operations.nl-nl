---
title: "Een productieorder beëindigen"
description: "Deze procedure laat zien hoe u een productieorder beëindigt."
author: johanhoffmann
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
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a1c2facdea21d1c2f88071a3484fcc89fb5437bc
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---
# <a name="end-a-production-order"></a><span data-ttu-id="f0870-103">Een productieorder beëindigen</span><span class="sxs-lookup"><span data-stu-id="f0870-103">End a production order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f0870-104">Deze procedure laat zien hoe u een productieorder beëindigt.</span><span class="sxs-lookup"><span data-stu-id="f0870-104">This procedure shows how to end a production order.</span></span> <span data-ttu-id="f0870-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="f0870-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f0870-106">Dit is de laatste procedure van zeven waarin de levenscyclus van de productieorder wordt uitgelegd.</span><span class="sxs-lookup"><span data-stu-id="f0870-106">This is the final procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="end-a-production-order"></a><span data-ttu-id="f0870-107">Een productieorder beëindigen</span><span class="sxs-lookup"><span data-stu-id="f0870-107">End a production order</span></span>
1. <span data-ttu-id="f0870-108">Ga naar Productiebeheer > Productieorders > Alle productieorders.</span><span class="sxs-lookup"><span data-stu-id="f0870-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="f0870-109">Selecteer een productieorder die de status Gereedgemeld heeft.</span><span class="sxs-lookup"><span data-stu-id="f0870-109">Select a production order that has the status Reported as finished.</span></span>  
2. <span data-ttu-id="f0870-110">Klik in het actievenster op Productieorder.</span><span class="sxs-lookup"><span data-stu-id="f0870-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="f0870-111">Klik op Beëindigen.</span><span class="sxs-lookup"><span data-stu-id="f0870-111">Click End.</span></span>
    * <span data-ttu-id="f0870-112">Op deze pagina kunt u bevestigen dat u de productieorder wilt beëindigen.</span><span class="sxs-lookup"><span data-stu-id="f0870-112">On this page, you can confirm that you want to end the production order.</span></span>  
4. <span data-ttu-id="f0870-113">Klik op het tabblad Algemeen.</span><span class="sxs-lookup"><span data-stu-id="f0870-113">Click the General tab.</span></span>
5. <span data-ttu-id="f0870-114">Voer een datum in het veld Datum in.</span><span class="sxs-lookup"><span data-stu-id="f0870-114">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="f0870-115">Selecteer 'Toewijzing' in het veld Uitvalmethode.</span><span class="sxs-lookup"><span data-stu-id="f0870-115">In the Scrap method field, select 'Allocation'.</span></span>
    * <span data-ttu-id="f0870-116">Wanneer u de methode Toewijzing selecteert, worden kosten van de uitgevallen materialen opgeteld bij de eindproducten.</span><span class="sxs-lookup"><span data-stu-id="f0870-116">When you select the Allocation method, costs from the scrapped materials are added to the finished goods.</span></span>  
7. <span data-ttu-id="f0870-117">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f0870-117">Click OK.</span></span>

## <a name="validate-calculation-results"></a><span data-ttu-id="f0870-118">Berekeningsresultaten valideren</span><span class="sxs-lookup"><span data-stu-id="f0870-118">Validate calculation results</span></span>
1. <span data-ttu-id="f0870-119">Klik in het actievenster op Kosten beheren.</span><span class="sxs-lookup"><span data-stu-id="f0870-119">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="f0870-120">Klik op Kostenvergelijking weergeven.</span><span class="sxs-lookup"><span data-stu-id="f0870-120">Click View cost comparison.</span></span>
    * <span data-ttu-id="f0870-121">Nadat u de productieorder hebt beëindigd, kunt u de geschatte kostprijs vergelijken met de gerealiseerde kostprijs om een overzicht te krijgen van de productvarianties.</span><span class="sxs-lookup"><span data-stu-id="f0870-121">After you have ended the production order, you can compare the estimated cost price against the realized cost price to get an overview of the production variances.</span></span>  

