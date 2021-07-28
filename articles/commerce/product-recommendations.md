---
title: Overzicht productaanbevelingen
description: Dit onderwerp biedt algemene informatie over het productaanbevelingen. Met productaanbevelingen kunnen klanten gemakkelijk en snel producten vinden die ze willen en zelfs producten die ze oorspronkelijk niet willen kopen.
author: Moonma
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fc7d47897d1a332ba1af7305525f9e75bca12afd
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/03/2021
ms.locfileid: "6337498"
---
# <a name="product-recommendations-overview"></a>Overzicht productaanbevelingen

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Commerce kan worden gebruikt om productaanbevelingen weer te geven op de e-commercewebsite en het POS-apparaat (Point of Sale). Productaanbevelingen zijn artikelen waarin een klant mogelijk geïnteresseerd is. De aanbevelingen zijn gebaseerd op de inkooptrends van andere klanten in online en fysieke winkels.

Met productaanbevelingen kunnen klanten gemakkelijk en snel producten vinden die ze willen, terwijl ze een goede bediening ervaren. Door middel van meerverkoop/bijverkoop kunnen klanten extra producten zoeken die ze oorspronkelijk niet wilden kopen. Wanneer aanbevelingen worden gebruikt om productdetectie te verbeteren, kunnen ze meer conversiemogelijkheden creëren, de verkoopopbrengsten verhogen en zelfs de klanttevredenheid en -retentie verbeteren.

In e-Commerce worden productaanbevelingen op grote schaal aangestuurd door machine learning-technologie voor Microsoft-aanbevelingen.

Deze service is een invoegtoepassing voor Dynamics 365 Commerce. Download de meest recente [Microsoft Dynamics 365-licentiehandleiding](https://go.microsoft.com/fwlink/?LinkId=866544) voor meer informatie.


## <a name="recommendation-service"></a>Aanbevelingsservice

De service voor productaanbevelingen maakt op de volgende manier gebruik van technologieën voor kunstmatige intelligentie en machines learning (AI-ML):

- Gegevens in de door de aanbevelingsservice vereiste indeling worden opgehaald uit de operationele handelsdatabase en naar Azure Data Lake Storage of de entiteitsopslag gezonden.
- De aanbevelingsservice gebruikt de opgeslagen gegevens voor het trainen van aanbevelingsmodellen voor de lijsten **Anderen vinden dit ook leuk**, **Vaak samen gekocht**, **Nieuw**, **Best verkocht** en **Trending**.

## <a name="scenarios"></a>Scenario's

Productaanbevelingen zijn beschikbaar voor de volgende scenario's:

- **Op elke winkelpagina voor browsen of landingspagina's in e-commerce:** als klanten of winkelmedewerkers een winkelpagina bezoeken, kan de aanbevelingsengine producten voorstellen in de lijsten **Nieuw**, **Best verkocht** en **Trending**.
- **Op de pagina Productgegevens:** als klanten of winkelmedewerkers een pagina met **productgegevens** bezoeken, worden er extra artikelen voorgesteld die mogelijk ook worden gekocht. Deze artikelen worden weergegeven in de lijst **Anderen vinden dit ook leuk**.
- **Op de pagina Transactie of uitchecken:** de aanbevelingsengine suggereert artikelen op basis van de hele lijst met artikelen in het mandje. Deze artikelen worden weergegeven in de lijst met **Vaak samen gekocht**.
- **Persoonlijke aanbevelingen:** merchandizers kunnen aangemelde klanten een persoonlijke lijst **Selectie voor u** sturen, naast nieuwe functionaliteit waarmee bestaande lijstscenario's kunnen worden gepersonaliseerd op basis van die klant. Zie [Gepersonaliseerde aanbevelingen inschakelen](personalized-recommendations.md) voor meer informatie.

### <a name="types-of-product-recommendations"></a>Typen productaanbevelingen

In de volgende tabel worden verschillende typen automatische productaanbevelingen beschreven die detailhandelaren kunnen implementeren in hun Dynamics 365 Commerce-oplossing via de [productverzamelingsmodule](product-collection-module-overview.md). Detailhandeleren kunnen nu ook gepersonaliseerde resultaten voor een aangemelde gebruiker weergeven als de auteur van de site die optie kiest.

| Productverzamelingsmodule  | Type | Omschrijving |
|----------------------------|------|-------------|
| Nieuw                        | Algoritme | In deze module wordt een lijst met de nieuwste producten weergegeven die recent zijn gesorteerd in afzetkanalen en catalogi. |
| Meest verkocht               | Algoritme | Deze module bevat een lijst met producten die worden gerangschikt op het hoogste verkoopaantal. |
| Trending                   | Algoritme | In deze module wordt een lijst weergegeven met de producten met de hoogste prestaties voor een bepaalde periode, gerangschikt naar omzet.  |
| Vaak samen gekocht | AI-ML | Deze module beveelt een lijst aan met producten die vaak samen met de inhoud van de huidige winkelwagen worden gekocht. |
| Wat mensen ook leuk vinden           | AI-ML | Deze module beveelt producten aan voor een bepaald seedproduct op basis van inkooppatronen van consumenten. |
| Selectie voor u              | AI-ML | Deze module beveelt een persoonlijke lijst met producten aan op basis van inkooppatronen van de aangemelde gebruiker. Voor een gastgebruiker wordt deze lijst samengevouwen. |

## <a name="additional-resources"></a>Aanvullende bronnen

[Azure Data Lake Storage inschakelen in een Dynamics 365 Commerce-omgeving](enable-adls-environment.md)

[Productaanbevelingen inschakelen](enable-product-recommendations.md)

[Gepersonaliseerde aanbevelingen inschakelen](personalized-recommendations.md)

[Afmelden voor gepersonaliseerde aanbevelingen](personalization-gdpr.md)

[Aanbevelingen voor vergelijkbare artikelen inschakelen](shop-similar-looks.md)

[Productaanbevelingen op POS toevoegen](product.md)

[Aanbevelingen toevoegen aan het transactiescherm](add-recommendations-control-pos-screen.md)

[Resultaten van AI-ML-aanbevelingen aanpassen](modify-product-recommendation-results.md)

[Handmatig gecureerde aanbevelingen maken](create-editorial-recommendation-lists.md)

[Aanbevelingen maken met voorbeeldgegevens](product-recommendations-demo-data.md)

[Veelgestelde vragen over productaanbevelingen](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
