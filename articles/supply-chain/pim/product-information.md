---
title: Overzicht met productinformatie
description: Dit onderwerp biedt informatie over productgegevensbeheer. Productgegevensbeheer werkt met een gedeelde productdefinitie, categorisatie en id's in alle rechtspersonen en specifieke configuraties van een product, zodat deze past in de bedrijfsprocessen.
author: t-benebo
ms.date: 06/01/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductListPage, EcoResProductVariantMaintainWorkspace, EcoResProductVariantPerCompanyImagePart, EcoResProductRelationType,EcoResProductAvailabilityPart,  EcoResProductReleasedSelect, EcoResProductLookup, EcoResProductVariantsPendingReleaseFormPart, EcoResProductSearchLookup, EcoResProductNumberRename, EcoResDimensionBasedConfigWorkspace, EcoResProductVariantImagePart, EcoResProductImagePart, EcoResProductVariantsPerCompanyPart, InventItemIdLookupByDefaultOrderSetting, EcoResProductReleaseSessions, EcoResProductVariantMaintainWorkspaceConfiguration, EcoResProductProcessManufacturingWorkspaceConfiguration, EcoResProductMasterVariantsPart, EcoResProductDiscreteManufacturingWorkspaceConfiguration, EcoResProductVariantAvailabilityPart, EcoResProductInformationFactBox, EcoResProductLookupTest, EcoResProductImageTest, EcoResProductReleasedRecentlyCreatedFormPart, EcoResPhysicalProductDimensions, PdsMRCRegulatedListItem, EcoResProductAvailabilityPart, PdsMRCRestrictionList, InventItemIdLookupAllocationId, EcoResProductAvailability, EcoResProductEntityAttributeTableFieldAssociation, EcoResProductImagePart, EcoResProductRelation, EcoResProductReleaseAddProduct, EcoResProductPerCompanyListPage, EcoResProductParameters, PdsMRCRestrictedItemByCountryState, EngChgCasePreview, InventTablePreview, PdsMRCItemDetails, EngChgCaseAssociate, PdsMRCCustomerHistory, PdsMRCVendorHistory, PdsMRCRestrictedCountryStateByItem, InventItemIdGroupLookup, InventLocationLookup, PdsMRCValidityIntervalbyCountry, PdsMRCValidityIntervalbyCountry, PdsMRCEventTracker, PdsMRCReportingCountry, PdsMRCDocument, PdsMRCReportingList, PdsMRCItemCAS, GraphicsTestForm, EngChgPicklist
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bf814ec7c76ff2a8fd6bb4f7bbf8aec109465e34
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2022
ms.locfileid: "7984315"
---
# <a name="product-information-overview"></a>Overzicht met productinformatie

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dit onderwerp biedt informatie over productgegevensbeheer. Productgegevensbeheer werkt met een gedeelde productdefinitie, categorisatie en id's in alle rechtspersonen en specifieke configuraties van een product, zodat deze past in de bedrijfsprocessen. 

Productgegevens vormen de basis van toepassingen voor supply chain en commerce in alle bedrijfstakken. Het verwijst naar processen en technologieën die gericht zijn op centraal beheer van informatie over producten (bijvoorbeeld in de toeleveringsketens). Het is essentieel dat gedeelde definities, documentatie, kenmerken en id's van producten worden gebruikt. In de verschillende modules van een oplossing zijn productspecifieke informatie en configuratie vereist om de bedrijfsprocessen te beheren die zijn gerelateerd aan specifieke producten, productfamilies of productcategorieën.

## <a name="product-definition"></a>Productdefinitie

Een product wordt voornamelijk gedefinieerd door een productnummer, -naam en -beschrijving. Andere gegevens zijn echter ook vereist om een product of service te beschrijven:

- Producttype: artikel of service
- Subtype product: verschillende producten of productmodellen
- Definitie van het productvariantmodel:

     - productdimensies en dimensiegroepen
     - Productnomenclatuur
     - Productconfiguratiemodellen

- Koppeling van het product aan een of meer categorieën
- Definitie van de kenmerken van het product en de categorie
- Productafbeeldingen
- Bijlagen
- Maateenheden en gerelateerde conversies
- Vertalingen voor alle namen en beschrijvingen

## <a name="distribution-export-and-import-of-product-data"></a>Distributie, export en import van productgegevens

De productdefinitie kan worden gemaakt in Supply Chain Management. U kunt hem ook importeren vanuit systemen voor productlevenscyclusbeheer (PLM), productgegevensbeheer (PDM) of productgegevensbeheer. Als u meer dan één exemplaar van Supply Chain Management gebruikt, wordt één exemplaar meestal gebruikt als de master van de productgegevens voor alle andere exemplaren. Deze benadering wordt ondersteund door een groot aantal gegevensentiteiten, die het exporteren en importeren van productdefinitiegegevens van het ene exemplaar naar het andere ondersteunen.

Ter ondersteuning van de verdeling van productgegevens naar veel exemplaren, kunt u in Supply Chain Management de Microsoft Dataverse gebruiken. De productdefinities kunnen worden geëxporteerd vanuit een exemplaar van Supply Chain Management naar de Microsoft Dataverse. De productdefinities kunnen vervolgens worden gebruikt om andere zakelijke toepassingen in te richten met productgegevens, zoals Dynamics 365 Sales.

Houd er rekening mee dat in dynamische en flexibele organisaties productgegevens elke dag wijzigen. Correcte en actuele productgegevens onderhouden is daarom op zich al een kritisch bedrijfsproces.

## <a name="product-masters-and-product-variants"></a>Productmodellen en productvarianten

