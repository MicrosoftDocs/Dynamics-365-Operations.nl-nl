---
title: Er is geen begindatumwaarde op het tabblad Actieve prijzen van de pagina Artikelprijs
description: Er is geen begindatumwaarde op het tabblad Actieve prijzen van de pagina Artikelprijs.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dd13f6a3e5ce3c894e96f420358d337f2e43dba
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026420"
---
# <a name="there-is-no-from-date-value-on-the-active-prices-tab-of-the-item-price-page"></a><span data-ttu-id="8c1f2-103">Er is geen begindatumwaarde op het tabblad Actieve prijzen van de pagina Artikelprijs</span><span class="sxs-lookup"><span data-stu-id="8c1f2-103">There is no From date value on the Active prices tab of the Item price page</span></span>

<span data-ttu-id="8c1f2-104">KB-nummer: 4613548</span><span class="sxs-lookup"><span data-stu-id="8c1f2-104">KB number: 4613548</span></span>

## <a name="symptoms"></a><span data-ttu-id="8c1f2-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="8c1f2-105">Symptoms</span></span>

<span data-ttu-id="8c1f2-106">Er is geen waarde bij **Begindatum** op het tabblad **Actieve prijzen** van de pagina **Artikelprijs**.</span><span class="sxs-lookup"><span data-stu-id="8c1f2-106">There is no **From date** value on the **Active prices** tab of the **Item price** page.</span></span>

## <a name="resolution"></a><span data-ttu-id="8c1f2-107">Oplossing</span><span class="sxs-lookup"><span data-stu-id="8c1f2-107">Resolution</span></span>

<span data-ttu-id="8c1f2-108">De waarde van **Begindatum** (ingangsdatum) die is ingesteld op de prijs in behandeling is niet overgezet naar de actieve prijs.</span><span class="sxs-lookup"><span data-stu-id="8c1f2-108">The **From date** value (effective date) that is set on the pending price isn't transferred to the active price.</span></span>

<span data-ttu-id="8c1f2-109">Een artikelkostenrecord wordt eerst ingevoerd met de status *In behandeling* en met een gewenste ingangsdatum.</span><span class="sxs-lookup"><span data-stu-id="8c1f2-109">When an item cost record is first entered, it has a status of *Pending* and an intended effective date.</span></span> <span data-ttu-id="8c1f2-110">Als u de artikelkostenrecord activeert, wordt de status naar *Actief* en de begindatum naar de activeringsdatum bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="8c1f2-110">When you activate the item cost record, the status is updated to *Active*, and the effective date is updated to the activation date.</span></span> <span data-ttu-id="8c1f2-111">Daarom is de activeringsdatum van de actieve prijs altijd de werkelijke datum van de activering.</span><span class="sxs-lookup"><span data-stu-id="8c1f2-111">Therefore, the active price's activation date is always the actual date of the activation.</span></span>

<span data-ttu-id="8c1f2-112">Zie [Overzicht van Kostprijsberekeningsversies](../../cost-management/costing-versions.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="8c1f2-112">For more information, see [Costing versions overview](../../cost-management/costing-versions.md).</span></span>
