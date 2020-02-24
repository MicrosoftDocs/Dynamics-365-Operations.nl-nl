---
title: Een nieuwe producthiërarchie maken
description: In dit onderwerp wordt beschreven hoe u een nieuwe producthiërarchie maakt in Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 73cecb0c6aacebf5c6fcf8a0edbc7513b3ce175d
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001893"
---
# <a name="create-a-new-product-hierarchy"></a><span data-ttu-id="b58db-103">Een nieuwe producthiërarchie maken</span><span class="sxs-lookup"><span data-stu-id="b58db-103">Create a new product hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b58db-104">In dit onderwerp wordt beschreven hoe u een nieuwe producthiërarchie maakt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b58db-104">This topic describes how to create a new product hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b58db-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="b58db-105">Overview</span></span>

<span data-ttu-id="b58db-106">Dynamics 365 Commerce ondersteunt meerdere detailhandelkanalen.</span><span class="sxs-lookup"><span data-stu-id="b58db-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="b58db-107">Deze detailhandelskanalen zijn o.a. online winkels, call centers en winkels (ook fysieke winkels genoemd).</span><span class="sxs-lookup"><span data-stu-id="b58db-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="b58db-108">Iedere Retail-winkelkanaal kan zijn eigen betalingsmethoden, prijsgroepen, verkooppuntkassa's (POS), inkomsten- en uitgavenrekeningen en personeel hebben.</span><span class="sxs-lookup"><span data-stu-id="b58db-108">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="b58db-109">U moet al deze elementen instellen voordat u een Retail-winkelkanaal kunt maken.</span><span class="sxs-lookup"><span data-stu-id="b58db-109">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="b58db-110">Gebruik een Commerce-producthiërarchietype om de algemene producthiërarchie voor uw organisatie te definiëren.</span><span class="sxs-lookup"><span data-stu-id="b58db-110">A Commerce product hierarchy is used to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="b58db-111">U kunt een Commerce-producthiërarchie gebruiken voor merchandising, prijzen en promoties, rapportage en assortimentplanning.</span><span class="sxs-lookup"><span data-stu-id="b58db-111">You can use a Commerce product hierarchy for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="b58db-112">Er kan per organisatie slechts één Commerce-producthiërarchie worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="b58db-112">Only one Commerce product hierarchy can be assigned per organization.</span></span>

## <a name="create-and-configure-a-product-hierarchy"></a><span data-ttu-id="b58db-113">Een producthiërarchie maken en configureren</span><span class="sxs-lookup"><span data-stu-id="b58db-113">Create and configure a product hierarchy</span></span>

<span data-ttu-id="b58db-114">Voer de volgende stappen uit om een Commerce-producthiërarchie te maken en te configureren.</span><span class="sxs-lookup"><span data-stu-id="b58db-114">To create and configure a Commerce product hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="b58db-115">Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Producten en categorieën \> Commerce-producthiërarchie**.</span><span class="sxs-lookup"><span data-stu-id="b58db-115">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Commerce product hierarchy**.</span></span>
1. <span data-ttu-id="b58db-116">Als er nog geen hiërarchie bestaat, selecteert u in het **actievenster** de optie **Nieuw** om de basis van de hiërarchie te maken.</span><span class="sxs-lookup"><span data-stu-id="b58db-116">If no hierachy exists yet, on the **Action pane**, select **New** to create the root of the hierarchy.</span></span>
1. <span data-ttu-id="b58db-117">Onder **Algemeen**:</span><span class="sxs-lookup"><span data-stu-id="b58db-117">Under **General**:</span></span>
    1. <span data-ttu-id="b58db-118">Voer in het vak **Naam** een naam in.</span><span class="sxs-lookup"><span data-stu-id="b58db-118">In the **Name** box, enter a name.</span></span>
    1. <span data-ttu-id="b58db-119">Voer in het vak **Omschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="b58db-119">In the **Description** box, enter a description.</span></span>
    1. <span data-ttu-id="b58db-120">Voer in het vak **Beschrijvende naam** een beschrijvende naam in.</span><span class="sxs-lookup"><span data-stu-id="b58db-120">In the **Friendly name** box, enter a friendly name.</span></span>
    1. <span data-ttu-id="b58db-121">Stel **Actief** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b58db-121">Set **Active** to **Yes**.</span></span>

## <a name="add-hierarchy-nodes"></a><span data-ttu-id="b58db-122">Hiërarchieknooppunten toevoegen</span><span class="sxs-lookup"><span data-stu-id="b58db-122">Add hierarchy nodes</span></span>

