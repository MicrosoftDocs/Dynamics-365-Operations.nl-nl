---
title: Kenmerken en kenmerkgroepen beheren
description: In dit artikel wordt beschreven hoe u kenmerken en kenmerkgroepen beheert om producten en hun kenmerken te beschrijven in Microsoft Dynamics 365 Commerce.
author: ashishmsft
ms.date: 08/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.openlocfilehash: aad448ea733aabdff3dc4438dcb682d49e0665c0
ms.sourcegitcommit: 09d4805aea6d148de47c8ca38d8244bbce9786ce
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/31/2022
ms.locfileid: "9386967"
---
# <a name="manage-attributes-and-attribute-groups"></a>Kenmerken en kenmerkgroepen beheren

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u kenmerken en kenmerkgroepen beheert om producten en hun kenmerken te beschrijven in Microsoft Dynamics 365 Commerce.

*Kenmerken* bieden een manier om producten en de bijbehorende kenmerken te beschrijven via door de gebruiker gedefinieerde velden. Voorbeelden zijn geheugengrootte, capaciteit op de vaste schijf en conformiteit met Energy Ster.

Kenmerken kunnen aan verschillende Commerce-entiteiten, zoals productcategorieën en kanalen, worden gekoppeld, en de standaardwaarden kunnen daarvoor worden ingesteld. Wanneer kenmerken worden gekoppeld aan productcategorieën of kanalen, krijgen producten die kenmerken en de bijbehorende standaardwaarden mee. Standaardwaarden van kenmerken kunnen worden overschreven op het afzonderlijke productniveau, op kanaalniveau of in een catalogus.

Een normaal televisieproduct kan bijvoorbeeld de volgende kenmerken hebben.

| Categorie   | Kenmerk           | Toegestane waarden                        | Standaardwaarde |
|------------|---------------------|-------------------------------------------|---------------|
| Tv en Video | Merk               | Een geldige merkwaarde                     | Geen          |
| TV         | Schermgrootte         | 20–85 inch                              | 55 inch     |
|            | Verticale resolutie | 4K (2160p), Full HD (1080p) of HD (720p) | 4K (2160p)    |
|            | Schermvernieuwingsfrequentie | 60hz, 120hz of 240hz                     | 60hz          |
|            | HDMI-ingang         | 0–10                                      | 3             |

## <a name="attributes-and-attribute-types"></a>Kenmerken en kenmerktypen

Kenmerken zijn gebaseerd op *kenmerktypen*. Een kenmerktype geeft het gegevenstype aan dat kan worden ingevoerd voor een specifiek kenmerk. De volgende kenmerktypen worden ondersteund in Commerce:

- **Valuta** - Dit kenmerktype ondersteunt een valutawaarde. Het kan begrensd zijn (oftewel kan het een waardebereik ondersteunen), of kan worden opengelaten.
- **DateTime** - Dit kenmerktype ondersteunt een datum- en tijdwaarde. Dit kan worden begrensd of open blijven.
- **Decimaal** - Dit kenmerktype ondersteunt een numerieke waarde die decimalen bevat. Het kan ook een maateenheid ondersteunen. Dit kan worden begrensd of open blijven.
- **Heel getal** - Dit kenmerktype ondersteunt een numerieke waarde. Het kan ook een maateenheid ondersteunen. Dit kan worden begrensd of open blijven.
- **Tekst** - Dit kenmerktype ondersteunt een tekstwaarde. Bovendien wordt een vooraf gedefinieerde set mogelijke waarden ondersteund wanneer de instelling **Vaste lijst** is ingeschakeld.
- **Booleaans** - Dit type kenmerk ondersteunt een binaire waarde (**waar** of **onwaar**).
- **Verwijzing** - Dit type verwijst naar de andere kenmerken.

> [!NOTE]
> Vanwege [beperkingen van de Azure-zoekindex](/rest/api/searchservice/data-type-map-for-indexers-in-azure-search) wordt het kenmerktype **Decimaal** niet ondersteund voor zoekervaringen in de cloud. Azure Cognitive Search ondersteunt geen conversie van kenmerken van het type **Decimaal** naar doelindexvelden van het type **Edm.Double**, omdat de precisie hieronder zou verminderen.

