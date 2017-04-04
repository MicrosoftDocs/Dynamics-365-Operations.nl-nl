---
title: Nummer nomenclature van product
description: In dit onderwerp wordt beschreven hoe kunt u een product number nomenclature ingesteld ter vervanging van de vaste getalnotatie is [product master - configuratie - grootte - kleur - stijl], met een doelgerichte indeling waarin de hoofdplanning productnummer, actieve productdimensies en scheidingstekens tekst van uw keuze. U kunt ook een nomenclature maken om configuraties aan te geven die worden gemaakt door de op beperkingen gebaseerde productconfigurator. Deze nomenclaturen kunnen kenmerken van uw keuze bevatten.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 220104
ms.assetid: 31c9efb4-b5f6-4af3-b884-8f1e128469bd
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 58afcd62e7ef317e624fd26d198c2606bf53e6a5
ms.lasthandoff: 03/31/2017


---

# <a name="product-number-nomenclature"></a>Nummer nomenclature van product

In dit onderwerp wordt beschreven hoe kunt u een product number nomenclature ingesteld ter vervanging van de vaste getalnotatie is [product master - configuratie - grootte - kleur - stijl], met een doelgerichte indeling waarin de hoofdplanning productnummer, actieve productdimensies en scheidingstekens tekst van uw keuze. U kunt ook een nomenclature maken om configuraties aan te geven die worden gemaakt door de op beperkingen gebaseerde productconfigurator. Deze nomenclaturen kunnen kenmerken van uw keuze bevatten.

Met de nieuwe nomenclatuur van productvariantnummers kunt u segmenten in uw productvariant-id's opnemen. Deze segmenten kunnen het productmodelnummer, de productdimensies, de nummerreeksen, de tekstconstantes en de kenmerken omvatten. Met deze functionaliteit kunt u snel een specifieke productvariant vinden wanneer u een verkooporder of een inkooporder maakt.

## <a name="nomenclature-of-predefined-product-variants"></a>Nomenclatuur met vooraf gedefinieerde productvarianten
De productvarianten worden gegenereerd voor productmodellen volgens drie configuratietechnologieën:

-   Vooraf gedefinieerde varianten
-   Op basis van beperkingen
-   Op basis van dimensies

Elke productvariant heeft een nummer en in de nomenclatuur van de productvariant-id's kunt u de segmenten selecteren die in elk productvariantnummer worden opgenomen. U kunt de volgende segmenten selecteren op de pagina **Productnomenclatuur**.

-   Nummer van basismaster
-   Nummerreekswaarde
-   Tekstconstante
-   Productdimensies
    -   Configuratie
    -   Kleur
    -   Grootte
    -   Opmaakmodel

Nadat een productvariant-id gedefinieerd, kan deze aan een productdimensiegroep worden gekoppeld. Vervolgens worden aan alle productmodellen die naar deze productdimensiegroep verwijzen, productvariantnummers toegewezen volgens de nomenclatuur. Het is ook mogelijk om een productvariantnomenclatuur rechtstreeks toe te wijzen aan een productmodel. In dat geval worden aan de productvarianten die bij dit model horen, productvariantnummers toegewezen volgens de nomenclatuur.

### <a name="example"></a>Voorbeeld

Een t-shirt (TS1234) wordt geproduceerd in 3 verschillende maten (S, M, L), 4 kleuren (rood groen, geel, blauw) en 2 stijlen (Polo, V) wat in totaal 24 mogelijke productvarianten geeft. Een nomenclatuur met productvariant-id's wordt gemaakt met de volgende segmenten:

1.  Nummer van basismaster
2.  Tekstconstante: '-'
3.  Kleur
4.  Tekstconstante: '-'
5.  Grootte
6.  Tekstconstante: '-'
7.  Opmaakmodel

Het productvariantnummer voor de rode Polo in S is: TS1234-rood-small-polo.

## <a name="nomenclature-of-constraintbased-configurations"></a>Nomenclature van constraintbased-configuraties
Voor op beperkingen gebaseerde configuraties, kan een specifieke nomenclatuur voor de configuratie van product-dimensie worden opgebouwd. U kunt de volgende segmenten selecteren op de pagina **Productnomenclatuur**.

-   Nummerreekswaarde
-   Tekstconstante
-   Kenmerkwaarde 

Elke component in een productconfiguratiemodel kan een eigen configuratienomenclatuur hebben. Alleen kenmerken die bij de component horen, worden gebruikt. De kenmerken van subcomponenten of gebruikersvereisten zijn niet beschikbaar.

### <a name="example"></a>Voorbeeld

Een productconfiguratiemodel heeft een hoofdcomponent met twee kenmerken.

-   Materiaal (plastic, hout, staal)
-   Lengte (10... 100)

Een configuratienomenclatuur wordt gedefinieerd met de volgende segmenten:

1.  Kenmerkwaarde: materiaal
2.  Tekstconstante: 'AAA'
3.  Kenmerkwaarde: lengte

De configuratie-id voor het materiaal hout met een lengte van 78 is als volgt: WoodAAA78.

## <a name="nomenclature-of-dimensionbased-configurations"></a>Nomenclature van dimensionbased-configuraties
Voor op dimensies gebaseerde configuraties, kan een specifieke nomenclatuur voor de configuratie van product-dimensie worden opgebouwd. U kunt de volgende segmenten selecteren op de pagina **Productnomenclatuur**.

-   Nummerreekswaarde
-   Tekstconstante
-   Configuratiegroepitem

Een configuratienomenclatuur kan worden gedefinieerd voor een stuklijst (BOM).

### <a name="example"></a>Voorbeeld

