---
title: Kortingen verwerken, controleren en boeken
description: In dit onderwerp wordt beschreven hoe u uw kortingsbeheerdeals verwerkt, de kortingen berekent, de gegenereerde transacties ccontroleert, transacties boekt en de boekingen bekijkt.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TAMRebateDeal
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: e255c60889fdb49dfd8a1fd01be839b6405b02c6
ms.sourcegitcommit: 890a0b3eb3c1f48d786b0789e5bb8641e0b8455e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/20/2021
ms.locfileid: "5919864"
---
# <a name="process-review-and-post-rebates"></a>Kortingen verwerken, controleren en boeken

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u uw kortingsbeheerdeals verwerkt, de kortingen berekent, de gegenereerde transacties ccontroleert, transacties boekt en de boekingen bekijkt.

## <a name="change-the-status-of-a-deal"></a>De status van een deal wijzigen

U aan elke deal een status toewijzen om deze bij te houden. De status is uitsluitend bedoeld voor informatieve doeleinden.

1. Selecteer een deal (bijvoorbeeld op de [pagina **Alle kortingsbeheerdeals**](rebate-management-deals.md)).
1. Selecteer vervolgens in het actievenster op het tabblad **Kortingsbeheerdeals** in de groep **Onderhouden** de optie **Status wijzigen**.
1. Stel in het dialoogvenster **Status wijzigen** het veld **Kortingsstatus** in op een nieuwe status.
1. Selecteer **OK**.

## <a name="calculate-fifo-purchase-prices"></a>FIFO-inkoopprijzen berekenen

De periodieke taak **FIFO-inkoopprijs berekenen** moet worden uitgevoerd om de kortingen te berekenen voor [deals](rebate-management-deals.md) waarbij het veld **Prijsbasis** is ingesteld op *FIFO*. Het systeem gebruikt een FIFO-regel (First In, First Out) om de waarde van de verkochte voorraad te berekenen. Deze waarde wordt vervolgens gebruikt om de leverancierskortingen te berekenen.

Ga naar **Kortingsbeheer \> Periodieke taken \> FIFO-inkoopprijs berekenen**. Selecteer **OK** in het dialoogvenster dat wordt weergegeven om de berekening uit te voeren.

## <a name="process-rebate-management-deals"></a>Deals voor kortingbeheer verwerken

Wanneer u een deal verwerkt, berekent het systeem alle relevante kortingen en royalty's die zijn ingesteld. Alleen geselecteerde deals met berekeningsperioden die gereed zijn om te worden berekend en die de status *Actief* hebben, worden verwerkt. Nadat de verwerking is voltooid, genereert het systeem een set transacties die u kunt controleren en vervolgens boeken.

> [!NOTE]
> In alle gevallen worden kortingen verwerkt op het niveau dat is opgegeven door de instelling **Afstemmen met** van elke deal (*Deal* of *Regels*). U kunt berekeningen met één regel alleen uitvoeren voor deals waarbij het veld **Afstemmen met** is ingesteld op *Regel*.

### <a name="process-all-lines-for-one-or-more-deals"></a>Alle regels verwerken voor een of meer deals

1. Open de juiste [lijstpagina met kortingsdeals](rebate-management-deals.md) voor het type deal waarmee u wilt werken.
1. Selecteer de rij voor elke deal die u wilt verwerken (of open de deal die u wilt verwerken).
1. Selecteer in het actievenster op het tabblad **Deals voor kortingbeheer** in de groep **Genereren** een van de volgende opdrachten:

    - **Verwerken \> Inrichten**: richt een set toerekeningen in voor elke relevante kortingsdeal, maar boek deze niet.
    - **Verwerken \> Kortingsbeheer**: verwerk een reeks transacties die de waarde van de korting voor elke deal bieden.
    - **Verwerken \> Afschrijven**: boek eerder geboekte transacties terug om ze af te schrijven, zodat nieuwe kortingsdealtransacties kunnen worden berekend.