### <a name="set-up-attribute-types"></a>Kenmerktypen instellen

Volg de stappen in deze voorbeeldprocedure om typen kenmerken in te stellen.

1. Meld u aan bij Commerce headquarters als merchandising manager.
1. Ga naar **Productgegevensbeheer \> Instellen \> Categorieën en kenmerken \> Kenmerktypen**.
1. Selecteer **Nieuw** in het actievenster.
1. Voer in het veld **Naam kenmerktype** de tekst **Type tas** in.
1. Selecteer in het veld **Type** **Tekst**.
1. Stel de optie **Vaste lijst** in op **Ja**.
1. Selecteer op het sneltabblad **Waarden** de optie **Toevoegen**.
1. Voer op de nieuwe regel in het veld **Waarde** de tekst **Boekentas** in.
1. Voeg nog vijf rijen toe. Voer in het veld **Waarde** van elk item een andere waarde in: **Clutch**, **Handtas**, **Rugzak**, **Schoudertas** of **Portefeuille**.
1. Selecteer **Opslaan** in het actievenster.
1. Selecteer **Nieuw** in het actievenster.
1. Voer in het veld **Naam kenmerktype** de tekst **Merk zonnebril** in.
1. Selecteer in het veld **Type** **Tekst**.
1. Stel de optie **Vaste lijst** in op **Ja**.
1. Selecteer op het sneltabblad **Waarden** de optie **Toevoegen**.
1. Voer op de nieuwe regel in het veld **Waarde** de tekst **Ray ban** in.
1. Voeg nog twee rijen toe. Voer in het veld **Waarde** van elk item een andere waarde in: **Aviator** of **Oakley**.
1. Selecteer **Opslaan** in het actievenster.

![Pagina Kenmerktypen.](media/AttributeType_2022Series.png)

### <a name="set-up-an-attribute"></a>Een kenmerk instellen

Volg de stappen in deze voorbeeldprocedure om een kenmerk in te stellen.

1. Meld u aan bij Commerce headquarters als merchandising manager.
1. Ga naar **Productgegevensbeheer \> Instellen \> Categorieën en kenmerken \> Kenmerken**.
1. Selecteer **Nieuw** in het actievenster.
1. Voer in het veld **Naam** **Type tas** in.
1. Selecteer in het veld **Kenmerktype** de optie **Type tas**.
1. Selecteer **Opslaan** in het actievenster.

![Pagina Kenmerken.](media/Attribute_2022Series.png)

## <a name="attribute-metadata"></a>Kenmerkmetagegevens

Bij *Metagegevens van het kenmerk* kunt u opties selecteren om op te geven hoe de kenmerken voor elk product moeten werken. U kunt bijvoorbeeld aangeven of kenmerken vereist zijn, kunnen worden gebruikt voor zoekopdrachten en kunnen worden gebruikt als filter in de online winkel.

Voor producten kunnen de instellingen van kenmerkmetagegevens worden overschreven op kanaalniveau.

De pagina **Kenmerken** van een kenmerk bevat verschillende opties die betrekking hebben op metagegevens. Als u bijvoorbeeld de optie **Kan worden verfijnd** instelt op **Ja** onder **Kenmerkmetagegevens voor handelskanalen**, wordt het kenmerk weergegeven voor verfijning of filteren van producten in zoekresultaten en op pagina's voor bladeren door categorieën. Als u een categorie wilt configureren als verfijnbaar, selecteert u eerst **Filterinstellingen** in het Actievenster en bevestigt u de filterinstellingen voor het kenmerk.

## <a name="filter-settings-for-attributes"></a>Filterinstellingen voor kenmerken

Met filterinstellingen voor kenmerken kunt u opgeven hoe de kenmerkfilters worden weergegeven in het verkooppunt (POS). Voor toegang tot de filterinstellingen voor een kenmerk op de pagina **Kenmerken** van het kenmerk, selecteert u **Filterinstellingen** in het Actievenster.

De pagina **Filterinstellingen** bevat de volgende velden:

