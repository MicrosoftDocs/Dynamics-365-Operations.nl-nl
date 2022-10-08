---
title: Productvergelijkingsmodules
description: In dit artikel worden productvergelijkingsmodules beschreven en wordt aangegeven hoe u deze implementeert zodat klanten productvergelijkingen kunnen uitvoeren op Microsoft Dynamics 365 Commerce-e-commercewebsites.
author: ashishmsft
ms.date: 10/03/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 9ff45f3fbcc86b21f336d580582adef586417de4
ms.sourcegitcommit: 66b954827826706ea2ba00c2afd5d694ad92148d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/03/2022
ms.locfileid: "9618380"
---
# <a name="product-comparison-modules"></a>Productvergelijkingsmodules

[!include [banner](../includes/banner.md)]

In dit artikel worden productvergelijkingsmodules beschreven en wordt aangegeven hoe u deze implementeert zodat klanten productvergelijkingen kunnen uitvoeren op Microsoft Dynamics 365 Commerce-e-commercewebsites.

> [!NOTE]
> De modules voor productvergelijking en de productvergelijkingsknop zijn beschikbaar vanaf versie Dynamics 365 Commerce 10.0.29. Ze kunnen worden gebruikt voor B2C- en B2B-websites.

Met de productvergelijkingsfunctionaliteit kunnen klanten productdetails op een productvergelijkingspagina vergelijken om betere inkoopbeslissingen te nemen. Deze functionaliteit wordt geconfigureerd in Commerce Site Builder met behulp van de productvergelijkingsmodule. Op productlijstpagina's, zoals pagina's met categorieresultaten, zoekresultaten en pagina's met productverzamelingen, kunt u een knop voor productvergelijkingen configureren waarmee klanten producten aan een vergelijkingsschaal kunnen toevoegen. Deze functionaliteit wordt in Site Builder geconfigureerd met de knop voor productvergelijkingen, die werkt als de [module voor snelle weergave](quick-view-module.md).

Wanneer sitegebruikers producten ter vergelijking toevoegen door deze te selecteren op producttegels, wordt onder aan de pagina een vergelijkingsschaal weergegeven. Hierin worden de producten weergegeven die de klant momenteel vergelijkt, samen met een kort voorbeeld van de producten. Sitegebruikers kunnen ook producten toevoegen van pagina's met productgegevens en ze kunnen specifieke productvarianten toevoegen om deze te vergelijken met productmodellen.

Wanneer klanten een paar producten aan de vergelijking hebben toegevoegd, kunnen ze **Vergelijken** selecteren om naar een productvergelijkingspagina te worden omgeleid. Deze pagina toont productdetails voor elk geselecteerd product zodat klanten afbeeldingen, prijzen, productdimensies (grootte, stijl en kleur), samengevoegde beoordelingsgegevens en andere productkenmerken kunnen vergelijken.

De onderstaande afbeelding toont voorbeelden van de knop voor het vergelijken van producten, de knop voor het verwijderen uit de vergelijking, de vergelijkingsschaal en de productvergelijkingspagina.

![Het productvergelijkingsoverzicht met de knop voor het vergelijken van producten, de knop voor het verwijderen uit de vergelijking, de vergelijkingsschaal en de productvergelijkingspagina.](./media/Product-Comparison-Overview.png)

> [!NOTE]
> - De pagina voor productvergelijking bevat een vergelijking van een standaardset producteigenschappen en alle kenmerken die op een pagina met productgegevens voor een bepaald product kunnen worden weergegeven.
> - Eigenschappen zoals de leveringsmodus, de voorhanden voorraad en de maateenheid kunnen niet worden weergegeven op een productvergelijkingspagina.
> - Klanten kunnen aan de vergelijkingsschaal producten uit verschillende categorieën toevoegen, mits de producten uit dezelfde catalogus komen.
> - De functie voor productvergelijking is momenteel beperkt tot het vergelijken van producten in een afzonderlijke catalogus. Sitegebruikers kunnen geen vergelijkingen tussen catalogi maken.
> - Zorg ervoor dat de eigenschap **Module weergeven voor klant** is uitgeschakeld voor alle productvergelijkingsmodules.
> - Zorg ervoor dat de caching op paginaniveau is uitgeschakeld voor alle pagina's waarin de productvergelijkingsmodule wordt gebruikt. Deze pagina's omvatten pagina's met productgegevens, productlijstpagina's en productvergelijkingspagina's. Zie [Paginacaching configureren](e-commerce-extensibility/page-caching.md) voor meer informatie.

