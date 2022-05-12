---
title: Verbeteringen van boekingsfunctionaliteit voor overzichten
description: In dit onderwerp worden verbeteringen beschreven die zijn aangebracht in de functie voor het boeken van overzichten.
author: analpert
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: analpert
ms.search.validFrom: 2018-04-30
ms.openlocfilehash: be9aa68aec1fd7deff315234a6dbf41edc3d6819
ms.sourcegitcommit: 9e1129d30fc4491b82942a3243e6d580f3af0a29
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/27/2022
ms.locfileid: "8649014"
---
# <a name="improvements-to-statement-posting-functionality"></a>Verbeteringen van boekingsfunctionaliteit voor overzichten

[!include [banner](includes/banner.md)]

In dit onderwerp wordt de eerste set verbeteringen beschreven die zijn aangebracht in de functie voor het boeken van overzichten. Deze verbeteringen zijn beschikbaar in Microsoft Dynamics 365 for Finance and Operations 7.3.2.

## <a name="activation"></a>Activering

Standaard is tijdens de implementatie van Finance and Operations 7.3.2 het programma ingesteld op het gebruik van de oude functie voor overzichtboekingen. Als u de verbeterde functie voor het boeken van overzichten wilt inschakelen, moet u de configuratiesleutel ervoor inschakelen.

- Ga naar **Systeembeheer** \> **Instellen** \> **Licentieconfiguratie** en schakel vervolgens onder het knooppunt **Detailhandel en commerce** het selectievakje **Overzichten (verouderd)** uit en schakel het selectievakje **Overzichten** in.

Wanneer de nieuwe configuratiesleutel **Overzichten** wordt ingeschakeld, wordt een nieuw menu-item met de naam **Overzichten** beschikbaar. Met dit menu-item kunt u handmatig overzichten maken, berekenen en boeken. Elk overzicht dat een fout veroorzaakt wanneer het batchboekingsproces wordt gebruikt, is ook beschikbaar via dit menu-item. (Wanneer de configuratiesleutel **Overzichten (verouderd)** wordt ingeschakeld, krijgt het menu-item de naam **Openstaande overzichten**.)

Commerce bevat de volgende validaties die zijn gerelateerd aan deze configuratiesleutels:

- Beide configuratiesleutels kunnen niet tegelijkertijd worden ingeschakeld.
- Dezelfde configuratiesleutels moeten worden gebruikt voor alle bewerkingen die worden uitgevoerd voor een bepaald overzicht tijdens de levenscyclus (Maken, Berekenen, Wissen, Boeken, enzovoort). U kunt bijvoorbeeld geen overzicht maken en berekenen terwijl de configuratiesleutel **Overzicht (verouderd)** is ingeschakeld en vervolgens hetzelfde overzicht probeert te boeken terwijl de configuratiesleutel **Overzicht** is ingeschakeld.

> [!NOTE]
> Wij raden u aan de configuratiesleutel **Overzichten** voor de verbeterde overzichtsboekingsfunctie te gebruiken, tenzij u dwingende redenen hebt om de configuratiesleutel **Overzichten (verouderd)** in plaats daarvan te gebruiken. Microsoft blijft investeren in de nieuwe en verbeterde overzichtsboekingsfunctie en het is belangrijk dat u er zo snel mogelijk naar overschakelt om ervan te kunnen profiteren. De verouderde overzichtsboekingsfunctie is vanaf versie 8.0 afgeschaft.

## <a name="setup"></a>Instellen

Als onderdeel van de nieuwe overzichtsboekingsfunctie zijn er drie nieuwe parameters geïntroduceerd op het sneltabblad **Overzicht** op het tabblad **Boeken** van de pagina **Commerce-parameters**:

