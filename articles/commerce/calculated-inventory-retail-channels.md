---
title: Beschikbaarheid van voorraad berekenen voor detailhandelskanalen
description: In dit onderwerp worden de opties beschreven die beschikbaar zijn voor het weergeven van de voorhanden voorraad voor de winkel- en online kanalen.
author: hhainesms
manager: annbe
ms.date: 08/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhainesms
ms.search.validFrom: 2020-02-11
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 6d25a426268ebfb6990eb3dadb1ad451f86f59a1
ms.sourcegitcommit: 65a8681c46a1d99e7ff712094f472d5612455ff0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/13/2020
ms.locfileid: "3694917"
---
# <a name="calculate-inventory-availability-for-retail-channels"></a>Beschikbaarheid van voorraad berekenen voor detailhandelskanalen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe een bedrijf Microsoft Dynamics 365 Commerce kan gebruiken om de geschatte beschikbaarheid van voorhanden voorraad te bekijken voor producten in de online- en winkelkanalen.

## <a name="accuracy-of-calculation"></a>Nauwkeurigheid van berekening

Commerce gebruikt meerdere servers en databases om schaalbaarheid en prestaties te garanderen. Het is daarom belangrijk dat u begrijpt dat de waarden voor de beschikbare voorraad die worden geleverd via de POS-toepassing, de Application Programming Interfaces (API's) voor voorraadbeschikbaarheid van e-Commerce en de pagina's voor voorhanden voorraad in Commerce Headquarters mogelijk niet 100 procent nauwkeurig zijn in realtime. Als transacties die zijn gemaakt voor producten in het online- of winkelkanaal nog niet zijn gesynchroniseerd met de Commerce Headquarters-server en -database, wordt op de pagina's met voorhanden voorraad in Commerce Headquarters mogelijk niet altijd een accurate waarde voor de realtime voorraad weergegeven voor deze producten. Omgekeerd geldt dat, als u uw bedrijf zo hebt geconfigureerd dat gebruikers in Commerce Headquarters of andere geïntegreerde toepassingen de voorraad kunnen verkopen, ontvangen, retourneren of anderszins aanpassen vanuit een winkel of online magazijn, het POS- of online kanaal mogelijk niet over alle informatie beschikt die is vereist om een accurate realtime waarde voor voorhanden voorraad van artikelen weer te geven.

In dit onderwerp worden de processen voor gegevenssynchronisatie beschreven die regelmatig kunnen worden uitgevoerd om de latentie van gegevens tussen toepassingen of kanalen te beperken. Het is echter van cruciaal belang dat u begrijpt dat alle beschikbaarheidsgegevens over voorhanden voorraad die tijdens de werkdag worden verstrekt, als een geschatte waarde worden beschouwd. Dus als u probeert de gegevens over de voorhanden voorraad te vergelijken met de werkelijke fysieke voorraad op de planken of als u probeert de waarden voor de voorhanden voorraad die in POS worden weergegeven te vergelijken met de gegevens die u hebt gevonden voor hetzelfde magazijn in Commerce Headquarters kunnen de waarden verschillen. Dit verschil tijdens de werkdag wordt verwacht en mag niet als een probleem worden beschouwd. Als u gegevens wilt controleren en ervoor wilt zorgen dat de waarden die zijn opgegeven in de API's voor voorraadbeschikbaarheid en Commerce Headquarters overeenkomen met de werkelijke fysieke eenheden die u vindt op uw winkel- of magazijnplanken, kunt u dit het beste doen nadat kanaalbewerkingen zijn gestopt voor de dag en alle transacties correct zijn gesynchroniseerd tussen Commerce Headquarters en het kanaal.

## <a name="use-inventory-lookup-apis-for-e-commerce-inventory-availability-requests"></a>API's voor het opzoeken van voorraad gebruiken voor beschikbaarheidsaanvragen voor voorraad in e-Commerce

U kunt de volgende API's gebruiken om de beschikbaarheid van voorraad voor een product weer te geven wanneer uw klanten op een e-Commerce-site winkelen.

- **GetEstimatedAvailability**: gebruik deze API om voorraadbeschikbaarheid voor het artikel op te halen in het magazijn van het e-Commerce-afzetkanaal of alle magazijnen die zijn gekoppeld aan de configuratie van de afhandelingsgroep voor het e-Commerce-afzetkanaal. Deze API kan ook worden gebruikt voor magazijnen in een bepaald zoekgebied of een bepaalde radius, op basis van gegevens over lengte- en breedtegraad.
- **GetEstimatedProductWarehouseAvailability**: gebruik deze API om voorraad voor een artikel uit een bepaald magazijn aan te vragen. U kunt deze bijvoorbeeld gebruiken om de beschikbaarheid van voorraad weer te geven in scenario's waarbij orders worden opgehaald.

> [!NOTE]
> Deze API's vervangen de API's **GetProductAvailabilities** en **GetAvailableInventoryNearby** in Dynamics 365 Retail versie 10.0.7 en eerder.

Beide API's halen gegevens op van de Commerce Server en geven een schatting van de voorhanden voorraad voor een specifieke combinatie van een product of productvariant en een magazijn. Hoewel andere API's die beschikbaar zijn op de Commerce Server direct naar Commerce Headquarters kunnen gaan om voorhanden hoeveelheden van producten op te halen, raden wij u niet aan deze te gebruiken in een e-Commerce-omgeving vanwege mogelijke prestatieproblemen en de daaraan verwante gevolgen voor veelvuldige aanvragen op uw Commerce Headquarters-servers. Als de voorhanden voorraad wordt berekend via de Commerce Server, is bij de berekening waarschijnlijk de voorraad inbegrepen die is verkocht in recente e-Commerce-transacties die nog niet zijn gesynchroniseerd met Commerce Headquarters. Hoewel in Commerce Headquarters mogelijk geen informatie over deze transacties wordt weergegeven, bevatten de Commerce Server en kanaaldatabase de gegevens. Daarom wordt rekening gehouden met de gegevens en kunnen deze bijdragen aan een nauwkeurigere schatting van de beschikbare voorraad van een product.

### <a name="get-started-with-e-commerce-calculated-inventory-availability"></a>Aan de slag met door e-Commerce berekende voorraadbeschikbaarheid

Voordat u de twee API's gebruikt die eerder zijn genoemd, moet u de functie **Geoptimaliseerde berekening voor productbeschikbaarheid** via het werkgebied **Functiebeheer** in Commerce Headquarters inschakelen.

Voordat de API's de beste schatting van de voorraadbeschikbaarheid voor een artikel kunnen berekenen, moet er een periodieke momentopname van de voorraadbeschikbaarheid vanuit Commerce Headquarters worden verwerkt en naar de kanaaldatabase worden verzonden die door de Commerce Scale Unit van e-Commerce wordt gebruikt. De momentopname staat voor de informatie die in Commerce Headquarters beschikbaar is over de voorraadbeschikbaarheid voor een specifieke combinatie van een product of productvariant en een magazijn. Het kan voorraadcorrecties of mutaties bevatten die worden veroorzaakt door voorraadontvangsten of door zendingen of andere processen die in Commerce Headquarters worden uitgevoerd en die alleen informatie bevat over het e-Commerce-afzetkanaal vanwege het synchronisatieproces.

Met de database-momentopname die door de taak **Beschikbaarheid product** wordt gemaakt, worden alleen de voorraadtransacties berekend die zijn verwerkt en geboekt in Commerce Headquarters op het moment waarop de momentopname werd gemaakt. Als er voorraad voor een product in een winkelmagazijn is verkocht via een contante transactie of een asynchrone verkooporder voor een klant in de POS-toepassing, beschikt Commerce Headquarters niet onmiddellijk over informatie over de bijbehorende transactie voor voorraaduitgifte voor de verkoop. Het bevat alleen informatie over de voorraad die voor deze typen winkelverkoop wordt verkocht nadat de P-taak de gerelateerde transactie heeft geüpload vanuit de kanaaldatabase van de winkel naar Commerce Headquarters en de bijbehorende verkooporder is gemaakt via een overzichtboeking of de processen voor groepsgewijs boeken. Tijdens het maken van de order in Commerce Headquarters worden de bijbehorende voorraadtransacties gemaakt. Voor e-Commerce-afzetkanaalorders beschikt Commerce Headquarters alleen over informatie over de voorraadtransacties nadat de transacties naar Commerce Headquarters zijn verzonden via de P-taak en het ordersynchronisatieproces is voltooid. Het is daarom belangrijk dat u begrijpt dat de waarde van de momentopname van de voorraad die in de taak **Beschikbaarheid product** wordt geleverd, in realtime niet 100 procent nauwkeurig is vanwege de constante verkoopverwerking die wordt uitgevoerd op gedistribueerde servers.

Voer de volgende stappen uit om een momentopname te maken van de voorraad in Commerce Headquarters.

1. Ga naar **Detailhandel en commerce \> IT detailhandel en commerce \> Producten en voorraad \> Beschikbaarheid product**.
1. Selecteer **OK** om de taak **Beschikbaarhied product** uit te voeren. U kunt deze taak ook plannen zodat deze wordt uitgevoerd in een batch.

Nadat de taak **Beschikbaarheid product** is voltooid, moeten de opgenomen gegevens naar de e-commerce-afzetkanaaldatabases worden gepusht, zodat de meest recente momentopname van de voorraad voor Commerce Headquarters kan worden meegenomen bij de berekening van de geschatte voorhanden voorraad.

1. Ga naar **Retail en Commerce \> Retail en Commerce IT \> Distributieplanning**.
1. Voer de taak **1130** (**Beschikbaarheid product**) uit om de momentopnamegegevens te synchroniseren die met de taak **Beschikbaarheid product** zijn gemaakt vanuit Commerce Headquarters naar uw kanaaldatabases.

Wanneer de beschikbaarheid van voorraad wordt opgevraagd vanuit de API **GetEstimatedAvailabilty** of **GetEstimatedProductWarehouseAvailability**, wordt een berekening uitgevoerd om de best mogelijke schatting van de voorraad voor het product te krijgen. De berekening verwijst naar alle e-Commerce-klantorders die zich in de kanaaldatabase bevinden, maar die niet zijn opgenomen in de gegevens voor de momentopname die de taak 1130 heeft geleverd. Deze logica wordt uitgevoerd door de laatste verwerkte voorraadtransactie van Commerce Headquarters te traceren en deze te vergelijken met de transacties in de kanaaldatabase. Het biedt een basislijn voor de berekeningslogica aan de kanaalzijde, zodat de extra voorraadmutaties die zijn opgetreden voor verkooptransacties van klantorders in de e-commerce-kanaaldatabase kunnen worden meegenomen in de geschatte voorraadwaarde die de API levert.

De berekeningslogica aan de kanaalzijde retourneert een geschatte fysieke beschikbaarheidswaarde en een totale beschikbaarheidswaarde voor het aangevraagde product en magazijn. De waarden kunnen op uw e-Commerce-site worden weergegeven als u dat wilt, of ze kunnen worden gebruikt om andere bedrijfslogica op uw e-Commerce-site te activeren. U kunt bijvoorbeeld een bericht 'niet-voorradig' weergeven in plaats van de werkelijke voorhanden hoeveelheid die door de API is doorgegeven.

De berekeningslogica die door de API's van e-Commerce voor de geschatte voorraadwaarde aan de kanaalzijde wordt gebruikt, kan alleen de voorraad bepalen op basis van klantorders die zijn gemaakt in de kanaaldatabase, maar die nog niet zijn gesynchroniseerd en geboekt in Commerce Headquarters. Als uw kanaaldatabase ook transactiegegevens bevat voor contante verkopen voor winkelmagazijnen, worden de contante verkopen niet opgenomen in de berekening aan de kanaalzijde van e-Commerce voor die magazijnen.

## <a name="configure-the-inventory-lookup-operation-in-the-pos-channel"></a>De bewerking voor zoeken naar voorraad in het POS-kanaal configureren

In Retail versie 10.0.9 en eerder werd gebruikgemaakt van de bewerking **Zoeken in voorraad** vanuit POS een realtime serviceaanroep naar Commerce Headquarters om voorraadinformatie op te halen voor het geselecteerde product, voor zowel de huidige winkel als andere winkels die zijn geconfigureerd voor de afhandelingsgroep als onderdeel van de kanaalconfiguratie voor de winkel. In Commerce versie 10.0.10 en hoger kunt u real-time serviceaanroepen naar Commerce Headquarters uitschakelen. In plaats daarvan kunt u de berekening aan de kanaalzijde op de Commerce Server gebruiken om de voorhanden voorraad te bepalen die fysiek beschikbaar is voor de winkel en andere locaties die in de afhandelingsgroep zijn gedefinieerd. Deze voor het kanaal berekende voorraadconfiguratie is ook handig voor locaties waar de internetverbinding onbetrouwbaar is, omdat u niet online hoeft te zijn om zoekacties voor voorraad vanuit Commerce Headquarters te kunnen ophalen.

Wanneer de berekening aan kanaalzijde op de juiste manier wordt geconfigureerd en beheerd, kan het een betrouwbaardere schatting van de huidige winkelvoorraad leveren, omdat deze de transactionele gegevens gebruikt die zich in de Commerce-kanaaldatabase bevinden, maar waarover Commerce Headquarters mogelijk nog geen informatie heeft. Als u bijvoorbeeld de bestaande realtime serviceaanroep voor het zoeken van voorraad in POS gebruikt, beschikt Commerce Headquarters waarschijnlijk nog niet over informatie over een contante verkoop die zojuist heeft plaatsgevonden voor een product. De voorhanden voorraadwaarde die door Commerce Headquarters wordt geretourneerd voor dat product zal waarschijnlijk één eenheid hoger zijn dan de werkelijke voorhanden voorraad van de winkel. Als u echter gebruikmaakt van de berekening aan kanaalzijde, kan de contante verkoop worden opgenomen in de berekening en worden afgetrokken van de waarde voor de voorhanden voorraad die wordt weergegeven. Hoewel de waarden die zowel door de berekening aan kanaalzijde als door de realtime serviceaanroepen worden geleverd, slechts ramingen zijn van de voorhanden voorraad, is het veel waarschijnlijker dat de waarde die de kanaalzijde biedt nauwkeurig is voor de huidige winkel.

### <a name="get-started-with-pos-channel-side-calculated-inventory-availability"></a>Aan de slag met door POS aan kanaalzijde berekende voorraadbeschikbaarheid

Als u de berekeningslogica aan de kanaalzijde wilt gebruiken en aanroepen van real-time service wilt uitschakelen voor voorraadzoekopdrachten vanuit de POS-toepassing, moet u eerst de functie **Geoptimaliseerde berekening voor productbeschikbaarheid** inschakelen via het werkgebied **Functiebeheer** in Commerce Headquarters. U moet niet alleen de functie inschakelen, maar ook wijzigingen aanbrengen in het **functionaliteitsprofiel**.

Volg deze stappen om het **functionaliteitsprofiel** te wijzigen:

1. Ga naar **Retail en Commerce \> Kanaalinstellingen \> POS-instellingen \> POS-profielen \> Functionaliteitsprofielen**.
1. Selecteer een functionaliteitsprofiel.
1. Wijzig op het sneltabblad **Functies** in de sectie **Berekening van voorraadbeschikbaarheid** de waarde van het veld **Modus voor berekening van voorraadbeschikbaarheid** van **Realtime service** in **Kanaal**. Alle functionaliteitsprofielen gebruiken standaard realtime serviceaanroepen. Daarom moet u de waarde van dit veld wijzigen als u de berekeningslogica aan kanaalzijde wilt gebruiken. Elke detailhandelwinkel die is gekoppeld aan het geselecteerde functionaliteitsprofiel wordt beïnvloed door deze wijziging.

U moet vervolgens de wijzigingen via het distributieschemaproces naar het kanaal synchroniseren door de volgende stappen uit te voeren:

1. Ga naar **Retail en Commerce \> Retail en Commerce IT \> Distributieplanning**.
1. Voer de taak **1070** (**Kanaalconfiguratie**) uit.

Nadat de configuratie is voltooid, maakt de informatie over de fysiek beschikbare voorraad niet langer gebruik van een realtime serviceaanroep wanneer een gebruiker in de POS-toepassing de bewerking **Zoeken in voorraad** (standaard- en matrixweergaven) gebruikt. In plaats daarvan worden gegevens over fysiek beschikbare voorraad voor de huidige winkel en alle winkels in de afhandelingsgroep berekend op basis van de laatst bekende momentopname die vanuit Commerce Headquarters aan de kanaaldatabase is geleverd. De waarde van de momentopname wordt verder verfijnd door de berekening aan kanaalzijde om de fysiek beschikbare waarde aan te passen, op basis van aanvullende verkoop- of retourtransacties voor het geselecteerde product in de kanaaldatabase die niet zijn opgenomen in de laatste gesynchroniseerde momentopname van de taak 1130. Als de kanaaldatabase geen transactiegegevens bevat voor een of meer magazijnen of winkels in de afhandelingsgroep, bevat de database geen extra transacties die kunnen worden opgenomen in een herberekening van de waarde. Daarom bestaat de beste schatting van voorhanden voorraad die kan worden weergegeven voor die magazijnen of winkels uit de gegevens van de laatste momentopname van Commerce Headquarters.

Op de schermen van **Orderafhandeling** van POS wordt eveneens gebruikgemaakt van de berekening aan kanaalzijde om voorhanden voorraad weer te geven voor artikelen als een orderafhandelingsregel wordt geselecteerd en een gebruiker het **detailvenster** bekijkt voor voorhanden voorraad voor het geselecteerde artikel.

## <a name="optimize-your-inventory-data"></a>Uw voorraadgegevens optimaliseren

Voor een optimale schatting van de voorraad is het van het grootste belang dat u de volgende Commerce-batchtaken gebruikt en regelmatig uitvoert:

- **P-taak**: de P-taak bevindt zich op de pagina **Distributieschema's** en moet regelmatig worden uitgevoerd. Met deze taak worden e-Commerce-orders, asynchrone klantorders die zijn gemaakt door POS en contante orders die zijn gemaakt op basis van de kanaaldatabases in Commerce Headquarters opgenomen, zodat deze verder kunnen worden verwerkt. Voordat deze gegevens worden gesynchroniseerd vanuit het kanaal met Commerce Headquarters, beschikt Commerce Headquarters niet over informatie over voorraadcorrecties voor producten in de magazijnen die het resultaat zijn van deze transacties.
- **Orders synchroniseren**: met deze taak worden de onbewerkte transactiegegevens in Commerce Headquarters verwerkt die de P-taak levert en die e-Commerce- en asynchrone klantordertransacties omzet in verkooporders in Commerce Headquarters. Totdat deze taak wordt verwerkt en de verkooporders zijn gemaakt, worden er geen voorraadtransacties gemaakt. Daarom worden de transacties niet opgenomen in voorhanden voorraad in Commerce Headquarters.
- **Transactieoverzichten in batch berekenen**: voor contante transacties die in de winkel zijn gemaakt, zorgt het proces voor groepsgewijs boeken dat de voorraad met betrekking tot de verkoop efficiënt wordt bijgewerkt. Voor de meest efficiënte verwerking van voorraadtransacties voor contante orders moet u ervoor zorgen dat u uw systeem configureert voor het gebruik van [groepsgewijs boeken](https://docs.microsoft.com/dynamics365/commerce/trickle-feed).
- **Transactionele overzichten boeken in batch**: deze taak is ook vereist voor groepsgewijs boeken. Het volgt de taak **Transactieoverzichten berekenen in batch**. Met deze taak worden de berekende overzichten systematisch geboekt, zodat verkooporders voor contante verkopen in Commerce Headquarters en Commerce Headquarters nauwkeuriger worden weergegeven in de voorraad van uw winkel.
- **Beschikbaarheid product**: deze taak maakt de momentopname van voorraad vanuit Commerce Headquarters.
- **1130 (Beschikbaarheid product)**: deze taak bevindt zich op de pagina **Distributieschema's** en moet direct na de taak **Beschikbaarheid product** worden uitgevoerd. Met deze taak worden de momentopnamegegevens voor de voorraad vanuit Commerce Headquarters naar de kanaaldatabases overgebracht.

Het wordt aangeraden om deze batchtaken niet te vaak uitvoeren (om de paar minuten). Met frequente uitvoeringen wordt Commerce Headquarters (HQ) overbelast en kunnen de prestaties hierdoor worden beïnvloed. Over het algemeen kunt u het beste de productbeschikbaarheid en 1130-taken op elk uur uitvoeren en P-taken, orders synchroniseren en taken voor groepsgewijs boeken met dezelfde of een hogere frequentie plannen.

> [!NOTE]
> Om prestatieredenen wordt bij gebruik van berekeningen van de voorraadbeschikbaarheid aan kanaalzijde om een beschikbaarheidsaanvraag voor voorraad te maken via de API's van e-Commerce of de nieuwe POS-voorraadlogica aan kanaalzijde, een cache gebruikt bij de berekening om vast te stellen of er voldoende de tijd is verstreken om het opnieuw uitvoeren van de berekeningslogica te rechtvaardigen. De standaardcache is ingesteld op 60 seconden. U hebt bijvoorbeeld de berekening aan kanaalzijde voor uw winkel ingeschakeld en de voorhanden voorraad voor een product bekeken op de pagina **Zoeken in voorraad**. Als vervolgens één eenheid van het product wordt verkocht, wordt op de pagina **Zoeken in voorraad** de gereduceerde voorraad pas weergegeven nadat de cache is leeggemaakt. Nadat gebruikers transacties in POS hebben geboekt, moeten ze 60 seconden wachten voordat ze controleren of de voorhanden voorraad is verminderd.

Als voor uw bedrijfsscenario een kortere cachetijd is vereist, neemt u contact op met de vertegenwoordiger van productondersteuning voor hulp.
