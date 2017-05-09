---
title: Opties voor het plannen van bewerkingen
description: Dit onderwerp beschrijft de opties voor het plannen van bewerkingen. U kunt het plannen van bewerkingen gebruiken om een algemene schatting te geven voor de duur van het productieproces.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProdSchedule
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 198123
ms.assetid: d680d7be-da64-4132-89fe-ad2fa59afb77
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 68cac68e1ea3db35b44c91f2c1901abf2aa521be
ms.lasthandoff: 03/31/2017


---

# <a name="operations-scheduling-options"></a>Opties voor het plannen van bewerkingen

[!include[banner](../includes/banner.md)]


Dit onderwerp beschrijft de opties voor het plannen van bewerkingen. U kunt het plannen van bewerkingen gebruiken om een algemene schatting te geven voor de duur van het productieproces.

Bewerkingsplanning berekent de volgende informatie voor een productieorder:

-   De begin- en einddatums worden voor de productieorder en elke bewerking ingesteld.
-   Resources worden aan bewerkingen toegewezen.

De manier waarop de productieplanningen worden berekend, wordt bepaald door verschillende instellingen. U kunt deze instellingen opgeven op de pagina **Bewerkingsplanning**. Hier volgt een omschrijving van de planningsopties.

## <a name="operations-scheduling"></a>Bewerkingsplanning
### <a name="scheduling-direction"></a>Planningsrichting

De planningsrichting is cruciaal voor het planningsproces. Een productie kan vanaf elke datum voorwaarts of achterwaarts worden gepland, afhankelijk van de tijd- en planningsvereisten.

-   **Voorwaarts plannen ** – U kunt de productie zo plannen dat deze zo vroeg mogelijk begint. De productie kan vandaag, morgen of op een specifieke datum in de toekomst van start gaan. De productie moet op een zo vroeg mogelijke datum beginnen en wordt vooruit gepland naar een zo vroeg mogelijke einddatum.
-   **Achterwaarts plannen** – U kunt de productie zo plannen dat deze zo laat mogelijk begint. De planning is gebaseerd op de datum waarop de productie moet zijn voltooid en telt achterwaarts naar de laatst mogelijke datum dat de productie kan worden begonnen zonder de gestelde deadline te missen.

De volgende opties zijn beschikbaar:

-   **Verder vanaf vandaag** - Vooruit gepland vanaf de huidige datum. (De huidige datum is de systeemdatum.)
-   **Verder vanaf gepland begin** - Vanaf een eerdere begindatum wordt er vooruit gepland. Als er niet eerder is gepland, is de planningsrichting voorwaarts vanaf de huidige datum.
-   **Verder vanaf planningsdatum** - Er wordt vooruit gepland vanaf de datum die is opgegeven in het veld **Planningsdatum**. Als u geen planningsdatum opgeeft, is de planningsrichting vooruit vanaf de huidige datum.
-   **Terug vanaf leveringsdatum** - Er wordt achteruit gepland vanaf de datum die is opgegeven voor de productieorder. Als u deze optie selecteert en er geen leveringsdatum is opgegeven, wordt de leveringsdatum ingesteld op de huidige datum.
-   **Terug vanaf gepland einde** - Er wordt achteruit gepland vanaf een eerder berekende einddatum. Als er nog niet is gepland, wordt de einddatum op de huidige datum ingesteld.
-   **Terug vanaf planningsdatum** - Er wordt achteruit gepland vanaf de datum die is opgegeven in het veld **Planningsdatum**. Als u geen planningsdatum opgeeft, wordt de huidige datum gebruikt. Terug vanaf planningsdatum wordt berekend voor de productieorder wanneer er voor het laatst een behoefte is berekend. Als er geen datum voor de productieorder is opgegeven, wordt de huidige systeemdatum gebruikt.
-   **Terug vanaf vertragingsdatum** - Achteruit plannen vanaf de vertragingsdatum die is berekend voor de productieorder wanneer er voor het laatst een behoefte is berekend. Als er geen vertragingsdatum voor de productieorder is opgegeven, wordt de huidige systeemdatum gebruikt.
-   **Zoals laatste planning** - Voor de planning van bewerkingen en taken worden de geselecteerde planningsrichting en -datum opgeslagen. Daarom kunt u deze optie selecteren voor achtereenvolgende planningen. Als er nog niet is gepland voor de productieorder, wordt er terug gepland vanaf de huidige systeemdatum.
-   **Verder vanaf morgen** - Er wordt vooruit gepland vanaf de huidige datum plus één dag.
-   **Verder vanaf vorige taak** - Deze optie is alleen relevant voor taakplanning. Als u deze planningsrichting selecteert voor de planning van bewerkingen, wordt de productieorder vooruit gepland vanaf de huidige datum. Bij taakplanning wordt een planning gemaakt voor één taak en worden alle andere taken voor de productie in overeenstemming hiermee gepland op basis van die taak.
-   **Achteruit vanaf vorige taak** - Deze optie is alleen relevant voor taakplanning. Als u deze planningsrichting selecteert voor de planning van bewerkingen, worden geplande orders terug gepland vanaf de huidige datum. Bij taakplanning wordt een planning gemaakt voor één taak en worden alle andere taken voor de productie in overeenstemming hiermee gepland op basis van die taak.