In een flexibele wereld, waarin producten snel moeten worden aangepast aan de wensen van klanten, geven productdefinities een reeks producten op in plaats van afzonderlijke producten. In Supply Chain Management worden die algemene producten *productmodellen* genoemd. Productmodellen bevatten de definitie en de regels die aangeven hoe afzonderlijke producten worden beschreven en zich gedragen in bedrijfsprocessen. Op basis van deze definities kunnen verschillende producten worden gegenereerd. Deze verschillende producten worden ook *productvarianten* genoemd.

Een productmodel is gekoppeld aan een productdimensiegroep en een configuratietechnologie om de bedrijfsregels op te geven. De productdimensies (Kleur, Grootte, Stijl en Configuratie) zijn een specifieke reeks kenmerken die in de applicatie kunnen worden gebruikt om specifieke gedrag van de gerelateerde producten te definiëren en bij te houden. Met deze dimensies kunnen gebruikers ook zoeken naar de producten en deze identificeren.

## <a name="configuration-technologies"></a>Configuratietechnologieën

U kunt kiezen uit drie configuratietechnologieën:

- De vooraf gedefinieerde varianten worden gedefinieerd door vooraf gedefinieerde productdimensies. De variantdefinitie omvat de definitie van een specifieke geldige combinatie van dimensies, zoals kleur, stijl en grootte. Elke combinatie levert een verschillende productvariant op.
- De op dimensies gebaseerde configuratie wordt meestal gebruikt in productiescenario's en stelt u in staat om de configuratiedimensie te gebruiken in de definitie van de stuklijsten. Nadat een specifieke configuratie is geselecteerd, gebruikt het systeem de subset van stuklijstregels die geldig zijn voor de desbetreffende configuratie voor planning en productie. Dit concept wordt ook wel *algemene stuklijst* genoemd, omdat één gedeelde stuklijst wordt gebruikt voor alle configuraties van een product.
- De op beperkingen gebaseerde configuratie gebruikt een productconfiguratiemodel om alle mogelijke kenmerken en onderdelen te beschrijven, die nodig zijn om alle mogelijke varianten van een product in één model te beschrijven. De beperkingen van combinaties van kenmerken kunnen via reguliere expressies of beperkingen op basis van een tabel worden beschreven. Configuratiemodellen en configurators worden in productinformatiebeheer steeds belangrijker en worden toegepast in alle bedrijfstakken.

Wanneer u de implementatie van Supply Chain Management plant, is het belangrijk dat u de juiste configuratietechnologie voor een bedrijfsproces kiest. Een product kan niet na invoering van het ene model worden geconverteerd naar een andere.

## <a name="product-variant-model-definition-workspace"></a>Het werkgebied Definitie van productvariantmodel

Het werkgebied **Definitie van productvariantmodel** geeft een overzicht van de productmodellen. Hier ziet u ook de status van de vrijgave van modellen en gerelateerde varianten voor specifieke rechtspersonen.

## <a name="released-products"></a>Vrijgegeven producten

De producten die zijn vrijgegeven aan een specifieke rechtspersoon worden ook aangeduid als *vrijgegeven producten*. Producten kunnen in bulk worden vrijgegeven voor één rechtspersoon of voor vele rechtspersonen tegelijk. Omdat verschillende eigenschappen en kenmerken van de producten mogelijk moet worden toegevoegd per rechtspersoon, kunt u in het werkgebied **Vrijgegeven productonderhoud** de onlangs vrijgegeven producten in iedere rechtspersoon controleren en voltooien, of in de suborganisaties van een rechtspersoon.

### <a name="released-product-maintenance-workspace"></a>Het werkgebied Vrijgegeven productonderhoud

U kunt het werkgebied **Vrijgegeven productonderhoud** configureren vanuit de menuopdracht **Mijn werkgebied configureren**. Selecteer een categoriehiërarchie en categorie waarop u het werkgebied wilt filteren Om de relevante productgegevens in het werkgebied aan te passen, kunt u ook definiëren (in dagen) de timefences voor **Onlangs vrijgegeven producten** en **Gestopte vrijgegeven producten**.

Het werkgebied bestaat uit een overzicht van de tegels en twee lijsten. De lijst **Openstaande aanvragen** laat aanvragen voor productwijzigingen zien, die producten bevatten uit de geselecteerde productcategoriehiërarchie die niet zijn voltooid en afgesloten. De lijst **Onlangs vrijgegeven** bevat producten die zijn vrijgegeven binnen de timefence die is ingesteld in de werkgebiedconfiguratie. Validatie wordt uitgevoerd voor elk artikel in de lijst en de validatiestatus wordt weergegeven. Deze status kan aangeven dat de vereiste configuraties voor de rechtspersoon niet zijn voltooid. Vanuit de lijst hebt u rechtstreeks toegang tot de pagina's **Vrijgegeven productdetails**, **Onderhoud productkenmerken**, **Onderhoud productcategorie**, **Standaard orderinstellingen** en **Tekstvertalingen** waarmee u de vereiste configuratie van het product kunt voltooien.

### <a name="manually-creating-a-new-released-product"></a>Handmatig een nieuw vrijgegeven product maken

U kunt handmatig een vrijgegeven product maken in een enkelvoudige run, afhankelijk van de bedrijfsprocessen van de organisatie en eventuele regels die bepalen of deze functie moet worden gebruikt. Deze functie maakt een nieuw product en geeft dit automatisch vrij naar de huidige rechtspersoon. Om een nieuw product te maken, klikt u op **Vrijgegeven producten** in het werkgebied **Vrijgegeven productonderhoud** of op de lijstpagina **Vrijgegeven product**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]