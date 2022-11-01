---
title: Het gebruik van tokens voor betalingen beperken
description: Dit artikel beschrijft de functie waarmee wordt beperkt hoe betalingstokens worden gebruikt in Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 10/20/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-09-20
ms.openlocfilehash: 8092ab0724f33f21759aa84d25e0bdcb5b2ad5dd
ms.sourcegitcommit: 6bd8822f7aa781d596b70956bead834117cf302c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709648"
---
# <a name="limit-payment-token-usage"></a>Het gebruik van tokens voor betalingen beperken

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Dit artikel beschrijft de functie waarmee wordt beperkt hoe betalingstokens worden gebruikt in Microsoft Dynamics 365 Commerce. Het tokengebruik wordt beperkt tot het bereik van een verkooporder of, als toestemming van de klant is verleend, wordt opgeslagen als kaart in een bestand.

## <a name="key-terms"></a>Belangrijke termen

| Voorwaarde | Description |
|---|---|
| Token | Een XML-er waarnaar wordt verwezen in het Dynamics 365-systeem waarin betalingsverwijzingen voor transactionele doeleinden worden opgeslagen. |
| Kaart in bestand | Een kaartverwijzingstoken waarmee is ingestemd voor toekomstig gebruik in het Dynamics 365-systeem of de betalingsgateway en dat specifiek is voor de rekening van een klant. |

De beperkingen op het gebruik van betalingstokens zijn van toepassing op elke omgeving die een gatewayservice gebruikt voor betalingen, waarbij terugkerende tokens worden gehanteerd. De kant-en-klare [Dynamics 365 Payment Connector voor Adyen](adyen-connector.md) gebruikt terugkerende betalingstokens om volgende orderacties uit te voeren, zoals autorisatiecorrecties en herautorisaties.

Om te bepalen hoe deze terugkerende betalingstokens in het gehele systeem worden gebruikt, beperkt de functie **Gebruik van betalingstoken beperken tot ordercontext** het gebruik van een terugkerend token tot het bereik van een verkooporder in het systeem. Wanneer deze functie is ingeschakeld, wordt de gebruikersinterface van Commerce headquarters aangepast door invoerpagina's voor betalingen bij te werken en de mogelijkheid te beperken dat er verwijzingen naar betalingen van klanten kunnen worden geselecteerd die in nieuwe transactie-exemplaren kunnen worden gebruikt.

