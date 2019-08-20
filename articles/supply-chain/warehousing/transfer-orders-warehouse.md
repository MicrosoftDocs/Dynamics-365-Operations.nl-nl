---
title: Magazijnen voor overboekingsorders instellen
description: In dit onderwerp wordt beschreven hoe u magazijnen voor transferorders kunt instellen.
author: Mirzaab
manager: AnnBe
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 91db6e8f921bd674211f6d478b6d0f0a832c983c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847010"
---
# <a name="set-up-warehouses-for-transfer-orders"></a><span data-ttu-id="1d41e-103">Magazijnen voor overboekingsorders instellen</span><span class="sxs-lookup"><span data-stu-id="1d41e-103">Set up warehouses for transfer orders</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1d41e-104">Met magazijnniveaus kunt u een hiërarchie maken die transferorders tussen magazijnen ondersteunt.</span><span class="sxs-lookup"><span data-stu-id="1d41e-104">You can use warehouse levels to create a hierarchy that supports transfer orders between warehouses.</span></span> <span data-ttu-id="1d41e-105">Op basis van deze instelling worden met de hoofdplanning artikelbehoeften op het afzonderlijke magazijnniveau berekend en worden geplande transferorders vanuit een toegewezen bronmagazijn voor aanvullen gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="1d41e-105">Based on this setup, master scheduling calculates item requirements at the individual warehouse level and generates planned transfer orders from an assigned source warehouse to fulfill them.</span></span>

1.  <span data-ttu-id="1d41e-106">Klik op **Voorraadbeheer > Instellingen > Opsplitsing van voorraad > Magazijnen**.</span><span class="sxs-lookup"><span data-stu-id="1d41e-106">Click **Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>

2.  <span data-ttu-id="1d41e-107">Selecteer het magazijn dat u wilt aanvullen.</span><span class="sxs-lookup"><span data-stu-id="1d41e-107">Select the warehouse that you want to refill.</span></span>

3.  <span data-ttu-id="1d41e-108">Kies op het sneltabblad **Hoofdplanning** het selectievakje **Aanvullen**.</span><span class="sxs-lookup"><span data-stu-id="1d41e-108">On the **Master planning** FastTab, select the **Refilling** check box.</span></span>

4.  <span data-ttu-id="1d41e-109">Selecteer in het veld **Hoofdmagazijn** het magazijn dat u wilt toewijzen als het magazijn voor aanvullen.</span><span class="sxs-lookup"><span data-stu-id="1d41e-109">In the **Main warehouse** field, select the warehouse that you want to assign as the refilling warehouse.</span></span> <span data-ttu-id="1d41e-110">Bij de hoofdplanning wordt een transferbehoefte voor het geselecteerde magazijn berekend en wordt een geplande transferorder vanuit het toegewezen **Hoofdmagazijn** gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="1d41e-110">Master scheduling calculates a transfer requirement for the selected warehouse and generates a planned transfer order from the assigned **Main warehouse**.</span></span>
   
    > [!NOTE]
    > <P><span data-ttu-id="1d41e-111">Als u het veld <STRONG>Aanvullen</STRONG> leegmaakt, wordt aan het geselecteerde magazijn een magazijnniveau met betrekking tot het <STRONG>Hoofdmagazijn</STRONG> toegewezen, maar wordt het <STRONG>Hoofdmagazijn</STRONG> niet als aanvullingsmagazijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="1d41e-111">If you clear the <STRONG>Refilling</STRONG> check box, the selected warehouse is assigned a warehouse level in regard to the <STRONG>Main warehouse</STRONG>, but the <STRONG>Main warehouse</STRONG> is not set up as a refilling warehouse.</span></span></P>

5.  <span data-ttu-id="1d41e-112">Sluit de pagina om de nieuwe instellingen toe te passen.</span><span class="sxs-lookup"><span data-stu-id="1d41e-112">Close the page to apply the new setup.</span></span>


> [!TIP]
> <P><span data-ttu-id="1d41e-113">Als u een magazijn voor aanvullen wilt toewijzen, moet u eerst het magazijn in de pagina <STRONG>Opslagdimensiegroepen</STRONG> als een opslagdimensie instellen.</span><span class="sxs-lookup"><span data-stu-id="1d41e-113">If you want to assign a warehouse for refilling, you must first set up the warehouse as a storage dimension on the <STRONG>Storage dimension groups</STRONG> page.</span></span> <span data-ttu-id="1d41e-114">Op deze pagina selecteert u het veld <STRONG>Actief</STRONG> en het veld <STRONG>Behoefteplan per dimensie</STRONG> voor het magazijn.</span><span class="sxs-lookup"><span data-stu-id="1d41e-114">On this page, select the <STRONG>Active</STRONG> field and the <STRONG>Coverage plan by dimension</STRONG> field for the warehouse.</span></span></P>

## <a name="set-up-transport-lead-time"></a><span data-ttu-id="1d41e-115">Doorlooptijd voor transport instellen</span><span class="sxs-lookup"><span data-stu-id="1d41e-115">Set up transport lead time</span></span>

<span data-ttu-id="1d41e-116">U moet ook de doorlooptijd voor het transport tussen de magazijnen instellen op de pagina **Transportdagen**.</span><span class="sxs-lookup"><span data-stu-id="1d41e-116">You must also set up the transport lead time between the warehouses on the **Transport days** page.</span></span> 
1. <span data-ttu-id="1d41e-117">Ga naar **Voorraadbeheer > instellingen > Distributie > Transportdagen**.</span><span class="sxs-lookup"><span data-stu-id="1d41e-117">Go to **Inventory management > Setup > Distribution > Transport days**.</span></span>
2. <span data-ttu-id="1d41e-118">Selecteer in het veld **Plaats van ontvangst** **Magazijn**.</span><span class="sxs-lookup"><span data-stu-id="1d41e-118">In the **Receiving point** field, select **warehouse**.</span></span>
3. <span data-ttu-id="1d41e-119">Selecteer het **Magazijn van verzending**, **Magazijn van ontvangst**, en **Transportdagen**.</span><span class="sxs-lookup"><span data-stu-id="1d41e-119">Select the **Shipping warehouse**, **Receiving warehouse**, and **Transport days**.</span></span> 
4. <span data-ttu-id="1d41e-120">(Optioneel) U kunt ook de transporttijd, afhankelijk van de leveringsmethode, onder het tabblad **Transportdagen per leveringsmethode** instellen.</span><span class="sxs-lookup"><span data-stu-id="1d41e-120">(Optional) You can also set transport time, depending on the mode of delivery, under the **Transport days per mode of delivery** tab.</span></span>
