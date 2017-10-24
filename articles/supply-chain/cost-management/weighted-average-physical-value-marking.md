---
title: Gewogen gemiddelde met fysieke waarde en markering
description: 
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 65501
ms.assetid: 25041ff0-bafe-484d-a94a-e1772ad43204
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c9db625e5af77b8f5d1569e35ce2d4c20e5be646
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="weighted-average-with-physical-value-and-marking"></a>Gewogen gemiddelde met fysieke waarde en markering

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]



Wanneer u een voorraad afsluit, worden alle ontvangsten vereffend met een virtuele uitgifte, die de totaal ontvangen hoeveelheid en waarde bevat. Deze virtuele uitgifte heeft een bijbehorende virtuele ontvangst, waarmee de uitgiften worden vereffend. Op deze manier hebben alle uitgiften dezelfde gemiddelde kosten. De virtuele uitgifte en ontvangst kunnen worden gezien als virtuele overboeking, die ook wel een overboeking van gewogen gemiddelde eindvoorraad wordt genoemd.

Als er slechts één ontvangst is, kunnen alle uitgiften hiermee worden vereffend en wordt er geen virtuele overboeking gemaakt. 

Wanneer u een gewogen gemiddelde gebruikt, kunt u voorraadtransacties markeren, zodat een specifieke artikelontvangst wordt vereffend met een specifieke uitgifte in plaats van dat de regel van het gewogen gemiddelde wordt gebruikt. 

U wordt aangeraden maandelijks een voorraadafsluiting uit te voeren wanneer u het voorraadmodel van het gewogen gemiddelde gebruikt. 

De gewogen gemiddelde kostprijsberekeningsmethode wordt berekend met behulp van de volgende formule:
-   Gewogen gemiddelde = (KW1\*P1 + KW2\*P2 + Hoev\*Pn) / (KW1 + KW2 + Hoev)

Voorraadtransacties die de voorraaduitgiften verlaten. Hieronder vallen verkooporders, voorraadjournalen en productieorders, die plaatsvinden tegen een geraamde kostprijs op de boekingsdatum. Deze geschatte kostprijs wordt ook wel het lopende gemiddelde genoemd. Op het moment van de voorraadafsluiting worden de voorraadtransacties voor voorgaande en huidige perioden geanalyseerd en wordt bepaald welke van de volgende afsluitingsprincipes moet worden gebruikt.
-   Directe vereffening
-   Samengevatte vereffening

Vereffeningen zijn voorraadafsluitingsboekingen die de uitgiften vanaf de sluitingsdatum bijwerken met het juiste gewogen gemiddelde. De volgende voorbeelden laten het effect van het gebruik van gewogen gemiddelden bij vijf verschillende configuraties zien:
-   Directe vereffening op basis van een gewogen gemiddelde zonder de optie Fysieke waarde opnemen
-   Samengevatte vereffening op basis van een gewogen gemiddelde zonder de optie Fysieke waarde opnemen
-   Directe vereffening op basis van een gewogen gemiddelde met de optie Fysieke waarde opnemen
-   Samengevatte vereffening op basis van een gewogen gemiddelde met de optie Fysieke waarde opnemen
-   Gewogen gemiddelde met markering

## <a name="weighted-average-direct-settlement-without-include-physical-value"></a>Directe vereffening op basis van een gewogen gemiddelde zonder Fysieke waarde opnemen
Het directe-vereffeningsprincipe is hetzelfde als het principe dat in eerdere versies werd gebruikt voor gewogen gemiddelden. Er wordt direct vereffend tussen ontvangsten en uitgiften. Het principe voor directe vereffening wordt in bepaalde situaties gebruikt:
-   Eén ontvangst en een of meer uitgiften zijn in de periode geboekt.
-   Er zijn alleen uitgiften in de periode geboekt en de voorraad bevat voorhanden artikelen uit een vorige afsluiting.

