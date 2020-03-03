---
title: Rapporten voor de Wet Betaalbare zorg (ACA) maken
description: Er is functionaliteit beschikbaar om werkgevers te helpen die de gegevens moeten bijhouden die wordt gemeld via de formulieren 1095-B en 1095-C, ter ondersteuning van het gedeelte Employer Mandate van de Affordable Care Act. Houd er rekening mee dat deze functionaliteit alleen beschikbaar is voor rechtspersonen in de Verenigde Staten.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 47532861203fedbffc49aa92d25fc99de9d25376
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008637"
---
# <a name="generate-affordable-care-act-aca-reports"></a><span data-ttu-id="02135-103">Rapporten voor de Wet Betaalbare zorg (ACA) maken</span><span class="sxs-lookup"><span data-stu-id="02135-103">Generate Affordable Care Act (ACA) reports</span></span>

<span data-ttu-id="02135-104">Er is functionaliteit beschikbaar om werkgevers te helpen die de gegevens moeten bijhouden die wordt gemeld via de formulieren 1095-B en 1095-C, ter ondersteuning van het gedeelte **Employer Mandate** van de Affordable Care Act. Houd er rekening mee dat deze functionaliteit alleen beschikbaar is voor rechtspersonen in de Verenigde Staten.</span><span class="sxs-lookup"><span data-stu-id="02135-104">Functionality is available to assist employers that need to track the information reported on forms 1095-B and 1095-C in support of the **Employer Mandate** portion of the Affordable Care Act. Note this functionality is only enabled for legal entities in the United States.</span></span>

## <a name="getting-started"></a><span data-ttu-id="02135-105">Aan de slag</span><span class="sxs-lookup"><span data-stu-id="02135-105">Getting started</span></span>
<span data-ttu-id="02135-106">Wanneer u begint informatie aan te geven via de formulieren 1095-B en 1095 C, moet u eerst een of meer ACA-dekkingsgroepen maken.</span><span class="sxs-lookup"><span data-stu-id="02135-106">When beginning to track information to report on forms 1095-B and 1095-C, you must first create one or more Affordable Care coverage groups.</span></span> <span data-ttu-id="02135-107">Deze ACA-dekkingsgroepen worden gebruikt om het dekkingsaanbod aan te geven dat aan een werknemer is verstrekt, het werknemersgedeelte van de laagste maandelijkse premie (als de kosten boven de federale armoedegrens ligt), evenals de Safe Harbor (indien toepasselijk) waar de werkgever gebruik van maakt.</span><span class="sxs-lookup"><span data-stu-id="02135-107">These Affordable Care coverage groups will be used to indicate the offer of coverage that was provided to an employee, the employee’s share of the lowest cost monthly premium (if the cost is above the federal poverty line) as well as Safe Harbor used by the employer, if applicable.</span></span> <span data-ttu-id="02135-108">Wanneer u ACA-groepen gebruikt, kunt u de informatie voor deze velden beheren zonder dat u elk werknemersdossier hoeft door te werken, zolang de omstandigheden identiek zijn.</span><span class="sxs-lookup"><span data-stu-id="02135-108">Using Affordable Care Act groups enables you to manage the information for these fields without needing to touch every employee record where the conditions are the same.</span></span> <span data-ttu-id="02135-109">Daarnaast kunnen ACA-dekkingsgroepen eenvoudig worden toegewezen aan een of meerdere werknemers, door middel van de functie Groepsgewijze toewijzing op de pagina.</span><span class="sxs-lookup"><span data-stu-id="02135-109">In addition, Affordable Care coverage groups can easily be assigned to one or more employees using the Mass assign functionality on the page.</span></span>

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a><span data-ttu-id="02135-110">Meerdere versies van een dekkingsgroep onderhouden</span><span class="sxs-lookup"><span data-stu-id="02135-110">Maintaining multiple versions of a coverage group</span></span>
<span data-ttu-id="02135-111">U kunt meerdere versies van een dekkingsgroep aanhouden, zodat u wijzigingen kunt aanbrengen die de informatie van de groep actueel houdt zonder dat u een nieuwe groep hoeft te maken en werknemers daaraan toewijst, wanneer iets wijzigt in uw organisatie of in secundaire arbeidsvoorwaarden die u aanbiedt.</span><span class="sxs-lookup"><span data-stu-id="02135-111">You can maintain multiple versions of any coverage group, which allows you to make changes that keep the group’s information current, without having to create a new group and reassign employees to it when something changes in your organization or in the benefits that are offered.</span></span> 

