--- 
title: Een plan voor een vestiging maken
description: De productieplanner berekent het materiaal en de capaciteitsbehoeften voor de productie van een specifiek artikel.
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqTransPOUrgentFormPart, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: ebe3841720b4eb76e58e2d6e2f557558b03156d6
ms.contentlocale: nl-nl
ms.lasthandoff: 09/11/2018

---
# <a name="create-a-plan-for-a-site"></a><span data-ttu-id="0c211-103">Een plan voor een vestiging maken</span><span class="sxs-lookup"><span data-stu-id="0c211-103">Create a plan for a site</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0c211-104">De productieplanner berekent het materiaal en de capaciteitsbehoeften voor de productie van een specifiek artikel.</span><span class="sxs-lookup"><span data-stu-id="0c211-104">The production planner calculates the material and capacity requirements for the production of a specific item.</span></span> <span data-ttu-id="0c211-105">Nadat de sourcingsuggesties zijn gemaakt, vindt de productieplanner de orders in de vestiging waarvoor hij/zij een planning maakt en hij/zij fiatteert de orders, waarbij met de urgente orders wordt begonnen.</span><span class="sxs-lookup"><span data-stu-id="0c211-105">After the sourcing suggestions are created, he finds the orders at the site for which he is planning and firms the orders, starting from the urgent ones.</span></span> <span data-ttu-id="0c211-106">De meest urgente orders zijn orders die op de huidige datum moeten worden gefiatteerd.</span><span class="sxs-lookup"><span data-stu-id="0c211-106">The most urgent orders are the ones that need to be firmed on the current date.</span></span> <span data-ttu-id="0c211-107">Gebruik het demobedrijf USMF om deze taken uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="0c211-107">Use the demo data company USMF to perform these tasks.</span></span>


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a><span data-ttu-id="0c211-108">Materialen en een capaciteitsplan maken voor een artikel</span><span class="sxs-lookup"><span data-stu-id="0c211-108">Create a materials and capacity plan for an item</span></span>
1. <span data-ttu-id="0c211-109">Klik op Hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="0c211-109">Click Master planning.</span></span>
    * <span data-ttu-id="0c211-110">U moet naar het standaarddashboard navigeren.</span><span class="sxs-lookup"><span data-stu-id="0c211-110">You need to navigate to the default Dashboard.</span></span>  
2. <span data-ttu-id="0c211-111">Klik op Uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="0c211-111">Click Run.</span></span>
3. <span data-ttu-id="0c211-112">Breid de sectie Op te nemen records uit.</span><span class="sxs-lookup"><span data-stu-id="0c211-112">Expand the Records to include section.</span></span>
4. <span data-ttu-id="0c211-113">Klik op Filter.</span><span class="sxs-lookup"><span data-stu-id="0c211-113">Click Filter.</span></span>
5. <span data-ttu-id="0c211-114">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="0c211-114">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="0c211-115">Typ een waarde in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="0c211-115">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="0c211-116">Voorbeeld: D0001</span><span class="sxs-lookup"><span data-stu-id="0c211-116">Example: D0001</span></span>  
7. <span data-ttu-id="0c211-117">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="0c211-117">Click OK.</span></span>
8. <span data-ttu-id="0c211-118">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="0c211-118">Click OK.</span></span>
    * <span data-ttu-id="0c211-119">Dit kan enkele minuten in beslag nemen.</span><span class="sxs-lookup"><span data-stu-id="0c211-119">This may take a few minutes.</span></span>  
9. <span data-ttu-id="0c211-120">Vernieuw de pagina.</span><span class="sxs-lookup"><span data-stu-id="0c211-120">Refresh the page.</span></span>

## <a name="identify-the-urgent-planned-orders-for-the-item"></a><span data-ttu-id="0c211-121">De urgente geplande orders voor het artikel identificeren</span><span class="sxs-lookup"><span data-stu-id="0c211-121">Identify the urgent planned orders for the item</span></span>
1. <span data-ttu-id="0c211-122">Open het filter van de kolom Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="0c211-122">Open Item number column filter.</span></span>
2. <span data-ttu-id="0c211-123">Pas een filter toe op het veld Artikelnummer met een waarde D0001 en de filteroperator ´begint met´.</span><span class="sxs-lookup"><span data-stu-id="0c211-123">Apply a filter on the "Item number" field, with a value of "D0001", using the "begins with" filter operator.</span></span>
3. <span data-ttu-id="0c211-124">Open de kolomfilter Orderdatum.</span><span class="sxs-lookup"><span data-stu-id="0c211-124">Open Order date column filter.</span></span>
4. <span data-ttu-id="0c211-125">Pas een filter op het veld "Orderdatum" met een waarde van huidige datum toe met behulp van de operator "is exact".</span><span class="sxs-lookup"><span data-stu-id="0c211-125">Apply a filter on the "Order date" field, with a value of current date, using the "is exactly" filter operator.</span></span>

## <a name="firm-all-the-urgent-orders-for-the-item"></a><span data-ttu-id="0c211-126">Alle urgente orders voor het artikel fiatteren</span><span class="sxs-lookup"><span data-stu-id="0c211-126">Firm all the urgent orders for the item</span></span>
1. <span data-ttu-id="0c211-127">Selecteer of deselecteer alle rijen in de lijst.</span><span class="sxs-lookup"><span data-stu-id="0c211-127">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="0c211-128">Klik op Fiatteren.</span><span class="sxs-lookup"><span data-stu-id="0c211-128">Click Firm.</span></span>
3. <span data-ttu-id="0c211-129">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="0c211-129">Click OK.</span></span>


