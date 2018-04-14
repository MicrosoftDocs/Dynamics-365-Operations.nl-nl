--- 
title: Een inkooporder maken voor een eenmalige leverancier
description: Deze procedure laat zien hoe u een inkooporder kunt maken voor een eenmalige leverancier.
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e068105bcd5983220c43613569f80700922360e5
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="c49db-103">Een inkooporder maken voor een eenmalige leverancier</span><span class="sxs-lookup"><span data-stu-id="c49db-103">Create a purchase order for a one-time supplier</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c49db-104">Deze procedure laat zien hoe u een inkooporder kunt maken voor een eenmalige leverancier.</span><span class="sxs-lookup"><span data-stu-id="c49db-104">This procedure shows you how to create a purchase order for a one-time supplier.</span></span> <span data-ttu-id="c49db-105">De leverancier wordt automatisch gemaakt met de inkooporder. De leveranciersrekening hoeft niet handmatig te worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c49db-105">The supplier is created automatically with the purchase order, rather than having to create the vendor account manually.</span></span> <span data-ttu-id="c49db-106">Inkooporders worden meestal gemaakt door een inkoper.</span><span class="sxs-lookup"><span data-stu-id="c49db-106">Purchase orders are typically created by a purchasing agent.</span></span> <span data-ttu-id="c49db-107">Het voorbeeld dat in deze handleiding wordt weergegeven, kan worden gebruikt in het USMF-demobedrijf.</span><span class="sxs-lookup"><span data-stu-id="c49db-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="c49db-108">Het is een vereiste dat een rekening voor een eenmalige leverancier wordt ingesteld op de pagina Parameters van module Leveranciers.</span><span class="sxs-lookup"><span data-stu-id="c49db-108">It is a prerequisite that a one-time vendor account has been set up in the Account payable parameters page.</span></span>


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="c49db-109">Een inkooporder maken voor een eenmalige leverancier</span><span class="sxs-lookup"><span data-stu-id="c49db-109">Create a purchase order for a one-time supplier</span></span>
1. <span data-ttu-id="c49db-110">Ga naar Inkoop en sourcing > Inkooporders > Alle inkooporders.</span><span class="sxs-lookup"><span data-stu-id="c49db-110">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="c49db-111">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="c49db-111">Click New.</span></span>
3. <span data-ttu-id="c49db-112">Selecteer Ja in het veld Eenmalige leverancier.</span><span class="sxs-lookup"><span data-stu-id="c49db-112">Select Yes in the One-time supplier field.</span></span>
    * <span data-ttu-id="c49db-113">Er wordt automatisch een leveranciersrekening gemaakt en aan de inkooporder toegewezen.</span><span class="sxs-lookup"><span data-stu-id="c49db-113">A vendor account is automatically created and assigned to the purchase order.</span></span> <span data-ttu-id="c49db-114">De leveranciersrekening wordt gemaakt op basis van de sjabloon die is opgegeven op het tabblad Algemeen op de pagina Parameters van module Leveranciers.</span><span class="sxs-lookup"><span data-stu-id="c49db-114">The vendor account is created based on the template that is specified on the General tab in the Accounts payable parameters page.</span></span>  
4. <span data-ttu-id="c49db-115">Typ in het veld Naam een naam voor de leverancier.</span><span class="sxs-lookup"><span data-stu-id="c49db-115">In the Name field, type a name for the supplier.</span></span>
5. <span data-ttu-id="c49db-116">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c49db-116">Click OK.</span></span>
    * <span data-ttu-id="c49db-117">De inkooporder kan nu worden voltooid en verwerkt als elke andere order.</span><span class="sxs-lookup"><span data-stu-id="c49db-117">The purchase order can now be completed and processed like any other order.</span></span> <span data-ttu-id="c49db-118">Er zijn geen speciale kenmerken verbonden aan hoe dit gebeurt.</span><span class="sxs-lookup"><span data-stu-id="c49db-118">There are no special characteristics related to how this is done.</span></span> <span data-ttu-id="c49db-119">Op de factuur wordt een transactie voor de leveranciersrekening aangegeven die met de order is gemaakt, waarna de betaling wordt verwerkt.</span><span class="sxs-lookup"><span data-stu-id="c49db-119">The invoice will account a due transaction on the vendor account that was created with the order, and payment will then be processed.</span></span> <span data-ttu-id="c49db-120">Wanneer dit is voltooid, kan de leveranciersrekening worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="c49db-120">When this is completed, the vendor account can be deleted.</span></span> <span data-ttu-id="c49db-121">Dit wordt meestal uitgevoerd door de leveranciersafdeling.</span><span class="sxs-lookup"><span data-stu-id="c49db-121">This is typically done by the accounts payable department.</span></span>  


