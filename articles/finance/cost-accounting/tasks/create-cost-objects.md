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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 91c25c52a2c6dc7f096a494577b361ff30406e9c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236789"
---
# <a name="create-cost-objects"></a><span data-ttu-id="8d76c-103">Kostenobjecten maken</span><span class="sxs-lookup"><span data-stu-id="8d76c-103">Create cost objects</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8d76c-104">Deze procedure laat zien hoe u kostenobjecten maakt door het importeren van financiële dimensies van kostenplaatsen in Kostprijsboekhouding via een gegevensconnector.</span><span class="sxs-lookup"><span data-stu-id="8d76c-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="8d76c-105">Het demobedrijf USMF wordt gebruikt om deze procedure te maken.</span><span class="sxs-lookup"><span data-stu-id="8d76c-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="8d76c-106">Nieuwe kostenobjecten maken</span><span class="sxs-lookup"><span data-stu-id="8d76c-106">Create new cost objects</span></span>
1. <span data-ttu-id="8d76c-107">Ga naar Kostprijsboekhouding > Dimensies > Dimensies van kostenobject.</span><span class="sxs-lookup"><span data-stu-id="8d76c-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="8d76c-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="8d76c-108">Click New.</span></span>
3. <span data-ttu-id="8d76c-109">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="8d76c-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="8d76c-110">Typ of selecteer een waarde in het veld Gegevensconnector voor dimensieleden.</span><span class="sxs-lookup"><span data-stu-id="8d76c-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="8d76c-111">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="8d76c-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="8d76c-112">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="8d76c-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="8d76c-113">De gegevensconnector configureren</span><span class="sxs-lookup"><span data-stu-id="8d76c-113">Configure the data connector</span></span>
1. <span data-ttu-id="8d76c-114">Klik op Dimensielidprovider configureren.</span><span class="sxs-lookup"><span data-stu-id="8d76c-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="8d76c-115">Selecteer CostCenter om de CostCenter-dimensie in Kostprijsboekhouding te importeren.</span><span class="sxs-lookup"><span data-stu-id="8d76c-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="8d76c-116">Selecteer Kostenplaats In het veld Dimensienaam.</span><span class="sxs-lookup"><span data-stu-id="8d76c-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="8d76c-117">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="8d76c-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="8d76c-118">Kostenplaatsen importeren</span><span class="sxs-lookup"><span data-stu-id="8d76c-118">Import cost centers</span></span>
1. <span data-ttu-id="8d76c-119">Klik op Dimensieleden importeren.</span><span class="sxs-lookup"><span data-stu-id="8d76c-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="8d76c-120">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="8d76c-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="8d76c-121">De geïmporteerde kostenplaatsen weergeven</span><span class="sxs-lookup"><span data-stu-id="8d76c-121">View the imported cost centers</span></span>
1. <span data-ttu-id="8d76c-122">Klik op Dimensieleden weergeven.</span><span class="sxs-lookup"><span data-stu-id="8d76c-122">Click View dimension members.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]