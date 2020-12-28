---
title: Nomenclatuur van productvariantnummers en -namen
description: In dit onderwerp wordt beschreven hoe u een productnummernomenclatuur instelt om de vaste indeling [productmodelnummer - configuratie - maat - kleur - stijl] te vervangen.
author: roxanadiaconu
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 90c01e4281246d890ef888c56ca137f83e83741c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425213"
---
# <a name="nomenclature-of-product-variant-numbers-and-names"></a>Nomenclatuur van productvariantnummers en -namen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een productnummernomenclatuur instelt om de vaste indeling [productmodelnummer - configuratie - maat - kleur - stijl] te vervangen. De nieuwe nomenclatuur heeft een beoogde indeling die het productmodelnummer, de actieve productdimensies en tekstscheidingstekens van uw keuze bevat. U kunt ook een nomenclatuur maken voor productnamen. Ten slotte kunt u een nomenclatuur maken om configuraties te identificeren die worden gemaakt door de op beperkingen gebaseerde productconfigurator. Deze nomenclaturen kunnen kenmerken van uw keuze bevatten.

Met de nieuwe nomenclaturen voor productvariantnummers en productvariantnamen kunt u segmenten in de id's opnemen voor productvarianten. Deze segmenten kunnen productmodelnummer en -naam, productdimensie-id's en -namen, nummerreeksen, tekstconstanten en kenmerken omvatten. Met deze functionaliteit kunt u snel een specifieke productvariant vinden wanneer u een verkooporder of een inkooporder maakt. U maakt nomenclaturen voor zowel productvariantnummers als productvariantnamen met behulp van de pagina **Productnomenclatuur**. Als u deze pagina wilt openen, klikt u op **Productgegevensbeheer** &gt; **Instellen**.

## <a name="nomenclature-of-predefined-product-variants"></a>Nomenclatuur met vooraf gedefinieerde productvarianten
De productvarianten worden gegenereerd voor productmodellen volgens drie configuratietechnologieën:

-   Vooraf gedefinieerde varianten
-   Op basis van beperkingen
-   Op basis van dimensies

Elke productvariant heeft een nummer en een naam en in de nomenclatuur van de productvariant-id's kunt u de segmenten selecteren die in elk productvariantnummer of -naam worden opgenomen. U kunt de volgende segmenten selecteren op de pagina **Productnomenclatuur**:

-   Nummer van basismaster
-   Naam van productmodel
-   Nummerreekswaarde
-   Tekstconstante
-   Productdimensies
    -   Configuratie-id of -naam
    -   Kleur-id of -naam
    -   Maat-id of -naam
    -   Stijl-id of -naam

Nadat een productvariant-id hebt gedefinieerd, kunt u deze koppelen aan een productdimensiegroep. Aan alle productmodellen die verwijzen naar deze productdimensiegroep, worden vervolgens productvariantnummers toegewezen op basis van de nomenclatuur. Nomenclaturen van productvariantnamen kunnen echter niet worden gekoppeld aan productdimensiegroepen. U kunt ook een nomenclatuur voor productvariant-id's direct aan een productmodel toewijzen. In dit geval worden aan de productvarianten die behoren tot het productmodel, productvariantnummers en -namen toegewezen volgens de nomenclaturen.

### <a name="example"></a>Voorbeeld

Een T-shirt (TS1234) wordt geproduceerd in drie maten (S, M, L), vier kleuren (rood, groen, blauw, geel) en twee stijlen (Polo, V). Daarom zijn 24 productvarianten mogelijk (= 3 × 4 × 2). U maakt een productvariantnummernomenclatuur met de volgende segmenten:

1.  Nummer van basismaster
2.  Tekstconstante: "-"
3.  Kleur
4.  Tekstconstante: "-"
5.  Grootte
6.  Tekstconstante: "-"
7.  Opmaakmodel

In dit geval is het productvariantnummer voor een rood, klein polo T-shirt TS1234-Rood-Klein-Polo.

## <a name="nomenclature-of-constraint-based-configurations"></a>Nomenclatuur met op beperkingen gebaseerde configuraties
Voor op beperkingen gebaseerde configuraties kunt u een specifieke nomenclatuur maken voor de configuratieproductdimensie. U kunt de volgende segmenten selecteren op de pagina **Productnomenclatuur**:

-   Nummerreekswaarde
-   Tekstconstante
-   Kenmerkwaarde

Elke component in een productconfiguratiemodel kan een eigen configuratienomenclatuur hebben. Alleen kenmerken die bij de component horen, kunnen worden gebruikt. Kenmerken van subcomponenten of gebruikersvereisten kunnen niet worden gebruikt.

### <a name="example"></a>Voorbeeld

Een productconfiguratiemodel heeft een hoofdcomponent met twee kenmerken:

-   Materiaal (plastic, hout, staal)
-   Lengte (10... 100)

U maakt een configuratienomenclatuur met de volgende segmenten:

1.  Kenmerkwaarde: materiaal
2.  Tekstconstante: "AAA"
3.  Kenmerkwaarde: lengte

In dit geval is de configuratie-id voor houten materiaal met een lengte van 78 WoodAAA78.

## <a name="nomenclature-of-dimension-based-configurations"></a>Nomenclatuur met op dimensies gebaseerde configuraties
Voor op dimensies gebaseerde configuraties kunt u een specifieke nomenclatuur maken voor de configuratieproductdimensie. U kunt de volgende segmenten selecteren op de pagina **Productnomenclatuur**:

-   Nummerreekswaarde
-   Tekstconstante
-   Configuratiegroepitem

U kunt een configuratienomenclatuur definiëren voor een stuklijst (BOM).

### <a name="example"></a>Voorbeeld

Een stuklijst heeft vier stuklijstregels die worden onderverdeeld in twee configuratiegroepen:

-   Stuklijstregel: M0007, standaardbehuizing
    -   Configuratiegroep: behuizing
-   Stuklijstregel: M0008, geavanceerde behuizing
    -   Configuratiegroep: behuizing
-   Stuklijstregel: M0021, voorgrill van stof
    -   Configuratiegroep: Voorgrill
-   Stuklijstregel: M0022, metalen voorgrill
    -   Configuratiegroep: Voorgrill

U maakt een configuratienomenclatuur met de volgende segmenten:

1.  Configuratiegroep: behuizing
2.  Tekstconstante: "&"
3.  Configuratiegroep: Voorgrill

In dit geval is de configuratie-id voor een standaardbehuizing met een voorgrill van stof M0007&M0021.

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a>Nomenclatuur voor een combinatie van productvarianten en configuraties
Als u de op beperkingen of dimensies gebaseerde configuratietechnologie gebruikt om productvarianten voor een productmodel te configureren, kunnen de productvariantnummers van de productvarianten de nomenclatuur bevatten van de configuratiedimensie. Volg deze stappen om varianten te configureren.

1.  Definieer op de pagina **Productnomenclatuur** een nomenclatuur van productvariantnummers die de configuratiedimensie omvat.
2.  Wijs de nomenclatuur toe aan een productdimensiegroep die de configuratiedimensie heeft.
3.  Definieer een configuratienomenclatuur voor de componenten of de stuklijsten die worden gebruikt voor het configureren van de productvarianten.

U kunt ook nomenclaturen maken voor de productvariantnamen. De productvariantnamen kunnen worden geconfigureerd voor het opnemen van de configuratie-ID of -naam.

### <a name="example-for-constraint-based-configurations"></a>Voorbeeld van op beperkingen gebaseerde configuraties

In dit voorbeeld gebruikt u een productvariantnummernomenclatuur die bestaat uit de volgende segmenten:

1.  Nummer van basismaster
2.  Tekstconstante "\_"
3.  Configuratie

De configuratienomenclatuur bestaat uit de volgende segmenten:

1.  Kenmerkwaarde: materiaal
2.  Tekstconstante: "AAA"
3.  Kenmerkwaarde: lengte

U kunt de volgende waarden voor segmenten invoeren:

-   Productmodelnummer = **M0099**
-   Materiaal = **Plastic**
-   Lengte = **12**

In dit geval is het productvariantnummer M0099\_PlasticAAA12.

### <a name="example-for-dimension-based-configurations"></a>Voorbeeld van op dimensies gebaseerde configuraties

In dit voorbeeld gebruikt u een productvariantnummernomenclatuur die bestaat uit de volgende segmenten:

1.  Nummer van basismaster
2.  Tekstconstante "//"
3.  Configuratie

De configuratienomenclatuur bestaat uit de volgende segmenten:

1.  Configuratiegroep: behuizing
2.  Tekstconstante: "&"
3.  Configuratiegroep: Voorgrill

U kunt de volgende waarden voor segmenten invoeren:

-   Productmodelnummer = **D0123**
-   Behuizing = **M0008**
-   Voorgrill = **M0022**

In dit geval is het productvariantnummer D0123//M0008&M0022.

## <a name="numbering-conflicts"></a>Nummeringsconflicten
In sommige gevallen is het mogelijk dat een nomenclatuur voor productvariantnummers die u instelt, geen unieke productvariantnummers produceert. De productvariantnummers zijn bijvoorbeeld niet uniek als één actieve productdimensie niet wordt opgenomen in de nomenclatuur van een productmodel dat de vooraf gedefinieerde variantconfiguratietechnologie gebruikt. De manier waarop u conflicten verwerken, varieert afhankelijk van de configuratietechnologie.

### <a name="predefined-variants"></a>Vooraf gedefinieerde varianten

Er treedt een fout op als u handmatig of automatisch probeert productvarianten te genereren, en meerdere productvarianten hetzelfde productvariantnummer krijgen. Als u dit scenario wilt voorkomen, moet u alle actieve productdimensies in de productdimensiegroep gebruiken. U kunt ook een nummerreeks opnemen om te garanderen dat de productvariantnummers uniek zijn.

### <a name="constraint-based-configurations"></a>Op beperkingen gebaseerde configuraties

Afhankelijk van de nomenclatuur kan het systeem proberen een niet-uniek productvariantnummer aan een configuratie toe te wijzen. In dit geval gebruikt het systeem de nummerreeks voor de configuratiedimensie als productvariantnummer. Als dit gebeurt, ontvangt u een waarschuwing. Als u dit scenario wilt voorkomen, moet u voldoende kenmerken opnemen in de nomenclatuur om unieke productvariantnummers te garanderen. U moet tevens zorgen dat de optie **Opnieuw gebruiken** is ingeschakeld voor het onderdeel.

### <a name="dimension-based-configurations"></a>Op dimensie gebaseerde configuraties

Tijdens een stap van het configuratieproces suggereert het systeem een configuratiewaarde volgens de nomenclatuur. In deze stap kunt u de configuratiewaarde handmatig wijzigen. Wanneer u de configuratie opslaat, controleert het systeem of de configuratiewaarde uniek is. Als de waarde die u hebt ingevoerd niet uniek is, ontvangt u een foutbericht. Als u de configuratie wilt opslaan, moet u een unieke configuratiewaarde invoeren.

<a name="additional-resources"></a>Aanvullende resources
--------

[Een nomenclatuur met productnummers maken voor vooraf gedefinieerde productvarianten](tasks/create-product-number-nomenclature-predefined-variants-2016-11.md)

[Een productnummernomenclatuur voor geconfigureerde productvarianten maken](tasks/create-product-number-nomenclature-product-variants_2016_11.md)

