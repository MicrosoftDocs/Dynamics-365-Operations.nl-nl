---
title: Aanvulling op basis van zonedrempels
description: Bij het aanvullen op basis van zones wordt een min/max-aanvullingsstrategie (minimum/maximum) gebruikt, maar gehele magazijnzones worden geëvalueerd in plaats van afzonderlijke locaties. Daarom kunnen magazijnbeheerders sneller ervaren wanneer er extra voorraad nodig is in een orderverzamelzone.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocDirHint, WHSLocDirTable, WHSRequestType
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 2e83d6885bf7400916d633a49d3b19b8843b0269
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965497"
---
# <a name="zone-threshold-replenishment"></a>Aanvulling op basis van zonedrempels

[!include [banner](../includes/banner.md)]

Bij het aanvullen op basis van zones wordt een [min/max-aanvullingsstrategie](replenishment.md) (minimum/maximum) gebruikt, maar gehele magazijnzones worden geëvalueerd in plaats van afzonderlijke locaties. Daarom kunnen magazijnbeheerders sneller ervaren wanneer er extra voorraad nodig is in een orderverzamelzone.

De instelling voor deze functie is vergelijkbaar met de instelling voor aanvulling op basis van locatie. Wanneer u echter een sjabloon instelt voor min/max-aanvulling, kunt u ook opgeven of de drempel per locatie of per zone moet worden geëvalueerd. Als u een evaluatie instelt die is gebaseerd op zones, moet u specifieke zones toevoegen aan de query voor zoneselectie.

Net als bij op locatie gebaseerde min/max-aanvulling, is op zones gebaseerde min/max-aanvulling gebaseerd op de configuratie van een drempel voor minimumvoorraad die het aanmaken van aanvullingswerk voor geselecteerde artikelen triggert. Met dit aanvulllingswerk wordt de voorraad verhoogd tot de opgegeven maximumdrempel voor de zone.

> [!NOTE]
> Aanvullingsprocessen voor zones voor productvarianten worden niet ondersteund in de huidige versie.


In tegenstelling tot min/max-aanvulling op basis van locaties, vereist op zones gebaseerde min/max-aanvulling geen vaste locaties om te evalueren of op een locatie een specifiek artikel moet worden opgeslagen. Daarom kunt u met behulp van op zones gebaseerde aanvulling min/max-aanvulling gebruiken, ook als u geen vaste locaties hebt voor elk artikel of elke artikelvariant in het magazijn. Wanneer een hoeveelheid in de zone onder de opgegeven minimum drempel zakt, wordt het aanvullingswerk gemaakt. In de locatie-instructies wordt bepaald op welke specifieke locatie de voorraad moet worden weggezet.

## <a name="turn-on-the-zone-threshold-replenishment-feature"></a>De functie Aanvulling op basis van zonedrempels inschakelen

Voordat u de functie *Aanvulling op basis van zonedrempels* kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en desgewenst in te schakelen. Schakel in het werkgebied **Functiebeheer** de functie als volgt in:

- **Module:** *Magazijnbeheer*
- **Functienaam:** *Aanvulling op basis van zonedrempels*

## <a name="set-up-zone-based-replenishment"></a><a name="setup"></a>Aanvulling op basis van zones instellen

Als u aanvulling op basis van zones wilt instellen, moet u verschillende onderdelen van het systeem configureren. In deze sectie worden de verschillende instellingen geïntroduceerd en worden waarden voor demogegevens weergegeven die u kunt invoeren als u het scenario aan het einde van dit onderwerp wilt doorlopen.

### <a name="set-up-directive-codes"></a>Instructiecodes instellen

Met [instructiecodes](control-warehouse-location-directives.md) kunt u specifieker bepalen welke locatiesjabloon in een werksjabloon wordt gebruikt. Met elke code wordt een algemene waarde ingesteld waarnaar u kunt verwijzen wanneer u elk type sjabloon configureert.

#### <a name="view-and-edit-directive-codes"></a>Instructiecodes weergeven en bewerken

Om de instructiecodes weer te geven of te bewerken, gaat u naar **Magazijnbeheer \> Instellingen \> Instructiecodes**.

#### <a name="prepare-demo-data-directive-codes"></a>Instructiecodes voor demogegevens voorbereiden

