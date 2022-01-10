---
title: Dual-write Application Orchestration-pakket is opgesplitst
description: Het Dual-write Application Orchestration-pakket is niet langer één pakket, maar is opgesplitst in kleinere pakketten. In dit onderwerp worden de oplossingen en kaarten besproken die elk pakket bevat en hun afhankelijkheid van andere pakketten.
author: RamaKrishnamoorthy
ms.date: 11/29/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.custom: separate-solution
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-11-29
ms.openlocfilehash: 3fe1b7707df72927fba78ee9659502cc62471799
ms.sourcegitcommit: 70ac76be31bab7ed5e93f92f4683e65031fbdf85
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/16/2021
ms.locfileid: "7924866"
---
# <a name="separated-dual-write-application-orchestration-package"></a>Dual-write Application Orchestration-pakket is opgesplitst

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Voorheen was het Dual-write Application Orchestration-pakket een enkel pakket dat de volgende oplossingen bevatte:

- Dynamics 365 Notes
- Algemeen anker voor Dynamics 365 Finance and Operations
- Entiteitstoewijzingen voor Dynamics 365 Finance and Operations Dual Write
- Dynamics 365-app voor activabeheer
- Dynamics 365 Activabeheer
- HCM - Algemeen
- Dynamics 365 Supply Chain Extended
- Dynamics 365 Finance Extended
- Dynamics 365 Finance and Operations Common
- Dynamics 365 Company
- Currency Exchange Rates
- Field Service Common

Omdat het één pakket was, heeft dit pakket voor een 'alles of niets'-situatie voor klanten gezorgd. Microsoft heeft de software echter nu opgesplitst in kleinere pakketten. Daarom kan de klant alleen de pakketten selecteren voor de oplossingen die zij nodig hebben. Als u bijvoorbeeld een Microsoft Dynamics 365 Supply Chain Management-klant bent en u geen integratie nodig hebt met Dynamics 365 Human Resources, notities en activabeheer, kunt u deze oplossingen uitsluiten van de geïnstalleerde oplossingen. Omdat de onderliggende oplossingsnamen, uitgever- en kaartversies blijven hetzelfde, is dit geen ingrijpende wijziging. Bestaande installaties worden bijgewerkt.

![Opgesplitst pakket.](media/separated-package-1.png)

In dit onderwerp worden de oplossingen en kaarten besproken die elk pakket bevat en hun afhankelijkheid van andere pakketten.

## <a name="dual-write-application-core"></a>Dual-write Application Core

Met het Dual-write Application Core-pakket kunnen gebruikers twee keer wegschrijven installeren en configureren zonder gebruik te maken van een app voor klantbetrokkenheid. De volgende vijf oplossingen zijn opgenomen.

| Unieke naam                           | Weergavenaam                               |
|---------------------------------------|--------------------------------------------|
| Dynamics365Company                    | Dynamics 365 Company                       |
| Dynamics365FinanceAndOperationsCommon | Dynamics 365 Finance and Operations Common |
| CurrencyExchangeRates                 | Currency Exchange Rates                    |
| msdyn_DualWriteAppCoreMaps            | Entiteitstoewijzingen voor Dual-write applications core   |
| msdyn_DualWriteAppCoreAnchor          | Basisanker voor Dual-write-toepassingen        |

De volgende kaarten zijn beschikbaar in dit pakket.

| Finance and Operations-apps     | Customer Engagement-apps                    |
|---------------------------------|---------------------------------------------|
| Operationele eenheid                  | msdyn_internalorganizations                 |
| Organisatiehiërarchie          | msdyn_internalorganizationhierarchies       |
| Rechtspersonen                  | msdyn_internalorganizations                 |
| Rechtspersonen                  | cdm_companies                               |
| Organisatiehiërarchiedoelstellingen | msdyn_internalorganizationhierarchypurposes |
| Valutapaar wisselkoers     | msdyn_currencyexchangeratepairs             |
| Voor- en achtervoegsel naam                    | msdyn_nameaffixes                           |
| Wisselkoerstype              | msdyn_exchangeratetypes                     |
| Wisselkoersen CDS              | msdyn_currencyexchangerates                 |
| Type organisatiehiërarchie     | msdyn_internalorganizationhierarchytypes    |
| Valuta's                      | transactioncurrencies                       |
| Entiteit mixed reality-guides     | msmrw_guides                                |

**Afhankelijkheidsgegevens**

Het Dual-write Application Core-pakket is niet afhankelijk van andere pakketten.

## <a name="dual-write-human-resources"></a>Dual-write Human Resources

Het Dual-write Human Resources-pakket bevat de oplossingen en kaarten die nodig zijn om Human Resources-gegevens te synchroniseren. Het bevat de volgende drie oplossingen.

