---
title: Siteselectiemodule
description: In dit onderwerp wordt beschreven wat de siteselectiemodule is en hoe u deze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/06/2022
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
ms.openlocfilehash: ad4d4d5f950d0631059d8f509e9e808a9106eb98
ms.sourcegitcommit: 4861ec2d3ae24cc9dd4ad3ac748fd05be3d80c70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/06/2022
ms.locfileid: "8551689"
---
# <a name="site-picker-module"></a>Siteselectiemodule

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven wat de siteselectiemodule is en hoe u deze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

Wanneer een bedrijf verschillende sites heeft voor verschillende markten, regio's en landen, hebben sitegebruikers een eenvoudige manier nodig om tussen sites te schakelen en hun favoriete winkelsite te selecteren. Voor dit scenario kunnen gebruikers met de siteselectiemodule bladeren door meerdere sites. Een siteverdeler wordt ook aangeraden wanneer [geodetectie en omleiding](geo-detection-redirection.md) zijn geïmplementeerd voor uw e-commercesite, zodat klanten een manier hebben om de sitevoorkeur te overschrijven die ze aangeven via de module voor [land-/regioselectie](country-region-picker-module.md). 

De siteselectiemodule moet worden geconfigureerd met de lijst met sites (markten, regio's of landinstellingen) waarin sitegebruikers kunnen bladeren. In de volgende afbeelding ziet u een voorbeeld van een siteselectiemodule die wordt weergegeven in de koptekst van een sitepagina.

![Voorbeeld van een siteselectiemodule in de koptekst van een sitepagina.](./media/ecommerce-sitepicker.PNG)

## <a name="site-picker-module-properties"></a>Eigenschappen van siteselectiemodule

| Naam van eigenschap. | Waarde                 | Description |
|---------------|-----------------------|-------------|
| Koptekst       | Tekst                  | De koptekst voor de module. |
| Siteopties  | Naam, afbeelding, URL      | Met deze eigenschap worden een naam, een koppeling naar de startpagina van de site en een optionele afbeelding opgegeven voor elke site die in de module is opgenomen. De afbeelding kan een vlag zijn of een bepaalde voorstelling van een markt, regio of landinstelling. |

## <a name="add-a-site-picker-module-to-a-page"></a>Een siteselectiemodule toevoegen aan een pagina

De siteselectiemodule kan in het vak **Siteselectie** van de [koptekstmodule](author-header-module.md) worden toegevoegd. Nadat een siteselectiemodule is toegevoegd, kunt u de modulekop en de siteopties definiëren. Over het algemeen is een koptekstmodule opgenomen in een koptekstfragment dat op e-commercepagina's voor een site kan worden gedeeld. In het volgende voorbeeld is de siteselectiemodule toegevoegd aan het vak **Siteselectie** van een koptekstmodule die is opgenomen in een koptekstfragment met de naam **HeaderContainer**.

![Voorbeeld van een siteselectiemodule in een koptekstfragment.](./media/ecommerce-sitepicker-2.png)

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Koptekstmodule](author-header-module.md)

[Breadcrumb-module](add-breadcrumb.md)

[Navigatiemenumodule](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
