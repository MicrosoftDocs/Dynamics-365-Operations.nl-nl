---
title: Producten cross-docken vanuit ontvangend magazijn naar winkels
description: Deze procedure doorloopt de stappen om een cross-dock te maken en te verwerken om producten van de ontvangende locatie van een inkooporder naar een of meer winkels te distribueren.
author: ShylaThompson
manager: AnnBe
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f38c2ad9561cc1a1c775c27aec54681124cffeec
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004083"
---
# <a name="cross-dock-products-from-receiving-warehouse-to-stores"></a>Producten cross-docken vanuit ontvangend magazijn naar winkels

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure doorloopt de stappen om een cross-dock te maken en te verwerken om producten van de ontvangende locatie van een inkooporder naar een of meer winkels te distribueren. De gebruiker kan meerdere configuraties definiëren en het systeem laten voorstellen hoe u de producten wilt verdelen, of handmatig invoeren waar de producten naar worden gedistribueerd en hoeveel naar elke winkel wordt verdeeld. De procedure bevat geen instelling van gegevens die in het cross-dock kunnen worden gebruikt, zoals aanvullingsregels, organisatiehiërarchieën en winkelgewichten. De procedure gebruikt het demobedrijf USRT.

1. Ga naar Alle inkooporders.
2. Selecteer een inkooporder in de lijst en klik op de koppeling om de order te openen.
3. Klik in het actievenster op Retail en Commerce.
4. Klik op Cross-docken.
5. Klik op Bewerken.
    * De categorie kan worden gebruikt om de artikelen in de sectie Regels te filteren.  
6. Zoek en selecteer de gewenste record in de lijst.
7. Typ een waarde in het veld Hoeveelheid voor cross-docken om op te geven hoeveel van de ingekochte hoeveelheid van het geselecteerde product moet worden verdeeld.
8. Voer in het veld Toegevoegde hoeveelheid voor cross-docken een waarde in om de hoeveelheden op te geven om te distribueren voor de beschikbare producten die worden ingekocht.
9. Voer in het veld Distributie 'Locatiegewicht' in.
    * U kunt de andere typen selecteren om de verschillende regels voor de verdeling te gebruiken.  
10. Selecteer een waarde in het veld Aanvullingshiërarchie.
11. Selecteer Ja in het veld Assortimenten respecteren.
12. Klik op Hoeveelheden berekenen.
13. Klik op Order maken.
14. Klik op Ja.
15. Zoek en selecteer in de lijst een magazijn dat producten heeft ontvangen.
16. Klik op Order om de orders weer te geven die voor het geselecteerde magazijn zijn gemaakt

