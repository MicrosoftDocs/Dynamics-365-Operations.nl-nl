---
title: Maateenheden beheren
description: In dit onderwerp wordt beschreven hoe u een maateenheid definieert, vertalingen voor de eenheid en de beschrijving ervan opgeeft en conversieregels voor gerelateerde eenheden definieert.
author: sorenva
ms.date: 04/09/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d36839cd8e3398225d3421bf0f268068599ca49f
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921336"
---
# <a name="manage-units-of-measure"></a><span data-ttu-id="976a3-103">Maateenheden beheren</span><span class="sxs-lookup"><span data-stu-id="976a3-103">Manage units of measure</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="976a3-104">In dit onderwerp wordt beschreven hoe u een maateenheid definieert, vertalingen voor de eenheid en de beschrijving ervan opgeeft en conversieregels voor gerelateerde eenheden definieert.</span><span class="sxs-lookup"><span data-stu-id="976a3-104">This topic describes how to define a unit of measure, provide translations for the unit and its description, and define conversion rules for related units.</span></span>

## <a name="open-the-units-page"></a><span data-ttu-id="976a3-105">De pagina Eenheden openen</span><span class="sxs-lookup"><span data-stu-id="976a3-105">Open the Units page</span></span>

<span data-ttu-id="976a3-106">Als u de maateenheden wilt maken die beschikbaar zijn in uw systeem en ermee wilt werken, gaat u naar **Organisatiebeheer \> Instellingen \> Eenheden \> Eenheden**.</span><span class="sxs-lookup"><span data-stu-id="976a3-106">To create and work with the units of measure that are available in your system, go to **Organization administration \> Setup \> Units \> Units**.</span></span>

<span data-ttu-id="976a3-107">In de overige secties van dit onderwerp wordt beschreven wat u op de pagina **Eenheden** kunt doen.</span><span class="sxs-lookup"><span data-stu-id="976a3-107">The remaining sections of this topic describe what you can do on the **Units** page.</span></span>

## <a name="create-standard-units-and-conversions"></a><span data-ttu-id="976a3-108">Standaardeenheden en conversies maken</span><span class="sxs-lookup"><span data-stu-id="976a3-108">Create standard units and conversions</span></span>

<span data-ttu-id="976a3-109">Als uw systeem nog niet de meest gangbare maateenheden voor het metrieke systeem en/of het USCS (US Customary System) bevat, kan de wizard Eenheden instellen u helpen snel aan de slag te gaan met definities en conversies voor de basiseenheden.</span><span class="sxs-lookup"><span data-stu-id="976a3-109">If your system doesn't already include the most commonly used units of measure for the metric system and/or the US customary system (USCS), the unit setup wizard can help you quickly get started with basic unit definitions and conversions.</span></span> <span data-ttu-id="976a3-110">Als u de wizard wilt doorlopen, selecteert u **Wizard Eenheid maken** in het actievenster en volgt u de instructies op het scherm.</span><span class="sxs-lookup"><span data-stu-id="976a3-110">To complete the wizard, select **Unit creation wizard** on the Action Pane, and then follow the on-screen instructions.</span></span>

## <a name="create-or-edit-a-unit-of-measure"></a><span data-ttu-id="976a3-111">Een maateenheid maken of bewerken</span><span class="sxs-lookup"><span data-stu-id="976a3-111">Create or edit a unit of measure</span></span>

<span data-ttu-id="976a3-112">Volg deze stappen om een maateenheid te maken of te bewerken.</span><span class="sxs-lookup"><span data-stu-id="976a3-112">To create or edit a unit of measure, follow these steps.</span></span>

