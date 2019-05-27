---
title: Materiaalverbruik berekenen
description: Dit artikel bevat informatie over verschillende opties met betrekking tot de berekening van materiaalverbruik.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMDesignerEditBOM, BOMTable, ProdBOM
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 53401
ms.assetid: 9cff88e4-0425-4707-9178-3c2cb10df7c2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3e4010b5abb6b5a871d098422f1489cb2db3a071
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572645"
---
# <a name="calculate-material-consumption"></a>Materiaalverbruik berekenen

[!include [banner](../includes/banner.md)]

Dit artikel bevat informatie over verschillende opties met betrekking tot de berekening van materiaalverbruik. 

De volgende opties die aan de berekening van het materiaalverbruik zijn gerelateerd zijn beschikbaar op de tabbladen **Instellen** en **Stapverbruik** op het sneltabbblad **Regeldetails** van de pagina **Stuklijst**.

## <a name="variable-and-constant-consumption"></a>Variabel en constant verbruik
In het veld **Verbruik** kunt u aangeven of verbruik moet worden berekend als een constante of een variabele hoeveelheid. Selecteer **Constante** als een vaste hoeveelheid of een vast volume nodig is voor de productie, ongeacht de hoeveelheid die wordt geproduceerd. Selecteer, **Variabel**, oftewel de standaardinstelling, als de vereiste hoeveelheid materiaal in de eindproducten proportioneel is aan het aantal geproduceerde eindproducten.

## <a name="calculating-consumption-from-a-formula"></a>Verbruik berekenen op basis van een formule
In het veld **Formule** kunt u verschillende formules instellen voor het berekenen van materiaalverbruik. Als u de standaardwaarde gebruikt, **Standaard**, wordt het verbruik niet berekend op basis van een formule. De volgende formules werken samen met de velden **Hoogte**, **Breedte**, **Diepte**, **Dichtheid** en **Constant**:

-   Hoogte \* constante
-   Hoogte \* breedte \* constante
-   Hoogte \* breedte \* diepte \* constante
-   (Hoogte \* breedte \* diepte/dichtheid) \* constante

## <a name="rounding-up-and-multiples"></a>Veelvouden afronden
Samen kunt u met de velden **Naar boven afronden** en **Veelvouden** de waarde voor het materiaalverbruik naar boven afronden. Zo kunt u bijvoorbeeld de waarde naar boven afronden op basis van de materiaalverwerkingseenheid waarin de grondstof voor productie wordt verzameld. De volgende opties zijn beschikbaar in het veld **Naar boven afronden**: **Hoeveelheid**, **Afmeting** en **Verbruik**.

### <a name="quantity"></a>Hoeveelheid

Als u **Hoeveelheid** selecteert als mechanisme voor naar boven afronden, moet de hoeveelheid een veelvoud zijn van de opgegeven hoeveelheid. Als er bijvoorbeeld gehele getallen vereist zijn, selecteert u **1** in het veld **Veelvouden**. Getallen worden vervolgens naar boven afgerond tot een hoeveelheid die deelbaar is door 1.

### <a name="measurement"></a>Meting

Doorgaans selecteert u **Afmeting** als mechanisme voor naar boven afronden wanneer de grondstof specifieke dimensies heeft. Stel dat een metalen buis van 2 meter lengte is vereist voor een eindproduct en de metalen buis wordt opgeslagen in lengten van 4,5 meter. In dit geval kan het mechanisme voor naar boven afronden **Afmeting** worden gebruikt om te berekenen hoeveel metalen buizen nodig zijn om een bepaald aantal stuks van het eindproduct te vervaardigen. In dit voorbeeld is het veld **Formule** ingesteld op **Hoogte \* constante**. Het veld **Hoogte** is ingesteld op **2** om de lengte aan te geven van de buis die vereist is voor het eindproduct. Het veld **Veelvoud** wordt ingesteld op **4,5** om aan te geven dat de buis in lengten van 4,5 meter wordt verzameld. Hier volgt de berekening:

1.  Aantal veelvouden dat is vereist voor 10 stuks van het eindproduct: 10 ÷ 2 = 5 stuks
2.  Totaal verbruik: 4,5 x 5 = 22,5 meter metalen buis

Er wordt aangenomen dat 0,5 meter buis als afval overblijft voor elke vijf stuks buizen die worden verbruikt.

### <a name="consumption"></a>Verbruik

Doorgaans selecteert u **Verbruik** als mechanisme voor naar boven afronden wanneer grondstoffen moeten worden verzameld in gehele hoeveelheden van een specifieke materiaalverwerkingseenheid van het product. Zo worden bijvoorbeeld 2 liter verf gebruikt om één eindproduct te maken, en de verf wordt verzameld in blikken van 25 liter. In dit geval kan het mechanisme voor afronding naar boven **Verbruik** worden gebruikt om het verbruik af te ronden op gehele getallen voor blikken van 25 liter. Hier volgt de berekening voor de hoeveelheid verf die is vereist als 180 stuks van het eindproduct moeten worden vervaardigd:

1.  Vereiste verf, exclusief uitval: 180 x 2 = 360 liter
2.  Aantal blikken: 360 ÷ 25 = 14,4, hetgeen wordt afgerond tot 15
3.  Vereiste verf, inclusief uitval: 15 x 25 = 375 liter

## <a name="step-consumption"></a>Stapverbruik
Stapverbruik wordt gebruikt voor het berekenen van het constante verbruik in hoeveelheidsintervallen. Als u **Stapverbruik** selecteert in het veld **Formule** op het tabblad **Instellingen**, kunt u informatie over de stappen toevoegen op het tabblad **Stapverbruik**. De vaste verbruikte hoeveelheid kan worden ingesteld in intervallen van de geproduceerde hoeveelheid. Stapverbruik wordt bijvoorbeeld,ingesteld op de wijze die in de volgende tabel wordt aangegeven.

| Van serie | Hoeveelheid |
|-------------|----------|
| 0,00        | 10,0000  |
| 100,00      | 20,0000  |
| 200,00      | 40,0000  |

De hoeveelheid van de stuklijst (BOM) is 1 en productiehoeveelheid is 110. De formule voor het verbruik is Van reeks (hoeveelheid) = Verbruik. Omdat de productiehoeveelheid 110 is, valt deze binnen de "Van 100 reeks". Daarom is de hoeveelheid 20.



