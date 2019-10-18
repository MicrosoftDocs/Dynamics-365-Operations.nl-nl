---
title: Werken met datum en tijd in Microsoft Dynamics 365 Talent
description: Begrijp wat u kunt verwachten wanneer u datum- en tijdvelden gebruikt in Microsoft Dynamics 365 Talent. Krijg inzicht in wat u kunt verwachten wanneer u met datum- en tijdgegevens in een formulier in Talent, een externe bron of Common Data Service werkt.
author: Darinkramer
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-06-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1a1d1a47bfe6bd58b1e1a0d4d46c2133f3bf48ad
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/23/2019
ms.locfileid: "2007962"
---
# <a name="date-and-time-fields-in-talent"></a><span data-ttu-id="e1f23-104">Datum- en tijdvelden in Talent</span><span class="sxs-lookup"><span data-stu-id="e1f23-104">Date and Time fields in Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e1f23-105">**Datum- en tijdvelden** vormen een fundamenteel concept in Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="e1f23-105">**Date and Time** fields are a fundamental concept in Dynamics 365 Talent.</span></span> <span data-ttu-id="e1f23-106">Het is belangrijk om te begrijpen hoe u met **datum- en tijdgegevens** in een Dynamics 365-formulier, Common Data Service en externe bronnen kunt werken.</span><span class="sxs-lookup"><span data-stu-id="e1f23-106">It's important to understand how to work with **Date and Time** data in a Dynamics 365 form, Common Data Service, and external sources.</span></span>

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a><span data-ttu-id="e1f23-107">Het verschil tussen veldgegevenstypen Datum en Datum en tijd</span><span class="sxs-lookup"><span data-stu-id="e1f23-107">Understanding the difference between Date and Date and Time field data types</span></span>

<span data-ttu-id="e1f23-108">Een veld **Datum en tijd** bevat informatie over de tijdzone, het veld **Datum** niet.</span><span class="sxs-lookup"><span data-stu-id="e1f23-108">**Date and Time** fields contain time zone information, while **Date** fields don't.</span></span> <span data-ttu-id="e1f23-109">Een veld **Datum** bevat dezelfde informatie op elke locatie.</span><span class="sxs-lookup"><span data-stu-id="e1f23-109">**Date** fields display the same information in any location.</span></span> <span data-ttu-id="e1f23-110">Wanneer u een datum in een veld **Datum** invoert, wordt diezelfde datum naar de database geschreven.</span><span class="sxs-lookup"><span data-stu-id="e1f23-110">When you enter a date into a **Date** field, Talent writes that same date to the database.</span></span>

<span data-ttu-id="e1f23-111">Wanneer gegevens worden weergegeven in een veld **Datum en tijd**, worden de datum en tijd aangepast op basis van de tijdzone van de gebruiker die is ingesteld in het formulier **Gebruikersopties** (**Algemeen > Instellingen > Gebruikersopties**).</span><span class="sxs-lookup"><span data-stu-id="e1f23-111">When displaying data in a **Date and Time** field, Talent adjusts the date and time based on the user's time zone set in the **User Options** form (**Common > Setup > User Options**).</span></span> <span data-ttu-id="e1f23-112">De datum- en tijdgegevens die u in het veld invoert, zijn mogelijk niet hetzelfde als de gegevens die naar de database worden geschreven.</span><span class="sxs-lookup"><span data-stu-id="e1f23-112">The date and time information you enter in the field might not be the same as the information written to the database.</span></span>

<span data-ttu-id="e1f23-113">[![Het formulier Gebruikersopties](./media/useroptionsform.png)](./media/useroptionsform.png)</span><span class="sxs-lookup"><span data-stu-id="e1f23-113">[![User options form](./media/useroptionsform.png)](./media/useroptionsform.png)</span></span>

## <a name="understanding-date-and-time-fields-in-forms"></a><span data-ttu-id="e1f23-114">Datum- en tijdvelden in formulieren begrijpen</span><span class="sxs-lookup"><span data-stu-id="e1f23-114">Understanding Date and Time fields in forms</span></span> 

<span data-ttu-id="e1f23-115">Wanneer u gegevens in een veld **Datum en tijd** invoert, komen de ingevoerde gegevens op het scherm niet overeen met de gegevens die in de database worden opgeslagen als de tijdzone van de gebruiker niet is ingesteld op UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="e1f23-115">When entering data in a **Date and Time** field, the data displayed on the screen isn't the same as the data stored in the database if the user's time zone isn't set to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="e1f23-116">De gegevens een veld **Datum en tijd** worden altijd als UTC opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="e1f23-116">Data in **Date and Time** fields is always stored as UTC.</span></span>

<span data-ttu-id="e1f23-117">[![Het formulier Medewerker](./media/worker-form.png)](./media/worker-form.png)</span><span class="sxs-lookup"><span data-stu-id="e1f23-117">[![Worker form](./media/worker-form.png)](./media/worker-form.png)</span></span>

