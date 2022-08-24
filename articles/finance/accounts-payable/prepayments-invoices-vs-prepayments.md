---
title: Vooruitbetalingsfacturen versus vooruitbetalingen
description: In dit artikel worden de twee methoden beschreven en vergeleken die organisaties kunnen gebruiken voor voorschotten (vooruitbetalingen).
author: abruer
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, PurchTable
audience: Application User
ms.reviewer: twheeloc
ms.custom: 15871
ms.assetid: a0bb5220-73d4-48ae-84d0-46a171c224fa
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 901683f2176189ce2f4186b4f9b3b5c64ec9f2b1
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2022
ms.locfileid: "9227770"
---
# <a name="prepayment-invoices-vs-prepayments"></a>Vooruitbetalingsfacturen versus vooruitbetalingen

[!include [banner](../includes/banner.md)]

In dit artikel worden de twee methoden beschreven en vergeleken die organisaties kunnen gebruiken voor voorschotten (vooruitbetalingen). Met één methode maakt u een aanbetalingsfactuur die aan een inkooporder is gekoppeld. Met de andere methode maakt u journaalboekstukken van vooruitbetaling door boekingen in een journaal te maken en ze als journaalboekstukken van vooruitbetaling te markeren.

Organisaties kunnen aanbetalingen (vooruitbetalingen) verzenden naar leveranciers voor goederen of services voordat deze goederen of services zijn afgehandeld. Voor het verzenden van vooruitbetalingen naar leveranciers kunnen twee methoden worden gebruikt. Om risico's te minimaliseren, kunt u vooruitbetalingen bijhouden door de vooruitbetaling op een inkooporder te definiëren. Voor deze methode moet u een aanbetalingsfactuur maken die aan een inkooporder is gekoppeld. Deze methode wordt aanbetalingsfacturering genoemd. Organisaties die vooruitbetalingen niet zo nauwgezet willen bijhouden of geen vooruitbetalingsfactuur van hun leverancier ontvangen, kunnen journaalboekstukken voor vooruitbetalingen gebruiken in plaats van de vooruitbetalingsfactureringsmethode. U kunt journaalboekstukken van vooruitbetaling maken door boekingen in een journaal te maken en ze als journaalboekstukken van vooruitbetaling te markeren. Bij deze methode kunt u niet bijhouden welke vooruitbetalingen aan een leverancier worden uitgevoerd en voor welke inkooporders. U kunt echter wel een geboekte vooruitbetaling voor vereffening voor een inkooporder markeren.

## <a name="when-to-use-prepayment-invoicing-vs-prepayments"></a>Gebruik van vooruitbetalingsfacturering versus vooruitbetalingen

| Vooruitbetalingsfacturering                                                                | Vooruitbetalingen                                                              |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Definieer een vooruitbetalingswaarde op de inkooporder.                                    | Er is geen vooruitbetalingswaarde op de inkooporder gedefinieerd.                    |
| Een vooruitbetalingsfactuur en een definitieve factuur moeten worden geboekt.                       | Er moet geen vooruitbetalingsfactuur worden geboekt.                                    |
| Aansprakelijkheid voor de vooruitbetaling maakt deel uit van de vooruitbetalingsrekening, niet de leveranciersrekening. | Aansprakelijkheid voor de vooruitbetaling maakt deel uit van de leveranciersrekening.                  |
| Het leverancierssaldo weerspiegelt niet de vooruitbetalingswaarde in het hele proces.     | Het leverancierssaldo weerspiegelt de vooruitbetalingswaarde in het hele proces. |
| Vooruitbetalingsfacturering is alleen beschikbaar in Leveranciers.                         | Vooruitbetalingen zijn beschikbaar in Klanten en Leveranciers.    |

## <a name="overview-of-the-prepayment-process"></a>Overzicht van het vooruitbetalingsproces
Bij de boekhouding in veel landen/regio´s is het vereist dat vooruitbetalingen van een klant of aan een leverancier niet naar de gewone totaalrekeningen voor de klant of de leverancier worden geboekt. In plaats daarvan worden deze vooruitbetalingen geboekt naar speciale grootboekrekeningen voor vooruitbetalingen. Wanneer een verkooporder of inkooporder wordt gemaakt, wordt een factuur naar de klant of van de leverancier gestuurd. Wanneer de factuur wordt betaald, wordt het vooruitbetalingsboekstuk voor de vooruitbetaling en btw op de vooruitbetalingsgrootboekrekeningen omgekeerd, en de factuurbedragen worden automatisch naar de gewone totaalrekeningen geboekt. Volg deze stappen om een vooruitbetaling te maken.

