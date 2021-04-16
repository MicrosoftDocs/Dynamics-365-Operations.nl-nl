---
title: Rapportdefinities in Ontwerper financiële rapporten
description: Dit artikel bevat informatie over rapportdefinities.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 52322453328814b06bacefb4829bb10bf9953186
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755439"
---
# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="171f7-103">Rapportdefinities in Ontwerper financiële rapporten</span><span class="sxs-lookup"><span data-stu-id="171f7-103">Report definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="171f7-104">Dit artikel bevat informatie over rapportdefinities.</span><span class="sxs-lookup"><span data-stu-id="171f7-104">This article provides information about report definitions.</span></span> <span data-ttu-id="171f7-105">Een rapportdefinitie is een rapportonderdeel (of bouwsteen) die gebruikmaakt van een rijdefinitie, een kolomdefinitie en een optionele rapportagestructuurdefinitie om een rapport te maken.</span><span class="sxs-lookup"><span data-stu-id="171f7-105">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="171f7-106">Een rapportdefinitie bevat ook opties en instellingen voor het aanpassen van een rapport.</span><span class="sxs-lookup"><span data-stu-id="171f7-106">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="171f7-107">Een rapportdefinitie is een rapportonderdeel (of bouwsteen) die gebruikmaakt van een rijdefinitie, een kolomdefinitie en een optionele rapportagestructuurdefinitie om een rapport te maken.</span><span class="sxs-lookup"><span data-stu-id="171f7-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="171f7-108">Daarnaast biedt een rapportdefinitie opties en instellingen die u kunt gebruiken voor het aanpassen van een rapport.</span><span class="sxs-lookup"><span data-stu-id="171f7-108">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="171f7-109">Nadat u rijdefinities en kolomdefinities hebt gedefinieerd, moet u deze in een rapportdefinitie combineren.</span><span class="sxs-lookup"><span data-stu-id="171f7-109">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="171f7-110">Op dit punt definieert u ook andere aspecten van de definities, zoals het detailniveau en de rapportdatum.</span><span class="sxs-lookup"><span data-stu-id="171f7-110">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="171f7-111">U kunt vervolgens een rapport opslaan en genereren.</span><span class="sxs-lookup"><span data-stu-id="171f7-111">You can then save and generate a report.</span></span> <span data-ttu-id="171f7-112">Financiële rapportage biedt de volgende detailniveaus:</span><span class="sxs-lookup"><span data-stu-id="171f7-112">Financial reporting offers the following levels of detail:</span></span>

- <span data-ttu-id="171f7-113">Financieel</span><span class="sxs-lookup"><span data-stu-id="171f7-113">Financial</span></span>
- <span data-ttu-id="171f7-114">Financieel en Rekening</span><span class="sxs-lookup"><span data-stu-id="171f7-114">Financial and Account</span></span>
- <span data-ttu-id="171f7-115">Financieel, Rekening en Transactie</span><span class="sxs-lookup"><span data-stu-id="171f7-115">Financial, Account, and Transaction</span></span>

<span data-ttu-id="171f7-116">Afhankelijk van de wijze waarop gegevens worden opgeslagen in het Microsoft Dynamics ERP-systeem, zijn de transactiedetails misschien niet beschikbaar in de rapporten.</span><span class="sxs-lookup"><span data-stu-id="171f7-116">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="171f7-117">Een rapportdefinitie maken</span><span class="sxs-lookup"><span data-stu-id="171f7-117">Create a report definition</span></span>
1. <span data-ttu-id="171f7-118">Klik in Report Designer in het menu **Bestand** op **Nieuw** en selecteer **Rapportdefinitie**.</span><span class="sxs-lookup"><span data-stu-id="171f7-118">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2. <span data-ttu-id="171f7-119">Geef de gewenste informatie op in de tabbladen **Rapport**, **Uitvoer en distributie** **Kop- en voetteksten** en **Instellingen**.</span><span class="sxs-lookup"><span data-stu-id="171f7-119">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="171f7-120">Inhoud van een rapportdefinitie</span><span class="sxs-lookup"><span data-stu-id="171f7-120">Contents of a report definition</span></span>
<span data-ttu-id="171f7-121">In de volgende tabel worden de tabbladen in een rapportdefinitie beschreven en hoe de gegevens worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="171f7-121">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="171f7-122">Tabblad</span><span class="sxs-lookup"><span data-stu-id="171f7-122">Tab</span></span></th>
<th><span data-ttu-id="171f7-123">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="171f7-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="171f7-124">Rapport</span><span class="sxs-lookup"><span data-stu-id="171f7-124">Report</span></span></td>
<td><span data-ttu-id="171f7-125">Maak een rapport, configureer een rapport of wijzig een bestaand rapport.</span><span class="sxs-lookup"><span data-stu-id="171f7-125">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="171f7-126">Uitvoer en distributie</span><span class="sxs-lookup"><span data-stu-id="171f7-126">Output and Distribution</span></span></td>
<td><span data-ttu-id="171f7-127">Wijzig het uitvoertype en de bestemming van het rapport.</span><span class="sxs-lookup"><span data-stu-id="171f7-127">Change the output type and destination of the report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="171f7-128">Kop- en voetteksten</span><span class="sxs-lookup"><span data-stu-id="171f7-128">Headers and Footers</span></span></td>
<td><span data-ttu-id="171f7-129">Definieer de kop- en voetteksten voor het rapport en maak deze op.</span><span class="sxs-lookup"><span data-stu-id="171f7-129">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="171f7-130">U kunt bijvoorbeeld tekst of afbeeldingen aan de kop- of voettekst toevoegen.</span><span class="sxs-lookup"><span data-stu-id="171f7-130">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="171f7-131">Financiële rapportage ondersteunt .bmp, .jpg en .png-bestanden voor afbeeldingen.</span><span class="sxs-lookup"><span data-stu-id="171f7-131">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="171f7-132">U kunt ook Autotekstcodes toevoegen om andere informatie, zoals een bedrijfsnaam, rapportnaam of paginanummer, in te voegen.</span><span class="sxs-lookup"><span data-stu-id="171f7-132">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="171f7-133">Instellingen</span><span class="sxs-lookup"><span data-stu-id="171f7-133">Settings</span></span></td>
<td><span data-ttu-id="171f7-134">Geef instellingen voor de rapportdefinitie op, zoals de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="171f7-134">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="171f7-135">Opmaken en afronden van bedragen</span><span class="sxs-lookup"><span data-stu-id="171f7-135">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="171f7-136">Opmaken van detailrapporten</span><span class="sxs-lookup"><span data-stu-id="171f7-136">Format detail reports</span></span></li>
<li><span data-ttu-id="171f7-137">Opmaken van rapportagestructuren</span><span class="sxs-lookup"><span data-stu-id="171f7-137">Format reporting trees</span></span></li>
<li><span data-ttu-id="171f7-138">Genereren van een uitzonderingenrapport</span><span class="sxs-lookup"><span data-stu-id="171f7-138">Generate an exception report</span></span></li>
<li><span data-ttu-id="171f7-139">Opgeven van valutaomrekening</span><span class="sxs-lookup"><span data-stu-id="171f7-139">Specify currency conversion</span></span></li>
<li><span data-ttu-id="171f7-140">Subtotaal en filter van rekeningdetails</span><span class="sxs-lookup"><span data-stu-id="171f7-140">Subtotal and filter account details</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="171f7-141">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="171f7-141">Additional resources</span></span>

[<span data-ttu-id="171f7-142">Financiële rapportage</span><span class="sxs-lookup"><span data-stu-id="171f7-142">Financial reporting</span></span>](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]