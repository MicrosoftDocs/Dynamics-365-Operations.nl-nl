---
title: Navigatiezoekfunctie
description: In dit onderwerp wordt beschreven hoe u de zoekfunctionaliteit gebruikt om naar pagina's in Microsoft Dynamics 365 for Finance and Operations te navigeren.
author: aneesmsft
manager: AnnBe
ms.date: 04/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 25991
ms.assetid: eef0676f-c4b1-490e-a032-e9c8580f3fea
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 431165d541c9a3b63100a93108ee770df8e88aa8
ms.contentlocale: nl-nl
ms.lasthandoff: 06/13/2017

---

# <a name="navigation-search"></a>Navigatiezoekfunctie

[!include[banner](../includes/banner.md)]


In dit onderwerp wordt beschreven hoe u de zoekfunctionaliteit gebruikt om naar pagina's in Microsoft Dynamics 365 for Finance and Operations te navigeren.

Finance and Operations bevat functionaliteit voor een uitgebreid aantal bedrijfstakken en verticalen. De toepassing bevat een aantal gebieden en pagina's waarmee u verschillende taken kunt uitvoeren. Met de navigatiezoekfunctie kunt u snel de pagina's vinden die u nodig hebt om uw taken uit te voeren. 

Als u deze functie wilt gebruiken, klikt op het pictogram **Zoeken** om het vak **Zoeken** weer te geven. U kunt vervolgens een of meer woorden in het vak typen. Het systeem zoekt onmiddellijk naar relevante pagina's in de toepassing die aan de ingevoerde woorden voldoen. U kunt bijvoorbeeld "leveranciersfactuur" typen en vervolgens worden de resultaten weergegeven die met die invoer overeenkomen. 

**Opmerking:** het vak **Zoeken** help u te zoeken naar pagina's en deze te openen. De functie helpt u niet om bepaalde gegevens of acties te vinden. 

[![search-box](media/navigation-search.png "Zoekvak") 

## <a name="quickly-navigate-to-a-particular-page"></a>Snel naar een bepaalde pagina navigeren
De navigatiezoekfunctie is ook erg handig om snel naar een bepaalde pagina te navigeren. Als u bijvoorbeeld als crediteurenadministrateur vaak de pagina **Betalingsjournaal** gebruikt, kunt u 'betalingsjournaal' opgeven in het **zoekvak**. Omdat de invoer een exacte overeenkomst met de titel vormt, staat de pagina bovenaan in de lijst met zoekresultaten en kunt u er snel naartoe navigeren. 

De zoekresultatenlijst geeft zowel de paginatitel als het navigatiepad weer. Dit toont de locatie van de pagina in de toepassing. Het helpt u ook om onderscheid te maken tussen twee of meer vergelijkbare pagina's in de resultaten. 

Wanneer u naar een pagina zoekt, wordt uw invoer vergeleken met de paginatitel en het bijbehorende navigatiepad. U voert bijvoorbeeld "klant" in het **zoekvak** in. U ziet dan resultaten voor de pagina's die beschikbaar voor u zijn in het gebied Klanten, hoewel de paginatitels niet het woord "klanten" bevatten. 

## <a name="quickly-navigate-to-a-page-based-on-the-technical-form-name"></a>Snel naar een pagina navigeren op basis van de technische formuliernaam
De navigatiezoekfunctionaliteit bevat ook een veelgevraagde functie voor hoofdgebruikers: de mogelijkheid om snel naar een pagina te navigeren op basis van de technische formuliernaam. Veel gebruikers zijn zo vertrouwd met het systeem dat ze de exacte formuliernamen weten waarmee ze werken. Als u een van deze gebruikers bent, kunt u **formulier:** gevolgd door de naam van het formulier dat u zoekt invoeren. Stel, u voert **formulier: levfactuur** in, dan geven de zoekresultaten alle pagina's weer waarvan de formuliernaam begint met **levfactuur**. 

## <a name="administration-and-security"></a>Beheer en beveiliging
Vanuit administratieve en beveiligingsoverwegingen haalt de navigatiezoekfunctionaliteit alleen twee typen resultaten op:

-   Pagina's die in de huidige configuratie zijn ingeschakeld (via configuratiesleutels).
-   Pagina's waartoe de gebruiker toegang heeft op basis van de rol van de gebruiker.

De lijst van de zoekresultaten is beperkt tot 10 items. Als in de resultaten niet vindt waarnaar u op zoek was, moet u de invoer verfijnen of wijzigen. 

## <a name="development"></a>Ontwikkeling 
Vanuit ontwikkelingsperspectief is de navigatiezoekfunctionaliteit heel handig te leveren omdat er vrijwel geen vertraging is tussen de levering van menuopdrachten en het vermogen te verschijnen in de zoekresultaten. Zolang de menu-items aan het navigatievenster of het dashboard zijn gekoppeld, worden ze automatisch doorzoekbaar. 
