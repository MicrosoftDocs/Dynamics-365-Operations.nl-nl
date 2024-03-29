---
title: Veiligheidsvoorraadafhandeling voor items
description: Dit artikel heeft betrekking op het afhandelen van veiligheidsvoorraad en het instellen van een hoeveelheid veiligheidsvoorraad voor artikelen.
author: t-benebo
ms.date: 8/23/2021
ms.topic: article
ms.search.form: ReqSafetyKey, ReqItemTableSetup, ReqItemJournalName, ReqItemTable, EcoResProductDetailsExtended, ReqSafetyKeyDefaultDataWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: 70461ad1de94c984cb41e6b1d46af9e310a928d6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887394"
---
# <a name="safety-stock-fulfillment-for-items"></a>Afhandeling van veiligheidsvoorraad voor artikelen

[!include [banner](../includes/banner.md)]

Veiligheidsvoorraad duidt op een extra hoeveelheid van een artikel dat op voorraad wordt gehouden om het risico te verkleinen dat het artikel uitverkocht is. Veiligheidsvoorraad wordt gebruikt als een buffervoorraad voor het geval er verkooporders binnenkomen en de leverancier de extra artikelen niet kan leveren om te voldoen aan de gevraagde verzenddatum van de klant. Wanneer veiligheidsvoorraad wordt gebruikt om een verkooporder af te handelen, wordt de veiligheidsvoorraad kleiner. U kunt Hoofdplanning gebruiken om het veiligheidsniveau voor de voorraad automatisch te herstellen.

## <a name="set-up-safety-stock-levels-for-items"></a>Veiligheidsvoorraadniveaus voor artikelen instellen

Veiligheidsvoorraad wordt als onderdeel van de artikelbehoefteplanning ingesteld op de pagina **Artikelbehoefteplanning** onder **Vrijgegeven producten\>Plannen\>Behoefteplanning**.

In het veld **Minimum** voert u de veiligheidsvoorraad in die u voor het artikel wilt aanhouden. De waarde wordt uitgedrukt in voorraadeenheden. Als u dit veld leeg laat, is het standaardminimumvoorraadniveau gelijk aan nul. Dit veld is beschikbaar als u **Periode**, **Behoefte** of **Min./Max.** selecteert in de lijst **Bestelmethode**. De voorraadniveaulimiet geldt voor de beschikbare voorraad, wat betekent dat reserveringen en markeringen aanvullingen van de veiligheidsvoorraad kunnen genereren voordat de fysieke hoeveelheid onder het opgegeven minimumniveau valt.

> [!NOTE]
> U moet alle andere behoefteplanningsdimensies definiëren voordat u het veld **Minimum** kunt definiëren. Deze regel voorkomt dat tijdens de hoofdplanning een ongeldige planning wordt gebruikt. Deze situatie kan zich bijvoorbeeld voordoen als een dimensiegroep wordt uitgebreid met een extra behoefteplanningsdimensie waarvoor de minimum- en maximumvoorraadhoeveelheden nog niet zijn gedefinieerd.

U kunt minimumsleutels gebruiken om seizoensschommelingen in de vraag te verwerken. U kunt bijvoorbeeld het minimale voorraadniveau van een artikel buiten het hoofdseizoen verlagen en dit niveau in de andere maanden geleidelijk verhogen. U maakt een minimumsleutel via **Hoofdplanning\>Instelling\>Behoefteplanning\>Minimum-/maximumsleutels**. U geeft de minimumsleutel op om het veiligheidsvoorraadniveau seizoensgebonden aan te passen in het veld **Minimumsleutel** op de pagina **Artikelbehoefteplanning**.

## <a name="example-minimum-key"></a>Voorbeeld: Minimumsleutel

De volgende procedure is een voorbeeld van het instellen van een minimumsleutel voor de hogere seizoensvraag gedurende de lente- en zomermaanden.

