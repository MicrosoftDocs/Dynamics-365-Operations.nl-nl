---
title: Documenten en boekstukken chronologisch nummeren
description: In dit onderwerp wordt uitgelegd hoe u chronologische nummers kunt instellen en gebruiken voor toepasselijke documenten en gerelateerde boekstukken.
author: ikond
manager: AnnBe
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceGroup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 401195
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-15
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 31745632de7339d167ac9f18f02e6611e1a78b28
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104367"
---
# <a name="numbering-documents-and-vouchers-chronologically"></a><span data-ttu-id="ede94-103">Documenten en boekstukken chronologisch nummeren</span><span class="sxs-lookup"><span data-stu-id="ede94-103">Numbering documents and vouchers chronologically</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="ede94-104">In sommige landen is het wettelijk verplicht documenten en gerelateerde boekstukken in chronologische volgorde te nummeren.</span><span class="sxs-lookup"><span data-stu-id="ede94-104">In some countries, there is a legal requirement to number documents and related vouchers in chronological order.</span></span> <span data-ttu-id="ede94-105">De chronologie moet door perioden worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="ede94-105">The chronology must be supported by periods.</span></span> <span data-ttu-id="ede94-106">Alle nummers die tot eerdere perioden behoren, moeten lager zijn dan de nummers die tot latere perioden behoren.</span><span class="sxs-lookup"><span data-stu-id="ede94-106">All of the numbers that belong to earlier periods must be less than the numbers that belong to later periods.</span></span> <span data-ttu-id="ede94-107">Om aan deze vereiste te voldoen, is de chronologische nummeringsfunctionaliteit geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="ede94-107">To meet this requirement, chronological numbering functionality has been implemented.</span></span> <span data-ttu-id="ede94-108">In dit onderwerp wordt uitgelegd hoe u chronologische nummers kunt configureren en gebruiken voor toepasselijke documenten en gerelateerde boekstukken.</span><span class="sxs-lookup"><span data-stu-id="ede94-108">This topic explains how to configure and use chronological numbers for applicable documents and related vouchers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ede94-109">Vereisten</span><span class="sxs-lookup"><span data-stu-id="ede94-109">Prerequisites</span></span>

