---
title: Geavanceerde automatische toeslagen voor meerdere kanalen
description: Dit onderwerp beschrijft de mogelijkheden voor het beheren van extra toeslagen voor detailhandelskanaalorders met behulp van de geavanceerde functie voor automatische toeslagen.
author: hhaines
manager: annbe
ms.date: 01/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10
ms.openlocfilehash: a980ae9571fb47522d3966dc172b2343641b827e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "345554"
---
# <a name="omni-channel-advanced-auto-charges"></a>Geavanceerde automatische toeslagen voor meerdere kanalen

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dit onderwerp bevat informatie over de configuratie en implementatie van de geavanceerde functie voor automatische-toeslagen die beschikbaar is in Dynamics 365 for Retail versie 10.0.

Wanneer de geavanceerde functie voor automatische toeslagen is ingeschakeld, kunnen orders die zijn gemaakt in een ondersteund detailhandelsafzetkanaal (verkooppunt (POS), callcenter en online), profiteren van de [automatische toeslagen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services)-configuraties gedefinieerd in de ERP-toepassing voor zowel toeslagen op koptekst als op regelniveau.  

In releases vóór Dynamics 365 for Retail versie 10.0 zijn [automatische toeslag](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services)-configuraties alleen toegankelijk voor orders die zijn gemaakt in e-commerce- callcenterkanalen. In versie 10.0 of hoger, kunnen POS-orders gebruikmaken van de automatische-toeslagenconfiguraties. Op die manier kunnen extra diverse toeslagen systematisch worden toegevoegd aan de verkooptransacties.

Bij gebruik van versies ouder dan versie 10.0 wordt een POS-gebruiker gevraagd handmatig verzendkosten in te voeren tijdens het maken van een 'alles verzenden' of 'geselecteerd verzenden' POS-transactie. Terwijl de mogelijkheden van de diverse toeslagen van de toepassing worden gebruikt met betrekking tot de manier waarop de toeslagen op de order worden geschreven, wordt er geen systematische berekening geboden--de berekening is afhankelijk van de invoer van de gebruiker om de hoogte van de toeslagen te bepalen. De toeslagen kunnen alleen worden toegevoegd als een enkele 'verzending'-gerelateerde toeslagencode en kunnen niet eenvoudig worden bewerkt of gewijzigd in het POS nadat ze zijn gemaakt. 

Het gebruik van handmatige prompts om verzendkosten toe te voegen is nog steeds beschikbaar in versies 10.0 en hoger. Als een organisatie de **Geavanceerde automatische toeslagen**-parameter niet inschakelt, blijven de POS-prompts voor handmatige invoer van toeslagen hetzelfde.

Met de geavanceerde functie voor automatische toeslagen beschikken POS-gebruikers over systematische berekeningen voor alle gedefinieerde diverse toeslagen op basis van de instellingentabellen voor automatische toeslagen. Daarnaast hebben gebruikers de mogelijkheid een onbeperkt aantal extra toeslagen en kosten aan een POS-verkooptransactie toe te voegen of te bewerken op kop- of regelniveau (voor contante transacties of een klantorder).

## <a name="enabling-advanced-auto-charges"></a>Geavanceerde automatische toeslagen inschakelen

Op de pagina **Detailhandel \> Instellingen hoofdkwartier \> Parameters \> Parameters detailhandel** gaat u naar het tabblad **Klantorders**. Op het sneltabblad **Toeslagen** zet u **Geavanceerde automatische toeslagen gebruiken** op **Ja**.

![Parameter geavanceerde automatische toeslagen](media/advancedchargesparameter.png)