1. Ga naar **Hoofdplanning \> Instellen \> Behoefteplanning \> Minimum-/maximumsleutels**.
1. Selecteer **Nieuw** om een minimum-/maximumsleutel te maken.
1. Voer in **het veld Minimum- of maximumsleutel** een ID in voor de sleutel. Voer in het veld **Naam** een naam voor de sleutel in.
1. Stel de optie **Ingangsdatum gebruiken** in op *Ja* en laat het veld **Ingangsdatum** leeg om de sleutel geldig te maken vanaf de eerste dag van het huidige jaar.

    > [!NOTE]
    > Met de combinatie van de instellingen **Ingangsdatum gebruiken** en **Ingangsdatum** kunt u de datum definiëren waarop de sleutel geldig is.
    >
    > - Wanneer de optie **Ingangsdatum** gebruiken is ingesteld op *Nee*, is de sleutel geldig vanaf de huidige datum of systeemdatum.
    > - Als de optie **Ingangsdatum gebruiken** is ingesteld op *Ja*, is de sleutel geldig vanaf de datum die is gedefinieerd in het veld **Ingangsdatum**.

1. Maak in de sectie **Perioden** 12 regels en stel de volgende waarden voor deze regels in:

    - **Wijzigen** – Wijs aan elke regel een uniek nummer toe van 1 tot en met 12. Dit veld geeft de incrementele wijziging in de tijdseenheid aan die wordt gedefinieerd door het veld **Eenheid**.
    - **Eenheid**: *maanden* selecteren voor elke regel.
    - **Einddatum**, **Einddatum** en **Maand**: deze velden worden automatisch ingesteld op basis van de instellingen **Wijzigen** en **Eenheid**. Maandelijkse perioden beginnen vanaf de eerste dag van het huidige jaar.
    - **Factor** - Voer in de waarden in die worden beschreven in de volgende tabel. Dit veld definieert de factor die u wilt vermenigvuldigen met de minimumvoorraad.

        | Regel (wijzigen) | Factor | Resultaat |
        |---|---|---|
        | 1–3 | 1 | De minimumvoorraad wordt gebaseerd op de instelling voor januari tot en met maart op de pagina **Artikelbehoefteplanning**. |
        | 4–5 | 2 | De minimumvoorraad wordt voor april en mei vermenigvuldigd met de factor 2. |
        | 6–8 | 2.5 | De minimumvoorraad wordt voor juni tot en met augustus vermenigvuldigd met de factor 2,5. |
        | 9–12 | 1 | De minimumvoorraad wordt voor september tot en met december teruggezet naar de instelling op de pagina **Artikelbehoefteplanning**. |

    Uw instellingen moeten nu op de instellingen in de volgende afbeelding lijken.

    ![Minimum- of maximumsleutelperioden.](media/min-max-key-periods.png "Minimum- of maximumsleutelperioden")

> [!NOTE]
> U kunt ook een wizard gebruiken om een minimum-/maximumsleutel in te stellen. Selecteer op de pagina **Minimum- of maximumsleutels** de wizard **Minimum- of maximumsleutels** om de wizard **Minimum-/maximumsleutels** te openen in het actievenster. De wizard helpt u stap voor stap bij het maken en instellen van de minimum-/maximumsleutel.

Als de behoefteplanningscode *Min./Max.* is, kunt u ook de maximale voorraadhoeveelheid opgeven die u voor een artikel wilt aanhouden. De waarde wordt ook uitgedrukt in voorraadeenheden. Als de geschatte beschikbare voorraad onder de minimumhoeveelheid uitkomt, wordt een geplande order gegenereerd om alle andere openstaande behoeften te vervullen en vervolgens het voorraadniveau weer op de opgegeven maximumhoeveelheid te brengen. Net als voor het veld Minimum moet u alle andere behoefteplanningsdimensies definiëren voordat u het veld **Maximum** kunt definiëren.

## <a name="example-minmax-coverage-code"></a>Voorbeeld: Min/Max behoefteplanningscode

De minimumhoeveelheid is 10 en de maximumhoeveelheid is 15. De huidige voorhanden voorraad is 4. De minimumhoeveelheidbehoefte is dan 6. Omdat de maximumhoeveelheid echter 15 is, wordt door de hoofdplanning een geplande order voor 11 artikelen gegenereerd.

