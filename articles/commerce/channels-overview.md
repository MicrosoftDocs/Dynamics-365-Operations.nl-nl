---
title: Overzicht van kanalen
description: Dit onderwerp geeft een overzicht van afzetkanalen in Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 099ccd9f769ea5c431c1a82532d8654cbbd082b1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002353"
---
# <a name="channels-overview"></a><span data-ttu-id="00b9c-103">Overzicht van kanalen</span><span class="sxs-lookup"><span data-stu-id="00b9c-103">Channels overview</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="00b9c-104">Dit onderwerp geeft een overzicht van afzetkanalen in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="00b9c-104">This topic presents an overview of channels in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="00b9c-105">Het bevat informatie over de taken die u vóór en na het instellen van elk afzetkanaal moet uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="00b9c-105">It includes information about the tasks that you must complete both before and after you set up each channel.</span></span>

## <a name="types-of-channels"></a><span data-ttu-id="00b9c-106">Typen afzetkanalen</span><span class="sxs-lookup"><span data-stu-id="00b9c-106">Types of Channels</span></span>

<span data-ttu-id="00b9c-107">Dynamics 365 Commerce ondersteunt drie verschillende afzetkanaaltypen: detailhandel, callcenter en online.</span><span class="sxs-lookup"><span data-stu-id="00b9c-107">Dynamics 365 Commerce supports three different channel types: retail, call center, and online channels.</span></span>

### <a name="retail-channels"></a><span data-ttu-id="00b9c-108">Detailhandelafzetkanalen</span><span class="sxs-lookup"><span data-stu-id="00b9c-108">Retail channels</span></span>

<span data-ttu-id="00b9c-109">Detailhandelkanalen zijn de standaard fysieke winkels.</span><span class="sxs-lookup"><span data-stu-id="00b9c-109">Retail channels represent standard brick-and-mortar stores.</span></span> <span data-ttu-id="00b9c-110">Iedere winkel kan zijn eigen POS-kassa's, prijsgroepen, inkomsten- en uitgavenrekeningen en personeel hebben.</span><span class="sxs-lookup"><span data-stu-id="00b9c-110">Each store can have its own point of sale (POS) registers, income and expense accounts, and staff.</span></span> 

### <a name="call-center-channels"></a><span data-ttu-id="00b9c-111">Callcenterafzetkanalen</span><span class="sxs-lookup"><span data-stu-id="00b9c-111">Call center channels</span></span>

<span data-ttu-id="00b9c-112">Callcenterafzetkanalen vormen het bestel- en klantenbeheer via callcenters.</span><span class="sxs-lookup"><span data-stu-id="00b9c-112">Call center channels represent call center order and customer management.</span></span>

### <a name="online-channels"></a><span data-ttu-id="00b9c-113">Online afzetkanalen</span><span class="sxs-lookup"><span data-stu-id="00b9c-113">Online channels</span></span>

<span data-ttu-id="00b9c-114">Online afzetkanalen zijn de webwinkels.</span><span class="sxs-lookup"><span data-stu-id="00b9c-114">Online channels represent online e-Commerce storefronts.</span></span> <span data-ttu-id="00b9c-115">Wanneer een online kanaal is gemaakt, moet er een website worden gemaakt met behulp van het hulpprogramma Microsoft Dynamics 365 Commerce Site Builder of een andere e-Commerce oplossing van derden.</span><span class="sxs-lookup"><span data-stu-id="00b9c-115">Once an online channel is created, a site must be created using the Microsoft Dynamics 365 Commerce Site Builder tool or other third-party e-Commerce solution.</span></span>

## <a name="channel-setup-basics"></a><span data-ttu-id="00b9c-116">Basisinformatie over het instellen van kanalen</span><span class="sxs-lookup"><span data-stu-id="00b9c-116">Channel setup basics</span></span>