In het scenario in de volgende secties zijn een financieel bijgewerkte ontvangst en uitgifte geboekt. Tijdens de voorraadafsluiting wordt de ontvangst direct vereffende met de uitgifte en hoeft de kostprijs bij de uitgifte niet te worden gecorrigeerd. In de afbeelding worden de volgende transacties geïllustreerd.
-   1a. Fysieke ontvangst in voorraad is bijgewerkt voor een hoeveelheid van 5 tegen EUR 10,00 per stuk
-   1b. Financiële ontvangst in voorraad is bijgewerkt voor een hoeveelheid van 5 tegen EUR 10,00 per stuk
-   2a. Fysieke uitgifte uit voorraad is bijgewerkt voor een hoeveelheid van 2 tegen EUR 10,00 per stuk
-   2b. Financiële uitgifte uit voorraad is bijgewerkt voor een hoeveelheid van 2 tegen EUR 10,00 per stuk
-   3. Voorraadafsluiting wordt uitgevoerd met behulp van de directe-vereffeningsmethode om de financiële ontvangst van de voorraad te vereffenen met de financiële uitgifte van de voorraad.

In het volgende diagram wordt voor deze reeks transacties geïllustreerd wat het effect is van het kiezen van het gewogen gemiddelde voorraadmodel en het principe van directe vereffening zonder de optie Fysieke waarde opnemen. 

![Gewogen gemiddelde DS zonder de optie fysieke waarde opnemen](./media/weightedaveragedirectsettlementwithoutincludephysicalvalue.gif) 

**Uitleg bij diagram**
-   Voorraadtransacties worden aangegeven met verticale pijlen.
-   Ontvangsten in voorraad worden aangegeven met verticale pijlen boven de tijdlijn.
-   Uitgiften uit voorraad worden aangegeven met verticale pijlen onder de tijdlijn.
-   Boven (of onder) elke verticale pijl wordt de waarde van de voorraadtransactie opgegeven in de indeling Quantity@Unitprice.
-   Een voorraadtransactiewaarde tussen haakjes geeft aan dat de voorraadtransactie fysiek naar de voorraad is geboekt.
-   Een voorraadtransactiewaarde zonder haakjes geeft aan dat de voorraadtransactie financieel naar de voorraad is geboekt.
-   Elke nieuwe ontvangst of uitgiftetransactie krijgt een nieuw label.
-   Elke verticale pijl heeft een opeenvolgende ID, zoals *1a*. De ID's geven de volgorde van voorraadtransactieboekingen op de tijdlijn aan.
-   Voorraadafsluitingen worden aangegeven met verticale rode streepjes en het label Voorraadafsluiting.
-   Vereffeningen die worden uitgevoerd tijdens de voorraadafsluiting, worden vertegenwoordigd door gestippelde rode pijlen die diagonaal van een ontvangst naar een uitgifte lopen.

## <a name="weighted-average-summarized-settlement-without-the-include-physical-value-option"></a>Samengevatte vereffening op basis van een gewogen gemiddelde zonder de optie Fysieke waarde opnemen
Voor gewogen gemiddelden wordt gebruikgemaakt van het vereffeningsprincipe dat alle ontvangsten binnen een afsluitingsperiode worden samengevat in een transactie met de naam Gewogen gemiddelde eindvoorraad. Alle ontvangsten voor de periode worden vereffend met de uitgifte van deze nieuwe voorraadoverboekingstransactie. Alle uitgiften voor de periode worden vereffend met de ontvangst van de nieuwe voorraadoverboekingstransactie. Als de voorhanden voorraad na de voorraadafsluiting positief is, worden die voorhanden voorraad en de waarde van de voorraad samengevat in de nieuwe voorraadoverboekingstransactie (ontvangst). Is de voorhanden voorraad na de voorraadafsluiting negatief, dan zijn de voorhanden voorraad en de waarde van de voorraad de som van de afzonderlijke uitgiften die nog niet volledig zijn vereffend. In het onderstaande scenario zijn verschillende financieel bijgewerkte ontvangsten en één uitgifte geboekt. 

