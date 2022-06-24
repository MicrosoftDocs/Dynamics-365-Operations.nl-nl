---
title: Vrijgeven naar magazijn
description: Dit artikel biedt informatie over het proces van het vrijgeven aan het magazijn. In het onderwerp worden entiteiten beschreven die worden gemaakt wanneer u een order vrijgeeft aan het magazijn en worden opties beschreven die u kunt gebruiken om het proces te starten.
author: Mirzaab
ms.date: 8/13/2021
ms.topic: article
ms.search.form: WHSReleaseToWarehouse, WHSReleaseToWarehouseSalesOrder, WHSReleaseToWarehouseTransferOrder, WHSLoadPlanningWorkbench, WHSWaveTemplateTable, WHSWorkTemplateTable, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-13
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: c3280b2e39d7af5ca99cad703cad6ecc7b307bff
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893173"
---
# <a name="release-to-warehouse"></a>Vrijgeven naar magazijn

[!include [banner](../../includes/banner.md)]

Dit artikel biedt informatie over het proces van het vrijgeven aan het magazijn. In het onderwerp worden entiteiten beschreven die worden gemaakt wanneer u een order vrijgeeft aan het magazijn en worden opties beschreven die u kunt gebruiken om het proces te starten.

## <a name="release-to-warehouse-overview"></a>Overzicht van vrijgeven naar magazijn

Vrijgave naar magazijn is het proces waarbij voorraad gereed wordt gemaakt voor verzending. Wanneer u een order vrijgeeft aan het magazijn, worden er door het systeem ladingsregels en zendingen gemaakt. Als automatische waveverwerking is ingesteld, worden er ook ladingen en vereist werk gemaakt. De configuratie van de betrokken entiteiten is afhankelijk van de systeeminstellingen. In deze sectie van het artikel worden de entiteiten besproken die zijn gemaakt tijdens het proces van het vrijgeven naar magazijn en de systeeminstellingen waarmee ze zijn gedefinieerd.

Een *zending* is een groep verkooporder- of transferorderregels voor dezelfde klant of hetzelfde afleveradres.

Een *lading* is een groep verkooporder- of transferorderregels die zijn gegroepeerd en die doorgaans worden verzonden in één truck, trein of via een andere transportmethode. Een lading kan uit een of meer zendingen bestaan. U kunt handmatig een lading maken door orderregels aan een nieuwe lading toe te voegen. In dit geval worden orderregels toegewezen aan de lading voordat het proces van het vrijgeven aan het magazijn wordt gestart en ze kunnen alleen worden vrijgegeven vanaf de pagina **Workbench ladingplanning**.

*Magazijnwerk* is een magazijnbewerking die wordt uitgevoerd door een magazijnmedewerker. Doorgaans bestaat dit magazijnwerk uit ten minste tweetal opeenvolgende acties: een magazijnwerknemer verzamelt voorhanden voorraad op de ene locatie en brengt de voorraad vervolgens naar een andere locatie.

Wanneer orders worden vrijgegeven naar het magazijn, worden er door het systeem *ladingsregels* gemaakt en worden deze gegroepeerd in zendingen. Met het consolidatieproces voor zendingen kunnen zendingen automatisch worden geconsolideerd tijdens het proces van vrijgave naar magazijn. Zie voor meer informatie [Beleidsregels voor consolidatie van zendingen](about-shipment-consolidation-policies.md).

Het systeem gebruikt *waves* om orderverzamelingswerk en ladingen voor verzending te maken. Er moet een *wavesjabloon* beschikbaar zijn voor het type wave dat u wilt maken en voor het magazijn van de orderregel. Wavesjablonen van het type *Verzending* worden gebruikt om artikelen te verzenden voor verkooporders en transferorders.

