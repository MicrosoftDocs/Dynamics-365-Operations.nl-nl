---
title: Onderhoudsbudgetten maken
description: In dit onderwerp wordt uitgelegd hoe u een onderhoudsbudget maakt in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetBudgetLineAdjust, EntAssetBudget, EntAssetBudgetRecalc, EntAssetBudgetCopy, EntAssetBudgetLine, EntAssetBudgetCreate, EntAssetBudgetApprove, EntAssetBudgetCalculateActualCost
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 602a00060c1e56285d9954981d019bececaf90fd
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020984"
---
# <a name="create-maintenance-budgets"></a><span data-ttu-id="1994e-103">Onderhoudsbudgetten maken</span><span class="sxs-lookup"><span data-stu-id="1994e-103">Create maintenance budgets</span></span>

[!include [banner](../../includes/banner.md)]

 



<span data-ttu-id="1994e-104">Onderhoudsbudgetten worden gebruikt om een overzicht te geven van verwachte kosten voor preventief onderhoud.</span><span class="sxs-lookup"><span data-stu-id="1994e-104">Maintenance budgets are used to provide an overview of expected costs for preventive maintenance.</span></span> <span data-ttu-id="1994e-105">Budgetregels worden berekend op basis van de regels voor onderhoudsplanning waarvoor de verwachte begindatum gedurende de budgetperiode is verstreken.</span><span class="sxs-lookup"><span data-stu-id="1994e-105">Budget lines are calculated based on maintenance schedule lines that have an expected start date during the budget period.</span></span>

<span data-ttu-id="1994e-106">Onderhoudsbudgetten zijn gebaseerd op de kostentypen die worden gebruikt in Activabeheer: **Preventief**, **Corrigerend** en **Investering**.</span><span class="sxs-lookup"><span data-stu-id="1994e-106">Maintenance budgets are based on the cost types that are used in Asset Management: **Preventive**, **Corrective**, and **Investment**.</span></span> <span data-ttu-id="1994e-107">Budgetkosten voor investeringsonderhoud worden opgenomen voor actieve activa met een vervangingsdatum gedurende de budgetperiode en een gerelateerde vervangingswaarde.</span><span class="sxs-lookup"><span data-stu-id="1994e-107">Budget costs for investment maintenance are included for active assets that have a replacement date during the budget period and a related replacement value.</span></span> <span data-ttu-id="1994e-108">Budgetkosten voor correctief onderhoud worden opgenomen als er een eerdere correctiedatum is opgenomen in de budget berekening.</span><span class="sxs-lookup"><span data-stu-id="1994e-108">Budget costs for corrective maintenance are included if a past corrective date is included in the budget calculation.</span></span> <span data-ttu-id="1994e-109">In dat geval worden correctiekosten van een eerdere periode berekend voor dezelfde toekomstige periode waarvoor u het onderhoudsbudget hebt berekend.</span><span class="sxs-lookup"><span data-stu-id="1994e-109">In that case, corrective costs from an earlier period are calculated for the same future period that you calculate the maintenance budget for.</span></span>

## <a name="create-a-maintenance-budget"></a><span data-ttu-id="1994e-110">Een onderhoudsbudget maken</span><span class="sxs-lookup"><span data-stu-id="1994e-110">Create a maintenance budget</span></span>

