---
title: Vaste-activatransacties boeken naar boekingslagen
description: Dit artikel geeft een overzicht van boekingslaagfunctionaliteit voor vaste-activatransacties.
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b210bddf640dff2d65e2aec63a18c27acebdc5a8
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="post-fixed-asset-transactions-to-posting-layers"></a><span data-ttu-id="b5dd0-103">Vaste-activatransacties boeken naar boekingslagen</span><span class="sxs-lookup"><span data-stu-id="b5dd0-103">Post fixed asset transactions to posting layers</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b5dd0-104">Dit artikel geeft een overzicht van boekingslaagfunctionaliteit voor vaste-activatransacties.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-104">This article gives an overview of posting layer functionality for fixed asset transactions.</span></span>

<span data-ttu-id="b5dd0-105">Vaste activa worden vaak op verschillende manieren en om verschillende redenen afgeschreven.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-105">A fixed asset is often depreciated in different ways for different purposes.</span></span> <span data-ttu-id="b5dd0-106">De afschrijving voor de belasting wordt berekend conform de huidige belastingregels om de hoogst mogelijke afschrijving voor de belasting te kunnen krijgen, maar het afschrijven voor rapportagedoeleinden wordt berekend conform de regels en standaarden van de boekhouding.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-106">Depreciation for tax purposes is calculated by using current tax rules to achieve the highest possible depreciation before taxes, but depreciation for reporting purposes is calculated according to accounting laws and standards.</span></span> <span data-ttu-id="b5dd0-107">De diverse soorten afschrijvingen worden afzonderlijk in de boekingslagen berekend en geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-107">The various kinds of depreciation are calculated and recorded separately in the posting layers.</span></span>

<span data-ttu-id="b5dd0-108">Elk boek dat is gekoppeld aan vaste activa, is ingesteld voor een bepaalde boekingslaag met een algemeen afschrijvingsdoel.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-108">Each book that is attached to a fixed asset is set up for a particular posting layer that has an overall depreciation objective.</span></span> <span data-ttu-id="b5dd0-109">Er zijn tien boekingslagen: Huidig, Bewerkingen, Btw en zeven douanelagen.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-109">There are ten posting layers: Current, Operations, Tax, and seven Custom layers.</span></span> <span data-ttu-id="b5dd0-110">U kunt het boeken naar het algemene grootboek voor het boek ook uitschakelen door het veld Boeken naar grootboek in te stellen op Nee.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-110">You can also disable posting to the general ledger for the book by setting the Post to general ledger field to No.</span></span> <span data-ttu-id="b5dd0-111">Het veld Boekingslaag wordt dan automatisch ingesteld op Geen.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-111">The Posting layer field is then automatically set to None.</span></span> <span data-ttu-id="b5dd0-112">De boeken die niet naar het grootboek boeken, worden gewoonlijk gebruikt voor belastingaangiftes.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-112">Typically, books that don’t post to the general ledger are used for tax reporting purposes.</span></span> <span data-ttu-id="b5dd0-113">Deze aanpak geeft u meer flexibiliteit om historische transacties voor het activumboek te verwijderen, omdat ze niet in het grootboek zijn bevestigd.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-113">This approach gives you the additional flexibility to delete historical transactions for the asset book, because they haven’t been committed to the general ledger.</span></span>

<span data-ttu-id="b5dd0-114">Vaste-activajournalen worden bepaald door de pagina Journaalnamen in Grootboek > Journaalinstellingen > Journaalnamen.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-114">Fixed asset journals are defined by using the Journal names page at General ledger > Journal setup > Journal names.</span></span> <span data-ttu-id="b5dd0-115">Elk journaal waarin u afschrijvingen kunt boeken, wordt voor slechts één boekingslaag door de journaalnaam gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-115">Each journal that you can post depreciations in is defined by its journal name for only one posting layer.</span></span> <span data-ttu-id="b5dd0-116">De boekingslaag in het journaal kan niet worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-116">The posting layer in the journal can’t be changed.</span></span> <span data-ttu-id="b5dd0-117">Deze beperking zorgt dat de transacties voor elke boekingslaag gescheiden blijven.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-117">This restriction helps guarantee that transactions for each posting layer are kept separate.</span></span> <span data-ttu-id="b5dd0-118">Voor elke boekingslaag moet er minstens één journaalnaam worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-118">At least one journal name must be created for each posting layer.</span></span> <span data-ttu-id="b5dd0-119">Als u boeken gebruikt die niet naar het grootboek boeken, moet u ook een journaal maken waarin de boekingslaag is ingesteld op Geen.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-119">If you’re using books that don’t post to the general ledger, you must also create a journal where the posting layer is set to None.</span></span>

<span data-ttu-id="b5dd0-120">U kunt grootboekrekeningen toewijzen voor vaste-activatransacties op de pagina Boekingsprofielen voor vaste activa.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-120">You can designate ledger accounts for fixed asset transactions on the Fixed asset posting profiles page.</span></span> <span data-ttu-id="b5dd0-121">Voor elk boekingsprofiel moet u het relevante transactietype en boek selecteren, en vervolgens de grootboekrekeningen aangeven.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-121">For each posting profile, you must select the relevant transaction type and book, and then designate the ledger accounts.</span></span> <span data-ttu-id="b5dd0-122">Stel een boekingsprofielrecord in voor elk boek dat naar het grootboek wordt geboekt.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-122">Set up a posting profile record for each book that will post to the general ledger.</span></span>

> [!NOTE] 
> <span data-ttu-id="b5dd0-123">Door afgeleide boeken te gebruiken, kunt u tegelijkertijd transacties naar verschillende boekingslagen boeken.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-123">By using derived books, you can post transactions to different posting layers at the same time.</span></span> <span data-ttu-id="b5dd0-124">U maakt de transacties van het primaire boek in een journaal waarvan de boekingslaag overeenkomt met de boekingslaag van het boek.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-124">You create the transactions of the primary book in a journal where the posting layer corresponds to the book posting layer.</span></span> <span data-ttu-id="b5dd0-125">Tijdens het boeken worden de transacties van het afgeleide boek naar de respectieve boekingslagen geboekt.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-125">During posting, the derived book transactions are posted to the appropriate posting layers.</span></span>

<span data-ttu-id="b5dd0-126">Zie voor meer informatie [Afgeleide boeken](derived-books.md) en [Boeken met afgeleide boeken](post-derived-value-models.md).</span><span class="sxs-lookup"><span data-stu-id="b5dd0-126">For more information see, [Derived books](derived-books.md) and [Posting with derived books](post-derived-value-models.md).</span></span>




