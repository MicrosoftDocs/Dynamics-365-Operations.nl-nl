---
title: Beoordelings- en recensiemodules
description: In dit onderwerp worden de modules voor beoordelingen en recensies beschreven die worden gebruikt op de pagina's met productdetails in Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: Release 10.0.6
ms.openlocfilehash: dee9a6a7e2a5278f069958ce00689b1beb9b1bd7
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792142"
---
# <a name="ratings-and-reviews-modules"></a>Beoordelings- en recensiemodules

[!include [banner](includes/banner.md)]

In dit onderwerp worden de modules voor beoordelingen en recensies beschreven die worden gebruikt op de pagina's met productdetails (PDP's) in Microsoft Dynamics 365 Commerce.

Beoordelingen en recensies over e-commerce-websites geven klanten meer informatie over producten voordat ze een aankoopbeslissing nemen en vormen tevens een mechanisme voor het verzamelen van feedback van klanten over producten. 

Beoordelingen worden weergegeven op pagina's met productlijsten, lijstpagina's categorieën of zoekresultaten en andere sitepagina's. 

Beoordelingshistogrammen en productrecensies worden weergegeven op PDP's. Met een knop **Schrijf een recensie** kunnen klanten beoordelingen en recensies voor een product verzenden. Deze PDP-functies worden geregeld door middel van modules voor beoordelingen en recensies.

## <a name="ratings-and-reviews-modules-on-pdps"></a>Beoordelings- en recensiemodules op pagina's met productgegevens 

Drie modules geven een overzicht van beoordelingen en recensies voor pagina's met productgegevens:
- Module voor recensie schrijven
- Module met productrecensie
- Module met beoordelingshistogram
 
In de volgende afbeelding ziet u hoe de modules voor beoordelingen en recensies er uitzien op een PDP.

![Beoordelings- en recensiemodules op een PDP](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> Zie [Overzicht van sjablonen en indelingen](templates-layouts-overview.md) voor informatie over het optimaliseren van de PDP-sjablonen en -indelingen zodat u de configuraties voor beoordelingen en revisies kunt delen tussen meerdere PDP-pagina's op uw e-commerce-site.

In de volgende afbeelding ziet u hoe in het dialoogvenster **Module toevoegen** modules voor beoordelingen en recensies in Dynamics 365 Commerce worden weergegeven.
![Het dialoogvenster Module toevoegen](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a>Module voor recensie schrijven

De module voor het schrijven van een recensie bevat een knop **Schrijf een recensie** waarmee gebruikers zich kunnen aanmelden, een beoordeling kunnen toewijzen en een recensie van een product kunnen schrijven. Met deze module kunnen gebruikers ook een beoordeling of een recensie bewerken die ze eerder hebben ingediend. Deze module wordt meestal weergegeven boven het beoordelingshistogram en de lijstmodules met productrecensies op een PDP.
In de volgende afbeelding ziet u het dialoogvenster **Schrijf een recensie** dat wordt weergegeven wanneer een klant **Schrijf een recensie** selecteert. De klant kan dit dialoog venster gebruiken om een beoordeling en een recensie in te dienen.
![Dialoogvenster Schrijf een recensie](media/rnr-eCommerce-write-review-module.png) In de volgende tabel wordt de eigenschap van de module voor het schrijven van een recensie weergegeven die moet worden geconfigureerd in het ontwerpgereedschap.
| Naam van eigenschap. | Waarde        | Beschrijving eigenschap                 |
|---------------|--------------|--------------------------------------|
| Naam          | Recensie schrijven | De naam van de module voor het schrijven van een recensie. |

### <a name="ratings-histogram-module"></a>Module met beoordelingshistogram

In de module met het beoordelingshistogram wordt een beoordelingshistogram weergegeven. Deze module wordt meestal weergegeven tussen de module Schrijf een recensie en de module met de productrecensielijst op een PDP-pagina.
Voor de module met het beoordelingshistogram is geen configuratie vereist. U hoeft de module alleen aan de PDP-sjabloon toe te voegen. De volgende illustraties laten zien hoe een PDP-sjabloon eruitziet in Dynamics 365 Commerce wanneer de modules voor beoordelingen en recensies zijn geconfigureerd voor weergave op productbeschrijvingen.
![PDP-sjabloon wanneer beoordelingen en recensies zijn geconfigureerd voor weergave in productbeschrijvingen](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a>Module met productrecensie

In de module met productrecensies wordt een lijst met productrecensies weergegeven met opties voor sorteren, filteren en paginering. Deze module wordt normaal gesproken weergegeven na de module met het beoordelingshistogram.
In de volgende tabel worden de eigenschappen van de module voor productrecensielijsten weergegeven die moet worden geconfigureerd in het ontwerpgereedschap.

| Naam van eigenschap.              | Waarde | Beschrijving eigenschap |
|----------------------------|-------| ---------------------|
| Recensies die op elke pagina worden weergegeven | 10    | Het aantal recensies dat tegelijk op een PDP moet worden weergegeven. De knoppen **Volgende** en **Vorige** zijn opgenomen, zodat gebruikers door de pagina's met recensies kunnen navigeren. |

#### <a name="ratings-histogram--summary-view"></a>Beoordelingshistogram – overzichtsweergave

De module met de productrecensielijst bevat een vak waarin u een beoordelingshistogrammodule kunt toevoegen. In de volgende afbeelding ziet u hoe u een beoordelingshistogrammodule in de module met de productrecensielijst kunt toevoegen in Dynamics 365 Commerce.

![Een beoordelingshistogrammodule toevoegen aan de module met de productrecensielijst](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Containermodule](add-container-module.md)

[Winkelwagenmodule](add-cart-module.md)

[Kassamodule](add-checkout-module.md)

[Orderbevestigingsmodule](order-confirmation-module.md)

[Koptekstmodule](author-header-module.md)

[Voettekstmodule](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]