---
title: Onkostenbeheer configureren
description: In dit artikel worden de overwegingen en de beslissingen beschreven die u tijdens het planningsproces moet maken voordat u Onkostenbeheer configureert in Microsoft Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 57a7cf4f6e6aaebd5d2a0ade84e0e9399e9086e1
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187516"
---
# <a name="configure-expense-management"></a><span data-ttu-id="320a4-103">Onkostenbeheer configureren</span><span class="sxs-lookup"><span data-stu-id="320a4-103">Configure expense management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="320a4-104">In dit onderwerp worden de overwegingen en de beslissingen beschreven die u tijdens het planningsproces moet maken voordat u Onkostenbeheer configureert.</span><span class="sxs-lookup"><span data-stu-id="320a4-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management.</span></span> <span data-ttu-id="320a4-105">In Onkostenbeheer kunt u onder andere informatie over betalingsmethoden, reisaanvragen, onkostennota's en beleid opslaan.</span><span class="sxs-lookup"><span data-stu-id="320a4-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="320a4-106">Omdat veel van de beslissingen die u neemt wanneer u uw configuratie voor Onkostenbeheer plant, zijn gebaseerd op de hiërarchie en financiële structuur van uw organisatie, moet u naar de planningsdocumenten voor die gebieden verwijzen.</span><span class="sxs-lookup"><span data-stu-id="320a4-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="320a4-107">Intercompany-onkosten</span><span class="sxs-lookup"><span data-stu-id="320a4-107">Intercompany expenses</span></span>

<span data-ttu-id="320a4-108">Wanneer u intercompany-onkosten inschakelt, stelt u rechtspersonen en werknemers in staat onkosten te maken namens een andere rechtspersoon en te innen van de rechtspersoon in uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="320a4-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="320a4-109">Bijvoorbeeld: een werknemer in rechtspersoon A voltooit een project voor rechtspersoon B en maakt voor het project reisgerelateerde onkosten.</span><span class="sxs-lookup"><span data-stu-id="320a4-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="320a4-110">Als Intercompany-onkosten zijn ingeschakeld, kan de werknemer vervolgens een onkostennota indienen om de onkosten te boeken naar rechtspersoon B. De onkosten moeten in dat geval worden betaald door rechtspersoon A. Als uw organisatie niet meerdere rechtspersonen omvat, hoeft u intercompany-onkosten niet in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="320a4-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="320a4-111">**Beslissing:** wilt u intercompany-onkosten inschakelen?</span><span class="sxs-lookup"><span data-stu-id="320a4-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="320a4-112">Financieel beheer</span><span class="sxs-lookup"><span data-stu-id="320a4-112">Financial management</span></span>

<span data-ttu-id="320a4-113">Onkostenbeheer is sterk geïntegreerd met het financieel beheer van uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="320a4-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="320a4-114">Veel van uw configuraties voor Onkostenbeheer zijn gebaseerd op de beslissingen die u over de financiën van uw organisatie hebt genomen.</span><span class="sxs-lookup"><span data-stu-id="320a4-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="320a4-115">In de volgende secties worden de verschillende gebieden beschreven waarvoor planning en beslissingen vereist zijn, gebaseerd op de financiële beslissingen van uw organisatie en de richtlijnen van uw managementteam.</span><span class="sxs-lookup"><span data-stu-id="320a4-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="320a4-116">Dagvergoedingen</span><span class="sxs-lookup"><span data-stu-id="320a4-116">Per diems</span></span>

<span data-ttu-id="320a4-117">U moet de dagvergoeding per werknemer definiëren die uw organisatie biedt.</span><span class="sxs-lookup"><span data-stu-id="320a4-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="320a4-118">Omdat dagvergoedingen doorgaan worden gebruikt om onkosten, zoals maaltijden, overnachtingen en andere incidentele kosten, te dekken, kunt u regels maken voor de dagvergoeding die uw organisatie aanbiedt.</span><span class="sxs-lookup"><span data-stu-id="320a4-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="320a4-119">De dagvergoedingstarieven kunnen worden gebaseerd op de tijd van het jaar en/of de reisbestemming.</span><span class="sxs-lookup"><span data-stu-id="320a4-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="320a4-120">Wanneer u een dagvergoedingsregel definieert, kunt u instellen dat er een percentage van een dagvergoedingstarief wordt ingehouden als een werknemer extra maaltijden of diensten ontvangt.</span><span class="sxs-lookup"><span data-stu-id="320a4-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="320a4-121">Ook kunt u dagtariefniveaus definiëren om het minimum of maximum aantal toegestane uren voor het dagvergoedingstarief op te geven dat kan worden toegepast op de reis van een werknemer.</span><span class="sxs-lookup"><span data-stu-id="320a4-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="320a4-122">**Beslissingen:**</span><span class="sxs-lookup"><span data-stu-id="320a4-122">**Decisions:**</span></span>