Tijdens de voorraadafsluiting wordt de samengevatte voorraadoverboekingstransactie gegenereerd en geboekt, en worden de ontvangsten voor de periode vereffend met de samengevatte voorraadoverboekingsuitgiftetransactie. Alle uitgiften die zijn geboekt voor de periode, worden vereffend met de samengevatte voorraadoverboekingsontvangsttransactie. Het gewogen gemiddelde wordt berekend op EUR 15,00. De uitgifte was oorspronkelijk geboekt met een geraamde kostprijs van EUR 14,67. Er wordt daarom een negatieve correctie van EUR 0,33 gemaakt en op de uitgifte geboekt. Vanaf de voorraadafsluitingsdatum is de voorhanden voorraad 3 stuks met een waarde van EUR 45,00. 

De volgende transacties worden in de onderstaande afbeelding geïllustreerd:
-   1a. Fysieke ontvangst in voorraad is bijgewerkt voor een hoeveelheid van 2 tegen EUR 11,00 aan kosten per stuk.
-   1b. Financiële ontvangst in voorraad is bijgewerkt voor een hoeveelheid van 2 tegen EUR 14,00 aan kosten per stuk.
-   2a. Fysieke ontvangst in voorraad is bijgewerkt voor een hoeveelheid van 1 tegen EUR 12,00 aan kosten per stuk.
-   2b. Financiële ontvangst in voorraad is bijgewerkt voor een hoeveelheid van 1 tegen EUR 16,00 aan kosten per stuk.
-   3a. Fysieke uitgifte uit voorraad is bijgewerkt voor een hoeveelheid van 1 tegen EUR 14,67 aan kosten per stuk (lopend gemiddelde).
-   3b. Financiële uitgifte uit voorraad is bijgewerkt voor een hoeveelheid van 1 tegen EUR 14,67 aan kosten per stuk (lopend gemiddelde).
-   4a. Fysieke ontvangst in voorraad is bijgewerkt voor een hoeveelheid van 1 tegen EUR 14,00 aan kosten per stuk.
-   4b. Financiële ontvangst in voorraad is bijgewerkt voor een hoeveelheid van 1 tegen EUR 16,00 aan kosten per stuk.
-   5. Voorraadafsluiting is uitgevoerd.
-   6a. Financiële uitgifte 'gewogen gemiddelde voorraadafsluitingstransactie' wordt gemaakt om de vereffeningen van alle financiële ontvangsten in voorraad bij elkaar op te tellen.
-   6b. Financiële ontvangst 'gewogen gemiddelde voorraadafsluitingstransactie' wordt gemaakt als tegenboeking voor 5a.

In het volgende diagram wordt voor deze reeks transacties geïllustreerd wat het effect is van het kiezen van het gewogen gemiddelde voorraadmodel en het principe van samengevatte vereffening zonder de optie Fysieke waarde opnemen. 

![Gewogen gemiddelde SS zonder de optie fysieke waarde opnemen](./media/weightedaveragesummarizedsettlementwithoutincludephysicalvalue.gif) 

**Uitleg bij diagram**
-   Voorraadtransacties worden aangegeven met verticale pijlen.
-   Ontvangsten in voorraad worden aangegeven met verticale pijlen boven de tijdlijn.
-   Uitgiften uit voorraad worden aangegeven met verticale pijlen onder de tijdlijn.
-   Boven (of onder) elke verticale pijl wordt de waarde van de voorraadtransactie opgegeven in de indeling Quantity@Unitprice.
-   Een voorraadtransactiewaarde tussen haakjes geeft aan dat de voorraadtransactie fysiek naar de voorraad is geboekt.
-   Een voorraadtransactiewaarde zonder haakjes geeft aan dat de voorraadtransactie financieel naar de voorraad is geboekt.
-   Elke nieuwe ontvangst of uitgiftetransactie krijgt een nieuw label.
-   Elke verticale pijl heeft een opeenvolgende ID, zoals *1a*. De ID's geven de volgorde van voorraadtransactieboekingen op de tijdlijn aan.
-   Voorraadafsluitingen worden aangegeven met verticale rode streepjes en het label Voorraadafsluiting.
-   Vereffeningen die worden uitgevoerd tijdens de voorraadafsluiting, worden vertegenwoordigd door gestippelde rode pijlen die diagonaal van een ontvangst naar een uitgifte lopen.
-   Rode pijlen duiden op ontvangsttransacties die worden vereffend met de uitgiftetransactie die is gemaakt door het systeem.
-   De groene pijl staat voor de door het systeem gegenereerde ontvangsttransactie waarmee de oorspronkelijk geboekte uitgiftetransactie wordt vereffend

