---
title: Winkelselectiemodule
description: In dit onderwerp wordt beschreven wat de winkelselectiemodule is en hoe u deze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8efc2345ded52bfaee2d400815795906f326f4fd
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/21/2020
ms.locfileid: "3157335"
---
# <a name="store-selector-module"></a>Winkelselectiemodule

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven wat de winkelselectiemodule is en hoe u deze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Een winkelselectiemodule wordt gebruikt voor het klantscenario Online kopen, ophalen in winkel. Er wordt een lijst weergegeven met winkels waar een product kan worden opgehaald, met de openingstijden en productvoorraad voor elke winkel.

Voor de winkelselectiemodule is de context van een product en een zoeklocatie nodig om winkels te kunnen vinden. Als er geen zoeklocatie is, wordt standaard de locatie van de browser van de klant ingesteld, op voorwaarde dat de klant toestemming geeft. De module bevat een invoervak waarin de klant een locatie (postcode of plaats en provincie) kan invoeren om winkels in de buurt te vinden.

De winkelselectiemodule is geïntegreerd in de API (Application Programming Interface) van Bing Kaarten om de locatie te converteren naar een breedtegraad en een lengtegraad. Er is een API-sleutel voor Bing Kaarten vereist. Deze moet worden toegevoegd aan de pagina Gedeelde Commerce-parameters in Dynamics 365 Commerce.

U kunt de winkelselectiemodule toevoegen aan een koopvakmodule op de pagina met productgegevens om winkels weer te geven waar een product kan worden opgehaald. De winkelselectiemodule kan ook aan een winkelwagenmodule worden toegevoegd. Wanneer de winkelselectiemodule aan een winkelwagenmodule wordt toegevoegd, worden in de winkelselectiemodule opties voor ophalen weergegeven voor elk item in de winkelwagen. Daarnaast kan deze module met aangepaste codering worden toegevoegd aan andere pagina's of modules via extensies en aanpassingen.

Het scenario Online kopen, ophalen in winkel werkt alleen als producten zijn geconfigureerd met de leveringsmethode 'ophalen door klant'. Anders wordt de module niet op de desbetreffende pagina's weergegeven. Zie [Leveringsmethoden instellen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery) voor meer informatie over het configureren van de leveringsmethode.

De volgende afbeelding toont een voorbeeld van een winkelselectiemodule die wordt gebruikt voor een pagina met productgegevens.

![Voorbeeld van een winkelselectiemodule](./media/BOPIS.PNG)

## <a name="store-selector-module-usage-in-e-commerce"></a>Gebruik van winkelselectiemodule in e-Commerce

- Een winkelselectiemodule kan op een pagina met productgegevens worden gebruikt om winkels in de buurt weer te geven waar een product kan worden opgehaald.
- Een winkelselectiemodule kan op een winkelwagenpagina worden gebruikt om winkels in de buurt weer te geven waar een product uit de winkelwagen kan worden opgehaald.

## <a name="store-selector-module-properties"></a>Eigenschappen van winkelselectiemodule

| Naam van eigenschap.             | Waarde                 | Omschrijving |
|---------------------------|-----------------------|-------------|
| Zoekstraal | Nummer | Hiermee definieert u de zoekradius voor winkels in kilometers. Als er geen waarde is opgegeven, wordt de standaardzoekradius van 50 kilometer gebruikt.|
|Servicevoorwaarden | URL    |  De URL naar de servicevoorwaarden die vereist is voor de Bing Kaarten-service. |

## <a name="add-a-store-selector-module-to-a-page"></a>Een winkelselectiemodule toevoegen aan een pagina

Een winkelselectiemodule heeft de context van een product nodig, dus kan alleen worden gebruikt binnen koopvak- en winkelwagenmodules. Winkelselectiemodules functioneren niet buiten deze modules.

- Zie [Module met vakje voor kopen](add-buy-box.md) voor informatie over het toevoegen van een winkelselectiemodule aan een koopvakmodule. 
- Zie [Winkelwagenmodule](add-cart-module.md) voor informatie over het toevoegen van een winkelselectiemodule aan een winkelwagenmodule

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht starterskit](starter-kit-overview.md)

[Module met vakje voor kopen](add-buy-box.md)

[Winkelwagenmodule](add-cart-module.md)

[Snelle rondleiding door de pagina met productgegevens](quick-tour-pdp.md)

[Snelle rondleiding door winkelwagen en kassa](quick-tour-cart-checkout.md)

[Leveringsmethoden instellen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)
