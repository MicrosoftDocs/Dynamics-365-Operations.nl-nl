---
title: Parameters onkostenbeheer
description: De volgende parameters bepalen de werking in Onkostenbeheer.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: c1bc754b92e647f0fdac6799564273fb6ea6fb20
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177163"
---
# <a name="expense-management-parameters"></a><span data-ttu-id="0ea10-103">Parameters onkostenbeheer</span><span class="sxs-lookup"><span data-stu-id="0ea10-103">Expense management parameters</span></span>

[!include [banner](../includes/banner.md)]

-----------------------------

<span data-ttu-id="0ea10-104">De volgende parameters bepalen de algemene werking in Onkostenbeheer.</span><span class="sxs-lookup"><span data-stu-id="0ea10-104">The parameters control the general behavior in Expense management.</span></span>

### <a name="general"></a><span data-ttu-id="0ea10-105">Algemeen</span><span class="sxs-lookup"><span data-stu-id="0ea10-105">General</span></span>

| <span data-ttu-id="0ea10-106">**Veld**</span><span class="sxs-lookup"><span data-stu-id="0ea10-106">**Field**</span></span>                                                | <span data-ttu-id="0ea10-107">**Omschrijving**</span><span class="sxs-lookup"><span data-stu-id="0ea10-107">**Description**</span></span>                                                 |
|----------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="0ea10-108">**Standaardtarief van kilometervergoeding**</span><span class="sxs-lookup"><span data-stu-id="0ea10-108">**Standard rate of mileage**</span></span>                             | <span data-ttu-id="0ea10-109">Voer het terugbetalingstarief in voor kilometervergoeding.</span><span class="sxs-lookup"><span data-stu-id="0ea10-109">Enter the reimbursement rate for mileage expenses.</span></span> <span data-ttu-id="0ea10-110">Het tarief wordt vermenigvuldigd met de reisafstand die is ingevoerd op de onkostennota voor het berekenen van het vergoedingsbedrag voor de reiskosten.</span><span class="sxs-lookup"><span data-stu-id="0ea10-110">The rate will be multiplied by the mileage entered on the expense to calculate the amount reimbursed for the travel expense.</span></span>                       |
|<span data-ttu-id="0ea10-111">**Persoonlijke onkosten betaald door**</span><span class="sxs-lookup"><span data-stu-id="0ea10-111">**Personal expenses paid by**</span></span>                             | <span data-ttu-id="0ea10-112">Selecteer de persoon die verantwoordelijk is voor het betalen van creditcardtransactiebedragen die zijn gecategoriseerd als persoonlijk.</span><span class="sxs-lookup"><span data-stu-id="0ea10-112">Select who is responsible for paying any credit card transaction amounts categorized as personal.</span></span>                                                                                                     |
|<span data-ttu-id="0ea10-113">**Volledige onkostennota weergeven bij drill-back**</span><span class="sxs-lookup"><span data-stu-id="0ea10-113">**Display entire expense report on drillback**</span></span>               | <span data-ttu-id="0ea10-114">Selecteer deze optie om alle onkosten voor een onkostennota weer te geven bij het bekijken van de details van het oorspronkelijke document van een specifiek boekstuk dat is gegenereerd bij het boeken van de onkostennota.</span><span class="sxs-lookup"><span data-stu-id="0ea10-114">Select this option to display all expenses for an expense report when viewing the details of the original document for a specific voucher that was generated when the expense report was posted.</span></span>              |
|<span data-ttu-id="0ea10-115">**Pre-autorisatie voor reizen is verplicht**</span><span class="sxs-lookup"><span data-stu-id="0ea10-115">**Pre-authorization of travel is mandatory**</span></span>                 | <span data-ttu-id="0ea10-116">Selecteer deze optie om te vereisen dat een reisaanvraag moet worden ingediend en goedgekeurd voordat een werknemer een onkostennota kan indienen.</span><span class="sxs-lookup"><span data-stu-id="0ea10-116">Select this option to require that a travel requisition be submitted and approved before an employee can submit an expense report.</span></span>                                                                    |
|<span data-ttu-id="0ea10-117">**Verdelingen kunnen vóór het boeken worden bewerkt**</span><span class="sxs-lookup"><span data-stu-id="0ea10-117">**Allow editing of distributions before posting**</span></span>            | <span data-ttu-id="0ea10-118">Selecteren of de verdelingen van een onkostennota kunnen worden bewerkt voordat ze worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="0ea10-118">Select whether the distributions of an expense report can be edited prior to posting.</span></span>                                                                                                                 |
|<span data-ttu-id="0ea10-119">**Beleid onkostenbeheer evalueren**</span><span class="sxs-lookup"><span data-stu-id="0ea10-119">**Evaluate expense management policies**</span></span>                     | <span data-ttu-id="0ea10-120">Selecteer wanneer onkosten worden beoordeeld om te bepalen of er een onkostenbeleid is geschonden.</span><span class="sxs-lookup"><span data-stu-id="0ea10-120">Select when expenses are evaluated to determine if an expense policy has been violated.</span></span> <span data-ttu-id="0ea10-121">Uitgaven kunnen worden gecontroleerd op overtredingen wanneer de onkostenboeking wordt ingevoerd en opgeslagen of wanneer de onkostennota ter goedkeuring wordt ingediend.</span><span class="sxs-lookup"><span data-stu-id="0ea10-121">Expenses can be checked for violations when the expense entry is entered and saved or when the expense is submitted for approval.</span></span> <span data-ttu-id="0ea10-122">De beleidsregels voor vereiste ontvangstbewijzen worden gecontroleerd wanneer de onkostenregel wordt opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="0ea10-122">The policy rules for receipts required will be checked when the expense line is saved.</span></span>                   |
|<span data-ttu-id="0ea10-123">**Intercompany-onkostenregels toestaan**</span><span class="sxs-lookup"><span data-stu-id="0ea10-123">**Allow intercompany expense lines**</span></span>                         | <span data-ttu-id="0ea10-124">Selecteer of de invoer van onkosten voor andere rechtspersonen is toegestaan in een onkostennota.</span><span class="sxs-lookup"><span data-stu-id="0ea10-124">Select whether to allow entry of expenses for other legal entities within an expense report.</span></span>                                                                                                          |
|<span data-ttu-id="0ea10-125">**Wisselkoers bewerken toestaan voor creditcardonkosten**</span><span class="sxs-lookup"><span data-stu-id="0ea10-125">**Allow editing the exchange rate for credit card expenses**</span></span> | <span data-ttu-id="0ea10-126">Selecteer deze optie om toe te staan dat de wisselkoers voor de geïmporteerde creditcardonkosten kan worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="0ea10-126">Select this option to allow the user to edit the exchange rate for imported credit card expenses.</span></span>                                                                        |
|<span data-ttu-id="0ea10-127">**Hiërarchievelden met meerdere niveaus om weer te geven**</span><span class="sxs-lookup"><span data-stu-id="0ea10-127">**Multi-level hierarchy fields to display**</span></span>                  | <span data-ttu-id="0ea10-128">Selecteer welke fiatteurvelden moeten worden weergegeven wanneer het workflowtoewijzingstype voor het onkostenrapport is ingesteld op hiërarchie en de hiërarchieselectie is ingesteld op Goedkeuringshiërarchie met meerdere niveaus voor onkosten.</span><span class="sxs-lookup"><span data-stu-id="0ea10-128">Select which approver fields to display when the expense report workflow assignment type is set to be hierarchy and the hierarchy selection is set to use the Expense multi-level approval hierarchy.</span></span> <span data-ttu-id="0ea10-129">Wanneer de goedkeuringshiërarchie met meerdere niveaus wordt gebruikt voor workflows, worden de geselecteerde velden weergegeven en bewerkt in de onkostennota.</span><span class="sxs-lookup"><span data-stu-id="0ea10-129">When the multi-level approval hierarchy is used for workflow, the selected fields will be displayed and editable in the Expense report.</span></span> |
|<span data-ttu-id="0ea10-130">**Creditcardnummer van personeel opgeven (update juli 2017)**</span><span class="sxs-lookup"><span data-stu-id="0ea10-130">**Enter employee credit card number (July 2017 update)**</span></span>     | <span data-ttu-id="0ea10-131">Selecteer of een getal van 15 of 16 tekens kan worden ingevoerd en opgeslagen in het veld **Kaart-id** op de pagina **Creditcards** voor een werknemer.</span><span class="sxs-lookup"><span data-stu-id="0ea10-131">Select whether a 15-or 16-character number can be entered and saved in the **Card ID** field in the **Credit cards** page for an employee.</span></span>                                                                          |

