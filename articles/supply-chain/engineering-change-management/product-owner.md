---
title: Producteigenaren
description: Dit onderwerp biedt informatie over producteigenaren. Een producteigenaar is een groep gebruikers die verantwoordelijk is voor specifieke producten. Alleen leden van de groep kunnen deze producten vrijgeven. De producteigenaar kan ook worden gebruikt in de goedkeuringswerkstroom.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductOwner
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: a1c3bc6f77fed83cfbbd502cdd469baa491fd81f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5266122"
---
# <a name="product-owners"></a><span data-ttu-id="76c06-106">Producteigenaren</span><span class="sxs-lookup"><span data-stu-id="76c06-106">Product owners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="76c06-107">De producteigenaar is een groep gebruikers die verantwoordelijk is voor specifieke producten.</span><span class="sxs-lookup"><span data-stu-id="76c06-107">The product owner is a group of users who are responsible for specific products.</span></span> <span data-ttu-id="76c06-108">Wanneer een producteigenaarsgroep aan een product wordt toegewezen, kunnen alleen de leden van die groep het product vrijgeven.</span><span class="sxs-lookup"><span data-stu-id="76c06-108">When a product owner group is assigned to a product, only the members of that group can release the product.</span></span> <span data-ttu-id="76c06-109">De producteigenaar kan ook worden gebruikt in de goedkeuringswerkstroom voor het beheer van technische wijzigingen.</span><span class="sxs-lookup"><span data-stu-id="76c06-109">The product owner can also be used in the approval workflow in engineering change management.</span></span>

<span data-ttu-id="76c06-110">Producteigenaren zijn algemene instellingen.</span><span class="sxs-lookup"><span data-stu-id="76c06-110">Product owners are global settings.</span></span> <span data-ttu-id="76c06-111">Deze zijn daarom beschikbaar voor alle rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="76c06-111">Therefore, they are available to all legal entities.</span></span>

## <a name="create-a-product-owner-group"></a><span data-ttu-id="76c06-112">Een producteigenaarsgroep maken</span><span class="sxs-lookup"><span data-stu-id="76c06-112">Create a product owner group</span></span>

<span data-ttu-id="76c06-113">Voer de volgende stappen uit om een producteigenaarsgroep te maken en hier leden aan toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="76c06-113">To create a product owner group and add members to it, follow these steps.</span></span>

1. <span data-ttu-id="76c06-114">Ga naar **Beheer van technische wijzigingen \> Instellingen \> Producteigenaren**.</span><span class="sxs-lookup"><span data-stu-id="76c06-114">Go to **Engineering change management \> Setup \> Product owners**.</span></span>
2. <span data-ttu-id="76c06-115">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="76c06-115">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="76c06-116">Voer een naam in voor de groep in het veld **Producteigenaar**.</span><span class="sxs-lookup"><span data-stu-id="76c06-116">In the **Product owner** field, enter a name for the group.</span></span>
4. <span data-ttu-id="76c06-117">Voer in het veld **Naam** een omschrijving in van de groep.</span><span class="sxs-lookup"><span data-stu-id="76c06-117">In the **Name** field, enter a description of the group.</span></span>
5. <span data-ttu-id="76c06-118">Voeg in sneltabblad **Leden** de werknemers toe die lid moeten zijn van de groep.</span><span class="sxs-lookup"><span data-stu-id="76c06-118">On the **Members** FastTab, add the workers who should be members of the group.</span></span>

## <a name="assign-a-product-owner-to-a-product"></a><span data-ttu-id="76c06-119">Een producteigenaar toewijzen aan een product</span><span class="sxs-lookup"><span data-stu-id="76c06-119">Assign a product owner to a product</span></span>

<span data-ttu-id="76c06-120">Om een producteigenaar aan een product toe te wijzen, volgt u deze stappen.</span><span class="sxs-lookup"><span data-stu-id="76c06-120">To assign a product owner to a product, follow these steps.</span></span>

1. <span data-ttu-id="76c06-121">Open de pagina **Productgegevens** voor het relevante product of productmodel.</span><span class="sxs-lookup"><span data-stu-id="76c06-121">Open the **Product details** page for the relevant product or product master.</span></span>
1. <span data-ttu-id="76c06-122">Op het sneltabblad **Algemeen** stelt u het veld **Producteigenaar** in op de naam van de relevante producteigenaarsgroep.</span><span class="sxs-lookup"><span data-stu-id="76c06-122">On the **General** FastTab, set the **Product owner** field to the name of the relevant product owner group.</span></span>

