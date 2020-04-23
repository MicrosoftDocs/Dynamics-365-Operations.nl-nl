---
title: Selectiecriteria voor verkoopprijs maken
description: Deze procedure laat zien hoe u een selectiecriterium voor de verkoopprijs maakt voor op kenmerk gebaseerde verkoopprijsmodellen.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6d1385a83da5b6448a9c753d7469979796043b60
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203764"
---
# <a name="create-sales-price-selection-criteria"></a><span data-ttu-id="820cd-103">Selectiecriteria voor verkoopprijs maken</span><span class="sxs-lookup"><span data-stu-id="820cd-103">Create sales price selection criteria</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="820cd-104">Deze procedure laat zien hoe u een selectiecriterium voor de verkoopprijs maakt voor op kenmerk gebaseerde verkoopprijsmodellen.</span><span class="sxs-lookup"><span data-stu-id="820cd-104">This procedure shows how to create a sales price selection criterion for attribute-based sales price models.</span></span> <span data-ttu-id="820cd-105">Deze procedure vereist dat er ten minste één verkoopprijsmodel beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="820cd-105">This procedure requires that at least one sales price model be available.</span></span> <span data-ttu-id="820cd-106">Dit voorbeeld gebruikt het verkoopprijsmodel van de luidsprekeroplossing in het USMF-bedrijf met demogegevens.</span><span class="sxs-lookup"><span data-stu-id="820cd-106">This example uses the price model for the Speaker solution sales price model in the USMF demo data company.</span></span> <span data-ttu-id="820cd-107">Gewoonlijk gebruikt een productmanager deze procedure.</span><span class="sxs-lookup"><span data-stu-id="820cd-107">Typically, a product manager uses this procedure.</span></span>


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a><span data-ttu-id="820cd-108">Voeg een nieuw criterium voor een bestaand verkoopprijsmodel toe</span><span class="sxs-lookup"><span data-stu-id="820cd-108">Add a new criterion for an existing sales price model</span></span>
1. <span data-ttu-id="820cd-109">Klik op Definitie van productvariantmodel.</span><span class="sxs-lookup"><span data-stu-id="820cd-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="820cd-110">Klik op Productconfiguratiemodellen.</span><span class="sxs-lookup"><span data-stu-id="820cd-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="820cd-111">Selecteer in de lijst de rij voor het productmodel van de luidsprekeroplossing, maar klik niet op de koppeling voor de modelnaam.</span><span class="sxs-lookup"><span data-stu-id="820cd-111">In the list, select the row for the Speaker solution product model, but don't click the link for the model name.</span></span>
4. <span data-ttu-id="820cd-112">Klik in het actievenster op Model.</span><span class="sxs-lookup"><span data-stu-id="820cd-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="820cd-113">Klik op Criteria voor prijsmodel.</span><span class="sxs-lookup"><span data-stu-id="820cd-113">Click Price model criteria.</span></span>
6. <span data-ttu-id="820cd-114">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="820cd-114">Click New.</span></span>
7. <span data-ttu-id="820cd-115">Typ 'Klantengroep 10' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="820cd-115">In the Name field, type 'Customer group 10'.</span></span>
    * <span data-ttu-id="820cd-116">De naam van het criterium prijsmodel wordt gebruikt om de onderliggende selectiecriteria te identificeren.</span><span class="sxs-lookup"><span data-stu-id="820cd-116">The name of the price model criterion is used to help identify the underlying selection criteria.</span></span>  
8. <span data-ttu-id="820cd-117">Typ of selecteer een waarde in het veld Prijsmodel.</span><span class="sxs-lookup"><span data-stu-id="820cd-117">In the Price model field, enter or select a value.</span></span>
9. <span data-ttu-id="820cd-118">Selecteer Verkooporder in het veld Ordertype.</span><span class="sxs-lookup"><span data-stu-id="820cd-118">In the Order type field, select Sales order.</span></span>
    * <span data-ttu-id="820cd-119">Het ordertype bepaalt de databasevelden die voor de selectiequery beschikbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="820cd-119">The order type determines the database fields that will be available for the selection query.</span></span>  
10. <span data-ttu-id="820cd-120">Typ een datum in het veld Geldig vanaf.</span><span class="sxs-lookup"><span data-stu-id="820cd-120">In the Valid from field, enter a date.</span></span>
11. <span data-ttu-id="820cd-121">Typ een datum in het veld Vervallen op.</span><span class="sxs-lookup"><span data-stu-id="820cd-121">In the Expire by field, enter a date.</span></span>
12. <span data-ttu-id="820cd-122">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="820cd-122">Click Save.</span></span>

## <a name="create-the-query-for-the-selection-criteria"></a><span data-ttu-id="820cd-123">Maak de query voor de selectiecriteria</span><span class="sxs-lookup"><span data-stu-id="820cd-123">Create the query for the selection criteria</span></span>
1. <span data-ttu-id="820cd-124">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="820cd-124">Click Edit.</span></span>
2. <span data-ttu-id="820cd-125">Selecteer Klanten in het veld Tabel.</span><span class="sxs-lookup"><span data-stu-id="820cd-125">In the Table field, select Customers.</span></span> 
3. <span data-ttu-id="820cd-126">Selecteer Klantengroep in het veld Veld.</span><span class="sxs-lookup"><span data-stu-id="820cd-126">In the Field field, select Customer group.</span></span>
    * <span data-ttu-id="820cd-127">In dit voorbeeld wordt een specifieke klantengroep voor de selectiecriteria gebruikt.</span><span class="sxs-lookup"><span data-stu-id="820cd-127">In this example, we will use a specific customer group for the selection criteria.</span></span>  
4. <span data-ttu-id="820cd-128">Selecteer Klantengroep 10 in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="820cd-128">In the Criteria field, select Customer group 10.</span></span> 
5. <span data-ttu-id="820cd-129">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="820cd-129">Click OK.</span></span>