### <a name="financial"></a><span data-ttu-id="0ea10-132">Financieel</span><span class="sxs-lookup"><span data-stu-id="0ea10-132">Financial</span></span>

| <span data-ttu-id="0ea10-133">**Veld**</span><span class="sxs-lookup"><span data-stu-id="0ea10-133">**Field**</span></span>                                                            | <span data-ttu-id="0ea10-134">**Omschrijving**</span><span class="sxs-lookup"><span data-stu-id="0ea10-134">**Description**</span></span>     |
|----------------------------------------------------------------------|------------------------------------|
|<span data-ttu-id="0ea10-135">**Naam dagelijks journaal grootboek**</span><span class="sxs-lookup"><span data-stu-id="0ea10-135">**Ledger daily journal name**</span></span>                                         | <span data-ttu-id="0ea10-136">Selecteer de naam van het grootboekjournaal waarnaar goedgekeurde onkostennota's worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="0ea10-136">Select the name of the ledger journal that approved expense reports are posted to.</span></span>            |
|<span data-ttu-id="0ea10-137">**Belastingterugvordering voor onkosten inschakelen**</span><span class="sxs-lookup"><span data-stu-id="0ea10-137">**Enable tax recovery from expenses**</span></span>                                  | <span data-ttu-id="0ea10-138">Selecteer deze optie om belastingteruggave voor onkosten in te schakelen voor in aanmerking komende uitgaven.</span><span class="sxs-lookup"><span data-stu-id="0ea10-138">Select this option to enable expense tax recovery for eligible expenses.</span></span> <span data-ttu-id="0ea10-139">Deze optie kan niet worden ingeschakeld als de Amerikaanse btw- en gebruiksbelastingregels zijn ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="0ea10-139">This option cannot be enabled if US sales tax and use tax rules are enabled.</span></span>      |
|<span data-ttu-id="0ea10-140">**Kasvoorschotten onmiddellijk boeken**</span><span class="sxs-lookup"><span data-stu-id="0ea10-140">**Post cash advances immediately**</span></span>                                     | <span data-ttu-id="0ea10-141">Selecteer deze optie voor het boeken van een goedgekeurd kasvoorschot wanneer het proces voor betalen en overboeken is voltooid.</span><span class="sxs-lookup"><span data-stu-id="0ea10-141">Select this option to post an approved cash advance when the process to Pay and transfer is completed.</span></span> <span data-ttu-id="0ea10-142">Als deze optie niet wordt geselecteerd, genereert het proces voor betalen en overboeken een niet-geboekt algemeen journaal.</span><span class="sxs-lookup"><span data-stu-id="0ea10-142">If this option is not selected, the Pay and transfer process will generate an unposted general journal.</span></span> |
|<span data-ttu-id="0ea10-143">**Boekingsdatum corrigeren tijdens boeken**</span><span class="sxs-lookup"><span data-stu-id="0ea10-143">**Correct accounting date during posting**</span></span>                             | <span data-ttu-id="0ea10-144">Selecteer deze optie om de boekingsdatum bij te werken wanneer onkosten worden geboekt terwijl huidige periode in de wachtstand staat of is gesloten.</span><span class="sxs-lookup"><span data-stu-id="0ea10-144">Select this option to update the accounting date when posting expenses if the current period is on hold or closed.</span></span> <span data-ttu-id="0ea10-145">De boekingsdatum wordt ingesteld op de volgende openstaande periode.</span><span class="sxs-lookup"><span data-stu-id="0ea10-145">The accounting date will be set to the next open period.</span></span>   |
|<span data-ttu-id="0ea10-146">**De groepering van transacties toestaan op basis van de standaardtegenrekening die is opgegeven in de betalingsmethode**</span><span class="sxs-lookup"><span data-stu-id="0ea10-146">**Allow grouping of transactions based on offset account specified in payment method**</span></span>      | <span data-ttu-id="0ea10-147">Selecteer deze optie om de onkostentransacties voor een onkostennota samen te vatten, op basis van de tegenrekening die is opgegeven in de betalingsmethode voor de onkosten.</span><span class="sxs-lookup"><span data-stu-id="0ea10-147">Select this option to summarize the expense transactions for an expense report, based on the offset account specified in the payment method for the expenses.</span></span>   
|<span data-ttu-id="0ea10-148">**Inclusief btw**</span><span class="sxs-lookup"><span data-stu-id="0ea10-148">**Tax included**</span></span>                                                   | <span data-ttu-id="0ea10-149">Selecteer deze optie om btw standaard op te nemen in het onkostenbedrag.</span><span class="sxs-lookup"><span data-stu-id="0ea10-149">Select this option to include sales tax in the expense amount by default.</span></span>             |
|<span data-ttu-id="0ea10-150">**Lasten vrijgeven bij sluiten van reisaanvragen**</span><span class="sxs-lookup"><span data-stu-id="0ea10-150">**Release encumbrances on closing travel requisitions**</span></span>            | <span data-ttu-id="0ea10-151">Selecteer deze optie om vorderingen vrij te geven wanneer een goedgekeurde reisaanvraag wordt gesloten.</span><span class="sxs-lookup"><span data-stu-id="0ea10-151">Select this option to release encumbered funds when an approved travel requisition is closed.</span></span>                                                                                   |
|<span data-ttu-id="0ea10-152">**Indienen van reisaanvraag toestaan bij budgetoverschrijding voor budgetregister en projectbudget**</span><span class="sxs-lookup"><span data-stu-id="0ea10-152">**Allow travel requisition submit on budget overrun for budget register and project budget**</span></span> | <span data-ttu-id="0ea10-153">Selecteer deze optie om werknemers toe te staan om reisaanvragen ter goedkeuring in te dienen die het toegestane budget in het budgetregister of het toegestane projectbudget overschrijden.</span><span class="sxs-lookup"><span data-stu-id="0ea10-153">Select this option to allow employees to submit travel requisitions for approval that exceed either the allowed budget that is set in the budget register or the allowed budget for a project.</span></span>            |
|<span data-ttu-id="0ea10-154">**Indienen van onkostennota toestaan bij budgetoverschrijding voor budgetregister en projectbudget**</span><span class="sxs-lookup"><span data-stu-id="0ea10-154">**Allow expense report submit on budget overrun for budget register and project budget**</span></span>    | <span data-ttu-id="0ea10-155">Selecteer deze optie om werknemers toe te staan om onkostennota's ter goedkeuring in te dienen die het toegestane budget in het budgetregister of het toegestane projectbudget overschrijden.</span><span class="sxs-lookup"><span data-stu-id="0ea10-155">Select this option to allow employees to submit expense reports for approval that exceed either the allowed budget that is set in the budget register or the allowed budget for a project.</span></span>                |
|<span data-ttu-id="0ea10-156">**Goedkeuren van onkostennota alleen toestaan bij budgetoverschrijding voor budgetregister**</span><span class="sxs-lookup"><span data-stu-id="0ea10-156">**Allow expense report approval on budget overrun for budget register only**</span></span>                | <span data-ttu-id="0ea10-157">Selecteer deze optie om fiatteurs toe te staan om onkostennota's goed te keuren die het toegestane budget in het budgetregister overschrijden.</span><span class="sxs-lookup"><span data-stu-id="0ea10-157">Select this option to allow approvers to approve expense reports that exceed the allowed budget that is set in the budget register.</span></span>                                                                       |

