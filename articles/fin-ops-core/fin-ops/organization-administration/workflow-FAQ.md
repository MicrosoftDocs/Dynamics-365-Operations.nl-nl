---
title: Veelgestelde vragen workflow
description: In dit onderwerp worden antwoorden op veelgestelde vragen over het workflowsysteem gegeven.
author: ChrisGarty
ms.date: 09/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a0068f7e678b069a6a2563ed227e42393ddacf5d78d988ca73f576cdcff5e3f6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6749383"
---
# <a name="workflow-faq"></a>Veelgestelde vragen over werkstromen

[!include [banner](../includes/banner.md)]

In dit onderwerp worden antwoorden op veelgestelde vragen over het workflowsysteem gegeven.

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Waarom worden er meerdere meldingen ontvangen wanneer een werkitem wordt afgewezen?
Wanneer een werkitem wordt afgewezen, wordt dat werkitem als afgewezen voltooid. Een andere werkitem wordt gemaakt en toegewezen aan de aanvrager. Dit betekent dat er een melding naar de aanvrager voor het afgewezen werkitem gaat en een aparte melding naar de gebruiker die is toegewezen aan het nieuwe werkitem waarvoor 'wijziging is aangevraagd'. 

Elke melding is voor een ander werkitem, maar doordat de meldingen op elkaar lijken kan er verwarring ontstaan. We proberen dit in een toekomstige versie te verbeteren.

## <a name="why-are-my-workflow-exports-failing"></a>Waarom mislukt het exporteren van mijn werkstromen?
Er geldt momenteel een beperking in de functie voor het exporteren van werkstromen waardoor namen van werkstromen niet langer kunnen zijn dan 48 tekens. Als u een naam gebruikt die langer is dan 48 tekens, kan het foutbericht 'Server kon de aanvraag niet verifiëren' worden weergegeven en/of kan worden voorkomen dat een bestand wordt geëxporteerd zonder bestandstype. Het volgende blogbericht bevat nadere details: [Problemen bij het exporteren van werkstromen oplossen](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).

## <a name="can-the-submitter-of-a-workflow-also-approve-the-workflow"></a>Kan de indiener van een workflow de workflow ook goedkeuren?
Ja, een indiener van een workflow kan de workflow ook goedkeuren als deze op die manier is geconfigureerd. Als u dit gedrag wilt voorkomen, stelt u **Systeembeheer > Workflow > Workflowparameters > Algemeen > Fiatteur > Goedkeuring door indiener niet toestaan** in op **Ja**.

## <a name="can-i-add-alerts-to-workflows-to-provide-notifications-to-users"></a>Kan ik waarschuwingen aan workflows toevoegen om gebruikers te voorzien van meldingen?
Hier volgen enkele belangrijke punten met betrekking tot het toevoegen van waarschuwingen aan workflows om meldingen te geven:
- Mechanismes van waarschuwingen en workflowmeldingen
    - Waarschuwingen kunnen worden ingesteld voor recordwijzigingen. Workflows wijzigen records, dus het is mogelijk om een waarschuwing in te stellen die is gerelateerd aan een recordwijziging die door een workflow is veroorzaakt. Aangezien workflows echter andere ingebouwde meldingsopties bieden, is het gebruik van waarschuwingen niet ideaal.
- Standaardmeldingen vanuit workflows 
    - Workflows bevatten ingebouwde e-mailmeldingen. Een klant kan de meldingen zo configureren dat de gebruikers e-mails ontvangen. Deze meldingen resulteren niet in actiecentrumberichten voor gebruikers.
    - In een toekomstige voegen we een actiecentrumbericht toe om aan workflowwerkitems aan gebruikers toe te wijzen. 
- Meldingen toevoegen aan workflows
    - Actiecentrumberichten kunnen worden gemaakt voor specifieke gebruikers, zoals een bericht dat is gemaakt op basis van een workflow in X++.
    - [Werkstromen bevatten zakelijke gebeurtenissen](../../dev-itpro/business-events/business-events-workflow.md) die de klant kan gebruiken voor het activeren van Flows met de gewenste meldingen.   

Overzicht: als gebruikers niet de juiste meldingen vanuit het actiecentrum ontvangen wanneer aan hen een workflowwerkitem wordt toegewezen, gebruikt u [Zakelijke gebeurtenissen voor werkstromen](../../dev-itpro/business-events/business-events-workflow.md) met Microsoft Power Automate om aanvullende of andere meldingen te bieden.

## <a name="why-is-workflow-editor-not-able-to-start-under-ad-fs"></a>Waarom kan ik de werkstroomeditor niet starten onder AD FS?
Wanneer de workfloweditor wordt uitgevoerd onder AD FS (Active Directory Federation Services) in een bijgewerkte omgeving, kan de workfloweditor problemen ondervinden bij het starten. Als dit het geval is, zorgt u ervoor dat de URL https://dynamicsaxworkfloweditor/ wordt toegevoegd aan de eigenschap **Microsoft Dynamics 365 for Operations On-premises - Workflow - Systeemeigen toepassing** in de AD FS-instellingen.

## <a name="why-am-i-getting-sql-deadlocks-on-workflow-processing"></a>Waarom krijg ik SQL-impasses bij het verwerken van werkstromen? 
De standaardveldwaarde voor **Aantal werkstroomartikelen per batchtaak** op de pagina **Werkstroomparameters** is 0. De waarde 0 geeft aan dat de standaardwaarde 20 artikelen per batch wordt gewijzigd. Wees voorzichtig met het aanpassen van deze waarde omdat een groot aantal artikelen per batch (> 40) SQL-impasses kan veroorzaken.

## <a name="what-is-the-workflow-enhanced-error-feature"></a>Wat is de Verbeterde werkstroomfoutmelding?
Met de verbeterde werkstroomfoutmelding in versie 10.0.13 worden foutcodes toegevoegd om verschillende klassen van werkstroomfouten van elkaar te onderscheiden. De weergegeven foutberichten komen grotendeels overeen, maar bevatten kleine verschillen om ze duidelijker te maken.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
