---
title: Module land-/regioselectie
description: Dit artikel gaat over de module voor land-/regioselectie en beschrijft hoe u deze configureert in Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 04/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-08-12
ms.dyn365.ops.version: Release 10.0.22
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 203a8e17e075f15b7ae3cceb98d24ced75539a01
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270286"
---
# <a name="countryregion-picker-module"></a>Module land-/regioselectie

[!include [banner](includes/banner.md)]

Dit artikel gaat over de module voor land-/regioselectie en beschrijft hoe u deze configureert in Microsoft Dynamics 365 Commerce.

De module voor land-/regioselectie gebruikt de functie voor [geodetectie en omleiding](geo-detection-redirection.md) in Dynamics 365 Commerce om aanbevolen sites weer te geven voor klanten die een URL voor een e-commercesite aanvragen die niet aan hun land of regio is gekoppeld.

Een klant in Canada vraagt bijvoorbeeld een site-URL aan die aan een ander land dan Canada is gekoppeld. In dit geval toont de module land-/regioselectie een dialoogvenster waarin site-URL's worden aanbevolen die aan Canada zijn gekoppeld. 

## <a name="how-it-works"></a>Hoe het werkt

Wanneer geodetectie en omleiding zijn ingeschakeld voor een site en een klant een site-URL aanvraagt, worden het gedetecteerde land voor de klant en de aangevraagde URL gebruikt om te bepalen of die URL is toegewezen aan het land waar de klant is. De toewijzing tussen URL's en landen wordt gedefinieerd op de pagina **Kanalen** onder **Site-instellingen** in Commerce Site Builder. 

Als de aanvraag-URL niet overeenkomst met een URL die aan het land van de klant is toegewezen, wordt de lijst met een of meer URL's die aan dat land zijn toegewezen, geretourneerd in het antwoord. De module voor land-/regioselectie vergelijkt elke URL in die lijst met de URL's die in de land-/regiomodule zijn geconfigureerd. Voor elke exacte overeenkomst die wordt gevonden, geeft de land-/regiomodule de weergavekop, subkop en afbeelding voor die URL weer en worden hyperlinks voor die elementen gemaakt door middel van de URL.

Wanneer een klant een optie selecteert in de land-/regiomodule, wordt deze naar de hyperlink-URL overgebracht. De URL wordt naar de cookie **\_msdyn365\_\_\_site\_** geschreven zodat deze kan worden gebruikt als de sitevoorkeur van de klant. De volgende keer dat de klant de URL aanvraagt die niet aan zijn land of regio is gekoppeld, wordt hij of zij dan automatisch doorgestuurd naar zijn of haar voorkeursland. Daarom is het raadzaam dat u ook de [siteselectiemodule](site-selector.md) op uw e-commercesite gebruikt, zodat klanten een manier hebben om hun sitevoorkeur te overschrijven of bij te werken. 

Als een klant het dialoogvenster voor de land-/regiomodule sluit, wordt er geen cookie geschreven en blijft de klant op de huidige site. 

De volgende afbeelding toont een voorbeeld van het dialoogvenster land-/regioselectie.

![Voorbeeld van een dialoogvenster voor land-/regioselectie op een startpagina.](./media/Geo_country-region-module-insitu.png)

## <a name="countryregion-picker-module-properties"></a>Eigenschappen module land-/regioselectie

| Naam van eigenschap.              | Waarde       | Beschrijving                                                  |
| -------------------------- | ----------- | ------------------------------------------------------------ |
| Koptekst                    | Tekst        | De kop die boven aan het dialoogvenster wordt weergegeven.       |
| Subkop                 | Tekst        | De subkop die onder de kop wordt weergegeven.               |
| Land: tekenreeks weergeven    | Tekst        | De weergavenaam voor een URL-optie (bijvoorbeeld 'Canada').   |
| Land: subtekenreeks weergeven | Tekst        | Een optionele weergavesubstring voor een URL-optie (bijvoorbeeld 'Engels' of 'Frans'). |
| Land: afbeelding land     | Media-activa | Een optionele afbeelding die is gekoppeld aan een URL-optie (bijvoorbeeld een afbeelding van de Canadese vlag). |
| Land: URL land       | Tekst        | De URL van de site voor het land dat of de regio die wordt geconfigureerd. Deze URL moet exact overeenkomen met de URL die u voor dit land of deze regio hebt opgegeven op de pagina **Kanalen** onder **Site-instellingen** in Commerce Site Builder. Bovendien moet het domein van de URL het aangepaste domein zijn dat is opgegeven in het veld **Domein afstemmen** op de pagina **Kanalen** en niet het werkadres van de site die Commerce biedt wanneer u uw e-commerceomgeving maakt (bijvoorbeeld de URL `https://<yourcompany>.commerce.dynamics.com/`). |
| Actiekoppeling                | Actiekoppeling | Een optionele koppeling die onderaan het dialoogvenster wordt weergegeven. Deze koppeling kan bijvoorbeeld verwijzen naar een interne pagina met een lijst van alle landen en regio's die door de site worden ondersteund. |

## <a name="add-a-countryregion-picker-module-to-a-page"></a>Een module land-/regioselectie toevoegen aan een pagina

De module land-/regioselectie kan rechtstreeks of via een gedeeld fragment aan de koptekstmodule worden toegevoegd. Raadpleeg [Koptekstmodule](author-header-module.md) voor meer informatie over koptekstmodules.

## <a name="configure-the-countryregion-picker-module-in-commerce-site-builder"></a>De module voor land-/regioselectie configureren in Commerce Site Builder

> [!NOTE]
> De URL's die u aan uw klanten aanbeveelt, moeten als landobjecten worden geconfigureerd in de module land-/regioselectie.

Volg deze stappen in Commerce Site Builder voor elke site-URL die u wilt weergegeven en aan klanten wilt aanbevelen.

1. Selecteer het vak voor de mmodule land-/regioselectie.
1. Selecteer in het deelvenster eigenschappen onder **Landlijst** **Land toevoegen**.
1. Schakel het nieuwe vak **Land** in.
1. Voer in het veld **Tekenreeks weergeven** een weergavenaam op (bijvoorbeeld **Canada**).
1. Optioneel: voer in het veld **Subtekenreeks weergeven** een weergavesubtekenreeks op (bijvoorbeeld **Frans** of **fr-ca**).
1. Optioneel: selecteer een afbeelding in de mediabibliotheek.
1. Voer in het veld **Land-URL** de URL in. Deze URL moet exact overeenkomen met de URL die wordt weergegeven op de pagina **Kanalen** en aan het kanaal is gekoppeld, inclusief de land/regio die aan het land of de regio is gekoppeld. 
1. Selecteer **OK**.
1. Herhaal deze stappen voor alle andere land-URL's die u wilt laten zien in de module voor land-/regioselectie.

## <a name="additional-resources"></a>Aanvullende bronnen

[Geodetectie en omleiding instellen](geo-detection-redirection.md)

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Koptekstmodule](author-header-module.md)

[Siteselectiemodule](site-selector.md)

[Breadcrumb-module](add-breadcrumb.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
