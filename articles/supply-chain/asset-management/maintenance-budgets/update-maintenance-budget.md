---
title: Onderhoudsbudgetten bijwerken
description: In dit onderwerp wordt uitgelegd hoe u een onderhoudsbudget bijwerkt in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 21aba6224bba98eb9bbb423847e123616003b5d9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253465"
---
# <a name="update-maintenance-budgets"></a><span data-ttu-id="15e21-103">Onderhoudsbudgetten bijwerken</span><span class="sxs-lookup"><span data-stu-id="15e21-103">Update maintenance budgets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="15e21-104">Op de pagina **Onderhoudsbudgetregels** worden alle budgetregels weer gegeven die zijn gemaakt voor het budget dat is geselecteerd op de pagina **Onderhoudsbudgetten**.</span><span class="sxs-lookup"><span data-stu-id="15e21-104">The **Maintenance budget lines** page shows all the budget lines that have been created for the budget that is selected on the **Maintenance budgets** page.</span></span> <span data-ttu-id="15e21-105">(Zie [Onderhoudsbudgetten maken](create-maintenance-budget.md) voor meer informatie.) U kunt de regels voor het onderhoudsbudget opnieuw berekenen en aanpassen totdat het onderhoudsbudget is goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="15e21-105">(For more information, see [Create maintenance budgets](create-maintenance-budget.md).) You can recalculate and adjust maintenance budget lines until the maintenance budget is approved.</span></span> <span data-ttu-id="15e21-106">Nadat de budgetperiode is verstreken en de kosten in het Activabeheer zijn geboekt, kunt u de budgetregels ook bijwerken met de werkelijke kosten.</span><span class="sxs-lookup"><span data-stu-id="15e21-106">After the budget period has passed, and costs have been posted in Asset Management, you can also update the budget lines with actual costs.</span></span>

## <a name="recalculate-a-maintenance-budget"></a><span data-ttu-id="15e21-107">Een onderhoudsbudget opnieuw berekenen</span><span class="sxs-lookup"><span data-stu-id="15e21-107">Recalculate a maintenance budget</span></span>

<span data-ttu-id="15e21-108">U kunt een onderhoudsbudget opnieuw berekenen op de pagina **Onderhoudsbudgetregels**.</span><span class="sxs-lookup"><span data-stu-id="15e21-108">You can recalculate a maintenance budget on the **Maintenance budget lines** page.</span></span> <span data-ttu-id="15e21-109">Wanneer u een onderhoudsbudget opnieuw berekent, worden de bestaande budgetregels verwijderd en wordt er een nieuwe berekening uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="15e21-109">When you recalculate a maintenance budget, the existing budget lines are deleted, and a new calculation is done.</span></span>

1. <span data-ttu-id="15e21-110">Selecteer op de pagina **Onderhoudsbudgetregels** **Opnieuw berekenen**.</span><span class="sxs-lookup"><span data-stu-id="15e21-110">On the **Maintenance budget lines** page, select **Recalculate**.</span></span>
2. <span data-ttu-id="15e21-111">Voer in het dialoogvenster **Budget opnieuw berekenen** de vereiste wijzigingen voor de nieuwe berekening in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="15e21-111">In the **Recalculate budget** dialog box, make the required changes for the new calculation, and then select **OK**.</span></span>

<span data-ttu-id="15e21-112">Nieuwe budgetregels worden gemaakt op basis van de waarden die u instelt.</span><span class="sxs-lookup"><span data-stu-id="15e21-112">New budget lines are created according to the values that you set.</span></span>

## <a name="adjust-budget-lines"></a><span data-ttu-id="15e21-113">Budgetregels aanpassen</span><span class="sxs-lookup"><span data-stu-id="15e21-113">Adjust budget lines</span></span>

<span data-ttu-id="15e21-114">In plaats van het gehele onderhoudsbudget opnieuw te berekenen, kunt u geselecteerde regels aanpassen die zijn gerelateerd aan budgetkosten.</span><span class="sxs-lookup"><span data-stu-id="15e21-114">Instead of recalculating the whole maintenance budget, you can adjust selected lines that are related to budget costs.</span></span>

