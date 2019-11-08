---
title: Financiële dimensies
description: In dit onderwerp worden de verschillende typen financiële dimensies beschreven en hoe ze worden ingesteld.
author: aprilolson
manager: AnnBe
ms.date: 01/03/2019
ms.topic: article
ems.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 0715d3e4e4cb167c55d9c7d98cdf599187bf3b43
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177121"
---
# <a name="financial-dimensions"></a><span data-ttu-id="76eda-103">Financiële dimensies</span><span class="sxs-lookup"><span data-stu-id="76eda-103">Financial dimensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="76eda-104">In dit onderwerp worden de verschillende typen financiële dimensies uitgelegd en hoe ze worden ingesteld.</span><span class="sxs-lookup"><span data-stu-id="76eda-104">This topic explains the various types of financial dimensions and how they are set up.</span></span>

<span data-ttu-id="76eda-105">Gebruik de pagina **Financiële dimensies** om financiële dimensies te maken die u als rekeningsegmenten kunt gebruiken voor rekeningschema's.</span><span class="sxs-lookup"><span data-stu-id="76eda-105">Use the **Financial dimensions** page to create financial dimensions that you can use as account segments for charts of accounts.</span></span> <span data-ttu-id="76eda-106">Er zijn twee typen financiële dimensies: aangepaste dimensies en door een entiteit ondersteunde dimensies.</span><span class="sxs-lookup"><span data-stu-id="76eda-106">There are two types of financial dimensions: custom dimensions and entity-backed dimensions.</span></span> <span data-ttu-id="76eda-107">De aangepaste dimensies worden gedeeld door rechtspersonen en de waarden worden door gebruikers ingevoerd en onderhouden.</span><span class="sxs-lookup"><span data-stu-id="76eda-107">Custom dimensions are shared across legal entities, and the values are entered and maintained by users.</span></span> <span data-ttu-id="76eda-108">Voor door een entiteit ondersteunde dimensies worden de waarden elders in het systeem gedefinieerd, zoals in de entiteiten Klanten of Winkels.</span><span class="sxs-lookup"><span data-stu-id="76eda-108">For entity-backed dimensions, the values are defined somewhere else in the system, such as in Customers or Stores entities.</span></span> <span data-ttu-id="76eda-109">Bepaalde door entiteiten ondersteunde dimensies zijn verdeeld over rechtspersonen en sommige door entiteiten ondersteunde dimensies zijn bedrijfsspecifiek.</span><span class="sxs-lookup"><span data-stu-id="76eda-109">Some entity-backed dimensions are shared across legal entities, whereas other entity-backed dimensions are company-specific.</span></span>

<span data-ttu-id="76eda-110">Nadat u de financiële dimensies hebt gemaakt, gebruikt u de pagina **Waarden van financiële dimensie** om aanvullende eigenschappen toe te wijzen aan elke financiële dimensie.</span><span class="sxs-lookup"><span data-stu-id="76eda-110">After you've created the financial dimensions, use the **Financial dimension values** page to assign additional properties to each financial dimension.</span></span>

<span data-ttu-id="76eda-111">U kunt financiële dimensies gebruiken om rechtspersonen te vertegenwoordigen.</span><span class="sxs-lookup"><span data-stu-id="76eda-111">You can use financial dimensions to represent legal entities.</span></span> <span data-ttu-id="76eda-112">U hoeft de rechtspersonen niet te maken in Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="76eda-112">You don't have to create the legal entities in Dynamics 365 Finance.</span></span> <span data-ttu-id="76eda-113">Financiële dimensies zijn echter niet bedoeld om te voldoen aan operationele of zakelijke behoeften van rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="76eda-113">However, financial dimensions aren't designed to address the operational or business requirements of legal entities.</span></span> <span data-ttu-id="76eda-114">De boekhouding tussen eenheden-functie in Finance is ontworpen om alleen met de boekhoudkundige vermeldingen te werken die door de transactie worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="76eda-114">The interunit accounting functionality in Finance is designed to address only the accounting entries that are created by each transaction.</span></span>

<span data-ttu-id="76eda-115">Voordat u de financiële dimensies instelt als rechtspersonen, moet u uw bedrijfsprocessen evalueren in de volgende gebieden om te bepalen of deze instelling zal werken voor uw organisatie:</span><span class="sxs-lookup"><span data-stu-id="76eda-115">Before you set up financial dimensions as legal entities, evaluate your business processes in the following areas to determine whether this setup will work for your organization:</span></span>