Een stuklijst heeft 4 stuklijstregels die in 2 configuratiegroepen worden verdeeld.

-   Stuklijstregel: M0007, standaardbehuizing
    -   Configuratiegroep: behuizing
-   Stuklijstregel: M0008, geavanceerde behuizing
    -   Configuratiegroep: behuizing
-   Stuklijstregel: M0021, voorgrill van stof
    -   Configuratiegroep: Voorgrill
-   Stuklijstregel: M0022, metalen voorgrill
    -   Configuratiegroep: Voorgrill

Een configuratienomenclatuur wordt gedefinieerd met de volgende segmenten:

1.  Configuratiegroep: behuizing
2.  Tekstconstante: '&'
3.  Configuratiegroep: Voorgrill

De configuratie-id voor een standaardbehuizing met een voorgrill van stof is: M0007&M0021.

## <a name="nomenclature-of-a-combination-of-product-variants-and-configurations"></a>Nomenclatuur van een combinatie van productvarianten en configuraties
Als u een op beperkingen of dimensies gebaseerde configuratietechnologie gebruikt om productvarianten voor een productmodel te configureren, kunnen de productvarianten productvariantnummers krijgen waarin de nomenclatuur van de configuratiedimensie is opgenomen. Volg deze stappen om varianten te configureren:

1.  Definieer een nomenclatuur van het productvariantnummer die de configuratiedimensie omvat op de pagina **Productnomenclatuur**.
2.  Wijs deze nomenclatuur toe aan een productdimensiegroep met de configuratiedimensie.
3.  Definieer een configuratienomenclatuur voor de componenten of de stuklijsten die voor het configureren van de productvarianten worden gebruikt.

### <a name="example-for-constraint-based-configurations"></a>Voorbeeld van op beperkingen gebaseerde configuraties

In dit voorbeeld kunt u een nomenclatuur van het productvariantnummer gebruiken die de volgende segmenten bevat:

1.  Nummer van basismaster
2.  Tekstconstante '\_'
3.  Configuratie

De configuratienomenclatuur kan bestaan uit de volgende segmenten:

1.  Kenmerkwaarde: materiaal
2.  Tekstconstante: 'AAA'
3.  Kenmerkwaarde: lengte

U kunt de volgende waarden voor segmenten invoeren:

-   Productmodelnummer = M0099
-   Materiaal = plastic
-   Lengte = 12

De variantcode van het product zal worden: M0099\_PlasticAAA12.

### <a name="example-for-dimension-based-configurations"></a>Voorbeeld van op dimensies gebaseerde configuraties

In dit voorbeeld kunt u een nomenclatuur van het productvariantnummer gebruiken die de volgende segmenten bevat:

1.  Nummer van basismaster
2.  Tekstconstante '//'
3.  Configuratie

De configuratienomenclatuur kan bestaan uit de volgende segmenten:

1.  Configuratiegroep: behuizing
2.  Tekstconstante: '&'
3.  Configuratiegroep: Voorgrill

U kunt de volgende waarden voor segmenten invoeren:

-   Productmodelnummer = D0123
-   Behuizing = M0008
-   Voorgrill = M0022

Het productvariantnummer wordt: D0123//M0008&M0022.

## <a name="numbering-conflicts"></a>Nummeringsconflicten
Het is mogelijk om een nomenclatuur voor productvariantnummers in te stellen die niet in unieke productvariantnummers resulteert. Dit kan bijvoorbeeld gebeuren als een actieve productdimensie niet is opgenomen in de nomenclatuur voor een productmodel dat de vooraf gedefinieerde technologie voor variantconfiguratie gebruikt. De conflicten worden anders behandeld voor de verschillende configuratietechnologieën.

### <a name="predefined-variants"></a>Vooraf gedefinieerde varianten

Een fout gebeurt als u handmatig of automatisch productvarianten probeert te genereren waarbij een of meerdere eindigen met hetzelfde productvariantnummer. Om dit te voorkomen moet u alle actieve productdimensies in de productdimensiegroep gebruiken of een nummerreeks bevatten opnemen om ervoor te zorgen dat de productvariantnummers uniek zijn.

### <a name="constraint-based-configurations"></a>Op beperkingen gebaseerde configuraties

Afhankelijk van de nomenclatuur kan het systeem proberen een niet-uniek productvariantnummer aan een configuratie toe te wijzen. In dit geval wordt het systeem gebruikt de nummerreeks voor de configuratiedimensie de variant van het productnummer in plaats daarvan. Als dit gebeurt, ontvangt u een waarschuwing. Om dit te voorkomen kunt u voldoende unieke kenmerken in de nomenclatuur opnemen en ervoor zorgen dat de optie **Opnieuw gebruiken** voor de component is ingeschakeld.

### <a name="dimension-based-configurations"></a>Op dimensie gebaseerde configuraties

Het configuratieproces bevat een stap waarin het systeem een configuratiewaarde volgens de nomenclatuur voorstelt. In deze stap kunt u de configuratiewaarde handmatig wijzigen. Wanneer u de configuratie opslaat, controleert het systeem of de configuratiewaarde uniek is. Als dat niet het geval is, wordt er een foutbericht weergegeven. U moet een unieke configuratiewaarde invoeren om de configuratie te slaan.



<a name="see-also"></a>Zie ook
--------

[Maken van een product number nomenclature voor vooraf gedefinieerde productvarianten (taak guide)](http://ax.help.dynamics.com/en/wiki/create-a-product-number-nomenclature-for-predefined-product-variants/)

[Maken van een product number nomenclature voor geconfigureerde productvarianten (taak guide)](http://ax.help.dynamics.com/en/wiki/create-a-product-number-nomenclature-for-configured-product-variants/)