Wanneer geavanceerde automatische toeslagen zijn ingeschakeld, wordt gebruikers niet meer gevraagd handmatig verzendkosten in te voeren in de POS-terminal bij het maken van een klantorder met alles verzenden of geselecteerd verzenden. Toeslagen op de POS-order worden automatisch berekend en toegevoegd aan de POS-transactie (als een bijbehorende automatische-toeslagen-tabel die overeenkomt met het criterium van de order die wordt gemaakt, wordt gevonden). Gebruikers kunnen ook toeslagen op kop- of regelniveau handmatig toevoegen of onderhouden via de toegevoegde POS-bewerkingen die kunnen worden toegevoegd aan de POS-schermindelingen.  

Wanneer geavanceerde automatische toeslagen zijn ingeschakeld, worden de bestaande **Parameters detailhandel** voor **Verzendkostencode** en **Verzendkosten terugbetalen** niet meer gebruikt. Deze parameters zijn alleen van toepassing als de **Geavanceerde automatische toeslagen gebruiken**-parameter is ingesteld op **Nee**.

Zorg ervoor dat voordat u deze functie inschakelt uw medewerkers zijn opgeleid en getest, want het bedrijfsproces voor het berekenen van verzend- of andere kosten en deze toevoegen aan de POS-verkooporder zal hiermee wijzigen. Zorg ervoor dat u weet wat de impact is van de processtroom op het maken van transacties vanuit het POS. Voor callcenter- en e-Commerce-orders is de impact van het inschakelen van geavanceerde automatische toeslagen minimaal. Callcenter- en e-Commerce-toepassingen gedragen zich als voorheen ten aanzien van de tabellen voor automatische toeslagen voor het berekenen van extra toeslagen of kosten voor een order. Gebruikers van het callcenterkanaal behouden de mogelijkheid om door het systeem berekende automatische toeslagen handmatig te verwerken op kop- of regelniveau of extra diverse toeslagen handmatig toe te voegen op kop- of regelniveau.

## <a name="additional-pos-operations"></a>Aanvullende POS-bewerkingen

Om geavanceerde automatische toeslagen goed te laten werken in uw POS-omgeving, zijn nieuwe POS-bewerkingen toegevoegd. Deze bewerkingen moeten worden toegevoegd aan uw [POS-schermindelingen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/pos-screen-layouts) en gedistribueerd naar de POS-apparaten als u geavanceerde automatische toeslagen implementeert. Als deze bewerkingen niet worden toegevoegd, is het voor gebruikers niet mogelijk diverse toeslagen op de POS-transacties te beheren of onderhouden en kunnen ze op geen enkele wijze de toeslagwaarden die systematisch worden berekend op basis van automatische-toeslagen-configuraties aanpassen of wijzigen. Ten minste wordt voorgesteld dat u de bewerking **Toeslagen beheren** in uw POS-indeling installeert.

De nieuwe bewerkingen zijn als volgt.

- **142 - toeslagen beheren** : u kunt deze bewerking gebruiken om POS-gebruikers de mogelijkheid te geven om diverse toeslagen voor de POS-transactie die handmatig of systematisch via berekeningen van automatische toeslagen zijn toegevoegd, weer te geven en te bewerken.
- **141 - toeslagen koptekst toevoegen** -gebruik deze bewerking om de gebruiker de mogelijkheid te geven om handmatig diverse toeslagen op koptekstniveau toe te voegen aan een POS-verkooptransactie (en de toeslagencode die moet worden gebruikt te selecteren).
- **140 - regeltoeslagen toevoegen** -gebruik deze bewerking om de gebruiker de mogelijkheid te geven om handmatig diverse toeslagen op regelniveau toe te voegen aan een POS-verkooptransactieregel (en de toeslagencode die moet worden gebruikt te selecteren).
- **143 - toeslagen herberekenen** -gebruik deze bewerking om een volledige nieuwe berekening van de toeslagen voor de verkooptransactie uit te voeren. Eventuele eerdere door de gebruiker overschreven automatische toeslagen worden herberekend op basis van de huidige configuratie in de winkelwagen.  

Zoals bij alle POS-bewerkingen kunnen beveiligingsconfiguraties worden gemaakt zodat goedkeuring van een manager is vereist om de bewerking te kunnen uitvoeren.