1. Stel in het dialoogvenster dat wordt weergegeven de velden **Van datum** en **Tot datum** in om het datumbereik voor de berekening te definiëren.
1. Selecteer **OK** om de berekening uit te voeren.

### <a name="process-one-or-more-specific-deal-lines-for-a-selected-deal"></a>Een of meer specifieke dealregels voor een geselecteerde deal verwerken

1. Open de juiste [lijstpagina met kortingsdeals](rebate-management-deals.md) voor het type deal waarmee u wilt werken.
1. Open de deal waarvan u een regel wilt verwerken.
1. Selecteer het tabblad **Regels** in de rechterbovenhoek.
1. Selecteer op het sneltabblad **Kortingsbeheer** de rij voor elke dealregel die u wilt verwerken.
1. Selecteer op de werkbalk van het sneltabblad **Kortingsbeheer** een van de volgende opdrachten. (Deze opdrachten zijn alleen beschikbaar voor deals waarbij het veld **Afstemmen met** is ingesteld op *Regel*.)

    - **Verwerken \> Inrichten**: richt een set toerekeningen in voor elke relevante dealregel, maar boek deze niet.
    - **Verwerken \> Kortingsbeheer**: verwerk een reeks transacties die de waarde van de korting voor elke dealregel bieden.
    - **Verwerken \> Afschrijven**: boek eerder geboekte transacties terug om ze af te schrijven, zodat nieuwe kortingsdealtransacties kunnen worden berekend.

1. Stel in het dialoogvenster dat wordt weergegeven de velden **Van datum** en **Tot datum** in om het datumbereik voor de berekening te definiëren.
1. Selecteer **OK** om de berekening uit te voeren.

### <a name="process-deals-using-a-batch-job"></a>Deals verwerken via een batchtaak

In plaats van specifieke deals of dealregels te verwerken, u een batchtaak uitvoeren om meerdere deals tegelijkertijd te verwerken. U kunt optioneel recordfilters toepassen en/of een terugkerend schema instellen. Volg deze stappen om deals te verwerken via een batchtaak.

1. Volg één van deze stappen:

    - Ga naar **Kortingsbeheer \> Periodieke taken \> Verwerken \> Inrichten** om een set toerekeningen in te richten voor elke relevante deal, maar zonder deze te boeken.
    - Ga naar **Kortingsbeheer \> Periodieke taken \> Verwerken \> Kortingsbeheer** om een reeks transacties te verwerken die de waarde van de korting voor elke deal bieden.
    - Ga naar **Kortingsbeheer \> Periodieke taken \> Verwerken \> Afschrijven** om eerder geboekte transacties terug te boeken om ze af te schrijven, zodat nieuwe kortingsdealtransacties kunnen worden berekend.

1. Stel in het dialoogvenster dat wordt weergegeven op het sneltabblad **Parameters** in de sectie **Periode** de velden **Van datum** en **Tot datum** in om het datumbereik voor transacties voor de berekening te definiëren.
1. Stel in de sectie **Garantieperiode** de velden **Van datum** en **Tot datum** in om het datumbereik voor garanties voor de berekening te definiëren.
1. Op het sneltabblad **Op te nemen records** kunt u filters instellen om de set deals te beperken die via de batchtaak worden verwerkt. Deze instellingen werken op dezelfde manier als voor andere typen batchtaken.
1. Op het sneltabblad **Op de achtergrond uitvoeren** kunt u indien nodig batchverwerkings- en planningsopties instellen. Deze instellingen werken op dezelfde manier als voor andere typen batchtaken.
1. Selecteer **OK** om de berekening uit te voeren en/of te plannen.

## <a name="view-and-edit-rebate-management-transactions"></a>Kortingsbeheertransacties weergeven en bewerken

Wanneer u een of meer deals verwerkt, maakt het systeem transacties die u kunt bekijken en mogelijk bewerken voordat u ze boekt.