<span data-ttu-id="02135-112">Nadat u de benodigde ACA-dekkingsgroepen hebt gemaakt, kunt u de groepen in bulk toewijzen aan werknemers die met behulp van de functie **Groepsgewijze toewijzing** op de pagina, of u kunt voor iedere werknemer aangeven of ACA-informatie moet worden getraceerd en gerapporteerd en ook de werknemer toewijzen aan een ACA-dekkingsgroep.</span><span class="sxs-lookup"><span data-stu-id="02135-112">After you’ve created the Affordable Care coverage groups that you need, you can choose to mass assign the groups to employees using the **Mass assignment** functionality on the page, or you can go to each employee and indicate whether ACA information needs to tracked and reported for that employee as well as assigning the employee to an Affordable Care coverage group.</span></span>

<span data-ttu-id="02135-113">Als u ACA-dekkingsinformatie niet hoeft bij te houden of te rapporteren voor een werknemer, bijvoorbeeld als deze een parttime-werknemer is, kunt u het veld **Dekking rapporteren** instellen op Nee.</span><span class="sxs-lookup"><span data-stu-id="02135-113">If affordable care coverage information doesn’t need to be tracked or reported for an employee, for example if they are a part-time employee, the **Report coverage** field could be set to No.</span></span> <span data-ttu-id="02135-114">Hoewel elke werknemer waarvoor u ACA-gegevens moet bijhouden, moet worden toegewezen aan een ACA-dekkingsgroep, kunt u nog steeds de opties **Dekkingsaanbod**, **Werknemersdeel van kosten** en **Safe Harbor** wijzigen voor elke maand (of alle maanden) waarin andere waarden nodig zijn dan de waarden die zijn ingevoerd in de ACA-dekkingsgroep.</span><span class="sxs-lookup"><span data-stu-id="02135-114">Although each employee for which ACA information needs to be tracked needs to be assigned to an Affordable Care coverage group, you can still change the **Offer of coverage**, **Employee share of cost** and **Safe Harbor** options for any month – or months – that may need different values than those entered in the Affordable Care coverage group.</span></span>

<span data-ttu-id="02135-115">Als u uitzonderingen wilt invoeren voor een of meer van de ACA-dekkingsgroepwaarden, klikt u op de koppeling Dekking betaalbare zorg op de pagina Medewerkergegevens, die u vindt onder de sectie Aanvullende gegevens op het tabblad Dienstverband.</span><span class="sxs-lookup"><span data-stu-id="02135-115">To enter exceptions to any of the Affordable Care coverage group values, click on the Affordable Care Coverage link found on the Worker detail page, which is under the Additional information section on the Employment tab.</span></span>

## <a name="reporting-health-care-coverage"></a><span data-ttu-id="02135-116">Gezondheidszorgdekking rapporteren</span><span class="sxs-lookup"><span data-stu-id="02135-116">Reporting health care coverage</span></span>
<span data-ttu-id="02135-117">Niet alleen moet u bijhouden of en zo ja, welke dekking is aangeboden aan een full-time werknemer; ook moet, als de werkgever meebetaalt aan interne zorgverzekering waarvoor de werknemer is aangemeld (ongeacht of deze full-time of part-time is), aanvullende informatie worden aangegeven via het formulier 1095-C.</span><span class="sxs-lookup"><span data-stu-id="02135-117">In addition to tracking what if any health insurance coverage was offered to a full-time employee, if the employer offers employer-sponsored self-insured health coverage for which the employee is enrolled (regardless of whether their employment status is full-time or part-time), additional information needs to be reported on the 1095-C.</span></span> <span data-ttu-id="02135-118">Elke werknemer (inclusief gezinsleden) die valt onder door de werkgever gesponsorde vergoedingsschema's moet worden vermeld in het rapport voor de maanden waarin zij verzekerd waren.</span><span class="sxs-lookup"><span data-stu-id="02135-118">Each employee (including dependents) covered by the employer-sponsored benefit plans needs to be included on the report for the months they were covered.</span></span> 

