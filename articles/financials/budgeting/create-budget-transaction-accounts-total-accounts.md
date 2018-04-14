---
title: Een budget maken op basis van transactierekeningen en totaalrekeningen.
description: Dit artikel biedt een overzicht van het proces voor het maken van budgetten op basis van totaalrekeningen. Daarnaast wordt beschreven hoe u budgetbeheer voor totaalrekeningen inschakelt, als budgetbeheer vereist is.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetControlConfiguration, BudgetPlanGenerate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 85b778caf209c2fb1845665169e08210bfeb45c1
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---

# <a name="create-a-budget-from-transaction-accounts-and-total-accounts"></a><span data-ttu-id="bf650-104">Een budget maken op basis van transactierekeningen en totaalrekeningen.</span><span class="sxs-lookup"><span data-stu-id="bf650-104">Create a budget from transaction accounts and total accounts</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="bf650-105">Dit artikel biedt een overzicht van het proces voor het maken van budgetten op basis van totaalrekeningen.</span><span class="sxs-lookup"><span data-stu-id="bf650-105">This article provides an overview of the process for creating budgets based on total accounts.</span></span> <span data-ttu-id="bf650-106">Daarnaast wordt beschreven hoe u budgetbeheer voor totaalrekeningen inschakelt, als budgetbeheer vereist is.</span><span class="sxs-lookup"><span data-stu-id="bf650-106">It also explains how to turn on budget control for total accounts, if budget control is required.</span></span>

<span data-ttu-id="bf650-107">Zowel met budgetplan- als budgetregisterinvoerdocumenten is budgettering voor hoofdrekeningen mogelijk die het hoofdrekeningtype **Totaal** hebben.</span><span class="sxs-lookup"><span data-stu-id="bf650-107">Both budget plan and budget register entry documents allow for budgeting on main accounts that have a main account type of **Total**.</span></span> <span data-ttu-id="bf650-108">Werkelijke kosten kunnen alleen naar transactiehoofdrekeningen worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="bf650-108">Actuals can be posted only to transactional main accounts.</span></span> 

<span data-ttu-id="bf650-109">Voor het periodieke proces **Budgetplan genereren op basis van grootboek** op het tabblad **Bron** kunt u het hoofdrekeningtype **Totaal** als criterium opgeven.</span><span class="sxs-lookup"><span data-stu-id="bf650-109">For the **Generate budget plan from General ledger** periodic process, on the **Source** tab, you can specify the **Total** main account type as a criterion.</span></span> <span data-ttu-id="bf650-110">In dit geval wordt elke totale hoofdrekening opgenomen in het doelbudgetplan en is het bedrag gelijk aan het totaalbedrag van het bereik van geselecteerde hoofdrekeningen.</span><span class="sxs-lookup"><span data-stu-id="bf650-110">In this case, each total main account will be included in the target budget plan, and the amount will equal the total amount of the range of selected main accounts.</span></span> 

<span data-ttu-id="bf650-111">U kunt budgetbeheer voor hoofdrekeningen van het type **Totaal** activeren.</span><span class="sxs-lookup"><span data-stu-id="bf650-111">You can activate budget control for main accounts of the **Total** type.</span></span> <span data-ttu-id="bf650-112">Deze functionaliteit wordt ondersteund via het gebruik van budgetgroepen.</span><span class="sxs-lookup"><span data-stu-id="bf650-112">This functionality is supported through the use of budget groups.</span></span> <span data-ttu-id="bf650-113">Voor elke totale hoofdrekening moet het budget dat moet worden beheerd voor een budgetgroep, worden gemaakt op de pagina **Budgetbeheerconfiguratie**.</span><span class="sxs-lookup"><span data-stu-id="bf650-113">For each total main account, the budget that should be controlled for a budget group must be created on the **Budget control configuration **page.</span></span> <span data-ttu-id="bf650-114">De criteria die u opgeeft, moeten de totale hoofdrekening en het bereik van rekeningen bevatten.</span><span class="sxs-lookup"><span data-stu-id="bf650-114">The criteria that you specify must include the total main account and the range of accounts.</span></span> <span data-ttu-id="bf650-115">Om het proces voor het maken van budgetgroepen te versnellen, kunt u profiteren van de gegevensentiteit van budgetbeheergroepen.</span><span class="sxs-lookup"><span data-stu-id="bf650-115">To speed up the process of creating budget groups, you can take advantage of the Budget control groups data entity.</span></span> 

<span data-ttu-id="bf650-116">Wanneer een budget wordt gebruikt bij rapportage, zoals in een financieel overzicht, bestaat de som van het budget voor de totaalrekening uit de volgende bedragen:</span><span class="sxs-lookup"><span data-stu-id="bf650-116">When a budget is used in reporting, such as on a financial statement, the budget sum for the total account consists of the following amounts:</span></span>

-   <span data-ttu-id="bf650-117">De budgetten die op elke transactiegrootboekrekening binnen het interval van de totaalrekening zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="bf650-117">The budgets that are created from each transaction ledger account in the interval of the total account.</span></span>
-   <span data-ttu-id="bf650-118">Het budgetbedrag dat direct op de totaalrekening is ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="bf650-118">The budget amount that is entered directly on the total account.</span></span>

<span data-ttu-id="bf650-119">Zo kunt u afzonderlijke budgetten voor de belangrijkste transactierekeningen binnen het interval van de totaalrekening maken en het beschikbare budgetbedrag vervolgens toevoegen aan de totaalrekening.</span><span class="sxs-lookup"><span data-stu-id="bf650-119">Therefore, you can create separate budgets for the most significant transaction accounts in the interval of the total account, and then add the available budget amount to the total account.</span></span>