<span data-ttu-id="ede94-110">Schakel in de werkruimte Functiebeheer de functie **Chronologische nummering** in.</span><span class="sxs-lookup"><span data-stu-id="ede94-110">In the Feature management workspace, turn on the **Chronological numbering** feature.</span></span> <span data-ttu-id="ede94-111">Zie [Overzicht van functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="ede94-111">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

## <a name="configure-chronological-numbering"></a><span data-ttu-id="ede94-112">Chronologische nummering configureren</span><span class="sxs-lookup"><span data-stu-id="ede94-112">Configure chronological numbering</span></span>

<span data-ttu-id="ede94-113">Chronologische nummering betreft de volgende documenten.</span><span class="sxs-lookup"><span data-stu-id="ede94-113">Chronological numbering affects the following documents.</span></span>

<span data-ttu-id="ede94-114">**Klanten**</span><span class="sxs-lookup"><span data-stu-id="ede94-114">**Accounts receivable**</span></span>
- <span data-ttu-id="ede94-115">Klantfactuur</span><span class="sxs-lookup"><span data-stu-id="ede94-115">Customer invoice</span></span>
- <span data-ttu-id="ede94-116">Leveranciersfactuurboekstuk</span><span class="sxs-lookup"><span data-stu-id="ede94-116">Customer invoice voucher</span></span>
- <span data-ttu-id="ede94-117">Verkoopcreditnota</span><span class="sxs-lookup"><span data-stu-id="ede94-117">Sales credit note</span></span>
- <span data-ttu-id="ede94-118">Verkoopcreditnotaboekstuk</span><span class="sxs-lookup"><span data-stu-id="ede94-118">Sales credit note voucher</span></span>
- <span data-ttu-id="ede94-119">Vrije-tekstfactuur</span><span class="sxs-lookup"><span data-stu-id="ede94-119">Free text invoice</span></span>
- <span data-ttu-id="ede94-120">Vrije-tekstfactuurboekstuk</span><span class="sxs-lookup"><span data-stu-id="ede94-120">Free text invoice voucher</span></span>
- <span data-ttu-id="ede94-121">Vrije-tekstcreditnota</span><span class="sxs-lookup"><span data-stu-id="ede94-121">Free text credit note</span></span>
- <span data-ttu-id="ede94-122">Vrije-tekstcreditnotaboekstuk</span><span class="sxs-lookup"><span data-stu-id="ede94-122">Free text credit note voucher</span></span>
- <span data-ttu-id="ede94-123">Pakbon</span><span class="sxs-lookup"><span data-stu-id="ede94-123">Packing slip</span></span>
- <span data-ttu-id="ede94-124">Boekstuk van pakbon</span><span class="sxs-lookup"><span data-stu-id="ede94-124">Packing slip voucher</span></span>
- <span data-ttu-id="ede94-125">Correctieboekstuk pakbon</span><span class="sxs-lookup"><span data-stu-id="ede94-125">Packing slip correction voucher</span></span>
- <span data-ttu-id="ede94-126">Rentenotaboekstuk</span><span class="sxs-lookup"><span data-stu-id="ede94-126">Interest note voucher</span></span>
- <span data-ttu-id="ede94-127">Aanmaningsboekstuk</span><span class="sxs-lookup"><span data-stu-id="ede94-127">Collection letter voucher</span></span>

<span data-ttu-id="ede94-128">**Leveranciers**</span><span class="sxs-lookup"><span data-stu-id="ede94-128">**Accounts payable**</span></span>
- <span data-ttu-id="ede94-129">Factuurboekstuk</span><span class="sxs-lookup"><span data-stu-id="ede94-129">Invoice voucher</span></span>
- <span data-ttu-id="ede94-130">Creditnotaboekstuk</span><span class="sxs-lookup"><span data-stu-id="ede94-130">Credit note voucher</span></span>
- <span data-ttu-id="ede94-131">Productontvangstbon</span><span class="sxs-lookup"><span data-stu-id="ede94-131">Product receipt voucher</span></span>

<span data-ttu-id="ede94-132">**Projectbeheer**</span><span class="sxs-lookup"><span data-stu-id="ede94-132">**Project management**</span></span>
- <span data-ttu-id="ede94-133">Factuur</span><span class="sxs-lookup"><span data-stu-id="ede94-133">Invoice</span></span>
- <span data-ttu-id="ede94-134">Factuurboekstuk</span><span class="sxs-lookup"><span data-stu-id="ede94-134">Invoice voucher</span></span>
- <span data-ttu-id="ede94-135">Creditnota</span><span class="sxs-lookup"><span data-stu-id="ede94-135">Credit note</span></span>
- <span data-ttu-id="ede94-136">Creditnotaboekstuk</span><span class="sxs-lookup"><span data-stu-id="ede94-136">Credit note voucher</span></span> 

### <a name="define-number-sequences"></a><span data-ttu-id="ede94-137">Nummerreeksen definiëren</span><span class="sxs-lookup"><span data-stu-id="ede94-137">Define number sequences</span></span>

<span data-ttu-id="ede94-138">Om nummerreeksen te definiëren, gaat u naar **Organisatiebeheer** > **Nummerreeksen** > **Nummerreeksen**.</span><span class="sxs-lookup"><span data-stu-id="ede94-138">To define number sequences, go to **Organization administration** > **Number sequences** > **Number sequences**.</span></span> <span data-ttu-id="ede94-139">U kunt zoveel nummerreeksen definiëren als u nodig hebt om de desbetreffende perioden voor vereiste documenten te dekken.</span><span class="sxs-lookup"><span data-stu-id="ede94-139">You can define as many number sequences as required to cover the affected periods for required documents.</span></span> 

<span data-ttu-id="ede94-140">Geef een bedrijf op voor elke nummerreeks.</span><span class="sxs-lookup"><span data-stu-id="ede94-140">Specify a company for each number sequence.</span></span> <span data-ttu-id="ede94-141">De segmenten van de nummerreeksen moeten zo worden gedefinieerd dat ze een chronologische volgorde voor perioden bieden.</span><span class="sxs-lookup"><span data-stu-id="ede94-141">The segments of the number sequences must be defined so that they provide chronological order for periods.</span></span> <span data-ttu-id="ede94-142">De segmentnamen kunnen bijvoorbeeld een speciaal voorvoegsel bevatten dat een specifieke periode aanduidt.</span><span class="sxs-lookup"><span data-stu-id="ede94-142">For example, the segment names can contain a special prefix that identifies a specific period.</span></span>

![Nummerreeks instellen](media/chrono-num-sequence.jpg)

### <a name="configure-number-sequence-groups"></a><span data-ttu-id="ede94-144">Nummerreeksgroepen configureren</span><span class="sxs-lookup"><span data-stu-id="ede94-144">Configure number sequence groups</span></span>

<span data-ttu-id="ede94-145">Om de nummerreeksgroepen te configureren, gaat u naar **Klanten** > **Instellingen** > **Klantparameters**.</span><span class="sxs-lookup"><span data-stu-id="ede94-145">To configure number sequence groups, go to **Accounts receivable** > **Setup** > **Accounts receivable parameters**.</span></span> <span data-ttu-id="ede94-146">Definieer op het tabblad **Nummerreeksen** zo veel nummerreeksgroepen als nodig is om de betreffende perioden te dekken.</span><span class="sxs-lookup"><span data-stu-id="ede94-146">On the **Number sequences** tab, define as many number sequences groups as required to cover the affected periods.</span></span> 

<span data-ttu-id="ede94-147">Selecteer voor elke groep een van de ondersteunde documentverwijzingen in de sectie **Verwijzing** en verwijs in het veld **Nummerreekscode** naar een nummerreeks die eerder is gemaakt voor de desbetreffende periode.</span><span class="sxs-lookup"><span data-stu-id="ede94-147">For each group, in the **Reference** section, select one of the supported document references, and in the **Number sequence code** field, refer to a number sequence that was previously created for the related period.</span></span>

![Nummerreeksgroep instellen](media/chrono-num-sequence-group.jpg)

<span data-ttu-id="ede94-149">Configureer ook nummerreeksgroepen in de modules **Klant** en **Projectbeheer en boekhouding**.</span><span class="sxs-lookup"><span data-stu-id="ede94-149">Similarly, configure number sequence groups in **Accounts payable** and **Project management and accounting** modules.</span></span>

### <a name="configure-number-sequence-groups-chronology"></a><span data-ttu-id="ede94-150">Chronologie voor nummerreeksgroepen configureren</span><span class="sxs-lookup"><span data-stu-id="ede94-150">Configure number sequence groups chronology</span></span>

<span data-ttu-id="ede94-151">Om de chronologie voor nummerreeksgroepen te configureren, gaat u naar **Organisatiebeheer** > **Nummerreeksen** > **Chronologische nummerreeksgroepen**.</span><span class="sxs-lookup"><span data-stu-id="ede94-151">To configure number sequence groups chronology, go to **Organization administration** > **Number sequences** > **Chronological number sequence groups**.</span></span> <span data-ttu-id="ede94-152">De toepasbaarheidsvoorwaarden voor nummerreeksgroepen definiëren.</span><span class="sxs-lookup"><span data-stu-id="ede94-152">Define the applicability conditions for number sequence groups.</span></span>

![Chronologische nummers instellen](media/chrono-num-sequence-group-period.jpg)

| <span data-ttu-id="ede94-154">Veld</span><span class="sxs-lookup"><span data-stu-id="ede94-154">Field</span></span>            | <span data-ttu-id="ede94-155">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="ede94-155">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ede94-156">Geldig vanaf</span><span class="sxs-lookup"><span data-stu-id="ede94-156">Effective</span></span>  | <span data-ttu-id="ede94-157">De begindatum van de toepasbaarheid van een nummerreeksgroep.</span><span class="sxs-lookup"><span data-stu-id="ede94-157">The start date of number sequence group applicability.</span></span> |
| <span data-ttu-id="ede94-158">Vervaldatum</span><span class="sxs-lookup"><span data-stu-id="ede94-158">Expiration</span></span>      | <span data-ttu-id="ede94-159">De einddatum van de toepasbaarheid van een nummerreeksgroep.</span><span class="sxs-lookup"><span data-stu-id="ede94-159">The end date of number sequence group applicability.</span></span> <span data-ttu-id="ede94-160">Als er geen einddatum wordt toegepast, selecteert u **Nooit**.</span><span class="sxs-lookup"><span data-stu-id="ede94-160">If no end date is applied, select **Never**.</span></span> |
| <span data-ttu-id="ede94-161">Nummerreeksgroep</span><span class="sxs-lookup"><span data-stu-id="ede94-161">Number sequence group</span></span> | <span data-ttu-id="ede94-162">Nummerreeksgroep die wordt gebruikt om documentnummers te genereren tijdens de periode.</span><span class="sxs-lookup"><span data-stu-id="ede94-162">Number sequence group that will be used to generate document numbers during the period.</span></span> |
| <span data-ttu-id="ede94-163">Oorspronkelijke nummerreeksgroep</span><span class="sxs-lookup"><span data-stu-id="ede94-163">Original number sequence group</span></span> | <span data-ttu-id="ede94-164">Deze nummerreeksgroepscode wordt gebruikt om extra te filteren op de cases wanneer er voor documenten al een specifieke *permanente* nummerreeksgroep is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="ede94-164">This number sequence group code is used for additional filtering for the cases when documents already have a specific *permanent* number sequence group assigned.</span></span> <span data-ttu-id="ede94-165">Een lege waarde wordt als een specifieke waarde beschouwd.</span><span class="sxs-lookup"><span data-stu-id="ede94-165">An empty value is considered a specific value.</span></span> <span data-ttu-id="ede94-166">Als u een voorlopige toegewezen groep moet negeren, gebruikt u de optie **Standaard** voor deze instelling.</span><span class="sxs-lookup"><span data-stu-id="ede94-166">If you need to ignore a preliminary assigned group, use the **Default** option for this setup.</span></span> |
| <span data-ttu-id="ede94-167">Standaard</span><span class="sxs-lookup"><span data-stu-id="ede94-167">Default</span></span> | <span data-ttu-id="ede94-168">Als deze is ingeschakeld, negeert het systeem de voorlopig toegewezen nummerreeksgroep voor documenten en gebruikt het systeem alleen de begin- en einddatum van de perioden voor de toepasbaarheidsanalyse.</span><span class="sxs-lookup"><span data-stu-id="ede94-168">If turned on, the system ignores the preliminary assigned document number sequence group and uses only the periods start and end dates for applicability analysis.</span></span> <span data-ttu-id="ede94-169">Als deze is uitgeschakeld, wordt de volledige combinatie **Geldig vanaf** + **Vervaldatum** + **Oorspronkelijke nummerreeksgroep** voor selectie gebruikt.</span><span class="sxs-lookup"><span data-stu-id="ede94-169">If turned off, the system uses the full combination **Effective** + **Expiration** + **Original number sequence group** for selection.</span></span> |

## <a name="document-posting"></a><span data-ttu-id="ede94-170">Documentboeking</span><span class="sxs-lookup"><span data-stu-id="ede94-170">Document posting</span></span>
<span data-ttu-id="ede94-171">Wanneer u een document boekt, wordt de betreffende nummerreeksgroep aan het document toegewezen op basis van de boekingsdatum van het document en vervolgens gebruikt om een documentnummer te genereren op basis van de gedetecteerde nummerreeks.</span><span class="sxs-lookup"><span data-stu-id="ede94-171">When you post a document, the appropriate number sequence group is assigned to the document, based on document's posting date, and then used to generate a document number based on the detected number sequence.</span></span> <span data-ttu-id="ede94-172">Er wordt een bericht weergegeven met betrekking tot de nummerreeksgroeptoewijzing.</span><span class="sxs-lookup"><span data-stu-id="ede94-172">The system provides a message regarding the number sequence group assignment.</span></span>

![Documentnummer](media/chrono-num-sequence-fti.jpg)

> [!NOTE]
> <span data-ttu-id="ede94-174">In sommige landen is er al een specifieke logica geïmplementeerd voor documentnummering.</span><span class="sxs-lookup"><span data-stu-id="ede94-174">For some countries, there is a specific logic already implemented for document numbering.</span></span> <span data-ttu-id="ede94-175">In dit geval heeft de landspecifieke logica voorrang op de functie voor **chronologische nummering**.</span><span class="sxs-lookup"><span data-stu-id="ede94-175">In this case, country-specific logic will override the **Chronological numbering** feature.</span></span>