## <a name="use-case-examples"></a>Voorbeeldzaken gebruiken
In deze sectie zie u voorbeelden van gebruik die u helpen de configuratie en het gebruik van automatische toeslagen en diverse toeslagen binnen de context van orders in het detailhandelskanaal te begrijpen. Deze voorbeelden illustreren de werking van de toepassing wanneer de parameter **Geavanceerde automatische toeslagen gebruiken** is ingeschakeld.

### <a name="auto-charges-header-charges-example"></a>Voorbeeld automatische toeslagen kopteksttoeslagen
#### <a name="use-case-scenario"></a>Voorbeeldscenario gebruiken  

Een retailer wil automatisch vrachtkosten in rekening brengen wanneer er transacties worden aangemaakt in een cdetailhandelskanaal die een verzending van producten naar de klant vereisen.  De detailhandelaar biedt 2 methoden van levering: grond en lucht. Als een klant voor grondlevering kiest en de orderwaarde kleiner is dan € 100, wil de detailhandelaar de klant een vrachttoeslag van € 10 in rekening brengen. Als de order hoger is dan € 100 en de klant kiest voor grondverzending, dan worden geen extra vrachtkosten in rekening gebracht.  Als de klant kiest voor luchtlevering voor alle orders dan gelden vrachtkosten van € 20, ongeacht hun totaalwaarde,

#### <a name="setup-and-configuration"></a>Instellingen en configuratie

Dit scenario vereist de configuratie van twee tabellen met automatische toeslagen.   

Ga naar **Klanten \> Instelling van toeslagen \> Automatische toeslagen**.  

Configureer twee verschillende automatische toeslagen op koptekstniveau. Configureer er een voor de 'grondleveringsmethode' en een voor de 'luchtleveringsmethode'. Stel ze in dit scenario in als gebruiken voor 'Alle klanten'.  

Voor de toeslagen van de grondlevering definieert u in het regelgedeelte van de pagina **Automatische toeslagen** een toeslag van € 10 die wordt toegepast voor orders tussen € ,01 en € 100. Maak een andere toeslagenregel om aan te geven dat voor bestellingen van meer dan € 100,01 geen toeslag geldt.

![Voorbeeld automatische toeslagen](media/headerchargesexample.png)

Voor de toeslagen van de luchtlevering definieert u in het regelgedeelte van het formuleer automatische toeslagen een toeslag van € 20 die wordt toegepast op alle orders (tussen € ,01 en € 9.999.999).

Verzend de wijzigingen naar de Retail Server/afzetkanaal DB, zodat het POS ze kan gebruiken door de taak **1040 distributieplanning** uit te voeren.

#### <a name="sales-processing-for-this-scenario"></a>Verkoopverwerking voor dit scenario

Nadat de bovenstaande configuratiestappen zijn voltooid en de wijzigingen zijn toegepast op de kanaaldatabase, zal elke klantbestelling of verkooptransactie gemaakt in het POS-, callcenter- of e-Commerce-kanaal dat de methoden grond- en luchtlevering heeft ingesteld op koptekstniveau deze toeslagen gebruiken en deze automatisch toepassen op de verkoop.   

Op dit moment zijn de kosten van toepassing op alle verkooptransacties gemaakt binnen de rechtspersoon die gebruikmaakt van deze leveringsmethoden, omdat er geen functionaliteit is om aan te geven dat een automatische-toeslag-configuratie alleen van toepassing is op een specifiek verkoopkanaal.

Voor POS- en e-commerce-scenario's, omdat er geen duidelijke 'koptekst' voor deze orders is gedefinieerd, gelden toeslagen op koptekstniveau alleen als voor alle verkoopregels van de transactie dezelfde leveringsmethode is ingesteld. Als er 'gemengde-leveringsmethoden' zijn voor de transacties die zijn gemaakt door het POS of in e-commerce, worden alleen automatische toeslagen op regelniveau beschouwd en toegepast.

