---
title: Kostenobjecten maken
description: Deze procedure laat zien hoe u kostenobjecten maakt door het importeren van financiële dimensies van Dynamics 365 for Finance and Operations, Enterprise edition-kostenplaatsen in Kostprijsboekhouding via een gegevensconnector.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e12de1d51658092fb19f652cef7c1cc78b255b5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "322669"
---
# <a name="create-cost-objects"></a><span data-ttu-id="9768d-103">Kostenobjecten maken</span><span class="sxs-lookup"><span data-stu-id="9768d-103">Create cost objects</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9768d-104">Deze procedure laat zien hoe u kostenobjecten maakt door het importeren van financiële dimensies van Dynamics 365 for Finance and Operations, Enterprise edition-kostenplaatsen in Kostprijsboekhouding via een gegevensconnector.</span><span class="sxs-lookup"><span data-stu-id="9768d-104">This procedure shows how to create cost objects by importing the Dynamics 365 for Finance and Operations, Enterprise edition cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="9768d-105">Het demobedrijf USMF wordt gebruikt om deze procedure te maken.</span><span class="sxs-lookup"><span data-stu-id="9768d-105">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="9768d-106">Deze procedure is voor een functie van Kostprijsboekhouding die in Dynamics 365 for Operations, versie 1611 is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="9768d-106">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-objects"></a><span data-ttu-id="9768d-107">Nieuwe kostenobjecten maken</span><span class="sxs-lookup"><span data-stu-id="9768d-107">Create new cost objects</span></span>
1. <span data-ttu-id="9768d-108">Ga naar Kostprijsboekhouding > Dimensies > Dimensies van kostenobject.</span><span class="sxs-lookup"><span data-stu-id="9768d-108">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="9768d-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="9768d-109">Click New.</span></span>
3. <span data-ttu-id="9768d-110">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="9768d-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="9768d-111">Typ of selecteer een waarde in het veld Gegevensconnector voor dimensieleden.</span><span class="sxs-lookup"><span data-stu-id="9768d-111">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="9768d-112">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="9768d-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="9768d-113">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="9768d-113">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="9768d-114">De gegevensconnector configureren</span><span class="sxs-lookup"><span data-stu-id="9768d-114">Configure the data connector</span></span>
1. <span data-ttu-id="9768d-115">Klik op Dimensielidprovider configureren.</span><span class="sxs-lookup"><span data-stu-id="9768d-115">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="9768d-116">Selecteer CostCenter om de CostCenter-dimensie in Kostprijsboekhouding te importeren.</span><span class="sxs-lookup"><span data-stu-id="9768d-116">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="9768d-117">Selecteer Kostenplaats In het veld Dimensienaam.</span><span class="sxs-lookup"><span data-stu-id="9768d-117">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="9768d-118">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="9768d-118">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="9768d-119">Kostenplaatsen importeren</span><span class="sxs-lookup"><span data-stu-id="9768d-119">Import cost centers</span></span>
1. <span data-ttu-id="9768d-120">Klik op Dimensieleden importeren.</span><span class="sxs-lookup"><span data-stu-id="9768d-120">Click Import dimension members.</span></span>
2. <span data-ttu-id="9768d-121">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="9768d-121">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="9768d-122">De geïmporteerde kostenplaatsen weergeven</span><span class="sxs-lookup"><span data-stu-id="9768d-122">View the imported cost centers</span></span>
1. <span data-ttu-id="9768d-123">Klik op Dimensieleden weergeven.</span><span class="sxs-lookup"><span data-stu-id="9768d-123">Click View dimension members.</span></span>

