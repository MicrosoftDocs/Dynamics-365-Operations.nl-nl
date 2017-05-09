---
title: Navigatiezoekfunctie
description: In dit artikel wordt beschreven hoe u de zoekfunctionaliteit gebruikt om naar pagina&quot;s in Microsoft Dynamics 365 for Operations te navigeren.
author: aneesmsft
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25991
ms.assetid: eef0676f-c4b1-490e-a032-e9c8580f3fea
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 87fed576f8cf358520d94f5cd5b326ff9801913a
ms.lasthandoff: 03/31/2017


---

# <a name="navigation-search"></a>Navigatiezoekfunctie

[!include[banner](../includes/banner.md)]


In dit artikel wordt beschreven hoe u de zoekfunctionaliteit gebruikt om naar pagina's in Microsoft Dynamics 365 for Operations te navigeren.

Dynamics 365 for Operations bevat functionaliteit voor een uitgebreid aantal bedrijfstakken en verticalen. De toepassing bevat een aantal gebieden en pagina's waarmee u verschillende taken kunt uitvoeren. Met de navigatiezoekfunctie kunt u snel de pagina's vinden die u nodig hebt om uw taken uit te voeren. Als u deze functie wilt gebruiken, klikt op het pictogram **Zoeken** om het vak **Zoeken** weer te geven. U kunt vervolgens een of meer woorden in het vak typen. Het systeem zoekt onmiddellijk naar relevante pagina's in de toepassing die aan de ingevoerde woorden voldoen. U kunt bijvoorbeeld "leveranciersfactuur" typen en vervolgens worden de resultaten weergegeven die met die invoer overeenkomen. **Opmerking:** het vak **Zoeken** help u te zoeken naar pagina's en deze te openen. De functie helpt u niet om bepaalde gegevens of acties te vinden. 

[![Zoekvak](./media/search-box.png)](./media/search-box.png) De navigatiezoekfunctie is ook erg handig om snel naar een bepaalde pagina te navigeren. Als u bijvoorbeeld als crediteurenadministrateur vaak de pagina **Betalingsjournaal** gebruikt, kunt u 'betalingsjournaal' opgeven in het zoekvak. Omdat de invoer een exacte overeenkomst met de titel vormt, staat de pagina bovenaan in de lijst met zoekresultaten en kunt u er snel naartoe navigeren. 

[![Zoeken naar Betalingsjournaal](./media/searching-for-payment-journal.png)](./media/searching-for-payment-journal.png) 

De zoekresultatenlijst geeft zowel de paginatitel als het navigatiepad weer. Hiermee kunt u de locatie van de pagina in de toepassing vinden. Het helpt u ook om onderscheid te maken tussen twee of meer vergelijkbare pagina's in de resultaten. Wanneer u naar een pagina zoekt, wordt uw invoer vergeleken met de paginatitel en het bijbehorende navigatiepad. U typt bijvoorbeeld "klant" in het** **zoekvak. U ziet dan resultaten voor de pagina's die beschikbaar voor u zijn in het gebied Klanten, hoewel de paginatitels niet het woord "klant" bevatten. 

[![Naar het woord klanten zoeken](./media/search-for-the-word-receivable.png)](./media/search-for-the-word-receivable.png) 

Vanuit overwegingen van beheer en beveiliging haalt de navigatiezoekfunctionaliteit alleen het volgende op:

-   Pagina's die in de huidige configuratie zijn ingeschakeld (via configuratiesleutels).
-   Pagina's waartoe de gebruiker toegang heeft op basis van de rol van de gebruiker

De lijst van de zoekresultaten is beperkt tot 10 items. Als in de resultaten niet vindt waarnaar u op zoek was, moet u de invoer verfijnen of wijzigen. Vanuit ontwikkelingsperspectief is de navigatiezoekfunctionaliteit heel handig te leveren omdat er vrijwel geen vertraging is tussen de levering van menuopdrachten en het vermogen te verschijnen in de zoekresultaten. Zolang de menu-items aan het navigatievenster of het dashboard zijn gekoppeld, worden ze automatisch doorzoekbaar. De navigatiezoekfunctionaliteit bevat ook een veelgevraagde functie voor hoofdgebruikers: de mogelijkheid om snel naar een pagina te navigeren op basis van de technische formuliernaam. Veel gebruikers zijn zo vertrouwd met het systeem dat ze de exacte formuliernamen weten waarmee ze werken. Als u een van deze gebruikers bent, kunt u **formulier:** gevolgd door de naam van het formulier dat u zoekt invoeren. Stel, u voert **formulier: levfactuur** in, dan geven de zoekresultaten alle pagina's weer waarvan de formuliernaam begint met **levfactuur**. 

[![Zoeken naar formulier vendinvoice](./media/search-for-form-vendinvoice.png)](./media/search-for-form-vendinvoice.png)




