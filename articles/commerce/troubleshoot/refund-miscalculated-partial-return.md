---
title: Terug te betalen kosten worden onjuist berekend op basis van de geretourneerde hoeveelheid
description: Dit onderwerp bevat richtlijnen voor het oplossen van problemen die kunnen helpen wanneer kassiers onjuiste terug te betalen kosten zien in het POS voor de hoeveelheid artikelen die wordt geretourneerd.
author: gvrmohanreddy
ms.date: 03/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: c8ecaa0cb73d06ac66b57cce815264e841a2259b
ms.sourcegitcommit: 94ebdaae6dc996b205ac78ed546e38f91f4f46ed
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/28/2022
ms.locfileid: "8490211"
---
# <a name="refundable-charges-are-miscalculated-based-on-the-quantity-returned"></a>Terug te betalen kosten worden onjuist berekend op basis van de geretourneerde hoeveelheid

[!include [banner](../../includes/banner.md)]

Dit onderwerp bevat richtlijnen voor het oplossen van problemen die kunnen helpen wanneer kassiers onjuiste terug te betalen kosten zien in het POS voor de hoeveelheid artikelen die wordt geretourneerd.

## <a name="description"></a>Description

Een klant retourneert een gedeeltelijke hoeveelheid van de artikelen die zijn gekocht voor een verkooporder met terug te betalen kosten op regelniveau. In plaats van dat een gedeeltelijke restitutie wordt weergegeven, worden in het POS echter alle kosten als terug te betalen weergegeven.

Een klant koopt bijvoorbeeld een hoeveelheid van vijf artikelen voor $ 5 per artikel, met $ 25 als totale kosten. De klant retourneert vervolgens drie van de vijf artikelen. De kassier krijgt echter een totale terug te betalen kostenpost van $ 25 te zien in plaats van de verwachte $ 15 aan restitutiekosten voor de drie artikelen die zijn geretourneerd.

## <a name="resolution"></a>Oplossing

### <a name="turn-on-the-enable-refunding-charges-based-on-the-refunded-quantity-feature"></a>De functie Restitutiekosten op basis van de gerestitueerde hoeveelheid inschakelen

Vanaf Microsoft Dynamics 365 Commerce versie 10.0.26 maakt de functie **Restitutiekosten op basis van de gerestitueerde hoeveelheid inschakelen** het mogelijk restitutie van kosten op regelniveau te berekenen op basis van de hoeveelheid geretourneerde artikelen.

Volg deze stappen om de functie **Restitutiekosten op basis van de gerestitueerde hoeveelheid inschakelen** in te schakelen in Commerce Headquarters.

1. Open de werkruimte **Functiebeheer** (**Systeembeheerder \> Werkruimten \> Functiebeheer**).
1. Zoek in de lijst met beschikbare functies naar de functie **Restitutiekosten op basis van de gerestitueerde hoeveelheid inschakelen** en selecteer deze.
1. Selecteer **Nu inschakelen** in het rechterdeelvenster.
