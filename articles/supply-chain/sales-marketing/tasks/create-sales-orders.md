---
title: Verkooporders maken
description: Deze procedure laat zien hoe u een verkooporder maakt.
author: omulvad
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, InventDimParmFixed, InventProductDimensionLookup, SalesTotals
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: da460106c95f046e5762787ed169744dece0749f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204368"
---
# <a name="create-sales-orders"></a>Verkooporders maken

[!include [banner](../../includes/banner.md)]

Deze procedure laat zien hoe u een verkooporder maakt. U kunt deze procedure met het bedrijf USMF van de demogegevens gebruiken. De verkooporders worden gewoonlijk gemaakt door een verkooporderbewerker. 

## <a name="enter-sales-order-header-details"></a>Verkooporderkopdetails invoeren
1. Ga naar **Navigatievenster > Modules > Verkoop en marketing > Verkooporders > Alle verkooporders**.
2. Selecteer **Nieuw**.
3. Selecteer in het veld **Klantrekening** de vervolgkeuzeknop om de zoekopdracht te openen.
4. Zoek en selecteer de klantrecord in de lijst.
    - Selecteer voor dit voorbeeld klantnummer US-004.  
5. Selecteer **OK**.

## <a name="enter-sales-order-line-details"></a>Verkooporderregeldetails invoeren
    
De producten die door uw organisatie worden verkocht, kunnen variëren qua dimensies, zoals configuratie, kleur, grootte, en stijl. Ook kunnen de producten worden ingesteld voor opslagdimensies, zoals locatie, magazijn en pallet, en traceringsdimensies, zoals batch- en serienummers. Wanneer deze dimensies worden toegewezen, moet u de waarden voor die dimensies op de orderregel selecteren. Om orderinvoerefficiëntie te verbeteren, kunt u de betreffende dimensievelden aan het orderraster toevoegen.
    
1. Selecteer onder de sectie **Verkooporderregels** de optie **Verkooporderregel**.
2. Selecteer **Dimensies**.
    
    Selecteer voor dit voorbeeld de dimensies Kleur, Locatie en Magazijn. De geselecteerde dimensies worden in het verkooporderraster weergegeven. Als u uw selecties wilt behouden, stelt u de optie **Instellingen opslaan** op Ja in.
    
3. Selecteer **OK**.
4. Selecteer in het veld **Artikelnummer** de vervolgkeuzeknop om de zoekopdracht te openen.
5. Selecteer voor dit voorbeeld T0004.
    - Als het artikel onderdeel van een verkoopcategorie is, wordt automatisch de artikelnaam in het verkoopcategorieveld weergegeven.  
    - Als de productdimensievelden al een waarde bevatten, is dit omdat de waarde van het productrecord is gekopieerd waar het is gedefinieerd als een standaardproductdimensie. U kunt de standaardwaarde altijd wijzigen.   
6. Selecteer in het veld **Kleur** de vervolgkeuzeknop om de zoekopdracht te openen.
7. Zoek en selecteer de gewenste record in de lijst.
8. Voer een getal in het veld **Hoeveelheid** in.
    - Als het artikel in verschillende eenheden wordt verkocht wanneer het wordt gekocht, geproduceerd en opgeslagen, en een verkoopeenheid is ingesteld in de productrecord, wordt deze waarde in het veld **Eenheid** weergegeven. U kunt de waarde op elk gewenst moment wijzigen.   
    - Als het veld **Locatie** al een waarde bevat, is de waarde gekopieerd van de orderkoptekst of de orderinstellingen die aan het product zijn gekoppeld. U kunt de waarde op elk gewenst moment wijzigen. Selecteer een waarde als het veld leeg is.   
    - Als het veld **Eenheidsprijs** al een waarde bevat, is de waarde gekopieerd van een geldige handelsovereenkomst, of van het productrecord. (De eenheidsprijs kan ook uit een verkoopovereenkomst afkomstig zijn, maar het proces om verkooporders van verkoopovereenkomsten te maken is verschillend van het hier weergegeven proces.) Als het veld leeg is, voert u een waarde in.   
    - Het veld **Korting** bevat een kortingsbedrag per producteenheid. Om het totale regelkortingbedrag te berekenen, wordt de kortingswaarde vermenigvuldigd met regelhoeveelheid. Als het veld **Korting** al een waarde bevat, is de waarde gekopieerd van een geldige handelsovereenkomst. Als het veld leeg is, en u de klant een regelkorting wilt geven, voert u een waarde in.  
    - Het veld **Kortingspercentage** bevat een procentuele waarde waarmee het totale regelbrutobedrag moet worden verminderd.  Als het veld **Kortingspercentage** al een waarde bevat, is de waarde gekopieerd van een geldige handelsovereenkomst. Als het veld leeg is, en u de klant een regelkorting wilt geven, voert u een waarde in. 
    - Het veld **Nettobedrag** bevat een waarde die op basis van de hoeveelheid en eenheidsprijs van de regel, aangepast door kortingen, wordt berekend.  U kunt de berekende waarde met een andere overschrijven.  

## <a name="review-the-order-totals"></a>De ordertotalen controleren
1. Selecteer **Verkooporder** in het **actievenster**.
2. Selecteer **Totalen**.
    
    De pagina **Totalen** bevat details over de gehele order. Dit omvat het subtotaalbedrag, wat een som is van alle regelnettobedragen, aangepast voor uiteindelijke regelkortingen, het totale factuurbedrag, dat een subtotaalbedrag is, aangepast voor uiteindelijke korting op orderniveau, toeslagen, btw, de situatie van de kredietlimiet van de klant, en meer. Het factuurbedrag is het bedrag dat op het factuurdocument van de klant wordt weergegeven.  
    
3. Selecteer **OK**.