1. <span data-ttu-id="15e21-115">Selecteer op de pagina **Onderhoudsbudgetregels** de regels waarvoor u de budgetkosten wilt bijwerken.</span><span class="sxs-lookup"><span data-stu-id="15e21-115">On the **Maintenance budget lines** page, select the lines to update the budget cost for.</span></span>
2. <span data-ttu-id="15e21-116">Selecteer **aanpassen**.</span><span class="sxs-lookup"><span data-stu-id="15e21-116">Select **Adjust**.</span></span>
3. <span data-ttu-id="15e21-117">Als u een bedrag wilt toevoegen aan de geselecteerde regels, schakelt u het selectievakje **Kosten toevoegen** in en voert u vervolgens de waarde in het veld **Waarde toevoegen** in.</span><span class="sxs-lookup"><span data-stu-id="15e21-117">To add an amount to the selected lines, select the **Add cost** check box, and then enter the value in the **Add value** field.</span></span>
4. <span data-ttu-id="15e21-118">Als u de gebudgetteerde kosten voor de geselecteerde budgetregels met een factor wilt vermenigvuldigen schakelt u het selectievakje **Kosten vermenigvuldigen** in en voert u de factor in het veld **Waarde vermenigvuldigen** in.</span><span class="sxs-lookup"><span data-stu-id="15e21-118">To multiply the budget cost on the selected budget lines by a factor, select the **Multiply cost** check box, and enter the factor in the **Multiply value** field.</span></span>

    <span data-ttu-id="15e21-119">Als u bijvoorbeeld **1,2** invoert in het veld **Waarde vermenigvuldigen**, verhoogt u de budgetkosten voor de geselecteerde regels met 20 procent.</span><span class="sxs-lookup"><span data-stu-id="15e21-119">For example, if you enter **1.2** in the **Multiply value** field, you increase the budget cost on the selected lines by 20 percent.</span></span> <span data-ttu-id="15e21-120">Als u **0,7** invoert, verlaagt u de budgetkosten voor de geselecteerde regels met 30 procent.</span><span class="sxs-lookup"><span data-stu-id="15e21-120">If you enter **0.7**, you reduce the budget cost on the selected lines by 30 percent.</span></span>

5. <span data-ttu-id="15e21-121">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="15e21-121">Select **OK**.</span></span>

<span data-ttu-id="15e21-122">De geselecteerde budgetregels worden bijgewerkt volgens de waarden die u in stap 3 of 4 hebt ingesteld.</span><span class="sxs-lookup"><span data-stu-id="15e21-122">The selected budget lines are updated according to the values that you set in step 3 or 4.</span></span>

## <a name="update-actual-costs"></a><span data-ttu-id="15e21-123">Werkelijke kosten bijwerken</span><span class="sxs-lookup"><span data-stu-id="15e21-123">Update actual costs</span></span>

<span data-ttu-id="15e21-124">Nadat de periode bij de budgetregels is verstreken en de kosten in het Activabeheer zijn geboekt, kunt u de werkelijke kosten bijwerken in het onderhoudsbudget.</span><span class="sxs-lookup"><span data-stu-id="15e21-124">After the dates on the budget lines have passed, and actual costs have been posted in Asset Management, you can update the actual costs on the maintenance budget.</span></span>

1. <span data-ttu-id="15e21-125">Selecteer op de pagina **Onderhoudsbudgetregels** **Kosten bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="15e21-125">On the **Maintenance budget lines** page, select **Update cost**.</span></span>
2. <span data-ttu-id="15e21-126">Selecteer in het dialoogvenster **Werkelijke kosten berekenen** de optie **OK**.</span><span class="sxs-lookup"><span data-stu-id="15e21-126">In the **Calculate actual cost** dialog box, select **OK**.</span></span>