1. <span data-ttu-id="1994e-111">Selecteer **Activabeheer** \> **Navragen** \> **Onderhoudsbudget** \> **Budget**.</span><span class="sxs-lookup"><span data-stu-id="1994e-111">Select **Asset management** \> **Inquiries** \> **Maintenance budget** \> **Budget**.</span></span>
2. <span data-ttu-id="1994e-112">Selecteer **Budget aanmaken**.</span><span class="sxs-lookup"><span data-stu-id="1994e-112">Select **Create budget**.</span></span>
3. <span data-ttu-id="1994e-113">Voer in het veld **Onderhoudsbudget** een budget-id in.</span><span class="sxs-lookup"><span data-stu-id="1994e-113">In the **Maintenance budget** field, enter a budget ID.</span></span>
4. <span data-ttu-id="1994e-114">Voer in het veld **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="1994e-114">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="1994e-115">Voer in het sneltabblad **Periode** in de velden **Begindatum** en **Einddatum** de begin- en einddatum van de budgetperiode in.</span><span class="sxs-lookup"><span data-stu-id="1994e-115">On the **Period** FastTab, in the **From date** and **To date** fields, enter the start and end dates of the budget period.</span></span>
5. <span data-ttu-id="1994e-116">Als u gecorrigeerde budgetkosten wilt opnemen die worden berekend op basis van de werkelijke kosten van een vorige periode, voert u in het veld **Corrigerend vanaf datum** de begindatum in van de periode waarvan deze kosten moeten worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="1994e-116">To include corrective budget costs that are calculated on the basis of actual costs from a previous period, in the **Corrective from date** field, enter the start date of the period that those costs should be included from.</span></span>
6. <span data-ttu-id="1994e-117">Stel, afhankelijk van het vereiste detail niveau in het budget, de relevante opties in op de vijf Sneltabbladen **Groeperen op**.</span><span class="sxs-lookup"><span data-stu-id="1994e-117">Depending on the level of detail that is required in the budget, set the relevant options on the five **Group by** FastTabs.</span></span>
7. <span data-ttu-id="1994e-118">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="1994e-118">Select **OK**.</span></span>
8. <span data-ttu-id="1994e-119">Selecteer **Budgetregels** om de **Budgetregels voor onderhoud** te openen. Hier kunt u alle budgetregels weergeven die voor de periode zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="1994e-119">Select **Budget lines** to open **Maintenance budget lines** page, where you can view all the budget lines that have been created for the period.</span></span>
9. <span data-ttu-id="1994e-120">Als u het budget wilt goedkeuren, selecteert u het op de pagina **Onderhoudsbudgetten** en selecteert u vervolgens **Goedkeuren**.</span><span class="sxs-lookup"><span data-stu-id="1994e-120">To approve the budget, select it on the **Maintenance budgets** page, and then select **Approve**.</span></span> <span data-ttu-id="1994e-121">Selecteer vervolgens in het dialoogvenster **Budget goedkeuren** de optie **OK**.</span><span class="sxs-lookup"><span data-stu-id="1994e-121">Then, in the **Approve budget** dialog box, select **OK**.</span></span> <span data-ttu-id="1994e-122">Uw naam wordt ingevoerd in het veld **Goedgekeurd door** op de pagina **Onderhoudsbudgetten**.</span><span class="sxs-lookup"><span data-stu-id="1994e-122">Your name is entered in the **Approved by** field on the **Maintenance budgets** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1994e-123">Nadat u een onderhoudsbudget hebt goedgekeurd, kunt u de gerelateerde regels niet opnieuw berekenen of aanpassen op de pagina **Budgetregels voor onderhoud**, tenzij u eerst de goedkeuring verwijdert.</span><span class="sxs-lookup"><span data-stu-id="1994e-123">After you've approved a maintenance budget, you can't recalculate or adjust the related lines on the **Maintenance budget lines** page unless you first remove the approval.</span></span> <span data-ttu-id="1994e-124">Als u de goedkeuring van een onderhoudsbudget wilt verwijderen, selecteert u het op de pagina **Onderhoudsbudgetten** en selecteert u vervolgens **Goedkeuren**.</span><span class="sxs-lookup"><span data-stu-id="1994e-124">To remove the approval of a maintenance budget, select it on the **Maintenance budgets** page, and then select **Approve**.</span></span> <span data-ttu-id="1994e-125">Selecteer vervolgens in het dialoogvenster **Budget goedkeuren** de optie **OK**.</span><span class="sxs-lookup"><span data-stu-id="1994e-125">Then, in the **Approve budget** dialog box, select **OK**.</span></span>

![Onderhoudsbudgetten](media/01-maintenance-budgets.png)

<span data-ttu-id="1994e-127">U kunt ook een nieuw onderhoudsbudget maken door een bestaand budget te kopiëren.</span><span class="sxs-lookup"><span data-stu-id="1994e-127">You can also create a new maintenance budget by copying an existing budget.</span></span> <span data-ttu-id="1994e-128">Selecteer op de pagina **Onderhoudsbudgetten** het te kopiëren budget en selecteer vervolgens **kopiëren**.</span><span class="sxs-lookup"><span data-stu-id="1994e-128">On the **Maintenance budgets** page, select the budget to copy, and then select **Copy**.</span></span> <span data-ttu-id="1994e-129">Deze benadering is handig als u bijvoorbeeld een budget hebt gemaakt voor één maand en dit wilt kopiëren naar andere maanden.</span><span class="sxs-lookup"><span data-stu-id="1994e-129">This approach is useful if, for example, you've created a budget for one month and want to copy it to other months.</span></span>

> [!NOTE]
> <span data-ttu-id="1994e-130">Het onderhoudsbudget berekent alleen budgetkosten op basis van regels voor onderhoudsplannings.</span><span class="sxs-lookup"><span data-stu-id="1994e-130">The maintenance budget calculates only budget costs based on maintenance schedule lines.</span></span> <span data-ttu-id="1994e-131">Als u de werkelijke kosten voor dezelfde periode wilt berekenen, kunt u die berekening uitvoeren op de pagina **Kostenbeheer activa**.</span><span class="sxs-lookup"><span data-stu-id="1994e-131">To calculate actual costs for the same period, you can do that calculation on the **Asset cost control** page.</span></span> 