Deze functie helpt bij het voldoen aan gebruiksregels van sommige kaartuitgevers voor betalingen, zoals Visa. In de [Visa Core Rules en Visa Product- en serviceregels](https://usa.visa.com/content/dam/VCOM/download/about-visa/visa-rules-public.pdf) geeft Visa aan dat het gebruik van tokens van betalingen moet worden beperkt tot het bereik van een transactie, tenzij de kaarthouder anders akkoord gaat.

De functie **Gebruik van betalingstoken beperken tot ordercontext** is alleen relevant als u een gatewayservice gebruikt voor betalingen die zich bedient van verwijzingen met terugkerende tokens.

## <a name="enable-the-feature"></a>De functie inschakelen

Als u de functie **Gebruik van betalingstoken beperken tot ordercontext** wilt inschakelen, gaat u in Commerce headquarters voor uw omgeving naar **Werkruimten \> Functiebeheer**, zoekt en selecteert u **Gebruik van betalingstoken beperken tot ordercontext** in de lijst en selecteert u vervolgens **Nu inschakelen**.

## <a name="limit-payment-token-usage"></a>Het gebruik van tokens voor betalingen beperken

Wanneer de functie is ingeschakeld, wordt bijgewerkt hoe wordt verwezen naar klantbetalingsmethoden die zich in bestand bevinden voor de klant. Dit gebeurt op de Commerce headquarters-pagina's voor het vastleggen van betalingsmethoden. Deze bijwerking heeft voornamelijk gevolgen voor twee bewerkingsgebieden:

- Hoe een klantkaart in bestand namens een klant wordt ingevoerd
- Hoe betalingsgegevens voor een klant worden opgeslagen voor toekomstige betalingsinvoer voor verkooporders

Wanneer een klant transacties uitvoert met Commerce-kanalen, worden betalingsgegevens opgeslagen in een verkoopordercontext. De verkoopordercontext beperkt het betalingstoken zodat dit niet wordt gebruikt als betalingsverwijzing voor de klantrecord op betalingspagina's voor nieuwe of bewerkte verkooporderbetalingen in Commerce headquarters.

### <a name="payment-form-changes"></a>Betalingsformulierwijzigingen

Wanneer een gebruiker van een callcenter of Commerce headquarters een betaling voor een klant aanneemt voor een verkooporder, worden op de betalingspagina selectiedetails voor de betalingsmethode getoond. Wanneer de functie **Gebruik van betalingstoken beperken tot ordercontext** is ingeschakeld, worden alleen opgeslagen 'kaart in bestand'-records weergegeven als een gebruiker het plusteken (**+**) op de betalingspagina selecteert. Bij wijzigingen moet de gebruiker van callcenter of Commerce headquarters de volledige betalingsgegevens invoeren die de klant heeft verstrekt bij het invullen van de pagina **Klantbetalingsgegevens invoeren** voor de nieuwe verkoopordertransactie.

De lijst met waarden voor het veld **Nummer** bevat alleen kaartverwijzingen die zijn gekoppeld aan de klant die de kaart in bestand heeft. Het filtert eventuele eerdere betalingsverwijzingen weg die niet binnen het bereik van een verkooporder vallen.

Het plusteken (**+**) onder het veld **Nummer** blijft beschikbaar en kan worden gebruikt om de betalingsgegevens in te voeren die de klant heeft opgegeven voor de transactie die is gekoppeld aan de verkooporder die wordt verwerkt.

### <a name="how-cards-on-file-work"></a>Hoe kaarten in bestand functioneren

Wanneer de functie **Gebruik van betalingstoken beperken tot ordercontext** is ingeschakeld, is een kaart in bestand een token voor terugkerende betalingen dat wordt opgeslagen voor een klantrecord en niet is beperkt tot het bereik van een verkooporder. Met een kaart in bestand kunnen gebruikers van Commerce headquarters snel naar informatie verwijzen wanneer ze de betalingspagina voor een nieuwe verkooporderbetaling invullen. Deze tokenverwijzing is alleen van toepassing in de Dynamics 365-omgeving. Voor online kanalen waarbij een betalingsgatewayservice wordt gebruikt waarmee gebruikers een betalingsmethode kunnen opslaan voor toekomstig gebruik in de iFrame-betalingsmodule, slaat de betalingsgateway deze verwijzingen veilig op als afzonderlijke verwijzing naar de Dynamics 365-kaart in bestand.

Als de Dynamics 365 Commerce Payment Connector voor Adyen bijvoorbeeld wordt gebruikt in een online kanaal, zien klanten die hun creditcardgegevens in de iFrame-betalingsmodule invoeren, alleen de opgeslagen kaartverwijzingen van de gatewayservice voor de volgende online aankoop wanneer ze worden geverifieerd. Ze zien de opgeslagen kaart in bestand van de Dynamics 365-omgeving niet als een optie in de iFrame-betalingsmodule. Evenzo, wanneer een klant een order via het callcenter plaatst, worden online opgeslagen kaartverwijzingen van de klant niet als opties getoond aan de callcentergebruiker. De callcentergebruiker ziet alleen vorige verwijzingen voor kaart in bestand uit het Dynamics 365-systeem (zoals is overeengekomen met de klant) om deze op te slaan voor toekomstige orders.

Gebruikers van Commerce headquarters kunnen een kaart in bestand opslaan voor een klant door naar **Retail en Commerce \> Klanten** te gaan en de rekeningrecord van de klant te selecteren. In de sectie **Klant \> Instellen** kunnen gebruikers die machtigingen hebben om de betalingspagina's te verwerken, de invoerpagina **Creditcards** gebruiken om een betalingskaart in te voeren die in bestand zal worden opgeslagen voor toekomstige transacties. Deze bewerking helpt u tijd te besparen wanneer toekomstige betalingen van verkooporders voor de klant worden verwerkt. Callcenter- en Commerce headquarters-gebruikers moeten de kaartdetails voor de kaart in bestand alleen invoeren als de klant akkoord gaat met het gebruik van de kaartverwijzing voor toekomstige transacties.

Met een selectievakje **Opslaan voor toekomstig gebruik** onder aan de betalingspagina's van Commerce headquarters kunnen gebruikers de kaart in bestand opslaan voor toekomstig gebruik. Dit selectievakje moet alleen worden gebruikt als de klant akkoord gaat om de kaart in bestand te gebruiken voor toekomstige transacties. U kunt het selectievakje **Opslaan voor toekomstig gebruik** tonen of beperken met de optie **Klantkaart in bestand toestaan** op het tabblad **Betaling** van de pagina **Parameters van callcenter** in Commerce headquarters. Als deze optie is ingesteld op **Ja**, kunnen gebruikers van Commerce headquarters die machtigingen hebben om betalingspagina's te verwerken, een kaart in bestand opslaan via het selectievakje **Opslaan voor toekomstig gebruik**. Wanneer de optie is ingesteld op **Nee**, is het selectievakje niet beschikbaar voor gebruikers van Commerce headquarters die machtigingen hebben om betalingspagina's te verwerken. De optie **Klantkaart in bestand toestaan** kan worden gebruikt als uw bedrijf het gebruik van terugkerende tokens in Commerce headquarters wil beperken, maar nog niet wil toestaan dat een kaart in bestand opgeslagen wordt zonder procedure om te verzekeren dat de toestemming door de klant wordt verleend.

### <a name="commerce-headquarters-pages-where-the-recurring-token-restrictions-are-enforced"></a>Commerce headquarters-pagina's waar de terugkerende tokenbeperkingen worden afgedwongen

Bereik voor tokens is van invloed op de volgende gebieden in Commerce headquarters als deze functie is ingeschakeld:

- Klantbetalingsgegevens bij **Verkooporder \> Betalingen \> Klantbetaling invoeren**
- Continuïteitsorders
- Termijnbetalingen
- Creditcardbetalingen in Klanten

### <a name="manage-payment-tokens-archiving-or-removal"></a>Betalingstokens beheren (archiveren of verwijderen)

Betalingstokens die zijn gemaakt voordat de functievlag **Gebruik van betalingstoken beperken tot ordercontext** werd ingeschakeld (of terwijl de functie was uitgeschakeld) blijven 'zonder bereik' in het systeem en er kan naar worden verwezen in selectielijsten op de betalingspagina van Commerce headquarters. Deze tokens kunnen op twee manieren in Commerce headquarters worden verwijderd:

- Gebruik de pagina **Creditcardtransactie archiveren** om een taak in te stellen die de betalingstokens regelmatig opschoont of archiveert. Als u de optie **Gegevens verwijderen zonder archivering** op **Ja** instelt, worden de tokens die voldoen aan de instelling **Minimale ouderdom van transactie (in dagen)** verwijderd. Zie [Gegevens van creditcardtransacties archiveren](archive-cc-data.md) voor meer informatie.
- Gebruik de nieuwe pagina **Creditcardtokens opschonen** (**Klanten \> Query's en rapporten \> Opschonen \> Creditcardtokens opschonen**). Hiermee kunt u een batchtaak uitvoeren of instellen waarmee betalingstokens worden verwijderd. Stel de volgende parameters in:

    - De waarde **Minimale ouderdom van token in dagen** moet 90 dagen of meer zijn.
    - Met de **Op de achtergrond uitvoeren**-instellingen kunt u instellingen voor **Terugkeerpatroon** of **Waarschuwingen** definiëren.
    - U kunt een batchgroep toewijzen om de taak uit te voeren voor een specifieke groep.
    - Als de optie **Privé** is ingesteld op **Ja**, kan alleen de gebruiker die de taak maakt, deze uitvoeren.
    - Met de instelling **Ja** voor de optie **Kritieke taak** wordt ervoor gezorgd dat de status van de taak actief door het systeem wordt bijgehouden.

Verwijderde tokens kunnen niet worden opgehaald. Stel het veld **Minimale ouderdom van token in dagen** in op een bereik dat past bij de langste transactionele levensduur voor uw omgeving (van autorisatie tot vastleggen of restitutie).

## <a name="additional-resources"></a>Aanvullende bronnen

[Veelgestelde vragen over betalingen](payments-retail.md)

[Kassamodule](../add-checkout-module.md)

[Betalingsmodule](../payment-module.md)
