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
ms.openlocfilehash: 8a9f8f519c54ffe4f1a2a44da51ac5d97c56182a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992215"
---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a><span data-ttu-id="49a86-103">Een status voor de productlevenscyclus toewijzen aan een vrijgegeven productmodel</span><span class="sxs-lookup"><span data-stu-id="49a86-103">Assign a product lifecycle state to a released product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="49a86-104">Deze procedure laat zien hoe u een status van productlevenscyclus toewijst aan een vrijgegeven productmodel en de bijbehorende varianten.</span><span class="sxs-lookup"><span data-stu-id="49a86-104">This procedure shows how to assign a product lifecycle state to a released product master and its variants.</span></span> <span data-ttu-id="49a86-105">Vereiste: U moet eerst de guide "Een nieuwe status voor de productlevenscyclus maken" afspelen om ervoor te zorgen dat er minimaal één status van productlevenscyclus is gemaakt voordat u deze guide kunt afspelen.</span><span class="sxs-lookup"><span data-stu-id="49a86-105">Prerequisite: You need to play the task guide "Create a new product lifecycle state" first to make sure that you have at least one product lifecycle state created before you can play this task guide.</span></span>


## <a name="find-a-released-product-master"></a><span data-ttu-id="49a86-106">Een vrijgegeven productmodel zoeken</span><span class="sxs-lookup"><span data-stu-id="49a86-106">Find a released product master</span></span>
1. <span data-ttu-id="49a86-107">Ga naar Productgegevensbeheer > Producten > Vrijgegeven producten.</span><span class="sxs-lookup"><span data-stu-id="49a86-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="49a86-108">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="49a86-108">In the list, find and select the desired record.</span></span>

> [!NOTE]
> <span data-ttu-id="49a86-109">Een productmodel heeft Productmodel als Subtype van product.</span><span class="sxs-lookup"><span data-stu-id="49a86-109">A product master has the Product subtype Product master.</span></span>  

## <a name="update-the-lifecycle-state"></a><span data-ttu-id="49a86-110">De levenscyclusstatus bijwerken</span><span class="sxs-lookup"><span data-stu-id="49a86-110">Update the lifecycle state</span></span>
1. <span data-ttu-id="49a86-111">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="49a86-111">Click Edit.</span></span>
2. <span data-ttu-id="49a86-112">Typ of selecteer een waarde in het veld Levenscyclusstatus van product.</span><span class="sxs-lookup"><span data-stu-id="49a86-112">In the Product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="49a86-113">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="49a86-113">Click Save.</span></span>
4. <span data-ttu-id="49a86-114">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="49a86-114">Click Yes.</span></span>

> [!NOTE]
> <span data-ttu-id="49a86-115">Als u Ja selecteert, worden alle gerelateerde vrijgegeven productvarianten met dezelfde oorspronkelijke status als het vrijgegeven productmodel bijgewerkt naar de nieuwe levenscyclusstatus van het product.</span><span class="sxs-lookup"><span data-stu-id="49a86-115">If Yes is selected, all the related released product variants that have the same original status as the released product master are also updated to the new product lifecycle state.</span></span> <span data-ttu-id="49a86-116">Als u Nee selecteert, behouden alle varianten hun huidige status.</span><span class="sxs-lookup"><span data-stu-id="49a86-116">If No is selected, all variants keep their actual state.</span></span> <span data-ttu-id="49a86-117">Varianten met een andere status van productlevenscyclus dan het vrijgegeven productmodel worden niet bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="49a86-117">Variants that have a different product lifecycle state from the released product master are not updated.</span></span>  

## <a name="verify-the-lifecycle-state-of-the-variants"></a><span data-ttu-id="49a86-118">De levenscyclusstatus van de varianten controleren</span><span class="sxs-lookup"><span data-stu-id="49a86-118">Verify the lifecycle state of the variants</span></span>
1. <span data-ttu-id="49a86-119">Klik op Vrijgegeven Productvarianten.</span><span class="sxs-lookup"><span data-stu-id="49a86-119">Click Released product variants.</span></span>

> [!NOTE]
> <span data-ttu-id="49a86-120">Houd er rekening mee dat alle varianten de status van productlevenscyclus hebben overgenomen van het vrijgegeven productmodel.</span><span class="sxs-lookup"><span data-stu-id="49a86-120">Note that all variants have inherited the selected lifecycle state from the released product master.</span></span>  

2. <span data-ttu-id="49a86-121">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="49a86-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="49a86-122">Typ of selecteer een waarde in het veld Levenscyclusstatus van product.</span><span class="sxs-lookup"><span data-stu-id="49a86-122">In the Product lifecycle state field, enter or select a value.</span></span>

