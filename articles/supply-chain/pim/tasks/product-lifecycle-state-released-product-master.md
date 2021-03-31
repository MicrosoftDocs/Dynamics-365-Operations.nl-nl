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
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a5d7f6532e3c0b61fcc5758f383257d4a9a09b5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226732"
---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a><span data-ttu-id="c2e12-103">Een status voor de productlevenscyclus toewijzen aan een vrijgegeven productmodel</span><span class="sxs-lookup"><span data-stu-id="c2e12-103">Assign a product lifecycle state to a released product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c2e12-104">Deze procedure laat zien hoe u een status van productlevenscyclus toewijst aan een vrijgegeven productmodel en de bijbehorende varianten.</span><span class="sxs-lookup"><span data-stu-id="c2e12-104">This procedure shows how to assign a product lifecycle state to a released product master and its variants.</span></span> <span data-ttu-id="c2e12-105">Vereiste: U moet eerst de guide "Een nieuwe status voor de productlevenscyclus maken" afspelen om ervoor te zorgen dat er minimaal één status van productlevenscyclus is gemaakt voordat u deze guide kunt afspelen.</span><span class="sxs-lookup"><span data-stu-id="c2e12-105">Prerequisite: You need to play the task guide "Create a new product lifecycle state" first to make sure that you have at least one product lifecycle state created before you can play this task guide.</span></span>


## <a name="find-a-released-product-master"></a><span data-ttu-id="c2e12-106">Een vrijgegeven productmodel zoeken</span><span class="sxs-lookup"><span data-stu-id="c2e12-106">Find a released product master</span></span>
1. <span data-ttu-id="c2e12-107">Ga naar Productgegevensbeheer > Producten > Vrijgegeven producten.</span><span class="sxs-lookup"><span data-stu-id="c2e12-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="c2e12-108">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="c2e12-108">In the list, find and select the desired record.</span></span>

> [!NOTE]
> <span data-ttu-id="c2e12-109">Een productmodel heeft Productmodel als Subtype van product.</span><span class="sxs-lookup"><span data-stu-id="c2e12-109">A product master has the Product subtype Product master.</span></span>  

## <a name="update-the-lifecycle-state"></a><span data-ttu-id="c2e12-110">De levenscyclusstatus bijwerken</span><span class="sxs-lookup"><span data-stu-id="c2e12-110">Update the lifecycle state</span></span>
1. <span data-ttu-id="c2e12-111">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="c2e12-111">Click Edit.</span></span>
2. <span data-ttu-id="c2e12-112">Typ of selecteer een waarde in het veld Levenscyclusstatus van product.</span><span class="sxs-lookup"><span data-stu-id="c2e12-112">In the Product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="c2e12-113">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="c2e12-113">Click Save.</span></span>
4. <span data-ttu-id="c2e12-114">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="c2e12-114">Click Yes.</span></span>

> [!NOTE]
> <span data-ttu-id="c2e12-115">Als u Ja selecteert, worden alle gerelateerde vrijgegeven productvarianten met dezelfde oorspronkelijke status als het vrijgegeven productmodel bijgewerkt naar de nieuwe levenscyclusstatus van het product.</span><span class="sxs-lookup"><span data-stu-id="c2e12-115">If Yes is selected, all the related released product variants that have the same original status as the released product master are also updated to the new product lifecycle state.</span></span> <span data-ttu-id="c2e12-116">Als u Nee selecteert, behouden alle varianten hun huidige status.</span><span class="sxs-lookup"><span data-stu-id="c2e12-116">If No is selected, all variants keep their actual state.</span></span> <span data-ttu-id="c2e12-117">Varianten met een andere status van productlevenscyclus dan het vrijgegeven productmodel worden niet bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="c2e12-117">Variants that have a different product lifecycle state from the released product master are not updated.</span></span>  

## <a name="verify-the-lifecycle-state-of-the-variants"></a><span data-ttu-id="c2e12-118">De levenscyclusstatus van de varianten controleren</span><span class="sxs-lookup"><span data-stu-id="c2e12-118">Verify the lifecycle state of the variants</span></span>
1. <span data-ttu-id="c2e12-119">Klik op Vrijgegeven Productvarianten.</span><span class="sxs-lookup"><span data-stu-id="c2e12-119">Click Released product variants.</span></span>

> [!NOTE]
> <span data-ttu-id="c2e12-120">Houd er rekening mee dat alle varianten de status van productlevenscyclus hebben overgenomen van het vrijgegeven productmodel.</span><span class="sxs-lookup"><span data-stu-id="c2e12-120">Note that all variants have inherited the selected lifecycle state from the released product master.</span></span>  

2. <span data-ttu-id="c2e12-121">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c2e12-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="c2e12-122">Typ of selecteer een waarde in het veld Levenscyclusstatus van product.</span><span class="sxs-lookup"><span data-stu-id="c2e12-122">In the Product lifecycle state field, enter or select a value.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]