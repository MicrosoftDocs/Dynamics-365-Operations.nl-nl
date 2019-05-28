---
title: Inzichten in klantbetalingen (preview)
description: In dit onderwerp wordt beschreven hoe Inzichten in klantbetalingen kan helpen voorspellen wanneer een factuur wordt betaald en organisaties helpen optimalisatiestrategieën op te stellen ter verbetering van de kans op tijdige betaling.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-04-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 9e722db6302d7ef51c01601cde245d4f4a333eba
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566233"
---
# <a name="customer-payment-insights-preview"></a>Inzichten in klantbetalingen (preview)

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> Deze functie maakt deel uit van een gerichte introductie en is alleen beschikbaar voor gebruikers die zich hebben aangemeld voor de particuliere preview. Deze functie wordt opgenomen in een komende algemene beschikbaarheidsversie.

# <a name="overview"></a>Overzicht

Organisaties vinden het vaak lastig om te voorspellen wanneer een klant hun facturen betaalt. Dit gebrek aan inzicht kan leiden tot onnauwkeurige cashflowprognoses, inefficiënte incassoprocessen en de mogelijkheid dat orders worden vrijgegeven aan klanten die een kredietrisico kunnen inhouden. Inzichten in klantbetalingen (preview) maakt gebruik van Machine Learning om te voorspellen wanneer een factuur wordt betaald. Daarnaast worden er optimalisatiestrategieën geboden die kunnen worden aangepast om de kans dat klanten op tijd betalen zo groot mogelijk te maken.

## <a name="predictions"></a>Voorspellingen

Betalingsvoorspellingen stellen organisaties in staat hun bedrijfsprocessen te verbeteren doordat zij helpen:

-   Op eenvoudige wijze de facturen te identificeren waarvoor late betaling wordt voorspeld.
-   Passende maatregelen te nemen ter verbetering van de kans op tijdige betaling.

Inzichten in klantbetalingen (preview) maakt gebruik van Machine Learning om te voorspellen wanneer een factuur wordt betaald. Er wordt gebruikgemaakt van historische factuur-, betalings- en klantgegevens om een model voor Machine Learning op te stellen dat wordt gebruikt om te voorspellen wanneer een factuur wordt betaald.

Voor elke openstaande factuur voorspelt Inzichten in klantbetaling (preview) drie waarschijnlijke betalingen:

-  Waarschijnlijkheid van betaling op tijd (voor de vervaldatum van de factuur).
-  Waarschijnlijkheid van betaling binnen 30 dagen na de vervaldatum van de factuur.
-  Waarschijnlijkheid van betaling later dan 30 dagen na de vervaldatum van de factuur.

De waarschijnlijkheid van betalingen kan worden weergegeven in de voorspellingssectie.

[![Betalingsvoorspellingen](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)

Aan elke factuur wordt tevens een winnende waarschijnlijkheid van betaling toegewezen via een van de drie voorspelde scenario's voor betalingswaarschijnlijkheid die hierboven zijn gedefinieerd. Het scenario met de hoogste waarschijnlijkheid van betaling is het winnende scenario.


Stel bijvoorbeeld dat de voorspelling voor een factuur aangeeft dat er een waarschijnlijkheid van 71 procent is dat de factuur op tijd worden betaald, een waarschijnlijkheid van 13 procent dat de factuur wordt betaald binnen 30 dagen na de vervaldatum en een waarschijnlijkheid van 16 procent waarschijnlijkheid dat de factuur later dan 30 dagen na de vervaldatum wordt betaald. De hoogste waarschijnlijkheid laat zien dat de factuur het scenario voor betaling op tijd volgt, dus wordt de factuur gelabeld met de waarschijnlijkheid van tijdige betaling.

[![Betalingsvoorspellingen](./media/payment-predict.png)](./media/payment-predict.png)

## <a name="optimization-strategies"></a>Optimalisatiestrategieën

Behalve voor betalingsvoorspellingen kan Inzichten in klantbetalingen (preview) worden gebruikt voor optimalisatiestrategieën ter verbetering van de kans van tijdige betaling. Hierdoor kunnen organisaties 'Wat als'-analyses uitvoeren door gebruikers in staat te stellen factuur- en klantparameters aan te passen en vervolgens het bijbehorende effect te vergelijken om de waarschijnlijkheid van tijdige ontvangst van betaling voor facturen te bepalen.

Een organisatie wil bijvoorbeeld het effect evalueren van het bijwerken van de korting voor contante betaling op de waarschijnlijkheid van het ontvangen van tijdige betaling. Wanneer de facturen zijn geoptimaliseerd voor gebruik van de nieuwe korting, kunnen de gebruikers het effect bekijken van het toepassen van de korting op de waarschijnlijkheid van het ontvangen van tijdige betalingen voor deze facturen. Als de kosten van het toepassen van de korting minimaal zijn in vergelijking met het voordeel van het tijdig innen van de betaling, kan de organisatie ervoor kiezen de geselecteerde korting toe te passen op alle toekomstige openstaande orders.

> [!NOTE] 
> Momenteel is alleen korting beschikbaar als optimalisatiestrategie voor Inzichten in klantbetalingen (preview).

[![Geoptimaliseerde voorspellingen](./media/optimized-pay.png)](./media/optimized-pay.png)

## <a name="how-to-get-customer-payment-insights-preview"></a>Inzichten in klantbetalingen (preview) ophalen

Als u geïnteresseerd bent in het uitproberen van Inzichten in klantbetalingen (preview), stuurt u een e-mail naar het [team voor preview van financiële inzichten](mailto:fiap@microsoft.com). 

## <a name="privacy-statement"></a>Privacyverklaring

Previews van opgeslagen klantgegevens in de Verenigde Staten Daarnaast geldt dat previews (1) mogelijk minder privacy- en beveiligingsmaatregelen bieden dan de service Dynamics 365 for Finance and Operations, (2) mogelijk niet worden opgenomen in de serviceovereenkomst voor deze service, (3) niet mogen worden gebruikt voor de verwerking van persoonsgegevens of andere gegevens die aan juridische of wettelijke nalevingvereisten zijn onderworpen en (4) slechts beperkt wordt ondersteund.
