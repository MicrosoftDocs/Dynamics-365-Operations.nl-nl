---
title: Put to wall - put to store
description: Dit onderwerp bevat informatie over de functionaliteit Put to wall - put to store. Met deze functie kunt u scenario's afhandelen waarin u een product moet consolideren naar een inpakvoorbereidingsruimte op basis van configureerbare criteria. Dit helpt om de orderverzameltijd te verkorten omdat orderverzamelen op één doelnummerplaat mogelijk is en meer wegzetplaatsen kunnen worden gebruikt dan bij het clusterverzamelen.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationType, WHSLocationProfile, WHSLocation, WHSPackProfile, WHSWaveStepCode, WHSOutboundSortTemplate, WHSPostMethod, WHSWaveTemplateTable, WHSLocDirTable, WHSWorkClass, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: e2dcfa18af457ea21618704bafa2ed81c615d952
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5228508"
---
# <a name="put-to-wall---put-to-store"></a>Put to wall - put to store

[!include [banner](../includes/banner.md)]

Met de functie *Put to wall - put to store* kunt u scenario's afhandelen waarin u een product moet consolideren naar een inpakvoorbereidingsruimte op basis van configureerbare criteria. Omdat deze functionaliteit orderverzamelen op één doelnummerplaat toestaat en meer wegzetposities kan gebruiken dan bij clusterverzamelen, hebben bedrijven die aan winkels leveren of kleine artikelen verwerken minder tijd nodig voor orderverzamelen.

De werkstroom voor deze functionaliteit zorgt ervoor dat het verzamelde product naar een sorteerlocatie wordt gestuurd voor distributie in verschillende containertypen. Meestal bevat elke sorteerlocatie meerdere sorteerposities. Elke sorteerpositie wordt toegewezen op basis van de criteria die zijn ingesteld door het bedrijfsproces. Standaardcriteria zijn de uiteindelijke bestemming, verzending of lading. Nadat een product is ontvangen, wordt het gedistribueerd naar elke sorteerpositie op basis van de hoeveelheid die is gekoppeld aan de order, bestemming, verzending of lading. Wanneer een container vol of volledig is, wordt deze verplaatst naar een faserings- of verzend locatie voor verdere verwerking, afhankelijk van het bedrijfsproces.

Voor deze magazijn functionaliteit wordt ook naar andere namen verwezen, zoals 'put-to-light' en 'break opens'.

## <a name="turn-on-the-outbound-sorting-feature"></a>De functie voor uitgaande sortering inschakelen