- **Overzicht wissen uitschakelen** : deze optie is alleen van toepassing op de verouderde functie voor het boeken van overzichten. Het is raadzaam dat u deze optie instelt op **Nee** om te voorkomen dat gebruikers overzichten wissen die half geboekt zijn. Als overzichten die half zijn geboekt worden gewist, raken gegevens beschadigd. U moet deze optie alleen in uitzonderlijke omstandigheden instellen op **Ja**.
- **Voorraad reserveren tijdens berekening**: wij raden u aan de batchtaak **Voorraad boeken** te gebruiken voor voorraadreservering en deze optie in te stellen op **Nee**. Als deze optie is ingesteld op **Nee**, wordt met de verbeterde functie voor het boeken van overzichten niet geprobeerd voorraadreserveringsposten te maken op het moment van berekening (als posten niet al zijn gemaakt via de batchtaak **Voorraad boeken**). In plaats daarvan worden met de functie alleen voorraadreserveringsposten gemaakt op het moment van boeken. Deze implementatie was een ontwerpkeuze en was gebaseerd op het feit dat het tijdvenster tussen het berekeningsproces en het boekingsproces doorgaans klein is. Als u voorraad echter wilt reserveren ten tijde van de berekening, kunt u deze optie instellen op **Ja**.

    Met de verouderde functie voor het boeken van overzichten wordt voorraad altijd gereserveerd tijdens het berekeningsproces van overzichten (als reservering niet al is gedaan via de batchtaak **Voorraad boeken**), ongeacht de instelling van deze optie.

- **Telling uitschakelen vereist**: wanneer deze optie is ingesteld op **Ja**, wordt het boekingsproces voor een overzicht voortgezet, zelfs als het verschil tussen het getelde bedrag en het transactiebedrag op het overzicht buiten de drempelwaarde valt die is gedefinieerd op het sneltabblad **Overzicht** voor winkels.

> [!NOTE]
> Wanneer vanaf Commerce versie 10.0.14 de functie **Detailhandeloverzichten - groepsgewijze invoer** wordt ingeschakeld , is de batchtaak **Voorraad boeken** niet meer van toepassing en kan deze niet meer worden uitgevoerd.

## <a name="processing"></a>Bezig met verwerken

Overzichten kunnen worden berekend en geboekt in een batch met de menu-items **Overzichten in batch berekenen** en **Overzichten in batch boeken**. Overzichten kunnen ook worden berekend en geboekt met behulp van het menu-item **Overzichten** dat de verbeterde functie voor het boeken van overzichten verschaft.

Het proces en de stappen voor het berekenen en boeken van overzichten in een batch zijn hetzelfde als in de verouderde functie voor het boeken van overzichten. Er zijn echter belangrijke verbeteringen aangebracht in de back-endverwerking van de overzichten. Deze verbeteringen maken het proces flexibeler en bieden een beter inzicht in de statuswaarden en de foutinformatie. Gebruikers kunnen daarom de hoofdoorzaak van fouten aanpakken en vervolgens doorgaan met het boekingsproces zonder dat gegevens beschadigd raken en zonder dat gegevens moeten worden gecorrigeerd.

In de volgende secties worden enkele belangrijke verbeteringen voor de functie voor het boeken van overzichten beschreven die worden weergegeven in de gebruikersinterface voor overzichten en geboekte overzichten.

### <a name="status-details"></a>Statusgegevens

Er is een nieuw statusmodel geïntroduceerd in de overzichtboekingsroutine voor het berekenings- en boekingsproces.

In de volgende tabel worden de verschillende statuswaarden en de volgorde ervan tijdens het berekeningsproces beschreven.

| Statusvolgorde | Provincie      | Omschrijving |
|-------------|------------|-------------|
| 1           | Begonnen    | Het overzicht is gemaakt en kan worden berekend. |
| 2           | Gemarkeerd     | De transacties die binnen het bereik van het overzicht vallen, worden geïdentificeerd op basis van de overzichtsparameters en ze worden gemarkeerd met de overzichts-ID. |
| 3           | Berekend | De overzichtsregels worden berekend en weergegeven. |

In de volgende tabel worden de verschillende statuswaarden en de volgorde ervan tijdens het boekingsproces beschreven.