In callcenterscenario's heeft de gebruiker controle over de instelling van de leveringsmethode op de orderkoptekst, daarom worden toeslagen op koptekstniveau van op deze orders toegepast, ook als sommige van de verkoopregels zijn geconfigureerd voor het gebruik van een andere leveringsmethode. Toeslagen op koptekstniveau voor callcenterorders altijd gebaseerd op de leveringsmethode die is gedefinieerd op het niveau van de koptekst van de verkooporder.

### <a name="auto-charges-line-charges-example"></a>Voorbeeld automatische toeslagen regeltoeslagen
#### <a name="use-case-scenario"></a>Voorbeeldscenario gebruiken 
Een leverancier wil een extra toeslag toevoegen voor installatiekosten wanneer de klant een bepaald model computer koopt. Deze computer vereist extra niet-optionele installatietaken die door de detailhandelaar voor de klant wordt uitgevoerd. De detailhandelaar heeft klanten laten weten dat er extra kosten voor deze instelling zijn. De retailer geeft er de voorkeur aan om de toeslagen met betrekking tot deze vergoeding apart te beheren van de verkoopprijs van het product ten behoeve van de financiële verslaglegging. Installatiekosten van € 19,99 zullen in rekening worden gebracht aan de klant wanneer deze specifieke computer wordt gekocht in een van de detailhandelskanalen.

#### <a name="setup-and-configuration"></a>Instellingen en configuratie

Dit scenario vereist de configuratie van een tabel voor automatische toeslagen op regelniveau.

Ga naar **Klanten \> Instelling van toeslagen \> Automatische toeslagen**.  

Stel in **Niveau** het vervolgkeuzemenu op **Regel** en maak een nieuwe record voor automatische toeslagen voor alle klanten en voor het specifieke product of de productgroep waarvoor de installatiekosten worden berekend.

![Voorbeeld automatische toeslagen](media/linechargesexample.png)

Verzend de toeslagen naar de Retail Server/afzetkanaal DB, zodat het POS ze kan gebruiken door de taak **1040 distributieplanning** uit te voeren.

#### <a name="sales-processing-for-this-scenario"></a>Verkoopverwerking voor dit scenario

Nadat de bovenstaande configuratiestappen zijn voltooid en de wijzigingen zijn toegepast op de kanaaldatabase, zal elke klantbestelling of verkooptransactie gemaakt in het POS-, callcenter- of e-Commerce-kanaal dat dit item op de order heeft staan een regeltoeslag oproepen die systematisch aan het ordertotaal wordt toegevoegd.   

Op dit moment zijn de kosten van toepassing op elke verkoopregel die overeenkomt met de configuratie van de automatische toeslag op regelniveau binnen de rechtspersoon, omdat er geen functionaliteit is om een automatische toeslag op regelniveau te configuratie die alleen van toepassing is op een specifiek verkoopkanaal.

### <a name="manual-header-charges-example"></a>Voorbeeld van handmatige koptoeslagen
#### <a name="use-case-scenario-description"></a>Beschrijving voorbeeldscenario gebruiken
Een detailhandelaar maakt een uitzondering op kenmerkende processen door speciale thuisbezorging aan te bieden aan klanten die producten in de winkel bestellen. De detailhandelaar en de klant zijn overeengekomen dat de klant € 25 administratiekosten voor deze service zal betalen. Op de order moet deze toeslag worden toegevoegd aan de transactie. Omdat de vergoeding een algemene vergoeding is en niet is gerelateerd aan een enkel product op de order, moet een koptoeslag worden gebruikt.

#### <a name="setup-and-configuration"></a>Instellingen en configuratie

Zorg ervoor dat de toeslagencode die wordt gebruikt in dit scenario juist is geconfigureerd door naar **Klanten \> Instelling toeslagen \> Toeslagen** te gaan om een juiste toeslagencode voor dit scenario te definiëren.

