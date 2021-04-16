---
title: Methoden voor restitutiebetalingen in callcenters
description: In dit onderwerp wordt uitgelegd hoe restituties worden gegenereerd via callcenters wanneer retouren worden gemaakt of wanneer orders of orderregels worden geannuleerd.
author: hhainesms
ms.date: 01/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: e3837ccebca0e6644ac5ded98344a5135cfb5d7a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799584"
---
# <a name="refund-payment-processing-in-call-centers"></a>Methoden voor restitutiebetalingen in callcenters

In dit onderwerp wordt uitgelegd hoe restituties worden gegenereerd via callcenters wanneer retouren worden gemaakt of wanneer orders of orderregels worden geannuleerd.

Een gebruiker die als callcentergebruiker in Microsoft Dynamics 365 Commerce Headquarters een retourorder voor een klant maakt, gebruikt de pagina **Retourorder** om de initiële retourmaterialenautorisatie (RMA) te maken. De RMA definieert de producten die de klant wil retourneren of ruilen, en maakt een gekoppelde retourverkooporder met het ordertype **Geretourneerde order**. Deze gekoppelde retourorder wordt gebruikt om de boeking van de geretourneerde voorraad en eventuele creditnota's of restitutiebedragen die worden geboekt bij te houden.

Als de optie **Ordervoltooiing inschakelen** is ingesteld op **Ja** voor het callcenterkanaal, moet de callcentergebruiker die de RMA maakt, de verwerkingsstroom voor ordervoltooiing uitvoeren door **Voltooien** op de pagina **Retourorder** te selecteren. De functie **Voltooien** geeft een berekend retouroverzicht met het verschuldigde restitutiebedrag. Bovendien maakt het, wanneer het juist is geconfigureerd, systematisch een restitutiebetalingsregel voor de geretourneerde order.

De logica van het callcenter bepaalt de betalingswijze voor de restitutiebetalingsregel op basis van de betalingswijze die is gebruikt voor de oorspronkelijke order. Als deze retourorder niet aan een oorspronkelijke order is gekoppeld, wordt een standaardbetalingswijze toegepast die afkomstig is uit een systeemparameter.

## <a name="how-a-call-center-determines-which-payment-method-to-apply-to-a-return-order"></a>Hoe een callcenter bepaalt welke betalingswijze op een retourorder moet worden toegepast

Het callcenter gebruikt de betalingswijze van de oorspronkelijke order om de betalingswijze te bepalen die moet worden toegepast op een retourorder. Hierna volgt de procedure voor de volgende oorspronkelijke betalingswijzen:

- **Normaal** (contant) of **Cheque**: wanneer een retourorder die is gemaakt, verwijst naar een oorspronkelijke order die is betaald met de normale betalingswijze (contant) of met een cheque, verwijst de callcentertoepassing naar configuraties op de pagina **Restitutiemethoden van callcenter**. Met deze pagina kunnen organisaties in ordervaluta definiëren hoe restituties aan klanten worden gedaan voor orders die oorspronkelijk zijn betaald met de normale betalingswijze of met een cheque. Via de pagina **Restitutiemethoden van callcenter** kunnen organisaties ook selecteren of een door het systeem gegenereerde restitutiecheque naar de klant wordt verzonden of dat er een klanttegoed wordt gemaakt voor het interne klantaccountsaldo. In deze scenario's verwijst de callcenterlogica naar de valuta van de retourorder en gebruikt ze vervolgens de waarde van de **Betalingswijze detailhandel** voor die valuta om een restitutiebetalingsregel op de retourverkooporder te maken. Later wordt een klantbetalingsjournaal voor klanten (AR) dat de toegewezen AR-betalingsmethode gebruikt, aan de valuta gekoppeld.

    De volgende illustratie toont de configuratie voor een scenario waarin een klant producten retourneert van een verkooporder die is gekoppeld aan de valuta USD, en die oorspronkelijk is betaald met de normale of cheque betalingswijze. In dit scenario wordt een restitutie aan de klant gedaan via een door het systeem gegenereerde restitutiecheque. De AR-betalingsmethode **REF-CHK** is geconfigureerd als betalingstype voor de restitutiecheque.

    ![Configuratie van restitutiemethoden in het callcenter voor normale betalingen en betalingen met cheques](media/callcenterrefundmethods.png)