Voor artikelen waarvoor een seizoensgebonden vraag geldt, moet u mogelijk verschillende maximumniveaus aanhouden. Hiervoor moet u **maximumsleutels** definiëren door naar **Hoofdplanning\>Instelling\>Behoefteplanning\>Minimum-/ maximumsleutels** te gaan. Vul het veld **Maximumsleutel** op de pagina **Artikelbehoefteplanning** in. U kunt de informatie over de veiligheidsvoorraadniveaus weergeven die via minimumsleutels op het tabblad **Min./Max.** op de pagina **artikelbehoefteplanning** zijn gedefinieerd. U moet ervoor zorgen dat voor een bepaalde periode de minimale en maximale waarden gesynchroniseerd blijven.

## <a name="safety-stock-fulfillment"></a>Afhandeling van veiligheidsvoorraad

Met de parameter **Minimum behalen** kunt u de datum of periode selecteren waarvoor het voorraadniveau moet voldoen aan de hoeveelheid die u hebt opgegeven in het veld **Minimum**. Dit veld is beschikbaar als u **Periode**, **Behoefte** of **Min./Max.** selecteert in de lijst **Bestelmethode**.

Als er **minimumsleutels** worden gebruikt, schakelt u het selectievakje **Minimumperioden** in als u wilt voldoen aan het minimumvoorraadniveau voor alle perioden die zijn gedefinieerd voor de minimumsleutel. Als u dit selectievakje uitschakelt, wordt alleen voldaan aan de minimumvoorraad voor de huidige periode.

In het volgende scenario ziet u hoe deze parameter werkt en wat de verschillen tussen de waarden zijn.

> [!NOTE]
> Voor alle afbeeldingen in dit artikel vertegenwoordigt de x-as de voorraad en de y-as het aantal dagen. Met de balken wordt het voorraadniveau aangegeven en de pijlen staan voor transacties, zoals verkooporderregels, inkooporderregels of geplande orders.

[![Gangbaar scenario voor afhandeling van veiligheidsvoorraad.](media/Scenario1.png)](media/Scenario1.png)

De parameter **Minimum behalen** kan de volgende waarden hebben:

### <a name="todays-date"></a>Datum van vandaag

Aan de opgegeven minimumhoeveelheid wordt voldaan op de datum waarop de hoofdplanning wordt uitgevoerd. Hoewel dit onrealistisch kan zijn vanwege de levertijd, wordt zo snel mogelijk geprobeerd te voldoen aan de limiet voor het veiligheidsniveau.

[![Vereiste voor datum van vandaag.](media/TodayReq.png)](media/TodayReq.png)

De geplande order P1 wordt gemaakt voor de datum van vandaag om de beschikbare voorraad op deze datum boven het veiligheidsvoorraadniveau te brengen. De verkooporderregels S1 tot en met S3 blijven het voorraadniveau verlagen. Geplande orders P2 tot en met P4 worden gegenereerd op basis van de hoofdplanning, zodat voor het voorraadniveau na elke verkooporderbehoefte weer de veiligheidslimiet wordt hersteld.

Wanneer de behoefteplanningscode **Behoefte** wordt gebruikt, worden meerdere geplande orders gemaakt. Het is altijd verstandig om de behoefteplanning **Periode** of **Min./Max.** te gebruiken voor gewilde artikelen en materialen, om de aanvulling te bundelen. In de volgende afbeelding ziet u een voorbeeld van de behoefteplanningscode **Periode**.

[![Periode. Datum van vandaag.](media/TodayPeriod.png)](media/TodayPeriod.png)

In de volgende afbeelding ziet u een voorbeeld van de behoefteplanningscode **Min/Max**.

[![Min./Max. Datum van vandaag.](media/TodayMinMax.png)](media/TodayMinMax.png)

### <a name="todays-date--procurement-time"></a>Datum van vandaag + levertijd

Aan de opgegeven minimumhoeveelheid wordt voldaan op de datum waarop de hoofdplanning wordt uitgevoerd, plus de inkoop- of productiedoorlooptijd. Deze tijd is inclusief veiligheidsmarges. Als het artikel onderdeel is van een handelsovereenkomst en het selectievakje **Handelsovereenkomsten zoeken** is ingeschakeld op de pagina **Parameters hoofdplanning**, wordt geen rekening gehouden met de levertijd in de handelsovereenkomst. Levertijden worden overgenomen uit de instellingen van de artikelbehoefteplanning of van het artikel.