![Voorbeeld toeslagen](media/chargesexample.png)

Als de toeslag moet worden beschouwd als 'verzendkosten' met het oog op verzendingsgerelateerde kortingen of promoties, zet u **Verzendkosten** op de toeslagencode op **Ja**. Als deze toeslag ook systematisch mag worden terugbetaald tijdens de verwerking van een retourtransactie in de POS-toepassing, stelt u **Terug te betalen** in op **Ja**. De markering **Terug te betalen** is alleen toe te passen wanneer de parameter **Geavanceerde automatische toeslagen gebruiken** is ingesteld op **Ja**.   

Verzend de toeslagen naar de Retail Server/afzetkanaal DB, zodat het POS ze kan gebruiken door de taak **1040 distributieplanning** uit te voeren.

De bewerking **Koptoeslag toevoegen** moet worden geconfigureerd uw [POS-schermindeling](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/pos-screen-layouts) zodat een knop die toegankelijk is voor de gebruiker vanuit het POS deze bewerking kan uitvoeren (bewerking 141).  Wijzigingen in de schermindeling moeten ook naar de detailhandel worden gedistribueerd via de functie voor distributieplanning. 

#### <a name="sales-processing-of-manual-header-charges"></a>Verkoopverwerking van handmatige koptoeslagen

Voor het uitvoeren van het scenario in de POS-toepassing, maakt de POS-gebruiker de verkooptransactie zoals gebruikelijk door de producten en eventuele andere configuraties toe te voegen aan de verkoop. Vóór het innen van de betaling moet de gebruiker de bewerking **Koptoeslag toevoegen** uitvoeren, de gebruiker wordt dan gevraagd om een toeslagencode te selecteren en het bedrag van de toeslag in te voeren. Nadat de gebruiker het proces heeft voltooid, wordt de toeslag toegevoegd aan de verkooporder als een toeslag op kopniveau.  

Dit proces kan worden toegepast in het callcenter met behulp van de bestaande **Toeslagen**-functie in het tabblad **Verkopen** op de werkbalk. Op de pagina **Toeslagen onderhouden** kan de gebruiker kan een nieuwe toeslagregel toevoegen aan de orderkop.

### <a name="manual-line-charges-example"></a>Voorbeeld van handmatige regeltoeslagen
#### <a name="use-case-scenario"></a>Voorbeeldscenario gebruiken
Een klant heeft gevraagd om 2 van de 5 artikelen op de verkooporder als cadeau te verpakken. De detailhandelaar biedt deze optionele service voor een vergoeding van € 2,00 per artikel. Op de order moeten deze kosten specifiek worden toegevoegd aan de artikelen die moeten worden ingepakt.

#### <a name="setup-and-configuration"></a>Instellingen en configuratie

Zorg ervoor dat de toeslagencode die wordt gebruikt in dit scenario juist is geconfigureerd door naar **Klanten \> Instelling toeslagen \> Toeslagen** te gaan om een juiste toeslagencode voor dit scenario te definiëren.

Als de toeslag moet worden beschouwd als 'verzendkosten' met het oog op verzendingsgerelateerde kortingen of promoties, zet u de **Verzendkosten** op de toeslagencode op **Ja**. Als de toeslag ook systematisch mag worden terugbetaald tijdens de verwerking van een retourtransactie in de POS-toepassing, stelt u **Terug te betalen** in op **Ja**. De markering **Terug te betalen** is alleen toe te passen wanneer de parameter **Geavanceerde automatische toeslagen gebruiken** is ingesteld op **Ja**.  

Verzend de toeslagen naar de Retail Server/afzetkanaal DB, zodat het POS ze kan gebruiken door de taak **1040 distributieplanning** uit te voeren.