- <span data-ttu-id="320a4-123">Standaardregels voor dagvergoedingen voor de eerste en laatste dagen:</span><span class="sxs-lookup"><span data-stu-id="320a4-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="320a4-124">Wat is het minimum aantal uren dat een werknemer voor een dag kan claimen als deze ook nog een dagvergoeding wil ontvangen?</span><span class="sxs-lookup"><span data-stu-id="320a4-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="320a4-125">Geldt er een reductie voor het bedrag dat voor maaltijden wordt aangeboden voor de eerste en laatste dag?</span><span class="sxs-lookup"><span data-stu-id="320a4-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="320a4-126">Wat is het percentage van de reductie, indien van toepassing?</span><span class="sxs-lookup"><span data-stu-id="320a4-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="320a4-127">Geldt er een reductie voor het bedrag dat voor een hotel wordt aangeboden voor de eerste en laatste dag?</span><span class="sxs-lookup"><span data-stu-id="320a4-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="320a4-128">Wat is het percentage van de reductie, indien van toepassing?</span><span class="sxs-lookup"><span data-stu-id="320a4-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="320a4-129">Geldt er een reductie voor het bedrag dat voor overige gemaakte onkosten wordt aangeboden voor de eerste en laatste dag?</span><span class="sxs-lookup"><span data-stu-id="320a4-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="320a4-130">Wat is het percentage van de reductie, indien van toepassing?</span><span class="sxs-lookup"><span data-stu-id="320a4-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="320a4-131">Standaardregels voor dagvergoedingen:</span><span class="sxs-lookup"><span data-stu-id="320a4-131">Default per diem rules:</span></span>

    - <span data-ttu-id="320a4-132">Geldt er een percentagereductie voor de dagvergoeding voor elke maaltijd als de maaltijd bijvoorbeeld gratis is?</span><span class="sxs-lookup"><span data-stu-id="320a4-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="320a4-133">Wat is het reductiepercentage voor elke maaltijd, indien van toepassing?</span><span class="sxs-lookup"><span data-stu-id="320a4-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="320a4-134">Wordt de maaltijdreductie berekend per dag, reis of het aantal maaltijden per dag?</span><span class="sxs-lookup"><span data-stu-id="320a4-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="320a4-135">Moeten per diem-vergoedingen op de normale wijze of naar boven afgerond worden?</span><span class="sxs-lookup"><span data-stu-id="320a4-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="320a4-136">Worden dagvergoedingen berekend op basis van een periode van 24 uur of op een kalenderdag?</span><span class="sxs-lookup"><span data-stu-id="320a4-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="320a4-137">Per diem-regels op basis van locatie:</span><span class="sxs-lookup"><span data-stu-id="320a4-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="320a4-138">Variëren per diem-tarieven per locatie?</span><span class="sxs-lookup"><span data-stu-id="320a4-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="320a4-139">Welke locaties zijn inbegrepen?</span><span class="sxs-lookup"><span data-stu-id="320a4-139">What locations are included?</span></span>
    - <span data-ttu-id="320a4-140">Welk percentagebedrag is beschikbaar voor de volgende soorten onkosten als per diem-tarieven variëren voor elke locatie:</span><span class="sxs-lookup"><span data-stu-id="320a4-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="320a4-141">Maaltijden</span><span class="sxs-lookup"><span data-stu-id="320a4-141">Meals</span></span>
        - <span data-ttu-id="320a4-142">Hotel</span><span class="sxs-lookup"><span data-stu-id="320a4-142">Hotel</span></span>
        - <span data-ttu-id="320a4-143">Overige uitgaven</span><span class="sxs-lookup"><span data-stu-id="320a4-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="320a4-144">Journalen en rekeningen voor onkostenbeheer</span><span class="sxs-lookup"><span data-stu-id="320a4-144">Expense management journals and accounts</span></span>

<span data-ttu-id="320a4-145">Onkostenbeheer vereist dat u meerdere journalen en rekeningen gebruikt.</span><span class="sxs-lookup"><span data-stu-id="320a4-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="320a4-146">U moet bijvoorbeeld bepalen of voor kasvoorschotten en creditcardgeschillen dezelfde rekening moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="320a4-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="320a4-147">**Beslissingen:**</span><span class="sxs-lookup"><span data-stu-id="320a4-147">**Decisions:**</span></span>

