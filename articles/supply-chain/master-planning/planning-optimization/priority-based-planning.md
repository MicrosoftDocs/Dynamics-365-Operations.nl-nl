---
title: Op prioriteit gebaseerde planning
description: In dit artikel wordt de functie van op prioriteit gebaseerde planning van Microsoft Dynamics 365 Supply Chain Management beschreven.
author: t-benebo
ms.date: 10/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 4997ba123f105f683daaa6b29fe8c5ee72cb47cb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873806"
---
# <a name="priority-based-planning"></a>Op prioriteit gebaseerde planning

[!include [banner](../../includes/banner.md)]

In dit artikel wordt de functie van op prioriteit gebaseerde planning van Microsoft Dynamics 365 Supply Chain Management beschreven. Met deze functie wordt ondersteuning toegevoegd voor vraaggestuurde planning. Dit is één stap van DDMRP (Demand Driven Material Requirements Planning). Met op prioriteit gebaseerde planning kunnen tijdens planningsoptimalisatie geplande orders worden gegenereerd die worden gestuurd door planningsprioriteiten in plaats van op basis van behoeftedatums.

Met op prioriteit gebaseerde planning kunt u de prioriteit van aanvullingsorders bepalen, zodat voorrang wordt verleend aan urgente vraag boven minder belangrijke vraag. Er wordt bijvoorbeeld voorrang verleend aan een voorraadaanvullingsorder boven een standaardaanvullingsorder. Het systeem kan automatisch grotere orders opsplitsen in kleinere orders, waarbij orderregels op prioriteit worden gegroepeerd. Alle orders met een hoge prioriteit kunnen vervolgens eerst worden verwerkt.

