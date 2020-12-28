---
title: Coproducten uit een bestaande formuleversie kopiëren
description: Deze procedure toont hoe u coproducten van een bestaande formuleversie kopieert naar een andere formuleversie voor een vrijgegeven product.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, PmfFormulaCoBy, BOMRouteCopyDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 79b70ccbdac2061baf3896ecbd9449da3c38842a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425171"
---
# <a name="copy-co-products-from-an-existing-formula-version"></a><span data-ttu-id="1c8e2-103">Coproducten uit een bestaande formuleversie kopiëren</span><span class="sxs-lookup"><span data-stu-id="1c8e2-103">Copy co-products from an existing formula version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1c8e2-104">Deze procedure toont hoe u coproducten van een bestaande formuleversie kopieert naar een andere formuleversie voor een vrijgegeven product.</span><span class="sxs-lookup"><span data-stu-id="1c8e2-104">This procedure shows how to copy co-products from an existing formula version to a different formula version for a released product.</span></span> <span data-ttu-id="1c8e2-105">Het is een vereiste dat er minimaal één formuleversie is gekoppeld aan coproducten.</span><span class="sxs-lookup"><span data-stu-id="1c8e2-105">It is a prerequisite that there is at least one formula version associated with co-products.</span></span> <span data-ttu-id="1c8e2-106">Het demobedrijf USP2 wordt gebruikt om deze procedure te maken.</span><span class="sxs-lookup"><span data-stu-id="1c8e2-106">The demo data company USP2 is used to create this procedure.</span></span>


## <a name="find-a-released-product"></a><span data-ttu-id="1c8e2-107">Een vrijgegeven product zoeken</span><span class="sxs-lookup"><span data-stu-id="1c8e2-107">Find a released product</span></span>
1. <span data-ttu-id="1c8e2-108">Ga naar Vrijgegeven producten.</span><span class="sxs-lookup"><span data-stu-id="1c8e2-108">Go to Released products.</span></span>
2. <span data-ttu-id="1c8e2-109">Klik op Filters weergeven.</span><span class="sxs-lookup"><span data-stu-id="1c8e2-109">Click Show filters.</span></span>
    * <span data-ttu-id="1c8e2-110">U staat op het punt het veld Productietype in het filterdialoogvenster toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="1c8e2-110">You are about to add the field Production type in the filter dialog box.</span></span>  
3. <span data-ttu-id="1c8e2-111">Klik op Een Filterveld toevoegen om het veld Productietype toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="1c8e2-111">Click Add a filter field to add the field Production type.</span></span>
    * <span data-ttu-id="1c8e2-112">In de volgende stap moet u handmatig Formule in het veld Productietype invoeren voordat u Toepassen selecteert.</span><span class="sxs-lookup"><span data-stu-id="1c8e2-112">In the next step, you need to manually enter Formula in the Production type field before you select Apply.</span></span> <span data-ttu-id="1c8e2-113">Hiermee wordt het filter ingesteld in de lijst van vrijgegeven producten.</span><span class="sxs-lookup"><span data-stu-id="1c8e2-113">This sets the filter on the list of released products.</span></span>  
4. <span data-ttu-id="1c8e2-114">Voer handmatig Formule in het veld Productietype in.</span><span class="sxs-lookup"><span data-stu-id="1c8e2-114">Manually enter Formula in the Production type field.</span></span>
5. <span data-ttu-id="1c8e2-115">Klik op Toepassen.</span><span class="sxs-lookup"><span data-stu-id="1c8e2-115">Click Apply.</span></span>

## <a name="select-a-released-product"></a><span data-ttu-id="1c8e2-116">Een vrijgegeven product selecteren</span><span class="sxs-lookup"><span data-stu-id="1c8e2-116">Select a released product</span></span>
1. <span data-ttu-id="1c8e2-117">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="1c8e2-117">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="1c8e2-118">Klik op Formuleversies.</span><span class="sxs-lookup"><span data-stu-id="1c8e2-118">Click Formula versions.</span></span>
    * <span data-ttu-id="1c8e2-119">Klik op het actievenster Engineering op Formuleversies.</span><span class="sxs-lookup"><span data-stu-id="1c8e2-119">On the Engineering Action Pane, click Formula versions.</span></span>  

## <a name="copy-co-products"></a><span data-ttu-id="1c8e2-120">Co-producten kopiëren</span><span class="sxs-lookup"><span data-stu-id="1c8e2-120">Copy co-products</span></span>
1. <span data-ttu-id="1c8e2-121">Klik in het actievenster op Formuleversie.</span><span class="sxs-lookup"><span data-stu-id="1c8e2-121">On the Action Pane, click Formula version.</span></span>
2. <span data-ttu-id="1c8e2-122">Klik op Coproducten.</span><span class="sxs-lookup"><span data-stu-id="1c8e2-122">Click Co-products.</span></span>
3. <span data-ttu-id="1c8e2-123">Klik op Kopiëren.</span><span class="sxs-lookup"><span data-stu-id="1c8e2-123">Click Copy.</span></span>
4. <span data-ttu-id="1c8e2-124">Typ of selecteer een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="1c8e2-124">In the Item number field, enter or select a value.</span></span>
5. <span data-ttu-id="1c8e2-125">Typ of selecteer een waarde in het veld Formuleversie.</span><span class="sxs-lookup"><span data-stu-id="1c8e2-125">In the Formula version field, enter or select a value.</span></span>
6. <span data-ttu-id="1c8e2-126">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="1c8e2-126">Click OK.</span></span>
7. <span data-ttu-id="1c8e2-127">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="1c8e2-127">Close the page.</span></span>