### <a name="per-diem"></a><span data-ttu-id="0ea10-158">Per diem</span><span class="sxs-lookup"><span data-stu-id="0ea10-158">Per diem</span></span>

| <span data-ttu-id="0ea10-159">**Veld**</span><span class="sxs-lookup"><span data-stu-id="0ea10-159">**Field**</span></span>                             | <span data-ttu-id="0ea10-160">**Omschrijving**</span><span class="sxs-lookup"><span data-stu-id="0ea10-160">**Description**</span></span>             |
|---------------------------------------|--------------------------------------------------------------------------------------|
|<span data-ttu-id="0ea10-161">**Minimum uren voor per diem**</span><span class="sxs-lookup"><span data-stu-id="0ea10-161">**Minimum hours for per diem**</span></span>           | <span data-ttu-id="0ea10-162">Geef het standaard minimumaantal uren op dat een werknemer moet werken op een dag om een dagvergoeding voor reiskosten te ontvangen.</span><span class="sxs-lookup"><span data-stu-id="0ea10-162">Enter the default minimum number of hours that an employee must work in a day to be eligible to receive a per diem for travel-related expenses.</span></span>  <span data-ttu-id="0ea10-163">Deze waarde wordt alleen gebruikt als standaardwaarde voor het veld Minimumaantal uren voor dagtariefniveaus.</span><span class="sxs-lookup"><span data-stu-id="0ea10-163">This value is only used as a default value for the Minimum hours field on per diem rate tiers.</span></span>                                                                                      |
|<span data-ttu-id="0ea10-164">**Percentage maaltijden**</span><span class="sxs-lookup"><span data-stu-id="0ea10-164">**Meal percent**</span></span>                          | <span data-ttu-id="0ea10-165">Voer het standaardpercentage voor de dagvergoeding voor maaltijden in dat wordt gebruikt op de eerste en laatste dag van reiskosten wanneer het veld **Maaltijdvergoeding berekenen per** is ingesteld op **Maaltijdtype per dag** of **Santal maaltijden per dag**.</span><span class="sxs-lookup"><span data-stu-id="0ea10-165">Enter the default percentage of the per diem for meals that is used on the first and last days of the travel-related expense when the **Calculate meal reduction by** field is set to either **Meal type per day** or **Number of meals per day**.</span></span> <span data-ttu-id="0ea10-166">De werkdag op de eerste en laatste dag is mogelijk korter dan een standaard werkdag.</span><span class="sxs-lookup"><span data-stu-id="0ea10-166">The work day on the first and last days may be shorter than a standard work day.</span></span> <span data-ttu-id="0ea10-167">Daarom kan het bedrag van de dagvergoeding op deze dagen verschillen van het standaardbedrag.</span><span class="sxs-lookup"><span data-stu-id="0ea10-167">Therefore, the amount of the per diem on these days may differ from the standard amount.</span></span> <span data-ttu-id="0ea10-168">Als het percentage is ingesteld op 0, wordt de aftrek van de eerste en laatste dag 0,00.</span><span class="sxs-lookup"><span data-stu-id="0ea10-168">If the percent is set to 0, then the first and last day deductions will be 0.00.</span></span> |
|<span data-ttu-id="0ea10-169">**Percentage hotel**</span><span class="sxs-lookup"><span data-stu-id="0ea10-169">**Hotel percent**</span></span>                        | <span data-ttu-id="0ea10-170">Voer het standaardpercentage per dag in voor hotelkosten dat wordt gebruikt voor de eerste en de laatste dag van de reiskosten.</span><span class="sxs-lookup"><span data-stu-id="0ea10-170">Enter the default percentage of the per diem for hotels that is used on the first and last days of the travel-related expense.</span></span> <span data-ttu-id="0ea10-171">De werkdag op de eerste en laatste dag is mogelijk korter dan een standaard werkdag.</span><span class="sxs-lookup"><span data-stu-id="0ea10-171">The work day on the first and last days may be shorter than a standard work day.</span></span> <span data-ttu-id="0ea10-172">Daarom kan het bedrag van de dagvergoeding op deze dagen verschillen van het standaardbedrag.</span><span class="sxs-lookup"><span data-stu-id="0ea10-172">Therefore, the amount of the per diem on these days may differ from the standard amount.</span></span> <span data-ttu-id="0ea10-173">Als het percentage is ingesteld op 0, wordt de aftrek van de eerste en laatste dag 0,00.</span><span class="sxs-lookup"><span data-stu-id="0ea10-173">If the percent is set to 0, then the first and last day deductions will be 0.00.</span></span>                                              |
|<span data-ttu-id="0ea10-174">**Percentage overige**</span><span class="sxs-lookup"><span data-stu-id="0ea10-174">**Other percent**</span></span>                        | <span data-ttu-id="0ea10-175">Voer het standaardpercentage per dag in voor diverse onkosten dat wordt gebruikt voor de eerste en de laatste dag van de reiskosten.</span><span class="sxs-lookup"><span data-stu-id="0ea10-175">Enter the default percentage of the per diem for miscellaneous expenses that is used on the first and last days of the travel-related expense.</span></span> <span data-ttu-id="0ea10-176">De werkdag op de eerste en laatste dag is mogelijk korter dan een standaard werkdag.</span><span class="sxs-lookup"><span data-stu-id="0ea10-176">The work day on the first and last days may be shorter than a standard work day.</span></span> <span data-ttu-id="0ea10-177">Daarom kan het bedrag van de dagvergoeding op deze dagen verschillen van het standaardbedrag.</span><span class="sxs-lookup"><span data-stu-id="0ea10-177">Therefore, the amount of the per diem on these days may differ from the standard amount.</span></span> <span data-ttu-id="0ea10-178">Als het percentage is ingesteld op 0, wordt de aftrek van de eerste en laatste dag 0,00.</span><span class="sxs-lookup"><span data-stu-id="0ea10-178">If the percent is set to 0, then the first and last day deductions will be 0.00.</span></span>                                                                                                     |
|<span data-ttu-id="0ea10-179">**Vergoeding in percentage voor ontbijt**</span><span class="sxs-lookup"><span data-stu-id="0ea10-179">**Reduction in percentage for breakfast**</span></span> | <span data-ttu-id="0ea10-180">Voer het bedrag in dat van de dagvergoeding wordt afgetrokken voor het ontbijt.</span><span class="sxs-lookup"><span data-stu-id="0ea10-180">Enter the amount that the per diem is reduced for breakfast.</span></span> <span data-ttu-id="0ea10-181">Als de prijs van het ontbijt is inbegrepen voor de werknemer, kunt u er bijvoorbeeld voor kiezen om het bedrag per dag met 10 procent te verminderen.</span><span class="sxs-lookup"><span data-stu-id="0ea10-181">For example, if an employee receives a complimentary breakfast, you may want to reduce the amount of the per diem by 10 percent.</span></span>                               |
|<span data-ttu-id="0ea10-182">**Vergoeding in percentage voor lunch**</span><span class="sxs-lookup"><span data-stu-id="0ea10-182">**Reduction in percentage for lunch**</span></span>    | <span data-ttu-id="0ea10-183">Voer het bedrag in waarmee de dagvergoeding wordt verminderd voor de lunch.</span><span class="sxs-lookup"><span data-stu-id="0ea10-183">Enter the amount that the per diem is reduced for lunch.</span></span> <span data-ttu-id="0ea10-184">Als de prijs van de lunch is inbegrepen voor de werknemer, kunt u er bijvoorbeeld voor kiezen om het bedrag per dag met 15 procent te verminderen.</span><span class="sxs-lookup"><span data-stu-id="0ea10-184">For example, if an employee receives a complimentary lunch, you may want to reduce the amount of the per diem by 15 percent.</span></span>                                       |
|<span data-ttu-id="0ea10-185">**Vergoeding in percentage voor diner**</span><span class="sxs-lookup"><span data-stu-id="0ea10-185">**Reduction in percentage for dinner**</span></span>   | <span data-ttu-id="0ea10-186">Voer het bedrag in waarmee de dagvergoeding wordt verminderd voor het diner.</span><span class="sxs-lookup"><span data-stu-id="0ea10-186">Enter the amount that the per diem is reduced for dinner.</span></span> <span data-ttu-id="0ea10-187">Als de prijs van het diner is inbegrepen voor de werknemer, kunt u er bijvoorbeeld voor kiezen om het bedrag per dag met 25 procent te verminderen.</span><span class="sxs-lookup"><span data-stu-id="0ea10-187">For example, if an employee receives a complimentary dinner, you may want to reduce the amount of the per diem by 25 percent.</span></span>                                     |
|<span data-ttu-id="0ea10-188">**Maaltijdvergoeding berekenen per**</span><span class="sxs-lookup"><span data-stu-id="0ea10-188">**Calculate meal reduction by**</span></span>         | <span data-ttu-id="0ea10-189">Selecteer hoe het systeem de dagvergoeding voor maaltijden moet berekenen door te selecteren of de vergoeding is gebaseerd op het maaltijdtype per reis of per dag, of op het toegestane aantal maaltijden per dag.</span><span class="sxs-lookup"><span data-stu-id="0ea10-189">Select how the system should calculate the per diem meal reduction by selecting if the reduction is based on the meal type per trip or per day, or if the reduction is based on the number of meals allowed per day.</span></span>|
|<span data-ttu-id="0ea10-190">**Afronding van per diem**</span><span class="sxs-lookup"><span data-stu-id="0ea10-190">**Per diem rounding**</span></span>                  | <span data-ttu-id="0ea10-191">Selecteer het type afronding dat voor de dagvergoedingen wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="0ea10-191">Select the type of rounding that is used for per diem expenses.</span></span> <span data-ttu-id="0ea10-192">Als u normale afronding selecteert, worden alle dagvergoedingen voor een bedrag van 0,50 afgerond naar 1,00 en alle dagvergoedingen voor een bedrag van minder dan 0,50 naar 0,00.</span><span class="sxs-lookup"><span data-stu-id="0ea10-192">If you select normal rounding, any per diem expense that has an amount of 0.50 is rounded up to 1.00, and any per diem expense that has an amount that is less than 0.50 is rounded down to 0.00.</span></span>                                                                                              |
|<span data-ttu-id="0ea10-193">**Berekening van per diem baseren op**</span><span class="sxs-lookup"><span data-stu-id="0ea10-193">**Base per diem calculation on**</span></span>         | <span data-ttu-id="0ea10-194">Selecteer of een dagvergoedingsbedrag is gebaseerd op een kalenderdag of een periode van 24 uur.</span><span class="sxs-lookup"><span data-stu-id="0ea10-194">Select whether a per diem amount is based on a calendar day or a 24-hour period.</span></span>       |