| Unieke naam                | Weergavenaam                             |
|----------------------------|------------------------------------------|
| HCMCommon                  | HCM - Algemeen                               |
| msdyn_Dynamics365HCMMaps   | Entiteitstoewijzingen voor Dynamics 365 Human Resources |
| msdyn_Dynamics365HCMAnchor | Anker voor Dynamics 365 Human Resources      |

De volgende kaarten zijn beschikbaar in dit pakket.

| Finance and Operations-apps | Customer Engagement-apps         |
|-----------------------------|----------------------------------|
| Etnische afkomst              | cdm_ethnicorigins                |
| Compensatie functiepositie   | cdm_jobfunctions                 |
| Posities V2                | cdm_jobpositions                 |
| Functies                        | cdm_jobs                         |
| Compensatietaaktype       | cdm_jobtypes                     |
| Taalcodes              | cdm_languages                    |
| Positietype               | cdm_positiontypes                |
| Medewerkertoewijzingen voor positie | cdm_positionworkerassignmentmaps |
| Oorlogsveteraanstatus              | cdm_veteranstatuses              |
| Werknemer                      | cdm_workers                      |
| Aanstelling per bedrijf      | cdm_employments                  |

**Afhankelijkheidsgegevens**

Het Dual-write Human Resources-pakket is afhankelijk van het Dual-write Application Core-pakket. Daarom moet u het Dual-write Application Core-pakket installeren voordat u het Dual-write Human Resources-pakket installeert.

## <a name="dual-write-supply-chain"></a>Dual-write Supply Chain

Het Dual-write Supply Chain-pakket bevat de oplossingen en kaarten die nodig zijn om gegevens van Supply Chain Management te synchroniseren. Het bevat de volgende drie oplossingen.

| Unieke naam                                | Weergavenaam                                              |
|--------------------------------------------|-----------------------------------------------------------|
| Dynamics365SupplyChainExtended             | Dynamics 365 Supply Chain Extended                        |
| msdyn_Dynamics365SupplyChainExtendedMaps   | Uitgebreide entiteitstoewijzingen voor Dynamics 365 Supply Chain Management |
| msdyn_Dynamics365SupplyChainExtendedAnchor | Uitgebreid anker voor Dynamics 365 Supply Chain Management      |

De volgende kaarten zijn beschikbaar in dit pakket.

| Finance and Operations-apps                 | Customer Engagement-apps                      |
|---------------------------------------------|-----------------------------------------------|
| Eenheden                                       | uoms                                          |
| CDS-verkooporderkopteksten                     | salesorders                                   |
| CDS-verkooporderregels                       | salesorderdetails                             |
| CDS-verkoopoffertekoptekst                  | offertes                                        |
| Regels van CDS-verkoopofferte                   | quotedetails                                  |
| Door CDS vrijgegeven verschillende producten              | producten                                      |
| Magazijnzones                             | msdyn_warehousezones                          |
| Magazijnzonegroepen                       | msdyn_warehousezonegroups                     |
| Werkregels magazijn                        | msdyn_warehouseworklines                      |
| Werkkopteksten magazijn                      | msdyn_warehouseworkheaders                    |
| Magazijnen                                  | msdyn_warehouses                              |
| Voorraadgang                             | msdyn_warehouseaisles                         |
| Eenheidsomrekeningen                            | msdyn_unitofmeasureconversions                |
| Leveringsvoorwaarden                           | msdyn_termsofdeliveries                       |
| Leveringsmethoden                           | msdyn_shipvias                                |
| Stijlen van productmodellen                       | msdyn_sharedproductstyles                     |
| Verkoopfactuurregels V2                      | factuurdetails                                |
| Kopteksten van verkoopfacturen V2                    | facturen                                      |
| Afmetingen van productmodellen                        | msdyn_sharedproductsizes                      |
| Vrijgegeven producten V2                        | msdyn_sharedproductdetails                    |
| Configuraties van productmodellen               | msdyn_sharedproductconfigurations             |
| Kleuren van productmodellen                       | msdyn_sharedproductcolors                     |
| Oorsprongcodes van verkooporder                    | msdyn_salesorderorigins                       |
| Koptekst productontvangstbon                      | msdyn_purchaseorderreceipts                   |
| Productontvangstbonregel                        | msdyn_purchaseorderreceiptproducts            |
| Inkooporderkopteksten V2                   | msdyn_purchaseorders                          |
| Verwijderde entiteit CDS-inkooporderregel | msdyn_purchaseorderproducts                   |
| Entiteit voor CDS-inkooporderregels              | msdyn_purchaseorderproducts                   |
| Traceringsdimensiegroepen                   | msdyn_producttrackingdimensiongroups          |
| Stijlen                                      | msdyn_productstyles                           |
| Opslagdimensiegroepen                    | msdyn_productstoragedimensiongroups           |
| Productspecifieke eenheidsconversies           | msdyn_productspecificunitofmeasureconversions |
| Standaard orderinstellingen voor product V2           | msdyn_productspecificdefaultordersettings     |
| Afmetingen                                       | msdyn_productsizes                            |
| Productdimensiegroepen                    | msdyn_productdimensiongroups                  |
| Standaard orderinstellingen                      | msdyn_productdefaultordersettings             |
| Configuraties                              | msdyn_productconfigurations                   |
| Alle producten                                | msdyn_globalproducts                          |
| Kleuren                                      | msdyn_productcolors                           |
| Hiërarchierollen van productcategorieën            | msdyn_productcategoryhierarchyroles           |
| Hiërarchieën van productcategorieën                | msdyn_productcategoryhierarchies              |
| Toewijzingen van productcategorieën                | msdyn_productcategoryassignments              |
| Productcategorieën                          | msdyn_productcategories                       |
| Magazijnlocaties                         | msdyn_inventorylocations                      |
| CDS-voorraad voorhanden                            | msdyn_inventoryonhandentries                  |
| Productcategorieën                          | msdyn_productcategories                       |
| CDS-voorraad voorhanden                            | msdyn_inventoryonhandrequests                 |
| Geïdentificeerde streepjescodes voor productnummer           | msdyn_productbarcodes                         |
| Loyaliteitskaart                                | msdyn_loyaltycards                            |
| Beloningspunten voor loyaliteit                       | msdyn_loyaltyrewardpoints                     |
| Prijsklantgroepen                       | msdyn_pricecustomergroups                     |
| Vestigingen                                       | msdyn_operationalsites                        |
| Regels van CDS-verkoopofferte                   | quotedetails                                  |
| CDS-verkooporderregels                       | salesorderdetails                             |

