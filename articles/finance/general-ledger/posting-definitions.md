---
title: Boekdefinities
description: Dit artikel bevat informatie over boekdefinities en hoe u deze definieert en koppelt. Voor ondersteunde boekingstypen en documenten kunt u boekdefinities in plaats van boekingsprofielen gebruiken om hoofdrekeningen en financiële dimensies voor boekhoudvermeldingen te classificeren.
author: ShylaThompson
manager: AnnBe
ms.date: 09/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans, LedgerParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15741
ms.assetid: 1495e7e0-2e39-464c-8da9-f55b1ca1c6bb
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 22a7b0acae02738e4f14905edb13fac1da0d0213
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441986"
---
# <a name="posting-definitions"></a>Boekdefinities

[!include [banner](../includes/banner.md)]

Dit artikel bevat informatie over boekdefinities en hoe u deze definieert en koppelt.
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


Zie voor meer informatie [Voorbeelden van boekdefinities](example-posting-definitions.md). 




[!INCLUDE[footer-include](../../includes/footer-banner.md)]