---
title: Een plan voor een vestiging maken
description: De productieplanner berekent het materiaal en de capaciteitsbehoeften voor de productie van een specifiek artikel.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqTransPOUrgentFormPart, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d84fcd0012d4f7d87e2bc0769261fbe5f5139670
ms.sourcegitcommit: 0cc89dd42c1924ca0ec735c6566bc56b39cc5f7d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/26/2021
ms.locfileid: "6102657"
---
# <a name="create-a-plan-for-a-site"></a><span data-ttu-id="b200b-103">Een plan voor een vestiging maken</span><span class="sxs-lookup"><span data-stu-id="b200b-103">Create a plan for a site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b200b-104">De productieplanner berekent het materiaal en de capaciteitsbehoeften voor de productie van een specifiek artikel.</span><span class="sxs-lookup"><span data-stu-id="b200b-104">The production planner calculates the material and capacity requirements for the production of a specific item.</span></span> <span data-ttu-id="b200b-105">Nadat de sourcingsuggesties zijn gemaakt, vinden productieplanners de orders in de vestiging waarvoor zij een planning maken en zij fiatteren de orders, waarbij met de urgente orders wordt begonnen.</span><span class="sxs-lookup"><span data-stu-id="b200b-105">After the sourcing suggestions are created, they find the orders at the site for which they are planning and firms the orders, starting from the urgent ones.</span></span> <span data-ttu-id="b200b-106">De meest urgente orders zijn orders die op de huidige datum moeten worden gefiatteerd.</span><span class="sxs-lookup"><span data-stu-id="b200b-106">The most urgent orders are the ones that need to be firmed on the current date.</span></span> <span data-ttu-id="b200b-107">Gebruik het demobedrijf USMF om deze taken uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="b200b-107">Use the demo data company USMF to perform these tasks.</span></span>


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a><span data-ttu-id="b200b-108">Materialen en een capaciteitsplan maken voor een artikel</span><span class="sxs-lookup"><span data-stu-id="b200b-108">Create a materials and capacity plan for an item</span></span>
1. <span data-ttu-id="b200b-109">Klik op Hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="b200b-109">Click Master planning.</span></span>
    * <span data-ttu-id="b200b-110">U moet naar het standaarddashboard navigeren.</span><span class="sxs-lookup"><span data-stu-id="b200b-110">You need to navigate to the default Dashboard.</span></span>  
2. <span data-ttu-id="b200b-111">Klik op Uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="b200b-111">Click Run.</span></span>
3. <span data-ttu-id="b200b-112">Breid de sectie Op te nemen records uit.</span><span class="sxs-lookup"><span data-stu-id="b200b-112">Expand the Records to include section.</span></span>
4. <span data-ttu-id="b200b-113">Klik op Filter.</span><span class="sxs-lookup"><span data-stu-id="b200b-113">Click Filter.</span></span>
5. <span data-ttu-id="b200b-114">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b200b-114">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="b200b-115">Typ een waarde in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="b200b-115">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="b200b-116">Voorbeeld: D0001</span><span class="sxs-lookup"><span data-stu-id="b200b-116">Example: D0001</span></span>  
7. <span data-ttu-id="b200b-117">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b200b-117">Click OK.</span></span>
8. <span data-ttu-id="b200b-118">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b200b-118">Click OK.</span></span>
    * <span data-ttu-id="b200b-119">Dit kan enkele minuten in beslag nemen.</span><span class="sxs-lookup"><span data-stu-id="b200b-119">This may take a few minutes.</span></span>  
9. <span data-ttu-id="b200b-120">Vernieuw de pagina.</span><span class="sxs-lookup"><span data-stu-id="b200b-120">Refresh the page.</span></span>

## <a name="identify-the-urgent-planned-orders-for-the-item"></a><span data-ttu-id="b200b-121">De urgente geplande orders voor het artikel identificeren</span><span class="sxs-lookup"><span data-stu-id="b200b-121">Identify the urgent planned orders for the item</span></span>
1. <span data-ttu-id="b200b-122">Open het filter van de kolom Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="b200b-122">Open Item number column filter.</span></span>
2. <span data-ttu-id="b200b-123">Pas een filter toe op het veld Artikelnummer met een waarde D0001 en de filteroperator ´begint met´.</span><span class="sxs-lookup"><span data-stu-id="b200b-123">Apply a filter on the "Item number" field, with a value of "D0001", using the "begins with" filter operator.</span></span>
3. <span data-ttu-id="b200b-124">Open de kolomfilter Orderdatum.</span><span class="sxs-lookup"><span data-stu-id="b200b-124">Open Order date column filter.</span></span>
4. <span data-ttu-id="b200b-125">Pas een filter op het veld "Orderdatum" met een waarde van huidige datum toe met behulp van de operator "is exact".</span><span class="sxs-lookup"><span data-stu-id="b200b-125">Apply a filter on the "Order date" field, with a value of current date, using the "is exactly" filter operator.</span></span>

## <a name="firm-all-the-urgent-orders-for-the-item"></a><span data-ttu-id="b200b-126">Alle urgente orders voor het artikel fiatteren</span><span class="sxs-lookup"><span data-stu-id="b200b-126">Firm all the urgent orders for the item</span></span>
1. <span data-ttu-id="b200b-127">Selecteer of deselecteer alle rijen in de lijst.</span><span class="sxs-lookup"><span data-stu-id="b200b-127">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="b200b-128">Klik op Fiatteren.</span><span class="sxs-lookup"><span data-stu-id="b200b-128">Click Firm.</span></span>
3. <span data-ttu-id="b200b-129">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b200b-129">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]