1.  Stel boekingsprofielen voor vooruitbetalingen in.
2.  Selecteer in Parameters van module Klanten en Parameters van module Leveranciers onder **Grootboek en btw** het nieuwe boekingsprofiel door de parameter **Boekingsprofiel voor betalingsjournaal met vooruitbetaling** te gebruiken.
3.  Maak een betalingsjournaal en vervolgens de nieuwe betaling.
4.  U kunt de betaling als vooruitbetaling markeren. Als een betaling als vooruitbetaling wordt gemarkeerd, wordt de betaling geboekt naar de grootboekrekeningen die zijn gedefinieerd in het boekingsprofiel dat u in stap 1 en 2 hebt ingesteld. Bovendien, als de betaling als vooruitbetaling wordt gemarkeerd, wordt de btw berekend. Sommige overheidsinstellingen vereisen dat de btw wordt betaald wanneer een vooruitbetaling wordt geregistreerd, zelfs als er geen factuur is.
5.  Boek de vooruitbetaling.
6.  Optioneel: u kunt de vooruitbetaling vereffenen met de inkooporder of verkooporder voordat u de factuur maakt. Gebruik op de verkooporder- of inkooporderpagina in het actievenster **Transacties vereffenen**.
7.  Nadat de leverancier de goederen of services heeft geleverd, registreert u de factuur. Als u de vooruitbetaling voor de inkooporder of de verkooporder in stap 6 hebt vereffend, wordt de vooruitbetaling automatisch vereffend voor de factuur die u hebt gemaakt. Als u de vooruitbetaling niet voor de inkooporder of de verkooporder hebt vereffend, kunt u deze handmatig vereffenen voor de factuur door **Transacties vereffenen** op de klant- of leverancierspagina te gebruiken. Het vooruitbetalingsbedrag wordt vervolgens teruggeboekt uit de tijdelijke klant- of leveranciersgrootboekrekening. Bovendien, als btw is berekend, wordt deze teruggeboekt, omdat de factuur de werkelijke btw heeft.

## <a name="overview-of-the-prepayment-invoicing-process"></a>Overzicht van het vooruitbetalingsfactureringsproces
Vooruitbetalingsfacturen worden veel in het bedrijfsleven gebruikt. Een leverancier maakt vooruitbetalingsfacturen om een voorschot voor de aankoop te vereisen voordat de inkooporder is vervuld. Een leverancier kan bijvoorbeeld een vooruitbetaling eisen voor aangepaste goederen of services. Als een leverancier een factuur uitgeeft voor vooruitbetaling, kunt u de functie voor vooruitbetalingsfacturering gebruiken. Een vooruitbetalingswaarde kan op de inkooporder worden gedefinieerd, een vooruitbetalingsfactuur wordt geregistreerd en betaald, en vervolgens wordt de vooruitbetalingsfactuur toegepast op de uiteindelijke factuur. Volg deze stappen om een vooruitbetaling te maken.

1.  De inkoopmedewerker maakt, bevestigt en verzendt een inkooporder waarvoor de leverancier een vooruitbetaling heeft gevraagd. De vooruitbetalingswaarde wordt gedefinieerd op de inkooporder als onderdeel van de overeenkomst.
2.  De leverancier geeft een vooruitbetalingsfactuur uit.
3.  De leverancierscoördinator registreert de vooruitbetalingsfactuur tegen de inkooporder en vervolgens wordt de vooruitbetalingsfactuur betaald.
4.  De leverancier verzendt een betalingsverzoek, ook wel een standaardleveranciersfactuur genoemd. Nadat de leverancier de goederen of services heeft geleverd en de bijbehorende standaardleveranciersfacturen zijn ontvangen, past de leverancierscoördinator het vooruitbetalingsbedrag toe dat al is betaald voor de standaardfactuur.
5.  De leverancierscoördinator betaalt en vereffent het resterende bedrag van de standaardfactuur.

