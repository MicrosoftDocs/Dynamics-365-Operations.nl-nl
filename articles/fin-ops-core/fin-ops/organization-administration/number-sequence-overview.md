---
title: Overzicht van Nummerreeksen
description: Nummerreeksen worden gebruikt om leesbare, unieke id´s te maken voor hoofdgegevensregistraties en transactieregistraties die deze nodig hebben.
author: MargoC
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceConfiguration
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 15461
ms.assetid: 6e19bd1d-192b-4da2-8573-84f6e1ce98ef
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c036a6bf315ddb4df93c43bb3aa2b9370c7fba36
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190069"
---
# <a name="number-sequences-overview"></a><span data-ttu-id="d9d52-103">Overzicht van Nummerreeksen</span><span class="sxs-lookup"><span data-stu-id="d9d52-103">Number sequences overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9d52-104">Nummerreeksen worden gebruikt om leesbare, unieke id´s te maken voor hoofdgegevensregistraties en transactieregistraties die deze nodig hebben.</span><span class="sxs-lookup"><span data-stu-id="d9d52-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require identifiers.</span></span> <span data-ttu-id="d9d52-105">Een hoofdgegevens- of transactieregistratie die een identificatie nodig heeft wordt een *verwijzing* genoemd.</span><span class="sxs-lookup"><span data-stu-id="d9d52-105">A master data record or transaction record that requires an identifier is referred to as a *reference*.</span></span>

<span data-ttu-id="d9d52-106">Voordat u nieuwe registraties voor een verwijzing kunt maken, moet u een nummerreeks instellen en deze aan de verwijzing koppelen.</span><span class="sxs-lookup"><span data-stu-id="d9d52-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="d9d52-107">Het is raadzaam om de formulieren in **Organisatiebeheer** te gebruiken om nummerreeksen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="d9d52-107">We recommend that you use the pages in **Organization administration** to set up number sequences.</span></span> <span data-ttu-id="d9d52-108">Als er modulespecifieke instellingen zijn vereist, kunt u de parameterpagina in een module gebruiken om nummerreeksen op te geven voor de verwijzingen in die module.</span><span class="sxs-lookup"><span data-stu-id="d9d52-108">If module-specific settings are required, you can use the parameters page in a module to specify number sequences for the references in that module.</span></span> <span data-ttu-id="d9d52-109">In **Klanten** en **Leveranciers** kunt u bijvoorbeeld nummerreeksgroepen instellen om specifieke nummerreeksen toe te wijzen aan specifieke klanten of leveranciers.</span><span class="sxs-lookup"><span data-stu-id="d9d52-109">For example, in **Accounts receivable** and **Accounts payable**, you can set up number sequence groups to allocate specific number sequences to specific customers or vendors.</span></span>

<span data-ttu-id="d9d52-110">Wanneer u een nummerreeks instelt, moet u een bereik opgeven die definieert welke organisatie de nummerreeks gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d9d52-110">When you set up a number sequence, you must specify a scope, which defines which organization uses the number sequence.</span></span> <span data-ttu-id="d9d52-111">De scope kan **Gedeeld**, **Bedrijf**, **Rechtspersoon** of **Operationele eenheid** zijn.</span><span class="sxs-lookup"><span data-stu-id="d9d52-111">The scope can be **Shared**, **Company**, **Legal entity**, or **Operating unit**.</span></span> <span data-ttu-id="d9d52-112">De scopes van **rechtspersonen** en **bedrijven** kunnen ook met **Fiscale kalenderperiode** worden gecombineerd om nog specifiekere nummerreeksen te maken.</span><span class="sxs-lookup"><span data-stu-id="d9d52-112">**Legal entity** and **Company** scopes can be combined with **Fiscal calendar period** to create even more specific number sequences.</span></span>