<span data-ttu-id="b58db-123">Voer de volgende stappen uit om hiërarchieknooppunten toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="b58db-123">To add hierarchy nodes, follow these steps.</span></span>

1. <span data-ttu-id="b58db-124">Klik in het actievenster op **Categoriehiërarchie**.</span><span class="sxs-lookup"><span data-stu-id="b58db-124">On the action pane, select **Edit category hierarchy**.</span></span>
1. <span data-ttu-id="b58db-125">Selecteer het bovenliggende knooppunt waaraan u een nieuwknoop punt wilt toevoegen en selecteer **Nieuw categorieknooppunt**.</span><span class="sxs-lookup"><span data-stu-id="b58db-125">Select the parent node you want to add a new node to, and then select **New category node**.</span></span>
1. <span data-ttu-id="b58db-126">Geef in de sectie **Algemeen** een **Naam**, **Beschrijving**, **Beschrijvende naam** en **Trefwoorden** op.</span><span class="sxs-lookup"><span data-stu-id="b58db-126">In the **General** section provide a **Name**, **Description**, **Friendly name** and **Keywords**.</span></span>
1. <span data-ttu-id="b58db-127">Onder **Algemeen**:</span><span class="sxs-lookup"><span data-stu-id="b58db-127">Under **General**:</span></span>
    1. <span data-ttu-id="b58db-128">Voer in het vak **Naam** een naam in.</span><span class="sxs-lookup"><span data-stu-id="b58db-128">In the **Name** box, enter a name.</span></span>
    1. <span data-ttu-id="b58db-129">Voer in het vak **Omschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="b58db-129">In the **Description** box, enter a description.</span></span>
    1. <span data-ttu-id="b58db-130">Voer in het vak **Beschrijvende naam** een beschrijvende naam in.</span><span class="sxs-lookup"><span data-stu-id="b58db-130">In the **Friendly name** box, enter a friendly name.</span></span>
    1. <span data-ttu-id="b58db-131">Voer in het vak **Trefwoorden** relevante trefwoorden in.</span><span class="sxs-lookup"><span data-stu-id="b58db-131">In the **Keywords** box, enter relevant keywords.</span></span>
    1. <span data-ttu-id="b58db-132">Voer in het vak **Weergavevolgorde** een getal voor de weergavevolgorde in (optioneel).</span><span class="sxs-lookup"><span data-stu-id="b58db-132">In the **Display order**box, enter a number for the display order (optional).</span></span>
1. <span data-ttu-id="b58db-133">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="b58db-133">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="b58db-134">Herhaal de bovenstaande stappen om extra knooppunten toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="b58db-134">Repeat the steps above to add additional nodes.</span></span>

<span data-ttu-id="b58db-135">De volgende afbeelding toont het maken van een nieuw knooppunt voor een producthiërarchie.</span><span class="sxs-lookup"><span data-stu-id="b58db-135">The following image shows the creation of a new product hierarchy node.</span></span>

![Een producthiërarchie maken](media/create-product-hierarchy.png)

## <a name="other-settings"></a><span data-ttu-id="b58db-137">Overige instellingen</span><span class="sxs-lookup"><span data-stu-id="b58db-137">Other settings</span></span>

<span data-ttu-id="b58db-138">Categoriekenmerkgroepen kunnen ook naar behoefte worden toegewezen aan elke groep.</span><span class="sxs-lookup"><span data-stu-id="b58db-138">Category attribute groups can also be assigned to each group as required.</span></span>  

## <a name="additional-resources"></a><span data-ttu-id="b58db-139">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="b58db-139">Additional resources</span></span>

[<span data-ttu-id="b58db-140">Detailhandelhiërarchieën</span><span class="sxs-lookup"><span data-stu-id="b58db-140">Retail hierarchies</span></span>](retail-hierarchies.md)

[<span data-ttu-id="b58db-141">Productcategorieën en producten beheren </span><span class="sxs-lookup"><span data-stu-id="b58db-141">Manage product categories and products </span></span>](category-management-product-creation.md)

[<span data-ttu-id="b58db-142">De sorteervolgorde voor entiteiten voor merchandising wijzigen</span><span class="sxs-lookup"><span data-stu-id="b58db-142">Change the sort order for merchandizing entities</span></span>](custom-order-categories-nav-retail-prod-hierarchy.md)