1. Volg één van deze stappen:

    - Selecteer de deal waarvoor u transacties wilt weergeven (bijvoorbeeld op de [pagina **Alle kortingsbeheerdeals**](rebate-management-deals.md)). Selecteer in het actievenster op het tabblad **Kortingsbeheerdeals** in de groep **Transacties** de optie **Transacties** of **Garantietransacties**, afhankelijk van het type transactie dat u wilt weergeven.
    - Open een deal (bijvoorbeeld op de [pagina **Alle kortingsbeheerdeals**](rebate-management-deals.md)) waarvan u de details wilt weergeven. Selecteer op het sneltabblad **Kortingsbeheer** de dealregel waarvoor u transacties wilt weergeven. Selecteer vervolgens op de werkbalk **Transacties** of **Garantietransacties**, afhankelijk van het type transactie dat u wilt weergeven. (Deze knoppen zijn alleen beschikbaar voor deals waarbij het veld **Afstemmen met** is ingesteld op *Regel*.)

1. De pagina **Datumtransacties voor kortingsbeheer** of **Garantietransacties voor kortingsbeheer** wordt weergegeven. Het bevat een raster, waarbij elke regel een verzameling transacties uit één kortings- of garantieperiode vertegenwoordigt. Selecteer een rij in het raster en selecteer vervolgens in het actievenster de optie **Brontransacties** om de transacties weer te geven die tot die rij behoren.
1. Op de pagina die wordt weergegeven, wordt een lijst weergegeven met de transacties van het geselecteerde type die tot de geselecteerde rij behoren. Elke transactie bevat relevante details, afhankelijk van het transactietype. Voor garantietransacties kunt u de lijst alleen bekijken. Voor andere typen transacties kunt u op deze pagina de volgende acties uitvoeren:

    - Als u de totale waarde van alle geclaimde transacties op de pagina wilt controleren, bekijkt u het veld **Geclaimd bedrag**.
    - Als u meer informatie over een transactie wilt weergeven, selecteert u deze en selecteert u vervolgens het tabblad **Algemeen**, **Financiële dimensie** of **Dimensie**.
    - Als u kortingen wilt weergeven die van toepassing zijn, selecteert u **Reductietransacties** in het actievenster. Zie [Kortingsreductieprincipes](rebate-reduction-principle.md) voor meer informatie.
    - Als u transacties wilt markeren als geclaimd of niet-geclaimd als u een claimproces gebruikt, selecteert u de relevante rijen en selecteert u vervolgens in het actievenster een van de volgende opdrachten. (U schakelt claimprocessen in op de [pagina **Kortingsbeheerparameters**](rebate-management-parameters.md).)

        - **Instellen als geclaimd \> Alles**: markeer alle transacties als geclaimd.
        - **Instellen als geclaimd \> Geselecteerd**: markeer de geselecteerde transacties als geclaimd.
        - **Instellen als niet-geclaimd \> Alles**: markeer alle transacties als niet-geclaimd.
        - **Instellen als niet-geclaimd \> Geselecteerd**: markeer de geselecteerde transacties als niet-geclaimd.

    - Als u de claim voor een of meer regels wilt boeken, selecteert u de relevante regels en selecteert u vervolgens **Boeken** in het actievenster. (De knop **Boeken** is alleen beschikbaar voor kortingstransacties. Het is niet beschikbaar voor inrichtings- en afschrijvingstransacties.) In het dialoogvenster **Boeken** worden de velden **Van datum** en **Tot datum** automatisch ingesteld. Stel het veld **Boekingsdatum** in en selecteer vervolgens **OK**.
    - Als u het bedrag wilt aanpassen dat wordt weergegeven voor een open of niet-geboekte transactie, selecteert u de transactie en volgt u een van de volgende stappen:

        - Bewerk de waarde in het veld **Gecorrigeerd bedrag**.
        - Selecteer in het actievenster de optie **Correctie instellen**. Voer vervolgens in het vervolgkeuzevenster dat wordt weergegeven in het veld **Gecorrigeerd bedrag** een waarde in.

> [!NOTE]
> Wanneer u de volgende periode verwerkt, bevat de transactielijst alle niet-geclaimde transacties uit de vorige boeking, plus eventuele nieuwe transacties voor de geselecteerde periode.