<span data-ttu-id="d9d52-113">Nummerreeksnotaties bestaan uit segmenten.</span><span class="sxs-lookup"><span data-stu-id="d9d52-113">Number sequence formats consist of segments.</span></span> <span data-ttu-id="d9d52-114">Nummerreeksen met een andere scope dan **Gedeeld**, kunnen segmenten bevatten die overeenkomen met de scope.</span><span class="sxs-lookup"><span data-stu-id="d9d52-114">Number sequences with a scope other than **Shared** can contain segments that correspond to the scope.</span></span> <span data-ttu-id="d9d52-115">Een nummerreeks met een scope van **Rechtspersoon** kan bijvoorbeeld een segment voor de rechtspersoon bevatten.</span><span class="sxs-lookup"><span data-stu-id="d9d52-115">For example, a number sequence with a scope of **Legal entity** can contain a legal entity segment.</span></span> <span data-ttu-id="d9d52-116">Door een scopesegmenten in de nummerreeksnotatie op te nemen, kunt u de scope van een specifieke registratie bepalen door naar het nummer te kijken.</span><span class="sxs-lookup"><span data-stu-id="d9d52-116">By including a scope segment in the number sequence format, you can identify the scope of a particular record by looking at its number.</span></span>

<span data-ttu-id="d9d52-117">Naast de segmenten die overeenkomen met scopes, kunnen nummerreeksnotaties **constante** en **alfanumerieke** segmenten bevatten.</span><span class="sxs-lookup"><span data-stu-id="d9d52-117">In addition to segments that correspond to scopes, number sequence formats can contain **Constant** and **Alphanumeric segments**.</span></span> <span data-ttu-id="d9d52-118">Een **constant** segment bevat een reeks letters, cijfers of symbolen die niet verandert.</span><span class="sxs-lookup"><span data-stu-id="d9d52-118">A **Constant** segment contains a set of letters, numbers, or symbols that does not change.</span></span> <span data-ttu-id="d9d52-119">Een **alfanumeriek** segment bevat een reeks letters of cijfers die worden verhoogd telkens als het nummer wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d9d52-119">An **Alphanumeric** segment contains a set of letters or numbers that increment every time that a number is used.</span></span> <span data-ttu-id="d9d52-120">Gebruik een hekje (\#) om stijgende nummers aan te geven en een en-teken (&) om stijgende letters aan te geven.</span><span class="sxs-lookup"><span data-stu-id="d9d52-120">Use a number sign (\#) to represent incrementing numbers and an ampersand (&) to represent incrementing letters.</span></span> <span data-ttu-id="d9d52-121">De indeling \#\#\#\#\#\_2017 maakt bijvoorbeeld de reeks 00001\_2017, 00002\_2017, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="d9d52-121">For example, the format \#\#\#\#\#\_2017 creates the sequence 00001\_2017, 00002\_2017, and so on.</span></span>

## <a name="number-sequence-examples"></a><span data-ttu-id="d9d52-122">Voorbeelden van nummerreeksen</span><span class="sxs-lookup"><span data-stu-id="d9d52-122">Number sequence examples</span></span>

<span data-ttu-id="d9d52-123">De volgende voorbeelden geven aan hoe u segmenten gebruikt om nummerreeksnotaties te maken.</span><span class="sxs-lookup"><span data-stu-id="d9d52-123">The following examples show how to use segments to create number sequence formats.</span></span> <span data-ttu-id="d9d52-124">De voorbeelden tonen in het bijzonder de effecten van het gebruik van scopesegmenten.</span><span class="sxs-lookup"><span data-stu-id="d9d52-124">In particular, the examples demonstrate the effects of using scope segments.</span></span>

### <a name="expense-report-numbers"></a><span data-ttu-id="d9d52-125">Onkostennotanummers</span><span class="sxs-lookup"><span data-stu-id="d9d52-125">Expense report numbers</span></span>

<span data-ttu-id="d9d52-126">In het volgende voorbeeld worden onkostennotanummer ingesteld voor de rechtspersoon die **CS** heet.</span><span class="sxs-lookup"><span data-stu-id="d9d52-126">In the following example, expense report numbers are set up for the legal entity that is titled **CS**.</span></span>

- <span data-ttu-id="d9d52-127">**Gebied:** Reis- en onkosten</span><span class="sxs-lookup"><span data-stu-id="d9d52-127">**Area:** Travel and expense</span></span>
- <span data-ttu-id="d9d52-128">**Referentie:** Het nummer van de onkostennota</span><span class="sxs-lookup"><span data-stu-id="d9d52-128">**Reference:** Expense report number</span></span>
- <span data-ttu-id="d9d52-129">**Bereik:** Rechtspersoon</span><span class="sxs-lookup"><span data-stu-id="d9d52-129">**Scope:** Legal entity</span></span>
- <span data-ttu-id="d9d52-130">**Rechtspersoon:** CS</span><span class="sxs-lookup"><span data-stu-id="d9d52-130">**Legal entity:** CS</span></span>