Met deze afhandelingsmodus worden plannen met minder vertragingen en minder geplande orders gemaakt, ongeacht de ingestelde behoefteplanningsgroep voor het artikel.

In de volgende afbeelding ziet u het resultaat van het plan als de behoefteplanningscode **Vereiste** of **Periode** is.

[![Vereiste of Periode. Datum van vandaag en doorlooptijd.](media/TodayPLTReq.png)](media/TodayPLTReq.png)

In de volgende afbeelding ziet u het resultaat van het plan als de behoefteplanningscode **Min/Max** is.

[![Min./Max. Datum van vandaag en doorlooptijd.](media/TodayPLTMinMax.png)](media/TodayPLTMinMax.png)

### <a name="first-issue"></a>Eerste uitgifte

Aan de opgegeven minimumhoeveelheid wordt voldaan op de datum waarop de beschikbare voorraad onder het minimumniveau valt, zoals in de volgende afbeelding wordt weergegeven. Zelfs als de beschikbare voorraad onder het minimumniveau valt op de datum waarop de hoofdplanning wordt uitgevoerd, wordt met **Eerste uitgifte** niet geprobeerd dit verschil te dekken tot de volgende vereiste binnenkomt.

In de volgende afbeelding ziet u een voorbeeld van de behoefteplanningscode **Vereiste**.

[![Een artikel plannen met de behoefteplanningscode Vereiste en de afhandeling Eerste uitgifte.](media/FirstIssueReq.png)](media/FirstIssueReq.png)

In de volgende afbeelding ziet u een voorbeeld van de behoefteplanningscode **Periode**.

[![Een artikel plannen met de behoefteplanningscode Periode en de afhandeling Eerste uitgifte.](media/FirstIssuePeriod.png)](media/FirstIssuePeriod.png)

In de volgende afbeelding ziet u een voorbeeld van de behoefteplanningscode **Min/Max**.

[![Een artikel plannen met de behoefteplanningscode Min./Max. en de afhandeling Eerste uitgifte.](media/FirstIssueMinMax.png)](media/FirstIssueMinMax.png)

Op de datum waarop de hoofdplanning wordt uitgevoerd, genereren **Datum van vandaag** en **Datum van vandaag + levertijd** de aanvulling onmiddellijk als de beschikbare voorraad al onder de limiet voor het veiligheidsniveau ligt. **Eerste uitgifte** wacht tot de volgende uitgiftetransactie, bijvoorbeeld een verkooporder- en stuklijstregelbehoefte, voor het artikel en triggert vervolgens de aanvulling op de datum van deze transactie.

Zoals in de onderstaande afbeelding wordt weergegeven, bieden **Datum van vandaag** en **Eerste uitgifte** precies hetzelfde resultaat op de datum waarop de hoofdplanning wordt uitgevoerd, als de beschikbare voorraad niet onder de veiligheidsvoorraadlimiet ligt.

[![Niet ondergrens.](media/ReqFirstIssue.png)](media/ReqFirstIssue.png)

Als de beschikbare voorraad niet onder de veiligheidsvoorraadlimiet ligt, biedt **Datum van vandaag + levertijd** het volgende resultaat op de datum waarop de hoofdplanning wordt uitgevoerd omdat de afhandeling wordt uitgesteld tot het einde van de levertijd.

![Afhandeling uitgesteld tot het einde van de aanschaffings doorlooptijd.](media/ReqTodayLT.png)

### <a name="coverage-time-fence"></a>Time fence voor behoefteplanning

Er wordt voldaan aan de opgegeven minimumhoeveelheid tijdens de periode die is opgegeven in het veld **Time fence voor behoefteplanning**. Deze optie is handig wanneer op basis van de hoofdplanning beschikbare voorraad bestemd voor echte orders, zoals verkopen of overdrachten, niet mag worden gebruikt om het veiligheidsniveau te handhaven. In een toekomstige versie is deze aanvullingsmethode echter niet meer nodig en wordt deze optie afgeschaft.

