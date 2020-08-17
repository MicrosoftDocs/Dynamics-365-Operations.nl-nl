---
title: Overzicht van betalingen voor meerdere kanalen
description: Dit onderwerp biedt een overzicht van betalingen voor meerdere kanalen in Dynamics 365 Commerce.
author: rubendel
manager: AnnBe
ms.date: 07/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 8.1.3
ms.openlocfilehash: 2127eb60a82bef8c6b5f5e9a917160331c483649
ms.sourcegitcommit: 59fb179c770c799918f624cf345848fd4202bbdd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/22/2020
ms.locfileid: "3613172"
---
# <a name="omni-channel-payments-overview"></a>Overzicht van betalingen voor meerdere kanalen

[!include [banner](../includes/banner.md)]

Dit onderwerp biedt een overzicht van betalingen voor meerdere kanalen in Dynamics 365 Commerce. Het bevat een uitgebreide lijst met ondersteunde scenario's, informatie over functionaliteit, installatie en probleemoplossing, en beschrijvingen van enkele veelvoorkomende problemen.

## <a name="key-terms"></a>Belangrijke termen

| Voorwaarde | Beschrijving |
|---|---|
| Token  | Een reeks gegevens die door een betalingsverwerker als verwijzing worden verstrekt. Tokens kunnen voor creditcardnummers, betalingsautorisaties en vastleggingen van eerdere betalingen staan. Tokens zijn belangrijk omdat hiermee gevoelige gegevens uit het POS-systeem (Point of Sale) kunnen worden gehouden. Dit worden ook wel *verwijzingen* genoemd. |
| Kaarttoken | Een token dat door een betalingsverwerker beschikbaar wordt gesteld voor opslag in het POS-systeem. Een kaarttoken kan alleen worden gebruikt door de verkoper die het token ontvangt. Kaarttokens worden ook wel *kaartverwijzingen* genoemd. |
| Autorisatietoken | Een unieke id die door een betalingsproces wordt gebruikt als onderdeel van het antwoord dat naar een POS-systeem wordt verzonden nadat het POS-systeem een autorisatieaanvraag heeft ingediend. Een autorisatietoken kan later worden gebruikt als de verwerker wordt aangeroepen om acties uit te voeren, zoals het terugdraaien of ongeldig maken van de autorisatie. Het wordt echter meestal gebruikt om fondsen vast te leggen wanneer aan een wordt voldaan of een transactie wordt afgerond. Autorisatietokens worden ook wel *autorisatieverwijzingen* genoemd. |
| Vastleggingstoken | Een verwijzing die door een betalingsverwerker aan een POS-systeem wordt doorgegeven wanneer een betaling wordt afgerond of vastgelegd. De vastleggingstoken kan vervolgens bij latere bewerkingen, zoals restitutieaanvragen, worden gebruikt om te verwijzen naar de betalingsregistratie. | 
| Kaart niet aanwezig | Een term die verwijst naar betalingstransacties waarbij geen fysieke kaart wordt aangeboden. Deze transacties kunnen bijvoorbeeld plaatsvinden in e-commerce- of callcenterscenario's. Voor deze transacties worden de betalingsgegevens handmatig ingevoerd op een e-commercewebsite, in een callcenterproces of op de POS- of de betalingsterminal. |
| Kaart aanwezig | Een term die verwijst naar betalingstransacties waarbij een fysieke kaart wordt gepresenteerd en gebruikt op een betalingsterminal die is verbonden met het Microsoft Dynamics 365 POS-systeem. |

## <a name="overview"></a>Overzicht

Over het algemeen verwijst *betalingen voor meerdere kanalen* naar de mogelijkheid om een order in één kanaal te maken en in een ander kanaal te vervullen. De sleutel tot de ondersteuning van betalingen voor meerdere kanalen is het bewaren van betalingsgegevens met de rest van de orderdetails om deze betalingsgegevens vervolgens te kunnen gebruiken wanneer de order wordt ingetrokken of verwerkt in een ander kanaal. Een klassiek voorbeeld is het scenario van online kopen en ophalen in de winkel. In dit scenario worden de betalingsgegevens toegevoegd wanneer de order online wordt gemaakt. Deze worden vervolgens weer ingetrokken in het POS om het bedrag in rekening te brengen van de betalingskaart van de klant bij het ophalen. 