| <span data-ttu-id="d9d52-131">Segmenten</span><span class="sxs-lookup"><span data-stu-id="d9d52-131">Segments</span></span>  | <span data-ttu-id="d9d52-132">Segmenttype</span><span class="sxs-lookup"><span data-stu-id="d9d52-132">Segment type</span></span> | <span data-ttu-id="d9d52-133">Waarde</span><span class="sxs-lookup"><span data-stu-id="d9d52-133">Value</span></span>     |
|-----------|--------------|-----------|
| <span data-ttu-id="d9d52-134">Segment 1</span><span class="sxs-lookup"><span data-stu-id="d9d52-134">Segment 1</span></span> | <span data-ttu-id="d9d52-135">Rechtspersoon</span><span class="sxs-lookup"><span data-stu-id="d9d52-135">Legal entity</span></span> | <span data-ttu-id="d9d52-136">CS</span><span class="sxs-lookup"><span data-stu-id="d9d52-136">CS</span></span>        |
| <span data-ttu-id="d9d52-137">Segment 2</span><span class="sxs-lookup"><span data-stu-id="d9d52-137">Segment 2</span></span> | <span data-ttu-id="d9d52-138">Constante</span><span class="sxs-lookup"><span data-stu-id="d9d52-138">Constant</span></span>     | <span data-ttu-id="d9d52-139">-ONKOSTEN-</span><span class="sxs-lookup"><span data-stu-id="d9d52-139">-EXPENSE-</span></span> |
| <span data-ttu-id="d9d52-140">Segment 3</span><span class="sxs-lookup"><span data-stu-id="d9d52-140">Segment 3</span></span> | <span data-ttu-id="d9d52-141">Alfanumeriek</span><span class="sxs-lookup"><span data-stu-id="d9d52-141">Alphanumeric</span></span> | \#\#\#\#  |

<span data-ttu-id="d9d52-142">**Voorbeeld van een opgemaakt nummer**: CS-EXPENSE-0039</span><span class="sxs-lookup"><span data-stu-id="d9d52-142">**Example of formatted number**: CS-EXPENSE-0039</span></span>

<span data-ttu-id="d9d52-143">U kunt een soortgelijke nummerreeksnotatie instellen voor andere rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="d9d52-143">You can set up a similar number sequence format for other legal entities.</span></span> <span data-ttu-id="d9d52-144">Voor een rechtspersoon die **RW** heeft, is, wanneer u alleen de waarde van de rechtspersoon van het rechtspersoonsegment wijzigt, het opgemaakte nummer RW-EXPENSE-0039.</span><span class="sxs-lookup"><span data-stu-id="d9d52-144">For example, for a legal entity that is named **RW**, if you change only the value of the legal entity segment, the formatted number is RW-EXPENSE-0039.</span></span> <span data-ttu-id="d9d52-145">U kunt ook de volledige nummerreeksnotatie wijzigen voor andere rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="d9d52-145">You can also change the whole number sequence format for other legal entities.</span></span> <span data-ttu-id="d9d52-146">U kunt bijvoorbeeld het scopesegment van de rechtspersoon weglaten om een opgemaakt nummer zoals Exp-0001 te maken.</span><span class="sxs-lookup"><span data-stu-id="d9d52-146">For example, you can omit the legal entity scope segment to create a formatted number such as Exp-0001.</span></span>

### <a name="sales-order-numbers"></a><span data-ttu-id="d9d52-147">Verkoopordernummers</span><span class="sxs-lookup"><span data-stu-id="d9d52-147">Sales order numbers</span></span>

<span data-ttu-id="d9d52-148">In het volgende voorbeeld worden verkoopordernummers ingesteld voor de bedrijfs-id **CEU**.</span><span class="sxs-lookup"><span data-stu-id="d9d52-148">In the following example, sales order numbers are set up for the company ID **CEU**.</span></span>

