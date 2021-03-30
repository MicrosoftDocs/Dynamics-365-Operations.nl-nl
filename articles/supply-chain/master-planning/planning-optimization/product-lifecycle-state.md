---
title: Producten met specifieke levenscyclusstatussen uitsluiten
description: In dit onderwerp wordt uitgelegd hoe u producten opneemt op basis van de levenscyclusstatus wanneer de functie Planningsoptimalisatie wordt gebruikt.
author: ChristianRytt
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-13
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a1e0c734db763ffa69e2d6540a07d5fa04c22ea1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227812"
---
# <a name="exclude-products-that-have-specific-product-lifecycle-states"></a><span data-ttu-id="e9a02-103">Producten met specifieke levenscyclusstatussen uitsluiten</span><span class="sxs-lookup"><span data-stu-id="e9a02-103">Exclude products that have specific product lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e9a02-104">Vrijgegeven producten en vrijgegeven productversies bevatten een veld **Levenscyclusstatus van het product**.</span><span class="sxs-lookup"><span data-stu-id="e9a02-104">Released products and released product versions include a **Product lifecycle state** field.</span></span> <span data-ttu-id="e9a02-105">Met dit veld kunt u onder andere bepalen welke producten in de hoofdplanning worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="e9a02-105">This field lets you control, among other things, which products are included during master planning.</span></span> <span data-ttu-id="e9a02-106">U kunt de levenscyclusstatussen naar wens toevoegen, verwijderen en bewerken door naar **Productgegevensbeheer \> Instellingen \> Levenscyclusstatus van het product** te gaan.</span><span class="sxs-lookup"><span data-stu-id="e9a02-106">You can add, remove, and edit lifecycle states as required by going to **Product information management \> Setup \> Product lifecycle state**.</span></span> <span data-ttu-id="e9a02-107">Stel voor elke levenscyclusstatus de optie **Is actief voor planning** op *Ja* als producten met die status moeten worden opgenomen in de hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="e9a02-107">For each product lifecycle state, set the **Is active for planning** option to *Yes* if products that have that state should be included during master planning.</span></span> <span data-ttu-id="e9a02-108">Wanneer de optie is ingesteld op *Nee*, worden de gekoppelde producten en varianten uitgesloten van alle hoofdplanningen en alle berekeningen op stuklijstniveau.</span><span class="sxs-lookup"><span data-stu-id="e9a02-108">When the option is set to *No*, the associated products and variants will be excluded from all master planning and all calculations at the bill of materials (BOM) level.</span></span>

<span data-ttu-id="e9a02-109">Vrijgegeven producten en varianten waarbij het veld **Levenscyclusstatus van het product** leeg is gelaten, worden verwerkt alsof ze een levenscyclusstatus hebben waarbij de optie **Is actief voor planning** is ingesteld op *Ja*.</span><span class="sxs-lookup"><span data-stu-id="e9a02-109">Released products and variants where the **Product lifecycle state** field is left blank are treated as though they have a product lifecycle state where the **Is active for planning** option is set to *Yes*.</span></span> <span data-ttu-id="e9a02-110">Met andere woorden, deze worden opgenomen in de hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="e9a02-110">In other words, they will be included during master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="e9a02-111">Om onnodige aanbodvoorstellen te voorkomen, raden we u aan om alle verouderde vrijgegeven producten en varianten te koppelen aan de productlevenscyclusstatus waarvoor de optie **Is actief voor planning** is ingesteld op *Nee*.</span><span class="sxs-lookup"><span data-stu-id="e9a02-111">To help avoid unnecessary supply suggestions, we strongly recommend that you associate all obsolete released products and variants with a product lifecycle state where the **Is active for planning** option is set to *No*.</span></span> <span data-ttu-id="e9a02-112">Deze aanpak is met name belangrijk wanneer u werkt met product configuratievarianten die niet herbruikbaar zijn, omdat u hiermee afval kunt voorkomen.</span><span class="sxs-lookup"><span data-stu-id="e9a02-112">This approach is especially important when you work with product configuration variants that aren't reusable, because it will help prevent waste.</span></span>

## <a name="related-resources"></a><span data-ttu-id="e9a02-113">Gerelateerde bronnen</span><span class="sxs-lookup"><span data-stu-id="e9a02-113">Related resources</span></span>

<span data-ttu-id="e9a02-114">Zie [Overzicht van Levenscyclusstatus van producten](../../pim/product-lifecycle.md) voor meer informatie over levenscyclusstatussen van producten.</span><span class="sxs-lookup"><span data-stu-id="e9a02-114">For more information about product lifecycle states, see [Product lifecycle state overview](../../pim/product-lifecycle.md).</span></span>

<span data-ttu-id="e9a02-115">Voor gedetailleerde informatie, waaronder stappen voor het gebruik van productlevenscyclusstatussen om producten uit te sluiten van de hoofdplanning en berekeningen op stuklijstniveau, gaat u naar [Een status voor de productlevenscyclus maken om producten uit te sluiten van Hoofdplanning](../../pim/tasks/exclude-products-master-planning.md).</span><span class="sxs-lookup"><span data-stu-id="e9a02-115">For detailed information that includes steps for using product lifecycle states to exclude products from master planning and BOM-level calculations, see [Create a product lifecycle state to exclude products from Master planning](../../pim/tasks/exclude-products-master-planning.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]