**Afhankelijkheidsgegevens**

Het Dual-write Supply Chain-pakket is afhankelijk van de volgende drie pakketten. Daarom moet u deze pakketten installeren voordat u het Dual-write Supply Chain-pakket installeert.

- Dual-write Application Core-pakket
- Dual-write Finance-pakket
- Dual-write Human Resources-pakket

## <a name="dual-write-finance"></a>Dual-write Finance

Het Dual-write Finance-pakket bevat de oplossingen en kaarten die nodig zijn om Dynamics 365 Finance-gegevens te synchroniseren. Het bevat de volgende vier oplossingen.

| Unieke naam                            | Weergavenaam                               |
|----------------------------------------|-------------------------------------------|
| Dynamics365FinanceExtended             | Dynamics 365 Finance Extended             |
| msdyn_Dynamics365FinanceExtendedMaps   | Uitgebreide entiteitstoewijzingen voor Dynamics 365 Finance |
| FieldServiceCommon                     | Field Service Common                      |
| msdyn_Dynamics365FinanceExtendedAnchor | Uitgebreid anker voor Dynamics 365 Finance      |

De volgende kaarten zijn beschikbaar in dit pakket.

| Finance and Operations-apps             | Customer Engagement-apps        |
|-----------------------------------------|---------------------------------|
| Bronbelastinggroepen                  | msdyn_withholdingtaxgroups      |
| CDS-contactpersonen V2 (klant)              | contacten                        |
| CDS-contactpersonen V2 (leverancier)                | contacten                        |
| Klanten V3                            | contacten                        |
| Bronbelastingcodes                   | msdyn_withholdingtaxcodes       |
| Leveranciers V2                              | msdyn_vendors                   |
| Leveranciersbetalingsmethode                   | msdyn_vendorpaymentmethods      |
| Leveranciersgroepen                           | msdyn_vendorgroups              |
| Rekeningschema                       | msdyn_chartofaccountses         |
| Groepen van boekingen in btw-grootboek V2      | msdyn_taxpostinggroups          |
| Btw-groep voor artikel                    | msdyn_taxitemgroups             |
| Btw-groepen                        | msdyn_taxgroups                 |
| Entiteit btw-vrijstellingscode voor CDS        | msdyn_taxexemptcodes            |
| Klantengroepen                         | msdyn_customergroups            |
| Betalingsmethode van klant                 | msdyn_customerpaymentmethods    |
| Financiële dimensies                    | msdyn_dimensionattributes       |
| Btw-dienst                   | msdyn_taxauthorities            |
| Indeling van financiële dimensie              | msdyn_financialdimensionformats |
| Fiscale kalenderperiode                  | msdyn_fiscalcalendarperiods     |
| Integratie entiteit fiscale kalender      | msdyn_fiscalcalendars           |
| Integratie entiteit fiscaal kalenderjaar | msdyn_fiscalcalendaryears       |
| Betalingsvoorwaarden                        | msdyn_paymentterms              |
| Betalingsplanning                        | msdyn_paymentschedules          |
| Regels van betalingsschema                  | msdyn_paymentschedulelines      |
| Betalingsdagen CDS                        | msdyn_paymentdays               |
| Betalingsdagregels CDS V2                | msdyn_paymentdaylines           |
| Hoofdrekening                            | msdyn_mainaccounts              |
| Categorieën van hoofdrekening                 | msdyn_mainaccountcategories     |
| Ledger                                  | msdyn_ledgers                   |
| Klanten V3                            | rekeningen                        |

