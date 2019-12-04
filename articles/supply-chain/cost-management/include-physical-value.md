---
title: Fysieke waarde opnemen
description: U kunt het selectievakje Fysieke waarde opnemen op het sneltabblad Voorraadmodel van het formulier Artikelmodelgroepen gebruiken om op te geven of fysiek bijgewerkte transacties moeten worden meegenomen wanneer de actieve gemiddelde kostprijs van een artikel wordt berekend.
author: AndersGirke
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 79033
ms.assetid: 1928c145-bf82-436d-87ca-e7a173e31923
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 834438f8389e295bbb992f0b8397ff45559690c3
ms.sourcegitcommit: 92322167f57b66d2accc134aaf862e6b9931ec94
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/31/2019
ms.locfileid: "2692992"
---
# <a name="include-physical-value"></a><span data-ttu-id="1824e-103">Fysieke waarde opnemen</span><span class="sxs-lookup"><span data-stu-id="1824e-103">Include physical value</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1824e-104">U kunt het selectievakje Fysieke waarde opnemen op het sneltabblad Voorraadmodel van het formulier Artikelmodelgroepen gebruiken om op te geven of fysiek bijgewerkte transacties moeten worden meegenomen wanneer de actieve gemiddelde kostprijs van een artikel wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="1824e-104">You use the Include physical value check box on the Inventory model FastTab of the Item model groups page to specify whether physically updated transactions are considered when the running average cost price is calculated for an item.</span></span>

<span data-ttu-id="1824e-105">Het selectievakje **Fysieke waarde opnemen** heeft de volgende waarden.</span><span class="sxs-lookup"><span data-stu-id="1824e-105">The **Include physical value** check box has the following values.</span></span>

| <span data-ttu-id="1824e-106">Waarde</span><span class="sxs-lookup"><span data-stu-id="1824e-106">Value</span></span>    | <span data-ttu-id="1824e-107">Resultaat</span><span class="sxs-lookup"><span data-stu-id="1824e-107">Result</span></span>                                                                                                                          |
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1824e-108">Geselecteerd</span><span class="sxs-lookup"><span data-stu-id="1824e-108">Selected</span></span> | <span data-ttu-id="1824e-109">Zowel fysiek als financieel bijgewerkte transacties worden gebruikt om de actieve gemiddelde kostprijs te berekenen.</span><span class="sxs-lookup"><span data-stu-id="1824e-109">Both physically updated transactions and financially updated transactions are used to calculate the running average cost price.</span></span> |
| <span data-ttu-id="1824e-110">Uitgeschakeld</span><span class="sxs-lookup"><span data-stu-id="1824e-110">Cleared</span></span>  | <span data-ttu-id="1824e-111">Alleen financieel bijgewerkte transacties worden gebruikt om de actieve gemiddelde kostprijs te berekenen.</span><span class="sxs-lookup"><span data-stu-id="1824e-111">Only financially updated transactions are used to calculate the running average cost price.</span></span>                                     |

<span data-ttu-id="1824e-112">Het in- of uitschakelen van het selectievakje heeft enigszins verschillende resultaten, afhankelijk van het voorraadmodel dat u gebruikt.</span><span class="sxs-lookup"><span data-stu-id="1824e-112">The check box has slightly different effects, depending on the inventory model that you use.</span></span>

