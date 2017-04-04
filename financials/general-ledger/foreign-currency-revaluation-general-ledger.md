---
title: Herwaardering van vreemde valuta voor Grootboek
description: Dit onderwerp biedt een overzicht van de volgende opties voor het herwaarderingsproces grootboek vreemde valuta - instelling, het gestart, berekening voor het verwerken en hoe u de herwaarderingstransacties omkeren indien nodig.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CurrencyLedgerGainLossAccount
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62153
ms.assetid: 842e8561-560f-4cc6-8668-70cca60b1ba3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 5d6d13fe44eef7766b4dcaf274c3522bce3da816
ms.lasthandoff: 03/31/2017


---

# <a name="foreign-currency-revaluation-for-general-ledger"></a>Herwaardering van vreemde valuta voor Grootboek

Dit onderwerp biedt een overzicht van de volgende opties voor het herwaarderingsproces grootboek vreemde valuta - instelling, het gestart, berekening voor het verwerken en hoe u de herwaarderingstransacties omkeren indien nodig. 

Als onderdeel van een periode-einde vereisen de boekhoudconventies dat grootboekrekeningsaldo's in vreemde valuta worden geherwaardeerd met verschillende typen wisselkoersen (huidig, historisch, gemiddeld, enzovoort). Eén boekhoudconventie vereist bijvoorbeeld dat betreffende activa en passiva worden geherwaardeerd tegen de huidige wisselkoers, vaste activa tegen de historische wisselkoers nb winst- en verliesrekeningen tegen het maandelijkse gemiddelde. Grootboekherwaardering van de vreemde valuta kan worden gebruikt om de balans en de winst- en verliesrekeningen te herwaarderen. 

> [!NOTE]
> Herwaardering van vreemde valuta is ook beschikbaar in (AR) voor klanten en leveranciers (AP). Als u deze modules worden gebruikt, moeten de openstaande transacties worden geherwaardeerd met behulp van de herwaardering van vreemde valuta in die modules. De herwaardering van vreemde valuta voor AR en AP maakt een journaalregel in het grootboek om de gerealiseerde winst of het gerealiseerde verlies aan te geven, zodat subjournalen en het grootboek kunnen worden afgestemd. Omdat de herwaardering van vreemde valuta voor AR en AP journaalregels in het grootboek kan maken, moeten de klant- en de leveranciershoofdrekeningen worden uitgesloten van de herwaardering van vreemde valuta voor het grootboek. 

Wanneer u het herwaarderingsproces uitvoert, wordt het saldo in elke hoofdrekening in een vreemde valuta geherwaardeerd. De niet-gerealiseerde winst- en verliestransacties die worden gemaakt tijdens het herwaarderingsproces worden door het systeem gegenereerd. Twee transacties kunnen worden gemaakt, één voor de valuta voor boekhouding en een tweede voor de aangiftevaluta, indien van toepassing. Elke vermelding boekhouding wordt geboekt naar de niet-gerealiseerde winst of verlies en de hoofdrekening die worden geherwaardeerd.

## <a name="prepare-to-run-foreign-currency-revaluation"></a>Voorbereiding van herwaardering van vreemde valuta
Voordat u het herwaarderingsproces kunt uitvoeren, zijn de volgende instellingen vereist.

-   Op de pagina **Hoofdrekening**:
-   Selecteer **Herwaardering van vreemde valuta** als de hoofdrekening moet worden geherwaardeerd in het grootboek. Schakel deze optie uit als de hoofdrekening niet moet worden geherwaardeerd (zoals voor AR en AP indien geherwaardeerd in de subjournalen).
-   Voer het **Wisselkoerstype** in als de hoofdrekening voor herwaardering is gemarkeerd. Dit type wisselkoers wordt gebruikt voor de herwaardering van de hoofdrekening. Er is een afzonderlijk veld **Wisselkoerstype voor financiële rapportage** beschikbaar voor financiële rapportage. De twee velden worden niet gesynchroniseerd dat verschillende wisselkoerstypen kunnen worden gebruikt voor herwaardering en financiële rapportage.

-   Op de pagina **Grootboek**:
-   Geef het **Wisselkoerstype** op. Als het wisselkoerstype niet is gedefinieerd voor de hoofdrekening, wordt dit wisselkoerstype gebruikt tijdens de herwaardering van vreemde valuta.
-   Geef de rekeningen op voor gerealiseerde winst, gerealiseerd verlies, niet-gerealiseerde winst en niet-gerealiseerd verlies voor herwaardering van valuta. Rekeningen voor gerealiseerde winst en gerealiseerd verlies worden gebruikt voor het vereffenen van AR- en AP-transacties en rekeningen voor niet-gerealiseerde winst en niet-gerealiseerd verlies worden gebruikt voor het herwaarderen van openstaande transacties en grootboekhoofdrekeningen.