- **Naam** - dit veld is standaard ingesteld op de naam van het kenmerk. U kunt de waarde echter wijzigen.
- **Weergaveoptie** - De volgende opties zijn beschikbaar:

    - **Eén waarde** - Deze optie is beschikbaar voor de volgende kenmerktypen: **Boolean**, **valuta**, **decimaal**, **geheel getal** en **tekst**. Hiermee kan slechts een enkele waarde worden geselecteerd voor verfijners op productlijst-pagina's, zoals pagina's voor bladeren door categorieën en pagina's voor zoekresultaten van producten.
    - **Meerdere waarden** - Deze optie is beschikbaar voor de volgende kenmerktypen: **valuta**, **decimaal**, **geheel getal** en **tekst**. Hiermee kunnen meerdere waarden voor het kenmerk worden geselecteerd in de client, voor verfijning.

- **Weergaveregeling** - De volgende opties zijn beschikbaar:

    - **Lijst**: deze optie is beschikbaar voor alle kenmerktypen.
    - **Bereik** - Deze optie is beschikbaar voor de volgende kenmerktypen: **Valuta**, **Decimaal** en **Geheel getal**.
    - **Schuifregelaar** - Deze optie is beschikbaar voor de volgende kenmerktypen: **Valuta**, **Decimaal** en **Geheel getal**.
    - **Schuifregelaar met staven** - Deze optie is beschikbaar voor de volgende kenmerktypen: **Valuta**, **Decimaal** en **Geheel getal**.

- **Drempelwaarde** - Deze instelling is vereist als u **Bereik** hebt geselecteerd als het type weergaveregeling. U kunt waarden definiëren met behulp van een puntkomma (;) als scheidingsteken.

    Voor een kenmerk **Tasvolume** dat bijvoorbeeld als kenmerktype **Geheel getal** heeft, kan de drempelwaarde bijvoorbeeld **10; 20; 50; 100; 200; 500; 1000; 5000** zijn. In dit geval toont het POS het volgende bereik. Bereiken die geen producten in de resultatenset hebben, worden grijs weergegeven.

    - Minder dan 10
    - 10 – 20
    - 20 – 50
    - 50 – 100
    - 100 – 200
    - 200 – 500
    - 500 of meer

Filterinstellingen voor kenmerken zijn alleen van toepassing op productkenmerken en kunnen worden gebruikt om de zoekresultaten voor producten en categorieën te verfijnen. Ze zijn niet van toepassing op klanten of bestellingen zoeken, hoewel dezelfde kenmerken kunnen worden gebruikt om klant- of bestelgegevens te verrijken.

In de standaardmodules van Commerce is er geen directe ondersteuning beschikbaar voor filterinstellingen voor **Weergaveregeling**, zoals **Bereik**, **Schuifregelaar** en **Schuifregelaar met staven**. De instellingen **Bereik** en **Schuifregelaar** worden ondersteund voor POS-oplossingen, terwijl de instelling **Schuifregelaar met staven** van toepassing is voor verouderde SharePoint online winkels; deze blijft beschikbaar voor integratie van derden en aangepaste scenario's.

Wij adviseren verfijnbare kenmerken een kenmerk van het type **Tekst** te geven, waarbij de optie **Vaste lijst** is ingeschakeld, en de lijst beheersbaar te houden (maximaal 100-200 unieke waarden). Als een verfijner 1000 of meer unieke waarden krijgt, is het beter een kenmerk van het type **Tekst** te gebruiken, waarbij de optie **Vaste lijst** is uitgeschakeld.

Vertalingen zijn cruciaal voor de naam en de waarden van kenmerken. Voor kenmerken van het type **Tekst**, waarbij de optie **Vaste lijst** is ingeschakeld, kunt u onder **Kenmerktype** vertalingen voor de kenmerkwaarden definiëren. Voor elk ander type kenmerk kunt u vertalingen definiëren op de pagina waar u de kenmerkwaarden definieert. Voor een kenmerk van het type **Tekst** kunt u bijvoorbeeld vertalingen voor de standaardwaarde definiëren op de pagina **Kenmerken** van het kenmerk. Als u echter de standaardwaarde op productniveau overschrijft, kunt u vertalingen voor het kenmerk definiëren op de pagina **Productkenmerken** van het product.

