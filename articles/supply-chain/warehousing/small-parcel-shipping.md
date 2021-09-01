---
title: Kleine pakketten verzenden
description: Dit onderwerp bevat informatie over de functie voor verzending van kleine pakketten. Met deze functie kan Microsoft Dynamics 365 Supply Chain Management gegevens over een verpakte container naar de vervoerder verzenden en vervolgens een verzendlabel, verzendtarief en traceringsnummer terugkrijgen van die vervoerder.
author: Mirzaab
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRateEngine, TMSCarrier, CustTable, TMSShippingCarrierCustomerAccount, TMSSmallParcelShippingFeature
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-08
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: e4682674e6f61b9b75276df57afa522b29b5f052fd8a4c450c7fcfbe79654f90
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6780453"
---
# <a name="small-parcel-shipping"></a>Kleine pakketten verzenden

[!include [banner](../../includes/banner.md)]

Met de functie voor verzending van kleine pakketten kan Microsoft Dynamics 365 Supply Chain Management rechtstreeks met vervoerders communiceren door een raamwerk te bieden voor communicatie via vervoerders-API's. Deze functionaliteit is handig wanneer u afzonderlijke verkooporders verzendt via commerciële vervoerders in plaats van containerverzending of LTL-verzending (Geen volledige vrachtwagen/Less Than Truckload).

Met de functie voor verzending van kleine pakketten wordt via een speciale *tarief-engine* met uw vervoerder gecommuniceerd. Uw organisatie moet deze tarief-engine ontwikkelen in samenwerking met uw vervoerder of vervoerdershubservice. Met de tarief-engine kan Supply Chain Management gegevens over een verpakte container naar uw vervoerder verzenden en vervolgens een verzendlabel, verzendtarief en traceringsnummer terugkrijgen van die vervoerder.

Het verzendtarief dat wordt geretourneerd, wordt als een diverse toeslag aan de gekoppelde verkooporder toegevoegd. Het verzendlabel dat wordt geretourneerd, kan vervolgens automatisch worden afgedrukt met een ZPL-printer (Zebra Programming Language) en op de zending worden toegepast. De vervoerder scant dit verzendlabel wanneer de pakketten in uw magazijn worden opgehaald.

## <a name="prepare-your-system-to-support-sps"></a>Uw systeem voorbereiden op ondersteuning van verzending van kleine pakketten

Voordat u de functie voor verzending van kleine pakketten kunt gaan gebruiken, moet u deze functie in Functiebeheer inschakelen, uw tarief-engine toevoegen en de modules **Transportbeheer** en **Magazijnbeheer** instellen om deze te ondersteunen.

### <a name="turn-on-the-sps-feature"></a>De functie voor verzending van kleine pakketten inschakelen

