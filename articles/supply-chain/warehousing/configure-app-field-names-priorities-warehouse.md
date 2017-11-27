---
title: Veldnamen in magazijnapp configureren
description: "In dit onderwerp wordt beschreven hoe u veldnamen en prioriteiten van de magazijnapp kunt definiëren en configureren in Finance and Operations."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2fbf9d84fa0fec32004936542003115cf580d91c
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="configure-app-field-names-in-warehousing-app"></a><span data-ttu-id="d5458-103">Veldnamen in magazijnapp configureren</span><span class="sxs-lookup"><span data-stu-id="d5458-103">Configure app field names in Warehousing app</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d5458-104">In dit onderwerp wordt beschreven hoe u veldnamen en prioriteiten van de magazijnapp kunt definiëren en configureren in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d5458-104">This topic describes how to define and configure warehouse app field names and priorities in Finance and Operations.</span></span> 

<span data-ttu-id="d5458-105">**Opmerking:** dit onderwerp is van toepassing op functies in Magazijnbeheer.</span><span class="sxs-lookup"><span data-stu-id="d5458-105">**Note:** This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="d5458-106">Het geldt niet voor functies in Voorraadbeheer.</span><span class="sxs-lookup"><span data-stu-id="d5458-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="d5458-107">Finance and Operations - Magazijnbeheer is een toepassing waarmee u magazijntaken kunt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="d5458-107">Finance and Operations - Warehousing is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="d5458-108">U kunt de in de app gebruikte veldnamen definiëren en configureren en u kunt ook de prioriteit configureren waaraan de veldnamen moeten worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="d5458-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="d5458-109">In dit onderwerp wordt uitgelegd hoe u deze veldnamen en prioriteiten van de magazijnapp kunt definiëren en configureren en hoe ze worden gebruikt in Finance and Operations - Magazijnbeheer.</span><span class="sxs-lookup"><span data-stu-id="d5458-109">This topic explains how to define and configure these warehouse app field names and priorities, and how they are used in Finance and Operations - Warehousing.</span></span> <span data-ttu-id="d5458-110">Raadpleeg voor gedetailleerde informatie over het configureren van de verbinding met Dynamics 365 for Finance and Operations - Magazijnbeheer, de zelfstudie [Dynamics 365 for Finance and Operations - Magazijnbeheer installeren en configureren](install-configure-warehousing-app.md).</span><span class="sxs-lookup"><span data-stu-id="d5458-110">For detailed information about how to configure the connection to Finance and Operations  - Warehousing, refer to the tutorial [Install and configure Finance and Operations - Warehousing](install-configure-warehousing-app.md).</span></span>

<a name="configure-warehouse-app-field-names"></a><span data-ttu-id="d5458-111">Veldnamen van magazijnapp configureren</span><span class="sxs-lookup"><span data-stu-id="d5458-111">Configure warehouse app field names</span></span>
===================================

