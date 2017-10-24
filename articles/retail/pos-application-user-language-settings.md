---
title: De taalinstellingen van de POS-toepassing en gebruiker
description: In dit onderwerp wordt beschreven hoe u taalinstellingen wijzigt in Retail Modern POS (MPOS) en Cloud POS.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: cabb63aea0da4b264aec8e0cc4d43b3e1014e71b
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="pos-application-and-user-language-settings"></a>De taalinstellingen van de POS-toepassing en gebruiker

[!include[banner](includes/banner.md)]


In dit onderwerp wordt beschreven hoe u taalinstellingen wijzigt in Retail Modern POS (MPOS) en Cloud POS.

<a name="overview"></a>Overzicht
========

Retail Modern POS (MPOS) en Cloud POS ondersteunen omgevingen waar de taalinstellingen en vertalingen tussen de winkel- en de gebruikerinstellingen kunnen verschillen. De winkel kan zich bijvoorbeeld bevinden in een regio waar klanten meestal Engels spreken, maar sommige werknemers kunnen er de voorkeur aan geven de toepassing te gebruiken met de Franse vertaling.

## <a name="data-language"></a>Gegevenstaal
Ongeacht de instellingen van de gebruiker gebruiken Retail Modern POS en Cloud POS altijd de taalinstellingen van de winkel om te bepalen welke vertalingen er voor gegevens moeten worden gebruikt. Dit zorgt ervoor dat alle gebruikers en klanten een consistente ervaring hebben.  Voorbeelden van de gegevens zijn:

-   Producten
-   Kenmerken en waarden
-   Categorienamen
-   Afgedrukte of ge-e-mailde transactieontvangstbewijzen
-   Namen betalingsmethodes
-   Regelweergaveberichten

De taal van de winkel wordt ook gebruikt voor het hoofdscherm voor aanmelding bij POS, aangezien de gebruiker niet bekend is voordat deze zich heeft aangemeld. Als geen vertaling beschikbaar is voor de taal van de winkel, wordt het POS teruggezet naar de taal van het bedrijf.

### <a name="configuring-the-stores-language-setting"></a>De taalinstelling van de winkel configureren

De taalinstelling van de winkel wordt ingesteld vanuit **Alle detailhandels** op de pagina **Detailhandel** onder Algemeen &gt; Landinstellingen &gt; Taal. **Gebruik de vervolgkeuzelijst om de taal voor elke winkel te kiezen.

## <a name="user-interface-language"></a>Taal gebruikersinterface
De taalinstellingen van de gebruiker van het POS bepalen welke vertalingen worden gebruikt in de gebruikersinterface van de toepassing. Dit omvat alle labels en menu's en lijsten die niet als gegevens worden beschouwd. Eén uitzondering hierop is de tekst die op POS-Knoppenrasters wordt weergegeven. Deze ondersteunen geen vertalingen, waardoor ze altijd de tekst weergeven die voor de knop is gedefinieerd. Om vertaalde knoppen te ondersteunen, moet u afzonderlijke knoppenrasters kopiëren en onderhouden en deze aan de juiste gebruikers toewijzen.

### <a name="configuring-the-users-language-setting"></a>De taalinstelling van de gebruiker configureren

De taalinstellingen van de gebruiker van het POS kunnen worden ingesteld via **Alle werknemers** op de pagina **Werknemer** onder **Detailhandel &gt; Taal**.  Het wordt niet ingesteld op het hoofdtabblad Profiel. Deze instelling wordt niet gebruikt door POS. Als de taal van de gebruiker niet is ingesteld of is ingesteld op een taal waarvoor geen vertalingen beschikbaar zijn, stapt het POS weer over op de taal van de winkel.  

|             |                            |                                                                   |
|-------------|----------------------------|-------------------------------------------------------------------|
| ** **       | **Taal van gebruikersinterface** ** **      | **Gegevenstaal (producten, ontvangstindelingen, regelweergave, enzovoort.)** |
| **Bedrijf** | Standaard                    | Standaard                                                           |
| **Winkel**   | Overschrijft bedrijf          | Overschrijft bedrijf                                                 |
| **Gebruiker**    | Overschrijft opslag of bedrijf | Nooit                                                             |