Wanneer een kenmerk is gemarkeerd als verfijnbaar voor een kanaal, werkt u het kenmerktype niet bij. Anders beïnvloedt u de publicatie van productgegevens in de zoekindex. In plaats daarvan is het raadzaam een nieuw kenmerk te maken voor een nieuw type verfijner en het vorige kenmerk buiten gebruik te stellen door dit te verwijderen uit andere kenmerkgroepen.

Zoeken op kenmerken wordt ondersteund, maar het resultaat wordt alleen opgehaald voor een exacte match van zoekwoorden. Een kenmerk **Stof** heeft bijvoorbeeld de waarde **Kasjmier/katoen**. Als een klant naar 'Kat' zoekt, worden er geen producten opgehaald met **Kasjmier/katoen** als de stof. Als een klant echter naar 'Kasjmier' , 'Katoen' of 'Kasjmier katoen' zoekt, worden er wel producten opgehaald met **Kasjmier/katoen** als de stof.

### <a name="additional-attribute-metadata-options"></a>Aanvullende opties voor metagegevens voor kenmerken

> [!NOTE]
> Deze opties voor metagegevens van kenmerken zijn alleen van toepassing op verouderde SharePoint online winkels en externe integraties. Zie [Overzicht van het zoekschema in SharePoint Server 2013](/SharePoint/search/search-schema-overview) voor meer informatie over deze opties voor metagegevens van kenmerken.

De volgende aanvullende opties voor metagegevens van kenmerken zijn ook beschikbaar op de pagina **Kenmerken**:

- Zoekbaar
- Ophaalbaar
- Kan worden opgezocht
- Sorteerbaar
- Hoofdlettergebruik en indeling negeren
- Volledige overeenkomst

Deze opties waren oorspronkelijk bedoeld voor het verbeteren van de zoekfunctie voor verouderde SharePoint online winkels. Deze zijn niet noodzakelijkerwijs van toepassing op e-commercewebsites van Commerce of POS-terminals. Omdat headless integratie nog steeds wordt ondersteund, zijn deze opties beschikbaar voor het exporteren van metagegevens van kenmerken met behulp van de Commerce software development kit (SDK). U kunt de Commerce SDK gebruiken om producten in een aangepaste, geoptimaliseerde externe zoekindex te zetten. Op deze manier zorgt u ervoor dat alleen kenmerken die moeten worden geïndexeerd, worden geïndexeerd.

## <a name="attribute-groups"></a>Kenmerkgroepen

Een *kenmerkgroep* wordt gebruikt om de afzonderlijke kenmerken van een onderdeel of subonderdeel in een productconfiguratiemodel te groeperen. U kunt een kenmerk opnemen in een of meer kenmerkgroepen. Met kenmerkgroepen kunnen gebruikers producten configureren omdat de verschillende selecties zijn gerangschikt in een specifieke context. U kunt kenmerkgroepen toewijzen aan categorieën of kanalen. U kunt ook standaardwaarden instellen voor kenmerken in een kenmerkgroep.

![Pagina Kenmerkgroepen.](media/AttributeGroup_2022Series.png)

### <a name="create-an-attribute-group"></a>Een kenmerkgroep maken

Volg de stappen in deze voorbeeldprocedure om een kenmerkgroep te maken.

1. Meld u aan bij Commerce headquarters als merchandising manager.
1. Ga naar **Productgegevensbeheer \> Instellen \> Categorieën en kenmerken \> Kenmerkgroepen**.
1. Maak een kenmerkgroep met de naam **Overhemden**.
1. Voeg de volgende kenmerken toe: **Reinigingsmethode**, **Kraagtype**, **Collectie** en **Ontwerp**.

> [!NOTE]
> De waarden voor de weergavevolgorde van kenmerken in de kenmerkgroep zijn niet van invloed op de volgorde van de verfijners in de resultaten van zoekopdrachten en bladeren door categorieën. Deze zijn alleen van toepassing op het scenario 'orderkenmerken'.

### <a name="assign-attribute-groups-to-categories"></a>Kenmerkgroepen toewijzen aan categorieën

Een of meer kenmerkgroepen kunnen worden gekoppeld aan categorieknooppunten in de volgende typen categoriehiërarchieën:

- Handelproducthiërarchie
- Hiërarchie van de kanaalnavigatiecategorieën
- Hiërarchie aanvullende productcategorieën