Voordat u deze functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen gebruikmaken van het werkgebied [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en de functie desgewenst in te schakelen. De functie wordt daar op de volgende manier weergegeven:

- **Module:** *Transportbeheer*
- **Functienaam:** *Verzending van kleine pakketten*

### <a name="deploy-and-set-up-rate-engines"></a>Tarief-engines implementeren en instellen

Supply Chain Management bevat geen tarief-engines. U moet zoveel tarief-engines verkrijgen of maken die u nodig hebt, en ze vervolgens aan uw systeem toevoegen. Microsoft bevat echter een demonstratietarief-engine die u kunt gebruiken voor testen.

#### <a name="download-and-deploy-the-demo-rate-engine"></a>De demonstratietarief-engine downloaden en implementeren

Voer de volgende stappen uit om de demonstratietarief-engine op te halen.

1. Download in GitHub de [DLL (Dynamic-Link Library) voor de demonstratietarief-engine](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS).
1. Sla de DLL op uw Supply Chain Management-server op in de map **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin**.

#### <a name="create-and-deploy-functional-rate-engines"></a>Functionele tarief-engines maken en implementeren

Zie de volgende onderwerpen voor informatie over het maken en implementeren van functionele tarief-engines zodat deze kunnen worden gebruikt in een productie- of testomgeving:

- [Een nieuwe transportbeheerengine maken](../transportation/create-new-transportation-management-engine.md)
- [Engines voor transportbeheer instellen](/dynamicsax-2012/appuser-itpro/set-up-transportation-management-engines)

Zie het volgende blogbericht: [Verzending van kleine pakketten: de functie voor verzending van kleine pakketten gebruiken in Microsoft Dynamics 365](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5) voor meer informatie over het maken van een tarief-engine voor verzending van kleine pakketten.

#### <a name="set-up-a-rate-engine-in-supply-chain-management"></a>Een tarief-engine instellen in Supply Chain Management

Nadat u een tarief-engine voor verzending van kleine pakketten hebt gemaakt en geïmplementeerd, voert u de volgende stappen uit om deze in te stellen.

1. Ga naar **Transportbeheer \> Instellingen \> Engines \> Tarief-engine**.
1. Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster.
1. Stel in de nieuwe rij de volgende velden in.

    - **Tarief-engine**: voer een unieke naam voor de tarief-engine in. Als u de demonstratietarief-engine gebruikt, voert u *Demonstratie-tariefengine* in.
    - **Naam**: voer een korte omschrijving van de tarief-engine in. Als u de demonstratietarief-engine gebruikt, voert u *Demonstratie-tariefengine* in.
    - **Id metagegevens beoordeling**: selecteer de basis die moet worden gebruikt om uw tarief te berekenen. Uw tarief kan bijvoorbeeld worden berekend op basis van afstand. Als u de demonstratietarief-engine gebruikt, kunt u dit veld leeg laten.
    - **Engine-assembly**: voer de bestandsnaam in van het DLL-pakket dat u hebt geïmplementeerd. Als u de demonstratietarief-engine gebruikt, voert u *TMSSmallParcelShippingEngine.dll* in.
    - **Engine-klasse**: voer de klassenaam in die voor uw tarief-engine is vastgelegd. Als u de demonstratietarief-engine gebruikt, voert u *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine* in.

## <a name="example-scenario"></a>Voorbeeldscenario

In dit voorbeeldscenario wordt getoond hoe u de functie voor verzending van kleine pakketten kunt instellen en gebruiken nadat u het systeem hebt voorbereid, zoals eerder in dit onderwerp is beschreven. Dit scenario gebruikt de eerder genoemde demonstratietarief-engine.

### <a name="make-demo-data-available"></a>Demogegevens beschikbaar maken

Als u dit scenario wilt doorlopen met de hier opgegeven demorecords en -waarden, moet u een systeem gebruiken waarop de standaard [demogegevens](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) zijn geïnstalleerd. U moet daarnaast ook de rechtspersoon **USMF** selecteren voordat u begint.

### <a name="set-up-the-scenario"></a>Het scenario configureren

Voor dit voorbeeldscenario moet u een vervoerder, vervoerdersgroep, verpakkingsbeleid en verpakkingsprofiel hebben. In de volgende subsecties wordt uitgelegd hoe u de vereiste records voor het scenario voorbereidt. In een productiescenario lijkt het instellingsproces meestal op het proces dat hier wordt beschreven. U stelt echter andere waarden in.

#### <a name="set-up-carriers"></a>Vervoerders instellen

Voer de volgende stappen uit om een vervoerder in te stellen.

1. Ga naar **Transportbeheer \> Instellingen \> Vervoerders \> Vervoerders**.
1. Selecteer **Nieuw** in het actievenster om een vervoerder toe te voegen.
1. Stel in de koptekst de volgende waarden in:

    - **Vervoerder:** *Demovervoerder*
    - **Naam:** *Demovervoerder*
    - **Methode:** *Grond*

1. Stel op het sneltabblad **Overzicht** de volgende waarden in:

    - **Vervoerder activeren:** *Ja*
    - **Beoordeling vervoerder activeren:** *Ja*

1. Selecteer op het sneltabblad **Services** **Nieuw** om een service toe te voegen aan het raster.
1. Stel de volgende waarden voor de nieuwe service in:

    - **Vervoerdersservice:** *Demovervoerdersservice*
    - **Naam:** *Demovervoerdersservice*
    - **Transportmethode:** *Grond*

    Voer indien nodig willekeurige waarden in voor alle andere velden. (Wanneer u de nieuwe vervoerdersrecord opslaat, wordt een nieuwe leveringsmethode gemaakt en wordt het veld **Leveringsmethode** automatisch ingesteld.)

1. Selecteer op het sneltabblad **Beoordelingsprofielen** de optie **Nieuw** om een beoordelingsprofiel aan het raster toe te voegen.
1. Stel de volgende waarden voor het nieuwe profiel in:

    - **Beoordelingsprofiel:** *Demovervoerdersservice*
    - **Naam:** *Demovervoerdersservice*
    - **Tarief-engine:** *Demonstratietarief-engine*

    Voer indien nodig willekeurige waarden in voor alle andere velden.

1. Selecteer **Opslaan** in het actievenster.

Zie [Vervoerders instellen](../transportation/tasks/set-up-shipping-carriers.md) voor meer informatie over het instellen van vervoerders.

#### <a name="set-up-carrier-service-accounts"></a>Serviceaccounts voor vervoerders instellen

Voer de volgende stappen uit om een serviceaccount voor vervoerders in te stellen.

1. Ga naar **Transportbeheer \> Instellingen \> Beoordeling \> Serviceaccount voor vervoerder**.
1. Selecteer in het actievenster de optie **Nieuw** om een serviceaccount voor vervoerders toe te voegen.
1. Stel de volgende waarden voor de nieuwe account in:

    - **Vervoerder:** *Demovervoerder*
    - **Vervoerdersservice:** *Demovervoerdersservice*
    - **Klantrekeningnummer vervoerder**: het klantrekeningnummer vervoerder dat wordt gebruikt om de verbinding met de vervoerder te controleren en te verifiëren. Deze waarde wordt door uw vervoerder verstrekt. Als u de demonstratieservice gebruikt, kunt u een willekeurige waarde invoeren.
    - **Locatie:** *6*
    - **Magazijn:** *62*

    > [!NOTE]
    > Vaak is de waarde van **Klantrekeningnummer vervoerder** de enige waarde die nodig is om de verbinding te verifiëren. Als uw vervoerder echter extra verificatieparameters vereist, moet uw organisatie deze pagina aanpassen om indien nodig extra velden toe te voegen.

#### <a name="set-up-a-container-packing-policy"></a>Inpakbeleid voor containers instellen

Voer de volgende stappen uit om een inpakbeleid voor containers in te stellen.

1. Als u nog geen ZPL-printerdefinitie hebt ingesteld, gebruikt u de toepassing Documentrouteringsagent om deze in te stellen. Zie [Overzicht van Documenten afdrukken](../../fin-ops-core/dev-itpro/analytics/print-documents.md) en gerelateerde onderwerpen voor meer informatie.
1. Ga naar **Magazijnbeheer \> Instellingen \> Containers \> Inpakbeleid voor container**.
1. Selecteer in het actievenster de optie **Nieuw** om een inpakbeleid voor containers toe te voegen.
1. Stel in de koptekst van het nieuwe beleid de volgende waarden in:

    - **Inpakbeleid voor container:** *Demonstratie-inpakbeleid*
    - **Beschrijving:** een omschrijving van het beleid

1. Stel op het sneltabblad **Overzicht** de volgende waarden in:

    - **Magazijn:** *62*
    - **Standaardlocatie voor uiteindelijke zending:** *laaddeur*
    - **Gewichtseenheid:** *kg*
    - **Beleid van de containerafsluiting:** *automatische vrijgave*
    - **Vrijgavebeleid voor container:** *Beschikbaar maken op uiteindelijke verzendlocatie*

1. Stel op het sneltabblad **Containermanifest** de volgende waarden in:

    - **Automatisch manifest bij sluiten van container:** *Ja*
    - **Manifestvereisten voor container:** *Transportbeheer*
    - **Containerinhoud afdrukken:** *Nee*

1. Stel op het sneltabblad **Vervoerderslabel afdrukken** de volgende waarden in:

    - **Verzendlabel container afdrukken:** *Altijd*
    - **Printernaam:** de naam van de ZPL-printer waarmee verzendlabels moeten worden afgedrukt

#### <a name="set-up-a-packing-profile"></a>Een verpakkingsprofiel instellen

Voer de volgende stappen uit om een verpakkingsprofiel in te stellen.

1. Ga naar **Magazijnbeheer \> Instellingen \> Verpakking \> Verpakkingsprofielen**.
1. Selecteer in het actievenster de optie **Nieuw** om een verpakkingsprofiel toe te voegen aan het raster.
1. Stel de volgende waarden voor het nieuwe profiel in:

    - **Verpakkingsprofiel-id:** *Demonstratieverpakkingsprofiel*
    - **Beschrijving:** een omschrijving van het profiel
    - **Inpakbeleid voor container:** *Demonstratie-inpakbeleid*
    - **Modus container-id:** *automatisch*
    - **Containertype:** *SmallBox*

#### <a name="set-up-a-customer-to-use-the-sps-carrier"></a>Een klant instellen voor gebruik van de vervoerder voor verzending van kleine pakketten

Voer de volgende stappen uit om een klant in te stellen zodat deze de vervoerder kan gebruiken die u hebt gemaakt.

1. Ga naar **Klanten \> Klanten \> Alle klanten**.
1. Zoek en selecteer klant *US-027* in het raster.
1. Selecteer in het actievenster op het tabblad **Algemeen** in de groep **Instellen** de optie **Klantrekeningen vervoerder**.
1. Selecteer in het actievenster **Nieuw** om een rekening aan het raster toe te voegen op de pagina **Klantrekeningen vervoerder**.
1. Stel de volgende waarden voor de nieuwe account in:

    - **Vervoerder:** *Demovervoerder*
    - **Klantrekeningnummer vervoerder:** *12345* (de waarde voor dit scenario is niet belangrijk, maar in de volgende sectie wordt ernaar verwezen.)

### <a name="go-through-the-example-scenario"></a>Het voorbeeldscenario doornemen

Nadat u alle voorbeeldgegevens hebt ingesteld, zoals beschreven in de vorige sectie, kunt u het voorbeeldscenario gaan gebruiken.

#### <a name="create-a-sales-order-and-process-the-work"></a>Een verkooporder maken en het werk verwerken

Voer de volgende stappen uit om een verkooporder te maken.

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
1. Selecteer **Nieuw** om een verkooporder te maken.
1. Stel in het dialoogvenster **Verkooporder maken** het veld **Klantrekening** in op de waarde *US-027*.
1. Selecteer **OK** om het dialoogvenster te sluiten en de verkooporder te maken.
1. De nieuwe verkooporder wordt geopend. Stel op het sneltabblad **Koptekst verkooporder** het veld **Klantrekeningnummer vervoerder** in op de waarde die u eerder voor deze klant hebt geselecteerd (*12345*).
1. Voeg in de sectie **Verkooporderregels** een verkoopregel toe en stel de volgende waarden voor de regel in:

    - **Artikelnummer:** *A0002*
    - **Hoeveelheid:** *1*
    - **Locatie:** *6*
    - **Magazijn:** *62*

1. Schakel over naar de weergave **Koptekst**.
1. Stel op het sneltabblad **Levering** de volgende waarden in:

    - **Vervoerder:** *Demovervoerder*
    - **Vervoerdersservice:** *Demovervoerdersservice*

1. Ga terug naar de weergave **Regels**. Als u wordt gevraagd de leveringsmethode voor de verkoopregels bij te werken, selecteert u **Ja**.
1. Selecteer in de sectie **Verkooporderregels** de orderregel die u eerder hebt ingesteld, en selecteer vervolgens **Voorraad \> Reservering**.
1. Selecteer op de pagina **Reservering** in het actievenster de optie **Partij reserveren** om de volledige hoeveelheid van de geselecteerde regel te reserveren in het magazijn.
1. Sluit de pagina **Reservering** om terug te keren naar de verkooporder.
1. Selecteer in het actievenster op het tabblad **Magazijn** de optie **Vrijgeven naar magazijn**.

    Er wordt werk gemaakt om artikelen van de orderverzamellocatie naar het inpakstation te verplaatsen.

1. Selecteer in de sectie **Verkooporderregels** **Magazijn \> Details van zending**.
1. Maak op de pagina **Details van zending** een notitie van de zendings-ID. U hebt deze nodig wanneer u de zending verpakt in het inpakstation.
1. Sluit de pagina **Details van zending** om terug te keren naar de verkooporder.
1. Maak een notitie van het verkoopordernummer en ga vervolgens naar **Magazijnbebeer \> Werk \> Alle werkzaamheden**.
1. Gebruik het verkoopordernummer om het werk te zoeken en te selecteren dat voor de order is gemaakt.
1. Selecteer in het actievenster op het tabblad **Werk** de optie **Werk voltooien**.
1. Selecteer een gebruikers-id op de pagina **Werkvoltooiing** in het veld **Gebruikers-id**. Selecteer vervolgens in het actievenster **Werk valideren**.
1. Als het werk is gevalideerd, selecteert u **Werk voltooien** in het actievenster.

    Het werk is gemarkeerd als voltooid om de verplaatsing van artikelen naar het inpakstation te simuleren.

#### <a name="pack-the-shipment"></a>De zending inpakken

Voer de volgende stappen uit om de zending in te pakken.

1. Ga naar **Magazijnbeheer \> Instellingen \> Medewerker** en zorg ervoor dat uw gebruikersaccount is gekoppeld aan een medewerkersaccount voor magazijnbeheer.
1. Ga naar **Magazijnbeheer \> Verpakking en containervorming \> Verpakken**.
1. Stel in het dialoogvenster **Inpakstation selecteren** de volgende waarden in:

    - **Locatie:** *6*
    - **Magazijn:** *62*
    - **Locatie:** *Verpakken*
    - **Verpakkingsprofiel-id:** *Demonstratieverpakkingsprofiel*

1. Selecteer **OK**.
1. De pagina **Verpakken** wordt weergegeven. In een productiescenario scant een medewerker een nummerplaat of zendings-ID. In dit scenario opent u echter de pagina **Alle zendingen** en zoekt u het zendingsnummer voor de zending die u zojuist hebt gemaakt. Voer vervolgens deze waarde in het veld **Nummerplaat of zending** in op de pagina **Verpakken**. U kunt ook de zendings-id invoeren die u eerder hebt genoteerd.
1. Selecteer **Nieuwe container** in het actievenster.
1. In het dialoogvenster dat wordt weergegeven, worden details over de nieuwe container weergegeven. Laat de standaardwaarden staan en selecteer vervolgens **OK**.
1. Selecteer *A0002* om het artikel te verpakken op de pagina **Verpakken** op het sneltabblad **Artikel verpakken** in het veld **Id**. Het artikel wordt aan de container toegevoegd.
1. Selecteer in het actievenster de optie **Containers voor zending**.

    De pagina **Containers voor zending** die wordt weergegeven, heeft een rij voor de container die u zojuist hebt gemaakt. Het veld **Containermanifest-id** in die rij is echter momenteel leeg, omdat u het verzendlabel en traceringsnummer nog niet van de vervoerder hebt ontvangen.

1. Selecteer **Container sluiten** in het actievenster.
1. Stel in het dialoogvenster **Container sluiten** het veld **Brutogewicht** in op *1 kg* en selecteer vervolgens **OK**.

    Het verzendlabel moet nu worden afgedrukt op de ZPL-printer die u eerder hebt geselecteerd. Het resultaat moet lijken op het volgende voorbeeld.

    ![Voorbeeldverzendlabel.](media/sps-label-example.png "Voorbeeldverzendlabel")

1. De waarden **Containermanifest-id** en **Totale vrachtkosten** zijn toegevoegd als ontvangen van de vervoerder.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]