In dit voorbeeld wordt getoond hoe u een instructiecode voorbereidt. Als u het scenario aan het einde van dit onderwerp wilt doorlopen, gebruikt u de voorbeeldgegevenswaarden die hier worden getoond. Gebruik anders uw eigen waarden.

1. Selecteer de rechtspersoon **USMF** om te werken met de demogegevens.
1. Ga naar **Magazijnbeheer \> Instellen \> Instructiecodes**.
1. Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster.
1. Stel in de nieuwe rij de volgende waarden in:

    - **Instructiecode:** _Zoneaanvulling_
    - **Instructiebeschrijving:** _Zoneaanvulling_

1. Selecteer **Opslaan** om de nieuwe code op te slaan.

### <a name="set-up-replenishment-templates"></a>Aanvullingssjablonen instellen

[Sjablonen voor min/max-aanvulling](tasks/set-up-min-max-replenishment-process.md) zijn het belangrijkste mechanisme voor het onderhouden van optimale niveaus op orderverzamellocaties. In deze sjablonen moet u de regels instellen die worden gebruikt om voorraad aan te vullen in het magazijn. De aanvulling waarvoor de sjablonen kunnen worden gebruikt, omvatten aanvulling op basis van zones.

#### <a name="view-and-edit-replenishment-templates"></a>Aanvullingssjablonen weergeven en bewerken

Een aanvullingssjabloon is een set regels die bepalen wanneer en hoe een locatie wordt aangevuld. U selecteert een sjabloon om te bepalen wanneer en hoe aanvulling wordt uitgevoerd. Om uw aanvullingssjablonen weer te geven en te bewerken gaat u naar **Magazijnbeheer \> Instellingen \> Aanvulling \> Aanvullingssjablonen**.

#### <a name="prepare-a-demo-data-replenishment-template"></a>Een aanvullingssjabloon met demogegevens voorbereiden

In dit voorbeeld wordt getoond hoe u een aanvullingssjabloon voorbereidt. Als u het scenario aan het einde van dit onderwerp wilt doorlopen, gebruikt u de voorbeeldgegevenswaarden die hier worden getoond. Gebruik anders uw eigen waarden.

1. Selecteer de rechtspersoon **USMF** om te werken met de demogegevens.
1. Ga naar **Magazijnbeheer \> Instellen \> Aanvulling \> Aanvullingssjablonen**.
1. Selecteer de optie **Bewerken** om de pagina in de bewerkingsmodus te openen.
1. Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster **Overzicht**.
1. Stel in de nieuwe rij de volgende waarden in. Accepteer de standaardwaarden voor alle overige velden.

    - **Aanvullingssjabloon:** _Zone min/max-aanv_
    - **Beschrijving:** _Zone min/max-aanvulling_
    - **Aanvullingstype:** _Minimum of maximum_

1. Selecteer **Opslaan**.
1. Terwijl de nieuwe rij nog steeds is geselecteerd in het raster **Overzicht**, selecteert u **Nieuw** boven het raster **Details van aanvullingssjabloon** om een rij toe te voegen die is gekoppeld aan de aanvullingssjabloon *Zone min/max-aanv* die u zojuist hebt gemaakt.
1. Stel in de nieuwe rij de volgende waarden in:

    - **Volgnummer:** Voer _1_ in.
    - **Beschrijving:** Voer _Aanvulling orderverzamelzone_ in.
    - **Aanvullingseenheid:** Selecteer _ea_.
    - **Aanvraagtype:** Laat dit veld leeg.
    - **Instructiecode:** Met dit veld word de aanvullingssjabloon gekoppeld aan een locatie-instructie. Selecteer de instructiecode voor de demogegevens die u eerder hebt gemaakt (_Zoneaanvulling_).
    - **Werksjabloon**: Laat dit veld leeg.
    - **Minimumhoeveelheid:** In dit veld stelt u de hoeveelheid in waarbij de aanvulling wordt getriggered. Voer _50_ in.
    - **Maximumaantal:** Met dit veld kunt u de maximumhoeveelheid van een artikel instellen die in een zone aanwezig kan zijn. Door het gegenereerde aanvullingswerk wordt de voorraad vergroot tot deze hoeveelheid. Voer _150_ in.
    - **Eenheid:** In dit veld wordt de eenheid voor de minimum- en maximumwaarden ingesteld. Selecteer _ea_.
    - **Vraagverhoging:** Selecteer _Afronden naar boven_.
    - **Lege vaste locaties aanvullen:** Schakel dit selectievakje in.
    - **Alleen vaste locaties aanvullen:** Schakel dit selectievakje uit.
    - **Productquerymodus:** Selecteer _Productquery_.
    - **Bereik aanvullingsdrempel:** Dit veld bepaalt of de sjabloon moet worden geëvalueerd per zone of op een specifieke locatie. Selecteer _Zone_.
    - **Magazijn:** Selecteer _61_.