## <a name="weighted-average-direct-settlement-with-the-include-physical-value-option"></a>Directe vereffening op basis van een gewogen gemiddelde met de optie Fysieke waarde opnemen
De parameter Fysieke waarde opnemen werkt anders in combinatie met het voorraadmodel van het gewogen gemiddelde dan in eerdere versies van het product. Schakel het selectievakje Fysieke waarde opnemen in voor een artikel op de pagina Artikelmodelgroepen. Vervolgens worden fysiek bijgewerkte ontvangsten gebruikt bij het berekenen van de geraamde kostprijs of de lopende, gemiddelde kostprijs. Uitgiften worden geboekt op basis van deze geraamde kostprijs tijdens de periode. Tijdens de voorraadafsluiting worden alleen financieel bijgewerkte ontvangsten meegenomen in de berekening van het gewogen gemiddelde. We raden u aan een maandelijkse voorraadafsluiting uit te voeren wanneer u het voorraadmodel van het gewogen gemiddelde gebruikt. In dit voorbeeld van een directe vereffening op basis van een gewogen gemiddelde is de artikelmodelgroep gemarkeerd voor het opnemen van de fysieke waarde. 

In de onderstaande afbeelding worden de volgende transacties geïllustreerd:
-   1a. Fysieke ontvangst in voorraad is bijgewerkt voor een hoeveelheid van 1 tegen EUR 11,00 aan kosten per stuk.
-   1b. Financiële ontvangst in voorraad is bijgewerkt voor een hoeveelheid van 1 tegen EUR 10,00 aan kosten per stuk.
-   2a. Fysieke ontvangst in voorraad is bijgewerkt voor een hoeveelheid van 1 tegen EUR 15,00 aan kosten per stuk.
-   3a. Fysieke uitgifte uit voorraad is bijgewerkt voor een hoeveelheid van 1 tegen EUR 12,50 aan kosten per stuk (lopende gemiddelde kosten, omdat er rekening is gehouden met de fysieke ontvangstwaarde).
-   3b. Financiële uitgifte uit voorraad is bijgewerkt voor een hoeveelheid van 1 tegen EUR 12,50 aan kosten per stuk (lopende gemiddelde kosten, omdat er rekening is gehouden met de fysieke ontvangstwaarde).
-   4. Voorraadafsluiting is uitgevoerd. Tijdens de voorraadafsluiting worden alle voorraadtransacties genegeerd die alleen fysiek zijn bijgewerkt. In plaats hiervan wordt het directe-vereffeningsprincipe gebruikt omdat er maar één financiële ontvangst bestaat. Er wordt een aanpassing van EUR 2,50 geboekt op de voorraadtransactie die financieel is uitgegeven vanaf de voorraadafsluitingsdatum. Na de voorraadafsluiting is de voorhanden voorraad gelijk aan een hoeveelheid van 1 met een lopende gemiddelde kostprijs van EUR 15,00.

In het volgende diagram wordt voor deze reeks transacties geïllustreerd wat het effect is van het kiezen van het gewogen gemiddelde voorraadmodel en het principe van directe vereffening met de optie Fysieke waarde opnemen. 

![Gewogen gemiddelde DS met fysieke waarde opnemen](./media/weightedaveragedirectsettlementwithincludephysicalvalue.gif) 

