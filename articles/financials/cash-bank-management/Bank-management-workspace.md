---
title: Werkgebied voor bankbeheer
description: Dit onderwerp bevat informatie over het werkgebied Bankbeheer. Dit werkgebied bevat informatie die is gerelateerd aan bedrijfsbankrekeningen en bevat een overzichtsweergave en een analysepagina. De overzichtsweergave bevat overzichtstegels, bankrekeninggegevens, een saldodiagram en gerelateerde informatie. De pagina Analyses gebruikt de mogelijkheden van Microsoft Power BI om visuele elementen te tonen die betrekking hebben op bankrekeningsaldi.
author: saraschi2
manager: AnnBe
ms.date: 05/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 91a6c2e5aeee4a10ffbd574f99218d49f9a19bbc
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="bank-management-workspace"></a><span data-ttu-id="a2ab9-106">Werkgebied voor bankbeheer</span><span class="sxs-lookup"><span data-stu-id="a2ab9-106">Bank management workspace</span></span>

<span data-ttu-id="a2ab9-107">Het werkgebied **Bankbeheer** bevat informatie die is gerelateerd aan bedrijfsbankrekeningen.</span><span class="sxs-lookup"><span data-stu-id="a2ab9-107">The **Bank management** workspace shows information that is related to company bank accounts.</span></span> <span data-ttu-id="a2ab9-108">Dit werkgebied bevat een **Overzicht** sweergave en de pagina **Analyses**.</span><span class="sxs-lookup"><span data-stu-id="a2ab9-108">This workspace includes a **Summary** view and an **Analytics** page.</span></span> <span data-ttu-id="a2ab9-109">De **Overzicht** sweergave bevat overzichtstegels, bankrekeninggegevens, een saldodiagram en gerelateerde informatie.</span><span class="sxs-lookup"><span data-stu-id="a2ab9-109">The **Summary** view shows summary tiles, bank account information, a balance chart, and related information.</span></span> <span data-ttu-id="a2ab9-110">De pagina **Analyses** gebruikt de mogelijkheden van Microsoft Power BI om visuele elementen te tonen die betrekking hebben op bankrekeningsaldi.</span><span class="sxs-lookup"><span data-stu-id="a2ab9-110">The **Analytics** page uses the capabilities of Microsoft Power BI to show visuals that are related to bank account balances.</span></span>

## <a name="summary-view"></a><span data-ttu-id="a2ab9-111">Overzichtsweergave</span><span class="sxs-lookup"><span data-stu-id="a2ab9-111">Summary view</span></span>

### <a name="summary"></a><span data-ttu-id="a2ab9-112">Overzicht</span><span class="sxs-lookup"><span data-stu-id="a2ab9-112">Summary</span></span>

<span data-ttu-id="a2ab9-113">De tegels in de sectie **Overzicht** bieden een overzicht van uw bankrekeningen en snelle toegang tot de pagina's die u het vaakst moet gebruiken.</span><span class="sxs-lookup"><span data-stu-id="a2ab9-113">The tiles in the **Summary** section give an overview of your bank accounts and provide quick access to the pages that you most often have to use.</span></span> <span data-ttu-id="a2ab9-114">De bankafstemmingsgegevens gelden specifiek voor de functie voor geavanceerde bankafstemming.</span><span class="sxs-lookup"><span data-stu-id="a2ab9-114">The bank reconciliation information is specific to the Advanced bank reconciliation functionality.</span></span> <span data-ttu-id="a2ab9-115">Informatie wordt alleen opgenomen voor de bankrekeningen waarvoor de optie **Geavanceerde bankafstemming** is ingesteld op **Ja** op de pagina **Bankrekening**.</span><span class="sxs-lookup"><span data-stu-id="a2ab9-115">Information is included only for those bank accounts that have the **Advanced bank reconciliation** option set to **Yes** on the **Bank account** page.</span></span> <span data-ttu-id="a2ab9-116">In de sectie **Overzicht** kunt u elektronische bankbestanden voor bankrekeningen importeren voor alle rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="a2ab9-116">From the **Summary** section, you can import electronic bank files for bank accounts across all legal entities.</span></span>

