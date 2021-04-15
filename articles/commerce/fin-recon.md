---
title: Financiële afstemming in detailhandelwinkels
description: In dit onderwerp wordt de financiële afstemming beschreven in detailhandelwinkels voor POS voor Microsoft Dynamics 365 Commerce.
author: anpurush
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-21
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0f57f3119039337922dcd4035e1c4d64e6ae7295
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792386"
---
# <a name="financial-reconciliation-in-retail-stores"></a>Financiële afstemming in detailhandels

[!include [banner](includes/banner.md)]

In Microsoft Dynamics 365 Commerce versie 10.0.10 en eerder maakt de functionaliteit van de POS-client (Point of Sale) voor eindedagprocessen in winkels het winkelmedewerkers en winkelmanagers mogelijk om eindedagbewerkingen uit te voeren. Ze kunnen bijvoorbeeld kassacontroles, diensten blind afsluiten, diensttransacties afstemmen en diensten afsluiten. POS heeft echter geen mogelijkheid om de financiële informatie voor diensten te voltooien, zodat deze kan worden gebruikt om de financiële gegevens te boeken in Commerce Headquarters. Vaak zijn winkelmanagers verantwoordelijk voor het voltooien van deze taak. Voordat ze een dienst kunnen afmelden, moeten ze de informatie controleren, eventuele vereiste correcties doorvoeren en de totalen voor die dienst afronden. De voltooide totalen moeten vervolgens worden geboekt in financiële modules in Commerce Headquarters.

Daarnaast kunnen winkelmanagers in Commerce versie 10.0.10 en eerder overzichtsregels controleren en hierin enkele aanpassingen doorvoeren in Commerce Headquarters. De mogelijkheden zijn echter beperkt en winkelmanagers hebben zelden toegang tot de Commerce Headquarters-client. Bovendien kan een financieel detailhandeloverzicht alleen worden gecontroleerd en aangepast wanneer de overzichten worden gemaakt in Commerce Headquarters. Dit proces wordt echter meestal 's nachts uitgevoerd. Winkelmanagers moeten daarom wachten tot de dienst zich afmeldt, het moment waarop financiële detailhandeloverzichten worden gemaakt in Commerce Headquarters.

In Commerce versie 10.0.11 en hoger kunnen winkelmanagers hun diensten op de POS-client zelf controleren, aanpassen en voltooien. Deze gegevens worden vervolgens gebruikt om financiële overzichten te maken en te boeken in Commerce Headquarters.

> [!NOTE]
> De functionaliteit die is gerelateerd aan financiële afstemming in detailhandelwinkels werkt alleen als het groepsgewijs maken van orders is ingeschakeld. Meer informatie over dit onderwerp vindt u in [Groepsgewijs orders voor detailhandeltransacties maken](trickle-feed.md).

## <a name="set-up-financial-reconciliation"></a>Financiële afstemming instellen

Voer de volgende stappen uit om de functie voor financiële afstemming te gebruiken.

1. Schakel in de werkruimte **Functiebeheer** de functie **Detailhandeloverzichten - groepsgewijze invoer** in.
1. Stel in het POS-functionaliteitsprofiel voor de betreffende winkel de optie **Financiële afstemming in winkel inschakelen** in op **Ja**.

## <a name="more-information-about-financial-reconciliation"></a>Meer informatie over financiële afstemming

Wanneer de functionaliteit voor financiële afstemming is ingeschakeld, worden sommige parameters die zijn gedefinieerd op het sneltabblad **Overzicht/afsluiting** van de pagina **Detailhandelwinkels** in Commerce Headquarters gesynchroniseerd met de kanaaldatabase. Dezelfde verzameling berekeningscriteria en drempelwaarden voor bedragen die voor retailoverzichten worden gebruikt, wordt afgedwongen.

Wanneer de bewerking **Ploeg sluiten** wordt geactiveerd, controleert het systeem of de door het systeem berekende bedragen en de gedeclareerde bedragen overeenkomen. Als deze verschillen en het verschil de gedefinieerde drempelwaarden overschrijdt, wordt de gebruiker gevraagd de vereiste correcties aan te brengen.

Voor elke betalingsmethode kunnen correcties worden gemaakt. Wanneer een betalingsmethode is geselecteerd, kan de gebruiker de totalen voor verschillende transactietypen weergeven en de totalen voor een bepaald transactietype bewerken. Tijdens het bewerken laat het systeem het oorspronkelijke berekende bedrag zien en het overschreven bedrag voor dat transactietype. De gebruiker kan ook notities vastleggen als onderdeel van het bewerkingsproces. Notities kunnen worden gebruikt voor controledoeleinden.

Gebruikers kunnen de validatieprompts en berichten negeren en kunnen door gaan met het afsluiten van de dienst. Als een gebruiker de validatieprompts negeert, worden dezelfde problemen gedetecteerd (en moeten deze worden gecorrigeerd) wanneer de dienst de financiële overzichten boekt in Commerce Headquarters.

Met de bewerking **Ploeg sluiten** in POS wordt ook gevalideerd of alle transacties in de offline database zijn gesynchroniseerd met de kanaaldatabase. Als er geen transacties worden gesynchroniseerd, ontvangt de gebruiker een waarschuwingsbericht, omdat deze situatie ertoe kunnen leiden dat het systeem de bedragen niet correct kan berekenen. In deze situatie kan de gebruiker de bewerking **Ploeg sluiten** beëindigen en proberen de offline transacties te synchroniseren met de kanaaldatabase. Als alternatief kan de gebruiker de door het systeem berekende bedragen handmatig aanpassen, om te compenseren voor de transacties die niet zijn gesynchroniseerd, zodat de juiste set financiële cijfers wordt voltooid en geboekt. 

Wanneer de overzichten groepsgewijs worden geboekt, zodat het boeken van transacties gescheiden gebeurt van het boeken van financiële transacties, kunt u de door het systeem berekende bedragen aanpassen voor ontbrekende offline transacties. Op deze manier zorgt u ervoor dat de financiële gegevens altijd correct worden verwerkt en geboekt, ongeacht de ontbrekende transacties. U kunt offline transacties synchroniseren met de kanaaldatabase en Commerce Headquarters en deze later boeken, apart van de financiële boekingen.

Details van de financiële afstemming voor een dienst worden gesynchroniseerd met Commerce Headquarters door middel van de P-taak.

In financiële detailhandeloverzichten in Commerce Headquarters worden geen totalen berekend om de details op de overzichtsregels weer te geven. In plaats daarvan worden de voltooide bedragen in de POS-client gebruikt om financiële overzichten voor detailhandelwinkels te maken en te boeken.


[!INCLUDE[footer-include](../includes/footer-banner.md)]