Zie de volgende video voor een snel overzicht van deze functie: [Planningsoptimalisatie-ondersteuning voor op prioriteit gebaseerde planning in Dynamics 365 Supply Chain Management](https://youtu.be/GmMHzFETTQc).

## <a name="turn-on-priority-based-planning-in-your-system"></a>Op prioriteit gebaseerde planning in uw systeem inschakelen

Voordat u deze functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en in te schakelen. Schakel in de werkruimte **Functiebeheer** de functie als volgt in:

- **Module:** *Hoofdplanning*
- **Functienaam:** *Prioriteitsgestuurde MRP-ondersteuning voor Planningsoptimalisatie*

## <a name="where-and-how-planning-priorities-are-assigned"></a>Waar en hoe planningsprioriteiten worden toegewezen

Informatie over *Planningsprioriteit* met betrekking tot vraag en aanbod is de basis voor op prioriteit gebaseerde planning. Met planningsprioriteit wordt het belang van een vraag- of aanbodregel bepaald. Dit wordt in Planningsoptimalisatie gebruikt wanneer het veld **Behoefteplanningscode** is ingesteld op *Prioriteit*.

De planningsprioriteit is meestal een getal tussen 0 (nul) en 100, waarbij 0 voor het grootste belang staat. De prioriteit wordt weergegeven en ingesteld in het veld **Planningsprioriteit**. U vindt dit veld op de volgende pagina's: **Vraagprognoseregels**, **Verkooporderdetails**, **Inkooporderdetails**, **Transferorderdetails** en **Details geplande order**.

Wanneer het veld **Behoefteplanningscode** voor het desbetreffende artikel of de desbetreffende behoefteplanningsgroep wordt ingesteld op *Prioriteit*, wordt met Planningsoptimalisatie het aanbod in balans gebracht met de vraag door middel van een vraaggestuurde benadering door de planningsprioriteit te berekenen en voor elk vrijgegeven product de waarden mee te nemen die zijn ingesteld voor de velden **Minimum**, **Bestelpunt** en **Maximum** op de pagina **Artikelbehoefteplanning**.

> [!NOTE]
> De waarde *Prioriteit* is alleen beschikbaar voor het veld **Behoefteplanningscode** als Planningsoptimalisatie is ingeschakeld.

Met de gerelateerde *planningsprioriteitsmodellen* wordt de planningsprioriteit beheerd en worden geplande orders opgesplitst per prioriteitsbereik. Hiermee kunt u ook standaardprioriteitswaarden voor de planning instellen voor elk type vraag of aanbod en kunt u de prioriteitsberekeningsmethode definiëren.

## <a name="types-of-priority-calculation-methods"></a>Methoden voor berekening van prioriteitstypen

Elk planningsprioriteitsmodel heeft een instelling voor **Methode voor berekening van prioriteit** waarmee wordt bepaald hoe in de hoofdplanning prioriteit wordt toegepast op geplande orders. De beschikbare waarden zijn *Percentage van maximale voorraadhoeveelheid* en *Prioriteitsbereiken*. *Prioriteitsbereiken* staan voor een geavanceerdere versie van de methode *Percentage van maximale voorraadhoeveelheid*.

### <a name="percent-of-maximum-inventory-quantity"></a>Percentage van maximale voorraadhoeveelheid

Bij de berekeningsmethode *Percentage van maximale voorraadhoeveelheid* wordt bij de berekening van de aanbodprioriteit de huidige *totaal beschikbare voorraad* (nettostroom) gevonden als percentage van de waarde voor **Maximale voorraadhoeveelheid** die is ingesteld voor een artikel. Er wordt vervolgens één geplande order per artikel en leverancier gemaakt (tenzij de maximale orderhoeveelheid wordt gebruikt om een splitsing af te dwingen). De planningsprioriteit van de order wordt berekend als een percentage van het maximum.

De volgende formule wordt hierbij gebruikt:

*Percentage van maximum* = (*nettostroompositie* × 100) ÷ *waarde van maximale voorraadhoeveelheid van de artikelbehoefteplanning*

In deze formule wordt *Nettostroompositie* als volgt berekend:

*Nettostroompositie* = *Voorhanden* + *In bestelling* – *Gekwalificeerde vraag*

- *In bestelling* is het verwachte aanbod.
- *Gekwalificeerde vraag* staat voor de nettobehoeften waarvan de behoeftedatum binnen de time fence voor planning valt.

Tijdens de uitvoering van de hoofdplanning worden nieuwe geplande orders gemaakt wanneer de nettostroompositie kleiner is dan de bestelpunthoeveelheid van een artikel. De hoeveelheid van de geplande orders is het verschil tussen de waarde van **Maximale voorraadhoeveelheid** die is ingesteld op artikelniveau en de nettostroompositie. De prioriteit van de geplande order wordt berekend als een percentage van *nettostroompositie* van de waarde van **Maximale voorraadhoeveelheid**.

> [!NOTE]
> De berekende prioriteit kan niet negatief zijn, zelfs niet als de vraag groter is dan het totale aanbod. Als de vraag groter is dan het totale aanbod, wordt de berekende prioriteit ingesteld op 0 (nul).

### <a name="priority-ranges"></a>Prioriteitsbereiken

De berekeningsmethode *Prioriteitsbereiken* is geavanceerder dan de methode *Percentage van maximale voorraadhoeveelheid* en wordt geconfigureerd op het niveau van het planningsprioriteitsmodel. Er kunnen meerdere nieuwe geplande aanbodorders worden gemaakt om aan de vraag per artikel te voldoen. De prioriteiten van het geplande aanbod worden bepaald door de waarden die zijn gedefinieerd in het raster **Planningsprioriteitsbereiken** op de pagina **Planningsprioriteitsmodellen**.

Als het veld **Methode voor berekening van prioriteit** is ingesteld op *Prioriteitsbereiken*, gelden de volgende extra regels:

- Als de optie **Vraagprioriteit overwegen** voor het geplande prioriteitsmodel is ingesteld op *Ja*, wordt de prioriteitsbereikperiode beperkt met de prioriteit die op elke vraagregel is ingesteld, . De prioriteit van een nieuwe geplande order voor aanbod is niet lager dan de prioriteit van de vraag. De bovengrens van het bereik wordt beschouwd als een drempel waarmee de prioriteitswaarde van de vraag wordt vergeleken. Als de prioriteit van de vraag precies in het midden staat tussen de bovenste drempelwaarden van twee bereiken, wordt het bereik met de hoogste prioriteit (dat wil zeggen de laagste prioriteitswaarde) geselecteerd.
- Als het veld **Geplande order maken** voor het geplande prioriteitsmodel is ingesteld op *Eén aanbod met de belangrijkste prioriteit*, wordt er slechts één aanbod gemaakt om helemaal tot aan het maximum te voldoen. De prioriteit wordt ingesteld op de prioriteit van het eerste bereik waarmee een aanbod wordt geactiveerd.
- Als er geen voorhanden voorraad, geen aanbod en geen vraag is, wordt de regel in het raster **Planningsprioriteitsbereiken** gebruikt waarin het veld **Van hoeveelheid** is ingesteld op *Nul*.
- Als er vraag is maar geen voorhanden voorraad of verwacht aanbod, wordt de regel in het raster **Planningsprioriteitsbereiken** gebruikt waarin het veld **Van hoeveelheid** is ingesteld op *Nul of minder*.
- Als het bereik wordt geëvalueerd waarvan de vraag deel uitmaakt, is de instelling van de optie **Vraagprioriteit overwegen** nog steeds van invloed.

## <a name="differences-between-traditional-timeline-calculations-and-priority-based-planning"></a>Verschillen tussen traditionele tijdlijnberekeningen en op prioriteit gebaseerde planning

Op prioriteit gebaseerde planning wijkt op de volgende manieren af van traditionele tijdlijnberekeningen:

- Alle gewone preprocessors voor planning zijn nog steeds van kracht. Deze preprocessors omvatten de tracering van de behoefte van goedgekeurde geplande orders ten opzichte van de vraag, verkoopvraag, toewijzing van opdrachten tot inkoop en reserveringslogica. Alleen de vraag die niet door deze preprocessors wordt voldaan, wordt verwerkt.
- Tijdens de tracering van de behoefte wordt rekening gehouden met al het aanbod, ongeacht de prioriteit. Dit aanbod omvat de voorhanden voorraad, vrijgegeven voorraad en het niet op behoefte getraceerde gedeelte van goedgekeurde geplande orders.
- Vraag van "negatieve dagen" kan niet op behoefte worden getraceerd ten opzichte van het aanbod gedurende de gehele behoefteplanningstijd.
- Wanneer voor het aanbod de behoefte wordt getraceerd ten opzichte van de vraag, wordt het aanbod met de hoogste prioriteit (dat wil zeggen de laagste prioriteitswaarde) als eerste gebruikt. Voor voorhanden aanbod wordt uitgegaan van een prioriteitswaarde van 0 (nul). Het wordt dus verbruikt als de allereerste bron.
- Er worden nieuwe geplande aanbodregels gemaakt volgens de normale regels voor minimale ordergrootte, maximale ordergrootte, hoeveelheidsveelvoud, enzovoort.

## <a name="planning-priority-models"></a>Planningsprioriteitsmodellen

*Planningsprioriteitsmodellen* worden toegewezen aan behoefteplanningsgroepen en bepalen de planningsprioriteit voor geplande orders. Deze modellen definiëren de logica die bepaalt hoe de planningsprioriteitswaarde wordt berekend voor elke geplande order, en hoe prioriteit wordt toegewezen aan geplande orders, aanbodregels en vraagregels.

Als u wilt werken met de planningsprioriteitsmodellen, gaat u naar **Hoofdplanning \> Instellen \> Planningsprioriteitsmodellen**. Zoals eerder is besproken, is een van de belangrijkste instellingen van een model de waarde van **Methode voor berekening van prioriteit**. Met deze instelling bepaalt u de berekeningsmethode die wordt gebruikt wanneer met de hoofdplanning een prioriteitswaarde aan geplande orders wordt toegewezen.

> [!NOTE]
> Planningsprioriteitsmodellen gelden voor de hele organisatie voor alle rechtspersonen.

### <a name="coverage-group"></a>Behoefteplanningsgroep

Stel een nieuwe behoefteplanningsgroep in die u wilt gebruiken voor op prioriteit gebaseerde planning, zoals beschreven in [Behoefteplanningsregels voor artikelen definiëren](../tasks/define-coverage-rules-items.md). Stel de volgende extra velden in nadat u de behoefteplanningsgroep hebt gemaakt:

- **Behoefteplanningscode**: selecteer *Prioriteit* als voor de behoefteplanningsgroep op prioriteit gebaseerde planning wordt gebruikt.
- **Planningspioriteitsmodel**: selecteer een planningsprioriteitsmodel voor de hele organisatie.

### <a name="item-coverage"></a>Artikelbehoefte

Stel instellingen voor artikelbehoefteplanning in zoals beschreven in [Behoefteplanningsinstellingen](../coverage-settings.md). Standaard wordt de voor de behoefteplanningsgroep geselecteerde waarde van **Behoefteplanningscode** gekopieerd naar de instellingen voor artikelbehoefteplanning. U kunt de standaardwaarde echter zo nodig overschrijven. In sommige gevallen wordt het veld **Behoefteplanningscode** voor een artikelbehoefteplanningsrecord ingesteld op *Planning*, maar wordt er geen planningsprioriteitsmodel gedefinieerd voor de gerelateerde behoefteplanningsgroep. In deze gevallen wordt elk model waarbij het veld **Methode voor berekening van prioriteit** is ingesteld op *Percentage van maximale voorraadhoeveelheid* en het veld **Geplande order maken** op *Eén aanbod met belangrijkste prioriteit* standaard toegepast.

Stel het veld **Behoefteplanningscode** in op *Prioriteit* om het veld **Bestelpunt** in de instellingen voor artikelbehoefteplanning beschikbaar te maken. Voer in dit veld de bestelpunthoeveelheid in die door het systeem moet worden gebruikt bij het bepalen wanneer geplande orders met een waarde voor **Behoefteplanningscode** van *Prioriteit* moeten worden geplaatst.

De bestelpunthoeveelheid wordt vaak berekend als de vraag tijdens de doorlooptijd plus een minimumwaarde (veiligheidsvoorraad). Dit moet een waarde zijn tussen de waarden voor **Minimum** en **Maximum**.

U kunt de velden bijvoorbeeld als volgt instellen:

- **Minimum:** *10*
- **Bestelpunt:** *45*
- **Maximum:** *60*

De bestelpunthoeveelheid voor dit voorbeeld is gebaseerd op een doorlooptijd van zeven dagen en een gemiddeld dagelijks gebruik van 5. Daarom is de vraag tijdens de doorlooptijd 35. De minimumwaarde 10 (veiligheidsvoorraad) wordt vervolgens toegevoegd om een bestelpunt van 45 te krijgen. Als deze instelling wordt gebruikt, wordt aanbod voorgesteld als het verwachte voorhanden niveau onder 45 ligt. De orderprioriteit wordt gebaseerd op de instelling van de planningsprioriteit.

### <a name="manage-planning-priority-models"></a>Planningsprioriteitsmodellen beheren

Als u met de planningsprioriteitsmodellen wilt werken, voert u de volgende stappen uit.

1. Ga naar **Hoofdplanning \> Instellen \> Planningsprioriteitsmodellen**.
1. Selecteer een bestaand model in het lijstvenster of selecteer **Nieuw** in het actievenster om een nieuw model te maken.
1. Stel in de koptekst van de record de volgende velden in:

    - **Naam**: voer een naam voor het model in. De naam moet uniek zijn voor alle rechtspersonen in uw organisatie.
    - **Beschrijving**: voer een beschrijving van het model in.
    - **Methode voor berekening van prioriteit**: selecteer een van de volgende waarden:

        - *Prioriteitsbereiken*: als u deze waarde selecteert, wordt het raster **Planningsprioriteitsbereiken** beschikbaar. U moet daar verschillende prioriteitsbereiken instellen om de planningsprioriteitswaarde te definiëren.
        - *Percentage van maximale voorraadhoeveelheid*: bereken de planningsprioriteitswaarde als een percentage op basis van het verwachte voorraadniveau boven de maximale voorraadhoeveelheid.

    - **Geplande order maken**: dit veld is beschikbaar als het veld **Methode voor berekening van prioriteit** is ingesteld op *Prioriteitsbereiken*. Selecteer een van de volgende waarden:

        - *Eén aanbod met de belangrijkste prioriteit*: geplande orders mogen niet worden gesplitst op basis van het prioriteitsbereik. De planningsprioriteit voor een geplande order is gebaseerd op het belangrijkste prioriteitsbereik (dat wil zeggen de laagste planningsprioriteitswaarde).
        - *Splitsen op basis van prioriteitsbereiken*: splits de vraag op in meerdere geplande orders op basis van de planningsprioriteitsbereiken. De planningsprioriteit voor afzonderlijke geplande orders wordt gedefinieerd door de planningsprioriteit van het gerelateerde planningsprioriteitsbereik.

    - **Vraagprioriteit overwegen**: stel deze optie in op *Ja* om de prioriteit te beperken van een nieuwe geplande order die voor het aanbod wordt gemaakt. (De prioriteit is niet lager dan de prioriteit van de gerelateerde vraag.) Als u deze optie op *Nee* instelt, wordt er geen rekening gehouden met de prioriteit van de vraagorder wanneer de prioriteit van de aanbodorder wordt berekend.

1. Als u het veld **Methode voor berekening van prioriteit** instelt op *Prioriteitsbereiken*, gebruikt u de knoppen **Toevoegen** en **Verwijderen** op de werkbalk van het sneltabblad **Planningsprioriteitsbereiken** om de prioriteitsbereikrijen indien nodig toe te voegen of te verwijderen. Als er meerdere rijen zijn en u een nieuwe rij invoegt, wordt de planningsprioriteit automatisch ingesteld op het gemiddelde van de geselecteerde rij en de rij erboven. Stel voor elke rij de volgende velden in:

    - **Planningsprioriteit**: voer een waarde in tussen 0,00 en 100,00. Deze waarde staat voor de planningsprioriteit die voor de rij wordt gebruikt. De laagste prioriteitswaarde staat voor de hoogste prioriteit. Er wordt een standaardwaarde toegewezen, maar u kunt deze naar wens wijzigen. Dezelfde waarde voor **Planningsprioriteit** kan niet worden gebruikt voor meerdere planningsprioriteitsbereiken in hetzelfde planningsprioriteitsmodel.
    - **Beschrijving**: voer een beschrijving van het planningsprioriteitsbereik in (bijvoorbeeld *Bestelpunt tot maximum*).
    - **Van hoeveelheid**: de ondergrens van het planningsprioriteitsbereik. Deze waarde is alleen-lezen en is gebaseerd op de waarden **Tot hoeveelheid** en **Percentage tot hoeveelheid** voor het vorige planningsprioriteitsbereik.
    - **Tot hoeveelheid**: selecteer het veld van de artikelbehoefteplanning die moet worden gebruikt om de bovengrens van het bereik te definiëren. De volgende waarden worden ondersteund en beïnvloeden de waarde **Van hoeveelheid** van het volgende bereik:

        - *Nul*: deze waarde staat voor een bereik van negatief tot nul (*Nul of minder* tot *Nul*). Voor rijen waarin deze waarde is geselecteerd, is het veld **Percentage van tot hoeveelheid** alleen-lezen en is het altijd ingesteld op *100* procent.
        - *Minimale voorraadhoeveelheid*: deze waarde staat voor de waarde **Minimum** van een artikel op de pagina **Artikelbehoefteplanning**. Voor rijen waarin deze waarde is geselecteerd, kan het veld **Percentage van tot hoeveelheid** worden bewerkt en gebruikt om de waarde **Van hoeveelheid** van het volgende bereik (bijvoorbeeld op *80% van minimale voorraadhoeveelheid*) in te stellen.
        - *Bestelpunt*: deze waarde staat voor de waarde van **Bestelpunt** voor een artikel op de pagina **Artikelbehoefteplanning**. Voor rijen waarin deze waarde is geselecteerd, kan het veld **Percentage van tot hoeveelheid** worden bewerkt en gebruikt om de waarde **Van hoeveelheid** van het volgende bereik (bijvoorbeeld op *80% van bestelpunt*) in te stellen.
        - *Maximale voorraadhoeveelheid*: deze waarde staat voor de waarde **Maximum** van een artikel op de pagina **Artikelbehoefteplanning**. Voor rijen waarin deze waarde is geselecteerd, kan het veld **Percentage van tot hoeveelheid** worden bewerkt en gebruikt om **Van hoeveelheid** van het volgende bereik (bijvoorbeeld op *80% van minimale voorraadhoeveelheid*) in te stellen.
        - *Onbeperkt*: deze waarde staat voor een onbeperkt hoogste niveau van het bereik (*Onbeperkt of minder* tot *Onbeperkt*). Voor rijen waarin deze waarde is geselecteerd, is het veld **Percentage van tot hoeveelheid** alleen-lezen en is het altijd ingesteld op *100* procent.

    - **Percentage van tot hoeveelheid**: voer een percentagewaarde in die wordt gebruikt om de bovengrens van het planningsprioriteitsbereik te berekenen op basis van de waarde die is geselecteerd in het veld **Tot hoeveelheid**. Als het veld **Tot hoeveelheid** bijvoorbeeld is ingesteld op *Minimale voorraadhoeveelheid* en het veld **Percentage van tot hoeveelheid** is ingesteld op *50*, is de bovengrens 50 procent van de minimale voorraadhoeveelheid van de gerelateerde artikelbehoefteplanning.

1. Stel op het sneltabblad **Standaardwaarden planningsprioriteit** de velden in die u nodig hebt voor het definiëren van standaardplanningsprioriteiten voor elk type vraag- of aanbodregel (verkooporder, inkooporder, transferorder of vraagprognose). Alleen positieve waarden kunnen worden ingevoerd.

## <a name="view-and-maintain-planning-priority"></a>Planningsprioriteit bekijken en onderhouden

De planningsprioriteit wordt weergegeven en ingesteld in het veld **Planningsprioriteit**. U vindt dit veld op de pagina's die in de volgende tabel worden weergegeven. De prioriteit wordt ingesteld als een getal tussen 0 (nul) en 100, waarbij 0 voor het grootste belang staat.

| Pagina | Veldlocatie | Waardebron |
|---|---|---|
| Vraagprognoseregels | <p>Tabblad **Artikel**</p><p>(Selecteer een regel in het bovenste gedeelte en selecteer vervolgens het tabblad **Artikel**.)</p> | Standaardwaarde of waarde die handmatig is ingesteld |
| Details verkooporder | <p>Tabblad **Levering** op het sneltabblad **Regeldetails**</p><p>(Selecteer een regel op het sneltabblad **Verkooporderregels** en selecteer vervolgens op het sneltabblad **Regeldetails** het tabblad **Levering**.)</p> | Standaardwaarde, waarde van intercompany of waarde die handmatig is ingesteld |
| Inkooporderdetails | <p>Tabblad **Levering** op het sneltabblad **Regeldetails**</p><p>(Selecteer een regel op het sneltabblad **Inkooporderregels** en selecteer vervolgens op het sneltabblad **Regeldetails** het tabblad **Levering**.)</p> | Waarde die wordt ingesteld tijdens het fiatteren van geplande orders, de waarde van intercompany of de waarde die handmatig is ingesteld |
| Details transferorder | <p>Tabblad **Levering** op het sneltabblad **Regeldetails**</p><p>(Selecteer een regel op het sneltabblad **Transferorderregels** en selecteer vervolgens op het sneltabblad **Regeldetails** het tabblad **Levering**.)</p> | Waarde die wordt ingesteld tijdens het fiatteren van geplande orders of de waarde die handmatig is ingesteld |
| Details van geplande orders | Sneltabblad **Algemeen** | Waarde die wordt berekend tijdens de hoofdplanning of waarde die handmatig is ingesteld |

### <a name="intercompany-trade"></a>Intercompany-handel

De waarde **Planningsprioriteit** op intercompany-regels voor vraag en aanbod wordt gedeeld door de gekoppelde entiteiten. Wijzigingen worden altijd weergegeven op de gekoppelde orderregel.

Hieronder volgen een aantal voorbeelden:

- Een gebruiker wijzigt de planningsprioriteit voor een intercompany-verkooporderregel van 20 in 30. Deze wijziging wordt weergegeven op de gekoppelde intercompany-inkooporderregel.
- Een gebruiker wijzigt de planningsprioriteit voor een intercompany-inkooporderregel van 40 in 50. Deze wijziging wordt weergegeven op de gekoppelde intercompany-verkooporderregel.
