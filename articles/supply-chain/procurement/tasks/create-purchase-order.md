---
title: Inkooporder maken
description: In dit onderwerp leest u hoe u een inkooporder handmatig maakt.
author: mkirknel
manager: tfehr
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventDimParmFixed, InventItemIdLookupPurchase, InventProductDimensionLookup, PurchTotals
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec91174f291bcfa7027a93ca344823561cc29e3f
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018144"
---
# <a name="create-a-purchase-order"></a>Inkooporder maken

[!include [banner](../../includes/banner.md)]

In dit onderwerp leest u hoe u een inkooporder handmatig maakt. Het is gebruikelijker dat inkooporders automatisch worden gemaakt als resultaat van hoofdplanning, directe levering en andere processen. Inkooporders worden meestal gemaakt door een inkoper. Het hier weergegeven voorbeeld kan in het demobedrijf USMF worden gebruikt met de waarden die in de notities voor verschillende stappen worden voorgesteld.


## <a name="create-the-purchase-order-header"></a>De koptekst van de inkooporder maken
1. Ga naar **Navigatievenster > Modules > Inkoopbeheer > Inkooporders > Alle inkooporders**.
2. Selecteer **Nieuw**.
3. Selecteer leveranciersrekening **US-101**. Wanneer u een leverancier selecteert, worden de details van de leveranciersrecord, zoals adres, factuurrekening, leveringsvoorwaarden en leveringsmodus als standaardwaarden naar de orderkoptekst gekopieerd. U kunt deze waarden op elk moment wijzigen.  
4. Vouw de sectie **Algemeen** uit.

    - Met het veld **Vestiging** samen met het veld **Magazijn** wordt opgegeven waar de aangeschafte goederen of services moeten worden geleverd. Het standaardafleveradres is de vestiging. In beide velden kunnen waarden worden ingevuld voor de geselecteerde leverancier. U kunt deze ook handmatig opgeven.  
    - Het veld **Leveringsdatum** wordt gebruikt om op te geven wanneer de aangeschafte goederen en services moeten worden geleverd. U kunt één leveringsdatum voor de order opgeven of u kunt unieke leveringsdatums aan de afzonderlijke orderregels geven. Als de hier opgegeven leveringsdatum niet kan worden gehaald voor specifieke producten of services omdat ze langere doorlooptijden hebben, worden deze regels hiervoor met een latere leveringsdatum gemaakt.  

5. Vouw de sectie **Beheer** uit. Het veld **Besteller** kan worden gebruikt om op te geven wie de order plaatst. Dit kan handig zijn om aan de leverancier door te geven voor het geval contact met deze persoon moet worden opgenomen. Aan het veld kan automatisch een waarde worden toegewezen als de huidige gebruikersaccount is gekoppeld aan een naam op de pagina **Gebruikers**.  
6. Selecteer **OK**. De orderkoptekst is nu gemaakt. Wanneer u werkt met inkooporderregels, wordt alleen een overzicht van de koptekstgegevens weergegeven. Als u de rest van de informatie moet bekijken, klikt op **Koptekst**.  

## <a name="add-a-purchase-order-line"></a>Een inkooporderregel toevoegen
1. Selecteer **Inkooporderregel**.
2. Selecteer **Dimensies**. De producten kunnen in varianten zijn die door dimensies, zoals kleur, grootte of stijl worden onderscheiden. Voor de producten kunnen ook opslagdimensies worden ingesteld, zoals vestiging en magazijn. Er zijn ook optionele traceringsdimensies, zoals batch- en serienummers. Om de efficiëntie van orderinvoer te verbeteren, kunt u de dimensievelden die u vaak gebruikt rechtstreeks toevoegen aan het orderraster.  
3. Schakel het selectievakje **Kleur** in. Optioneel: als u het veld **Instellingen opslaan** selecteert, worden de dimensies die u hebt gekozen ook weergegeven in het orderregelraster als u de inkooporderpagina de volgende keer opent.  
4. Selecteer **OK**.
5. Selecteer in het veld **Artikelnummer** de optie **T0004**.

    - De orderregels worden gemaakt voor producten en services door een artikelnummer op te geven of als uitgaven door een aanschaffingscategorie op te geven. 
    - Het veld **Aanschaffingscategorie** wordt gebruikt voor het toevoegen van regels waarop aangeschafte artikelen direct worden opgevoerd, in plaats van naar de voorraad te gaan. Dit betekent dat als u een aanschaf moet opvoeren, dit kunt doen door een inkooporderregel te maken waarmee een aanschaffingscategorie wordt opgegeven, in plaats van een regel met een artikelnummer te maken. Artikelen kunnen ook worden gekoppeld aan een aanschaffingscategorie en in dit geval wordt de aanschaffingscategorie alleen ter informatie weergegeven.  