- <span data-ttu-id="76eda-116">Voorraad</span><span class="sxs-lookup"><span data-stu-id="76eda-116">Inventory</span></span>
- <span data-ttu-id="76eda-117">Verkoop en inkoop tussen financiële dimensies en rechtspersonen</span><span class="sxs-lookup"><span data-stu-id="76eda-117">Sales and purchases between financial dimensions and legal entities</span></span>
- <span data-ttu-id="76eda-118">Btw-berekening en rapportage</span><span class="sxs-lookup"><span data-stu-id="76eda-118">Sales tax calculation and reporting</span></span>
- <span data-ttu-id="76eda-119">Operationele rapporteren</span><span class="sxs-lookup"><span data-stu-id="76eda-119">Operational reporting</span></span>

<span data-ttu-id="76eda-120">Hieronder vindt u enkele beperkingen:</span><span class="sxs-lookup"><span data-stu-id="76eda-120">Here are some of the limitations:</span></span>

- <span data-ttu-id="76eda-121">U kunt de btw-functionaliteit alleen gebruiken met rechtspersonen, niet met financiële dimensies.</span><span class="sxs-lookup"><span data-stu-id="76eda-121">You can use sales tax functionality only with legal entities, not with financial dimensions.</span></span>
- <span data-ttu-id="76eda-122">Sommige rapporten bevatten geen financiële dimensies.</span><span class="sxs-lookup"><span data-stu-id="76eda-122">Some reports don't include financial dimensions.</span></span> <span data-ttu-id="76eda-123">Als u op basis van financiële dimensie wilt rapporteren, moet u dus mogelijk de rapporten wijzigen.</span><span class="sxs-lookup"><span data-stu-id="76eda-123">Therefore, to report by financial dimension, you might have to modify the reports.</span></span>

## <a name="custom-dimensions"></a><span data-ttu-id="76eda-124">Aangepaste dimensies</span><span class="sxs-lookup"><span data-stu-id="76eda-124">Custom dimensions</span></span>

<span data-ttu-id="76eda-125">Als u een door de gebruiker gedefinieerde financiële dimensie wilt maken, selecteert u **Aangepaste dimensie** in het veld **Waarden gebruiken van**.</span><span class="sxs-lookup"><span data-stu-id="76eda-125">To create a user-defined financial dimension, in the **Use values from** field, select **Custom dimension**.</span></span>

