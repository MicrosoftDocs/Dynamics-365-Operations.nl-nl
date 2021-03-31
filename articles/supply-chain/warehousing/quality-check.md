---
title: Kwaliteitscontrole
description: Dit onderwerp bevat informatie over de functie voor kwaliteitscontrole. Met deze functie kunnen magazijnmedewerkers snel controleren op kwaliteit terwijl zij artikelen ontvangen naar het inkomend docking-gebied.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSQualityCheckTemplate, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSQualityCheckResult
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 31afcfcb9d8dbb91f4ea4e3e7a7282c2a87328d4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5228460"
---
# <a name="quality-check"></a>Kwaliteitscontrole

[!include [banner](../includes/banner.md)]

Met de functie *Kwaliteitscontrole* kunnen magazijnmedewerkers snel controleren op kwaliteit terwijl zij artikelen ontvangen naar het inkomend docking-gebied. Deze controles zijn nuttig wanneer werknemers verpakking of andere gemakkelijk herkenbare delen van een artikel controleren. De functie helpt werknemers om snel te kijken of er iets misgaat of beschadigd raakt voordat ze de voorraad in de wegzetlocatie opslaan.

Deze functie is een alternatief voor het standaardproces voor kwaliteitscontrole. Het biedt meer flexibiliteit en snellere verwerking.

Wanneer u deze functie gebruikt, worden de ontvangst en de kwaliteitscontrole op de volgende manier uitgevoerd:

1. Wanneer een zending arriveert, registreert een magazijnmedewerker de ontvangst. De werknemer scant ook een nummerplaat om de locatie te registreren.
1. De werknemer voert een snelle kwaliteitscontrole uit en registreert het resultaat (geslaagd of mislukt) voor die nummerplaat.
1. Een van de volgende acties wordt uitgevoerd:

    - Als de kwaliteitscontrole slaagt, wordt de nummerplaat op de gebruikelijke manier geaccepteerd en doorgeleid naar de locatie van ontvangst.
    - Als de kwaliteitscontrole mislukt, wordt de nummerplaat afgewezen en wordt het bestaande wegzetwerk ervoor omgeleid naar een alternatieve locatie voor verdere inspectie. Er wordt een nieuwe kwaliteitsorder gemaakt. Als u de kwaliteitsorder wilt weergeven die is gemaakt voor de mislukte kwaliteitscontrole, gaat u naar **Voorraadbeheer \> Periodieke taken \> Kwaliteitsbeheer \> Kwaliteitsorders**.

Dit proces kan ook zo worden ingesteld dat alle gescande nummerplaten direct naar de locatie van de kwaliteitscontrole worden gebracht.

## <a name="turn-on-the-quality-check-feature"></a>De functie Kwaliteitscontrole inschakelen

Voordat u de functie *Kwaliteitscontrole* kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en desgewenst in te schakelen. Schakel in het werkgebied **Functiebeheer** de functie als volgt in:

- **Module:** *Magazijnbeheer*
- **Functienaam:** *Kwaliteitscontrole*

## <a name="set-up-the-feature-for-the-example-scenario"></a>De functie instellen voor het voorbeeldscenario

Deze sectie bevat richtlijnen en een voorbeeld waarin wordt uitgelegd hoe u de functie *Kwaliteitscontrole* instelt en voorbeeldgegevens voorbereidt voor het voorbeeldscenario dat verderop in dit onderwerp wordt gegeven.

### <a name="make-sample-data-available"></a>Voorbeeldgegevens beschikbaar maken

