---
title: Klantorders in POS (Point of Sale)
description: Dit onderwerp bevat informatie over klantorders in POS (Point of Sale). Klantorders worden ook wel speciale orders genoemd. In dit onderwerp worden de gerelateerde parameters en transactiestromen besproken.
author: josaw1
manager: AnnBe
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 9e5770de82638e6cef6d4c1dffd1dc85549fb11f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411363"
---
# <a name="customer-orders-in-point-of-sale-pos"></a>Klantorders in POS (Point of Sale)

[!include [banner](includes/banner.md)]

Dit onderwerp bevat informatie over het maken en beheren van klantorders in POS (Point of Sale). Klantorders kunnen worden gebruikt om verkopen te registreren waarbij kopers op een latere datum producten willen ophalen, producten op een andere locatie willen ophalen of artikelen willen laten verzenden. 

Veel detailhandelaren bieden de optie van klantorders, oftewel speciale orders, om aan verschillende product- en afhandelingsbehoeften te voldoen. Hierna vindt u enkele typische scenario's:

- Een klant wil dat de producten worden afgeleverd op een specifiek adres op een specifieke datum.
- Een klant wil producten bij een andere winkel of locatie ophalen dan de winkel of locatie waar de klant deze producten heeft gekocht.
- Een klant binnen een winkellocatie wil vandaag producten bestellen om deze op een latere datum op te halen bij dezelfde winkellocatie.

Detailhandelaren kunnen klantorders ook gebruiken om verloren verkoop te minimaliseren waarmee anders voorraadtekorten kunnen worden veroorzaakt, omdat de producten op een ander tijdstip of een andere plaats kunnen worden afgeleverd of opgehaald.

## <a name="set-up-customer-orders"></a>Klantorders instellen
Voordat u de bestelfunctionaliteit van de klant in POS probeert te gebruiken, moet u controleren of u alle vereiste configuraties in Commerce Headquarters hebt voltooid.

### <a name="configure-modes-of-delivery"></a>Leveringsmethoden configureren

