---
title: Rapporten maken voor Affordable Care Act (Amerikaanse wet inzake betaalbare zorg)
description: Rapportage voor de Affordable Care Act (ACA) genereert de formulieren 1095-B en 1095-C ter ondersteuning van het deel **Werkgeversmandaag** van de ACA.
author: andreabichsel
ms.date: 02/03/2020
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
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 055de1f0ff3f8fd4fadba0a685fd703b9d19d918
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805989"
---
# <a name="generate-aca-reports"></a><span data-ttu-id="b9832-103">ACA-rapporten genereren</span><span class="sxs-lookup"><span data-stu-id="b9832-103">Generate ACA reports</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b9832-104">Rapportage voor de Affordable Care Act (ACA) genereert de formulieren 1095-B en 1095-C ter ondersteuning van het deel **Werkgeversmandaag** van de ACA.</span><span class="sxs-lookup"><span data-stu-id="b9832-104">Affordable Care Act (ACA) reporting generates forms 1095-B and 1095-C in support of the **Employer Mandate** portion of the Affordable Care Act.</span></span>

> [!NOTE]
> <span data-ttu-id="b9832-105">ACA-rapportage is alleen ingeschakeld voor rechtspersonen in de Verenigde Staten.</span><span class="sxs-lookup"><span data-stu-id="b9832-105">ACA reporting is only enabled for legal entities in the United States.</span></span>

## <a name="getting-started"></a><span data-ttu-id="b9832-106">Aan de slag</span><span class="sxs-lookup"><span data-stu-id="b9832-106">Getting started</span></span>

<span data-ttu-id="b9832-107">Om informatie te volgen voor de formulieren 1095-B en 1095 C, moet u eerst een of meer ACA-dekkingsgroepen maken.</span><span class="sxs-lookup"><span data-stu-id="b9832-107">To track information for forms 1095-B and 1095-C, you must first create one or more Affordable care coverage groups.</span></span> <span data-ttu-id="b9832-108">In de ACA-dekkingsgroepen wordt de volgende informatie geregistreerd:</span><span class="sxs-lookup"><span data-stu-id="b9832-108">Affordable Care coverage groups indicate:</span></span>

- <span data-ttu-id="b9832-109">Het dekkingsaanbod voor een werknemer</span><span class="sxs-lookup"><span data-stu-id="b9832-109">The offer of coverage for an employee</span></span>
- <span data-ttu-id="b9832-110">Het werknemersdeel van de maandelijkse premie van de laagste kosten als de kosten hoger zijn dan de federale armoedegrens</span><span class="sxs-lookup"><span data-stu-id="b9832-110">The employee’s share of the lowest cost monthly premium, if the cost is above the federal poverty line</span></span>
- <span data-ttu-id="b9832-111">Welke Safe Harbor de werkgever gebruikt, indien van toepassing</span><span class="sxs-lookup"><span data-stu-id="b9832-111">Safe Harbor used by the employer, if applicable</span></span>

<span data-ttu-id="b9832-112">Wanneer u ACA-dekkingsgroepen gebruikt, kunt u de informatie voor deze velden beheren zonder dat u elke werknemersrecord hoeft te wijzigen zolang de voorwaarden identiek zijn.</span><span class="sxs-lookup"><span data-stu-id="b9832-112">Affordable Care coverage groups allow you to manage the information for these fields without changing every employee record where the conditions are the same.</span></span> <span data-ttu-id="b9832-113">U kunt ACA-dekkingsgroepen eenvoudig toewijzen aan een of meerdere werknemers, door middel van de functie **Groepsgewijze toewijzing** op de pagina.</span><span class="sxs-lookup"><span data-stu-id="b9832-113">You can easily assign Affordable Care coverage groups to one or more employees by using the **Mass assign** option on the page.</span></span>

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a><span data-ttu-id="b9832-114">Meerdere versies van een dekkingsgroep onderhouden</span><span class="sxs-lookup"><span data-stu-id="b9832-114">Maintaining multiple versions of a coverage group</span></span>

<span data-ttu-id="b9832-115">U kunt van elke dekkingsgroep meerdere versies onderhouden.</span><span class="sxs-lookup"><span data-stu-id="b9832-115">You can maintain multiple versions of any coverage group.</span></span> <span data-ttu-id="b9832-116">Met deze functionaliteit kunt u wijzigingen aanbrengen zonder dat u een nieuwe groep moet maken en werknemers daar weer aan moet toewijzen.</span><span class="sxs-lookup"><span data-stu-id="b9832-116">This functionality allows you to make changes without having to create a new group and reassign employees to it.</span></span> 

