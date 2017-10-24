---
title: Afgeleide boeken
description: In dit artikel vindt u een overzicht van de functionaliteit van het afgeleide boek.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5afdabf93128bc52cb223d0c35c6bcdae5f5ca2a
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="derived-books"></a><span data-ttu-id="5f5fe-103">Afgeleide boeken</span><span class="sxs-lookup"><span data-stu-id="5f5fe-103">Derived books</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5f5fe-104">In dit artikel vindt u een overzicht van de functionaliteit van het afgeleide boek.</span><span class="sxs-lookup"><span data-stu-id="5f5fe-104">This article provides an overview of derived book functionality.</span></span>

<span data-ttu-id="5f5fe-105">Het doel van afgeleide boeken is de vereenvoudiging van het boeken van transacties in het vaste-activaboek die op gezette tijden zijn gepland.</span><span class="sxs-lookup"><span data-stu-id="5f5fe-105">The purpose of derived books is to simplify the posting of fixed asset book transactions that are planned for regular intervals.</span></span>  <span data-ttu-id="5f5fe-106">U kiest één boek als het primaire boek.</span><span class="sxs-lookup"><span data-stu-id="5f5fe-106">You choose one book as the primary book.</span></span> <span data-ttu-id="5f5fe-107">Dit is gewoonlijk het boek dat wordt gebruikt voor boekhoudkundige afschrijving.</span><span class="sxs-lookup"><span data-stu-id="5f5fe-107">This usually is the book that is used for accounting depreciation.</span></span> <span data-ttu-id="5f5fe-108">Vervolgens koppelt u dit aan andere boeken die zijn ingesteld om transacties te boeken in dezelfde intervallen als het primaire boek.</span><span class="sxs-lookup"><span data-stu-id="5f5fe-108">You then attach to it other books that are set up to post transactions in the same intervals as the primary book.</span></span> <span data-ttu-id="5f5fe-109">Belastingafschrijvingsboeken zijn vaak ingesteld als afgeleide boeken.</span><span class="sxs-lookup"><span data-stu-id="5f5fe-109">Tax depreciation books are often set up as derived books.</span></span> 

<span data-ttu-id="5f5fe-110">De meest algemene transacties die u kunt instellen op het boeken naar afgeleide boeken zijn verwervingen, bijboekingscorrrecties en afboekingen.</span><span class="sxs-lookup"><span data-stu-id="5f5fe-110">The most common transactions to set up to post to derived books are acquisitions, acquisition adjustments, and disposals.</span></span> 

## <a name="example"></a><span data-ttu-id="5f5fe-111">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="5f5fe-111">Example</span></span>

<span data-ttu-id="5f5fe-112">Boek B en boek C zijn ingesteld als afgeleide boeken voor boek A voor het transactietype verwerving.</span><span class="sxs-lookup"><span data-stu-id="5f5fe-112">Book B and book C are set up as derived books for book A for the Acquisition transaction type.</span></span> <span data-ttu-id="5f5fe-113">In boek A voert u een verwervingstransactie in voor activum 123 voor 1.500,00.</span><span class="sxs-lookup"><span data-stu-id="5f5fe-113">In book A, you enter an acquisition transaction for asset 123 for 1,500.00.</span></span> 

<span data-ttu-id="5f5fe-114">Als de transactie geboekt is, wordt een verwervingstransactie gegenereerd en geboekt in activum 123 voor boek B en in activum 123 voor boek C voor 1.500,00.</span><span class="sxs-lookup"><span data-stu-id="5f5fe-114">When the transaction is posted, an acquisition transaction is generated and posted in asset 123 for book B and in asset 123 for book C for 1,500.00.</span></span> <span data-ttu-id="5f5fe-115">Wanneer u de transacties van het primaire boek voorbereidt voor het boeken in het vaste-activajournaal, kunt u ook de transacties van de afgeleide boeken weergeven en wijzigen.</span><span class="sxs-lookup"><span data-stu-id="5f5fe-115">When you prepare the transactions of the primary book for posting in the fixed asset journal, you can also view and modify the transactions of the derived books.</span></span> <span data-ttu-id="5f5fe-116">Als u de transacties van het primaire boek voorbereidt voor het boeken in een ander journaal, worden de transacties van de afgeleide waarde niet weergegeven.</span><span class="sxs-lookup"><span data-stu-id="5f5fe-116">If you prepare the primary book transactions in another journal, the transactions of the derived value are not displayed.</span></span> <span data-ttu-id="5f5fe-117">Deze worden echter geboekt naar de juiste rekeningen en boekingslagen wanneer u de transacties van het primaire boek boekt.</span><span class="sxs-lookup"><span data-stu-id="5f5fe-117">However, they are posted to the appropriate accounts and posting layers when you post the primary book transactions.</span></span>

> [!NOTE]                                                                                                                               
> <span data-ttu-id="5f5fe-118">Boeken die zijn ingesteld op het boeken van transacties op andere tijden dan de tijden van het primaire boek moeten als afzonderlijke boeken aan de vaste activa worden gekoppeld en niet als afgeleide boeken.</span><span class="sxs-lookup"><span data-stu-id="5f5fe-118">Books that are set up to post transactions at intervals other than the primary book intervals must be attached to the fixed asset as separate books and not as derived books.</span></span>  

<span data-ttu-id="5f5fe-119">Zie voor meer informatie [Boeken met afgeleide boeken](post-derived-value-models.md).</span><span class="sxs-lookup"><span data-stu-id="5f5fe-119">For more information, see [Posting with derived books](post-derived-value-models.md).</span></span>




