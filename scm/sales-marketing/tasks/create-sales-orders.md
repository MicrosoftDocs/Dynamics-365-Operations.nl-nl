--- 
title: Verkooporders maken
description: Deze procedure laat zien hoe u een verkooporder maakt.
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 62276765e1cc76b2328a7b5b57bd18593d93e4ab
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="create-sales-orders"></a>Verkooporders maken

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u een verkooporder maakt. U kunt deze procedure met het bedrijf USMF van de demogegevens gebruiken. De verkooporders worden gewoonlijk gemaakt door een verkooporderbewerker. 




## <a name="enter-sales-order-header-details"></a>Verkooporderkopdetails invoeren
1. Ga naar Verkoop en marketing > Verkooporders > Alle verkooporders.
2. Klik op Nieuw.
3. Klik in het veld Klantrekening op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Zoek en selecteer de klantrecord in de lijst.
    * Selecteer voor dit voorbeeld klantnummer US-004.  
5. Klik in de lijst op de koppeling in de geselecteerde rij.
6. Klik op OK.

## <a name="enter-sales-order-line-details"></a>Verkooporderregeldetails invoeren
    * De producten die door uw organisatie worden verkocht, kunnen variëren qua dimensies, zoals configuratie, kleur, grootte, en stijl. Ook kunnen de producten worden ingesteld voor opslagdimensies, zoals locatie, magazijn en pallet, en traceringsdimensies, zoals batch- en serienummers. Wanneer deze dimensies worden toegewezen, moet u de waarden voor die dimensies op de orderregel selecteren. Om orderinvoerefficiëntie te verbeteren, kunt u de betreffende dimensievelden aan het orderraster toevoegen.  
1. Klik op Verkooporderregel.
2. Klik op Dimensies.
    * Selecteer voor dit voorbeeld de dimensies Kleur, Locatie en Magazijn. De geselecteerde dimensies worden in het verkooporderraster weergegeven. Als u uw selecties wilt behouden, stelt u de optie Instellingen opslaan op Ja in.   
3. Klik op OK.
4. Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.
5. Selecteer voor dit voorbeeld T0004.
6. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Als het artikel onderdeel van een verkoopcategorie is, wordt automatisch de artikelnaam in het verkoopcategorieveld weergegeven.  
    * Als de productdimensievelden al een waarde bevatten, is dit omdat de waarde van het productrecord is gekopieerd waar het is gedefinieerd als een standaardproductdimensie. U kunt de standaardwaarde altijd wijzigen.   
7. Klik in het veld Kleur op de vervolgkeuzeknop om de zoekopdracht te openen.
8. Zoek en selecteer het gewenste record in de lijst.
9. Klik in de lijst op de koppeling in de geselecteerde rij.
10. Voer in het veld Hoeveelheid een getal in.
    * Als het artikel in verschillende eenheden wordt verkocht wanneer het wordt gekocht, geproduceerd en opgeslagen, en een verkoopeenheid is ingesteld in de productrecord, wordt deze waarde in het veld Eenheid weergegeven. U kunt de waarde op elk gewenst moment wijzigen.   
    * Als het veld Locatie al een waarde bevat, is de waarde gekopieerd van de orderkoptekst of de orderinstellingen die aan het product zijn gekoppeld. U kunt de waarde op elk gewenst moment wijzigen. Selecteer een waarde als het veld leeg is.   
    * Als het veld Eenheidsprijs al een waarde bevat, is de waarde gekopieerd van een geldige handelsovereenkomst, of van het productrecord. (De eenheidsprijs kan ook uit een verkoopovereenkomst afkomstig zijn, maar het proces om verkooporders van verkoopovereenkomsten te maken is verschillend van het hier weergegeven proces.) Als het veld leeg is, voert u een waarde in.   
    * Het kortingsveld bevat een kortingsbedrag per producteenheid. Om het totale regelkortingbedrag te berekenen, wordt de kortingswaarde vermenigvuldigd met regelhoeveelheid.    Als het veld Korting al een waarde bevat, is de waarde gekopieerd van een geldige handelsovereenkomst. Als het veld leeg is, en u de klant een regelkorting wilt geven, voert u een waarde in.  
    * Het veld Kortingspercentage bevat een procentuele waarde waarmee het totale regelbrutobedrag moet worden verminderd.  Als het veld Kortingspercentage al een waarde bevat, is de waarde gekopieerd van een geldige handelsovereenkomst. Als het veld leeg is, en u de klant een regelkorting wilt geven, voert u een waarde in.  
    * Het veld Nettobedrag bevat een waarde die op basis van de hoeveelheid en eenheidsprijs van de regel, aangepast door kortingen, wordt berekend.  U kunt de berekende waarde met een andere overschrijven.  

## <a name="review-the-order-totals"></a>De ordertotalen controleren
1. Klik in het actievenster op Verkooporder.
2. Klik op Totalen.
    * De pagina Totalen bevat details over de gehele order. Dit omvat het subtotaalbedrag, wat een som is van alle regelnettobedragen, aangepast voor uiteindelijke regelkortingen, het totale factuurbedrag, dat een subtotaalbedrag is, aangepast voor uiteindelijke korting op orderniveau, toeslagen, btw, de situatie van de kredietlimiet van de klant, en meer.  Het factuurbedrag is het bedrag dat op het factuurdocument van de klant wordt weergegeven.  
3. Klik op OK.


