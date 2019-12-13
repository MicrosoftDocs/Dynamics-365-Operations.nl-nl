---
title: Overzicht productaanbevelingen
description: Dit onderwerp biedt algemene informatie over het productaanbevelingen. Met productaanbevelingen kunnen klanten gemakkelijk en snel producten vinden die ze willen en zelfs producten die ze oorspronkelijk niet willen kopen.
author: Moonma
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: eb369e6d1356ba13a2310d523b671ac57b9642bf
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770041"
---
# <a name="product-recommendations-overview"></a>Overzicht productaanbevelingen

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Commerce kan worden gebruikt om productaanbevelingen weer te geven op de e-commercewebsite en het POS-apparaat (Point of Sale). Productaanbevelingen zijn artikelen waarin een klant mogelijk geïnteresseerd is. De aanbevelingen zijn gebaseerd op de inkooptrends van andere klanten in online en fysieke winkels.

Met productaanbevelingen kunnen klanten gemakkelijk en snel producten vinden die ze willen, terwijl ze een goede bediening ervaren. Door middel van meerverkoop/bijverkoop kunnen klanten extra producten zoeken die ze oorspronkelijk niet zouden willen kopen. Wanneer aanbevelingen worden gebruikt om productdetectie te bevorderen, kunnen ze meer conversiemogelijkheden creëren, de verkoopopbrengsten verhogen en zelfs de klanttevredenheid en -retentie verbeteren.

In Commerce worden productaanbevelingen op grote schaal aangestuurd door machine learning technologie voor Microsoft-aanbevelingen.


## <a name="scenarios"></a>Scenario's

Productaanbevelingen zijn beschikbaar voor de volgende scenario's:

- **Op elke winkelpagina voor browsen of landingspagina's in e-commerce:** als klanten of winkelmedewerkers een winkelpagina bezoeken, kan de aanbevelingsengine producten voorstellen in de lijsten **Nieuw**, **Best verkocht** en **Trending**.
- **Op de pagina Productgegevens:** als klanten of winkelmedewerkers een pagina met **productgegevens** bezoeken, worden er extra artikelen voorgesteld die mogelijk ook worden gekocht. Deze artikelen worden weergegeven in de lijst **Anderen vinden dit ook leuk**.
- **Op de pagina Transactie of uitchecken:** de aanbevelingsengine suggereert artikelen op basis van de hele lijst met artikelen in het mandje. Deze artikelen worden weergegeven in de lijst met **Vaak samen gekocht**.

## <a name="recommendation-service"></a>Aanbevelingsservice

Productaanbevelingen gebruiken de machine learning-technologie voor aanbevelingen op de volgende manier:

- Gegevens in de door de aanbevelingsservice vereiste indeling worden opgehaald uit de operationele handelsdatabase en naar de entiteitsopslag gezonden.
- De aanbevelingsservice gebruikt de gegevens voor het trainen van aanbevelingsmodellen voor de lijsten **Anderen vinden dit ook leuk**, **Vaak samen gekocht**, **Nieuw**, **Best verkocht** en **Trending**.

## <a name="additional-resources"></a>Aanvullende resources

[Productaanbevelingen inschakelen](enable-product-recommendations.md)

[Lijst met gecureerde productaanbevelingen maken](create-editorial-recommendation-lists.md)

[Resultaten van productaanbevelingen op basis van AI-ML beheren](modify-product-recommendation-results.md)

[Lijsten met productaanbevelingen toevoegen aan pagina's](add-reco-list-to-page.md)