## <a name="set-up-parameters-to-enable-the-prepayment-invoicing-process"></a>Parameters instellen om het factureringsproces voor vooruitbetalingen in te schakelen
Er moet een vooruitbetalingsrekening worden gedefinieerd op het tabblad **Inkooporder** van de pagina **Voorraadboeking** (**Voorraadbeheer \> Instellingen \> Boeking \> Boeking**). De vooruitbetalingsrekening wordt bijgewerkt, meestal gedebiteerd, wanneer de vooruitbetalingsfactuur wordt geboekt. Het saldo in de vooruitbetalingsrekening wordt teruggeboekt bij boeking van de standaardfactuur die op de vooruitbetalingsfactuur wordt toegepast. Als u de vooruitbetalingsfactuur niet vereffent met een betaling voordat u de vooruitbetalingsfactuur toepast op de standaardfactuur, worden de boekhoudposten van de geboekte vooruitbetalingsfactuur teruggeboekt wanneer de standaardfactuur wordt geboekt.

De totaalrekening voor verrekening voor crediteuren wordt gedefinieerd in het **boekingsprofiel van leveranciers**. Als u het standaardboekingsprofiel wilt definiëren, klikt u op **Leveranciers \>Instellingen \> Parameters van module Leveranciers \>tabblad Grootboek en btw \> Boekingsprofiel met leveranciersfactuur voor vooruitbetaling**.

Het **beleid voor aanbetalingsaanvragen** geeft aan of het systeem vereffende vooruitbetalingsfacturen automatisch toepast op de eindfactuur die handmatig is gemaakt. Facturen die worden gemaakt met behulp van een gegevensentiteit, verwijzen niet naar het **beleid voor aanbetalingsaanvragen**. U moet vereffende vooruitbetalingsfacturen handmatig toepassen op facturen die zijn gemaakt met behulp van een gegevensentiteit. Als u het beleid wilt definiëren, gaat u naar **Leveranciers \>Instellingen \> Parameters van module Leveranciers \> tabblad Grootboek en btw \> Beleid voor aanbetalingsaanvragen**. Als het veld **Beleid voor aanbetalingsaanvragen** is ingesteld op **Automatisch**, wordt de vooruitbetalingsfactuur automatisch gemarkeerd voor vereffening met de eindfactuur. Als het veld is ingesteld op **Melding**, wordt een visuele indicatie weergegeven dat een vooruitbetalingsfactuur kan worden aangevraagd wanneer de eindfactuur wordt gemaakt.

## <a name="create-a-purchase-order-that-contains-prepayment-invoice-information"></a>Een inkooporder maken die vooruitbetalingsfactuurgegevens bevat
Wanneer een leverancier u vertelt dat ze een aanbetaling willen ontvangen voor goederen en services op een inkooporder, moet u de vooruitbetalingswaarde voor de gekoppelde inkooporder definiëren. Ga naar **Leveranciers \> Algemeen \> Inkooporders \> Alle inkooporders** en zoek de inkooporder van de leverancier. Selecteer het tabblad **Inkoop** in het actievenster en selecteer **Vooruitbetaling**. Voer gegevens in voor de vooruitbetaling, waaronder een beschrijving, de waarde van de vooruitbetaling, of de vooruitbetaling een vast bedrag of een percentage is en een categorie-id voor de vooruitbetaling. 

U kunt niet meerdere vooruitbetalingen definiëren in een inkooporder. Als u meerdere vooruitbetalingen in een inkooporder wilt toestaan, boekt u de betalingen met behulp van het betalingsjournaal in plaats van een vooruitbetalingsfactuur.

De vooruitbetaling kan uit de inkooporder worden verwijderd, tenzij u al een betaling hebt vereffend met de geboekte vooruitbetalingsfactuur of de standaardfactuur hebt geboekt. Als u vooruitbetalingsgegevens uit de inkooporder wilt verwijderen, selecteert u **Leveranciers \> Algemeen \> Inkooporders \> Alle inkooporders** en zoekt u de inkooporder van de leverancier. Selecteer het tabblad **Inkoop** in het actievenster en selecteer **Vooruitbetaling verwijderen**.

