---
title: Een productieorder ramen
description: U kunt deze procedure uitvoeren met behulp van het demobedrijf USMF of met uw eigen gegevensset.
author: johanhoffmann
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 58a0f8e9247e5885b1f148b3b28b7e67b1fa292d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240312"
---
# <a name="estimate-a-production-order"></a><span data-ttu-id="e6baf-103">Een productieorder ramen</span><span class="sxs-lookup"><span data-stu-id="e6baf-103">Estimate a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e6baf-104">U kunt deze procedure uitvoeren met behulp van het demobedrijf USMF of met uw eigen gegevensset.</span><span class="sxs-lookup"><span data-stu-id="e6baf-104">You can run this procedure by using the USMF demo data company or your own data set.</span></span> <span data-ttu-id="e6baf-105">In beide gevallen hebt u een open productieorder nodig die de status Gemaakt heeft.</span><span class="sxs-lookup"><span data-stu-id="e6baf-105">In both cases, you need to have an open production order that has the Created status.</span></span> <span data-ttu-id="e6baf-106">Dit is de tweede procedure van zeven waarin de levenscyclus van de productieorder wordt uitgelegd.</span><span class="sxs-lookup"><span data-stu-id="e6baf-106">This is the second procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="estimate-a-production-order"></a><span data-ttu-id="e6baf-107">Een productieorder ramen</span><span class="sxs-lookup"><span data-stu-id="e6baf-107">Estimate a production order</span></span>
1. <span data-ttu-id="e6baf-108">Ga naar Productiebeheer > Productieorders > Alle productieorders.</span><span class="sxs-lookup"><span data-stu-id="e6baf-108">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="e6baf-109">Selecteer een order met de status Gemaakt in het raster.</span><span class="sxs-lookup"><span data-stu-id="e6baf-109">Select an order that has the Created status in the grid.</span></span>
3. <span data-ttu-id="e6baf-110">Klik in het actievenster op Productieorder.</span><span class="sxs-lookup"><span data-stu-id="e6baf-110">On the Action Pane, click Production order.</span></span>
4. <span data-ttu-id="e6baf-111">Klik op Raming.</span><span class="sxs-lookup"><span data-stu-id="e6baf-111">Click Estimate.</span></span>
    * <span data-ttu-id="e6baf-112">In deze stap worden de geschatte kosten van één productieorder berekend.</span><span class="sxs-lookup"><span data-stu-id="e6baf-112">In this step, the estimated costs of a single production order is calculated.</span></span>   
5. <span data-ttu-id="e6baf-113">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="e6baf-113">Click OK.</span></span>

## <a name="view-the-calculation-details"></a><span data-ttu-id="e6baf-114">De berekeningsdetails weergeven</span><span class="sxs-lookup"><span data-stu-id="e6baf-114">View the calculation details</span></span>
1. <span data-ttu-id="e6baf-115">Klik in het actievenster op Kosten beheren.</span><span class="sxs-lookup"><span data-stu-id="e6baf-115">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="e6baf-116">Klik op Berekeningsdetails weergeven.</span><span class="sxs-lookup"><span data-stu-id="e6baf-116">Click View calculation details.</span></span>
    * <span data-ttu-id="e6baf-117">Op deze pagina wordt de kostenanalyse weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e6baf-117">This page displays the cost breakdown.</span></span> <span data-ttu-id="e6baf-118">U kunt bijvoorbeeld de totale kostprijs per eenheid weergeven voor het eindproduct op de eerste regel.</span><span class="sxs-lookup"><span data-stu-id="e6baf-118">For example, you can view the total cost price per unit for the finished product in the first row.</span></span> <span data-ttu-id="e6baf-119">De volgende rijen bevatten kosten volgens de stuklijst, productieroute en indirecte kosten.</span><span class="sxs-lookup"><span data-stu-id="e6baf-119">The subsequent rows contain costs according to the bill of materials, production route, and indirect costs.</span></span>  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]