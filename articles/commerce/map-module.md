---
title: Kaartmodule
description: In dit artikel worden kaartmodules beschreven en hoe u ze configureert in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: d72091baf2f216bfbe33950950f8917c3ba1ba5c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283341"
---
# <a name="map-module"></a>Kaartmodule

[!include [banner](includes/banner.md)]


In dit artikel worden kaartmodules beschreven en hoe u ze configureert in Microsoft Dynamics 365 Commerce.

Een kaartmodule toont de locaties van winkels op een interactieve kaart die wordt gegenereerd met behulp van het [V8-webbesturingselement van Bing Kaarten](/bingmaps/v8-web-control/). Er is een API-sleutel voor Bing Kaarten vereist. Deze moet worden toegevoegd aan de pagina met gedeelde parameters in Commerce Headquarters. Kaartmodules bieden verschillende weergaven, zoals Road, Aerial en Streetside, die gebruikers kunnen selecteren om kaartlocaties weer te geven. Ze maken ook interacties mogelijk, zoals in- en uitzoomen en gebruik van de locatie van de gebruiker.

Een kaartmodule werkt samen met de winkelselectiemodule om de geografische locaties van winkels te bepalen die moeten worden weergegeven op een kaart. Winkelselectie- en kaartmodules communiceren wanneer een gebruiker een winkel selecteert in een van deze modules op een sitepagina. Kaartmodules kunnen worden uitgebreid voor andere scenario's, naast interactie met winkelselectiemodules. Het aanpassen van modules is echter vereist.

> [!NOTE]
> De kaartmodule is beschikbaar in de Dynamics 365 Commerce versie 10.0.13.

De volgende afbeelding toont een voorbeeld van een kaartmodule die wordt gebruikt op winkellocatiepagina.

![Voorbeeld van een winkelselectiemodule.](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a>Module-eigenschappen

| Naam van eigenschap.             | Waarde                 | Beschrijving |
|---------------------------|-----------------------|-------------|
| Koptekst | Tekst | De koptekst voor de module. |
| Punaiseopties: standaardpictogram | Afbeelding | Het punaisesymbool dat moet worden gebruikt voor winkels die op een kaart worden weergegeven. |
| Punaiseopties: pictogram Actief | Afbeelding | Het punaisesymbool dat moet worden gebruikt voor een winkel die op een kaart is geselecteerd. |
| Punaiseopties: standaardpictogramkleur | Tekenreeks | De tekst of hexadecimale waarde voor de kleur van punaisesymbolen op een kaart. |
| Punaiseopties: actieve pictogramkleur | Tekenreeks | De tekst of hexadecimale waarde voor de kleur van geselecteerde punaisesymbolen op een kaart. |
| Index weergeven | **True** of **False** | Als deze eigenschap is ingesteld op **Waar**, wordt voor elk punaisesymbool dat een winkel aangeeft, een index weergegeven. Deze index komt overeen met de index in de lijstweergave die in de winkelselectiemodule wordt weergegeven. |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a>Toegestane toewijzings-URL's toevoegen aan de beleidsrichtlijnen van de inhoudsbeveiliging van een site

Om de kaartmodules te laten communiceren met Bing Kaarten moet u ervoor zorgen dat de volgende toewijzings-URL's zijn toegestaan volgens het inhoudsbeveiligingsbeleid van uw site (CSP). Deze instelling wordt uitgevoerd in Commerce Site Builder door toegestane URL's toe te voegen aan verschillende CSP-instructies voor de site (bijvoorbeeld **img-src**). Zie voor meer informatie [Beveiligingsbeleid voor inhoud](manage-csp.md). 

- Voeg aan de **connect-src**-richtlijn **&#42;.bing.com** toe.
- Voeg aan de **img-src**-richtlijn **&#42;.virtualearth.net** toe.
- Voeg aan de **script-src**-instructie **&#42;.bing.com, &#42;.virtualearth.net** toe.
- Voeg aan de **script style-src**-instructie **&#42;.bing.com** toe.

## <a name="add-a-map-module-to-a-page"></a>Een kaartmodule toevoegen aan een pagina

Zie [Winkelselectiemodule](store-selector.md) voor meer informatie over het configureren van een kaartmodule op een pagina. 
 
## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Module met vakje voor kopen](add-buy-box.md)

[Winkelwagenmodule](add-cart-module.md)

[Winkelselectiemodule](store-selector.md)

[Bing Kaarten voor uw organisatie beheren](./dev-itpro/manage-bing-maps.md)

[V8-webbesturingselement van Bing Kaarten](/bingmaps/v8-web-control/)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
