---
title: Module voor zoekresultaten
description: In dit onderwerp worden modules voor zoekresultaten beschreven en wordt aangegeven hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: dc4a01e520379a74ca3b21c1d588531412e762be
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647507"
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

## <a name="enable-inventory-awareness-for-the-search-results-module"></a>Inzicht in de voorraad voor de module voor zoekresultaten inschakelen

Klanten verwachten doorgaans dat een e-commercesite tijdens het browsen inzicht biedt in de voorraad, zodat ze kunnen beslissen wat ze moeten doen als een product niet op voorraad is. De module voor zoekresultaten kan worden verbeterd door er voorraadgegevens in op te nemen, zodat de module de volgende mogelijkheden kan bieden:

- Een voorraadbeschikbaarheidslabel weergeven bij de producten.
- Producten die niet op voorraad zijn, verbergen.
- Producten die niet op voorraad zijn, aan het einde van de lijst met zoekresultaten weergeven.
    
Om deze mogelijkheden beschikbaar te maken, moet u de volgende vereiste instellingen configureren in Commerce Headquarters.

### <a name="enable-the-enhanced-e-commerce-product-discovery-to-be-inventory-aware-feature"></a>De functie Uitgebreide productdetectie in e-Commerce voor inzicht in voorraad inschakelen

> [!NOTE]
> De functie **Uitgebreide productdetectie in e-Commerce voor inzicht in voorraad** is beschikbaar vanaf versie 10.0.20 van Commerce.

Als u in Commerce Headquarters de functie **Uitgebreide productdetectie in e-Commerce voor inzicht in voorraad** wilt inschakelen, neemt u deze stappen.

1. Ga naar **Werkruimten \> Functiebeheer**.
1. Ga op zoek naar de functie **Uitgebreide productdetectie in e-Commerce voor inzicht in voorraad** en schakel deze in.

### <a name="configure-the-populate-product-attributes-with-inventory-level-job"></a>De taak Productkenmerken vullen met voorraadniveau configureren

Met de taak **Productkenmerken vullen met voorraadniveau** wordt een nieuw productkenmerk gemaakt om de beschikbaarheid van de voorraad vast te leggen en wordt dat kenmerk ingesteld op de meest recente voorraadniveauwaarde voor elk hoofdproduct. Omdat de voorraadbeschikbaarheid van een product of assortiment dat wordt verkocht, constant verandert, raden we u sterk aan om de taak als batchproces te plannen.

Als u in Commerce Headquarters de taak **Productkenmerken vullen met voorraadniveau** wilt inschakelen, neemt u deze stappen.

1. Ga naar **Retail en Commerce \> IT Retail en Commerce \> Producten en voorraad**.
1. Selecteer **Productkenmerken vullen met voorraadniveau**.
1. Volg deze stappen in het dialoogvenster **Productkenmerken vullen met voorraadniveau**:

    1. Geef onder **Parameters** in het veld **Naam van productkenmerk en -type** een naam op voor het specifieke productkenmerk dat wordt gemaakt om de beschikbaarheid van de voorraad vast te leggen.
    1. Selecteer onder **Parameters** in het veld **Voorraadbeschikbaarheid gebaseerd op** de hoeveelheid waar de berekening van het voorraadniveau op moet worden gebaseerd (bijvoorbeeld **Fysiek beschikbaar**).
    1. Configureer onder **Op de achtergrond uitvoeren** de taak die u wilt uitvoeren op de achtergrond en schakel desgewenst de optie **Batchverwerking** in. 

> [!NOTE]
> Voor een consistente berekening van het voorraadniveau op PDP's en productlijstpagina's op uw e-commercesite moet u ervoor zorgen dat u dezelfde hoeveelheidsoptie selecteert voor zowel de instelling **Voorraadbeschikbaarheid gebaseerd op** in Commerce Headquarters als de instelling **Voorraadniveau gebaseerd op** in Commerce Site Builder. Zie [Voorraadinstellingen toepassen](inventory-settings.md) voor meer informatie over voorraadinstellingen in Site Builder.

### <a name="configure-the-new-product-attribute"></a>Het nieuwe productkenmerk configureren

Nadat de taak **Productkenmerken vullen met voorraadniveau** is uitgevoerd, moet u het pas gemaakte productkenmerk configureren op de e-commercesite waar u inzicht in de voorraad voor de module voor zoekresultaten wilt inschakelen.

Als u het nieuwe productkenmerk wilt configureren in Commerce Headquarters, neemt u de volgende stappen.

1. Ga naar **Retail en Commerce \> Kanaalinstellingen \> Kanaalcategorieën en productkenmerken** en selecteer de e-commercesite.
1. Selecteer en open een gekoppelde kenmerkgroep, voeg het nieuwe productkenmerk hieraan toe en sluit vervolgens de pagina.
1. Selecteer **Metagegevens van kenmerken instellen**, selecteer het zojuist toegevoegde productkenmerk en schakel vervolgens de opties **Kenmerk in kanaal weergeven**, **Ophaalbaar**, **Kan worden verfijnd** en **Kan worden opgezocht** in.

> [!NOTE]
> Voor producten die in de module voor zoekresultaten worden weergegeven, wordt het voorraadniveau ingevoerd op het niveau van het hoofdproduct in plaats van het niveau van de afzonderlijke variant. Er zijn slechts twee mogelijke waarden: 'beschikbaar' en 'niet voorradig'. De werkelijke tekst voor de waarden wordt opgehaald uit de definitie van het [voorraadniveauprofiel](inventory-buffers-levels.md). Een hoofdproduct wordt alleen als 'niet voorradig' beschouwd als alle varianten niet op voorraad zijn. Het voorraadniveau van een variant wordt bepaald op basis van de definitie van het voorraadniveauprofiel van het product. 

Nadat alle voorgaande configuratiestappen zijn voltooid, tonen de verfijningen op de pagina's met zoekresultaten een voorraadfilter en haalt de module voor zoekresultaten achter de schermen voorraadgegevens op. U kunt vervolgens de instelling **Voorraadinstellingen voor productlijstpagina's** configureren in Commerce Site Builder om te bepalen hoe in de module voor zoekresultaten niet voorradige producten worden weergegeven. Zie [Voorraadinstellingen toepassen](inventory-settings.md) voor meer informatie.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van de standaard landingspagina voor categorieën en pagina met zoekresultaten](category-search-page-overview.md)

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Module voor snelle weergave](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
