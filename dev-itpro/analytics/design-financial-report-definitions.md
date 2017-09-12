---
title: "Rapportdefinities in Ontwerper financiële rapporten"
description: Dit artikel bevat informatie over rapportdefinities. Een rapportdefinitie is een rapportonderdeel (of bouwsteen) die gebruikmaakt van een rijdefinitie, een kolomdefinitie en een optionele rapportagestructuurdefinitie om een rapport te maken. Een rapportdefinitie bevat ook opties en instellingen voor het aanpassen van een rapport.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Management Reporter, UnifiedOperations, Core
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 96090a3ae15294d98d6207c8eb4a1e58429ca9eb
ms.contentlocale: nl-nl
ms.lasthandoff: 07/18/2017

---

# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="78e15-105">Rapportdefinities in Ontwerper financiële rapporten</span><span class="sxs-lookup"><span data-stu-id="78e15-105">Report definitions in financial report designer</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="78e15-106">Dit artikel bevat informatie over rapportdefinities.</span><span class="sxs-lookup"><span data-stu-id="78e15-106">This article provides information about report definitions.</span></span> <span data-ttu-id="78e15-107">Een rapportdefinitie is een rapportonderdeel (of bouwsteen) die gebruikmaakt van een rijdefinitie, een kolomdefinitie en een optionele rapportagestructuurdefinitie om een rapport te maken.</span><span class="sxs-lookup"><span data-stu-id="78e15-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="78e15-108">Een rapportdefinitie bevat ook opties en instellingen voor het aanpassen van een rapport.</span><span class="sxs-lookup"><span data-stu-id="78e15-108">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="78e15-109">Een rapportdefinitie is een rapportonderdeel (of bouwsteen) die gebruikmaakt van een rijdefinitie, een kolomdefinitie en een optionele rapportagestructuurdefinitie om een rapport te maken.</span><span class="sxs-lookup"><span data-stu-id="78e15-109">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="78e15-110">Een rapportdefinitie biedt ook opties en instellingen waarmee u een rapport kunt aanpassen.</span><span class="sxs-lookup"><span data-stu-id="78e15-110">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="78e15-111">Nadat u rijdefinities en kolomdefinities hebt gedefinieerd, moet u deze in een rapportdefinitie combineren.</span><span class="sxs-lookup"><span data-stu-id="78e15-111">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="78e15-112">Op dit punt definieert u ook andere aspecten van de definities, zoals het detailniveau en de rapportdatum.</span><span class="sxs-lookup"><span data-stu-id="78e15-112">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="78e15-113">U kunt vervolgens een rapport opslaan en genereren.</span><span class="sxs-lookup"><span data-stu-id="78e15-113">You can then save and generate a report.</span></span> <span data-ttu-id="78e15-114">Financiële rapportage biedt de volgende detailniveaus:</span><span class="sxs-lookup"><span data-stu-id="78e15-114">Financial reporting offers the following levels of detail:</span></span>

-   <span data-ttu-id="78e15-115">Financieel</span><span class="sxs-lookup"><span data-stu-id="78e15-115">Financial</span></span>
-   <span data-ttu-id="78e15-116">Financieel en Rekening</span><span class="sxs-lookup"><span data-stu-id="78e15-116">Financial and Account</span></span>
-   <span data-ttu-id="78e15-117">Financieel, Rekening en Transactie</span><span class="sxs-lookup"><span data-stu-id="78e15-117">Financial, Account, and Transaction</span></span>