Wanneer producten worden gecategoriseerd in categorieën die aan kenmerkgroepen zijn gekoppeld, nemen ze de kenmerken over die in die kenmerkgroepen zijn opgenomen.

![Het sneltabblad Productkenmerkgroepen op de producthiërarchiepagina van Commerce.](media/AGRetailProdHierarchy_2022Series.png)

Om kenmerkgroepen toe te wijzen aan categorieën in de Commerce-producthiërarchie, volgt u de stappen in deze voorbeeldprocedure.

1. Meld u aan bij Commerce headquarters als merchandising manager.
1. Ga naar **Retail en Commerce \> Producten en categorieën \> Commerce-producthiërarchie**.
1. Selecteer de navigatiehiërarchie **Mode**.
1. Selecteer onder **Herenmode** de categorie **Broek**, klik op het sneltabblad **Productkenmerkgroepen** en voeg een kenmerkgroep toe met de naam **Herenriem**.
1. Selecteer de categorie **Modieuze zonnebril** en controleer de nieuwe kenmerken in de kenmerkgroep **Modieuze zonnebril** door **Kenmerken weergeven** te selecteren. De kenmerkgroep zou nu de nieuwe kenmerken **Vorm lens** en **Merk zonnebril** moeten weergeven.
1. Selecteer de categorie **Broek** en controleer de kenmerken voor de kenmerkgroep **Herenriem** door **Kenmerken weergeven** te selecteren. De kenmerkgroep zou **Merk herenriem**, **Stof riem** en **Maat riem** moeten weergeven.

Dezelfde standaard procedure kan ook worden gebruikt om kenmerkgroepen toe te wijzen aan categorieën in de hiërarchie van kanaalnavigatiecategorieën en de aanvullende productcategoriehiërarchie. Gebruik echter in stap 2 een van de volgende paden, afhankelijk van de hiërarchie die u aan kenmerkgroepen wilt toewijzen:

- **Hiërarchie van categorieën voor afzetkanaalnavigatie:** Ga naar **Retail en handel \> Categorie- en productbeheer \> Categorieën voor afzetkanaalnavigatie**.
- **Hiërarchie van aanvullende productcategorieën:** Ga naar **Retail en handel \> Categorie- en productbeheer \> Aanvullende productcategorieën**.

> [!NOTE]
> Zorg ervoor dat u alleen kenmerkgroepen koppelt in een categoriehiërarchie op het sneltabblad **Productkenmerkgroepen**, niet op het sneltabblad **Waarden van categoriekenmerk**. Als kenmerken worden weergegeven op het sneltabblad **Waarden van categoriekenmerk**, selecteert u **Categoriehiërarchie bewerken** in het actievenster. Selecteer vervolgens de categorieknooppunten op het sneltabblad **Categoriekenmerkgroepen** en selecteer **Verwijderen**. Het ophalen van kenmerken per categorie via de Commerce Scale Unit wordt niet ondersteund.

## <a name="identify-viewable-and-refinable-attributes-for-commerce-channels-for-the-default-product-collection"></a>Weergeefbare en verfijnbare kenmerken identificeren voor Commerce-kanalen voor de standaard productcollectie

Wanneer u verschillende kenmerkgroepen aan categorieën in verschillende hiërarchieën (Commerce producthiërarchie of kanaalnavigatiecategorieën) en gedefinieerde kenmerkwaarden voor elk product hebt gekoppeld op basis van de categoriekoppeling, moet u de markering **Kenmerk in kanaal weergeven** inschakelen om deze kenmerken weergeefbaar te maken in een specifiek kanaal.

1. Ga naar **Retail en Commerce \> Kanaalinstellingen \> Kanaalcategorieën en productkenmerken**.
1. Selecteer **Metagegevens van kenmerken instellen** en selecteer daarna een kenmerk in het linkernavigatiedeelvenster.
1. Stel op het sneltabblad **Afzetkanaalproductkenmerken** (niet het sneltabblad **Categoriekenmerken**), de optie **Kenmerk weergeven in kanaal** op **Ja** om het kenmerk weergeefbaar te maken.
1. Als u het kenmerk ook verfijnbaar wilt maken, stelt u de optie **Kan worden verfijnd** in op **Ja**.

