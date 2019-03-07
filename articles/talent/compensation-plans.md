---
title: Compensatieplannen
description: Managers Compensatie en emolumenten kunnen Compensatiebeheer gebruiken om plannen voor vaste en variabele compensatie voor de werknemers van de organisatie te beheren en te verwerken.
author: kherr75
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCompensationLevel, HRCCompGrid, HRMCompFixedAction, HRMCompFixedBudget, HRMCompFixedPlanTable
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: e80b3ebc9c374073ff5a2dfc8c2acf1d7f6c6287
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "303875"
---
# <a name="compensation-plans"></a><span data-ttu-id="06a0f-103">Compensatieplannen</span><span class="sxs-lookup"><span data-stu-id="06a0f-103">Compensation plans</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="06a0f-104">Managers Compensatie en emolumenten kunnen Compensatiebeheer gebruiken om plannen voor vaste en variabele compensatie voor de werknemers van de organisatie te beheren en te verwerken.</span><span class="sxs-lookup"><span data-stu-id="06a0f-104">Compensation and Benefits Managers can use Compensation management to maintain and process fixed and variable compensation plans for the organization's employees.</span></span>

### <a name="introduction"></a><span data-ttu-id="06a0f-105">Introductie</span><span class="sxs-lookup"><span data-stu-id="06a0f-105">Introduction</span></span>

<span data-ttu-id="06a0f-106">Compensatiebeheer wordt gebruikt om de betaling van basisloon en beloningen te beheren.</span><span class="sxs-lookup"><span data-stu-id="06a0f-106">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="06a0f-107">Het vaste basissalaris en verdiensteverhogingen van een werknemer worden via vaste compensatieplannen beheerd.</span><span class="sxs-lookup"><span data-stu-id="06a0f-107">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="06a0f-108">De betaling van prestatiebeloningen, zoals bonusbetalingen, beloningen voor prestaties, aandelenopties, en subsidies en ook eenmalige beloningen, worden gecontroleerd door middel van plannen voor variabele compensatie.</span><span class="sxs-lookup"><span data-stu-id="06a0f-108">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span> 

<span data-ttu-id="06a0f-109">Werknemers kunnen aangemeld zijn voor een of meer plannen van beide typen.</span><span class="sxs-lookup"><span data-stu-id="06a0f-109">Employees can be enrolled in one or more plans of both types.</span></span> <span data-ttu-id="06a0f-110">Een werknemer moet voldoen aan de volgende eisen om in aanmerking te komen voor inschrijving bij een compensatieplan:</span><span class="sxs-lookup"><span data-stu-id="06a0f-110">An employee must meet the following requirements in order to be eligible for enrollment in a compensation plan:</span></span>
-   <span data-ttu-id="06a0f-111">De werknemer moet zijn toegewezen aan een actieve functie.</span><span class="sxs-lookup"><span data-stu-id="06a0f-111">The employee must have an active position assignment.</span></span>
-   <span data-ttu-id="06a0f-112">De werknemer moet voldoen aan de criteria die zijn opgesteld om in aanmerking te komen voor een compensatieplan.</span><span class="sxs-lookup"><span data-stu-id="06a0f-112">The employee must meet the criteria that are defined by eligibility rules for a compensation plan.</span></span>

