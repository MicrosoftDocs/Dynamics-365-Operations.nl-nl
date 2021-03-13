---
title: Een inkooporder maken voor een eenmalige leverancier
description: Deze procedure laat zien hoe u een inkooporder kunt maken voor een eenmalige leverancier.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c4885547cdf2f8496446761e27ce39e67e670f15
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016397"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="a0f03-103">Een inkooporder maken voor een eenmalige leverancier</span><span class="sxs-lookup"><span data-stu-id="a0f03-103">Create a purchase order for a one-time supplier</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a0f03-104">Deze procedure laat zien hoe u een inkooporder kunt maken voor een eenmalige leverancier.</span><span class="sxs-lookup"><span data-stu-id="a0f03-104">This procedure shows you how to create a purchase order for a one-time supplier.</span></span> <span data-ttu-id="a0f03-105">De leverancier wordt automatisch gemaakt met de inkooporder. De leveranciersrekening hoeft niet handmatig te worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="a0f03-105">The supplier is created automatically with the purchase order, rather than having to create the vendor account manually.</span></span> <span data-ttu-id="a0f03-106">Inkooporders worden meestal gemaakt door een inkoper.</span><span class="sxs-lookup"><span data-stu-id="a0f03-106">Purchase orders are typically created by a purchasing agent.</span></span> <span data-ttu-id="a0f03-107">Het voorbeeld dat in deze handleiding wordt weergegeven, kan worden gebruikt in het USMF-demobedrijf.</span><span class="sxs-lookup"><span data-stu-id="a0f03-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="a0f03-108">Het is een vereiste dat een rekening voor een eenmalige leverancier wordt ingesteld op de pagina Parameters van module Leveranciers.</span><span class="sxs-lookup"><span data-stu-id="a0f03-108">It is a prerequisite that a one-time vendor account has been set up in the Account payable parameters page.</span></span>


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="a0f03-109">Een inkooporder maken voor een eenmalige leverancier</span><span class="sxs-lookup"><span data-stu-id="a0f03-109">Create a purchase order for a one-time supplier</span></span>
1. <span data-ttu-id="a0f03-110">Ga naar Inkoop en sourcing > Inkooporders > Alle inkooporders.</span><span class="sxs-lookup"><span data-stu-id="a0f03-110">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="a0f03-111">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="a0f03-111">Click New.</span></span>
3. <span data-ttu-id="a0f03-112">Selecteer Ja in het veld Eenmalige leverancier.</span><span class="sxs-lookup"><span data-stu-id="a0f03-112">Select Yes in the One-time supplier field.</span></span>
    * <span data-ttu-id="a0f03-113">Er wordt automatisch een leveranciersrekening gemaakt en aan de inkooporder toegewezen.</span><span class="sxs-lookup"><span data-stu-id="a0f03-113">A vendor account is automatically created and assigned to the purchase order.</span></span> <span data-ttu-id="a0f03-114">De leveranciersrekening wordt gemaakt op basis van de sjabloon die is opgegeven op het tabblad Algemeen op de pagina Parameters van module Leveranciers.</span><span class="sxs-lookup"><span data-stu-id="a0f03-114">The vendor account is created based on the template that is specified on the General tab in the Accounts payable parameters page.</span></span>  
4. <span data-ttu-id="a0f03-115">Typ in het veld Naam een naam voor de leverancier.</span><span class="sxs-lookup"><span data-stu-id="a0f03-115">In the Name field, type a name for the supplier.</span></span>
5. <span data-ttu-id="a0f03-116">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a0f03-116">Click OK.</span></span>
    * <span data-ttu-id="a0f03-117">De inkooporder kan nu worden voltooid en verwerkt als elke andere order.</span><span class="sxs-lookup"><span data-stu-id="a0f03-117">The purchase order can now be completed and processed like any other order.</span></span> <span data-ttu-id="a0f03-118">Er zijn geen speciale kenmerken verbonden aan hoe dit gebeurt.</span><span class="sxs-lookup"><span data-stu-id="a0f03-118">There are no special characteristics related to how this is done.</span></span> <span data-ttu-id="a0f03-119">Op de factuur wordt een transactie voor de leveranciersrekening aangegeven die met de order is gemaakt, waarna de betaling wordt verwerkt.</span><span class="sxs-lookup"><span data-stu-id="a0f03-119">The invoice will account a due transaction on the vendor account that was created with the order, and payment will then be processed.</span></span>