1. Selecteer **Producten selecteren** boven het raster **Details aanvullingssjabloon**.
1. Selecteer in het dialoogvenster **Productquery** op het tabblad **Bereik** de optie **Toevoegen** om een rij aan het raster toe te voegen.
1. Stel in de nieuwe rij de volgende waarden in:

    - **Tabel:** _Artikelen_
    - **Afgeleide tabel:** _Artikelen_
    - **Veld:** _Artikelnummer_
    - **Criteria:** _A0001_

1. Selecteer **OK** om de query op te slaan en het dialoogvenster te sluiten.
1. Selecteer **Zones selecteren voor aanvulling** boven het raster **Details aanvullingssjabloon**.
1. Voeg in het dialoogvenster **Zonequery** op het tabblad **Bereik** een regel aan het raster toe.
1. Stel in de nieuwe rij de volgende waarden in:

    - **Tabel:** _Magazijnzone_
    - **Afgeleide tabel:** _Magazijnzone_
    - **Veld:** _Zone-id_
    - **Criteria:** _VERDIEPING_

1. Selecteer **OK** om de query op te slaan en het dialoogvenster te sluiten.

### <a name="set-up-location-directives"></a>Locatie-instructies instellen

Anders dan bij min/max-aanvulling op basis van op een locatie, vereist op zone gebaseerde min/max-aanvulling dat u beide locatie-instructies voor orderverzamelen en wegzetten configureert, omdat het systeem voor uitgaand werk de gehele zone evalueert, in plaats van alleen de orderverzamellocatie.

#### <a name="view-and-edit-location-directives"></a>Locatie-instructies weergeven en bewerken

Om de locatie-instructies weer te geven of te bewerken, gaat u naar **Magazijnbeheer \> Instellingen \> Locatie-instructies**.

In de volgende sectie vindt u voorbeelden waarin wordt uitgelegd hoe u met de instellingen de vereiste locatie-instructies voor orderverzamelen en wegzetten kunt maken.

#### <a name="prepare-demo-data-location-directives"></a>Locatie-instructies voor demogegevens voorbereiden

Om demogegevens voor te bereiden zodat deze in het scenario aan het einde van dit onderwerp kunnen worden gebruikt, moet u twee locatie-instructies maken: een voor de orderverzamelen en een voor wegzetten.

##### <a name="create-a-replenishment-pick-directive"></a>Een instructie voor aanvullingsverzamelen maken

1. Selecteer de rechtspersoon **USMF** om te werken met de demogegevens.
1. Ga naar **Magazijnbeheer \> Instellen \> Locatierichtlijnen**.
1. Stel in het linkerdeelvenster het veld **Werkordertype** in op _Aanvullen_.
1. Selecteer in het actievenster **Nieuw** om een nieuwe instructie te maken.
1. Stel de volgende waarden in:

    - **Volgnummer:** Accepteer de standaard waarde.
    - **Naam:** Voer _Zone verzamelen_ in.
    - **Werktype:** Selecteer _Orderverzamelen_.
    - **Locatie:** Selecteer _6_.
    - **Magazijn:** Selecteer _61_.
    - **Instructiecode:** Laat dit veld leeg.
    - **Meerdere SKU's:** Stel deze optie in op _Nee_.

