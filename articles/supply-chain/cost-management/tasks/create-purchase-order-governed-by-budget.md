---
title: Een inkooporder maken die wordt geregeld door een budget
description: Via deze procedure kunt u een inkooporder maken die is gecontroleerd op beschikbaar budget.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e82e40d67547f5932a4805f2580e8c9f58def284
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "366530"
---
# <a name="create-a-purchase-order-governed-by-budget"></a><span data-ttu-id="6ddf6-103">Een inkooporder maken die wordt geregeld door een budget</span><span class="sxs-lookup"><span data-stu-id="6ddf6-103">Create a purchase order governed by budget</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6ddf6-104">Via deze procedure kunt u een inkooporder maken die is gecontroleerd op beschikbaar budget.</span><span class="sxs-lookup"><span data-stu-id="6ddf6-104">Use this procedure to create a purchase order that is checked for available budget.</span></span> <span data-ttu-id="6ddf6-105">Deze registratie gebruikt het USMF-demogegevensbedrijf.</span><span class="sxs-lookup"><span data-stu-id="6ddf6-105">This recording uses the USMF demo data company.</span></span>


## <a name="review-the-budget-control-configuration"></a><span data-ttu-id="6ddf6-106">De budgetbeheerconfiguratie controleren</span><span class="sxs-lookup"><span data-stu-id="6ddf6-106">Review the budget control configuration</span></span>
1. <span data-ttu-id="6ddf6-107">Ga naar Budgettering > Instelling > Budgetbeheer > Configuratie budgetbeheer.</span><span class="sxs-lookup"><span data-stu-id="6ddf6-107">Go to Budgeting > Setup > Budget control > Budget control configuration.</span></span>
2. <span data-ttu-id="6ddf6-108">Klik op het tabblad Beschikbare budgetfondsen.</span><span class="sxs-lookup"><span data-stu-id="6ddf6-108">Click the Budget funds available tab.</span></span>
3. <span data-ttu-id="6ddf6-109">Klik op het tabblad Documenten en journalen.</span><span class="sxs-lookup"><span data-stu-id="6ddf6-109">Click the Documents and journals tab.</span></span>
4. <span data-ttu-id="6ddf6-110">Klik op het tabblad Regels voor budgetbeheer definiëren.</span><span class="sxs-lookup"><span data-stu-id="6ddf6-110">Click the Define budget control rules tab.</span></span>
5. <span data-ttu-id="6ddf6-111">Klik op het tabblad Budgetgroepen definiëren.</span><span class="sxs-lookup"><span data-stu-id="6ddf6-111">Click the Define budget groups tab.</span></span>
6. <span data-ttu-id="6ddf6-112">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6ddf6-112">Close the page.</span></span>

## <a name="create-the-purchase-order-header"></a><span data-ttu-id="6ddf6-113">De koptekst van de inkooporder maken</span><span class="sxs-lookup"><span data-stu-id="6ddf6-113">Create the purchase order header</span></span>
1. <span data-ttu-id="6ddf6-114">Ga naar Inkoop en sourcing > Inkooporders > Alle inkooporders.</span><span class="sxs-lookup"><span data-stu-id="6ddf6-114">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="6ddf6-115">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="6ddf6-115">Click New.</span></span>
3. <span data-ttu-id="6ddf6-116">Typ of selecteer een waarde in het veld Leveranciersrekening.</span><span class="sxs-lookup"><span data-stu-id="6ddf6-116">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="6ddf6-117">Vouw de sectie Algemeen uit.</span><span class="sxs-lookup"><span data-stu-id="6ddf6-117">Expand the General section.</span></span>
5. <span data-ttu-id="6ddf6-118">Stel in het veld Boekingsdatum de datum in op '2016-01-01'.</span><span class="sxs-lookup"><span data-stu-id="6ddf6-118">In the Accounting date field, set the date to '2016-01-01'.</span></span>
6. <span data-ttu-id="6ddf6-119">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="6ddf6-119">Click OK.</span></span>

## <a name="add-a-purchase-order-line"></a><span data-ttu-id="6ddf6-120">Een inkooporderregel toevoegen</span><span class="sxs-lookup"><span data-stu-id="6ddf6-120">Add a purchase order line</span></span>
1. <span data-ttu-id="6ddf6-121">Typ of selecteer een waarde in het veld Aanschaffingscategorie.</span><span class="sxs-lookup"><span data-stu-id="6ddf6-121">In the Procurement category field, enter or select a value.</span></span>
2. <span data-ttu-id="6ddf6-122">Stel Hoeveelheid in op '2'.</span><span class="sxs-lookup"><span data-stu-id="6ddf6-122">Set Quantity to '2'.</span></span>
3. <span data-ttu-id="6ddf6-123">Typ of selecteer een waarde in het veld Eenheid.</span><span class="sxs-lookup"><span data-stu-id="6ddf6-123">In the Unit field, enter or select a value.</span></span>
4. <span data-ttu-id="6ddf6-124">Stel Eenheidsprijs in op '10000'.</span><span class="sxs-lookup"><span data-stu-id="6ddf6-124">Set Unit price to '10000'.</span></span>
5. <span data-ttu-id="6ddf6-125">Klik op Financiële items.</span><span class="sxs-lookup"><span data-stu-id="6ddf6-125">Click Financials.</span></span>
6. <span data-ttu-id="6ddf6-126">Klik op Bedragen verdelen.</span><span class="sxs-lookup"><span data-stu-id="6ddf6-126">Click Distribute amounts.</span></span>
7. <span data-ttu-id="6ddf6-127">Geef in het veld Grootboekrekening de waarde '601300-001-023--' op.</span><span class="sxs-lookup"><span data-stu-id="6ddf6-127">In the Ledger account field, specify the value '601300-001-023--'.</span></span>
8. <span data-ttu-id="6ddf6-128">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6ddf6-128">Close the page.</span></span>

## <a name="perform-budget-checking"></a><span data-ttu-id="6ddf6-129">Budgetcontrole uitvoeren</span><span class="sxs-lookup"><span data-stu-id="6ddf6-129">Perform budget checking</span></span>
1. <span data-ttu-id="6ddf6-130">Klik op Financiële items.</span><span class="sxs-lookup"><span data-stu-id="6ddf6-130">Click Financials.</span></span>
2. <span data-ttu-id="6ddf6-131">Klik op Budgetcontrole uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="6ddf6-131">Click Perform budget checking.</span></span>
3. <span data-ttu-id="6ddf6-132">Klik op Financiële items.</span><span class="sxs-lookup"><span data-stu-id="6ddf6-132">Click Financials.</span></span>
4. <span data-ttu-id="6ddf6-133">Klik op Fouten of waarschuwingen van budgetcontrole.</span><span class="sxs-lookup"><span data-stu-id="6ddf6-133">Click Budget check errors or warnings.</span></span>
5. <span data-ttu-id="6ddf6-134">Klik op Sluiten.</span><span class="sxs-lookup"><span data-stu-id="6ddf6-134">Click Close.</span></span>