Alle scenario's die in dit onderwerp worden beschreven, kunnen worden geïmplementeerd met de standaard-SDK Betalingen die met Commerce wordt geleverd. De [Dynamics 365-betalingsconnector voor Adyen](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3) biedt een standaardimplementatie van elk scenario dat hier wordt beschreven. 

### <a name="prerequisites"></a>Vereisten

Voor elk scenario dat in dit onderwerp wordt beschreven, hebt u een betalingsconnector die betalingen voor meerdere kanalen ondersteunt. De kant-en-klare Adyen-connector kan ook worden gebruikt omdat deze de scenario's ondersteunt die beschikbaar worden gesteld via de SDK Betalingen. Voor meer informatie over het implementeren van betalingsconnectors en over de Retail SDK in het algemeen gaat u naar de startpagina [Retail voor IT-professionals en ontwikkelaars](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/dev-retail-home-page#payment-connectors).

#### <a name="supported-versions"></a>Ondersteunde versies

De mogelijkheden voor betalingen voor meerdere kanalen die in dit onderwerp worden beschreven, zijn uitgebracht als onderdeel van Microsoft Dynamics 365 for Retail 8.1.3. 

#### <a name="card-present-and-card-not-present-connectors"></a>Connectors voor transacties met of zonder kaart

De Betalingen-SDK vertrouwt op twee sets API's (Application Programming Interface) voor betalingen. De eerste set API's heeft de naam **iPaymentProcessor**. Deze wordt gebruikt voor de implementatie van connectors voor betalingen zonder kaart die kunnen worden gebruikt in callcenters en het platform Microsoft Dynamics e-Commerce. Zie voor meer informatie over de interface **iPaymentProcessor** de whitepaper [Implement a payment connector and a payment device](https://download.microsoft.com/download/e/2/7/e2735c65-1e66-4b8d-8a3c-e6ef3a319137/The%20Guide%20to%20Implementing%20Payment%20Connector%20and%20Payment%20Device_update.pdf) over betalingen. 

De tweede set API's heeft de naam **iNamedRequestHandler**. Deze set ondersteunt de implementatie van integraties van betalingen met kaart waarbij een betalingsterminal wordt gebruikt. Zie voor meer informatie over de interface **iNamedRequestHandler** het onderwerp [Betalingsintegratie maken voor een betalingsterminal](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/end-to-end-payment-extension). 

### <a name="setup-and-configuration"></a>Instellingen en configuratie

De volgende onderdelen en installatiestappen zijn vereist:

- **eCommerce-integratie:** een integratie met Commerce is vereist ter ondersteuning van scenario's waarin een order afkomstig is uit een online winkel. Zie [e-Commerce platform software development kit (SDK)](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/ecommerce-platform-sdk) voor meer informatie over de SDK Retail e-Commerce. In een demo-omgeving ondersteunt de referentiewinkel scenario's voor betalingen voor meerdere kanalen. 
- **Configuratie van online betalingen**: de instellingen van het online kanaal moeten een betalingsconnector bevatten die is bijgewerkt ter ondersteuning van betalingen voor meerdere kanalen. U kunt ook de kant-en-klare betalingsconnector gebruiken. Zie [Adyen-betalingsconnector](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3#e-commerce) voor informatie over het configureren van de Adyen-betalingsconnector voor online winkels. Naast de installatiestappen voor e-commerce die in dat onderwerp worden beschreven, moet de parameter **Opslaan van betalingsgegevens toestaan in e-commerce** zijn ingesteld op **Waar** in de instellingen voor de Adyen-connector. 
- **Configuratie van betalingen voor meerdere kanalen**: ga in de back-office naar **Retail en Commerce \> Instelling van hoofdkantoor \> Parameters \> Gedeelde Commerce-parameters**. Stel vervolgens op het tabblad **Betalingen voor meerdere kanalen** de optie **Betalingen voor meerdere kanalen gebruiken** in op **Ja**. In Commerce versies 10.0.12 en hoger bevindt deze instelling zich in het werkgebied **Functiebeheer**. Selecteer de functie **Betalingen voor meerdere kanalen** en klik op **Nu inschakelen**. 
- **Betalingsservices:** het callcenter gebruikt de standaardbetalingsconnector op de pagina **Betalingsservices** om betalingen te verwerken. Ter ondersteuning van scenario's, zoals 'kopen in callcenter, ophalen in winkel' wilt ondersteunen, moet deze standaardbetalingsconnector de Adyen-betalingsconnector of een betalingsconnector zijn die voldoet aan de implementatievereisten voor betalingen voor meerdere kanalen.
- **EFT-service** : betalingen via een betalingsterminal moeten worden ingesteld op het sneltabblad **EFT-service** van het hardwareprofiel. De Adyen-connector ondersteunt kant-en-klare betalingen voor meerdere kanalen. Andere betalingsconnectors die de interface **iNamedRequestHandler** ondersteunen, kunnen ook worden gebruikt als ze betalingen voor meerdere kanalen ondersteunen.
- **Beschikbaarheid van betalingsconnector:** wanneer een order wordt ingetrokken, bevatten de regels van de betalingsmethode die met de order worden ingetrokken de naam van de betalingsconnector die is gebruikt voor het maken van de autorisaties die aan die order zijn gekoppeld. Wanneer de order wordt voltooid, probeert de SDK Betalingen dezelfde connector te gebruiken die is gebruikt om de oorspronkelijke autorisatie te maken. Daarom moet een betalingsconnector met dezelfde zakelijke eigenschappen beschikbaar zijn voor registratie. 
- **Kaarttypen:** scenario's met betalingen voor meerdere kanalen werken alleen naar behoren als voor elk kanaal dezelfde typen betalingsmethoden zijn ingesteld die voor meerdere kanalen kunnen worden gebruikt. Hierbij gaat het onder andere om betalingsmethode-id' en kaarttype-id's. Als het type betalingsmethode **Kaarten** bijvoorbeeld de id **2** heeft in de instelling van de online winkel, moet deze dezelfde id hebben in de instelling van de detailhandelwinkel. Dezelfde vereiste geldt voor kaarttype-id's. Als kaartnummer **12** is ingesteld op **VISA** in de online winkel, moet dezelfde id worden ingesteld voor de detailhandelwinkel. 
- Het Retail Modern POS voor Windows of Android met ingebouwd hardwarestation   -of-
- Modern POS voor iOS of cloud-POS met verbonden, gedeeld hardwarestation. 

### <a name="basic-principle-supporting-omni-channel-payments"></a>Basisprincipe voor het ondersteunen van betalingen voor meerdere kanalen

Betalingsconnectors en betalingsprocessors gebruiken tokens of verwijzingen om te verwijzen naar interacties die betrekking hebben op kaartbetalingen. Wanneer bijvoorbeeld een betalingsautorisatie wordt aangevraagd, wordt een verwijzing naar die autorisatie gegeven. Daarom kan later worden verwezen naar de autorisatie wanneer fondsen worden vastgelegd op het moment van afhandeling. Deze autorisatie is uniek voor de verkoper, betalingsconnector en verwerker. 

Als een order die online is gemaakt, wordt opgehaald in de winkel, moeten dezelfde betalingsgegevens voor die order worden ingetrokken en gebruikt. Wanneer de oorspronkelijke details worden verstrekt als onderdeel van de aanvraag om een betaling vast te leggen op basis van de oorspronkelijke autorisatie, kan de betalingsverwerker de aanvraag afhandelen en de betaling vastleggen. 

Voor een juiste verwijzing naar de online order moet ook een connector voor betalingen zonder kaart beschikbaar zijn die dezelfde verwerker ondersteunt. Op deze manier kan het POS-systeem één verwerker hebben voor betalingen met kaart, maar heeft het ook toegang tot andere betalingsconnectors, zodat orders kunnen worden afgehandeld die in andere kanalen worden gemaakt met verschillende betalingsprocessors. 

## <a name="supported-scenarios"></a>Ondersteunde scenario's

De volgende scenario's voor betalingen voor meerdere kanalen worden ondersteund:

- Online kopen, ophalen in winkel
- Kopen in callcenter, ophalen in winkel
- Kopen in winkel A, ophalen in winkel B
- Kopen in winkel A, verzenden naar klant

Variaties op deze scenario's worden ook ondersteund. Een online order kan bijvoorbeeld regels bevatten die worden verzonden naar de klant en regels die worden opgehaald in een winkel. Alle opties voor orderafhandeling worden ondersteund via betalingen voor meerdere kanalen. 

In de volgende secties worden de stappen voor elk scenario beschreven en wordt aangegeven hoe u het scenario kunt uitvoeren met behulp van demogegevens. 

### <a name="buy-online-pick-up-in-store"></a>Online kopen, ophalen in winkel

Voordat u begint, moet u ervoor zorgen dat aan de volgende voorwaarden wordt voldaan:

- U hebt een referentiewinkel waar de Adyen-connector is geconfigureerd.
- De optie **Betalingen voor meerdere kanalen** op de pagina **Gedeelde Commerce-parameters** wordt ingesteld op **Waar**. In latere versies wordt deze instelling verplaatst naar het werkgebied **Functiebeheer**, waar u de functie **Betalingen voor meerdere kanalen** kunt selecteren en op **Nu inschakelen** kunt klikken. 
- De Adyen-betalingsconnector is geconfigureerd voor de Houston POS-kassa.
- Het Retail Modern POS voor Windows of Android met ingebouwd hardwarestation   -of-
- Modern POS voor iOS of cloud-POS met verbonden, gedeeld hardwarestation. 

Voer de volgende stappen uit om het scenario uit te voeren.

1. Maak in de referentiewinkel een bestelling die in de winkel moet worden afgehaald. Selecteer de juiste winkel **Houston**. 
2. Voer de stappen voor afrekenen uit en betaal met een testcreditcardnummer. U kunt op de pagina met [testkaartnummers van Adyen](https://docs.adyen.com/development-resources/test-cards/test-card-numbers/#description) testcreditcardnummers vinden.
3. In Commerce gebruikt u de batchtaak **Orders synchroniseren** en het distributieschema **P-001** om de orders in de back-office te maken.
4. Selecteer in de POS-pagina op de pagina Welkom de **orders waarvoor u** de order wilt ophalen om de orders voor de afhalen in de winkel te bekijken. 
5. Selecteer een of meer regels uit de order die is gemaakt in de referentiewinkel en selecteer **Verzamelen**.

    De order wordt opgehaald uit de back-office. 

6. Wanneer de orderregeldetails worden opgehaald uit de back-office er een kaartbetaling wordt gedetecteerde die kan worden gebruikt voor betalingen voor meerdere kanalen, wordt aangegeven dat een betalingsmethode beschikbaar is.
7. Selecteer **Beschikbare betalingsmethode gebruiken** om de transactie te voltooien op basis van de kaartgegevens die in de referentiewinkel zijn ingevoerd.

    De orderregels worden op de transactiepagina geladen en het openstaande saldo is 0 (nul). 

8. Selecteer het tabblad **Betalingen** om de regel met de betalingsmethode weer te geven die uit de online order is gehaald. 
9. Selecteer een betalingsmethode om de transactie te voltooien. 

### <a name="buy-in-call-center-pick-up-in-store"></a>Kopen in callcenter, ophalen in winkel

1. Voer in Commerce op de pagina **Klantenservice** de naam **Karen Berg** in de zoekbalk in en selecteer **Zoeken**. 
3. Selecteer **Karen Berg** in de zoekresultaten.
4. Als Karen Berg is geladen op de pagina **Klantenservice**, selecteert u **Nieuwe verkooporder**.
5. Selecteer **Koptekst** op de pagina Nieuwe verkooporder om de orderkoptekst weer te geven. 
6. Op de pagina **Orderkoptekst** stelt u als locatie **Centraal** in en als magazijn **Houston**.
7. Stel op het tabblad **Leveren** het veld **Leveringsmethode** in op **60** voor ophalen door klanten.
8. Selecteer **Regels**en voeg vervolgens een of meer regels toe aan de order. 
9. Selecteer **Voltooien** om de ordervoltooiingsstroom in te voeren.
10. Schuif naar beneden naar het betalingsgedeelte, selecteer **Toevoegen** en selecteer vervolgens een regel waarvoor het type betalingsmethode is ingesteld op **Kaarten**. 
11. Selecteer het plusteken (**+**) om een kaartbetaling toe te voegen. 
12. Voer de details voor een testcreditcardnummer in dat u hebt gevonden op de [pagina met testkaartnummers van Adyen](https://docs.adyen.com/development-resources/test-cards/test-card-numbers/#description) en selecteer vervolgens **OK**.

    > [!NOTE]
    > Als het kaartmerk voor het ingevoerde kaartnummer afwijkt van het merk dat is geselecteerd toen de betaling werd gestart, wordt de betaling nog steeds uitgevoerd. In dat geval wordt de betaling echter geboekt naar de rekeningen die zijn toegewezen aan het kaartmerk dat u in stap 10 hebt geselecteerd.

12. Selecteer nogmaals **OK** om het dialoogvenster **Betalingen ordervoltooiingen** te sluiten.
13. Selecteer op de pagina **Overzicht van verkooporder** de optie **Indienen**.
14. Selecteer in de POS-pagina op de pagina Welkom de **orders waarvoor u** de order wilt ophalen om de orders voor de afhalen in de winkel te bekijken. 
15. Selecteer een of meer regels uit de order die is gemaakt in de referentiewinkel en selecteer **Verzamelen**.

    De order wordt opgehaald uit de back-office. 

16. Wanneer de orderregeldetails worden opgehaald uit de back-office er een kaartbetaling wordt gedetecteerde die kan worden gebruikt voor betalingen voor meerdere kanalen, wordt aangegeven dat een betalingsmethode beschikbaar is.
17. Selecteer **Beschikbare betalingsmethode gebruiken** om de transactie te voltooien op basis van de kaartgegevens die in de referentiewinkel zijn ingevoerd.

    De orderregels worden op de transactiepagina geladen en het openstaande saldo is 0 (nul).

18. Selecteer het tabblad **Betalingen** om de regel met de betalingsmethode weer te geven die uit de online order is gehaald. 
19. Selecteer een betalingsmethode om de transactie te voltooien. 

### <a name="buy-in-store-a-pick-up-in-store-b"></a>Kopen in winkel A, ophalen in winkel B

1. Start het POS voor de Houston-winkel.
2. Voeg op de pagina **Transactie** Karen Berg toe aan de transactie door met het numerieke toetsenblok **2001** in te voeren.
3. Voeg een of meer regels toe aan de transactie.
4. Selecteer **Orders** om de orderopties weer te geven.
5. Selecteer **Alles verzamelen** en selecteer vervolgens de optie **Klantorder** wanneer u daarom wordt gevraagd.
6. Voer **Seattle** in de zoekbalk in en selecteer de winkel in **Seattle** voor ophalen. 
7. Selecteer **OK** om de huidige datum te accepteren als datum van ophalen.
9. Selecteer **Betaalkaart** om de betalingsreferentie te initiëren.
10. Wijs de kaartbetaling toe voor het verschuldigde bedrag voor het deposito. 
11. Voltooi de depositobetaling op de betalingsterminal. 
12. Nadat het deposito is betaald, selecteert u de optie om dezelfde kaart te gebruiken voor afhandeling en wacht u totdat de order is voltooid. 
13. Start het POS voor de Seattle-winkel.
14. Selecteer in de POS-pagina op de pagina Welkom de **orders waarvoor u** de order wilt ophalen om de orders voor de afhalen in de winkel te bekijken. 
15. Selecteer een of meer regels uit de order die is gemaakt in de referentiewinkel en selecteer **Verzamelen**.

    De order wordt opgehaald uit de back-office. 

16. Wanneer de orderregeldetails worden opgehaald uit de back-office er een kaartbetaling wordt gedetecteerde die kan worden gebruikt voor betalingen voor meerdere kanalen, wordt aangegeven dat een betalingsmethode beschikbaar is.
17. Selecteer **Beschikbare betalingsmethode gebruiken** om de transactie te voltooien op basis van de kaartgegevens die in de referentiewinkel zijn ingevoerd.

    De orderregels worden op de transactiepagina geladen en het openstaande saldo is 0 (nul).

18. Selecteer het tabblad **Betalingen** om de regel met de betalingsmethode weer te geven die uit de online order is gehaald. 
19. Selecteer een betalingsmethode om de transactie te voltooien. 

### <a name="buy-in-store-a-ship-to-customer"></a>Kopen in winkel A, verzenden naar klant

1. Start het POS voor de Houston-winkel.
2. Voeg op de pagina **Transactie** Karen Berg toe aan de transactie door met het numerieke toetsenblok **2001** in te voeren.
3. Voeg een of meer regels toe aan de transactie.
4. Selecteer **Orders** om de orderopties weer te geven.
5. Selecteer **Alles verzamelen** en selecteer vervolgens de optie **Klantorder** wanneer u daarom wordt gevraagd.
6. Voer **Seattle** in de zoekbalk in en selecteer de winkel in **Seattle** voor ophalen. 
7. Selecteer **OK** om de huidige datum te accepteren als datum van ophalen.
8. Selecteer **Betaalkaart** om de betalingsreferentie te initiëren.
9. Wijs de kaartbetaling toe voor het verschuldigde bedrag voor het deposito. 
10. Voltooi de depositobetaling op de betalingsterminal. 
11. Nadat het deposito is betaald, selecteert u de optie om dezelfde kaart te gebruiken voor afhandeling en wacht u totdat de order is voltooid.

Wanneer de order wordt verzameld, verpakt en gefactureerd in de back-office, worden de betalingsdetails op het POS gebruikt om de fondsen vast te leggen voor de goederen die naar de klant worden verzonden. 

## <a name="scenario-details"></a>Scenariodetails

Naast de basisscenario's die we zojuist hebben beschreven, zijn er diverse verbeteringen aangebracht in de betalings-SDK ter ondersteuning van betalingen voor meerdere kanalen. 

### <a name="pos"></a>POS

#### <a name="single-swipedip-for-customer-orders"></a>Eén keer doorhalen voor klantorders

Voordat de functie voor betalingen voor meerdere kanalen werd geïmplementeerd, moesten klanten voor klantorders met deposito's die in het POS waren gemaakt hun kaart twee keer doorhalen: één keer om het deposito te betalen en één keer voor tokenisatie van de kaart voor de verdere afhandeling van de order. Wanneer de functie voor tokenisatie voor meerdere kanalen is ingeschakeld, hoeven klanten de kaart nog maar één keer door te halen om het deposito te betalen en het bedrag te betalen voor voor goederen die later worden afgehandeld. Bij afhandeling worden de geautoriseerde fondsen vastgelegd. Voordat de functie voor tokenisatie voor meerdere kanalen was geïmplementeerd, werd er alleen een terugkerend kaarttoken gemaakt voor de verdere afhandeling van orders. Daarom werden de fondsen voor de afhandeling in behandeling niet geautoriseerd en omdat deze fondsen niet werden vastgehouden voor die specifieke aankoop, was de kans minder groot dat deze later konden worden vastgelegd.

> [!NOTE]
> Eén keer doorhalen wordt niet ondersteund Retail 8.1.3. Klantorders in versie 8.1.3 gebruiken dezelfde flow die werd gebruikt voordat de functie voor tokenisatie voor meerdere kanalen werd geïmplementeerd. 

### <a name="cards-that-cant-issue-recurring-card-tokens"></a>Kaarten die geen terugkerende kaarttokens kunnen uitgeven

Sommige kaarten kunnen niet worden gebruikt voor betalingen voor meerdere kanalen omdat deze geen ondersteuning bieden voor het uitgeven van terugkerende kaarttokens. Wanneer een order wordt gemaakt in het POS en het deposito wordt betaald met behulp van een kaart die terugkerende kaarttokens niet ondersteunt, wordt de vorige flow voor de tokenisatie van kaarten gebruikt. Daarom moet een klant die een betaling wil aanbieden die voor de verdere orderafhandeling wordt gebruikt, een tweede kaart aanbieden. Als de tweede kaart geen terugkerende kaarttokens ondersteunt, wordt de actie voor tokenisatie geweigerd en wordt de kassamedewerker gevraagd de klant te vragen om een andere kaart te tonen. 

### <a name="using-a-different-card"></a>Een andere kaart gebruiken

Een klant die bij de winkel komt om een order op te halen, heeft de optie om een andere kaart te gebruiken. Wanneer de kassamedewerker het verzoek **Beschikbare betalingsmethode gebruiken** ontvangt op het moment dat dat de order wordt opgehaald, kan hij of zij vragen of de klant dezelfde kaart wil gebruiken. Als de klant de kaart kwijt is die is gebruikt om de order te maken en de order wil betalen met een andere kaart, kan de kassamedewerker de optie **Een andere betalingsmethode gebruiken**selecteren. Als de klant later terugkomt om meer artikelen voor dezelfde order op te halen en de oorspronkelijke kaartautorisatie nog steeds geldig is, kan de kassamedewerker opnieuw vragen of de klant die kaart wil gebruiken.

### <a name="invalid-authorizations"></a>Ongeldige autorisaties

Als de kaart die is gebruikt om een order te maken niet meer geldig is wanneer producten worden geselecteerd voor ophalen, mislukt de aanvraag voor het vastleggen van de betaling. De POS-betalingsconnector probeert vervolgens een nieuwe autorisatie te maken en vast te leggen met dezelfde kaartgegevens. Als de nieuwe autorisatie of vastlegging mislukt, wordt de kassier ervan op de hoogte gesteld dat de betaling niet kan worden verwerkt. De kassamedewerker moet vervolgens een nieuwe betaling van de klant ontvangen. 

### <a name="multiple-available-payments"></a>Meerdere beschikbare betalingen

Wanneer een order met meerdere betalingsmethoden en meerdere regels wordt opgehaald, ontvangt de kassier eerst de optie **Beschikbare betalingsmethode gebruiken**. Als er meerdere kaarten zijn en de kassamedewerker **Beschikbare betalingsmethode gebruiken** selecteert, worden bestaande regels voor de kaartbetalingsmethode vastgelegd totdat aan het saldo wordt voldaan voor de goederen die momenteel worden opgehaald. De kassamedewerker beschikt niet over de optie om de kaart te selecteren die moet worden gebruikt voor de goederen die worden opgehaald. 

## <a name="related-topics"></a>Verwante onderwerpen

- [Veelgestelde vragen over betalingen](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/payments-retail)
- [Dynamics 365-betalingsconnector voor Adyen](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3)
- [BOPIS configureren in een Dynamics 365 Commerce-evaluatieomgeving](https://docs.microsoft.com/en-us/dynamics365/commerce/cpe-bopis)