1. <span data-ttu-id="976a3-113">Volg één van deze stappen:</span><span class="sxs-lookup"><span data-stu-id="976a3-113">Follow one of these steps:</span></span>

    - <span data-ttu-id="976a3-114">Als u een bestaande eenheid wilt bewerken, selecteert u deze in het lijstvenster.</span><span class="sxs-lookup"><span data-stu-id="976a3-114">To edit an existing unit, select it in the list pane.</span></span>
    - <span data-ttu-id="976a3-115">Selecteer in het actievenster **Nieuw** om een nieuwe maateenheid te maken.</span><span class="sxs-lookup"><span data-stu-id="976a3-115">To create a new unit, select **New** on the Action Pane.</span></span>

1. <span data-ttu-id="976a3-116">Stel in de koptekst van de record de volgende velden in:</span><span class="sxs-lookup"><span data-stu-id="976a3-116">On the header of the record, set the following fields:</span></span>

    - <span data-ttu-id="976a3-117">**Eenheid**: Voer de id of het symbool in die moet worden gebruikt om naar de eenheid te verwijzen in de systeemtaal.</span><span class="sxs-lookup"><span data-stu-id="976a3-117">**Unit** – Enter the ID or symbol to use to refer to the unit in the system language.</span></span> <span data-ttu-id="976a3-118">Deze id of dit symbool is meestal een algemene afkorting voor de eenheid, zoals *st* voor stuks of *cm* voor centimeter.</span><span class="sxs-lookup"><span data-stu-id="976a3-118">This ID or symbol is usually a common abbreviation for the unit, such as *ea* for each or *cm* for centimeter.</span></span>
    - <span data-ttu-id="976a3-119">**Beschrijving**: Voer een beschrijvende naam in voor de maateenheid in de systeemtaal.</span><span class="sxs-lookup"><span data-stu-id="976a3-119">**Description** – Enter a descriptive name for the unit in the system language.</span></span> <span data-ttu-id="976a3-120">Deze naam is meestal de volledige naam van de eenheid, zoals *stuks* of *Centimeter*.</span><span class="sxs-lookup"><span data-stu-id="976a3-120">This name is usually the full name of the unit, such as *Each* or *Centimeter*.</span></span>

