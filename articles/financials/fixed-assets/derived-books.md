---
title: Afgeleide boeken
description: In dit artikel vindt u een overzicht van de functionaliteit van het afgeleide boek.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 153b6437205d5a849fa6a90c0d3b9f3d51dd6768
ms.contentlocale: nl-nl
ms.lasthandoff: 08/07/2018

---

# <a name="derived-books"></a><span data-ttu-id="705d8-103">Afgeleide boeken</span><span class="sxs-lookup"><span data-stu-id="705d8-103">Derived books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="705d8-104">In dit artikel vindt u een overzicht van de functionaliteit van het afgeleide boek.</span><span class="sxs-lookup"><span data-stu-id="705d8-104">This article provides an overview of derived book functionality.</span></span>

<span data-ttu-id="705d8-105">Het doel van afgeleide boeken is de vereenvoudiging van het boeken van transacties in het vaste-activaboek die op gezette tijden zijn gepland.</span><span class="sxs-lookup"><span data-stu-id="705d8-105">The purpose of derived books is to simplify the posting of fixed asset book transactions that are planned for regular intervals.</span></span>  <span data-ttu-id="705d8-106">U kiest één boek als het primaire boek.</span><span class="sxs-lookup"><span data-stu-id="705d8-106">You choose one book as the primary book.</span></span> <span data-ttu-id="705d8-107">Dit is gewoonlijk het boek dat wordt gebruikt voor boekhoudkundige afschrijving.</span><span class="sxs-lookup"><span data-stu-id="705d8-107">This usually is the book that is used for accounting depreciation.</span></span> <span data-ttu-id="705d8-108">Vervolgens koppelt u dit aan andere boeken die zijn ingesteld om transacties te boeken in dezelfde intervallen als het primaire boek.</span><span class="sxs-lookup"><span data-stu-id="705d8-108">You then attach to it other books that are set up to post transactions in the same intervals as the primary book.</span></span> <span data-ttu-id="705d8-109">Belastingafschrijvingsboeken zijn vaak ingesteld als afgeleide boeken.</span><span class="sxs-lookup"><span data-stu-id="705d8-109">Tax depreciation books are often set up as derived books.</span></span> 

<span data-ttu-id="705d8-110">De meest algemene transacties die u kunt instellen op het boeken naar afgeleide boeken zijn verwervingen, bijboekingscorrrecties en afboekingen.</span><span class="sxs-lookup"><span data-stu-id="705d8-110">The most common transactions to set up to post to derived books are acquisitions, acquisition adjustments, and disposals.</span></span> 

## <a name="example"></a><span data-ttu-id="705d8-111">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="705d8-111">Example</span></span>

<span data-ttu-id="705d8-112">Boek B en boek C zijn ingesteld als afgeleide boeken voor boek A voor het transactietype verwerving.</span><span class="sxs-lookup"><span data-stu-id="705d8-112">Book B and book C are set up as derived books for book A for the Acquisition transaction type.</span></span> <span data-ttu-id="705d8-113">In boek A voert u een verwervingstransactie in voor activum 123 voor 1.500,00.</span><span class="sxs-lookup"><span data-stu-id="705d8-113">In book A, you enter an acquisition transaction for asset 123 for 1,500.00.</span></span> 

<span data-ttu-id="705d8-114">Als de transactie geboekt is, wordt een verwervingstransactie gegenereerd en geboekt in activum 123 voor boek B en in activum 123 voor boek C voor 1.500,00.</span><span class="sxs-lookup"><span data-stu-id="705d8-114">When the transaction is posted, an acquisition transaction is generated and posted in asset 123 for book B and in asset 123 for book C for 1,500.00.</span></span> <span data-ttu-id="705d8-115">Wanneer u de transacties van het primaire boek voorbereidt voor het boeken in het vaste-activajournaal, kunt u ook de transacties van de afgeleide boeken weergeven en wijzigen.</span><span class="sxs-lookup"><span data-stu-id="705d8-115">When you prepare the transactions of the primary book for posting in the fixed asset journal, you can also view and modify the transactions of the derived books.</span></span> <span data-ttu-id="705d8-116">Als u de transacties van het primaire boek voorbereidt voor het boeken in een ander journaal, worden de transacties van de afgeleide waarde niet weergegeven.</span><span class="sxs-lookup"><span data-stu-id="705d8-116">If you prepare the primary book transactions in another journal, the transactions of the derived value are not displayed.</span></span> <span data-ttu-id="705d8-117">Deze worden echter geboekt naar de juiste rekeningen en boekingslagen wanneer u de transacties van het primaire boek boekt.</span><span class="sxs-lookup"><span data-stu-id="705d8-117">However, they are posted to the appropriate accounts and posting layers when you post the primary book transactions.</span></span>

> [!NOTE]                                                                                                                               
> <span data-ttu-id="705d8-118">Boeken die zijn ingesteld op het boeken van transacties op andere tijden dan de tijden van het primaire boek moeten als afzonderlijke boeken aan de vaste activa worden gekoppeld en niet als afgeleide boeken.</span><span class="sxs-lookup"><span data-stu-id="705d8-118">Books that are set up to post transactions at intervals other than the primary book intervals must be attached to the fixed asset as separate books and not as derived books.</span></span>  

<span data-ttu-id="705d8-119">Zie voor meer informatie [Boeken met afgeleide boeken](post-derived-value-models.md).</span><span class="sxs-lookup"><span data-stu-id="705d8-119">For more information, see [Posting with derived books](post-derived-value-models.md).</span></span>