| Statusvolgorde | Provincie                   | Omschrijving |
|-------------|-------------------------|-------------|
| 1           | Gecontroleerd                 | Meerdere validaties worden uitgevoerd die betrekking hebben op parameters (bijvoorbeeld de beschikkingstoeslag) en op het overzicht en de overzichtsregels (bijvoorbeeld het verschil tussen het getelde bedrag en het transactiebedrag). |
| 2           | Samengevoegd              | Verkooptransacties voor klanten met en zonder naam worden samengevoegd op basis van de configuratie. Elke samengevoegde transactie wordt uiteindelijk geconverteerd naar een verkooporder. |
| 3           | Klantorder gemaakt  | Op basis van de samengevoegde transactie worden verkooporders in het systeem gemaakt. |
| 4           | Klantorder gefactureerd | Verkooporders worden gefactureerd. |
| 5           | Kortingen geboekt        | Periodieke kortingsjournalen worden geboekt op basis van de configuratie. |
| 6           | Inkomsten/uitgaven geboekt   | Inkomsten-/uitgaventransacties worden als boekstukken geboekt. |
| 7           | Boekstukken gekoppeld         | Betalingsjournalen worden gemaakt en gekoppeld aan de bijbehorende factuur. |
| 8           | Betalingen geboekt         | Betalingsjournalen worden geboekt. |
| 9           | Geschenkbonnen geboekt       | Geschenkbontransacties worden als boekstukken geboekt. |
| 10          | Geboekt                  | Het overzicht wordt gemarkeerd als geboekt. |

Elke status in de voorgaande tabellen is onafhankelijk van aard en er wordt een hiërarchische afhankelijkheid tussen de statuswaarden gemaakt. Deze afhankelijkheid loopt van boven naar beneden. Als het systeem fouten aantreft tijdens het verwerken van een status, wordt de status van het overzicht weer ingesteld op de vorige status. Een eventuele latere nieuwe poging van het proces wordt hervat vanuit de mislukte status voorwaarts. Deze benadering heeft de volgende voordelen:

- De gebruiker heeft volledig zicht op de status waarin de fout is opgetreden.
- Gegevensbeschadiging wordt voorkomen. In de verouderde functie voor het boeken van overzichten waren er bijvoorbeeld gevallen waarin sommige verkooporders werden gefactureerd, maar andere open bleven staan. Er waren ook gevallen waarin sommige betalingsjournalen geen bijbehorende factuur voor vereffening hadden, omdat er een fout zat in de factuurboeking.
- Gebruikers kunnen de huidige status van een overzicht bekijken met de knop **Statusdetails** in de groep **Uitvoeringsdetails** van het overzicht. De statusdetailpagina bestaat uit drie gedeelten:

    - Het eerste deel toont de huidige status van het overzicht, samen met de foutcode en een gedetailleerd foutbericht als er een fout opgetreden.
    - Het tweede deel toont de verschillende statuswaarden van het berekeningsproces. Visuele aanwijzingen geven statuswaarden aan die met succes zijn uitgevoerd, statuswaarden die niet kunnen worden uitgevoerd vanwege fouten en statuswaarden die nog niet zijn uitgevoerd.
    - Het derde deel bevat de verschillende statuswaarden van het boekingsproces. Visuele aanwijzingen geven statuswaarden aan die met succes zijn uitgevoerd, statuswaarden die niet kunnen worden uitgevoerd vanwege fouten en statuswaarden die nog niet zijn uitgevoerd.

De koptekst van het tweede en derde gedeelte bevat bovendien de algemene status van het desbetreffende proces.

### <a name="event-logs"></a>Gebeurtenislogboeken

Een overzicht doorloopt verschillende bewerkingen (zoals maken, berekenen, wissen en boeken) en er kunnen meerdere exemplaren van dezelfde bewerking worden aangeroepen tijdens de levenscyclus van het overzicht. Nadat een overzicht is gemaakt en berekend, kan een gebruiker bijvoorbeeld het overzicht wissen en opnieuw berekenen. De knop **Gebeurtenislogboeken** in de groep **Uitvoeringsdetails** van het overzicht biedt een complete audittrail van de verschillende bewerkingen die zijn aangeroepen in een overzicht, samen met informatie over de bewerkingen die zijn aangeroepen.

