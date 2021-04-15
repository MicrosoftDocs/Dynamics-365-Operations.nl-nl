---
title: Velden configureren voor de mobiele app Magazijnbeheer
description: In dit onderwerp wordt beschreven hoe u veldnamen en prioriteiten van velden die worden weergegeven in de mobiele app Magazijnbeheer kunt definiëren en configureren.
author: MarkusFogelberg
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c6ed726536085b836f4014c59ea8df4755577ab5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808817"
---
# <a name="configure-fields-for-the-warehouse-management-mobile-app"></a><span data-ttu-id="3a958-103">Velden configureren voor de mobiele app Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="3a958-103">Configure fields for the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3a958-104">In dit onderwerp wordt beschreven hoe u veldnamen en prioriteiten van velden die worden weergegeven in de mobiele app Magazijnbeheer kunt definiëren en configureren.</span><span class="sxs-lookup"><span data-stu-id="3a958-104">This topic describes how to define and configure names and priorities of fields shown in the Warehouse Management mobile app.</span></span>

> [!NOTE]
> <span data-ttu-id="3a958-105">Dit onderwerp is van toepassing op functies in Magazijnbeheer.</span><span class="sxs-lookup"><span data-stu-id="3a958-105">This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="3a958-106">Het geldt niet voor functies in Voorraadbeheer.</span><span class="sxs-lookup"><span data-stu-id="3a958-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="3a958-107">De mobiele app Magazijnbeheer is een toepassing waarmee u magazijntaken kunt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="3a958-107">The Warehouse Management mobile app is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="3a958-108">U kunt de in de app gebruikte veldnamen definiëren en configureren en u kunt ook de prioriteit configureren waaraan de veldnamen moeten worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="3a958-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="3a958-109">In dit onderwerp wordt uitgelegd hoe u deze veldnamen en prioriteiten van de mobiele app Magazijnbeheer kunt definiëren en configureren en hoe ze worden gebruikt in Magazijnbeheer.</span><span class="sxs-lookup"><span data-stu-id="3a958-109">This topic explains how to define and configure these Warehouse Management mobile app field names and priorities, and how they are used.</span></span>

## <a name="configure-warehouse-app-field-names"></a><span data-ttu-id="3a958-110">Veldnamen van magazijnapp configureren</span><span class="sxs-lookup"><span data-stu-id="3a958-110">Configure warehouse app field names</span></span>

