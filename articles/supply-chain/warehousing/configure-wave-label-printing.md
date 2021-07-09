---
title: Wavelabels afdrukken
description: In dit onderwerp wordt beschreven hoe u wavelabels afdrukt en hoe u dit kunt instellen.
author: perlynne
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSDocumentRouting, WHSWaveTableListPage, WHSPostMethod, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelType, WHSWaveLabelTemplateGroup, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: yyyy-mm-dd
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 6360f36b6a3526cdc5680a4059ae1202896986a5
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301766"
---
# <a name="wave-label-printing"></a>Wavelabels afdrukken

[!include [banner](../includes/banner.md)]

Het afdrukken van wavelabels is een alternatieve manier om labels af te drukken door de introductie van een nieuwe wavestapmethode waarmee u labels rechtstreeks vanuit de wavesjabloon kunt maken en afdrukken tijdens het uitvoeren van de wave. Daarom zijn de labels al beschikbaar voordat de werknemers de werkorder op een mobiel apparaat uitvoeren. Werknemers kunnen de vereiste labels tijdens het orderverzamelen koppelen in plaats van na het orderverzamelen.

Bij het afdrukken van wavelabels wordt de Zebra Programming Language (ZPL) gebruikt om labelindelingen te maken. Een labelindeling is onderverdeeld in drie secties (koptekst, hoofdtekst en voettekst) om labels met een herhalende structuur toe te staan. Met wavelabelsjablonen wordt aangegeven welke labelindeling moet worden gebruikt. Gebruikers kunnen opgeven welke printer wordt gebruikt. Ze kunnen ook labels op meerdere printers tegelijk afdrukken, als dat nodig is. Op de pagina **Historie van wavelabels** ziet u een overzicht van alle labels die met deze instellingen zijn gemaakt.

U kunt labels afdrukken en sorteren op basis van werkkopteksten, u kunt onderbrekingsetiketten afdrukken per werkkoptekst en u kunt labels voor containerinhoud, kisten en andere vergelijkbare labels afdrukken.

> [!NOTE]
> Deze functie vervangt niet de bestaande afdrukfuncties voor labels die zijn gebaseerd op documentroutering.

Bij het afdrukken van wavelabels kunt u de volgende uitbreidingen kiezen:

- Labels afdrukken op basis van het aantal dozen op één werklijn, zonder gebruik te maken van containers. (Een "doos" is een eenheid die is opgegeven op de regels van de eenheidsvolgordegroep.)
- Druk verschillende labelreeksen af (bijvoorbeeld labels voor dozen en pallets).
- Neem labelopsomming op (bijvoorbeeld 1/124, 2/124,... 124/124) en definieer het opsommingsbereik (bijvoorbeeld werkregel, laadregel of verzending).
- Maak een vrachtbrief-id en druk deze af op labels voordat de vrachtbrief wordt gegenereerd.
- Maak voor elke doos een unieke Serial Shipping Container Code (SSCC) en voeg deze op elk label toe.
- Maak GS1-compatibele nummerreeksen voor vrachtbrief-Id's en SSCC's.
- Druk labels opnieuw af vanaf mobiele apparaten of rich clients.
- Maak labels ongeldig (bijvoorbeeld in korte orderverzamelscenario's) en druk ze opnieuw af.
- Schoon de wavelbelhistorie op.
- Verbeteringen in indelingen voor documentroutering worden gedeeld tussen documentrouteringsindelingen en wavelabelindelingen. (Zie voor meer informatie [Documentrouteringsindeling voor nummerplaten](../warehousing/document-routing-layout-for-license-plates.md).)

Deze uitbreidingen maken het efficiënter om dozen te labelen voor palletisering. Dit is met name handig voor bedrijven die naar grote winkels verzenden waar ontvangstbewijzen van orders automatisch worden bevestigd door het scannen van elke doos afzonderlijk.

> [!NOTE]
> U kunt de configuratiescenario's die in dit onderwerp worden beschreven, afzonderlijk of in combinatie implementeren, afhankelijk van uw zakelijke vereisten. U kunt verschillende wavelabelsjablonen ontwerpen die in de juiste volgorde worden uitgevoerd (zoals aangegeven in scenario 3). U kunt bijvoorbeeld scenario 1 gebruiken om labels voor dozen af te drukken en scenario 2 om palletlabels af te drukken (als de grootte en samenstelling van pallets verschillen).

## <a name="turn-on-the-wave-label-printing-feature"></a>De functie Wavelabels afdrukken inschakelen

Voordat u de functie *Wavelabels afdrukken* kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen het werkgebied [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de status van de functie te controleren en desgewenst in te schakelen. De functie wordt daar op de volgende manier weergegeven:

- **Module:** *Magazijnbeheer*
- **Functienaam:** *Wavelabels afdrukken*

## <a name="scenario-1-wave-label-printing-where-a-single-wave-label-is-generated"></a>Scenario 1: Wavelabels afdrukken waarbij één wavelabel wordt gegenereerd

Dit scenario laat zien hoe een bedrijf verzendlabels afdrukt voor een grote detailhandelaar die ontvangstbewijzen automatisch bevestigt door elke doos afzonderlijk te scannen.

Dit scenario toont de volledige stroom.

### <a name="make-demo-data-available"></a>Demogegevens beschikbaar maken

Voor dit scenario moeten demogegevens zijn geïnstalleerd en moet u de rechtspersoon **USMF** selecteren.

### <a name="make-sure-that-the-wave-label-method-is-available"></a>Controleer of de wavelabelmethode beschikbaar is

Mogelijk moet u de waveverwerkingsmethoden opnieuw genereren om de methode voor het afdrukken van wavelabels beschikbaar te maken.

1. Ga naar **Magazijnbeheer \> Instellen \> Waves \> Methoden voor verwerking van waves**.
1. Controleer of **waveLabelPrinting** in de lijst staat. Als dat niet zo is, selecteert u **Methoden opnieuw genereren** in het actievenster om deze toe te voegen.

### <a name="configure-a-wave-template"></a>Een wavesjabloon configureren

Met wavesjablonen kunt u specifieke exemplaren van wavemethoden koppelen aan een corresponderende wavelabelsjabloon.

1. Ga naar **Magazijnbeheer \> Instellen \> Waves \> Wavesjablonen**.
1. Selecteer een sjabloon zoals **62 Standaardverzending**.
1. Verplaats op het sneltabblad **Methoden** de methode **Wavelabels afdrukken** naar de kolom **Geselecteerde methoden**.
1. Selecteer in de kolom **Geselecteerde methoden** de methode **Wavelabels afdrukken** en stel het veld **Wavestapcode** in op *PrintLabel*. Zie [Wavestapcodes](wave-step-codes.md) voor meer informatie.

### <a name="create-a-wave-label-layout"></a>Een wavelabelindeling maken

De labelindeling bepaalt welke informatie op het label wordt afgedrukt en hoe deze wordt ingedeeld. Hier voert u de ZPL-code in die naar de printer wordt verzonden.

1. Ga naar **Magazijnbeheer \> Instellingen \> Documentroutering \> Wavelabelindelingen**.
1. Maak een record met de volgende instellingen:

    - **Labelindeling-id:** *Doos*
    - **Omschrijving:** *doos (SSCC)*

1. Selecteer **Opslaan** in het actievenster.
1. Selecteer in het actievenster **Instellingen voor wavelabelrijen**.

    De pagina **Instellingen voor wavelabelrijen** wordt weergegeven. Hier kunt u het dynamische deel van het label configureren.

1. Voeg een rij toe met de volgende instellingen:

    - **Rij-id:** *WaveLabel*
    - **Naam van tabelrij:** *WHSWaveLabel*
    - **Beginpositie rij:** *0*

        Dit veld bepaalt de verticale positie waar de rij begint op het label.

    - **Rijhoogte:** *0*

        Dit veld definieert de hoogte van elke rij (in punten) volgens de ZPL-standaard. De rijhoogte is positief voor horizontale labels en negatief voor verticale labels. Omdat dit voorbeeld slechts één rij bevat, kunt u de waarde instellen op *0* (nul).

    - **Rijen per pagina:** *1*

        Dit veld bepaalt het aantal rijen dat op elk label kan worden afgedrukt.

        > [!NOTE]
        > Deze instelling zorgt ervoor dat een afzonderlijk ZPL-label wordt afgedrukt voor elke record in de tabel met wavelabels.

1. Sluit de pagina.
1. Selecteer **Query bewerken** in het actievenster.
1. Voeg in het dialoogvenster Query-editor op het tabblad **Bereik** een rij toe met de volgende instellingen:

    - **Tabel:** *Werkregels*
    - **Afgeleide tabel:** *Werkregels*
    - **Veld:** *Werktype*
    - **Criteria:** *Orderverzamelen*

    Met deze query zorgt u ervoor dat alleen werkregels van het orderverzameltype worden afgedrukt op het label, niet de werkregels van het wegzettype.

1. Als u de vrachtbrief-id wilt kunnen afdrukken, selecteert u op het tabblad **Joins** de tabel **Werkregels** en voegt u de tabel **Zendingen** eraan toe.
1. Sluit het dialoogvenster Query-editor.
1. Het sneltabblad **Printertekstindeling** bevat drie secties waarin u printercode kunt schrijven: **koptekstsectie**, **hoofdsectie** en **voettekstsectie**. Voer in de **Koptekstsectie** in het veld **Labelkoptekst** de code in voor de vereiste koptekst. Als u bijvoorbeeld Zebra-printers gebruikt, kunt u de volgende code gebruiken.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. Voer in de **Hoofdsectie** in het veld **Labelhoofdtekst** ZPL-code in voor de vereiste hoofdtekst. Hier volgt een voorbeeld.

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. Voer in de **Hoofdsectie** in het veld **Labelvoettekst** ZPL-code in voor de vereiste voettekst. Hier volgt een voorbeeld.

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Er wordt één exemplaar van elk label afgedrukt. Als u meer exemplaren nodig hebt (bijvoorbeeld één exemplaar voor elke zijde van de pallet), stelt u de waarde **n** voor de sectie **\^PQn** in de voettekst in op het vereiste aantal exemplaren. Als u bijvoorbeeld vier kopieën van elk label wilt afdrukken, geeft u **\^PQ4** op.

Uw label is nu klaar voor gebruik.

### <a name="create-a-wave-label-type"></a>Een wavelabeltype maken

Wavelabeltypen worden gebruikt om wavelabelsjablonen te koppelen aan een eenheid op de volgordegroepsregels van de eenheid.

1. Ga naar **Magazijnbeheer \> Instellingen \> Documentroutering \> Wavelabeltypen**.
1. Voeg een wavelabeltype met de volgende instellingen toe:

    - **Labeltype:** *Doos*
    - **Omschrijving:** *Doos*

### <a name="set-up-unit-sequence-groups"></a>Eenheidvolgordegroepen instellen

Stel vervolgens de eenheidsvolgordegroep in voor het wavelabeltype.

1. Ga naar **Magazijnbeheer \> Instellingen \> Magazijn \> Volgordegroepen eenheid**.
1. Selecteer de groep **Ea Box PL**.
1. Stel voor de regel **Doos** het veld **Waveniveautype** in op *Doos*.

### <a name="create-a-wave-label-template"></a>Een wavelabelsjabloon maken

Maak vervolgens de wavelabelsjabloon voor het wavelabeltype.

1. Ga naar **Magazijnbeheer \> Instellingen \> Documentroutering \> Wavelabelsjablonen**.
1. Voeg een waveniveausjabloon toe en stel de volgende waarden in de koptekst in:

    - **Naam van labelsjabloon:** *Dooslabels*
    - **Omschrijving:** *Dooslabels*
    - **Wavestapcode:** *PrintLabel*
    - **Magazijn:** *62*

1. Stel op het sneltabblad **Algemeen** het veld **Wavelabeltype** in op *Doos*.
1. Voeg op het sneltabblad **Sjabloondetails van wavelabels** een nieuwe rij toe met de volgende instellingen:

    - **Labelindeling-id:** *Doos*
    - **Printernaam:** selecteer een geschikte ZPL-printer.
    - **Query uitvoeren:** *Ja* (deze instelling is optioneel, maar wordt wel aanbevolen voor optimale prestaties.)

1. Selecteer **Opslaan** in het actievenster.
1. Optioneel: als u een klantspecifiek labelontwerp instelt, moet u een query maken om het klantaccount te zoeken. Ga naar het sneltabblad **Sjabloondetails van wavelabels** en selecteer **Query bewerken**. Voeg vervolgens in het dialoogvenster Query-editor op het tabblad **Bereik** een rij toe met de volgende instellingen:

    - **Tabel:** *Zendingen*
    - **Afgeleide tabel:** *Zendingen*
    - **Veld:** *Accountnummer*
    - **Criteria:** Voer het betreffende accountnummer van de klant in.

    Wanneer u klaar bent, selecteert u **OK** om het dialoogvenster Query-editor te sluiten.

1. Selecteer in het actievenster de optie **Query bewerken** om het dialoogvenster Query-editor te openen voor de hele labelsjabloon.
1. Voeg in het dialoogvenster Query-editor op het tabblad **Sortering** een rij toe met de volgende instellingen:

    - **Tabel:** *Werkregels*
    - **Afgeleide tabel:** *Werkregels*
    - **Veld:** *Verwijzing ladingsregel-id (record-id)*
    - **Zoekrichting:** *Oplopend*

1. Selecteer **OK** om het dialoogvenster Query-editor te sluiten.
1. U wordt gevraagd om de bewerking voor het opnieuw instellen van de groepering te bevestigen. Selecteer **Ja** om door te gaan.
1. Selecteer in het actievenster **Sjabloongroep voor wavelabel**.
1. Selecteer in het dialoogvenster **Sjabloongroep voor wavelabel** de rij waar het veld **Verwijzing veldnaam** is ingesteld op *Verwijzing ladingsregel-id* en schakel vervolgens het selectievakje **Labelbuild-id** in voor deze rij.

    > [!NOTE]
    > Met deze instelling wordt één labelreeks ("doos 1 van X") per ladingsregel gemaakt in de hele wave, ongeacht de instelling van de werkgroepering. Deze labelreeks kan worden afgedrukt op de labelindeling.

### <a name="configure-number-sequence-extensions"></a>Nummerreeksuitbreidingen configureren

Nummerreeksuitbreidingen bepalen de GS1-naleving van specifieke nummerreeksen. Deze configuratie is optioneel voor het huidige scenario. Zie [Nummerreeksuitbreidingen configureren](../warehousing/configure-number-sequence-extensions.md) voor meer informatie en configuratie-instructies.

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Een verkooporder maken en vrijgeven naar het magazijn

1. Ga naar **Verkoop en marketing \> Verkooporder \> Alle verkooporders**.
1. Maak een verkooporder met de volgende instellingen:

    - **Klantrekening:** *US-001*
    - **Magazijn:** *62*

1. Voeg twee verkooporderregels toe met de volgende instellingen:

    - Verkooporderregel 1:

        - **Artikelnummer:** *A0001*
        - **Hoeveelheid:** *9024*
        - **Eenheid:** *ea* (9024 ea = 376 dozen = 47 PL)

    - Verkooporderregel 2:

        - **Artikelnummer:** *A0002*
        - **Hoeveelheid:** *9016*
        - **Eenheid:** *ea* (9016 ea = 322 dozen = 46 PL)

    > [!NOTE]
    > De artikelen en hoeveelheden die hier worden vermeld, dienen alleen als voorbeeld. Ze moeten de volgordegroep van de eenheid gebruiken die u eerder hebt gedefinieerd. Er moeten correcte eenheidsomrekeningen van *ea* naar *doos* naar *PL* zijn gedefinieerd en ze moeten op voorraad zijn in magazijn *62*. Zie [Maateenheid en voorraadbeleid](unit-measure-stocking-policies.md) voor meer informatie.

1. Selecteer verkooporderregel 1. Selecteer in de sectie **Verkooporderregel** in het menu **Voorraad** de optie **Reservering**.
1. Ga naar de pagina **Reservering** en selecteer in het actievenster de optie **Partij reserveren** en sluit de pagina vervolgens.
1. Herhaal stap 4 en 5 voor verkooporderregel 2.
1. Selecteer in het actievenster op het tabblad **Magazijn** de optie **Vrijgeven naar magazijn**.

    De volgende gebeurtenissen vinden plaats:

    - Het systeem verwerkt de gemaakte zending met behulp van de sjabloon die de stap voor het afdrukken van labels bevat. De labelindeling wordt gebruikt om de indeling van het label te definiëren en het resultaat is een label dat wordt afgedrukt op de printer die is geselecteerd in de labelsjabloon.
    - Er worden wavelabels gegenereerd en afgedrukt. Het aantal labels komt overeen met het aantal dozen (in dit voorbeeld 376 labels voor regel 1 en 322 labels voor regel 2).
    - Er wordt een nieuwe vrachtbrief-id gegenereerd voor de zendingen. Als u de nummerreeksuitbreidingen hebt geconfigureerd, volgen de wavelabel-id's de nummernotatie **SSCC-18**. 

U kunt wavelabels weergeven en opnieuw afdrukken op de volgende pagina's. Selecteer in het actievenster van elke pagina op het tabblad **Zendingen** in de groep **Verwante informatie** de optie **Wavelabels**.

- Alle zendingen \> Details van zending
- Alle ladingen \> Details van lading
- Alle waves
- Wavelabels
- Historie wavelabel

## <a name="scenario-2-wave-label-printing-for-containerization-without-wave-label-records"></a>Scenario 2: Wavelabels afdrukken voor containers (zonder wavelabelrecords)

Met dit scenario kunt u wavelabels wanneer u containers gebruikt om artikelen automatisch in dozen te splitsen, zodat u geen wavelabelrecord hoeft te gebruiken. In dit geval fungeert de container-id als tijdelijke aanduiding voor de SSCC.

Dit zijn de belangrijkste verschillen tussen dit scenario en scenario 1:

- **Sjablonen voor wavelabels:** u selecteert geen wavelabeltype in de sjabloon voor wavelabels en u hebt geen labelbuildgroepering nodig. Anders configureert u de wavelabelsjabloon en gaat u op dezelfde manier naar de wavesjabloon als in scenario 1 wordt beschreven. U moet het naar de wavelabeltype leeg laten om te voorkomen dat er wavelabels worden gegenereerd.
- **Indeling van wavelabels:** u configureert de instellingen voor de rij met de wavelabelindeling voor werkregels in plaats van wavelabelrecords. U moet de rij-instelling voor de labelindeling configureren met de tabel **WHSWorkLine** in plaats van de tabel **WHSWaveLabel**. De instelling **Rijen per pagina** bepaalt het aantal rijen dat de hoofdsectie zal hebben. 

Deze configuratie is ook geschikt voor zakelijke scenario's waarbij meerdere verschillende artikelen in één gelabelde door of pallet worden verpakt. Dit verpakkingsproces kan worden gedefinieerd door het maken van werk (bijvoorbeeld werk dat is gegroepeerd op zending).

Dit scenario toont de volledige stroom.

### <a name="make-demo-data-available"></a>Demogegevens beschikbaar maken

Voor dit scenario moeten demogegevens zijn geïnstalleerd en moet u de rechtspersoon **USMF** selecteren.

### <a name="make-sure-that-the-wave-label-method-is-available"></a>Controleer of de wavelabelmethode beschikbaar is

Mogelijk moet u de waveverwerkingsmethoden opnieuw genereren om de methode voor het afdrukken van wavelabels beschikbaar te maken.

1. Ga naar **Magazijnbeheer \> Instellen \> Waves \> Methoden voor verwerking van waves**.
1. Controleer of **waveLabelPrinting** in de lijst staat. Als dat niet zo is, selecteert u **Methoden opnieuw genereren** in het actievenster om deze toe te voegen.

### <a name="set-up-a-wave-template"></a>Een wavesjabloon instellen

Met wavesjablonen kunt u specifieke exemplaren van wavemethoden koppelen aan een corresponderende wavelabelsjabloon.

1. Ga naar **Magazijnbeheer \> Instellen \> Waves \> Wavesjablonen**.
1. Selecteer een sjabloon zoals **63 Containervorming**.
1. Verplaats op het sneltabblad **Methoden** de methode **Wavelabels afdrukken** naar de kolom **Geselecteerde methoden**.
1. Selecteer in de kolom **Geselecteerde methoden** de methode **Wavelabels afdrukken** en stel het veld **Wavestapcode** in op *PrintLabel*. Zie [Wavestapcodes](wave-step-codes.md) voor meer informatie.

### <a name="create-a-wave-label-layout"></a>Een wavelabelindeling maken

1. Ga naar **Magazijnbeheer \> Instellingen \> Documentroutering \> Wavelabelindelingen**.
1. Maak een record met de volgende instellingen:

    - **Labelindeling-id:** *Doos*
    - **Omschrijving:** *doos (SSCC)*

1. Selecteer **Opslaan** in het actievenster.
1. Selecteer in het actievenster **Instellingen voor wavelabelrijen**.

    De pagina **Instellingen voor wavelabelrijen** wordt weergegeven. Hier kunt u het dynamische deel van het label configureren.

1. Voeg een rij toe met de volgende instellingen:

    - **Rij-id:** *WorkLine*
    - **Naam van tabelrij:** *WHSWorkLine*
    - **Beginpositie rij:** *500*

        Dit veld bepaalt de verticale positie waar de rij begint op het label.

    - **Rijhoogte:** *-50*

        In dit veld wordt de hoogte van elke rij gedefinieerd. De rijhoogte is positief voor horizontale labels en negatief voor verticale labels.

    - **Rijen per pagina:** *5*

        Dit veld bepaalt het aantal rijen dat op elk label kan worden afgedrukt.

        > [!NOTE]
        > Er worden verschillende ZPL-labels per taak afgedrukt, waarbij elke pagina maximaal vijf werkregels kan bevatten. Als er bijvoorbeeld een label wordt afgedrukt voor een container met 12 regels, worden drie labels afgedrukt. Als u een afzonderlijk label wilt afdrukken voor elke orderverzamelregel, stelt u deze waarde in op *1*.

1. Sluit de pagina.
1. Selecteer **Query bewerken** in het actievenster.
1. Voeg in het dialoogvenster Query-editor op het tabblad **Bereik** een rij toe met de volgende instellingen:

    - **Tabel:** *Werkregels*
    - **Afgeleide tabel:** *Werkregels*
    - **Veld:** *Werktype*
    - **Criteria:** *Orderverzamelen*

1. Als u de vrachtbrief-id wilt kunnen afdrukken, selecteert u op het tabblad **Joins** de tabel **Werkregels** en voegt u de tabel **Zendingen** eraan toe.
1. Sluit het dialoogvenster Query-editor.
1. Het sneltabblad **Printertekstindeling** bevat drie secties waarin u printercode kunt schrijven: **koptekstsectie**, **hoofdsectie** en **voettekstsectie**. Voer in de **Koptekstsectie** in het veld **Labelkoptekst** de code in voor de vereiste koptekst. Als u bijvoorbeeld Zebra-printers gebruikt, kunt u de volgende code gebruiken.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkTable.ContainerId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. Voer in de **Hoofdsectie** in het veld **Labelhoofdtekst** ZPL-code in voor de vereiste hoofdtekst. Hier volgt een voorbeeld.

    ```plaintext
    <Row name="WorkLine">
    <Heading>
    //Optional heading for section of rows
    </Heading>
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWorkLine.ItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWorkLine.QtyWork$ ^FS
    </Row>
    ```

1. Voer in de **Hoofdsectie** in het veld **Labelvoettekst** ZPL-code in voor de vereiste voettekst. Hier volgt een voorbeeld.

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Er wordt één exemplaar van elk label afgedrukt. Als u meer exemplaren nodig hebt (bijvoorbeeld één exemplaar voor elke zijde van de pallet), stelt u de waarde **n** voor de sectie **\^PQn** in de voettekst in op het vereiste aantal exemplaren. Als u bijvoorbeeld vier kopieën van elk label wilt afdrukken, geeft u **\^PQ4** op.

Uw label is nu klaar voor gebruik.

### <a name="create-a-wave-label-template"></a>Een wavelabelsjabloon maken

1. Ga naar **Magazijnbeheer \> Instellingen \> Documentroutering \> Wavelabelsjablonen**.
1. Voeg een waveniveausjabloon toe en stel de volgende waarden in de koptekst in:

    - **Naam van labelsjabloon:** *Containerlabels*
    - **Omschrijving:** *Containerlabels*
    - **Wavestapcode:** *PrintLabel*
    - **Magazijn:** *63*

1. Voeg op het sneltabblad **Sjabloondetails van wavelabels** een rij toe met de volgende instellingen:

    - **Labelindeling-id:** *Container*
    - **Printernaam:** selecteer een geschikte ZPL-printer.
    - **Query uitvoeren:** *Ja* (deze instelling is optioneel, maar wordt wel aanbevolen voor optimale prestaties.)

1. Selecteer **Opslaan** in het actievenster.
1. Optioneel: als u een klantspecifiek labelontwerp instelt, moet u een query maken om het klantaccount te zoeken. Ga naar het sneltabblad **Sjabloondetails van wavelabels** en selecteer **Query bewerken**. Voeg vervolgens in het dialoogvenster Query-editor op het tabblad **Bereik** een rij toe met de volgende instellingen:

    - **Tabel:** *Zendingen*
    - **Afgeleide tabel:** *Zendingen*
    - **Veld:** *Accountnummer*
    - **Criteria:** Voer het betreffende accountnummer van de klant in.

    Wanneer u klaar bent, selecteert u **OK** om het dialoogvenster Query-editor te sluiten.

### <a name="configure-number-sequence-extensions"></a>Nummerreeksuitbreidingen configureren

Nummerreeksuitbreidingen bepalen de GS1-naleving van specifieke nummerreeksen. Deze configuratie is optioneel voor het huidige scenario. Zie [Nummerreeksuitbreidingen configureren](../warehousing/configure-number-sequence-extensions.md) voor meer informatie en configuratie-instructies.

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Een verkooporder maken en vrijgeven naar het magazijn

1. Ga naar **Verkoop en marketing \> Verkooporder \> Alle verkooporders**.
1. Maak een verkooporder met de volgende instellingen:

    - **Klantrekening:** *US-001*
    - **Magazijn:** *63*

1. Vijf verkooporderregels toevoegen:

    - Verkooporderregel 1:

        - **Artikelnummer:** *A0001*
        - **Hoeveelheid:** *10*

    - Verkooporderregel 2:

        - **Artikelnummer:** *A0002*
        - **Hoeveelheid:** *20*

    - Verkooporderregel 3:

        - **Artikelnummer:** *L0006*
        - **Hoeveelheid:** *20*

    - Verkooporderregel 4:

        - **Artikelnummer:** *L0100*
        - **Hoeveelheid:** *40*

    - Verkooporderregel 5:

        - **Artikelnummer:** *L0101*
        - **Hoeveelheid:** *50*

    > [!NOTE]
    > De artikelen en hoeveelheden die hier worden vermeld, dienen alleen als voorbeeld. Er moet voorraad aanwezig zijn in het opgegeven magazijn.

1. Selecteer verkooporderregel 1. Selecteer in de sectie **Verkooporderregel** in het menu **Voorraad** de optie **Reservering**.
1. Ga naar de pagina **Reservering** en selecteer in het actievenster de optie **Partij reserveren** en sluit de pagina vervolgens.
1. Herhaal stap 4 en 5 elke extra verkooporderregel.
1. Selecteer in het actievenster op het tabblad **Magazijn** de optie **Vrijgeven naar magazijn**.

    De volgende gebeurtenissen vinden plaats:

    - Het systeem verwerkt de gemaakte zending met de sjabloon die de stap voor het afdrukken van labels bevat. De labelindeling wordt gebruikt om de indeling van het label te definiëren en het eindresultaat is een label met vijf regels dat wordt afgedrukt op de printer die is geselecteerd in de labelsjabloon.
    - Er wordt een nieuwe vrachtbrief-id gegenereerd voor de zendingen. Als u de nummerreeksuitbreidingen hebt geconfigureerd, volgen de wavelabel-id's de nummernotatie **SSCC-18**. 

U kunt deze wavelabels opnieuw afdrukken via **Magazijnbeheer \> Query's en rapporten \> Historie van wavelabels**.

## <a name="scenario-3-wave-label-printing-for-multi-tiered-labels"></a>Scenario 3: Wavelabels afdrukken voor labels met meerdere lagen

In dit scenario ziet u hoe u de functie voor het afdrukken van wavelabels gebruikt wanneer voor de magazijnprocessen verschillende niveaus van verzendlabels nodig zijn. Het kan bijvoorbeeld voorkomen dat afzonderlijke labels voor dozen en pallets moeten worden afgedrukt en dat een onderbrekingslabel voor een hele zending moet worden afgedrukt. Onderbrekingslabels zijn een afzonderlijk labeltype dat kan worden gebruikt als scheiding tussen rollen en containers, zoals labels voor de zendings-id en een streepjescode, zodat de labels gemakkelijk kunnen worden gesorteerd nadat ze zijn afgedrukt.

Het belangrijkste verschil tussen de configuratie van dit scenario en de configuratie van scenario 1 is, naast dat onderbrekingslabels zijn ingeschakeld, er meerdere wavelabeltypen moeten worden gekoppeld aan wavelabelsjablonen en aan regels voor de volgordegroep van de eenheid. Als u deze configuratie wilt voltooien, stelt u de volgende elementen in voor dit scenario:

- **Waveverwerkingsmethoden:** u markeert de wavelabelmethode als 'herhaalbaar', voegt deze twee (of meer) keer toe aan de wavesjabloon en stelt verschillende wavestapcodes in.
- **Sjablonen voor wavelabels:** u configureert de wavelabelsjablonen en koppelt deze aan de wavesjabloon. Elke wavelabelsjabloon heeft een eigen wavelabeltype.
- **Indelingen van wavelabel:** u maakt meerdere wavelabelindelingen. Er is een afzonderlijke labelindeling voor elke categorie labels en er is ook een indeling voor onderbrekingslabels.

Dit scenario toont de volledige stroom.

### <a name="make-demo-data-available"></a>Demogegevens beschikbaar maken

Voor dit scenario moeten demogegevens zijn geïnstalleerd en moet u de rechtspersoon **USMF** selecteren.

### <a name="set-up-a-wave-process-method"></a>Een waveverwerkingsmethode instellen

1. Ga naar **Magazijnbeheer \> Instellen \> Waves \> Methoden voor verwerking van waves**.
1. Controleer of **waveLabelPrinting** in de lijst staat. Als dat niet zo is, selecteert u **Methoden opnieuw genereren** in het actievenster om deze toe te voegen.
1. Voor de methode **waveLabelPrinting** schakelt u het selectievakje **Methode herhaalbaar maken** in.

### <a name="set-up-a-wave-template"></a>Een wavesjabloon instellen

1. Ga naar **Magazijnbeheer \> Instellen \> Waves \> Wavesjablonen**.
2. Selecteer een sjabloon zoals **62 Standaardverzending**.
3. Verplaats op het sneltabblad **Methoden** de methode **Wavelabels afdrukken** naar de kolom **Geselecteerde methoden**.
4. Wijs in de kolom **Geselecteerde methoden** een **wavestapcode** toe, zoals *doos*, aan de **Afdrukmethode voor wavelabels**. Zie [Wavestapcodes](wave-step-codes.md) voor meer informatie.
5. Verplaats de methode **Wavelabels afdrukken** nogmaals naar de kolom **Geselecteerde methoden**.
6. Wijs in de kolom **Geselecteerde methoden** een andere **wavestapcode** toe, zoals *pallet*, aan de tweede **Afdrukmethode voor wavelabels**. Zie [Wavestapcodes](wave-step-codes.md) voor meer informatie.

### <a name="create-three-wave-label-layouts"></a>Drie wavelabelindelingen maken

1. Ga naar **Magazijnbeheer \> Instellingen \> Documentroutering \> Wavelabelindelingen**.
1. Maak een record met de volgende instellingen:

    - **Labelindeling-id:** *Doos*
    - **Omschrijving:** *doos (SSCC)*

1. Selecteer **Opslaan** in het actievenster.
1. Selecteer in het actievenster **Instellingen voor wavelabelrijen**.

    De pagina **Instellingen voor wavelabelrijen** wordt weergegeven. Hier kunt u het dynamische deel van het label configureren.

1. Voeg een rij toe met de volgende instellingen:

    - **Rij-id:** *WaveLabel*
    - **Naam van tabelrij:** *WHSWaveLabel*
    - **Beginpositie rij:** *0*

        Dit veld bepaalt de verticale positie waar de rij begint op het label.

    - **Rijhoogte:** *0*

        Dit veld definieert de hoogte van elke rij (in punten) volgens de ZPL-standaard. De rijhoogte is positief voor horizontale labels en negatief voor verticale labels. Omdat dit voorbeeld slechts één rij bevat, kunt u de waarde instellen op *0* (nul).

    - **Rijen per pagina:** *1*

        Dit veld bepaalt het aantal rijen dat op elk label kan worden afgedrukt.

        > [!NOTE]
        > Deze instelling zorgt ervoor dat een afzonderlijk ZPL-label wordt afgedrukt voor elke record in de tabel met wavelabels.

1. Sluit de pagina.
1. Selecteer **Query bewerken** in het actievenster.
1. Voeg in het dialoogvenster Query-editor op het tabblad **Bereik** een rij toe met de volgende instellingen:

    - **Tabel:** *Werkregels*
    - **Afgeleide tabel:** *Werkregels*
    - **Veld:** *Werktype*
    - **Criteria:** *Orderverzamelen*

    Met deze query zorgt u ervoor dat alleen werkregels van het orderverzameltype worden afgedrukt op het label, niet de werkregels van het wegzettype.

1. Als u de vrachtbrief-id wilt kunnen afdrukken, selecteert u op het tabblad **Joins** de tabel **Werkregels** en voegt u de tabel **Zendingen** eraan toe. 
1. Sluit het dialoogvenster Query-editor.
1. Het sneltabblad **Printertekstindeling** bevat drie secties waarin u printercode kunt schrijven: **koptekstsectie**, **hoofdsectie** en **voettekstsectie**. Voer in de **Koptekstsectie** in het veld **Labelkoptekst** de code in voor de vereiste koptekst. Als u bijvoorbeeld Zebra-printers gebruikt, kunt u de volgende code gebruiken.


    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. Voer in de **Hoofdsectie** in het veld **Labelhoofdtekst** ZPL-code in voor de vereiste hoofdtekst. Hier volgt een voorbeeld.

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. Voer in de **Hoofdsectie** in het veld **Labelvoettekst** ZPL-code in voor de vereiste voettekst. Hier volgt een voorbeeld.

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Er wordt één exemplaar van elk label afgedrukt. Als u meer exemplaren nodig hebt (bijvoorbeeld één exemplaar voor elke zijde van de pallet), stelt u de waarde **n** voor de sectie **\^PQn** in de voettekst in op het vereiste aantal exemplaren. Als u bijvoorbeeld vier kopieën van elk label wilt afdrukken, geeft u **\^PQ4** op.

1. Het eerste label is nu klaar voor gebruik.
1. Maak een tweede indelingsrecord met de volgende instellingen:

    - **Labelindeling-id:** *Pallet*
    - **Omschrijving:** *Pallet*

1. Selecteer **Opslaan** in het actievenster.
1. Selecteer in het actievenster **Instellingen voor wavelabelrijen**.

    De pagina **Instellingen voor wavelabelrijen** wordt weergegeven. Hier kunt u het dynamische deel van het label configureren.

1. Voeg een rij toe met de volgende instellingen:

    - **Rij-id:** *WaveLabel*
    - **Naam van tabelrij:** *WHSWaveLabel*
    - **Beginpositie rij:** *0*

        Dit veld bepaalt de verticale positie waar de rij begint op het label.

    - **Rijhoogte:** *0*

        Dit veld definieert de hoogte van elke rij (in punten) volgens de ZPL-standaard. De rijhoogte is positief voor horizontale labels en negatief voor verticale labels. Omdat dit voorbeeld slechts één rij bevat, kunt u de waarde instellen op *0* (nul).

    - **Rijen per pagina:** *1*

        Dit veld bepaalt het aantal rijen dat op elk label kan worden afgedrukt.

        > [!NOTE]
        > Deze instelling zorgt ervoor dat een afzonderlijk ZPL-label wordt afgedrukt voor elke record in de tabel met wavelabels.

1. Sluit de pagina.
1. Selecteer **Query bewerken** in het actievenster.
1. Voeg in het dialoogvenster Query-editor op het tabblad **Bereik** een rij toe met de volgende instellingen:

    - **Tabel:** *Werkregels*
    - **Afgeleide tabel:** *Werkregels*
    - **Veld:** *Werktype*
    - **Criteria:** *Orderverzamelen*

    Met deze query zorgt u ervoor dat alleen werkregels van het orderverzameltype worden afgedrukt op het label, niet de werkregels van het wegzettype.

1. Als u de vrachtbrief-id wilt kunnen afdrukken, selecteert u op het tabblad **Joins** de tabel **Werkregels** en voegt u de tabel **Zendingen** eraan toe.
1. Sluit het dialoogvenster Query-editor.
1. Het sneltabblad **Printertekstindeling** bevat drie secties waarin u printercode kunt schrijven: **koptekstsectie**, **hoofdsectie** en **voettekstsectie**. Voer in de **Koptekstsectie** in het veld **Labelkoptekst** de code in voor de vereiste koptekst. Als u bijvoorbeeld Zebra-printers gebruikt, kunt u de volgende code gebruiken.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWaveLabel.WaveLabelId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. Voer in de **Hoofdsectie** in het veld **Labelhoofdtekst** ZPL-code in voor de vereiste hoofdtekst. Hier volgt een voorbeeld.

    ```plaintext
    <Row name="WaveLabel">
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWaveLabel.LabelItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWaveLabel.QtyWork$ ^FS
    </Row>
    ```

1. Voer in de **Hoofdsectie** in het veld **Labelvoettekst** ZPL-code in voor de vereiste voettekst. Hier volgt een voorbeeld.

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Er wordt één exemplaar van elk label afgedrukt. Als u meer exemplaren nodig hebt (bijvoorbeeld één exemplaar voor elke zijde van de pallet), stelt u de waarde **n** voor de sectie **\^PQn** in de voettekst in op het vereiste aantal exemplaren. Als u bijvoorbeeld vier kopieën van elk label wilt afdrukken, geeft u **\^PQ4** op.

1. Het tweede label is nu klaar voor gebruik.
1. Maak een derde indelingsrecord met de volgende instellingen:

    - **Labelindeling-id:** *Onderbreking*
    - **Beschrijving:** *Onderbrekingslabel*

1. Selecteer **Opslaan** in het actievenster.
1. Het sneltabblad **Printertekstindeling** bevat drie secties waarin u printercode kunt schrijven: **koptekstsectie**, **hoofdsectie** en **voettekstsectie**. Voer in de **Koptekstsectie** in het veld **Labelkoptekst** de ZPL-code in voor de vereiste koptekst. Hier volgt een voorbeeld.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ```

1. Deze keer is er geen hoofdtekst verplicht. Voer daarom alleen de vereiste tekst in de **Voettekstsectie** in. Hier volgt een voorbeeld.

    ```plaintext
    ^XZ
    ```

    Het derde label is nu klaar voor gebruik.

    > [!NOTE]
    > Dit derde label is een onderbrekingslabel dat wordt gebruikt als scheiding tussen labelrollen.

### <a name="create-two-wave-label-types"></a>Twee wavelabeltypen maken

1. Ga naar **Magazijnbeheer \> Instellingen \> Documentroutering \> Wavelabeltypen**.
1. Maak een record met de volgende instellingen:

    - **Labeltype:** *Doos*
    - **Omschrijving:** *Doos*

1. Maak een tweede record met de volgende instellingen:

    - **Labeltype:** *Pallet*
    - **Omschrijving:** *Pallet*

### <a name="set-up-unit-sequence-groups"></a>Eenheidvolgordegroepen instellen

1. Ga naar **Magazijnbeheer \> Instellingen \> Magazijn \> Volgordegroepen eenheid**.
1. Selecteer of maak een groep **Ea Box PL**.
1. Stel voor de regel **Doos** het veld **Waveniveautype** in op *Doos*.
1. Stel voor de regel **PL** het veld **Waveniveautype** in op *Pallet*.

### <a name="create-wave-label-templates"></a>Wavelabelsjablonen maken

1. Ga naar **Magazijnbeheer \> Instellingen \> Documentroutering \> Wavelabelsjablonen**.
1. Maak een labelsjabloon met de volgende instellingen:

    - **Naam van labelsjabloon:** *Dooslabels*
    - **Omschrijving:** *Dooslabels*
    - **Wavestapcode:** *Doos*
    - **Magazijn:** *62*

1. Op het sneltabblad **Algemeen** selecteert u een waarde zoals **Doos** in het veld *Wavelabeltype*.
1. Voeg op het sneltabblad **Sjabloondetails van wavelabels** een rij toe met de volgende instellingen:

    - **Labelindeling-id:** *Doos*
    - **Printernaam:** selecteer een geschikte ZPL-printer.
    - **Query uitvoeren:** *Ja* (deze instelling is optioneel, maar wordt wel aanbevolen voor optimale prestaties.)

1. Selecteer **Opslaan** in het actievenster.
1. Optioneel: als u een klantspecifiek labelontwerp instelt, moet u een query maken om het klantaccount te zoeken. Ga naar het sneltabblad **Sjabloondetails van wavelabels** en selecteer **Query bewerken**. Voeg vervolgens in het dialoogvenster Query-editor op het tabblad **Bereik** een rij toe met de volgende instellingen:

    - **Tabel:** *Zendingen*
    - **Afgeleide tabel:** *Zendingen*
    - **Veld:** *Accountnummer*
    - **Criteria:** Voer het betreffende accountnummer van de klant in.

    Wanneer u klaar bent, selecteert u **OK** om het dialoogvenster Query-editor te sluiten.

1. Selecteer in het actievenster de optie **Query bewerken** om het dialoogvenster Query-editor te openen voor de hele labelsjabloon.
1. Voeg in het dialoogvenster Query-editor op het tabblad **Sortering** een rij toe met de volgende instellingen:

    - **Tabel:** *Werkregels*
    - **Afgeleide tabel:** *Werkregels*
    - **Veld:** *Verwijzing ladingsregel-id (record-id)*
    - **Zoekrichting:** *Oplopend*

1. Voeg een tweede rij toe met de volgende instellingen:

    - **Tabel:** *Werkregels*
    - **Afgeleide tabel:** *Werkregels*
    - **Veld:** *Zending-id*
    - **Zoekrichting:** *Oplopend*

1. Selecteer **OK** om het dialoogvenster Query-editor te sluiten.
1. U wordt gevraagd om de bewerking voor het opnieuw instellen van de groepering te bevestigen. Selecteer **Ja** om door te gaan.
1. Selecteer in het actievenster **Sjabloongroep voor wavelabel**.
1. Stel in het dialoogvenster **Sjabloongroep voor wavelabel** de volgende waarden in voor de rij waarin het veld **Naam verwijzingsveld** is ingesteld op *Zending-id*:

    - **Onderbrekingslabel afdrukken:** schakel dit selectievakje in.
    - **Labelindelings-id:** selecteer een onderbrekingslabel. (Selecteer bijvoorbeeld de indeling *Onderbrekingslabel* die u eerder in dit scenario hebt gemaakt.)
    - **Printernaam:** selecteer de printer voor het onderbrekingslabel. (Gewoonlijk moet u voor het splitsen van labelrollen dezelfde printer selecteren die is geselecteerd op het Het sneltabblad **Sjabloondetails van wavelabel**. Er zijn echter andere scenario's mogelijk.)

1. Schakel het selectievakje **Labelbuild-id** in voor de rij waarin het veld *Naam verwijzingsveld* is ingesteld op **Verwijzing ladingsregel-id**.

    > [!NOTE]
    > Met deze instelling wordt één labelreeks ("doos 1 van X") per ladingsregel gemaakt in de hele wave, ongeacht de instelling van de werkgroepering. Deze labelreeks kan worden afgedrukt op een labelindeling. Bovendien worden labels voor verschillende zendingen gescheiden door het geselecteerde onderbrekingslabel.

1. Selecteer **OK** om het dialoogvenster **Sjabloongroep voor wavelabel** te sluiten.
1. Maak een tweede labelsjabloon met de volgende instellingen:

    - **Naam van labelsjabloon:** *Palletlabels*
    - **Omschrijving:** *Palletlabels*
    - **Wavestapcode:** *Pallet*
    - **Magazijn:** *62*

1. Op het sneltabblad **Algemeen** selecteert u een waarde zoals **Pallet** in het veld *Wavelabeltype*.
1. Voeg op het sneltabblad **Sjabloondetails van wavelabels** een rij toe met de volgende instellingen:

    - **Labelindeling-id:** *Pallet*
    - **Printernaam:** selecteer een geschikte ZPL-printer.
    - **Query uitvoeren:** *Ja* (deze instelling is optioneel, maar wordt wel aanbevolen voor optimale prestaties.)

1. Selecteer **Opslaan** in het actievenster.
1. Optioneel: als u een klantspecifiek labelontwerp instelt, moet u een query maken om het klantaccount te zoeken. Ga naar het sneltabblad **Sjabloondetails van wavelabels** en selecteer **Query bewerken**. Voeg vervolgens in het dialoogvenster Query-editor op het tabblad **Bereik** een rij toe met de volgende instellingen:

    - **Tabel:** *Zendingen*
    - **Afgeleide tabel:** *Zendingen*
    - **Veld:** *Accountnummer*
    - **Criteria:** Voer het betreffende accountnummer van de klant in.

    Wanneer u klaar bent, selecteert u **OK** om het dialoogvenster Query-editor te sluiten. 

1. Selecteer in het actievenster de optie **Query bewerken** om het dialoogvenster Query-editor te openen voor de hele labelsjabloon.
1. Voeg in het dialoogvenster Query-editor op het tabblad **Sortering** een rij toe met de volgende instellingen:

    - **Tabel:** *Werkregels*
    - **Afgeleide tabel:** *Werkregels*
    - **Veld:** *Verwijzing ladingsregel-id (record-id)*
    - **Zoekrichting:** *Oplopend*

1. Voeg een tweede rij toe met de volgende instellingen:

    - **Tabel:** *Werkregels*
    - **Afgeleide tabel:** *Werkregels*
    - **Veld:** *Zending-id*
    - **Zoekrichting:** *Oplopend*

1. Selecteer **OK** om het dialoogvenster Query-editor te sluiten.
1. U wordt gevraagd om de bewerking voor het opnieuw instellen van de groepering te bevestigen. Selecteer **Ja** om door te gaan.
1. Selecteer in het actievenster **Sjabloongroep voor wavelabel**.
1. Stel in het dialoogvenster **Sjabloongroep voor wavelabel** de volgende waarden in voor de rij waarin het veld **Naam verwijzingsveld** is ingesteld op *Zending-id*:

    - **Onderbrekingslabel afdrukken:** schakel dit selectievakje in.
    - **Labelindelings-id:** selecteer een onderbrekingslabel. (Selecteer bijvoorbeeld de indeling *Onderbrekingslabel* die u eerder in dit scenario hebt gemaakt.)
    - **Printernaam:** selecteer de printer voor het onderbrekingslabel. (Gewoonlijk moet u voor het splitsen van labelrollen dezelfde printer selecteren die is geselecteerd op het Het sneltabblad **Sjabloondetails van wavelabel**. Er zijn echter andere scenario's mogelijk.)

1. Schakel het selectievakje **Labelbuild-id** in voor de rij waarin het veld *Naam verwijzingsveld* is ingesteld op **Verwijzing ladingsregel-id**.

    > [!NOTE]
    > Met deze instelling wordt één labelreeks ("doos 1 van X") per ladingsregel gemaakt in de hele wave, ongeacht de instelling van de werkgroepering. Deze labelreeks kan worden afgedrukt op een labelindeling. Bovendien worden labels voor verschillende zendingen gescheiden door het geselecteerde onderbrekingslabel.

### <a name="configure-number-sequence-extensions"></a>Nummerreeksuitbreidingen configureren

Nummerreeksuitbreidingen bepalen de GS1-naleving van specifieke nummerreeksen. Deze configuratie is optioneel voor het huidige scenario. Zie [Nummerreeksuitbreidingen configureren](../warehousing/configure-number-sequence-extensions.md) voor meer informatie en configuratie-instructies.

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Een verkooporder maken en vrijgeven naar het magazijn

1. Ga naar **Verkoop en marketing \> Verkooporder \> Alle verkooporders**.
1. Maak een verkooporder met de volgende instellingen:

    - **Klantrekening:** *US-001*
    - **Magazijn:** *62*

1. Twee verkooporderregels toevoegen:

    - Verkooporderregel 1:

        - **Artikelnummer:** *A0001*
        - **Hoeveelheid:** *9024*
        - **Eenheid:** *ea* (9024 ea = 376 dozen = 47 PL)

    - Verkooporderregel 2:

        - **Artikelnummer:** *A0002*
        - **Hoeveelheid:** *9016*
        - **Eenheid:** *ea* (9016 ea = 322 dozen = 46 PL)

    > [!NOTE]
    > De artikelen en hoeveelheden die hier worden vermeld, dienen alleen als voorbeeld. Ze moeten de volgordegroep van de eenheid gebruiken die u eerder hebt gedefinieerd. Er moeten correcte eenheidsomrekeningen van *ea* naar *doos* naar *PL* zijn gedefinieerd en ze moeten op voorraad zijn in magazijn *62*. Zie [Maateenheid en voorraadbeleid](unit-measure-stocking-policies.md) voor meer informatie.

1. Selecteer verkooporderregel 1. Selecteer in de sectie **Verkooporderregel** in het menu **Voorraad** de optie **Reservering**.
1. Ga naar de pagina **Reservering** en selecteer in het actievenster de optie **Partij reserveren** en sluit de pagina vervolgens.
1. Herhaal stap 4 en 5 voor verkooporderregel 2.
1. Selecteer in het actievenster op het tabblad **Magazijn** de optie **Vrijgeven naar magazijn**.

    De volgende gebeurtenissen vinden plaats: 

    - Het systeem verwerkt de gemaakte zending met behulp van de sjabloon die de stap voor het afdrukken van labels bevat. De labelindeling wordt gebruikt om de indeling van het label te definiëren en het resultaat is een label dat wordt afgedrukt op de printer die is geselecteerd in de labelsjabloon.
    - Er worden wavelabels gegenereerd en afgedrukt. Het aantal labels komt overeen met het aantal dozen (in dit voorbeeld 376 labels voor regel 1, 322 labels voor regel 2, 47 PL-labels voor regel 1, 47 PL-labels voor regel 2 en twee onderbrekingslabels met de zending-id).
    - Er wordt een nieuwe vrachtbrief-id gegenereerd voor de zendingen. Als u de nummerreeksuitbreidingen hebt geconfigureerd, volgen de wavelabel-id's de nummernotatie **SSCC-18**. 

U kunt wavelabels weergeven en opnieuw afdrukken op de volgende pagina's:

- Alle zendingen \> Details van zending
- Alle ladingen \> Details van lading
- Alle waves
- Wavelabels
- Historie wavelabel

Voor de meeste van deze pagina's kunt u de relevante functie vinden door **Wavelabels** te selecteren in de groep **Verwante informatie** op het tabblad **Zendingen** van het actievenster.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Wavelabels opnieuw afdrukken en ongeldig maken](reprint-and-void-wave-labels.md)
- [Wavelabel afdrukken plannen tijdens wave](configure-task-based-wave-label-printing.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
