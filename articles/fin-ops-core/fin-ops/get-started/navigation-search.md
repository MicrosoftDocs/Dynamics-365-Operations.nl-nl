---
title: Navigatiezoekfunctie
description: In dit artikel wordt uitgelegd hoe u met de zoekfunctionaliteit naar pagina's navigeert.
author: jasongre
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 25991
ms.assetid: eef0676f-c4b1-490e-a032-e9c8580f3fea
ms.openlocfilehash: 4c362e4cd83f926e7e21d775abd24ae6ddfcbbed
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292332"
---
# <a name="navigation-search"></a>Navigatiezoekfunctie

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

In dit artikel wordt uitgelegd hoe u met de zoekfunctionaliteit naar pagina's navigeert.

De toepassing bevat een aantal gebieden en pagina's waarmee u verschillende taken kunt uitvoeren. Met de navigatiezoekfunctie kunt u snel de pagina's vinden die u nodig hebt om uw taken uit te voeren.

Als u deze functie wilt gebruiken, klikt op het pictogram **Zoeken** om het vak **Zoeken** weer te geven. U kunt vervolgens een of meer woorden in het vak typen. Het systeem zoekt onmiddellijk naar relevante pagina's in de toepassing die aan de ingevoerde woorden voldoen. U kunt bijvoorbeeld 'leveranciersfactuur' typen en vervolgens worden de resultaten weergegeven die met die invoer overeenkomen.

> [!NOTE]
> Het vak **Zoeken** help u te zoeken naar pagina's en deze te openen. De functie helpt u niet om bepaalde gegevens of acties te vinden.

![zoekvak.](media/navigation-search.png "Zoekvak")

## <a name="quickly-navigate-to-a-particular-page"></a>Snel naar een bepaalde pagina navigeren

De navigatiezoekfunctie is ook erg handig om snel naar een bepaalde pagina te navigeren. Als u bijvoorbeeld als crediteurenadministrateur vaak de pagina **Betalingsjournaal** gebruikt, kunt u 'betalingsjournaal' opgeven in het **zoekvak**. Omdat de invoer een exacte overeenkomst met de titel vormt, staat de pagina bovenaan in de lijst met zoekresultaten en kunt u er snel naartoe navigeren.

De zoekresultatenlijst geeft zowel de paginatitel als het navigatiepad weer. Dit toont de locatie van de pagina in de toepassing. Het helpt u ook om onderscheid te maken tussen twee of meer vergelijkbare pagina's in de resultaten.

Wanneer u naar een pagina zoekt, wordt uw invoer vergeleken met de paginatitel en het bijbehorende navigatiepad. U voert bijvoorbeeld 'klant' in het vak **Zoeken** in. U ziet dan resultaten voor de pagina's die beschikbaar voor u zijn in het gebied Klanten, hoewel de paginatitels niet het woord 'klant' bevatten.

## <a name="quickly-navigate-to-a-page-based-on-the-technical-form-name"></a>Snel naar een pagina navigeren op basis van de technische formuliernaam

De navigatiezoekfunctionaliteit bevat ook een veelgevraagde functie voor hoofdgebruikers: de mogelijkheid om snel naar een pagina te navigeren op basis van de technische formuliernaam. Veel gebruikers zijn zo vertrouwd met het systeem dat ze de exacte formuliernamen weten waarmee ze werken. Als u een van deze gebruikers bent, kunt u **formulier:** gevolgd door de naam van het formulier dat u zoekt invoeren. Stel, u voert **formulier: levfactuur** in, dan geven de zoekresultaten alle pagina's weer waarvan de formuliernaam begint met **levfactuur**.

## <a name="administration-and-security"></a>Beheer en beveiliging

Vanuit administratieve en beveiligingsoverwegingen haalt de navigatiezoekfunctionaliteit alleen twee typen resultaten op:

- Pagina's die in de huidige configuratie zijn ingeschakeld (via configuratiesleutels).
- Pagina's waartoe de gebruiker toegang heeft op basis van de rol van de gebruiker.

De lijst van de zoekresultaten is beperkt tot 10 items. Als in de resultaten niet vindt waarnaar u op zoek was, moet u de invoer verfijnen of wijzigen.

## <a name="development"></a>Ontwikkeling

Vanuit ontwikkelingsperspectief is de navigatiezoekfunctionaliteit heel handig te leveren omdat er vrijwel geen vertraging is tussen de levering van menuopdrachten en het vermogen te verschijnen in de zoekresultaten. Zolang de menu-items aan het navigatievenster of het dashboard zijn gekoppeld, worden ze automatisch doorzoekbaar.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
