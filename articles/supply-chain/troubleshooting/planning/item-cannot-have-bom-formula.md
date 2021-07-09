---
title: Een artikel kan geen stuklijst of formule hebben
description: Wanneer u een order probeert te valideren, wordt er tijdens het valideren van het artikel een foutbericht weergegeven. In die formule staat dat het artikel geen stuklijst of formule mag hebben.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6739b8b1e4d080055a2a0501427eac1c2e8a96c5
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294047"
---
# <a name="item-cant-have-a-bom-or-formula"></a><span data-ttu-id="cf81e-104">Een artikel kan geen stuklijst of formule hebben</span><span class="sxs-lookup"><span data-stu-id="cf81e-104">Item can't have a BOM or formula</span></span>

<span data-ttu-id="cf81e-105">Foutcode: PRO2614</span><span class="sxs-lookup"><span data-stu-id="cf81e-105">Error code: PRO2614</span></span>

## <a name="symptoms"></a><span data-ttu-id="cf81e-106">Symptomen</span><span class="sxs-lookup"><span data-stu-id="cf81e-106">Symptoms</span></span>

<span data-ttu-id="cf81e-107">Wanneer u een order probeert te valideren, wordt tijdens het valideren van het artikel het volgende foutbericht weergegeven:</span><span class="sxs-lookup"><span data-stu-id="cf81e-107">When you try to firm an order, you receive the following error message during item validation:</span></span>

> <span data-ttu-id="cf81e-108">Artikel kan geen stuklijst of formule hebben</span><span class="sxs-lookup"><span data-stu-id="cf81e-108">Item cannot have a BOM or formula</span></span>

## <a name="resolution"></a><span data-ttu-id="cf81e-109">Oplossing</span><span class="sxs-lookup"><span data-stu-id="cf81e-109">Resolution</span></span>

<span data-ttu-id="cf81e-110">Artikelen met een stuklijst of formule moeten van het type *Planningsartikel*, *Stuklijst* of *formule* zijn.</span><span class="sxs-lookup"><span data-stu-id="cf81e-110">Items that have a bill of materials (BOM) or formula must be of the *Planning item*, *BOM*, or *formula* type.</span></span> <span data-ttu-id="cf81e-111">Als u het type van een artikel wilt wijzigen, volgt u deze stappen.</span><span class="sxs-lookup"><span data-stu-id="cf81e-111">To change the type of an item, follow these steps.</span></span>

1. <span data-ttu-id="cf81e-112">Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="cf81e-112">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="cf81e-113">Open het relevante product.</span><span class="sxs-lookup"><span data-stu-id="cf81e-113">Open the relevant product.</span></span>
1. <span data-ttu-id="cf81e-114">Op het sneltabblad **Technicus** stelt u het veld **Productietype** in op *Planningsartikel*, *Stuklijst* of *formule*.</span><span class="sxs-lookup"><span data-stu-id="cf81e-114">On the **Engineer** FastTab, set the **Production type** field to *Planning item*, *BOM*, or *formula*.</span></span>
