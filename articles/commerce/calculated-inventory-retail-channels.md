---
title: Voorraadbeschikbaarheid voor retail-kanalen berekenen
description: In dit onderwerp wordt beschreven hoe een bedrijf Microsoft Dynamics 365 Commerce kan gebruiken om de geschatte beschikbaarheid van voorhanden voorraad te bekijken voor producten in de online- en winkelkanalen.
author: hhainesms
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-11
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 1b1e0ea264dd74f6583d3b7fd3ecce551c73fbae
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/23/2021
ms.locfileid: "7674670"
---
# <a name="calculate-inventory-availability-for-retail-channels"></a>Voorraadbeschikbaarheid voor Retail-kanalen berekenen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe een bedrijf Microsoft Dynamics 365 Commerce kan gebruiken om de geschatte beschikbaarheid van voorhanden voorraad te bekijken voor producten in de online- en winkelkanalen.

## <a name="accuracy-of-inventory-availability"></a>Nauwkeurigheid van voorraadbeschikbaarheid

Commerce gebruikt meerdere servers en databases om schaalbaarheid en prestaties te garanderen. Het is daarom belangrijk dat u begrijpt dat de waarden voor de beschikbare voorraad die worden geleverd via de POS-toepassing, de Application Programming Interfaces (API's) voor voorraadbeschikbaarheid van e-commerce en de pagina's voor voorhanden voorraad in Commerce Headquarters mogelijk niet 100 procent nauwkeurig zijn in realtime. Als transacties die zijn gemaakt voor producten in het online- of winkelkanaal nog niet zijn gesynchroniseerd met Headquarters, wordt op de pagina's met voorhanden voorraad in Headquarters mogelijk niet altijd een accurate waarde voor de realtime voorraad weergegeven voor deze producten. Omgekeerd geldt dat, als u uw bedrijf zo hebt geconfigureerd dat gebruikers in Headquarters of andere geïntegreerde toepassingen de voorraad kunnen verkopen, ontvangen, retourneren of anderszins aanpassen vanuit een winkel of online magazijn, het POS- of online kanaal mogelijk niet over alle informatie beschikt die is vereist om accurate realtime waarden voor voorhanden voorraad van artikelen weer te geven.

Het is van cruciaal belang dat u begrijpt dat alle beschikbaarheidsgegevens over voorhanden voorraad die tijdens de werkdag worden verstrekt, als een geschatte waarde worden beschouwd. Dus als u probeert de gegevens over de voorhanden voorraad te vergelijken met de werkelijke fysieke voorraad op de planken of als u probeert de waarden voor de voorhanden voorraad die in POS worden weergegeven te vergelijken met de gegevens die u hebt gevonden voor hetzelfde magazijn in Headquarters, kunnen de waarden verschillen. Dit verschil tijdens de werkdag wordt verwacht en mag niet als een probleem worden beschouwd. Als u gegevens wilt controleren en ervoor wilt zorgen dat de waarden die zijn opgegeven in POS, API's en Headquarters overeenkomen met de werkelijke fysieke eenheden die u vindt op uw winkel- of magazijnplanken, kunt u dit het beste doen nadat kanaalbewerkingen zijn gestopt voor de dag en alle transacties correct zijn gesynchroniseerd tussen Headquarters en het kanaal.

## <a name="channel-side-inventory-calculation"></a>Berekening van voorraad aan kanaalzijde

De berekening van de voorraad aan de kanaalzijde is een mechanisme waarbij de laatst bekende kanaalvoorraadgegevens in Commerce Headquarters als basis worden genomen. Vervolgens worden extra voorraadwijzigingen verwerkt die zich aan de kanaalzijde voordeden en die niet in die basisgegevens zijn opgenomen, om een geschatte voorhanden voorraad te berekenen die dicht bij de real-time waarde ligt. 

De volgende voorraadwijzigingen worden momenteel meegenomen in de logica voor de berekening van de voorraadbeschikbaarheid aan kanaalzijde:

- Voorraad verkocht via contante transacties in de winkel
- Voorraad verkocht via klantorders in de winkel of het online kanaal
- Voorraad die naar de winkel is geretourneerd
- Afgehandelde voorraad (verzamelen, verpakken, verzenden) vanuit het winkelmagazijn

Als u de voorraadberekening aan kanaalzijde wilt gebruiken, moet u de functie **Geoptimaliseerde berekening voor productbeschikbaarheid** inschakelen.

Als uw Commerce-omgeving release **10.0.8 tot 10.0.11** draait, volgt u deze stappen.

1. Ga in Commerce Headquarters naar **Retail en commerce** \> **Gedeelde Commerce-parameters**.
1. Selecteer op het tabblad **Voorraad** in het veld **Taak Beschikbaarheid product** de optie **Taak Geoptimaliseerd proces voor productbeschikbaarheid gebruiken**.

Als uw Commerce-omgeving release **10.0.12 of later** draait, volgt u deze stappen.

1. Ga in Commerce Headquafters naar **Werkruimten \> Functiebeheer** en schakel de functie **Geoptimaliseerde berekening voor productbeschikbaarheid** in.
1. Als voor uw online en winkelkanalen dezelfde afhandelingsmagazijnen worden gebruikt, moet u ook de functie **Verbeterde logica voor voorraadberekening aan kanaalzijde voor e-commerce** inschakelen. Op die manier wordt bij de berekeningslogica van het kanaal rekening houden met de niet-geboekte transacties die in het winkelkanaal zijn aangemaakt. (Deze transacties kunnen cash-and-carry-transacties, klantorders en retouren zijn.)
1. Voer de taak **1070** (**Kanaalconfiguratie**) uit.

Als uw Commerce-omgeving is bijgewerkt vanuit een versie die eerder is dan Commerce versie 10.0.8, moet u nadat u de functie **Geoptimaliseerde berekening voor productbeschikbaarheid** hebt ingeschakeld, ook de functie **Commerce Scheduler initialiseren** uitvoeren om de functie van kracht te laten worden. Om de initialisatie uit te voeren, gaat u naar **Retail en commerce** \> **Instellingen van hoofdkantoor** \> **Commerce-planner**.

Als u de berekening voor de kanaalvoorraad wilt gebruiken, moet periodiek een momentopname van de voorraadgegevens in het hoofdkantoor worden gemaakt door de taak **Beschikbaarheid product** en naar de kanaaldatabases worden verzonden. De momentopname staat voor de informatie die in Headquarters beschikbaar is over de voorraadbeschikbaarheid voor een specifieke combinatie van een product of productvariant en een magazijn. Deze bevat alleen de voorraadtransacties die in Headquarters waren verwerkt en geboekt op het moment dat de momentopname werd genomen. Het kan zijn dat de momentopname niet 100 procent nauwkeurig in real time is, vanwege de constante verwerking van verkopen die plaatsvindt op gedistribueerde servers.

- Als er voorraad voor een product in een winkel is verkocht via een contante transactie of een asynchrone verkooporder voor een klant in de POS-toepassing, beschikt Headquarters niet onmiddellijk over informatie over de bijbehorende transactie voor voorraaduitgifte voor de verkoop. Headquarters bevat alleen informatie over de voorraad die voor deze typen winkelverkoop wordt verkocht nadat de P-taak de gerelateerde transactie heeft geüpload vanuit de kanaaldatabase van de winkel naar Headquarters en de bijbehorende verkooporders zijn gemaakt via een overzichtboeking of de processen voor groepsgewijs boeken. Tijdens het maken van de orders in Headquarters worden de bijbehorende voorraadtransacties gemaakt. 
- Voor e-commerce-afzetkanaalorders beschikt Headquarters alleen over informatie over de voorraadtransacties nadat de transacties naar Headquarters zijn verzonden via de P-taak en het ordersynchronisatieproces is voltooid.

Voer de volgende stappen uit om een momentopname te maken van de voorraad in Commerce Headquarters.

1. Ga naar **Detailhandel en commerce \> IT detailhandel en commerce \> Producten en voorraad \> Beschikbaarheid product**.
1. Selecteer **OK** om de taak **Beschikbaarhied product** uit te voeren. U kunt deze taak ook plannen om te worden uitgevoerd in een batch.

Nadat de taak **Beschikbaarheid product** is voltooid, moeten de opgenomen gegevens naar de e-commerce-afzetkanaaldatabases worden gepusht, zodat de meest recente momentopname van de voorraad voor Headquarters kan worden meegenomen bij de berekening aan kanaalzijde van de geschatte voorhanden voorraad.

Volg deze stappen om momentopnamegegevens te synchroniseren van Headquarters naar uw kanaaldatabases.

1. Ga naar **Retail en Commerce \> Retail en Commerce IT \> Distributieplanning**.
1. Voer de taak **1130** (**Beschikbaarheid product**) uit om de momentopnamegegevens te synchroniseren die met de taak **Beschikbaarheid product** zijn gemaakt vanuit Headquarters naar uw kanaaldatabases.

## <a name="inventory-availability-apis-for-e-commerce"></a>API's voor voorraadbeschikbaarheid voor e-commerce

Commerce biedt de volgende API's voor e-commerce-scenario's om de voorraadbeschikbaarheid van een product op te vragen:

- **GetEstimatedAvailability**: gebruik deze API om een query uit te voeren op voorraad voor een product of productvariant in het online kanaalmagazijn of magazijnen die zijn gekoppeld aan de vervullingsgroep van het online kanaal.
- **GetEstimatedProductWarehouseAvailability**: gebruik deze API om voorraad voor een product of productvariant uit een bepaald magazijn op te vragen.

> [!NOTE]
> Deze API's vervangen de API's **GetProductAvailabilities** en **GetAvailableInventoryNearby** in Commerce, versie 10.0.7 en eerder.

Beide API's maken intern gebruik van de logica voor berekening aan de kanaalzijde en het retourneren de geraamde **fysiek beschikbare** hoeveelheid, de **totaal beschikbare** hoeveelheid, de **maateenheid** en het **voorraadniveau** voor het gevraagde product en magazijn. De geretourneerde waarden kunnen op uw e-commerce-site worden weergegeven als u dat wilt, of ze kunnen worden gebruikt om andere bedrijfslogica op uw e-commerce-site te activeren. U kunt bijvoorbeeld voorkomen dat producten worden gekocht met een voorraadniveau 'niet op voorraad'.

Hoewel andere API's die beschikbaar zijn in Commerce direct naar Headquarters kunnen gaan om voorhanden hoeveelheden van producten op te halen, raden wij u niet aan deze te gebruiken in een e-commerce-omgeving vanwege mogelijke prestatieproblemen en het effect dat veelvuldige aanvragen kunnen hebben op uw Headquarters-servers. Bovendien kunnen de twee hierboven genoemde API's met de berekening aan de kanaalzijde een nauwkeuriger schatting geven van de beschikbaarheid van een product door rekening te houden met de transacties die zijn aangemaakt in de kanalen die nog niet bekend zijn bij het hoofdkantoor.

Volg deze stappen om te definiëren hoe producthoeveelheid moet worden geretourneerd in de API-uitvoer.

1. Ga naar **Detailhandel en commerce \> Instelling van hoofdkantoor \> Parameters \> Commerce-parameters**.
1. Klik op het tabblad **Voorraad** en configureer vervolgens op het sneltabblad **API's voor voorraadbeschikbaarheid voor e-commerce** de waarde van de instelling **Hoeveelheid in API-uitvoer**.
1. Voer taak **1070** (**Kanaalconfiguratie**) uit om de nieuwste waarde te synchroniseren met de kanalen.

De instelling **Hoeveelheid in API-uitvoer** biedt drie opties:

- **Voorraadhoeveelheid retourneren** - fysiek beschikbare en totaal beschikbare hoeveelheid van een gevraagd product worden geretourneerd in de API-uitvoer.
- **Voorraadhoeveelheid retourneren minus voorraadbuffer**- de hoeveelheid die wordt geretourneerd in de API-uitvoer wordt gecorrigeerd er door de voorraadbufferwaarde van af te trekken. Meer informatie over de voorraadbuffer vindt u in [Voorraadbuffers en voorraadniveaus configureren](inventory-buffers-levels.md).
- **Voorraadhoeveelheid niet retourneren** - alleen het voorraadniveau wordt geretourneerd in de API-uitvoer. Meer informatie over de voorraadniveaus vindt u in [Voorraadbuffers en voorraadniveaus configureren](inventory-buffers-levels.md).

U kunt de API-parameter `QuantityUnitTypeValue` gebruiken om het eenheidstype op te geven waarmee u de hoeveelheid in de API's wilt laten retourneren. Deze parameter ondersteunt de opties **voorraadeenheid** (standaardwaarde), **inkoopeenheid** en **verkoopeenheid**. De geretourneerde hoeveelheid wordt afgerond op de gedefinieerde precisie van de betreffende maateenheid in Headquarters.

De API **GetEstimatedAvailability** biedt de volgende invoerparameters ter ondersteuning van verschillende queryscenario's:

- `DefaultWarehouseOnly` - gebruik deze parameter om voorraad op te vragen voor een product in het standaardmagazijn van het online kanaal. 
- `FilterByChannelFulfillmentGroup` en `SearchArea` - gebruik deze twee parameters om voorraad op te vragen voor een product vanuit alle verzamellocaties in een specifiek zoekgebied op basis van `longitude`, `latitude` en `radius`. 
- `FilterByChannelFulfillmentGroup` en `DeliveryModeTypeFilterValue` - gebruik deze twee parameters om voorraad op te vragen voor een product in specifieke magazijnen die zijn gekoppeld aan de vervullingsgroep van een online kanaal en die zijn geconfigureerd om bepaalde leveringsmethoden te ondersteunen. De parameter `DeliveryModeTypeFilterValue` ondersteunt de opties **alle** (standaardwaarde), **verzenden** en **afhalen**. In een scenario waarbij een online order kan worden vervuld vanuit meerdere verzendmagazijnen, kunt u met deze twee parameters de voorraadbeschikbaarheid van een product in al deze magazijnen opvragen. De API retourneert in dit geval de hoeveelheid voorhanden voorraad en het voorraadniveau van het product in elk verzendmagazijn, plus een totale hoeveelheid en een totaal voorraadniveau van alle verzendmagazijnen in de query.
 
De modules koopvak, winkelselector, verlanglijst, winkelwagen en winkelwagenpictogram in Commerce verbruiken de hierboven genoemde API's en parameters om berichten over voorraadniveau weer te geven op de e-commerce-site. De Commerce Site Builder levert verschillende voorraadinstellingen om handels- en inkoopgedrag te regelen. Zie [Voorraadinstellingen toepassen](inventory-settings.md) voor meer informatie.

## <a name="pos-inventory-lookup-with-channel-side-calculation"></a>Voorraad opvragen in POS met berekening aan kanaalzijde

In Commerce, versies 10.0.9 en eerder, gebruikte de bewerking **Zoeken in voorraad** in POS een realtime serviceaanroep naar Headquarters om voorraadinformatie op te halen voor het geselecteerde product, voor zowel de huidige winkel van de gebruikers als ook andere winkels die zijn geconfigureerd voor de afhandelingsgroep als onderdeel van de kanaalconfiguratie voor de winkel. In Commerce, release 10.0.10 en later, kunt u de real-time serviceaanroepen naar Headquarters uitschakelen en in plaats daarvan gebruik maken van berekening aan de kanaalzijde op de Commerce-server om te bepalen welke voorhanden voorraad fysiek beschikbaar is voor de winkel en andere locaties die in de vervullingsgroep zijn gedefinieerd. Deze in het kanaal berekende voorraadconfiguratie is ook handig voor locaties waar de internetverbinding onbetrouwbaar is, omdat u niet online hoeft te zijn om zoekacties voor voorraad vanuit Headquarters te kunnen ophalen.

Wanneer de berekening aan kanaalzijde op de juiste manier wordt geconfigureerd en beheerd, kan het een betrouwbaardere schatting van de huidige winkelvoorraad leveren, omdat deze de transactionele gegevens gebruikt die zich in de Commerce-kanaaldatabase bevinden, maar waarover Headquarters mogelijk nog geen informatie heeft. Als u bijvoorbeeld de bestaande realtime serviceaanroep voor het zoeken van voorraad in POS gebruikt, beschikt Headquarters waarschijnlijk nog niet over informatie over een contante verkoop die zojuist heeft plaatsgevonden voor een product. De waarde voor de voorhanden voorraad die door Headquarters wordt geretourneerd voor dat product zal waarschijnlijk één eenheid hoger zijn dan de werkelijke voorhanden voorraad van de winkel. Als u echter gebruikmaakt van de berekening aan kanaalzijde, kan de contante verkoop worden opgenomen in de berekening en worden afgetrokken van de waarde voor de voorhanden voorraad die wordt weergegeven. Hoewel de waarden die zowel door de berekening aan kanaalzijde als door de realtime serviceaanroepen worden geleverd, slechts ramingen zijn van de voorhanden voorraad, is het veel waarschijnlijker dat de waarde die de kanaalzijde biedt nauwkeurig is voor de huidige winkel.

Als u de POS-bewerking **Zoeken in voorraad** in Commerce Headquarters wilt configureren om de berekeningslogica aan de kanaalzijde te gebruiken en aanroepen van real-time service uit te schakelen, moet u eerst de functie **Geoptimaliseerde berekening voor productbeschikbaarheid** inschakelen via de werkruimte **Functiebeheer** in Commerce Headquarters en vervolgens deze stappen uitvoeren.

1. Ga naar **Retail en Commerce \> Kanaalinstellingen \> POS-instellingen \> POS-profielen \> Functionaliteitsprofielen**.
1. Selecteer een functionaliteitsprofiel.
1. Wijzig op het sneltabblad **Functies** in de sectie **Berekening van voorraadbeschikbaarheid** de waarde van het veld **Modus voor berekening van voorraadbeschikbaarheid** van **Realtime service** in **Kanaal**. Alle functionaliteitsprofielen gebruiken standaard realtime serviceaanroepen. U moet de waarde van dit veld wijzigen als u de logica voor berekening aan kanaalzijde wilt gebruiken. Elke detailhandelwinkel die is gekoppeld aan het geselecteerde functionaliteitsprofiel wordt beïnvloed door deze wijziging.

U moet vervolgens de wijzigingen via het distributieschemaproces naar het kanaal synchroniseren in Headquarters door de volgende stappen uit te voeren.

1. Ga naar **Retail en Commerce \> Retail en Commerce IT \> Distributieplanning**.
1. Voer de taak **1070** (**Kanaalconfiguratie**) uit.

Nadat de configuratie is voltooid, maakt de informatie over de fysiek beschikbare voorraad niet langer gebruik van een realtime serviceaanroep wanneer een gebruiker in de POS-toepassing de bewerking **Zoeken in voorraad** (standaard- en matrixweergaven) gebruikt. In plaats daarvan worden gegevens over fysiek beschikbare voorraad voor de huidige winkel en alle winkels in de afhandelingsgroep berekend op basis van de laatst bekende momentopname die vanuit Commerce Headquarters aan de kanaaldatabase is geleverd. De waarde van de momentopname wordt verder verfijnd door de berekening aan kanaalzijde om de fysiek beschikbare waarde aan te passen, op basis van aanvullende verkoop- of retourtransacties voor het geselecteerde product in de kanaaldatabase die niet zijn opgenomen in de laatste gesynchroniseerde momentopname van de taak 1130. Als de kanaaldatabase geen transactiegegevens bevat voor een of meer magazijnen of winkels in de afhandelingsgroep, bevat de database geen extra transacties die kunnen worden opgenomen in een herberekening van de waarde. Daarom bestaat de beste schatting van voorhanden voorraad die kan worden weergegeven voor die magazijnen of winkels uit de gegevens van de laatste momentopname van Commerce Headquarters.

Op de schermen van **Orderafhandeling** van POS wordt eveneens gebruikgemaakt van de berekening aan kanaalzijde om voorhanden voorraad weer te geven voor artikelen als een orderafhandelingsregel wordt geselecteerd en een gebruiker het **detailvenster** bekijkt voor voorhanden voorraad voor het geselecteerde artikel.

## <a name="optimize-your-inventory-data"></a>Uw voorraadgegevens optimaliseren

Voor een optimale schatting van de voorraad is het van het grootste belang dat u de volgende Commerce-batchtaken gebruikt en regelmatig uitvoert:

- **P-taak**: de P-taak bevindt zich op de pagina **Distributieschema's** en moet regelmatig worden uitgevoerd. Met deze taak worden e-Commerce-orders, asynchrone klantorders die zijn gemaakt door POS en contante orders die zijn gemaakt op basis van de kanaaldatabases in Commerce Headquarters opgenomen, zodat deze verder kunnen worden verwerkt. Voordat deze gegevens worden gesynchroniseerd vanuit het kanaal met Commerce Headquarters, beschikt Commerce Headquarters niet over informatie over voorraadcorrecties voor producten in de magazijnen die het resultaat zijn van deze transacties.
- **Orders synchroniseren**: met deze taak worden de onbewerkte transactiegegevens in Commerce Headquarters verwerkt die de P-taak levert en die e-Commerce- en asynchrone klantordertransacties omzet in verkooporders in Commerce Headquarters. Totdat deze taak wordt verwerkt en de verkooporders zijn gemaakt, worden er geen voorraadtransacties gemaakt. Daarom worden de transacties niet opgenomen in voorhanden voorraad in Commerce Headquarters.
- **Transactieoverzichten in batch berekenen**: voor contante transacties die in de winkel zijn gemaakt, zorgt het proces voor groepsgewijs boeken dat de voorraad met betrekking tot de verkoop efficiënt wordt bijgewerkt. Voor de meest efficiënte verwerking van voorraadtransacties voor contante orders moet u ervoor zorgen dat u uw systeem configureert voor het gebruik van [groepsgewijs boeken](./trickle-feed.md).
- **Transactionele overzichten boeken in batch**: deze taak is ook vereist voor groepsgewijs boeken. Het volgt de taak **Transactieoverzichten berekenen in batch**. Met deze taak worden de berekende overzichten systematisch geboekt, zodat verkooporders voor contante verkopen in Commerce Headquarters en Commerce Headquarters nauwkeuriger worden weergegeven in de voorraad van uw winkel.
- **Beschikbaarheid product**: deze taak maakt de momentopname van voorraad vanuit Commerce Headquarters.
- **1130 (Beschikbaarheid product)**: deze taak bevindt zich op de pagina **Distributieschema's** en moet direct na de taak **Beschikbaarheid product** worden uitgevoerd. Met deze taak worden de momentopnamegegevens voor de voorraad vanuit Commerce Headquarters naar de kanaaldatabases overgebracht.

> [!NOTE]
> - De best practice is om de taken **Beschikbaarheid product** en **1130** elk uur uit te voeren en P-taken, orders synchroniseren en taken voor groepsgewijs boeken te plannen met dezelfde of een hogere frequentie.
> - Als berekeningen van de voorraadbeschikbaarheid aan kanaalzijde worden gebruikt om een aanvraag voor voorraadbeschikbaarheid te maken via de API's van e-commerce of de POS-voorraadlogica aan kanaalzijde, wordt omwille van de prestaties een cache gebruikt bij de berekening om vast te stellen of er voldoende de tijd is verstreken om het opnieuw uitvoeren van de berekeningslogica te rechtvaardigen. De standaardcache is ingesteld op 60 seconden. U hebt bijvoorbeeld de berekening aan kanaalzijde voor uw winkel ingeschakeld en de voorhanden voorraad voor een product bekeken op de pagina **Zoeken in voorraad**. Als vervolgens één eenheid van het product wordt verkocht, wordt op de pagina **Zoeken in voorraad** de gereduceerde voorraad pas weergegeven nadat de cache is leeggemaakt. Nadat gebruikers transacties in POS hebben geboekt, moeten ze 60 seconden wachten voordat ze controleren of de voorhanden voorraad is verminderd.

Als voor uw bedrijfsscenario een kortere cachetijd is vereist, neemt u contact op met de vertegenwoordiger van productondersteuning voor ondersteuning.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
