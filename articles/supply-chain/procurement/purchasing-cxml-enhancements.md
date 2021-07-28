---
title: Inkoop-cXML-verbeteringen
description: De functie Inkoop-cXML-verbeteringen maakt gebruik van de bestaande externe-catalogusfunctionaliteit, PunchOut, die wordt gebruikt voor opdrachten tot inkoop.
author: dasani-madipalli
ms.date: 08/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatCXMLParameters, CatCXMLPurchRequest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-08-03
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: b579ebff28e01caa727a22b01ae636ff713a27aa
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359952"
---
# <a name="purchasing-cxml-enhancements"></a>Inkoop-cXML-verbeteringen

[!include [banner](../includes/banner.md)]

De functie _Inkoop-cXML-verbeteringen_ maakt gebruik van de [bestaande externe-catalogusfunctionaliteit](set-up-external-catalog-for-punchout.md) die wordt gebruikt voor opdrachten tot inkoop. Deze bestaande functionaliteit wordt ook wel _PunchOut_ genoemd. Hoewel een inkooporder niet afkomstig hoeft te zijn van een opdracht tot inkoop, moet er een koppeling zijn tussen de leverancier op een inkooporder en de parameters die worden gebruikt om het inkooporderdocument te verzenden.

## <a name="turn-on-the-purchasing-cxml-enhancements-feature"></a>De functie Inkoop-cXML-verbeteringen inschakelen