- <span data-ttu-id="320a4-148">Naar welk grootboekjournaal worden goedgekeurde onkostennota's geboekt?</span><span class="sxs-lookup"><span data-stu-id="320a4-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="320a4-149">Welke rekening wordt gebruikt voor kasvoorschotten?</span><span class="sxs-lookup"><span data-stu-id="320a4-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="320a4-150">Moeten kasvoorschotten onmiddellijk worden geboekt?</span><span class="sxs-lookup"><span data-stu-id="320a4-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="320a4-151">Betalingsmethoden</span><span class="sxs-lookup"><span data-stu-id="320a4-151">Payment methods</span></span>

<span data-ttu-id="320a4-152">Als u werknemers toestemming geeft om onkosten namens uw bedrijf te maken, moet u de betalingsmethoden definiëren die werknemers kunnen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="320a4-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="320a4-153">U kunt werknemers bijvoorbeeld toestemming geven contant geld of een zakelijke creditcard te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="320a4-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="320a4-154">U kunt werknemers ook toestemming geven om persoonlijke creditcards te gebruiken en de werknemers vervolgens terugbetalen.</span><span class="sxs-lookup"><span data-stu-id="320a4-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="320a4-155">U moet de volgende beslissingen nemen voor elke betalingsmethode die u toestaat.</span><span class="sxs-lookup"><span data-stu-id="320a4-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="320a4-156">**Beslissingen:**</span><span class="sxs-lookup"><span data-stu-id="320a4-156">**Decisions:**</span></span>

- <span data-ttu-id="320a4-157">Welke betalingsmethoden zijn toegestaan?</span><span class="sxs-lookup"><span data-stu-id="320a4-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="320a4-158">Wie betaalt de onkosten voor de betalingsmethode?</span><span class="sxs-lookup"><span data-stu-id="320a4-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="320a4-159">Is er een soort tegenrekening?</span><span class="sxs-lookup"><span data-stu-id="320a4-159">Is there an offset account type?</span></span> <span data-ttu-id="320a4-160">Wat is het type tegenrekening, indien van toepassing?</span><span class="sxs-lookup"><span data-stu-id="320a4-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="320a4-161">Wat is de tegenrekening, indien van toepassing?</span><span class="sxs-lookup"><span data-stu-id="320a4-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="320a4-162">Kan de betalingsmethode alleen voor geïmporteerde transacties worden gebruikt als de betalingsmethode een creditcard is?</span><span class="sxs-lookup"><span data-stu-id="320a4-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="320a4-163">Onkostencategorieën en gedeelde categorieën</span><span class="sxs-lookup"><span data-stu-id="320a4-163">Expense categories and shared categories</span></span>

<span data-ttu-id="320a4-164">Wanneer werknemers een onkostennota maken, moeten alle geregistreerde onkosten aan een onkostencategorie worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="320a4-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="320a4-165">Onkostencategorieën worden afgeleid van gedeelde categorieën die door alle rechtspersonen in uw organisatie kunnen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="320a4-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="320a4-166">Deze categorieën kunnen ook in Projectbeheer en boekhouding worden gedeeld, afhankelijk van hoe uw organisatie is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="320a4-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="320a4-167">Bepaal op basis van de definitie van uw organisatie en richtlijnen van het implementatieteam of de gebruikte categorieën in Onkostenbeheer alleen in Onkostenbeheer moeten worden gebruikt of moeten worden gedeeld tussen Projectbeheer en boekhouding en Onkostenbeheer.</span><span class="sxs-lookup"><span data-stu-id="320a4-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="320a4-168">Deze categorieën kunnen tussen Project en Onkosten of Project en Productie worden gedeeld, maar niet tussen Onkosten en Productie.</span><span class="sxs-lookup"><span data-stu-id="320a4-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="320a4-169">U moet de volgende beslissingen nemen voor elke onkostencategorie.</span><span class="sxs-lookup"><span data-stu-id="320a4-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="320a4-170">**Beslissingen:**</span><span class="sxs-lookup"><span data-stu-id="320a4-170">**Decisions:**</span></span>

