---
title: Op kenmerken gebaseerde prijzen instellen voor configureerbare producten
description: In dit onderwerp wordt uitgelegd hoe u op kenmerken gebaseerde prijsdetails instelt.
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0c30c520e7265c2676937f5191844f6789c364e6
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921236"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="f4ab0-103">Op kenmerken gebaseerde prijzen instellen voor configureerbare producten</span><span class="sxs-lookup"><span data-stu-id="f4ab0-103">Set up attribute-based pricing for configurable products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f4ab0-104">In dit onderwerp wordt uitgelegd hoe u op kenmerken gebaseerde prijsdetails instelt.</span><span class="sxs-lookup"><span data-stu-id="f4ab0-104">This topic explains how to set up attribute-based pricing.</span></span> <span data-ttu-id="f4ab0-105">Als eerste vereiste moet u een productconfiguratiemodel hebben dat een of meerdere onderdelen en kenmerken heeft.</span><span class="sxs-lookup"><span data-stu-id="f4ab0-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="f4ab0-106">In dit voorbeeld wordt het model Geavanceerde luidspreker gebruikt in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="f4ab0-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="f4ab0-107">Gewoonlijk gebruikt een productmanager deze procedure.</span><span class="sxs-lookup"><span data-stu-id="f4ab0-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="f4ab0-108">Eem nieuw prijsmodel maken</span><span class="sxs-lookup"><span data-stu-id="f4ab0-108">Create a new price model</span></span>

1. <span data-ttu-id="f4ab0-109">Ga naar **Productgegevensbeheer \> Producten \> Productconfiguratiemodellen**.</span><span class="sxs-lookup"><span data-stu-id="f4ab0-109">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="f4ab0-110">In de lijst selecteert u de regel **Geavanceerde luidspreker**, maar selecteert u niet de koppeling voor de naam.</span><span class="sxs-lookup"><span data-stu-id="f4ab0-110">In the list, select the **High End Speaker** line, but don't select the link for the name.</span></span>
1. <span data-ttu-id="f4ab0-111">Selecteer **Model** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="f4ab0-111">On the Action Pane, select **Model**.</span></span>
1. <span data-ttu-id="f4ab0-112">Selecteer **Prijsmodellen**.</span><span class="sxs-lookup"><span data-stu-id="f4ab0-112">Select **Price models**.</span></span>
1. <span data-ttu-id="f4ab0-113">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="f4ab0-113">Select **New**.</span></span>
1. <span data-ttu-id="f4ab0-114">Typ een waarde in het veld **Naam prijsmodel**.</span><span class="sxs-lookup"><span data-stu-id="f4ab0-114">In the **Price model name** field, type a value.</span></span> <span data-ttu-id="f4ab0-115">Gebruik een naam waaraan u het model gemakkelijk kunt herkennen.</span><span class="sxs-lookup"><span data-stu-id="f4ab0-115">Use a name that makes the model easy to identify.</span></span>  
1. <span data-ttu-id="f4ab0-116">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="f4ab0-116">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="f4ab0-117">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="f4ab0-117">Select **Save**.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="f4ab0-118">Prijselementen toevoegen</span><span class="sxs-lookup"><span data-stu-id="f4ab0-118">Add price elements</span></span>

1. <span data-ttu-id="f4ab0-119">Selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="f4ab0-119">Select **Edit**.</span></span> <span data-ttu-id="f4ab0-120">Elke component in een productmodel kan een element van de basisprijs en elk gewenst aantal prijsexpressieregels hebben.</span><span class="sxs-lookup"><span data-stu-id="f4ab0-120">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="f4ab0-121">U kunt ook prijzen in andere valuta toevoegen.</span><span class="sxs-lookup"><span data-stu-id="f4ab0-121">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="f4ab0-122">Typ een waarde in het veld **Basisprijsexpressie**.</span><span class="sxs-lookup"><span data-stu-id="f4ab0-122">In the **Base price expression** field, type a value.</span></span> <span data-ttu-id="f4ab0-123">Typ bijvoorbeeld 100.</span><span class="sxs-lookup"><span data-stu-id="f4ab0-123">For example, type 100.</span></span> <span data-ttu-id="f4ab0-124">Een expressie van de basisprijs kan een numerieke waarde zijn of bestaan uit een rekenkundige berekening die een of meer kenmerken bevat.</span><span class="sxs-lookup"><span data-stu-id="f4ab0-124">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="f4ab0-125">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="f4ab0-125">Select **Add**.</span></span>
4. <span data-ttu-id="f4ab0-126">Typ in het veld **Naam** `Rosewood`.</span><span class="sxs-lookup"><span data-stu-id="f4ab0-126">In the **Name** field, type `Rosewood`.</span></span> <span data-ttu-id="f4ab0-127">De naam van de prijsexpressie helpt bij het herkennen waarvoor het prijselement staat.</span><span class="sxs-lookup"><span data-stu-id="f4ab0-127">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="f4ab0-128">In dit voorbeeld wordt een prijselement gemaakt voor de rozenhouten afwerking van de luidsprekerkast.</span><span class="sxs-lookup"><span data-stu-id="f4ab0-128">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="f4ab0-129">Selecteer **Voorwaarde bewerken**.</span><span class="sxs-lookup"><span data-stu-id="f4ab0-129">Select **Edit condition**.</span></span> <span data-ttu-id="f4ab0-130">Een prijsvoorwaarde zorgt ervoor dat een element van de prijsexpressie alleen in de verkoopprijs wordt opgenomen als een specifieke combinatie van kenmerken aanwezig is.</span><span class="sxs-lookup"><span data-stu-id="f4ab0-130">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="f4ab0-131">In het veld **ConstraintBody** voert u `CabinetFinish=="Rosewood"` in.</span><span class="sxs-lookup"><span data-stu-id="f4ab0-131">In the **ConstraintBody** field, enter `CabinetFinish=="Rosewood"`.</span></span>
7. <span data-ttu-id="f4ab0-132">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="f4ab0-132">Select **OK**.</span></span>
8. <span data-ttu-id="f4ab0-133">Typ een waarde in het veld **Expressie**.</span><span class="sxs-lookup"><span data-stu-id="f4ab0-133">In the **Expression** field, type a value.</span></span> <span data-ttu-id="f4ab0-134">Typ bijvoorbeeld `50`.</span><span class="sxs-lookup"><span data-stu-id="f4ab0-134">For example, type `50`.</span></span> 
9. <span data-ttu-id="f4ab0-135">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f4ab0-135">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]