<span data-ttu-id="b9832-117">Nadat u ACA-dekkingsgroepen hebt gemaakt, kunt u deze groepen groepsgewijs toewijzen aan werknemers met de optie **Groepsgewijze toewijzing**.</span><span class="sxs-lookup"><span data-stu-id="b9832-117">After you’ve created ACA coverage groups, you can mass assign the groups to employees with the **Mass assignment** option.</span></span> <span data-ttu-id="b9832-118">U kunt ook afzonderlijk aangeven of u ACA-gegevens wilt bijhouden en rapporteren, en een werknemer toewijzen aan een ACA-dekkingsgroep.</span><span class="sxs-lookup"><span data-stu-id="b9832-118">You can also individually indicate whether to track and report ACA information, and assign an employee to an Affordable Care coverage group.</span></span>

<span data-ttu-id="b9832-119">U hoeft bepaalde ACA-dekkingsgegevens niet bij te houden, bijvoorbeeld voor parttime werknemers.</span><span class="sxs-lookup"><span data-stu-id="b9832-119">You don't need to track some ACA coverage information, such as for part-time employees.</span></span> <span data-ttu-id="b9832-120">In dit geval stelt u het veld **Dekking rapporteren** in op **Nee**.</span><span class="sxs-lookup"><span data-stu-id="b9832-120">In this case, set the **Report coverage** field to **No**.</span></span> <span data-ttu-id="b9832-121">Hoewel u elke werknemer met bij te houden ACA-gegevens moet toewijzen aan een ACA-dekkingsgroep , kunt u toch de volgende opties wijzigen voor maanden met verschillende waarden:</span><span class="sxs-lookup"><span data-stu-id="b9832-121">Although you must assign each employee with trackable ACA information to an Affordable Care coverage group, you can still change the following options for months with different values:</span></span>

- <span data-ttu-id="b9832-122">**Dekkingsaanbod**</span><span class="sxs-lookup"><span data-stu-id="b9832-122">**Offer of coverage**</span></span>
- <span data-ttu-id="b9832-123">**Werknemersdeel van kosten**</span><span class="sxs-lookup"><span data-stu-id="b9832-123">**Employee share of cost**</span></span>
- <span data-ttu-id="b9832-124">**Safe Harbor**</span><span class="sxs-lookup"><span data-stu-id="b9832-124">**Safe Harbor**</span></span>

<span data-ttu-id="b9832-125">Als u uitzonderingen wilt invoeren voor een of meer van de ACA-dekkingsgroepwaarden, klikt u op de koppeling **Dekking betaalbare zorg** op de pagina **Medewerkergegevens**, die u vindt onder de sectie **Aanvullende gegevens** op het tabblad **Dienstverband**.</span><span class="sxs-lookup"><span data-stu-id="b9832-125">To enter exceptions for Affordable Care coverage group values, select the **Affordable Care Coverage** link on the **Worker detail** page under the **Additional information** section on the **Employment tab**.</span></span>

## <a name="reporting-health-care-coverage"></a><span data-ttu-id="b9832-126">Gezondheidszorgdekking rapporteren</span><span class="sxs-lookup"><span data-stu-id="b9832-126">Reporting health care coverage</span></span>

<span data-ttu-id="b9832-127">Niet alleen moet u bijhouden of en zo ja, welke dekking is aangeboden aan full-time werknemers; ook moet, als de werkgever meebetaalt aan interne zorgverzekering waarvoor de werknemer is aangemeld (ongeacht of deze full-time of part-time is), aanvullende informatie worden aangegeven via het formulier 1095-C.</span><span class="sxs-lookup"><span data-stu-id="b9832-127">In addition to tracking health insurance coverage offered to full-time employees, if the employer offers employer-sponsored self-insured health coverage for which the employee is enrolled (regardless of whether their employment status is full-time or part-time), additional information needs to be reported on the 1095-C.</span></span> <span data-ttu-id="b9832-128">Elke werknemer (inclusief gezinsleden) die valt onder door de werkgever gesponsorde vergoedingsschema's moet worden vermeld in het rapport voor de maanden waarin zij verzekerd waren.</span><span class="sxs-lookup"><span data-stu-id="b9832-128">Each employee (including dependents) covered by the employer-sponsored benefit plans needs to be included on the report for the months they were covered.</span></span> 

