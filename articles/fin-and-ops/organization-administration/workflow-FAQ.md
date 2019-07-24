---
title: Veelgestelde vragen workflow
description: In dit onderwerp worden antwoorden op veelgestelde vragen over het workflowsysteem in Microsoft Dynamics 365 for Finance and Operations gegeven.
author: ChrisGarty
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: adcc9bbc422a3fddfd51d248daf95c0da6d4c9bb
ms.sourcegitcommit: 8cf77e9171d6cad8ae6c8bfad9e4f9a46fef6d23
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/19/2019
ms.locfileid: "1688995"
---
# <a name="workflow-faq"></a>Veelgestelde vragen over werkstromen

[!include [banner](../includes/banner.md)]

In dit onderwerp worden antwoorden op veelgestelde vragen over het workflowsysteem in Microsoft Dynamics 365 for Finance and Operations gegeven.

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Waarom worden er meerdere meldingen ontvangen wanneer een werkitem wordt afgewezen?
Wanneer een werkitem wordt afgewezen, wordt dat werkitem als afgewezen voltooid. Een andere werkitem wordt gemaakt en toegewezen aan de aanvrager. Dit betekent dat er een melding naar de aanvrager voor het afgewezen werkitem gaat en een aparte melding naar de gebruiker die is toegewezen aan het nieuwe werkitem waarvoor 'wijziging is aangevraagd'. 

Elke melding is voor een ander werkitem, maar doordat de meldingen op elkaar lijken kan er verwarring ontstaan. We proberen dit in een toekomstige versie te verbeteren.

## <a name="why-are-my-workflow-exports-failing"></a>Waarom mislukt het exporteren van mijn werkstromen?
Er geldt momenteel een beperking in de functie voor het exporteren van werkstromen waardoor namen van werkstromen niet langer kunnen zijn dan 48 tekens. Als u een naam gebruikt die langer is dan 48 tekens, kan het foutbericht 'Server kon de aanvraag niet verifiëren' worden weergegeven en/of kan worden voorkomen dat een bestand wordt geëxporteerd zonder bestandstype. Het volgende blogbericht bevat nadere details: [Problemen bij het exporteren van werkstromen oplossen](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).

## <a name="can-the-submitter-of-a-workflow-also-approve-the-workflow"></a>Kan de indiener van een workflow de workflow ook goedkeuren?
Ja, een indiener van een workflow kan de workflow ook goedkeuren als deze op die manier is geconfigureerd. Als u dit gedrag wilt voorkomen, stelt u **Workflowparameters > Algemeen > Fiatteur > Goedkeuring door indiener niet toestaan** in op **Ja**.

## <a name="can-i-add-alerts-to-workflows-to-provide-notifications-to-users"></a>Kan ik waarschuwingen aan workflows toevoegen om gebruikers te voorzien van meldingen?
Hier volgen enkele belangrijke punten met betrekking tot het toevoegen van waarschuwingen aan workflows om meldingen te geven:
- Mechanismes van waarschuwingen en workflowmeldingen
    - Waarschuwingen kunnen worden ingesteld voor recordwijzigingen. Workflows wijzigen records, dus het is mogelijk om een waarschuwing in te stellen die is gerelateerd aan een recordwijziging die door een workflow is veroorzaakt. Aangezien workflows echter andere ingebouwde meldingsopties bieden, is het gebruik van waarschuwingen niet ideaal.
- Standaardmeldingen vanuit workflows 
    - Workflows bevatten ingebouwde e-mailmeldingen. Een klant kan de meldingen zo configureren dat de gebruikers e-mails ontvangen. Deze meldingen resulteren niet in actiecentrumberichten voor gebruikers.
    - In een toekomstige voegen we een actiecentrumbericht toe om aan workflowwerkitems aan gebruikers toe te wijzen. 
- Meldingen toevoegen aan workflows
    - Actiecentrumberichten kunnen worden gemaakt voor specifieke gebruikers, zoals een bericht dat is gemaakt op basis van een workflow in X++.
    - [Workflows bevatten zakelijke gebeurtenissen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) die de klant kan gebruiken voor het activeren van flows met de gewenste meldingen.   

Overzicht: als gebruikers niet de juiste meldingen vanuit het actiecentrum ontvangen wanneer aan hen een workflowwerkitem wordt toegewezen, gebruikt u [Zakelijke gebeurtenissen voor workflows](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) met Microsoft Flow om aanvullende of andere meldingen te bieden.
