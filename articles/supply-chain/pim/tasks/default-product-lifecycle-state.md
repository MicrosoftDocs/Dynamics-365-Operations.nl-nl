---
title: Een standaardstatus voor de productlevenscyclus maken
description: Deze procedure laat zien hoe u een standaardstatus voor een productlevenscyclus maakt en hoe u de standaardstatus koppelt aan vrijgegeven producten.
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6e7e637157ee06a3d07a1a9c5da71295eb75b424
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564173"
---
# <a name="create-a-default-product-lifecycle-state"></a><span data-ttu-id="ae396-103">Een standaardstatus voor de productlevenscyclus maken</span><span class="sxs-lookup"><span data-stu-id="ae396-103">Create a default product lifecycle state</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ae396-104">Deze procedure laat zien hoe u een standaardstatus voor een productlevenscyclus maakt en hoe u de standaardstatus koppelt aan vrijgegeven producten.</span><span class="sxs-lookup"><span data-stu-id="ae396-104">This procedure shows how to create a default product lifecycle state as well as how to associate the default state with released products.</span></span>


## <a name="create-a-default-lifecycle-state"></a><span data-ttu-id="ae396-105">Een standaardstatus voor de levenscyclus maken</span><span class="sxs-lookup"><span data-stu-id="ae396-105">Create a default lifecycle state</span></span>
1. <span data-ttu-id="ae396-106">Ga naar Productgegevensbeheer > Instellen > Levenscyclusstatus van product.</span><span class="sxs-lookup"><span data-stu-id="ae396-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="ae396-107">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="ae396-107">Click New.</span></span>
3. <span data-ttu-id="ae396-108">Typ een waarde in het veld Status.</span><span class="sxs-lookup"><span data-stu-id="ae396-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="ae396-109">Selecteer Ja in het veld Standaard bij vrijgave aan rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="ae396-109">Select Yes in the Default when released to legal entity field.</span></span>
5. <span data-ttu-id="ae396-110">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="ae396-110">In the Description field, type a value.</span></span>
6. <span data-ttu-id="ae396-111">Selecteer Nee in het veld Is actief voor planning.</span><span class="sxs-lookup"><span data-stu-id="ae396-111">Select No in the Is active for planning field.</span></span>

> [!NOTE]
> <span data-ttu-id="ae396-112">Selecteer Nee, als u een nieuw vrijgegeven product niet wilt opnemen in de Hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="ae396-112">If a new released product should not be included in Master planning, select No.</span></span> <span data-ttu-id="ae396-113">Als het wel moet worden opgenomen in de Hoofdplanning, laat u de standaardwaarde Ja staan.</span><span class="sxs-lookup"><span data-stu-id="ae396-113">If it should be included in Master planning, leave the control at its default value Yes.</span></span>  

## <a name="create-a-new-released-product"></a><span data-ttu-id="ae396-114">Een nieuw vrijgegeven product maken</span><span class="sxs-lookup"><span data-stu-id="ae396-114">Create a new released product</span></span>
1. <span data-ttu-id="ae396-115">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ae396-115">Close the page.</span></span>
2. <span data-ttu-id="ae396-116">Ga naar Productgegevensbeheer > Producten > Vrijgegeven producten.</span><span class="sxs-lookup"><span data-stu-id="ae396-116">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="ae396-117">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="ae396-117">Click New.</span></span>
4. <span data-ttu-id="ae396-118">Typ een waarde in het veld Productnummer.</span><span class="sxs-lookup"><span data-stu-id="ae396-118">In the Product number field, type a value.</span></span>
5. <span data-ttu-id="ae396-119">Typ een waarde in het veld Productnaam.</span><span class="sxs-lookup"><span data-stu-id="ae396-119">In the Product name field, type a value.</span></span>
6. <span data-ttu-id="ae396-120">Typ een waarde in het veld Zoeknaam.</span><span class="sxs-lookup"><span data-stu-id="ae396-120">In the Search name field, type a value.</span></span>
7. <span data-ttu-id="ae396-121">Typ of selecteer een waarde in het veld Artikelmodelgroep.</span><span class="sxs-lookup"><span data-stu-id="ae396-121">In the Item model group field, enter or select a value.</span></span>
8. <span data-ttu-id="ae396-122">Typ of selecteer een waarde in het veld Artikelgroep.</span><span class="sxs-lookup"><span data-stu-id="ae396-122">In the Item group field, enter or select a value.</span></span>
9. <span data-ttu-id="ae396-123">Typ of selecteer een waarde in het veld Opslagdimensiegroep.</span><span class="sxs-lookup"><span data-stu-id="ae396-123">In the Storage dimension group field, enter or select a value.</span></span>
10. <span data-ttu-id="ae396-124">Typ of selecteer een waarde in het veld Traceringsdimensiegroep.</span><span class="sxs-lookup"><span data-stu-id="ae396-124">In the Tracking dimension group field, enter or select a value.</span></span>
11. <span data-ttu-id="ae396-125">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="ae396-125">Click OK.</span></span>

> [!NOTE]
> <span data-ttu-id="ae396-126">De standaardstatus voor de productlevenscyclus is een algemene definitie.</span><span class="sxs-lookup"><span data-stu-id="ae396-126">The default product lifecycle state is a global definition.</span></span>  

## <a name="change-the-product-to-an-active-state"></a><span data-ttu-id="ae396-127">Het product wijzigen in een actieve status</span><span class="sxs-lookup"><span data-stu-id="ae396-127">Change the product to an active state</span></span>
1. <span data-ttu-id="ae396-128">Typ of selecteer een waarde in het veld Levenscyclusstatus van product.</span><span class="sxs-lookup"><span data-stu-id="ae396-128">In the Product lifecycle state field, enter or select a value.</span></span>

> [!NOTE]
> <span data-ttu-id="ae396-129">Stel dat u een actieve status hebt ingesteld, dan kunt u nu de actieve status selecteren om toe te staan dat het product wordt gebruikt in de Hoofdplanning en in de berekening op stuklijstniveau.</span><span class="sxs-lookup"><span data-stu-id="ae396-129">Assume that you have set up an active state, you can now select the active state to allow the product to be used in Master planning and BOM-level calculation.</span></span> <span data-ttu-id="ae396-130">Uiteraard is dit alleen zinvol als de productgegevens zijn opgegeven die vereist zijn voor een consistente planning.</span><span class="sxs-lookup"><span data-stu-id="ae396-130">Obviously, this only makes sense if all the product details that are required for consistent planning are specified.</span></span>  