### <a name="aggregated-transactions"></a>Getotaliseerde transacties

Tijdens het boekingsproces worden contante transacties samengevoegd per klant en product. Hierdoor worden minder verkooporders en -regels gemaakt. De samengevoegde transacties worden in het systeem opgeslagen en gebruikt om verkooporders te maken. Met elke samengevoegde transactie wordt één bijbehorende verkooporder in het systeem gemaakt. 

Als een overzicht niet volledig is geboekt, kunt u samengevoegde transacties in het overzicht weergeven. Selecteer in het actievenster op het tabblad **Overzicht** in de groep **Uitvoeringsdetails** de optie **Getotaliseerde transacties**.

![De knop Samengevoegde transacties voor een overzicht dat niet volledig is geboekt.](media/aggregated-transactions.png)

Voor geboekte overzichten kunt u samengevoegde transacties op de pagina **Geboekte overzichten** weergeven. Selecteer **Query's** in het actiedeelvenster en selecteer vervolgens **Getotaliseerde transacties**.

![Opdracht Getotaliseerde transacties voor geboekte overzichten.](media/aggregated-transactions-posted-statements.png)

Het sneltabblad **Details van verkooporder** van een samengevoegde transactie bevat de volgende informatie:

- **Record-ID**: de ID van de samengevoegde transactie.
- **Overzichtsnummer**: het overzicht waartoe de samengevoegde transactie behoort.
- **Datum**: de datum waarop de samengevoegde transactie is gemaakt.
- **Verkoop-ID**: wanneer een verkooporder wordt gemaakt op basis van de samengevoegde transactie, de id van de verkooporder. Als dit veld leeg is, is de bijbehorende verkooporder nog niet gemaakt.
- **Aantal samengevoegde regels**: het totale aantal regels voor de samengevoegde transactie en de verkooporder.
- **Status**: de laatste status van de samengevoegde transactie.
- **Factuur-ID**: wanneer de verkooporder voor de samengevoegde transactie wordt gefactureerd, de id van de verkoopfactuur Als dit veld leeg is, is de factuur voor de verkooporder niet geboekt.
- **Foutcode:** dit veld wordt ingesteld als de samenvoeging een fout bevat.
- **Foutbericht:** dit veld wordt ingesteld als de samenvoeging een fout bevat. Het geeft details weer over de oorzaak van het mislukken van het proces. U kunt de informatie in de foutcode gebruiken om het probleem op te lossen en het proces vervolgens handmatig opnieuw starten. Afhankelijk van het type oplossing moeten samengevoegde verkopen mogelijk worden verwijderd en verwerkt in een nieuw overzicht.

![Velden op het sneltabblad Verkooporderdetails van een samengevoegde transactie.](media/aggregated-transactions-error-message-view.png)

Het sneltabblad **Transactiedetails** van een samengevoegde transactie bevat alle transacties die naar de samengevoegde transactie zijn gehaald. De samengevoegde regels op de samengevoegde transactie tonen alle samengevoegde records van de transacties. De samengevoegde regels bevatten ook details zoals artikel, variant, hoeveelheid, prijs, nettobedrag, eenheid en magazijn. In principe komt elke samengevoegde regel overeen met één verkooporderregel.

![Het sneltabblad Transactiedetails van een samengevoegde transactie.](media/aggregated-transactions-sales-details.png)

In bepaalde situaties kunnen samengevoegde transacties hun geconsolideerde verkooporder mogelijk niet boeken. In deze situaties wordt een foutcode aan de overzichtsstatus gekoppeld. Als u alleen samengevoegde transacties met fouten wilt weergeven, kunt u het filter **Alleen fouten weergeven** in de weergave van samengevoegde transacties inschakelen door het selectievakje in te schakelen. Als u dit filter inschakelt, beperkt u de resultaten tot samengevoegde transacties met fouten die een oplossing vereisen. Zie [Online orders en asynchrone ordertransacties van klanten bewerken en controleren](edit-order-trans.md) voor informatie over het oplossen van deze problemen.