Elke wavesjabloon bevat *wavemethoden*. Met deze wavemethoden worden acties uitgevoerd, zoals het maken van werk voor de wave of het maken van ladingen. Een wavesjabloon voor zendingwaves kan bijvoorbeeld methoden bevatten voor het maken van ladingen, het toewijzen van regels aan waves, het maken van aanvullingen en het maken van verzamelwerk voor de wave. Met de wavesjabloon worden instellingen geactiveerd die definiëren hoe de wave wordt gegenereerd en verwerkt, welke stappen handmatig moeten worden uitgevoerd en welke automatisch plaatsvinden. Zie [Wavesjablonen](wave-templates.md) voor meer informatie. Afhankelijk van de configuratie van uw wavesjabloon wordt er dus automatisch een wave gemaakt, verwerkt en vrijgegeven wanneer u een order naar het magazijn vrijgeeft of worden sommige of alle acties handmatig uitgevoerd na de vrijgave naar magazijn.

Wanneer er een wave wordt verwerkt, maakt het systeem werk voor het verzamelen van orders op basis van een geschikte *werksjabloon* en *locatierichtlijn* en maakt dat werk beschikbaar op mobiele apparaten. De werksjabloon bepaalt hoe het werk wordt uitgevoerd voor elk magazijnproces en de locatierichtlijn geeft de verzamel- en neerzetlocaties aan voor de verplaatsing van voorraad. Zie voor meer informatie [Magazijnwerk beheren met werksjablonen en locatie-instructies](control-warehouse-location-directives.md).

> [!NOTE]
> Standaard worden waves in batchmodus verwerkt.

Tijdens de wave-verwerking wordt in het systeem gewoonlijk een nieuwe lading gemaakt voor elke zending waaraan geen lading is toegewezen. Als u wilt dat het systeem in plaats daarvan niet-toegewezen zendingen aan bestaande ladingen toewijst, kunt u de geavanceerde functionaliteit voor ladingopbouw van waves gebruiken. Zie [Geavanceerde ladingopbouw tijdens wave](advanced-load-building-during-wave.md) voor meer informatie.

Op de pagina's **Verkooporders** en **Transferorders** kunt u de entiteiten bekijken die voor orderregels zijn gemaakt tijdens het proces van vrijgave naar magazijn.

- Pagina **Verkooporders**:

    - Selecteer op het sneltabblad **Verkooporderregels** de optie **Magazijn** en selecteer vervolgens in het menu **Zendingsgegevens** de optie **Ladinggegevens** om de gerelateerde ladingen te selecteren of selecteer **Werkgegevens** om gerelateerde werkdetails te openen.
    - Selecteer op het sneltabblad **Regeldetails** het tabblad **Lading** om gerelateerde ladingen te bekijken.

- Pagina **Transferorders**:

    - Selecteer in het actievenster op het tabblad **Verzending** de optie **Zendingsgegevens** om gerelateerde zendingen te openen of selecteer **Ladinggegevens** om gerelateerde ladingen te openen.
    - Selecteer op het sneltabblad **Transferorderregels** de optie **Werkgegevens** om gerelateerde werkgegevens te openen.

Wanneer een order dus naar het magazijn wordt vrijgegeven, werkt de meest geautomatiseerde stroom als volgt:

1. Het systeem maakt een zending voor de order en een wave.
1. De wave wordt verwerkt.
1. het systeem maakt een lading en een werk-id.

Afhankelijk van wavesjablonen, werksjablonen en instellingen voor locatierichtlijnen moeten sommige stappen in deze stroom mogelijk handmatig worden uitgevoerd. De algehele stroom blijft echter hetzelfde.

U hebt verschillende mogelijkheden om een order vrij te geven naar het magazijn. U kunt de bewerking handmatig uitvoeren of u kunt een batchtaak instellen. In de resterende secties van dit artikel komen uitgebreid de verschillende manieren aan de orde waarop u een vrijgave naar een magazijnbewerking kunt uitvoeren.

## <a name="manual-release-to-the-warehouse-from-the-sales-orders-and-transfer-orders-pages"></a>Handmatige vrijgave naar het magazijn vanuit de pagina's Verkooporders en Transferorders