<span data-ttu-id="00b9c-117">Een kanaal wordt ingesteld met het Commerce-hulpprogramma.</span><span class="sxs-lookup"><span data-stu-id="00b9c-117">Channel set up is performed in the Commerce tool.</span></span> <span data-ttu-id="00b9c-118">Elk kanaal kan zijn eigen betalingsmethoden, prijsgroepen, producthiërarchieën, assortimenten en reeks producten hebben.</span><span class="sxs-lookup"><span data-stu-id="00b9c-118">Each channel can have its own payment methods, price groups, product hierarchies, assortments, and set of products.</span></span> <span data-ttu-id="00b9c-119">Nadat u een kanaal hebt gemaakt, wijst u de producten toe die u wilt voeren en verkopen.</span><span class="sxs-lookup"><span data-stu-id="00b9c-119">After you create a channel, you assign the products that you want it to carry and sell.</span></span> <span data-ttu-id="00b9c-120">Elk kanaaltype heeft een unieke set functies die mogelijk moeten worden geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="00b9c-120">Each channel type has a unique set of features that may need to be configured.</span></span> <span data-ttu-id="00b9c-121">Zo moeten aan een detailhandelafzetkanaal werknemers, kassa's en klanten worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="00b9c-121">For example, a retail channel needs assigned employees, registers, and customers.</span></span> <span data-ttu-id="00b9c-122">Nadat u een nieuw kanaal hebt gemaakt, moet dit worden toegewezen aan een organisatiehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="00b9c-122">Once a new channel is created, it needs to be assigned to an organization hierarchy.</span></span>

## <a name="channel-setup-prerequisites"></a><span data-ttu-id="00b9c-123">Vereisten voor het instellen van kanalen</span><span class="sxs-lookup"><span data-stu-id="00b9c-123">Channel setup prerequisites</span></span>

<span data-ttu-id="00b9c-124">Voordat u een kanaal kunt instellen, moet u een aantal vereiste taken uitvoeren op basis van het type kanaaltype.</span><span class="sxs-lookup"><span data-stu-id="00b9c-124">Before you can set up a channel, you must complete some prerequisite tasks based on the channel type.</span></span> <span data-ttu-id="00b9c-125">Zie [Vereisten voor het instellen van kanalen](channels-prerequisites.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="00b9c-125">For more information, see [Channel setup prerequisites](channels-prerequisites.md).</span></span>

## <a name="set-up-a-channel"></a><span data-ttu-id="00b9c-126">Een kanaal instellen</span><span class="sxs-lookup"><span data-stu-id="00b9c-126">Set up a channel</span></span>

<span data-ttu-id="00b9c-127">Nadat u de vereiste taken hebt voltooid, gebruikt u de volgende koppelingen voor verdere installatie-instructies.</span><span class="sxs-lookup"><span data-stu-id="00b9c-127">After you complete the prerequisite tasks, for further setup instructions, use the following links.</span></span>

- [<span data-ttu-id="00b9c-128">Een detailhandelafzetkanaal instellen</span><span class="sxs-lookup"><span data-stu-id="00b9c-128">Set up a retail channel</span></span>](channel-setup-retail.md)
- [<span data-ttu-id="00b9c-129">Een callcenterkanaal instellen</span><span class="sxs-lookup"><span data-stu-id="00b9c-129">Set up a call center channel</span></span>](channel-setup-callcenter.md)
- [<span data-ttu-id="00b9c-130">Een online afzetkanaal instellen</span><span class="sxs-lookup"><span data-stu-id="00b9c-130">Set up an online channel</span></span>](channel-setup-online.md)

<!--
## Post-channel configuration

After you create a channel, you may need to complete some of the below tasks:

- [Add channel to an organizational hierarchy](add-channel-org-hierarchy.md)
- Set up fulfillment groups. (LINK TBD)
- Configure the POS registers for the store. (LINK TBD)
- Assign product assortments to the store. (LINK TBD)
- Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store. (LINK TBD)
- Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.(LINK TBD)
- Publish the retail store to send store data to Retail POS. (LINK TBD)
- Run the jobs to send the store data to Retail POS. (LINK TBD)
-->

## <a name="additional-resources"></a><span data-ttu-id="00b9c-131">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="00b9c-131">Additional resources</span></span>

[<span data-ttu-id="00b9c-132">Vereisten voor het instellen van kanalen</span><span class="sxs-lookup"><span data-stu-id="00b9c-132">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="00b9c-133">Een detailhandelafzetkanaal instellen</span><span class="sxs-lookup"><span data-stu-id="00b9c-133">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="00b9c-134">Een online afzetkanaal instellen</span><span class="sxs-lookup"><span data-stu-id="00b9c-134">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="00b9c-135">Een callcenterkanaal instellen</span><span class="sxs-lookup"><span data-stu-id="00b9c-135">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="00b9c-136">Organisatiehiërarchieën instellen</span><span class="sxs-lookup"><span data-stu-id="00b9c-136">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)
