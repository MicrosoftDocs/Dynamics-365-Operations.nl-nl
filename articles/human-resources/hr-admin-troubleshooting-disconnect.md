---
title: De verbinding met de client wordt verbroken
description: In dit onderwerp wordt uitgelegd wat u moet doen als de klant geen verbinding meer heeft met de omgeving.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f99731d4d0658ed6f06b9e6915237532601a0a1d
ms.sourcegitcommit: 7e32e5e39e762a4b1606161cb603a450d13b5251
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/23/2021
ms.locfileid: "7413506"
---
# <a name="client-disconnects"></a>De verbinding met de client wordt verbroken

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Omgevingsdetails** 

Dit probleem kan optreden in alle omgevingen.
 
**Symptoom** 

De klant heeft geen verbinding meer met de omgeving en weet niet waarom. Een van de volgende foutberichten wordt weergegeven:

- De verbinding is verbroken. Klik op Sluiten om verder te gaan met werken.
- Het lijkt erop dat de netwerkverbinding is verbroken. Klik op Opnieuw proberen om het opnieuw te proberen.

**Rode vlag**

Dit gebeurt vaak als gebruikers zich in de implementatiefase bevinden, gegevens tussen productie- en testomgevingen vergelijken en vergeten dat ze tussen sessies overschakelen. Gebruikers ondervinden dit probleem waarschijnlijk als ze zich in deze fase bevinden.

**Uitgifte** 

**Browsertypen:** Google Chrome Internet Explorer en Microsoft Edge

Microsoft Dynamics 365 Human Resources verbreekt de verbinding met gebruikers wanneer twee verschillende sessies tegelijkertijd geopend zijn voor dezelfde gebruiker en hetzelfde browsertype. (bijvoorbeeld wanneer gebruiker A zowel omgeving 1 als omgeving 2 bekijkt in Chrome). Het maakt niet uit of de gebruikers verschillende browservensters of -tabbladen openen. Als dezelfde gebruikersreferenties worden gebruikt voor de gelijktijdige aanmelding bij omgeving 1 en 2 in hetzelfde browsertype, wordt in Human Resources de verbinding met een van de sessies verbroken.

**Oplossing**

Zorg dat altijd slechts één omgeving tegelijk is geopend voor een bepaald browsertype. Gebruikers kunnen meerdere sessies naar dezelfde omgeving openen (meerdere tabbladen in dezelfde browser).

Gebruikers die tegelijkertijd tussen twee omgevingen willen schakelen, moeten deze omgevingen in verschillende browsertypen openen. (Gebruiker A kan omgeving 1 bijvoorbeeld in Chrome en omgeving 2 in Microsoft Edge openen.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