![Selectievakje voor het filter Alleen weergeven in de weergave van samengevoegde transacties.](media/aggregated-transactions-failure-view.png)

Op de pagina **Samengevoegde transacties** kunt u de XML voor een specifieke samengevoegde transactie downloaden door **Aggregatiegegevens exporteren**. U kunt de XML in elke XML-indeling controleren om de werkelijke gegevens te bekijken die betrekking hebben op het maken en boeken van verkooporders. De functionaliteit voor het downloaden van de XML voor samengevoegde transacties is niet beschikbaar voor overzichten die zijn geboekt.

![De knop Aggregatiegegevens exporteren op de pagina Samengevoegde transacties.](media/aggregated-transactions-export.png)

Als u de fout niet kunt herstellen door gegevens in de verkooporder of gegevens die de verkooporder ondersteunen te corrigeren, is een knop **Klantorder verwijderen** beschikbaar. Als u een order wilt verwijderen, selecteert u de samengevoegde transactie die is mislukt en **Klantorder verwijderen**. Zowel de samengevoegde transactie als de bijbehorende verkooporder wordt verwijderd. U kunt de transacties nu controleren met de functie voor bewerken en controleren. U kunt ze ook opnieuw verwerken via een nieuw overzicht. Nadat alle fouten zijn opgelost, kunt u de overzichtsboeking hervatten door de functie voor het boeken van overzichten voor het betreffende overzicht uit te voeren.

![De knop Klantorder verwijderen in de weergave van samengevoegde transacties.](media/aggregated-transactions-delete-cust-order.png)

De weergave met samengevoegde transacties biedt de volgende voordelen:

- De gebruiker heeft zicht op de samengevoegde transacties die zijn mislukt tijdens het maken van verkooporders en de verkooporders die zijn mislukt tijdens het factureren.
- De gebruiker heeft zicht op de wijze waarop transacties worden samengevoegd.
- De gebruiker heeft een volledige audittrail, van transacties tot verkooporders, tot verkoopfacturen. Deze audittrail was niet beschikbaar in de verouderde functie voor het boeken van overzichten.
- Samengevoegde XML-bestanden maken het eenvoudiger om problemen te identificeren tijdens het maken van verkooporders en tijdens facturering.

### <a name="journal-vouchers"></a>Journaalboekstukken

De knop **Journaalboekstukken** in de groep **Uitvoeringsdetails** van het overzicht bevat alle verschillende boekstuktransacties die zijn gemaakt voor een overzicht en die zijn gerelateerd aan kortingen, rekeningen voor inkomsten/uitgaven, geschenkbonnen, enzovoort.

Op dit moment laat het programma deze gegevens alleen voor geboekte overzichten zien.

### <a name="payment-journals"></a>Betalingsjournalen

De knop **Betalingsjournalen** in de groep **Uitvoeringsdetails** van het overzicht bevat alle verschillende betalingsjournalen die zijn gemaakt voor een overzicht.

Op dit moment laat het programma deze gegevens alleen voor geboekte overzichten zien.

## <a name="other-improvements"></a>Andere verbeteringen

Andere back-endverbeteringen die gebruikers kunnen zien, zijn aangebracht in de functie voor het boeken van overzichten. Hieronder vindt u enkele voorbeelden:

- Bij de samenvoeging wordt geen rekening gehouden met personeels-, terminal- en dienstentiteiten. Omdat er minder parameters voor samenvoeging zijn, moeten er minder verkooporderregels worden verwerkt.
- Een impasse voor transactietabellen vindt minder vaak plaats door aanvullende extensietabellen te introduceren en invoegbewerkingen uit te voeren in plaats van bijwerkbewerkingen in de transactietabellen.
- Het aantal actieve batchtaken is met parameters ingesteld en beperkt. Daarom kan dit aantal beter worden afgestemd op de omgeving van een klant. In de verouderde functie voor het boeken van overzichten werd een onbeperkt aantal batchtaken tegelijkertijd gemaakt. Het resultaat was onbeheerbare belastingen, overhead en problemen op de batchserver.
- Overzichten worden efficiënt in de wachtrij geplaatst voor verwerking door prioriteit te geven aan de overzichten die het maximum aantal transacties bevatten.
- Batchprocessen zoals **Overzicht in batch berekenen** en **Overzichten in batch boeken** worden alleen in batchmodus uitgevoerd. In de verouderde functie voor het boeken van overzichten kunnen gebruikers ervoor kiezen deze batchprocessen uit te voeren in een interactieve modus die één bewerking met threads behelst in tegenstelling tot batchprocessen die meerdere threads bevatten.
- In de verouderde functie voor het boeken van overzichten kreeg de gehele batchtaak de foutstatus als er een fout optrad in de batchtaak. In de verbeterde functie zorgen batchtaakfouten er niet voor dat de gehele batchtaak een foutstatus krijgt als andere batchtaken met succes worden voltooid. U moet de boekingsstatus voor een batchuitvoering beoordelen met behulp van de pagina **Overzichten** waarop u alle overzichten kunt zien die niet zijn geboekt vanwege fouten.
- In de verouderde functie voor het boeken van overzichten zorgde de eerste fout in een overzicht ervoor dat de gehele batch mislukte. De resterende overzichten worden niet verwerkt. In de verbeterde functie blijft het batchproces alle overzichten verwerken, zelfs als sommige van de overzichten mislukken. Eén voordeel is dat gebruikers zicht krijgen op het exacte aantal overzichten dat fouten bevat. Gebruikers hoeven dus niet steeds maar fouten op te blijven lossen en het boekingsproces van overzichten uit te voeren totdat alle overzichten zijn geboekt.

## <a name="general-guidance-about-the-statement-posting-process"></a>Algemene richtlijnen voor het boekingsproces van overzichten

- We raden u aan het overzichtboekingsproces in een batch uit te voeren, omdat bij batchuitvoeringen wordt geprofiteerd van de kracht van het batchframework in termen van meerdere threads. Meerdere threads zijn vereist voor het verwerken van enorme aantallen transacties die normaal gesproken in overzichtboekingen worden gezien.
- Wij raden u aan negatieve fysieke voorraad in de artikelmodelgroep in te schakelen voor een naadloze boekingservaring. In sommige scenario´s kunnen negatieve overzichten alleen worden geboekt als er negatieve fysieke voorraad is. Als er bijvoorbeeld in theorie slechts één eenheid van een artikel in voorraad is en er zijn een verkooptransactie en een retourtransactie voor het artikel geweest, moet de transactie kunnen worden geboekt, zelfs als negatieve voorraad niet is ingeschakeld. Omdat met het boekingsproces voor overzichten zowel de verkooptransactie als de retourtransactie in één klantorder worden opgehaald, is er echter geen garantie dat de verkoopregel eerst wordt geboekt, gevolgd door de retourregel. Daarom kunnen er fouten optreden. Als negatieve voorraad in dit scenario wordt ingeschakeld, wordt de transactieboeking niet negatief beïnvloed en wordt de voorraad correct in het systeem weergegeven.
- Wij raden u aan samenvoeging te gebruiken tijdens het berekenen en boeken van overzichten. Daarom worden de volgende instellingen aanbevolen voor bepaalde samenvoegingsparameters:

    - Ga naar **Detailhandel en commerce** \> **Instelling van hoofdkantoor** \> **Parameters** \> **Commerce-parameters**. Selecteer op het tabblad **Boeken** op het sneltabblad **Voorraadbijwerking** in het veld **Detailniveau** **Overzicht**.
    - Ga naar **Detailhandel en commerce** \> **Instelling van hoofdkantoor** \> **Parameters** \> **Commerce-parameters**. Stel vervolgens op het tabblad **Boeken** op het sneltabblad **Samenvoeging** de optie **Boekstuktransacties** in op **Ja**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