### <a name="bank-accounts"></a><span data-ttu-id="a2ab9-117">Bankrekeningen</span><span class="sxs-lookup"><span data-stu-id="a2ab9-117">Bank accounts</span></span>

<span data-ttu-id="a2ab9-118">Elke bankrekening in de rechtspersoon wordt vertegenwoordigd door een kaart in de sectie **Bankrekeningen**.</span><span class="sxs-lookup"><span data-stu-id="a2ab9-118">Each bank account in the legal entity is represented by a card in the **Bank accounts** section.</span></span> <span data-ttu-id="a2ab9-119">Het huidige saldo wordt weergegeven en u kunt inzoomen op de transacties waaruit het overzichtssaldobedrag bestaat.</span><span class="sxs-lookup"><span data-stu-id="a2ab9-119">The current balance is shown, and you can drill down to the transactions that make up that summary balance amount.</span></span> <span data-ttu-id="a2ab9-120">Met het bedrag aan **Overbruggingstransacties** kunt u ook inzoomen op de transacties waaruit dit overzichtsbedrag bestaat.</span><span class="sxs-lookup"><span data-stu-id="a2ab9-120">The **Bridged transactions** amount also lets you drill down to the transactions that make up that summary amount.</span></span> <span data-ttu-id="a2ab9-121">Overbruggingstransacties zijn alle transacties in behandeling die zijn geboekt met behulp van de overbruggingsfunctionaliteit, maar die nog niet zijn verrekend.</span><span class="sxs-lookup"><span data-stu-id="a2ab9-121">Bridged transactions are any pending transactions that have been posted by using bridging functionality, but that haven't yet been cleared.</span></span> <span data-ttu-id="a2ab9-122">Het bedrag van **Saldo in behandeling** is het huidige saldo minus de overbruggingstransacties of transacties in behandeling.</span><span class="sxs-lookup"><span data-stu-id="a2ab9-122">The **Pending balance** amount is the current balance minus the bridged, or pending, transactions.</span></span>

<span data-ttu-id="a2ab9-123">De kaart wordt ook weergegeven wanneer de bankrekening voor het laatst is afgestemd.</span><span class="sxs-lookup"><span data-stu-id="a2ab9-123">The card also shows when the bank account was last reconciled.</span></span> <span data-ttu-id="a2ab9-124">Deze informatie wordt alleen weergegeven als Geavanceerde bankafstemming is ingeschakeld voor de bankrekening.</span><span class="sxs-lookup"><span data-stu-id="a2ab9-124">This information is shown only if Advanced bank reconciliation is enabled for the bank account.</span></span>

### <a name="balance"></a><span data-ttu-id="a2ab9-125">Balans</span><span class="sxs-lookup"><span data-stu-id="a2ab9-125">Balance</span></span>

<span data-ttu-id="a2ab9-126">Het diagram **Saldo** toont historische saldogegevens voor de bankrekening die is geselecteerd in de sectie **Bankrekeningen** of een overzicht van historische saldogegevens voor alle bankrekeningen in de rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="a2ab9-126">The **Balance** chart shows either historic balance information for the bank account that is selected in the **Bank accounts** section or a summary of historic balance information for all bank accounts in the legal entity.</span></span> <span data-ttu-id="a2ab9-127">Deze informatie is beschikbaar voor verschillende perioden: de huidige week, de huidige maand, het huidige jaar, de laatste vijf jaar en alle perioden (de volledige historie van de bankrekening).</span><span class="sxs-lookup"><span data-stu-id="a2ab9-127">This information is available for various periods: the current week, the current month, the current year, the last five years, and all periods (the full history of the bank account).</span></span> 