<span data-ttu-id="78e15-118">Afhankelijk van hoe de gegevens in het Microsoft Dynamics ERP-systeem worden opgeslagen, zijn transactiedetails mogelijk niet beschikbaar in rapporten.</span><span class="sxs-lookup"><span data-stu-id="78e15-118">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="78e15-119">Een rapportdefinitie maken</span><span class="sxs-lookup"><span data-stu-id="78e15-119">Create a report definition</span></span>
1.  <span data-ttu-id="78e15-120">Klik in Report Designer in het menu **Bestand** op **Nieuw** en selecteer **Rapportdefinitie**.</span><span class="sxs-lookup"><span data-stu-id="78e15-120">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2.  <span data-ttu-id="78e15-121">Geef de gewenste informatie op in de tabbladen **Rapport**, **Uitvoer en distributie** **Kop- en voetteksten** en **Instellingen**.</span><span class="sxs-lookup"><span data-stu-id="78e15-121">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="78e15-122">Inhoud van een rapportdefinitie</span><span class="sxs-lookup"><span data-stu-id="78e15-122">Contents of a report definition</span></span>
<span data-ttu-id="78e15-123">In de volgende tabel worden de tabbladen in een rapportdefinitie beschreven en hoe de gegevens worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="78e15-123">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="78e15-124">Tabblad</span><span class="sxs-lookup"><span data-stu-id="78e15-124">Tab</span></span></th>
<th><span data-ttu-id="78e15-125">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="78e15-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="78e15-126">Rapport</span><span class="sxs-lookup"><span data-stu-id="78e15-126">Report</span></span></td>
<td><span data-ttu-id="78e15-127">Maak een rapport, configureer een rapport of wijzig een bestaand rapport.</span><span class="sxs-lookup"><span data-stu-id="78e15-127">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="78e15-128">Uitvoer en distributie</span><span class="sxs-lookup"><span data-stu-id="78e15-128">Output and Distribution</span></span></td>
<td><span data-ttu-id="78e15-129">Wijzig het uitvoertype en de bestemming van het rapport.</span><span class="sxs-lookup"><span data-stu-id="78e15-129">Change the output type and destination of the report.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="78e15-130">Kop- en voetteksten</span><span class="sxs-lookup"><span data-stu-id="78e15-130">Headers and Footers</span></span></td>
<td><span data-ttu-id="78e15-131">Definieer de kop- en voetteksten voor het rapport en maak deze op.</span><span class="sxs-lookup"><span data-stu-id="78e15-131">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="78e15-132">U kunt bijvoorbeeld tekst of afbeeldingen aan de kop- of voettekst toevoegen.</span><span class="sxs-lookup"><span data-stu-id="78e15-132">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="78e15-133">Financiële rapportage ondersteunt .bmp, .jpg en .png-bestanden voor afbeeldingen.</span><span class="sxs-lookup"><span data-stu-id="78e15-133">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="78e15-134">U kunt ook Autotekstcodes toevoegen om andere informatie, zoals een bedrijfsnaam, rapportnaam of paginanummer, in te voegen.</span><span class="sxs-lookup"><span data-stu-id="78e15-134">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="78e15-135">Instellingen</span><span class="sxs-lookup"><span data-stu-id="78e15-135">Settings</span></span></td>
<td><span data-ttu-id="78e15-136">Geef instellingen voor de rapportdefinitie op, zoals de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="78e15-136">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="78e15-137">Opmaken en afronden van bedragen</span><span class="sxs-lookup"><span data-stu-id="78e15-137">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="78e15-138">Opmaken van detailrapporten</span><span class="sxs-lookup"><span data-stu-id="78e15-138">Format detail reports</span></span></li>
<li><span data-ttu-id="78e15-139">Opmaken van rapportagestructuren</span><span class="sxs-lookup"><span data-stu-id="78e15-139">Format reporting trees</span></span></li>
<li><span data-ttu-id="78e15-140">Genereren van een uitzonderingenrapport</span><span class="sxs-lookup"><span data-stu-id="78e15-140">Generate an exception report</span></span></li>
<li><span data-ttu-id="78e15-141">Opgeven van valutaomrekening</span><span class="sxs-lookup"><span data-stu-id="78e15-141">Specify currency conversion</span></span></li>
<li><span data-ttu-id="78e15-142">Subtotaal en filter van rekeningdetails</span><span class="sxs-lookup"><span data-stu-id="78e15-142">Subtotal and filter account details</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a><span data-ttu-id="78e15-143">Zie ook</span><span class="sxs-lookup"><span data-stu-id="78e15-143">See also</span></span>
--------

[<span data-ttu-id="78e15-144">Financiële rapportage</span><span class="sxs-lookup"><span data-stu-id="78e15-144">Financial reporting</span></span>](financial-reporting-intro.md)