<span data-ttu-id="b9832-129">U kunt voor elk vergoedingsschema bepalen of het moet worden aangegeven door het selectievakje **Aan te geven voor ACA** in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="b9832-129">You can indicate whether or not each benefit plan must be reported by selecting the **ACA reportable** check box.</span></span>

<span data-ttu-id="b9832-130">Als werknemers er daarnaast voor kiezen om een of meerdere gezinsleden onder een van de vergoedingen te laten vallen, kunt u voor elke werknemer apart aangeven op welke datums de afhankelijke was verzekerd op de pagina **Vergoedingen onderhouden**.</span><span class="sxs-lookup"><span data-stu-id="b9832-130">In addition, if employees have chosen to have any of their dependents covered under a benefit, you can indicate the dates the dependent was covered for each employee on the **Maintain benefits** page.</span></span> <span data-ttu-id="b9832-131">Om aan te geven dat de afhankelijke wordt gedekt door de vergoeding, kiest u de knop **Bewerken** in het actievenster van het sneltabblad **Afhankelijken**.</span><span class="sxs-lookup"><span data-stu-id="b9832-131">To indicate that the dependent is covered under the benefit, select the **Edit** button in the action pane of the **Dependents** fast tab.</span></span>

<span data-ttu-id="b9832-132">Op de pagina **Datumbeheer dekking afhankelijke** kunt u opgeven op welke datums de afhankelijke is gedekt door de vergoeding.</span><span class="sxs-lookup"><span data-stu-id="b9832-132">On the **Dependent coverage date manager** page, you can indicate the dates the dependent was covered by the benefit.</span></span> <span data-ttu-id="b9832-133">Wanneer u datums op deze pagina invoert, wordt automatisch het selectievakje **Gedekt** op de pagina **Vergoedingen onderhouden** ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="b9832-133">Entering dates on this page will automatically select the **Covered** checkbox on the **Maintain benefits** page.</span></span>

## <a name="generate-1095-b-and-1095-c-forms"></a><span data-ttu-id="b9832-134">Formulieren 1095-B en 1095-C genereren</span><span class="sxs-lookup"><span data-stu-id="b9832-134">Generate 1095-B and 1095-C forms</span></span>

<span data-ttu-id="b9832-135">U kunt ook de formulieren 1095-B en 1095-C genereren in het product en distribueren naar uw werknemers.</span><span class="sxs-lookup"><span data-stu-id="b9832-135">You can also generate 1095-B and 1095-C forms from within the product, and distribute them to each of your employees.</span></span> <span data-ttu-id="b9832-136">Het systeem kan ook elektronisch 1095-C-formulieren en de 1094-C IRS-verzendbestanden genereren.</span><span class="sxs-lookup"><span data-stu-id="b9832-136">The system can also electronically generate 1095-C forms and the 1094-C IRS transmittal files.</span></span>  

<span data-ttu-id="b9832-137">Bij het genereren van het 1095-C-formulier geeft u het betreffende belastingjaar op en geeft u aan of Social Security-nummers moeten worden gemaskeerd.</span><span class="sxs-lookup"><span data-stu-id="b9832-137">When generating the 1095-C form, enter the appropriate tax year and indicate if social security numbers should be masked.</span></span> <span data-ttu-id="b9832-138">Als u 1095-C-formulieren voor meer dan 500 werknemers afdrukt, ontvangt u meer dan één PDF-bestand.</span><span class="sxs-lookup"><span data-stu-id="b9832-138">If you're printing 1095-C forms for more than 500 employees, you'll receive more than one PDF file.</span></span> <span data-ttu-id="b9832-139">Het is raadzaam de waarde voor **Maximale bestandsgrootte** in het venster **Parameters voor documentbeheer** te verhogen naar 150 MB.</span><span class="sxs-lookup"><span data-stu-id="b9832-139">It’s recommended that you increase the **Maximum file size** in the **Document management parameters** window to 150 MB.</span></span>

## <a name="viewing-information"></a><span data-ttu-id="b9832-140">Informatie weergeven</span><span class="sxs-lookup"><span data-stu-id="b9832-140">Viewing information</span></span>

