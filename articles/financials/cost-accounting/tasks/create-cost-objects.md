--- 
title: Kostenobjecten maken
description: "Deze procedure laat zien hoe u kostenobjecten maakt door het importeren van financiële dimensies van Dynamics 365 for Finance and Operations-kostenplaatsen in Kostprijsboekhouding via een gegevensconnector."
author: ShylaThompson
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 571406164236c7c079e059367e5d757cc4cefb1f
ms.contentlocale: nl-nl
ms.lasthandoff: 08/07/2018

---
# <a name="create-cost-objects"></a><span data-ttu-id="fda4d-103">Kostenobjecten maken</span><span class="sxs-lookup"><span data-stu-id="fda4d-103">Create cost objects</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fda4d-104">Deze procedure laat zien hoe u kostenobjecten maakt door het importeren van financiële dimensies van Dynamics 365 for Finance and Operations-kostenplaatsen in Kostprijsboekhouding via een gegevensconnector.</span><span class="sxs-lookup"><span data-stu-id="fda4d-104">This procedure shows how to create cost objects by importing the Dynamics 365 for Finance and Operations cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="fda4d-105">Het demobedrijf USMF wordt gebruikt om deze procedure te maken.</span><span class="sxs-lookup"><span data-stu-id="fda4d-105">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="fda4d-106">Deze procedure is voor een Kostprijsboekhoudingsfunctie die in versie 1611 van Dynamics 365 for Operations is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="fda4d-106">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-objects"></a><span data-ttu-id="fda4d-107">Nieuwe kostenobjecten maken</span><span class="sxs-lookup"><span data-stu-id="fda4d-107">Create new cost objects</span></span>
1. <span data-ttu-id="fda4d-108">Ga naar Kostprijsboekhouding > Dimensies > Dimensies van kostenobject.</span><span class="sxs-lookup"><span data-stu-id="fda4d-108">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="fda4d-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="fda4d-109">Click New.</span></span>
3. <span data-ttu-id="fda4d-110">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="fda4d-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="fda4d-111">Typ of selecteer een waarde in het veld Gegevensconnector voor dimensieleden.</span><span class="sxs-lookup"><span data-stu-id="fda4d-111">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="fda4d-112">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="fda4d-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="fda4d-113">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="fda4d-113">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="fda4d-114">De gegevensconnector configureren</span><span class="sxs-lookup"><span data-stu-id="fda4d-114">Configure the data connector</span></span>
1. <span data-ttu-id="fda4d-115">Klik op Dimensielidprovider configureren.</span><span class="sxs-lookup"><span data-stu-id="fda4d-115">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="fda4d-116">Selecteer CostCenter om de CostCenter-dimensie in Kostprijsboekhouding te importeren.</span><span class="sxs-lookup"><span data-stu-id="fda4d-116">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="fda4d-117">Selecteer Kostenplaats In het veld Dimensienaam.</span><span class="sxs-lookup"><span data-stu-id="fda4d-117">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="fda4d-118">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="fda4d-118">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="fda4d-119">Kostenplaatsen importeren</span><span class="sxs-lookup"><span data-stu-id="fda4d-119">Import cost centers</span></span>
1. <span data-ttu-id="fda4d-120">Klik op Dimensieleden importeren.</span><span class="sxs-lookup"><span data-stu-id="fda4d-120">Click Import dimension members.</span></span>
2. <span data-ttu-id="fda4d-121">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="fda4d-121">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="fda4d-122">De geïmporteerde kostenplaatsen weergeven</span><span class="sxs-lookup"><span data-stu-id="fda4d-122">View the imported cost centers</span></span>
1. <span data-ttu-id="fda4d-123">Klik op Dimensieleden weergeven.</span><span class="sxs-lookup"><span data-stu-id="fda4d-123">Click View dimension members.</span></span>