<span data-ttu-id="15e21-127">De velden **Werkelijke kosten** op de budgetregels worden bijgewerkt als de werkelijke kosten zijn geboekt.</span><span class="sxs-lookup"><span data-stu-id="15e21-127">The **Actual cost** fields on the budget lines are updated if actual costs have been posted.</span></span> <span data-ttu-id="15e21-128">Er kunnen nieuwe budgetregels worden gegenereerd als er nieuwe activatypen zijn gemaakt nadat u het budget hebt gemaakt, en als deze activatypen zijn gebruikt voor activa waarvoor werkorders zijn gemaakt en gerelateerde kosten zijn geboekt.</span><span class="sxs-lookup"><span data-stu-id="15e21-128">New budget lines might be generated if new asset types have been created since you created the budget, and if those asset types have been used on assets that work orders have been created for and related costs have been posted for.</span></span> <span data-ttu-id="15e21-129">Op nieuwe budgetregels worden alleen de werkelijke kosten weergegeven, omdat er geen budgetkosten voor zijn berekend.</span><span class="sxs-lookup"><span data-stu-id="15e21-129">New budget lines show only actual costs, because no budget costs were calculated for them.</span></span>

> [!NOTE]
> <span data-ttu-id="15e21-130">Als u een overzicht wilt weergeven van de werkelijke kosten die zijn onderverdeeld in preventieve, corrigerende en investeringskosten, kunt u een berekening uitvoeren voor dezelfde periode op de pagina **Beheer activakosten**.</span><span class="sxs-lookup"><span data-stu-id="15e21-130">To see an overview of actual costs divided into preventive, corrective, and investment costs, you can do a calculation for the same period on the **Asset cost control** page.</span></span> 

## <a name="manually-add-budget-lines"></a><span data-ttu-id="15e21-131">Handmatig budgetregels toevoegen.</span><span class="sxs-lookup"><span data-stu-id="15e21-131">Manually add budget lines</span></span>

<span data-ttu-id="15e21-132">Op de pagina **Onderhoudsbudgetregels** kunt u handmatig een nieuwe budgetregel toevoegen door **Nieuw** te selecteren en vervolgens selecties te maken op de regel.</span><span class="sxs-lookup"><span data-stu-id="15e21-132">On the **Maintenance budget lines** page, you can manually add a new budget line by selecting **New** and then making selections on the line.</span></span> <span data-ttu-id="15e21-133">Hier volgen enkele voorbeelden van situaties waarin deze aanpak nuttig kan zijn:</span><span class="sxs-lookup"><span data-stu-id="15e21-133">Here are some examples of situations where this approach might be useful:</span></span>

- <span data-ttu-id="15e21-134">U weet dat de revisie van bepaalde activa momenteel in de planningsfase is, maar gerelateerde taken zijn nog niet in het Activabeheer opgenomen.</span><span class="sxs-lookup"><span data-stu-id="15e21-134">You know that refurbishment of some assets is currently in the planning phase, but related jobs haven't yet been created in Asset Management.</span></span> <span data-ttu-id="15e21-135">Budgetkosten voor deze taken moeten echter worden opgenomen in het onderhoudsbudget.</span><span class="sxs-lookup"><span data-stu-id="15e21-135">However, you want budget costs for those jobs to be included in the maintenance budget.</span></span>
- <span data-ttu-id="15e21-136">Nieuwe activa of activatypen zijn gemaakt nadat u het onderhoudsbudget hebt gemaakt, maar er zijn nog geen onderhoudsplannen voor de activa of activatypen ingesteld.</span><span class="sxs-lookup"><span data-stu-id="15e21-136">New assets or asset types have been created since you made the maintenance budget, but maintenance plans haven't yet been set up on those assets or asset types.</span></span> <span data-ttu-id="15e21-137">Budgetkosten voor deze activatypen moeten echter worden opgenomen in het onderhoudsbudget.</span><span class="sxs-lookup"><span data-stu-id="15e21-137">However, you want budget costs for those asset types to be included in the maintenance budget.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]