- **Creditcard**: wanneer een gemaakte retourorder verwijst naar een oorspronkelijke order die met een creditcard is betaald, past de callcenter-logica voor restitutiebetalingen dezelfde oorspronkelijke creditcard toe op de retourorder.
- **Klantenkaart**: wanneer een gemaakte retourorder verwijst naar een oorspronkelijke order die met een klantenkaart is betaald, past de callcenter-logica voor restitutiebetalingen de restitutie toe op dezelfde klantenkaart.
- **Cadeaubon** (intern): wanneer een gemaakte retourorder verwijst naar een oorspronkelijke order die is betaald met een cadeaubon die is uitgegeven vanuit Dynamics 365 Commerce (interne cadeaubonfunctionaliteit), past de callcenterlogica voor restitutiebetalingen de restitutie toe op hetzelfde oorspronkelijke cadeaubonnummer.
- **Cadeaubon** (extern): wanneer een gemaakte retourorder verwijst naar een oorspronkelijke order die is betaald met een externe cadeaubon van een derde partij, past de callcenterlogica voor restitutiebetalingen de standaard betalingswijze voor retourzendingen toe die is gedefinieerd op het tabblad **RMA/Retour** van de pagina **Callcenter-parameters**.

Als de oorspronkelijke betalingswijze van de order om welke reden dan ook onbekend is, of als er meerdere betalingswijzen zijn gebruikt om de oorspronkelijke order te betalen, past de callcenterlogica de standaard restitutiebetalingswijze toe die is gedefinieerd op het tabblad **RMA/Retour** van de pagina **Callcenter-parameters**.

In de volgende afbeelding ziet u het veld **Betalingswijze** op het tabblad **RMA/Retour** van de pagina **Callcenter-parameter**.

![Het veld Betalingswijze op het tabblad RMA/Retour van de pagina Callcenter-parameter](media/callcenterrefundparameters.png)

> [!NOTE]
> De restitutieverwerkingsregels die eerder zijn beschreven, zijn ook van toepassing op orders of orderregels die een callcentergebruiker in Commerce Headquarters annuleert. Als door het annuleren van een order of bepaalde orderregels overbetalingen ontstaan, worden dezelfde regels gebruikt om betalingsregels voor restituties te genereren.

Normaal gesproken wordt bij een retourorder een standaardproces uitgevoerd, waarbij voorraad wordt ontvangen (of wordt geboekt als uitval), een pakbon wordt geboekt op de retourorder en er vervolgens een factuurboekingsproces wordt uitgevoerd voor de retourverkooporder. De retourverkooporder wordt gekoppeld en systematisch gegenereerd als onderdeel van het maken van de retourorder. In normale scenario's worden restituties pas aan klanten gedaan als de factuur voor de retourverkooporder is geboekt.

### <a name="what-happens-when-an-invoice-is-posted-on-a-return-sales-order"></a>Wat gebeurt er wanneer een factuur wordt geboekt op een retourverkooporder?

In de volgende scenario's wordt uitgelegd wat er gebeurt wanneer een factuur wordt geboekt op een retourverkooporder:

- Als de restitutie op de retourorder voor een creditcard is, wordt extra logica aangeroepen wanneer de factuur wordt geboekt. Deze logica belt de betalingsverwerker om de restitutie op de creditcard van de klant te doen. Er wordt ook een boekstuk voor de restitutie gemaakt en door het systeem geboekt op de rekening van de klant. Dit betalingsjournaal zal worden verrekend met het boekstuk voor de retouropdracht.
- Als de restitutie voor het betalingstype cheque is, wordt een boekstuk voor de klant gemaakt die de AR-betalingswijze gebruikt en die handmatig moet worden geboekt of afgedrukt voordat het boekstuk op de klantrekening kan worden geboekt. Om de restitutiecheque te verwerken, kunnen gebruikers ofwel de pagina **Journaal met betalingen van klant** in Klanten of de gespecialiseerde pagina **Verwerking van restitutiecheque** in Retail and Commerce gebruiken.
- Als de restitutiebetaling die moet worden gedaan betrekking heeft op het interne betalingstype cadeaubon of klantenkaart, wordt bij de facturering van de retourorder het boekstuk voor de restitutiebetaling gemaakt en geboekt op de klantenrekening. Deze factureringsstap telt het restitutiebedrag ook weer op bij het intern bijgehouden cadeaubon- of klantenkaartsaldo van de klant.
- Als een betalingswijze die gebruikmaakt van de functie **Klant** (bijvoorbeeld een klantaccount), is gekoppeld aan de retourverkooporder, worden kredietlimietvalidaties genegeerd wanneer de betaling wordt verwerkt. Er wordt in deze context geen boekstuk gemaakt of geboekt. Wanneer een klantbetalingstype wordt gebruikt op een retourorder, dient het creditnotaboekstuk dat tijdens het factuurboekingsproces is gemaakt als het creditboekstuk van de klant en geeft het een restitutie ten goede van het AR-saldo van de klant aan.

