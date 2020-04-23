---
title: Een status voor de productlevenscyclus toewijzen aan een vrijgegeven productmodel
description: Deze procedure laat zien hoe u een status van productlevenscyclus toewijst aan een vrijgegeven productmodel en de bijbehorende varianten.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab8c4e02a064fe84446fa54cc05b9a6a902c1860
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213142"
---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a><span data-ttu-id="779e0-103">Een status voor de productlevenscyclus toewijzen aan een vrijgegeven productmodel</span><span class="sxs-lookup"><span data-stu-id="779e0-103">Assign a product lifecycle state to a released product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="779e0-104">Deze procedure laat zien hoe u een status van productlevenscyclus toewijst aan een vrijgegeven productmodel en de bijbehorende varianten.</span><span class="sxs-lookup"><span data-stu-id="779e0-104">This procedure shows how to assign a product lifecycle state to a released product master and its variants.</span></span> <span data-ttu-id="779e0-105">Vereiste: U moet eerst de taakbegeleiding "Een nieuwe status voor de productlevenscyclus maken" afspelen om ervoor te zorgen dat er minimaal één status van productlevenscyclus is gemaakt voordat u deze taakbegeleiding kunt afspelen.</span><span class="sxs-lookup"><span data-stu-id="779e0-105">Prerequisite: You need to play the task guide "Create a new product lifecycle state" first to make sure that you have at least one product lifecycle state created before you can play this task guide.</span></span>


## <a name="find-a-released-product-master"></a><span data-ttu-id="779e0-106">Een vrijgegeven productmodel zoeken</span><span class="sxs-lookup"><span data-stu-id="779e0-106">Find a released product master</span></span>
1. <span data-ttu-id="779e0-107">Ga naar Productgegevensbeheer > Producten > Vrijgegeven producten.</span><span class="sxs-lookup"><span data-stu-id="779e0-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="779e0-108">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="779e0-108">In the list, find and select the desired record.</span></span>

> [!NOTE]
> <span data-ttu-id="779e0-109">Een productmodel heeft Productmodel als Subtype van product.</span><span class="sxs-lookup"><span data-stu-id="779e0-109">A product master has the Product subtype Product master.</span></span>  

## <a name="update-the-lifecycle-state"></a><span data-ttu-id="779e0-110">De levenscyclusstatus bijwerken</span><span class="sxs-lookup"><span data-stu-id="779e0-110">Update the lifecycle state</span></span>
1. <span data-ttu-id="779e0-111">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="779e0-111">Click Edit.</span></span>
2. <span data-ttu-id="779e0-112">Typ of selecteer een waarde in het veld Levenscyclusstatus van product.</span><span class="sxs-lookup"><span data-stu-id="779e0-112">In the Product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="779e0-113">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="779e0-113">Click Save.</span></span>
4. <span data-ttu-id="779e0-114">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="779e0-114">Click Yes.</span></span>

> [!NOTE]
> <span data-ttu-id="779e0-115">Als u Ja selecteert, worden alle gerelateerde vrijgegeven productvarianten met dezelfde oorspronkelijke status als het vrijgegeven productmodel bijgewerkt naar de nieuwe levenscyclusstatus van het product.</span><span class="sxs-lookup"><span data-stu-id="779e0-115">If Yes is selected, all the related released product variants that have the same original status as the released product master are also updated to the new product lifecycle state.</span></span> <span data-ttu-id="779e0-116">Als u Nee selecteert, behouden alle varianten hun huidige status.</span><span class="sxs-lookup"><span data-stu-id="779e0-116">If No is selected, all variants keep their actual state.</span></span> <span data-ttu-id="779e0-117">Varianten met een andere status van productlevenscyclus dan het vrijgegeven productmodel worden niet bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="779e0-117">Variants that have a different product lifecycle state from the released product master are not updated.</span></span>  

## <a name="verify-the-lifecycle-state-of-the-variants"></a><span data-ttu-id="779e0-118">De levenscyclusstatus van de varianten controleren</span><span class="sxs-lookup"><span data-stu-id="779e0-118">Verify the lifecycle state of the variants</span></span>
1. <span data-ttu-id="779e0-119">Klik op Vrijgegeven Productvarianten.</span><span class="sxs-lookup"><span data-stu-id="779e0-119">Click Released product variants.</span></span>

> [!NOTE]
> <span data-ttu-id="779e0-120">Houd er rekening mee dat alle varianten de status van productlevenscyclus hebben overgenomen van het vrijgegeven productmodel.</span><span class="sxs-lookup"><span data-stu-id="779e0-120">Note that all variants have inherited the selected lifecycle state from the released product master.</span></span>  

2. <span data-ttu-id="779e0-121">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="779e0-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="779e0-122">Typ of selecteer een waarde in het veld Levenscyclusstatus van product.</span><span class="sxs-lookup"><span data-stu-id="779e0-122">In the Product lifecycle state field, enter or select a value.</span></span>