-   Op de pagina **Rekeningen voor valutaherwaardering**:
-   Selecteer verschillende valutaherwaarderingsrekeningen voor elke valuta en elk bedrijf. Als u geen rekeningen hebt gedefinieerd, worden rekeningen van de pagina **Grootboek** gebruikt.

## <a name="process-foreign-currency-revaluation"></a>Herwaardering van vreemde valuta verwerken
Nadat de configuratie is voltooid, kunt u de pagina **Herwaardering van vreemde valuta** gebruiken om de saldi van de hoofdrekeningen te herwaarderen. U kunt het proces in realtime uitvoeren of inplannen om het in batch uit te voeren. 

De pagina **Herwaardering van vreemde valuta** geeft de historie van elk herwaarderingsproces weer, wanneer het proces is uitgevoerd, welke criteria zijn gedefinieerd, een koppeling met het boekstuk dat voor de herwaardering is gemaakt en een record als een eerdere herwaardering is omgekeerd. U kunt het herwaarderingsproces uitvoeren door de knop **Herwaardering van vreemde valuta** te selecteren. 

De waarden voor **Begindatum** en **Einddatum** definiëren het datuminterval voor het berekenen van het saldo in vreemde valuta dat wordt geherwaardeerd. Wanneer u winst- en verliesrekeningen herwaardeert, wordt het totaal van alle transacties binnen het datuminterval geherwaardeerd. Wanneer u balansrekeningen herwaardeert, wordt de Begindatum genegeerd. In plaats daarvan wordt het te herwaarderen saldo gedefinieerd door van het begin van het boekjaar tot de Einddatum te gaan. 

De **datum van koers** kunnen worden gebruikt voor het definiëren van de datum waarop de wisselkoers standaard moet worden ingesteld. U kunt bijvoorbeeld de saldi tussen de datum bereik van januari 1 tot en met 31 januari herwaardeert, maar de wisselkoers die is gedefinieerd voor 1 februari. 

Selecteer welke hoofdrekeningen worden geherwaardeerd: Alle, Balans of Winst en verlies. Alleen hoofdrekeningen gemarkeerd voor herwaardering (op de pagina van de hoofd-account) opnieuw gewaardeerd. Als u verder beperken het bereik van hoofdrekeningen wilt, gebruikt u de Records **om op te nemen** tabblad om een bereik van hoofdrekeningen of afzonderlijke hoofdrekeningen. 

Herwaardering kan worden uitgevoerd voor een of meer rechtspersonen. De zoekopdracht wordt alleen de rechtspersonen waartoe u toegang hebt weergegeven. Selecteer de rechtspersonen waarvoor u wilt uitvoeren van de herwaardering. 

De herwaardering kan voor een of meer vreemde valuta worden uitgevoerd. De zoekopdracht bevat alle valuta's die zijn geboekt in het datumbereik relevant zijn voor het type hoofdrekening (balans of winst en verlies) voor de rechtspersonen die zijn geselecteerd om te herwaarderen. De valuta voor boekhouding worden opgenomen in de lijst, maar niets worden geherwaardeerd als de valuta voor boekhouding is geselecteerd. 

Instellen **voorbeeld vóór het boeken** naar **Ja** als u wilt controleren van het resultaat van de herwaardering van het grootboek. Het voorbeeld in het grootboek wijkt af van de simulatie van de AR en AP herwaardering van vreemde valuta. De simulatie in AR en AP is een rapport, maar het grootboek is een voorbeeld dat kan worden geboekt, zonder dat het herwaarderingsproces opnieuw uitvoeren. De resultaten van het voorbeeld kunnen naar Microsoft Excel worden geëxporteerd om de historie te bewaren voor hoe de bedragen zijn berekend. U kunt geen batchverwerking gebruiken als u een voorbeeld van de herwaarderingsresultaten wilt bekijken. Vanuit het voorbeeld heeft de gebruiker de optie om de resultaten van alle rechtspersonen te boeken met de knop **Boeken**. Als er een probleem is met de resultaten voor een rechtspersoon, heeft de gebruiker ook de optie om een subset van de rechtspersonen te boeken met de knop **Te boeken rechtspersonen selecteren**. 

Nadat de herwaardering van vreemde valuta voltooid is, wordt een record worden gemaakt voor het bijhouden van de geschiedenis van elke serie.  Een afzonderlijke record gemaakt voor elke rechtspersoon en boekingslaag.