## <a name="advance-credit"></a>Voorschotcredit

Wanneer een gebruiker retouropdrachten verwerkt als callcentergebruiker in een callcenter waar de optie **Ordervoltooiing inschakelen** is ingesteld op **Ja**, kan er een uitzondering op het eerder beschreven proces voor het boeken van de restitutiebetaling optreden als de callcentergebruiker die de retouropdracht maakt, de optie **Krediet vooraf** instelt op **Ja** op het tabblad **RMA/Retour** van de pagina **Callcenterparameters**. In dit geval vindt de restitutie plaats onmiddellijk nadat de retouropdracht is ingediend met behulp van de functie **Indienen** op de pagina **Retourenoverzicht**. Het systeem maakt onmiddellijk een voorschotbon voor de retourwaarde, ook al is de retourverkooporder zelf nog niet gefactureerd. Deze aanpak kan worden gebruikt in situaties waarin een organisatie vooraf restituties aan klanten moet uitbetalen wegens problemen met de klantenservice, en niet wil dat de geretourneerde inventaris ontvangen wordt voordat de restituties zijn uitbetaald.

## <a name="replacement-orders"></a>Vervangingsorders

Wanneer een retourorder wordt uitgegeven, kan de functie **Vervangende order** worden gebruikt om een nieuwe verkooporder voor de klant te genereren. Deze aanpak kan worden gebruikt in ruilscenario's. De functie **Vervangende order** maakt een andere verkooporder voor de nieuwe artikelen die moeten worden verzonden, maar een kruisverwijzingskoppeling op het tabblad **RMA/Retour** van de pagina **Callcenterparameters** koppelt de vervangende order, de RMA en de geretourneerde verkooporder.

Wanneer betalingen voor een vervangingsorder worden verwerkt, hebben organisaties twee opties:

- De klant terugbetalen voor de retourorder op basis van de oorspronkelijke betalingswijze, en vervolgens een afzonderlijke betaling voor de vervangingsorder innen. Er is geen extra configuratie vereist om deze optie te gebruiken.
- Zet de optie **Creditering toepassen** op **Ja** op het tabblad **RMA/Retour** van de pagina **Callcenterparameters**. In dit geval wordt een klantbetalingswijze systematisch toegepast op zowel de retourorder als de vervangingsorder. Met deze optie voorkomt u dat externe restituties worden uitgegeven. Hiermee voorkomt u ook dat een betaling op de transactie wordt verwerkt. Dit kan nuttig zijn in situaties waarin een gelijke omruiling wordt verwerkt en de organisatie er de voorkeur aan geeft de creditnota die bij de facturering van de retouropdracht wordt gegenereerd, te gebruiken om de factuur te betalen die door de vervangingsorder wordt gegenereerd. Wanneer de optie **Creditering toepassen** op **Ja** is ingesteld, moet de organisatie de creditnota handmatig verrekenen met de factuur van de vervangingsorder nadat deze beide financiële documenten zijn gegenereerd.

De instelling **Ja** voor de optie **Creditering toepassen** is alleen van toepassing wanneer de retourorder aan een vervangingsorder wordt gekoppeld. In dit geval wordt de betalingswijze van de klant die wordt gebruikt om systematisch voor de retour- en ruilorder te betalen, gedefinieerd door het veld **Betalingswijze voor creditering toepassen** op het tabblad **RMA/Retour** van de pagina **Callcenterparameters**. Alleen een betaling van het type **Klant** kan in dit veld worden geselecteerd.

> [!NOTE]
> Voor een retourorder die geen gekoppelde vervangingsorder heeft, heeft de instelling **Ja** voor de optie **Creditering toepassen** geen effect op de betalingslogica van de retourorder, omdat deze instelling alleen geldt voor vervangingsorders.

![Het veld Betalingswijze voor creditering toepassen op het tabblad RMA/Retour van de pagina Callcenterparameter](media/callcenterrefundparameters1.png)