1. Selecteer **Opslaan** om een instructie te maken met de instellingen die u tot op dit punt hebt geconfigureerd.
1. Ga naar het sneltabblad **Regels** en selecteer **Nieuw** om een regel toe te voegen aan het raster.
1. Stel op de nieuwe regel de volgende waarden in:

    - **Volgnummer:** Voer _1_ in.
    - **Vanaf hoeveelheid:** Voer _0_ in.
    - **Tot hoeveelheid:** Voer _10000000_ in.
    - **Eenheid:** Laat dit veld leeg.
    - **Hoeveelheid zoeken:** Selecteer _Geen_.
    - **Beperken op eenheid:** Schakel dit selectievakje uit.
    - **Afronden naar eenheid:** Schakel dit selectievakje uit.
    - **Verpakkingshoeveelheid zoeken:** Schakel dit selectievakje uit.
    - **Splitsen toestaan:** Schakel dit selectievakje in.

1. Selecteer **Opslaan** om de nieuwe regel op te slaan.
1. Terwijl de nieuwe regel nog steeds is geselecteerd in het raster **Regels**, selecteert u **Nieuw** op het sneltabblad **Locatie-instructieacties** om een rij toe te voegen aan het raster.
1. Stel in de nieuwe rij de volgende waarden in:

    - **Volgnummer:** Voer _1_ in.
    - **Naam:** Kies _Verzamelen uit bulk_.
    - **Gebruik vaste locaties:** Selecteer _Vaste en niet-vaste locaties_.
    - **Negatieve voorraad toestaan**: Schakel dit selectievakje uit.
    - **Batch ingeschakeld**: Schakel dit selectie vakje uit.
    - **Strategie:** Selecteer _Geen_.

1. Selecteer **Opslaan** om de nieuwe actie op te slaan.
1. Terwijl uw nieuwe actie nog steeds is geselecteerd, selecteert u **Query bewerken** boven het raster **Locatie-instructieacties**.
1. Een querydialoogvenster wordt geopend, waarin u de locaties kunt selecteren van waaruit u wilt aanvullen. Selecteer op het tabblad **Bereik** de optie **Toevoegen** om een regel toe te voegen aan het raster.
1. Stel in de nieuwe rij de volgende waarden in:

    - **Tabel:** _Locaties_
    - **Afgeleide tabel:** _Locaties_
    - **Veld:** _Zone-id_
    - **Criteria:** _BULK_

1. Selecteer **OK** om de query op te slaan en het dialoogvenster te sluiten.
1. Selecteer **Opslaan** om de locatie-instructie op te slaan.

##### <a name="create-a-replenishment-put-directive"></a>Een instructie voor aanvullingswegzetten maken

1. Controleer op de pagina **Locatie-instructies** in het linkerdeelvenster of het veld **Werkordertype** nog is ingesteld op _Aanvulling_.
1. Selecteer in het actievenster **Nieuw** om nog een nieuwe instructie te maken.
1. Stel de volgende waarden in:

    - **Volgnummer:** Accepteer de standaard waarde.
    - **Naam:** Voer _Zone wegzetten_ in.
    - **Werkordertype:** Selecteer _Wegzetten_.
    - **Locatie:** Selecteer _6_.
    - **Magazijn:** Selecteer _61_.
    - **Instructiecode:** Selecteer _Zoneaanvulling_ om deze locatie-instructie te koppelen aan de aanvullingssjabloon die u eerder hebt gemaakt met behulp van de code die u eerder hebt gemaakt.
    - **Meerdere SKU's:** Stel deze optie in op _Nee_.

1. Selecteer **Opslaan** om een instructie te maken met de instellingen die u tot op dit punt hebt geconfigureerd.
1. Ga naar het sneltabblad **Regels** en selecteer **Nieuw** om een regel toe te voegen aan het raster.
1. Stel op de nieuwe regel de volgende waarden in:

    - **Volgnummer:** Voer _1_ in.
    - **Vanaf hoeveelheid:** Voer _0_ in.
    - **Tot hoeveelheid:** Voer _10000000_ in.
    - **Eenheid:** Laat dit veld leeg.
    - **Hoeveelheid zoeken:** Selecteer _Geen_.
    - **Beperken op eenheid:** Schakel dit selectievakje uit.
    - **Afronden naar eenheid:** Schakel dit selectievakje uit.
    - **Verpakkingshoeveelheid zoeken:** Schakel dit selectievakje uit.
    - **Splitsen toestaan:** Schakel dit selectievakje in.