### <a name="control-visibility-of-dimension-based-refiners-such-as-size-style-and-color"></a>De zichtbaarheid regelen van op dimensie gebaseerde verfijners zoals maat, stijl en kleur

Productdimensies, zoals grootte, stijl en kleur, zijn de meest gebruikte verfijners. Om deze productdimensies beschikbaar te maken als verfijners, moet u op kanaalniveau een kenmerkgroep koppelen die een verwijzing bevat naar een kenmerktype dat automatisch waarden overneemt van productdimensiewaarden.

U kunt aangeven dat productdimensies zichtbaar en verfijnbaar zijn door markeringen bij te werken op de pagina **Afzetkanaalcategorieën en productkenmerken**. Selecteer het hoofdknooppunt in het navigatiedeelvenster en stel op het sneltabblad **Afzetkanaalproductkenmerken** de optie **Kenmerk weergeven in kanaal** in op **Ja** voor de kenmerken **Maat**, **Stijl** en **Kleur**. Als u deze kenmerken ook verfijnbaar wilt maken, stelt u de optie **Kan worden verfijnd** voor elk kenmerk in op **Ja**.

![Metagegevens van kenmerken instellen voor dimensieverfijners.](./media/ProductDimensionRefinersMetadataSetup_2022Series.png)

Volg de stappen in deze voorbeeldprocedure om de kenmerken zo in te stellen dat deze beschikbaar zijn in het op demonstratiegegevens gebaseerde kanaal.

1. Ga naar **Retail en Commerce \> Kanaalinstellingen \> Kanaalcategorieën en productkenmerken**.
1. Selecteer het kanaal **Houston**.
1. Selecteer in het actievenster **Metagegevens van kenmerken instellen**.
1. Selecteer het categorieknooppunt **Mode** en selecteer vervolgens op het sneltabblad **Afzetkanaalproductkenmerken** **Kenmerk opnemen** voor elk kenmerk.
1. Selecteer het categorieknooppunt **Mode-accessoires**, selecteer de categorie **Modieuze zonnebril** en selecteer vervolgens op het sneltabblad **Afzetkanaalproductkenmerken** **Kenmerk opnemen** voor elk kenmerk.
1. Selecteer het categorieknooppunt **Mannenmode**, selecteer de categorie **Broek** en selecteer vervolgens op het sneltabblad **Afzetkanaalproductkenmerken** **Kenmerk opnemen** voor elk kenmerk.
1. Nadat u de metagegevens van kenmerken voor uw bedoelde kenmerken en verfijners hebt bijgewerkt, moet u ervoor zorgen dat u de wijzigingen opslaat en de taak **Afzetkanaalupdates publiceren** uitvoert. Nadat de updates zijn gepubliceerd, moet u vervolgens de volgende taken uitvoeren: **1070** (**Kanaalconfiguratie**), **1040** (**Producten**) en **1150** (**Catalogus**).

> [!NOTE]
> - Als uw bedrijf vereist dat u vaak producten in de navigatiehiërarchie toevoegt of verwijdert, of dat u wijzigingen aanbrengt zoals het bijwerken van waarden voor de weergavevolgorde, het toevoegen van nieuwe categorieën en het toevoegen van nieuwe kenmerkgroepen aan categorieën, dan raden wij u aan de taak **Kanaalupdates publiceren** te configureren om als een frequente batch-taak uit te voeren. U kunt ook handmatig de taak **Kanaalupdates publiceren** activeren, en dan de volgende Commerce Data Exchange (CDX)-taken: **1070** (**Kanaalconfiguratie**), **1040** (**Producten**) en **1150** (**Catalogus**).
> - Selecteer de optie dat dit kanaal de kenmerkgroepen van het bovenliggende kanaal in de hiërarchie moet **Overnemen**. Als u de optie **Overnemen** op **Ja** instelt, neemt het onderliggende kanaalknooppunt alle kenmerkgroepen en kenmerken van deze kenmerkgroepen over.
> - Als de knop **Metagegevens voor kenmerken instellen** in het actievenster niet beschikbaar is, controleert u of de **Navigatiehiërarchie** aan uw kanaal is gekoppeld op het sneltabblad **Algemeen**.
> - U mag geen kenmerkgroepen koppelen, behalve op dimensie gebaseerde kenmerkgroepen op kanaalniveau (bijvoorbeeld onder **Kenmerkgroepen** op de pagina **Afzetkanaalcategorieën en productkenmerken**).
> - Na de invoering van ondersteuning voor klantspecifieke business-to-business-catalogi (B2B) in Commerce versie 10.0.27, wordt van u verwacht dat u de instellingen voor verfijners en kenmerken voor elke B2B-catalogus identificeert op dezelfde manier als in dit artikel wordt beschreven.