## <a name="understand-date-and-time-fields-in-the-database"></a><span data-ttu-id="e1f23-118">Datum- en tijdvelden in de database begrijpen</span><span class="sxs-lookup"><span data-stu-id="e1f23-118">Understand Date and Time fields in the database</span></span> 

<span data-ttu-id="e1f23-119">Wanneer in Talent een waarde voor **Datum en tijd** naar de database wordt geschreven, worden de gegevens in UTC opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="e1f23-119">When Talent writes a **Date and time** value to the database, it stores the data in UTC.</span></span> <span data-ttu-id="e1f23-120">Op deze manier kunnen gebruikers de gegevens in **Datum en tijd** weergeven in relatie tot de tijdzone die is gedefinieerd in hun gebruikersopties.</span><span class="sxs-lookup"><span data-stu-id="e1f23-120">This allows users to see any **Date and Time** data relative to the time zone defined in their user options.</span></span>
 
<span data-ttu-id="e1f23-121">In het vorige voorbeeld is de begintijd een moment, niet een bepaalde datum.</span><span class="sxs-lookup"><span data-stu-id="e1f23-121">In the example above, the start time is a point in time, not a particular date.</span></span> <span data-ttu-id="e1f23-122">Door de tijdzone van de aangemelde gebruiker te wijzigen van GMT + 12:00 in GMT UTC, wordt dezelfde record die net is gemaakt, weergegeven met 30-04-2019 12:00:00 in plaats van 01-05-2019 12:00:00.</span><span class="sxs-lookup"><span data-stu-id="e1f23-122">By changing the time zone of the logged in user from GMT +12:00 to GMT UTC, the same record just created shows 04/30/2019 12:00:00 instead of 05/01/2019 12:00:00.</span></span>
  
<span data-ttu-id="e1f23-123">In het onderstaande voorbeeld wordt het dienstverband van medewerker 000724 op hetzelfde moment actief, ongeacht de tijdzone.</span><span class="sxs-lookup"><span data-stu-id="e1f23-123">In the example below, employee 000724’s employment becomes active at the same time regardless of time zone.</span></span> <span data-ttu-id="e1f23-124">De medewerker wordt actief op 30-04-2019 in de tijdzone GMT, wat hetzelfde is als 01-05-2019 in de tijdzone GMT+12:00.</span><span class="sxs-lookup"><span data-stu-id="e1f23-124">The employee will be active on 04/30/2019 in the GMT time zone, which is the same as 05/01/2019 in GMT+12:00 time zone.</span></span> <span data-ttu-id="e1f23-125">Beide verwijzen naar hetzelfde moment en niet naar een bepaalde datum.</span><span class="sxs-lookup"><span data-stu-id="e1f23-125">Both refer to the same point in time and not a particular date.</span></span> 

<span data-ttu-id="e1f23-126">[![Het formulier Medewerker](./media/worker-form2.png)](./media/worker-form2.png)</span><span class="sxs-lookup"><span data-stu-id="e1f23-126">[![Worker form](./media/worker-form2.png)](./media/worker-form2.png)</span></span>

## <a name="date-and-time-data-in-data-management-framework-excel-common-data-service-and-power-bi"></a><span data-ttu-id="e1f23-127">Datum- en tijdgegevens in Data Management Framework, Excel, Common Data Service en Power BI</span><span class="sxs-lookup"><span data-stu-id="e1f23-127">Date and Time data in Data Management Framework, Excel, Common Data Service, and Power BI</span></span> 

<span data-ttu-id="e1f23-128">Data Management Framework, de Excel-invoegtoepassing, Common Data Service en Power BI-rapportage zijn allemaal ontworpen om rechtstreeks met gegevens te werken op databaseniveau.</span><span class="sxs-lookup"><span data-stu-id="e1f23-128">The Data Management Framework, Excel Add-In, Common Data Service, and Power BI reporting are all designed to interact with data directly on the database level.</span></span> <span data-ttu-id="e1f23-129">Omdat er geen client is om de gegevens in **Datum en tijd** aan te passen aan de tijdzone van de gebruiker, worden alle waarden voor **Datum en tijd** in UTC weergegeven. Dit kan leiden tot enkele onjuiste aannames bij het invoeren of weergeven van gegevens.</span><span class="sxs-lookup"><span data-stu-id="e1f23-129">Since there is no client to adjust **Date and Time** data to the time zone of the user, all **Date and Time** values are in UTC, which can lead to some incorrect assumptions when entering or viewing data.</span></span>  
 
<span data-ttu-id="e1f23-130">Voor de gegevens voor **Datum en tijd** die worden ingediend via DMF, Excel of Common Data Service, wordt er voor de database van uitgegaan dat deze in UTC zijn.</span><span class="sxs-lookup"><span data-stu-id="e1f23-130">**Date and Time** data that is submitted via DMF, Excel, or Common Data Service is assumed to be in UTC by the database.</span></span> <span data-ttu-id="e1f23-131">Dit kan leiden tot verwarring wanneer de ingediende waarde voor **Datum en tijd** niet wordt weergegeven zoals verwacht omdat de gebruiker die de gegevens weergeeft niet de tijdzone UTC heeft ingesteld.</span><span class="sxs-lookup"><span data-stu-id="e1f23-131">This can cause some confusion when the submitted **Date and Time** value doesn't display as expected because the user viewing the data doesn't have their user time zone  set to UTC.</span></span> 
 
