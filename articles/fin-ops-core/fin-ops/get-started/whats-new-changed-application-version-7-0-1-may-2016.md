---
title: Wat is nieuw of gewijzigd in Dynamics AX-toepassingsversie 7.0.1 (mei 2016)
description: In dit artikel worden de functies beschreven die in Microsoft Dynamics AX versie 7.0.1 nieuw of gewijzigd zijn. Deze versie werd uitgebracht in mei 2016 en heeft een buildnummer van 7.0.1265.23014.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.custom: 91213
ms.assetid: f0bbc78f-87fc-40e9-b46a-6655893f69be
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 715e0f8d08c6abbde35eb917cddc4ecf4b7b67ed
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811451"
---
# <a name="whats-new-or-changed-in-dynamics-ax-application-version-701-may-2016"></a><span data-ttu-id="67cf5-104">Wat is nieuw of gewijzigd in Dynamics AX-toepassingsversie 7.0.1 (mei 2016)</span><span class="sxs-lookup"><span data-stu-id="67cf5-104">What's new or changed in Dynamics AX application version 7.0.1 (May 2016)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="67cf5-105">In dit artikel worden de functies beschreven die in Microsoft Dynamics AX versie 7.0.1 nieuw of gewijzigd zijn.</span><span class="sxs-lookup"><span data-stu-id="67cf5-105">This article describes features that are either new or changed in Microsoft Dynamics AX application version 7.0.1.</span></span> <span data-ttu-id="67cf5-106">Deze versie werd uitgebracht in mei 2016 en heeft een buildnummer van 7.0.1265.23014.</span><span class="sxs-lookup"><span data-stu-id="67cf5-106">This version was released in May 2016 and has a build number of 7.0.1265.23014.</span></span>

## <a name="electronic-reporting-er"></a><span data-ttu-id="67cf5-107">Elektronische rapportage (ER)</span><span class="sxs-lookup"><span data-stu-id="67cf5-107">Electronic reporting (ER)</span></span>

