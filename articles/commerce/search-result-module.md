---
title: Module voor zoekresultaten
description: In dit onderwerp worden modules voor zoekresultaten beschreven en wordt aangegeven hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3761be29955458099d01f2271057884fc1fd6f28
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097173"
---
# <a name="search-results-module"></a>Module voor zoekresultaten

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

In dit onderwerp worden modules voor zoekresultaten beschreven en wordt aangegeven hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

De module voor zoekresultaten retourneert zoekresultaten met producten en een lijst met toepasselijke verfijningen voor de producten. Modules voor zoekresultaten kunnen op Dynamics 365 Commerce-sites worden gebruikt om pagina's weer te geven voor de volgende scenario's:

- Zoekresultaten die worden gestart door een zoekopdracht van een gebruiker
- Zoekresultaten waarmee een specifieke verzameling producten wordt weergegeven, zoals 'Vergelijkbare artikelen'.
- Lijsten met producten die tot een bepaalde categorie behoren

Zie [Overzicht van de standaard landingspagina voor categorieën en pagina met zoekresultaten](category-search-page-overview.md) voor meer informatie over categorie- en zoekresultatenpagina's.

In de volgende afbeelding ziet u een voorbeeld van een zoekresultatenpagna voor een categorie op de site van Fabrikam.

![Voorbeeld van een pagina met zoekresultaten op de Fabrikam-site](./media/SimpleCategoryLandingDressCategory.png)

## <a name="search-results-module-properties"></a>Eigenschappen van modules voor zoekresultaten

In de volgende tabel worden de eigenschappen van modules voor zoekresultaten met hun waarden en omschrijvingen weergegeven.

| Eigenschap | Waarden | Beschrijving |
|----------|--------|-------------|
| Artikelen per pagina | Geheel getal | Het aantal items dat op elke pagina moet worden weergegeven. |
| Terug naar PDP toestaan | **True** of **False** | Als deze eigenschap is ingesteld op **Waar** en een gebruiker een product selecteert op de zoekresultatenpagina, wordt op de breadcrumb-navigatie op de pagina met productgegevens die wordt geopend een koppeling Terug naar resultaten weergegeven. |
| Verfijningen uitvouwen | **Alle**, **1**, **2**, **3** of **4** | Het aantal topverfijningen dat moet worden uitgevouwen wanneer een pagina wordt geladen. Als deze eigenschap bijvoorbeeld is ingesteld op **3**, worden de eerste drie verfijningen op de pagina uitgevouwen. |
| Weergave categoriehiërarchie verbergen | **True** of **False** | Als deze eigenschap is ingesteld op **Waar**, wordt de weergave van categoriehiërarchie op de pagina verborgen. Deze eigenschap moet worden ingesteld op **Waar** als u de [breadcrumb-module](add-breadcrumb.md) gebruikt om de categoriehiërarchie weer te geven.|
| Productkenmerken opnemen in zoekresultaten | **True** of **False** | Als deze eigenschap is ingesteld op **Waar**, worden kenmerken geretourneerd voor de producten in de zoekresultaten. Hoewel deze kenmerken kunnen worden weergegeven op een Commerce-site, is een extensie vereist.|
| Prijzen van aansluiting weergeven | **True** of **False** | Als deze eigenschap is ingesteld op **Waar**, worden aansluitingsprijzen voor producten weergegeven in de zoekresultaten wanneer een aangemelde gebruiker door de pagina bladert. |

> [!IMPORTANT]
> In Dynamics 365 Commerce 10.0.16 en hoger kan de configuratie **Prijzen voor aansluitingen** worden gebruikt om prijzen voor aansluitingen op de pagina weer te geven.

## <a name="supported-modules"></a>Ondersteunde modules

De module voor zoekresultaten ondersteunt de [module voor snelle weergave](quick-view-module.md), waarmee gebruikers productgegevens kunnen bekijken en artikelen aan het winkelwagentje kunnen toevoegen vanuit de zoekresultatenpagina.

## <a name="add-a-search-results-module-to-a-category-page"></a>Een module voor zoekresultaten aan een categoriepagina toevoegen

Voer deze stappen uit om een module voor zoekresultaten aan een categoriepagina toe te voegen.

1. Ga naar **Sjablonen** en selecteer **Nieuw** om een nieuwe sjabloon te maken.
1. Voer in het dialoogvenster **Nieuwe sjabloon** de naam **Zoekresultaten** in en selecteer vervolgens **OK**.
1. Selecteer het weglatingsteken (...) in het vak **Hoofdtekst** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Standaardpagina** en selecteer vervolgens **OK**.
1. Selecteer in het vak **Hoofd** van de module **Standaardpagina** het weglatingsteken (...) en vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Container** en selecteer vervolgens **OK**.
1. Selecteer het weglatingsteken (...) in het vak **Container** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Breadcrumb** en selecteer vervolgens **OK**.
1. Voer in het eigenschappenvenster **Breadcrumb** de waarde **1** in voor **Min. voorvallen**.
1. Selecteer het weglatingsteken (...) in het vak **Container** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Zoekresultaten** en selecteer vervolgens **OK**.
1. Voer in het eigenschappenvenster **Zoekresultaten** de waarde **1** voor **Min. voorvallen** in en stel vervolgens andere vereiste eigenschappen in voor de module voor zoekresultaten. Door deze eigenschappen in de sjabloon in te stellen, zorgt u ervoor dat de aanpassingen voor een specifieke categoriepagina automatisch deze instellingen bevatten.
1. Selecteer **Bewerken voltooien** en **Publiceren** om de sjabloon te publiceren.
1. Ga naar **Pagina's** en selecteer **Nieuw** om een nieuwe pagina te maken.
1. Selecteer in het dialoogvenster **Een sjabloon kiezen** de sjabloon **Zoekresultaten** die u hebt gemaakt, voer **Categoriepagina** voor **Paginanaam** in en selecteer **OK**. Aangezien alle waarden in de sjabloon zijn ingesteld, kan de pagina worden gepubliceerd.
1. Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van de standaard landingspagina voor categorieën en pagina met zoekresultaten](category-search-page-overview.md)

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Module voor snelle weergave](quick-view-module.md)
