---
title: Vooruitbetalingsfacturen versus vooruitbetalingen
description: "Dit artikel beschrijft en vergelijkt de twee methoden met elkaar start die de organisaties voor voorschotten (vooruitbetalingen) gebruiken. Bij één methode kunt u een aanbetalingsfactuur maken die aan een inkooporder is gekoppeld. Bij de andere methode kunt u journaalboekstukken van vooruitbetaling maken door boekingen in een journaal te maken en ze als journaalboekstukken van vooruitbetaling te markeren."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, PurchTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15871
ms.assetid: a0bb5220-73d4-48ae-84d0-46a171c224fa
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c4f127007cea1d8ccd0b4e9ea637f0674775278d
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="prepayment-invoices-vs-prepayments"></a>Vooruitbetalingsfacturen versus vooruitbetalingen

[!include[banner](../includes/banner.md)]


Dit artikel beschrijft en vergelijkt de twee methoden met elkaar start die de organisaties voor voorschotten (vooruitbetalingen) gebruiken. Bij één methode kunt u een aanbetalingsfactuur maken die aan een inkooporder is gekoppeld. Bij de andere methode kunt u journaalboekstukken van vooruitbetaling maken door boekingen in een journaal te maken en ze als journaalboekstukken van vooruitbetaling te markeren.

Organisaties kunnen aanbetalingen (vooruitbetalingen) verzenden naar leveranciers voor goederen of services voordat deze goederen of services zijn afgehandeld. Voor het verzenden van vooruitbetalingen naar leveranciers kunnen twee methoden worden gebruikt. Om risico's te minimaliseren, kunt u vooruitbetalingen bijhouden door de vooruitbetaling op een inkooporder te definiëren. Voor deze methode moet u een aanbetalingsfactuur maken die aan een inkooporder is gekoppeld. Deze methode wordt aanbetalingsfacturering genoemd. Organisaties die vooruitbetalingen niet zo nauwgezet willen bijhouden of geen vooruitbetalingsfactuur van hun leverancier ontvangen, kunnen journaalboekstukken voor vooruitbetalingen gebruiken in plaats van de vooruitbetalingsfactureringsmethode. U kunt journaalboekstukken van vooruitbetaling maken door boekingen in een journaal te maken en ze als journaalboekstukken van vooruitbetaling te markeren. Bij deze methode kunt u niet bijhouden welke vooruitbetalingen aan een leverancier worden uitgevoerd en voor welke inkooporders. U kunt echter wel een geboekte vooruitbetaling voor vereffening voor een inkooporder markeren.

## <a name="when-to-use-prepayment-invoicing-vs-prepayments"></a>Gebruik van vooruitbetalingsfacturering versus vooruitbetalingen
| Vooruitbetalingsfacturering                                                                | Vooruitbetalingen                                                              |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Definieer een vooruitbetalingswaarde op de inkooporder.                                    | Er is geen vooruitbetalingswaarde op de inkooporder gedefinieerd.                    |
| Belangrijk: Een vooruitbetalingsfactuur en een definitieve factuur moeten worden geboekt.                       | Er moet geen vooruitbetalingsfactuur worden geboekt.                                    |
| Aansprakelijkheid voor de vooruitbetaling maakt deel uit van de vooruitbetalingsrekening, niet de leveranciersrekening. | Aansprakelijkheid voor de vooruitbetaling maakt deel uit van de leveranciersrekening.                  |
| Het leverancierssaldo weerspiegelt niet de vooruitbetalingswaarde in het hele proces.     | Het leverancierssaldo weerspiegelt de vooruitbetalingswaarde in het hele proces. |
| Vooruitbetalingsfacturering is alleen beschikbaar in Leveranciers.                         | Vooruitbetalingen zijn beschikbaar in Klanten en Leveranciers.    |

