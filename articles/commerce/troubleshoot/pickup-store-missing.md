---
title: Detailhandel wordt niet weergegeven in de lijst met winkels waarbij kan worden opgehaald
description: Dit onderwerp bevat richtlijnen voor het oplossen van problemen die kunnen helpen wanneer een detailhandelwinkel niet wordt weergegeven in de lijst met winkels waar artikelen kunnen worden opgehaald.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: ad7ddf8a17640471a2344c45eef76f682d29ef2b
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020813"
---
# <a name="retail-store-doesnt-appear-in-the-list-of-stores-to-pick-up-from"></a><span data-ttu-id="5bab6-103">Detailhandel wordt niet weergegeven in de lijst met winkels waarbij kan worden opgehaald</span><span class="sxs-lookup"><span data-stu-id="5bab6-103">Retail store doesn't appear in the list of stores to pick up from</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5bab6-104">Dit onderwerp bevat richtlijnen voor het oplossen van problemen die kunnen helpen wanneer een detailhandelwinkel niet wordt weergegeven in de lijst met winkels waar artikelen kunnen worden opgehaald.</span><span class="sxs-lookup"><span data-stu-id="5bab6-104">This topic provides troubleshooting guidance that can help when a retail store doesn't appear in the list of stores where items can be picked up.</span></span>

## <a name="description"></a><span data-ttu-id="5bab6-105">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="5bab6-105">Description</span></span>

<span data-ttu-id="5bab6-106">Een detailhandelwinkel wordt niet weergegeven in de lijst met winkels waar artikelen kunnen worden opgehaald.</span><span class="sxs-lookup"><span data-stu-id="5bab6-106">A retail store doesn't appear in the list of stores where items can be picked up.</span></span>

## <a name="resolution"></a><span data-ttu-id="5bab6-107">Oplossing</span><span class="sxs-lookup"><span data-stu-id="5bab6-107">Resolution</span></span>

### <a name="configure-the-longitude-and-latitude-for-the-store-address-in-commerce-headquarters"></a><span data-ttu-id="5bab6-108">De lengtegraad en breedtegraad configureren voor het winkeladres in Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="5bab6-108">Configure the longitude and latitude for the store address in Commerce headquarters</span></span>

<span data-ttu-id="5bab6-109">Voer deze stappen uit om de lengtegraad en breedtegraad te configureren voor het winkeladres in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="5bab6-109">To configure the longitude and latitude for the store address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="5bab6-110">Ga naar **Retail en Commerce \> Afzetkanalen \> Winkels \> Alle winkels**.</span><span class="sxs-lookup"><span data-stu-id="5bab6-110">Go to **Retail and Commerce \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="5bab6-111">Zoek de winkel die u wilt weergeven als ophaaloptie op de e-commercesite.</span><span class="sxs-lookup"><span data-stu-id="5bab6-111">Find the store that you want to appear among the pickup options on the e-commerce site.</span></span> <span data-ttu-id="5bab6-112">Noteer de waarde bij **Nummer van operationele eenheid**.</span><span class="sxs-lookup"><span data-stu-id="5bab6-112">Make a note of its **Operating unit number** value.</span></span>
1. <span data-ttu-id="5bab6-113">Ga naar **Organisatiebeheer \> Organisaties \> Operationele eenheden**.</span><span class="sxs-lookup"><span data-stu-id="5bab6-113">Go to **Organization administration \> Organizations \> Operating units**.</span></span>
1. <span data-ttu-id="5bab6-114">Zoek naar het nummer van de operationele eenheid dat u eerder hebt genoteerd en selecteer vervolgens de operationele eenheid in de zoekresultaten.</span><span class="sxs-lookup"><span data-stu-id="5bab6-114">Search for the operating unit number that you noted earlier, and then select the operating unit in the search results.</span></span>
1. <span data-ttu-id="5bab6-115">Selecteer op het sneltabblad **Adressen** de optie **Meer opties** en selecteer vervolgens **Geavanceerd**.</span><span class="sxs-lookup"><span data-stu-id="5bab6-115">On the **Addresses** FastTab, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="5bab6-116">Ga naar het sneltabblad **Algemeen** en zorg ervoor dat de velden **Lengtegraad** en **Breedtegraad** correct zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="5bab6-116">On the **General** FastTab, make sure that the **Longitude** and **Latitude** fields are correctly set.</span></span> <span data-ttu-id="5bab6-117">In deze stap controleert u of de waarden correct zijn opgegeven als positieve of negatieve getallen.</span><span class="sxs-lookup"><span data-stu-id="5bab6-117">As part of this step, make sure that the values are correctly specified as positive or negative numbers.</span></span>

### <a name="configure-fulfillment-groups-in-commerce-headquarters"></a><span data-ttu-id="5bab6-118">Afhandelingsgroepen configureren in Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="5bab6-118">Configure fulfillment groups in Commerce headquarters</span></span>

<span data-ttu-id="5bab6-119">Voer deze stappen uit om afhandelingsgroepen te configureren in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="5bab6-119">To configure fulfillment groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="5bab6-120">Ga naar **Retail en Commerce \> Afzetkanalen \> Online winkels**.</span><span class="sxs-lookup"><span data-stu-id="5bab6-120">Go to **Retail and Commerce \> Channels \> Online stores**.</span></span>
1. <span data-ttu-id="5bab6-121">Selecteer de online winkel die u wilt configureren.</span><span class="sxs-lookup"><span data-stu-id="5bab6-121">Select the online store to configure.</span></span>
1. <span data-ttu-id="5bab6-122">Selecteer in het actievenster de optie **Instellingen** en selecteer vervolgens **Toewijzing afhandelingsgroep**.</span><span class="sxs-lookup"><span data-stu-id="5bab6-122">On the Action Pane, select **Set up**, and then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="5bab6-123">Selecteer op de pagina **Toewijzing afhandelingsgroep** de afhandelingsgroep voor de online winkel.</span><span class="sxs-lookup"><span data-stu-id="5bab6-123">On the **Fulfillment group assignment** page, select the fulfillment group for the online store.</span></span>
1. <span data-ttu-id="5bab6-124">Zorg er onder **Instellingen** voor dat de detailhandelwinkel correct is geconfigureerd voor de afhandelingsgroep.</span><span class="sxs-lookup"><span data-stu-id="5bab6-124">Under **Setup**, make sure that the retail store is correctly configured for the fulfillment group.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5bab6-125">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="5bab6-125">Additional resources</span></span> 

[<span data-ttu-id="5bab6-126">Een operationele eenheid maken</span><span class="sxs-lookup"><span data-stu-id="5bab6-126">Create an operating unit</span></span>](../../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md)

[<span data-ttu-id="5bab6-127">Een online afzetkanaal instellen</span><span class="sxs-lookup"><span data-stu-id="5bab6-127">Set up an online channel</span></span>](../channel-setup-online.md)