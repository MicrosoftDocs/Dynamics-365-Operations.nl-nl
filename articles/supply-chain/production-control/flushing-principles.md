---
title: Wisprincipes
description: Dit artikel beschrijft de vier wisprincipes die voor verbruik van grondstoffen worden gebruikt.
author: johanhoffmann
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgShopSupervisorReleaseOrders
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 89fd38ea6d2c1635e9d8974ab99c2e4cdae4d6be
ms.sourcegitcommit: 8d072505f66f507aafbaae65bedf3b530eb6cb7b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9266423"
---
# <a name="flushing-principles"></a>Wisprincipes

[!include [banner](../includes/banner.md)]

De wisprincipes vertegenwoordigen verschillende verbruikstrategieën voor grondstoffen die worden gebruikt in de productieprocessen. Verbruik is het proces dat materiaal van de voorhanden voorraad aftrekt en de waarde van het verbruikte materiaal instelt op **Onderhanden werk** (OHW) voor productieorders en batchorders. Grondstoffen worden meestal verbruikt vanaf een locatie die is geconfigureerd voor het proces waarbij het materiaal wordt verbruikt. Deze locatie wordt de productie-invoerlocatie genoemd.

De materialen worden voordat het materiaal wordt verbruikt, verplaatst naar de invoerlocatie. De volgende afbeelding licht het proces toe.

[![scenario4a.](./media/scenario4a.png)](./media/scenario4a.png)

1. Materiaalmagazijn
2. Orderverzameling van grondstoffen
3. Productie-invoerlocatie
4. Verbruik grondstoffen
5. Productieproces

Het materiaalverbruik wordt beheerd door volgende vier wisprincipes:

- Handmatig
- Beginnen
- Voltooien
- Beschikbaar op locatie

De wisprincipes worden geconfigureerd in een hiërarchie van standaardwaarden. De hiërarchie begint bij het vrijgegeven product, waarbij het wisprincipe de waarde **Beginnen** heeft. Op de stuklijst (BOM) of formuleregel kan het wisprincipe van het product worden overschreven. Het standaardwisprincipe op de productiestuklijstregels of de formuleregels van de batchorder wordt overgenomen van het product of de overschreven waarde op de stuklijst of in de formules.

## <a name="description-of-the-flushing-principles"></a>Omschrijving van de wisprincipes

### <a name="manual"></a>Handmatig
Het handmatige wisprincipe geeft aan dat de registratie van materiaalverbruik een handmatige bewerking is. Dit principe is relevant als u bijvoorbeeld de tijd wilt bijhouden en de hoeveelheid verbruikte batchnummers of serienummers moeten worden verantwoord ter controle. Handmatig verbruik wordt geregistreerd in een orderverzamellijstjournaal voor de productie. Voor artikelen die zijn ingeschakeld voor magazijnbeheerprocessen (WMS), kan een handheld stroom worden toegepast.

### <a name="start"></a>Begin
Het wisprincipe Beginnen geeft aan dat materiaal automatisch wordt verbruikt wanneer de productieorder wordt gestart. De hoeveelheid materiaal die wordt verbruikt is evenredig aan de hoeveelheid die wordt gestart. Wanneer u het wisprincipe Beginnen samen met het productie-uitvoeringssysteem gebruikt, kan het ook worden gebruikt om materialen te wissen wanneer een bewerking of een procestaak is begonnen. Dit principe is van belang als, bijvoorbeeld de variantie in het verbruik laag is, de materialen een lage waarde hebben, er geen bijhoudvereisten zijn of er een korte uitvoeringstijd is voor de bewerkingen. 

### <a name="finish"></a>Voltooien
Het wisprincipe Voltooien geeft aan dat materiaal automatisch worden verbruikt wanneer de productieorder wordt gereedgemeld of wanneer een bewerking die wordt ingesteld op het verbruiken van de materialen, wordt geregistreerd als voltooid. De hoeveelheid materiaal die wordt verbruikt is evenredig aan de hoeveelheid die wordt gerapporteerd als voltooid. Wanneer u het wisprincipe Voltooien samen met het productie-uitvoeringssysteem gebruikt, kan het ook worden gebruikt om materialen te wissen wanneer een bewerking of een procestaak is voltooid. Dit principe is relevant voor dezelfde situaties als het principe Beginnen. Het principe Voltooien is echter bedoeld voor bewerkingen met een langere bewerkingstijd waar materialen niet moeten worden ingesteld op OHW voordat de bewerking is voltooid.

> [!NOTE]
> Wisprincipe voltooien kan niet samen met planningsartikelen worden gebruikt. Wij raden aan om in plaats daarvan de entiteit Wisprincipe beginnen te gebruiken. Planningsartikelen hebben producttype *Planningsartikel*, en er kunnen alleen co-producten en bijproducten als voltooid worden gemeld voor batchorders die voor planningsartikelen zijn aangemaakt.

### <a name="available-at-location"></a>Beschikbaar op locatie
Het wisprincipe Beschikbaar op locatie geeft aan dat het materiaal automatisch wordt verbruikt wanneer het wordt geregistreerd als gepickt voor productie. Het materiaal is geregistreerd als gepickt vanaf locatie, wanneer het verzamelen van de grondstoffen is voltooid of wanneer materiaal beschikbaar is op de productie-invoerlocatie en de materiaalregel wordt vrijgegeven voor het magazijn. De orderverzamellijst die wordt gegenereerd tijdens het proces wordt geboekt in een batchtaak. Dit principe is relevant als u bijvoorbeeld veel orderverzamelactiviteiten voor één productieorder hebt. In dit geval hoeft u de orderverzamellijst niet handmatig bij te werken en krijgt u een actuele weergave van het OHW-saldo.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