- <span data-ttu-id="320a4-171">Wat is de onkostencategorie?</span><span class="sxs-lookup"><span data-stu-id="320a4-171">What is the expense category?</span></span> <span data-ttu-id="320a4-172">Voorbeelden zijn categorieën voor vluchten, hotels of kilometervergoeding.</span><span class="sxs-lookup"><span data-stu-id="320a4-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="320a4-173">Kan de onkostencategorie ook worden gebruikt in Projectbeheer en boekhouding?</span><span class="sxs-lookup"><span data-stu-id="320a4-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="320a4-174">Wat is het onkostentype?</span><span class="sxs-lookup"><span data-stu-id="320a4-174">What is the expense type?</span></span>
- <span data-ttu-id="320a4-175">Wat is de standaardbetalingsmethode voor de onkostencategorie?</span><span class="sxs-lookup"><span data-stu-id="320a4-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="320a4-176">Moeten onkosten in de onkostencategorie worden gespecificeerd?</span><span class="sxs-lookup"><span data-stu-id="320a4-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="320a4-177">Wat is de belangrijkste standaardrekening voor de onkostencategorie?</span><span class="sxs-lookup"><span data-stu-id="320a4-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="320a4-178">Wat is de standaard btw-groep voor artikelen voor de onkostencategorie?</span><span class="sxs-lookup"><span data-stu-id="320a4-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="320a4-179">Zijn extra betalingsmethoden toegestaan voor de onkostencategorie?</span><span class="sxs-lookup"><span data-stu-id="320a4-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="320a4-180">Welke extra betalingsmethoden zijn toegestaan, indien van toepassing?</span><span class="sxs-lookup"><span data-stu-id="320a4-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="320a4-181">Zijn er subcategorieën in deze onkostencategorie?</span><span class="sxs-lookup"><span data-stu-id="320a4-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="320a4-182">Als er subcategorieën zijn, moet u ook de volgende beslissingen nemen:</span><span class="sxs-lookup"><span data-stu-id="320a4-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="320a4-183">Zijn er subcategorieën uitgesloten van btw-teruggave?</span><span class="sxs-lookup"><span data-stu-id="320a4-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="320a4-184">Wat is de btw-groep voor artikelen van de subcategorieën?</span><span class="sxs-lookup"><span data-stu-id="320a4-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="320a4-185">Als de onkostencategorie ook in Projectbeheer en boekhouding wordt gebruikt, moet u ook de resterende vragen beantwoorden.</span><span class="sxs-lookup"><span data-stu-id="320a4-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="320a4-186">In het andere geval kunt u doorgaan met de volgende sectie.</span><span class="sxs-lookup"><span data-stu-id="320a4-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="320a4-187">Welke kostenrekeningen worden voor de volgende onkosten gebruikt?</span><span class="sxs-lookup"><span data-stu-id="320a4-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="320a4-188">Kosten</span><span class="sxs-lookup"><span data-stu-id="320a4-188">Cost</span></span>
    - <span data-ttu-id="320a4-189">Salaristoewijzing</span><span class="sxs-lookup"><span data-stu-id="320a4-189">Payroll allocation</span></span>
    - <span data-ttu-id="320a4-190">OHW - kostprijs</span><span class="sxs-lookup"><span data-stu-id="320a4-190">WIP-cost value</span></span>
    - <span data-ttu-id="320a4-191">Kosten - artikel</span><span class="sxs-lookup"><span data-stu-id="320a4-191">Cost-item</span></span>
    - <span data-ttu-id="320a4-192">OHW - kostprijs - artikel</span><span class="sxs-lookup"><span data-stu-id="320a4-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="320a4-193">Transitorisch verlies</span><span class="sxs-lookup"><span data-stu-id="320a4-193">Accrued loss</span></span>
    - <span data-ttu-id="320a4-194">OHW - transitorisch verlies</span><span class="sxs-lookup"><span data-stu-id="320a4-194">WIP-accrued loss</span></span>