De bewerking **Regeltoeslag toevoegen** moet worden geconfigureerd uw [POS-schermindeling](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/pos-screen-layouts) zodat een knop die toegankelijk is voor de gebruiker vanuit het POS deze bewerking kan uitvoeren (bewerking 140).  Wijzigingen in de schermindeling moeten ook naar de detailhandel worden gedistribueerd via de functie voor distributieplanning. 

#### <a name="sales-processing-of-the-manual-line-charge"></a>Verkoopverwerking van de handmatige regeltoeslag

Voor het uitvoeren van het scenario in de POS-toepassing, maakt de POS-gebruiker de verkooptransactie zoals gebruikelijk door de producten en eventuele andere configuraties toe te voegen aan de verkoop. Vóór het innen van de betaling, moet de gebruiker de specifieke regel selecteren waarop de toeslag van toepassing zal zijn in de weergegeven lijst met POS-artikelen en de bewerking **Regeltoeslag toevoegen** uitvoeren. De gebruiker wordt gevraagd om een toeslagencode te selecteren en het bedrag van de toeslag in te voeren. Nadat de gebruiker het proces heeft voltooid, wordt de toeslag gekoppeld aan de regel en toegevoegd aan de verkooporder als een toeslag op regelniveau. De gebruiker kan het proces herhalen om extra kosten toe te voegen aan andere artikelregels van de transactie indien nodig.

Hetzelfde proces kan worden toegepast in het callcenter met de functie 'toeslagen onderhouden' gevonden onder de **Financiën** vervolgkeuzelijst in het gedeelte **Verkooporderregels** op de pagina **Verkooporder**.  Hiermee opent u de pagina **Toeslagen onderhouden** waarin de gebruiker een nieuwe toeslag voor een specifieke regel aan de transactie kan toevoegen.

## <a name="additional-features"></a>Extra functies

### <a name="editing-charges-on-a-pos-sales-transaction"></a>Toeslagen op een POS-verkooptransactie bewerken

De bewerking **Toeslagen beheren** (142) moet worden toegevoegd aan de [POS-schermindeling](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/pos-screen-layouts) zodat een gebruiker alle systeemberekende of handmatig gemaakte kop- of regeltoeslagen kan bekijken en bewerken of overschrijven. Als de bewerking niet wordt toegevoegd, zullen gebruikers niet in staat zijn om het bedrag van de toeslagen op de POS-transactie aan te passen, noch zullen zij in staat zijn om de details van de toeslagen, zoals het type toeslagencode gekoppeld aan de toeslag te bekijken.  

Op de pagina **Toeslagen beheren** op het POS kan de gebruiker de details van de toeslagen op kop- en regelniveau bekijken. De gebruiker kan de functie **Bewerken** die beschikbaar is op deze pagina gebruiken om het bedrag in een specifieke toeslagregel te wijzigen. Wanneer een toeslagregel handmatig is overschreven, wordt deze niet systematisch herberekend tenzij de gebruiker de bewerking **Toeslagen herberekenen** start.

Als de **Redencode voor overschrijven toeslag** is geconfigureerd op de instellingspagina **Parameters detailhandel** wordt de gebruiker gevraagd een redencode op te geven wanneer de toeslagen zijn gewijzigd in de POS-toepassing.

Als er redencodes zijn vastgelegd voor overschreven toeslagen, is er ook een nieuw rapport beschikbaar om deze overschrijvingen te bekijken en te controleren. Het rapport kunt u vinden in **Detailhandel \> Query's en rapporten \> Geschiedenis toeslag overschrijven**.

### <a name="refunding-charges-on-a-pos-return-transaction"></a>Toeslagen terugbetalen op een POS-retourtransactie

Als de parameter **Geavanceerde automatische toeslagen gebruiken** is ingesteld op **Ja**, is de bestaande retail-parameter voor **Verzendkosten terugbetalen** niet langer van toepassing. Om aan te geven welke kosten systematisch moeten worden terugbetaald aan een klant bij het gebruik van geavanceerde automatische toeslagen, moe u ervoor zorgen dat de bijbehorende toeslagencode is geconfigureerd als **Terug te betalen** op de instellingspagina **Toeslagencode**. Zorg ervoor dat de instellingen zijn gesynchroniseerd met de databases van uw detailhandelskanaal via de verwerking van de distributieplanning.