## <a name="post-rebates-transactions"></a>Kortingstransacties boeken

Als u de waarde van de kortingen en inhoudingen wilt boeken, moet u het boekingsproces uitvoeren, tenzij u uw systeem hebt ingesteld om ze automatisch te boeken.

### <a name="set-up-the-system-to-post-all-transactions-automatically"></a>Het systeem instellen om alle transacties automatisch te boeken

Als u wilt instellen dat uw systeem alle transacties boekt zodra ze zijn gegenereerd, schakelt u de optie **Journalen automatisch boeken** en/of **Automatisch vrije-tekstfacturen boeken** op de pagina **Kortingsbeheerparameters** in. Zie [Kortingsbeheerparameters](rebate-management-parameters.md) voor meer informatie.

### <a name="post-transactions-for-all-lines-for-one-or-more-deals"></a>Transacties boeken voor alle regels voor een of meer deals

Als u geen automatische boeking gebruikt nadat u de relevante deals hebt verwerkt, volgt u deze stappen om de gegenereerde transacties voor alle regels voor een of meer deals te controleren en te boeken.

1. Open de juiste [lijstpagina met kortingsdeals](rebate-management-deals.md) voor het type deal waarmee u wilt werken.
1. Selecteer de rij voor elke deal die u wilt boeken (of open de deal die u wilt boeken).
1. Selecteer in het actievenster op het tabblad **Deals voor kortingbeheer** in de groep **Genereren** een van de volgende opdrachten:

    - **Boeken \> Inrichten**: boek beschikbare toerekeningstransacties die u hebt gemaakt.
    - **Boeken \> Kortingsbeheer**: boek beschikbare kortingstransacties die u hebt gemaakt.
    - **Boeken \> Afschrijven**: boek beschikbare afschrijvingstransacties die u hebt gemaakt.

1. Stel in het dialoogvenster dat verschijnt het veld **Boekingsdatum** in. Stel vervolgens de velden **Van datum** en **Tot datum** in om het datumbereik te definiëren voor de transacties die moeten worden geboekt.
1. Selecteer **OK** om de transacties te boeken.

### <a name="post-transactions-for-one-or-more-specific-deal-lines-for-a-selected-deal"></a>Transacties boeken voor een of meer specifieke dealregels voor een geselecteerde deal

Als u geen automatische boeking gebruikt nadat u de relevante deals hebt verwerkt, volgt u deze stappen om de gegenereerde transacties voor een of meer specifieke dealregels voor een geselecteerde deal te controleren en te boeken.

1. Open de juiste [lijstpagina met kortingsdeals](rebate-management-deals.md) voor het type deal waarmee u wilt werken.
1. Open de deal met een regel waarvoor u transacties wilt boeken.
1. Selecteer het tabblad **Regels** in de rechterbovenhoek.
1. Selecteer op het sneltabblad **Kortingsbeheer** de rij voor elke dealregel die u wilt boeken.
1. Selecteer op de werkbalk van het sneltabblad **Kortingsbeheer** een van de volgende opdrachten. (Deze opdrachten zijn alleen beschikbaar voor deals waarbij **Afstemmen met** is ingesteld op *Regel*.)

    - **Boeken \> Inrichten**: boek beschikbare toerekeningstransacties die u hebt gemaakt.
    - **Boeken \> Kortingsbeheer**: boek beschikbare kortingstransacties die u hebt gemaakt.
    - **Boeken \> Afschrijven**: boek beschikbare afschrijvingstransacties die u hebt gemaakt.

1. Stel in het dialoogvenster dat verschijnt het veld **Boekingsdatum** in. Stel vervolgens de velden **Van datum** en **Tot datum** in om het datumbereik te definiëren voor de transacties die moeten worden geboekt.
1. Selecteer **OK** om de transacties te boeken.

### <a name="post-transactions-using-a-batch-job"></a>Transacties boeken via een batchtaak