- <span data-ttu-id="d9d52-149">**Gebied:** Verkoop</span><span class="sxs-lookup"><span data-stu-id="d9d52-149">**Area:** Sales</span></span>
- <span data-ttu-id="d9d52-150">**Referentie:** Verkooporder</span><span class="sxs-lookup"><span data-stu-id="d9d52-150">**Reference:** Sales order</span></span>
- <span data-ttu-id="d9d52-151">**Bereik:** Bedrijf</span><span class="sxs-lookup"><span data-stu-id="d9d52-151">**Scope:** Company</span></span>
- <span data-ttu-id="d9d52-152">**Bedrijf:** CEU</span><span class="sxs-lookup"><span data-stu-id="d9d52-152">**Company:** CEU</span></span>

| <span data-ttu-id="d9d52-153">Segmenten</span><span class="sxs-lookup"><span data-stu-id="d9d52-153">Segments</span></span>  | <span data-ttu-id="d9d52-154">Segmenttype</span><span class="sxs-lookup"><span data-stu-id="d9d52-154">Segment type</span></span> | <span data-ttu-id="d9d52-155">Waarde</span><span class="sxs-lookup"><span data-stu-id="d9d52-155">Value</span></span>    |
|-----------|--------------|----------|
| <span data-ttu-id="d9d52-156">Segment 1</span><span class="sxs-lookup"><span data-stu-id="d9d52-156">Segment 1</span></span> | <span data-ttu-id="d9d52-157">Constante</span><span class="sxs-lookup"><span data-stu-id="d9d52-157">Constant</span></span>     | <span data-ttu-id="d9d52-158">SO-</span><span class="sxs-lookup"><span data-stu-id="d9d52-158">SO-</span></span>      |
| <span data-ttu-id="d9d52-159">Segment 2</span><span class="sxs-lookup"><span data-stu-id="d9d52-159">Segment 2</span></span> | <span data-ttu-id="d9d52-160">Alfanumeriek</span><span class="sxs-lookup"><span data-stu-id="d9d52-160">Alphanumeric</span></span> | \#\#\#\# |

<span data-ttu-id="d9d52-161">**Voorbeeld van een opgemaakt nummer**: SO-0029</span><span class="sxs-lookup"><span data-stu-id="d9d52-161">**Example of formatted number**: SO-0029</span></span>

<span data-ttu-id="d9d52-162">Hoewel een scopesegment niet in de notaties is opgenomen, begint de nummering opnieuw voor elke bedrijfs-ID.</span><span class="sxs-lookup"><span data-stu-id="d9d52-162">Even though a scope segment is not included in the format, numbering restarts for each company ID.</span></span> <span data-ttu-id="d9d52-163">Als u dezelfde notatie gebruikt voor alle bedrijfs-ID´s, dan worden dezelfde nummers in elk bedrijf gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d9d52-163">If you use the same format for all company IDs, the same numbers are used in each company.</span></span> <span data-ttu-id="d9d52-164">Het verkoopordernummer SO-0029 wordt bijvoorbeeld in elk bedrijf gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d9d52-164">For example, sales order number SO-0029 is used in each company.</span></span> <span data-ttu-id="d9d52-165">U kunt ook de volledige nummerreeksnotatie wijzigen voor andere bedrijfs-ID´s.</span><span class="sxs-lookup"><span data-stu-id="d9d52-165">You can also change the whole number sequence format for other company IDs.</span></span>

### <a name="purchase-requisition-numbers"></a><span data-ttu-id="d9d52-166">Nummers van opdrachten tot inkoop</span><span class="sxs-lookup"><span data-stu-id="d9d52-166">Purchase requisition numbers</span></span>

<span data-ttu-id="d9d52-167">In het volgende voorbeeld zijn de nummers van de opdracht tot inkoop organisatiebreed.</span><span class="sxs-lookup"><span data-stu-id="d9d52-167">In the following example, purchase requisition numbers are organization-wide.</span></span>

- <span data-ttu-id="d9d52-168">**Gebied:** Inkoop</span><span class="sxs-lookup"><span data-stu-id="d9d52-168">**Area:** Purchase</span></span>
- <span data-ttu-id="d9d52-169">**Referentie:** Opdracht tot inkoop</span><span class="sxs-lookup"><span data-stu-id="d9d52-169">**Reference:** Purchase requisition</span></span>
- <span data-ttu-id="d9d52-170">**Bereik:** Gedeeld</span><span class="sxs-lookup"><span data-stu-id="d9d52-170">**Scope:** Shared</span></span>