Als u het [voorbeeldscenario](#example-scenario) wilt doorlopen met de hier opgegeven voorbeeldrecords en -waarden, moet u een systeem gebruiken waarop de standaard [demogegevens](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) zijn geïnstalleerd. U moet daarnaast ook de rechtspersoon **USMF** selecteren voordat u begint.

### <a name="quality-check-template"></a><a name="quality-template"></a>Sjabloon kwaliteitscontrole

Met de sjabloon voor kwaliteitscontrole worden de regels gedefinieerd voor het uitvoeren van snelle controles op kwaliteit op het moment van ontvangst.

1. Ga naar **Magazijnbeheer \> Instellen \> Werk \> Kwaliteitscontrolesjablonen**.
1. Selecteer **Nieuw** om een sjabloon toe te voegen aan het raster.
1. Stel de volgende waarden in om de nieuwe sjabloon te definiëren:

    - **Naam van sjabloon voor kwaliteitscontrole:** *Dock-controle*

        Voer een naam in die het beleid aanduidt dat voor deze sjabloon wordt toegepast.

    - **Acceptatiebeleid:** *Vragen aan gebruiker*

        Geef op of gebruikers moet worden gevraagd de kwaliteit van de voorraad te accepteren of af te wijzen tijdens het verwerken van het werk, of dat de kwaliteit automatisch moet worden afgewezen. De beschikbare opties zijn *Automatisch afwijzen* en *Vragen aan gebruiker*.

    - **Beleid voor kwaliteitsverwerkings:** *Kwaliteitsorder maken*

        Selecteer het beleid dat moet worden gebruikt bij het afwijzen van de kwaliteit van de voorraad. De volgende opties zijn beschikbaar:

        - *Alleen werk maken*: alleen werk maken om de voorraadverplaatsing te vergemakkelijken.
        - *Kwaliteitsorder maken*: een kwaliteitsorder maken om kwaliteitstests te vergemakkelijken.

    - **Testgroep:** *Monster*

        Geef de testgroep op die moet worden gebruikt in de kwaliteitsorder die wordt gemaakt. Testgroepen worden ingesteld in de module **Voorraadbeheer**.

        Laat de optie **Destructieve tekst** uitgeschakeld voor de testgroep. Deze optie definieert wanneer het monster wordt vernietigd als onderdeel van de tests in de testgroep. Als een destructieve test wordt gebruikt, genereert het systeem een voorraadtransactie wanneer een kwaliteitsorder voor het artikel wordt gemaakt. De nieuwe voorraadtransactie voorspelt de voorraadreductie voor de testhoeveelheid. De voorraadreductie treedt op wanneer de kwaliteitsorder wordt voltooid door de validatiestap. De voorraadtransactie wordt aangeduid als een kwaliteitsorder.

### <a name="work-class--quality-check"></a><a name="work-class"></a>Werkklasse: Kwaliteitscontrole

Werkklassen worden gebruikt om het type werkorderregels te bepalen en/of beperken dat magazijnwerknemers op een mobiel apparaat kunnen verwerken.

1. Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werkklassen**.
1. Selecteer **Nieuw** om een werkklasse te maken.
1. Stel in de koptekst de volgende waarden in:

    - **Werkklasse-id:** *Kwaliteitscontrole*

        Voer een naam in waarmee de werkklasse wordt aangeduid.

    - **Omschrijving:** *Kwaliteitscontrole*

        Voer een korte omschrijving in waarmee wordt aangegeven waarvoor de werkklasse wordt gebruikt.

    - **Werkordertype:** *Kwaliteit in kwaliteitscontrole*

        Het type werkorder selecteren dat door de werkklasse wordt gemaakt. Wanneer u het kwaliteitscontrolewerk instelt, moet u altijd *Kwaliteit in kwaliteitscontrole* selecteren.

1. Laat op het tabblad **Geldige typen locaties voor plaatsing** het veld **Locatietype** leeg.

    Als u een locatie type selecteert, beperkt u de locaties waar artikelen kunnen worden geplaatst nadat ze zijn verzameld. Dit veld wordt gebruikt wanneer een locatierichtlijn probeert de locatie op te lossen of wanneer een magazijnwerknemer handmatig de locatie voor menuopdrachten van mobiele apparaten opgeeft.

Zie voor meer informatie over werkklassen en hoe u ze maakt [Werkklassen maken](tasks/create-work-class.md).

### <a name="work-template"></a>Werksjabloon

Op de pagina Werksjablonen kunt u de werkbewerkingen definiëren die in het magazijn moet worden uitgevoerd. Doorgaans bestaan de bewerkingen van het magazijnwerk uit een tweetal acties: een magazijnwerknemer verzamelt voorhanden voorraad in één locatie en brengt de voorraad vervolgens naar een andere locatie. Met een werksjabloon voor kwaliteitscontrole worden de werkbewerkingen gedefinieerd voor het uitvoeren van kwaliteitscontroles.

#### <a name="purchase-orders"></a>Inkooporders

1. Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werksjablonen**.
1. Stel in de koptekst het veld **Werkordertype** in op *Inkooporders*.
1. Selecteer **Bewerken** in het actievenster.
1. Selecteer een werksjabloon die een kwaliteitscontrolestap moet bevatten. Selecteer in het gedeelte **Overzicht** in het veld **Werksjabloon** *51 IO-ontvangst*.
1. In de sectie **Werksjabloongegevens** ziet u dat het raster twee bestaande regels bevat: een voor *Verzamelen* en een voor *Wegzetten*.
1. Selecteer in de sectie **Werksjabloongegevens** **Nieuw** om een rij voor kwaliteitscontrole toe te voegen aan het raster. Het veld **Regelnummer** voor de nieuwe regel wordt ingesteld op *3*.
1. Stel op de nieuwe regel de volgende waarden in. Accepteer de standaardwaarden voor de overige velden.

    - **Werksoort:** *Kwaliteitscontrole*
    - **Werkklasse-id:** *Aankoop*
    - **Naam van sjabloon voor kwaliteitscontrole:** *Dock-controle*

        Selecteer de unieke ID voor de werkklasse. U gebruikt deze waarde om de menuopties op het mobiele apparaat en typen het werk te configureren die deze menu-items kunnen verwerken.

1. Selecteer in het actievenster de optie **Opslaan** om uw werk tot dusverre op te slaan.

    U ontvangt een bericht met de mededeling dat de kwaliteitscontrole direct na de verzameling moet komen. Daarom moet u de waarde **Regelnummer** wijzigen voor de regel die u zojuist hebt toegevoegd.

1. Voer de volgende stappen uit om de waarde **Regelnummer** voor de nieuwe regel te wijzigen:

    1. Selecteer in de sectie **Werksjabloongegevens** de regel waarvoor het veld **Werksoort** is ingesteld op *Kwaliteitscontrole*.
    2. Selecteer de knop **Omhoog verplaatsen** of **Omlaag verplaatsen** om de regel *Kwaliteitscontrole* te verplaatsen, zodat deze na de regel *Verzamelen* valt.

1. Selecteer **Opslaan** in het actievenster.

#### <a name="quality-in-quality-check"></a>Kwaliteit in kwaliteitscontrole

Maak vervolgens een werksjabloon voor de kwaliteitscontrole.

1. Wijzig in de koptekst van de pagina **Werksjablonen** de waarde van het veld **Werkordertype** in *Kwaliteitscontrole*.
1. Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster in de sectie **Overzicht**.
1. Stel in de nieuwe rij de volgende waarden in:

    - **Werksjabloon:** *51 Kwaliteitscontrole*

        Voer een naam voor de sjabloon in.

    - **Omschrijving werksjabloon:** *51 Kwaliteitscontrole*

1. Selecteer in het actievenster **Opslaan** om de sectie **Werksjabloongegevens** beschikbaar te maken.
1. Selecteer terwijl de nieuwe sjabloon nog is geselecteerd in de sectie **Overzicht** **Nieuw** in de sectie **Werksjabloongegevens** om een rij toe te voegen aan het raster daar.
1. Stel in de nieuwe rij de volgende waarden in:

    - **Werktype:** *Orderverzamelen*
    - **Werkklasse-id:** *Kwaliteitscontrole*

        Selecteer de naam van de [werkklasse](#work-class) die u eerder hebt gemaakt voor kwaliteitscontrolewerk.

1. Selecteer **Nieuw** in de sectie **Werksjabloongegevens** om nog een rij toe te voegen.
1. Stel in de nieuwe rij de volgende waarden in:

    - **Werktype:** *Wegzetten*
    - **Werkklasse-id:** *Kwaliteitscontrole*

        Selecteer de naam van de [werkklasse](#work-class) die u eerder hebt gemaakt voor kwaliteitscontrolewerk.

1. Selecteer **Opslaan** in het actievenster.

Zie voor meer informatie over werksjablonen [Magazijnwerk beheren met werksjablonen en locatierichtlijnen](control-warehouse-location-directives.md)

### <a name="location-directive--quality-failures"></a>Locatierichtlijn: Kwaliteitsproblemen

De locatierichtlijnen zijn regels die verzamelings- en wegzetlocaties identificeren voor voorraadverplaatsing. Bijvoorbeeld, in een verkoopordertransactie, bepaalt een locatierichtlijn waar de artikelen worden verzameld en waar de verzamelde artikelen worden weggezet. U moet een locatierichtlijnregel configureren om te definiëren hoe mislukte kwaliteitscontroles worden verwerkt.

1. Ga naar **Magazijnbeheer \> Instellen \> Locatierichtlijnen**.
1. Stel in het linkerdeelvenster het veld **Werkordertype** in op *Inkooporders* om te werken met locatierichtlijnen van dat type.
1. Selecteer in het actievenster de optie **Nieuw** om een locatierichtlijn voor kwaliteitscontroles te maken.
1. Stel in de koptekst de volgende waarden in:

    - **Volgnummer:** Accepteer de standaard waarde.
    - **Naam:** *51 Naar kwaliteit*

1. Stel op het sneltabblad **Locatie-instructies** de volgende waarden in. Accepteer de standaardwaarden voor de overige velden.

    - **Werktype:** *Wegzetten*
    - **Locatie:** *5*
    - **Magazijn:** *51*

1. Selecteer in het actievenster **Opslaan** om uw richtlijn op te slaan en het sneltabblad **Regels** beschikbaar te maken.
1. Ga naar het sneltabblad **Regels** en selecteer **Nieuw** om een regel toe te voegen aan het raster.
1. Stel op de nieuwe regel de volgende waarden in. Accepteer de standaardwaarden voor de overige velden.

    - **Vanaf hoeveelheid:** *1*
    - **Tot hoeveelheid:** *1000000*

1. Selecteer in het actievenster **Opslaan** om de nieuwe regel op te slaan en het sneltabblad **Locatie-instructieacties** beschikbaar te maken.
1. Terwijl de nieuwe regel nog steeds is geselecteerd op het sneltabblad **Regels**, selecteert u **Nieuw** op het sneltabblad **Locatie-instructieacties** om een rij toe te voegen aan het raster daar, zodat u een actie voor de regel kunt instellen.
1. Stel op de nieuwe rij het veld **Naam** in op *Kwaliteit*. Accepteer de standaardwaarden voor de overige velden.
1. Selecteer in het actievenster **Opslaan** om de knop **Query bewerken** op het sneltabblad **Locatie-instructieacties** beschikbaar te maken.
1. Terwijl de regel die u zojuist hebt toegevoegd nog steeds is geselecteerd op het sneltabblad **Locatie-instructieacties**, selecteert u **Query bewerken** om een dialoogvenster te openen waarin u de query voor de actie kunt bewerken.
1. Selecteer op het tabblad **Bereik** de optie **Toevoegen** om een rij toe te voegen aan de query.
1. Stel in de nieuwe rij de volgende waarden in:

    - **Tabel:** *Locaties*
    - **Afgeleide tabel:** *Locaties*
    - **Veld:** *Locatie*
    - **Criteria:** *QMS*

    De *QMS*-locatie is een magazijnlocatie voor kwaliteit.

1. Selecteer **OK** om het dialoogvenster te sluiten.
1. U moet nu de volgorde van de bestaande inkooporderlocatierichtlijnen wijzigen voor magazijn *51*. Sla de nieuwe locatierichtlijn *51 Naar kwaliteit* op, vernieuw de pagina en selecteer de locatierichtlijn in de lijst. Gebruik vervolgens de knoppen **Omhoog verplaatsen** en **Omlaag verplaatsen** in het actievenster om de locatie-instructie voor magazijn *51* in de volgende volgorde te plaatsen. (Voordat u **Omhoog verplaatsen** of **Omlaag verplaatsen** selecteert, moet u een locatierichtlijn selecteren in de lijst.)

    1. 51 Naar kwaliteit
    2. 51 IO direct
    3. 51 QMS

### <a name="mobile-device-menu-items"></a>Menuopties voor mobiel apparaat

Configureer een menuopdracht zodat mobiele apparaten de functie **Kwaliteitscontrole** kunnen uitvoeren.

#### <a name="purchase-putaway"></a>Opslag van inkoop

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.
1. Selecteer de menuopdracht **Opslag van inkoop** in de lijst.
1. Selecteer **Bewerken** in het actievenster.
1. Selecteer in de sectie **Werkklassen** **Nieuw** om een rij toe te voegen aan het raster.
1. Stel in de nieuwe rij de volgende waarden in:

    - **Werkklasse-id:** *Kwaliteitscontrole*

        Voer de naam in van de [werkklasse](#work-class) die u eerder hebt gemaakt voor kwaliteitscontrolewerk.

    - **Werkordertype:** *Kwaliteit in kwaliteitscontrole*

1. Selecteer **Opslaan** in het actievenster.

#### <a name="purchase-order-line-receiving"></a>Ontvangen van inkooporderregel

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.
1. Selecteer **Nieuw** in het actievenster.
1. Stel in de koptekst de volgende waarden in:

    - **Menuoptie:** *IO-regel ontvangst*
    - **Titel:** *IO-regel ontvangst*
    - **Modus:** *werk*
    - **Bestaand werk gebruiken:** *Nee*

1. Stel op het sneltabblad **Algemeen** de volgende waarden in. Accepteer de standaardwaarden voor de overige velden.

    - **Procedure voor het maken van werk:** *Ontvangen van inkooporderregel en wegzetten*
    - **Nummerplaat maken:** *Ja*
    - **Werksjabloon:** *51 IO ontvangst*

1. Selecteer **Opslaan** in het actievenster.

#### <a name="add-the-menu-item-to-a-mobile-device-menu"></a>De menuopdracht toevoegen aan het menu van een mobiel apparaat

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menu voor mobiel apparaat**.
1. Selecteer het menu **Inkomend** in het linkerdeelvenster.
1. Selecteer **Bewerken** in het actievenster.
1. Selecteer in de kolom **Beschikbare menu's en menuopdrachten** de nieuwe menuopdracht **IO-regel ontvangst**.
1. Selecteer de pijl naar rechts om **IO-regel ontvangst** naar de kolom **Menustructuur** te verplaatsen.
1. Selecteer in de kolom **Menustructuur** de optie **IO-regel ontvangst** en selecteer vervolgens de knop pijl-omhoog of pijl-omlaag om de menuoptie naar de gewenste positie in het menu van het mobiele apparaat te verplaatsen.
1. Selecteer **Opslaan** in het actievenster.

## <a name="example-scenario"></a><a name="example-scenario"></a>Voorbeeldscenario

Nadat u alle eerder beschreven voorbeeldgegevens hebt gemaakt en ingesteld, kunt u dit scenario doorlopen om de functie *Kwaliteitscontrole* uit te proberen. Bij de waarden die in dit scenario worden weergegeven, wordt ervan uitgegaan dat u werkt met de standaarddemonstratiegegevens, dat u de rechtspersoon **USMF** hebt geselecteerd en dat u de voorbeeldrecords hebt voorbereid die eerder in dit onderwerp zijn beschreven. Dit scenario dient ook als voorbeeld waarin wordt aangegeven hoe de functie in een productie-instelling kan worden gebruikt.

### <a name="create-a-purchase-order"></a>Inkooporder maken

1. Ga naar **Inkoop en sourcing \> Inkooporders \> Alle inkooporders**.
1. Selecteer **Nieuw** in het actievenster.
1. Stel in het dialoogvenster **Inkooporder maken** de volgende waarden in:

    - **Leverancierrekening:** *104*
    - **Magazijn:** *51*

1. Selecteer **OK** om het dialoogvenster te sluiten en de nieuwe inkooporder te openen.
1. Op het sneltabblad **Inkooporderregels** bevat het raster een nieuwe, lege regel. Stel op deze regel de volgende waarden in:

    - **Artikelnummer:** *M9203*
    - **Hoeveelheid:** *3*
    - **Eenheid:** *PL*

1. Selecteer **Opslaan** in het actievenster.

### <a name="process-quality-check-receiving"></a>Ontvangst controleren van proceskwaliteit

Nadat de inkooporder is gemaakt, kunt u deze ontvangen met de menuopdracht **IO-regel ontvangst** en de functionaliteit van de functie *Kwaliteitscontrole*.

#### <a name="receive-pallet-1"></a>Pallet 1 ontvangen

1. Meld u aan bij de magazijnapp als een gebruiker voor magazijn *51*. (Geef *51* op als gebruikers-id en *1* als wachtwoord.)
1. Ga naar **Inkomend \> IO-regel ontvangst**.
1. Voer in het veld **Inkoopordernummer** het inkoopordernummer in.
1. Bevestig het inkoopordernummer.
1. Voer in het veld **Regelnummer** het regelnummer in van de inkooporderregel die u ontvangt. Aangezien de order slechts één regel bevat in dit scenario, voert u *1* in het veld **Regelnummer** in voor elke ontvangststap.
1. Controleer het regelnummer.
1. Voer in het veld **Hoeveelheid** de te ontvangen hoeveelheid in. Aangezien de inkooporder voor drie pallets (*PL*) is in dit scenario en er drie ontvangststappen zijn, voert u *1* in het veld **Hoeveelheid** in voor elke ontvangststap.
1. Bevestig de hoeveelheid.

    De pagina **Kwaliteitscontrole** die wordt weergegeven, bevat geen invoervelden. De pagina bevat alleen de bevestigingsknop (vinkje) onderaan en de menuknop (**≡**) bovenaan. (De menuknop wordt ook wel de hamburger of de hamburgerknop genoemd.) Om het proces voor de kwaliteitscontrole te versnellen, bevestigt de gebruiker alleen de pagina **Kwaliteitscontrole** wanneer de pallet langs de kwaliteitscontrole komt.

    ![Pagina Kwaliteitscontrole](media/quality-check.png "Pagina Kwaliteitscontrole")

1. Selecteer de bevestigingsknop om de kwaliteitscontrole door te geven voor pallet 1 van regel 1.

    Op de pagina **Inkoop orders: wegzetten** staan details van het wegzetwerk.

    - **LOC:** de door het systeem vastgestelde locatie

        Deze locatie is de aangewezen wegzetlocatie voor het ontvangen van inkooporders.

    - **LP:** de door het systeem gegenereerde nummerplaat-id
    - **Artikel:** *M9203*
    - **Hoeveelheid:** *1 PL: 100 stuks*

    De artikelomschrijving wordt ook weergegeven.

1. Bevestig het wegzetwerk.

    Op de pagina **Taak** voor het ontvangen van inkooporderregels wordt het bericht 'Werk voltooid' weergegeven. Het veld **Regelnummer** is beschikbaar zodat u de volgende pallet kunt ontvangen.

#### <a name="receive-pallet-2"></a>Pallet 2 ontvangen

Voor dit scenario wordt pallet 2 afgewezen.

1. Voer *1* in het veld **Regelnummer** in en bevestig het regelnummer.
1. Het veld **Hoeveelheid** is nu beschikbaar. Voer *1* in en bevestig de hoeveelheid.

    De pagina **Kwaliteitscontrole** wordt weergegeven. Voor deze ontvangst wordt de pallet afgewezen voor kwaliteit en wordt deze op de kwaliteitslocatie *QMS* weggezet.

1. Selecteer de menuknop (**≡**) boven aan de pagina en selecteer vervolgens in het menu de optie **Weigeren**.
1. Voer op de pagina **Taak** die verschijnt **QMS** in als de *wegzet* locatie voor het verzenden van de pallet voor verdere inspectie.

    Op de pagina **Kwaliteit in kwaliteitscontrole: Wegzetten**, die wordt weergegeven, staan details van het wegzetwerk.

    - **LOC:** *QMS*

        Deze locatie is de aangewezen wegzetlocatie voor wegens kwaliteit geweigerde ontvangst.

    - **LP:** de door het systeem gegenereerde nummerplaat-id
    - **Artikel:** *M9203*
    - **Hoeveelheid:** *1 PL: 100 stuks*

    De artikelomschrijving wordt ook weergegeven.

1. Bevestig het wegzetwerk.

    Op de pagina **Taak** voor het ontvangen van inkooporderregels wordt het bericht 'Werk voltooid' weergegeven. Het veld **Regelnummer** is beschikbaar zodat u de volgende pallet kunt ontvangen.

U hebt de kwaliteitscontrole nu voltooid en een kwaliteitsorder gemaakt voor de afgekeurde pallet. Als u de gemaakte order wilt weergeven, gaat u naar **Voorraadbeheer \> Periodieke taken \> Kwaliteitsbeheer \> Kwaliteitsorders**.

Het testen van kwaliteitsorders kan nu worden verwerkt. Kwaliteitstests worden niet behandeld in dit onderwerp.

Zie voor meer informatie over kwaliteitsbeheer [Overzicht van kwaliteitsbeheer](../inventory/enable-quality-management.md)

#### <a name="receive-pallet-3"></a>Pallet 3 ontvangen

Voor dit scenario wordt pallet 3 geaccepteerd.

1. Voer *1* in het veld **Regelnummer** in en bevestig het regelnummer.
1. Het veld **Hoeveelheid** is nu beschikbaar. Voer *1* in en bevestig de hoeveelheid.

    De pagina **Kwaliteitscontrole** wordt weergegeven. Voor deze ontvangst wordt de pallet geaccepteerd voor kwaliteit en wordt deze op een bulkwegzetlocatie weggezet.

1. Selecteer de bevestigingsknop om de kwaliteitscontrole te laten slagen.

    Op de pagina **Inkoop orders: wegzetten** staan details van het wegzetwerk.

    - **LOC:** de door het systeem vastgestelde locatie

        Deze locatie is de aangewezen wegzetlocatie voor het ontvangen van inkooporders.

    - **LP:** de door het systeem gegenereerde nummerplaat-id
    - **Artikel:** *M9203*
    - **Hoeveelheid:** *1 PL: 100 stuks*

    De artikelomschrijving wordt ook weergegeven.

1. Bevestig het wegzetwerk.

    Op de pagina **Taak** voor het ontvangen van inkooporderregels wordt het bericht 'Werk voltooid' weergegeven. Het veld **Regelnummer** is beschikbaar zodat u de volgende pallet kunt ontvangen.

1. Selecteer de menuknop (**≡**) boven aan de pagina en selecteer vervolgens in het menu de optie **Annuleren** om terug te keren naar het menu.

U kunt nu de mobiele app sluiten.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]