In plaats van transacties te boeken voor specifieke deals of dealregels, kunt u een batchtaak uitvoeren om transacties te boeken voor meerdere deals tegelijk. U kunt optioneel recordfilters toepassen en/of een terugkerend schema instellen. Volg deze stappen om transacties te boeken via een batchtaak.

1. Volg één van deze stappen:

    - Ga naar **Kortingsbeheer \> Periodieke taken \> Boeken \> Inrichten** om beschikbare toerekeningstransacties te boeken die u hebt gemaakt.
    - Ga naar **Kortingsbeheer \> Periodieke taken \> Boeken \> Kortingsbeheer** om beschikbare kortingstransacties te boeken die u hebt gemaakt.
    - Ga naar **Kortingsbeheer \> Periodieke taken \> Boeken \> Afschrijven** om beschikbare afschrijvingstransacties te boeken die u hebt gemaakt.

1. Stel in het dialoogvenster dat wordt weergegeven op het sneltabblad **Parameters** in de sectie **Periode** het veld **Boekingsdatum** in. Stel vervolgens de velden **Van datum** en **Tot datum** in om het datumbereik te definiëren voor de transacties die moeten worden geboekt. 
1. Stel in de sectie **Garantieperiode** de velden **Van datum** en **Tot datum** in om het datumbereik voor de garanties die moeten worden geboekt.
1. Op het sneltabblad **Op te nemen records** kunt u filters instellen om de set deals te beperken die via de batchtaak worden verwerkt. Deze instellingen werken op dezelfde manier als voor andere typen batchtaken.
1. Op het sneltabblad **Op de achtergrond uitvoeren** kunt u indien nodig batchverwerkings- en planningsopties instellen. Deze instellingen werken op dezelfde manier als voor andere typen batchtaken.
1. Selecteer **OK** om de berekening uit te voeren en/of te plannen.

## <a name="review-rebate-management-journals"></a>Kortingsbeheerjournalen controleren

Nadat uw transacties zijn geboekt, kunt u de resulterende dagboeken, documenten of artikelen bekijken. Doeltransacties voor kortingen en royalty's zijn gebaseerd op het betalingstype dat is ingesteld in het boekingsprofiel en het uitvoertype van de korting. Als de kortingsuitvoer bijvoorbeeld is ingesteld op *Artikel*, wordt een verkooporder gemaakt en kan deze worden bekeken via de doeltransacties. Als de betaling is ingesteld voor het gebruik van Leveranciers, wordt er een leveranciersfactuur gemaakt voor de leverancier die voor de klant is ingesteld ten behoeve van klantkortingen.

Volg deze stappen om de journaalposten te controleren die zijn gekoppeld aan een kortingsbeheerdeal.

1. Open de juiste [lijstpagina met kortingsdeals](rebate-management-deals.md) voor het type deal waarmee u wilt werken.
1. Selecteer de deal waarvoor u journaalposten wilt inspecteren.
1. Selecteer in het actievenster op het tabblad **Kortingsbeheerdeals** in de groep **Transacties** de optie **Transacties** of **Kortingstransacties**, afhankelijk van het type transacties dat u wilt bekijken.
1. Zorg ervoor dat het veld **Weergeven** is ingesteld op *Alles* of *Geboekt*.
1. Zoek en selecteer de transactieverzameling die u wilt inspecteren en selecteer vervolgens in het actievenster een van de volgende knoppen. (Deze knoppen zijn alleen beschikbaar als er relevante boekingen bestaan voor de geselecteerde transactieverzameling.)

    - **Doeltransacties**: bekijk relevante journalen en andere typen documenten die zijn gegenereerd door de geselecteerde deal.
    - **Artikelen**: bekijk relevante artikelen die zijn gegenereerd door de geselecteerde deal.

1. Er wordt een lijst met relevante dagboeken, documenten of artikelen weergegeven. Als u meer informatie over een journaal, document of artikel wilt weergeven, selecteert u de bijbehorende rij en selecteert u vervolgens in het actievenster de optie **Details weergeven**.