In de volgende afbeelding ziet u een voorbeeld van een productvergelijkingsprogramma.

![Productvergelijkingspagina.](./media/Product-Comparison-Page.png)

## <a name="add-the-product-comparison-module-to-a-new-product-comparison-page"></a>De productvergelijkingsmodule toevoegen aan een nieuwe productvergelijkingspagina

U kunt een toegewezen productvergelijkingspagina maken door een productvergelijkingsmodule aan de hoofdtekst van een pagina toe te voegen. Behalve dat u klanten in staat stelt om productdetails van verschillende producten te vergelijken, kunt u de productvergelijkingsmodule zo configureren dat klanten snel hun aankoop kunnen voltooien nadat ze producten hebben vergeleken. De productvergelijkingsmodule bevat ook een vak **Lege vergelijking**, waar u een inhoudsblok module kunt toevoegen die de lege status omschrijft (bijvoorbeeld 'Uw productvergelijking is leeg').

Voer de volgende stappen uit om een productvergelijkingsmodule aan een nieuwe productvergelijkingspagina toe te voegen.

1. Ga naar **Pagina's** en selecteer **Nieuw** om een nieuwe pagina te maken.
1. Voer in het dialoogvenster **Een nieuwe pagina maken** onder **Paginanaam** een geschikte paginanaam in (bijvoorbeeld **Productvergelijking**) en selecteer vervolgens **Volgende**.
1. Selecteer onder **Een sjabloon kiezen** de juiste sjabloon (bijvoorbeeld de sjabloon die wordt gebruikt door uw standaardpagina voor categorieën) en selecteer vervolgens **Volgende**.
1. Selecteer onder **Een indeling kiezen** een pagina-indeling (bijvoorbeeld **Flexibele indeling**) en selecteer vervolgens **Volgende**.
1. Controleer de paginaconfiguratie onder **Controle en voltooien**. Selecteer **Terug** als u de pagina-informatie moet bewerken. Als de paginagegevens juist zijn, selecteert u **Pagina maken**.
1. Selecteer in **Hoofdvak** het beletselteken (**...**) en selecteer vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Container** en selecteer vervolgens **OK**.
1. Selecteer het weglatingsteken (**...**) in het vak **Container** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Productvergelijking** en selecteer vervolgens **OK**.
1. Selecteer in het vak **De knop Snelle weergave** de knop met het beletselteken (**...**) en selecteer vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Snelle weergave voor producten** en selecteer vervolgens **OK**.
1. Configureer in het eigenschappenvenster rechts de eigenschappen voor de module **Snelle weergave voor producten**.
1. Selecteer het weglatingsteken (**...**) in het vak **Lege vergelijking** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Inhoudsblok** en selecteer vervolgens **OK**.
1. Configureer de eigenschappen van de module **Inhoudsblok** in het eigenschappenvenster rechts. 
1. Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken.
1. Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.

In de volgende afbeelding ziet u een voorbeeld van een lege vergelijkingspagina in Site Builder.

![Productvergelijkingsmodule.](./media/Product-comparison-module.png)

## <a name="add-a-product-comparison-button-to-product-tiles-on-search-and-category-results-pages"></a>Een knop voor productvergelijking toevoegen aan producttegels op zoek- en categorieresultatenpagina's

Met de knop voor productvergelijking kunnen gebruikers snel een product aan de vergelijking toevoegen wanneer ze door producten bladeren op een lijstpagina. Ze kunnen een of meer producten aan de vergelijkingsschaal van een lijstpagina toevoegen zonder dat ze naar een pagina met productgegevens hoeven te gaan.

De knop voor productvergelijking wordt ondersteund door de modules voor productverzameling, zoekresultaten en koopvakken op pagina's met productgegevens.

Voer de volgende stappen uit om een knop voor productvergelijking toe te voegen aan producttegels op zoek- en categorieresultatenpagina's.

