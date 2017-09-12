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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2d4dabaf6e1d79cbd626294ee4e327f2725a5e43
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="870b0-103">Een inkooporder maken voor een eenmalige leverancier</span><span class="sxs-lookup"><span data-stu-id="870b0-103">Create a purchase order for a one-time supplier</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="870b0-104">Deze procedure laat zien hoe u een inkooporder kunt maken voor een eenmalige leverancier.</span><span class="sxs-lookup"><span data-stu-id="870b0-104">This procedure shows you how to create a purchase order for a one-time supplier.</span></span> <span data-ttu-id="870b0-105">De leverancier wordt automatisch gemaakt met de inkooporder. De leveranciersrekening hoeft niet handmatig te worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="870b0-105">The supplier is created automatically with the purchase order, rather than having to create the vendor account manually.</span></span> <span data-ttu-id="870b0-106">Inkooporders worden meestal gemaakt door een inkoper.</span><span class="sxs-lookup"><span data-stu-id="870b0-106">Purchase orders are typically created by a purchasing agent.</span></span> <span data-ttu-id="870b0-107">Het voorbeeld dat in deze handleiding wordt weergegeven, kan worden gebruikt in het USMF-demobedrijf.</span><span class="sxs-lookup"><span data-stu-id="870b0-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="870b0-108">Het is een vereiste dat een rekening voor een eenmalige leverancier wordt ingesteld op de pagina Parameters van module Leveranciers.</span><span class="sxs-lookup"><span data-stu-id="870b0-108">It is a prerequisite that a one-time vendor account has been set up in the Account payable parameters page.</span></span>


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="870b0-109">Een inkooporder maken voor een eenmalige leverancier</span><span class="sxs-lookup"><span data-stu-id="870b0-109">Create a purchase order for a one-time supplier</span></span>
1. <span data-ttu-id="870b0-110">Ga naar Inkoop en sourcing > Inkooporders > Alle inkooporders.</span><span class="sxs-lookup"><span data-stu-id="870b0-110">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="870b0-111">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="870b0-111">Click New.</span></span>
3. <span data-ttu-id="870b0-112">Selecteer Ja in het veld Eenmalige leverancier.</span><span class="sxs-lookup"><span data-stu-id="870b0-112">Select Yes in the One-time supplier field.</span></span>
    * <span data-ttu-id="870b0-113">Er wordt automatisch een leveranciersrekening gemaakt en aan de inkooporder toegewezen.</span><span class="sxs-lookup"><span data-stu-id="870b0-113">A vendor account is automatically created and assigned to the purchase order.</span></span> <span data-ttu-id="870b0-114">De leveranciersrekening wordt gemaakt op basis van de sjabloon die is opgegeven op het tabblad Algemeen op de pagina Parameters van module Leveranciers.</span><span class="sxs-lookup"><span data-stu-id="870b0-114">The vendor account is created based on the template that is specified on the General tab in the Accounts payable parameters page.</span></span>  
4. <span data-ttu-id="870b0-115">Typ in het veld Naam een naam voor de leverancier.</span><span class="sxs-lookup"><span data-stu-id="870b0-115">In the Name field, type a name for the supplier.</span></span>
5. <span data-ttu-id="870b0-116">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="870b0-116">Click OK.</span></span>
    * <span data-ttu-id="870b0-117">De inkooporder kan nu worden voltooid en verwerkt als elke andere order.</span><span class="sxs-lookup"><span data-stu-id="870b0-117">The purchase order can now be completed and processed like any other order.</span></span> <span data-ttu-id="870b0-118">Er zijn geen speciale kenmerken verbonden aan hoe dit gebeurt.</span><span class="sxs-lookup"><span data-stu-id="870b0-118">There are no special characteristics related to how this is done.</span></span> <span data-ttu-id="870b0-119">Op de factuur wordt een transactie voor de leveranciersrekening aangegeven die met de order is gemaakt, waarna de betaling wordt verwerkt.</span><span class="sxs-lookup"><span data-stu-id="870b0-119">The invoice will account a due transaction on the vendor account that was created with the order, and payment will then be processed.</span></span> <span data-ttu-id="870b0-120">Wanneer dit is voltooid, kan de leveranciersrekening worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="870b0-120">When this is completed, the vendor account can be deleted.</span></span> <span data-ttu-id="870b0-121">Dit wordt meestal uitgevoerd door de leveranciersafdeling.</span><span class="sxs-lookup"><span data-stu-id="870b0-121">This is typically done by the accounts payable department.</span></span>  