**Uitleg bij diagram**
-   Voorraadtransacties worden aangegeven met verticale pijlen.
-   Ontvangsten in voorraad worden aangegeven met verticale pijlen boven de tijdlijn.
-   Uitgiften uit voorraad worden aangegeven met verticale pijlen onder de tijdlijn.
-   Boven (of onder) elke verticale pijl wordt de waarde van de voorraadtransactie opgegeven in de indeling Quantity@Unitprice.
-   Een voorraadtransactiewaarde tussen haakjes geeft aan dat de voorraadtransactie fysiek naar de voorraad is geboekt.
-   Een voorraadtransactiewaarde zonder haakjes geeft aan dat de voorraadtransactie financieel naar de voorraad is geboekt.
-   Elke nieuwe ontvangst of uitgiftetransactie krijgt een nieuw label.
-   Elke verticale pijl heeft een opeenvolgende ID, zoals *1a*. De ID's geven de volgorde van voorraadtransactieboekingen op de tijdlijn aan.
-   Voorraadafsluitingen worden aangegeven met verticale rode streepjes en het label Voorraadafsluiting.
-   Vereffeningen die worden uitgevoerd tijdens de voorraadafsluiting, worden vertegenwoordigd door gestippelde rode pijlen die diagonaal van een ontvangst naar een uitgifte lopen.

## <a name="weighted-average-summarized-settlement-with-the-include-physical-value-option"></a>Samengevatte vereffening op basis van een gewogen gemiddelde met de optie Fysieke waarde opnemen
De parameter Fysieke waarde opnemen werkt anders in combinatie met het gewogen gemiddelde dan in eerdere versies van het programma. Schakel het selectievakje Fysieke waarde opnemen in voor een artikel op de pagina Artikelmodelgroepen. Vervolgens worden fysiek bijgewerkte ontvangsten gebruikt bij het berekenen van de geraamde kostprijs of de lopende, gemiddelde kostprijs. Uitgiften worden tijdens de periode geboekt op basis van deze geschatte kostprijs. Tijdens de voorraadafsluiting worden alleen financieel bijgewerkte ontvangsten meegenomen in de berekening van het gewogen gemiddelde. We raden u aan een maandelijkse voorraadafsluiting uit te voeren wanneer u het gewogen gemiddelde voorraadmodel gebruikt. In dit voorbeeld van een samengevatte vereffening op basis van een gewogen gemiddelde is het voorraadmodel gemarkeerd voor het opnemen van de fysieke waarde. 

De volgende transacties worden in de onderstaande afbeelding geïllustreerd:
-   1a. Fysieke ontvangst in voorraad is bijgewerkt voor een hoeveelheid van 2 tegen EUR 11,00 aan kosten per stuk.
-   1b. Financiële ontvangst in voorraad is bijgewerkt voor een hoeveelheid van 2 tegen EUR 14,00 aan kosten per stuk.
-   2. Fysieke ontvangst in voorraad is bijgewerkt voor een hoeveelheid van 1 tegen EUR 10,00 aan kosten per stuk.
-   3a. Fysieke ontvangst in voorraad is bijgewerkt voor een hoeveelheid van 1 tegen EUR 12,00 aan kosten per stuk.
-   3b. Financiële ontvangst in voorraad is bijgewerkt voor een hoeveelheid van 1 tegen EUR 16,00 aan kosten per stuk.
-   4a. Fysieke uitgifte uit voorraad is bijgewerkt voor een hoeveelheid van 1 tegen EUR 13,50 aan kosten per stuk (lopende gemiddelde kosten, omdat er rekening is gehouden met de fysieke ontvangstwaarde).
-   4b. Financiële uitgifte uit voorraad is bijgewerkt voor een hoeveelheid van 1 tegen EUR 13,50 aan kosten per stuk (lopende gemiddelde kosten, omdat er rekening is gehouden met de fysieke ontvangstwaarde).
-   5a. Fysieke ontvangst in voorraad is bijgewerkt voor een hoeveelheid van 1 tegen EUR 14,00 aan kosten per stuk.
-   5b. Financiële ontvangst in voorraad is bijgewerkt voor een hoeveelheid van 1 tegen EUR 16,00 aan kosten per stuk.
-   6. Voorraadafsluiting is uitgevoerd. Tijdens de voorraadafsluiting worden alle voorraadtransacties genegeerd die alleen fysiek zijn bijgewerkt. Het samengevatte-vereffeningsprincipe wordt gebruikt omdat er maar één financiële ontvangst bestaat. Er wordt een aanpassing van EUR 1,50 geboekt op de voorraadtransactie die financieel is uitgegeven vanaf de voorraadafsluitingsdatum. Na de voorraadafsluiting is de voorhanden voorraad gelijk aan een hoeveelheid van 3 met een lopende gemiddelde kostprijs van EUR 15,00.
-   7a. Financiële uitgifte 'gewogen gemiddelde voorraadafsluitingstransactie' wordt gemaakt om de vereffeningen van alle financiële ontvangsten in voorraad bij elkaar op te tellen.
-   7b. Financiële ontvangst 'gewogen gemiddelde voorraadafsluitingstransactie' wordt gemaakt als tegenboeking voor 5a.

