---
title: Taalinstellingen voor verkooppunttoepassing (POS) en gebruiker
description: In dit onderwerp wordt beschreven hoe u taalinstellingen wijzigt in Modern POS (MPOS) en Cloud POS.
author: jblucher
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: bdd03dff359e7c2799eff53b0e999580ce8b1c06
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193098"
---
# <a name="point-of-sale-pos-application-and-user-language-settings"></a>Taalinstellingen voor verkooppunttoepassing (POS) en gebruiker

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u taalinstellingen wijzigt in Modern POS (MPOS) en Cloud POS.

## <a name="overview"></a>Overzicht
Modern POS (MPOS) en Cloud POS ondersteunen omgevingen waar de taalinstellingen en vertalingen tussen de winkel- en de gebruikerinstellingen kunnen verschillen. De winkel kan zich bijvoorbeeld bevinden in een regio waar klanten meestal Engels spreken, maar sommige werknemers kunnen er de voorkeur aan geven de toepassing te gebruiken met de Franse vertaling.

## <a name="data-language"></a>Gegevenstaal

Ongeacht de instellingen van de gebruiker gebruiken MPOS en Cloud POS altijd de taalinstellingen van de winkel om te bepalen welke vertalingen er voor gegevens moeten worden gebruikt. Dit zorgt ervoor dat alle gebruikers en klanten een consistente ervaring hebben. Voorbeelden van de gegevens zijn:

- Producten
- Kenmerken en waarden
- Categorienamen
- Afgedrukte of ge-e-mailde transactieontvangstbewijzen
- Namen betalingsmethodes
- Regelweergaveberichten

De taal van de winkel wordt ook gebruikt voor het hoofdscherm voor aanmelding bij POS, aangezien de gebruiker niet bekend is voordat deze zich heeft aangemeld. Als geen vertaling beschikbaar is voor de taal van de winkel, wordt het POS teruggezet naar de taal van het bedrijf.

### <a name="configuring-the-stores-language-setting"></a>De taalinstelling van de winkel configureren

De taalinstelling van de winkel wordt ingesteld vanuit **Alle winkels** op de pagina **Winkel** onder **Algemeen &gt; Landinstellingen &gt; Taal**. Gebruik de vervolgkeuzelijst om de taal voor elke winkel te kiezen.

## <a name="user-interface-language"></a>Taal gebruikersinterface

De taalinstellingen van de gebruiker van het POS bepalen welke vertalingen worden gebruikt in de gebruikersinterface van de toepassing. Dit omvat alle labels en menu's en lijsten die niet als gegevens worden beschouwd. Eén uitzondering hierop is de tekst die op POS-Knoppenrasters wordt weergegeven. Deze ondersteunen geen vertalingen, waardoor ze altijd de tekst weergeven die voor de knop is gedefinieerd. Om vertaalde knoppen te ondersteunen, moet u afzonderlijke knoppenrasters kopiëren en onderhouden en deze aan de juiste gebruikers toewijzen.

### <a name="configuring-the-users-language-setting"></a>De taalinstelling van de gebruiker configureren

De taalinstellingen van de gebruiker van het POS kunnen worden ingesteld via **Alle werknemers** op de pagina **Werknemer** onder **Retail en Commerce &gt; Taal**. Deze instelling wordt niet ingesteld op het hoofdtabblad Profiel. Deze instelling wordt niet gebruikt door POS. Als de taal van de gebruiker niet is ingesteld of is ingesteld op een taal waarvoor geen vertalingen beschikbaar zijn, stapt het POS weer over op de taal van de winkel.

| &nbsp;      | Taal van gebruikersinterface                   | Gegevenstaal (producten, ontvangstindelingen, regelweergave, enzovoort.) |
|-------------|----------------------------|---------------------------------------------------------------|
| **Bedrijf** | Standaard                    | Standaard                                                       |
| **Winkel**   | Overschrijft bedrijf          | Overschrijft bedrijf                                             |
| **Gebruiker**    | Overschrijft opslag of bedrijf | Nooit                                                         |


[!INCLUDE[footer-include](../includes/footer-banner.md)]