<span data-ttu-id="02135-119">U kunt voor elk vergoedingsschema bepalen of het moet worden aangegeven door het selectievakje **Aan te geven voor ACA** in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="02135-119">You can indicate whether or not each Benefit plan must be reported by selecting the **ACA reportable** check box.</span></span>

<span data-ttu-id="02135-120">Als werknemers er daarnaast voor kiezen om een of meerdere gezinsleden onder een van de vergoedingen te laten vallen, kunt u voor elke werknemer apart aangeven op welke datums het gezinslid was verzekerd op de pagina Vergoedingen onderhouden.</span><span class="sxs-lookup"><span data-stu-id="02135-120">In addition, if employees have chosen to have any of their dependents covered under a benefit you can indicate the dates the dependent was covered for each employee on the Maintain benefits page.</span></span> <span data-ttu-id="02135-121">Om aan te geven dat het gezinslid wordt gedekt door de vergoeding, kiest u de knop bewerken in het actievenster van het sneltabblad Afhankelijken.</span><span class="sxs-lookup"><span data-stu-id="02135-121">To indicate that the dependent is covered under the benefit, choose the Edit button in the action pane of the Dependents FastTab.</span></span>

<span data-ttu-id="02135-122">Op de pagina **Datumbeheer dekking afhankelijke** kunt u opgeven op welke datums de afhankelijke is gedekt door de vergoeding.</span><span class="sxs-lookup"><span data-stu-id="02135-122">On the **Dependent coverage date manager** page, you can indicate the dates the dependent was covered by the benefit.</span></span> <span data-ttu-id="02135-123">Wanneer u datums op deze pagina invoert, wordt automatisch het selectievakje **Gedekt** op de pagina **Vergoedingen onderhouden** ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="02135-123">Entering dates on this page will automatically select the **Covered** checkbox on the **Maintain benefits** page.</span></span>

## <a name="generate-1095b-and-1095c-forms"></a><span data-ttu-id="02135-124">De formulieren 1095-B en 1095-C genereren</span><span class="sxs-lookup"><span data-stu-id="02135-124">Generate 1095B and 1095C forms</span></span>
<span data-ttu-id="02135-125">U kunt ook de formulier 1095-B en 1095-C genereren in het product en distribueren naar uw werknemers.</span><span class="sxs-lookup"><span data-stu-id="02135-125">You can also generate 109-B and 1095-C forms from with in the product, and distribute them to each of your employees.</span></span> <span data-ttu-id="02135-126">U kunt ook vanuit het systeem het formulier 1095-C en de bijbehorende 1094-C-verzendbestanden elektronisch genereren, waarmee u het geheel naar de IRS kunt verzenden.</span><span class="sxs-lookup"><span data-stu-id="02135-126">Electronically generating 1095-C and the corresponding 1094-C transmittal files which can be used to send to the IRS, can also be generated from the system.</span></span>  

<span data-ttu-id="02135-127">Bij het genereren van het 1095-C-formulier geeft u het betreffende belastingjaar op en geeft u aan of bsn-nummers moeten worden gemaskeerd.</span><span class="sxs-lookup"><span data-stu-id="02135-127">When generating the 1095-C form, enter in the appropriate tax year and indicate if social security numbers should be masked.</span></span> <span data-ttu-id="02135-128">Als u 1095-C-formulieren voor meer dan 500 werknemers afdrukt, ontvangt u meer dan één PDF-bestand.</span><span class="sxs-lookup"><span data-stu-id="02135-128">If you are printing 1095-C forms for more than 500 employees, you will receive more than one PDF file.</span></span> <span data-ttu-id="02135-129">Het is raadzaam de waarde voor **Maximale bestandsgrootte** in het venster **Parameters voor documentbeheer** te verhogen naar 150 MB.</span><span class="sxs-lookup"><span data-stu-id="02135-129">It’s recommended that you increase the **Maximum file size** in the **Document management parameters** window to 150 MB.</span></span>

