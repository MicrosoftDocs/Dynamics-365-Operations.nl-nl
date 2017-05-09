---
title: Boekdefinities
description: "Dit artikel bevat informatie over boekdefinities en hoe u deze definieert en koppelt. Voor ondersteunde boekingstypen en documenten kunt u boekdefinities in plaats van boekingsprofielen gebruiken om hoofdrekeningen en financiële dimensies voor boekhoudvermeldingen te classificeren."
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans, LedgerParameters
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15741
ms.assetid: 1495e7e0-2e39-464c-8da9-f55b1ca1c6bb
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: 357ae498e84ef27e46142c7dcc0f90ecb0ee9f1c
ms.lasthandoff: 03/31/2017


---

# <a name="posting-definitions"></a>Boekdefinities

Dit artikel bevat informatie over boekdefinities en hoe u deze definieert en koppelt. Voor ondersteunde boekingstypen en documenten kunt u boekdefinities in plaats van boekingsprofielen gebruiken om hoofdrekeningen en financiële dimensies voor boekhoudvermeldingen te classificeren.

Voor ondersteunde boekingstypen en documenten kunt u boekdefinities in plaats van boekingsprofielen gebruiken om hoofdrekeningen en financiële dimensies voor boekhoudvermeldingen te classificeren. U kunt de ondersteunde documenten en boekingstypen op de pagina **Boekdefinities voor transacties** weergeven. 

Als u boekdefinities wilt gaan gebruiken, selecteert u de optie **Boekdefinities gebruiken** op de pagina **Grootboekparameters**. Zelfs wanneer u boekdefinities gebruikt, moet u nog steeds boekingsprofielen definiëren voor de oorspronkelijke vermeldingen en niet-ondersteunde boekingstypen en documenten. 

U moet boekdefinities gebruiken om vorderingsboekhouding in te schakelen voor inkooporders en voorvorderingsboekhouding voor opdrachten tot inkoop.

## <a name="defining-posting-definitions"></a>Boekdefinities definiëren
Gebruik de pagina **Boekdefinities** om de matchcriteria en de gegevens op te geven die moeten worden gegenereerd wanneer een overeenkomst optreedt. De matchcriteria worden geëvalueerd voor de oorspronkelijke invoer als boekhoudingsverdelingen. 

Op de pagina **Boekdefinities** kunt u ook prioriteitsnummers toewijzen aan invoerregels om de volgorde te bepalen waarin de regels worden geëvalueerd. De regels met het laagste prioriteitsnummer worden eerst geëvalueerd. Alle regels met prioriteit 1 worden bijvoorbeeld geëvalueerd, vervolgens regels met prioriteit 2, enzovoort. Wanneer een match wordt gevonden, worden de andere matchcriteria genegeerd. Bovendien maken alleen de criteria in de groep die overeenkomt met de oorspronkelijke transactie gegenereerde vermeldingen. 

U kunt uw boekdefinities valideren met behulp van de wizard **Boekdefinitie testen**. Nadat u een oorspronkelijke vermelding voor een boekdefinitie hebt gedefinieerd, ziet u de gegenereerde vermeldingen. 

U kunt boekdefinitieversies samen met ingangsdatums gebruiken. U kunt bijvoorbeeld een toekomstige versie maken van een boekingsdefinitie die in een nieuw boekjaar naar een andere grootboekrekening moet worden geboekt. 

Gebruik de pagina **Boekdefinities voor transacties** om boekdefinities toe te wijzen aan transactietypen.

## <a name="linking-posting-definitions"></a>Boekdefinities koppelen
U kunt van een boekingsdefinities naar een andere koppelen wanneer u boekingsdefinities maakt. Met de criteria voor de definitie waarmee u hebt gekoppeld, wordt vervolgens rekening gehouden naast de criteria voor de huidige boekdefinitie. Deze functie bespaart u tijd, omdat u criteria niet opnieuw hoeft in te voeren op het sneltabblad **Vermeldingen** op de pagina **Boekdefinities** voor de huidige boekdefinitie als u deze regels al voor een andere definitie hebt ingevoerd. 

Vermeld alle koppelingen die u wellicht gebruikt in de diagrammen of tabellen. Zorg ervoor dat de regels in alle boekdefinities waarnaar u koppelt, uniek zijn om conflicten met de huidige boekdefinitie te voorkomen. 

De volgende beperkingen gelden wanneer u koppelingen maakt in boekingsdefinities.

-   Een bepaalde boekdefinitie kan een koppeling zijn naar een andere boekdefinitie of er kan naar worden gekoppeld via een andere boekdefinitie, maar niet beide. Een boekdefinitie kan echter met meerdere boekdefinities worden gekoppeld.
-   U kunt uitsluitend koppelingen instellen tussen boekingsdefinities in dezelfde module.
-   U kunt een boekingsdefinitie toewijzen aan ieder transactietype, maar het transactietype moet zich in dezelfde module bevinden als de boekingsdefinitie. Gebruik de pagina **Boekdefinities voor transacties** om te zien in welke module een transactietype zich bevindt.


Zie voor meer informatie [Voorbeelden van boekingsdefinities](/general-ledger/example-posting-definitions.md). 