1. Ga in Site Builder naar **Pagina's** en open de categoriepagina waaraan u een knop voor productvergelijking wilt toevoegen.
1. Selecteer in **Hoofdvak** het beletselteken (**...**) en selecteer vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Zoekresultaten** en selecteer vervolgens **OK**.
1. Selecteer in het vak **Knop voor productvergelijking** van de module **Zoekresultaten** het weglatingsteken (**...**) en vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Knop voor productvergelijking** en selecteer vervolgens **OK**.
1. Configureer in het eigenschappenvenster rechts de eigenschappen voor de module **Knop voor productvergelijking**.
1. Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken.
1. Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.

## <a name="add-a-product-comparison-preview-panel-module-to-pages-on-your-website"></a>Een voorbeeldvenstermodule voor productvergelijking toevoegen aan pagina's op uw website

Een voorbeeldvenstermodule voor productvergelijking biedt uw klanten de mogelijkheid producten te controleren die ze toevoegen aan of verwijderen uit de vergelijking. Het voorbeeldvenster bevat ook opties om rechtstreeks naar de vergelijkingspagina te navigeren of de gehele lijst met producten te verwijderen. 

U kunt het beste het voorbeeldvenster inschakelen op alle pagina's waar de knop **Productvergelijking** is ingeschakeld. De module kan als een vak aan de knop **Productvergelijking** worden toegevoegd of kan worden gebruikt als zelfstandige module die u op elke pagina kunt configureren, zelfs als er geen functionaliteit voor het toevoegen of verwijderen van producten is om te vergelijken. 

U moet de voorbeeldvenstermodule voor productvergelijking handmatig toevoegen aan een pagina. U kunt slechts één voorbeeldvenstermodule toevoegen aan een pagina. Als u meerdere exemplaren van de module aan een pagina toevoegt, wordt de eerste module weergegeven en worden de overige exemplaren genegeerd.

![Voorbeeldvenster voor productvergelijking](./media/product-comparison-preview-panel-2.png)

Als u een productvergelijkingslimiet opgeeft, kunt u in het voorbeeldvenster tijdelijke aanduidingen inschakelen waarmee wordt aangegeven hoeveel producten er aan de vergelijking kunnen worden toegevoegd. De grijze tijdelijke aanduidingen worden vervangen door producten wanneer ze aan de vergelijking worden toegevoegd. Als u een productvergelijkingslimiet wilt configureren en tijdelijke aanduidingen wilt inschakelen, gaat u in Site Builder naar **Site-instellingen > Extensions** en brengt u wijzigingen aan in de sectie **Productvergelijkingen**. De configuratie wordt toegepast op alle voorbeeldvensters van alle pagina's. 


## <a name="specify-the-maximum-number-of-products-to-show-in-the-comparison-tray"></a>Opgeven hoeveel producten maximaal kunnen worden weergegeven in de vergelijkingsschaal

U kunt het maximum aantal producten voor vergelijkingen opgeven via **Site-instellingen \> Uitbreidingen** in Site Builder. U kunt afzonderlijke maximumlimieten configureren voor weergaven op het bureaublad en op mobiele apparaten/tablets. Standaard wordt er geen limiet afgedwongen als er geen maximumlimiet is gedefinieerd.

> [!NOTE]
> Voor een optimale browse-ervaring is het raadzaam om het maximum aantal producten in de vergelijking in te stellen op **2** voor de mobiele viewport en **4** voor de viewport voor het bureaublad, zodat u minder horizontaal hoeft te scrollen.

Voer de volgende stappen uit om het maximum aantal producten in de vergelijkingsschaal op te geven.

1. Ga in Site Builder naar **Site-instellingen \> Extensies**.
1. Voer voor de eigenschap **Producten in de vergelijkingslimiet - bureaubladapparaten** het maximum aantal producten in dat moet worden weergegeven in de vergelijkingsschaal voor viewports voor het bureaublad.
1. Voer voor de eigenschap **Producten in de vergelijkingslimiet - mobiele en tabletapparaten** het maximum aantal producten in dat moet worden weergegeven in de vergelijkingsschaal voor viewports voor mobiele apparaten en tablets.
1. Selecteer **Opslaan en publiceren** op de opdrachtbalk.

![Site-instellingen om producten te beperken in de vergelijkingsschaal.](./media/Site-settings-to-limit-products-in-comparison-tray.png)