**Afhankelijkheidsgegevens**

Het Dual-write Finance-pakket is afhankelijk van het Dual-write Application Core-pakket. Daarom moet u het Dual-write Application Core-pakket installeren voordat u het Dual-write Finance-pakket installeert.

## <a name="dual-write-notes"></a>Dual-write Notes

Het Dual-write Notes-pakket bevat de oplossingen en kaarten die nodig zijn om gegevens van notities of aantekeningen te synchroniseren. Het bevat de volgende vier oplossingen.

| Unieke naam                  | Weergavenaam                   |
|------------------------------|--------------------------------|
| Dynamics365Notes             | Dynamics 365 Notes             |
| Dynamics365NotesExtended     | Dynamics 365 notes extended    |
| msdyn_Dynamics365NotesMaps   | Entiteitstoewijzingen voor Dynamics 365 Notes |
| msdyn_Dynamics365NotesAnchor | Anker voor Dynamics 365 Notes      |

De volgende kaarten zijn beschikbaar in dit pakket.

| Finance and Operations                     | Customer Engagement |
|--------------------------------------------|---------------------|
| Documentbijlagen van verkooporderkoptekst    | aantekeningen         |
| Klantbijlagen                       | aantekeningen         |
| Bijlagen van leveranciersdocument                | aantekeningen         |
| Documentbijlagen van inkooporderkoptekst | aantekeningen         |

**Afhankelijkheidsgegevens**

Het Dual-write Notes-pakket is afhankelijk van de volgende twee pakketten. Daarom moet u deze pakketten installeren voordat u het Dual-write Notes-pakket installeert.

- Dual-write Application Core-pakket
- Dual-write Finance-pakket

## <a name="dual-write-asset-management"></a>Dual-write Activabeheer

Het Dual-write Activabeheer-pakket bevat de oplossingen en kaarten die nodig zijn om activagegevens van Supply Chain Management of Dynamics 365 Field Service te synchroniseren. Het bevat de volgende vier oplossingen.

| Unieke naam                          | Weergavenaam                              |
|--------------------------------------|-------------------------------------------|
| Dynamics365AssetManagement           | Dynamics 365 Activabeheer             |
| Dynamics365AssetManagementApp        | Dynamics 365-app voor activabeheer          |
| msdyn_DualWriteAssetManagementMaps   | Entiteitstoewijzingen voor Dynamics 365 Activabeheer |
| msdyn_DualWriteAssetManagementAnchor | Anker voor Dynamics 365 Activabeheer      |

De volgende kaarten zijn beschikbaar in dit pakket.

| Finance and Operations-apps                           | Customer Engagement-apps                |
|-------------------------------------------------------|-----------------------------------------|
| Garantie voor activabeheer                             | msdyn_warranties                        |
| Modellen voor activabeheer                               | msdyn_models                            |
| Fabrikanten voor activabeheer                        | msdyn_manufacturers                     |
| Functionele locatietypen voor activabeheer            | msdyn_functionallocationtypes           |
| Functionele locaties voor activabeheer                 | msdyn_functionallocations               |
| Levenscyclusstatussen voor functionele locaties voor activabeheer | msdyn_functionallocationlifecyclestates |
| Levenscyclusmodellen voor functionele locaties voor activabeheer | msdyn_functionallocationlifecyclemodels |
| Activa voor activabeheer                               | msdyn_customerassets                    |
| Activatypen voor activabeheer                          | msdyn_customerassetcategories           |
| Statussen van levenscyclus van activa voor activabeheer               | msdyn_assetlifecyclestates              |
| Levenscyclusmodellen van activa voor activabeheer               | msdyn_assetlifecyclemodels              |

**Afhankelijkheidsgegevens**

Het Dual-write Activabeheer-pakket is afhankelijk van het Dual-write Application Core-pakket. Daarom moet u het Dual-write Application Core-pakket installeren voordat u het Dual-write Activabeheer-pakket installeert.

## <a name="packages-required-for-project-operations"></a>Pakketten die vereist zijn voor Project Operations
Project Operations is afhankelijk van de volgende pakketten. Daarom moet u deze pakketten installeren voordat u Project Operations installeert.

- Dual-write Application Core-pakket
- Dual-write Finance-pakket
- Dual-write Supply Chain-pakket
- Dual-write Activabeheer-pakket
- Dual-write Human Resources-pakket
