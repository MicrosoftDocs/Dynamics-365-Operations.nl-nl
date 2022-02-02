---
title: Klantorders in POS (Point of Sale)
description: Dit onderwerp bevat informatie over klantorders in POS (Point of Sale). Klantorders worden ook wel speciale orders genoemd. In dit onderwerp worden de gerelateerde parameters en transactiestromen besproken.
author: josaw1
ms.date: 08/02/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.custom:
- "260594"
- intro-internal
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 9ebdad47d761f775cf26666dc3e2736818fb4832
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2022
ms.locfileid: "7982813"
---
# <a name="customer-orders-in-point-of-sale-pos"></a>Klantorders in POS (Point of Sale)

[!include [banner](includes/banner.md)]

Dit onderwerp bevat informatie over het maken en beheren van klantorders in de POS-app (Point of Sale). Klantorders kunnen worden gebruikt om verkopen te registreren waarbij kopers op een latere datum producten willen ophalen, producten op een andere locatie willen ophalen of artikelen willen laten verzenden. 

Veel detailhandelaren bieden de optie van klantorders, oftewel speciale orders, om aan verschillende product- en afhandelingsbehoeften te voldoen. Hierna vindt u enkele typische scenario's:

- Een klant wil dat de producten worden afgeleverd op een specifiek adres op een specifieke datum.
- Een klant wil producten bij een andere winkel of locatie ophalen dan de winkel of locatie waar de klant deze producten heeft gekocht.
- Een klant binnen een winkellocatie wil vandaag producten bestellen om deze op een latere datum op te halen bij dezelfde winkellocatie.

Detailhandelaren kunnen klantorders ook gebruiken om verloren verkoop te minimaliseren waarmee anders voorraadtekorten kunnen worden veroorzaakt, omdat de producten op een ander tijdstip of een andere plaats kunnen worden afgeleverd of opgehaald.

## <a name="set-up-customer-orders"></a>Klantorders instellen
Voordat u de bestelfunctionaliteit van de klant in POS probeert te gebruiken, moet u controleren of u alle vereiste configuraties in Commerce Headquarters hebt voltooid.

### <a name="configure-modes-of-delivery"></a>Leveringsmethoden configureren

