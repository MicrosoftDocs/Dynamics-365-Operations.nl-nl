---
title: Een kanaal voor een kanaalnavigatiehiërarchie configureren
description: In dit onderwerp wordt beschreven hoe u een kanaal configureert om een kanaalnavigatiehiërarchie in Microsoft Dynamics 365 Commerce te gebruiken.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3dcba743e6557b1bd366ac79ecb49ead831dceb4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001020"
---
# <a name="configure-a-channel-to-use-a-channel-navigation-hierarchy"></a><span data-ttu-id="aa0e3-103">Een kanaal voor een kanaalnavigatiehiërarchie configureren</span><span class="sxs-lookup"><span data-stu-id="aa0e3-103">Configure a channel to use a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="aa0e3-104">In dit onderwerp wordt beschreven hoe u een kanaal configureert om een kanaalnavigatiehiërarchie in Microsoft Dynamics 365 Commerce te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="aa0e3-104">This topic describes how to configure a channel to use a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="aa0e3-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="aa0e3-105">Overview</span></span>

<span data-ttu-id="aa0e3-106">Met kanaalnavigatiehiërarchieën kunt u producten indelen in categorieën, zodat de producten kunnen worden bezocht op een e-commerce site of op verkooppunten (POS).</span><span class="sxs-lookup"><span data-stu-id="aa0e3-106">Channel navigation hierarchies organize products into categories so that the products can be browsed on an e-Commerce site or at points of sale (POS).</span></span> <span data-ttu-id="aa0e3-107">Winkel- en online kanalen moeten met kanaalnavigatiehiërarchieën worden geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="aa0e3-107">Retail and online channels must be configured with channel navigation hierarchies.</span></span>

## <a name="configure-the-channel"></a><span data-ttu-id="aa0e3-108">Het kanaal configureren</span><span class="sxs-lookup"><span data-stu-id="aa0e3-108">Configure the channel</span></span>

<span data-ttu-id="aa0e3-109">Voer de volgende stappen uit om een kanaal te configureren voor het gebruik van een kanaalnavigatiehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="aa0e3-109">To configure a channel to use a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="aa0e3-110">Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Kanaalinstellingen \> Kanaalcategorieën en productkenmerken**.</span><span class="sxs-lookup"><span data-stu-id="aa0e3-110">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="aa0e3-111">Selecteer het kanaal dat u wilt configureren.</span><span class="sxs-lookup"><span data-stu-id="aa0e3-111">Select the channel to configure.</span></span>
1. <span data-ttu-id="aa0e3-112">Selecteer in het actievenster **Metagegevens van kenmerken instellen**.</span><span class="sxs-lookup"><span data-stu-id="aa0e3-112">On the action pane, select **Set attribute metadata**.</span></span>
1. <span data-ttu-id="aa0e3-113">Selecteer in de vervolgkeuzelijst **Categoriehiërarchie** de juiste kanaalnavigatiehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="aa0e3-113">In the **Category hierarchy** drop-down list, select the appropriate channel navigation hierarchy.</span></span>
1. <span data-ttu-id="aa0e3-114">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="aa0e3-114">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="aa0e3-115">Voeg onder **Kenmerkgroep** kenmerkgroepen toe die algemene kenmerken voor alle knooppunten moeten worden.</span><span class="sxs-lookup"><span data-stu-id="aa0e3-115">Under **Attribute group**, add any attribute groups that will be global attributes for all nodes.</span></span>

<span data-ttu-id="aa0e3-116">In de volgende afbeelding ziet u hoe u een kanaal configureert voor het gebruik van een kanaalnavigatiehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="aa0e3-116">The following image shows how to configure a channel to use a channel navigation hierarchy.</span></span>

![Voorbeeld van kanaalconfiguratie](media/configure-channel-hierarchy-1.png)

## <a name="set-attribute-metadata"></a><span data-ttu-id="aa0e3-118">Metagegevens van kenmerken instellen</span><span class="sxs-lookup"><span data-stu-id="aa0e3-118">Set attribute metadata</span></span>

<span data-ttu-id="aa0e3-119">Als u de metagegevens voor het kenmerk instelt, kunt u op elk knooppunt kenmerken configureren.</span><span class="sxs-lookup"><span data-stu-id="aa0e3-119">Setting the attribute metadata will allow configuration of attributes on each node.</span></span>

