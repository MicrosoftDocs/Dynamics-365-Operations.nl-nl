---
title: Een status voor de productlevenscyclus toewijzen aan een vrijgegeven productmodel
description: Deze procedure laat zien hoe u een status van productlevenscyclus toewijst aan een vrijgegeven productmodel en de bijbehorende varianten.
author: cvocph
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 66859c7f7f5be6eaadd9470fd9b792daa28ce33d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807877"
---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a><span data-ttu-id="4ca2a-103">Een status voor de productlevenscyclus toewijzen aan een vrijgegeven productmodel</span><span class="sxs-lookup"><span data-stu-id="4ca2a-103">Assign a product lifecycle state to a released product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4ca2a-104">Deze procedure laat zien hoe u een status van productlevenscyclus toewijst aan een vrijgegeven productmodel en de bijbehorende varianten.</span><span class="sxs-lookup"><span data-stu-id="4ca2a-104">This procedure shows how to assign a product lifecycle state to a released product master and its variants.</span></span> <span data-ttu-id="4ca2a-105">Vereiste: U moet eerst de guide "Een nieuwe status voor de productlevenscyclus maken" afspelen om ervoor te zorgen dat er minimaal één status van productlevenscyclus is gemaakt voordat u deze guide kunt afspelen.</span><span class="sxs-lookup"><span data-stu-id="4ca2a-105">Prerequisite: You need to play the task guide "Create a new product lifecycle state" first to make sure that you have at least one product lifecycle state created before you can play this task guide.</span></span>


## <a name="find-a-released-product-master"></a><span data-ttu-id="4ca2a-106">Een vrijgegeven productmodel zoeken</span><span class="sxs-lookup"><span data-stu-id="4ca2a-106">Find a released product master</span></span>
1. <span data-ttu-id="4ca2a-107">Ga naar Productgegevensbeheer > Producten > Vrijgegeven producten.</span><span class="sxs-lookup"><span data-stu-id="4ca2a-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="4ca2a-108">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="4ca2a-108">In the list, find and select the desired record.</span></span>

> [!NOTE]
> <span data-ttu-id="4ca2a-109">Een productmodel heeft Productmodel als Subtype van product.</span><span class="sxs-lookup"><span data-stu-id="4ca2a-109">A product master has the Product subtype Product master.</span></span>  

## <a name="update-the-lifecycle-state"></a><span data-ttu-id="4ca2a-110">De levenscyclusstatus bijwerken</span><span class="sxs-lookup"><span data-stu-id="4ca2a-110">Update the lifecycle state</span></span>
1. <span data-ttu-id="4ca2a-111">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="4ca2a-111">Click Edit.</span></span>
2. <span data-ttu-id="4ca2a-112">Typ of selecteer een waarde in het veld Levenscyclusstatus van product.</span><span class="sxs-lookup"><span data-stu-id="4ca2a-112">In the Product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="4ca2a-113">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="4ca2a-113">Click Save.</span></span>
4. <span data-ttu-id="4ca2a-114">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="4ca2a-114">Click Yes.</span></span>

> [!NOTE]
> <span data-ttu-id="4ca2a-115">Als u Ja selecteert, worden alle gerelateerde vrijgegeven productvarianten met dezelfde oorspronkelijke status als het vrijgegeven productmodel bijgewerkt naar de nieuwe levenscyclusstatus van het product.</span><span class="sxs-lookup"><span data-stu-id="4ca2a-115">If Yes is selected, all the related released product variants that have the same original status as the released product master are also updated to the new product lifecycle state.</span></span> <span data-ttu-id="4ca2a-116">Als u Nee selecteert, behouden alle varianten hun huidige status.</span><span class="sxs-lookup"><span data-stu-id="4ca2a-116">If No is selected, all variants keep their actual state.</span></span> <span data-ttu-id="4ca2a-117">Varianten met een andere status van productlevenscyclus dan het vrijgegeven productmodel worden niet bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="4ca2a-117">Variants that have a different product lifecycle state from the released product master are not updated.</span></span>  

## <a name="verify-the-lifecycle-state-of-the-variants"></a><span data-ttu-id="4ca2a-118">De levenscyclusstatus van de varianten controleren</span><span class="sxs-lookup"><span data-stu-id="4ca2a-118">Verify the lifecycle state of the variants</span></span>
1. <span data-ttu-id="4ca2a-119">Klik op Vrijgegeven Productvarianten.</span><span class="sxs-lookup"><span data-stu-id="4ca2a-119">Click Released product variants.</span></span>

> [!NOTE]
> <span data-ttu-id="4ca2a-120">Houd er rekening mee dat alle varianten de status van productlevenscyclus hebben overgenomen van het vrijgegeven productmodel.</span><span class="sxs-lookup"><span data-stu-id="4ca2a-120">Note that all variants have inherited the selected lifecycle state from the released product master.</span></span>  

2. <span data-ttu-id="4ca2a-121">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="4ca2a-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="4ca2a-122">Typ of selecteer een waarde in het veld Levenscyclusstatus van product.</span><span class="sxs-lookup"><span data-stu-id="4ca2a-122">In the Product lifecycle state field, enter or select a value.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]