Voordat u de functie *Put to wall - put to store* gebruikt, moet de functie *Uitgaande sortering* worden ingeschakeld in uw systeem. Beheerders kunnen het werkgebied [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de status van de functie te controleren en desgewenst in te schakelen. De functie wordt daar op de volgende manier weergegeven:

- **Module:** *Magazijnbeheer*
- **Functienaam:** *Uitgaande sortering*

De functie *Uitgaande sortering* kan worden gebruikt in combinatie met de functie *Organisatiebrede wavestapcode* als deze is ingeschakeld. U moet deze functie ook inschakelen als u vooraf gedefinieerde codes wilt gebruiken die zijn ingesteld op wavestapcodes. Schakel in het werkgebied **Functiebeheer** deze functie als volgt in:

- **Module:** *Magazijnbeheer*
- **Functienaam:** *Organisatiebrede wave-stapcode*

## <a name="setup"></a>Instellen

Voor deze demo worden standaard Contoso-gegevens en magazijn *62* gebruikt. Sommige toevoegingen die verderop worden vermeld, worden ook gebruikt.

### <a name="location-type"></a>Locatietype

1. Ga naar **Magazijnbeheer \> Instellingen \> Magazijn \> Locatietypen**.
1. Selecteer in het actievenster de optie **Nieuw** om een locatietype voor sorteren te maken.
1. Stel de volgende waarden in:

    - **Locatietype:** *SORTEREN*
    - **Omschrijving:** *Sorteren*

1. Selecteer **Opslaan**.

### <a name="warehouse-management-parameters"></a>Parameters voor magazijnbeheer

1. Ga naar **Magazijnbeheer \> Instellingen \> Parameters voor magazijnbeheer**.
1. Voer op het tabblad **Algemeen** op het sneltabblad **Locatietypen** in het veld **Locatietype voor sorteren** *SORTEREN* in.
1. Selecteer **Opslaan**.

### <a name="location-profile"></a>Locatieprofiel

1. Ga naar **Magazijnbeheer \> Instellen \> Magazijn \> Locatieprofielen**.
1. Selecteer in het actievenster de optie **Nieuw** om een locatieprofiel voor de sorteerlocatie te maken.
1. Stel in de koptekst de volgende waarden in:

    - **Locatieprofiel-id:** *Sorteren*
    - **Naam:** *Sorteren*

1. Stel op het sneltabblad **Algemeen** de volgende waarden in:

    - **Locatie-indeling:** *INPAKKEN*
    - **Locatietype:** *SORTEREN*
    - **Bijhouden nummerplaat gebruiken:** *Ja*
    - **Gemengde artikelen toestaan:** *Ja*
    - **Gemengde voorraadstatussen toestaan:** *Ja*

1. Selecteer **Opslaan**.

### <a name="locations"></a>Locaties

1. Ga naar **Magazijnbeheer \> Instellingen \> Magazijn \> Locaties**.
1. Schakel het selectievakje **Controlecijfers genereren voor locatie** uit.
1. Selecteer in het actievenster **Nieuw** en stel de volgende waarden in:

    - **Magazijn:** *62*
    - **Locatie:** *Sorteren*
    - **Locatieprofiel-id:** *Sorteren*

1. Selecteer **Opslaan**.

### <a name="packing-profiles"></a>Verpakkingsprofielen

1. Ga naar **Magazijnbeheer \> Instellingen \> Verpakking \> Verpakkingsprofielen**.
1. Selecteer in het actievenster **Nieuw** en stel de volgende waarden in:

    - **Verpakkingsprofiel-id:** *Sorteren*
    - **Omschrijving:** *Sorteren*
    - **Inpakbeleid voor container:** laat dit veld leeg.
    - **Modus container-id:** *automatisch*
    - **Containertype:** *PALLET 48X48*
    - **Automatisch container maken bij sluiten van container:** laat dit veld leeg.

1. Selecteer **Opslaan**.

### <a name="wave-step-codes"></a>Wave-stapcodes

Als u de functie *Organisatiebrede wavestapcode* hebt ingeschakeld, stelt u de volgende code in.

1. Ga naar **Magazijnbeheer \> Instellen \> Waves \> Wavestapcodes**.
1. Selecteer in het actievenster **Nieuw** en stel de volgende waarden in:

    - **Wavestapcode:** *Sorteren*
    - **Beschrijving wavestap:** *Sorteren*
    - **Type wavestap:** *Sorteersjabloon*

1. Selecteer **Opslaan**.

### <a name="outbound-sorting-template"></a>Uitgaande sorteersjabloon

De sorteersjabloon bepaalt of er sorteerposities worden gemaakt, welke criteria worden gebruikt en andere kenmerken van het sorteerproces.

1. Ga naar **Magazijnbeheer \> Instellingen \> Verpakking \> Uitgaande sorteersjabloon**.
1. Selecteer in het actievenster **Nieuw** om een sorteersjabloon te maken.
1. Stel in de koptekst van de nieuwe sjabloon de volgende waarden in:

    - **Id van uitgaande sorteersjabloon:** *Wave sorteren*
    - **Beschrijving:** *Wave sorteren*
    - **Sorteersjabloontype:** *Wavevraag*

        Dit veld bepaalt het proces waarvoor de sorteersjabloon wordt gebruikt. De volgende waarden zijn beschikbaar:

        - **Wavevraag**: de sorteersjabloon wordt gebruikt voor het proces *Put to wall*. Dit sjabloontype wordt gebruikt om de verpakkingsplaats over te slaan en de voorraad rechtstreeks uit de wave te verwerken. U kunt dit type alleen gebruiken als de **sorteermethode** van het waveproces wordt opgenomen in de wavesjabloon.
        - **Container**: de sorteersjabloon wordt gebruikt voor het proces *Pallet opbouwen na verpakking*. Dit sjabloontype wordt gebruikt voor het verwerken van containers die worden gesloten op de verpakkingsplaats en moeten worden gesorteerd op pallets.

    - **Magazijn:** *62*
    - **Locatie:** *Sorteren*

1. Stel op het sneltabblad **Algemeen** de volgende waarden in:

    - **Verificatie sorteren:** *Positie scannen*

        In dit veld wordt de verificatie gedefinieerd die is vereist tijdens het sorteren. De volgende waarden zijn beschikbaar:

        - None
        - Nummerplaat scannen
        - Positie scannen

    - **Werk maken bij positie sluiten:** *Ja*

        Als deze optie wordt ingesteld op *Ja*, wordt werk gemaakt wanneer de positie is gesloten om voorraad te verplaatsen naar de definitieve verzendlocatie. Als dit wordt ingesteld op *Nee*, wordt voorraad onmiddellijk verzameld op de order wanneer de positie wordt gesloten.

    - **Positietoewijzing:** *Handmatig*

        In dit veld wordt het type positietoewijzing gedefinieerd. De volgende waarden zijn beschikbaar:

        - **Handmatig**: de gebruiker moet altijd aangeven op welke positie de voorraad moet worden gesorteerd.
        - **Automatisch**: het systeem wijst de voorraad automatisch toe aan een positie, indien mogelijk op basis van de opsplitsingen in de sorteersjablonen.

    - **Criteria voor sorteerpositie toewijzen:** *alleen lege positie gebruiken*

        Met dit veld wordt bepaald of rekening wordt gehouden met voorraad die al aanwezig is op sorteerposities bij het toewijzen van een positie voor de vraag. De volgende waarden zijn beschikbaar:

        - **Alleen lege positie gebruiken**: er wordt rekening gehouden met posities waaraan al voorraad is gekoppeld
        - **Aannemen dat positie leeg is**: alle voorraad die al op de positie staat, wordt tijdens de toewijzing genegeerd. Alle beschikbare posities worden gebruikt.

    - **Wavestapcode:** *Sorteren*

        Als de functie *Organisatiebrede wave-stapcode* is ingeschakeld, moet de wavestapcode *Sorteren* ook worden ingesteld in wavestapcodes.

    - **Sorteerpositie automatisch sluiten:** *Ja*

        Wanneer deze optie is ingesteld op *Ja*, wordt de sorteerpositie automatisch gesloten wanneer alle werk voor de positie is voltooid.

    - **Aantal sorteerposities:** *3*

        Dit veld bepaalt het maximumaantal sorteerposities dat door het systeem wordt gemaakt.

    - **Voorvoegsel sorteerpositie:** *SP-*

        Dit veld definieert het voorvoegsel dat het systeem vóór het positienummer toewijst.

    - **Sorteerpositie automatisch inpakken:** *Ja*

        Als deze optie wordt ingesteld op *Ja*, wordt de voorraad op de sorteerpositie in een container verpakt wanneer de positie wordt afgesloten.

    - **Verpakkingsprofiel-id:** *Sorteren*

        In dit veld wordt het verpakkingsprofiel bepaald dat wordt gebruikt wanneer de sorteerpositie in een container wordt verpakt.

1. Selecteer in het actievenster **Query bewerken** om de criteria op te geven die worden gebruikt voor deze sorteersjabloon.
1. Selecteer in het querydialoogvenster op het tabblad **Sorteren** de optie **Nieuw** om een regel toe te voegen en stel vervolgens de volgende waarden in:

    - **Tabel:** *Gegevens lading*
    - **Afgeleide tabel:** *Gegevens lading*
    - **Veld:** *Zending-id*
    - **Zoekrichting:** *Oplopend*

1. Selecteer **OK**.
1. Het volgende bericht kan worden weergegeven: 'Groeperen wordt opnieuw ingesteld, doorgaan?' Selecteer **Ja**.

    De knop **Onderbrekingen van sjabloon uitgaande sortering** in het actievenster wordt beschikbaar.

1. Selecteer in het actievenster **Onderbrekingen van sjabloon uitgaande sortering**.
1. Schakel het selectievakje **Groeperen op-veld** in om te groeperen op zending-id.

    Met deze instelling wordt één sorteerpositie gemaakt per zending die een container in de wave is.

1. Selecteer **OK**.

### <a name="wave-process-methods"></a>Methoden voor verwerking van waves

1. Ga naar **Magazijnbeheer \> Instellen \> Waves \> Methoden voor verwerking van waves**.
1. Selecteer in het actievenster **Methoden opnieuw genereren**.

    De **sorteer** methode wordt toegevoegd aan de lijst met beschikbare methoden en het sjabloontype *Zending* voor de wave wordt hiervoor geselecteerd.

### <a name="wave-templates"></a>Wavesjablonen

Bewerk de wavesjabloon die wordt gebruikt voor het sorteren van de wavevraag.

1. Ga naar **Magazijnbeheer \> Instellen \> Waves \> Wavesjablonen**.
1. Selecteer in het veld **Type wavesjabloon** de optie *Zending*.
1. Selecteer de bestaande standaardsjabloon **62 zending**.
1. Selecteer **Bewerken** in het actievenster.
1. Breng op het sneltabblad **Algemeen** de volgende wijzigingen aan:

    - Stel de optie **Wave verwerken bij vrijgave door magazijn** in op *Nee*.
    - Stel de optie **Toewijzen aan open waves** in op *Ja*.

1. Stel op het sneltabblad **Methoden** de **sorteermethode** in:

    1. Selecteer **Sorteren** in het raster **Resterende methoden**.
    2. Selecteer de knop pijl-rechts om de methode **sorteren** te verplaatsen naar het raster **Geselecteerde methoden**.
    3. Selecteer **Sorteren** in het raster **Geselecteerde methoden**.
    4. Stel het veld **Wavestapcode** in op *Sorteren*.

1. Selecteer **Opslaan**.

### <a name="mobile-device-menu-items"></a>Menuopties voor mobiel apparaat

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.
1. Selecteer **Nieuw** in het actievenster.
1. Stel in de koptekst de volgende waarden in:

    - **Naam menuopdracht:** *Sorteren*
    - **Titel:** *Sorteren*
    - **Modus:** *Indirect*
    - **Bestaand werk gebruiken:** *Nee*

1. Stel op het sneltabblad **Algemeen** de volgende waarden in:

    - **Activiteitscode:** *uitgaande sortering*
    - **Verwerkingsinstructies gebruiken:** *Ja* (standaardwaarde)
    - **Id van uitgaande sorteersjabloon:** *Wave sorteren*

1. Selecteer **Opslaan**.

### <a name="mobile-device-menu"></a>Menu voor mobiel apparaat

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menu voor mobiel apparaat**.
1. Selecteer in de lijst met menu's de waarde **Uitgaand**.
1. Selecteer **Bewerken** in het actievenster.
1. Zoek in het raster **Beschikbare menu's en menuopdrachten** de menuopdracht **Sorteren** die u zojuist hebt gemaakt.
1. Selecteer de knop pijl-rechts om **Sorteren** naar het raster **Menustructuur** te verplaatsen. Op deze manier voegt u de menuopdracht toe aan het menu **Uitgaand**.
1. Selecteer **Opslaan**.

### <a name="location-directives"></a>Locatie-instructies

U moet locatie-instructies maken om het werk te begeleiden dat wordt gemaakt nadat de sortering is voltooid.

1. Ga naar **Magazijnbeheer \> Instellen \> Locatierichtlijnen**.
1. Selecteer *Inkooporders* in het veld **Orderverzameling van gesorteerde voorraad**.
1. Selecteer **Nieuw** in het actievenster.
1. Stel in de koptekst de volgende waarden in:

    - **Reeks:** *1*
    - **Naam:** *Wegzetten naar laaddeur*

1. Stel op het sneltabblad **Locatierichtlijnen** de volgende waarden in:

    - **Werktype:** *Wegzetten*
    - **Locatie:** *6*
    - **Magazijn:** *62*
    - **Instructiecode:** Laat dit veld leeg.
    - **Meerdere SKU's:** *Nee*

1. Selecteer **Opslaan** om het sneltabblad **Regels** beschikbaar te maken.
1. Selecteer **Nieuw** op het sneltabblad **Regels** en stel de volgende waarden in. Accepteer de standaardwaarden voor alle overige velden.

    - **Volgnummer:** *1*
    - **Vanaf hoeveelheid:** *0*
    - **Tot hoeveelheid:** *1000000*

1. Selecteer **Opslaan** om het sneltabblad **Locatie-instructieacties** beschikbaar te maken.
1. Selecteer **Nieuw** op het sneltabblad **Locatie-instructieacties** en stel de volgende waarden in. Accepteer de standaardwaarden voor alle overige velden.

    - **Volgnummer:** *1*
    - **Naam:** *Laaddeur*

1. Selecteer **Opslaan** om de knop **Query bewerken** op het sneltabblad **Locatie-instructieacties** beschikbaar te maken.
1. Selecteer op het sneltabblad **Locatie-instructieacties** de optie **Query bewerken**.
1. Zoek in het querydialoogvenster op het tabblad **Bereik** de rij waar het veld **Veld** is ingesteld op *Locatie*. Stel het veld **Criteria** voor deze rij in op *Laaddeur*.
1. Selecteer **OK** om de bewerking te bevestigen.

### <a name="work-classes"></a>Werkklassen

1. Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werkklassen**.
1. Selecteer **Nieuw** in het actievenster.
1. Stel in de koptekst de volgende waarden in:

    - **Werkklasse-id:** *Sorteren*
    - **Omschrijving:** *Sorteren*
    - **Type werkorder:** *Orderverzameling van gesorteerde voorraad*

1. Selecteer **Opslaan**.

### <a name="work-templates"></a>Werksjablonen

1. Ga naar **Magazijnbeheer \> Werk \> Werksjablonen**.
1. Selecteer *Verkooporders* in het veld **Werkordertype**.
1. Selecteer in het raster de werksjabloon **62 Orderverzamelen voor inpakken**.
1. Selecteer **Opsplitsingen voor werkkoptekst** in het actievenster.
1. Selecteer **Bewerken** in het actievenster.
1. Schakel op de regel waarvoor het veld **Veldnaam** is ingesteld op *Zending-id* het selectievakje **Groeperen op dit veld** uit.
1. Selecteer **Opslaan** en sluit het dialoogvenster **Opsplitsingen voor werkkoptekst**.
1. Selecteer *Inkooporders* in het veld **Orderverzameling van gesorteerde voorraad**.
1. Selecteer **Nieuw** om een werksjabloon te maken.
1. Stel op de sectie **Overzicht** de volgende waarden in. Accepteer de standaardwaarden voor alle overige velden.

    - **Werksjabloon:** *Orderverzameling gesorteerd*
    - **Beschrijving werksjabloon:** *Orderverzameling gesorteerd*

1. Selecteer **Opslaan** om de sectie **Werksjabloongegevens** beschikbaar te maken.
1. Maak in de sectie **Details van werksjabloon** twee regels. Selecteer **Nieuw** en stel de volgende waarden voor regel 1 in:

    - **Werktype:** *Orderverzamelen*
    - **Verplicht:** geselecteerd (= *Ja*)
    - **Werkklasse-id:** *Sorteren*

1. Selecteer nogmaals **Nieuw** en stel de volgende waarden voor regel 2 in:

    - **Werktype:** *Wegzetten*
    - **Verplicht:** geselecteerd (= *Ja*)
    - **Werkklasse-id:** *Sorteren*

1. Selecteer **Opslaan**.

## <a name="example-scenario"></a>Voorbeeldscenario

In dit scenario wordt een situatie gesimuleerd waarbij in het magazijn kleine artikelen op locaties worden opgeslagen die moeten worden ingepakt in dozen voordat ze worden verzonden, en waarbij de functionaliteit van het verpakkingsstation niet echt geschikt is. Werknemers verzamelen orders voor meerdere klanten en verschillende adressen tegelijk om de verzamelsnelheid te verhogen. Nadat het orderverzamelen is voltooid, arriveren de werknemers op de sorteerlocatie, waar de verzamelde artikelen kunnen worden gesorteerd in de juiste doos op basis van vereiste criteria. In dit voorbeeld wordt de zending-id gebruikt om de juiste doos te bepalen, omdat elke zending een ander adres heeft. Nadat alle artikelen van de lading zijn ingepakt en gesorteerd op zending, worden de dozen verplaatst naar het klaarzetgebied en uiteindelijk op een truck geladen.

Controleer voordat u het scenario start of alle standaard magazijnfuncties juist zijn ingesteld voor het magazijn. Standaard wordt het Contoso-magazijn *62* gebruikt voor dit doeleinde. Standaardconfiguraties zijn niet gewijzigd, behalve wat in de instellingen is beschreven.

### <a name="create-demand"></a>Vraag maken

Voordat u de functionaliteit kunt demonstreren, moet u een bepaalde vraag maken. Voor dit scenario maakt u drie verkooporders voor drie verschillende klanten om verschillende afleveradressen te simuleren. Op deze manier maakt u drie afzonderlijke zendingen.

Voordat u verkooprders en zendingen maakt, moet u er ook voor zorgen dat de orderverzamellocaties voldoende voorraad hebben voor alle artikelen op de orders. Controleer de instellingen voor de locatie-instructie om de orderverzamellocaties te bevestigen worden gebruikt voor het verzamelen van verkooporders. Als u de voorraad moet corrigeren, kunt u handmatige verplaatsingen maken en aanvulling of elke andere stroom gebruiken. Reserveer vervolgens de voorraad.

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
1. Selecteer **Nieuw** om een verkooporder voor order 1 te maken.
1. Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:

    - **Klant:** *US-001*
    - **Magazijn:** *62*

1. Selecteer **OK**.
1. Een nieuwe regel wordt toegevoegd aan het raster op het sneltabblad **Verkooporderregels**. Stel de volgende waarden in:

    - **Artikelnummer:** *A0001*
    - **Hoeveelheid:** *5*

1. Selecteer **Regel toevoegen** om een tweede regel toe te voegen en stel de volgende waarden in:

    - **Artikelnummer:** *A0002*
    - **Hoeveelheid:** *10*

1. Herhaal de volgende stappen voor elke verkoopregel op de order om de voorraad te reserveren:

    1. Selecteer op het sneltabblad **Verkooporderregels** in het menu **Voorraad** boven het raster de waarde **Reservering**.
    1. Ga naar de pagina **Reservering** en selecteer de optie **Partij reserveren** en sluit de pagina vervolgens.
    1. Selecteer **Opslaan**.

1. Selecteer **Nieuw** om een verkooporder voor order 2 te maken.
1. Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:

    - **Klant:** *US-004*
    - **Magazijn:** *62*

1. Selecteer **OK**.
1. Een nieuwe regel wordt toegevoegd aan het raster op het sneltabblad **Verkooporderregels**. Stel de volgende waarden in:

    - **Artikelnummer:** *A0001*
    - **Hoeveelheid:** *7*

1. Selecteer **Regel toevoegen** om een tweede regel toe te voegen en stel de volgende waarden in:

    - **Artikelnummer:** *A0002*
    - **Hoeveelheid:** *3*

1. Herhaal de volgende stappen voor elke verkoopregel op de order om de voorraad te reserveren:

    1. Selecteer op het sneltabblad **Verkooporderregels** in het menu **Voorraad** boven het raster de waarde **Reservering**.
    1. Ga naar de pagina **Reservering** en selecteer de optie **Partij reserveren** en sluit de pagina vervolgens.
    1. Selecteer **Opslaan**.

1. Selecteer **Nieuw** om een verkooporder voor order 3 te maken.
1. Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:

    - **Klant:** *US-007*
    - **Magazijn:** *62*

1. Selecteer **OK**.
1. Een nieuwe regel wordt toegevoegd aan het raster op het sneltabblad **Verkooporderregels**. Stel de volgende waarden in:

    - **Artikelnummer:** *A0001*
    - **Hoeveelheid:** *8*

1. Om voorraad te reserveren voor een verkoopregel, voert u de volgende stappen uit:

    1. Selecteer op het sneltabblad **Verkooporderregels** in het menu **Voorraad** boven het raster de waarde **Reservering**.
    1. Ga naar de pagina **Reservering** en selecteer de optie **Partij reserveren** en sluit de pagina vervolgens.
    1. Selecteer **Opslaan**.

Voer de volgende procedure uit om elke verkooporder vrij te geven in het magazijn. Er worden drie verschillende zendingen gemaakt. Vervolgens voegt u de drie zendingen toe aan één nieuwe wave.

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
1. Selecteer in het raster de eerste verkooporder die u hebt gemaakt.
1. Selecteer in het actievenster op het tabblad **Magazijn** de optie **Vrijgeven naar magazijn**.

    U ontvangt een informatieve melding waarin de wave-id en zending-id worden vermeld die zijn gemaakt.

1. Herhaal de vorige stappen om verkooporders 2 en 3 aan het magazijn vrij te geven. Het informatiebericht dat u ontvangt, geeft aan dat er een zending is toegevoegd aan de wave die is gemaakt bij het vrijgegeven van verkooporder 1.
1. Ga naar **Magazijnbeheer \> Uitgaande waves \> Zendingwaves \> Alle waves**.
1. Selecteer de wave-id die is gemaakt op basis van de vrijgegeven verkooporders om de pagina **Waves** te openen. Op deze pagina worden de wavegegevens weergegeven. Op het sneltabblad **Waveregels** worden de zendingen weergegeven die zijn gemaakt.

    U moet nu werk maken om artikelen van de orderverzamellocaties naar de sorteerlocatie te brengen.

1. Selecteer **Verwerken** in het actievenster.

    Tijdens de waveverwerking gebruikt de sorteermethode de sorteersjabloon om de voorraad toe te wijzen voor de sorteerposities. Wanneer de waveverwerking is voltooid, ontvangt u een bericht om aan te geven dat de wave is geboekt en het werk is gemaakt.

1. Selecteer in het actievenster op het tabblad **Wave** in de groep **Verwante informatie** de optie **Werk** om het gemaakte werk weer te geven. Noteer de werk-id.
1. Ga naar **Magazijnbeheer \> Verpakking en containervorming \> Toewijzingen uitgaande sorteerpositie**.
1. In de linkerkolom kunt u de uitgaande sorteerpositie weergeven die voor elke zending is gemaakt.
1. Op het sneltabblad **Criteria sorteerpositie** kunt u de zending-id voor die positie weergeven.

Er is één werk-id gemaakt om voorraad van de orderverzamellocaties naar de sorteerlocatie te brengen. Als u het werk wilt voltooien, hebt u de werk-id nodig die tijdens de waveverwerking is gemaakt.

### <a name="sales-order-picking-to-the-sorting-location"></a>Orderverzameling van verkooporders naar de sorteerlocatie

1. Meld u aan bij de mobiele app als een medewerker in magazijn *62*.
1. Selecteer **Uitgaand** in het hoofdmenu.
1. Selecteer **Orderverzamelen** in het menu **Uitgaand**.
1. Selecteer het veld **Id** en voer de werk-id van de waveverwerking in.
1. Bevestig uw invoer.

    Vervolgens wordt u gevraagd om een doelnummerplaat in te voeren. U ziet dat regel 1 van verkooporder 1 moet worden opgenomen en toegevoegd aan de doelnummerplaat. Het artikelnummer, de hoeveelheid, de artikelomschrijving en de verzamellocatie worden weergegeven.

1. Voer in het veld **Doel-LP** het nummer van de nummerplaat in.

    U gaat alle regels verzamelen die van de verwerkte wave op dezelfde doelnummerplaat zijn gemaakt.

1. Bevestig uw invoer.

    In de mobiele app wordt nu een reeks pagina's met **pickinstructies** weergegeven over de orderverzamellocatie, en het artikel en de hoeveelheid die moeten worden verzameld. Nadat het verzamelde artikel aan de nummerplaat is toegevoegd, bevestigt u het pickaantal. De laatste pagina geeft het werk aan om de verzamelde artikelen op de sorteerlocatie te plaatsen.

1. Bevestig de eerste orderverzameling.
1. De volgende orderverzameling wordt weergegeven. Bevestig de orderverzameling.
1. Ga door met het bevestigen van de resterende orderverzamelingen.
1. De laatste stap is het voltooien van de wegzetwerkzaamheden. Bevestig de opslag naar de sorteerlocatie.

    U ziet de melding "Werk voltooid".

1. Sluit **Orderverzamelen** in de mobiele app af.

### <a name="sortingput-to-wall"></a>Sortering/put-to-wall

Nu alle voorraad op de sorteerlocatie is geplaatst, moet deze worden gesorteerd op de juiste sorteerpositie.

1. Meld u aan bij de mobiele app.
1. Selecteer **Uitgaand** in het hoofdmenu.
1. Selecteer in het menu **Uitgaand** de optie **Sorteren** om de artikelen te gaan sorteren.
1. Voer in het veld **LP/CON** de doelnummerplaat in van de verzamelde verkooporder.
1. Bevestig uw invoer.
1. Voer het artikelnummer in dat u als eerste wilt sorteren.
1. Het systeem bepaalt de eerste sorteerpositie die moet worden weergegeven. Bevestig de sorteerpositie.
1. U wordt gevraagd een nummerplaat aan de sorteerpositie toe te wijzen. Selecteer het veld **LP**, voer een nummer voor de nummerplaat in en bevestig uw invoer.

    Omdat de sorteerpositie is gerelateerd aan de zending-id, kunt u de verzamelde artikelen op een nummerplaat sorteren die specifiek is voor de uitgaande zending en verkooporder.

    Op de volgende pagina worden de artikel-id, de hoeveelheid, de sorteerpositie-id en de nummerplaat-id's 'vanaf' (orderverzamelen) en 'naar' (sorteren) weergegeven. De informatie op deze pagina geeft aan dat u het opgegeven artikel en de hoeveelheden van de nummerplaat voor orderverzamelen te sorteren naar de nummerplaat voor het sorteren.

1. Bevestig de sorteerpositie.
1. Sorteer de artikelen op de eerste sorteerpositie. Wanneer u klaar bent, leidt het systeem u naar de volgende sorteerpositie.
1. Herhaal deze procedure voor alle verzamelde regels op de werkorder. U moet dit proces ook gebruiken als er meerdere pickregels met hetzelfde artikelnummer zijn.

    Wanneer u dit proces voor alle artikelen herhaalt, evalueert het systeem de criteria van het volgende gescande artikel (werkregel) en wordt bepaald op welke sorteerpositie het moet worden geplaatst. U wordt automatisch doorverwezen om het artikel op de juiste sorteerpositie te plaatsen. Afhankelijk van de bevestigingsinstellingen wordt u ook gevraagd om deze actie te bevestigen door het positienummer of de nummerplaat-id in te voeren.

    > [!NOTE]
    > Als automatische sortering is ingeschakeld, is handmatig overschrijven niet beschikbaar.

1. Wanneer u klaar bent, opent u in Microsoft Dynamics 365 Supply Chain Management de pagina **Toewijzingen voor uitgaande sorteerposities** om de status van de posities te controleren.

    - Als posities automatisch worden gesloten, selecteert u **Gesloten weergeven** om de gesloten posities weer te geven.
    - U ziet dat de transacties van de sorteerpositie worden weergegeven. Het artikel en de hoeveelheid die via de positie zijn verwerkt, worden weergegeven.

    Wanneer u de sjabloon voor uitgaande sorteervolgorde instelt, stelt u de optie **Sorteerpositie automatisch sluiten** in op *Ja*. Daarom wordt de positie automatisch gesloten wanneer de laatste verwachte voorraad is geplaatst. De sorteerposities hebben de status **Gesloten** en werk is gemaakt om de gesorteerde voorraad naar de locatie *Laaddeur* te verplaatsen.

1. Voltooi de gesorteerde voorraadpicks om de voorraad naar de verzendlocatie te verplaatsen. Wanneer de voorraad gereed is, moet u de verzending bevestigen.

> [!NOTE]
> Voor een correcte verwerking van gesorteerde voorraadpicks kan een menuopdracht van het mobiele apparaat met een werkklasse-id waarvoor het veld **Werkordertype** is ingesteld op *Gesorteerde voorraadverzameling*, worden gebruikt voor het verplaats- en laadproces.

### <a name="manually-close-a-position-optional"></a>Handmatig een positie sluiten (optioneel)

Als de sorteerposities handmatig moeten worden gesloten, moet de optie **Sorteerpositie automatisch sluiten** voor de uitgaande sorteersjabloon zijn ingesteld op *Nee* en moet er worden afgesloten voordat de voorraad kan worden verplaatst naar het laaddeurgebied. Posities kunnen op verschillende manieren worden gesloten:

- Via de magazijnapp:

    - De gebruiker kan een van de artikelen scannen die zich al op de positie bevinden en vervolgens **Sluiten** selecteren om de positie te sluiten.
    - Als de gebruiker een container scant die al is gesorteerd, wordt een foutbericht weergegeven. De gebruiker kan echter wel doorgaan met het sluiten van de positie.

- Op de pagina Microsoft Dynamics 365 Supply Chain Management **Toewijzingen voor uitgaande sorteerposities**:

    - De gebruiker kan de uitgaande positierecord selecteren en vervolgens **Positie sluiten** selecteren in het actievenster.

## <a name="tips"></a>Tips

- Artikelen kunnen niet worden verplaatst tussen posities nadat ze aan een positie zijn toegewezen. Het systeem evalueert hoeveel van elk artikel naar een bepaalde positie moet gaan.
- Sorteersjablonen kunnen zo worden geconfigureerd dat er automatisch containers worden gemaakt wanneer posities worden gesloten. Met deze aanpak wordt een standaardstructuur met container-id's gemaakt die is gebaseerd op het opgegeven verpakkingsprofiel.

> [!IMPORTANT]
> Nadat de verplaatsingswerkzaamheden zijn gemaakt op basis van de sorteerlocatie, moet u het werk niet annuleren. Anders worden de positie en de containers uit het systeem verwijderd en zijn ze niet beschikbaar voor verdere verwerking. De voorraad wordt ook verwijderd.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]