### <a name="scheduling-date"></a>Planningsdatum

Deze datum wordt gebruikt voor de planningsrichtingen **Verder vanaf planningsdatum** en **Terug vanaf planningsdatum**. Planning is terug of verder vanaf deze datum. Zie voor meer informatie de vorige sectie "Planningsrichting".

### <a name="recalculate-bom-levels"></a>Stuklijstniveaus bijwerken

Wanneer u **Stuklijstniveaus bijwerken** selecteert, worden de stuklijstniveaus (BOM) opnieuw berekend om de juiste planningsvolgorde te garanderen.

## <a name="limitations"></a>Beperkingen
### <a name="finite-capacity"></a>Eindige capaciteit

De planning is afhankelijk van de beschikbaarheid van de resources die nodig zijn om de productie te voltooien. Als er onvoldoende capaciteit is, kunnen de productieorders worden uitgesteld of zelfs gestopt. Als eindige capaciteit wordt toegepast op de bewerkingsplanning, worden bestaande capaciteitsreserveringen op de resources in overweging genomen en wordt die capaciteit als niet beschikbaar beschouwd. De productieorder wordt gepland op basis van de beschikbaarheid van de capaciteit van de benodigde resources. Bewerkingsplanning gebruikt de opgegeven volgorde van bewerkingen om de volgorde van bewerkingen in de productieroute te bepalen. Bewerkingsplanning reserveert capaciteit op de resourcegroepen op basis van de bewerkingstijden die op de productieroute zijn gedefinieerd. De capaciteit van de resourcegroepen is gelijk aan de som van de beschikbare capaciteiten voor alle resources in de resourcegroepen.

### <a name="finite-material"></a>Eindig materiaal

De planning is ook afhankelijk van de beschikbaarheid van de materialen die nodig zijn voor de productie. Een tekort aan onderdelen kan ook tot productievertraging leiden. Planning kan ook worden gebaseerd op het gebruik van materialen. Geef alleen de materialen op die beschikbaar moeten zijn voor productie in plaats van de materialen die niet van kritiek belang zijn. Dit type planning wordt plannen met beperkt materiaal genoemd. Wanneer u eindige materialen opgeeft, wordt de productie gepland op basis van de beschikbaarheid van materialen. **Opmerking:** Bij optimalisatie op basis van zowel capaciteit als materialen wordt de productie zo berekend dat aan beide beperkingen wordt voldaan. Er wordt rekening gehouden met de beschikbaarheid van capaciteit en materialen en het starten van de bewerkingen van de productieorder kan niet worden gepland totdat de capaciteit en materialen op hetzelfde moment en in de vereiste hoeveelheden beschikbaar zijn. Schakel dit selectievakje in als er bij de planning rekening mee moet worden gehouden dat de hoeveelheid materialen beperkt is. Als de hoeveelheid materialen beperkt is, wordt er rekening gehouden met de behoefteplanning van het materiaal voor die tijd. Met andere woorden, er wordt bij de planning rekening gehouden met de vertragingsdatums die worden berekend voor de artikelen. Bij de planning worden grondstoffen gereserveerd en wordt de huidige productie geëxplodeerd. Als er meermaals wordt gepland, wordt er alleen bij de eerste planning een explosie uitgevoerd en worden reserveringen gemaakt. Als u wijzigingen aanbrengt in de productiestuklijst of -route, wordt bij de volgende planning een explosie uitgevoerd. Voor de explosie wordt aangenomen dat de materialen op dezelfde dag nodig zijn. Aangezien de productie niet is gepland op het tijdstip van de explosie van de hoofdplanning, wordt de huidige datum gebruikt als de beste schatting voor de datum waarop de artikelen beschikbaar komen. Bij de explosie wordt gecontroleerd of de artikelen beschikbaar zijn. Als de artikelen beschikbaar zijn, kan er aan de productiebehoefte worden voldaan. Als de artikelen niet beschikbaar zijn op de huidige datum, wordt een geplande order gegenereerd en een tegenboekingsselectie gemaakt voor de geplande order. Als automatische fiattering is ingesteld voor de geplande order, wordt de geplande order automatisch gefiatteerd voor aankoop of productie. De productiestatus wordt automatisch gewijzigd in de status die is opgegeven in het veld **Gevraagde productiestatus** van het dialoogvenster **Behoefteplanningsgroepen**. Als het selectievakje is uitgeschakeld, wordt ervan uitgegaan dat de materialen altijd beschikbaar zijn. Daarom wordt bij de planning geen rekening gehouden met de vraag of de materialen beschikbaar zijn op het gewenste moment.

