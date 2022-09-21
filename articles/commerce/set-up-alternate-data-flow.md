---
title: Een alternatieve gegevensstroom voor aanbevelingen instellen
description: In dit artikel wordt beschreven hoe u een omgeving configureert met een alternatieve gegevensflow die gegevens aan de aanbevelingenservice levert.
author: bebeale
ms.date: 09/08/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: b507b9bb57c68aca9424b53f8ccc009efea733bc
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460159"
---
# <a name="set-up-an-alternate-dataflow-for-recommendations"></a>Een alternatieve gegevensstroom voor aanbevelingen instellen

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u een omgeving configureert met een alternatieve gegevensflow die gegevens aan de aanbevelingenservice levert.

## <a name="comparison-of-out-of-the-box-dataflow-with-alternate-dataflow"></a>Vergelijking van out-of-the-box-gegevensflow met alternatieve gegevensflow

In de volgende afbeelding wordt de out-of-the-box-gegevensstroom in een omgeving weergegeven.

![Out-of-the-box-gegevensstroom in een omgeving](media/reco-out-of-the-box-dataflow-2.png)

In de volgende afbeelding wordt een alternatieve gegevensstroom weergegeven, waarbij de synchronisatiebatchtaak voor de entiteitsopslag wordt vervangen door alternatieve gegevensstroomstappen.

![Alternatieve gegevensstroom in een omgeving](media/reco-alternate-dataflow-2.png)

## <a name="assumptions"></a>Aannames

- In dit artikel wordt ervan uitgegaan dat u de aanbevelingenservice al hebt ingeschakeld voor uw omgeving. Zie voor meer informatie [Productaanbevelingen inschakelen](enable-product-recommendations.md).
- Als u werkt met bestanden en mappen in de Microsoft Azure Data Lake Storage-account:

    - U kunt de interface van het Azure-webportal gebruiken of de toepassing Azure Storage Explorer.
    - De beginpunten voor het werken met bestanden en mappen zijn in de container **dynamics365-financeandoperations**, die zich bevindt onder de map met de naam die overeenkomt met uw omgevings-URL.
    - Als de naam van uw sandbox-omgeving **MyUAT** is, is de basis-URL voor de omgeving als volgt: `myuat.sandbox.operations.dynamics.com`.
    - Als meerdere omgevingen aan dezelfde opslagaccount zijn gekoppeld, heeft elke omgeving een eigen hoofdmap.

## <a name="prerequisites"></a>Vereisten

Voordat u het scenario met de alternatieve gegevensstroom kunt implementeren, moet aan de volgende voorwaarden zijn voldaan:

### <a name="set-up-microsoft-power-platform"></a>Microsoft Power Platform instellen

Als u Microsoft Power Platform wilt configureren, volgt u de instructies in [De Microsoft Power Platform-integratie inschakelen](../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md).

### <a name="install-the-export-to-data-lake-add-in"></a>De invoegtoepassing Exporteren naar Data Lake installeren

