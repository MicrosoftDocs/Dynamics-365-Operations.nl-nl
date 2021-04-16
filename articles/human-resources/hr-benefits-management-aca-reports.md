---
title: ACA-rapporten genereren in Vergoedingenbeheer
description: In dit onderwerp wordt beschreven hoe Vergoedingenbeheer u helpt gegevens bij te houden die worden gerapporteerd met formulier 1095-B en formulier 1095-C voor het werkgeversmandaat van de Affordable Care Act (ACA).
author: andreabichsel
ms.date: 12/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: a41195ea3b52a707ce9deae38f12eb90de2ff5aa
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805797"
---
# <a name="generate-aca-reports-in-benefits-management"></a><span data-ttu-id="c9481-103">ACA-rapporten genereren in Vergoedingenbeheer</span><span class="sxs-lookup"><span data-stu-id="c9481-103">Generate ACA reports in Benefits management</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="c9481-104">Vergoedingenbeheer helpt u gegevens bij te houden die worden gerapporteerd met formulier 1095-B en formulier 1095-C voor het werkgeversmandaat van de Affordable Care Act (ACA).</span><span class="sxs-lookup"><span data-stu-id="c9481-104">Benefits management helps you track information that is reported on Form 1095-B and Form 1095-C for the Affordable Care Act (ACA) employer mandate.</span></span> <span data-ttu-id="c9481-105">Net zoals de ACA-rapportagefunctionaliteit in het oude werkgebied **Vergoedingen**, is deze functionaliteit alleen van toepassing op rechtspersonen in de Verenigde Staten.</span><span class="sxs-lookup"><span data-stu-id="c9481-105">Like the ACA reporting capability in the old **Benefits** workspace, this functionality applies only to legal entities in the United States.</span></span>

