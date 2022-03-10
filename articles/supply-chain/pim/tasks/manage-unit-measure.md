---
title: Maateenheden beheren
description: In dit onderwerp wordt beschreven hoe u een maateenheid definieert, vertalingen voor de eenheid en de beschrijving ervan opgeeft en conversieregels voor gerelateerde eenheden definieert.
author: t-benebo
ms.date: 04/09/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e13897396810507bb4b2cbb415b873eb3dd7f4e8
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565514"
---
# <a name="manage-units-of-measure"></a>Maateenheden beheren

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een maateenheid definieert, vertalingen voor de eenheid en de beschrijving ervan opgeeft en conversieregels voor gerelateerde eenheden definieert.

## <a name="open-the-units-page"></a>De pagina Eenheden openen

Als u de maateenheden wilt maken die beschikbaar zijn in uw systeem en ermee wilt werken, gaat u naar **Organisatiebeheer \> Instellingen \> Eenheden \> Eenheden**.

In de overige secties van dit onderwerp wordt beschreven wat u op de pagina **Eenheden** kunt doen.

## <a name="create-standard-units-and-conversions"></a>Standaardeenheden en conversies maken

Als uw systeem nog niet de meest gangbare maateenheden voor het metrieke systeem en/of het USCS (US Customary System) bevat, kan de wizard Eenheden instellen u helpen snel aan de slag te gaan met definities en conversies voor de basiseenheden. Als u de wizard wilt doorlopen, selecteert u **Wizard Eenheid maken** in het actievenster en volgt u de instructies op het scherm.

## <a name="create-or-edit-a-unit-of-measure"></a>Een maateenheid maken of bewerken

Volg deze stappen om een maateenheid te maken of te bewerken.

1. Volg één van deze stappen:

    - Als u een bestaande eenheid wilt bewerken, selecteert u deze in het lijstvenster.
    - Selecteer in het actievenster **Nieuw** om een nieuwe maateenheid te maken.

1. Stel in de koptekst van de record de volgende velden in:

    - **Eenheid**: Voer de id of het symbool in die moet worden gebruikt om naar de eenheid te verwijzen in de systeemtaal. Deze id of dit symbool is meestal een algemene afkorting voor de eenheid, zoals *st* voor stuks of *cm* voor centimeter.
    - **Beschrijving**: Voer een beschrijvende naam in voor de maateenheid in de systeemtaal. Deze naam is meestal de volledige naam van de eenheid, zoals *stuks* of *Centimeter*.

1. Stel op het sneltabblad **Algemeen** de volgende velden in:<!-- KFM: confirm this:    - **Fixed unit assignment** and **Fixed unit** – These fields have an effect only if you're using the Microsoft Retail Essentials product. If the current unit can be mapped to one of the fixed units that are used by Retail Essentials, set the **Fixed unit assignment** option to *Yes*. Then select the fixed unit in the **Fixed unit** field. -->

    - **Eenheidsklasse**: selecteer de eigenschap die de eenheid meet (zoals lengte, oppervlak, massa of hoeveelheid).
    - **Eenhedenstelsel**: selecteer het meetsysteem waar de eenheid deel van uitmaakt (*Metrieke eenheden* of *United States Customary Units*).
    - **Basiseenheid**: Stel deze optie in op *Ja* als u de huidige eenheid wilt gebruiken als basiseenheid voor de eenheidsklasse waartoe het behoort. In dit geval hoeft u alleen de omrekeningsfactor op te geven tussen de basiseenheid en elke aanvullende eenheid in de eenheidsklasse. Het systeem kan vervolgens omrekenen tussen alle eenheden in die eenheidsklasse. Daarom is het eenvoudiger om omrekeningen in te stellen.

        Als gallon bijvoorbeeld de basiseenheid is voor de eenheidsklasse *Volume*, hoeft u alleen omrekeningsfactoren in te stellen van quart naar gallon en van pint naar gallon. Het systeem kan vervolgens ook omrekenen van quart naar pint.

        U kunt slechts één basiseenheid per eenheidsklasse instellen.

    - **Systeemeenheid**: Stel deze optie in op *Ja* als u de huidige eenheid wilt gebruiken als de aangenomen eenheid voor alle niet-gespecificeerde meeteenheden in de eenheidsklasse. Als bijvoorbeeld een veld waarin een hoeveelheid wordt ingevoerd geen eenheid mag opgeven (of als de gebruiker geen eenheid selecteert), wordt de eenheid gebruikt die is ingesteld als systeemeenheid voor de eenheidsklasse *Hoeveelheid*. U kunt slechts één systeemeenheid per eenheidsklasse instellen.
    - **Decimale precisie**: Geef het aantal decimalen op waarop de waarden moeten worden afgerond die zijn opgegeven voor de huidige eenheid of waarnaar ze moeten worden omgerekend.

1. Selecteer **Opslaan** in het actievenster.

