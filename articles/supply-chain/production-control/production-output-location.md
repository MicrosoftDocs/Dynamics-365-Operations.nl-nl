---
title: Productie-uitvoerlocatie
description: "In dit onderwerp wordt de hiërarchie beschreven die wordt gebruikt ter identificatie van de uitvoerlocatie van de productie."
author: johanhoffmann
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: e53c8e96579dba3b47bef0c00e55b8fa786fc55c
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---

# <a name="production-output-location"></a>Productie-uitvoerlocatie

[!include[banner](../includes/banner.md)]

In dit onderwerp wordt de hiërarchie beschreven die wordt gebruikt ter identificatie van de uitvoerlocatie van de productie.

De productie-uitvoerlocatie is de locatie waar een eindproduct eerst wordt opgeslagen nadat het is geproduceerd. Deze locatie bevindt zich meestal in de buurt van het productieproces dat het gerede product produceert. De productie-uitvoerlocatie wordt gebruikt als tussentijdse opslag voor het materiaal voordat het wordt verplaatst naar het verzendgebied, een opslaglocatie, een productie-invoerlocatie voor een stroomafwaartse productieproces, enzovoort. 

Een standaardlocatie voor de productie-uitvoer wordt ingesteld wanneer eindproducten worden gemeld op een productieorder of batchorder. De volgende hiërarchie wordt gebruikt voor deze uitvoerlocatie:

1. Gebruik de uitvoerlocatie die wordt gedefinieerd in de koptekst van de productieorder of batchorder.
2. Als er geen locatie wordt gevonden, gebruikt u de uitvoerlocatie die wordt gedefinieerd voor de bron die is gebruikt door de laatste bewerking die is gedefinieerd in de productieroute.
3. Als er geen locatie wordt gevonden, gebruikt u de uitvoerlocatie die wordt gedefinieerd voor de brongroep die is gebruikt door de bron voor de laatste bewerking die is gedefinieerd in de productieroute.
4. Als er geen locatie wordt gevonden, gebruikt u de uitvoerlocatie die is gedefinieerd in het magazijn dat is gedefinieerd voor de productieorder.

Een standaardlocatie voor de productie-uitvoer wordt alleen ingesteld voor producten die zijn ingesteld met geavanceerde magazijnprocessen. Wanneer dit type artikel is gereedgemeld, wordt een magazijntaak van het type **Eindproducten wegzetten** of **Coproducten en bijproducten wegzetten** gemaakt. Dit type tak gebruikt de productie-uitvoerlocatie als orderverzamellocatie. De opslaglocatie wordt bepaald door de richtlijnen van de locatie.
