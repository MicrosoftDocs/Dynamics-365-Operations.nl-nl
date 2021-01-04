---
title: Groepen met consolidatierekeningen en aanvullende consolidatierekeningen
description: In dit onderwerp wordt informatie gegeven over groepen met consolidatierekeningen en aanvullende consolidatierekeningen en wordt uitgelegd hoe deze worden gebruikt in Microsoft Dynamics 365 Finance.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerConsolidateAccountGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 8db7a60656434aafd8114b08c2c0e9493140f27b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442085"
---
# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a><span data-ttu-id="45784-103">Groepen met consolidatierekeningen en aanvullende consolidatierekeningen</span><span class="sxs-lookup"><span data-stu-id="45784-103">Consolidation account groups and additional consolidation accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="45784-104">In dit onderwerp wordt informatie gegeven over groepen met consolidatierekeningen en aanvullende consolidatierekeningen en wordt uitgelegd hoe deze worden gebruikt in Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="45784-104">This topic provides information about consolidation account groups and additional consolidation accounts, and explains how they are used in Microsoft Dynamics 365 Finance.</span></span>

<a name="consolidation-account-groups"></a><span data-ttu-id="45784-105">Groepen met consolidatierekeningen</span><span class="sxs-lookup"><span data-stu-id="45784-105">Consolidation account groups</span></span>
----------------------------

<span data-ttu-id="45784-106">Met groepen consolidatierekeningen kunt u groepen maken van de rekeningen die u wilt gebruiken om gegevens te consolideren.</span><span class="sxs-lookup"><span data-stu-id="45784-106">Consolidation account groups let you create groups of the accounts that you want to use to consolidate data.</span></span> <span data-ttu-id="45784-107">Meestal wordt met een groep consolidatierekeningen een door de overheid voorgeschreven rekeningschema vertegenwoordigd of worden rekeningen aan een groep toegewezen die door het hoofdkantoor van het bedrijf is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="45784-107">Most often, a consolidation account group represents a government-mandated chart of accounts or maps accounts to a group that is defined by the company's headquarters.</span></span> <span data-ttu-id="45784-108">U vindt groepen consolidatierekeningen in het gebied **Instellen** van de module **Consolidaties**.</span><span class="sxs-lookup"><span data-stu-id="45784-108">You can find consolidation account groups in the **Setup** area of the **Consolidations** module.</span></span> <span data-ttu-id="45784-109">Wanneer u een nieuwe groep toevoegt, voert u een unieke ID en een naam in voor de rekeninggroep.</span><span class="sxs-lookup"><span data-stu-id="45784-109">When you add a new group, you enter a unique identifier for the account group and a name.</span></span>

## <a name="additional-consolidation-accounts"></a><span data-ttu-id="45784-110">Aanvullende consolidatiebedragen</span><span class="sxs-lookup"><span data-stu-id="45784-110">Additional consolidation accounts</span></span>
<span data-ttu-id="45784-111">Met aanvullende consolidatierekeningen kunt u een rekening vanuit een bestaand rekeningschema toewijzen aan een groep consolidatierekeningen.</span><span class="sxs-lookup"><span data-stu-id="45784-111">Additional consolidation accounts let you assign an account from an existing chart of accounts to a consolidation account group.</span></span> <span data-ttu-id="45784-112">U kunt vervolgens een waarde en naam voor de consolidatierekening opgeven.</span><span class="sxs-lookup"><span data-stu-id="45784-112">You can then specify a consolidation account value and name.</span></span> 

<span data-ttu-id="45784-113">U vindt aanvullende consolidatierekeningen in het gebied **Instellen** van de module **Consolidaties**.</span><span class="sxs-lookup"><span data-stu-id="45784-113">You can find additional consolidation accounts in the **Setup** area of the **Consolidations** module.</span></span> <span data-ttu-id="45784-114">Wanneer u een nieuwe consolidatierekening maakt, moet u de volgende gegevens opgeven:</span><span class="sxs-lookup"><span data-stu-id="45784-114">When you create a new consolidation account, you must specify the following information:</span></span>

-   <span data-ttu-id="45784-115">**Hoofdrekening** : dit veld is een zoekveld waarin de belangrijkste rekeningen worden weergegeven die zijn gebaseerd op het rekeningschema dat u hebt geselecteerd op de pagina.</span><span class="sxs-lookup"><span data-stu-id="45784-115">**Main account** – This field is a lookup that shows all the main accounts that are based on the chart of accounts that you selected on the page.</span></span> <span data-ttu-id="45784-116">Wanneer u een rekening selecteert, wordt de naam automatisch ingevoerd in het veld **Naam hoofdrekening**.</span><span class="sxs-lookup"><span data-stu-id="45784-116">When you select an account, the name is automatically entered in the **Main account name** field.</span></span>
-   <span data-ttu-id="45784-117">**Groep met consolidatierekeningen** : met dit veld kunt u de groep opgeven waaraan u de rekening wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="45784-117">**Consolidation account group** – Use this field to specify the group to assign the account to.</span></span> <span data-ttu-id="45784-118">Als u op twee verschillende manieren consolideert, moet u dezelfde rekening toevoegen aan alle vier de groepen consolidatierekeningen.</span><span class="sxs-lookup"><span data-stu-id="45784-118">If you consolidate in two different ways, you must add the same account to all four consolidation account groups.</span></span>
-   <span data-ttu-id="45784-119">**Consolidatierekening**: voer de waarde van de consolidatierekening in.</span><span class="sxs-lookup"><span data-stu-id="45784-119">**Consolidation account** – Enter the value of the consolidation account.</span></span> <span data-ttu-id="45784-120">Deze waarde hoeft geen rekening van een rekeningschema te zijn.</span><span class="sxs-lookup"><span data-stu-id="45784-120">This value doesn't have to be an account from a chart of accounts.</span></span> <span data-ttu-id="45784-121">Het kan een waarde zijn die u nodig hebt.</span><span class="sxs-lookup"><span data-stu-id="45784-121">It can be any value that you require.</span></span>
-   <span data-ttu-id="45784-122">**Naam van consolidatierekening**: voer de naam van de rekening in als u wilt dat deze in query´s en rapporten verschijnt.</span><span class="sxs-lookup"><span data-stu-id="45784-122">**Consolidation account name** – Enter the name of account as you want it to appear on inquiries and reports.</span></span>
-   <span data-ttu-id="45784-123">**SAT-niveau**: dit veld wordt gebruikt voor aangifte van rekeningoverzichten bij de Mexicaanse belastingdienst.</span><span class="sxs-lookup"><span data-stu-id="45784-123">**SAT level** – This field is used to report account statements to the Mexican tax authorities.</span></span> 

<span data-ttu-id="45784-124">Wanneer u de groepen consolidatierekeningen en aanvullende consolidatierekeningen hebt gemaakt, kunt u de groep selecteren in het online proces Consolideren.</span><span class="sxs-lookup"><span data-stu-id="45784-124">When you've finished creating your consolidation account groups and additional consolidation accounts, you can select the group in the Consolidate online process.</span></span>


<span data-ttu-id="45784-125">Zie [Consolidatiegroepen en extra consolidatierekeningen maken](../general-ledger/tasks/create-consolidation-groups.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="45784-125">For more information, see [Create consolidation groups and additional consolidation accounts](../general-ledger/tasks/create-consolidation-groups.md).</span></span> 



