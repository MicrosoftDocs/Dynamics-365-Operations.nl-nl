---
title: Een productieorder beëindigen
description: Deze procedure laat zien hoe u een productieorder beëindigt.
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f5cb4afdc0285a6ccf28dbd362df3799c0ecc74
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555834"
---
# <a name="end-a-production-order"></a><span data-ttu-id="077f3-103">Een productieorder beëindigen</span><span class="sxs-lookup"><span data-stu-id="077f3-103">End a production order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="077f3-104">Deze procedure laat zien hoe u een productieorder beëindigt.</span><span class="sxs-lookup"><span data-stu-id="077f3-104">This procedure shows how to end a production order.</span></span> <span data-ttu-id="077f3-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="077f3-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="077f3-106">Dit is de laatste procedure van zeven waarin de levenscyclus van de productieorder wordt uitgelegd.</span><span class="sxs-lookup"><span data-stu-id="077f3-106">This is the final procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="end-a-production-order"></a><span data-ttu-id="077f3-107">Een productieorder beëindigen</span><span class="sxs-lookup"><span data-stu-id="077f3-107">End a production order</span></span>
1. <span data-ttu-id="077f3-108">Ga naar Productiebeheer > Productieorders > Alle productieorders.</span><span class="sxs-lookup"><span data-stu-id="077f3-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="077f3-109">Selecteer een productieorder die de status Gereedgemeld heeft.</span><span class="sxs-lookup"><span data-stu-id="077f3-109">Select a production order that has the status Reported as finished.</span></span>  
2. <span data-ttu-id="077f3-110">Klik in het actievenster op Productieorder.</span><span class="sxs-lookup"><span data-stu-id="077f3-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="077f3-111">Klik op Beëindigen.</span><span class="sxs-lookup"><span data-stu-id="077f3-111">Click End.</span></span>
    * <span data-ttu-id="077f3-112">Op deze pagina kunt u bevestigen dat u de productieorder wilt beëindigen.</span><span class="sxs-lookup"><span data-stu-id="077f3-112">On this page, you can confirm that you want to end the production order.</span></span>  
4. <span data-ttu-id="077f3-113">Klik op het tabblad Algemeen.</span><span class="sxs-lookup"><span data-stu-id="077f3-113">Click the General tab.</span></span>
5. <span data-ttu-id="077f3-114">Voer een datum in het veld Datum in.</span><span class="sxs-lookup"><span data-stu-id="077f3-114">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="077f3-115">Selecteer 'Toewijzing' in het veld Uitvalmethode.</span><span class="sxs-lookup"><span data-stu-id="077f3-115">In the Scrap method field, select 'Allocation'.</span></span>
    * <span data-ttu-id="077f3-116">Wanneer u de methode Toewijzing selecteert, worden kosten van de uitgevallen materialen opgeteld bij de eindproducten.</span><span class="sxs-lookup"><span data-stu-id="077f3-116">When you select the Allocation method, costs from the scrapped materials are added to the finished goods.</span></span>  
7. <span data-ttu-id="077f3-117">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="077f3-117">Click OK.</span></span>

## <a name="validate-calculation-results"></a><span data-ttu-id="077f3-118">Berekeningsresultaten valideren</span><span class="sxs-lookup"><span data-stu-id="077f3-118">Validate calculation results</span></span>
1. <span data-ttu-id="077f3-119">Klik in het actievenster op Kosten beheren.</span><span class="sxs-lookup"><span data-stu-id="077f3-119">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="077f3-120">Klik op Kostenvergelijking weergeven.</span><span class="sxs-lookup"><span data-stu-id="077f3-120">Click View cost comparison.</span></span>
    * <span data-ttu-id="077f3-121">Nadat u de productieorder hebt beëindigd, kunt u de geschatte kostprijs vergelijken met de gerealiseerde kostprijs om een overzicht te krijgen van de productvarianties.</span><span class="sxs-lookup"><span data-stu-id="077f3-121">After you have ended the production order, you can compare the estimated cost price against the realized cost price to get an overview of the production variances.</span></span>  
