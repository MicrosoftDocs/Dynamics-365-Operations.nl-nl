---
title: Afhankelijkheidsketen van entiteiten (synchronisatievolgorde)
description: In dit onderwerp wordt de synchronisatievolgorde aangegeven die u moet volgen om de eerste gegevens te maken.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 4adb2c8d57ad8f67346b8d34212b7a4b0bd052ab
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173126"
---
# <a name="entity-dependency-chain-synchronization-order"></a>Afhankelijkheidsketen van entiteiten (synchronisatievolgorde)

[!include [banner](../../includes/banner.md)]



In de volgende tabel worden de entiteiten vermeld in de volgorde waarin u ze moet inschakelen. Wanneer u een kaart voor initiële synchronisatie inschakelt, detecteert de functie voor twee keer wegschrijven andere toewijzingen die moeten worden ingeschakeld. U kunt de pagina **Twee keer wegschrijven** in Finance and Operations-apps gebruiken om de entiteiten te selecteren of de selectie te annuleren tijdens de initiële synchronisatie.

In de meest recente versie van de functie voor twee keer wegschrijven kunt u ook slechts enkele entiteiten inschakelen en worden de afhankelijkheden voor u afgehandeld.

## <a name="dynamics-365-supply-chain-management-entities"></a>Dynamics 365 Supply Chain Management-entiteiten

De volgende entiteiten voor Supply Chain Management worden vermeld in de volgorde waarin u ze moet inschakelen.