### <a name="fax-cover-pages"></a><span data-ttu-id="0ea10-195">Faxvoorbladen</span><span class="sxs-lookup"><span data-stu-id="0ea10-195">Fax cover pages</span></span>

| <span data-ttu-id="0ea10-196">**Veld**</span><span class="sxs-lookup"><span data-stu-id="0ea10-196">**Field**</span></span>                      | <span data-ttu-id="0ea10-197">**Omschrijving**</span><span class="sxs-lookup"><span data-stu-id="0ea10-197">**Description**</span></span>            |
|--------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="0ea10-198">**Instructies**</span><span class="sxs-lookup"><span data-stu-id="0ea10-198">**Instructions**</span></span>                   | <span data-ttu-id="0ea10-199">Voer de instructies in die werknemers moeten volgen wanneer ze een voorblad maken voor een fax die wordt gebruikt om ontvangstbewijzen te verzenden die betrekking hebben op een onkostennota.</span><span class="sxs-lookup"><span data-stu-id="0ea10-199">Enter the instructions that employees must follow when they create a cover page for a fax that is used to send receipts that are related to an expense report.</span></span> <span data-ttu-id="0ea10-200">Klik op de knop **Vertalingen** om de taalspecifieke tekst in te voeren die verschijnt op basis van de taal van de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="0ea10-200">Click the **Translations** button to enter language-specific text that will be displayed based on the user language.</span></span> |
|<span data-ttu-id="0ea10-201">**Gebruikers-id (Streepjescodegegevens)**</span><span class="sxs-lookup"><span data-stu-id="0ea10-201">**User ID (Bar code information)**</span></span> | <span data-ttu-id="0ea10-202">Selecteer deze optie om de unieke id van een werknemer op te slaan in de streepjescode op het voorblad van de fax.</span><span class="sxs-lookup"><span data-stu-id="0ea10-202">Select this option to store an employee’s unique identifier in the bar code that is used on the cover page of the fax.</span></span>                 |
|<span data-ttu-id="0ea10-203">**Streepjescode**</span><span class="sxs-lookup"><span data-stu-id="0ea10-203">**Bar code**</span></span>                      | <span data-ttu-id="0ea10-204">Selecteer de streepjescode die wordt gebruikt op het voorblad van de fax.</span><span class="sxs-lookup"><span data-stu-id="0ea10-204">Select the bar code that is used on the cover page of the fax.</span></span> <span data-ttu-id="0ea10-205">Streepjescodes 39 en 128 worden ondersteund door Onkostenbeheer.</span><span class="sxs-lookup"><span data-stu-id="0ea10-205">Bar codes 39 and 128 are supported with Expense management.</span></span>               |