In het volgende diagram wordt voor deze reeks transacties geïllustreerd wat het effect is van het kiezen van het gewogen gemiddelde voorraadmodel en het principe van samengevatte vereffening zonder de optie Fysieke waarde opnemen. 

![Gewogen gemiddelde SS met de optie fysieke waarde](./media/weightedaveragesummarizedsettlementwithincludephysicalvalue.gif) 

**Uitleg bij diagram**
-   Voorraadtransacties worden aangegeven met verticale pijlen.
-   Ontvangsten in voorraad worden aangegeven met verticale pijlen boven de tijdlijn.
-   Uitgiften uit voorraad worden aangegeven met verticale pijlen onder de tijdlijn.
-   Boven (of onder) elke verticale pijl wordt de waarde van de voorraadtransactie opgegeven in de indeling Quantity@Unitprice.
-   Een voorraadtransactiewaarde tussen haakjes geeft aan dat de voorraadtransactie fysiek naar de voorraad is geboekt.
-   Een voorraadtransactiewaarde zonder haakjes geeft aan dat de voorraadtransactie financieel naar de voorraad is geboekt.
-   Elke nieuwe ontvangst of uitgiftetransactie krijgt een nieuw label.
-   Elke verticale pijl heeft een opeenvolgende ID, zoals 1a. De ID's geven de volgorde van voorraadtransactieboekingen op de tijdlijn aan.
-   Voorraadafsluitingen worden aangegeven met verticale rode streepjes en het label Voorraadafsluiting.
-   Vereffeningen die worden uitgevoerd tijdens de voorraadafsluiting, worden vertegenwoordigd door gestippelde rode pijlen die diagonaal van een ontvangst naar een uitgifte lopen.
-   Rode pijlen duiden op ontvangsttransacties die worden vereffend met de uitgiftetransactie die is gemaakt door het systeem.
-   De groene pijl staat voor de door het systeem gegenereerde ontvangsttransactie waarmee de oorspronkelijk geboekte uitgiftetransactie wordt vereffend

## <a name="weighted-average-with-marking"></a>Gewogen gemiddelde met markering
Markeren is een proces waarmee u een uitgiftetransactie aan een ontvangsttransactie kunt koppelen (of markeren). Markering kan plaatsvinden voor- of nadat een transactie is geboekt. U kunt markering gebruiken als u zeker wilt zijn van de juiste kosten van de voorraad wanneer de transactie wordt geboekt of wanneer de voorraad wordt afgesloten. 

De afdeling Klantenservice heeft een spoedorder van een belangrijke klant aangenomen. Omdat dit een spoedorder is, moet u meer voor dit artikel betalen om aan de vraag van de klant te voldoen. U moet er zeker van zijn dat de kosten van dit voorraadartikel worden weerspiegeld in de marge, of kosten van verkochte goederen, voor deze verkooporderfactuur. 

