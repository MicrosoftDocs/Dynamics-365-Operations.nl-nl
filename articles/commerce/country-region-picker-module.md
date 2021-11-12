---
title: Module land-/regioselectie
description: Dit onderwerp gaat over de module voor land-/regioselectie en beschrijft hoe u deze configureert in Microsoft Dynamics 365 Commerce.
author: stuharg
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2021-08-12
ms.dyn365.ops.version: Release 10.0.22
ms.openlocfilehash: 35d78cdcc356d35776940147e9b0afee0f0be2a2
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/23/2021
ms.locfileid: "7674718"
---
# <a name="countryregion-picker-module"></a>Module Land-/regioselectie

[!include [banner](includes/banner.md)]

Dit onderwerp gaat over de module voor land-/regioselectie en beschrijft hoe u deze configureert in Microsoft Dynamics 365 Commerce.

De module land-/regioselectie gebruikt de functie [geo-detectie- en omleiding](geo-detection-redirection.md) in Dynamics 365 Commerce om aanbevolen URL's weer te geven aan klanten die een URL voor een e-commercesite aanvragen die niet aan hun land of regio is gekoppeld.

Een klant in Canada vraagt bijvoorbeeld een site-URL aan die niet aan Canada is gekoppeld. In dit geval toont de module land-/regioselectie een dialoogvenster waarin site-URL's worden aanbevolen die aan Canada zijn gekoppeld. De volgende afbeelding toont een voorbeeld van het dialoogvenster land-/regioselectie.

![Voorbeeld van een dialoogvenster voor land-/regioselectie op een startpagina.](./media/Geo_country-region-module-insitu.png)

## <a name="countryregion-picker-module-properties"></a>Eigenschappen module land-/regioselectie

| Naam van eigenschap.              | Waarde       | Beschrijving |
| -------------------------- | ----------- | ----------- |
| Koptekst                    | Tekst        | De kop die boven aan het dialoogvenster wordt weergegeven. |
| Subkop                 | Tekst        | De subkop die onder de kop wordt weergegeven. |
| Land: tekenreeks weergeven    | Tekst        | De weergavenaam voor een URL-optie (bijvoorbeeld 'Canada'). |
| Land: subtekenreeks weergeven | Tekst        | Een optionele weergavesubstring voor een URL-optie (bijvoorbeeld 'Engels' of 'Frans'). |
| Land: afbeelding land     | Media-activa | Een optionele afbeelding die is gekoppeld aan een URL-optie (bijvoorbeeld een afbeelding van de Canadese vlag). |
| Land: URL land       | Tekst        | De URL die overeenkomt met het kanaal en de landinstelling die zijn geconfigureerd voor het land of de regio op de pagina **Kanalen** van Commerce Site Builder (**Site-instellingen \> Kanalen**). Deze URL moet exact overeenkomen met de URL die op de pagina **Kanalen** is geconfigureerd. |
| Actiekoppeling                | Actiekoppeling | Een optionele koppeling die onderaan het dialoogvenster wordt weergegeven. Deze koppeling kan bijvoorbeeld verwijzen naar een interne pagina met een lijst van alle landen en regio's die door de site worden ondersteund. |

## <a name="add-a-countryregion-picker-module-to-a-page"></a>Een module land-/regioselectie toevoegen aan een pagina

De module land-/regioselectie kan rechtstreeks of via een gedeeld fragment aan de koptekstmodule worden toegevoegd. Raadpleeg [Koptekstmodule](author-header-module.md) voor meer informatie over koptekstmodules.

## <a name="configure-the-countryregion-picker-module-in-commerce-site-builder"></a>De module voor land-/regioselectie configureren in Commerce Site Builder

> [!NOTE]
> De URL's die u aan uw klanten aanbeveelt, moeten als landobjecten worden geconfigureerd in de module land-/regioselectie.

Volg deze stappen in Commerce Site Builder voor elke URL die u wilt weergegeven en aan klanten wilt aanbevelen.

1. Selecteer het vak voor de mmodule land-/regioselectie.
1. Selecteer in het deelvenster eigenschappen onder **Landlijst** **Land toevoegen**.
1. Schakel het nieuwe vak **Land** in.
1. Voer in het veld **Tekenreeks weergeven** een weergavenaam op (bijvoorbeeld **Canada**).
1. Optioneel: voer in het veld **Subtekenreeks weergeven** een weergavesubtekenreeks op (bijvoorbeeld **Frans** of **fr-ca**).
1. Optioneel: selecteer een afbeelding in de mediabibliotheek.
1. Voer in het veld **Land-URL** de URL in. Deze URL moet exact overeenkomen met de URL die wordt weergegeven op de pagina **Kanalen** en is aan het kanaal gekoppeld, inclusief de land/regio die aan het land of de regio is gekoppeld.
1. Selecteer **OK**.
1. Herhaal deze stappen voor alle andere land-URL's die u wilt laten zien in de module voor land-/regioselectie.

## <a name="additional-resources"></a>Aanvullende bronnen

[Geodetectie en omleiding instellen](geo-detection-redirection.md)

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Koptekstmodule](author-header-module.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
