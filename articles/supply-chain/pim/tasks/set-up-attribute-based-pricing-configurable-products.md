--- 
title: Op kenmerken gebaseerde prijzen instellen voor configureerbare producten
description: Deze procedure laat zien hoe u op kenmerken gebaseerde prijsdetails instelt.
author: ShylaThompson
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: f1eaa53a652a59d4d970781f734e1332aa762ca2
ms.contentlocale: nl-nl
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="32fc4-103">Op kenmerken gebaseerde prijzen instellen voor configureerbare producten</span><span class="sxs-lookup"><span data-stu-id="32fc4-103">Set up attribute-based pricing for configurable products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="32fc4-104">Deze procedure laat zien hoe u op kenmerken gebaseerde prijsdetails instelt.</span><span class="sxs-lookup"><span data-stu-id="32fc4-104">This procedure shows how to set up attribute-based pricing.</span></span> <span data-ttu-id="32fc4-105">Als eerste vereiste moet u een productconfiguratiemodel hebben dat een of meerdere onderdelen en kenmerken heeft.</span><span class="sxs-lookup"><span data-stu-id="32fc4-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="32fc4-106">In dit voorbeeld wordt het model Geavanceerde luidspreker gebruikt in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="32fc4-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="32fc4-107">Gewoonlijk gebruikt een productmanager deze procedure.</span><span class="sxs-lookup"><span data-stu-id="32fc4-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="32fc4-108">Eem nieuw prijsmodel maken</span><span class="sxs-lookup"><span data-stu-id="32fc4-108">Create a new price model</span></span>
1. <span data-ttu-id="32fc4-109">Klik op Definitie van productvariantmodel.</span><span class="sxs-lookup"><span data-stu-id="32fc4-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="32fc4-110">Klik op Productconfiguratiemodellen.</span><span class="sxs-lookup"><span data-stu-id="32fc4-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="32fc4-111">In de lijst selecteert u de regel van de Geavanceerde luidspreker, maar klikt u niet op de koppeling voor de naam.</span><span class="sxs-lookup"><span data-stu-id="32fc4-111">In the list, select the High End Speaker line, but don’t click the link for the name.</span></span>
4. <span data-ttu-id="32fc4-112">Klik in het actievenster op Model.</span><span class="sxs-lookup"><span data-stu-id="32fc4-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="32fc4-113">Klik op Prijsmodellen.</span><span class="sxs-lookup"><span data-stu-id="32fc4-113">Click Price models.</span></span>
6. <span data-ttu-id="32fc4-114">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="32fc4-114">Click New.</span></span>
7. <span data-ttu-id="32fc4-115">Typ een waarde in het veld Prijsmodel.</span><span class="sxs-lookup"><span data-stu-id="32fc4-115">In the Price model name field, type a value.</span></span>
    * <span data-ttu-id="32fc4-116">Gebruik een naam waaraan u het model gemakkelijk kunt herkennen.</span><span class="sxs-lookup"><span data-stu-id="32fc4-116">Use a name that makes the model easy to identify.</span></span>  
8. <span data-ttu-id="32fc4-117">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="32fc4-117">In the Description field, type a value.</span></span>
9. <span data-ttu-id="32fc4-118">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="32fc4-118">Click Save.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="32fc4-119">Prijselementen toevoegen</span><span class="sxs-lookup"><span data-stu-id="32fc4-119">Add price elements</span></span>
1. <span data-ttu-id="32fc4-120">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="32fc4-120">Click Edit.</span></span>
    * <span data-ttu-id="32fc4-121">Elke component in een productmodel kan een element van de basisprijs en elk gewenst aantal prijsexpressieregels hebben.</span><span class="sxs-lookup"><span data-stu-id="32fc4-121">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="32fc4-122">U kunt ook prijzen in andere valuta toevoegen.</span><span class="sxs-lookup"><span data-stu-id="32fc4-122">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="32fc4-123">Typ een waarde in het veld Basisprijsexpressie.</span><span class="sxs-lookup"><span data-stu-id="32fc4-123">In the Base price expression field, type a value.</span></span>
    * <span data-ttu-id="32fc4-124">Typ bijvoorbeeld 100.</span><span class="sxs-lookup"><span data-stu-id="32fc4-124">For example, type 100.</span></span>   <span data-ttu-id="32fc4-125">Een expressie van de basisprijs kan een numerieke waarde zijn of bestaan uit een rekenkundige berekening die een of meer kenmerken bevat.</span><span class="sxs-lookup"><span data-stu-id="32fc4-125">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="32fc4-126">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="32fc4-126">Click Add.</span></span>
4. <span data-ttu-id="32fc4-127">Typ Rozenhouten in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="32fc4-127">In the Name field, type ‘Rosewood’.</span></span>
    * <span data-ttu-id="32fc4-128">De naam van de prijsexpressie helpt bij het herkennen waarvoor het prijselement staat.</span><span class="sxs-lookup"><span data-stu-id="32fc4-128">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="32fc4-129">In dit voorbeeld wordt een prijselement gemaakt voor de rozenhouten afwerking van de luidsprekerkast.</span><span class="sxs-lookup"><span data-stu-id="32fc4-129">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="32fc4-130">Klik op Voorwaarde bewerken.</span><span class="sxs-lookup"><span data-stu-id="32fc4-130">Click Edit condition.</span></span>
    * <span data-ttu-id="32fc4-131">Een prijsvoorwaarde zorgt ervoor dat een element van de prijsexpressie alleen in de verkoopprijs wordt opgenomen als een specifieke combinatie van kenmerken aanwezig is.</span><span class="sxs-lookup"><span data-stu-id="32fc4-131">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="32fc4-132">Typ in het veld ConstraintBody 'CabinetFinish=="Rosewood"'.</span><span class="sxs-lookup"><span data-stu-id="32fc4-132">In the ConstraintBody field, enter 'CabinetFinish=="Rosewood"'.</span></span>
7. <span data-ttu-id="32fc4-133">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="32fc4-133">Click OK.</span></span>
8. <span data-ttu-id="32fc4-134">Typ een waarde in het veld Expressie.</span><span class="sxs-lookup"><span data-stu-id="32fc4-134">In the Expression field, type a value.</span></span>
    * <span data-ttu-id="32fc4-135">Typ bijvoorbeeld 50.</span><span class="sxs-lookup"><span data-stu-id="32fc4-135">For example, type 50.</span></span>  
9. <span data-ttu-id="32fc4-136">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="32fc4-136">Close the page.</span></span>
10. <span data-ttu-id="32fc4-137">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="32fc4-137">Close the page.</span></span>