1. Selecteer **Opslaan** om de nieuwe regel op te slaan.
1. Terwijl de nieuwe regel nog steeds is geselecteerd in het raster **Regels**, selecteert u **Nieuw** op het sneltabblad **Locatie-instructieacties** om een rij toe te voegen aan het raster.
1. Stel in de nieuwe rij de volgende waarden in:

    - **Volgnummer:** Voer _1_ in.
    - **Naam:** Voer _Zone wegzetten_ in.
    - **Gebruik vaste locaties:** Selecteer _Vaste en niet-vaste locaties_.
    - **Negatieve voorraad toestaan**: Schakel dit selectievakje uit.
    - **Batch ingeschakeld**: Schakel dit selectie vakje uit.
    - **Strategie:** Selecteer _Consolideren_.

1. Selecteer **Opslaan** om de nieuwe actie op te slaan.
1. Terwijl uw nieuwe actie nog steeds is geselecteerd, selecteert u **Query bewerken** boven het raster **Locatie-instructieacties**.
1. Een querydialoogvenster wordt geopend, waarin u de zone kunt selecteren waarnaar u wilt aanvullen. Deze zone moet dezelfde zone zijn die is opgegeven in de aanvullingssjabloon. Selecteer op het tabblad **Bereik** de optie **Toevoegen** om een regel toe te voegen aan het raster.
1. Stel in de nieuwe rij de volgende waarden in:

    - **Tabel:** _Locaties_
    - **Afgeleide tabel:** _Locaties_
    - **Veld:** _Zone-id_
    - **Criteria:** _VERDIEPING_

1. Selecteer **OK** om de query op te slaan en het dialoogvenster te sluiten.
1. Selecteer **Opslaan** om de locatie-instructie op te slaan.

## <a name="scenario"></a>Scenario's

In deze sectie wordt een voorbeeldscenario besproken waarin u kunt zien hoe u met de functie kunt werken.

### <a name="prepare-the-sample-data-that-is-required-for-the-sample-scenario"></a>De voorbeeldgegevens voorbereiden die zijn vereist voor het voorbeeldscenario

Voordat u het scenario gaat doorlopen, moet u voorbeeld gegevens activeren en de functie configureren, zoals beschreven in deze en de vorige sectie in dit onderwerp.

#### <a name="use-the-usmf-legal-entity"></a>De rechtspersoon USMF gebruiken

Als u het scenario wilt doorlopen met de hier opgegeven voorbeeldrecords en -waarden, moet u een systeem gebruiken waarop de standaard [demogegevens](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) zijn geïnstalleerd. U moet daarnaast ook de rechtspersoon **USMF** selecteren voordat u begint.

#### <a name="prepare-additional-sample-data"></a>Extra voorbeeldgegevens voorbereiden