U kunt een order rechtstreeks vanaf de pagina **Verkooporders** of de pagina **Transferorders** vrijgeven naar het magazijn door **Vrijgave naar magazijn** te selecteren.

- Op de pagina **Verkooporders** bevindt de knop zich op het tabblad **Magazijn** van het actievenster.
- Op de pagina **Transfer** bevindt de knop zich op het tabblad **Verzenden** van het actievenster.

Vanaf de pagina **Verkooporders** kunt u meerdere verkooporders tegelijk vrijgeven.

## <a name="manual-release-to-the-warehouse-from-the-release-to-warehouse-pages"></a>Handmatige vrijgave naar het magazijn vanaf de pagina's Vrijgave naar magazijn

Het systeem biedt momenteel drie pagina's waarin u regels voor meerdere orders kunt controleren en deze kunt vrijgeven naar het magazijn:

- **Vrijgave naar magazijn** (**Magazijnbeheer \> Vrijgave naar magazijn \> Vrijgave naar magazijn**). Op deze pagina kunt u zowel met verkooporders als met transferorders werken. Via deze pagina verloopt de verwerking echter minder snel dan via de andere twee pagina's. Deze pagina wordt binnenkort afgeschaft.
- **Verkooporders vrijgeven naar magazijn** (**Magazijnbeheer \> Vrijgave naar magazijn \> Verkooporders vrijgeven naar magazijn**). Op deze pagina kunt u alleen met verkooporders werken. Deze pagina biedt betere prestaties dan de pagina **Vrijgave naar magazijn**.
- **Transferorders vrijgeven naar magazijn** (**Magazijnbeheer \> Vrijgave naar magazijn \> Transferorders vrijgeven naar magazijn**). Op deze pagina kunt u alleen met transferorders werken. Deze pagina biedt betere prestaties dan de pagina **Vrijgave naar magazijn**.

Alle drie de pagina's bieden soortgelijke functies, zoals in het resterende gedeelte van deze sectie wordt beschreven. Met al deze functies kunt u orderregels of hele orders selecteren en deze vervolgens vrijgeven naar het magazijn.

Elke pagina's bestaat uit een gedeelte bovenaan, waar u orderregels kunt selecteren, en een gedeelte onderaan, waar u de vrijgave naar het magazijnproces kunt starten. U kunt in het gedeelte bovenaan filters gebruiken om naar de verkooporderregels te zoeken die u wilt vrijgeven. De pagina **Vrijgave naar magazijn** biedt een apart tabblad voor verkoop- en transferorders in het bovenste gedeelte, terwijl op de andere twee pagina's slechts één type order wordt weergegeven.

De werkbalk in het bovenste gedeelte bevat de volgende knoppen waarmee u orderregels kunt selecteren die u naar het magazijn wilt vrijgeven:

- **Toevoegen**: selecteer een of meer orderregels in het bovenste gedeelte en selecteer vervolgens deze knop voor de regels in het onderste gedeelte.
- **Alles toevoegen**: voeg alle regels van het bovenste gedeelte toe aan het onderste gedeelte.
- **Order toevoegen**: selecteer een order en selecteer vervolgens deze knop om alle regels van die order toe te voegen aan het onderste gedeelte.

Wanneer u klaar bent met het toevoegen van regels aan het onderste gedeelte, markeert u elke regel die u wilt vrijgeven. Selecteer vervolgens **Vrijgave naar magazijn** op de werkbalk om deze regels vrij te geven naar het magazijn.

## <a name="manual-release-to-the-warehouse-from-the-load-planning-workbench-page"></a>Handmatig vrijgeven naar het magazijn vanaf de pagina Workbench ladingplanning

U kunt ook handmatig orders naar het magazijn vrijgeven via de pagina **Workbench ladingplanning**. Op deze pagina kunt u orderregels in ladingen ordenen en deze vervolgens vrijgeven naar het magazijn.

