---
title: Dimensieleden van kostenelement toewijzen aan een gemeenschappelijke set van dimensieleden
description: Door verschillende kostenelementendimensieleden aan een gemeenschappelijke set kostenelementendimensieleden toe te wijzen, kunt u gegevens samenvoegen in een gemeenschappelijke indeling ten behoeve van analyse.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: deb9b5aab9cd69270c78d4e1ea0e2a6cac6ac370
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177167"
---
# <a name="map-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a><span data-ttu-id="62c83-103">Dimensieleden van kostenelement toewijzen aan een gemeenschappelijke set van dimensieleden</span><span class="sxs-lookup"><span data-stu-id="62c83-103">Map cost element dimension members to a common set of dimension members</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="62c83-104">Door verschillende kostenelementendimensieleden aan een gemeenschappelijke set kostenelementendimensieleden toe te wijzen, kunt u gegevens samenvoegen in een gemeenschappelijke indeling ten behoeve van analyse.</span><span class="sxs-lookup"><span data-stu-id="62c83-104">By mapping different cost element dimension members to a common set of cost element dimension members, you merge data into a common format for analysis purposes.</span></span>

<span data-ttu-id="62c83-105">Als uw bedrijf wereldwijd actief is en de wettelijke boekhoudvereisten naleeft, maakt u mogelijk gebruik van meerdere rekeningschema's.</span><span class="sxs-lookup"><span data-stu-id="62c83-105">If you're a global company and comply with statutory accounting requirements, you might use multiple charts of accounts.</span></span> <span data-ttu-id="62c83-106">Wanneer u kostenelementendimensieleden uit verschillende rekeningschema's importeert, kan het resultaat een wirwar van rekeningen zijn.</span><span class="sxs-lookup"><span data-stu-id="62c83-106">When you import cost element dimension members from different charts of accounts, you can end up with a mix of accounts.</span></span> <span data-ttu-id="62c83-107">Maar deze rekeningen kunnen dezelfde aard hebben, en u wilt misschien de kosten voor deze rekeningen analyseren en toewijzen met behulp van een gemeenschappelijke indeling.</span><span class="sxs-lookup"><span data-stu-id="62c83-107">However, these accounts might actually have the same nature, and you might want to analyze and allocate costs for them by using a common format.</span></span>

## <a name="map-cost-element-dimension-members-to-a-common-format"></a><span data-ttu-id="62c83-108">Kostenelementdimensieleden toewijzen aan een gemeenschappelijke indeling</span><span class="sxs-lookup"><span data-stu-id="62c83-108">Map cost element dimension members to a common format</span></span>
<span data-ttu-id="62c83-109">In het volgende voorbeeld wordt getoond hoe u als kostencontroller een nieuwe kostenelementendimensie aanmaakt in Kostprijsboekhouding. Deze dimensie wijst kostenelementendimensieleden van het Amerikaanse rekeningschemastructuur en de Franse rekeningschemastructuur toe aan een gemeenschappelijke set kostenelementdimensieleden.</span><span class="sxs-lookup"><span data-stu-id="62c83-109">The following example shows how you, as a cost controller, can create a new cost element dimension in Cost accounting that maps cost element dimension members from the US chart of accounts structure and the French chart of accounts structure to a common set of cost element dimension members.</span></span> <span data-ttu-id="62c83-110">U kunt vervolgens met de gemeenschappelijke set kostenelementendimensieleden kostengegevens van de twee rechtspersonen analyseren in een kostprijsboekhoudinggrootboek.</span><span class="sxs-lookup"><span data-stu-id="62c83-110">You can then use the common set of cost element dimension members to analyze cost data from the two legal entities in a cost accounting ledger.</span></span>

