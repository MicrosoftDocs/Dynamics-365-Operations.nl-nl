---
title: Kortingen verwerken, controleren en boeken
description: In dit onderwerp wordt beschreven hoe u uw kortingsbeheerdeals verwerkt, de kortingen berekent, de gegenereerde transacties ccontroleert, transacties boekt en de boekingen bekijkt.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateDeal
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 1a9603df8fd3b2c81c37ca95fd1b13d0b6f4004a38b0cf86846486e3b5d41bfa
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6729404"
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

## <a name="create-source-transactions"></a>Brontransacties maken

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

U kunt de verkooporders of inkooporders met brontransacties maken voor of nadat u een toepasselijke kortingsbeheeractie maakt.

U kunt elke kortingsregel zo instellen dat er automatisch een kortingsvoorziening wordt gemaakt door de levering of factuur voor een verkoop- of inkooporder te boeken. Stel het veld **Transactietype** voor de dealregel in op *Levering* of *Factuur* en stel de optie **Verwerken bij boeking** in op *Ja*. Als het veld **Transactietype** is ingesteld op *Order*, wordt de verwerking tijdens het boeken uitgeschakeld. Voor brontransacties die zijn gemaakt nadat een transactie was geactiveerd, kunt u de voorziening nog altijd verwerken zoals beschreven in de sectie [Kortingsbeheer verwerken](#process-deals) verder in dit onderwerp.

### <a name="enable-price-details"></a>Prijsdetails inschakelen

Voordat u brontransacties kunt maken, moet u de optie **Prijsdetails inschakelen** voor klanten inschakelen.

1. Ga naar **Klanten \> Instellen \> Parameters van module Klanten**.
1. Stel op het tabblad **Prijzen** op het sneltabblad **Prijsdetails** de optie **Prijsdetails inschakelen** in op *Ja*.

### <a name="create-a-source-transaction"></a>Brontransacties maken

Volg deze stappen om een brontransactie te maken.

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
1. Selecteer **Nieuw**.

    Om de manier om na te bootsen waarop kortingsclaims worden gegenereerd is de volgende taak een verkooporder te maken waarbij het product en de hoeveelheid de klant doen kwalificeren voor een korting.

1. Typ of selecteer in het veld **Klantrekening** een klant die in aanmerking komt voor een kortingsdeal.
1. Selecteer **OK** om de verkooporder te maken.
1. Voeg op het sneltabblad **Verkooporderregels** een regel toe en stel de volgende velden hiervoor in:

    - **Artikelnummer** – Een artikel opgeven dat in aanmerking komt voor een korting.
    - **Hoeveelheid** – Een hoeveelheid opgeven die in aanmerking komt voor een kortingsdeal die een regel bevat waarvoor het **Basis** veld is ingesteld op *Hoeveelheid*.
    - **Eenheidsprijs** – Een prijs opgeven die in aanmerking komt voor een kortingsdeal die een regel bevat waarvoor het **Basis** veld is ingesteld op *Waarde*.
    - **Locatie** – Een locatie selecteren waarop het product beschikbaar is en die in aanmerking komt voor een kortingsdeal.
    - **Magazijn** – Een magazijn selecteren waar het product beschikbaar is en dat in aanmerking komt voor een kortingsdeal.

1. Selecteer in het sneltabblad **Verkooporderdetails** op de werkbalk **Verkooporderregels \> Prijsgegevens**. Deze opdracht is alleen beschikbaar als u prijsdetails hebt ingeschakeld zoals beschreven in de vorige sectie.
1. Selecteer op de pagina **Prijsgegevens** het sneltabblad **Kortingsbeheer**. Dit sneltabblad bevat alle kortingsdeals die van toepassing zijn op de huidige orderregel en toont het geraamde kortingsbedrag in de valuta van de orders. Houd er rekening mee dat de bedragen alleen ramingen zijn van toekomstige kortingsaanvragen. De werkelijke kortingsbedragen kunnen verschillen. Hieronder staan enkele factoren die van invloed kunnen zijn op de werkelijke bedragen:

    - Het totale verkoopvolume dat de klant heeft behaald onder een periodieke kortingsovereenkomst.
    - Of de klant alle hoeveelheden of gedeeltelijke hoeveelheden heeft geretourneerd.
    - Of de van toepassing zijnde verkooporder het transactietype (*Order, Levering* of *Factuur*) heeft bereikt dat is gedefinieerd voor de kortingsbeheertransactie.
    - De **uitvoer** waarde van de deal. Er wordt een leeg kortingsbedrag weergegeven voor deals waarbij het veld **Uitvoer** is ingesteld op *Artikel*.

1. In het sneltabgebied **Detail** ziet u dat de sectie **Margeschatting** de volgende velden bevat. Deze velden worden toegevoegd via Kortingsbeheer. Met deze waarden worden alle waarden per eenheid weergegeven (terwijl in de velden op het sneltabformulier **Kortingsbeheer** de totale waarden voor de regel worden genoemd).

    - **Kortingsbeheer kortingsbedrag** (alleen verkooporders)
    - **Kortingsbeheer royalty-bedrag** (alleen verkooporders)
    - **Kortingsbeheer leverancierskortingsbedrag** (verkooporders en inkooporders)

1. Sluit de pagina **Prijsgegevens**.
1. Als de verkooporder niet in aanmerking komt voor de kortingen die u zojuist hebt bekeken, volgt u deze stappen om kortingen uit te sluiten. (U sluit doorgaans echter geen kortingen uit.)

    1. Selecteer de betreffende orderregel op het sneltabblad **Verkooporderregels**.
    1. Stel op het sneltabblad **Regeldetails** op het tabblad **Prijs en korting** de optie **Uitsluiten van kortingsbeheer** in op *Ja*. Deze optie is niet van toepassing op inkooporders. Bovendien worden alleen klantkortingen uitgesloten als deze optie is ingesteld op *Ja*. Royaltykortingen van klanten en leverancierskortingen zijn nog steeds van toepassing.

1. Selecteer in het actievenster, op het tabblad **Verzamelen en inpakken** in de groep **Genereren** de optie **Pakbon boeken**.
1. Selecteer *Alle* in het veld **Hoeveelheid** op het sneltabblad **Parameters**.
1. Selecteer **OK**.
1. Klik op **Ja** als u wordt gevraagd de actie te bevestigen.
1. Selecteer in het actievenster op het tabblad **Factuur** in de groep **Genereren** de optie **Factuur**.
1. Selecteer *Alle* of *Pakbon* in het veld **Hoeveelheid** op het sneltabblad **Parameters**.
1. Selecteer **OK**.
1. Klik op **Ja** als u wordt gevraagd de actie te bevestigen.

## <a name="process-rebate-management-deals"></a><a name="process-deals"></a>Deals voor kortingbeheer verwerken

Wanneer u een deal verwerkt, berekent het systeem alle relevante kortingen en royalty's die zijn ingesteld. Alleen geselecteerde deals met berekeningsperioden die gereed zijn om te worden berekend en die de status *Actief* hebben, worden verwerkt. Nadat de verwerking is voltooid, genereert het systeem een set transacties die u kunt controleren en vervolgens boeken.

> [!NOTE]
> In alle gevallen worden kortingen verwerkt op het niveau dat is opgegeven door de instelling **Afstemmen met** van elke deal (*Deal* of *Regels*). U kunt berekeningen met één regel alleen uitvoeren voor deals waarbij het veld **Afstemmen met** is ingesteld op *Regel*.

### <a name="process-all-lines-for-one-or-more-deals"></a>Alle regels verwerken voor een of meer deals

1. Open de juiste [lijstpagina met kortingsdeals](rebate-management-deals.md) voor het type deal waarmee u wilt werken.
1. Selecteer de rij voor elke deal die u wilt verwerken (of open de deal die u wilt verwerken).
1. Selecteer in het actievenster op het tabblad **Deals voor kortingbeheer** in de groep **Genereren** een van de volgende opdrachten:

    - **Verwerken \> Inrichten**: richt een set toerekeningen in voor elke relevante kortingsdeal, maar boek deze niet. Deze menuopdracht is niet beschikbaar voor acties waarbij het veld **Kortingsuitvoer** is ingesteld op *Artikel*.
    - **Verwerken \> Kortingsbeheer**: verwerk een reeks transacties die de waarde van de korting voor elke deal bieden.
    - **Verwerken \> Afschrijven**: verwerk voor elke brontransactie voor de kortingsdeal en de opgegeven periode de afwijking tussen de bedragen die zijn geboekt voor een voorziening en voor kortingsbeheer. Deze menuopdracht is niet beschikbaar voor acties waarbij het veld **Kortingsuitvoer** is ingesteld op *Artikel*.

1. Stel in het dialoogvenster dat wordt weergegeven de velden **Van datum** en **Tot datum** in om het datumbereik voor de berekening te definiëren.
1. Selecteer **OK** om de berekening uit te voeren.

### <a name="process-one-or-more-specific-deal-lines-for-a-selected-deal"></a>Een of meer specifieke dealregels voor een geselecteerde deal verwerken

1. Open de juiste [lijstpagina met kortingsdeals](rebate-management-deals.md) voor het type deal waarmee u wilt werken.
1. Open de deal waarvan u een regel wilt verwerken.
1. Selecteer het tabblad **Regels** in de rechterbovenhoek.
1. Selecteer op het sneltabblad **Kortingsbeheer** de rij voor elke dealregel die u wilt verwerken.
1. Selecteer op de werkbalk van het sneltabblad **Kortingsbeheer** een van de volgende opdrachten. (Deze opdrachten zijn alleen beschikbaar voor deals waarbij het veld **Afstemmen met** is ingesteld op *Regel*.)

    - **Verwerken \> Inrichten**: richt een set toerekeningen in voor elke relevante dealregel, maar boek deze niet. Deze menuopdracht is niet beschikbaar voor acties waarbij het veld **Kortingsuitvoer** is ingesteld op *Artikel*.
    - **Verwerken \> Kortingsbeheer**: verwerk een reeks transacties die de waarde van de korting voor elke dealregel bieden.
    - **Verwerken \> Afschrijven**: verwerk voor elke brontransactie voor de kortingsdeal en de opgegeven periode de afwijking tussen de bedragen die zijn geboekt voor een voorziening en voor kortingsbeheer. Deze menuopdracht is niet beschikbaar voor acties waarbij het veld **Kortingsuitvoer** is ingesteld op *Artikel*. 

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

### <a name="process-deals-by-using-the-rebate-workbench"></a>Deals verwerken met behulp van de kortingsworkbench

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

In plaats van specifieke deals of dealregels te verwerken, kunt u de *kortingsworkbench* gebruiken om meerdere deals tegelijkertijd te verwerken. U kunt optioneel recordfilters toepassen en/of een terugkerend schema instellen. U hoeft geen rijen te selecteren. Alle regels worden verwerkt die voldoen aan de datum- en filtervereisten die u hebt ingesteld.

Volg deze stappen om deals te verwerken met de kortingsworkbench.

1. Ga naar **Kortingsbeheer \> Deals voor kortingbeheer \> Kortingsworkbench**.
1. Selecteer in het actievenster op het tabblad **Kortingsworkbench** in de groep **In verwerking** een van de volgende opdrachten:

    - **Verwerken \> Inrichten** – Richt een set toerekeningen in voor elke relevante dealregel, maar boek deze niet.
    - **Verwerken \> Kortingsbeheer**: verwerk een reeks transacties die de waarde van de korting voor elke dealregel bieden.
    - **Verwerken \> Afschrijven** – Verwerk de afwijking tussen inrichten en kortingsbeheer die is geboekt voor elke brontransactie voor de kortingsdeal en de opgegeven periode.

1. Stel in het dialoogvenster **Kortingsbeheer** in de sectie **Periode** de velden **Van datum** en **Tot datum** in om het datumbereik voor de berekening te definiëren.
1. Stel in de sectie **Garantieperiode** de velden **Van datum** en **Tot datum** in om het datumbereik voor garanties voor de berekening te definiëren.
1. Op het sneltabblad **Op te nemen records** kunt u filters instellen om de set deals te beperken die via de batchtaak worden verwerkt. Deze instellingen werken op dezelfde manier als voor andere typen batchtaken.
1. Op het sneltabblad **Op de achtergrond uitvoeren** kunt u indien nodig batchverwerkings- en planningsopties instellen. Deze instellingen werken op dezelfde manier als voor andere typen batchtaken.
1. Selecteer **OK** om de berekening uit te voeren en/of te plannen.

## <a name="view-and-edit-rebate-management-transactions"></a>Kortingsbeheertransacties weergeven en bewerken

Wanneer u een of meer deals verwerkt, maakt het systeem transacties die u kunt bekijken en mogelijk bewerken voordat u ze boekt.

### <a name="view-and-edit-rebate-management-transactions-by-using-the-rebate-deals-list-page"></a>Kortingsbeheertransacties weergeven en bewerken met de lijstpagina kortingsdeals

Doe het volgende om kortingsbeheertransacties weer te geven en te bewerken met de lijstpagina kortingsdeals.

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

    - Selecteer **Boeken** in het actievenster om de claim voor alle relevante regels te boeken. Als u een claimproces gebruikt (wanneer de optie **Claimproces gebruiken** is ingeschakeld op de pagina **Parameters van kortingsbeheer**), worden alleen de regels geboekt die zijn gemarkeerd als **Geclaimd**. Anders worden alle brontransacties voor de geselecteerde kortingstransactie geboekt. De knop **Boeken** is alleen beschikbaar voor kortingstransacties. De knop is niet beschikbaar voor voorzienings- en afschrijvingstransacties. In het dialoogvenster **Boeken** zijn de velden **Begindatum** en **Einddatum** automatisch ingesteld. Stel het veld **Boekingsdatum** in en selecteer vervolgens **OK**.
    - Als u het bedrag wilt aanpassen dat wordt weergegeven voor een open of niet-geboekte transactie, selecteert u de transactie en volgt u een van de volgende stappen:

        - Bewerk de waarde in het veld **Gecorrigeerd bedrag**.
        - Selecteer in het actievenster de optie **Correctie instellen**. Voer vervolgens in het vervolgkeuzevenster dat wordt weergegeven in het veld **Gecorrigeerd bedrag** een waarde in.

> [!NOTE]
> Als u een claimproces gebruikt, bevat de transactielijst wanneer u de volgende periode verwerkt alle niet-geclaimde transacties uit de vorige boeking, plus eventuele nieuwe transacties voor de geselecteerde periode.

### <a name="view-and-edit-rebate-management-transactions-by-using-the-rebate-workbench"></a>Kortingsbeheertransacties weergeven en bewerken met de kortingsworkbench

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Doe het volgende om kortingsbeheertransacties weer te geven en te bewerken met de kortingsworkbench.

1. Ga naar **Kortingsbeheer \> Deals voor kortingbeheer \> Kortingsworkbench**.
1. Stel het veld **Tonen** in op *Niet geboekt*.
1. Op **de pagina** Kortingsworkbench wordt een lijst met de transacties weergegeven. Elke transactie geeft relevante details. Deze details variëren afhankelijk van het transactietype. Op deze pagina kunt u de volgende acties uitvoeren:

    - Als u meer informatie over een transactie wilt weergeven, selecteert u deze en selecteert u vervolgens het tabblad **Algemeen**, **Financiële dimensie** of **Dimensie**.
    - Als u een claimsproces gebruikt, kunt u transacties markeren als geclaimd of niet-geclaimd. Selecteer de relevante rijen en vervolgens in het actievenster op het tabblad **Kortingsworkbench** een van de volgende opdrachten. (U schakelt claimprocessen in op de pagina [**Kortingsbeheerparameters**](rebate-management-parameters.md).)

        - **Instellen als geclaimd** – Markeer de geselecteerde transacties als geclaimd.
        - **Instellen als niet-geclaimd** – Markeer de geselecteerde transacties als niet-geclaimd.

    - Selecteer de betreffende regels om de claim voor een of meer regels te boeken. Selecteer vervolgens in het actiepaneel op het tabblad **Kortingsworkbench** de optie **Boeken**. De knop **Boeken** is beschikbaar voor voorzienings-, kortings- of afschrijvingstransacties. In het dialoogvenster **Boeken** zijn de velden **Begindatum** en **Einddatum** automatisch ingesteld. Stel het veld **Boekingsdatum** in en selecteer vervolgens **OK**.
    - Als u het bedrag wilt aanpassen dat wordt weergegeven voor een open of niet-geboekte transactie, selecteert u de transactie en volgt u een van de volgende stappen:

        - Bewerk de waarde in het veld **Gecorrigeerd bedrag**.
        - Selecteer in het actiepaneel op het tabblad **Kortingsworkbench** de optie **Correctie instellen**. Voer vervolgens in het vervolgkeuzevenster dat wordt weergegeven in het veld **Gecorrigeerd bedrag** een waarde in.

> [!NOTE]
> Als u een claimproces gebruikt, bevat de transactielijst wanneer u de volgende periode verwerkt alle niet-geclaimde transacties uit de vorige boeking, plus eventuele nieuwe transacties voor de geselecteerde periode.

## <a name="post-rebates-transactions"></a>Kortingstransacties boeken

Als u de waarde van een verwerkte voorziening, kortingsbeheerbedrag en afschrijving wilt boeken, moet u het boekingsproces uitvoeren. Het boekingsproces markeert de voorzienings-, kortingsbeheer- of afschrijvingstransacties als geboekt en maakt de doeltransactie. Als u de doeltransactie niet hoeft te controleren, kunt u deze transacties zo instellen dat ze automatisch worden geboekt.

### <a name="set-up-the-system-to-post-all-target-transactions-automatically"></a>Het systeem instellen om alle doeltransacties automatisch te boeken

Als u wilt instellen dat uw systeem alle doeltransacties boekt zodra ze zijn gegenereerd door een voorziening, kortingsbeheerbedrag en afschrijving, schakelt u de optie **Journalen automatisch boeken** en/of **Automatisch vrije-tekstfacturen boeken** op de pagina **Kortingsbeheerparameters** in. Zie [Kortingsbeheerparameters](rebate-management-parameters.md) voor meer informatie.

### <a name="post-transactions-for-all-lines-for-one-or-more-deals"></a>Transacties boeken voor alle regels voor een of meer deals

Nadat u de relevante deals hebt verwerkt, volgt u deze stappen om de gegenereerde transacties voor alle regels voor een of meer deals te controleren en te boeken.

1. Open de juiste [lijstpagina met kortingsdeals](rebate-management-deals.md) voor het type deal waarmee u wilt werken.
1. Selecteer de rij voor elke deal die u wilt boeken (of open de deal die u wilt boeken).
1. Selecteer in het actievenster op het tabblad **Deals voor kortingbeheer** in de groep **Genereren** een van de volgende opdrachten:

    - **Boeken \> Inrichten**: boek beschikbare toerekeningstransacties die u hebt gemaakt.
    - **Boeken \> Kortingsbeheer**: boek beschikbare kortingstransacties die u hebt gemaakt.
    - **Boeken \> Afschrijven**: boek beschikbare afschrijvingstransacties die u hebt gemaakt.

1. Stel in het dialoogvenster dat verschijnt het veld **Boekingsdatum** in. Stel vervolgens de velden **Van datum** en **Tot datum** in om het datumbereik te definiëren voor de transacties die moeten worden geboekt.
1. Selecteer **OK** om de transacties te boeken.

### <a name="post-transactions-for-one-or-more-specific-deal-lines-for-a-selected-deal"></a>Transacties boeken voor een of meer specifieke dealregels voor een geselecteerde deal

Nadat u de relevante deals hebt verwerkt, volgt u deze stappen om de gegenereerde transacties voor alle regels voor een of meer specifieke dealregels voor een geselecteerde deal te controleren en te boeken. Deze procedure is alleen van toepassing op deals waarbij het veld **Afstemmen met** is ingesteld op *Regel*.

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

### <a name="post-transactions-by-using-the-rebate-workbench"></a>Transacties boeken met behulp van de kortingsworkbench

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Nadat u voorzienings-, kortings- of afschrijvingstransacties hebt verwerkt, volgt u deze stappen om de kortingsworkbench te gebruiken om de gegenereerde transacties voor een of meer specifieke transactieregels voor alle deals te controleren en te boeken.

1. Ga naar **Kortingsbeheer \> Deals voor kortingbeheer \> Kortingsworkbench**.
1. Selecteer in het raster de rij voor elke transactieregel die u wilt boeken. U kunt niet-geboekte voorzienings-, kortings- en/of afschrijvingstransacties selecteren. De volgende regels zijn van toepassing:

    - Alle regels met hetzelfde **kortingstransactienummer** als de regels die u selecteert worden ook geboekt.
    - Regels van het type *Korting* stransactie die niet als geclaimed zijn gemarkeerd, worden niet geboekt.
    - Als u reeds geboekte regels selecteert, slaat het systeem de geboekte regels over.
    - De knop **Boeken** is alleen beschikbaar als u minimaal één niet-geboekte regel selecteert.

1. Selecteer in het Actievenster op het tabblad **Kortingsworkbench** in de groep **In verwerking** de optie **Boeken**.
1. Stel in het dialoogvenster **Boeken** het veld **Boekingsdatum** in. De velden **Begindatum** en **Einddatum** worden automatisch ingesteld op basis van de vroegste **begindatum** waarde en de laatste **einddatum** waarde voor de geselecteerde rijen.
1. Selecteer **OK** om de transacties te boeken.

## <a name="review-rebate-management-journals"></a><a name="review-journals"></a>Kortingsbeheerjournalen controleren

Nadat uw transacties zijn geboekt, kunt u de resulterende dagboeken, documenten of artikelen bekijken. Doeltransacties voor kortingen en royalty's zijn gebaseerd op het betalingstype dat is ingesteld in het boekingsprofiel en het uitvoertype van de korting. Als de kortingsuitvoer bijvoorbeeld is ingesteld op *Artikel*, wordt er een verkooporder gemaakt voor een klantkorting en wordt er een inkooporder gemaakt voor een leverancierskorting. Deze orders kunnen worden bekeken via de doeltransacties. Als de betaling is ingesteld voor het gebruik van Leveranciers, wordt er een leveranciersfactuur gemaakt voor de leverancier die voor de klant is ingesteld ten behoeve van klantkortingen.

### <a name="review-journals-by-using-the-rebate-deals-list-page"></a>Journalen controleren met de lijstpagina voor kortingsdeals

Volg deze stappen om de journaalposten te controleren die zijn gekoppeld aan een kortingsbeheerdeal.

1. Open de juiste [lijstpagina met kortingsdeals](rebate-management-deals.md) voor het type deal waarmee u wilt werken.
1. Selecteer de deal waarvoor u journaalposten wilt inspecteren.
1. Selecteer in het actievenster op het tabblad **Kortingsbeheerdeals** in de groep **Transacties** de optie **Transacties** of **Garantietransacties**, afhankelijk van het type transacties dat u wilt bekijken.
1. Stel het veld **Weergeven** in op *Alle* of *Geboekt*.
1. Zoek en selecteer de transactieverzameling die u wilt inspecteren en selecteer vervolgens in het actievenster een van de volgende knoppen. (Deze knoppen zijn alleen beschikbaar als er relevante boekingen bestaan voor de geselecteerde transactieverzameling.)

    - **Doeltransacties**: bekijk relevante journalen en andere typen documenten die zijn gegenereerd door de geselecteerde deal.
    - **Artikelen**: bekijk relevante verkooporders of inkooporders die door de geselecteerde deal zijn gegenereerd.

1. Er wordt een lijst met relevante dagboeken, documenten of artikelen weergegeven. Als u meer informatie over een journaal, document of artikel wilt weergeven, selecteert u de bijbehorende rij en selecteert u vervolgens in het actievenster de optie **Details weergeven**.

### <a name="review-journals-by-using-the-rebate-workbench"></a>Journalen controleren met behulp van de kortingsworkbench

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Volg deze stappen om journalen te controleren met de kortingsworkbench.

1. Ga naar **Kortingsbeheer \> Deals voor kortingbeheer \> Kortingsworkbench**.
1. Stel het veld **Tonen** in op _Alle_ of _Geboekt_.
1. Zoek en selecteer de regel die u wilt controleren. Selecteer vervolgens in het actievenster op het tabblad **Kortingsworkbench** in de groep **Weergeven** **Doeltransacties**. Deze knop is alleen beschikbaar als er relevante boekingen bestaan voor de geselecteerde regel.
1. Er wordt een lijst met relevante dagboeken, documenten of artikelen weergegeven. Als u meer informatie over een journaal, document of artikel wilt weergeven, selecteert u de bijbehorende rij en selecteert u vervolgens in het actievenster de optie **Details weergeven**.

## <a name="rebate-management-transactions-on-the-deduction-workbench"></a>Kortingsbeheertransacties op de inhoudingsworkbench

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Wanneer u een kortingsbeheertransactie met een van de volgende **betalingstype** waarden boekt, wordt een klantinhoudingsjournaal of een vrije-tekstfactuur gemaakt voor de relevante klantrekening:

- Klantinhoudingen
- Klantinhoudingen voor belastingfacturen
- Handelsuitgave
- Rapportage

Nadat een doeltransactie is gemaakt en geboekt, is deze beschikbaar als een openstaande transactie op de pagina **Inhoudingsworkbench** (**Verkoop en marketing \> Handelstoeslagen \> Inhoudingen \> Inhoudingsworkbench**). Openstaande transacties hebben de waarde *Kortingsbeheer* als **Claimtype** en er is een waarde voor **Kortingstransactienummer** beschikbaar om traceerbaarheid in te stellen. De datum wordt ingesteld op de boekingsdatum van de doeltransactie kortingsbeheer. Als u de inhoudingsworkbench wilt gebruiken om openstaande transacties te vereffenen met bestaande inhoudingen voor dezelfde klantrekening, selecteert u **Onderhouden \> Overeenkomst** in het actievenster.

Zie voor meer informatie [Inhoudingen beheren met de inhoudingsworkbench](deduction-workbench.md).

## <a name="purge-unposted-transactions"></a>Niet-geboekte transacties leegmaken

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Nadat u voorzienings-, kortings- of afschrijvingstransacties hebt verwerkt, gaat u als volgt te werk om geselecteerde niet-boekte transacties leeg te maken.

1. Ga naar **Kortingsbeheer \> Deals voor kortingbeheer \> Kortingsworkbench**.
2. Stel het veld **Tonen** in op *Niet geboekt*.
3. Zoek en selecteer de transacties die u wilt verwijderen. Selecteer vervolgens in het actievenster op het tabblad **Kortingsworkbench** in de groep **In verwerking** de optie **Leegmaken**.
4. Klik op **OK** om de niet-geboekte transacties te verwijderen.

## <a name="cancel-a-posted-provision"></a>Een geboekte voorziening annuleren

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Nadat u een voorziening hebt verwerkt en geboekt, volgt u deze stappen om de geboekte voorzieningstransacties te annuleren.

1. Ga naar **Kortingsbeheer \> Deals voor kortingbeheer \> Kortingsworkbench**.
2. Stel het veld **Tonen** in op *Geboekt*.
3. Zoek en selecteer de inrichtingstransacties die u wilt verwijderen. Selecteer vervolgens in het actievenster op het tabblad **Kortingsworkbench** in de groep **In verwerking** de optie **Inrichting annuleren**.
4. Selecteer **OK** om de transacties om te keren.

Deze voorzieningsomkeringen worden ook weergegeven in de relevante [kortingsbeheerjournalen](#review-journals).