Wanneer de inkooporder wordt geboekt, wordt de voorraad ontvangen voor het bedrag van EUR 120,00. Dit verkooporderdocument is bijvoorbeeld aan de inkooporder gekoppeld voordat de pakbon of factuur wordt geboekt. De kosten van de verkochte goederen bedragen dan EUR 120,00 in plaats van de huidige gemiddelde kosten voor het artikel. Als de pakbon of de factuur van de verkooporder wordt geboekt voordat er wordt gemarkeerd, wordt de COGS geboekt tegen de lopende, gemiddelde kostprijs. 

Voordat de voorraad wordt afgesloten, worden deze twee transacties naar elkaar gemarkeerd. 

Een ontvangsttransactie wordt aan een uitgiftetransactie gekoppeld. Vervolgens wordt de waarderingsmethode voor de artikelmodelgroep van het artikel genegeerd en worden deze transacties met elkaar vereffend. 

U kunt een uitgiftetransactie aan een ontvangst koppelen voordat de transactie wordt geboekt. U kunt dit doen vanaf een verkooporderregel op de pagina Details verkooporder. De openstaande ontvangsttransacties kunnen worden bekeken op de pagina Markering. 

U kunt een uitgiftetransactie aan een ontvangst koppelen nadat de transactie is geboekt. U kunt een uitgiftetransactie voor een openstaande ontvangsttransactie voor een geïnventariseerd artikel afstemmen of markeren vanuit een geboekt voorraadcorrectiejournaal. 

In de onderstaande afbeelding worden de volgende transacties geïllustreerd:
-   1a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 10,00 per stuk.
-   1b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 10,00 per stuk.
-   2a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 20,00 per stuk.
-   2b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 20,00 per stuk.
-   3a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 25,00 per stuk.
-   4a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
-   4b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
-   5a. Fysieke uitgifte uit voorraad voor een hoeveelheid van 1 tegen een kostprijs van EUR 21,25 (lopend gemiddelde van bijgewerkte financiële en fysieke transacties).
-   5b. Financiële uitgifte uit voorraad voor een hoeveelheid van 1 is gekoppeld aan de voorraadontvangst 2b voordat de transactie is geboekt. Deze transactie wordt geboekt met een kostprijs van EUR 20,00.
-   6a. Fysieke uitgifte uit voorraad voor een hoeveelheid van 1 tegen een kostprijs van EUR 21,25 per stuk.
-   7. Voorraadafsluiting is uitgevoerd. Aangezien de bijgewerkte financiële transactie is gekoppeld aan een bestaande ontvangst, worden deze transacties met elkaar vereffend en wordt er geen correctie uitgevoerd.

De nieuwe gemiddelde kostprijs weerspiegelt het gemiddelde van de financieel en fysiek bijgewerkte transacties met USD 27,50. 

In het volgende diagram wordt voor deze reeks transacties het effect geïllustreerd van het kiezen van het gewogen gemiddelde voorraadmodel met markering. 

![Gewogen gemiddelde met markering](./media/weightedaveragewithmarking.gif) 

**Uitleg bij diagram**
-   Voorraadtransacties worden aangegeven met verticale pijlen.
-   Ontvangsten in voorraad worden aangegeven met verticale pijlen boven de tijdlijn.
-   Uitgiften uit voorraad worden aangegeven met verticale pijlen onder de tijdlijn.
-   Boven (of onder) elke verticale pijl wordt de waarde van de voorraadtransactie opgegeven in de indeling Quantity@Unitprice.
-   Een voorraadtransactiewaarde tussen haakjes geeft aan dat de voorraadtransactie fysiek naar de voorraad is geboekt.
-   Een voorraadtransactiewaarde zonder haakjes geeft aan dat de voorraadtransactie financieel naar de voorraad is geboekt.
-   Elke nieuwe ontvangst of uitgiftetransactie krijgt een nieuw label.
-   Elke verticale pijl heeft een opeenvolgende ID, zoals *1a*. De ID's geven de volgorde van voorraadtransactieboekingen op de tijdlijn aan.
-   Voorraadafsluitingen worden aangegeven met verticale rode streepjes en het label Voorraadafsluiting.
-   Vereffeningen door voorraadafsluitingen worden aangegeven met rode stippelpijlen die diagonaal van een ontvangst naar een uitgifte lopen.