Als u de functie wilt inschakelen, opent u de pagina **[Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** en zoekt u naar de functie met de naam *Inkoop-cXML-verbeteringen*. Selecteer de functie en selecteer **Nu inschakelen** om deze in te schakelen.

Nadat u de functie hebt ingeschakeld, moet u de instellingen in de volgende drie gebieden configureren:

- **[cXML-parameters](#cxml-parameters)**: gebruik deze instellingen om enkele algemene parameters voor de functionaliteit in te stellen voor het verzenden van inkooporders.
- **[Leveranciersinstellingen](#vendor-setup)**: als commerce EXtensible Markup Language (cXML) standaard moet worden gebruikt voor alle nieuwe inkooporders die voor een leverancier worden gemaakt, stelt u de optie **Inkooporder verzenden via cXML** voor die leverancier in op _Ja_.
- **[Externe catalogi](#external-catalog-setup)**: gebruik de nieuwe instellingen voor **Ordereigenschappen** om de indeling van het inkooporderdocument en de manier waarop dit wordt verzonden te definiëren.

In de volgende afbeelding wordt deze configuratie samengevat.

![Gebieden voor het instellen van cXML-kenmerken.](media/cxml-settings-areas.png "Gebieden voor het instellen van cXML-kenmerken")

Daarnaast moet u de [batchtaak voor het aanvragen van inkooporders](#po-batch) instellen. Deze batchtaak wordt gebruikt om de bevestigde inkooporders te verzenden.

## <a name="set-up-global-cxml-parameters"></a><a name="cxml-parameters"></a>Globale cXML-parameters instellen

Gebruik de pagina **cXML-parameters** om enkele algemene instellingen te maken die van toepassing zijn op de functionaliteit voor het verzenden van inkooporders.

![Pagina cXML-parameters.](media/cxml-parameters.png "Pagina cXML-parameters")

Ga naar **Inkoopbeheer \> Instellen \> cXML-beheer \> cXML-parameters** en stel de volgende parameters in:

- **cXML-testmodus**: deze algemene parameter is van invloed op de manier waarop inkooporders fysiek vanuit de batchtaak worden verzonden. Selecteer een van de volgende waarden:

    - **Test**: in deze modus kan de batchtaak worden uitgevoerd en wordt het XML-document voor het bericht gegenereerd, maar het wordt niet verzonden. In plaats daarvan wordt het in het inkooporderverzoek opgeslagen voor revisiedoeleinden. Deze modus is handig wanneer u een eerste implementatie uitvoert en wilt zien hoe gegevens worden ingevoerd in het cXML-bericht. Misschien wilt u ook voorbeeldberichten genereren die u naar leveranciers kunt verzenden voor een eerste validatie.
    - **Live**: in deze modus gebruikt de functie de [instellingen van de externe catalogus](#external-catalog-setup) om elk document fysiek naar de leverancier te verzenden.

- **Updates voor inkoopaanvragen verzenden**: stel deze optie in op *Ja* als u een updatebericht voor inkooporders wilt verzenden. Stel deze in op *Nee* om te voorkomen dat het bericht wordt verzonden. De meeste leveranciers geven er de voorkeur aan om geen updateberichten te ontvangen. In plaats daarvan moeten klanten via telefoon of e-mail contact met hen opnemen als een inkooporder moet worden gewijzigd. Deze parameter is een globale parameter en het is niet mogelijk om in de externe catalogus van een leverancier een overschrijving op te geven. Een inkooporder wordt gemarkeerd als bijgewerkt als u een tweede bevestiging voor een inkooporder boekt terwijl de eerste bevestiging is al verzonden en door de leverancier is bevestigd. Als er een tweede bevestiging is en de eerste bevestiging nog niet is verzonden, wordt de tweede bevestiging beschouwd als een nieuw document. U kunt een inkooporder zo vaak bevestigen als u wilt, totdat er één bevestiging is verzonden. De volgende bevestiging wordt dan behandeld als een updatebericht.
- **Verwijdering van inkoopaanvraag verzenden**: stel deze optie in op *Ja* als u een verwijderingsbericht voor inkooporders wilt verzenden. Stel deze in op *Nee* om te voorkomen dat het bericht wordt verzonden. De meeste leveranciers geven er de voorkeur aan om geen verwijderingsberichten te ontvangen. In plaats daarvan moeten klanten via telefoon of e-mail contact met hen opnemen als een inkooporder per ongeluk is verzonden. Deze parameter is een globale parameter en het is niet mogelijk om in de externe catalogus van een leverancier een overschrijving op te geven. Een inkooporder wordt gemarkeerd als verwijderd als u de inkooporder annuleert in Supply Chain Management.
- **Bestand archiveren**: geef het bestandspad op waarnaar u gearchiveerde cXML-documenten wilt exporteren en opslaan. Het pad wordt gebruikt wanneer u de functie Leegmaken uitvoert op de pagina **Aanvraag van inkooporder**.
- **Maximum aantal tekens voor straat**: voer het maximum aantal tekens in dat kan worden gebruikt in het veld Straat voor adressen in het cXML document. Deze algemene parameter is van invloed op alle leveranciers tenzij er een overschrijving is opgegeven in de eigenschappen van de externe catalogus.

## <a name="set-up-vendor-purchase-orders-to-use-cxml"></a><a name="vendor-setup"></a>Inkooporders van leverancier instellen voor gebruik van cXML

Telkens wanneer u een inkooporder bevestigt waarvoor de optie **Inkooporder verzenden via cXML** is ingesteld op _Ja_, genereert het systeem automatisch het cXML-bericht en wordt dit geleverd aan de leverancier die aan die inkooporder is gekoppeld. U kunt deze optie op twee manieren beheren voor uw inkooporders:

- Als u een leverancier zo wilt instellen dat deze automatisch cXML gebruikt voor alle nieuwe inkooporders die worden gemaakt op basis van een opdracht, gaat u naar **Inkoopbeheer \> Leveranciers \> Alle leveranciers** en selecteert of maakt u een leverancier om de detailpagina ervan te openen. Stel vervolgens op het sneltabblad **Standaardinstellingen van inkooporder** de optie **Inkooporder verzenden via cXML** in op _Ja_. Als cXML ook automatisch moet worden gebruikt voor nieuwe inkooporders die **niet** zijn gemaakt op basis van een opdracht, moet u ook de ordereigenschap **ENABLEMANUALPO** instellen op _True_ voor de gerelateerde externe catalogus. Dit wordt beschreven in de sectie [Ordereigenschappen instellen](#set-order-properties) verderop in dit onderwerp.
- Ga voor afzonderlijke inkooporders naar **Inkoopbeheer \> Inkooporders \> Alle inkooporders** en selecteer of maak een inkooporder om de detailpagina ervan te openen. Ga naar de **koptekst** weergave en stel vervolgens op het sneltabblad **Instellingen** de optie **Inkooporder verzenden via cXML** in.

![Standaardinstellingen voor inkooporders van leverancier.](media/cxml-order-defaults.png "Standaardinstellingen voor inkooporders van leverancier")

## <a name="set-up-an-external-catalog-to-use-cxml"></a><a name="external-catalog-setup"></a>Een externe catalogus instellen voor gebruik van cXML

Op de pagina **Externe catalogi** kunt u voor elk van uw catalogi de functionaliteit PunchOut en de functionaliteit voor het verzenden van inkooporders instellen. Om de relevante instellingen te vinden, gaat u naar **Inkoopbeheer \> Catalogi \> Externe catalogi**. Begin met het [instellen van elke catalogus zoals gebruikelijk](set-up-external-catalog-for-punchout.md). Dit proces omvat het toewijzen van een leverancier, het selecteren van de categorieën die de leverancier mag leveren, en het activeren van de catalogus. Configureer vervolgens de extra instellingen die in deze sectie worden beschreven.

> [!NOTE]
> Wanneer u een inkooporder bevestigt die via cXML kan worden verzonden, zoekt het systeem naar de leverancier die aan de inkooporder is gekoppeld en wordt vervolgens gezocht naar de eerste actieve externe catalogus die aan die leverancier is gekoppeld. Het systeem gebruikt vervolgens de instellingen uit die externe catalogus om de inkooporder te verzenden. Als er meerdere externe catalogi zijn ingesteld, gebruikt het systeem alleen de eerste externe catalogus die wordt gevonden op basis van de leverancier op de inkooporder. Daarom raden wij aan dat u slechts één externe catalogus voor elke leverancier maakt.

![Instellingen van externe catalogus.](media/cxml-supplier-catalog.png "Instellingen van externe catalogus")

### <a name="set-the-punchout-protocol-type"></a>Het type PunchOut-protocol instellen

Stel op het tabblad **Algemeen** van de pagina **Externe catalogi** het veld **Type Punchout-protocol** in op _cXML_. Deze optie is de enige beschikbare optie, tenzij een partner de functionaliteit heeft uitgebreid en een extra optie in de uitbreiding biedt.

Als u ook de catalogus voor PunchOut gebruikt, moet u ook [de berichtindeling instellen](set-up-external-catalog-for-punchout.md). De berichtindeling wordt gebruikt om de verbinding met de leverancier in de PunchOut-transactie te maken vanuit de bestelopdracht. Wanneer een inkooporder wordt verzonden, worden de ordereigenschappen gebruikt om de verbinding met een leverancier tot stand te brengen.

### <a name="set-the-order-properties"></a><a name="set-order-properties"></a>De ordereigenschappen instellen

De functie _Inkoop-cXML-verbeteringen_ beschikt een nieuw sneltabblad **Ordereigenschappen** voor externe catalogi. Dit sneltabblad bevat een raster waarin u de ordereigenschappen kunt definiëren. Het bevat ook een werkbalk. Deze werkbalk bevat de volgende drie knoppen, waarmee u de ordereigenschappen kunt beheren:

- **Standaardeigenschappen**: wanneer u een nieuwe catalogus instelt, selecteert u deze knop om een vooraf gedefinieerde verzameling veelgebruikte eigenschappen aan het raster toe te voegen.
- **Nieuw**: een nieuwe eigenschap aan het raster toevoegen.
- **Verwijderen**: de geselecteerde eigenschap uit het raster verwijderen. Als u per ongeluk een standaardeigenschap verwijdert, selecteert u **Standaardeigenschappen** om alle ontbrekende eigenschappen terug te zetten.

Telkens wanneer u een of meer eigenschappen toevoegt aan het raster, gebruikt u de rechterkolom om een waarde voor elke eigenschap op te geven.

Gebruik de standaardeigenschappen op de volgende manier:

- **BUYER\_COOKIE**: dit traceringsveld kan worden gebruikt om specifieke informatie voor uw bedrijf aan te geven. Tenzij u een overeenkomst hebt met de leverancier over de manier waarop deze eigenschap wordt gebruikt, heeft deze niet veel betekenis bij het verzenden van een inkooporder. Stel deze dan ook in op een eenvoudige waarde.
- **DELIVERTO**: wanneer het verzendadres in het document wordt ingevoerd vanuit de inkooporder, wordt het veld **Informatie ter attentie van** gebruikt om het veld **DeliverTo** in het XML-bericht in te stellen. Als u deze waarde de naam van een aanvrager moet zijn en het veld Aanvrager in de koptekst van de inkooporder wordt ingesteld, voer dan de waarde _REQUESTER_ voor deze eigenschap in, zodat de naam van de aanvrager wordt ingevoerd in het veld **DeliverTo** in de XML. In dit geval worden het primaire e-mailadres en het telefoonnummer van de aanvrager gebruikt in plaats van die van de besteller.
- **DEPLOYMENTMODE**: stel deze eigenschap in volgens de instructies van de leverancier. De waarden zijn meestal _PRODUCTION_ of _TEST_. Stel de waarde in op basis van uw communicatie met de leverancier. Meestal moet deze overeenkomen met het bedoelde systeem achter de **ORDERCHECKURL**-waarde die de leverancier aanduidt als test- of productiesysteem.
- **FIXEDBILLADDRESSID**: wanneer het veld **addressID** in het XML-bericht is ingesteld, wordt de locatie opgehaald die is opgegeven in het adres. Als de ID-waarde die u aan de leverancier hebt verstrekt om welke reden dan ook verschilt van de waarde van de adreslocatie, kunt u een overschrijving forceren door hier de waarde op te geven. De veronderstelling is dat u maar één adres gebruikt bij de leverancier en dat het adres is ingesteld in het systeem van de leverancier. Het factuuradres is het primaire factuuradres dat voor de rechtspersoon is opgegeven in Supply Chain Management.
- **FIXEDSHIPADDRESSID**: wanneer het veld **addressID** in het XML-bericht is ingesteld, wordt de locatie opgehaald die is opgegeven in het adres. Als de ID-waarde die u aan de leverancier hebt verstrekt om welke reden dan ook verschilt van de waarde van de adreslocatie, kunt u een overschrijving forceren door hier de waarde op te geven. De veronderstelling is dat u maar één adres gebruikt bij de leverancier en dat het adres is ingesteld in het systeem van de leverancier. Het verzendadres is het adres dat is opgegeven in de koptekst van de inkooporder. De meeste leveranciers accepteren alleen koptekstadressen, geen regeladressen. Hoewel de XML velden voor regeladressen bevat, worden deze ingesteld op het adres van de koptekst.
- **FROM\_DOMAIN**: geef de waarde op die wordt gebruikt voor het verzenden van inkooporderdocumenten. Deze waarde wordt door de leverancier geleverd.
- **FROM\_IDENTITY**: geef de waarde op die wordt gebruikt voor het verzenden van inkooporderdocumenten. Deze waarde wordt door de leverancier geleverd.
- **ORDERCHECKURL**: voer de URL in waarnaar inkooporderdocumenten moeten worden verzonden. Deze URL begint met `https://` en wordt geleverd door de leverancier.
- **PAYLOAD\_ID**: voer een voorvoegselwaarde in voor de id van de nettolading, zoals is vereist voor de bedrijfsprocessen die de huidige leverancier heeft geïmplementeerd.
- **SENDER\_DOMAIN**: geef de waarde op die wordt gebruikt voor het verzenden van inkooporderdocumenten. Deze waarde wordt door de leverancier geleverd.
- **SENDER\_IDENTITY**: geef de waarde op die wordt gebruikt voor het verzenden van inkooporderdocumenten. Deze waarde wordt door de leverancier geleverd.
- **SHARED\_SECRET**: geef de waarde op die wordt gebruikt voor het verzenden van inkooporderdocumenten. Deze waarde wordt door de leverancier geleverd.
- **STREETLENGTH**: voer een getal in dat staat voor het maximum aantal tekens dat de leverancier als straatnaam accepteert. Als hier een waarde wordt ingevoerd, overschrijft deze de waarde die is opgegeven op de pagina **cXML-parameters**. Regeleinden en spaties worden door het systeem verwijderd om het standaardadres in Supply Chain Management in te passen in het aantal tekens dat hier is opgegeven. Eventuele extra tekens worden afgekapt.
- **TO\_DOMAIN**: geef de waarde op die wordt gebruikt voor het verzenden van inkooporderdocumenten. Deze waarde wordt door de leverancier geleverd.
- **TO\_IDENTITY**: geef de waarde op die wordt gebruikt voor het verzenden van inkooporderdocumenten. Deze waarde wordt door de leverancier geleverd.
- **USERAGENT**: voer een waarde in om het systeem te identificeren dat u gebruikt. Voer bijvoorbeeld _Dynamics 365 Supply Chain Management_ in.
- **VERSION**: voer een cXML-versienummer in als de leverancier deze informatie vraagt. De standaardversie is *1.2.008*. Deze versie is stabiel en wordt door de meeste leveranciers geaccepteerd.
- **RESPONSETEXT**: voer eventuele aangepaste tekst in die de leverancier in het cXML-antwoordbericht verwacht nadat de order is verzonden. Op deze manier kan het systeem het bericht markeren als _Bevestigd_. Als het antwoord niet overeenkomt met de standaardtekst of de klanttekst die u hier invoert, wordt de aanvraag gemarkeerd als _Fout_.
- **RESPONSETEXTSUB**: stel deze eigenschap in op _TRUE_ als u de antwoordtekst van de leverancier wilt doorzoeken op de waarden die zijn opgegeven in het veld **RESPONSETEXT**. De leverancier kan bijvoorbeeld een lange tekenreeks retourneren die "OK" in het antwoord bevat. In dat geval kunt u _OK_ invoeren in het veld **RESPONSETEXT** en **RESPONSETESTSUB** instellen op _TRUE_ om ergens in het antwoord naar 'OK' te zoeken. De order kan vervolgens worden ingesteld op _Bevestigd_.
- **CONTENTTYPE**: in een standaard catalogusinstelling hoeft u deze eigenschap niet in te stellen. Als u een 'server 500'-fout ontvangt van het systeem van een leverancier wanneer u een inkooporder verzendt, kunt u een test uitvoeren door deze eigenschap op in te stellen op _FALSE_. Deze waarde verandert een instelling in de webaanvraag waardoor het bericht voor bepaalde platforms kan worden verzonden.
- **ENABLEHEADERS**: stel deze eigenschap in op _TRUE_ om kopteksten samen met de inkooporder te verzenden. Stel deze eigenschap alleen in als de leverancier deze nodig heeft. Als u deze eigenschap instelt op _TRUE_, kunt u extra aangepaste eigenschappen toevoegen die zijn gebaseerd op de namen die de leverancier levert en daar het voorvoegsel _H\__ aan toevoegen. Bekende voorbeelden zijn **H\_USERID**, **H\_PASSWORD**, **H\_RECEIVERID** en **H\_ACTIONREQUEST**. De volgende aangepaste eigenschappen zijn opgenomen in de standaardeigenschappen:

    - **H \_USERID**: als de handelspartner vereist dat u een gebruikers-id verzendt als onderdeel van de URL om een inkooporder in te dienen, voert u hier de waarde in.
    - **H\_PASSWORD**: als de handelspartner vereist dat u een wachtwoord verzendt als onderdeel van de URL om een inkooporder in te dienen, voert u hier de waarde in.

- **ENABLEMANUALPO**: als deze eigenschap is ingesteld op _TRUE_, nemen handmatig gemaakte inkooporders (dat wil zeggen wanneer ze niet vanuit een bestelopdracht worden gegenereerd), de instelling over van de optie **Inkooporder verzenden via cXML** van de leverancier. Als deze eigenschap niet is ingesteld of als deze is ingesteld op _FALSE_, wordt de optie **Inkooporder verzenden via cXML** niet ingesteld voor de inkooporderkoptekst van de handmatig gemaakte inkooporders. Voor inkooporders die zijn gemaakt op basis van een opdracht, wordt de instelling van de optie **Inkooporder verzenden via cXML** altijd overgenomen van de leverancier, ongeacht de instelling van deze eigenschap. Zie voor meer informatie de sectie [Inkooporders van leverancier instellen voor gebruik van cXML](#vendor-setup) eerder in dit onderwerp.
- **PUNCHOUTPOONLY**: als deze eigenschap is ingesteld op _TRUE_, zal de optie **Inkooporder verzenden via cXML** in de inkooporderkoptekst alleen worden ingesteld voor regels van opdrachten tot inkoop die zijn gemaakt op basis van het PunchOut-proces. Bovendien moet het regeltype van de opdracht tot inkoop van alle regels op de inkooporder _Extern catalogusartikel_ zijn. Anders kan de cXML-inkooporder niet worden gemaakt.
- **PUNCHOUTSHIPTO**: als deze eigenschap is ingesteld op _TRUE_, wordt het standaardadres van de rechtspersoon toegevoegd aan het bericht van de PunchOut-instellingsaanvraag wanneer de gebruiker een externe catalogus opent. Dit adres wordt toegevoegd als het **ShipTo**-adres. Leveranciers gebruiken het **ShipTo**-adres om de prijzen weer te geven op basis van de locatie van het bedrijf.
- **TRACEPUNCHOUT**: stel deze eigenschap in op _TRUE_ als er een foutbericht wordt weergegeven wanneer u vanuit de bestelopdracht naar een externe catalogus probeert te bladeren. Vervolgens worden traceringsgegevens ingevuld voor de **PunchOutSetupRequest**- en **PunchOutResponse**-berichten die tussen Supply Chain Management en de leverancierslocatie worden verzonden. U kunt deze gegevens bekijken op de pagina **Berichtenlogboek van cXML-winkelwagen**, die u kunt openen vanuit de pagina **Externe catalogus instellen** voor de leverancierscatalogus waarmee u problemen ondervindt. Stel deze eigenschap alleen in op _TRUE_ als u problemen wilt oplossen, omdat hierdoor voor elke PunchOut een grote prestatieoverhead in de database ontstaat. Zie de sectie [Het berichtenlogboek van cXML-winkelwagen voor PunchOut van externe catalogus bekijken](#message-log) verderop in dit onderwerp voor meer informatie.
- **REPLACENEWLINE**: stel deze eigenschap in op _TRUE_ als u een probleem hebt omdat het systeem van een leverancier een **PunchOutResponse**-bericht verzendt dat nieuweregeltekens bevat (\\n). Dit probleem kan optreden als de berichten van de leverancier worden geparseerd via middleware of een aanschaffingshub. Als u een probleem hebt met nieuwe leveranciersinstellingen, stelt u de eigenschap **TRACEPUNCHOUT** in op _TRUE_ om het **PunchOutResponse**-bericht weer te geven en te bepalen of de XML-codes zijn opgesplitst in nieuweregeltekens.
- **POCOMMENTS**: stel deze eigenschap in op _TRUE_ als u wilt dat het cXML-document notities bevat die zijn gekoppeld aan de inkooporder in Supply Chain Management. De tekst van de bijlage wordt opgenomen in de opmerkingen in de koptekst in het inkooporderbericht. Zie de sectie [Notities koppelen aan een inkooporder](#attach-po-notes) verderop in dit onderwerp voor meer informatie over hoe het systeem deze bijlagen selecteert en verwerkt.
- **VENDCOMMENTS**: stel deze eigenschap in op _TRUE_ als u wilt dat het cXML-document notities bevat die zijn gekoppeld aan de inkooporder in Supply Chain Management. De tekst van de bijlage wordt opgenomen in de opmerkingen in de koptekst in het inkooporderbericht. Zie de sectie [Notities koppelen aan een inkooporder](#attach-po-notes) voor meer informatie over hoe het systeem deze bijlagen selecteert en verwerkt.
- **CLEANAMP**: stel deze eigenschap in op _TRUE_ als er een foutbericht wordt weergegeven wanneer u een PunchOut aan een leverancier probeert uit te voeren en de retour-URL van de leverancier onjuist gecodeerde ampersands (\&) bevat.
- **PUNCHOUTTZ**: stel deze eigenschap in op _TRUE_ als de leverancier waarmee u werkt, gebruikmaakt van de ISO 8601-standaard (International Organization for Standardization) om een specifieke validatie uit te voeren van de datum en tijd van het PunchOut-aanvraagbericht. Supply Chain Management gebruikt de UTC-datum (Coordinated Universal Time) in het **PunchOutSetupRequest**-bericht. Wanneer u deze eigenschap instelt op _TRUE_, wordt *+00:00* aan de datum- en tijdnotatie toegevoegd.
- **WMSADDRESSID**: stel deze eigenschap in op _TRUE_ als u het magazijnnummer op de inkooporderkoptekst wilt gebruiken als de **addressID**-waarde in het **ShipTo**-adres voor de inkooporderaanvraag die naar de leverancier is verzonden. Als u een waarde instelt voor de eigenschap **FIXEDSHIPADDRESSID**, heeft die waarde voorrang op deze waarde. U moet daarom de ene of de andere eigenschap gebruiken om de waarde van **addressID** waarde in te stellen in het **ShipTo**-adres voor het document.
- **PUNCHOUTSHIPTOUSER**: deze eigenschap werkt samen met de eigenschap **PUNCHOUTSHIPTO**. Als **PUNCHOUTSHIPTO** is ingesteld op _TRUE_, wordt het adres voor de rechtspersoon opgehaald. Als **PUNCHOUTSHIPTOUSER** is ingesteld op _TRUE_, wordt het primaire adres van de PunchOut-gebruiker gebruikt in plaats van het adres van de rechtspersoon.

### <a name="activate-the-external-catalog"></a>De externe catalogus activeren

Wanneer u klaar bent met het instellen van alle eigenschappen en het configureren van andere instellingen voor uw externe catalogus, gaat u terug naar het sneltabblad **Algemeen** van de pagina **Externe catalogi** en stelt u de optie **Actief** in op *Ja*.

### <a name="attach-notes-to-a-purchase-order"></a><a name="attach-po-notes"></a>Notities koppelen aan een inkooporder

Zoals vermeld in de sectie [Ordereigenschappen instellen](#set-order-properties), kunt u de eigenschap **POCOMMENTS** en/of **VENDCOMMENTS** in de instellingen van de externe catalogus instellen op _TRUE_ als u wilt dat de geleverde cXML-tekst tekst bevat uit notities die zijn bijgevoegd bij de relevante inkooporder en/of leveranciersrecords. In deze sectie vindt u meer informatie over hoe het systeem deze bijlagen selecteert en verwerkt, als u deze gebruikt.

Als u de typen notities wilt instellen waarnaar het systeem zal zoeken, gaat u naar **Inkoopbeheer \> Instellen \> Formulieren \> Formulier instellen**. Stel vervolgens op het tabblad **Inkooporder** het veld **Documenten opnemen van type** in op het type notitie dat u wilt kunnen opnemen. Alleen tekstnotities worden opgenomen, geen documentbijlagen.

![Pagina Formulier instellen.](media/cxml-form-setup.png "Pagina Formulier instellen")

Bijlagen worden alleen in een inkooporder opgenomen als het veld **Type** is ingesteld op de waarde die u selecteert in het veld **Documenten opnemen van het type** en als het veld **Beperking** is ingesteld op _Extern_. Als u de bijlagen voor een inkooporder wilt maken, weergeven of bewerken, gaat u naar **Inkoopbeheer \> Alle inkooporders**, selecteert of maakt u een inkooporder en selecteert u vervolgens de knop **Bijlagen** (het symbool van de paperclip) in de rechterbovenhoek.

![Bijgevoegde nota die is ingesteld om te worden verzonden naar een leverancier.](media/cxml-note-to-vendor.png "Bijgevoegde nota die is ingesteld om te worden verzonden naar een leverancier")

## <a name="view-the-cxml-cart-message-log-for-external-catalog-punchout"></a><a name="message-log"></a>Het berichtenlogboek van cXML-winkelwagen weergeven voor PunchOut van externe catalogus

Wanneer u het veld **Type Punchout-protocol** voor een externe catalogus instelt op _cXML_, wordt door het systeem een berichtenlogboek vastgelegd van de winkelwagens die terugkomen van leveranciers. Dit logboek kan worden gebruikt voor het oplossen van problemen en andere gegevensdoeleinden.

Om het logboek voor een externe catalogus te openen, selecteert u de relevante catalogus en selecteert u vervolgens in het actievenster de optie **Berichtenlogboek van cXML-winkelwagen**. Op de pagina **Berichtenlogboek van cXML-winkelwagen** wordt een lijst weergegeven met de winkelwagens die zijn geretourneerd, de XML die is gerelateerd aan die winkelwagens en de regels die zijn gemaakt voor de gerelateerde opdracht tot inkoop.

![Pagina Berichtenlogboek van cXML-winkelwagen.](media/cxml-cart-message-log.png "Pagina Berichtenlogboek van cXML-winkelwagen")

## <a name="set-the-extrinsic-elements-for-external-catalog-punchout"></a>De extrinsieke elementen voor PunchOut van externe catalogus instellen

Wanneer u het **Type Punchout-protocol** voor een externe catalogus instelt op *cXML*, kunt u aangepaste extrinsieke elementen toevoegen die op de juiste plaats in het XML-aanvraagbericht worden ingevoegd.

Voer de volgende stappen uit om extrinsieke elementen toe te voegen aan een externe catalogus.

1. Ga naar **Inkoopbeheer \> Catalogi \> Externe catalogi**.
1. Selecteer de betreffende catalogus.
1. Ga op het sneltabblad **Berichtindeling** naar de sectie **Extrinsieken** en selecteer de optie **Toevoegen** om aan het raster een rij toe te voegen voor elk extrinsiek element dat u wilt opnemen. Stel in elke rij de volgende velden in:

    - **Naam**: voer een naam in voor het element. Deze waarde wordt de waarde van het kenmerk **naam** voor het **Extrinsieke** XML-element dat door elke rij wordt gemaakt. Meestal bespreekt u de naam van elk extrinsiek element met uw leverancier.
    - **Waarde**: selecteer een waarde voor het element. Deze waarde wordt de waarde van het XML-element dat door elke rij wordt gemaakt. De volgende waarden zijn beschikbaar:

        - **Gebruikersnaam**: gebruik de naam van de gebruiker die de PunchOut doet. Deze naam is de aanmeldingsnaam voor Supply Chain Management.
        - **E-mailadres van gebruiker**: gebruik het e-mailadres van de gebruiker die de PunchOut doet. Dit adres is het adres dat de gebruiker heeft ingesteld op het tabblad **Account** van de pagina **Gebruikersopties**.
        - **Willekeurige waarde**: gebruik een unieke willekeurige waarde.
        - **Volledige naam van gebruiker**: gebruik de volledige naam van de contactpersoon die is gekoppeld aan de gebruiker die toegang heeft tot de externe catalogus.
        - **Voornaam**: gebruik de voornaam van de contactpersoon die is gekoppeld aan de gebruiker die toegang heeft tot de externe catalogus.
        - **Achternaam**: gebruik de achternaam van de contactpersoon die is gekoppeld aan de gebruiker die toegang heeft tot de externe catalogus.
        - **Telefoonnummer**: gebruik het primaire telefoonnummer van de contactpersoon die is gekoppeld aan de gebruiker die toegang heeft tot de externe catalogus.

![Instellingen van extrinsiek element.](media/cxml-extrinsics.png "Instellingen van extrinsiek element")

De gebruiker of beheerder ziet de extrinsieke elementen niet, omdat deze pas worden toegevoegd wanneer de gebruiker een PunchOut uitvoert. Deze worden automatisch ingevoegd tussen de **BuyerCookie**- en **BrowserFromPost**-elementen in het aanvraagbericht voor cXML-instelling. Daarom hoeft u deze niet handmatig in te stellen in de XML wanneer u de externe catalogus instelt.

![Extrinsieke elementen die aan het XML-bestand zijn toegevoegd.](media/cxml-extrinsics-xml.png "Extrinsieke elementen die aan het XML-bestand zijn toegevoegd")

## <a name="create-and-process-a-purchase-order"></a><a name="create-po"></a>Een inkooporder maken en verwerken

Wanneer u een inkooporder voor een leverancier maakt, neemt deze de instelling van de optie **Inkooporder verzenden via cXML** van die leverancier over. De instelling blijft echter beschikbaar op het sneltabblad **Instellen** in de weergave **Koptekst** van de inkooporder. U kunt deze dus later indien nodig wijzigen.

![Inkooporder ingesteld voor gebruik van cXML.](media/cxml-purchase-order.png "Inkooporder ingesteld voor gebruik van cXML")

Wanneer u een inkooporder maakt vanuit een opdracht tot inkoop die afkomstig is uit een PunchOut-stroom, worden alle vereiste regeldetails ingevuld. U kunt vervolgens handmatig inkooporderregels toevoegen of deze vanuit andere inkooporders kopiëren. Zorg ervoor dat u alle vereiste velden instelt. Deze vereiste velden bevatten het externe verwijzingsnummer. Dit is het leveranciersnummer dat wordt gebruikt in het cXML-bericht.

![Voorbeeld van een extern verwijzingsnummer.](media/cxml-line-details.png "Voorbeeld van een extern verwijzingsnummer")

Wanneer u alle gegevens voor de inkooporder hebt ingevuld, moet u deze bevestigen. Er wordt geen bericht verzonden, tenzij de inkooporder is bevestigd. Om een inkooporder te bevestigen, gaat u in het actievenster naar het tabblad **Inkoop** en selecteert u in de groep **Acties** de optie **Bevestigen**. 

Nadat de inkooporder is bevestigd, kunt u de status van de bevestiging weergeven via de journalen **Inkooporderbevestigingen**. Ga in het Actievenster naar het tabblad **Inkoop** en selecteer in de groep **Journalen** de optie **Inkooporderbevestigingen**.

Elke inkooporder kan een groot aantal bevestigingen hebben. Elke bevestiging wordt gemarkeerd met een oplopend nummer. In de volgende afbeelding ziet u de inkooporder *00000275* en de bevestiging *00000275-1*. Deze nummering weerspiegelt de standaardfunctionaliteit van Supply Chain Management, waarbij wijzigingen in een inkooporder, en dus het type cXML-bericht dat naar de leverancier moet worden verzonden, worden geïdentificeerd op basis van de bevestiging. Zoals u in de afbeelding ziet, bevat de pagina **Inkooporderbevestigingen** ook de velden **Verzendstatus van order** en **Leveranciersstatus van orderaanvraag**. Zie de sectie [Aanvragen voor inkooporders controleren](#monitor-po-requests) verderop in dit onderwerp voor meer informatie over de verschillende statuswaarden die op deze pagina kunnen worden weergegeven.

![Pagina Inkooporderbevestigingen.](media/cxml-po-confirmations.png "Pagina Inkooporderbevestigingen")

Als u meer informatie over het document wilt bekijken, selecteert u **Inkooporderaanvraag** boven het raster.

De pagina **Inkooporderaanvraag** bevat twee rasters. Het raster in het bovenste gedeelte van de pagina bevat één record voor elke inkooporder die is gemarkeerd voor verzending. Het raster op het tabblad **Aanvraaggeschiedenis van inkooporder** in het onderste gedeelte van de pagina kan meerdere records voor de geselecteerde inkooporder hebben, om de status van elke bevestiging aan te geven. In de volgende afbeelding ziet u inkooporder 00000275 in het bovenste raster en document 00000275-1 in het raster op het tabblad **Aanvraaggeschiedenis van inkooporder**.

![Pagina Inkooporderaanvraag.](media/cxml-po-request.png "Pagina Inkooporderaanvraag")

Als de batchtaak is ingesteld en wordt uitgevoerd, wordt het document verzonden. U kunt de statuswijziging bekijken nadat het document is verzonden. In de volgende afbeelding is het veld **Verzendstatus van order** ingesteld op _Verzonden_. Het veld **Leveranciersstatus van order** wordt ingesteld op _Bevestigd_ om aan te geven dat de leverancier het document heeft ontvangen en het heeft kunnen lezen en kunnen opslaan in het systeem. Het raster op het tabblad **Aanvraaggeschiedenis van inkooporder** toont het tijdstip waarop het document is verzonden. Zie de sectie [Aanvragen voor inkooporders controleren](#monitor-po-requests) voor meer informatie over de verschillende statuswaarden die op deze pagina kunnen worden weergegeven.

![Statusberichten op de pagina Inkooporderaanvraag.](media/cxml-po-request-2.png "Statusberichten op de pagina Inkooporderaanvraag")

## <a name="schedule-the-purchase-order-request-batch-job"></a><a name="po-batch"></a>De batchtaak voor het aanvragen van inkooporders plannen

Als u de batchtaak voor het verzenden van inkooporderaanvragen wilt activeren, gaat u naar **Inkoopbeheer \> Instellen \> cXML-beheer \> Inkooporderaanvraag**. Ga in het actievenster naar het tabblad **Inkooporderaanvraag** en selecteer in de groep **Batch** de optie **Taak indienen** om het dialoogvenster **Inkoopaanvraag voorbereiden en verzenden** te openen. U kunt dit dialoogvenster gebruiken om het terugkeerpatroon in te stellen, net zoals u altijd doet voor batchtaken in Supply Chain Management. Selecteer een interval op basis van uw bestelvolume. Hoewel u de batchtaak elke minuut kunt uitvoeren, is het waarschijnlijk het beste om per dag batches te verzenden op basis van de orderontvangstvensters die overeenkomen met de planningen van uw leveranciers.

Stel, de leverancier heeft een beleid dat aangeeft dat alle orders die vóór 1 uur zijn ontvangen, op dezelfde dag worden verzonden. In dat geval hoeft u de batch mogelijk slechts een paar keer in de ochtend uit te voeren om alle binnengekomen orders te communiceren. De overige orders worden de volgende dag verzonden. Deze beslissing is louter een bedrijfsbeslissing. U kunt dit controleren en de parameters hiervoor dienovereenkomstig instellen.

Tijdens dit proces wordt gezocht naar documenten voor inkooporderaanvragen met de status *Wachten*. Als u een order hebt die u direct naar een leverancier moet verzenden, kunt u **Taak indienen** selecteren en de optie **Batchverwerking** instellen op *Nee*.

## <a name="monitor-purchase-order-requests"></a><a name="monitor-po-requests"></a>Inkooporderaanvragen bewaken

### <a name="view-the-status-of-a-purchase-order"></a>De status van een inkooporder bekijken

Wanneer orders die via cXML kunnen worden verzonden, zijn bevestigd, krijgen ze de status _Wachten_. Zoals beschreven in de sectie [Een inkooporder maken en verwerken](#create-po) kunt u de status van de inkooporder weergeven op de pagina **Inkooporderaanvraag**. Elke inkooporderaanvraag kan, afhankelijk van de parameters en gegevens, een bepaalde status hebben. In deze sectie worden de verschillende statustypen en de waarden ervan beschreven. Deze informatie kan u helpen om problemen te beheren en de status van uw inkooporders te begrijpen.

![Status van inkooporder op de pagina Inkooporderaanvraag.](media/cxml-monitor-po-request.png "Status van inkooporder op de pagina Inkooporderaanvraag")

Het raster in het bovenste gedeelte van de pagina **Inkooporderaanvraag** kan de volgende statuswaarden tonen:

- **Verzendstatus van order**: dit veld kan een van de volgende waarden hebben:

    - **Wachten**: het document wacht op verzending.
    - **Verzonden**: het document is verzonden.
    - **Gestopt**: het document is gemarkeerd als _Gestopt_ voordat het is verzonden. (Als u een document wilt markeren als _Gestopt_, selecteert u **Stoppen** in het actievenster van de pagina **Inkoopaanvraag**.)
    - **Archiveren**: het document is leeggemaakt. (Als u een document wilt leegmaken, selecteert u **Leegmaken** in het actievenster van de pagina **Inkoopaanvraag**.)

- **Leveranciersstatus van orderaanvraag**: dit veld kan een van de volgende waarden hebben:

    - **Wachten**: het document wacht op verzending.
    - **Bevestigd**: het document is bevestigd als ontvangen door de leverancier. U kunt het gedetailleerde XML-bericht dat door de leverancier is geretourneerd, controleren door het tabblad **Antwoord-XML** in het onderste gedeelte van de pagina te selecteren.
    - **Fout**: het document is naar de leverancier verzonden, maar er is een fout opgetreden. U kunt het foutbericht bekijken door in het onderste gedeelte van de pagina het tabblad **Antwoord-XML** te selecteren.

Het raster op het tabblad **Aanvraaggeschiedenis van inkooporder** in het onderste gedeelte van de pagina **Aanvraag voor inkooporder** kan de volgende waarden bevatten:

- **Type orderaanvraag**: dit veld kan een van de volgende waarden hebben:

    - **Nieuw**: de regel wordt direct na bevestiging van de inkooporder gemarkeerd als nieuw.
    - **Bijwerken**: als er al een bevestiging is verzonden en door de leverancier is bevestigd, wordt de volgende bevestiging gemarkeerd als _Update_. Updates worden alleen verzonden als de optie **Updates van inkoopaanvragen verzenden** is ingesteld op *Ja* in de [algemene cXML-parameters](#cxml-parameters).
    - **Verwijderen**: als er al een bevestiging is verzonden en door de leverancier is bevestigd, maar de inkooporder is geannuleerd, wordt de bevestiging gemarkeerd als _Verwijderd_. Verwijderingen worden alleen verzonden als de optie **Verwijdering van inkoopaanvragen verzenden** is ingesteld op *Ja* in de [algemene cXML-parameters](#cxml-parameters).

- **Aanvraagtijd**: het tijdstip waarop de orderbevestiging is gemaakt. U kunt de aanvraagtijd vergelijken met de orderstatustijd om de tijd tussen bevestiging en leveranciersbevestiging te bepalen.
- **Verzendstatus van order**: dit veld is hetzelfde als het veld **Verzendstatus van order** in het bovenste gedeelte van de pagina. Deze wordt hier herhaald, zodat u de status gemakkelijker kunt bekijken op het bevestigingsniveau. Als het veld **Type orderaanvraag** is ingesteld op *Nieuw* en de inkooporder opnieuw wordt bevestigd voordat een bevestiging is verzonden, wordt het veld **Verzendstatus van order** ingesteld op *Archiveren*.
- **Orderstatustijd**: de tijd waarop de record van de inkooporderaanvraaggeschiedenis het laatst is bijgewerkt. (De updates bevatten statuswijzigingen.)
- **Leveranciersstatus van orderaanvraag**: dit veld is hetzelfde als het veld **Leveranciersstatus van orderaanvraag** in het bovenste gedeelte van de pagina. Deze wordt hier herhaald, zodat u de status gemakkelijker kunt bekijken op het bevestigingsniveau.
- **Opnieuw ingediend om**: het tijdstip waarop de record opnieuw is ingediend.
- **Aantal keer opnieuw ingediend**: het aantal keer dat de record opnieuw is ingediend. Een hoge waarde kan betekenen dat er meerdere fouten zijn geweest en kan dus duiden op een probleem met uw gegevensconfiguratie of die van de leverancier.

### <a name="view-the-xml-for-a-purchase-order-request-message"></a>De XML voor een aanvraagbericht voor een inkooporder weergeven

Als u de XML voor het aanvraagbericht voor de inkooporder wilt weergeven, selecteert u het tabblad **XML-tekst van aanvraag** onderaan de pagina **Inkooporderaanvraag**. De informatie op dit tabblad kan handig zijn tijdens het testen of bij het valideren van fouten. Om de informatie beter leesbaar te maken, kunt u deze weergeven als een bericht met opmaak. Kopieer de inhoud van het tabblad naar een tekstbestand en bekijk het bestand in een XML-editor.

![Tabblad XML-tekst van aanvraag.](media/cxml-request-xml-text.png "Tabblad XML-tekst van aanvraag")

### <a name="view-the-details-of-the-vendor-response"></a>De details van het leveranciersantwoord weergeven

Als u de inhoud van een leveranciersbevestiging of foutrespons wilt bekijken, selecteert u het tabblad **Antwoord-XML** onderaan de pagina **Inkooporderaanvraag**.

![Tabblad Antwoord-XML.](media/cxml-response-xml.png "Tabblad Antwoord-XML")

## <a name="additional-resources"></a>Aanvullende bronnen

- [Externe catalogus instellen voor PunchOut eProcurement](set-up-external-catalog-for-punchout.md)
- [Externe catalogi gebruiken voor PunchOut eProcurement](use-external-catalogs-for-punchout.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]