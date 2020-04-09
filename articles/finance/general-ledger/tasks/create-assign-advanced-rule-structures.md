---
title: Geavanceerde regelstructuren maken en toewijzen
description: In dit onderwerp wordt uitgelegd hoe u een geavanceerde regelstructuur maakt en toewijst aan een rekeningstructuur.
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cb18b96d6d7db84262f8fcfadb15afa80e2fa3d8
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145118"
---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="76daa-103">Geavanceerde regelstructuren maken en toewijzen</span><span class="sxs-lookup"><span data-stu-id="76daa-103">Create and assign advanced rule structures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="76daa-104">In dit onderwerp wordt uitgelegd hoe u een geavanceerde regelstructuur maakt en toewijst aan een rekeningstructuur.</span><span class="sxs-lookup"><span data-stu-id="76daa-104">This topic explains how to create and assign an advanced rule structure to an account structure.</span></span> <span data-ttu-id="76daa-105">Deze taakbegeleiding gebruikt het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="76daa-105">This guide uses the USMF demo company.</span></span>

## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="76daa-106">Een geavanceerde regelstructuur maken</span><span class="sxs-lookup"><span data-stu-id="76daa-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="76daa-107">Ga naar **Navigatievenster > Modules > Grootboek > Rekeningschema > Structuren > Geavanceerde regelstructuren**.</span><span class="sxs-lookup"><span data-stu-id="76daa-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Advanced rule structures**.</span></span>
2. <span data-ttu-id="76daa-108">Selecteer **Nieuw** om het uitklapvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="76daa-108">Select **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="76daa-109">Typ in het veld **Geavanceerde regelstructuur** een naam om de regelstructuur te beschrijven.</span><span class="sxs-lookup"><span data-stu-id="76daa-109">In the **Advanced rule structure** field, type a name to describe the rule structure.</span></span>
4. <span data-ttu-id="76daa-110">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="76daa-110">Select **OK**.</span></span>
5. <span data-ttu-id="76daa-111">Selecteer **Segment toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="76daa-111">Select **Add segment**.</span></span>
6. <span data-ttu-id="76daa-112">Selecteer een financiële dimensie in de lijst van segmenten.</span><span class="sxs-lookup"><span data-stu-id="76daa-112">In the list of segments, select a financial dimension.</span></span> <span data-ttu-id="76daa-113">Bijvoorbeeld **Opslag**.</span><span class="sxs-lookup"><span data-stu-id="76daa-113">For example, **Store**.</span></span>  
7. <span data-ttu-id="76daa-114">Selecteer **Segment toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="76daa-114">Select **Add segment**.</span></span>
8. <span data-ttu-id="76daa-115">Selecteer **Activeren**.</span><span class="sxs-lookup"><span data-stu-id="76daa-115">Select **Activate**.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="76daa-116">Een geavanceerde regel toepassen op een rekeningstructuur</span><span class="sxs-lookup"><span data-stu-id="76daa-116">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="76daa-117">Ga naar **navigatievenster > Modules > Grootboek > Rekeningschema > Structuren > Regelstructuren configureren**.</span><span class="sxs-lookup"><span data-stu-id="76daa-117">Go to **navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="76daa-118">Zoek en selecteer in de lijst de rekeningstructuur waarop u de geavanceerde regel wilt toepassen.</span><span class="sxs-lookup"><span data-stu-id="76daa-118">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
3. <span data-ttu-id="76daa-119">Selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="76daa-119">Select **Edit**.</span></span> <span data-ttu-id="76daa-120">U kunt ook **Geavanceerde regels** selecteren, waarna u wordt gevraagd om de rekeningstructuur in de **Conceptmodus** te plaatsen.</span><span class="sxs-lookup"><span data-stu-id="76daa-120">You can also select **Advanced rules** and you will be prompted to put the account structure in **Draft mode**.</span></span>  
4. <span data-ttu-id="76daa-121">Selecteer **Geavanceerde regels**.</span><span class="sxs-lookup"><span data-stu-id="76daa-121">Select **Advanced rules**.</span></span>
5. <span data-ttu-id="76daa-122">Selecteer **Nieuw** om het uitklapvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="76daa-122">Select **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="76daa-123">Typ een waarde in het veld **Geavanceerde regel**.</span><span class="sxs-lookup"><span data-stu-id="76daa-123">In the **Advanced rule** field, type a value.</span></span>
7. <span data-ttu-id="76daa-124">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="76daa-124">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="76daa-125">Selecteer **Maken**.</span><span class="sxs-lookup"><span data-stu-id="76daa-125">Select **Create**.</span></span>
9. <span data-ttu-id="76daa-126">Selecteer **Nieuwe criteria toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="76daa-126">Select **Add new criteria**.</span></span>
10. <span data-ttu-id="76daa-127">Selecteer een hoofdrekening of financiële dimensie in het veld **Waar**.</span><span class="sxs-lookup"><span data-stu-id="76daa-127">In the **Where** field, select main account or a financial dimension.</span></span>
11. <span data-ttu-id="76daa-128">Selecteer in het veld **Operator** een optie, zoals **ligt tussen** en **bevat**.</span><span class="sxs-lookup"><span data-stu-id="76daa-128">In the **Operator** field, select an option, such as **is between** and **includes**.</span></span>
12. <span data-ttu-id="76daa-129">Typ een waarde in het veld **Waarde**.</span><span class="sxs-lookup"><span data-stu-id="76daa-129">In the **Value** field, type a value.</span></span>
13. <span data-ttu-id="76daa-130">Typ een waarde in het veld **Tot en met**.</span><span class="sxs-lookup"><span data-stu-id="76daa-130">In the **through** field, type a value.</span></span>
14. <span data-ttu-id="76daa-131">Selecteer **Toevoegen** om het uitklapvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="76daa-131">Select **Add** to open the drop dialog.</span></span>
15. <span data-ttu-id="76daa-132">Zoek in de lijst de geavanceerde regelstructuur die u wilt gebruiken wanneer aan de criteria zijn voldaan.</span><span class="sxs-lookup"><span data-stu-id="76daa-132">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
16. <span data-ttu-id="76daa-133">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="76daa-133">Select **Add**.</span></span>
17. <span data-ttu-id="76daa-134">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="76daa-134">Close the page.</span></span>
18. <span data-ttu-id="76daa-135">Selecteer **Activeren**.</span><span class="sxs-lookup"><span data-stu-id="76daa-135">Select **Activate**.</span></span>

