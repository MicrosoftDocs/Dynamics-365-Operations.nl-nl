---
title: Een status voor de productlevenscyclus maken om producten uit te sluiten van Hoofdplanning
description: Deze procedure laat zien hoe u een nieuwe status van de productlevenscyclus maakt die de producten uitsluit van de hoofdplanning en berekening op stuklijstniveau.
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
ms.openlocfilehash: cadf1d812e737309dbe8ca26d04ffb1ee88ef16a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818032"
---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a><span data-ttu-id="de6d0-103">Een status voor de productlevenscyclus maken om producten uit te sluiten van Hoofdplanning</span><span class="sxs-lookup"><span data-stu-id="de6d0-103">Create a product lifecycle state to exclude products from Master planning</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="de6d0-104">Deze procedure laat zien hoe u een nieuwe status van de productlevenscyclus maakt die de producten uitsluit van de hoofdplanning en berekening op stuklijstniveau.</span><span class="sxs-lookup"><span data-stu-id="de6d0-104">This procedure shows how to create a new product lifecycle state that excludes the products from Master planning and BOM-level calculation.</span></span>


## <a name="create-an-obsolete-state"></a><span data-ttu-id="de6d0-105">Een verouderde status maken</span><span class="sxs-lookup"><span data-stu-id="de6d0-105">Create an obsolete state</span></span>
1. <span data-ttu-id="de6d0-106">Ga naar Productgegevensbeheer > Instellen > Levenscyclusstatus van product.</span><span class="sxs-lookup"><span data-stu-id="de6d0-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="de6d0-107">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="de6d0-107">Click New.</span></span>
3. <span data-ttu-id="de6d0-108">Typ een waarde in het veld Status.</span><span class="sxs-lookup"><span data-stu-id="de6d0-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="de6d0-109">Selecteer Nee in het veld Is actief voor planning.</span><span class="sxs-lookup"><span data-stu-id="de6d0-109">Select No in the Is active for planning field.</span></span>
5. <span data-ttu-id="de6d0-110">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="de6d0-110">In the Description field, type a value.</span></span>

## <a name="associate-the-obsolete-state-to-a-released-product"></a><span data-ttu-id="de6d0-111">De verouderde status koppelen aan een vrijgegeven product</span><span class="sxs-lookup"><span data-stu-id="de6d0-111">Associate the obsolete state to a released product</span></span>
1. <span data-ttu-id="de6d0-112">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="de6d0-112">Close the page.</span></span>
2. <span data-ttu-id="de6d0-113">Ga naar Productgegevensbeheer > Producten > Vrijgegeven producten.</span><span class="sxs-lookup"><span data-stu-id="de6d0-113">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="de6d0-114">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="de6d0-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="de6d0-115">Filter bijvoorbeeld op het veld Zoeknaam met de waarde 'M00'.</span><span class="sxs-lookup"><span data-stu-id="de6d0-115">For example, filter on the Search name field with a value of 'M00'.</span></span>
4. <span data-ttu-id="de6d0-116">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="de6d0-116">Click Edit.</span></span>
5. <span data-ttu-id="de6d0-117">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="de6d0-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="de6d0-118">Typ of selecteer een waarde in het veld Levenscyclusstatus van product.</span><span class="sxs-lookup"><span data-stu-id="de6d0-118">In the Product lifecycle state field, enter or select a value.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]