| <span data-ttu-id="d9d52-171">Segmenten</span><span class="sxs-lookup"><span data-stu-id="d9d52-171">Segments</span></span>  | <span data-ttu-id="d9d52-172">Segmenttype</span><span class="sxs-lookup"><span data-stu-id="d9d52-172">Segment type</span></span> | <span data-ttu-id="d9d52-173">Waarde</span><span class="sxs-lookup"><span data-stu-id="d9d52-173">Value</span></span>    |
|-----------|--------------|----------|
| <span data-ttu-id="d9d52-174">Segment 1</span><span class="sxs-lookup"><span data-stu-id="d9d52-174">Segment 1</span></span> | <span data-ttu-id="d9d52-175">Constante</span><span class="sxs-lookup"><span data-stu-id="d9d52-175">Constant</span></span>     | <span data-ttu-id="d9d52-176">Behoefte</span><span class="sxs-lookup"><span data-stu-id="d9d52-176">Req</span></span>      |
| <span data-ttu-id="d9d52-177">Segment 2</span><span class="sxs-lookup"><span data-stu-id="d9d52-177">Segment 2</span></span> | <span data-ttu-id="d9d52-178">Alfanumeriek</span><span class="sxs-lookup"><span data-stu-id="d9d52-178">Alphanumeric</span></span> | \#\#\#\# |

<span data-ttu-id="d9d52-179">**Voorbeeld van een opgemaakt nummer**: Req0052</span><span class="sxs-lookup"><span data-stu-id="d9d52-179">**Example of formatted number**: Req0052</span></span>

<span data-ttu-id="d9d52-180">Omdat het bereik **Gedeeld** is, wordt de nummerreeksnotatie in de hele organisatie gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d9d52-180">Because the scope is **Shared**, the number sequence format is used across the organization.</span></span> <span data-ttu-id="d9d52-181">U kunt geen verschillende nummerreeksnotaties instellen voor verschillende delen van de organisatie.</span><span class="sxs-lookup"><span data-stu-id="d9d52-181">You cannot set up different number sequence formats for different parts of the organization.</span></span>

## <a name="performance-considerations-for-number-sequences"></a><span data-ttu-id="d9d52-182">Prestatieoverwegingen voor nummerreeksen</span><span class="sxs-lookup"><span data-stu-id="d9d52-182">Performance considerations for number sequences</span></span>

<span data-ttu-id="d9d52-183">Bekijk de volgende gegevens over hoe de configuratie van nummerreeksen de systeemprestaties kan beïnvloeden voordat u nummerreeksen instelt.</span><span class="sxs-lookup"><span data-stu-id="d9d52-183">Consider the following information about how the configuration of number sequences can affect system performance before you set up number sequences.</span></span>

### <a name="continuous-and-non-continuous-number-sequences"></a><span data-ttu-id="d9d52-184">Doorlopende en niet-doorlopende nummerreeksen</span><span class="sxs-lookup"><span data-stu-id="d9d52-184">Continuous and non-continuous number sequences</span></span>

<span data-ttu-id="d9d52-185">Nummerreeksen kunnen doorlopend of niet-doorlopend zijn.</span><span class="sxs-lookup"><span data-stu-id="d9d52-185">Number sequences can be continuous or non-continuous.</span></span> <span data-ttu-id="d9d52-186">Een doorlopende nummerreeks slaat geen nummers over, maar de nummers mogen niet opeenvolgend worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d9d52-186">A continuous number sequence does not skip any numbers, but numbers may not be used sequentially.</span></span> <span data-ttu-id="d9d52-187">Nummers van een niet-doorlopende nummerreeks worden opeenvolgend gebruikt, maar de nummerreeks kan nummers overslaan.</span><span class="sxs-lookup"><span data-stu-id="d9d52-187">Numbers from a non-continuous number sequence are used sequentially, but the number sequence may skip numbers.</span></span> <span data-ttu-id="d9d52-188">Als een gebruiker bijvoorbeeld een transactie annuleert, wordt een nummer gegenereerd, maar niet gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d9d52-188">For example, if a user cancels a transaction, a number is generated, but not used.</span></span> <span data-ttu-id="d9d52-189">In een doorlopende nummerreeks, wordt dat nummer later opnieuw gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d9d52-189">In a continuous number sequence, that number is recycled later.</span></span> <span data-ttu-id="d9d52-190">In een niet-doorlopende nummerreeks, wordt het nummer niet gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d9d52-190">In a non-continuous number sequence, the number is not used.</span></span>