## <a name="overview-of-the-prepayment-process"></a>Overzicht van het vooruitbetalingsproces
Bij de boekhouding in veel landen/regio's is het vereist dat vooruitbetalingen van een klant of aan een leverancier niet naar de gewone totaalrekeningen voor de klant of de leverancier worden geboekt. In plaats daarvan worden deze vooruitbetalingen geboekt naar speciale grootboekrekeningen voor vooruitbetalingen. Wanneer een verkooporder of inkooporder wordt gemaakt, wordt een factuur naar de klant of van de leverancier gestuurd. Wanneer de factuur wordt betaald, wordt het vooruitbetalingsboekstuk voor de vooruitbetaling en btw op de vooruitbetalingsgrootboekrekeningen omgekeerd, en de factuurbedragen worden automatisch naar de gewone totaalrekeningen geboekt. Volg deze stappen om een vooruitbetaling te maken.

1.  Stel boekingsprofielen voor vooruitbetalingen in.
2.  Selecteer in Parameters van module Klanten en Parameters van module Leveranciers onder **Grootboek en btw** het nieuwe boekingsprofiel door de parameter **Boekingsprofiel voor betalingsjournaal met vooruitbetaling** te gebruiken.
3.  Maak een betalingsjournaal, en vervolgens de nieuwe betaling.
4.  U kunt de betaling als vooruitbetaling markeren. Als een betaling als vooruitbetaling wordt gemarkeerd, wordt de betaling geboekt naar de grootboekrekeningen die zijn gedefinieerd in het boekingsprofiel dat u in stap 1 en 2 hebt ingesteld. Bovendien, als de betaling als vooruitbetaling wordt gemarkeerd, wordt de btw berekend. Sommige overheidsinstellingen vereisen dat de btw wordt betaald wanneer een vooruitbetaling wordt geregistreerd, zelfs als er geen factuur is.
5.  Boek de vooruitbetaling.
6.  Optioneel: U kunt de vooruitbetaling vereffenen met de inkooporder of verkooporder voordat u de factuur maakt. Gebruik op de verkooporder- of inkooporderpagina in het actievenster **Transacties vereffenen**.
7.  Nadat de leverancier de goederen of services heeft geleverd, registreert u de factuur. Als u de vooruitbetaling voor de inkooporder of de verkooporder in stap 6 hebt vereffend, wordt de vooruitbetaling automatisch vereffend voor de factuur die u hebt gemaakt. Als u de vooruitbetaling niet voor de inkooporder of de verkooporder hebt vereffend, kunt u deze handmatig vereffenen voor de factuur door **Transacties vereffenen** op de klant- of leverancierspagina te gebruiken. Het vooruitbetalingsbedrag wordt vervolgens teruggeboekt uit de tijdelijke klant- of leveranciersgrootboekrekening. Bovendien, als btw is berekend, wordt deze teruggeboekt, omdat de factuur de werkelijke btw heeft.

## <a name="overview-of-the-prepayment-invoicing-process"></a>Overzicht van het vooruitbetalingsfactureringsproces
Vooruitbetalingsfacturen worden veel in het bedrijfsleven gebruikt. Een leverancier maakt vooruitbetalingsfacturen om een voorschot voor de aankoop te vereisen voordat de inkooporder is vervuld. Een leverancier kan bijvoorbeeld een vooruitbetaling eisen voor aangepaste goederen of services. Als een leverancier een factuur verzendt voor vooruitbetaling, kunt u de functie voor vooruitbetalingsfacturering gebruiken. Een vooruitbetalingswaarde kan op de inkooporder worden gedefinieerd, een vooruitbetalingsfactuur wordt geregistreerd en betaald, en vervolgens wordt de vooruitbetalingsfactuur toegepast op de uiteindelijke factuur. Volg deze stappen om een vooruitbetaling te maken.

1.  De inkoopmedewerker maakt, bevestigt en verzendt een inkooporder waarvoor de leverancier een vooruitbetaling heeft gevraagd. De vooruitbetalingswaarde wordt gedefinieerd op de inkooporder als onderdeel van de overeenkomst.
2.  De leverancier geeft een vooruitbetalingsfactuur uit.
3.  De leverancierscoördinator registreert de vooruitbetalingsfactuur tegen de inkooporder en vervolgens wordt de vooruitbetalingsfactuur betaald.
4.  Nadat de leverancier de goederen of services heeft geleverd en de bijbehorende leveranciersfacturen zijn ontvangen, past de leverancierscoördinator het vooruitbetalingsbedrag toe dat al is betaald voor de factuur.
5.  De leverancierscoördinator betaalt en vereffent het resterende bedrag van de factuur.