<span data-ttu-id="b9832-141">Op de pagina **Dekking betaalbare zorg werknemer** kunt u zien welke werknemers zijn toegewezen aan de verschillende dekkingsgroepen, welke werknemers niet hoeven te worden opgenomen in een rapport en welke werknemers niet zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="b9832-141">You can use the **Worker Affordable Care coverage** page to see which employees have been assigned to each coverage group, which employees don’t need to be included on a report, and which employees are unassigned.</span></span>

<span data-ttu-id="b9832-142">Als een van de standaardwaarden van de ACA-dekkingsgroep is overschreven, wordt dit aangegeven met een asterisk naast de gewijzigde waarde.</span><span class="sxs-lookup"><span data-stu-id="b9832-142">If any of the default values from the Affordable Care coverage group have been overridden, an asterisk will appear next to the value that was changed.</span></span> <span data-ttu-id="b9832-143">Als de waarden voor alle twaalf maanden hetzelfde zijn en niet zijn overschreven, wordt de waarde weergegeven in de kolom **Alle 12 maanden**.</span><span class="sxs-lookup"><span data-stu-id="b9832-143">If the values for all 12 months are the same and haven’t been overridden, the value will print in the **All 12 months** column.</span></span>

<span data-ttu-id="b9832-144">U kunt het informatievenster ook gebruiken om te begrijpen welke werknemers zijn gemarkeerd als niet-rapporteerbaar voor de ACA.</span><span class="sxs-lookup"><span data-stu-id="b9832-144">You can also use the inquiry window to understand which employees have been flagged as not ACA reportable.</span></span> <span data-ttu-id="b9832-145">U hoeft niet bij te houden of de dekking aan hen is aangeboden en u hoeft hen aan het einde van het jaar geen 1095-C te verstrekken.</span><span class="sxs-lookup"><span data-stu-id="b9832-145">You don’t need to track whether coverage was offered to them and won't need to issue a 1095-C to them at the end of the year.</span></span> <span data-ttu-id="b9832-146">Selecteer **Niet aan te geven onder ACA** in het veld **Filteren op** om een lijst te genereren met alle werknemers die geen 1095-C ontvangen.</span><span class="sxs-lookup"><span data-stu-id="b9832-146">Select **Not ACA reportable** in the **Filter by** field to generate a list of all employees who won't receive a 1095-C.</span></span>

<span data-ttu-id="b9832-147">Daarnaast kunt u ook alle werknemers zien die niet zijn toegewezen (zonder waarde in het veld **ACA-dekking aangeven**) of die zijn toegewezen aan een ACA-dekkingsgroep die is verlopen voor het jaar dat is geselecteerd in het veld **Jaar**.</span><span class="sxs-lookup"><span data-stu-id="b9832-147">In addition, you can view any employees who are unassigned (the **ACA Report coverage** field is empty) or who have been assigned to an Affordable Care coverage group that is expired for the year selected in the **Year** field.</span></span>

<span data-ttu-id="b9832-148">U kunt via een van de filteropties gegenereerde lijsten met werknemers naar Excel exporteren.</span><span class="sxs-lookup"><span data-stu-id="b9832-148">You can export lists of employees that were generated using any of the filtering options to Excel.</span></span>

<span data-ttu-id="b9832-149">Als u gedekte personen moet rapporteren omdat u interne verzekering aanbiedt, kunt u alle afhankelijken weergeven die zijn gedekt door vergoedingsplannen die zijn gemarkeerd als **Aan te geven onder ACA**.</span><span class="sxs-lookup"><span data-stu-id="b9832-149">If you need to report covered individuals because you provide self-insured coverage, you can view any dependents covered under benefit plans marked as **ACA reportable**.</span></span> <span data-ttu-id="b9832-150">Selecteer in het actievenster de optie **Gezinsdekking weergeven**.</span><span class="sxs-lookup"><span data-stu-id="b9832-150">Select **View Dependent coverage** on the action pane.</span></span>

> [!NOTE]
> <span data-ttu-id="b9832-151">Alleen vergoedingsplannen die zijn gemarkeerd als **Aan te geven onder ACA** worden getoond in het informatievenster.</span><span class="sxs-lookup"><span data-stu-id="b9832-151">Only benefit plans marked as **ACA reportable** display in the inquiry window.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]