## <a name="viewing-information"></a><span data-ttu-id="02135-130">Informatie weergeven</span><span class="sxs-lookup"><span data-stu-id="02135-130">Viewing information</span></span>
<span data-ttu-id="02135-131">Op de pagina **Dekking betaalbare zorg werknemer** kunt u zien welke werknemers zijn toegewezen aan de verschillende dekkingsgroepen, welke werknemers niet hoeven te worden opgenomen in een rapport en welke werknemers niet zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="02135-131">You can use the **Worker Affordable Care coverage** page to see which employees have been assigned to each coverage group, which employees don’t need to be included on a report, and which employees are unassigned.</span></span>

<span data-ttu-id="02135-132">Als een van de standaardwaarden van de ACA-dekkingsgroep is overschreven, wordt dit aangegeven met een asterisk naast de gewijzigde waarde.</span><span class="sxs-lookup"><span data-stu-id="02135-132">If any of the default values from the Affordable Care coverage group have been overridden an asterisk will appear next to the value that was changed.</span></span> <span data-ttu-id="02135-133">Als de waarden voor alle twaalf maanden hetzelfde zijn en niet zijn overschreven, wordt de waarde weergegeven in de kolom **Alle 12 maanden**.</span><span class="sxs-lookup"><span data-stu-id="02135-133">If the values for all 12 months are the same and haven’t been overridden, the value will print in the **All 12 months** column.</span></span>

<span data-ttu-id="02135-134">In het informatievenster kunt u ook zien welke werknemers zijn gemarkeerd als niet te rapporteren volgens de ACA, wat inhoudt dat u niet hoeft bij te houden of dekking is aangeboden en hen ook geen formulier 1095-C hoeft te verstrekken aan het einde van het jaar.</span><span class="sxs-lookup"><span data-stu-id="02135-134">You can also use the inquiry window to understand which employees have been flagged as not ACA reportable, meaning you don’t need to track whether coverage was offered to them and will not need to issue a 1095-C to them at the end of the year.</span></span> <span data-ttu-id="02135-135">Als u **Niet aan te geven onder ACA** selecteert in het veld **Filteren op**, kunt u een lijst met alle werknemers genereren die zijn gemarkeerd om geen 1095-C te ontvangen.</span><span class="sxs-lookup"><span data-stu-id="02135-135">By selecting **Not ACA reportable** in the **Filter by** field, you can generate a list of all employees that have been flagged to not receive a 1095-C.</span></span>

<span data-ttu-id="02135-136">Naast een lijst met werknemers die u niet onder de ACA hoeft aan te geven, kunt u ook alle werknemers zien die niet zijn toegewezen (zonder waarde in het veld **ACA-dekking aangeven**) of die zijn toegewezen aan een ACA-dekkingsgroep die is verlopen voor het jaar dat is geselecteerd in het veld **Jaar**.</span><span class="sxs-lookup"><span data-stu-id="02135-136">In addition to viewing a list of employees that are not ACA reportable, you can also view any employees who are unassigned (the **ACA Report coverage** field is empty) or that have been assigned to an Affordable Care coverage group that is expired for the year selected in the **Year** field.</span></span>

<span data-ttu-id="02135-137">U kunt via een van de filteropties gegenereerde lijsten met werknemers naar Excel exporteren.</span><span class="sxs-lookup"><span data-stu-id="02135-137">You can export lists of employees that were generated using any of the filtering options to Excel.</span></span>

<span data-ttu-id="02135-138">Als u gedekte personen moet aangeven omdat u als werkgever interne verzekering aanbiedt, kunt u ook alle afhankelijken zien die zijn gedekt onder vergoedingsplannen die zijn gemarkeerd als **Aan te geven voor ACA**, door de actie Gezinsdekking weergeven in de actievensterstrook te kiezen.</span><span class="sxs-lookup"><span data-stu-id="02135-138">If you need to report covered individuals because as an employer you provide self-insured coverage you can also view any dependents covered under benefit plans that have been marked as **ACA reportable** by selecting the View Dependent coverage action on the action pane strip.</span></span>

<span data-ttu-id="02135-139">**Opmerking**: Alleen vergoedingen waarvan het plan is gemarkeerd als **Aan te geven voor ACA** worden weergegeven in het informatievenster.</span><span class="sxs-lookup"><span data-stu-id="02135-139">**Note:** Only benefits whose plan has been marked as **ACA reportable** will display in the inquiry window.</span></span>