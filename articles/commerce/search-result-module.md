---
title: Module voor zoekresultaten
description: In dit artikel worden modules voor zoekresultaten beschreven en wordt aangegeven hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 08/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: eeb7cd0769fcb866a3d7dcc03e8e87daf24b2c5d
ms.sourcegitcommit: 1d5cebea3e05b6d758cd01225ae7f566e05698d2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/02/2022
ms.locfileid: "9405288"
---
# <a name="search-results-module"></a>Module voor zoekresultaten

[!include [banner](includes/banner.md)]

In dit artikel worden modules voor zoekresultaten beschreven en wordt aangegeven hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

De module voor zoekresultaten retourneert zoekresultaten met producten en een lijst met toepasselijke verfijningen voor de producten. Modules voor zoekresultaten kunnen op Dynamics 365 Commerce-sites worden gebruikt om pagina's weer te geven voor de volgende scenario's:

- Zoekresultaten die worden gestart door een zoekopdracht van een gebruiker
- Zoekresultaten waarmee een specifieke verzameling producten wordt weergegeven, zoals 'Vergelijkbare artikelen'.
- Lijsten met producten die tot een bepaalde categorie behoren

Zie [Overzicht van de standaard landingspagina voor categorieën en pagina met zoekresultaten](category-search-page-overview.md) voor meer informatie over categorie- en zoekresultatenpagina's.

In de volgende afbeelding ziet u een voorbeeld van een zoekresultatenpagna voor een categorie op de site van Fabrikam.

![Voorbeeld van een pagina met zoekresultaten op de Fabrikam-site.](./media/SimpleCategoryLandingDressCategory.png)

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
| Deelvenster voor verfijningen bijwerken | **True** of **False** | Als deze eigenschap is ingesteld op **Waar**, wordt het deelvenster voor verfijningen bijgewerkt wanneer verfijningen worden geselecteerd. In deze modus gedragen sommige verfijningen met meerdere selecties zich als verfijningen met één selectie wanneer het deelvenster voor verfijningen wordt bijgewerkt. |

> [!IMPORTANT]
> In Commerce versie 10.0.16 en hoger kan de configuratie **Prijzen van aansluiting weergeven** worden gebruikt om prijzen voor aansluitingen op de pagina weer te geven.
>
> In Commerce versie 10.0.20 en hoger kan de configuratie **Deelvenster voor verfijningen bijwerken** worden gebruikt om het deelvenster voor verfijningen bij te werken tijdens de selectie van de verfijning.

## <a name="supported-modules"></a>Ondersteunde modules

De module voor zoekresultaten ondersteunt de [module voor snelle weergave](quick-view-module.md), waarmee gebruikers productgegevens kunnen bekijken en artikelen aan het winkelwagentje kunnen toevoegen vanuit de zoekresultatenpagina.

## <a name="add-a-search-results-module-to-a-category-page"></a>Een module voor zoekresultaten aan een categoriepagina toevoegen

Voer de volgende stappen uit om een module voor zoekresultaten toe te voegen aan een categoriepagina in Site Builder.

1. Ga naar **Sjablonen** en selecteer **Nieuw** om een nieuwe sjabloon te maken.
1. Voer in het dialoogvenster **Nieuwe sjabloon** de naam **Zoekresultaten** in en selecteer vervolgens **OK**.
1. Selecteer in het vak **Hoofdtekst** het beletselteken (...) en selecteer vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Standaardpagina** en selecteer vervolgens **OK**.
1. Selecteer in het vak **Hoofd** van de module **Standaardpagina** het beletselteken (...) en selecteer vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Container** en selecteer vervolgens **OK**.
1. Selecteer in het vak **Container** het beletselteken (...) en selecteer vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Breadcrumb** en selecteer vervolgens **OK**.
1. Voer in het eigenschappenvenster **Breadcrumb** de waarde **1** in voor **Min. voorvallen**.
1. Selecteer in het vak **Container** het beletselteken (...) en selecteer vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Zoekresultaten** en selecteer vervolgens **OK**.
1. Voer in het eigenschappenvenster **Zoekresultaten** de waarde **1** voor **Min. voorvallen** in en stel vervolgens andere vereiste eigenschappen in voor de module voor zoekresultaten. Door deze eigenschappen in de sjabloon in te stellen, zorgt u ervoor dat de aanpassingen voor een specifieke categoriepagina automatisch deze instellingen bevatten.
1. Selecteer **Bewerken voltooien** en **Publiceren** om de sjabloon te publiceren.
1. Ga naar **Pagina's** en selecteer **Nieuw** om een nieuwe pagina te maken.
1. Voer in het dialoogvenster **Een nieuwe pagina maken** onder **Paginanaam** **Categoriepagina** in en selecteer vervolgens **Volgende**.
1. Selecteer onder **Een sjabloon kiezen** de sjabloon **Zoekresultaten** die u hebt gemaakt en selecteer vervolgens **Volgende**.
1. Selecteer onder **Een indeling kiezen** een pagina-indeling (bijvoorbeeld **Flexibele indeling**) en selecteer vervolgens **Volgende**.
1. Controleer de paginaconfiguratie onder **Controle en voltooien**. Selecteer **Terug** als u de pagina-informatie wilt bewerken. Als de paginagegevens juist zijn, selecteert u **Pagina maken**.
1. Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.

## <a name="inventory-aware-search-results-module"></a>Module voor zoekresultaten met voorraadinzichten

De module voor zoekresultaten kan worden geconfigureerd om er voorraadgegevens in op te nemen, zodat de module de volgende mogelijkheden kan bieden:

- Labels met voorraadniveau naast de producten weergeven.
- Producten die niet op voorraad zijn, niet tonen in de productlijst.
- Producten die niet op voorraad zijn, onderin de productlijst weergeven.
- Productfilters op basis van voorraad ondersteunen.

Als u deze ervaring wilt inschakelen, moet u eerst de functie **Uitgebreide productdetectie in e-Commerce voor inzicht in voorraad** inschakelen en vervolgens een aantal vereiste instellingen configureren in Commerce headquarters. Zie [Productlijst met voorraadinzicht](inventory-aware-product-listing.md) voor meer informatie.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van de standaard landingspagina voor categorieën en pagina met zoekresultaten](category-search-page-overview.md)

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Module voor snelle weergave](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
