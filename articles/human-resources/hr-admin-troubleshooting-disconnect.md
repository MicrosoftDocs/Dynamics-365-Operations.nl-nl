---
title: De verbinding met de client wordt verbroken
description: In dit artikel wordt uitgelegd wat u moet doen als de klant geen verbinding meer heeft met zijn of haar omgeving en niet weet waarom.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6808132e182ea6fed4fb0605fd07c008d208e89f
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468174"
---
# <a name="client-disconnects"></a>De verbinding met de client wordt verbroken

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

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

Microsoft Dynamics 365 Human Resources verbreekt de verbinding met gebruikers wanneer twee verschillende sessies tegelijkertijd geopend zijn voor dezelfde gebruiker en hetzelfde browsertype. (bijvoorbeeld wanneer gebruiker A zowel omgeving 1 als omgeving 2 bekijkt in Chrome). Het maakt niet uit of de gebruikers verschillende browservensters of -tabbladen openen. Als dezelfde gebruikersreferenties worden gebruikt voor de gelijktijdige aanmelding bij omgeving 1 en 2 in hetzelfde browsertype, wordt in Human Resources de verbinding met een van de sessies verbroken.

**Oplossing**

Zorg dat altijd slechts één omgeving tegelijk is geopend voor een bepaald browsertype. Gebruikers kunnen meerdere sessies naar dezelfde omgeving openen (meerdere tabbladen in dezelfde browser).

Gebruikers die tegelijkertijd tussen twee omgevingen willen schakelen, moeten deze omgevingen in verschillende browsertypen openen. (Gebruiker A kan omgeving 1 bijvoorbeeld in Chrome en omgeving 2 in Microsoft Edge openen.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]