6. Typ of selecteer een waarde in het veld **Kleur**. In de velden **Vestiging** en **Magazijn** worden gewoonlijk waarden ingevuld uit de orderkoptekst, maar het is mogelijk de velden te overschrijven als sommige regels op verschillende locaties moeten worden geleverd.  
7. Voer een getal in het veld **Hoeveelheid** in.

    - Selecteer de hoeveelheid die u wilt aanschaffen. Het veld **Hoeveelheid** wordt automatisch ingevuld met de minimale orderhoeveelheid voor het product als deze is ingesteld, of met de waarde 1.  
    - Met het veld **Eenheid** wordt de maateenheid voor de bestelde hoeveelheid aangegeven. Doorgaans wordt de eenheid automatisch op basis van de inkoopmaateenheid van de productmodelgegevens verschaft, maar u kunt dit wijzigen.  
    - Het veld **Eenheidsprijs** bevat meestal een waarde van een inkoopovereenkomst of een handelsovereenkomst. Het is mogelijk de eenheidsprijs op afzonderlijke orderregels te wijzigen, bijvoorbeeld als een unieke prijs met de leverancier is overeengekomen.  
    - Het veld **Korting** bevat een kortingsbedrag per eenheid. Met deze korting wordt daarom de eenheidsprijs verlaagd. Deze korting wordt over het algemeen automatisch op basis van inkoopovereenkomsten of handelsovereenkomsten verschaft, maar het is mogelijk deze op afzonderlijke regels te overschrijven als unieke kortingen met de leverancier zijn overeengekomen.  
    - Er kan een kortingspercentage worden ingevoerd waarmee het nettobedrag dienovereenkomstig voor de regel wordt verlaagd. Het kortingspercentage wordt vaak automatisch op basis van inkoopovereenkomsten of handelsovereenkomsten verschaft, maar het is mogelijk het op afzonderlijke regels te overschrijven als een unieke korting met de leverancier is overeengekomen.  
    - De waarde in het veld **Nettobedrag** wordt berekend op basis van andere velden op de regel, inclusief hoeveelheid, eenheidsprijs, korting en kortingspercentage. Het is mogelijk om het nettobedrag te wijzigen, maar dan zijn de velden **Eenheidsprijs** , **Korting** en **Kortingspercentage** leeg en wanneer u naar de regel boekt, is het geboekte bedrag evenredig aan het nettobedrag. Meestal wordt het veld **Nettobedrag** alleen gebruikt voor het weergeven van het nettobedrag van de regel.  

8. Vouw de sectie **Regeldetails** uit.
9. Selecteer het tabblad **Levering**. Er kan een unieke leveringsdatum aan elke orderregel worden toegewezen. De datum wordt overgenomen van het veld in de koptekst van de inkooporder, maar u kunt dit wijzigen.  

## <a name="review-order-totals"></a>Ordertotalen controleren
1. Selecteer **Totalen**.

    - Als u de actie **Totalen** niet ziet, selecteert u het tabblad **Inkooporder** in het actievenster.  
    - Dit dialoogvenster bevat totalen voor de gehele order.  
    - Met het veld **Selectie** kunt u de basis wijzigen van de manier waarop totalen worden berekend. U kunt bijvoorbeeld **Productontvangstbonhoeveelheid** kiezen om totalen te tonen die gerelateerd zijn aan het bedrag van het product of de producten die is of zijn ontvangen, of u kunt **Bestelde hoeveelheid** kiezen om het bedrag van het bestelde product weer te geven.  

2. Selecteer **OK**.

