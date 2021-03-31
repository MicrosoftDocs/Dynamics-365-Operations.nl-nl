---
title: Op kenmerken gebaseerde prijzen instellen voor configureerbare producten
description: In dit onderwerp wordt uitgelegd hoe u op kenmerken gebaseerde prijsdetails instelt.
author: ShylaThompson
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e540e0f25afa65e84cdb11fb0c56437b72891f9f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220747"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="473f9-103">Op kenmerken gebaseerde prijzen instellen voor configureerbare producten</span><span class="sxs-lookup"><span data-stu-id="473f9-103">Set up attribute-based pricing for configurable products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="473f9-104">In dit onderwerp wordt uitgelegd hoe u op kenmerken gebaseerde prijsdetails instelt.</span><span class="sxs-lookup"><span data-stu-id="473f9-104">This topic explains how to set up attribute-based pricing.</span></span> <span data-ttu-id="473f9-105">Als eerste vereiste moet u een productconfiguratiemodel hebben dat een of meerdere onderdelen en kenmerken heeft.</span><span class="sxs-lookup"><span data-stu-id="473f9-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="473f9-106">In dit voorbeeld wordt het model Geavanceerde luidspreker gebruikt in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="473f9-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="473f9-107">Gewoonlijk gebruikt een productmanager deze procedure.</span><span class="sxs-lookup"><span data-stu-id="473f9-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="473f9-108">Eem nieuw prijsmodel maken</span><span class="sxs-lookup"><span data-stu-id="473f9-108">Create a new price model</span></span>
1. <span data-ttu-id="473f9-109">Selecteer **Definitie van productvariantmodel** op de startpagina.</span><span class="sxs-lookup"><span data-stu-id="473f9-109">Select **Product variant model definition** on the home page.</span></span>
2. <span data-ttu-id="473f9-110">Selecteer **Productconfiguratiemodellen** in de sectie **koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="473f9-110">Select **Product configuration models** in the **links** section.</span></span>
3. <span data-ttu-id="473f9-111">In de lijst selecteert u de regel **Geavanceerde luidspreker**, maar selecteert u niet de koppeling voor de naam.</span><span class="sxs-lookup"><span data-stu-id="473f9-111">In the list, select the **High End Speaker** line, but don't select the link for the name.</span></span>
4. <span data-ttu-id="473f9-112">Selecteer **Model** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="473f9-112">On the Action Pane, select **Model**.</span></span>
5. <span data-ttu-id="473f9-113">Selecteer **Prijsmodellen**.</span><span class="sxs-lookup"><span data-stu-id="473f9-113">Select **Price models**.</span></span>
6. <span data-ttu-id="473f9-114">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="473f9-114">Select **New**.</span></span>
7. <span data-ttu-id="473f9-115">Typ een waarde in het veld **Naam prijsmodel**.</span><span class="sxs-lookup"><span data-stu-id="473f9-115">In the **Price model name** field, type a value.</span></span> <span data-ttu-id="473f9-116">Gebruik een naam waaraan u het model gemakkelijk kunt herkennen.</span><span class="sxs-lookup"><span data-stu-id="473f9-116">Use a name that makes the model easy to identify.</span></span>  
8. <span data-ttu-id="473f9-117">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="473f9-117">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="473f9-118">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="473f9-118">Select **Save**.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="473f9-119">Prijselementen toevoegen</span><span class="sxs-lookup"><span data-stu-id="473f9-119">Add price elements</span></span>
1. <span data-ttu-id="473f9-120">Selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="473f9-120">Select **Edit**.</span></span> <span data-ttu-id="473f9-121">Elke component in een productmodel kan een element van de basisprijs en elk gewenst aantal prijsexpressieregels hebben.</span><span class="sxs-lookup"><span data-stu-id="473f9-121">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="473f9-122">U kunt ook prijzen in andere valuta toevoegen.</span><span class="sxs-lookup"><span data-stu-id="473f9-122">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="473f9-123">Typ een waarde in het veld **Basisprijsexpressie**.</span><span class="sxs-lookup"><span data-stu-id="473f9-123">In the **Base price expression** field, type a value.</span></span> <span data-ttu-id="473f9-124">Typ bijvoorbeeld 100.</span><span class="sxs-lookup"><span data-stu-id="473f9-124">For example, type 100.</span></span> <span data-ttu-id="473f9-125">Een expressie van de basisprijs kan een numerieke waarde zijn of bestaan uit een rekenkundige berekening die een of meer kenmerken bevat.</span><span class="sxs-lookup"><span data-stu-id="473f9-125">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="473f9-126">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="473f9-126">Select **Add**.</span></span>
4. <span data-ttu-id="473f9-127">Typ in het veld **Naam** `Rosewood`.</span><span class="sxs-lookup"><span data-stu-id="473f9-127">In the **Name** field, type `Rosewood`.</span></span> <span data-ttu-id="473f9-128">De naam van de prijsexpressie helpt bij het herkennen waarvoor het prijselement staat.</span><span class="sxs-lookup"><span data-stu-id="473f9-128">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="473f9-129">In dit voorbeeld wordt een prijselement gemaakt voor de rozenhouten afwerking van de luidsprekerkast.</span><span class="sxs-lookup"><span data-stu-id="473f9-129">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="473f9-130">Selecteer **Voorwaarde bewerken**.</span><span class="sxs-lookup"><span data-stu-id="473f9-130">Select **Edit condition**.</span></span> <span data-ttu-id="473f9-131">Een prijsvoorwaarde zorgt ervoor dat een element van de prijsexpressie alleen in de verkoopprijs wordt opgenomen als een specifieke combinatie van kenmerken aanwezig is.</span><span class="sxs-lookup"><span data-stu-id="473f9-131">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="473f9-132">In het veld **ConstraintBody** voert u `CabinetFinish=="Rosewood"` in.</span><span class="sxs-lookup"><span data-stu-id="473f9-132">In the **ConstraintBody** field, enter `CabinetFinish=="Rosewood"`.</span></span>
7. <span data-ttu-id="473f9-133">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="473f9-133">Select **OK**.</span></span>
8. <span data-ttu-id="473f9-134">Typ een waarde in het veld **Expressie**.</span><span class="sxs-lookup"><span data-stu-id="473f9-134">In the **Expression** field, type a value.</span></span> <span data-ttu-id="473f9-135">Typ bijvoorbeeld `50`.</span><span class="sxs-lookup"><span data-stu-id="473f9-135">For example, type `50`.</span></span> 
9. <span data-ttu-id="473f9-136">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="473f9-136">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]