## <a name="create-and-post-a-prepayment-invoice"></a>Een vooruitbetalingsfactuur maken en boeken
Als u de vooruitbetalingsfactuur van de leverancier wilt vastleggen, gaat u naar de pagina **Leveranciersfactuur** door de optie **Vooruitbetalingsfactuur** te selecteren op de pagina **Inkooporders** (**Leveranciers \> Algemeen \> Inkooporders \> Alle inkooporders \> tabblad Factuur \> Vooruitbetalingsfactuur**). Voor gegevens in voor de aanbetalingsfactuur, waaronder het factuurnummer. U kunt de hoeveelheden voor een aanbetalingsfactuur niet wijzigen. Als de leverancier een gedeeltelijk bedrag van de vooruitbetalingswaarde heeft gefactureerd die is gedefinieerd op de inkooporder, kunt u de eenheidsprijs aanpassen aan de gedeeltelijke waarde.

Het leverancierssaldo en de vooruitbetalingsrekening worden bijgewerkt wanneer de vooruitbetalingsfactuur wordt geboekt. De waarde van **Aanbetalingsaanvraag** in de vooruitbetalingsdefinitie op de inkooporder wordt ook bijgewerkt. De standaardboekposten voor financiële dimensies voor het geboekte vooruitbetalingsboekstuk worden uit de koptekstgegevens op de inkooporder gehaald.

Als de functie **Financiële dimensies in factuurregels op aanbetalingsfactuur van leverancier vergrendelen** op de pagina **Functiebeheer** is ingeschakeld, kunnen de dimensies in de koptekst of regels van de aanbetaling niet worden bijgewerkt. 

## <a name="post-and-settle-payments-for-the-prepayment-invoice"></a>Betalingen voor de vooruitbetalingsfactuur boeken en vereffenen
Vervolgens wordt de vooruitbetalingsfactuur betaald via de pagina **Betalingsjournaal**. Als u betalingsjournalen wilt openen, klikt u op **Leveranciers \> Journalen \> Betalingen \> Betalingsjournaal**. Na boeking van de vereffening van de betaling naar de vooruitbetalingsfactuur wordt de restwaarde van de **aanbetalingsaanvraag** van de inkooporder bijgewerkt.

Voordat u de standaardfactuur voor de vooruitbetalingsfactuur boekt, kunt u de vereffening van de betaling omkeren vanuit de vooruitbetalingsfactuur. Nadat een standaardfactuur is toegepast op de vooruitbetalingsfactuur, kan de vereffening van de betaling echter niet worden omgekeerd vanuit de vooruitbetalingsfactuur.

## <a name="post-the-standard-vendor-invoice-for-the-purchase-order-and-apply-the-prepayment-invoice-to-the-standard-invoice"></a>De standaardleveranciersfactuur voor de inkooporder boeken en de vooruitbetalingsfactuur toepassen op de standaardfactuur
Leg de standaardfactuur vast die van de leverancier is ontvangen. Als onderdeel van dit proces u de vereffende vooruitbetalingsfactuur toepassen op de leveranciersfactuur, zodat de waarde van de factuur wordt verminderd met het bedrag dat al is betaald. Als u de vooruitbetalingsfactuur toepast op de leveranciersfactuur, zorgt u ervoor dat journaalregels uit de vooruitbetalingsfactuur worden omgekeerd.

## <a name="application-of-the-prepayment-invoice-after-posting-the-standard-invoice"></a>Toepassing van de vooruitbetalingsfactuur na het boeken van de standaardfactuur
Als u vergeet de vooruitbetaling toe te passen op de standaardleveranciersfactuur op het moment dat de leveranciersfactuur wordt geboekt, kan de vereffende vooruitbetaling worden toegepast op andere facturen van deze leverancier via de pagina **Leveranciers** (**Leveranciers \> Algemeen \> Leveranciers \> Alle leveranciers \> tabblad Factuur \> Toepassen**).

## <a name="reversal-of-the-prepayment-application-process"></a>Omkering van het proces voor de aanbetalingsaanvraag
Als u de vereffening of aanvraag van een vooruitbetalingsfactuur vanuit een standaardfactuur ongedaan wilt maken of wilt omkeren, selecteert u de actie **Omkeren** op de pagina **Leveranciers** (**Leveranciers \> Algemeen \> Leveranciers \> Alle leveranciers \> tabblad Factuur \> Omkeren**). Nadat de vooruitbetalingsaanvraag is teruggedraaid, kunt u de vooruitbetaling toepassen op een andere standaardfactuur. 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
