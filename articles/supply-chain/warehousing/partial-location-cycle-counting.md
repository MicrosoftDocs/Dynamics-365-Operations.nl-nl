---
title: Gedeeltelijke cyclustelling van locatie
description: Cyclustellingsplannen sturen de werkelijke telbewerkingen aan. U kunt verzoeken dat alleen specifieke producten en productvarianten worden geteld, in plaats van alle voorhanden voorraad op een locatie.
author: perlynne
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable, WHSRFMenuItemCycleCount, WHSCycleCountPlanListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9f06b39f3c2d2f5a0bdfef1da9395c71686ed46968a1143305b5a10787f7e85f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778429"
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

Voor het gedeeltelijke cyclustellingsproces wordt de datum/tijd **Laatste cyclustelling** voor de locatie niet bijgewerkt, ook niet als alle voorhanden artikelen op een bepaalde locatie worden geteld. De gedeeltelijke cyclustelling houdt geen rekening met de parameter **Dagen tussen cyclustellingen** op de pagina **Cyclustelplannen**. Gedeeltelijke cyclustelling biedt geen ondersteuning voor gelijktijdige telling van meerdere artikelen op dezelfde locatie. De functionaliteit voor gedeeltelijke cyclustellingen kan ertoe leiden dat dezelfde locatie meerdere keren wordt geteld voor een artikel wanneer **Cyclustellingsplan verwerken** wordt uitgevoerd. Geef filters op in het veld **Locaties selecteren** om dat scenario te vermijden.

> [!NOTE]
> De mobiele app Magazijnbeheer beschikt niet over de knop **LP of artikel toevoegen** wanneer u het gedeeltelijke cyclustellingsproces gebruikt.

## <a name="example"></a>Voorbeeld

In dit voorbeeld moet alleen artikelnummer A0001 in magazijn 61 worden geteld.

1. Een nieuwe werksjabloon voor cyclustelling wordt gemaakt. Met de optie **Opsplitsing werkregels** worden telwerkregels gegroepeerd op artikelnummer. Daarom heeft het aangemaakte cyclustellingswerk regels op artikelnummer. U kunt de regels ook groeperen op productvariantnummer.
1. Een nieuw cyclustellingsplan wordt gemaakt, dat verwijst naar de zojuist gemaakte werksjabloon. Het cyclustellingsplan bevat alle locaties in magazijn 61 (query **Locaties selecteren**) die voorraad bevatten voor artikelnummer A0001. De selectie van specifieke producten wordt gedefinieerd in de sectie **Productselecties voor cyclustellingsplan**.
1. U kunt producten voor cyclustellingsplannen selecteren door het veld **Lege locaties** in te stellen op **Lege uitsluiten**. Wanneer het cyclustellingsplan wordt verwerkt, wordt gedeeltelijk cyclustellingswerk aangemaakt voor artikelnummer A0001. Het werkelijke telproces kan worden uitgevoerd via een mobiel menu-item voor geleide cyclustelling.

## <a name="additional-resources"></a>Aanvullende resources

[Cyclustelling](cycle-counting.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]