<span data-ttu-id="3a958-111">Wanneer u Magazijnbeheer op uw mobiele apparaat gebruikt, kunt u configureren hoe metagegevens moeten worden weergegeven op uw apparaat op de pagina **Veldnamen magazijnapp**.</span><span class="sxs-lookup"><span data-stu-id="3a958-111">When you use Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="3a958-112">Selecteer in een nieuw bedrijf **Standaardinstelling maken** om alle veldnamen te genereren die worden gebruikt in de magazijnworkflows van het mobiele apparaat en wijs er vervolgens een gewenste invoermodus en invoertype aan toe.</span><span class="sxs-lookup"><span data-stu-id="3a958-112">In a new company, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="3a958-113">Nadat u alle veldnamen hebt gegenereerd, kunt u de volgende invoeropties selecteren.</span><span class="sxs-lookup"><span data-stu-id="3a958-113">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3a958-114">Optie</span><span class="sxs-lookup"><span data-stu-id="3a958-114">Option</span></span></th>
<th><span data-ttu-id="3a958-115">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="3a958-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3a958-116">Geprefereerde invoermethode</span><span class="sxs-lookup"><span data-stu-id="3a958-116">Preferred input mode</span></span></td>
<td><span data-ttu-id="3a958-117">Met deze optie wordt bepaald of het veld Scannen of een invoerveld voor handmatige invoer moet worden weergegeven voor de geselecteerde veldnaam.</span><span class="sxs-lookup"><span data-stu-id="3a958-117">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="3a958-118">Dit is handig om velden te onderscheiden, afhankelijk van de vraag of er streepjescodes voor het veld worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="3a958-118">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="3a958-119"><strong>Opmerking:</strong> voor veldnamen waarvan de gewenste invoermodus is ingesteld op <strong>Scannen</strong>, kunt u gegevens handmatig invoeren als de streepjescode onleesbaar of is beschadigd is.</span><span class="sxs-lookup"><span data-stu-id="3a958-119"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a958-120">Invoertype</span><span class="sxs-lookup"><span data-stu-id="3a958-120">Input type</span></span></td>
<td><span data-ttu-id="3a958-121">Met deze optie wordt bepaald welk invoertype moet worden gebruikt voor de geselecteerde veldnaam.</span><span class="sxs-lookup"><span data-stu-id="3a958-121">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="3a958-122">Er zijn vier opties beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="3a958-122">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="3a958-123"><strong>Selectie</strong> - bevat een lijst met opties waaruit u kunt kiezen.</span><span class="sxs-lookup"><span data-stu-id="3a958-123"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="3a958-124">Veldnamen met deze optie kunnen niet worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="3a958-124">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="3a958-125"><strong>Datum</strong> - veldnamen die zijn opgegeven als datum, bevatten een datumnotatie met het label.</span><span class="sxs-lookup"><span data-stu-id="3a958-125"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="3a958-126">Aan de hand hiervan kunnen magazijnmedewerkers zien in welke notatie de datum moet worden ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="3a958-126">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="3a958-127">Veldnamen met deze optie kunnen niet worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="3a958-127">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="3a958-128"><strong>Alfa</strong> - als deze optie is geselecteerd, wordt het toetsenbord van het apparaat gebruikt bij het handmatig invoeren van gegevens in de app.</span><span class="sxs-lookup"><span data-stu-id="3a958-128"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="3a958-129">De toetsenbordervaring kan worden gewijzigd. Dit hangt af van het apparaat dat wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="3a958-129">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="3a958-130"><strong>Numeriek</strong> - voor veldnamen waarin alleen numerieke invoer wordt gebruikt, kunt u deze optie selecteren om een aangepast numeriek toetsenblok weer te geven met het invoerveld in plaats van het toetsenbord van het apparaat.</span><span class="sxs-lookup"><span data-stu-id="3a958-130"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a><span data-ttu-id="3a958-131">Veldprioriteit van magazijnapp configureren</span><span class="sxs-lookup"><span data-stu-id="3a958-131">Configure warehouse app field priority</span></span>