## <a name="override-attribute-values"></a>Kenmerkwaarden overschrijven

De standaardwaarden van kenmerken kunnen voor afzonderlijke producten worden overschreven op het productniveau. Ze kunnen ook worden overschreven voor afzonderlijke producten in specifieke catalogi die gericht zijn op specifieke kanalen.

### <a name="override-the-attribute-values-of-an-individual-product"></a>De waarden van kenmerken van een afzonderlijk product overschrijven

Volg de stappen in deze voorbeeldprocedure om de kenmerkwaarden van een afzonderlijk product te overschrijven.

1. Meld u aan bij Commerce headquarters als merchandising manager.
1. Ga naar **Retail en handel \> Categorie- en productbeheer \> Vrijgegeven producten per categorie**.
1. Selecteer **Mode \> Mode-accessoires \> Modieuze zonnebril**.
1. Selecteer het vereiste product in het raster. Selecteer vervolgens in het Actievenster het tabblad **Product** in de groep **Instellen** en selecteer **Productkenmerken**.
1. Selecteer een kenmerk in het linkerdeelvenster en werk vervolgens de waarde bij in het rechterdeelvenster.

![Pagina productkenmerkwaarden.](media/ProdDetailsProdAttrValues_2022Series.png)

### <a name="override-the-attribute-values-of-all-products-in-a-catalog"></a>De kenmerkwaarden van alle producten in een catalogus overschrijven

Volg de stappen in deze voorbeeldprocedure om de kenmerkwaarden van alle producten in een catalogus te overschrijven.

1. Meld u aan bij Commerce headquarters als merchandising manager.
1. Ga naar **Retail en handel \> Catalogusbeheer \> Alle catalogi**.
1. Selecteer de catalogus **Fabrikam Base Catalog**.
1. Selecteer **Mode \> Mode-accessoires \> Modieuze zonnebril**.
1. Selecteer op het sneltabblad **Producten** het vereiste product en selecteer vervolgens **Kenmerken** boven het productraster.
1. Werk de waarden van de vereiste kenmerken bij op de volgende sneltabbladen:

    - Gedeelde productmedia
    - Gedeelde productkenmerken
    - Afzetkanaalmedia
    - Afzetkanaalproductkenmerken

### <a name="override-the-attribute-values-of-all-products-in-a-channel"></a>De waarden van kenmerken van alle producten in een kanaal overschrijven

Volg de stappen in deze voorbeeldprocedure om de kenmerkwaarden van alle producten in een kanaal te overschrijven.

1. Meld u aan bij Commerce headquarters als merchandising manager.
1. Ga naar **Retail en Commerce \> Kanaalinstellingen \> Kanaalcategorieën en productkenmerken**.
1. Selecteer het kanaal **Houston**.
1. Selecteer op het sneltabblad **Producten** het vereiste product en selecteer vervolgens **Kenmerken** boven het productraster.
1. Als geen producten beschikbaar zijn, selecteert u **Toevoegen** op het sneltabblad **Producten** en selecteert u de vereiste producten in het dialoogvenster **Producten toevoegen**.
1. Werk de waarden van de vereiste kenmerken bij op de volgende sneltabbladen:

    - Gedeelde productmedia
    - Gedeelde productkenmerken
    - Afzetkanaalmedia
    - Afzetkanaalproductkenmerken

### <a name="define-variant-specific-attribute-values-and-define-multiple-values-for-product-attributes"></a>Variantspecifieke kenmerkwaarden definiëren en meerdere waarden voor productkenmerken bepalen

Volg de stappen in deze voorbeeldprocedure om variantspecifieke kenmerkwaarden te definiëren en meerdere waarden voor productkenmerken te definiëren.