- <span data-ttu-id="320a4-195">Welke opbrengstrekeningen worden voor het volgende gebruikt?</span><span class="sxs-lookup"><span data-stu-id="320a4-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="320a4-196">Gefactureerde opbrengst</span><span class="sxs-lookup"><span data-stu-id="320a4-196">Invoiced revenue</span></span>
    - <span data-ttu-id="320a4-197">Transitorische opbrengsten - verkoopwaarde</span><span class="sxs-lookup"><span data-stu-id="320a4-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="320a4-198">OHW - verkoopwaarde</span><span class="sxs-lookup"><span data-stu-id="320a4-198">WIP-sales value</span></span>
    - <span data-ttu-id="320a4-199">Transitorische opbrengsten - productie</span><span class="sxs-lookup"><span data-stu-id="320a4-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="320a4-200">OHW - productie</span><span class="sxs-lookup"><span data-stu-id="320a4-200">WIP-production</span></span>
    - <span data-ttu-id="320a4-201">Transitorische opbrengsten - winst</span><span class="sxs-lookup"><span data-stu-id="320a4-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="320a4-202">OHW - winst</span><span class="sxs-lookup"><span data-stu-id="320a4-202">WIP-profit</span></span>
    - <span data-ttu-id="320a4-203">Transitorische opbrengsten - abonnement</span><span class="sxs-lookup"><span data-stu-id="320a4-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="320a4-204">OHW - abonnement</span><span class="sxs-lookup"><span data-stu-id="320a4-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="320a4-205">Belasting</span><span class="sxs-lookup"><span data-stu-id="320a4-205">Taxes</span></span>

<span data-ttu-id="320a4-206">Voor btw gerelateerd aan onkosten moet u bepalen wat wordt opgenomen of ingeschakeld op onkostennota's.</span><span class="sxs-lookup"><span data-stu-id="320a4-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="320a4-207">**Beslissingen:**</span><span class="sxs-lookup"><span data-stu-id="320a4-207">**Decisions:**</span></span>

- <span data-ttu-id="320a4-208">Is btw inbegrepen in de onkostenbedragen?</span><span class="sxs-lookup"><span data-stu-id="320a4-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="320a4-209">Moet btw-teruggave worden ingeschakeld voor onkosten?</span><span class="sxs-lookup"><span data-stu-id="320a4-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="320a4-210">Als u tijdens de planning van het grootboek Amerikaanse btw- en gebruiksbelastingregels hebt toegepast, kunt u btw-teruggave voor uitgaven niet inschakelen.</span><span class="sxs-lookup"><span data-stu-id="320a4-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="320a4-211">(Als u Amerikaanse btw- en gebruiksbelastingregels wilt toepassen, stelt u de optie **Belastingregels btw toepassen** in op **Ja**.)</span><span class="sxs-lookup"><span data-stu-id="320a4-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="320a4-212">Beleid</span><span class="sxs-lookup"><span data-stu-id="320a4-212">Policies</span></span>

<span data-ttu-id="320a4-213">U kunt beleid voor onkostennota's maken zodat uw organisatie tijd en geld kan besparen wanneer werknemers onkosten maken namens het bedrijf.</span><span class="sxs-lookup"><span data-stu-id="320a4-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="320a4-214">Beleid zorgt ervoor dat werknemers binnen het budget blijven, alle vereiste gegevens doorgeven en alleen waar nodig geld uitgeven.</span><span class="sxs-lookup"><span data-stu-id="320a4-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="320a4-215">U moet de volgende beslissingen nemen voor elk gemaakt beleid en goedkeuringsbeleid voor onkostennota's.</span><span class="sxs-lookup"><span data-stu-id="320a4-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="320a4-216">**Beslissingen:**</span><span class="sxs-lookup"><span data-stu-id="320a4-216">**Decisions:**</span></span>

- <span data-ttu-id="320a4-217">Wat is de naam van het beleid?</span><span class="sxs-lookup"><span data-stu-id="320a4-217">What is the name of the policy?</span></span>
- <span data-ttu-id="320a4-218">Waarvoor is het onkostenbeleid bedoeld?</span><span class="sxs-lookup"><span data-stu-id="320a4-218">What is the expense policy for?</span></span>
- <span data-ttu-id="320a4-219">Op welke bedrijven in uw organisatie is dit beleid van toepassing als u eerder hebt besloten intercompany-onkosten in te schakelen?</span><span class="sxs-lookup"><span data-stu-id="320a4-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="320a4-220">Wanneer gaat het beleid in?</span><span class="sxs-lookup"><span data-stu-id="320a4-220">When does the policy become effective?</span></span>
- <span data-ttu-id="320a4-221">Wanneer verloopt het beleid?</span><span class="sxs-lookup"><span data-stu-id="320a4-221">When does the policy expire?</span></span>
- <span data-ttu-id="320a4-222">Wat is de beleidsregel?</span><span class="sxs-lookup"><span data-stu-id="320a4-222">What is the policy rule?</span></span>
- <span data-ttu-id="320a4-223">Wat is de uitkomt van de beleidsregel?</span><span class="sxs-lookup"><span data-stu-id="320a4-223">What is the outcome of the policy rule?</span></span>