Ga naar **Magazijnbeheer \> Ladingen** om de pagina **Workbench ladingplanning** te openen. U kunt de pagina ook openen vanaf de pagina's **Verkooporders** en **Transferorders**. In het bovenste gedeelte van de pagina kunt u verkooporderregels selecteren op het tabblad **Verkoopregels** en transferorderregels op het tabblad **Transferregels** en deze regels vervolgens aan een nieuwe of bestaande lading toevoegen.

Het tabblad **Vraag en aanbod** in het actievenster bevat de volgende knoppen waarmee u orderregels in het bovenste gedeelte aan een lading kunt toevoegen:

- **Naar nieuwe lading**: selecteer een of meer orderregels in het bovenste gedeelte en selecteer vervolgens deze knop om een nieuwe lading te maken en die regels aan de lading toe te voegen.
- **Naar bestaande lading**: selecteer een of meer orderregels in het bovenste gedeelte en selecteer vervolgens deze knop om die regels aan een bestaande lading toe te voegen.
- **Gehele order naar nieuwe lading**: selecteer orders en selecteer vervolgens deze knop om een nieuwe lading te maken en voeg alle regels van die orders aan de lading toe.
- **Gehele order naar bestaande lading**: selecteer een order en selecteer vervolgens deze knop om alle regels van die order aan een bestaande lading toe te voegen.

In het onderste gedeelte kunt u de ladingen controleren die zijn gemaakt. Als u ladingen wilt vrijgeven naar het magazijn, selecteert u de ladingen en selecteert u vervolgens **Vrijgeven \> Vrijgave naar magazijn** op de werkbalk. Als u automatische waveverwerking gebruikt, omdat ladingen al aan orderregels zijn toegewezen, maakt het systeem zendingen en werk-id's wanneer de bewerking van de vrijgave naar het magazijn wordt uitgevoerd.

## <a name="automatic-release-to-the-warehouse"></a>Automatische vrijgave naar het magazijn

Als u orders automatisch wilt vrijgeven naar het magazijn, gebruikt u de functies **Verkooporders automatisch vrijgeven** en **Transferorders automatisch vrijgeven**.

Als u een batchtaak wilt instellen om verkooporders vrij te geven, volgt u deze stappen.

1. Ga naar **Magazijnbeheer \> Vrijgave naar magazijn \> Automatische vrijgave van verkooporders**.
1. Stel in het dialoogvenster **Verkooporders automatisch vrijgeven** op het sneltabblad **Parameters** de volgende velden in:

    - **Hoeveelheid voor vrijgave**: selecteer of de gehele hoeveelheid of slecht de fysiek gereserveerde hoeveelheid moet worden vrijgegeven naar het magazijn.
    - **Vrijgave van gedeeltelijk vrijgegeven orders toestaan**: geef op of resterende hoeveelheden voor gedeeltelijk vrijgegeven orders naar het magazijn moeten worden vrijgegeven.
    - **Reserveringen behouden bij mislukte vrijgave**: geef op of hoeveelheden die automatisch zijn gereserveerd voor een verkooporder, gereserveerd moeten blijven als het proces voor vrijgave naar magazijn mislukt.
    - **Groepsvrijgaven per klant**: geef op of het systeem de vrijgave van magazijnbewerkingen afzonderlijk voor elke klant moet verwerken of dat alle verkooporders tegelijk moeten worden vrijgeven. Als deze optie is ingesteld op *Ja*, worden alle verkooporderregels voor een geselecteerde klant verzameld, worden deze orders aan het magazijn vrijgegeven en wordt vervolgens de volgende klant verwerkt. Als deze optie is ingesteld op *Nee*, worden alle beschikbare verkooporderregels in één Vrijgave naar magazijn-bewerking vrijgegeven. Als u deze optie inschakelt, worden de prestaties en tolerantie van het Vrijgave naar magazijn-proces verbeterd. U moet echter voorzichtig zijn als u deze optie gebruikt in combinatie met wavesjablonen die zijn geconfigureerd voor het verwerken van waves bij vrijgave naar het magazijn omdat deze combinatie veel waves voor afzonderlijke klanten kan genereren, waarbij voor elke wave werk alleen voor die klant wordt gegenereerd. Als u werk wilt genereren waarin zendingen voor meerdere klanten worden gecombineerd, moet u de optie *Groepsvrijgaven per klant* uitschakelen of uw wavesjablonen configureren voor het gebruik van uitgestelde verwerking.
    - **Verwerking van vergrendelde orders**: selecteer hoe het systeem verkooporders moet verwerken die momenteel zijn vergrendeld omdat ze worden bewerkt door andere gebruikers of processen:

        - *Wachten tot orders zijn ontgrendeld*: het systeem moet wachten tot de orders zijn ontgrendeld voordat ze naar het magazijn worden vrijgegeven. In dit geval kan het proces van het vrijgeven naar het magazijn meer tijd in beslag nemen.
        - *Vergrendelde orders overslaan*: het systeem moet vergrendelde orders overslaan.

    - **Geldige ordertypen**: selecteer de typen verkooporders die u in de batch wilt opnemen.
    - **Kredietlimiettype**: selecteer of kredietlimieten moeten worden gecontroleerd tijdens het proces van het vrijgeven naar het magazijn en, als de controles moeten worden uitgevoerd, de transactiegegevens erin moeten worden opgenomen.