| <span data-ttu-id="67cf5-108">Wat kunt u doen?</span><span class="sxs-lookup"><span data-stu-id="67cf5-108">What can you do?</span></span> | <span data-ttu-id="67cf5-109">Waarom is dit belangrijk?</span><span class="sxs-lookup"><span data-stu-id="67cf5-109">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="67cf5-110">Configureer een dialoogvenster tijdens de uitvoering voor het ontwerpen van ER-rapporten (elektronische rapportage), zodat gebruikers de financiële dimensies kunnen selecteren die ze willen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="67cf5-110">Configure a run-time dialog box for designing Electronic reporting (ER) reports, so that users can select the financial dimensions that they want.</span></span> | <span data-ttu-id="67cf5-111">Tijdens de uitvoering kunnen gebruikers in het dialoogvenster voor het uitvoeren van een ER-rapport meerdere financiële dimensies selecteren.</span><span class="sxs-lookup"><span data-stu-id="67cf5-111">At run time, in the dialog box for running an ER report, users can select multiple financial dimensions.</span></span> <span data-ttu-id="67cf5-112">De details van de geselecteerde financiële dimensies wordt weergegeven in het elektronische document dat wordt gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="67cf5-112">The details of the selected financial dimensions will be displayed in the electronic document that is generated.</span></span> |
| <span data-ttu-id="67cf5-113">Configureer toegang tot meerdere financiële dimensies bij het ontwerp van een ER-rapport, via één toewijzing voor de gewenste gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="67cf5-113">Configure access to multiple financial dimensions during the design of an ER report, via a single mapping to the desired data source.</span></span> | <span data-ttu-id="67cf5-114">Dezelfde configuratie voor ER-rapporten kan worden gebruikt voor het genereren van elektronische documenten die transactiegegevens presenteren alsmede details van financiële dimensies, ongeacht het aantal financiële dimensies dat is geselecteerd door de gebruiker of geconfigureerd voor de huidige rechtspersoon of het huidige exemplaar.</span><span class="sxs-lookup"><span data-stu-id="67cf5-114">The same ER report configuration can be used to generate electronic documents that present transactional data together with details of financial dimensions, regardless of the number of financial dimensions that are either selected by the user or configured for the current legal entity or instance.</span></span> |
| <span data-ttu-id="67cf5-115">Configureer een ER-rapport voor het invoeren van gegevens in dynamisch gegenereerde kolommen van een elektronisch document dat is gemaakt in OPENXML-werkbladindeling.</span><span class="sxs-lookup"><span data-stu-id="67cf5-115">Configure an ER report to enter data in dynamically generated columns of an electronic document that is created in OPENXML worksheet format.</span></span> | <span data-ttu-id="67cf5-116">Een ER-rapport kan gegevens invoeren in een OPENXML-werkblad dat wordt gegenereerd via het horizontaal repliceren van kolommen.</span><span class="sxs-lookup"><span data-stu-id="67cf5-116">An ER report can enter data in an OPENXML worksheet that is generated, via horizontally replicating columns.</span></span> <span data-ttu-id="67cf5-117">Daarom kan dezelfde ER-rapportconfiguratie opnieuw worden gebruikt voor het genereren van elektronische documenten met een verschillend aantal dynamisch gegenereerde kolommen.</span><span class="sxs-lookup"><span data-stu-id="67cf5-117">Therefore, the same ER report configuration can be reused to generate electronic documents that have a different number of dynamically generated columns.</span></span> |
| <span data-ttu-id="67cf5-118">Configureer ER-bestemmingen zodat het resultaat van de uitvoer van een indeling wordt omgeleid naar een specifieke bestemming: bestand, e-mailadres of archief (Microsoft SharePoint-map of Microsoft Azure-opslag).</span><span class="sxs-lookup"><span data-stu-id="67cf5-118">Configure ER destinations so that the output result of a format is directed to specific destination: file, email, or archive (Microsoft SharePoint folder or Microsoft Azure Storage).</span></span> | <span data-ttu-id="67cf5-119">Voorheen, wanneer u een ER-configuratie uitvoerde, werd er een bericht weergegeven waarin gebruikersactie werd vereist voor het opslaan of openen van een bestand.</span><span class="sxs-lookup"><span data-stu-id="67cf5-119">Previously, when you ran an ER configuration, a message box appeared that required user action to save or open a file.</span></span> <span data-ttu-id="67cf5-120">U kunt nu apart een bestemming vooraf configureren voor elke indelingsconfiguratie en voor elk uitvoeronderdeel (een map of een bestand).</span><span class="sxs-lookup"><span data-stu-id="67cf5-120">You can now pre-configure a destination for each format configuration and for each output component (a folder or a file) separately.</span></span> <span data-ttu-id="67cf5-121">Gebruikers die over de juiste toegangsrechten beschikken, kunnen tevens bestemmingsinstellingen wijzigen tijdens de uitvoering.</span><span class="sxs-lookup"><span data-stu-id="67cf5-121">Users who have appropriate access rights can also modify destination settings at run time.</span></span> |

## <a name="pos--microsoft-dynamics-ax-retail"></a><span data-ttu-id="67cf5-122">POS – Microsoft Dynamics AX Retail</span><span class="sxs-lookup"><span data-stu-id="67cf5-122">POS – Microsoft Dynamics AX Retail</span></span>

