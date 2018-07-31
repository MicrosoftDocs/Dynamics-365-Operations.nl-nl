---
title: "Startpagina Grootboek en Financiële rapportage"
description: "Met Grootboek kunt u de financiële records van de rechtspersoon definiëren en beheren."
author: twheeloc
manager: AnnBe
ms.date: 08/31/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: GeneralJournalEntryWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 03bab1d03be71c0e23a6ea93f542d6a52a212a1f
ms.openlocfilehash: 9ee3f73cd11b38ed2237ea3fe08db18000e55f07
ms.contentlocale: nl-nl
ms.lasthandoff: 06/25/2018

---

# <a name="general-ledger"></a><span data-ttu-id="b2462-103">Grootboek</span><span class="sxs-lookup"><span data-stu-id="b2462-103">General ledger</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b2462-104">Met Grootboek kunt u de financiële records van de rechtspersoon definiëren en beheren.</span><span class="sxs-lookup"><span data-stu-id="b2462-104">Use General ledger to define and manage the legal entity’s financial records.</span></span> <span data-ttu-id="b2462-105">Het grootboek is een register met debet- en creditposten.</span><span class="sxs-lookup"><span data-stu-id="b2462-105">The general ledger is a register of debit and credit entries.</span></span> <span data-ttu-id="b2462-106">Deze posten worden geclassificeerd met behulp van de rekeningen in een rekeningschema.</span><span class="sxs-lookup"><span data-stu-id="b2462-106">These entries are classified using the accounts that are listed in a chart of accounts.</span></span> 

 - [<span data-ttu-id="b2462-107">Uw rekeningschema plannen</span><span class="sxs-lookup"><span data-stu-id="b2462-107">Plan your chart of accounts</span></span>](plan-chart-of-accounts.md)
 - [<span data-ttu-id="b2462-108">Hoofdrekeningtypen</span><span class="sxs-lookup"><span data-stu-id="b2462-108">Main account types</span></span>](main-account-types.md)

<span data-ttu-id="b2462-109">U kunt bedragen toewijzen aan (of verdelen over) een of meer rekeningen of combinaties van rekeningen en dimensies op basis van toewijzingsregels.</span><span class="sxs-lookup"><span data-stu-id="b2462-109">You can allocate, or distribute, monetary amounts to one or more accounts or account and dimension combinations based on allocation rules.</span></span> <span data-ttu-id="b2462-110">Er zijn twee typen toewijzingen: vaste en variabele.</span><span class="sxs-lookup"><span data-stu-id="b2462-110">There are two types of allocations: fixed and variable.</span></span> <span data-ttu-id="b2462-111">U kunt ook transacties tussen grootboekrekeningen vereffenen en valutabedragen herwaarderen.</span><span class="sxs-lookup"><span data-stu-id="b2462-111">You can also settle transactions between ledger accounts and revalue currency amounts.</span></span> <span data-ttu-id="b2462-112">Aan het einde van een boekjaar moet u afsluittransacties genereren en de rekeningen voorbereiden op het nieuwe boekjaar.</span><span class="sxs-lookup"><span data-stu-id="b2462-112">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span> <span data-ttu-id="b2462-113">Met de consolidatiefunctionaliteit kunt u de financiële resultaten van verschillende dochtermaatschappijen samenvoegen tot de resultaten voor één geconsolideerde organisatie.</span><span class="sxs-lookup"><span data-stu-id="b2462-113">You can use the consolidation functionality to combine the financial results for several subsidiary legal entities into results for a single, consolidated organization.</span></span> <span data-ttu-id="b2462-114">De dochtermaatschappijen kunnen zich in dezelfde database in Microsoft Dynamics 365 for Finance and Operations bevinden, of in afzonderlijke databases.</span><span class="sxs-lookup"><span data-stu-id="b2462-114">The subsidiaries can be in the same Microsoft Dynamics 365 for Finance and Operations database or in separate databases.</span></span>

- [<span data-ttu-id="b2462-115">Overzicht van consolidatie en schrapping</span><span class="sxs-lookup"><span data-stu-id="b2462-115">Consolidation and elimination overview</span></span>](../budgeting/consolidation-elimination-overview.md)
- [<span data-ttu-id="b2462-116">Grootboekrekeningsaldi</span><span class="sxs-lookup"><span data-stu-id="b2462-116">General ledger account balances</span></span>](general-ledger-account-balances.md)
- [<span data-ttu-id="b2462-117">Financiële dimensies</span><span class="sxs-lookup"><span data-stu-id="b2462-117">Financial dimensions</span></span>](financial-dimensions.md)

<span data-ttu-id="b2462-118">[![Bedrijfsproces](./media/GL-process.PNG)](./media/GL-process.PNG)</span><span class="sxs-lookup"><span data-stu-id="b2462-118">[![Business process](./media/GL-process.PNG)](./media/GL-process.PNG)</span></span>