## <a name="compensation-setup"></a><span data-ttu-id="06a0f-113">Instellen van compensatie</span><span class="sxs-lookup"><span data-stu-id="06a0f-113">Compensation setup</span></span>
<span data-ttu-id="06a0f-114">De volgende tabel geeft een overzicht van de onderdelen van het compensatieproces dat geïntegreerd kan worden bij het instellen van de compensatieplannen van uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="06a0f-114">The following table lists components of the compensation process that can be integral in setting up your company's compensation plans.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="06a0f-115">Onderdeel</span><span class="sxs-lookup"><span data-stu-id="06a0f-115">Component</span></span></th>
<th><span data-ttu-id="06a0f-116">Meer informatie...</span><span class="sxs-lookup"><span data-stu-id="06a0f-116">More information…</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="06a0f-117">Vastecompensatieacties</span><span class="sxs-lookup"><span data-stu-id="06a0f-117">Fixed compensation actions</span></span></td>
<td><span data-ttu-id="06a0f-118">Acties voor vaste compensatie hebben twee doelen:</span><span class="sxs-lookup"><span data-stu-id="06a0f-118">Fixed compensation actions accomplish two purposes:</span></span>
<ul>
<li><span data-ttu-id="06a0f-119">Acties kunnen het type informatie opgeven dat moet worden geregistreerd wanneer de compensatie van een werknemer wordt gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="06a0f-119">Actions can specify the kind of information that must be recorded when an employee’s compensation changes.</span></span> <span data-ttu-id="06a0f-120">U kunt bijvoorbeeld vereisen dat de reden van een wijziging, zoals een promotie of demotie, wordt geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="06a0f-120">For example, you can require that the reason a change, such as a promotion or a demotion be recorded.</span></span></li>
<li><span data-ttu-id="06a0f-121">Acties kunnen ervoor zorgen dat een berekening wordt toegepast wanneer vaste compensatieplannen worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="06a0f-121">Actions can ensure that a calculation is applied when fixed compensation plans are processed.</span></span>  <span data-ttu-id="06a0f-122">Acties van het type Eigen vermogen vergelijken bijvoorbeeld de betaling voor de werknemer met het minimumreferentiepunt voor het niveau van de werknemer en zorgen ervoor dat de werknemer minstens het minimumbedrag krijgt betaald.</span><span class="sxs-lookup"><span data-stu-id="06a0f-122">For example, actions of type Equity will compare the employees pay to the minimum reference point for the level on the employee&#39;s and ensure the employee is getting paid at least the minimum.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06a0f-123">Niveaus</span><span class="sxs-lookup"><span data-stu-id="06a0f-123">Levels</span></span></td>
<td><span data-ttu-id="06a0f-124">Niveaus worden gekoppeld aan taken en eventuele functies die zijn gerelateerd aan een taakverwijzing.</span><span class="sxs-lookup"><span data-stu-id="06a0f-124">Levels are associated with jobs and any positions that are related to a job reference.</span></span> <span data-ttu-id="06a0f-125">U kunt afzonderlijke niveaus voor de drie typen compensatieplannen maken: schaal, schijf en stap.</span><span class="sxs-lookup"><span data-stu-id="06a0f-125">You can create discrete levels for the three types of compensation plans: Grade, Band, and Step.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06a0f-126">Bereikgebruiksmatrix</span><span class="sxs-lookup"><span data-stu-id="06a0f-126">Range utilization matrix</span></span></td>
<td><span data-ttu-id="06a0f-127">Een bereikgebruiksmatrix ondersteunt bij de overgang van werknemers naar het besturingspunt voor hun taken.</span><span class="sxs-lookup"><span data-stu-id="06a0f-127">A range utilization matrix helps you transition employees to the control point for their jobs.</span></span> <span data-ttu-id="06a0f-128">Via bereikgebruik kunt u ook het loontariefvermogen in het bedrijf beheren, ongeacht de prestaties van een afzonderlijke werknemer of de algehele prestaties van het bedrijf.</span><span class="sxs-lookup"><span data-stu-id="06a0f-128">You can also use range utilization to control pay rate equity in the company without regard to an individual employee&#39;s performance or the overall performance of the company.</span></span> <span data-ttu-id="06a0f-129">Werknemers die bijvoorbeeld lager worden betaald binnen hun bereik ontvangen een hogere procentuele toename dan werknemers die hoger in het bereik worden betaald.</span><span class="sxs-lookup"><span data-stu-id="06a0f-129">For example, employees who are paid lower in their range get higher percentage increases than employees who are paid higher in the range.</span></span> <span data-ttu-id="06a0f-130">Op deze manier kunt u systematisch vermogensverschillen compenseren.</span><span class="sxs-lookup"><span data-stu-id="06a0f-130">In this manner, you can systematically offset equity differences.</span></span> <span data-ttu-id="06a0f-131">Het bereikgebruik wordt als volgt berekend: (tarief vast salaris - bereik, Minimum) ÷ (bereik Maximum - bereik, Minimum).</span><span class="sxs-lookup"><span data-stu-id="06a0f-131">The range utilization is calculated as follows: (Fixed Pay Rate - Range Minimum) ÷ (Range Maximum - Range Minimum).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06a0f-132">Referentiepuntinstellingen</span><span class="sxs-lookup"><span data-stu-id="06a0f-132">Reference point setups</span></span></td>
<td><span data-ttu-id="06a0f-133">Referentiepuntinstellingen zijn inclusief een aantal referentiepunten die bereikwaarden in een matrix weergeven.</span><span class="sxs-lookup"><span data-stu-id="06a0f-133">A reference point setup includes a set of reference points that represent ranges in a matrix.</span></span> <span data-ttu-id="06a0f-134">Elk bereik kan worden gekoppeld aan een betalingstarief.</span><span class="sxs-lookup"><span data-stu-id="06a0f-134">Each range can be associated with a pay rate.</span></span> <span data-ttu-id="06a0f-135">Schaalplannen hebben bijvoorbeeld vaak referentiepunten zoals Minimum, Middelpunt en Maximum.</span><span class="sxs-lookup"><span data-stu-id="06a0f-135">For example, grade plans will often have reference points of Minimum, Midpoint, and Maximum.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06a0f-136">Compensatiematrix</span><span class="sxs-lookup"><span data-stu-id="06a0f-136">Compensation matrix</span></span></td>
<td><span data-ttu-id="06a0f-137">Een compensatiematrix is de set van referentiepunten en niveaus die u kunt gebruiken om een compensatiestructuur te maken.</span><span class="sxs-lookup"><span data-stu-id="06a0f-137">A compensation matrix is the set of reference points and levels that you use to create a compensation structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06a0f-138">Compensatiestructuur</span><span class="sxs-lookup"><span data-stu-id="06a0f-138">Compensation structure</span></span></td>
<td><span data-ttu-id="06a0f-139">Een compensatiestructuur is een compensatiematrix waarin loontarieven zijn gekoppeld de referentiepunten voor elk niveau.</span><span class="sxs-lookup"><span data-stu-id="06a0f-139">A compensation structure is a compensation matrix that has pay rates associated with the reference points for each level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06a0f-140">Geschiktheidsregels</span><span class="sxs-lookup"><span data-stu-id="06a0f-140">Eligibility rules</span></span></td>
<td><span data-ttu-id="06a0f-141">Er worden geschiktheidsregels toegepast voor het identificeren van werknemers in specifieke taken, taakfuncties, taaktypen, afdelingen, vakbonden of compensatiegebieden waarvoor specifieke compensatieplannen gelden.</span><span class="sxs-lookup"><span data-stu-id="06a0f-141">Eligibility rules are used to identify employees in specific jobs, job functions, job types, departments, labor unions, or compensation regions that are covered by specific compensation plans.</span></span> <span data-ttu-id="06a0f-142">U moet geschiktheidsregels voor plannen voor zowel variabele als vaste compensatie maken, om werknemers in een plan in te schrijven.</span><span class="sxs-lookup"><span data-stu-id="06a0f-142">You must create eligibility rules for both variable and fixed compensation plans in order to enroll employees in the plan.</span></span> <span data-ttu-id="06a0f-143">Nadat u de geschiktheidsregels voor een compensatieplan hebt opgegeven, kunt u de niveaus definiëren die moeten worden gehanteerd voor de taken waarop het plan betrekking heeft.</span><span class="sxs-lookup"><span data-stu-id="06a0f-143">After eligibility rules are specified for a compensation plan, you can define the levels that should apply to the jobs that are covered by the plan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06a0f-144">Betalingsfrequenties</span><span class="sxs-lookup"><span data-stu-id="06a0f-144">Pay frequencies</span></span></td>
<td><span data-ttu-id="06a0f-145">Betalingsfrequenties worden gebruikt om de periode te definiëren waarvoor de compensatie is vastgelegd.</span><span class="sxs-lookup"><span data-stu-id="06a0f-145">Pay frequencies are used to define the time period for which the compensation is specified.</span></span>  <span data-ttu-id="06a0f-146">De betalingsfrequentie helpt u bijvoorbeeld inzicht te krijgen als het compensatiebedrag is opgegeven als een jaarsalaris versus een uurtarief.</span><span class="sxs-lookup"><span data-stu-id="06a0f-146">For example, the pay frequency helps you understand if the compensation amount is specified as an annual salary versus an hourly pay rate.</span></span> <span data-ttu-id="06a0f-147">Betalingsfrequenties worden ook gebruikt voor het instellen van conversiefactoren om compensatiebedragen van maandelijks, wekelijks, tweewekelijks en per uur te converteren naar jaarlijkse frequentie.</span><span class="sxs-lookup"><span data-stu-id="06a0f-147">Pay frequencies are also used to set up conversion factors to convert compensation amounts from monthly, weekly, biweekly and hourly pay frequencies to an annual pay frequency.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06a0f-148">Compensatieregio's</span><span class="sxs-lookup"><span data-stu-id="06a0f-148">Compensation regions</span></span></td>
<td><span data-ttu-id="06a0f-149">Compensatieregio's worden gebruikt voor het aangeven van werknemerscompensatie op basis van de locatie van de werkplek.</span><span class="sxs-lookup"><span data-stu-id="06a0f-149">Compensation regions are used to specify employee compensation based on the location of the workplace.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06a0f-150">Controlepunt</span><span class="sxs-lookup"><span data-stu-id="06a0f-150">Control point</span></span></td>
<td><span data-ttu-id="06a0f-151">Met het controlepunt geeft u het optimale loontarief aan voor alle werknemers op een bepaald compensatieniveau.</span><span class="sxs-lookup"><span data-stu-id="06a0f-151">The control point defines what you consider to be the ideal pay rate for all employees at a compensation level.</span></span> <span data-ttu-id="06a0f-152">Voor salarisschaalstructuren zijn controlepunten meestal het midden van het bereik.</span><span class="sxs-lookup"><span data-stu-id="06a0f-152">For grade plan structures, control points are typically the midpoint of the ranges.</span></span> <span data-ttu-id="06a0f-153">Bandstructuren maken zelden gebruik van besturingspunten.</span><span class="sxs-lookup"><span data-stu-id="06a0f-153">Band structures rarely use control points.</span></span> <span data-ttu-id="06a0f-154">U kunt het controlepunt van een plan voor vaste compensatie opgeven in het formulier Vastecompensatieplannen.</span><span class="sxs-lookup"><span data-stu-id="06a0f-154">You can specify the control point for a fixed compensation plan in the Fixed compensation plans form.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06a0f-155">Taakfuncties</span><span class="sxs-lookup"><span data-stu-id="06a0f-155">Job functions</span></span></td>
<td><span data-ttu-id="06a0f-156">Taakfuncties worden gebruikt om compensatieplannen te classificeren en te filteren voor specifieke taken.</span><span class="sxs-lookup"><span data-stu-id="06a0f-156">Job functions are used to classify and filter compensation plans to specific jobs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06a0f-157">Taaktypen</span><span class="sxs-lookup"><span data-stu-id="06a0f-157">Job types</span></span></td>
<td><span data-ttu-id="06a0f-158">Taakfuncties worden gebruikt om compensatieplannen te classificeren en te filteren voor specifieke taken.</span><span class="sxs-lookup"><span data-stu-id="06a0f-158">Job types are used to classify and filter compensation plans to specific jobs.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06a0f-159">Variabelecompensatietypen</span><span class="sxs-lookup"><span data-stu-id="06a0f-159">Variable compensation types</span></span></td>
<td><span data-ttu-id="06a0f-160">Variabele compensatietypen, zoals beloningen in aandelen of bonussen in contant geld, worden ingesteld in variabele compensatieplannen.</span><span class="sxs-lookup"><span data-stu-id="06a0f-160">Variable compensation types, such as stock awards or cash award bonuses, are set up in variable compensation plans.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06a0f-161">Compensatierasters</span><span class="sxs-lookup"><span data-stu-id="06a0f-161">Compensation grids</span></span></td>
<td><span data-ttu-id="06a0f-162">Compensatierasters bevatten de compensatiestructuur.</span><span class="sxs-lookup"><span data-stu-id="06a0f-162">Compensation grids contain the compensation structure.</span></span>  <span data-ttu-id="06a0f-163">Compensatierasters kunnen worden gebruikt door een of meer compensatieplannen.</span><span class="sxs-lookup"><span data-stu-id="06a0f-163">Compensation grids can be used by one or more compensation plans.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06a0f-164">Prestatieplannen</span><span class="sxs-lookup"><span data-stu-id="06a0f-164">Performance plans</span></span></td>
<td><span data-ttu-id="06a0f-165">Prestatieplannen worden gebruikt voor het koppelen van prestatie aan een toewijzingsmatrix, zodat u het plan kunt gebruiken bij de strategie van prestatieloon.</span><span class="sxs-lookup"><span data-stu-id="06a0f-165">Performance plans are used to associate performance with an allocation matrix, so that you can use the plan in a pay-for-performance strategy.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06a0f-166">Prestatieclassificaties</span><span class="sxs-lookup"><span data-stu-id="06a0f-166">Performance ratings</span></span></td>
<td><span data-ttu-id="06a0f-167">Prestatieclassificaties worden in compensatieplannen gebruikt om het bedrag van een verdienstebeloning of prestatiebeloning vast te stellen.</span><span class="sxs-lookup"><span data-stu-id="06a0f-167">Performance ratings are used in performance plans to determine the amount of a merit award or performance award.</span></span></td>
</tr>
</tbody>
</table>