<span data-ttu-id="d9d52-191">Doorlopende nummerreeksen zijn normaal gezien vereist voor externe documenten, zoals inkooporders, verkooporders en facturen.</span><span class="sxs-lookup"><span data-stu-id="d9d52-191">Continuous number sequences are typically required for external documents, such as purchase orders, sales orders, and invoices.</span></span> <span data-ttu-id="d9d52-192">Doorlopende nummerreeksen kunnen de reactietijden van het systeem nadelig beïnvloeden, maar het systeem moet een nummer aanvragen bij de database telkens als een nieuw document of registratie wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d9d52-192">However, continuous number sequences can adversely affect system response times because the system must request a number from the database every time that a new document or record is created.</span></span>

<span data-ttu-id="d9d52-193">Als u een niet-doorlopende nummerreeks gebruikt, kunt u **Voorafgaande toewijzing** inschakelen op het sneltabblad **Prestaties** op de pagina **Nummerreeksen**.</span><span class="sxs-lookup"><span data-stu-id="d9d52-193">If you use a non-continuous number sequence, you can enable **Preallocation** on the **Performance** FastTab of the **Number sequences** page.</span></span> <span data-ttu-id="d9d52-194">Wanneer u een hoeveelheid nummers opgeeft om vooraf toe te wijzen, selecteert het systeem die nummers en bewaart het ze in het geheugen.</span><span class="sxs-lookup"><span data-stu-id="d9d52-194">When you specify a quantity of numbers to preallocate, the system selects those numbers and stores them in memory.</span></span> <span data-ttu-id="d9d52-195">Nieuwe nummers worden alleen bij de database opgevraagd nadat de vooraf toegewezen hoeveelheid is gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d9d52-195">New numbers are requested from the database only after the preallocated quantity has been used.</span></span>

<span data-ttu-id="d9d52-196">Tenzij er een regelgevende vereiste is die doorlopende nummerreeksen gebruikt, bevelen we u aan om niet-doorlopende nummerreeksen te gebruiken voor betere prestaties.</span><span class="sxs-lookup"><span data-stu-id="d9d52-196">Unless there is a regulatory requirement that you use continuous number sequences, we recommend that you use non-continuous number sequences for better performance.</span></span>

### <a name="automatic-cleanup-of-number-sequences"></a><span data-ttu-id="d9d52-197">Automatische opschoning van nummerreeksen</span><span class="sxs-lookup"><span data-stu-id="d9d52-197">Automatic cleanup of number sequences</span></span>

<span data-ttu-id="d9d52-198">Bij een stroomuitval, een toepassingsfout of andere onverwachte storting, kan het systeem nummers niet automatisch opnieuw gebruiken voor doorlopende nummerreeksen.</span><span class="sxs-lookup"><span data-stu-id="d9d52-198">In case of a power failure, an application error, or other unexpected failure, the system cannot recycle numbers automatically for continuous number sequences.</span></span> <span data-ttu-id="d9d52-199">U kunt het opschoonproces handmatig of automatisch uitvoeren om de verloren nummers te herstellen.</span><span class="sxs-lookup"><span data-stu-id="d9d52-199">You can run the cleanup process manually or automatically to recover the lost numbers.</span></span>

<span data-ttu-id="d9d52-200">Overweeg zorgvuldig het servergebruik wanneer u het opschoonproces plant.</span><span class="sxs-lookup"><span data-stu-id="d9d52-200">Carefully consider server usage when you plan the cleanup process.</span></span> <span data-ttu-id="d9d52-201">Het is aan te raden het opschonen als batchtaak uit te voeren tijdens de daluren.</span><span class="sxs-lookup"><span data-stu-id="d9d52-201">We recommend that you perform the cleanup as a batch job during non-peak hours.</span></span>