---
title: Overzicht met productinformatie
description: Dit onderwerp biedt informatie over productgegevensbeheer. Productgegevensbeheer werkt met een gedeelde productdefinitie, categorisatie en id's in alle rechtspersonen en specifieke configuraties van een product, zodat deze past in de bedrijfsprocessen.
author: cvocph
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductListPage, EcoResProductVariantMaintainWorkspace
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: 
ms.author: cvocph
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: db8a9666518b58b6b32bb4a14933095dd9416aa0
ms.contentlocale: nl-nl
ms.lasthandoff: 06/13/2017

---

# <a name="product-information-overview"></a>Overzicht met productinformatie

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]

Dit onderwerp biedt informatie over productgegevensbeheer. Productgegevensbeheer werkt met een gedeelde productdefinitie, categorisatie en id's in alle rechtspersonen en specifieke configuraties van een product, zodat deze past in de bedrijfsprocessen. 

Productgegevens vormen de basis van toepassingen voor supply chain en retail in alle bedrijfstakken. Het verwijst naar processen en technologieën die gericht zijn op centraal beheer van informatie over producten (bijvoorbeeld in de toeleveringsketens). Het is essentieel dat gedeelde definities, documentatie, kenmerken en id's van producten worden gebruikt. In de verschillende modules van een oplossing zijn productspecifieke informatie en configuratie vereist om de bedrijfsprocessen te beheren die zijn gerelateerd aan specifieke producten, productfamilies of productcategorieën.

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

U kunt de productdefinitie maken in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition. U kunt hem ook importeren vanuit systemen voor productlevenscyclusbeheer (PLM), productgegevensbeheer (PDM) of productgegevensbeheer. Als u meer dan één exemplaar van Finance and Operations gebruikt, wordt één exemplaar meestal gebruikt als de master van de productgegevens voor alle andere exemplaren. Deze benadering wordt ondersteund door een groot aantal gegevensentiteiten, die het exporteren en importeren van productdefinitiegegevens van het ene exemplaar naar het andere ondersteunen.

Ter ondersteuning van de verdeling van productgegevens naar veel exemplaren, kunt u in Finance and Operations de Common Date Service gebruiken. De productdefinities kunnen worden geëxporteerd vanuit een exemplaar van Finance and Operations naar de Common Data Service. De productdefinities kunnen vervolgens worden gebruikt om andere zakelijke toepassingen in te richten met productgegevens, zoals Microsoft Dynamics 365 for Sales.

Houd er rekening mee dat in dynamische en flexibele organisaties productgegevens elke dag wijzigen. Correcte en actuele productgegevens onderhouden is daarom op zich al een kritisch bedrijfsproces.

## <a name="product-masters-and-product-variants"></a>Productmodellen en productvarianten

In een flexibele wereld, waarin producten snel moeten worden aangepast aan de wensen van klanten, geven productdefinities een reeks producten op in plaats van afzonderlijke producten. In Microsoft Dynamics 365 for Finance and Operations worden die algemene producten aangeduid als *productmodellen*. Productmodellen bevatten de definitie en de regels die aangeven hoe afzonderlijke producten worden beschreven en zich gedragen in bedrijfsprocessen. Op basis van deze definities kunnen verschillende producten worden gegenereerd. Deze verschillende producten worden ook *productvarianten* genoemd.

In Finance and Operations is een productmodel gekoppeld aan een productdimensiegroep en een configuratietechnologie om de bedrijfsregels op te geven. De productdimensies (Kleur, Grootte, Stijl en Configuratie) zijn een specifieke reeks kenmerken die in de applicatie kunnen worden gebruikt om specifieke gedrag van de gerelateerde producten te definiëren en bij te houden. Met deze dimensies kunnen gebruikers ook zoeken naar de producten en deze identificeren.

## <a name="configuration-technologies"></a>Configuratietechnologieën

U kunt kiezen uit drie configuratietechnologieën:

- De vooraf gedefinieerde varianten worden gedefinieerd door vooraf gedefinieerde productdimensies. De variantdefinitie omvat de definitie van een specifieke geldige combinatie van dimensies, zoals kleur, stijl en grootte. Elke combinatie levert een verschillende productvariant op.
- De op dimensies gebaseerde configuratie wordt meestal gebruikt in productiescenario's en stelt u in staat om de configuratiedimensie te gebruiken in de definitie van de stuklijsten. Nadat een specifieke configuratie is geselecteerd, gebruikt het systeem de subset van stuklijstregels die geldig zijn voor de desbetreffende configuratie voor planning en productie. Dit concept wordt ook wel *algemene stuklijst* genoemd, omdat één gedeelde stuklijst wordt gebruikt voor alle configuraties van een product.
- De op beperkingen gebaseerde configuratie gebruikt een productconfiguratiemodel om alle mogelijke kenmerken en onderdelen te beschrijven, die nodig zijn om alle mogelijke varianten van een product in één model te beschrijven. De beperkingen van combinaties van kenmerken kunnen via reguliere expressies of beperkingen op basis van een tabel worden beschreven. Configuratiemodellen en configurators worden in productinformatiebeheer steeds belangrijker en worden toegepast in alle bedrijfstakken.

Wanneer u de implementatie van Finance and Operations plant, is het belangrijk dat u de juiste configuratietechnologie voor een bedrijfsproces kiest. Een product kan niet na invoering van het ene model worden geconverteerd naar een andere.

## <a name="product-variant-model-definition-workspace"></a>Het werkgebied Definitie van productvariantmodel

Het werkgebied **Definitie van productvariantmodel** geeft een overzicht van de productmodellen. Hier ziet u ook de status van de vrijgave van modellen en gerelateerde varianten voor specifieke rechtspersonen.

## <a name="released-products"></a>Vrijgegeven producten

De producten die zijn vrijgegeven aan een specifieke rechtspersoon worden ook aangeduid als *vrijgegeven producten*. Producten kunnen in bulk worden vrijgegeven voor één rechtspersoon of voor vele rechtspersonen tegelijk. Omdat verschillende eigenschappen en kenmerken van de producten mogelijk moet worden toegevoegd per rechtspersoon, kunt u in het werkgebied **Vrijgegeven productonderhoud** de onlangs vrijgegeven producten in iedere rechtspersoon controleren en voltooien, of in de suborganisaties van een rechtspersoon.

### <a name="released-product-maintenance-workspace"></a>Het werkgebied Vrijgegeven productonderhoud

U kunt het werkgebied **Vrijgegeven productonderhoud** configureren vanuit de menuopdracht **Mijn werkgebied configureren**. Selecteer een categoriehiërarchie en categorie waarop u het werkgebied wilt filteren Om de relevante productgegevens in het werkgebied aan te passen, kunt u ook definiëren (in dagen) de timefences voor **Onlangs vrijgegeven producten** en **Gestopte vrijgegeven producten**.

Het werkgebied bestaat uit een overzicht van de tegels en twee lijsten. De lijst **Openstaande aanvragen** laat aanvragen voor productwijzigingen zien, die producten bevatten uit de geselecteerde productcategoriehiërarchie die niet zijn voltooid en afgesloten. De lijst **Onlangs vrijgegeven** bevat producten die zijn vrijgegeven binnen de timefence die is ingesteld in de werkgebiedconfiguratie. Validatie wordt uitgevoerd voor elk artikel in de lijst en de validatiestatus wordt weergegeven. Deze status kan aangeven dat de vereiste configuraties voor de rechtspersoon niet zijn voltooid. Vanuit de lijst hebt u rechtstreeks toegang tot de pagina's **Vrijgegeven productdetails**, **Onderhoud productkenmerken**, **Onderhoud productcategorie**, **Standaard orderinstellingen** en **Tekstvertalingen** waarmee u de vereiste configuratie van het product kunt voltooien.

### <a name="manually-creating-a-new-released-product"></a>Handmatig een nieuw vrijgegeven product maken

U kunt handmatig een vrijgegeven product maken in een enkelvoudige run, afhankelijk van de bedrijfsprocessen van de organisatie en eventuele regels die bepalen of deze functie moet worden gebruikt. Deze functie maakt een nieuw product en geeft dit automatisch vrij naar de huidige rechtspersoon. Om een nieuw product te maken, klikt u op **Vrijgegeven producten** in het werkgebied **Vrijgegeven productonderhoud** of op de lijstpagina **Vrijgegeven product**.