| Naam van toewijzing op de pagina Twee keer wegschrijven | Naam van entiteitsmetagegevens in Supply Chain Management | Naam van entiteitsmetagegevens in Common Data Service | Opmerkingen |
|---|---|---|---|
| Eenheden ... uoms                                                                      | UnitOfMeasureEntity                                    | uom                                          | |
| Eenheidsomrekeningen ... msdyn_unitofmeasureconversions                                 | UnitOfMeasureConversionEntity                          | msdyn_unitofmeasureconversion                | |
| Alle producten ... msdyn_globalproducts                                               | EcoResEveryproductEntity                               | msdyn_globalproduct                          | |
| Productdimensiegroepen ... msdyn_productdimensiongroups                           | EcoResProductDimensionGroupEntity                      | msdyn_productdimensiongroup                  | |
| Opslagdimensiegroepen ... msdyn_productstoragedimensiongroups                    | EcoResStorageDimensionGroupEntity                      | msdyn_productstoragedimensiongroup           | |
| Traceringsdimensiegroepen ... msdyn_producttrackingdimensiongroups                  | EcoResTrackingDimensionGroupEntity                     | msdyn_producttrackingdimensiongroup          | |
| Kleuren ... msdyn_productcolors                                                      | EcoResProductColorEntity                               | msdyn_productcolor                           | |
| Afmetingen ... msdyn_productsizes                                                        | EcoResProductSizeEntity                                | msdyn_productsize                            | |
| Stijl ... msdyn_productstyles                                                      | EcoResProductStyleEntity                               | msdyn_productstyle                           | |
| Configuraties ... msdyn_productconfigurations                                      | EcoResProductConfigurationEntity                       | msdyn_productconfiguration                   | |
| Vrijgegeven producten V2 ... msdynsharedproductdetails                                 | EcoResReleasedProductV2Entity                          | msdyn_sharedproductdetail                    | |
| In Common Data Service vrijgegeven verschillende producten ... products                         | EcoResReleasedDistinctProductCommon Data ServiceEntity | product                                      | |
| Productnummer geïdentificeerd met streepjescode ... msdyn_productbarcodes                         | EcoResProductNumberIdentifiedBarcodeEntity             | msdyn_productbarcode                         | |
| Standaard orderinstellingen ... msdyn_productdefaultordersettings                        | InventProductDefaultOrderSettingsEntity                | msdyn_productdefaultordersetting             | |
| Standaard orderinstellingen voor product V2... msdyn_productspecificdefaultordersettings     | InventProductSpecificOrderSettingsV2Entity             | msdyn_productspecificdefaultordersetting     | |
| Omrekeningen van productspecifieke eenheden ... msdyn_productspecificunitofmeasureconversions | EcoResProductSpecificUnitConversionEntity              | msdyn_productspecificunitofmeasureconversion | |
| Locaties ... msdyn_operationalsites                                                    | InventOperationalSiteEntity                            | msdyn_operationalsite                        | |
| Magazijnen ... msdyn_warehouses                                                     | InventWarehouseEntity                                  | msdyn_warehouse                              | Zie [opmerking 1](#scm-notes). |
| Kleuren van productmodellen ... msdyn_sharedproductcolors                                 | EcoResProductMasterColorEntity                         | msdyn_sharedproductcolor                     | |
| Afmetingen van productmodellen ... msdyn_sharedproductsizes                                   | EcoResProductMasterSizeEntity                          | msdyn_sharedproductsize                      | |
| Stijlen van productmodellen ... msdyn_sharedproductstyles                                 | EcoResProductMasterStyleEntity                         | msdyn_sharedproductstyle                     | |
| Configuraties van productmodellen ... msdyn_sharedproductconfigurations                 | EcoResProductMasterConfigurationEntity                 | msdyn_sharedproductconfiguration             | |
| Productcategorieën ... msdyn_productcategories                                      | EcoResProductCategoryEntity                            | msdyn_productcategory                        | Zie [opmerking 2](#scm-notes). |
| Toewijzingen van productcategorieën ... msdyn_productcategoryassignments                   | EcoResProductCategoryAssignmentEntity                  | msdyn_productcategoryassignment              | |
| Productcategoriehiërarchieën ... msdyn_productcategoryhierarchies                   | EcoResProductCategoryHierarchyEntity                   | msdyn_productcategoryhierarchy               | |
| Productcategoriehiërarchierollen ... msdyn_productcategoryhierarchies            | EcoResProductCategoryHierarchyRoleEntity               | msdyn_productcategoryhierarchyrole           | |
| Voorraadgang ... msdyn_warehouseaisles                                           | WMSWarehouseAisleEntity                                | msdyn_warehouseaisle                         | |
| Magazijnzones ... msdyn_warehousezones                                            | WHSWarehouseZoneEntity                                 | msdyn_warehousezone                          | |
| Magazijnzonegroepen ... msdyn_warehousezonegroups                                 | WHSWarehouseZoneGroupEntity                            | msdyn_warehousezonegroup                     | |
| Magazijnlocaties ... msdyn_inventorylocations                                    | WMSWarehouseLocationEntity                             | msdyn_inventorylocation                      | Zie [opmerking 3](#scm-notes). |
| Magazijnwerkkoppen ... msdyn_warehouseworkheaders                               | WHSWarehouseWorkHeaderEntity                           | msdyn_warehouseworkheader                    | |
| Magazijnwerkregels ... msdyn_warehouseworklines                                    | WHSWarehouseWorkLineEntity                             | msdyn_warehouseworklines                     | Zie [opmerking 4](#scm-notes). |
| Leveringsmethoden ... msdyn_shipvias                                                | DlvDeliveryModeEntity                                  | msdyn_shipvias                               | |
| Leveringsvoorwaarden ... msdyn_termsofdeliveries                                       | DeliveryTermsEntity                                    | msdyn_termsofdelivery                        | |
| Oorsprongcodes van verkooporder ... msdyn_salesorderorigins                                | SalesOrderOriginEntity                                 | msdyn_salesorderorigin                       | |
| Common Data Service-verkooporderkoppen ... salesorders                             | SalesOrderHeaderCommon Data ServiceEntity              | salesorder                                   | |
| Common Data Service-verkooporderregels ... salesorderdetails                         | SalesOrderLineCommon Data ServiceEntity                | salesorderdetails                            | |
| Common Data Service-verkoopoffertekoptekst ... quotes                               | SalesQuotationHeaderCommon Data ServiceEntity          | offerte                                        | |
| Common Data Service-verkoopofferteregels ... quotedetails                          | SalesQuotationLineCommon Data ServiceEntity            | QuoteDetails                                 | |
| Kopteksten van verkoopfacturen V2 ... invoices                                               | SalesInvoiceHeaderV2Entity                             | factuur                                      | |
| Verkoopfactuurregels V2 ... invoicedetails                                           | SalesInvoiceLineV2Entity                               | invoicedetail                                | |

### <a name="mapping-specific-notes"></a><a id='scm-notes'></a>Toewijzingsspecifieke opmerkingen

1. Vanwege zelfafhankelijkheid moet u de initiële synchronisatie mogelijk twee keer uitvoeren.
2. Standaard is de initiële synchronisatie uitgeschakeld vanwege de relatie tussen bovenliggende en onderliggende items (slimme ordening wordt niet door het platform afgehandeld). Daarom moeten de bestaande productcategorieën handmatig worden gesynchroniseerd (bijvoorbeeld door de beschrijving van de categorie bij te werken) in de juiste volgorde (eerst hoofdcategorie, vervolgens onderliggende items en vervolgens onderliggende items van onderliggende items). Ga naar **Productgegevensbeheer \> Instellen \> Categorieën en kenmerken \> Categoriehiërarchieën**. Op de pagina **Categoriehiërarchieën** kunt u elke hiërarchie selecteren en de productcategorieën hierin bekijken.
3. De toewijzing van lege opzoekvelden van het type **ItemNumberInLocation** en de eerste, tweede en derde aanvullende magazijnzones leiden ertoe dat de initiële synchronisatie mislukt. Daarom worden deze toewijzingen voor nu verwijderd.
4. De toewijzing van het lege veld **CaptureWeight** heeft tot gevolg dat de initiële synchronisatie mislukt. Daarom wordt deze toewijzing voor nu verwijderd.

### <a name="setup-related-information"></a>Informatie over instellingen

+ Wanneer records voor het eerst worden gemaakt in de entiteit **Producten** in modelgestuurde apps in Dynamics 365, hebben ze de status **Concept**. Als u de status wilt wijzigen in **Actief**, gaat u naar **Instellingen \> Beheer \> Systeeminstellingen \> Verkoop** in de modelgestuurde app en stelt u de optie **Producten maken in actieve status** in op **Ja**.
+ Als u records maakt in de entiteit **Producten** in modelgestuurde apps in Dynamics 365 of in Common Data Service voordat u Twee keer wegschrijven inschakelt, worden deze records alleen bijgewerkt als de gehele sleutel, inclusief **Bedrijf**, overeenkomt met gegevens in de app Finance and Operations.
+ Synchronisatie van de entiteit **Producten** is in één richting, van Finance and Operations-apps naar Common Data Service. Als een toegewezen veld in de entiteit **Producten** in modelgestuurde apps in Dynamics 365 wordt bijgewerkt, wordt de update overschreven tijdens de volgende synchronisatie van de Finance and Operations-app.

### <a name="known-issues"></a>Bekende problemen

- Er treedt een fout op wanneer een eenheid in een Finance and Operations-app wordt verwijderd. Wanneer maateenheden vanuit de Finance and Operations-app naar Common Data Service worden gesynchroniseerd, wordt de eerste eenheid van een specifieke klasse gemaakt als primaire eenheid en wordt verwijdering voorkomen.

    **Risicobeperking:** verwijder de eenheid eerst in Common Data Service. Deze kan vervolgens worden verwijderd in de Finance and Operations-app.

- Er treedt een fout op wanneer een operationele site wordt verwijderd in Common Data Service. In het fout bericht staat 'Infologboek: Waarschuwing: het primaire adres kan niet worden verwijderd. Waarschuwing: de entiteitsrecord kan niet worden verwijderd omdat de validatie is mislukt voor de volgende gegevensbron: InventSiteLogisticsLocation (InventSiteLogisticsLocation).' Deze fout wordt veroorzaakt door een probleem in de gegevensentiteit in de Finance and Operations-app.

    **Risicobeperking:** u kunt de site in de Finance and Operations-app verwijderen. De site wordt vervolgens verwijderd in Common Data Service als de bijbehorende toewijzing voor Twee keer wegschrijven wordt uitgevoerd.

## <a name="dynamics-365-finance-entities"></a>Dynamics 365 Finance-entiteiten

De volgende entiteiten voor Dynamics 365 Finance worden vermeld in de volgorde waarin u ze moet inschakelen.

| Naam van toewijzing op de pagina Twee keer wegschrijven | Naam van entiteitsmetagegevens in Finance | Naam van entiteitsmetagegevens in Common Data Service | Opmerkingen |
|---|---|---|---|
| Valuta's ... transactioncurrencies                                            | CurrencyEntity                              | Valuta                                   | |
| Wisselkoerstype ... msdyn_exchangeratetypes                                  | ExchangeRateTypeEntity                      | msdyn_exchangeratetype                     | |
| Valutapaar wisselkoers ... msdyn_currencyexchangeratepairs                 | ExchangeRateCurrencyPairEntity              | msdyn_currencyexchangeratepair             | |
| Wisselkoersen Common Data Service .... msdyn_currencyexchangerates              | ExchangeRateCommon Data ServiceEntity       | msdyn_currencyexchangerate                 | Zie [opmerking 1](#fin-notes). |
| Entiteit voor integratie van fiscale kalender ... msdyn_fiscalcalendars                    | FiscalCalendarEntity                        | msdyn_fiscalcalendar                       | |
| Entiteit voor integratie van fiscaal kalenderjaar ... msdyn_fiscalcalendaryears           | FiscalCalendarYearEntity                    | msdyn_fiscalcalendaryear                   | |
| Fiscale kalenderperiode ... msdyn_fiscalcalendarperiods                          | FiscalPeriodEntity                          | msdyn_fiscalcalendarperiod                 | |
| Organisatiehiërarchietype ... msdyn_internalorganizationhierarchytypes        | OMOrganizationHierarchyTypeEntity           | msdyn_internalorganizationhierarchytype    | Zie [opmerking 1](#fin-notes). |
| Organisatiehiërarchiedoelstellingen ... msdyn_internalorganizationhierarchypurposes | OMOrganizationHierarchyPurposeEntity        | msdyn_internalorganizationhierarchypurpose | Zie [opmerking 1](#fin-notes). |
| Rechtspersonen ... msdyn_internalorganizations                                  | OMLegalEntity                               | msdyn_internalorganization                 | Zie [opmerking 1](#fin-notes). |
| Rechtspersonen ... cdm_companies                                                | OMLegalEntity                               | cdm_company                                | |
| Operationele eenheid ... msdyn_internalorganizations                                  | OMOperatingUnitEntity                       | msdyn_internalorganization                 | Zie [opmerking 1](#fin-notes). |
| Organisatiehiërarchie - gepubliceerd ... msdyn_internalorganizationhierarchies    | OMOrganizationHierarchyPublishedEntity      | msdyn_internalorganizationhierarchy        | Zie [opmerking 1](#fin-notes). |
| Naamachtervoegsels ... msdyn_nameaffixes                                              | DirNameAffixEntity                          | msdyn_nameaffix                            | |
| Betaaldagen Common Data Service ... msdyn_paymentdays                          | PaymentDayCommon Data ServiceEntity         | msdyn_paymentday                           | |
| Betalingsdagregels Common Data Service V2 ... msdyn_paymentdaylines              | PaymentDayLineCommon Data ServiceV2Entity   | msdyn_paymentdayline                       | |
| Betalingsschema ... msdyn_paymentschedules                                     | PaymentScheduleEntity                       | msdyn_paymentschedule                      | |
| Betalingsschemaregels ... msdyn_paymentschedulelines                           | PaymentScheduleLineEntity                   | msdyn_paymentscheduleline                  | |
| Betalingstermijnen ... msdyn_paymentterms                                         | PaymentTermEntity                           | msdyn_paymentterm                          | |
| Betalingsmethode van klant ... msdyn_customerpaymentmethods                        | CustomerPaymentMethodEntity                 | msdyn_customerpaymentmethod                | |
| Betalingsmethode van leverancier ... msdyn_vendorpaymentmethods                            | VendorPaymentMethodEntity                   | msdyn_vendorpaymentmethod                  | |
| Klantengroepen ... msdyn_customergroups                                        | CustCustomerGroupEntity                     | msdyn_customergroup                        | |
| Leveranciersgroepen ... msdyn_vendorgroups                                            | VendVendorGroupEntity                       | msdyn_vendorgroup                          | |
| Btw-groepen ... msdyn_taxgroups                                            | TaxGroupEntity                              | msdyn_taxgroup                             | |
| Btw-groepen voor artikel ... msdyn_taxitemgroups                                   | TaxItemGroupEntity                          | msdyn_taxitemgroup                         | |
| Boekingsgroepen in btw-grootboek V2 ... msdyn_taxpostinggroups                   | TaxPostingGroupEntityV2                     | msdyn_taxpostinggroup                      | |
| Entiteit btw-vrijstellingscode in Common Data Service ... msdyn_taxexemptcodes       | TaxExemptCodeCommon Data ServiceEntity      | msdyn_taxexemptcode                        | |
| Btw-dienst ... msdyn_taxauthorities                                  | TaxAuthorityEntity                          | msdyn_taxauthority                         | |
| Btw-code ... msdyn_taxcodes                                               | TaxCodeEntity                               | msdyn_taxcode                              | Zie [opmerking 1](#fin-notes). |
| Indeling van financiële dimensies ... msdyn_financialdimensionformats                  | DimensionIntegrationFormatEntity            | msdyn_financialdimensionformat             | |
| Financiële dimensies ... msdyn_dimensionattributes                              | DimensionAttributeEntity                    | msdyn_dimensionattribute                   | |
| Bronbelastinggroepen ... msdyn_withholdingtaxgroups                           | TaxWithholdingGroupEntity                   | msdyn_withholdingtaxgroup                  | |
| Bronbelastingcodes ... msdyn_withholdingtaxcodes                             | TaxWithholdingTaxCodes                      | msdyn_withholdingtaxcode                   | |
| Rekeningschema ... msdyn_chartofaccountses                                   | LedgerChartOfAccountsEntity                 | msdyn_chartofaccounts                      | |
| Grootboek ... msdyn_ledgers                                                        | LedgerEntity                                | msdyn_ledger                               | Zie [opmerking 1](#fin-notes). |
| Hoofdrekeningcategorieën ... msdyn_mainaccountcategories                         | MainAccountCategoryEntity                   | msdyn_mainaccountcategory                  | |
| Hoofdrekening ... msdyn_mainaccounts                                             | MainAccountEntity                           | msdyn_mainaccount                          | |
| Klanten V3 ... accounts                                                       | CustCustomerV3Entity                        | rekening                                    | Zie [opmerking 2](#fin-notes). |
| Klanten V3 ... contacts                                                       | CustCustomerV3Entity                        | contactpersoon/contact                                    | Zie [opmerking 3](#fin-notes). |
| Leveranciers v2 ... msdyn_vendors                                                    | VendVendorV2Entity                          | msdyn_vendor                               | Zie [opmerking 2](#fin-notes). |
| Common Data Service-contactpersonen V2 ... contactpersonen                                    | smmContactPersonCommon Data ServiceV2Entity | contactpersoon/contact                                    | Zie [opmerking 4](#fin-notes). |
| Common Data Service-contactpersonen V2 ... contactpersonen                                    | smmContactPersonCommon Data ServiceV2Entity | contactpersoon/contact                                    | Zie [opmerking 5](#fin-notes). |

### <a name="mapping-specific-notes"></a><a id='fin-notes'></a>Toewijzingsspecifieke opmerkingen

1. Er vindt synchronisatie in één richting plaats van Finance and Operations-apps naar Common Data Service.
2. Vanwege zelfafhankelijkheid moet u de initiële synchronisatie mogelijk meerdere keren uitvoeren. Zorg ervoor dat u **Klant** selecteert als relatietype wanneer u een rekening maakt via de pagina **Rekeningen** in Common Data Service. Als u problemen ondervindt met het veld **Primaire contactpersoon** tijdens de initiële synchronisatie, verwijdert u dat veld uit de toewijzing en voert u de initiële synchronisatie opnieuw uit. Na de initiële synchronisatie stopt u de toewijzing en voegt u het veld **Primaire contactpersoon** opnieuw hieraan toe. Start vervolgens de toewijzing, maar sla de initiële synchronisatie over. De waarde van het veld **Primaire contactpersoon** wordt niet opgenomen in de initiële synchronisatie en u moet de waarden handmatig migreren.
3. Zorg ervoor dat u de optie **Verkoopbaar** op **Ja** hebt ingesteld op de pagina **Contactpersoon** in Common Data Service wanneer u een klant van het type **Persoon** probeert te maken.
4. Deze toewijzing heeft aan beide zijden een filter om klantcontactpersonen te koppelen. Open de toewijzingsdetails, selecteer de filterknop (trechtersymbool) naast de entiteitsnaam **Sales.Contact** en controleer of de bestandscriteria **msdyn_contactforvendor eq true en msdyn_sellable eq false** bevatten.
5. Deze toewijzing heeft aan beide zijden een filter om leverancierscontactpersonen te koppelen. Open de toewijzingsdetails, selecteer de filterknop (trechtersymbool) naast de entiteitsnaam **Sales.Contact** en controleer of de filtercriteria **msdyn_contactforvendor eq true en msdyn_sellable eq false** bevatten. 

## <a name="dynamics-365-human-resources-entities"></a>Dynamics 365 Human Resources-entiteiten

De volgende entiteiten voor Dynamics 365 Human Resources worden vermeld in de volgorde waarin u ze moet inschakelen.

| Naam van toewijzing op de pagina Twee keer wegschrijven | Naam van entiteitsmetagegevens in Human Resources | Naam van entiteitsmetagegevens in Common Data Service | Opmerkingen |
|---|---|---|---|
| cdm_jobfunction - Functiepositie                                |                                   | cdm_jobfunction                  | |
| cdm_jobtypes - Functietypen                                      |                                   | cdm_jobtypes                     | |
| cdm_jobs - Functies                                               |                                   | cdm_jobs                         | |
| cdm_jobs - Functiedetails                                        |                                   | cdm_jobs                         | |
| cdm_positiontype - PositionType                               | HcmPositionTypeEntity             | cdm_positiontype                 | |
| cdm_jobpositions - Basispositie                              | HcmPositionBaseEntity             | cdm_jobposition                  | Zie [opmerking 1](#hr-notes). |
| cdm_jobposition - Positiedetails                            | HcmPositionDetailEntity           | cdm_jobposition                  | Zie [opmerking 1](#hr-notes). |
| cdm_jobposition - Positieduur                           | HcmPositionDurationEntity         | cdm_jobposition                  | Zie [opmerking 1](#hr-notes). |
| cdm_jobposition - Functiehiërarchieën                        | HcmPositionHierarchyEntity        | cdm_jobposition                  | Zie [opmerking 1](#hr-notes). |
| cdm_veteranstatus - Veteraanstatus                            |                                   | cdm_veteranstatus                | |
| cdm_ethnicorigin - Etnische afkomst                              |                                   | cdm_ethnicorigin                 | |
| cdm_languagecode - Taalcode                              |                                   | cdm_languagecode                 | |
| cdm_worker - Medewerker                                           | HcmWorkerEntity                   | cdm_worker                       | |
| cdm_employments - Aanstellingen                                 |                                   | cdm_employments                  | |
| cdm_employments - Details dienstverband                           |                                   | cdm_employments                  | |
| cdm_positionworkerassignmentmaps - Medewerkertoewijzing voor positie | HcmPositionWorkerAssignmentEntity | cdm_positionworkerassignmentmaps | Zie [opmerking 2](#hr-notes).|

### <a name="mapping-specific-notes"></a><a id='hr-notes'></a>Toewijzingsspecifieke opmerkingen

1. Eén Common Data Service-entiteit wordt toegewezen aan verschillende Finance and Operations-app-entiteiten.
2. Deze toewijzing heeft een verwijzing naar zichzelf.

## <a name="asset-management-entities"></a>Entiteiten voor Activabeheer

De volgende entiteiten voor Activabeheer voor Dynamics 365 Supply Chain Management worden vermeld in de volgorde waarin u ze moet inschakelen.

| Naam van toewijzing op de pagina Twee keer wegschrijven | Naam van entiteitsmetagegevens in Activabeheer | Naam van entiteitsmetagegevens in Common Data Service | Opmerkingen |
|---|---|---|---|
| FO.AssetManagementAssetLifecycleStates--Common Data Service.msdyn_assetlifecyclestates                           | Statussen van levenscyclus van activa voor activabeheer               | msdyn_assetlifecyclestates               | |
| FO.AssetManagementAssetLifecycleModels--Common Data Service.msdyn_assetlifecyclemodels                           | Levenscyclusmodellen van activa voor activabeheer               | msdyn_assetlifecyclemodels               | |
| FO.AssetManagementFunctionalLocationLifecycleModels--Common Data Service.msdyn_functionallocationlifecyclemodels | Levenscyclusmodellen voor functionele locaties voor activabeheer | msdyn_functionallocationlifecyclemodels  | |
| FO.AssetManagementFunctionalLocationLifecycleStates--Common Data Service.msdyn_functionallocationlifecyclestates | Levenscyclusstatussen voor functionele locaties voor activabeheer | msdyn_functionallocationlifecyclestates  | |
| FO.AssetManagementAssetTypes--Common Data Service.msdyn_customerassetcategories                                  | Activatypen voor activabeheer                          | msdyn_customerassetcategories            | |
| FO.AssetManagementFunctionalLocationTypes--Common Data Service.msdyn_functionallocationtypes                     | Functionele locatietypen voor activabeheer            | msdyn_functionallocationtypes            | |
| FO.AssetManagementFunctionalLocations--Common Data Service.msdyn_functionallocations                             | Functionele locaties voor activabeheer                 | msdyn_functionallocations                | Zie [de opmerking](#am-notes). |
| FO.AssetManagementAssets--Common Data Service.msdyn_customerassets                                               | Activa voor activabeheer                               | msdyn_customerassets                     | Zie [de opmerking](#am-notes). |
| FO.AssetManagementManufacturers--Common Data Service.msdyn_manufacturers                                         | Fabrikanten voor activabeheer                        | msdyn_manufacturers                      | |
| FO.AssetManagementModels--Common Data Service.msdyn_models                                                       | Modellen voor activabeheer                               | msdyn_models                             | |
| FO.AssetManagementWarranty--Common Data Service.msdyn_warranties                                                 | Garantie voor activabeheer                             | msdyn_warranties                         | |

### <a name="mapping-specific-notes"></a><a id='am-notes'></a>Toewijzingsspecifieke opmerkingen

- Vanwege zelfafhankelijkheid moet u de initiële synchronisatie mogelijk meerdere keren uitvoeren.
