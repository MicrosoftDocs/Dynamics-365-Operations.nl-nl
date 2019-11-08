---
title: Toewijzingen verwerken
description: Dit artikel bevat informatie over toewijzingen, de opties voor verwerking hiervan in Microsoft Dynamics 365 Finance en de wijze waarop u deze kunt gebruiken in budgetplanningen. Toewijzingen worden gebruikt om bedragen over meerdere combinaties van grootboekrekeningen te verdelen. Hiermee kunt u ervoor zorgen dat uitgaven en opbrengsten in de boekhouding aan het juiste object worden doorberekend.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bf889169357ea0598a3fe24b09a6eb565209b9c0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186343"
---
# <a name="process-allocations"></a><span data-ttu-id="4f4dd-105">Toewijzingen verwerken</span><span class="sxs-lookup"><span data-stu-id="4f4dd-105">Process allocations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4f4dd-106">Dit artikel bevat informatie over toewijzingen, de opties voor verwerking hiervan en de wijze waarop u deze kunt gebruiken in budgetplanningen.</span><span class="sxs-lookup"><span data-stu-id="4f4dd-106">This article provides information about allocations, the options for processing them, and how they can be used in budget planning.</span></span> <span data-ttu-id="4f4dd-107">Toewijzingen worden gebruikt om bedragen over meerdere combinaties van grootboekrekeningen te verdelen.</span><span class="sxs-lookup"><span data-stu-id="4f4dd-107">Allocations are used to distribute amounts across multiple ledger account combinations.</span></span> <span data-ttu-id="4f4dd-108">Hiermee kunt u ervoor zorgen dat uitgaven en opbrengsten in de boekhouding aan het juiste object worden doorberekend.</span><span class="sxs-lookup"><span data-stu-id="4f4dd-108">They help ensure that expenses or revenues are charged to the correct object in accounting.</span></span>

<span data-ttu-id="4f4dd-109">De volgende mogelijkheden ondersteunen dit proces:</span><span class="sxs-lookup"><span data-stu-id="4f4dd-109">The following capabilities support this process:</span></span>

-   <span data-ttu-id="4f4dd-110">Handmatig toewijzen van transactiebedragen door de actie Splitsen in boekhoudingsverdelingen te gebruiken of door standaardsjablonen van financiële dimensies toe te passen op een document.</span><span class="sxs-lookup"><span data-stu-id="4f4dd-110">Manually allocate transaction amounts by using the Split action in accounting distributions, or by applying financial dimension default templates to a document.</span></span> <span data-ttu-id="4f4dd-111">Zie [Boekhoudingsverdelingen](../accounts-payable/accounting-distributions.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="4f4dd-111">For more information, see [Accounting distributions.](../accounts-payable/accounting-distributions.md)</span></span>
-   <span data-ttu-id="4f4dd-112">Automatisch toewijzen van transactiebedragen op basis van toewijzingstermijnen die zijn gedefinieerd in de afzonderlijke hoofdrekening.</span><span class="sxs-lookup"><span data-stu-id="4f4dd-112">Automatically allocate transactions amounts based on allocation terms defined on individual main account.</span></span> <span data-ttu-id="4f4dd-113">Toewijzingsjournaalregels worden gegenereerd voor elk journaal op basis van het percentage en de doelgrootboekrekening wanneer een journaalregel voldoet aan de criteria die als brongrootboekrekening zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="4f4dd-113">Allocation account entries will be generated for each journal based on the percentage and destination ledger account whenever an accounting entry meets the criteria defined as the source ledger account.</span></span>
-   <span data-ttu-id="4f4dd-114">Automatisch toewijzen van grootboeksaldi of vaste bedragen op basis van grootboektoewijzingsregels.</span><span class="sxs-lookup"><span data-stu-id="4f4dd-114">Automatically allocate ledger balances or fixed amounts based on ledger allocation rules.</span></span> <span data-ttu-id="4f4dd-115">De grootboektoewijzingsregels worden verwerkt op periodieke basis met toewijzingsjournalen.</span><span class="sxs-lookup"><span data-stu-id="4f4dd-115">The ledger allocation rules are processed on a periodic basis using allocation journals.</span></span> 

###  <a name="allocations-in-budget-planning"></a><span data-ttu-id="4f4dd-116">Toewijzingen in budgetplanning</span><span class="sxs-lookup"><span data-stu-id="4f4dd-116">Allocations in budget planning</span></span>

<span data-ttu-id="4f4dd-117">Grootboektoewijzingsregels kunnen worden gebruikt voor budgetplannen.</span><span class="sxs-lookup"><span data-stu-id="4f4dd-117">Ledger allocation rules can be used for budget plans.</span></span> <span data-ttu-id="4f4dd-118">Als u toewijzingsregels voor het grootboek gebruikt in budgetplanning, werken de toewijzingsregels op dezelfde manier als in het grootboek, alleen komen de bron- en doelgegevens uit het budgetplan.</span><span class="sxs-lookup"><span data-stu-id="4f4dd-118">When you use ledger allocation rules in budget planning, the allocation rules work the same way they would in the ledger, but the source data and destination data comes from the budget plan.</span></span> <span data-ttu-id="4f4dd-119">U kunt handmatig toewijzingsregels voor het grootboek selecteren voor budgetplanning.</span><span class="sxs-lookup"><span data-stu-id="4f4dd-119">You can manually select ledger allocation rules to use for budget plans.</span></span> <span data-ttu-id="4f4dd-120">U kunt ook een toewijzingsschema gebruiken dat als onderdeel van een werkstroomproces werkt.</span><span class="sxs-lookup"><span data-stu-id="4f4dd-120">Alternatively, you can use an allocation schedule that runs as part of a workflow process.</span></span>

> [!NOTE]
> <span data-ttu-id="4f4dd-121">U kunt geen intercompany-toewijzingsregels voor het grootboek gebruiken voor budgetplanning.</span><span class="sxs-lookup"><span data-stu-id="4f4dd-121">You can’t use intercompany ledger allocation rules for budget planning.</span></span>