Selecteer eerst de rechtspersoon **USMF** en voeg de benodigde aanvullende voorbeeldgegevens toe, zoals beschreven in de sectie [Op zone gebaseerde aanvulling instellen](#setup) eerder in dit onderwerp.

#### <a name="check-your-on-hand-inventory"></a>Controleer de voorhanden voorraad

Voer de volgende stappen uit om te controleren of uw systeem voldoende voorraad bevat om het voorbeeldscenario te ondersteunen.

1. Zorg ervoor dat er voorhanden voorraad is voor artikel *A0001* op twee verschillende locaties in de orderverzamelzone (*VERDIEPING*) die is opgegeven in de aanvullingssjabloon. De totale voorraad moet echter kleiner zijn dan de vereiste minimumhoeveelheid (*50*) die is opgegeven in de aanvullingssjabloon. Op deze manier kunt u simuleren hoe de berekening wordt uitgevoerd voor de gehele zone in plaats van alleen voor één locatie. **U kunt alle relevante magazijnprocessen gebruiken om waar nodig de voorraad aan te passen.**
1. Zorg ervoor dat er voldoende voorraad is voor artikel *A0001* op een bulk locatie die is opgegeven in de locatie-instructie Zone orderverzamelen, waar het aanvullingswerk de artikelen uit zone-id *BULK* moet verzamelen. De totale voorraad moet groter zijn dan de vereiste maximumhoeveelheid (*150*) die is opgegeven in de aanvullingssjabloon.
1. Optioneel maar aanbevolen: Voer de volgende stappen uit om een voorraadcorrectiejournaal te maken:

    1. Ga naar **Voorraadbeheer \> Journaalboekingen \> Artikelen \> Voorraadcorrectie**.
    1. Selecteer **Nieuw**.
    1. Selecteer in het dialoogvenster **Voorraadjournaal maken** in het veld **Magazijn** de waarde *61*.
    1. Selecteer **OK**.
    1. Gebruik op het sneltabblad **Journaalregels** de knop **Nieuw** om drie regels aan het raster toe te voegen en stel de volgende waarden in. Nadat u alle regels hebt ingesteld, selecteert u **Opslaan**.

        - **Regel 1:**

            - **Artikelnummer:** *A0001*
            - **Locatie:** *6*
            - **Magazijn:** *61*
            - **Locatie:** *02A01R1S1B*
            - **Nummerplaat:** Selecteer een bestaande nummerplaat in de lijst of maak een nieuwe nummerplaat.
            - **Hoeveelheid:** *1000*

        - **Regel 2:**

            - **Artikelnummer:** *A0001*
            - **Locatie:** *6*
            - **Magazijn:** *61*
            - **Locatie:** *07A01R2S1B*
            - **Nummerplaat:** Selecteer een bestaande nummerplaat in de lijst of maak een nieuwe nummerplaat.
            - **Hoeveelheid:** *15*

        - **Regel 3:**

            - **Artikelnummer:** *A0001*
            - **Locatie:** *6*
            - **Magazijn:** *61*
            - **Locatie:** *07A01R1S1B*
            - **Nummerplaat:** Selecteer een bestaande nummerplaat in de lijst of maak een nieuwe nummerplaat.
            - **Hoeveelheid:** *10*

    1. Selecteer in het actievenster de optie **Valideren**. Verhelp eventuele fouten die worden gevonden voordat u doorgaat naar de volgende stap.
    1. Selecteer in het actievenster de optie **Boeken** om de voorraad naar het magazijn te boeken.

### <a name="sample-scenario-run-zone-based-minmax-replenishment"></a>Voorbeeldscenario: Op zones gebaseerde min/max-aanvulling uitvoeren

Nadat alle vereiste voorbeeldgegevens zijn ingevoerd, kunt u aanvulling activeren door de volgende stappen uit te voeren.

1. Ga naar **Magazijnbeheer \> Aanvulling \> Aanvullingen**.
1. Selecteer in het dialoogvenster **Aanvulling** op het sneltabblad **Op te nemen records** de optie **Filteren**.
1. Bewerk in het dialgoogvenster **Query** op het tabblad **Bereik** de standaardtabelrij op de volgende manier:

    - **Tabel:** Selecteer _Aanvullingssjablonen_.
    - **Afgeleide tabel:** Selecteer _Aanvullingssjablonen_.
    - **Veld:** Selecteer _Aanvullingssjabloon_.
    - **Criteria:** Selecteer _Zone min/max-aanv_. Deze aanvullingssjabloon is de aanvullingssjabloon die u hebt gemaakt toen u de demogegevens voor dit scenario voorbereidde.

1. Selecteer **OK** om de query op te slaan en terug te gaan naar het dialoogvenster **Aanvulling**.
1. Selecteer **OK** om de aanvullingssjabloon uit te voeren.

Er wordt nu aanvullingswerk gemaakt om de voorraad uit de zone *BULK* te verzamelen en deze aan te vullen naar de zone *VERDIEPING*.

## <a name="notes-and-tips"></a>Opmerkingen en tips

Hier volgen enkele opmerkingen en tips voor het werken met de functie:

- Als u aanvullingswerk wilt instellen dat naar de gewenste zone gaat, kunt u de regels van de aanvullingssjabloon en de locatie-instructies koppelen op een van de volgende manieren:

    - Bewerk de query voor de locatie-instructiekoptekst en filter de geselecteerde regels van de aanvullingssjabloon.
    - Gebruik een instructiecode op de aanvullingssjabloonregel en laat deze overeenkomen met de locatie-instructie voor wegzetten.

- Als u dynamische locaties gebruikt, wordt aanvullingswerk gemaakt voor de eerste beschikbare locatie of voor een locatie die al voorraad bevat, als de locatie-instructieactie is ingesteld op het gebruik van de strategie **Consolideren**.
- Als u vaste locaties gebruikt in plaats van zones, moet u [standaard min/max-aanvulling gebruiken](tasks/set-up-min-max-replenishment-process.md).