## <a name="plan-safety-stock-replenishment-for-first-expired-first-out-fefo-items"></a>Aanvulling van veiligheidsvoorraad plannen voor FEFO-artikelen (First Expired, First Out)

Op elk moment wordt de voorraadontvangst met de laatste vervaldatum gebruikt voor de veiligheidsvoorraad, zodat werkelijke vraag, zoals verkoop- of stuklijstregels, kan worden afgehandeld op basis van de FEFO-volgorde.

In het volgende scenario ziet u hoe dit werkt.

[![FEFO-scenario.](media/FEFOScenario.png)](media/FEFOScenario.png)

Wanneer de planning wordt uitgevoerd, wordt met de voorhanden voorraad voldaan aan de eerste verkooporder en wordt een aanvullende inkooporder gebruikt voor de resterende hoeveelheid.

[![FEFO 1.](media/FEFO1.png)](media/FEFO1.png)

Er wordt een geplande order gemaakt om ervoor te zorgen dat de veiligheidslimiet wordt hersteld voor de beschikbare voorraad.

[![FEFO 2.](media/FEFO2.png)](media/FEFO2.png)

Wanneer de tweede verkooporder wordt gepland, wordt de eerder gemaakte geplande order voor de veiligheidsvoorraad gebruikt om deze hoeveelheid te dekken. De veiligheidsvoorraad is dus voortdurend in beweging.

[![FEFO 3.](media/FEFO3.png)](media/FEFO3.png)

Tot slot wordt nog een geplande order gemaakt om de veiligheidsvoorraad te dekken.

[![FEFO 4.](media/FEFO4.png)](media/FEFO4.png)

Alle batches verlopen op volgorde en er worden geplande orders gemaakt om de veiligheidsvoorraad na verloop aan te vullen.

## <a name="how-master-planning-handles-the-safety-stock-constraint"></a>Hoe de hoofdplanning omgaat met de beperking van veiligheidsvoorraad

De veiligheidsvoorraad wordt in het systeem bijgehouden als een type vereiste, net als verkoopregels of stuklijstvereisten. U kunt de regel voor de vereiste van de veiligheidsvoorraad op de pagina **Nettobehoeften** weergeven als u het standaardfilter voor de kolom **Type behoefte** verwijdert.

De prioriteit van het afhandelen van transacties voor de vereiste van de veiligheidsvoorraad wordt verlaagd als wordt vastgesteld dat dit vertragingen veroorzaakt bij het voldoen aan werkelijke vraag, zoals verkoopregels, stuklijstregels, overdrachtsvereisten of vraagprognoseregels. Anders heeft het handhaven van de beschikbare voorraad boven het niveau van de veiligheidsvoorraad dezelfde prioriteit als alle andere soorten vraag. Zo treden er geen vertragingen voor echte transacties op en wordt voorkomen dat veiligheidsvoorraad te veel en te vroeg wordt aangevuld.

Tijdens de behoefteplanningsfase van de hoofdplanning geldt de lagere prioriteit voor aanvulling van de veiligheidsvoorraad niet meer. Voorhanden voorraad kan worden gebruikt vóór alle andere vraagsoorten. Tijdens de berekening van vertraging wordt er nieuwe logica toegevoegd om de vertraagde verkoopregels, stuklijstregelbehoeften en alle andere soorten vraag te analyseren en te bepalen of een tijdige levering mogelijk is als de veiligheidsvoorraad wordt gebruikt. Als wordt vastgesteld dat vertragingen kunnen worden beperkt met veiligheidsvoorraad, wordt veiligheidsvoorraad gebruikt om te voorzien in de behoeften op de verkoop- of stuklijstregels en wordt vervolgens de veiligheidsvoorraad aangevuld.

Als het plan of artikel niet is ingesteld voor de berekening van vertraging, heeft de beperking van veiligheidsvoorraad dezelfde prioriteit als andere soorten vraag. Dit betekent dat er een reserve voor voorhanden voorraad en andere beschikbare voorraad bestaat voor andere soorten vraag.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Het veiligheidsvoorraadjournaal gebruiken om de minimumbehoefteplanning voor artikelen bij te werken](safety-stock-journal.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
