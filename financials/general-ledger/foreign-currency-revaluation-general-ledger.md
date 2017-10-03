---
title: Herwaardering van vreemde valuta voor Grootboek
description: 'Dit onderwerp bevat een overzicht van de volgende onderdelen van het herwaarderingsproces van vreemde valuta voor het grootboek: instellingen, het proces uitvoeren, berekening voor het proces en het omkeren van de herwaarderingstransacties, indien nodig.'
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CurrencyLedgerGainLossAccount
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62153
ms.assetid: 842e8561-560f-4cc6-8668-70cca60b1ba3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 8031f5b4be79b0642134898db60188311d1ca6d2
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017

---

# <a name="foreign-currency-revaluation-for-general-ledger"></a>Herwaardering van vreemde valuta voor Grootboek

[!include[banner](../includes/banner.md)]


Dit onderwerp bevat een overzicht van de volgende onderdelen van het herwaarderingsproces van vreemde valuta voor het grootboek: instellingen, het proces uitvoeren, berekening voor het proces en het omkeren van de herwaarderingstransacties, indien nodig. 

Als onderdeel van een periode-einde vereisen de boekhoudconventies dat grootboekrekeningsaldo's in vreemde valuta worden geherwaardeerd met verschillende typen wisselkoersen (huidig, historisch, gemiddeld, enzovoort). Eén boekhoudconventie vereist bijvoorbeeld dat betreffende activa en passiva worden geherwaardeerd tegen de huidige wisselkoers, vaste activa tegen de historische wisselkoers nb winst- en verliesrekeningen tegen het maandelijkse gemiddelde. Grootboekherwaardering van de vreemde valuta kan worden gebruikt om de balans en de winst- en verliesrekeningen te herwaarderen. 

> [!NOTE]
> Herwaardering van vreemde valuta is ook beschikbaar in Leveranciers en Klanten. Als u deze modules gebruikt, moeten de openstaande transacties worden geherwaardeerd met behulp van de herwaardering van vreemde valuta in die modules. De herwaardering van vreemde valuta voor AR en AP maakt een journaalregel in het grootboek om de gerealiseerde winst of het gerealiseerde verlies aan te geven, zodat subjournalen en het grootboek kunnen worden afgestemd. Omdat de herwaardering van vreemde valuta voor AR en AP journaalregels in het grootboek kan maken, moeten de klant- en de leveranciershoofdrekeningen worden uitgesloten van de herwaardering van vreemde valuta voor het grootboek. 

Wanneer u het herwaarderingsproces uitvoert, wordt het saldo in elke hoofdrekening in een vreemde valuta geherwaardeerd. De niet-gerealiseerde winst- en verliestransacties die worden gemaakt tijdens het herwaarderingsproces worden door het systeem gegenereerd. Er kunnen twee transacties worden gemaakt, één voor de valuta voor boekhouding en een tweede voor de aangiftevaluta, indien van toepassing. Elke journaalregel wordt geboekt naar de niet-gerealiseerde winst/verlies en de hoofdrekening die wordt geherwaardeerd.

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

De **Datum van koers** kan worden gebruikt om de datum te definiëren waarvoor de wisselkoers standaard moet worden ingesteld. U kunt bijvoorbeeld de saldi herwaarderen tussen het datumbereik van 1 januari tot 31 januari, maar de wisselkoers gebruiken die is gedefinieerd voor 1 februari. 

Selecteer welke hoofdrekeningen worden geherwaardeerd: Alle, Balans of Winst en verlies. Alleen hoofdrekeningen die zijn gemarkeerd voor herwaardering (op de pagina Hoofdrekening), worden geherwaardeerd. Als u het bereik van hoofdrekeningen verder wilt beperken, gebruikt u het tabblad **Op te nemen records** om een bereik van hoofdrekeningen of afzonderlijke hoofdrekeningen te definiëren. 

Het herwaarderingsproces kan voor een of meer rechtspersonen worden uitgevoerd. Met de zoekopdracht worden alleen de rechtspersonen weergegeven waartoe u toegang hebt. Selecteer de rechtspersonen waarvoor u het herwaarderingsproces wilt uitvoeren. 

De herwaardering kan voor een of meer vreemde valuta worden uitgevoerd. De zoekopdracht omvat alle valuta's die zijn geboekt binnen het datumbereik dat relevant is voor het type hoofdrekening (balans of winst en verlies) voor de rechtspersonen die zijn geselecteerd voor herwaardering. De valuta voor boekhouding wordt opgenomen in de lijst, maar er wordt niets geherwaardeerd als de valuta voor boekhouding wordt geselecteerd. 

Stel **Bekijken alvorens te boeken** in op **Ja** als u het resultaat van de herwaardering van het grootboek wilt controleren. Het voorbeeld in het grootboek wijkt af van de simulatie van de herwaardering van vreemde valuta voor AR en AP. De simulatie in AR en AP is een rapport, maar het grootboek heeft een voorbeeld dat kan worden geboekt, zonder dat het herwaarderingsproces opnieuw moet worden uitgevoerd. De resultaten van het voorbeeld kunnen naar Microsoft Excel worden geëxporteerd om de historie te bewaren voor hoe de bedragen zijn berekend. U kunt geen batchverwerking gebruiken als u een voorbeeld van de herwaarderingsresultaten wilt bekijken. Vanuit het voorbeeld heeft de gebruiker de optie om de resultaten van alle rechtspersonen te boeken met de knop **Boeken**. Als er een probleem is met de resultaten voor een rechtspersoon, heeft de gebruiker ook de optie om een subset van de rechtspersonen te boeken met de knop **Te boeken rechtspersonen selecteren**. 

Nadat het herwaarderingsproces van vreemde valuta is voltooid, wordt een record gemaakt om de historie voor elke uitvoering bij te houden.  Er wordt een afzonderlijke record gemaakt voor elke rechtspersoon en boekingslaag.

## <a name="calculate-unrealized-gainloss"></a>Niet-gerealiseerde winst/verlies berekenen
De niet-gerealiseerde winst- of verliestransacties worden voor de grootboekherwaardering op een andere manier gemaakt dan in het AR- en AP-herwaarderingsproces. In AR en AP wordt de vorige herwaardering volledig omgekeerd (ervan uitgaande van de transactie nog niet is vereffend) en een nieuwe herwaarderingtransactie gemaakt voor de niet-gerealiseerde winst/verlies op basis van de nieuwe wisselkoers. Daarom wordt elke afzonderlijke transactie in AR en AP geherwaardeerd. In het grootboek wordt de vorige herwaardering niet omgekeerd. In plaats daarvan wordt een transactie gemaakt voor de delta tussen het saldo van de hoofdrekening, inclusief alle vorige herwaarderingsbedragen, en de nieuwe waarde op basis van de wisselkoers voor de Datum van koers. 

**Voorbeeld** De volgende saldi zijn aanwezig voor hoofdrekening 110110.

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

U kunt de resultaten van de verouderde herwaarderingsvolgorde omkeren, maar mogelijk moet u ook een meer recente herwaardering omkeren om de juiste saldi voor elke geherwaardeerde hoofdrekening te garanderen. Omkeringen kunnen verouderd raken omdat er geen manier is om te regelen welke hoofdrekeningen zijn geherwaardeerd en de frequentie waarmee ze zijn geherwaardeerd. Een organisatie kan er bijvoorbeeld voor kiezen om de contante hoofdrekeningen elk kwartaal te herwaarderen, maar alle andere hoofdrekeningen maandelijks.




