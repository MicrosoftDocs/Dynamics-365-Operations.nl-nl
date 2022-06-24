---
title: Indirecte kosten boeken
description: In dit artikel wordt uitgelegd hoe u indirecte kosten boekt, kostengroepen maakt en knooppunten toevoegt aan het kostenblad voor indirecte kosten.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: CostSheetDesigner, BOMCostGroup, ProjCategory, CostingVersion, CostSheetCalculationFactor
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 04af10760ec50d60cbbc31c233109dffb786933c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868426"
---
# <a name="indirect-cost-posting"></a>Indirecte kosten boeken

Indirecte kosten zijn kosten die niet direct zijn gerelateerd aan één activiteit in het productieproces. Voorbeelden zijn administratiekosten, zoals salarissen van werknemers, kosten van de boekhoudafdeling en overheadkosten, zoals huur, voorzieningen en machinekosten.

## <a name="calculating-indirect-costs"></a>Indirecte kosten berekenen

Microsoft Dynamics 365 Finance biedt geen automatische manier om het tarief voor indirecte kosten te berekenen. U moet uw indirecte kosten bepalen, codes voor indirecte kosten maken en het tarief voor alle indirecte kosten in het kostenblad bijhouden.

Het exacte proces dat wordt gebruikt voor het berekenen van indirecte kosten kan enigszins verschillen per bedrijf. Over het algemeen bestaat het proces echter uit de volgende basisstappen:

1. Een lijst met indirecte kosten maken die in productie moeten worden toegerekend. Deze lijst kan huur, administratieve onkosten, boekhoudingskosten en juridische kosten bevatten. De lijst moet niet grondstof- of arbeidskosten bevatten die in productieroutes worden toegerekend.
2. Alle indirecte kosten opsommen. U kunt gelijksoortige typen indirecte kosten groepen of van elkaar gescheiden houden. Alle geconfigureerde indirecte kosten kunnen verschillende hoofdrekeningen hebben die worden gebruikt om naar het grootboek te boeken.
3. De indirecte kosten vergelijken met een factor, die ook wel de absorptiebasis wordt genoemd. U kunt elke gewenste factor kiezen. Hieronder vindt u een aantal gangbare voorbeelden:

    - Omzet
    - Totale hoeveelheid die wordt geproduceerd
    - Insteltijd
    - Uitvoeringstijd

    U kunt de periode selecteren waarvoor u de indirecte kosten wilt berekenen, bijvoorbeeld maandelijks, per kwartaal of jaarlijks. De som van uw indirecte kosten en de som van uw factor moeten voor dezelfde tijd gelden. De volgende formule wordt gebruikt om het indirecte kostprijstarief te berekenen:

    *Indirect kostprijstarief* = *Totale indirecte onkosten* &divide; *Totale factor*

4. Indirecte-kostengroepen maken.
5. De kostprijsberekening configureren met uw tarieven.
6. De kosten voor de indirecte kosten in de kostprijsberekeningsversie bijhouden.

> [!NOTE]
> U kunt de module **Kostprijsboekhouding** gebruiken om kosten te verzamelen en uw overhead vanuit verschillende bronnen, zoals productie, projecten en het grootboek, te bepalen. Zie [Kostprijsboekhouding](/cost-accounting/cost-accounting-home-page.md) voor meer informatie.

> [!IMPORTANT]
> Verschillende wettelijke instanties hebben richtlijnen gepubliceerd over de typen kosten die als indirecte kosten of overheadkosten in de kosten van uw eindproducten kunnen worden opgenomen. Voordat u indirecte kosten gaat configureren, is het raadzaam om contact op te nemen met uw accountant en lokale regelgeving raadpleegt om er zeker van te zijn dat u zich aan alle regelgeving houdt.

## <a name="create-cost-groups-for-indirect-costs"></a>Kostengroepen maken voor indirecte kosten

U moet ten minste één kostengroep maken voor gebruik voor indirecte kosten. Er is geen limiet voor het aantal kostengroepen dat u kunt gebruiken. Overweeg hoe u uw kosten berekent en of er verschillende tarieven voor verschillende typen kosten zijn. Stel dat uw organisatie voedingsproducten produceert. Sommige grondstoffen en eindproducten zijn droge goederen waarvoor één indirecte kostenpost voor magazijnbeheer bestaat. Andere grondstoffen en eindproducten worden gekoeld en hebben hogere indirecte kosten. In dit geval wilt u mogelijk twee kostengroepen maken: **Overhead droog materiaal** en **Overhead gekoeld materiaal**.

Volg deze stappen om een kostengroep voor indirecte kosten te maken.

1. Ga naar **Productiebeheer &gt; Instellingen &gt; Routes &gt; Routegroepen**.
2. Selecteer **Nieuw** om een groep te maken.
3. Voer in het veld **Kostengroep** een unieke naam in voor de kostengroep, bijvoorbeeld **MATOVH**.
4. Voer in het veld **Naam** een beschrijving in voor de kostengroep, bijvoorbeeld **Materiaaloverhead**.
5. Selecteer **Indirect** in het veld **Kostengroeptype**.
6. Optioneel: selecteer **Vaste kosten** of **Variabele kosten** in het veld **Gedrag**.