<span data-ttu-id="aa0e3-120">Volg deze stappen om metagegevens voor kenmerken in te stellen.</span><span class="sxs-lookup"><span data-stu-id="aa0e3-120">To set attribute metadata, follow these steps.</span></span>

1. <span data-ttu-id="aa0e3-121">Selecteer in het actievenster **Metagegevens van kenmerken instellen**.</span><span class="sxs-lookup"><span data-stu-id="aa0e3-121">On the action pane, select **Set attribute metadata**.</span></span>
1. <span data-ttu-id="aa0e3-122">Selecteer **Kanaalproductkenmerken** voor elk knooppunt.</span><span class="sxs-lookup"><span data-stu-id="aa0e3-122">For each node select **Channel product attributes**.</span></span>
1. <span data-ttu-id="aa0e3-123">Stel **Kenmerk in kanaal weergeven** in op **Ja** en **Kan worden verfijnd** op **Ja** om verfijningen voor dat kanaal in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="aa0e3-123">Set **Show attribute on channel** to **Yes** and **Can be refined** to **Yes**, to enable refiners on that channel.</span></span>
1. <span data-ttu-id="aa0e3-124">Nadat u elk knooppunt naar wens hebt geconfigureerd, selecteert u in het **actievenster** de knop **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="aa0e3-124">After configuring each node as desired, on the **Action pane**, select the **Save** button to save.</span></span>
1. <span data-ttu-id="aa0e3-125">Selecteer de **X** in de rechterbovenhoek om dit scherm af te sluiten en terug te gaan naar de pagina **Kanaalcategorieën en productkenmerken**.</span><span class="sxs-lookup"><span data-stu-id="aa0e3-125">Select the **X** in the top right corner to exit this screen back to the **Channel categories and product attributes** page.</span></span>

<span data-ttu-id="aa0e3-126">De volgende afbeelding toont een voorbeeld van een set productkenmerken voor kanalen die is geconfigureerd op een knooppunt van een kanaalcategorie.</span><span class="sxs-lookup"><span data-stu-id="aa0e3-126">The following image shows an example set of channel product attributes configured on a channel category node.</span></span>

![Kanaalkenmerken in een kanaalcategorieknooppunt](media/configure-channel-hierarchy-2.png)

## <a name="publish-changes"></a><span data-ttu-id="aa0e3-128">Wijzigingen publiceren</span><span class="sxs-lookup"><span data-stu-id="aa0e3-128">Publish changes</span></span>

<span data-ttu-id="aa0e3-129">U moet de wijzigingen publiceren om de wijzigingen van kracht te laten worden.</span><span class="sxs-lookup"><span data-stu-id="aa0e3-129">For changes to take effect, you will need to publish the changes.</span></span>

<span data-ttu-id="aa0e3-130">Voer deze stappen uit om wijzigingen te publiceren.</span><span class="sxs-lookup"><span data-stu-id="aa0e3-130">To publish changes, follow these steps.</span></span>

1. <span data-ttu-id="aa0e3-131">Selecteer in het actievenster **Kanaalupdates publiceren**.</span><span class="sxs-lookup"><span data-stu-id="aa0e3-131">On the action pane, select **Publish channel updates**.</span></span>
1. <span data-ttu-id="aa0e3-132">Selecteer **OK** in het deelvenster **Kanaalupdates publiceren**.</span><span class="sxs-lookup"><span data-stu-id="aa0e3-132">In the **Publish channel updates** pane, select **OK**.</span></span>

<span data-ttu-id="aa0e3-133">De volgende afbeelding laat zien hoe u kanaalupdates kunt publiceren.</span><span class="sxs-lookup"><span data-stu-id="aa0e3-133">The following image shows how to publish channel updates.</span></span>

![Afzetkanaalupdates publiceren](media/configure-channel-hierarchy-3.png)

## <a name="additional-resources"></a><span data-ttu-id="aa0e3-135">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="aa0e3-135">Additional resources</span></span>

[<span data-ttu-id="aa0e3-136">Een afzetkanaalnavigatiehiërarchie maken</span><span class="sxs-lookup"><span data-stu-id="aa0e3-136">Create a channel navigation hierarchy</span></span>](create-channel-hierarchy.md)