1. <span data-ttu-id="976a3-121">Stel op het sneltabblad **Algemeen** de volgende velden in:</span><span class="sxs-lookup"><span data-stu-id="976a3-121">On the **General** FastTab, set the following fields:</span></span><!-- KFM: confirm this:    - **Fixed unit assignment** and **Fixed unit** – These fields have an effect only if you're using the Microsoft Retail Essentials product. If the current unit can be mapped to one of the fixed units that are used by Retail Essentials, set the **Fixed unit assignment** option to *Yes*. Then select the fixed unit in the **Fixed unit** field. -->

    - <span data-ttu-id="976a3-122">**Eenheidsklasse**: selecteer de eigenschap die de eenheid meet (zoals lengte, oppervlak, massa of hoeveelheid).</span><span class="sxs-lookup"><span data-stu-id="976a3-122">**Unit class** – Select the property that the unit measures (such as length, area, mass, or quantity).</span></span>
    - <span data-ttu-id="976a3-123">**Eenhedenstelsel**: selecteer het meetsysteem waar de eenheid deel van uitmaakt (*Metrieke eenheden* of *United States Customary Units*).</span><span class="sxs-lookup"><span data-stu-id="976a3-123">**System of units** – Select the measurement system that the unit belongs to (*Metric units* or *United States customary units*).</span></span>
    - <span data-ttu-id="976a3-124">**Basiseenheid**: Stel deze optie in op *Ja* als u de huidige eenheid wilt gebruiken als basiseenheid voor de eenheidsklasse waartoe het behoort.</span><span class="sxs-lookup"><span data-stu-id="976a3-124">**Base unit** – Set this option to *Yes* to use the current unit as the base unit for its unit class.</span></span> <span data-ttu-id="976a3-125">In dit geval hoeft u alleen de omrekeningsfactor op te geven tussen de basiseenheid en elke aanvullende eenheid in de eenheidsklasse.</span><span class="sxs-lookup"><span data-stu-id="976a3-125">In this case, you only have to specify the conversion factor between the base unit and each additional unit in the unit class.</span></span> <span data-ttu-id="976a3-126">Het systeem kan vervolgens omrekenen tussen alle eenheden in die eenheidsklasse.</span><span class="sxs-lookup"><span data-stu-id="976a3-126">The system can then convert between all units in that unit class.</span></span> <span data-ttu-id="976a3-127">Daarom is het eenvoudiger om omrekeningen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="976a3-127">Therefore, it's easier to set up conversions.</span></span>

        <span data-ttu-id="976a3-128">Als gallon bijvoorbeeld de basiseenheid is voor de eenheidsklasse *Volume*, hoeft u alleen omrekeningsfactoren in te stellen van quart naar gallon en van pint naar gallon.</span><span class="sxs-lookup"><span data-stu-id="976a3-128">For example, if gallon is the base unit for the *Volume* unit class, you only have to set up conversion factors from quart to gallon and from pint to gallon.</span></span> <span data-ttu-id="976a3-129">Het systeem kan vervolgens ook omrekenen van quart naar pint.</span><span class="sxs-lookup"><span data-stu-id="976a3-129">The system can then also convert from quart to pint.</span></span>

        <span data-ttu-id="976a3-130">U kunt slechts één basiseenheid per eenheidsklasse instellen.</span><span class="sxs-lookup"><span data-stu-id="976a3-130">You can have only one base unit per unit class.</span></span>

    - <span data-ttu-id="976a3-131">**Systeemeenheid**: Stel deze optie in op *Ja* als u de huidige eenheid wilt gebruiken als de aangenomen eenheid voor alle niet-gespecificeerde meeteenheden in de eenheidsklasse.</span><span class="sxs-lookup"><span data-stu-id="976a3-131">**System unit** – Set this option to *Yes* to use the current unit as the assumed unit for all unspecified measurements in its unit class.</span></span> <span data-ttu-id="976a3-132">Als bijvoorbeeld een veld waarin een hoeveelheid wordt ingevoerd geen eenheid mag opgeven (of als de gebruiker geen eenheid selecteert), wordt de eenheid gebruikt die is ingesteld als systeemeenheid voor de eenheidsklasse *Hoeveelheid*.</span><span class="sxs-lookup"><span data-stu-id="976a3-132">For example, if a field that is used to enter a quantity doesn't allow a unit to be specified (of if the user doesn't select a unit), the system uses the unit that is set as the system unit for the *Quantity* unit class.</span></span> <span data-ttu-id="976a3-133">U kunt slechts één systeemeenheid per eenheidsklasse instellen.</span><span class="sxs-lookup"><span data-stu-id="976a3-133">You can have only one system unit per unit class.</span></span>
    - <span data-ttu-id="976a3-134">**Decimale precisie**: Geef het aantal decimalen op waarop de waarden moeten worden afgerond die zijn opgegeven voor de huidige eenheid of waarnaar ze moeten worden omgerekend.</span><span class="sxs-lookup"><span data-stu-id="976a3-134">**Decimal precision** – Specify the number of decimal places that values that are specified for the current unit or converted to it should be rounded to.</span></span>

1. <span data-ttu-id="976a3-135">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="976a3-135">On the Action Pane, select **Save**.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="976a3-136">Eenheidsvertalingen definiëren</span><span class="sxs-lookup"><span data-stu-id="976a3-136">Define unit translations</span></span>

<span data-ttu-id="976a3-137">Volg deze stappen om vertalingen te definiëren voor de id of het symbool en de beschrijving van een maateenheid.</span><span class="sxs-lookup"><span data-stu-id="976a3-137">To define translations for the ID or symbol and the description for a unit of measure, follow these steps.</span></span>