1. Als u wilt aangeven welke orders moeten worden verwerkt, selecteert u op het sneltabblad **Op te nemen records** de optie **Filter**. Er wordt een standaard querydialoogvenster weergegeven, waarin u selectiecriteria, sorteercriteria en joins kunt definiëren. De velden werken op dezelfde manier als bij andere typen query's in Microsoft Dynamics 365 Supply Chain Management.
1. Kies op het sneltabblad **Op de achtergrond uitvoeren** of de taak in de batchmodus moet worden uitgevoerd en/of stel een terugkeerpatroon in. De velden werken op dezelfde manier als bij andere typen [achtergrondtaken](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) in Supply Chain Management.
1. Selecteer **OK** om de instellingen toe te passen en het proces van het vrijgeven naar het magazijn te starten.

Als u een batchtaak wilt instellen om transferorders vrij te geven, volgt u deze stappen.

1. Ga naar **Magazijnbeheer \> Vrijgave naar magazijn \> Automatische vrijgave van overboekingsorders**.
1. Stel in het dialoogvenster **Transferorders automatisch vrijgeven** op het sneltabblad **Parameters** de volgende velden in:

    - **Hoeveelheid voor vrijgave**: selecteer of de gehele hoeveelheid of slecht de fysiek gereserveerde hoeveelheid moet worden vrijgegeven naar het magazijn.
    - **Vrijgave van gedeeltelijk vrijgegeven orders toestaan**: geef op of resterende hoeveelheden voor gedeeltelijk vrijgegeven orders naar het magazijn moeten worden vrijgegeven.
    - **Vrijgaven groeperen op doelmagazijn**: geef op of alle transferorders tegelijk moeten worden vrijgeven of dat transferorderregels moeten worden gegroepeerd op doelmagazijn en elke groep vervolgens afzonderlijk naar het magazijn moet worden vrijgeven.

1. Als u wilt aangeven welke orders moeten worden verwerkt, selecteert u op het sneltabblad **Op te nemen records** de optie **Filter**. Er wordt een standaard querydialoogvenster weergegeven, waarin u selectiecriteria, sorteercriteria en joins kunt definiëren. De velden werken op dezelfde manier als bij andere typen query's in Supply Chain Management.
1. Kies op het sneltabblad **Op de achtergrond uitvoeren** of de taak in de batchmodus moet worden uitgevoerd en/of stel een terugkeerpatroon in. De velden werken op dezelfde manier als bij andere typen [achtergrondtaken](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) in Supply Chain Management.
1. Selecteer **OK** om de instellingen toe te passen en het proces van het vrijgeven naar het magazijn te starten.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
