---
title: Siteselectiemodule
description: In dit onderwerp wordt beschreven wat de siteselectiemodule is en hoe u deze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/20/2020
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: b69156ee79dbbe8cbb8f5eb5988a751f0488d8e5
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6357733"
---
# <a name="site-selector-module"></a>Siteselectiemodule

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven wat de siteselectiemodule is en hoe u deze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

Wanneer een bedrijf verschillende sites heeft voor verschillende markten, regio's en landen, hebben sitegebruikers een eenvoudige manier nodig om tussen sites te schakelen en hun favoriete winkelsite te selecteren. Voor dit scenario kunnen gebruikers met de siteselectiemodule bladeren door meerdere sites.

De siteselectiemodule moet worden geconfigureerd met de lijst met sites (markten, regio's of landinstellingen) waarin sitegebruikers kunnen bladeren.

> [!NOTE]
> De siteselectiemodule is beschikbaar in Dynamics 365 Commerce versie 10.0.14.

In de volgende afbeelding ziet u een voorbeeld van een siteselectiemodule die wordt weergegeven in de koptekst van een sitepagina.

![Voorbeeld van een siteselectiemodule in de koptekst van een sitepagina.](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a>Eigenschappen van siteselectiemodule

| Naam van eigenschap. | Waarde                 | Beschrijving |
|---------------|-----------------------|-------------|
| Kop       | Tekst                  | De koptekst voor de module. |
| Siteopties  | Naam, afbeelding, URL      | Met deze eigenschap worden een naam, een koppeling naar de startpagina van de site en een optionele afbeelding opgegeven voor elke site die in de module is opgenomen. De afbeelding kan een vlag zijn of een bepaalde voorstelling van een markt, regio of landinstelling. |

## <a name="add-a-site-selector-module-to-a-page"></a>Een siteselectiemodule toevoegen aan een pagina

De siteselectiemodule kan aan de [Koptekstmodule](author-header-module.md) onder de sleuf van de siteselectie worden toegevoegd. Nadat deze is toegevoegd, kunt u de modulekop en de siteopties definiëren.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Koptekstmodule](author-header-module.md)

[Breadcrumb-module](add-breadcrumb.md)

[Navigatiemenumodule](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]