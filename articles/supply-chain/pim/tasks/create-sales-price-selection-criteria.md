---
title: Selectiecriteria voor verkoopprijs maken
description: Deze procedure laat zien hoe u een selectiecriterium voor de verkoopprijs maakt voor op kenmerk gebaseerde verkoopprijsmodellen.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 69d22c3321beaa2667ee20bff00acd746714b993
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920526"
---
# <a name="create-sales-price-selection-criteria"></a><span data-ttu-id="b3828-103">Selectiecriteria voor verkoopprijs maken</span><span class="sxs-lookup"><span data-stu-id="b3828-103">Create sales price selection criteria</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b3828-104">Deze procedure laat zien hoe u een selectiecriterium voor de verkoopprijs maakt voor op kenmerk gebaseerde verkoopprijsmodellen.</span><span class="sxs-lookup"><span data-stu-id="b3828-104">This procedure shows how to create a sales price selection criterion for attribute-based sales price models.</span></span> <span data-ttu-id="b3828-105">Deze procedure vereist dat er ten minste één verkoopprijsmodel beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="b3828-105">This procedure requires that at least one sales price model be available.</span></span> <span data-ttu-id="b3828-106">Dit voorbeeld gebruikt het verkoopprijsmodel van de luidsprekeroplossing in het USMF-bedrijf met demogegevens.</span><span class="sxs-lookup"><span data-stu-id="b3828-106">This example uses the price model for the Speaker solution sales price model in the USMF demo data company.</span></span> <span data-ttu-id="b3828-107">Gewoonlijk gebruikt een productmanager deze procedure.</span><span class="sxs-lookup"><span data-stu-id="b3828-107">Typically, a product manager uses this procedure.</span></span>

## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a><span data-ttu-id="b3828-108">Voeg een nieuw criterium voor een bestaand verkoopprijsmodel toe</span><span class="sxs-lookup"><span data-stu-id="b3828-108">Add a new criterion for an existing sales price model</span></span>

1. <span data-ttu-id="b3828-109">Ga naar **Productgegevensbeheer \> Producten \> Productconfiguratiemodellen**.</span><span class="sxs-lookup"><span data-stu-id="b3828-109">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="b3828-110">Selecteer in de lijst de rij voor het productmodel van de luidsprekeroplossing, maar selecteer niet de koppeling voor de modelnaam.</span><span class="sxs-lookup"><span data-stu-id="b3828-110">In the list, select the row for the Speaker solution product model, but don't select the link for the model name.</span></span>
1. <span data-ttu-id="b3828-111">Selecteer **Model** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="b3828-111">On the Action Pane, select **Model**.</span></span>
1. <span data-ttu-id="b3828-112">Selecteer **Criteria voor prijsmodel**.</span><span class="sxs-lookup"><span data-stu-id="b3828-112">Select **Price model criteria**.</span></span>
1. <span data-ttu-id="b3828-113">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="b3828-113">Select **New**.</span></span>
1. <span data-ttu-id="b3828-114">Typ 'Klantengroep 10' in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="b3828-114">In the **Name** field, type 'Customer group 10'.</span></span>
    * <span data-ttu-id="b3828-115">De naam van het criterium prijsmodel wordt gebruikt om de onderliggende selectiecriteria te identificeren.</span><span class="sxs-lookup"><span data-stu-id="b3828-115">The name of the price model criterion is used to help identify the underlying selection criteria.</span></span>  
1. <span data-ttu-id="b3828-116">Typ of selecteer een waarde in het veld **Prijsmodel**.</span><span class="sxs-lookup"><span data-stu-id="b3828-116">In the **Price model** field, enter or select a value.</span></span>
1. <span data-ttu-id="b3828-117">Selecteer *Verkooporder* in het veld **Ordertype**.</span><span class="sxs-lookup"><span data-stu-id="b3828-117">In the **Order type** field, select *Sales order*.</span></span>
    * <span data-ttu-id="b3828-118">Het ordertype bepaalt de databasevelden die voor de selectiequery beschikbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="b3828-118">The order type determines the database fields that will be available for the selection query.</span></span>  
1. <span data-ttu-id="b3828-119">Typ een datum in het veld **Geldig vanaf**.</span><span class="sxs-lookup"><span data-stu-id="b3828-119">In the **Valid from** field, enter a date.</span></span>
1. <span data-ttu-id="b3828-120">Typ een datum in het veld **Vervallen op**.</span><span class="sxs-lookup"><span data-stu-id="b3828-120">In the **Expire by** field, enter a date.</span></span>
1. <span data-ttu-id="b3828-121">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="b3828-121">Select **Save**.</span></span>

## <a name="create-the-query-for-the-selection-criteria"></a><span data-ttu-id="b3828-122">Maak de query voor de selectiecriteria</span><span class="sxs-lookup"><span data-stu-id="b3828-122">Create the query for the selection criteria</span></span>

1. <span data-ttu-id="b3828-123">Selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="b3828-123">Select **Edit**.</span></span>
2. <span data-ttu-id="b3828-124">Selecteer **Klanten** in het veld *Tabel*.</span><span class="sxs-lookup"><span data-stu-id="b3828-124">In the **Table** field, select *Customers*.</span></span>
3. <span data-ttu-id="b3828-125">Selecteer **Klantengroep** in het veld *Veld*.</span><span class="sxs-lookup"><span data-stu-id="b3828-125">In the **Field** field, select *Customer group*.</span></span>
    * <span data-ttu-id="b3828-126">In dit voorbeeld wordt een specifieke klantengroep voor de selectiecriteria gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b3828-126">In this example, we will use a specific customer group for the selection criteria.</span></span>  
4. <span data-ttu-id="b3828-127">Selecteer **Klantengroep 10** in het veld *Criteria*.</span><span class="sxs-lookup"><span data-stu-id="b3828-127">In the **Criteria** field, select *Customer group 10*.</span></span>
5. <span data-ttu-id="b3828-128">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="b3828-128">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]