1. Meld u aan bij Commerce headquarters als merchandising manager.
1. Ga naar **Retail en Commerce \> Kanaalinstellingen \> Kanaalcategorieën en productkenmerken**.
1. Selecteer het kanaal **Houston**.
1. Selecteer op het sneltabblad **Producten** de vereiste productvariant en selecteer vervolgens **Kenmerken** boven het productraster.
1. Als geen producten beschikbaar zijn, selecteert u **Toevoegen** op het sneltabblad **Producten** en selecteert u de vereiste productvarianten in het dialoogvenster **Producten toevoegen**.
1. Werk de waarden van de vereiste kenmerken bij op de volgende sneltabbladen:

    - Gedeelde productmedia
    - Gedeelde productkenmerken
    - Afzetkanaalmedia
    - Afzetkanaalproductkenmerken

#### <a name="example-of-variant-specific-attribute-configuration"></a>Voorbeeld van variantspecifieke kenmerkconfiguratie
        
In dit voorbeeld is het product **P001-Master** een activiteit met meerdere activiteiten met drie varianten: **Hardlopen**, **Wandelen** en **Trekking**. Voor elke variant wilt u de waarde van het kenmerk **Activiteit** uniek definiëren. Op het sneltabblad **Producten** van de pagina **Afzetkanaalcategorieën en productkenmerken** voor uw kanaal definieert u de kenmerkwaarde **Activiteit** voor de varianten, zoals wordt weergegeven in de volgende tabel.

| Variant     | Kenmerkwaarde Activiteit |
|-------------|--------------------------|
| P001-Master | Sport                   |
| P001-1      | Hardlopen                  |
| P001-2      | Wandelen                  |
| P001-3      | Trekking                 |

Als een gebruiker naar 'schoenen' zoekt, wordt het product **P001-Master** in de zoekresultaten weergegeven. Als u het kenmerk **Activiteit** als verfijnbaar hebt geconfigureerd, vermeldt de verfijner **Activiteit** alleen **Sport** als verfijnbare waarde, omdat die waarde voor het kenmerk **Activiteit** op **P001-Master** productniveau is gedefinieerd.

Standaard zijn kenmerken op variantniveau alleen bedoeld voor gebruik op productdetailpagina's (PDP's). Wanneer u een specifieke productvariant op een PDP selecteert, worden de productspecificaties op het PDP bijgewerkt voor die specifieke variant.

Om de waarden van de kenmerken door verfijners op te laten pikken die op het niveau van de productvariant zijn gedefinieerd, moet u een kenmerk op het niveau van de productmaster definiëren, het selectievakje **Meerdere waarden toestaan** inschakelen en het kenmerktype op **Tekst** instellen.

Vervolgens moet u alle mogelijke waarden voor uw productvarianten bepalen. Mogelijke waarden voor het kenmerk **Activiteit** dat in dit voorbeeld wordt gebruikt, zijn onder andere **Hardlopen**, **Wandelen**, **Wandeltochten**, **Trekking**, **Kamperen**, **Watersport** en **Wintersport**.

Nadat u hebt bepaald wat de variantkenmerkwaarden moeten zijn, kunt u deze definiëren op productmodelniveau met behulp van door een pipe-teken gescheiden waarden. Voor het kenmerk **Activiteit** kunt u de kenmerkwaarde in het productmodel definiëren als **Hardlopen|Wandelen|Wandeltochten|Trekking|Kamperen|Watersport|Wintersport**.

Vervolgens kunt u voor elke variant kenmerkwaarden definiëren door waarden tussen pipe-tekens of enkele waarden in te voeren. Voor het kenmerk **Activiteit** kunt u een afzonderlijke productvariant configureren als **Hardlopen|Wandelen|Wandeltochten**, **Hardlopen**, **Hardlopen|Wandeltochten|Watersport**, enzovoort.

Nadat u de waarden van de variantkenmerken hebt gedefinieerd, selecteert u op de pagina **Afzetkanaalcategorieën en productkenmerken** in het actievenster de optie **Afzetkanaalupdates publiceren**, en vervolgens voert u de taken **1150**, **1040** en **1070** uit.

Nadat de taken zijn voltooid en de zoekindex is bijgewerkt, moeten alle verwachte waarden worden weergegeven in de zoekresultaten en in de resultaten voor het bladeren door categorieën.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