<span data-ttu-id="3a958-132">Op de pagina **Veldprioriteit van magazijnapp** kunt u veldnamen in verschillende prioriteitsgroepen plaatsen.</span><span class="sxs-lookup"><span data-stu-id="3a958-132">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="3a958-133">Hierdoor kunt u bepalen welke informatie moet worden weergegeven op de hoofdtaakpagina wanneer magazijnmedewerkers taken uitvoeren met de app.</span><span class="sxs-lookup"><span data-stu-id="3a958-133">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="3a958-134">Als u op **Standaardinstelling maken** klikt, wordt een standaardset prioriteitsgroepen gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="3a958-134">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="3a958-135">Het is mogelijk zoveel prioriteitsgroepen te maken als nodig is, maar slechts drie prioriteitsgroepen worden op de taakpagina weergegeven.</span><span class="sxs-lookup"><span data-stu-id="3a958-135">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="3a958-136">Als het systeem metagegevens naar de app verzendt, wordt aan elk veld een relatieve prioriteit toegewezen, afhankelijk van de bijbehorende prioriteitsgroep. In de app worden de eerste prioriteitsgroepen in de metagegevens op de taakpagina weergegeven.</span><span class="sxs-lookup"><span data-stu-id="3a958-136">When the system sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="3a958-137">De rest van de overlopende metagegevens wordt weergegeven op een secundaire detailpagina.</span><span class="sxs-lookup"><span data-stu-id="3a958-137">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="3a958-138">De volgende tabel bevat een voorbeeld van vijf prioriteitsgroepen.</span><span class="sxs-lookup"><span data-stu-id="3a958-138">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3a958-139">Prioriteitsgroep</span><span class="sxs-lookup"><span data-stu-id="3a958-139">Priority group</span></span></th>
<th><span data-ttu-id="3a958-140">Toegewezen velden</span><span class="sxs-lookup"><span data-stu-id="3a958-140">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="3a958-141">Prioriteit 10</span><span class="sxs-lookup"><span data-stu-id="3a958-141">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="3a958-142">Artikel</span><span class="sxs-lookup"><span data-stu-id="3a958-142">Item</span></span></li>
<li><span data-ttu-id="3a958-143">Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="3a958-143">Quantity</span></span></li>
<li><span data-ttu-id="3a958-144">Maateenheid</span><span class="sxs-lookup"><span data-stu-id="3a958-144">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="3a958-145">Prioriteit 20</span><span class="sxs-lookup"><span data-stu-id="3a958-145">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="3a958-146">Clusterpositie</span><span class="sxs-lookup"><span data-stu-id="3a958-146">Cluster position</span></span></li>
<li><span data-ttu-id="3a958-147">Cluster</span><span class="sxs-lookup"><span data-stu-id="3a958-147">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="3a958-148">Prioriteit 30</span><span class="sxs-lookup"><span data-stu-id="3a958-148">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="3a958-149">Artikelomschrijving.</span><span class="sxs-lookup"><span data-stu-id="3a958-149">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="3a958-150">Prioriteit 40</span><span class="sxs-lookup"><span data-stu-id="3a958-150">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="3a958-151">Configuratie</span><span class="sxs-lookup"><span data-stu-id="3a958-151">Configuration</span></span></li>
<li><span data-ttu-id="3a958-152">Kleur</span><span class="sxs-lookup"><span data-stu-id="3a958-152">Color</span></span></li>
<li><span data-ttu-id="3a958-153">Grootte</span><span class="sxs-lookup"><span data-stu-id="3a958-153">Size</span></span></li>
<li><span data-ttu-id="3a958-154">Opmaakmodel</span><span class="sxs-lookup"><span data-stu-id="3a958-154">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="3a958-155">Prioriteit 50</span><span class="sxs-lookup"><span data-stu-id="3a958-155">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="3a958-156">Locatie</span><span class="sxs-lookup"><span data-stu-id="3a958-156">Location</span></span></li>
<li><span data-ttu-id="3a958-157">Nummerplaat</span><span class="sxs-lookup"><span data-stu-id="3a958-157">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3a958-158">Als een magazijnmedewerker bijvoorbeeld een taak uitvoert op een mobiel apparaat, als de metagegevens die worden weergegeven in de app uit de volgende velden bestaan:</span><span class="sxs-lookup"><span data-stu-id="3a958-158">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="3a958-159">Artikel</span><span class="sxs-lookup"><span data-stu-id="3a958-159">Item</span></span>
-   <span data-ttu-id="3a958-160">Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="3a958-160">Quantity</span></span>
-   <span data-ttu-id="3a958-161">Maateenheid</span><span class="sxs-lookup"><span data-stu-id="3a958-161">Unit of measure</span></span>
-   <span data-ttu-id="3a958-162">Artikelomschrijving.</span><span class="sxs-lookup"><span data-stu-id="3a958-162">Item description</span></span>
-   <span data-ttu-id="3a958-163">Grootte en locatie</span><span class="sxs-lookup"><span data-stu-id="3a958-163">Size and Location</span></span>

<span data-ttu-id="3a958-164">Op basis van de instellingen van de veldprioriteit van de magazijnapp in de bovenstaande tabel worden de volgende 3 rijen met gegevens weergegeven op de taakpagina:</span><span class="sxs-lookup"><span data-stu-id="3a958-164">Based on the warehouse app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="3a958-165">Rij 1: Artikel, Hoeveelheid, Maateenheid</span><span class="sxs-lookup"><span data-stu-id="3a958-165">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="3a958-166">Rij 2: Artikelomschrijving</span><span class="sxs-lookup"><span data-stu-id="3a958-166">Row 2: Item description</span></span>
-   <span data-ttu-id="3a958-167">Rij 3: Grootte</span><span class="sxs-lookup"><span data-stu-id="3a958-167">Row 3: Size</span></span>

<span data-ttu-id="3a958-168">De resterende metagegevens, bijvoorbeeld Locatie, worden niet weergegeven op de taakpagina, maar worden op een detailpagina weergegeven.</span><span class="sxs-lookup"><span data-stu-id="3a958-168">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="3a958-169">Raadpleeg voor meer informatie en voorbeelden van de gebruikersinterface het blogbericht [Finance and Operations - Magazijnbeheer aankondigen](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span><span class="sxs-lookup"><span data-stu-id="3a958-169">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

<a name="additional-resources"></a><span data-ttu-id="3a958-170">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="3a958-170">Additional resources</span></span>
--------

[<span data-ttu-id="3a958-171">De mobiele app Magazijnbeheer installeren en verbinden</span><span class="sxs-lookup"><span data-stu-id="3a958-171">Install and connect the Warehouse Management mobile app</span></span>](../warehousing/install-configure-warehouse-management-app.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]