<span data-ttu-id="d5458-112">Wanneer u Finance and Operations - Magazijnbeheer op uw mobiele apparaat gebruikt, kunt u configureren hoe metagegevens moeten worden weergegeven op uw apparaat op de pagina **Veldnamen magazijnapp**.</span><span class="sxs-lookup"><span data-stu-id="d5458-112">When you use Finance and Operations - Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="d5458-113">Selecteer in een nieuw bedrijf in Finance and Operations **Standaardinstelling maken** om alle veldnamen te genereren die worden gebruikt in de magazijnworkflows van het mobiele apparaat en wijs er vervolgens een gewenste invoermodus en invoertype aan toe.</span><span class="sxs-lookup"><span data-stu-id="d5458-113">In a new company in Finance and Operations, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="d5458-114">Nadat u alle veldnamen hebt gegenereerd, kunt u de volgende invoeropties selecteren.</span><span class="sxs-lookup"><span data-stu-id="d5458-114">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d5458-115">Optie</span><span class="sxs-lookup"><span data-stu-id="d5458-115">Option</span></span></th>
<th><span data-ttu-id="d5458-116">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="d5458-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d5458-117">Geprefereerde invoermethode</span><span class="sxs-lookup"><span data-stu-id="d5458-117">Preferred input mode</span></span></td>
<td><span data-ttu-id="d5458-118">Met deze optie wordt bepaald of het veld Scannen of een invoerveld voor handmatige invoer moet worden weergegeven voor de geselecteerde veldnaam.</span><span class="sxs-lookup"><span data-stu-id="d5458-118">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="d5458-119">Dit is handig om velden te onderscheiden, afhankelijk van de vraag of er streepjescodes voor het veld worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d5458-119">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="d5458-120"><strong>Opmerking:</strong> voor veldnamen waarvan de gewenste invoermodus is ingesteld op <strong>Scannen</strong>, kunt u gegevens handmatig invoeren als de streepjescode onleesbaar of is beschadigd is.</span><span class="sxs-lookup"><span data-stu-id="d5458-120"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5458-121">Invoertype</span><span class="sxs-lookup"><span data-stu-id="d5458-121">Input type</span></span></td>
<td><span data-ttu-id="d5458-122">Met deze optie wordt bepaald welk invoertype moet worden gebruikt voor de geselecteerde veldnaam.</span><span class="sxs-lookup"><span data-stu-id="d5458-122">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="d5458-123">Er zijn vier opties beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="d5458-123">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="d5458-124"><strong>Selectie</strong> - bevat een lijst met opties waaruit u kunt kiezen.</span><span class="sxs-lookup"><span data-stu-id="d5458-124"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="d5458-125">Veldnamen met deze optie kunnen niet worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="d5458-125">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="d5458-126"><strong>Datum</strong> - veldnamen die zijn opgegeven als datum, bevatten een datumnotatie met het label.</span><span class="sxs-lookup"><span data-stu-id="d5458-126"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="d5458-127">Aan de hand hiervan kunnen magazijnmedewerkers zien in welke notatie de datum moet worden ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="d5458-127">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="d5458-128">Veldnamen met deze optie kunnen niet worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="d5458-128">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="d5458-129"><strong>Alfa</strong> - als deze optie is geselecteerd, wordt het toetsenbord van het apparaat gebruikt bij het handmatig invoeren van gegevens in de app.</span><span class="sxs-lookup"><span data-stu-id="d5458-129"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="d5458-130">De toetsenbordervaring kan worden gewijzigd. Dit hangt af van het apparaat dat wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d5458-130">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="d5458-131"><strong>Numeriek</strong> - voor veldnamen waarin alleen numerieke invoer wordt gebruikt, kunt u deze optie selecteren om een aangepast numeriek toetsenblok weer te geven met het invoerveld in plaats van het toetsenbord van het apparaat.</span><span class="sxs-lookup"><span data-stu-id="d5458-131"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<a name="configure-warehouse-app-field-priority"></a><span data-ttu-id="d5458-132">Veldprioriteit van magazijnapp configureren</span><span class="sxs-lookup"><span data-stu-id="d5458-132">Configure warehouse app field priority</span></span>
======================================

