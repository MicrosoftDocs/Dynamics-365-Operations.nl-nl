---
title: Siteselectiemodule
description: In dit artikel wordt beschreven wat de siteselectiemodule is en hoe u deze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/04/2022
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
ms.openlocfilehash: efd58206d88618aedb6b574afb47da1e9e578ef1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276743"
---
# <a name="site-picker-module"></a>Siteselectiemodule

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven wat de siteselectiemodule is en hoe u deze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

Wanneer een bedrijf verschillende sites heeft voor verschillende markten, regio's en landen, hebben sitegebruikers een eenvoudige manier nodig om tussen sites te schakelen en hun favoriete winkelsite te selecteren. Voor dit scenario kunnen gebruikers met de siteselectiemodule bladeren door meerdere sites. Een siteverdeler wordt ook aangeraden wanneer [geodetectie en omleiding](geo-detection-redirection.md) zijn geïmplementeerd voor uw e-commercesite, zodat klanten een manier hebben om de sitevoorkeur te overschrijven die ze aangeven via de module voor [land-/regioselectie](country-region-picker-module.md). 

De siteselectiemodule moet worden geconfigureerd met de lijst met sites (markten, regio's of landinstellingen) waarin sitegebruikers kunnen bladeren. In de volgende afbeelding ziet u een voorbeeld van een siteselectiemodule die wordt weergegeven in de koptekst van een sitepagina.

![Voorbeeld van een siteselectiemodule in de koptekst van een sitepagina.](./media/ecommerce-sitepicker.PNG)

## <a name="site-picker-module-properties"></a>Eigenschappen van siteselectiemodule

| Naam van eigenschap. | Waarde                 | Description |
|---------------|-----------------------|-------------|
| Koptekst       | Tekst                  | De koptekst voor de module. |
| Siteopties  | Naam, afbeelding, URL      | Met deze eigenschap worden een naam, een koppeling naar de startpagina van de site en een optionele afbeelding opgegeven voor elke site die in de module is opgenomen. De afbeelding kan een vlag zijn of een bepaalde voorstelling van een markt, regio of landinstelling. |

## <a name="add-a-site-picker-module-to-a-page"></a>Een siteselectiemodule toevoegen aan een pagina

De siteselectiemodule kan in het vak **Siteselectie** van de [koptekstmodule](author-header-module.md) worden toegevoegd. Nadat een siteselectiemodule is toegevoegd, kunt u de modulekop en de siteopties definiëren. Over het algemeen is een koptekstmodule opgenomen in een koptekstfragment dat op e-commercepagina's voor een site kan worden gedeeld. 

Volg deze stappen om een siteselectiemodule toe te voegen aan een koptekstmodule voor uw site.

1. Selecteer in het vak **Siteselectie** van de koptekstmodule van het koptekstfragment het weglatingsteken (**...**) en selecteer vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** een module **Siteselectie** en selecteer vervolgens **OK.**
1. Selecteer **Optielijst voor sites toevoegen** in het eigenschappendeelvenster voor de **Siteselectie**. Er wordt een bewerkbare optie voor **Optielijst voor sites** weergegeven.
1. Selecteer **Optielijst voor sites**. Het dialoogvenster **Optielijst voor sites** wordt weergegeven.
1. Voer onder **Sitemnaam** de tekst van de sitenaam in die wordt weergegeven in de vervolgkeuzelijst voor de siteselectie.
1. Selecteer onder **Site-omleidings-URL** **Een koppeling toevoegen**. Het flyoutdeelvenster **Een koppeling toevoegen** wordt geopend.
1. Selecteer in het flyoutdeelvenster **Een koppeling toevoegen** de optie **Aangepaste pagina** en **Volgende**.
1. Selecteer in de lijst met site-URL's de URL met het pad dat u hebt gemaakt bij het toevoegen van het kanaal aan de site ( bijvoorbeeld `www.adventure-works.com/fr-ca`) en selecteer **Toepassen**.
1. Selecteer **OK**.
1. Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.
1. Selecteer **Publiceren** om de pagina te publiceren.

In het volgende voorbeeld is de siteselectiemodule toegevoegd aan het vak **Siteselectie** van een koptekstmodule die is opgenomen in een koptekstfragment met de naam **HeaderContainer**.

![Voorbeeld van een siteselectiemodule in een koptekstfragment.](./media/ecommerce-sitepicker-2.png)

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Koptekstmodule](author-header-module.md)

[Breadcrumb-module](add-breadcrumb.md)

[Navigatiemenumodule](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