## <a name="define-unit-translations"></a>Eenheidsvertalingen definiëren

Volg deze stappen om vertalingen te definiëren voor de id of het symbool en de beschrijving van een maateenheid.

1. Maak of selecteer de eenheid waarvoor u vertalingen wilt maken.
1. Selecteer in het actievenster de optie **Eenheidsteksten**.

    De pagina **Eenheidsteksten** wordt geopend. Op deze pagina definieert u vertalingen voor de id of het symbool voor de geselecteerde eenheid. Deze vertalingen kunnen vervolgens worden gebruikt op externe documenten in klantspecifieke of leverancierspecifieke talen.

1. Selecteer **Nieuw** in het actievenster.
1. Voer in het veld **Taal** de taal in waarnaar de eenheids-id of het symbool moet worden vertaald.
1. Voer in het veld **Tekst** de vertaling van de eenheids-ID of het eenheidssymbool in de geselecteerde taal in.
1. Selecteer **Opslaan** in het actievenster.
1. Sluit de pagina.
1. Selecteer in het **actievenster** de optie **Vertaalde eenheidsbeschrijvingen**.

    De pagina **Vertaalde eenheidsbeschrijvingen** wordt geopend. Op deze pagina definieert u taalspecifieke beschrijvingen voor de geselecteerde eenheid.

1. Selecteer **Nieuw** in het actievenster.
1. Voer in het veld **Taal** de taal in waarnaar de beschrijving van de eenheid moet worden vertaald.
1. Voer in het veld **Beschrijving** de vertaling van de beschrijving in de geselecteerde taal in.
1. Selecteer **Opslaan** in het actievenster.
1. Sluit de pagina.

## <a name="define-unit-conversion-rules"></a>Regels voor eenheidsconversie definiëren

Volg deze stappen om regels te definiëren voor omrekeningen tussen maateenheden.

1. Maak of selecteer de eenheid waarvoor u omrekeningsregels wilt maken.
1. Selecteer in het actievenster de optie **Eenheidsomrekeningen**.

    De pagina **Eenheidsomrekeningen** wordt geopend. Op deze pagina definieert u regels voor het omrekenen van de maateenheid van en naar andere maateenheden in de eenheidsklasse.

1. Selecteer een van de volgende tabbladen, afhankelijk van het type omrekening dat u wilt instellen:

    - **Standaardomrekeningen**: Configureer standaardomrekenregels voor alle producten.
    - **Omrekeningen binnen klasse**: Configureer productspecifieke omrekenregels voor maateenheden in dezelfde eenheidsklasse.
    - **Omrekeningen tussen klassen**: Configureer productspecifieke omrekenregels voor maateenheden in verschillende eenheidsklassen.

1. Volg één van deze stappen:

    - Selecteer in het actievenster **Nieuw** om een nieuwe omrekening te maken.
    - Als u een bestaande omrekening wilt bewerken, selecteert u de omrekening in het raster en selecteert u vervolgens **Bewerken** op de werkbalk.

1. Stel in het dialoogvenster met de vervolgkeuzelijsten de volgende velden in:

    - **Product**: Selecteer het specifieke product waarop de omrekening van toepassing is. Dit veld is alleen beschikbaar voor omrekeningen binnen een klasse en tussen verschillende klassen.
    - **Formule-indeling**: Laat dit veld ingesteld op *Eenvoudig* om een eenvoudige omrekening op te geven met één factor. Stel het veld in op *Geavanceerd* om een meer ingewikkelde vergelijking in te stellen. De indeling voor geavanceerde vergelijkingen varieert, afhankelijk van de eenheidsklasse.
    - **Van eenheid**: Dit veld geeft de geselecteerde eenheid weer. Normaal gesproken hoeft de waarde niet te wijzigen. (Als u de waarde wijzigt, moet u de pagina **Eenheidsomrekeningen** voor de geselecteerde eenheid openen om de nieuwe omrekening weer te geven nadat u deze hebt opgeslagen.)
    - **Naar eenheid**: Selecteer de eenheid waarnaar u wilt converteren.
    - **Afronding**: Selecteer hoe decimalen moeten worden afgerond op basis van de waarde in **Decimale precisie** van de geselecteerde eenheid (*Naar dichtstbijzijnde*, *Omhoog* of *Omlaag*).
    - **Omrekeningsformule**: In de overige velden boven in het dialoogvenster kunt u de formule opgeven voor het omrekenen tussen de twee eenheden. Welke velden beschikbaar zijn varieert, afhankelijk van de eenheidsklasse en formule-indeling die u hebt geselecteerd.

1. Selecteer **OK**.
1. Sluit de pagina.

> [!TIP]
> U kunt ook eenheidsomrekeningen instellen per productvariant. Meer informatie over dit onderwerp vindt u in [Conversie van maateenheid per productvariant](../uom-conversion-per-product-variant.md).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