## <a name="calculate-unrealized-gainloss"></a>Niet-gerealiseerde winst/verlies berekenen
De niet-gerealiseerde winst- of verliestransacties worden voor de grootboekherwaardering op een andere manier gemaakt dan in het AR- en AP-herwaarderingsproces. In AR en AP wordt de vorige herwaardering volledig omgekeerd (ervan uitgaande van de transactie nog niet is vereffend) en een nieuwe herwaarderingtransactie gemaakt voor de niet-gerealiseerde winst/verlies op basis van de nieuwe wisselkoers. Daarom wordt elke afzonderlijke transactie in AR en AP geherwaardeerd. In het grootboek wordt de vorige herwaardering niet omgekeerd. In plaats daarvan wordt een transactie gemaakt voor de delta tussen het saldo van de hoofdrekening, met inbegrip van eventuele eerdere herwaarderingen van bedragen en de nieuwe waarde op basis van de wisselkoers voor de datum van koers. 

**Voorbeeld** de volgende saldi bestaan voor de hoofdrekening 110110.

|            |                    |                        |                       |
|------------|--------------------|------------------------|-----------------------|
| **Datum**   | **Grootboekrekening** | **Transactiebedrag** | **Boekhoudingsbedrag** |
| 20 januari | 110110 (Kas)      | EUR 500 (Debet)        | USD 1000 (Debet)      |

De hoofdrekening wordt geherwaardeerd op 31 januari.  De niet-gerealiseerde winst/verlies wordt als volgt berekend.

|                                             |                                            |                                  |                                    |                             |
|---------------------------------------------|--------------------------------------------|----------------------------------|------------------------------------|-----------------------------|
| **Huidig saldo in transactievaluta** | **Huidig saldo in valuta voor boekhouding** | **Wisselkoers voor herwaardering** | **Nieuw bedrag in valuta voor boekhouding** | **Niet-gerealiseerde winst/verlies**    |
| EUR 500                                     | USD 1000                                   | 166.6667                         | EUR 833,33 (500 x 1,666667)        | 166,67 verlies (833,33 – 1000) |

De volgende vermelding in de boekhouding wordt gemaakt.

|            |                          |           |            |
|------------|--------------------------|-----------|------------|
| **Datum**   | **Grootboekrekening**       | **Debet** | **Krediet** |
| 31 januari | 110110 (Kas)            |           | 166.67     |
| 31 januari | 801400 (Niet-gerealiseerd verlies) | 166.67    |            |

Er worden geen nieuwe transacties geboekt voor de maand februari.  De hoofdrekening wordt geherwaardeerd op 28 februari.

|                                             |                                            |                                  |                                    |                             |
|---------------------------------------------|--------------------------------------------|----------------------------------|------------------------------------|-----------------------------|
| **Huidig saldo in transactievaluta** | **Huidig saldo in valuta voor boekhouding** | **Wisselkoers voor herwaardering** | **Nieuw bedrag in valuta voor boekhouding** | **Niet-gerealiseerde winst/verlies**    |
| EUR 500                                     | USD 833,33 (1000 - 166,67)                 | 250.0000                         | USD 1250 (500 x 2,5)               | 416,67 winst (1250 – 833,33) |

De volgende vermelding in de boekhouding wordt gemaakt.

|             |                          |           |            |
|-------------|--------------------------|-----------|------------|
| **Datum**    | **Grootboekrekening**       | **Debet** | **Krediet** |
| 28 februari | 110110 (Kas)            | 416.67    |            |
| 28 februari | 801600 (Niet-gerealiseerde winst) |           | 416.67     |

## <a name="reverse-foreign-currency-revaluation"></a>Herwaardering van vreemde valuta omkeren
Als u de herwaarderingtransactie moet omkeren, selecteert u de knop **Transactie omkeren** op de pagina **Herwaardering van vreemde valuta**. Er wordt een nieuw historisch record voor herwaardering van vreemde valuta gemaakt om de historische audittrail te onderhouden voor wanneeer de herwaardering heeft plaatsgevonden of is omgekeerd. 

U kunt de resultaten van de herwaardering van uit de datumvolgorde omkeren, maar mogelijk moet u ook een meer actuele herwaardering zodat het correcte saldo voor elke hoofdrekening geherwaardeerde terugboeken. De omkeringen kunnen verouderd order optreden omdat er geen manier om te bepalen welke hoofdrekeningen worden geherwaardeerd en de frequentie van wanneer deze worden geherwaardeerd. Een organisatie kan bijvoorbeeld voor kiezen hun contante hoofdrekeningen op kwartaalbasis, maar alle andere hoofdrekeningen maandelijks herwaardeerd.