### <a name="anti-corruption"></a><span data-ttu-id="0ea10-206">Anti-corruptie</span><span class="sxs-lookup"><span data-stu-id="0ea10-206">Anti-corruption</span></span>

|                 <span data-ttu-id="0ea10-207"><strong>Veld</strong></span><span class="sxs-lookup"><span data-stu-id="0ea10-207"><strong>Field</strong></span></span>                 |                                                                                                                                                                                            <span data-ttu-id="0ea10-208"><strong>Beschrijving</strong></span><span class="sxs-lookup"><span data-stu-id="0ea10-208"><strong>Description</strong></span></span>                                                                                                                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <span data-ttu-id="0ea10-209"><strong>Anti-corruptieattest weergeven</strong></span><span class="sxs-lookup"><span data-stu-id="0ea10-209"><strong>Display anti-corruption attestation</strong></span></span>  | <span data-ttu-id="0ea10-210">Selecteer deze optie om de anti-corruptietekst weer te geven wanneer een nieuwe onkostennota wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0ea10-210">Select this option to display the anti-corruption text when creating a new expense report.</span></span> <span data-ttu-id="0ea10-211">Voor bepaalde onkostencategorieën kan vervolgens worden ingeschakeld dat het anti-corruptieattest moet worden geselecteerd in de onkostennota.</span><span class="sxs-lookup"><span data-stu-id="0ea10-211">Specific expense categories can then be enabled that will require the anti-corruption attestation to be selected on the expense report.</span></span> <span data-ttu-id="0ea10-212">Bij een geschenkencategorie voor onkosten voor een overheidsfunctionaris kan bijvoorbeeld worden geëist dat de werknemer bevestigt dat de onkosten voldoen aan het bedrijfsbeleid voor overheidsfunctionarissen.</span><span class="sxs-lookup"><span data-stu-id="0ea10-212">For example, a gift category related to a government official expense may require the employee to confirm that the expense meets company policy related to government officials.</span></span> |
| <span data-ttu-id="0ea10-213"><strong>Anti-corruptiebericht voor inzender</strong></span><span class="sxs-lookup"><span data-stu-id="0ea10-213"><strong>Anti-corruption message for submitter</strong></span></span> |                                                                                             <span data-ttu-id="0ea10-214">Voer de tekst in die aan de werknemer wordt weergegeven wanneer een nieuwe onkostennota wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0ea10-214">Enter the text that will be displayed to the employee when creating a new expense report.</span></span> <span data-ttu-id="0ea10-215">Klik op de knop <strong>Vertalingen</strong> om de taalspecifieke tekst in te voeren die verschijnt op basis van de taal van de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="0ea10-215">Click the <strong>Translations</strong> button to enter language specific text that will be displayed based on the user language.</span></span>                                                                                             |
| <span data-ttu-id="0ea10-216"><strong>Anti-corruptiebericht voor fiatteur</strong></span><span class="sxs-lookup"><span data-stu-id="0ea10-216"><strong>Anti-corruption message for approver</strong></span></span>  |                                                                                             <span data-ttu-id="0ea10-217">Voer de tekst in die aan de fiatteur wordt weergegeven wanneer een nieuwe onkostennota wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0ea10-217">Enter the text that will be displayed to the approver when creating a new expense report.</span></span> <span data-ttu-id="0ea10-218">Klik op de knop <strong>Vertalingen</strong> om de taalspecifieke tekst in te voeren die verschijnt op basis van de taal van de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="0ea10-218">Click the <strong>Translations</strong> button to enter language specific text that will be displayed based on the user language.</span></span>                                                                                             |