## <a name="sales-tax"></a><span data-ttu-id="b2462-119">Btw</span><span class="sxs-lookup"><span data-stu-id="b2462-119">Sales tax</span></span>
<span data-ttu-id="b2462-120">Ieder bedrijf int en betaalt btw aan verschillende btw-diensten.</span><span class="sxs-lookup"><span data-stu-id="b2462-120">Every company collects and pays taxes to various tax authorities.</span></span> <span data-ttu-id="b2462-121">De regels en tarieven variëren per land/regio, staat, graafschap en stad.</span><span class="sxs-lookup"><span data-stu-id="b2462-121">The rules and rates vary by country/region, state, county, and city.</span></span>
<span data-ttu-id="b2462-122">Bovendien moeten de regels periodiek worden bijgewerkt wanneer de belastingdienst de vereisten wijzigt.</span><span class="sxs-lookup"><span data-stu-id="b2462-122">In addition, the rules must be updated periodically when tax authorities change their requirements.</span></span> <span data-ttu-id="b2462-123">De btw-codes bevatten de basisinformatie over de bedragen die u int en de bedragen die u aan de btw-dienst betaalt.</span><span class="sxs-lookup"><span data-stu-id="b2462-123">Sales tax codes contain the basic information about how much you collect and pay to the authorities.</span></span> <span data-ttu-id="b2462-124">Wanneer u btw-codes instelt, definieert u de bedragen of percentages die moeten worden geïnd.</span><span class="sxs-lookup"><span data-stu-id="b2462-124">When you set up sales tax codes, you define the amounts or percentages that must be collected.</span></span> <span data-ttu-id="b2462-125">U definieert ook de verschillende methoden waarmee deze bedragen of percentages waarop de transactiebedragen worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="b2462-125">You also define the various methods by which those amounts or percentages are applied to transaction amounts.</span></span> <span data-ttu-id="b2462-126">De onderwerpen in dit hoofdstuk geven informatie over hoe u btw-codes instelt voor de methoden en tarieven die uw belastingdienst oplegt.</span><span class="sxs-lookup"><span data-stu-id="b2462-126">The topics in this section provide information about how to set up sales tax codes for the methods and rates that your tax authorities require.</span></span>

 - [<span data-ttu-id="b2462-127">Btw-overzicht</span><span class="sxs-lookup"><span data-stu-id="b2462-127">Sales tax overview</span></span>](indirect-taxes-overview.md)
 - [<span data-ttu-id="b2462-128">Btw-tarieven op basis van Marginale basis en Berekeningsmethoden</span><span class="sxs-lookup"><span data-stu-id="b2462-128">Sales tax rates based on the Marginal base and Calculation methods</span></span>](marginal-base-field.md)
 - [<span data-ttu-id="b2462-129">Btw-betalingen en afrondingsregels</span><span class="sxs-lookup"><span data-stu-id="b2462-129">Sales tax payments and rounding rules</span></span>](round-sales-tax-payments.md)


## <a name="additional-resources"></a><span data-ttu-id="b2462-130">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="b2462-130">Additional resources</span></span>

### <a name="whats-new"></a><span data-ttu-id="b2462-131">Wat is er nieuw</span><span class="sxs-lookup"><span data-stu-id="b2462-131">What's new</span></span>

<span data-ttu-id="b2462-132">Ga naar [Opmerkingen bij release](https://docs.microsoft.com/en-us/business-applications-release-notes/) om te zien welke nieuwe functies beschikbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="b2462-132">Go to the [Release notes](https://docs.microsoft.com/en-us/business-applications-release-notes/) to see what new features have been released.</span></span> 

### <a name="videos"></a><span data-ttu-id="b2462-133">Video's</span><span class="sxs-lookup"><span data-stu-id="b2462-133">Videos</span></span>

<span data-ttu-id="b2462-134">Bekijk de procedurevideo's die nu beschikbaar zijn op het [Microsoft Dynamics 365 YouTube-kanaal](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span><span class="sxs-lookup"><span data-stu-id="b2462-134">Check out the how-to videos that are now available on the [Microsoft Dynamics 365 YouTube Channel](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span></span>

### <a name="blogs"></a><span data-ttu-id="b2462-135">Weblogs</span><span class="sxs-lookup"><span data-stu-id="b2462-135">Blogs</span></span>

<span data-ttu-id="b2462-136">U kunt adviezen, nieuws en andere informatie over Leveranciers en andere oplossingen vinden op de [Microsoft Dynamics 365-blog](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise).</span><span class="sxs-lookup"><span data-stu-id="b2462-136">You can find opinions, news, and other information about Accounts payable and other solutions on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise).</span></span>

<span data-ttu-id="b2462-137">Er zijn veel berichten over Grootboek beschikbaar op de [blog van het Microsoft Dynamics AX-productteam](https://blogs.msdn.microsoft.com/dax/).</span><span class="sxs-lookup"><span data-stu-id="b2462-137">There are many posts about General ledger on the [Microsoft Dynamics AX product team blog](https://blogs.msdn.microsoft.com/dax/).</span></span> <span data-ttu-id="b2462-138">Hoewel sommige van deze berichten zijn geschreven voor de vorige versie van Grootboek, zijn dezelfde concepten nog steeds van toepassing en komen ook de procedures overeen in de huidige versie.</span><span class="sxs-lookup"><span data-stu-id="b2462-138">Although some of these posts were written for the previous version of General ledger, the same concepts still apply, and the procedures are also similar in the current version.</span></span>

<span data-ttu-id="b2462-139">De [Microsoft Dynamics Operations Partner Community Blog](https://community.dynamics.com/partner/b/operationspartnercommunityblog) geeft Microsoft Dynamics-partners een enkele bron met informatie over wat nieuw is en welke trends er zijn in MBS Operations.</span><span class="sxs-lookup"><span data-stu-id="b2462-139">The [Microsoft Dynamics Operations Partner Community Blog](https://community.dynamics.com/partner/b/operationspartnercommunityblog) gives Microsoft Dynamics Partners a single resource where they can learn what is new and trending in MBS Operations.</span></span>

#### <a name="community-blogs"></a><span data-ttu-id="b2462-140">Community-blogs</span><span class="sxs-lookup"><span data-stu-id="b2462-140">Community blogs</span></span>

- [<span data-ttu-id="b2462-141">Wat u moet weten over grootboeken in Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b2462-141">What you should know about ledger in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/04/29/what-you-should-know-about-ledger-in-dynamics-365-for-finance-and-operations)


