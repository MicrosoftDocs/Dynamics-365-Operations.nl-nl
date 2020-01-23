---
title: De verbinding met de Talent-klant wordt verbroken
description: In dit onderwerp wordt uitgelegd wat u moet doen als de klant geen verbinding meer heeft met zijn of haar omgeving en niet weet waarom.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 02df31b56c0e960a16ec2aadd8b1e817e0b6ec65
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898452"
---
# <a name="talent-client-disconnects"></a>De verbinding met de Talent-klant wordt verbroken

**Omgevingsdetails** 

Dit probleem kan optreden in alle omgevingen.
 
**Symptoom** 

De klant heeft geen verbinding meer met zijn of haar omgeving en weet niet waarom. Een van de volgende foutberichten wordt weergegeven:

- De verbinding is verbroken. Klik op Sluiten om verder te gaan met werken.
- Het lijkt erop dat de netwerkverbinding is verbroken. Klik op Opnieuw proberen om het opnieuw te proberen.

**Rode vlag**

Dit gebeurt vaak als gebruikers zich in de implementatiefase bevinden, gegevens tussen productie- en testomgevingen vergelijken en vergeten dat ze tussen sessies overschakelen. Gebruikers ondervinden dit probleem waarschijnlijk als ze zich in deze fase bevinden.

**Uitgifte** 

**Browsertypen:** Google Chrome Internet Explorer en Microsoft Edge

Microsoft Dynamics 365 Talent verbreekt de verbinding met gebruikers wanneer twee verschillende sessies tegelijkertijd geopend zijn voor dezelfde gebruiker en hetzelfde browsertype. (bijvoorbeeld wanneer gebruiker A zowel omgeving 1 als omgeving 2 bekijkt in Chrome). Het maakt niet uit of de gebruikers verschillende browservensters of -tabbladen openen. Als dezelfde gebruikersreferenties worden gebruikt voor de gelijktijdige aanmelding bij omgeving 1 en 2 in hetzelfde browsertype, wordt de verbinding met een van de sessies verbroken.

**Oplossing**

Zorg dat altijd slechts één omgeving tegelijk is geopend voor een bepaald browsertype. Gebruikers kunnen meerdere sessies naar dezelfde omgeving openen (meerdere tabbladen in dezelfde browser).

Gebruikers die tegelijkertijd tussen twee omgevingen willen schakelen, moeten deze omgevingen in verschillende browsertypen openen. (Gebruiker A kan omgeving 1 bijvoorbeeld in Chrome en omgeving 2 in Microsoft Edge openen.)