### <a name="refunding-charges-on-a-return-order-transaction"></a>Toeslagen terugbetalen op een retourordertransactie

Toeslagen worden niet systematisch terugbetaald in **Retourorders** gemaakt in de detailhandel. Gebruikers moeten de optie **Toeslagen kopiëren** selecteren bij het maken van de **Retourorder**. Als **Toeslagen kopiëren** niet is geselecteerd, worden de toeslagen uit de oorspronkelijke verkooptransactie niet automatisch terugbetaald. Als **Toeslagen kopiëren** is geselecteerd, dan worden alle toeslagen gekopieerd naar de retourorder en kan de gebruiker handmatig de toeslagen bewerken of verwijderen die ze niet willen terugbetalen. Het callcenter retourorderproces herkent momenteel niet de markering **Terug te betalen** in de **Toeslagencode**-instellingen.

### <a name="configuring-pos-receipts-to-show-charges"></a>Configureren van POS-ontvangstbewijzen om toeslagen weer te geven

De volgende elementen voor het ontvangstbewijs zijn toegevoegd aan de ontvangstregel- en voetteksten ter ondersteuning van de functionaliteit van geavanceerde automatische toeslagen.

- **Regel verzendkosten** -dit element op regelniveau kan worden gebruikt om specifieke toeslagencodes die zijn toegepast op de verkoopregel samen te vatten. Alleen codes die zijn gemarkeerd als **Verzend**-kosten op de pagina **Toeslagencode** worden weergegeven.

- **Regel andere toeslagen** -dit element op regelniveau kan worden gebruikt om niet-verzendspecifieke toeslagencodes die zijn toegepast op de verkoopregel samen te vatten. Dit zijn toeslagencodes waarvoor de markering **Verzending** op de pagina **Toeslagencode** niet is ingeschakeld.

- **Details verzendkosten order** -dit element op voettekstniveau geeft de omschrijvingen van de toeslagencodes toegepast op de order die zijn gemarkeerd als **Verzend**-kosten op de instellingspagina **Toeslagencode**.

- **Verzendkosten order** -dit element op voettekstniveau toont de eurowaarde van de toeslagen voor verzending.

- **Details overige toeslagen** - dit element op voettekstniveau geeft de omschrijving van de toeslagencodes toegepast op de order die niet zijn gemarkeerd als Verzendkosten.

- **Overige toeslagen order** -dit element op voettekstniveau toont de eurowaarde van de overige toeslagen die niet gerelateerd zijn aan de verzending.

Het is raadzaam dat de organisatie ook vrije-tekstvelden toevoegt aan de voettekst van het ontvangstbewijs, om de gebieden te kunnen definiëren waar toeslagen worden samengevat. 

### <a name="preventing-charges-from-being-calculated-until-the-pos-order-is-completed"></a>Voorkomen dat toeslagen worden berekend voordat de POS-order is voltooid

Sommige organisaties kunnen er de voorkeur aan geven om te wachten totdat de gebruiker alle verkoopregels aan de POS-transactie heeft toegevoegd vóór de toeslagen worden berekend. Om te voorkomen dat de berekening van toeslagen wordt gemaakt wanneer artikelen worden toegevoegd aan de POS-transactie stelt u de parameter **Toeslag handmatig berekenen** in in het **Functieprofiel** van de winkel. Als u deze parameter inschakelt, dient de POS-gebruiker de bewerking **Totalen berekenen** te gebruiken wanneer die gereed is met het toevoegen van producten aan de POS-transactie. De bewerking **Totalen berekenen** activeert vervolgens de berekening van eventuele automatische toeslagen voor de orderkop of -regels indien van toepassing.