## <a name="configure-the-costing-sheet-for-indirect-costs"></a>Het kostenblad voor indirecte kosten configureren

Nadat u een of meer kostengroepen hebt gemaakt, kunt u het kostenblad met indirecte kosten configureren en de berekening definiëren. Mogelijk wilt u indirecte kosten in het kostenblad groeperen. Als u indirecte kosten wilt groeperen, kunt u een optionele koptekst in het kostenblad maken. U moet minimaal één knooppunt maken voor elke kostengroep in het kostenblad. Voor elke kostengroep voor indirecte kosten kunt u nog een berekening van indirecte kosten toevoegen.

### <a name="indirect-cost-node-types"></a>Typen knooppunten voor indirecte kosten

In deze sectie worden de verschillende typen knooppunten voor indirecte kosten beschreven.

#### <a name="surcharge"></a>Toeslag

**Toeslag** is een van de meest algemene typen indirecte kosten. Het berekent een kostenpercentage op basis van de absorptiebasis van kosten in de productieorder. U definieert de basis voor absorptie door de kostengroepen te selecteren die zijn gekoppeld aan uw materiaal- of tijdcomponenten in het kostenblad.

Een toeslag van drie procent kan bijvoorbeeld worden toegevoegd aan de productiekosten voor alle grondstoffen in een productieorder.

#### <a name="rate"></a>Tarief

Indirecte kosten van het type **Tarief** worden gebruikt om een vast bedrag aan kosten aan de productieorder toe te voegen op basis van een absorptiebasis van kosten in de productieorder. Het tarief kan worden gebaseerd op een van de drie subtypes:

- **Proces**: het tarief wordt gebaseerd op de uitvoeringstijd in de route.
- **Instelling**: het tarief wordt gebaseerd op de instellingstijd in de route.
- **Hoeveelheid**: het tarief is gebaseerd op de geproduceerde hoeveelheid.

U definieert de basis voor absorptie door de kostengroepen te selecteren die zijn gekoppeld aan de materiaal- of tijdcomponenten in het kostenblad.

Aan elke productieorder wordt bijvoorbeeld een vast bedrag van 2,00 euro toegevoegd op basis van de uitvoeringstijd in de route voor de arbeidskostengroep in uw kostenblad.

#### <a name="output-unit-based"></a>Op basis van uitvoereenheid

Indirecte kosten van het type **Op basis van uitvoereenheid** worden berekend door het bedrag op het sneltabblad **Tarief** van het kostenblad te vermenigvuldigen met het geselecteerde subtype. U kunt de hoeveelheid, het gewicht of het volume van het afgewerkte goed selecteren als de vermenigvuldigingsfactor voor de indirecte kosten.

U gebruikt bijvoorbeeld de hoeveelheid om een afschrijving van 1,50 EUR per machine te berekenen voor elke geproduceerde hoeveelheid. In een ander voorbeeld gebruikt u het volume om 2,00 EUR te berekenen voor het volume aan ruimte dat de eindproducten innemen in uw koeleenheden.

#### <a name="input-unit-based"></a>Op basis van invoereenheid

Indirecte kosten van het type **Op basis van invoereenheid** worden berekend door de hoeveelheid grondstoffen die in een productieorder wordt verbruikt, te vermenigvuldigen met een bedrag. U kunt het gewicht of volume van de invoer in de productieorder gebruiken om het totaal te berekenen. U kunt de berekening beperken tot een deel van de materialen door een of meer kostengroepen te selecteren op het sneltabblad **Absorptiebasis** van het kostenblad.

U gebruikt bijvoorbeeld het invoervolume voor een specifieke kostengroep die is gekoppeld aan gekoelde producten om 1,00 EUR aan de productieorder toe te voegen.

### <a name="create-a-total-node-for-indirect-costs-in-the-costing-sheet"></a>Een knooppunt Totaal voor indirecte kosten in het kostenblad maken

Volg deze stappen om een knooppunt Totaal voor indirecte kosten in het kostenblad te maken.

1. Ga naar **Kostenbeheer &gt; Instelling voor boekhoudingbeleid indirecte kosten &gt; Kostenblad**.
2. Selecteer in de structuur een knooppunt dat de kosten van geproduceerde goederen vertegenwoordigt.
3. Selecteer **Nieuw** om een knooppunt te maken.
4. Selecteer in het veld **Knooppunttype selecteren** de waarde **Totaal**.
5. Geef in het veld **Code** een unieke id voor het knooppunt op, zoals **Productieoverheads**.
6. Schakel het selectievakje **Koptekst** in.
7. Schakel het selectievakje **Totaal** in.
8. Selecteer **OK**.