Als u klantorders wilt gebruiken, moet u de leveringsmethoden configureren die door het winkelafzetkanaal kunnen worden gebruikt. U moet minimaal één leveringsmethode definiëren die kan worden gebruikt wanneer orderregels vanuit een winkel naar een klant worden verzonden. U moet ook minimaal één ophaalmethode definiëren die kan worden gebruikt wanneer orderregels uit de winkel worden opgehaald. Leveringsmethoden worden gedefinieerd op de pagina **Leveringsmethoden** in Commerce Headquarters. Zie [Leveringsmethoden definiëren](https://docs.microsoft.com/dynamics365/commerce/configure-call-center-delivery#define-delivery-modes) voor meer informatie over het instellen van leveringsmethoden.

![De pagina Leveringsmethoden](media/customer-order-modes-of-delivery.png)


### <a name="set-up-fulfillment-groups"></a>Afhandelingsgroepen instellen

Sommige winkels of magazijnlocaties kunnen klantorders mogelijk niet uitvoeren. Door afhandelingsgroepen te configureren, kan een organisatie opgeven welke winkels en magazijnlocaties als opties worden weergegeven voor gebruikers die klantorders in POS maken. Afhandelingsgroepen worden geconfigureerd op de pagina **Afhandelingsgroepen**. Organisaties kunnen zoveel afhandelingsgroepen maken als ze nodig hebben. Nadat een afhandelingsgroep is gedefinieerd, kunt u deze koppelen aan een winkel met behulp van een knop op het tabblad **Instellen** in het actievenster van de pagina **Winkels**.

In Commerce-versie 10.0.12 en hoger kunnen organisaties bepalen of de magazijnen of combinaties van magazijnen/winkels die zijn gedefinieerd in afhandelingsgroepen, kunnen worden gebruikt voor verzending en/of ophalen. Daarom heeft de winkel extra flexibiliteit ten aanzien van de magazijn- en winkelopties die worden weergegeven voor gebruikers die een order voor ophalen maken in plaats van een order voor verzending. Als u wilt gebruikmaken van deze configuratieopties, moet u de functie **Mogelijkheid om locaties op te geven als 'Verzenden ' of 'Ophalen' binnen Afhandelingsgroep** inschakelen. Als een magazijn dat is gekoppeld aan een afhandelingsgroep geen winkel is, kan dit magazijn alleen worden geconfigureerd als verzendlocatie. Het kan niet worden gebruikt wanneer er orders voor ophalen zijn geconfigureerd in POS.

![De pagina Afhandelingsgroepen](media/customer-order-fulfillment-group.png)

### <a name="configure-channel-settings"></a>Kanaalinstellingen configureren

Wanneer u in POS met klantorders werkt, moet u rekening houden met enkele van de instellingen van het winkelafzetkanaal. Deze instellingen vindt u op de pagina **Winkels** in Commerce Headquarters.

- **Magazijn**: dit veld geeft het magazijn aan dat wordt gebruikt om te voldoen aan orders die zijn geconfigureerd voor verzending vanuit de winkel.
- **Toewijzing van afhandelingsgroep**: selecteer deze knop (op het tabblad **Instellen** in het actievenster) om de afhandelingsgroepen waarnaar wordt verwezen te koppelen om opties voor afhaallocaties of de bron van verzending weer te geven wanneer klantorders worden gemaakt in POS.
- **Op bestemming gebaseerde btw gebruiken**: met deze optie wordt aangegeven of het verzendadres wordt gebruikt om de btw-groep te bepalen die wordt toegepast op orderregels die worden verzonden naar het adres van de klant.
- **Op klant gebaseerde btw gebruiken**: met deze optie wordt aangegeven of de gedefinieerde btw-groep voor het afleveradres van de klant wordt gebruikt om de btw te bepalen voor klantorders die in POS voor verzending naar het huis van de klant worden gemaakt.

![Instellingen van winkelafzetkanaal op de pagina Winkels](media/customer-order-all-stores.png)

### <a name="set-up-customer-order-parameters"></a>Parameters voor klantorder instellen

Voordat u probeert klantorders in POS te maken, moet u de betreffende parameters in Commerce Headquarters configureren. U kunt deze parameters vinden op het tabblad **Klantorders** van de pagina **Commerce-parameters**.

- **Standaardordertype**: u kunt het ordertype opgeven dat standaard wordt toegewezen aan klantorders die in POS zijn gemaakt. Deze klantorders kunnen verkooporders of offerteorders zijn. Ongeacht het standaardordertype kunnen gebruikers nog steeds zowel verkooporders als klantorders maken vanuit POS.
- **Standaard aanbetalingspercentage**: geef het percentage van het totaalbedrag van de order op dat de klant moet betalen als een aanbetaling voordat een order kan worden bevestigd. Afhankelijk van hun bevoegdheden kunnen winkelmedewerkers het bedrag mogelijk overschrijven via de bewerking **Deposito overschrijven** in POS als die bewerking is geconfigureerd voor de indeling van het transactiescherm.
- **Ophaalmodus van levering**: geef de leveringsmethode op die moet worden toegepast op verkooporderregels die zijn geconfigureerd voor ophalen in POS.
- **Uitvoeringsmodus van levering**: geef de leveringsmethode op die moet worden toegepast op verkooporderregels die worden beschouwd als uitvoeringsorderregels wanneer een gemengde winkelwagen wordt gemaakt waar sommige regels worden opgehaald of verzonden en andere regels onmiddellijk door de klant worden uitgevoerd.
- **Percentage annuleringskosten**: als een toeslag moet worden toegepast wanneer een klantorder wordt geannuleerd, geeft u het bedrag van die toeslag op.
- **Code annuleringskosten**: geef de toeslagcode voor Klanten op die moet worden gebruikt wanneer een annuleringstoeslag wordt toegepast op geannuleerde klantorders via POS. De toeslagcode definieert de financiële boekingslogica voor de annuleringstoeslag.
- **Code verzendkosten**: als de optie **Geavanceerde automatische toeslagen gebruiken** is ingesteld op **Ja**, heeft deze parameter geen effect. Als deze optie is ingesteld op **Nee**, wordt de gebruikers gevraagd handmatig een verzendtoeslag in te voeren bij het maken van klantorders in POS. Gebruik deze parameter om een toeslagcode voor Klanten toe te wijzen die wordt toegepast op orders wanneer gebruikers een verzendingstoeslag invoeren. De toeslagcode definieert de financiële boekingslogica voor de verzendingstoeslag.
- **Geavanceerde automatische toeslagen gebruiken**: stel deze optie in op **Ja** als u automatisch door het systeem berekende toeslagen wilt gebruiken wanneer er klantorders worden gemaakt in POS. Deze automatische toeslagen kunnen worden gebruikt om verzendkosten of andere order- of artikeltoeslagen te berekenen. Zie [Geavanceerde automatische toeslagen voor meerdere kanalen](https://docs.microsoft.com/dynamics365/commerce/omni-auto-charges) voor meer informatie over het instellen en gebruiken van geavanceerde automatische toeslagen.

![Het tabblad Klantorders op de pagina Commerce-parameters](media/customer-order-parameters.png)

### <a name="update-transaction-screen-layouts-in-pos"></a>Transactieschermindelingen bijwerken in POS

Controleer of de [schermindeling](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts) in POS is geconfigureerd om het maken en beheren van klantorders te ondersteunen en of alle vereiste POS-bewerkingen zijn geconfigureerd. Hier volgt een aantal POS-bewerkingen die worden aanbevolen om het maken en beheren van klantorders goed te ondersteunen:
- **Alle producten verzenden**: deze bewerking wordt gebruikt om op te geven dat alle regels in de winkelwagen voor de transactie naar een bestemming worden verzonden.
- **Geselecteerde producten verzenden**: deze bewerking wordt gebruikt om op te geven dat bepaalde regels in de winkelwagen voor de transactie naar een bestemming worden verzonden.
- **Alle producten ophalen**: deze bewerking wordt gebruikt om op te geven dat alle regels in de winkelwagen voor de transactie van een bepaalde winkellocatie worden opgehaald.
- **Geselecteerde producten ophalen**: deze bewerking wordt gebruikt om op te geven dat bepaalde regels in de winkelwagen voor de transactie van een bepaalde winkellocatie worden opgehaald.
- **Alle producten uitvoeren**: deze bewerking wordt gebruikt om op te geven dat alle regels in de winkelwagen voor de transactie worden uitgevoerd. Als deze bewerking wordt gebruikt in POS, wordt de klantorder omgezet in een cash-and-carry-transactie.
- **Geselecteerde producten uitvoeren** : deze bewerking wordt gebruikt om op te geven dat bepaalde regels in de winkelwagen voor de transactie worden uitgevoerd door de klant op het moment van aankoop. Deze bewerking is alleen nuttig in een scenario met een [hybride order](https://docs.microsoft.com/dynamics365/commerce/hybrid-customer-orders).
- **Order terugroepen**: deze bewerking wordt gebruikt om klantorders te zoeken en op te halen, zodat POS-gebruikers deze kunnen bewerken of annuleren of hierop de benodigde bewerkingen voor afhandeling kunnen uitvoeren.
- **Leveringsmethode wijzigen**: deze bewerking kan worden gebruikt om snel de leveringsmethode te wijzigen voor regels die al voor verzending zijn geconfigureerd, zonder dat gebruikers de stroom 'alle producten verzenden' of 'geselecteerde producten verzenden' opnieuw doorlopen.
- **Deposito overschrijven**: deze bewerking kan worden gebruikt om het depositobedrag te wijzigen dat de klant voor de geselecteerde klantorder betaalt.

![Bewerkingen in het POS-transactiescherm](media/customer-order-screen-layout.png)

## <a name="working-with-customer-orders-in-pos"></a>Werken met klantorders in POS

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
5. Selecteer een ophaaldatum.
6. Gebruik de betalingsfuncties om de verschuldigde berekende bedragen te betalen of gebruik de bewerking **Deposito overschrijven** om de bedragen te wijzigen die verschuldigd zijn en pas vervolgens de betaling toe.
7. Als niet het totale bedrag van de order is betaald, geeft u op of de klant later betaalt (bij het ophalen) of dat nu een creditcardtoken wordt gebruikt om de creditcard vervolgens gebruiken en vast te leggen tijdens het ophalen.

### <a name="edit-an-existing-customer-order"></a>Een bestaande klantorder bewerken

Detailhandelorders die in het online- of winkelkanaal worden gemaakt, kunnen zo nodig worden teruggeroepen en bewerkt via POS.

> [!IMPORTANT]
> Orders die in een callcenterkanaal worden gemaakt, kunnen niet worden bewerkt via POS als de instelling [Ordervoltooiing inschakelen](https://docs.microsoft.com/dynamics365/commerce/set-up-order-processing-options#enable-order-completion) is ingeschakeld voor het callcenterkanaal. Om de juiste verwerking van de betaling te garanderen, moeten orders die afkomstig zijn uit een callcenterkanaal en waarvoor de functionaliteit Ordervoltooiing inschakelen wordt gebruikt, worden bewerkt via de callcentertoepassing in Commerce Headquarters.

In Commerce-versies 10.0.13 en eerder kunnen gebruikers alleen ondersteunde klantorders alleen bewerken via POS als de orders volledig open staan. Als er al regels van een order zijn verwerkt voor uitvoering (verzamelen, inpakken, enzovoort), wordt de order vergrendeld voor bewerking in POS.

> [!NOTE]
> In Commerce-versie 10.0.14 kunnen POS-gebruikers met een functie die is vrijgegeven in de [openbare preview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms) klantorders bewerken via POS, zelfs als een deel van de order al is afgehandeld. Orders die volledig zijn gefactureerd, kunnen echter nog steeds niet worden bewerkt via POS. Als u deze preview-functie wilt testen en aanvullende feedback wilt geven, schakelt u de optie **(Preview) Gedeeltelijk afgehandelde orders bewerken in Point of Sale** in de werkruimte **Functiebeheer** in. Klantorders die afkomstig zijn van een callcenterkanaal en de functie Ordervoltooiing inschakelen gebruiken, kunnen niet worden bewerkt, ook niet als deze functie is ingeschakeld.

1. Selecteer **Order terugroepen**.
2. Gebruik **Zoeken** om filters in te voeren om de order te vinden en selecteer vervolgens **Toepassen**.
3. Selecteer de order in de lijst met resultaten en selecteer vervolgens **Bewerken**. Als de knop **Bewerken** niet beschikbaar is, heeft de order een status waarin deze niet kan worden bewerkt.
4. Breng in het winkelwagentje voor de transactie de benodigde wijzigingen aan in de klantorder. Sommige wijzigingen zijn mogelijk niet toegestaan tijdens het bewerken.
5. Voltooi het bewerkingsproces door een betalingsbewerking te selecteren.
6. Als u het bewerkingsproces wilt afsluiten zonder wijzigingen op te slaan, kunt u de bewerking **Ongeldig gemaakte transactie** gebruiken.



### <a name="cancel-a-customer-order"></a>Een klantorder annuleren

1. Selecteer **Order terugroepen**.
2. Gebruik **Zoeken** om filters in te voeren om de order te vinden en selecteer vervolgens **Toepassen**.
3. Selecteer de order in de lijst met resultaten en selecteer vervolgens **Annuleren**. Als de knop **Annuleren** niet beschikbaar is, heeft de order een status waarin deze niet meer kan worden geannuleerd.
4. Als er annuleringskosten zijn geconfigureerd, bevestigt u deze. U kunt de annuleringskosten aanpassen voordat u deze bevestigt, indien nodig. 
5. Voltooi in de winkelwagentje voor de transactie het annuleringsproces door een betalingsbewerking te selecteren. Als de betaalde stortingen hoger zijn dan de annuleringskosten, kunnen restitutiebetalingen verschuldigd zijn.
6. Als u het annuleringsproces wilt afsluiten zonder wijzigingen op te slaan, kunt u de bewerking **Ongeldig gemaakte transactie** gebruiken.

## <a name="finalizing-the-customer-order-shipment-or-pickup-from-pos"></a>De verzending of het ophalen van de klantorder voltooien vanuit POS

Nadat een order is gemaakt, worden de artikelen door de klant opgehaald uit een winkellocatie of verzonden, afhankelijk van de configuratie van de order. Raadpleeg de documentatie voor [afhandeling van orders in winkels](https://docs.microsoft.com/dynamics365/commerce/order-fulfillment-overview) voor meer informatie over dit proces.

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Asynchrone transactiestroom voor klantorders

Klantorders kunnen worden gemaakt in POS, in de synchrone of asynchrone modus. Als u prestatieproblemen of gebruikersvertragingen ziet wanneer u klantorders maakt in POS, kunt u het beste het maken van asynchrone orders inschakelen.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Mogelijk maken dat klantorders in de asynchrone modus worden gemaakt

1. Selecteer in Commerce Headquarters op de pagina **Functionaliteitsprofielen** het functionaliteitsprofiel dat overeenkomt met de winkel die u wilt configureren.
2. Stel op het sneltabblad **Algemeen** de optie **Klantorder maken in asynchrone modus** in op **Ja**.

Wanneer de optie **Klantorder maken in asynchrone modus** is ingesteld op **Ja**, worden klantorders altijd in de asynchrone modus gemaakt, zelfs als Retail Transaction Service (RTS) beschikbaar is. Als u deze optie instelt op **Nee**, worden klantorders altijd gemaakt in de synchrone modus via RTS. Wanneer klantorders worden gemaakt in de asynchrone modus, worden deze opgehaald en gemaakt als detailhandeltransacties in Commerce Headquarters vanuit de Pull-taken (P). De bijbehorende verkooporders voor de detailhandeltransacties worden gemaakt wanneer **Orders synchroniseren** handmatig of via een batchproces wordt uitgevoerd.

## <a name="additional-resources"></a>Aanvullende resources

[Hybride klantorders](hybrid-customer-orders.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]