---
title: Kostenobjecten maken
description: Deze procedure laat zien hoe u kostenobjecten maakt door het importeren van financiële dimensies van kostenplaatsen in Kostprijsboekhouding via een gegevensconnector.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed020348e50158362fda7b6b36dcdb17c48b4532
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142312"
---
# <a name="create-cost-objects"></a><span data-ttu-id="8f178-103">Kostenobjecten maken</span><span class="sxs-lookup"><span data-stu-id="8f178-103">Create cost objects</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8f178-104">Deze procedure laat zien hoe u kostenobjecten maakt door het importeren van financiële dimensies van kostenplaatsen in Kostprijsboekhouding via een gegevensconnector.</span><span class="sxs-lookup"><span data-stu-id="8f178-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="8f178-105">Het demobedrijf USMF wordt gebruikt om deze procedure te maken.</span><span class="sxs-lookup"><span data-stu-id="8f178-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="8f178-106">Nieuwe kostenobjecten maken</span><span class="sxs-lookup"><span data-stu-id="8f178-106">Create new cost objects</span></span>
1. <span data-ttu-id="8f178-107">Ga naar Kostprijsboekhouding > Dimensies > Dimensies van kostenobject.</span><span class="sxs-lookup"><span data-stu-id="8f178-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="8f178-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="8f178-108">Click New.</span></span>
3. <span data-ttu-id="8f178-109">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="8f178-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="8f178-110">Typ of selecteer een waarde in het veld Gegevensconnector voor dimensieleden.</span><span class="sxs-lookup"><span data-stu-id="8f178-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="8f178-111">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="8f178-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="8f178-112">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="8f178-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="8f178-113">De gegevensconnector configureren</span><span class="sxs-lookup"><span data-stu-id="8f178-113">Configure the data connector</span></span>
1. <span data-ttu-id="8f178-114">Klik op Dimensielidprovider configureren.</span><span class="sxs-lookup"><span data-stu-id="8f178-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="8f178-115">Selecteer CostCenter om de CostCenter-dimensie in Kostprijsboekhouding te importeren.</span><span class="sxs-lookup"><span data-stu-id="8f178-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="8f178-116">Selecteer Kostenplaats In het veld Dimensienaam.</span><span class="sxs-lookup"><span data-stu-id="8f178-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="8f178-117">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="8f178-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="8f178-118">Kostenplaatsen importeren</span><span class="sxs-lookup"><span data-stu-id="8f178-118">Import cost centers</span></span>
1. <span data-ttu-id="8f178-119">Klik op Dimensieleden importeren.</span><span class="sxs-lookup"><span data-stu-id="8f178-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="8f178-120">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="8f178-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="8f178-121">De geïmporteerde kostenplaatsen weergeven</span><span class="sxs-lookup"><span data-stu-id="8f178-121">View the imported cost centers</span></span>
1. <span data-ttu-id="8f178-122">Klik op Dimensieleden weergeven.</span><span class="sxs-lookup"><span data-stu-id="8f178-122">Click View dimension members.</span></span>