1. <span data-ttu-id="976a3-138">Maak of selecteer de eenheid waarvoor u vertalingen wilt maken.</span><span class="sxs-lookup"><span data-stu-id="976a3-138">Create or select the unit to create translations for.</span></span>
1. <span data-ttu-id="976a3-139">Selecteer in het actievenster de optie **Eenheidsteksten**.</span><span class="sxs-lookup"><span data-stu-id="976a3-139">On the Action Pane, select **Unit texts**.</span></span>

    <span data-ttu-id="976a3-140">De pagina **Eenheidsteksten** wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="976a3-140">The **Unit texts** page appears.</span></span> <span data-ttu-id="976a3-141">Op deze pagina definieert u vertalingen voor de id of het symbool voor de geselecteerde eenheid.</span><span class="sxs-lookup"><span data-stu-id="976a3-141">You use this page to define translations for the ID or symbol for the selected unit.</span></span> <span data-ttu-id="976a3-142">Deze vertalingen kunnen vervolgens worden gebruikt op externe documenten in klantspecifieke of leverancierspecifieke talen.</span><span class="sxs-lookup"><span data-stu-id="976a3-142">Those translations can then be used on external documents in customer-specific or vendor-specific languages.</span></span>

1. <span data-ttu-id="976a3-143">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="976a3-143">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="976a3-144">Voer in het veld **Taal** de taal in waarnaar de eenheids-id of het symbool moet worden vertaald.</span><span class="sxs-lookup"><span data-stu-id="976a3-144">In the **Language** field, select the language to translate the unit ID or symbol to.</span></span>
1. <span data-ttu-id="976a3-145">Voer in het veld **Tekst** de vertaling van de eenheids-ID of het eenheidssymbool in de geselecteerde taal in.</span><span class="sxs-lookup"><span data-stu-id="976a3-145">In the **Text** field, enter the translation of the unit ID or symbol in the selected language.</span></span>
1. <span data-ttu-id="976a3-146">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="976a3-146">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="976a3-147">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="976a3-147">Close the page.</span></span>
1. <span data-ttu-id="976a3-148">Selecteer in het **actievenster** de optie **Vertaalde eenheidsbeschrijvingen**.</span><span class="sxs-lookup"><span data-stu-id="976a3-148">On the **Action Pane**, select **Translated unit descriptions**.</span></span>

    <span data-ttu-id="976a3-149">De pagina **Vertaalde eenheidsbeschrijvingen** wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="976a3-149">The **Translated unit descriptions** page appears.</span></span> <span data-ttu-id="976a3-150">Op deze pagina definieert u taalspecifieke beschrijvingen voor de geselecteerde eenheid.</span><span class="sxs-lookup"><span data-stu-id="976a3-150">You use this page to define language-specific descriptions for the selected unit.</span></span>

1. <span data-ttu-id="976a3-151">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="976a3-151">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="976a3-152">Voer in het veld **Taal** de taal in waarnaar de beschrijving van de eenheid moet worden vertaald.</span><span class="sxs-lookup"><span data-stu-id="976a3-152">In the **Language** field, select the language to translate the unit description to.</span></span>
1. <span data-ttu-id="976a3-153">Voer in het veld **Beschrijving** de vertaling van de beschrijving in de geselecteerde taal in.</span><span class="sxs-lookup"><span data-stu-id="976a3-153">In the **Description** field, enter the translation of the unit description in the selected language.</span></span>
1. <span data-ttu-id="976a3-154">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="976a3-154">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="976a3-155">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="976a3-155">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="976a3-156">Regels voor eenheidsconversie definiëren</span><span class="sxs-lookup"><span data-stu-id="976a3-156">Define unit conversion rules</span></span>

<span data-ttu-id="976a3-157">Volg deze stappen om regels te definiëren voor omrekeningen tussen maateenheden.</span><span class="sxs-lookup"><span data-stu-id="976a3-157">To define rules for conversions between units of measure, follow these steps.</span></span>