<span data-ttu-id="a2ab9-128">Als u het diagram **Saldo** bekijkt voor één bankrekening, worden de historische saldi weergegeven in de bankrekeningvaluta.</span><span class="sxs-lookup"><span data-stu-id="a2ab9-128">If you're viewing the **Balance** chart for a single bank account, the historic balances are shown in the bank account currency.</span></span> <span data-ttu-id="a2ab9-129">Als u het diagram bekijkt voor alle bankrekeningen in de rechtspersoon, worden de historische saldi weergegeven in de valuta voor boekhouding.</span><span class="sxs-lookup"><span data-stu-id="a2ab9-129">If you're viewing the chart for all bank accounts in the legal entity, the historic balances are shown in the accounting currency.</span></span>

<span data-ttu-id="a2ab9-130">Informatie over wanneer de gegevens voor het laatst zijn bijgewerkt, vindt u boven aan het diagram.</span><span class="sxs-lookup"><span data-stu-id="a2ab9-130">Information about when the data was last updated appears at the top of the chart.</span></span> <span data-ttu-id="a2ab9-131">U kunt de gegevens desgewenst bijwerken.</span><span class="sxs-lookup"><span data-stu-id="a2ab9-131">You can update the data as you require.</span></span>

### <a name="related-information"></a><span data-ttu-id="a2ab9-132">Verwante informatie</span><span class="sxs-lookup"><span data-stu-id="a2ab9-132">Related information</span></span>

<span data-ttu-id="a2ab9-133">In de sectie **Verwante informatie** kunt u de pagina **Algemeen journaal** openen om bankoverschrijvingen te voltooien.</span><span class="sxs-lookup"><span data-stu-id="a2ab9-133">From the **Related information** section, you can open the **General journal** page to complete bank transfers.</span></span> <span data-ttu-id="a2ab9-134">U kunt ook de pagina´s **Banktransacties** en **Overbruggingstransacties** snel openen.</span><span class="sxs-lookup"><span data-stu-id="a2ab9-134">You can also quickly open the **Bank transactions** and **Bridged transactions** pages.</span></span>

## <a name="analytics-view"></a><span data-ttu-id="a2ab9-135">Analyseweergave</span><span class="sxs-lookup"><span data-stu-id="a2ab9-135">Analytics view</span></span>

<span data-ttu-id="a2ab9-136">De pagina **Analyses** bevat belangrijke metrische gegevens over de bankrekeningen in het huidige bedrijf.</span><span class="sxs-lookup"><span data-stu-id="a2ab9-136">The **Analytics** page provides important metrics about the bank accounts in the current company.</span></span> <span data-ttu-id="a2ab9-137">De volgende visualisaties zijn beschikbaar op de pagina:</span><span class="sxs-lookup"><span data-stu-id="a2ab9-137">The following visualizations are available on the page:</span></span>

-   <span data-ttu-id="a2ab9-138">Totaal banksaldo in systeemvaluta</span><span class="sxs-lookup"><span data-stu-id="a2ab9-138">Total bank balance in system currency</span></span>
-   <span data-ttu-id="a2ab9-139">Saldo per rechtspersoon</span><span class="sxs-lookup"><span data-stu-id="a2ab9-139">Balance by legal entity</span></span>
-   <span data-ttu-id="a2ab9-140">Werkelijk versus voorspeld saldo van vandaag in valuta van de bankrekening</span><span class="sxs-lookup"><span data-stu-id="a2ab9-140">Today’s actual vs forecasted balance in bank account currency</span></span>
-   <span data-ttu-id="a2ab9-141">Saldo per bankrekening</span><span class="sxs-lookup"><span data-stu-id="a2ab9-141">Balance by bank account</span></span>
-   <span data-ttu-id="a2ab9-142">Saldo per valuta</span><span class="sxs-lookup"><span data-stu-id="a2ab9-142">Balance by currency</span></span>

<span data-ttu-id="a2ab9-143">U kunt bankanalyses bekijken voor alle bedrijven in het werkgebied **Overzicht van contant geld - alle bedrijven**.</span><span class="sxs-lookup"><span data-stu-id="a2ab9-143">You can view bank analytics across all companies from the **Cash overview – all companies** workspace.</span></span>

