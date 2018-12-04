---
title: Gedeeltelijke cyclustelling van locatie
description: Cyclustellingsplannen sturen de werkelijke telbewerkingen aan. U kunt verzoeken dat alleen specifieke producten en productvarianten worden geteld, in plaats van alle voorhanden voorraad op een locatie.
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 643d9a07681beeffe90f39e5a0dc5ed9ad71b097
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---

# <a name="partial-location-cycle-counting"></a>Gedeeltelijke cyclustelling van locatie

[!include [banner](../includes/banner.md)]

Cyclustellingsplannen sturen de werkelijke telbewerkingen aan. U kunt verzoeken dat alleen specifieke producten en productvarianten worden geteld, in plaats van alle voorhanden voorraad op een locatie.

Als u telwerk maakt door middel van cyclustellingsplannen, kunt u de werkelijke telbewerkingen aansturen. U kunt verzoeken dat alleen specifieke producten en productvarianten worden geteld, in plaats van alle voorhanden voorraad op een locatie. Door te filteren op specifieke producten, kan de magazijnbeheerder de overhead voor controle verminderen, fouten bij consolidatie vermijden en tijd besparen.

## <a name="how-to-configure-partial-location-cycle-counting"></a>Gedeeltelijke cyclustelling van locatie instellen
Wanneer u het magazijnwerkproces gebruikt voor telbewerkingen, wordt een werkkoptekst gemaakt voor elke locatie. Wanneer u het cyclustellingsplan definieert, kunt u met de query **Locaties selecteren** het cyclustellingswerk beperken dat wordt aangemaakt. Wanneer u producten voor het cyclustellingsplan selecteert, selecteert u query's voor zowel producten als productvarianten om te verfijnen wat moet worden geteld. 

U kunt een **werksjabloon** aan een cyclustellingsplan koppelen, om te definiëren hoe het cyclustellingswerk moet worden gemaakt. De werksjabloon voor telbewerkingen wordt rechtstreeks aangeroepen vanuit het cyclustellingsplan. 

Wanneer u de gegevens van de werksjabloon definieert, kunt u met de optie **Werkregelopsplitsingen** opgeven of de telwerkregels moeten worden gegroepeerd op artikelnummer of op productvariantnummer. Deze instelling is vereist als u alleen voorhanden voorraad wilt tellen voor bepaalde producten op een locatie. De cyclustellingswerkregels die zijn gemaakt, hebben het niveau van de informatie die u hier definieert en de begeleide telbewerking worden afgewerkt op basis van dit niveau. 

Als u cyclustellingsplannen koppelt aan werksjablonen met behulp van de optie **Werkregels afbreken**, wordt het veld **Gedeeltelijke cyclustelling** ingeschakeld voor het cyclustellingswerk dat is gemaakt en meerdere cyclustellingswerkregels worden gemaakt op basis van de definitie van de werksjabloon. 

Voordat gedeeltelijk cyclustellingswerk kan worden verwerkt, moet u ten minste **Artikelnummer weergeven** selecteren voor het mobiele menuonderdeel als onderdeel van de instellingen voor cyclustelling. De magazijnoperator wordt gevraagd om alleen telinformatie vast te leggen die is gekoppeld aan de tellingsregels (artikelnummers en productdimensies). Alle overige voorhanden voorraad wordt voor dit telproces genegeerd. 

Voor het gedeeltelijke cyclustellingsproces wordt de datum/tijd **Laatste cyclustelling** voor de locatie niet bijgewerkt.

## <a name="example"></a>Voorbeeld
In dit voorbeeld moet alleen artikelnummer A0001 in magazijn 61 worden geteld.

1.  Een nieuwe werksjabloon voor cyclustelling wordt gemaakt. Met de optie **Opsplitsing werkregels** worden telwerkregels gegroepeerd op artikelnummer. Daarom heeft het aangemaakte cyclustellingswerk regels op artikelnummer. U kunt de regels ook groeperen op productvariantnummer.
2.  Een nieuw cyclustellingsplan wordt gemaakt, dat verwijst naar de zojuist gemaakte werksjabloon. Het cyclustellingsplan bevat alle locaties in magazijn 61 (query **Locaties selecteren**) die voorraad bevatten voor artikelnummer A0001. De selectie van specifieke producten wordt gedefinieerd in de sectie **Productselecties voor cyclustellingsplan**.
3.  U kunt producten voor cyclustellingsplannen selecteren door het veld **Lege locaties** in te stellen op **Lege uitsluiten**. Wanneer het cyclustellingsplan wordt verwerkt, wordt gedeeltelijk cyclustellingswerk aangemaakt voor artikelnummer A0001. Het werkelijke telproces kan worden uitgevoerd via een mobiel menu-item voor geleide cyclustelling.



<a name="additional-resources"></a>Aanvullende resources
--------

[Cyclustelling](cycle-counting.md)