| <span data-ttu-id="67cf5-123">Wat kunt u doen?</span><span class="sxs-lookup"><span data-stu-id="67cf5-123">What can you do?</span></span> | <span data-ttu-id="67cf5-124">Waarom is dit belangrijk?</span><span class="sxs-lookup"><span data-stu-id="67cf5-124">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="67cf5-125">Gebruik de Google Chrome browser.</span><span class="sxs-lookup"><span data-stu-id="67cf5-125">Use the Google Chrome browser.</span></span> | <span data-ttu-id="67cf5-126">Detailhandelaren kunnen Cloud POS nu starten vanuit de browser Chrome en beschikken over alle functionaliteit die beschikbaar is in de Microsoft Edge en Internet Explorer-versie van Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="67cf5-126">Retailers can now start Cloud POS from the Chrome browser, and can experience all the functionality that is available in the Microsoft Edge and Internet Explorer version of Cloud POS.</span></span> |

## <a name="financial-reporting"></a><span data-ttu-id="67cf5-127">Financiële rapportage</span><span class="sxs-lookup"><span data-stu-id="67cf5-127">Financial reporting</span></span>

| <span data-ttu-id="67cf5-128">Wat kunt u doen?</span><span class="sxs-lookup"><span data-stu-id="67cf5-128">What can you do?</span></span> | <span data-ttu-id="67cf5-129">Waarom is dit belangrijk?</span><span class="sxs-lookup"><span data-stu-id="67cf5-129">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="67cf5-130">Bouw de datamart voor financiële rapportage opnieuw op.</span><span class="sxs-lookup"><span data-stu-id="67cf5-130">Rebuild the Financial reporting data mart.</span></span> | <span data-ttu-id="67cf5-131">Wanneer u Dynamics AX-databases tussen omgevingen verplaatst of andere ingrijpende wijzigingen in de omgeving doorvoert, moet mogelijk de database voor financiële rapportage opnieuw worden opgebouwd.</span><span class="sxs-lookup"><span data-stu-id="67cf5-131">When you move Dynamics AX databases between environments or make other invasive changes to the environment, the Financial reporting database might have to be rebuilt.</span></span> <span data-ttu-id="67cf5-132">Er is nu een Windows PowerShell-script beschikbaar dat de database opnieuw voor u opbouwt.</span><span class="sxs-lookup"><span data-stu-id="67cf5-132">A Windows PowerShell script is now provided to rebuild the database for you.</span></span> |
| <span data-ttu-id="67cf5-133">U kunt niet langer opties voor rapportontwerper selecteren die niet geldig zijn.</span><span class="sxs-lookup"><span data-stu-id="67cf5-133">You can no longer select report designer options that aren't valid.</span></span> | <span data-ttu-id="67cf5-134">Verschillende opties voor rapportontwerper die werden gebruikt in de versies van Management Reporter op de markt gelden niet voor deze versie van Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="67cf5-134">Several report designer options that were used in the in-market versions of Management reporter don't apply to this version of Dynamics AX.</span></span> <span data-ttu-id="67cf5-135">Deze opties waren gerelateerd aan het ontwerp, de uitvoer en de koppeling van financiële rapportage.</span><span class="sxs-lookup"><span data-stu-id="67cf5-135">These options were related to financial report design, output, and linking.</span></span> <span data-ttu-id="67cf5-136">Deze opties zijn verwijderd uit de functie voor het ontwerpen van financiële rapporten om gebruikersfouten te voorkomen.</span><span class="sxs-lookup"><span data-stu-id="67cf5-136">These options have been removed from the financial report designer to prevent user errors.</span></span> |

## <a name="financial-management"></a><span data-ttu-id="67cf5-137">Financieel beheer</span><span class="sxs-lookup"><span data-stu-id="67cf5-137">Financial management</span></span>

| <span data-ttu-id="67cf5-138">Wat kunt u doen?</span><span class="sxs-lookup"><span data-stu-id="67cf5-138">What can you do?</span></span> | <span data-ttu-id="67cf5-139">Waarom is dit belangrijk?</span><span class="sxs-lookup"><span data-stu-id="67cf5-139">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="67cf5-140">Genereer positieve betalingsbestanden voor leveranciersbetalingen.</span><span class="sxs-lookup"><span data-stu-id="67cf5-140">Generate positive pay files for accounts payable payments.</span></span> | <span data-ttu-id="67cf5-141">Positieve betalingsbestanden kunnen worden gegenereerd om fraude met cheques te helpen voorkomen.</span><span class="sxs-lookup"><span data-stu-id="67cf5-141">Positive pay files can be generated to help prevent check fraud.</span></span> |

