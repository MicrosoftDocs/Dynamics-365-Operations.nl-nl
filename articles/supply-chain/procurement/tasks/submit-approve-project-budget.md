---
title: Projectbudget indienen en goedkeuren
description: In deze procedure wordt beschreven hoe u het budget voor een project maakt en indient.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjBudget, WorkflowSubmitDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ffa7b4f23e63196947fef1b2180145702531e0a6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843908"
---
# <a name="submit-and-approve-project-budget"></a><span data-ttu-id="eaac5-103">Projectbudget indienen en goedkeuren</span><span class="sxs-lookup"><span data-stu-id="eaac5-103">Submit and approve project budget</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eaac5-104">In deze procedure wordt beschreven hoe u het budget voor een project maakt en indient.</span><span class="sxs-lookup"><span data-stu-id="eaac5-104">This procedure shows you how to create and submit the budget for a project.</span></span> 

<span data-ttu-id="eaac5-105">Wanneer u een projectbudget opstelt, kunt u geschatte opbrengsten en kosten voor een project invoeren en deze vervolgens gebruiken om de daadwerkelijke projecttransacties te controleren.</span><span class="sxs-lookup"><span data-stu-id="eaac5-105">When you create a project budget, you can enter estimated revenues and costs for a project, and then use those to control actual project transactions.</span></span> <span data-ttu-id="eaac5-106">Bij projectbudgettering moeten alle oorspronkelijke budgetten en revisies ter goedkeuring naar de projectworkflow worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="eaac5-106">In project budgeting, all original budgets and revisions must be sent to project workflow for approval.</span></span> <span data-ttu-id="eaac5-107">De werkstroom geeft u meer controle over het proces en registreert de wijzigingshistorie.</span><span class="sxs-lookup"><span data-stu-id="eaac5-107">Workflow gives you increased control over the process and creates a change history record.</span></span>

<span data-ttu-id="eaac5-108">Deze taak is gemaakt met de gegevensset van USSI.</span><span class="sxs-lookup"><span data-stu-id="eaac5-108">This task was created using the USSI data set.</span></span>

1. <span data-ttu-id="eaac5-109">Ga naar Projectbeheer en boekhouding > Projecten > Alle projecten.</span><span class="sxs-lookup"><span data-stu-id="eaac5-109">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="eaac5-110">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="eaac5-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="eaac5-111">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="eaac5-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="eaac5-112">Klik op Plannen in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="eaac5-112">On the Action Pane, click Plan.</span></span>
5. <span data-ttu-id="eaac5-113">Klik op Projectbudget.</span><span class="sxs-lookup"><span data-stu-id="eaac5-113">Click Project budget.</span></span>
6. <span data-ttu-id="eaac5-114">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="eaac5-114">In the Description field, type a value.</span></span>
7. <span data-ttu-id="eaac5-115">Vouw de sectie Kosten uit.</span><span class="sxs-lookup"><span data-stu-id="eaac5-115">Expand the Cost section</span></span>
8. <span data-ttu-id="eaac5-116">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="eaac5-116">Click New.</span></span>
9. <span data-ttu-id="eaac5-117">Selecteer een optie in het veld Transactietype.</span><span class="sxs-lookup"><span data-stu-id="eaac5-117">In the Transaction type field, select an option.</span></span>
10. <span data-ttu-id="eaac5-118">Typ of selecteer een waarde in het veld Categorie.</span><span class="sxs-lookup"><span data-stu-id="eaac5-118">In the Category field, enter or select a value.</span></span>
11. <span data-ttu-id="eaac5-119">Voer in het veld Oorspronkelijk budget een getal in.</span><span class="sxs-lookup"><span data-stu-id="eaac5-119">In the Original budget field, enter a number.</span></span>
12. <span data-ttu-id="eaac5-120">Vouw de sectie Opbrengsten uit.</span><span class="sxs-lookup"><span data-stu-id="eaac5-120">Expand the Revenues section.</span></span>
13. <span data-ttu-id="eaac5-121">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="eaac5-121">Click New.</span></span>
14. <span data-ttu-id="eaac5-122">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="eaac5-122">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="eaac5-123">Selecteer een optie in het veld Transactietype.</span><span class="sxs-lookup"><span data-stu-id="eaac5-123">In the Transaction type field, select an option.</span></span>
16. <span data-ttu-id="eaac5-124">Typ of selecteer een waarde in het veld Categorie.</span><span class="sxs-lookup"><span data-stu-id="eaac5-124">In the Category field, enter or select a value.</span></span>
17. <span data-ttu-id="eaac5-125">Voer in het veld Oorspronkelijk budget een getal in.</span><span class="sxs-lookup"><span data-stu-id="eaac5-125">In the Original budget field, enter a number.</span></span>
18. <span data-ttu-id="eaac5-126">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="eaac5-126">Click Save.</span></span>
19. <span data-ttu-id="eaac5-127">Klik op Workflow.</span><span class="sxs-lookup"><span data-stu-id="eaac5-127">Click Workflow.</span></span>
20. <span data-ttu-id="eaac5-128">Klik op Aanbieden.</span><span class="sxs-lookup"><span data-stu-id="eaac5-128">Click Submit.</span></span>
21. <span data-ttu-id="eaac5-129">Typ een waarde in het veld Opmerking.</span><span class="sxs-lookup"><span data-stu-id="eaac5-129">In the Comment field, type a value.</span></span>
22. <span data-ttu-id="eaac5-130">Klik op Aanbieden.</span><span class="sxs-lookup"><span data-stu-id="eaac5-130">Click Submit.</span></span>