<span data-ttu-id="76c06-123">Terwijl een producteigenaar aan een product is toegewezen, kunnen alleen de leden van de producteigenaarsgroep de instelling **Producteigenaar** bewerken.</span><span class="sxs-lookup"><span data-stu-id="76c06-123">While a product owner is assigned to a product, only the members of the product owner group can edit the **Product owner** setting.</span></span>

<span data-ttu-id="76c06-124">De product eigenaar wordt ook weergegeven op de pagina **Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="76c06-124">The product owner is also visible on the **Released products** page.</span></span>

## <a name="product-owners-and-product-releases"></a><span data-ttu-id="76c06-125">Producteigenaars en productvrijgaves</span><span class="sxs-lookup"><span data-stu-id="76c06-125">Product owners and product releases</span></span>

<span data-ttu-id="76c06-126">Alleen gebruikers uit de producteigenaarsgroep van een product kunnen dat product vrijgeven.</span><span class="sxs-lookup"><span data-stu-id="76c06-126">Only users from a product's product owner group can release that product.</span></span> <span data-ttu-id="76c06-127">Er is echter een uitzondering wanneer het product een onderliggend artikel is en het bovenliggende artikel wordt vrijgegeven door de eigenaar van het bovenliggende artikel.</span><span class="sxs-lookup"><span data-stu-id="76c06-127">However, there is an exception when the product is a child item, and its parent is released by the parent's owner.</span></span> <span data-ttu-id="76c06-128">Met andere woorden, als het product deel uitmaakt van de stuklijst van een ander product, controleert het systeem de producteigenaar van elk artikel in de stuklijst niet.</span><span class="sxs-lookup"><span data-stu-id="76c06-128">In other words, if the product is part of the BOM of another product, the system doesn't check the product owner of each item in the BOM.</span></span> <span data-ttu-id="76c06-129">Alleen de producteigenaar van het bovenliggende artikel wordt gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="76c06-129">It checks only the product owner of the parent item.</span></span>

<span data-ttu-id="76c06-130">Product X wordt bijvoorbeeld toegewezen aan de producteigenaarsgroep *Designkasten*.</span><span class="sxs-lookup"><span data-stu-id="76c06-130">For example, product X is assigned to the *Design cabinets* product owner group.</span></span> <span data-ttu-id="76c06-131">Product X maakt ook deel uit van de stuklijst van product Y, dat is toegewezen aan de producteigenaarsgroep *Designluidsprekers*.</span><span class="sxs-lookup"><span data-stu-id="76c06-131">Product X is also part of the BOM of product Y, which is assigned to the *Design Speakers* product owner group.</span></span> <span data-ttu-id="76c06-132">Als een gebruiker in de producteigenaarsgroep *Designluidsprekers* product Y en de bijbehorende stuklijst vrijgeeft, wordt product X samen met product Y vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="76c06-132">If a user from the *Design Speakers* product owner group releases product Y and its BOM, product X will be released together with product Y.</span></span>

## <a name="product-owners-and-approvals"></a><span data-ttu-id="76c06-133">Producteigenaren en goedkeuringen</span><span class="sxs-lookup"><span data-stu-id="76c06-133">Product owners and approvals</span></span>

<span data-ttu-id="76c06-134">Omdat de producteigenaren weten of hun producten baat hebben bij specifieke technische wijzigingen, is het vaak zinvol om hen op te nemen als onderdeel van het goedkeuringsproces in het beheer technische wijzigingen.</span><span class="sxs-lookup"><span data-stu-id="76c06-134">Because product owners know whether specific engineering changes will benefit their products, it often makes sense to include them as part of the approval process in engineering change management.</span></span> <span data-ttu-id="76c06-135">U kunt deze aanpak implementeren door de producteigenaren in te stellen als deelnemende leveranciers in de workflows die worden gebruikt voor het beheer van technische wijzigingen.</span><span class="sxs-lookup"><span data-stu-id="76c06-135">You can implement this approach by setting up the product owners as participant providers in the workflows that are used for engineering change management.</span></span> <span data-ttu-id="76c06-136">Het systeem wijst vervolgens goedkeuringstaken toe in de werkstromen, op basis van de producten in de aanvragen voor technische wijzigingen en de orders voor technische wijzigingen.</span><span class="sxs-lookup"><span data-stu-id="76c06-136">The system will then assign approval tasks in the workflows, based on the products that are in engineering change requests and engineering change orders.</span></span> <span data-ttu-id="76c06-137">Zie [Wijzigingen in technische producten beheren](engineering-change-management.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="76c06-137">For more information, see [Manage changes to engineering products](engineering-change-management.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]