> [!IMPORTANT]
> Als gebruikers die vervangingsorders maken van plan zijn de optie **Creditering toepassen** te gebruiken, moeten zij de functie **Voltooien** niet op de vervangingsorder uitvoeren voordat zij de optie **Creditering toepassen** op **Ja** hebben gezet. Nadat de functie **Voltooien** is uitgevoerd, wordt de restitutiebetaling berekend en toegepast op de retourverkooporder. Elke poging om de optie **Creditering toepassen** op **Ja** te zetten nadat een restitutiebetaling reeds is berekend en toegepast, leidt niet tot een herberekening van de restitutiebetaling, en de betalingswijze die is geselecteerd in het veld **Betalingswijze voor creditering toepassen**, wordt niet toegepast. Als de optie **Creditering toepassen** in deze context moet worden gebruikt, moet de gebruiker de vervangingsorder en de RMA verwijderen en een nieuwe RMA maken. Op dit moment moet de gebruiker controleren of de optie **Creditering toepassen** is ingesteld op **Ja** voordat de functie **Voltooien** wordt uitgevoerd.

## <a name="payment-overrides-for-call-center-returns"></a>Overschrijving van betalingen voor retourzendingen van callcenters

Hoewel de callcenterlogica systematisch de betalingswijze voor de restitutie bepaalt op de manier die eerder in dit onderwerp is beschreven, willen gebruikers die betalingen soms overschrijven. Een gebruiker kan bijvoorbeeld bestaande betalingsregels voor restituties bewerken of verwijderen en nieuwe betalingsregels toepassen. Door het systeem berekende restitutiebetalingen kunnen alleen worden gewijzigd door gebruikers met de juiste overschrijvingsmachtigingen. Deze machtigingen kunnen worden geconfigureerd op de pagina **Overschrijvingsmachtigingen** in Retail en Commerce. Om een restitutiebetaling te overschrijven, moet de gebruiker gekoppeld zijn aan een beveiligingsrol waarbij de optie **Alternatieve betaling toestaan** op **Ja** staat op de pagina **Overschrijvingsmachtigingen**.

![De optie Alternatieve betaling toestaan op de pagina Overschrijvingsmachtigingen](media/overridepermissions.png)

Als alternatief kan een organisatie op het tabblad **RMA/Retour** van de pagina **Callcenterparameters** de optie **Betalingsoverschrijving toestaan** op **Ja** zetten. In dat geval moet in het veld **Beveilgingsoverschrijvingscode** een overschrijvingscode worden geselecteerd. De code voor het overschrijven van beveiliging is een alfanumerieke code die extern moet worden beheerd, omdat gebruikers deze niet kunnen weergeven in Commerce Headquarters nadat deze is ingesteld. De code voor het overschrijven van de beveiliging mag slechts bij enkele belangrijke vertrouwde personen in een organisatie bekend zijn. Als de optie **Betalingsoverschrijving toestaan** is ingesteld op **Ja**, dan kunnen gebruikers die niet de juiste rolmachtigingen hebben, de betalingswijze van een retourorder wijzigen door de beveiligingsoverschrijvingscode in te voeren. Als ze deze niet weten of als een manager of leidinggevende het niet voor hen kunnen invoeren, kunnen ze de betalingswijze voor retouren niet overschrijven.

> [!NOTE]
> Als de beveiligingsoverschrijvingscode is kwijtgeraakt of vergeten, moet de organisatie deze opnieuw instellen door een nieuwe overschrijvingscode te definiëren in het veld **Beveiligingsoverschrijvingscode** op het tabblad **RMA/Retour** van de pagina **Callcenterparameters**.

![Overschrijvingsparameters voor betalingen op het tabblad RMA/Retour van de pagina Callcenterparameters](media/overridepaymentparameter.png)

> [!IMPORTANT]
> Voordat organisaties restitutiebetalingen willen overschrijven die als betalingstype creditcards gebruiken, moeten ze controleren of hun creditcardverwerker niet-gekoppelde retouren toestaat. Veel verwerkers vereisen dat restituties worden teruggeboekt naar de oorspronkelijke kaart. Elke poging om restitutie van een creditcard te verstrekken die geen eerdere gegevens heeft, kan leiden tot boekingsfouten bij de verwerker.

## <a name="additional-resources"></a>Aanvullende bronnen

[Betalingsmethoden in callcenters](work-with-payments.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]