<span data-ttu-id="e1f23-132">Hetzelfde kan in tegengestelde richting gebeuren wanneer er gegevens worden geëxporteerd.</span><span class="sxs-lookup"><span data-stu-id="e1f23-132">The same thing can happen in reverse when data is exported.</span></span> <span data-ttu-id="e1f23-133">De gegevens bij **Datum en tijd** in de geëxporteerde DMF-entiteit kunnen verschillen van wat wordt weergegeven in de Dynamics-client.</span><span class="sxs-lookup"><span data-stu-id="e1f23-133">The **Date and Time** data in the exported DMF entity can be different then what is displayed in the Dynamics client.</span></span> 
 
<span data-ttu-id="e1f23-134">Wanneer u externe bronnen als DMF gebruikt om gegevens te bekijken of op te geven, moet u er rekening mee houden dat er standaard van uitgegaan wordt dat de de waarden voor **Datum en tijd** in UTC zijn, ongeacht de tijdzone van de computer van de gebruiker of de huidige tijdzone-instellingen van de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="e1f23-134">When using external sources like DMF to view or author data, it is important to keep in mind that the **Date and Time** values are considered by default to be in UTC regardless of the time zone of the user's computer or their current user time zone settings.</span></span> 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a><span data-ttu-id="e1f23-135">Voorbeelden van dezelfde record die in verschillende productgebieden wordt weergegeven</span><span class="sxs-lookup"><span data-stu-id="e1f23-135">Examples of the same record being displayed in different product areas</span></span> 

<span data-ttu-id="e1f23-136">**Talent met de tijdzone ingesteld op UTC**</span><span class="sxs-lookup"><span data-stu-id="e1f23-136">**Talent with user time zone set to UTC**</span></span>

<span data-ttu-id="e1f23-137">[![Het formulier Medewerker](./media/worker-form3.png)](./media/worker-form3.png)</span><span class="sxs-lookup"><span data-stu-id="e1f23-137">[![Worker form](./media/worker-form3.png)](./media/worker-form3.png)</span></span>

<span data-ttu-id="e1f23-138">**Talent met de tijdzone ingesteld op GMT +12:00**</span><span class="sxs-lookup"><span data-stu-id="e1f23-138">**Talent with user time zone set to GMT +12:00**</span></span> 

<span data-ttu-id="e1f23-139">[![Het formulier Medewerker](./media/worker-form4.png)](./media/worker-form4.png)</span><span class="sxs-lookup"><span data-stu-id="e1f23-139">[![Worker form](./media/worker-form4.png)](./media/worker-form4.png)</span></span>

<span data-ttu-id="e1f23-140">**Excel via OData**</span><span class="sxs-lookup"><span data-stu-id="e1f23-140">**Excel Via OData**</span></span>

<span data-ttu-id="e1f23-141">[![Excel via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span><span class="sxs-lookup"><span data-stu-id="e1f23-141">[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span></span>

<span data-ttu-id="e1f23-142">**DMF-fasering**</span><span class="sxs-lookup"><span data-stu-id="e1f23-142">**DMF Staging**</span></span>

<span data-ttu-id="e1f23-143">[![DMF-fasering](./media/DMFStaging.png)](./media/DMFStaging.png)</span><span class="sxs-lookup"><span data-stu-id="e1f23-143">[![DMF Staging](./media/DMFStaging.png)](./media/DMFStaging.png)</span></span>

<span data-ttu-id="e1f23-144">**DMF-export**</span><span class="sxs-lookup"><span data-stu-id="e1f23-144">**DMF Export**</span></span>

<span data-ttu-id="e1f23-145">[![DMF-fasering](./media/DMFexport.png)](./media/DMFexport.png)</span><span class="sxs-lookup"><span data-stu-id="e1f23-145">[![DMF Staging](./media/DMFexport.png)](./media/DMFexport.png)</span></span>

<span data-ttu-id="e1f23-146">**Excel via Common Data Service**</span><span class="sxs-lookup"><span data-stu-id="e1f23-146">**Excel via Common Data Service**</span></span>

<span data-ttu-id="e1f23-147">[![Excel via Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span><span class="sxs-lookup"><span data-stu-id="e1f23-147">[![Excel via Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span></span>

### <a name="see-also"></a><span data-ttu-id="e1f23-148">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e1f23-148">See also</span></span>

[<span data-ttu-id="e1f23-149">Datum- en tijdgegevens</span><span class="sxs-lookup"><span data-stu-id="e1f23-149">Date and time data</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[<span data-ttu-id="e1f23-150">Voorkeurstijdzones van gebruiker</span><span class="sxs-lookup"><span data-stu-id="e1f23-150">User preferred time zones</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 