1. <span data-ttu-id="976a3-158">Maak of selecteer de eenheid waarvoor u omrekeningsregels wilt maken.</span><span class="sxs-lookup"><span data-stu-id="976a3-158">Create or select the unit to define conversion rules for.</span></span>
1. <span data-ttu-id="976a3-159">Selecteer in het actievenster de optie **Eenheidsomrekeningen**.</span><span class="sxs-lookup"><span data-stu-id="976a3-159">On the Action Pane, select **Unit conversions**.</span></span>

    <span data-ttu-id="976a3-160">De pagina **Eenheidsomrekeningen** wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="976a3-160">The **Unit conversions** page appears.</span></span> <span data-ttu-id="976a3-161">Op deze pagina definieert u regels voor het omrekenen van de maateenheid van en naar andere maateenheden in de eenheidsklasse.</span><span class="sxs-lookup"><span data-stu-id="976a3-161">You use this page to define rules for converting the selected unit to and from other units in the unit class.</span></span>

1. <span data-ttu-id="976a3-162">Selecteer een van de volgende tabbladen, afhankelijk van het type omrekening dat u wilt instellen:</span><span class="sxs-lookup"><span data-stu-id="976a3-162">Select one of the following tabs, depending on the type of conversion that you want to set up:</span></span>

    - <span data-ttu-id="976a3-163">**Standaardomrekeningen**: Configureer standaardomrekenregels voor alle producten.</span><span class="sxs-lookup"><span data-stu-id="976a3-163">**Standard conversions** – Set up standard conversion rules for all products.</span></span>
    - <span data-ttu-id="976a3-164">**Omrekeningen binnen klasse**: Configureer productspecifieke omrekenregels voor maateenheden in dezelfde eenheidsklasse.</span><span class="sxs-lookup"><span data-stu-id="976a3-164">**Intra-class conversions** – Set up product-specific conversion rules for units in the same unit class.</span></span>
    - <span data-ttu-id="976a3-165">**Omrekeningen tussen klassen**: Configureer productspecifieke omrekenregels voor maateenheden in verschillende eenheidsklassen.</span><span class="sxs-lookup"><span data-stu-id="976a3-165">**Inter-class conversions** – Set up product-specific conversion rules for units across unit classes.</span></span>

1. <span data-ttu-id="976a3-166">Volg één van deze stappen:</span><span class="sxs-lookup"><span data-stu-id="976a3-166">Follow one of these steps:</span></span>

    - <span data-ttu-id="976a3-167">Selecteer in het actievenster **Nieuw** om een nieuwe omrekening te maken.</span><span class="sxs-lookup"><span data-stu-id="976a3-167">To create a new conversion, select **New** on the toolbar.</span></span>
    - <span data-ttu-id="976a3-168">Als u een bestaande omrekening wilt bewerken, selecteert u de omrekening in het raster en selecteert u vervolgens **Bewerken** op de werkbalk.</span><span class="sxs-lookup"><span data-stu-id="976a3-168">To edit an existing conversion, select the conversion in the grid, and then select **Edit** on the toolbar.</span></span>