<span data-ttu-id="d5458-133">Op de pagina **Veldprioriteit van magazijnapp** kunt u veldnamen in verschillende prioriteitsgroepen plaatsen.</span><span class="sxs-lookup"><span data-stu-id="d5458-133">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="d5458-134">Hierdoor kunt u bepalen welke informatie moet worden weergegeven op de hoofdtaakpagina wanneer magazijnmedewerkers taken uitvoeren met de app.</span><span class="sxs-lookup"><span data-stu-id="d5458-134">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="d5458-135">Als u op **Standaardinstelling maken** klikt, wordt een standaardset prioriteitsgroepen gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="d5458-135">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="d5458-136">Het is mogelijk zoveel prioriteitsgroepen te maken als nodig is, maar slechts drie prioriteitsgroepen worden op de taakpagina weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d5458-136">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="d5458-137">Als Finance and Operations metagegevens naar de app verzendt, wordt aan elk veld een relatieve prioriteit toegewezen, afhankelijk van de bijbehorende prioriteitsgroep. In de app worden de eerste prioriteitsgroepen in de metagegevens op de taakpagina weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d5458-137">When Finance and Operations sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="d5458-138">De rest van de overlopende metagegevens wordt weergegeven op een secundaire detailpagina.</span><span class="sxs-lookup"><span data-stu-id="d5458-138">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="d5458-139">De volgende tabel bevat een voorbeeld van vijf prioriteitsgroepen.</span><span class="sxs-lookup"><span data-stu-id="d5458-139">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d5458-140">Prioriteitsgroep</span><span class="sxs-lookup"><span data-stu-id="d5458-140">Priority group</span></span></th>
<th><span data-ttu-id="d5458-141">Toegewezen velden</span><span class="sxs-lookup"><span data-stu-id="d5458-141">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="d5458-142">Prioriteit 10</span><span class="sxs-lookup"><span data-stu-id="d5458-142">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="d5458-143">Artikel</span><span class="sxs-lookup"><span data-stu-id="d5458-143">Item</span></span></li>
<li><span data-ttu-id="d5458-144">Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="d5458-144">Quantity</span></span></li>
<li><span data-ttu-id="d5458-145">Maateenheid</span><span class="sxs-lookup"><span data-stu-id="d5458-145">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="d5458-146">Prioriteit 20</span><span class="sxs-lookup"><span data-stu-id="d5458-146">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="d5458-147">Clusterpositie</span><span class="sxs-lookup"><span data-stu-id="d5458-147">Cluster position</span></span></li>
<li><span data-ttu-id="d5458-148">Cluster</span><span class="sxs-lookup"><span data-stu-id="d5458-148">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="d5458-149">Prioriteit 30</span><span class="sxs-lookup"><span data-stu-id="d5458-149">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="d5458-150">Artikelomschrijving.</span><span class="sxs-lookup"><span data-stu-id="d5458-150">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="d5458-151">Prioriteit 40</span><span class="sxs-lookup"><span data-stu-id="d5458-151">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="d5458-152">Configuratie</span><span class="sxs-lookup"><span data-stu-id="d5458-152">Configuration</span></span></li>
<li><span data-ttu-id="d5458-153">Kleur</span><span class="sxs-lookup"><span data-stu-id="d5458-153">Color</span></span></li>
<li><span data-ttu-id="d5458-154">Grootte</span><span class="sxs-lookup"><span data-stu-id="d5458-154">Size</span></span></li>
<li><span data-ttu-id="d5458-155">Opmaakmodel</span><span class="sxs-lookup"><span data-stu-id="d5458-155">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="d5458-156">Prioriteit 50</span><span class="sxs-lookup"><span data-stu-id="d5458-156">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="d5458-157">Locatie</span><span class="sxs-lookup"><span data-stu-id="d5458-157">Location</span></span></li>
<li><span data-ttu-id="d5458-158">Nummerplaat</span><span class="sxs-lookup"><span data-stu-id="d5458-158">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d5458-159">Als een magazijnmedewerker bijvoorbeeld een taak uitvoert op een mobiel apparaat, als de metagegevens die worden weergegeven in de app uit de volgende velden bestaan:</span><span class="sxs-lookup"><span data-stu-id="d5458-159">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="d5458-160">Artikel</span><span class="sxs-lookup"><span data-stu-id="d5458-160">Item</span></span>
-   <span data-ttu-id="d5458-161">Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="d5458-161">Quantity</span></span>
-   <span data-ttu-id="d5458-162">Maateenheid</span><span class="sxs-lookup"><span data-stu-id="d5458-162">Unit of measure</span></span>
-   <span data-ttu-id="d5458-163">Artikelomschrijving.</span><span class="sxs-lookup"><span data-stu-id="d5458-163">Item description</span></span>
-   <span data-ttu-id="d5458-164">Grootte en locatie</span><span class="sxs-lookup"><span data-stu-id="d5458-164">Size and Location</span></span>

<span data-ttu-id="d5458-165">Op basis van de instellingen van de veldprioriteit van de magazijnapp in de bovenstaande tabel worden de volgende 3 rijen met gegevens weergegeven op de taakpagina:</span><span class="sxs-lookup"><span data-stu-id="d5458-165">Based on the warehouse app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="d5458-166">Rij 1: Artikel, Hoeveelheid, Maateenheid</span><span class="sxs-lookup"><span data-stu-id="d5458-166">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="d5458-167">Rij 2: Artikelomschrijving</span><span class="sxs-lookup"><span data-stu-id="d5458-167">Row 2: Item description</span></span>
-   <span data-ttu-id="d5458-168">Rij 3: Grootte</span><span class="sxs-lookup"><span data-stu-id="d5458-168">Row 3: Size</span></span>

<span data-ttu-id="d5458-169">De resterende metagegevens, bijvoorbeeld Locatie, worden niet weergegeven op de taakpagina, maar worden op een detailpagina weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d5458-169">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="d5458-170">Raadpleeg voor meer informatie en voorbeelden van de gebruikersinterface het blogbericht [Finance and Operations - Magazijnbeheer aankondigen](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span><span class="sxs-lookup"><span data-stu-id="d5458-170">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

<a name="see-also"></a><span data-ttu-id="d5458-171">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d5458-171">See also</span></span>
--------

[<span data-ttu-id="d5458-172">Microsoft Dynamics 365 for Finance and Operations - Warehousing installeren en configureren</span><span class="sxs-lookup"><span data-stu-id="d5458-172">Install and configure Microsoft Dynamics 365 for Finance and Operations – Warehousing</span></span>](install-configure-warehousing-app.md)




