---
title: Artikelen zonder voorraad kunnen worden uitgecheckt
description: Dit onderwerp biedt richtlijnen voor probleemoplossing die u kunnen helpen wanneer klanten artikelen uit voorraad aan hun winkelwagentje kunnen toevoegen en kunnen uitchecken.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 6df9c77248c7f4e16765b98327fe5838f0fce7e4
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585265"
---
# <a name="items-without-inventory-can-be-checked-out"></a><span data-ttu-id="c599a-103">Artikelen zonder voorraad kunnen worden uitgecheckt</span><span class="sxs-lookup"><span data-stu-id="c599a-103">Items without inventory can be checked out</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c599a-104">Dit onderwerp biedt richtlijnen voor probleemoplossing die u kunnen helpen wanneer klanten artikelen uit voorraad aan hun winkelwagentje kunnen toevoegen en kunnen uitchecken.</span><span class="sxs-lookup"><span data-stu-id="c599a-104">This topic provides troubleshooting guidance that can help when customers can add out-of-stock items to their cart and proceed to checkout.</span></span>

## <a name="description"></a><span data-ttu-id="c599a-105">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="c599a-105">Description</span></span>

<span data-ttu-id="c599a-106">Gebruikers kunnen een artikel aan hun winkelwagentje toevoegen, zelfs als er geen voorhanden voorraad is in de winkel, en vervolgens doorgaan naar de uitcheckpagina.</span><span class="sxs-lookup"><span data-stu-id="c599a-106">Users can add an item to their cart, even though there is no on-hand inventory in the store, and then proceed to the checkout page.</span></span>

## <a name="resolution"></a><span data-ttu-id="c599a-107">Oplossing</span><span class="sxs-lookup"><span data-stu-id="c599a-107">Resolution</span></span>

### <a name="enable-the-show-out-of-stock-errors-property-in-commerce-site-builder"></a><span data-ttu-id="c599a-108">De eigenschap Fouten voor niet op voorraad weergeven inschakelen in Commerce Site Builder</span><span class="sxs-lookup"><span data-stu-id="c599a-108">Enable the Show Out Of Stock Errors property in Commerce site builder</span></span>

<span data-ttu-id="c599a-109">Voer deze stappen uit om de eigenschap **Fouten voor niet op voorraad weergeven** inschakelen in Commerce Site Builder.</span><span class="sxs-lookup"><span data-stu-id="c599a-109">To enable the **Show Out Of Stock Errors** property in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="c599a-110">Selecteer de site waaraan u werkt.</span><span class="sxs-lookup"><span data-stu-id="c599a-110">Select the site that you're working on.</span></span>
1. <span data-ttu-id="c599a-111">Selecteer **Pagina's** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="c599a-111">In the left navigation, select **Pages**.</span></span>
1. <span data-ttu-id="c599a-112">Selecteer **CartPage** om deze te openen.</span><span class="sxs-lookup"><span data-stu-id="c599a-112">Select **CartPage** to open it.</span></span>
1. <span data-ttu-id="c599a-113">Selecteer het vak **Winkelwagen 1**, selecteer **Bewerken** en schakel vervolgens, in het eigenschappenvenster, het selectievakje **‭Fouten voor niet op voorraad weergeven** in.</span><span class="sxs-lookup"><span data-stu-id="c599a-113">Select the **Cart 1** slot, select **Edit**, and then, in the properties pane, select the **Show Out Of Stock Errors** check box.</span></span>
1. <span data-ttu-id="c599a-114">Sla de pagina op en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="c599a-114">Save and publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c599a-115">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="c599a-115">Additional resources</span></span>

[<span data-ttu-id="c599a-116">Voorraadinstellingen toepassen</span><span class="sxs-lookup"><span data-stu-id="c599a-116">Apply inventory settings</span></span>](../inventory-settings.md)

[<span data-ttu-id="c599a-117">Voorraadbeschikbaarheid voor Retail-kanalen berekenen</span><span class="sxs-lookup"><span data-stu-id="c599a-117">Calculate inventory availability for retail channels</span></span>](../calculated-inventory-retail-channels.md)

[<span data-ttu-id="c599a-118">Voorraadbuffers en voorraadniveaus configureren</span><span class="sxs-lookup"><span data-stu-id="c599a-118">Configure inventory buffers and inventory levels</span></span>](../inventory-buffers-levels.md)