| <span data-ttu-id="62c83-111">Bron: Amerikaans rekeningschema</span><span class="sxs-lookup"><span data-stu-id="62c83-111">Source: US chart of accounts</span></span>                                          | <span data-ttu-id="62c83-112">Bron: Frans rekeningschema</span><span class="sxs-lookup"><span data-stu-id="62c83-112">Source: French chart of accounts</span></span>                                          | <span data-ttu-id="62c83-113">Nieuwe gemeenschappelijke set kostenelementendimensieleden</span><span class="sxs-lookup"><span data-stu-id="62c83-113">New common set of cost element dimension members</span></span>                        |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="62c83-114">Geïmporteerde kostenelementendimensieleden van het Amerikaanse rekeningschema.</span><span class="sxs-lookup"><span data-stu-id="62c83-114">Imported cost element dimension members from the US chart of accounts</span></span> | <span data-ttu-id="62c83-115">Geïmporteerde kostenelementendimensieleden van het Franse rekeningschema.</span><span class="sxs-lookup"><span data-stu-id="62c83-115">Imported cost element dimension members from the French chart of accounts</span></span> | <span data-ttu-id="62c83-116">Toewijzing van de Franse en Amerikaanse kostenelementendimensieleden aan een gemeenschappelijke set</span><span class="sxs-lookup"><span data-stu-id="62c83-116">Mapping of US and French cost element dimension members to a common set</span></span> |
| <span data-ttu-id="62c83-117">5001: Verkoop</span><span class="sxs-lookup"><span data-stu-id="62c83-117">5001: Sales</span></span>                                                           | <span data-ttu-id="62c83-118">5001: Verkoop en advertenties</span><span class="sxs-lookup"><span data-stu-id="62c83-118">5001: Sales and advertising</span></span>                                               | <span data-ttu-id="62c83-119">5000: Verkoop en advertenties</span><span class="sxs-lookup"><span data-stu-id="62c83-119">5000: Sales and advertising</span></span>                                             |
| <span data-ttu-id="62c83-120">5030: Advertenties</span><span class="sxs-lookup"><span data-stu-id="62c83-120">5030: Advertising</span></span>                                                     | <span data-ttu-id="62c83-121">6390: Voorraadinkoop\*</span><span class="sxs-lookup"><span data-stu-id="62c83-121">6390: Stock purchase\*</span></span>                                                    | <span data-ttu-id="62c83-122">7000: Schoonmaakkosten</span><span class="sxs-lookup"><span data-stu-id="62c83-122">7000: Cleaning expenses</span></span>                                                 |
| <span data-ttu-id="62c83-123">7001: Schoonmaakkosten</span><span class="sxs-lookup"><span data-stu-id="62c83-123">7001: Cleaning expenses</span></span>                                               | <span data-ttu-id="62c83-124">7001: Reiskosten</span><span class="sxs-lookup"><span data-stu-id="62c83-124">7001: Travel expense</span></span>                                                      | <span data-ttu-id="62c83-125">7001: Reiskosten</span><span class="sxs-lookup"><span data-stu-id="62c83-125">7001: Travel expenses</span></span>                                                   |

<span data-ttu-id="62c83-126">\*Het Franse kostenelementdimensielid Voorraadinkoop is niet toegewezen.</span><span class="sxs-lookup"><span data-stu-id="62c83-126">\*The Stock purchase French cost element dimension member isn't mapped.</span></span>

## <a name="currency-conversion"></a><span data-ttu-id="62c83-127">Valutaomrekening</span><span class="sxs-lookup"><span data-stu-id="62c83-127">Currency conversion</span></span>
<span data-ttu-id="62c83-128">De verschillende rekeningschema's die u gebruikt zijn mogelijk ingesteld voor verschillende valuta's.</span><span class="sxs-lookup"><span data-stu-id="62c83-128">The various charts of accounts that you use might be set up to use different currencies.</span></span> <span data-ttu-id="62c83-129">Specificeer in dit geval een valutaomrekening, zodat de kostengegevens worden verwerkt met de juiste valuta zoals is gedefinieerd in het kostenboekhoudingsgrootboek waarin de kostenelementdimensieleden worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="62c83-129">In this case, be sure to specify a currency conversion, so that cost data is processed by using the correct currency, as defined in the cost accounting ledger where the cost element dimension members are used.</span></span> <span data-ttu-id="62c83-130">In het voorafgaande voorbeeld geldt dat als Amerikaanse dollars (USD) worden gebruikt in het kostprijsboekhoudinggrootboek, u een valutaomrekening moet maken van USD naar euro's (EUR) om transacties voor de toegewezen kostenelementdimensieleden te kunnen verwerken.</span><span class="sxs-lookup"><span data-stu-id="62c83-130">In the preceding example, if US dollars (USD) are used in the cost accounting ledger, you must create a currency conversion from USD to euros (EUR) to process transactions for the mapped cost element dimension members.</span></span>

## <a name="update-mappings-at-any-time"></a><span data-ttu-id="62c83-131">Toewijzingen op elk gewenst moment bijwerken</span><span class="sxs-lookup"><span data-stu-id="62c83-131">Update mappings at any time</span></span>
<span data-ttu-id="62c83-132">U kunt de toewijzingsdefinities voor een kostenelementendimensie op elk gewenst moment bijwerken.</span><span class="sxs-lookup"><span data-stu-id="62c83-132">You can update the mapping definitions for a cost element dimension at any time.</span></span> <span data-ttu-id="62c83-133">Omdat de toewijzingen niet beïnvloed worden door de datum, worden wijzigingen toegepast bij de volgende keer dat u kostentransacties verwerkt of kostenberekeningen uitvoert.</span><span class="sxs-lookup"><span data-stu-id="62c83-133">Because mappings aren't date-effective, changes are applied the next time that you process cost transactions or run cost calculations.</span></span>