<span data-ttu-id="c9481-106">Als u deze functionaliteit wilt gebruiken, moet u eerst **Geavanceerd vergoedingenbeheer** inschakelen.</span><span class="sxs-lookup"><span data-stu-id="c9481-106">To use this functionality, you must first turn on **Advanced Benefits Management**.</span></span> <span data-ttu-id="c9481-107">Meer informatie, inclusief belangrijke voorbehouden voor Vergoedingenbeheer, vindt u in [Vergoedingenbeheer in- of uitschakelen](hr-admin-manage-features.md#enable-or-disable-benefits-management).</span><span class="sxs-lookup"><span data-stu-id="c9481-107">For more information, including important caveats about Benefits management, see [Enable or disable Benefits management](hr-admin-manage-features.md#enable-or-disable-benefits-management).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c9481-108">U kunt ACA-rapportages alleen gebruiken vanuit het werkgebied **Vergoedingenbeheer** of het oude werkgebied **Vergoedingen**, niet vanuit beide.</span><span class="sxs-lookup"><span data-stu-id="c9481-108">You can use ACA reporting only from either the **Benefits management** workspace or the old **Benefits** workspace, not from both.</span></span> <span data-ttu-id="c9481-109">Als u bijvoorbeeld bent overgestapt naar Vergoedingenbeheer, is ACA-rapportage alleen beschikbaar vanuit het werkgebied **Vergoedingenbeheer** en niet vanuit het oude werkgebied **Vergoedingen**.</span><span class="sxs-lookup"><span data-stu-id="c9481-109">For example, if you switched to Benefits management, ACA reporting is available only from the **Benefits management** workspace, not from the old **Benefits** workspace.</span></span>
>
> <span data-ttu-id="c9481-110">Als u midden in een inschrijvingsjaar overschakelt naar Vergoedingenbeheer, moet u in Vergoedingenbeheer de werknemersgegevens voor het hele jaar correct configureren.</span><span class="sxs-lookup"><span data-stu-id="c9481-110">If you switch to Benefits management in the middle of an enrollment year, you must correctly configure employee data for the whole year in Benefits management.</span></span> <span data-ttu-id="c9481-111">Op deze manier zorgt u ervoor dat u nauwkeurige rapporteringsinformatie voor het gehele jaar ontvangt.</span><span class="sxs-lookup"><span data-stu-id="c9481-111">In this way, you ensure that you will receive accurate reporting information for the whole year.</span></span>

## <a name="getting-started"></a><span data-ttu-id="c9481-112">Aan de slag</span><span class="sxs-lookup"><span data-stu-id="c9481-112">Getting started</span></span>

<span data-ttu-id="c9481-113">Om informatie te volgen voor de 1095-formulieren moet u eerst een of meer ACA-dekkingsgroepen maken.</span><span class="sxs-lookup"><span data-stu-id="c9481-113">To track information for 1095 forms, first create one or more Affordable Care coverage groups.</span></span> <span data-ttu-id="c9481-114">In deze groepen wordt de volgende informatie geregistreerd:</span><span class="sxs-lookup"><span data-stu-id="c9481-114">These groups indicate the following information:</span></span>

- <span data-ttu-id="c9481-115">Het dekkingsaanbod dat aan een werknemer is geboden</span><span class="sxs-lookup"><span data-stu-id="c9481-115">The offer of coverage that was provided to an employee</span></span>
- <span data-ttu-id="c9481-116">Het werknemersdeel van de maandelijkse premie van de laagste kosten als de kosten hoger zijn dan de federale armoedegrens</span><span class="sxs-lookup"><span data-stu-id="c9481-116">The employee's share of the lowest-cost monthly premium, if the cost is above the federal poverty line</span></span>
- <span data-ttu-id="c9481-117">Welke Safe Harbor de werkgever gebruikt, indien van toepassing</span><span class="sxs-lookup"><span data-stu-id="c9481-117">The safe harbor that is used by the employer, if applicable</span></span>

<span data-ttu-id="c9481-118">Met ACA-dekkingsgroepen kunt u deze informatie beheren voor meerdere werknemersrecords met dezelfde voorwaarden.</span><span class="sxs-lookup"><span data-stu-id="c9481-118">Affordable Care coverage groups help you manage this information for multiple employee records that have the same conditions.</span></span> <span data-ttu-id="c9481-119">U kunt eenvoudig groepen aan een of meer werknemers toewijzen.</span><span class="sxs-lookup"><span data-stu-id="c9481-119">You can easily assign groups to one or more employees.</span></span>

### <a name="create-or-edit-an-affordable-care-coverage-group"></a><span data-ttu-id="c9481-120">Een ACA-dekkingsgroep maken of bewerken</span><span class="sxs-lookup"><span data-stu-id="c9481-120">Create or edit an Affordable Care coverage group</span></span>

1. <span data-ttu-id="c9481-121">Selecteer in het werkgebied **Vergoedingenbeheer** de optie **ACA-dekkingsgroep**.</span><span class="sxs-lookup"><span data-stu-id="c9481-121">In the **Benefits management** workspace, select **Affordable Care coverage group**.</span></span>

    ![Een ACA-dekkingsgroep selecteren](./media/hr-benefits-management-aca-coverage-group.png)

2. <span data-ttu-id="c9481-123">Selecteer **Nieuw** om een nieuwe ACA-dekkingsgroep te maken of **Bewerken** om een bestaande groep te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="c9481-123">Select **New** to create a new Affordable Care coverage group or **Edit** to change an existing group.</span></span>

    ![Nieuw of Bewerken selecteren](./media/hr-benefits-management-aca-new.png)

3. <span data-ttu-id="c9481-125">Stel de volgende velden in.</span><span class="sxs-lookup"><span data-stu-id="c9481-125">Set the following fields.</span></span>

    | <span data-ttu-id="c9481-126">Veld</span><span class="sxs-lookup"><span data-stu-id="c9481-126">Field</span></span> | <span data-ttu-id="c9481-127">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="c9481-127">Description</span></span> |
    |---|---|
    | <span data-ttu-id="c9481-128">Naam</span><span class="sxs-lookup"><span data-stu-id="c9481-128">Name</span></span> | <span data-ttu-id="c9481-129">Voer een naam voor de groep in.</span><span class="sxs-lookup"><span data-stu-id="c9481-129">Enter a name for the group.</span></span> |
    | <span data-ttu-id="c9481-130">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="c9481-130">Description</span></span> | <span data-ttu-id="c9481-131">Voer een omschrijving in van de groep.</span><span class="sxs-lookup"><span data-stu-id="c9481-131">Enter a description of the group.</span></span> |
    | <span data-ttu-id="c9481-132">Dekkingsaanbod</span><span class="sxs-lookup"><span data-stu-id="c9481-132">Offer of coverage</span></span> | <span data-ttu-id="c9481-133">De dekking die wordt geboden aan werknemers, hun echtgenoot/echtgenote of partner, en hun afhankelijken (gezinsleden).</span><span class="sxs-lookup"><span data-stu-id="c9481-133">The coverage that is offered to employees, their spouse or partner, and their dependents.</span></span> |
    | <span data-ttu-id="c9481-134">Werknemersdeel van kosten</span><span class="sxs-lookup"><span data-stu-id="c9481-134">Employee share of cost</span></span> | <span data-ttu-id="c9481-135">Het bedrag dat voor rekening van de werknemer komt.</span><span class="sxs-lookup"><span data-stu-id="c9481-135">The amount that the employee is responsible for.</span></span> |
    | <span data-ttu-id="c9481-136">Toepasselijke sectie 4980H Safe Harbor</span><span class="sxs-lookup"><span data-stu-id="c9481-136">Applicable section 4980H safe harbor</span></span> | <span data-ttu-id="c9481-137">De 4980H-code voor de Safe Harbor of Transition Relief.</span><span class="sxs-lookup"><span data-stu-id="c9481-137">The 4980H safe harbor or transition relief code.</span></span> |
    | <span data-ttu-id="c9481-138">Beginmaand van plan</span><span class="sxs-lookup"><span data-stu-id="c9481-138">Plan start month</span></span> | <span data-ttu-id="c9481-139">Selecteer de kalendermaand wanneer uw vergoedingsplanjaar begint.</span><span class="sxs-lookup"><span data-stu-id="c9481-139">Select the calendar month when your benefit plan year begins.</span></span> |
    | <span data-ttu-id="c9481-140">Groep geldig vanaf</span><span class="sxs-lookup"><span data-stu-id="c9481-140">Group valid from</span></span> | <span data-ttu-id="c9481-141">De eerste datum waarop deze record geldig is.</span><span class="sxs-lookup"><span data-stu-id="c9481-141">The first date when this record is valid.</span></span> |
    | <span data-ttu-id="c9481-142">Groep geldig tot</span><span class="sxs-lookup"><span data-stu-id="c9481-142">Group valid through</span></span> | <span data-ttu-id="c9481-143">De laatste datum waarop deze record geldig is.</span><span class="sxs-lookup"><span data-stu-id="c9481-143">The last date when this record is valid.</span></span> <span data-ttu-id="c9481-144">Voer **Nooit** in als er geen vervaldatum is.</span><span class="sxs-lookup"><span data-stu-id="c9481-144">If there is no expiration date, enter **Never**.</span></span> |

    ![Een dekkingsgroep maken](./media/hr-benefits-management-aca-new-group.png)

4. <span data-ttu-id="c9481-146">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c9481-146">Select **Save**.</span></span>

### <a name="assign-multiple-employees-to-an-affordable-care-coverage-group"></a><span data-ttu-id="c9481-147">Meerdere werknemers toewijzen aan een ACA-dekkingsgroep</span><span class="sxs-lookup"><span data-stu-id="c9481-147">Assign multiple employees to an Affordable Care coverage group</span></span>

1. <span data-ttu-id="c9481-148">Selecteer in het werkgebied **Vergoedingenbeheer** de optie **ACA-dekkingsgroep**.</span><span class="sxs-lookup"><span data-stu-id="c9481-148">In the **Benefits management** workspace, select **Affordable Care coverage group**.</span></span>
2. <span data-ttu-id="c9481-149">Selecteer de groep waaraan u werknemers wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="c9481-149">Select the group to assign employees to.</span></span>
3. <span data-ttu-id="c9481-150">Selecteer **Groepsgewijze toewijzing**.</span><span class="sxs-lookup"><span data-stu-id="c9481-150">Select **Mass assignment**.</span></span>

    ![Groepsgewijze toewijzing selecteren](./media/hr-benefits-management-aca-mass-assignment.png)

4. <span data-ttu-id="c9481-152">Selecteer werknemers in de lijst en selecteer vervolgens **Toewijzen**.</span><span class="sxs-lookup"><span data-stu-id="c9481-152">Select employees in the list, and then select **Assign**.</span></span>

    ![Geselecteerde werknemers toewijzen aan een groep](./media/hr-benefits-management-aca-assign-coverage-group.png)

## <a name="maintain-multiple-versions-of-coverage-options"></a><span data-ttu-id="c9481-154">Meerdere versies van dekkingsopties onderhouden</span><span class="sxs-lookup"><span data-stu-id="c9481-154">Maintain multiple versions of coverage options</span></span>

<span data-ttu-id="c9481-155">U kunt van elke dekkingsgroep meerdere versies onderhouden.</span><span class="sxs-lookup"><span data-stu-id="c9481-155">You can maintain multiple versions of any coverage group.</span></span> <span data-ttu-id="c9481-156">Wanneer er iets wijzigt in uw organisatie of de vergoedingen die worden geboden, kunt u de informatie van de groep up-to-date houden zonder dat u een nieuwe groep moet maken en daar weer werknemers aan moet toewijzen.</span><span class="sxs-lookup"><span data-stu-id="c9481-156">When something changes in your organization or the benefits that are offered, you can keep the group's information up to date without having to create a new group and reassign employees to it.</span></span>

<span data-ttu-id="c9481-157">Nadat u ACA-dekkingsgroepen gemaakt hebt, kunt u er groepsgewijs werknemers aan toewijzen.</span><span class="sxs-lookup"><span data-stu-id="c9481-157">After you've created Affordable Care coverage groups, you can mass-assign employees to them.</span></span> <span data-ttu-id="c9481-158">U kunt werknemers ook afzonderlijk aan groepen toewijzen en aangeven of ACA-informatie wordt gevolgd en gerapporteerd.</span><span class="sxs-lookup"><span data-stu-id="c9481-158">You can also individually assign employees to groups, and indicate whether ACA information is tracked and reported.</span></span>

<span data-ttu-id="c9481-159">Als u geen ACA-gegevens voor een werknemer hoeft bij te houden en te rapporteren, kunt u de optie **Dekking rapporteren** instellen op **Nee**.</span><span class="sxs-lookup"><span data-stu-id="c9481-159">If you don't have to track and report ACA information for an employee, you can set the **Report coverage** option to **No**.</span></span> <span data-ttu-id="c9481-160">Bijvoorbeeld hebt u te maken met parttime werknemers waarvoor geen ACA-rapportage vereist is.</span><span class="sxs-lookup"><span data-stu-id="c9481-160">For example, you might have part-time employees who don't require ACA reporting.</span></span>

### <a name="override-default-values-for-an-employee"></a><span data-ttu-id="c9481-161">Standaardwaarden voor een werknemer overschrijven</span><span class="sxs-lookup"><span data-stu-id="c9481-161">Override default values for an employee</span></span>

<span data-ttu-id="c9481-162">Voor werknemers die zijn toegewezen aan een ACA-dekkingsgroep kunt u de volgende opties wijzigen voor maanden die afwijkende waarden vereisen:</span><span class="sxs-lookup"><span data-stu-id="c9481-162">For employees who are assigned to an Affordable Care coverage group, you can change the following options for any months that require different values:</span></span>

- <span data-ttu-id="c9481-163">Dekkingsaanbod</span><span class="sxs-lookup"><span data-stu-id="c9481-163">Offer of coverage</span></span>
- <span data-ttu-id="c9481-164">Werknemersdeel van kosten</span><span class="sxs-lookup"><span data-stu-id="c9481-164">Employee share of cost</span></span>
- <span data-ttu-id="c9481-165">Toepasselijke sectie 4980H Safe Harbor</span><span class="sxs-lookup"><span data-stu-id="c9481-165">Applicable section 4980H safe harbor</span></span>

> [!NOTE]
> <span data-ttu-id="c9481-166">Voor ACA-rapporten over 2020 moet u de postcodes van zowel het werkadres als het thuisadres vermelden op formulier 1095-C.</span><span class="sxs-lookup"><span data-stu-id="c9481-166">For 2020 ACA reports, you must report both work and home ZIP Codes on Form 1095-C.</span></span> <span data-ttu-id="c9481-167">Waarden worden automatisch ingevuld op basis van de huidige actieve locaties.</span><span class="sxs-lookup"><span data-stu-id="c9481-167">Values are automatically filled in, based on current active locations.</span></span> <span data-ttu-id="c9481-168">Als een van beide locaties gedurende een deel van het jaar anders is, moet u de waarde overschrijven.</span><span class="sxs-lookup"><span data-stu-id="c9481-168">If either location was different during any part of the year, you must override the value.</span></span> <span data-ttu-id="c9481-169">Het veld **Postcode** (regel 17) van het 1095-C-rapport wordt alleen ingevuld als de code **Dekkingsaanbod** een waarde uit de reeks **1L** tot en met **1Q** bevat, als volgt:</span><span class="sxs-lookup"><span data-stu-id="c9481-169">The **ZIP Code** field (line 17) of the 1095-C report is filled in only if the **Offer of coverage** code contains **1L** through **1Q**, as follows:</span></span>
>
> - <span data-ttu-id="c9481-170">**1L, 1M of 1N:** de postcode van de primaire woonadres</span><span class="sxs-lookup"><span data-stu-id="c9481-170">**1L, 1M, or 1N:** The primary residence ZIP Code</span></span>
> - <span data-ttu-id="c9481-171">**1O, 1P, 1Q:** de postcode van het primaire werkadres</span><span class="sxs-lookup"><span data-stu-id="c9481-171">**1O, 1P, 1Q:** The primary work ZIP Code</span></span>

<span data-ttu-id="c9481-172">Voer de volgende stappen uit om uitzonderingen in te voeren voor alle waarden van een ACA-dekkingsgroep.</span><span class="sxs-lookup"><span data-stu-id="c9481-172">To enter exceptions for any values of an Affordable Care coverage group, follow these steps.</span></span>

1. <span data-ttu-id="c9481-173">Selecteer in het werkgebied **Personeelsbeheer** de optie **Koppelingen** en selecteer vervolgens **Werknemers**.</span><span class="sxs-lookup"><span data-stu-id="c9481-173">In the **Personnel management** workspace, select **Links**, and then select **Workers**.</span></span>
2. <span data-ttu-id="c9481-174">Selecteer de werknemer in de lijst.</span><span class="sxs-lookup"><span data-stu-id="c9481-174">Select the employee in the list.</span></span>
3. <span data-ttu-id="c9481-175">Selecteer op het tabblad **Dienstverband**, in de sectie **Meer informatie**, de optie **ACA-dekking**.</span><span class="sxs-lookup"><span data-stu-id="c9481-175">On the **Employment** tab, in the **More information** section, select **Affordable Care coverage**.</span></span>

    ![Opties voor één werknemer wijzigen](./media/hr-benefits-management-aca-change-single-employee.png)

4. <span data-ttu-id="c9481-177">Selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="c9481-177">Select **Edit**.</span></span>
5. <span data-ttu-id="c9481-178">Schakel het selectievakje **Standaardwaarden overschrijven** in voor elke maand die moet worden gewijzigd en wijzig vervolgens de andere waarden waar nodig.</span><span class="sxs-lookup"><span data-stu-id="c9481-178">For each month that requires changes, select the **Override default** check box, and then change the other values as required.</span></span>

    ![Standaardwaarden overschrijven](./media/hr-benefits-management-aca-override-default.png)

6. <span data-ttu-id="c9481-180">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c9481-180">Select **Save**.</span></span>

## <a name="report-health-care-coverage"></a><span data-ttu-id="c9481-181">Gezondheidszorgdekking rapporteren</span><span class="sxs-lookup"><span data-stu-id="c9481-181">Report health care coverage</span></span>

<span data-ttu-id="c9481-182">U moet iedere door de werkgever gesponsorde zorgdekking uit interne verzekering bijhouden voor fulltime en parttime werknemers.</span><span class="sxs-lookup"><span data-stu-id="c9481-182">You must track any employer-sponsored, self-insured health care coverage for full-time and part-time employees.</span></span> <span data-ttu-id="c9481-183">Voeg elke werknemer toe, samen met diens afhankelijken, op het 1095-C-rapport voor de maanden waarin ze dekking kregen.</span><span class="sxs-lookup"><span data-stu-id="c9481-183">Include each employee, together with their dependents, on the 1095-C report for the months when they were covered.</span></span>

<span data-ttu-id="c9481-184">Volg deze stappen om aan te geven of een vergoedingsplan moet worden gerapporteerd.</span><span class="sxs-lookup"><span data-stu-id="c9481-184">To indicate whether a benefit plan must be reported, follow these steps.</span></span>

1. <span data-ttu-id="c9481-185">Selecteer in het werkgebied **Vergoedingenbeheer** de optie **Vergoedingsplannen**.</span><span class="sxs-lookup"><span data-stu-id="c9481-185">In the **Benefits management** workspace, select **Benefit plans**.</span></span>
2. <span data-ttu-id="c9481-186">Selecteer het vergoedingsplan waarover u wilt rapporteren.</span><span class="sxs-lookup"><span data-stu-id="c9481-186">Select the benefit plan to report.</span></span>
3. <span data-ttu-id="c9481-187">Selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="c9481-187">Select **Edit**.</span></span>
4. <span data-ttu-id="c9481-188">Stel de optie **Aangegeven onder de Affordable Care Act** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="c9481-188">Set the **Reported under the Affordable Care Act** option to **Yes**.</span></span>

    ![Gezondheidszorgdekking rapporteren](./media/hr-benefits-management-aca-report-coverage.png)

5. <span data-ttu-id="c9481-190">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c9481-190">Select **Save**.</span></span>

<span data-ttu-id="c9481-191">Als een werknemer zorgdekking kiest voor een afhankelijke, wordt de dekkingsperiode van de afhankelijke bepaald door de datum waarop de afhankelijke is ingeschreven of verwijderd.</span><span class="sxs-lookup"><span data-stu-id="c9481-191">If an employee chooses health care coverage for a dependent, the dependent's coverage period is determined by the date when the dependent was enrolled or removed.</span></span> <span data-ttu-id="c9481-192">De dekkingsdatums voor een afhankelijke worden automatisch berekend op basis van de periode waarin de afhankelijke gedurende het inschrijvingsjaar in aanmerking komt en actief was in een plan.</span><span class="sxs-lookup"><span data-stu-id="c9481-192">Coverage dates for dependents are automatically calculated based on the period when the dependent was eligible and active in a plan during the enrollment year.</span></span>

## <a name="generate-1095-b-and-1095-c-forms"></a><span data-ttu-id="c9481-193">Formulieren 1095-B en 1095-C genereren</span><span class="sxs-lookup"><span data-stu-id="c9481-193">Generate 1095-B and 1095-C forms</span></span>

<span data-ttu-id="c9481-194">U kunt ook de ACA-formulieren 1095-B en 1095-C genereren in het product en distribueren naar uw werknemers.</span><span class="sxs-lookup"><span data-stu-id="c9481-194">You can generate ACA 1095-B and 1095-C forms, and then distribute them to each of your employees.</span></span> <span data-ttu-id="c9481-195">U kunt ook formulier 1095-C en de bijbehorende 1094-C-verzendbestanden elektronisch genereren om naar de Internal Revenue Service (IRS) te verzenden.</span><span class="sxs-lookup"><span data-stu-id="c9481-195">You can also electronically generate Form 1095-C and the corresponding 1094-C transmittal files to send to the Internal Revenue Service (IRS).</span></span>

1. <span data-ttu-id="c9481-196">Selecteer in het werkgebied **Vergoedingenbeheer** de optie **Formulier ACA 1095-B** of **Formulier ACA 1095-C**.</span><span class="sxs-lookup"><span data-stu-id="c9481-196">In the **Benefits management** workspace, select **ACA 1095-B form** or **ACA 1095-C form**.</span></span>
2. <span data-ttu-id="c9481-197">Wijzig waar nodig de parameters en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="c9481-197">Change the parameters as required, and then select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c9481-198">Als u 1095-C-formulieren voor meer dan 500 werknemers afdrukt, ontvangt u meer dan één PDF-bestand.</span><span class="sxs-lookup"><span data-stu-id="c9481-198">If you're printing 1095-C forms for more than 500 employees, you will receive more than one PDF file.</span></span> <span data-ttu-id="c9481-199">U wordt aangeraden de waarde van het veld **Maximumbestandsgrootte in megabytes** op de pagina **Parameters voor documentbeheer** te verhogen naar **150**.</span><span class="sxs-lookup"><span data-stu-id="c9481-199">We recommend that you increase the value of the **Maximum file size in megabytes** field on the **Document management parameters** page to **150**.</span></span> <span data-ttu-id="c9481-200">(Als u die pagina snel wilt openen, kunt u het zoekveld op de navigatiebalk gebruiken.)</span><span class="sxs-lookup"><span data-stu-id="c9481-200">(To quickly open that page, you can use the search field on the navigation bar.)</span></span>
    >
    > ![De maximumbestandsgrootte wijzigen](./media/hr-benefits-management-aca-maximum-file-size.png)

3. <span data-ttu-id="c9481-202">Als u de status van uw rapporten wilt controleren en weergeven, gebruikt u het zoekveld op de navigatiebalk om de pagina **Elektronische rapportagetaken** te openen.</span><span class="sxs-lookup"><span data-stu-id="c9481-202">To check the status of your reports and view them, use the search field on the navigation bar to open the **Electronic reporting jobs** page.</span></span>

    ![De pagina Elektronische rapportagetaken zoeken](./media/hr-benefits-management-aca-search-electronic-reporting-jobs.png)

4. <span data-ttu-id="c9481-204">Selecteer het rapport dat u wilt weergeven en selecteer vervolgens **Bestanden weergeven**.</span><span class="sxs-lookup"><span data-stu-id="c9481-204">Select the report to view, and then select **Show files**.</span></span>

    ![Bestanden weergeven](./media/hr-benefits-management-aca-show-files.png)

5. <span data-ttu-id="c9481-206">Selecteer **Openen**.</span><span class="sxs-lookup"><span data-stu-id="c9481-206">Select **Open**.</span></span>

    ![Een bestand openen](./media/hr-benefits-management-aca-open-file.png)

6. <span data-ttu-id="c9481-208">Open vanuit de Meldingsbalk die onderin het browservenster wordt weergegeven het zip-bestand en selecteer het rapport.</span><span class="sxs-lookup"><span data-stu-id="c9481-208">From the Notification bar that appears at the bottom of the browser window, open the zip file, and then select the report.</span></span> <span data-ttu-id="c9481-209">U kunt het PDF-bestand weergeven of afdrukken.</span><span class="sxs-lookup"><span data-stu-id="c9481-209">You can view or print the PDF file.</span></span>

    ![Voorbeeldformulier 1095-C](./media/hr-benefits-management-aca-1095-c-form.png)

## <a name="view-aca-coverage-information"></a><span data-ttu-id="c9481-211">Informatie over ACA-dekking weergeven</span><span class="sxs-lookup"><span data-stu-id="c9481-211">View ACA coverage information</span></span>

<span data-ttu-id="c9481-212">Op de pagina **Dekking betaalbare zorg werknemer** wordt de volgende informatie getoond:</span><span class="sxs-lookup"><span data-stu-id="c9481-212">The **Worker Affordable Care coverage** page shows the following information:</span></span>

- <span data-ttu-id="c9481-213">Werknemers die aan alle dekkingsgroepen zijn toegewezen</span><span class="sxs-lookup"><span data-stu-id="c9481-213">Employees who are assigned to each coverage group</span></span>
- <span data-ttu-id="c9481-214">Werknemers die niet in een rapport hoeven te worden opgenomen</span><span class="sxs-lookup"><span data-stu-id="c9481-214">Employees who don't have to be included on a report</span></span>
- <span data-ttu-id="c9481-215">Niet-toegewezen werknemers</span><span class="sxs-lookup"><span data-stu-id="c9481-215">Unassigned employees</span></span>

<span data-ttu-id="c9481-216">Voer de volgende stappen uit om deze informatie weer te geven.</span><span class="sxs-lookup"><span data-stu-id="c9481-216">To view this information, follow these steps.</span></span>

1. <span data-ttu-id="c9481-217">Selecteer in het werkgebied **Vergoedingenbeheer** de optie **Dekking betaalbare zorg werknemer**.</span><span class="sxs-lookup"><span data-stu-id="c9481-217">In the **Benefits management** workspace, select **Worker Affordable Care coverage**.</span></span>
2. <span data-ttu-id="c9481-218">Selecteer een groep in het veld **Groepsnaam**.</span><span class="sxs-lookup"><span data-stu-id="c9481-218">In the **Group name** field, select a group.</span></span>

    ![ACA-dekking weergeven](./media/hr-benefits-management-aca-view-coverage.png)

<span data-ttu-id="c9481-220">Als een van de standaardwaarden van de ACA-dekkingsgroep is overschreven, wordt dit aangegeven met een asterisk naast de gewijzigde waarde.</span><span class="sxs-lookup"><span data-stu-id="c9481-220">If any default values from the Affordable Care coverage group have been overridden, an asterisk appears next to the value that was changed.</span></span> <span data-ttu-id="c9481-221">Als de waarden voor alle twaalf maanden hetzelfde zijn en niet zijn overschreven, wordt de waarde weergegeven in de kolom **Alle 12 maanden**.</span><span class="sxs-lookup"><span data-stu-id="c9481-221">If the values for all 12 months are the same and haven't been overridden, the value appears in the **All 12 months** column.</span></span>

<span data-ttu-id="c9481-222">U kunt werknemers weergeven die zijn gemarkeerd als niet vereist om aan te melden voor de ACA en waarvoor geen Formulier 1095-C vereist is.</span><span class="sxs-lookup"><span data-stu-id="c9481-222">You can view employees who are marked as not ACA-reportable, and who won't require a Form 1095-C.</span></span> <span data-ttu-id="c9481-223">Selecteer in het veld **Filteren op** de optie **Niet aan te geven onder ACA**.</span><span class="sxs-lookup"><span data-stu-id="c9481-223">In the **Filter by** field, select **Not ACA reportable**.</span></span>

<span data-ttu-id="c9481-224">U kunt werknemers weergeven die niet aan een groep zijn toegewezen of die aan een verlopen groep zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="c9481-224">You can view employees who aren't assigned to a group, or who are assigned to an expired group.</span></span> <span data-ttu-id="c9481-225">Selecteer in het veld **Filteren op** de optie **Niet-toegewezen of verlopen groep**.</span><span class="sxs-lookup"><span data-stu-id="c9481-225">In the **Filter by** field, select **Unassigned or expired group**.</span></span>

### <a name="export-to-excel"></a><span data-ttu-id="c9481-226">Exporteren naar Excel</span><span class="sxs-lookup"><span data-stu-id="c9481-226">Export to Excel</span></span>

<span data-ttu-id="c9481-227">Als u een van de lijsten wilt exporteren naar Microsoft Excel, gaat u als volgt te werk.</span><span class="sxs-lookup"><span data-stu-id="c9481-227">To export any of the lists to Microsoft Excel, follow these steps.</span></span>

1. <span data-ttu-id="c9481-228">Selecteer de knop **Openen in Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="c9481-228">Select the **Open in Microsoft Office** button.</span></span>
2. <span data-ttu-id="c9481-229">Selecteer **HCM Human Resources tijdelijke tabel voor intern gebruik**.</span><span class="sxs-lookup"><span data-stu-id="c9481-229">Select **HCM Human Resources temporary table for internal use**.</span></span>
3. <span data-ttu-id="c9481-230">Selecteer **Downloaden**.</span><span class="sxs-lookup"><span data-stu-id="c9481-230">Select **Download**.</span></span>

### <a name="view-aca-reportable-dependents"></a><span data-ttu-id="c9481-231">Onder ACA aan te geven afhankelijken weergeven</span><span class="sxs-lookup"><span data-stu-id="c9481-231">View ACA-reportable dependents</span></span>

<span data-ttu-id="c9481-232">Als u gedekte personen moet rapporteren omdat u interne verzekering aanbiedt, kunt u alle afhankelijken weergeven die zijn gedekt door vergoedingsplannen die zijn gemarkeerd als **Aan te geven onder ACA**.</span><span class="sxs-lookup"><span data-stu-id="c9481-232">If you must report covered individuals because you provide self-insured coverage, you can view dependents who are covered under benefit plans that are marked as **ACA reportable**.</span></span> <span data-ttu-id="c9481-233">Selecteer in het actievenster de optie **Gezinsdekking weergeven**.</span><span class="sxs-lookup"><span data-stu-id="c9481-233">On the Action Pane, select **View Dependent coverage**.</span></span>

![Gezinsdekking weergeven](./media/hr-benefits-management-aca-view-dependent-coverage.png)

<span data-ttu-id="c9481-235">De dekkingsinformatie voor de afhankelijken van de werknemer wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="c9481-235">Coverage information for the employee's dependents is shown.</span></span>

![Gezinsdekking](./media/hr-benefits-management-aca-dependents.png)

> [!NOTE]
> <span data-ttu-id="c9481-237">Op de pagina worden alleen vergoedingsplannen weergegeven die zijn gemarkeerd als **Aan te geven onder ACA**.</span><span class="sxs-lookup"><span data-stu-id="c9481-237">The page shows only benefits plans that are marked as **ACA reportable**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]