## <a name="process-events"></a><span data-ttu-id="06a0f-168">Procesgebeurtenissen</span><span class="sxs-lookup"><span data-stu-id="06a0f-168">Process events</span></span>
<span data-ttu-id="06a0f-169">Een procesgebeurtenis berekent compensatiegegevens voor een bepaalde periode voor alle werknemers die zijn ingeschreven in een of meer vaste of variabele compensatieplannen.</span><span class="sxs-lookup"><span data-stu-id="06a0f-169">A process event calculates compensation information for a specific period for all employees who are enrolled in one or more fixed or variable compensation plans.</span></span> <span data-ttu-id="06a0f-170">U kunt een procesgebeurtenis herhaaldelijk uitvoeren om de berekende compensatieresultaten te testen of bij te werken.</span><span class="sxs-lookup"><span data-stu-id="06a0f-170">You can run a process event repeatedly to test or update calculated compensation results.</span></span>

<a name="compensation-events"></a><span data-ttu-id="06a0f-171">Compensatiegebeurtenissen</span><span class="sxs-lookup"><span data-stu-id="06a0f-171">Compensation events</span></span>
-------------------

<span data-ttu-id="06a0f-172">Telkens wanneer een procesgebeurtenis wordt uitgevoerd, wordt een compensatiegebeurtenis gemaakt.</span><span class="sxs-lookup"><span data-stu-id="06a0f-172">Each time a process event is run, a compensation event is created.</span></span>  <span data-ttu-id="06a0f-173">Compensatiegebeurtenissen bevatten de resultaten van het compensatieproces voor elke werknemer die is opgenomen in deze procesgebeurtenis.</span><span class="sxs-lookup"><span data-stu-id="06a0f-173">Compensation events contain the results of the compensation process for each employee included in that process event.</span></span>  <span data-ttu-id="06a0f-174">Wanneer de berekeningen juist zijn, kunt u de compensatiegebeurtenis laden om de compensatierecords bij te werken voor de werknemers op wie de procesgebeurtenis van invloed is.</span><span class="sxs-lookup"><span data-stu-id="06a0f-174">When the calculations are correct, you can load the compensation event to update the compensation records for the employees who are affected by the process event.</span></span>

## <a name="recommendations"></a><span data-ttu-id="06a0f-175">Aanbevelingen</span><span class="sxs-lookup"><span data-stu-id="06a0f-175">Recommendations</span></span>
<span data-ttu-id="06a0f-176">Nadat u een procesgebeurtenis uitvoert, kunt u aanbevelingen doen voor aanpassingen aan de toename van de verdiensten van een werknemer of een toekenningsbedrag op basis van de berekende richtlijnen van de procesgebeurtenis.</span><span class="sxs-lookup"><span data-stu-id="06a0f-176">After you run a process event, you can recommend adjustments to an employee’s merit increase or award amount, based on the calculated guidelines of the process event.</span></span> <span data-ttu-id="06a0f-177">Als u aanbevelingen voor werknemers wilt doen, moet u aanbevelingen inschakelen wanneer u compensatieplannen instelt of wanneer u de procesgebeurtenis instelt.</span><span class="sxs-lookup"><span data-stu-id="06a0f-177">To make recommendations for employees, you must enable recommendations when you set up compensation plans or when you set up the process event.</span></span>