### <a name="create-an-indirect-cost-group-node-in-the-costing-sheet"></a>Een knooppunt voor een indirecte-kostengroep in het kostenblad maken

Volg deze stappen om een knooppunt voor een indirecte-kostengroep in het kostenblad te maken.

1. Ga naar **Kostenbeheer &gt; Instelling voor boekhoudingbeleid indirecte kosten &gt; Kostenblad**.
2. Selecteer in de structuur het knooppunt waaronder u de indirecte kosten wilt maken. Selecteer bijvoorbeeld het knooppunt Totaal voor **Productieoverhead**.
3. Selecteer **Nieuw** om een knooppunt te maken.
4. Selecteer **Kostengroep** in het veld **Knooppunttype selecteren**.
5. Geef in het veld **Code** een unieke id voor het knooppunt op, zoals **TRANSP**.
6. Voer in het veld **Omschrijving** een korte omschrijving in, zoals **Transportoverhead**.
7. Selecteer **OK**.
8. Selecteer in het veld **Kostengroep** de kostengroep, zoals **OVH1: Transportoverhead**.

### <a name="create-a-surcharge-indirect-cost"></a>Indirecte kosten voor een toeslag maken

Volg deze stappen om indirecte kosten voor een toeslag in uw kostenblad te maken.

1. Ga naar **Kostenbeheer &gt; Instelling voor boekhoudingbeleid indirecte kosten &gt; Kostenblad**.
2. Selecteer in de structuur het knooppunt voor de indirecte-kostengroep waaronder u de indirecte kosten wilt maken. Selecteer bijvoorbeeld het knooppunt Totaal voor **TRANSP - Transportoverhead**.
3. Selecteer **Nieuw** om een knooppunt te maken.
4. Selecteer in het veld **Knooppunttype selecteren** de waarde **Toeslag**.
5. Geef in het veld **Code** een unieke id voor het knooppunt op, zoals **Transporttoeslag**.
6. Selecteer **OK**.
7. Selecteer in het veld **Subtype** de optie **Totaal**.
8. Selecteer op het sneltabblad **Absorptiebasis** de optie **Nieuw** om een nieuwe kostencode te maken.
9. Selecteer in het veld **Code** een kostengroep voor het berekenen van de toeslag.
10. Optioneel: herhaal stap 8 tot en met 9 voor elke extra kostengroep die u voor de berekening wilt gebruiken.
11. Selecteer op het sneltabblad **Toeslag** de optie **Nieuw** om een tarief te maken.
12. Selecteer in het veld **Versie** de kostprijsberekeningsversie waaraan u de toeslag wilt toevoegen.
13. Optioneel: voer in het veld **Locatie** een locatie in waarop de toeslag moet worden toegepast.
14. Voer in het veld **Percentage** het percentage in dat moet worden berekend in productieorders vanuit de kostengroepen die zijn gedefinieerd op het sneltabblad **Absorptiebasis**.
15. Selecteer op het sneltabblad **Grootboekboekingen** de hoofdrekening die u wilt gebruiken voor **Geraamde indirect geabsorbeerde kosten**, **Geraamde kosten van verbruikte indirecte kosten, OHW**, **Indirect geabsorbeerde kosten** en **Kosten van verbruikte indirecte kosten, OHW**.
16. Optioneel: geef op het sneltabblad **Financiële dimensies** de financiële dimensies op die standaard moeten worden opgegeven voor transacties wanneer deze naar het grootboek worden geboekt.

In de voorgaande procedure wordt aangegeven hoe u indirecte kosten maakt van het type **Toeslag**. Vergelijkbare stappen worden gebruikt om andere typen indirecte kosten te maken. In de volgende secties worden de verschillen voor elk type beschreven.

#### <a name="rate"></a>Tarief

- Selecteer **Tarief** in plaats van **Toeslag** in stap 4.
- Selecteer **Proces**, **Instellingen** of **Hoeveelheid** in plaats van **Totaal** in stap 7.
- Gebruik in stap 11 het sneltabblad **Tarief** in plaats van het sneltabblad **Toeslag**.
- Voer in stap 14 in plaats van een percentage in het veld **Percentage** een bedrag in het veld **Bedrag** in.

#### <a name="output-unit-based"></a>Op basis van uitvoereenheid

- Selecteer in stap 4 **Op basis van uitvoereenheid** in plaats van **Toeslag**.
- Selecteer **Hoeveelheid**, **Gewicht** of **Volume** in plaats van **Totaal** in stap 7.
- Sla stap 8 t/m 10 over.
- Gebruik in stap 11 het sneltabblad **Tarief** in plaats van het sneltabblad **Toeslag**.

#### <a name="input-unit-based"></a>Op basis van invoereenheid

- Selecteer in stap 4 **Op basis van invoereenheid** in plaats van **Toeslag**.
- Selecteer **Gewicht** of **Volume** in plaats van **Totaal** in stap 7.
- Gebruik in stap 11 het sneltabblad **Tarief** in plaats van het sneltabblad **Toeslag**.