<span data-ttu-id="76eda-126">U kunt ook een opmaakmasker opgeven om de hoeveelheid en het type gegevens te beperken die voor dimensiewaarden kunnen worden ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="76eda-126">You can also specify an account mask to limit the amount and type of information that can be entered for dimension values.</span></span> <span data-ttu-id="76eda-127">U kunt tekens, zoals letters of een koppelteken (-), invoeren die voor elke dimensiewaarde hetzelfde blijven.</span><span class="sxs-lookup"><span data-stu-id="76eda-127">You can enter characters that remain the same for each dimension value, such as letters or a hyphen (-).</span></span> <span data-ttu-id="76eda-128">U kunt ook hekjes (\#) en en-tekens (&) invoeren die dienen als tijdelijke aanduidingen voor tekens die elke keer worden gewijzigd als een dimensiewaarde wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="76eda-128">You can also enter number signs (\#) and ampersands (&) as placeholders for characters that will change every time that a dimension value is created.</span></span> <span data-ttu-id="76eda-129">Gebruik een hekje (\#) als tijdelijke aanduiding voor een cijfer en een en-teken (&) als tijdelijke aanduiding voor een letter.</span><span class="sxs-lookup"><span data-stu-id="76eda-129">Use a number sign (\#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span> <span data-ttu-id="76eda-130">Het veld voor het opmaakmasker is alleen beschikbaar wanneer u **Aangepaste dimensie** selecteert in het veld **Waarden gebruiken van**.</span><span class="sxs-lookup"><span data-stu-id="76eda-130">The field for the format mask is available only when you select **Custom dimension** in the **Use values from** field.</span></span>

<span data-ttu-id="76eda-131">**Voorbeeld**</span><span class="sxs-lookup"><span data-stu-id="76eda-131">**Example**</span></span>

<span data-ttu-id="76eda-132">Om de dimensiewaarde te beperken tot de letters "CC" en drie getallen, voert u **CC\#\#\#** als opmaakmasker in.</span><span class="sxs-lookup"><span data-stu-id="76eda-132">To limit the dimension value to the letters "CC" and three numbers, enter **CC-\#\#\#** as the format mask.</span></span>

## <a name="entity-backed-dimensions"></a><span data-ttu-id="76eda-133">Door een entiteit ondersteunde dimensies</span><span class="sxs-lookup"><span data-stu-id="76eda-133">Entity-backed dimensions</span></span>

<span data-ttu-id="76eda-134">Als u een door een entiteit ondersteunde financiële dimensie wilt maken, selecteert u in het veld **Waarden gebruiken van** een door het systeem gedefinieerde entiteit waarop de financiële dimensie moet worden gebaseerd.</span><span class="sxs-lookup"><span data-stu-id="76eda-134">To create an entity-backed financial dimension, in the **Use values from** field, select a system-defined entity to base the financial dimension on.</span></span> <span data-ttu-id="76eda-135">Waarden van financiële dimensies worden vervolgens op basis van die entiteit gemaakt.</span><span class="sxs-lookup"><span data-stu-id="76eda-135">Financial dimension values are then created from that entity.</span></span> <span data-ttu-id="76eda-136">Als u bijvoorbeeld dimensiewaarden voor projecten wilt maken, selecteert u **Projecten**.</span><span class="sxs-lookup"><span data-stu-id="76eda-136">For example, to create dimension values for projects, select **Projects**.</span></span> <span data-ttu-id="76eda-137">Er wordt vervolgens voor elke projectnaam een dimensiewaarde gemaakt.</span><span class="sxs-lookup"><span data-stu-id="76eda-137">A dimension value is then created for each project name.</span></span> <span data-ttu-id="76eda-138">Op de pagina **Waarden van financiële dimensies** worden de waarden voor de entiteit weergegeven.</span><span class="sxs-lookup"><span data-stu-id="76eda-138">The **Financial dimension values** page shows the values for the entity.</span></span> <span data-ttu-id="76eda-139">Als deze waarden specifiek voor het bedrijf zijn, wordt op de pagina ook het bedrijf weergegeven.</span><span class="sxs-lookup"><span data-stu-id="76eda-139">If those values are company-specific, the page also shows the company.</span></span>

## <a name="activating-dimensions"></a><span data-ttu-id="76eda-140">Dimensies activeren</span><span class="sxs-lookup"><span data-stu-id="76eda-140">Activating dimensions</span></span>

<span data-ttu-id="76eda-141">Wanneer u een financiële dimensie activeert, wordt de tabel bijgewerkt om de naam van de financiële dimensie te bevatten.</span><span class="sxs-lookup"><span data-stu-id="76eda-141">When you activate a financial dimension, the table is updated so that it includes the name of the financial dimension.</span></span> <span data-ttu-id="76eda-142">Verwijderde dimensies worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="76eda-142">Deleted dimensions are removed.</span></span> <span data-ttu-id="76eda-143">U kunt dimensiewaarden invoeren voordat u een financiële dimensie activeert.</span><span class="sxs-lookup"><span data-stu-id="76eda-143">You can enter dimension values before you activate a financial dimension.</span></span> <span data-ttu-id="76eda-144">Een financiële dimensie kan echter pas ergens worden gebruikt als deze wordt geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="76eda-144">However, a financial dimension can't be consumed anywhere until it's activated.</span></span> <span data-ttu-id="76eda-145">U kunt een financiële dimensie bijvoorbeeld pas toevoegen aan een rekeningstructuur als de financiële dimensie is geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="76eda-145">For example, you can't add a financial dimension to an account structure until the financial dimension has been activated.</span></span> <span data-ttu-id="76eda-146">Wanneer u **Activeren** selecteert, worden alle dimensies bijgewerkt en worden statuswijzigingen weergegeven.</span><span class="sxs-lookup"><span data-stu-id="76eda-146">When you select **Activate**, all dimensions are updated and show status changes.</span></span>

## <a name="translations"></a><span data-ttu-id="76eda-147">Taalteksten</span><span class="sxs-lookup"><span data-stu-id="76eda-147">Translations</span></span>

<span data-ttu-id="76eda-148">Op de pagina **Tekstvertaling** kunt u tekst invoeren voor de geselecteerde financiële dimensie in verschillende talen.</span><span class="sxs-lookup"><span data-stu-id="76eda-148">On the **Text translation** page, you can enter text for the selected financial dimension in various languages.</span></span> <span data-ttu-id="76eda-149">Op de pagina **Vertaling hoofdrekening** kunt u tekst invoeren voor de hoofdrekening in verschillende talen.</span><span class="sxs-lookup"><span data-stu-id="76eda-149">On the **Main account translation** page, you can enter text for the main account in various languages.</span></span> 

## <a name="legal-entity-overrides"></a><span data-ttu-id="76eda-150">Overschrijvingen rechtspersoon</span><span class="sxs-lookup"><span data-stu-id="76eda-150">Legal entity overrides</span></span>

<span data-ttu-id="76eda-151">Niet alle dimensies zijn geldig voor alle rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="76eda-151">Not all dimensions are valid for all legal entities.</span></span> <span data-ttu-id="76eda-152">Daarnaast zijn sommige dimensies mogelijk alleen relevant voor een bepaalde periode.</span><span class="sxs-lookup"><span data-stu-id="76eda-152">Additionally, some dimensions might be relevant only for a specific period.</span></span> <span data-ttu-id="76eda-153">In deze gevallen kunt u de sectie **Overschrijvingen rechtspersoon** gebruiken om de bedrijven op te geven waarvoor de dimensie moet worden opgeschort, wie de eigenaar is en gedurende welke periode de dimensie actief is.</span><span class="sxs-lookup"><span data-stu-id="76eda-153">In these cases, you can use the **Legal entity overrides** section to specify the companies that the dimension should be suspended for, the owner, and the period when the dimension is active.</span></span>

## <a name="deleting-financial-dimensions"></a><span data-ttu-id="76eda-154">Financiële dimensies verwijderen</span><span class="sxs-lookup"><span data-stu-id="76eda-154">Deleting financial dimensions</span></span>

<span data-ttu-id="76eda-155">Om de referentiële integriteit van de gegevens te helpen waarborgen, kunnen financiële dimensies zelden worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="76eda-155">To help maintain referential integrity of the data, financial dimensions can rarely be deleted.</span></span> <span data-ttu-id="76eda-156">Als u een financiële dimensie probeert te verwijderen, worden de volgende criteria geëvalueerd:</span><span class="sxs-lookup"><span data-stu-id="76eda-156">If you try to delete a financial dimension, the following criteria are evaluated:</span></span>

- <span data-ttu-id="76eda-157">Is de financiële dimensie gebruikt in geboekte of niet-geboekte transacties of een willekeurig type dimensiewaardecombinatie?</span><span class="sxs-lookup"><span data-stu-id="76eda-157">Has the financial dimension been used on any posted or unposted transactions, or in any type of dimension value combination?</span></span>
- <span data-ttu-id="76eda-158">Wordt de financiële dimensie gebruikt in een actieve rekeningstructuur, geavanceerde regelstructuur of set met financiële dimensies?</span><span class="sxs-lookup"><span data-stu-id="76eda-158">Is the financial dimension used in any active account structure, advanced rule structure, or financial dimension set?</span></span>
- <span data-ttu-id="76eda-159">Maakt de financiële dimensie deel uit van een standaardindeling voor de integratie van financiële dimensies?</span><span class="sxs-lookup"><span data-stu-id="76eda-159">Is the financial dimension part of a default financial dimension integration format?</span></span>
- <span data-ttu-id="76eda-160">Is de financiële dimensie ingesteld als een standaarddimensie?</span><span class="sxs-lookup"><span data-stu-id="76eda-160">Has the financial dimension been set up as a default dimension?</span></span>

<span data-ttu-id="76eda-161">Als aan een van de criteria wordt voldaan, kunt u de financiële dimensie niet verwijderen.</span><span class="sxs-lookup"><span data-stu-id="76eda-161">If any of the criteria are met, you can't delete the financial dimension.</span></span>

## <a name="default-dimension-values"></a><span data-ttu-id="76eda-162">Waarden standaarddimensie</span><span class="sxs-lookup"><span data-stu-id="76eda-162">Default dimension values</span></span>

<span data-ttu-id="76eda-163">U kunt waarden uit hoofdrecords, zoals klanten en leveranciers, als standaardwaarden gebruiken in nieuwe dimensies.</span><span class="sxs-lookup"><span data-stu-id="76eda-163">You can use values from master records, such as customer and vendor, as default values in new dimensions.</span></span> <span data-ttu-id="76eda-164">Wanneer de nieuwe dimensies worden gemaakt, wordt de hoofdrecord-id in de dimensiewaarden ingevoerd voor deze hoofdrecords.</span><span class="sxs-lookup"><span data-stu-id="76eda-164">When the new dimensions are created, the master record ID is entered in the dimension values for those master records.</span></span> <span data-ttu-id="76eda-165">Wanneer u een nieuwe klant maakt, wordt de klant-id bijvoorbeeld ingevoerd in de klantdimensie.</span><span class="sxs-lookup"><span data-stu-id="76eda-165">For example, when you create a new customer, the customer ID is entered in the customer dimension.</span></span> <span data-ttu-id="76eda-166">Wanneer u verkooporders, facturen of andere documenten maakt waarvoor u een klant-id nodig hebt, worden de bestaande standaardregels gebruikt en wordt de klant-id toegevoegd aan het document.</span><span class="sxs-lookup"><span data-stu-id="76eda-166">When you create sales orders, invoices, or other documents that require a customer ID, the existing defaulting rules are used, and the customer ID is added to the document.</span></span>

<span data-ttu-id="76eda-167">Deze functie is gekoppeld aan een instelling in de dimensie.</span><span class="sxs-lookup"><span data-stu-id="76eda-167">This feature is controlled by a setting in the dimension.</span></span> <span data-ttu-id="76eda-168">De naam van deze instelling is **Kopieer waarden naar deze dimensie op elk nieuw gemaakte DimensionName**, waarbij **DimensionName** de naam van de dimensie is.</span><span class="sxs-lookup"><span data-stu-id="76eda-168">This setting is named **Copy values to this dimension on each new DimensionName created**, where **DimensionName** is the name of the dimension.</span></span> <span data-ttu-id="76eda-169">De functie is standaard uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="76eda-169">By default, the feature is turned off.</span></span> <span data-ttu-id="76eda-170">Deze kan op elk gewenst moment worden ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="76eda-170">However, it can be turned on at any time.</span></span>

<span data-ttu-id="76eda-171">Als er al records bestaan voor de dimensie, worden de hoofdrecords bijgewerkt wanneer u de functie inschakelt.</span><span class="sxs-lookup"><span data-stu-id="76eda-171">If records already exist for the dimension, the master records are updated when you turn the feature on.</span></span> <span data-ttu-id="76eda-172">Bestaande documenten en transacties worden echter niet bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="76eda-172">However, existing documents and transactions aren't updated.</span></span>

<span data-ttu-id="76eda-173">Als u een sjabloon gebruikt om een hoofdrecord te maken, moet u ervoor zorgen dat de sjabloonwaarde voor de hoofddimensie leeg is.</span><span class="sxs-lookup"><span data-stu-id="76eda-173">If you are using a template to create a master record, make sure that the template value for the master dimension is blank.</span></span> <span data-ttu-id="76eda-174">Als u klanten op basis van een sjabloon maakt, moet u er bijvoorbeeld voor zorgen dat klantdimensie in de sjabloon leeg is.</span><span class="sxs-lookup"><span data-stu-id="76eda-174">For example, if you're creating customers from a template, make sure that the customer dimension in the template is blank.</span></span> <span data-ttu-id="76eda-175">De klantdimensiewaarde wordt standaard ingesteld op basis van het nieuwe klantnummer wanneer u de nieuwe klant maakt.</span><span class="sxs-lookup"><span data-stu-id="76eda-175">The customer dimension value will default from the new customer number when you create the new customer.</span></span>  

## <a name="derived-dimensions"></a><span data-ttu-id="76eda-176">Afgeleide dimensies</span><span class="sxs-lookup"><span data-stu-id="76eda-176">Derived dimensions</span></span>

<span data-ttu-id="76eda-177">U kunt een dimensie zo configureren dat gegevens voor andere dimensies automatisch worden ingevoerd wanneer u die dimensie in een document invoert.</span><span class="sxs-lookup"><span data-stu-id="76eda-177">You can configure a dimension so that information for other dimensions is automatically entered when you enter that dimension in a document.</span></span> <span data-ttu-id="76eda-178">Als u kostenplaats 10 invoert, kan bijvoorbeeld automatisch een waarde van **20** worden ingevoerd in de afdelingsdimensie.</span><span class="sxs-lookup"><span data-stu-id="76eda-178">For example, if you enter cost center 10, a value of **20** can be automatically entered in the department dimension.</span></span>

<span data-ttu-id="76eda-179">U kunt afgeleide waarden instellen op de pagina Dimensies.</span><span class="sxs-lookup"><span data-stu-id="76eda-179">You can set up derived values on the dimensions page.</span></span>

1. <span data-ttu-id="76eda-180">Selecteer een dimensie en selecteer vervolgens **Afgeleide dimensies**.</span><span class="sxs-lookup"><span data-stu-id="76eda-180">Select a dimension and then select **Derived dimensions**.</span></span>

    <span data-ttu-id="76eda-181">De pagina **Afgeleide dimensies** bevat een raster.</span><span class="sxs-lookup"><span data-stu-id="76eda-181">The **Derived dimensions** page includes a grid.</span></span> <span data-ttu-id="76eda-182">Het geselecteerde dimensiesegment is de eerste kolom in dit raster.</span><span class="sxs-lookup"><span data-stu-id="76eda-182">The selected dimension segment is the first column in this grid.</span></span>

2. <span data-ttu-id="76eda-183">Voeg de segmenten toe die moeten worden afgeleid.</span><span class="sxs-lookup"><span data-stu-id="76eda-183">Add the segments that should be derived.</span></span> <span data-ttu-id="76eda-184">Elk segment wordt weergegeven als een kolom.</span><span class="sxs-lookup"><span data-stu-id="76eda-184">Each segment appears as a column.</span></span>

<span data-ttu-id="76eda-185">Voer de dimensiecombinaties in die moeten worden afgeleid van de dimensie in de eerste kolom.</span><span class="sxs-lookup"><span data-stu-id="76eda-185">Enter the dimension combinations that should be derived from the dimension in the first column.</span></span> <span data-ttu-id="76eda-186">Als u de kostenplaats wilt gebruiken als de dimensie waarvan de afdeling en locatie moeten worden afgeleid, voert u bijvoorbeeld kostenplaats 10, afdeling 20 en locatie 30 in.</span><span class="sxs-lookup"><span data-stu-id="76eda-186">For example, to use the cost center as the dimension that the department and location are derived from, enter cost center 10, department 20, and location 30.</span></span> <span data-ttu-id="76eda-187">Wanneer u vervolgens kostenplaats 10 invoert in een hoofdrecord of op een transactiepagina, worden afdeling 20 en locatie 30 standaard ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="76eda-187">Then, when you enter cost center 10 in a master record or on a transaction page, department 20 and location 30 are entered by default.</span></span>

### <a name="overriding-existing-values-with-derived-dimensions"></a><span data-ttu-id="76eda-188">Bestaande waarden overschrijven met afgeleide dimensies</span><span class="sxs-lookup"><span data-stu-id="76eda-188">Overriding existing values with derived dimensions</span></span>
 
<span data-ttu-id="76eda-189">Het afgeleide dimensieproces overschrijft standaard bestaande waarden niet voor afgeleide dimensies.</span><span class="sxs-lookup"><span data-stu-id="76eda-189">By default, the derived dimension process doesn't override existing values for derived dimensions.</span></span> <span data-ttu-id="76eda-190">Als u kostenplaats 10 invoert en er geen andere dimensie wordt ingevoerd, worden afdeling 20 en locatie 30 standaard ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="76eda-190">For example, if you enter cost center 10, and no other dimension is entered, department 20 and location 30 are entered by default.</span></span> <span data-ttu-id="76eda-191">Als u de kostenplaats wijzigt, worden de waarden die al zijn ingevoerd niet meer gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="76eda-191">However, if you change the cost center, the values that have already been established aren't changed.</span></span> <span data-ttu-id="76eda-192">Daarom kunt u standaarddimensies voor hoofdrecords maken. Deze dimensies worden niet gewijzigd door afgeleide dimensies.</span><span class="sxs-lookup"><span data-stu-id="76eda-192">Therefore, you can establish default dimensions on master records, and those dimensions won't be changed by derived dimensions.</span></span>

<span data-ttu-id="76eda-193">U kunt de werking van afgeleide dimensies om bestaande waarden te overschrijven wijzigen door het selecteren van het selectievakje **Bestaande dimensiewaarden vervangen door afgeleide waarden** op de pagina **Afgeleide dimensies**.</span><span class="sxs-lookup"><span data-stu-id="76eda-193">You can change the behavior of derived dimensions to override existing values by selecting the **Replace existing dimension values with derived values** check box on the **Derived dimensions** page.</span></span> <span data-ttu-id="76eda-194">Als dit veld is geselecteerd, kunt u een dimensie met afgeleide dimensiewaarden invoeren en overschrijven deze afgeleide dimensiewaarden alle waarden die al bestaan.</span><span class="sxs-lookup"><span data-stu-id="76eda-194">If this field is selected, you can enter a dimension with derived dimension values and those derived dimension values will override any values that already exist.</span></span> <span data-ttu-id="76eda-195">Als u in het vorige voorbeeld bijvoorbeeld kostenplaats 10 invoert en er geen andere dimensie wordt ingevoerd, worden afdeling 20 en locatie 30 standaard ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="76eda-195">Using the previous example, if you enter cost center 10, and no other dimension is entered, department 20 and location 30 are entered by default.</span></span> <span data-ttu-id="76eda-196">Echter, als de waarden al afdeling 50 en locatie 60 waren, worden de waarden nu gewijzigd in afdeling 20 en locatie 30.</span><span class="sxs-lookup"><span data-stu-id="76eda-196">However, if the values were already department 50 and location 60, the values will now be changed to department 20 and location 30.</span></span>
 
<span data-ttu-id="76eda-197">Afgeleide dimensies met deze instelling vervangen niet automatisch de bestaande standaardwaarden voor dimensies wanneer standaardwaarden voor dimensies worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="76eda-197">Derived dimensions with this setting do not automatically replace the existing default dimensions values when dimension values are defaulted.</span></span> <span data-ttu-id="76eda-198">Dimensiewaarden worden alleen overschreven wanneer u een nieuwe dimensiewaarde op een pagina invoert en er bestaande afgeleide waarden voor die dimensie op de pagina zijn.</span><span class="sxs-lookup"><span data-stu-id="76eda-198">Dimension values will only be overridden when you enter a new dimension value on a page and there are existing derived values for that dimension on the page.</span></span>

### <a name="preventing-changes-with-derived-dimensions"></a><span data-ttu-id="76eda-199">Wijzigingen met afgeleide dimensies voorkomen</span><span class="sxs-lookup"><span data-stu-id="76eda-199">Preventing changes with derived dimensions</span></span>
 
<span data-ttu-id="76eda-200">Als u **Segment toevoegen** gebruikt op de **pagina Afgeleide dimensies** om een segment toe te voegen als een afgeleide dimensie, is er onder aan de pagina **Segment toevoegen** een optie waarmee u wijzigingen in die dimensie kunt voorkomen wanneer deze op een pagina wordt afgeleid.</span><span class="sxs-lookup"><span data-stu-id="76eda-200">When you use **Add segment"** on the **Derived dimensions page** to add a segment as a derived dimension, an option is provided at the bottom of the **Add segment** page that allows you to prevent changes to that dimension when it is derived on a page.</span></span> <span data-ttu-id="76eda-201">De standaardinstelling is uitgeschakeld, zodat niet wordt voorkomen dat de afgeleide dimensiewaarden worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="76eda-201">The default setting is off so it does not prevent the derived dimension values from being changed.</span></span> <span data-ttu-id="76eda-202">Wijzig de instelling in **Ja** als u wilt voorkomen dat de dimensie wordt gewijzigd nadat deze is afgeleid.</span><span class="sxs-lookup"><span data-stu-id="76eda-202">Change the setting to **Yes** if you want prevent the dimension from being changed after it has been derived.</span></span> <span data-ttu-id="76eda-203">Als de waarde voor de dimensie Afdeling bijvoorbeeld is afgeleid van de waarde van de dimensie Kostenplaats, kan de waarde van Afdeling niet worden gewijzigd als de instelling **Wijzigingen voorkomen** **Ja** is.</span><span class="sxs-lookup"><span data-stu-id="76eda-203">For example, if the value for the Department dimension is derived from the value of the Cost center dimension, the Department value cannot be changed if the **Prevent changes** setting is **Yes**.</span></span> 
 
<span data-ttu-id="76eda-204">De instelling voorkomt geen wijzigingen als de dimensiewaarde geldig is, maar deze niet wordt vermeld in de lijst met afgeleide dimensies.</span><span class="sxs-lookup"><span data-stu-id="76eda-204">The setting does not prevent changes if the dimension value is valid but it is not listed in the derived dimensions list.</span></span> <span data-ttu-id="76eda-205">Als Afdeling 20 bijvoorbeeld is afgeleid van Kostenplaats 10 en u Kostenplaats 10 invoert, kunt u Afdeling 20 niet bewerken.</span><span class="sxs-lookup"><span data-stu-id="76eda-205">For example, if Department 20 is derived from Cost center 10 and you enter Cost center 10, then you will not be able to edit Department 20.</span></span> <span data-ttu-id="76eda-206">Als u echter Kostenplaats 20 invoert en dit is niet in de lijst van afgeleide dimensies voor de kostenplaats staat, kunt u de waarde Afdeling wel bewerken.</span><span class="sxs-lookup"><span data-stu-id="76eda-206">However, if you enter Cost center 20 and it is not in the list of derived dimensions for Cost center, then you can edit the Department value.</span></span> 
 
<span data-ttu-id="76eda-207">In alle gevallen worden de rekeningwaarde en alle dimensiewaarden nog steeds gevalideerd tegen de rekeningstructuren nadat de afgeleide dimensiewaarden zijn toegepast.</span><span class="sxs-lookup"><span data-stu-id="76eda-207">In all cases, the account value and all dimensions values will still be validated against the account structures after the derived dimensions values have been applied.</span></span> <span data-ttu-id="76eda-208">Als u afgeleide dimensies gebruikt en de validatie ervan mislukt wanneer ze op een pagina worden gebruikt, moet u de afgeleide dimensiewaarden op de pagina met afgeleide dimensies wijzigen voordat u ze in transacties kunt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="76eda-208">If you use derived dimensions and they fail validation when used on a page, you must change the derived dimensions values on the derived dimensions page before you can use them in transactions.</span></span> 
 
<span data-ttu-id="76eda-209">Wanneer u dimensies wijzigt op het sneltabblad **Financiële dimensies**, is de dimensie die is gemarkeerd om wijzigingen te voorkomen, niet bewerkbaar.</span><span class="sxs-lookup"><span data-stu-id="76eda-209">When you change dimensions on the **Financials dimensions** FastTab, the dimension that is marked to prevent changes will not be editable.</span></span> <span data-ttu-id="76eda-210">Als u een rekening en dimensies in het besturingselement met gesegmenteerde invoer invoert op een pagina, zijn de dimensies bewerkbaar.</span><span class="sxs-lookup"><span data-stu-id="76eda-210">If you are entering an account and dimensions into the segmented entry control on a page, the dimensions are editable.</span></span> <span data-ttu-id="76eda-211">Wanneer u echter de markering uit het besturingselement voor gesegmenteerde invoer verplaatst en naar een ander veld gaat of een actie uitvoert, worden de rekening en de dimensies gevalideerd tegen de lijst met afgeleide dimensies en de rekeningstructuren om te zorgen dat u de juiste waarden hebt ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="76eda-211">However, when you move the highlight off the segmented entry control and move to another field or take an action, the account and dimensions will be validated against the derived dimensions list and the account structures to ensure that you have entered the appropriate values.</span></span> 

### <a name="derived-dimensions-and-entities"></a><span data-ttu-id="76eda-212">Afgeleide dimensies en entiteiten</span><span class="sxs-lookup"><span data-stu-id="76eda-212">Derived dimensions and entities</span></span>

<span data-ttu-id="76eda-213">U kunt de segmenten en waarden van afgeleide dimensies instellen met behulp van entiteiten.</span><span class="sxs-lookup"><span data-stu-id="76eda-213">You can set up the derived dimensions segments and values by using entities.</span></span>

- <span data-ttu-id="76eda-214">Met de entiteit Afgeleide dimensies configureert u de aansturende dimensies en de segmenten die worden gebruikt voor deze dimensies.</span><span class="sxs-lookup"><span data-stu-id="76eda-214">The Derived dimensions entity sets up the driving dimensions and the segments that are used for those dimensions.</span></span>
- <span data-ttu-id="76eda-215">Met de entiteit Afgeleide dimensiewaarde kunt u de waarden importeren die moeten worden afgeleid voor elke aansturende dimensie.</span><span class="sxs-lookup"><span data-stu-id="76eda-215">The Derived dimensions value entity lets you import the values that should be derived for each driving dimension.</span></span>

<span data-ttu-id="76eda-216">Wanneer u een entiteit gebruikt om gegevens te importeren en er met die entiteit dimensies worden geïmporteerd, worden de afgeleide dimensieregels toegepast tijdens het importeren, tenzij de entiteit die dimensies specifiek overschrijft.</span><span class="sxs-lookup"><span data-stu-id="76eda-216">When you use an entity to import data, if that entity imports dimensions, the derived dimension rules are applied during the import unless the entity specifically overrides those dimensions.</span></span>

<span data-ttu-id="76eda-217">Zie de volgende onderwerpen voor meer informatie:</span><span class="sxs-lookup"><span data-stu-id="76eda-217">For more information, see the following topics:</span></span>

- [<span data-ttu-id="76eda-218">Financiële dimensies definiëren</span><span class="sxs-lookup"><span data-stu-id="76eda-218">Define financial dimensions</span></span>](tasks/define-financial-dimensions.md)
- [<span data-ttu-id="76eda-219">Standaardsjablonen voor financiële dimensies onderhouden</span><span class="sxs-lookup"><span data-stu-id="76eda-219">Maintain financial dimension default templates</span></span>](tasks/maintain-financial-dimension-default-templates.md)