### <a name="finite-property"></a>Beperking

Schakel dit selectievakje in als bij de taakplanning rekening moet worden gehouden met eventuele vereisten voor eigenschappen.

### <a name="keep-production-unit"></a>Productie-eenheid behouden

Selecteer of de planningsengine alleen bronnen moet plannen die reeds op de productie-eenheid gespecificeerd zijn.

### <a name="keep-warehouse-from-resource"></a>Magazijn behouden van resource

Selecteer of de planningsengine alleen bronnen moet plannen die gekoppeld zijn aan het invoermagazijn dat op de bron is opgegeven.

## <a name="references"></a>Verwijzingen
### <a name="schedule-references"></a>Verwijzingen plannen

Als er verwijzingen afhankelijk zijn van productieorders, staan deze ook bekend als subproducties. De subproducties kunnen als onderdeel van de planning van een productieorder worden gepland. Schakel dit selectievakje in als het plannen van subproducties moet worden gebaseerd op het plannen van de hoofdproductie. In relatie tot de hoofdproductie worden bovenliggende producties vooruit gepland en onderliggende achteruit. U kunt verwijzingen naar productieorders weergeven in het veld **Verwijzingsniveau** op de pagina **Productieorders**.

### <a name="synchronize-references"></a>Verwijzingen synchroniseren

U kunt verwijzingen synchroniseren met de productieorder. Als deze optie is geselecteerd, worden de datums van de subproducties verschoven en afgestemd wanneer wijzigingen worden aangebracht in de planning van de productieorder. Als een productieorder een of meer subproducties heeft, kunt u deze beter tegelijk met de subproducties plannen. In dat geval kan de hoofdproductie pas kan worden gestart nadat de bijbehorende subproducties zijn voltooid. Schakel daarom dit selectievakje in als het plannen van subproducties moet worden gebaseerd op de begin- en eindtijden van de geselecteerde productie. U kunt dit selectievakje alleen inschakelen als het selectievakje** Verwijzingen plannen** ook is geselecteerd.

## <a name="cancellation"></a>Annulering
### <a name="cancel-queue-time"></a>Wachttijd annuleren

Schakel dit selectievakje in als u de wachttijd wilt uitsluiten van de planning.

### <a name="cancel-setup"></a>Insteltijd annuleren

Schakel dit selectievakje in als u de insteltijd wilt uitsluiten van de planning.

### <a name="cancel-process"></a>Uitvoeringstijd annuleren

Schakel dit selectievakje in als u de uitvoeringstijd wilt uitsluiten van de planning.

### <a name="cancel-overlap"></a>Overlapping annuleren

Schakel dit selectievakje in als u de overlappingstijd wilt uitsluiten van de planning.

### <a name="cancel-transport"></a>Transport annuleren

Schakel dit selectievakje in als u de transporttijd wilt uitsluiten van de planning.

## <a name="set-default"></a>Standaardwaarden instellen
U kunt de huidige waarden als standaardwaarden opslaan. Hiervoor zijn er twee opties:

-   Als mijn standaard instellen
-   Als standaard instellen voor iedereen


<a name="see-also"></a>Zie ook
--------

[Bewerkingsplanning](operations-scheduling.md)