-   <span data-ttu-id="1824e-113">Als u het selectievakje **Fysieke waarde opnemen** inschakelt wanneer u het FIFO (First in, first out)-, LIFO (Last in, first out)- of LIFO-datumvoorraadmodel gebruikt, worden ook fysiek bijgewerkte transacties aangepast wanneer u de voorraad sluit.</span><span class="sxs-lookup"><span data-stu-id="1824e-113">If you select the **Include physical value** check box when you use the FIFO (First in, first out), LIFO (Last in, first out), or LIFO date inventory model, inventory close also makes adjustments to physically updated transactions.</span></span>
-   <span data-ttu-id="1824e-114">Als u het selectievakje **Fysieke waarde opnemen** niet inschakelt wanneer u deze voorraadmodellen gebruikt, worden alleen financieel bijgewerkte transacties vereffend wanneer u de voorraad sluit.</span><span class="sxs-lookup"><span data-stu-id="1824e-114">If you don't select the **Include physical value** check box when you use these inventory models, inventory close makes settlements only to financially updated transactions.</span></span>
-   <span data-ttu-id="1824e-115">Wanneer u het voorraadmodel gewogen gemiddelde of datum gewogen gemiddelde gebruikt, worden bij voorraadafsluiting altijd alleen financieel bijgewerkte transacties vereffend, ook al schakelt u het selectievakje **Fysieke waarde opnemen** in.</span><span class="sxs-lookup"><span data-stu-id="1824e-115">When you use the weighted average or weighted average date inventory model, inventory close settles only financially updated transactions, regardless of whether you select the **Include physical value** check box.</span></span>

<span data-ttu-id="1824e-116">**Voorbeeld 1** U hebt het selectievakje **Fysieke waarde opnemen** ingeschakeld en u ontvangt de volgende inkooporders:</span><span class="sxs-lookup"><span data-stu-id="1824e-116">**Example 1** You've selected the **Include physical value** check box and receive the following purchase orders:</span></span>

-   <span data-ttu-id="1824e-117">Een inkooporder voor 2 stuks tegen een kostprijs van EUR 10,00 die met de pakbon is bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="1824e-117">A purchase order for a quantity of 2 and a cost price of USD 10.00 that has been packing slip–updated.</span></span>
-   <span data-ttu-id="1824e-118">Een inkooporder voor 3 stuks tegen een kostprijs van EUR 12,00 die volgens de factuur is bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="1824e-118">A purchase order for a quantity of 3 and a cost price of USD 12.00 that has been invoice-updated.</span></span>

<span data-ttu-id="1824e-119">In dit geval zal de actieve gemiddelde kostprijs EUR 11,20 = (2x10+3x12)/(2+3) zijn omdat zowel fysiek als financieel bijgewerkte transacties worden gebruikt om de kostprijs te berekenen.</span><span class="sxs-lookup"><span data-stu-id="1824e-119">In this case, the running average cost price will be USD 11.20 = (2x10+3x12)/(2+3), because both physically updated transactions and financially updated transactions are used to calculate the cost price.</span></span> 

<span data-ttu-id="1824e-120">**Voorbeeld 2** U hebt het selectievakje **Fysieke waarde opnemen** niet ingeschakeld en de kostprijs in de artikelinstellingen is EUR 10,00.</span><span class="sxs-lookup"><span data-stu-id="1824e-120">**Example 2** You haven't selected the **Include physical value** check box, and the cost price on the item setup is USD 10.00.</span></span> 

-   <span data-ttu-id="1824e-121">U ontvangt een inkooporder voor 20 stuks tegen een kostprijs van EUR 12,00 die met de pakbon is bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="1824e-121">You receive a purchase order for a quantity of 20 and a cost price of USD 12.00 that has been packing slip–updated.</span></span>

<span data-ttu-id="1824e-122">Wanneer een verkooporder wordt geboekt, is de geboekte kostprijs EUR 10,00 omdat de actieve gemiddelde kostprijs geen fysiek geboekte transacties omvat.</span><span class="sxs-lookup"><span data-stu-id="1824e-122">When a sales order is posted, the posted cost amount is USD 10.00, because the running average cost price won't include physically posted transactions.</span></span> 

> [!NOTE]
> <span data-ttu-id="1824e-123">Ter vergelijking: als u het selectievakje **Fysieke waarde opnemen** voor dit artikel inschakelt wanneer een verkooporder wordt geboekt, is de geboekte kostprijs EUR 12,00.</span><span class="sxs-lookup"><span data-stu-id="1824e-123">For comparison, if you select the **Include physical value** check box for this item, when a sales order is posted, the posted cost amount will be USD 12.00.</span></span>