1. <span data-ttu-id="976a3-169">Stel in het dialoogvenster met de vervolgkeuzelijsten de volgende velden in:</span><span class="sxs-lookup"><span data-stu-id="976a3-169">In the drop-down dialog box that appears, set the following fields:</span></span>

    - <span data-ttu-id="976a3-170">**Product**: Selecteer het specifieke product waarop de omrekening van toepassing is.</span><span class="sxs-lookup"><span data-stu-id="976a3-170">**Product** – Select the specific product that the conversion applies to.</span></span> <span data-ttu-id="976a3-171">Dit veld is alleen beschikbaar voor omrekeningen binnen een klasse en tussen verschillende klassen.</span><span class="sxs-lookup"><span data-stu-id="976a3-171">This field is available only for intra-class and inter-class conversions.</span></span>
    - <span data-ttu-id="976a3-172">**Formule-indeling**: Laat dit veld ingesteld op *Eenvoudig* om een eenvoudige omrekening op te geven met één factor.</span><span class="sxs-lookup"><span data-stu-id="976a3-172">**Formula layout** – Leave this field set to *Simple* to specify a simple conversion that has a single factor.</span></span> <span data-ttu-id="976a3-173">Stel het veld in op *Geavanceerd* om een meer ingewikkelde vergelijking in te stellen.</span><span class="sxs-lookup"><span data-stu-id="976a3-173">Set it to *Advanced* to set up a more complex equation.</span></span> <span data-ttu-id="976a3-174">De indeling voor geavanceerde vergelijkingen varieert, afhankelijk van de eenheidsklasse.</span><span class="sxs-lookup"><span data-stu-id="976a3-174">The format for advanced equations varies, depending on the unit class.</span></span>
    - <span data-ttu-id="976a3-175">**Van eenheid**: Dit veld geeft de geselecteerde eenheid weer.</span><span class="sxs-lookup"><span data-stu-id="976a3-175">**From unit** – This field shows the selected unit.</span></span> <span data-ttu-id="976a3-176">Normaal gesproken hoeft de waarde niet te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="976a3-176">Usually, you should not change the value.</span></span> <span data-ttu-id="976a3-177">(Als u de waarde wijzigt, moet u de pagina **Eenheidsomrekeningen** voor de geselecteerde eenheid openen om de nieuwe omrekening weer te geven nadat u deze hebt opgeslagen.)</span><span class="sxs-lookup"><span data-stu-id="976a3-177">(If you do change the value, you must open the **Unit conversions** page for the selected unit to view your new conversion after you save it.)</span></span>
    - <span data-ttu-id="976a3-178">**Naar eenheid**: Selecteer de eenheid waarnaar u wilt converteren.</span><span class="sxs-lookup"><span data-stu-id="976a3-178">**To unit** – Select the unit to convert to.</span></span>
    - <span data-ttu-id="976a3-179">**Afronding**: Selecteer hoe decimalen moeten worden afgerond op basis van de waarde in **Decimale precisie** van de geselecteerde eenheid (*Naar dichtstbijzijnde*, *Omhoog* of *Omlaag*).</span><span class="sxs-lookup"><span data-stu-id="976a3-179">**Rounding** – Select how fractions should be rounded, based on the **Decimal precision** value of the selected unit (*To nearest*, *Up*, or *Down*).</span></span>
    - <span data-ttu-id="976a3-180">**Omrekeningsformule**: In de overige velden boven in het dialoogvenster kunt u de formule opgeven voor het omrekenen tussen de twee eenheden.</span><span class="sxs-lookup"><span data-stu-id="976a3-180">**Conversion formula** – Use the remaining fields at the top of the drop-down dialog box to specify the formula for converting between the two units.</span></span> <span data-ttu-id="976a3-181">Welke velden beschikbaar zijn varieert, afhankelijk van de eenheidsklasse en formule-indeling die u hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="976a3-181">The available fields vary, depending on the unit class and formula layout that you've selected.</span></span>

1. <span data-ttu-id="976a3-182">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="976a3-182">Select **OK**.</span></span>
1. <span data-ttu-id="976a3-183">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="976a3-183">Close the page.</span></span>

> [!TIP]
> <span data-ttu-id="976a3-184">U kunt ook eenheidsomrekeningen instellen per productvariant.</span><span class="sxs-lookup"><span data-stu-id="976a3-184">You can also set up unit conversions per product variant.</span></span> <span data-ttu-id="976a3-185">Meer informatie over dit onderwerp vindt u in [Conversie van maateenheid per productvariant](../uom-conversion-per-product-variant.md).</span><span class="sxs-lookup"><span data-stu-id="976a3-185">For more information, see [Unit of measure conversion per product variant](../uom-conversion-per-product-variant.md).</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