Als u de invoegtoepassing Exporteren naar Data Lake wilt installeren, volgt u de instructies in [De invoegtoepassing Export naar Azure Data Lake installeren](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

> [!NOTE]
> Noteer de geconfigureerde waarden, omdat u deze nodig hebt voor een aantal van de volgende stappen.

### <a name="configure-tables-to-export-in-dynamics-365"></a>Tabellen configureren voor export in Dynamics 365

De synchronisatie van tabellen van Dynamics 365 naar Azure Data Lake Storage wordt beheerd op de pagina **Exporteren naar Data Lake**. Aangezien deze pagina momenteel geen menu-items bevat, kunnen alleen gebruikers met de beveiligingsrol **Systeembeheerder** deze openen.

Als u tabellen wilt configureren voor export in Dynamics 365, gaat u als volgt te werk.

1. Als u de pagina **Exporteren naar Data Lake** wilt openen, voegt u de tekenreeks `?mi=DataFeedsDefinitionWorkspace` toe aan de basis-URL van de omgeving, zoals in het volgende voorbeeld:

    `https://<environment-URL>/?mi=DataFeedsDefinitionWorkspace`

1. Kopieer op de pagina **Exporteren naar Data Lake** de tabellen die worden vermeld in de sectie [Lijst met RetailSales-cubetabellen](#list-of-retailsales-cube-tables) in dit artikel.
1. Vouw in de kolom **Systeemnaam** de lijst met filteropties uit.
1. Selecteer als filtertype de optie **is een van**. Plaats vervolgens de cursor in het tekstvak en plak de lijst met tabellen die u hebt gekopieerd van de pagina **Exporteren naar Data Lake**.
1. Selecteer onderaan de lijst met filteropties **Toepassen**.
1. Selecteer alle rijen in het raster en selecteer Vervolgens **Activeren**.

> [!NOTE]
> Voordat u naar de volgende stap gaat, moeten alle rijen de status **Wordt uitgevoerd** hebben. Spoor eventuele fouten op en los ze op.

### <a name="create-a-synapse-workspace"></a>Een Synapse-werkgebied maken

Als u nog geen Synapse-werkgebied hebt, maakt u er een volgens de instructies in [Snelstart: Een Synapse-werkgebied maken](/azure/synapse-analytics/quickstart-create-workspace).

Om uw Azure-resources overzichtelijk te houden, raden we u aan de Data Lake-opslagaccount en het Synapse-werkgebied in een resourcegroep in Azure te groeperen. U kunt hiervoor de opslagaccount gebruiken die u hebt gemaakt toen u de invoegtoepassing Exporteren naar Data Lake installeerde.

## <a name="create-a-database-in-synapse-for-recommendation-data-processing"></a>Een database in Synapse maken voor de verwerking van aanbevelingsgegevens

Maak met behulp van de consoletoepassing Common Data Model Utility (CDMUtil_ConsoleApp) een database in uw Synapse-werkgebied en vul deze vanuit de CMD-tabellen in Data Lake Storage. Het is raadzaam om de Common Data Model Utility te gebruiken met uw database in een ontwikkelomgeving, voor het geval er extensies zijn.

> [!NOTE]
> In de volgende stappen wordt ervan uit gegaan dat er geen extensiegegevens worden toegevoegd aan de cube RetailSales.

Volg deze stappen om een database te maken in Synapse.

1. Ga naar [Dynamics-365-FastTrack-Implementation-Assets GitHub](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Analytics/CDMUtilSolution#2-cdmutil-console-app) en volg de stappen om het zip-bestand **CDMUtilConsoleApp.zip** te downloaden.
1. Pak het zip-bestand uit in een lokale map.
1. Open het bestand **CDMUtil_ConsoleApp.dll.config** in een teksteditor en werk de volgende waarden bij:

    1. Stel de waarde van **Tenant ID** in (id van Azure-tenant).
    1. Stel de waarde van **Access key** in (de toegangssleutel voor de Data Lake Storage-account).

        1. Open uw opslagaccount in de Azure Portal.
        1. Selecteer in het menu aan de linkerkant van de pagina de optie **Toegangssleutels**.
        1. Selecteer **Sleutels tonen** bovenaan de pagina.
        1. Selecteer de knop Kopiëren voor een van de twee sleutelvelden en plak de waarde tussen de dubbele aanhalingstekens in het configuratiebestand.

    1. Stel de waarde voor **ManifestURL** in op de URL van uw bestand **Tables.manifest.cdm.json** in Azure Data Lake Storage. Voor de URL bladert u naar het bestand in de Azure-portal, selecteert u het ellipsis-teken (**...**) aan de rechterkant van de weergave en selecteert u vervolgens **Eigenschappen**. De URL is de eerste eigenschap die wordt getoond op het tabblad **Overzicht**.
    1. Stel de waarde van **TargetDbConnectionString** in op de verbindingsreeks voor de ingebouwde serverless SQL-pool van uw Synapse-werkgebied.

        1. Selecteer het tabblad **Beheren** in het Synapse-werkgebied.
        1. Selecteer in het submenu de optie **SQL pools**.
        1. Selecteer de naam **Built-in** om de eigenschappen van de pool weer te geven.
        1. Selecteer in het dialoogvenster met eigenschappen het ADO.NET-verbindingstype dat u wilt gebruiken. Kopieer vervolgens de waarde van de verbindingstekenreeks en plak deze tussen de dubbele aanhalingstekens in het configuratiebestand.

        > [!NOTE]
        > U moet machtigingen hebben om databases te maken. Om deze taak makkelijker uit te voeren, moet u misschien de ingebouwde beheerdersaccount **sqladminuser** gebruiken.

    1. Verwijder de opmerkingstekens bij het knooppunt **ProcessEntities** en stel de waarde ervan in op **true** (bijvoorbeeld `<add key="ProcessEntities" value ="true"/>`).

1. Sla het bestand **CDMUtil_ConsoleApp.dll.config** op en sluit het .
1. Kopieer het bestand **EntityList.json** naar de map **/Manifest**.
1. Voer in een opdrachtpromptvenster **cdmutil_consoleapp.exe** uit.

> [!NOTE]
> Controleer de uitvoer: er moeten 35 entiteiten/weergaven, minimaal 75 tabellen en geen fouten zijn.

## <a name="prepare-the-data-lake-retailsales-aggregate-measurements-directory"></a>De map Data Lake RetailSales Aggregate Measurements voorbereiden

### <a name="back-up-your-current-retailsales-cube-data-from-data-lake-storage"></a>Een back-up maken van uw huidige RetailSales-cubegegevens vanuit Data Lake Storage

De gemakkelijkste manier om een back-up te maken van uw huidige RetailSales-cubegegevens, is door de naam van de map **RetailSales** in Data Lake Storage te wijzigen in **RetailSales-backup** of iets dergelijks. Hiermee blijven de bestaande gegevens behouden, als het later nodig is om problemen op te lossen.

U vindt de cube-map **/RetailSales** op de volgende locatie:

`<storage-account>/dynamics365-financeandoperations/<environment-url (for example, myuat.sandbox.operations.dynamics.com)>/AggregateMeasurements/RetailSales`

### <a name="create-a-new-retailsales-folder-and-upload-the-model-file"></a>Een nieuwe map RetailSales maken en het modelbestand uploaden

Volg deze stappen om een nieuwe map **RetailSales** te maken en het bestand **model.json** te uploaden naar Data Lake Storage.

1. Maak een nieuwe lege map op hetzelfde niveau als de vorige map en geef deze de naam **RetailSales**.
1. Upload het bestand **model.json** naar de nieuwe map.

## <a name="create-a-pipeline-to-copy-the-retailsales-cube-data"></a>Een pijplijn maken om de gegevens van de RetailSales-cube te kopiëren

Via de pijplijn worden de weergaven van de RetailSales-cube gelezen en worden de gegevens geëxporteerd naar csv-bestanden in Data Lake Storage.

Volg deze stappen om een pijplijn te maken voor het kopiëren van de gegevens uit de RetailSales-cube.

1. Selecteer het tabblad **Integreren** in het Synapse-werkgebied.
1. Selecteer het plusteken (**+**) en selecteer Vervolgens **Importeren uit pijplijnsjabloon**.
1. Download het zip-bestand [ExportRetailSalesCubeViews.zip](https://aka.ms/reco-alternate-dataflow-files) en selecteer het.
1. Selecteer de service die aan de SQL-database is gekoppeld.
1. Selecteer de service die aan de opslagaccount is gekoppeld.
1. Start het hulpprogramma **Gegevens kopiëren** en wijzig de eigenschap **Mappad** in **\<environment_name\>/...**.

### <a name="test-execution-of-the-pipeline"></a>Testuitvoering van de pijplijn

Het is raadzaam om de pijplijn te testen met slechts één weergave. De weergave **RetailSales_RetailMediaTemplateView** werkt goed, omdat deze meestal minder dan 10 rijen bevat.

## <a name="schedule-the-pipeline-to-run-on-a-recurring-schedule"></a>De pijplijn plannen om op een terugkerend schema uit te voeren

Telkens wanneer de pijplijn wordt uitgevoerd, vindt het verbruik in Azure plaats. We raden u aan om uitvoeringen te plannen met intervallen van 48 uur of langer. U kunt de pijplijn altijd handmatig uitvoeren als u gegevens onmiddellijk moet synchroniseren. 
 
## <a name="table-list-for-synchronization-from-dynamics-365-to-data-lake-storage"></a>Lijst met tabellen voor synchronisatie van Dynamics 365 naar Data Lake Storage

De volgende lijst met tabellen is een subset van alle tabellen die nodig zijn voor de gehele RetailSales-cube. Slechts 15 weergaven in de RetailSales-cube worden gebruikt door de aanbevelingenservice en de lijst met vereiste tabellen is dienovereenkomstig gefilterd.

### <a name="list-of-retailsales-cube-tables"></a>Lijst met tabellen van RetailSales-cube

- BICalendarOffsets
- BIDateDimension
- BIDateDimensionValue
- Catalog
- CatalogProduct
- CatalogProductCategory
- CustInvoiceJour
- CustInvoiceTrans
- CustTable
- DataArea
- DimensionAttributeValueCombination
- DimensionAttributeValueSet
- DirPartyTable
- EcoResCategory
- EcoResCategoryHierarchy
- EcoResCategoryHierarchyRole
- EcoResColor
- EcoResConfiguration
- EcoResProduct
- EcoResProductCategory
- EcoResProductTranslation
- EcoResSize
- EcoResStyle
- HcmWorker
- InventDim
- InventDimCombination
- InventItemGroup
- InventItemGroupItem
- InventItemSetupSupplyType
- InventTable
- InventTrans
- LogisticsAddressCountryRegion
- LogisticsAddressCountryRegionTranslation
- LogisticsLocation
- LogisticsPostalAddress
- OMHIERARCHYPURPOSE
- RetailAssortmentLookup
- RetailAssortmentLookupChannelGroup
- RetailChannelProfile
- RetailChannelProfileProperty
- RetailChannelTable
- RetailChannelTableExt
- RetailConnDatabaseProfile
- RetailCustInvoiceJourTable
- RetailCustTable
- RetailMediaTemplate
- RetailOfflineProfile
- RetailPeriodicDiscount
- RetailRecoListConfigurationParameters
- RetailSalesTaxOverrideGroup
- RetailSharedParameters
- RetailSpecialCategoryMember
- RetailTenderTypeCardTable
- RetailTenderTypeTable
- RetailTerminalTable
- RetailTmpProductMedia
- RetailTransactionDiscountTrans
- RetailTransactionPaymentTrans
- RetailTransactionPaymentTransExt
- RetailTransactionSalesTrans
- RetailTransactionSalesTransExt
- RetailTransactionTable
- SalesLine
- SalesTable
- SystemParameters
- RETAILCATALOGINTERNALORG
- RETAILGROUPMEMBERLINE
- RETAILINTERNALORGANIZATION
- RETAILSPECIALCATEGORYPRODUCT
- RETAILPRODUCTCATEGORY
- ECORESCONFIGURATION
- DIMENSIONATTRIBUTE
- DIMENSIONATTRIBUTEVALUESET
- DIMENSIONHIERARCHY
- DIMENSIONHIERARCHYINTEGRATION
- DIMENSIONHIERARCHYLEVEL
- DIMENSIONPARAMETER
- OMExplodedOrganizationSecurityGraph

### <a name="view-list-for-the-parameter-to-pass-to-the-synapse-pipeline"></a>Lijst met weergaven voor de parameter om door te geven aan de Synaps-pijplijn

De volgende lijst met gegevens die met komma's zijn gescheiden, bevat de RetailSales-cubeweergaven waarop via de pijplijn een "select"-bewerking wordt uitgevoerd. De resultaten worden vervolgens gekopieerd naar Data Lake Storage.

RetailSales_RetailAssortmentRulesView,RetailSales_RetailChannelNavigationHierarchiesView,RetailSales_RetailChannelNavigationHierarchyCatalogProductsView,RetailSales_RetailChannelNavigationHierarchyCategoryNodesView,RetailSales_RetailChannelNavigationHierarchyCategoryProductsView,RetailSales_RetailMediaBaseUrlChannelView,RetailSales_RetailMediaRelativeUrlProductView,RetailSales_RetailMediaTemplateView,RetailSales_RetailOptOutCustomersView,RetailSales_RetailProductCategory,RetailSales_RetailProductTransaction,RetailSales_RetailProductVariantDimensionsView,RetailSales_RetailRecoListConfigurationParametersView,RetailSales_RetailRecoListsSharedParametersView,RetailSales_RetailEcoResProductTranslation

> [!IMPORTANT]
> De pijplijnparameter moet een lijst met weergavenamen zijn, die worden gescheiden door enkele komma's. Er mogen geen spaties of nieuwe regels zijn.

## <a name="environment-specific-fixes"></a>Omgevingsspecifieke oplossingen

### <a name="retailchannelview-fix"></a>Fix voor RETAILCHANNELVIEW

De weergava **RETAILCHANNELVIEW** bevat een in code vastgelegd geheel getal dat een organisatie van het type 'detailhandelafzetkanaal' vertegenwoordigt. De werkelijke waarde van het type kan verschillen van omgeving naar omgeving, of van tenant naar tenant.

```SQL
CREATE OR ALTER   VIEW [dbo].[RETAILCHANNELVIEW]
AS
SELECT T1.RECID AS RECID1,
       T1.STOREAREA AS STOREAREA,
       T1.OMOPERATINGUNITID AS OMOPERATINGUNITID,
       T1.DEFAULTCUSTACCOUNT AS DEFAULTCUSTOMER,
       T1.RETAILCHANNELID AS RETAILCHANNELID,
       T1.CHANNELTYPE AS CHANNELTYPE,
       T1.PARTITION AS PARTITION,
       T1.RECID AS RECID,
       T2.OMOPERATINGUNITNUMBER AS OMOPERATINGUNITNUMBER,
       T3.NAME AS NAME
FROM   dbo.RETAILCHANNELTABLE AS T1 CROSS JOIN dbo.DIRPARTYTABLE AS T2 CROSS JOIN dbo.DIRPARTYTABLE AS T3
WHERE  ((((T1.OMOPERATINGUNITID = T2.RECID)
          )
         AND ((T2.RECID = T3.RECID)
              ))
        AND T2.INSTANCERELATIONTYPE IN (8363));
```

Volg deze stappen om deze integer bij te werken.

1. Zoek in Dynamics 365 de waarde voor **ChannelID** voor uw online kanaal op.
1. Voer de volgende query uit in een exemplaar van SQL Server Management Studio (SSMS), die aan de Synapse-database is gekoppeld.

    ```SQL
    select INSTANCERELATIONTYPE, NAME, NAMEALIAS, * from dbo.DIRPARTYTABLE where RECID IN (select OMOPERATINGUNITID from dbo.RETAILCHANNELTABLE where RETAILCHANNELID =     <channelID>)
    ```

1. Kopieer de waarde van de eerste kolom (**INSTANCERELATIONTYPE**) en plak deze in de weergavedefinitie.

## <a name="troubleshooting"></a>Problemen oplossen

### <a name="pipeline-task-fails"></a>Pijplijntaak mislukt

Er moeten vijftien pijplijntaakuitvoeringen zijn voor de taak **CopyData**. Als een uitvoering mislukt, moet u controleren of alle afhankelijke SQL-objecten bestaan en of de query's worden uitgevoerd. De gemakkelijkste manier om alle afhankelijkheden te vinden, is door verbinding te maken met de database via SSMS. U kunt vervolgens een weergave selecteren en deze vasthouden (of er met de rechtermuisknop op klikken) en de optie **Generate CREATE as to a new window** (MAKEN als genereren in een nieuw venster).

Het foutbericht kan de volgende tekst bevatten.

- Error: Failure happened on 'Source' side
- Error handling external file: 'Max errors count'.
- /RetailSales/RetailSales_xxxxxx

#### <a name="example-scenario"></a>Voorbeeldscenario

In dit voorbeeld mislukt de **RetailSales_RetailproductCategory** en ontvangt u een fout 'Max errors count'.

Volg deze stappen om de fout op te lossen.

1. Open het bestand **EntityList.json** in een teksteditor (bijvoorbeeld Visual Studio Code).
1. Zoek de weergavedefinitie voor **RetailSales_RetailproductCategory**.

    ```SQL
    CREATE  VIEW [dbo].[RetailSales_RetailProductCategory] AS SELECT 0 AS ROW_UNIQUEKEY ,CATEGORY AS CATEGORYID ,PRODUCT AS PRODUCTID ,PRODUCTNAME ,CATEGORYNAME     ,PARENTCATEGORY AS PARENTCATEGORYID ,PARTITION ,RECID FROM RetailProductCategoryView
    ```

1. Deze weergave is afhankelijk van slechts één andere weergave: **RetailProductCategoryView** _. Zoek de weergavedefinitie voor **RetailProductCategoryView**.

    ```SQL
    CREATE VIEW [DBO].[RETAILPRODUCTCATEGORYVIEW] AS SELECT T1.CATEGORY AS CATEGORY, T1.PRODUCT AS PRODUCT, T1.PARTITION AS PARTITION, T1.RECID AS RECID, T2.PRODUCTNAME AS PRODUCTNAME, T2.PARTITION AS PARTITION#2, T3.NAME AS CATEGORYNAME, T3.PARENTCATEGORY AS PARENTCATEGORY, T3.PARTITION AS PARTITION#3 FROM RETAILPRODUCTCATEGORY T1 CROSS JOIN ECORESPRODUCTTRANSLATIONS T2 CROSS JOIN RETAILCATEGORYEXPANDED T3 WHERE((( T1.PRODUCT = T2.PRODUCT) AND ( T1.PARTITION = T2.PARTITION)) AND (( T1.CATEGORY = T3.RECID) AND ( T1.PARTITION = T3.PARTITION)))
    ```

1. Deze weergave is afhankelijk van drie andere weergaven: **RETAILPRODUCTCATEGORY**, **ECORESPRODUCTTRANSLATIONS** en **RETAILCATEGORYEXPANDED**. Zoek de definitie voor elk van deze weergaven en bekijk de afhankelijkheden. Ga verder totdat u alle afhankelijke weergaven hebt gevonden.

    Hier volgt de gehele lijst in de volgorde waarin ze in de afhankelijkheidsstructuur staan. Dertien weergaven moeten zijn gevalideerd.

    - RetailSales_RetailProductCategory

        - RetailProductCategoryView

            - RETAILPRODUCTCATEGORY

                - ECORESPRODUCTCATEGORY
                - ECORESCATEGORYHIERARCHYROLE
                - RETAILSPECIALCATEGORYPRODUCT

                    - ECORESPRODUCT
                    - RETAILGROUPMEMBERLINE
                    - RETAILSPECIALCATEGORYMEMBER

            - ECORESPRODUCTTRANSLATIONS

                - ECORESPRODUCT
                - ECORESPRODUCTTRANSLATION
                - SYSTEMPARAMETERS

            - RETAILCATEGORYEXPANDED

                - ECORESCATEGORY
                - ECORESCATEGORYHIERARCHYROLE

1. Maak in Excel de volgende 13 instructies **select count(\*) from \<view_name\>** aan. Voer deze instructies uit in SSMS en verzend de resultaten naar tekst. Blader vervolgens door de resultaten om te zien of een van de weergaven is mislukt. De eerste fout geeft aan dat minimaal een van de weergaven mislukt.

    ```SQL
    select count(*) from RetailProductCategoryView
    select count(*) from RETAILPRODUCTCATEGORY
    select count(*) from ECORESPRODUCTCATEGORY
    select count(*) from ECORESCATEGORYHIERARCHYROLE
    select count(*) from RETAILSPECIALCATEGORYPRODUCT
    select count(*) from ECORESPRODUCT
    select count(*) from RETAILGROUPMEMBERLINE
    select count(*) from RETAILSPECIALCATEGORYMEMBER
    select count(*) from ECORESPRODUCTTRANSLATIONS
    select count(*) from ECORESPRODUCTTRANSLATION
    select count(*) from SYSTEMPARAMETERS
    select count(*) from RETAILCATEGORYEXPANDED
    select count(*) from ECORESCATEGORY
    ```

1. Een manier om te valideren wat u zoekt, is een basisafhankelijke weergave maken om de weergavedefinitie in SSMS te genereren. Controleer vervolgens of er een bestandskolom in Azure Data Lake is met de naam **r.filepath**. De aanwezigheid van deze kolom geeft aan dat de weergave die u controleert, gegevens leest uit Data Lake Storage.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht productaanbevelingen](product-recommendations.md)

[Azure Data Lake Storage inschakelen in een Dynamics 365 Commerce-omgeving](enable-adls-environment.md)

[Gepersonaliseerde aanbevelingen inschakelen](personalized-recommendations.md)

[Aanbevelingen voor vergelijkbare artikelen inschakelen](shop-similar-looks.md)

[Afmelden voor gepersonaliseerde aanbevelingen](personalization-gdpr.md)

[Productaanbevelingen toevoegen op POS](product.md)

[Aanbevelingen toevoegen aan het transactiescherm](add-recommendations-control-pos-screen.md)

[Resultaten van AI-ML-aanbevelingen aanpassen](modify-product-recommendation-results.md)

[Handmatig gecureerde aanbevelingen maken](create-editorial-recommendation-lists.md)

[Aanbevelingen maken met voorbeeldgegevens](product-recommendations-demo-data.md)

[Veelgestelde vragen over productaanbevelingen](faq-recommendations.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