## <a name="warehouse-and-production"></a><span data-ttu-id="67cf5-142">Magazijn en productie</span><span class="sxs-lookup"><span data-stu-id="67cf5-142">Warehouse and production</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="67cf5-143">Wat kunt u doen?</span><span class="sxs-lookup"><span data-stu-id="67cf5-143">What can you do?</span></span></th>
<th><span data-ttu-id="67cf5-144">Waarom is dit belangrijk?</span><span class="sxs-lookup"><span data-stu-id="67cf5-144">Why is this important?</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="67cf5-145">Definieer een werkbeleid voor magazijnen dat het maken van werk voor een reeks van producten op specifieke locaties regelt.</span><span class="sxs-lookup"><span data-stu-id="67cf5-145">Define a warehouse work policy that controls the creation of work for a set of products at specific locations.</span></span></td>
<td><span data-ttu-id="67cf5-146">Magazijnprocessen omvatten niet altijd werk.</span><span class="sxs-lookup"><span data-stu-id="67cf5-146">Warehouse processes don't always include work.</span></span> <span data-ttu-id="67cf5-147">Met behulp van het nieuwe magazijnwerkbeleid kunt u voorkomen dat werk wordt gemaakt voor het verzamelen en wegzetten van grondstoffen voor afgewerkte goederen voor een reeks producten op specifieke locaties.</span><span class="sxs-lookup"><span data-stu-id="67cf5-147">By using the new warehouse work policy, you can prevent work from being created for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="67cf5-148">Geef op dat op een locatie voor productie-uitvoer niet worden gecontroleerd op nummerplaat.</span><span class="sxs-lookup"><span data-stu-id="67cf5-148">Specify that a production output location isn't license plate–controlled.</span></span></td>
<td><span data-ttu-id="67cf5-149">U kunt nu opgeven dat een locatie voor productuitvoer niet wordt gecontroleerd op nummerplaat.</span><span class="sxs-lookup"><span data-stu-id="67cf5-149">You can now specify that a product output location isn't license plate–controlled.</span></span> <span data-ttu-id="67cf5-150">Deze functie is bijvoorbeeld handig als een upstream productieorder artikelen rechtstreeks gereedmeldt op een locatie die als productie-invoerlocatie voor een downstream productieorder fungeert.</span><span class="sxs-lookup"><span data-stu-id="67cf5-150">For example, this feature is useful when an upstream production order reports items as finished directly to a location that acts as production input location for a downstream production order.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="67cf5-151">Ondersteun stuklijsten die artikelen met verschillende productafmetingen van hetzelfde artikel bevatten.</span><span class="sxs-lookup"><span data-stu-id="67cf5-151">Support BOMs that include items with different product dimensions of the same item.</span></span></td>
<td><span data-ttu-id="67cf5-152">Wanneer u een of meerdere van de productafmetingen in productie gebruikt, kunt u situaties hebben waarin u een artikel wilt produceren op basis van een andere variant van hetzelfde artikel.</span><span class="sxs-lookup"><span data-stu-id="67cf5-152">When using one or multiple of the product dimensions in production, you can have situations where you would like to produce an item, based on a different variant of the same item.</span></span> <span data-ttu-id="67cf5-153">Zie <a href="https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/">deze blog</a> voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="67cf5-153">For more information, see <a href="https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/">this blog</a>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="67cf5-154">Productieorders met circulaire structuren op het eerste niveau van de stuklijsten zijn uitgesloten van berekening op stuklijstniveau voor de planning van materiaalresources.</span><span class="sxs-lookup"><span data-stu-id="67cf5-154">Production orders with circular structures at the first level of their BOMs are excluded from BOM level calculation for material resource planning.</span></span></td>
<td><span data-ttu-id="67cf5-155">Het is niet mogelijk correcte stuklijstniveaus toe te wijzen aan productvarianten voor productieorders die correctheid in de stuklijsthiërarchie veroorzaken.</span><span class="sxs-lookup"><span data-stu-id="67cf5-155">It is not possible to assign correct BOM levels to product variants for production orders that cause circularity in the BOM hierarchy.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="67cf5-156">Bereken afzonderlijke stuklijstniveaus voor de planning van materiaalresources en kostenberekening:</span><span class="sxs-lookup"><span data-stu-id="67cf5-156">Calculate separate BOM levels for material resource planning and cost calculation:</span></span>
<ul>
<li><span data-ttu-id="67cf5-157">Voor de planning van materiaalresources worden stuklijstniveaus berekend in de nieuwe tabel <strong>ReqItemLevel</strong>.</span><span class="sxs-lookup"><span data-stu-id="67cf5-157">For material resource planning, BOM levels are calculated in the new <strong>ReqItemLevel</strong> table.</span></span> <span data-ttu-id="67cf5-158">Beëindigde productieorders worden genegeerd in de berekening.</span><span class="sxs-lookup"><span data-stu-id="67cf5-158">Ended production orders are ignored in the calculation.</span></span></li>
<li><span data-ttu-id="67cf5-159">Voor de berekening van de productiekosten worden stuklijstniveaus berekend in de tabel <strong>InventTable</strong>.</span><span class="sxs-lookup"><span data-stu-id="67cf5-159">For production cost calculation, BOM levels are calculated in the <strong>InventTable</strong>.</span></span> <span data-ttu-id="67cf5-160">Beëindigde productieorders worden opgenomen in de berekening.</span><span class="sxs-lookup"><span data-stu-id="67cf5-160">Ended production orders are included in the calculation.</span></span></li>
</ul>
</td>
<td>
<ul>
<li><span data-ttu-id="67cf5-161">Bij het uitvoeren van de planning van materiaalresources, bijvoorbeeld planning en explosie van de hoofdplanning, hoeven alleen stuklijstniveaus die worden gebruikt voor de planning van de materiaalresources opnieuw te worden berekend.</span><span class="sxs-lookup"><span data-stu-id="67cf5-161">When running material resource planning, for example, master planning plan scheduling and explosion, only BOM levels used for material resource planning need to be recalculated.</span></span> <span data-ttu-id="67cf5-162">Met andere woorden, er hoeven geen stuklijstniveaus te worden berekend die worden gebruikt voor de berekening van de productiekostprijs.</span><span class="sxs-lookup"><span data-stu-id="67cf5-162">In other words, there is no need to calculate BOM levels used for production costing calculation.</span></span></li>
<li><span data-ttu-id="67cf5-163">Bij het uitvoeren van bewerkingen voor kostprijsberekening, bijvoorbeeld de afsluiting van voorraad, hoeven alleen stuklijstniveaus die worden gebruikt voor kostprijsberekening voor de productie opnieuw te worden berekend.</span><span class="sxs-lookup"><span data-stu-id="67cf5-163">When running costing operations, for example, inventory closing, only BOM levels used for production costing calculation need to be recalculated.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="67cf5-164">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="67cf5-164">Additional resources</span></span>

[<span data-ttu-id="67cf5-165">Startpagina Nieuw of gewijzigd in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="67cf5-165">What's new or changed in Finance and Operations home page</span></span>](whats-new-changed.md)

[<span data-ttu-id="67cf5-166">Nieuwe of bijgewerkte taakbegeleidingen (mei 2016)</span><span class="sxs-lookup"><span data-stu-id="67cf5-166">New or updated task guides (May 2016)</span></span>](new-updated-task-guides-available-may-2016.md)