Als u klantorders wilt gebruiken, moet u de leveringsmethoden configureren die door het winkelafzetkanaal kunnen worden gebruikt. U moet minimaal één leveringsmethode definiëren die kan worden gebruikt wanneer orderregels vanuit een winkel naar een klant worden verzonden. U moet ook minimaal één ophaalmethode definiëren die kan worden gebruikt wanneer orderregels uit de winkel worden opgehaald. Leveringsmethoden worden gedefinieerd op de pagina **Leveringsmethoden** in Commerce Headquarters. Zie [Leveringsmethoden definiëren](./configure-call-center-delivery.md#define-delivery-modes) voor meer informatie over het instellen van leveringsmethoden.

![De pagina Leveringsmethoden.](media/customer-order-modes-of-delivery.png)


### <a name="set-up-fulfillment-groups"></a>Afhandelingsgroepen instellen

Sommige winkels of magazijnlocaties kunnen klantorders mogelijk niet uitvoeren. Door afhandelingsgroepen te configureren, kan een organisatie opgeven welke winkels en magazijnlocaties als opties worden weergegeven voor gebruikers die klantorders in POS maken. Afhandelingsgroepen worden geconfigureerd op de pagina **Afhandelingsgroepen**. Organisaties kunnen zoveel afhandelingsgroepen maken als ze nodig hebben. Nadat een afhandelingsgroep is gedefinieerd, koppelt u deze aan een winkel door **Afhandelingsgroeptoewijzing** op het tabblad **Instellen** in het actievenster van de pagina **Winkels**.

In Commerce-versie 10.0.12 en hoger kunnen organisaties bepalen of de magazijnen of combinaties van magazijnen en winkels die zijn gedefinieerd in afhandelingsgroepen, kunnen worden gebruikt voor verzending en/of ophalen. Dit biedt de onderneming extra flexibiliteit om te bepalen welke magazijnen kunnen worden geselecteerd bij het maken van een klantenorder voor te verzenden artikelen, en welke winkels kunnen worden geselecteerd bij het maken van een klantenorder voor af te halen artikelen. Als u deze configuratieoptie wilt gebruiken, schakelt u de functie **Mogelijkheid om locaties op te geven als 'Verzenden ' of 'Ophalen' binnen Afhandelingsgroep** in. Als een magazijn dat is gekoppeld aan een afhandelingsgroep geen winkel is, kan dit magazijn alleen worden geconfigureerd als verzendlocatie. Het kan niet worden gebruikt wanneer er orders voor ophalen zijn geconfigureerd in POS.

![De pagina Afhandelingsgroepen.](media/customer-order-fulfillment-group.png)

### <a name="configure-channel-settings"></a>Kanaalinstellingen configureren

Wanneer u in POS met klantorders werkt, moet u rekening houden met enkele van de instellingen van het winkelafzetkanaal. Deze instellingen vindt u op de pagina **Winkels** in Commerce Headquarters.

- **Magazijn**: dit veld geeft het magazijn aan dat wordt gebruikt bij het verminderen van de voorraad voor contant geld en ophaalorders van klanten die aan deze winkel zijn gekoppeld. Als aanbevolen procedure moedigen we het gebruik van unieke magazijnen voor elk winkelkanaal aan om problemen met tegenstrijdige bedrijfslogica in winkels te voorkomen.
- **Verzendmagazijn**: dit veld geeft het magazijn aan dat wordt gebruikt bij het verminderen van de voorraad voor klantorders die vanuit de geselecteerde winkel worden verzonden. Als de functie **Mogelijkheid om locaties op te geven als 'Verzenden ' of 'Ophalen' binnen Afhandelingsgroep** is ingeschakeld in uw omgeving, kunnen POS-gebruikers een specifiek magazijn kiezen om vanuit POS te verzenden, in plaats van een winkel te kiezen om vanuit te verzenden. Wanneer die functie is ingeschakeld, wordt het verzendmagazijn daarom niet meer gebruikt, omdat de gebruiker het specifieke magazijn kiest om de order te verzenden vanaf het moment dat de order wordt gemaakt.
- **Toewijzing van afhandelingsgroep**: selecteer deze knop (op het tabblad **Instellen** in het actievenster) om de afhandelingsgroepen waarnaar wordt verwezen te koppelen om opties voor afhaallocaties of de bron van verzending weer te geven wanneer klantorders worden gemaakt in POS.
- **Op bestemming gebaseerde btw gebruiken**: met deze optie wordt aangegeven of het verzendadres wordt gebruikt om de btw-groep te bepalen die wordt toegepast op orderregels die worden verzonden naar het adres van de klant.
- **Op klant gebaseerde btw gebruiken**: met deze optie wordt aangegeven of de gedefinieerde btw-groep voor het afleveradres van de klant wordt gebruikt om de btw te bepalen voor klantorders die in POS voor verzending naar het huis van de klant worden gemaakt.

![Instellingen van winkelafzetkanaal op de pagina Winkels.](media/customer-order-all-stores.png)

### <a name="set-up-customer-order-parameters"></a>Parameters voor klantorder instellen

Voordat u probeert klantorders in POS te maken, moet u de betreffende parameters in Commerce Headquarters configureren. U kunt deze parameters vinden op het tabblad **Klantorders** van de pagina **Commerce-parameters**.

- **Standaardordertype**: u kunt het ordertype opgeven dat standaard wordt toegewezen aan klantorders die in POS zijn gemaakt. Deze klantorders kunnen verkooporders of offerteorders zijn. Ongeacht het standaardordertype kunnen gebruikers nog steeds zowel verkooporders als klantorders maken vanuit POS.
- **Standaard aanbetalingspercentage**: geef het percentage van het totaalbedrag van de order op dat de klant moet betalen als een aanbetaling voordat een order kan worden bevestigd. Afhankelijk van hun bevoegdheden kunnen winkelmedewerkers het bedrag mogelijk overschrijven via de bewerking **Deposito overschrijven** in POS als die bewerking is geconfigureerd voor de indeling van het transactiescherm.
- **Ophaalmodus van levering**: geef de leveringsmethode op die moet worden toegepast op verkooporderregels die zijn geconfigureerd voor ophalen in POS.
- **Uitvoeringsmodus van levering**: geef de leveringsmethode op die moet worden toegepast op verkooporderregels die worden beschouwd als uitvoeringsorderregels wanneer een gemengde winkelwagen wordt gemaakt waar sommige regels worden opgehaald of verzonden en andere regels onmiddellijk door de klant worden uitgevoerd.
- **Percentage annuleringskosten**: als een toeslag moet worden toegepast wanneer een klantorder wordt geannuleerd, geeft u het bedrag van die toeslag op.
- **Code annuleringskosten**: geef de toeslagcode voor Klanten op die moet worden gebruikt wanneer een annuleringstoeslag wordt toegepast op geannuleerde klantorders via POS. De toeslagcode definieert de financiële boekingslogica voor de annuleringstoeslag.
- **Code verzendkosten**: als de optie **Geavanceerde automatische toeslagen gebruiken** is ingesteld op **Ja**, heeft deze parameter geen effect. Als deze optie is ingesteld op **Nee**, wordt de gebruikers gevraagd handmatig een verzendtoeslag in te voeren bij het maken van klantorders in POS. Gebruik deze parameter om een toeslagcode voor Klanten toe te wijzen die wordt toegepast op orders wanneer gebruikers een verzendingstoeslag invoeren. De toeslagcode definieert de financiële boekingslogica voor de verzendingstoeslag.
- **Geavanceerde automatische toeslagen gebruiken**: stel deze optie in op **Ja** als u automatisch door het systeem berekende toeslagen wilt gebruiken wanneer er klantorders worden gemaakt in POS. Deze automatische toeslagen kunnen worden gebruikt om verzendkosten of andere order- of artikeltoeslagen te berekenen. Zie [Geavanceerde automatische toeslagen voor meerdere kanalen](./omni-auto-charges.md) voor meer informatie over het instellen en gebruiken van geavanceerde automatische toeslagen.

![Het tabblad Klantorders op de pagina Commerce-parameters.](media/customer-order-parameters.png)

### <a name="update-transaction-screen-layouts-in-pos"></a>Transactieschermindelingen bijwerken in POS

Controleer of de [schermindeling](./pos-screen-layouts.md) in POS is geconfigureerd om het maken en beheren van klantorders te ondersteunen en of alle vereiste POS-bewerkingen zijn geconfigureerd. Hier volgt een aantal POS-bewerkingen die worden aanbevolen om het maken en beheren van klantorders goed te ondersteunen:
- **Alle producten verzenden**: deze bewerking wordt gebruikt om op te geven dat alle regels in de winkelwagen voor de transactie naar een bestemming worden verzonden.
- **Geselecteerde producten verzenden**: deze bewerking wordt gebruikt om op te geven dat bepaalde regels in de winkelwagen voor de transactie naar een bestemming worden verzonden.
- **Alle producten ophalen**: deze bewerking wordt gebruikt om op te geven dat alle regels in de winkelwagen voor de transactie van een bepaalde winkellocatie worden opgehaald.
- **Geselecteerde producten ophalen**: deze bewerking wordt gebruikt om op te geven dat bepaalde regels in de winkelwagen voor de transactie van een bepaalde winkellocatie worden opgehaald.
- **Alle producten uitvoeren**: deze bewerking wordt gebruikt om op te geven dat alle regels in de winkelwagen voor de transactie worden uitgevoerd. Als deze bewerking wordt gebruikt in POS, wordt de klantorder omgezet in een cash-and-carry-transactie.
- **Geselecteerde producten uitvoeren** : deze bewerking wordt gebruikt om op te geven dat bepaalde regels in de winkelwagen voor de transactie worden uitgevoerd door de klant op het moment van aankoop. Deze bewerking is alleen nuttig in een scenario met een [hybride order](./hybrid-customer-orders.md).
- **Order intrekken**: deze bewerking wordt gebruikt om klantorders te zoeken en op te halen, zodat POS-gebruikers deze kunnen bewerken of annuleren of hierop de benodigde bewerkingen voor afhandeling kunnen uitvoeren.
- **Leveringsmethode wijzigen**: deze bewerking kan worden gebruikt om snel de leveringsmethode te wijzigen voor regels die al voor verzending zijn geconfigureerd, zonder dat gebruikers de stroom 'alle producten verzenden' of 'geselecteerde producten verzenden' opnieuw doorlopen.
- **Deposito overschrijven**: deze bewerking kan worden gebruikt om het depositobedrag te wijzigen dat de klant voor de geselecteerde klantorder betaalt.

![Bewerkingen in het POS-transactiescherm.](media/customer-order-screen-layout.png)

## <a name="work-with-customer-orders-in-pos"></a>Werken met klantorders in POS

> [!NOTE]
> Functionaliteit voor opbrengsttoerekening wordt momenteel niet ondersteund voor gebruik in Commerce-kanalen (e-commerce, POS, callcenter). Artikelen die zijn geconfigureerd met opbrengsttoerekening, mogen niet worden toegevoegd aan orders die zijn gemaakt in Commerce-kanalen. 

### <a name="create-a-customer-order-for-products-that-will-be-shipped-to-the-customer"></a>Een klantorder maken voor producten die naar de klant worden verzonden

1. Voeg in het POS-transactiescherm een klant toe aan de transactie.
2. Voeg producten aan de winkelwagen toe.
3. Selecteer **Selectie verzenden** of **Alles verzenden** om de producten naar een adres op de klantrekening te verzenden.
4. Selecteer de optie om een klantorder te maken.
5. Bevestig of wijzig de verzendlocatie, bevestig of wijzig het verzendadres en selecteer een verzendmethode.
6. Voer de gewenste orderverzendingsdatum van de klant in.
7. Gebruik de betalingsfuncties om de verschuldigde berekende bedragen te betalen of gebruik de bewerking **Deposito overschrijven** om de bedragen te wijzigen die verschuldigd zijn en pas vervolgens de betaling toe.
8. Als het totale bedrag van de volledige order niet is betaald, voert u een creditcard in die moet worden vastgelegd voor het saldo dat voor de order moet worden gefactureerd.

### <a name="create-a-customer-order-for-products-that-the-customer-will-pick-up"></a>Een klantorder maken voor producten die de klant ophaalt

1. Voeg in het POS-transactiescherm een klant toe aan de transactie.
2. Voeg producten aan de winkelwagen toe.
3. Selecteer **Selectie ophalen** of **Alles ophalen** om de configuratie voor het ophalen van orders te starten.
4. Selecteer de winkel waar de klant de geselecteerde producten komt ophalen.
5. Selecteer een datum waarop het artikel wordt opgehaald.
6. Gebruik de betalingsfuncties om de verschuldigde berekende bedragen te betalen of gebruik de bewerking **Deposito overschrijven** om de bedragen te wijzigen die verschuldigd zijn en pas vervolgens de betaling toe.
7. Als niet het totale bedrag van de order is betaald, geeft u op of de klant later betaalt (bij het ophalen) of dat nu een creditcardtoken wordt gebruikt en bij het afhalen wordt vastgelegd.

### <a name="edit-an-existing-customer-order"></a>Een bestaande klantorder bewerken

Detailhandelorders die in het online- of winkelkanaal worden gemaakt, kunnen zo nodig worden teruggeroepen en bewerkt via POS.

> [!IMPORTANT]
> Niet alle detailhandelorders kunnen worden bewerkt via de POS-toepassing. Orders die in een callcenterkanaal worden gemaakt, kunnen niet worden bewerkt via POS als de instelling [Ordervoltooiing inschakelen](./set-up-order-processing-options.md#enable-order-completion) is ingeschakeld voor het callcenterkanaal. Om de juiste verwerking van de betaling te garanderen, moeten orders die afkomstig zijn uit een callcenterkanaal en waarvoor de functionaliteit Ordervoltooiing inschakelen wordt gebruikt, worden bewerkt via de callcentertoepassing in Commerce Headquarters.

> [!NOTE]
> Het wordt aangeraden orders en offertes die door een niet-callcentergebruiker in Commerce Headquarters zijn gemaakt, niet te bewerken in POS. Voor deze orders en offertes wordt geen gebruik gemaakt van de Commerce-prijsengine. Als de orders en offertes worden bewerkt in POS, wordt de prijs ervan met de Commerce-prijsengine opnieuw bepaald.


In versie 10.0.17 en hoger kunnen gebruikers in aanmerking komende orders bewerken via de POS-toepassing, zelfs als de order gedeeltelijk is vervuld. Orders die volledig zijn gefactureerd, kunnen echter nog steeds niet worden bewerkt via POS. Als u deze functie wilt inschakelen, schakelt u de optie **Gedeeltelijk afgehandelde orders bewerken in Point of Sale** in de werkruimte **Functiebeheer** in. Als deze functie niet is ingeschakeld of als u versie 10.0.16 of eerder gebruikt, kunnen gebruikers alleen klantorders in POS bewerken als de order volledig is geopend. Als de functie is ingeschakeld, kunt u bovendien beperken welke winkels gedeeltelijk vervulde orders kunnen bewerken. De optie om deze mogelijkheid voor specifieke winkels uit te schakelen, kan worden geconfigureerd via het **Functionaliteitsprofiel** op het sneltabblad **Algemeen**.


1. Selecteer **Order intrekken**.
2. Gebruik **Zoeken** om filters in te voeren om de order te vinden en selecteer vervolgens **Toepassen**.
3. Selecteer de order in de lijst met resultaten en selecteer vervolgens **Bewerken**. Als de knop **Bewerken** niet beschikbaar is, heeft de order een status waarin deze niet kan worden bewerkt.
4. Breng in het winkelwagentje voor de transactie de benodigde wijzigingen aan in de klantorder. Sommige wijzigingen zijn mogelijk niet toegestaan tijdens het bewerken.
5. Voltooi het bewerkingsproces door een betalingsbewerking te selecteren.
6. Als u het bewerkingsproces wilt afsluiten zonder wijzigingen op te slaan, kunt u de bewerking **Ongeldig gemaakte transactie** gebruiken.

#### <a name="pricing-impact-when-orders-are-edited"></a>Invloed op prijzen wanneer orders worden bewerkt

Als orders in een POS of op een e-commercesite van Commerce worden geplaatst, leggen klanten zich vast op een bedrag. Dit bedrag bevat een prijs en kan ook een korting bevatten. Een klant die een order plaatst en later contact opneemt met het callcenter om de betreffende order te wijzigen (bijvoorbeeld om een ander artikel toe te voegen), heeft specifieke verwachtingen over de toepassing van kortingen. Zelfs als de promoties op de bestaande orderregels zijn vervallen, verwacht de klant dat de kortingen die oorspronkelijk van toepassing waren op deze regels, van kracht blijven. Als er echter geen korting van kracht was toen de order oorspronkelijk werd geplaatst, maar er sinds die tijd een korting geldt, verwacht de klant dat de nieuwe korting wordt toegepast op de gewijzigde order. Anders annuleert de klant mogelijk alleen de bestaande order en maakt vervolgens een nieuwe order waarop de nieuwe korting van toepassing is. Zoals dit scenario laat zien, moeten prijzen en kortingen die klanten hebben toegezegd, blijven behouden. Tegelijkertijd moeten gebruikers van POS en callcenters de flexibiliteit hebben om prijzen en kortingen voor verkooporderregels indien nodig opnieuw te berekenen.

Wanneer orders worden ingetrokken en bewerkt in POS, worden de prijzen en kortingen van de bestaande orderregels als 'vergrendeld' beschouwd. Dit wil zeggen dat de prijzen en kortingen niet worden gewijzigd, ook niet als sommige orderregels worden geannuleerd of gewijzigd, of als er nieuwe orderregels worden toegevoegd. Om de prijzen en kortingen van bestaande verkoopregels te wijzigen, moet de POS-gebruiker **Herberekenen** selecteren. De prijsvergrendeling wordt vervolgens uit de bestaande orderregels verwijderd. Vóór de release van Commerce versie 10.0.21 was deze mogelijkheid echter niet beschikbaar in het callcenter. In plaats daarvan zorgden wijzigingen in orderregels ervoor dat prijzen en kortingen opnieuw werden berekend.

In de release van Commerce versie 10.0.21 is een nieuwe functie met de naam **Onbedoelde prijsberekening voor commerce-orders voorkomen** beschikbaar in de werkruimte **Functiebeheer**. Standaard is deze functie ingeschakeld. Als deze functie is ingeschakeld, is de nieuwe eigenschap **Prijs vergrendeld** beschikbaar voor alle e-commerce-orders. Als de order is vastgelegd voor orders die vanaf een willekeurig kanaal zijn geplaatst, wordt deze eigenschap automatisch ingeschakeld (het selectievakje is ingeschakeld) voor alle orderregels. Met de Commerce-prijsengine worden deze orderregels vervolgens van alle prijs- en kortingsberekeningen uitgesloten. Als de order wordt bewerkt, worden orderregels dus standaard uitgesloten van de prijs- en kortingsberekening. Gebruikers van callcenters kunnen de eigenschap echter uitschakelen (dus het selectievakje uitschakelen) voor een orderregel en vervolgens **Herberekenen** selecteren om de bestaande orderregels op te nemen in de prijsberekeningen.

Zelfs wanneer ze een handmatige korting op een bestaande verkoopregel toepassen, moeten gebruikers van het callcenter de eigenschap **Prijs vergrendeld** op de verkoopregel uitschakelen voordat ze de handmatige korting toepassen.

Gebruikers van callcenters kunnen de eigenschap **Prijs vergrendeld** ook uitschakelen voor orderregels in bulk door **Prijsvergrendeling verwijderen** in de groep **Berekenen** op het tabblad **Verkopen** in het actievenster van de pagina **Verkooporder** te selecteren. In dit geval wordt de prijsvergrendeling verwijderd uit alle orderregels behalve regels die niet kunnen worden bewerkt (met andere woorden: regels met de status **Gedeeltelijk gefactureerd** of **Gefactureerd**). Nadat de wijzigingen in de order zijn voltooid en zijn ingediend, wordt de prijsvergrendeling vervolgens opnieuw toegepast op alle orderregels.

> [!IMPORTANT]
> Als de functie **Onbedoelde prijsberekening voor commerce-orders voorkomen** is ingeschakeld, worden de instellingen van een handelsovereenkomstevaluatie genegeerd in de prijsbepalingsworkflows. Met andere woorden: in de dialoogvensters voor handelsovereenkomstevaluatie wordt de sectie **Prijsgerelateerd** niet weergegeven. Dit gedrag treedt op omdat zowel de instelling van de evaluatie van handelsovereenkomsten als de prijsvergrendelingsfunctie een vergelijkbaar doel hebben: onbedoelde prijswijzigingen voorkomen. De gebruikerservaring voor de evaluatie van handelsovereenkomsten kan echter niet goed worden geschaald voor grote orders, waarbij gebruikers een of meer orderregels moeten selecteren voor een nieuwe prijsbepaling.

> [!NOTE]
> De eigenschap **Prijs vergrendeld** kan alleen voor een of meer geselecteerde regels worden uitgeschakeld als de module **Callcenter** wordt gebruikt. Het gedrag van POS blijft ongewijzigd. Met andere woorden: POS-gebruikers kunnen prijzen voor geselecteerde orderregels niet ontgrendelen. Ze kunnen echter wel **Herberekenen** selecteren om de prijsvergrendeling van alle bestaande orderregels te verwijderen.

### <a name="cancel-a-customer-order"></a>Een klantorder annuleren

1. Selecteer **Order intrekken**.
2. Gebruik **Zoeken** om filters in te voeren om de order te vinden en selecteer vervolgens **Toepassen**.
3. Selecteer de order in de lijst met resultaten en selecteer vervolgens **Annuleren**. Als de knop **Annuleren** niet beschikbaar is, heeft de order een status waarin deze niet meer kan worden geannuleerd.
4. Als er annuleringskosten zijn geconfigureerd, bevestigt u deze. U kunt de annuleringskosten aanpassen voordat u deze bevestigt, indien nodig. 
5. Voltooi in de winkelwagentje voor de transactie het annuleringsproces door een betalingsbewerking te selecteren. Als de betaalde stortingen hoger zijn dan de annuleringskosten, kunnen restitutiebetalingen verschuldigd zijn.
6. Als u het annuleringsproces wilt afsluiten zonder wijzigingen op te slaan, kunt u de bewerking **Ongeldig gemaakte transactie** gebruiken.

## <a name="finalizing-the-customer-order-shipment-or-pickup-from-pos"></a>De verzending of het ophalen van de klantorder voltooien vanuit POS

Nadat een order is gemaakt, worden de artikelen door de klant opgehaald uit een winkellocatie of verzonden, afhankelijk van de configuratie van de order. Raadpleeg de documentatie voor [afhandeling van orders in winkels](./order-fulfillment-overview.md) voor meer informatie over dit proces.

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Asynchrone transactiestroom voor klantorders

Klantorders kunnen worden gemaakt in POS, in de synchrone of asynchrone modus. Als u prestatieproblemen of gebruikersvertragingen ziet wanneer u klantorders maakt in POS, kunt u het beste het maken van asynchrone orders inschakelen.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Mogelijk maken dat klantorders in de asynchrone modus worden gemaakt

1. Selecteer in Commerce Headquarters op de pagina **Functionaliteitsprofielen** het functionaliteitsprofiel dat overeenkomt met de winkel die u wilt configureren.
2. Stel op het sneltabblad **Algemeen** de optie **Klantorder maken in asynchrone modus** in op **Ja**.

Wanneer de optie **Klantorder maken in asynchrone modus** is ingesteld op **Ja**, worden klantorders altijd in de asynchrone modus gemaakt, zelfs als Retail Transaction Service (RTS) beschikbaar is. Als u deze optie instelt op **Nee**, worden klantorders altijd gemaakt in de synchrone modus via RTS. Wanneer klantorders worden gemaakt in de asynchrone modus, worden deze opgehaald en gemaakt als detailhandeltransacties in Commerce Headquarters vanuit de Pull-taken (P). De bijbehorende verkooporders voor de detailhandeltransacties worden gemaakt wanneer **Orders synchroniseren** handmatig of via een batchproces wordt uitgevoerd.

## <a name="additional-resources"></a>Aanvullende resources

[Hybride klantorders](hybrid-customer-orders.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
