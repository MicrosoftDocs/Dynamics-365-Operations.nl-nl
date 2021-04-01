---
title: Verwerking van catch weight-producten bij magazijnbeheer
description: In dit onderwerp wordt beschreven hoe werksjablonen en locatie-instructies kunnen worden gebruikt om te bepalen hoe en waar werk wordt gedaan in het magazijn.
author: perlynne
manager: tfehr
ms.date: 08/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCatchWeightTag, WHSCatchWeightItemHandlingPolicy, TMSLoadBuildWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-1-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 45f8d53b5ac212866a9c693e0039631507e14dd7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233074"
---
# <a name="catch-weight-product-processing-with-warehouse-management"></a>Verwerking van catch weight-producten bij magazijnbeheer

[!include [banner](../includes/banner.md)]


## <a name="feature-exposure"></a>Functierisico

Als u magazijnbeheer wilt gebruiken om catch weight-producten te verwerken, moet u een licentieconfiguratiesleutel gebruiken om de functionaliteit in te schakelen. Ga naar **Systeembeheer \> Instellingen \> Licentieconfiguratie**. Klik vervolgens op het tabblad **Configuratiesleutels**, vouw **Handel \> Magazijn en transportmanagement** uit en selecteer het selectievakje **Catch weight voor magazijn**.

> [!NOTE]
> De licentieconfiguratiesleutel **Magazijn en transportbeheer** en de licentieconfiguratiesleutel **Procesdistributie \> catch weight** moeten ook zijn ingeschakeld. Als u de configuratiesleutels voor catch weight wilt instellen, moet u de functie ook inschakelen via het werkgebied **Functiebeheer**. De hoofdfunctie die moet worden ingeschakeld, is **Verwerking van catch weight-producten bij magazijnbeheer**. Twee verwante maar optionele functies die u mogelijk wilt inschakelen, zijn **Wijzigingen in de voorraadstatus voor catch weight-producten** en **Bestaande codes voor catch weight gebruiken bij het gereedmelden van productieorders**.

Nadat de licentieconfiguratiesleutel is ingeschakeld en u een vrijgegeven product maakt, kunt u **Catch weight-** selecteren. U kunt ook het vrijgegeven product koppelen aan een opslagdimensiegroep waarvoor de **Magazijnanagementprocessen gebruiken**-parameter voor is geselecteerd.

Voordat u het product in magazijnbeheer kunt gebruiken, moet u enkele productspecifieke basisinstellingen voor catch weight maken:

- De nominale gewichtsconversie tussen de eenheid van catch weight (doos) en de voorraadeenheid (kilogram \[kg\]) definiëren als onderdeel van een definitie voor eenheidsconversie.
- De minimale en maximale gewichttoleranties definiëren als onderdeel van de instellingen van de catch weight-eenheid.
- Een eenheidsvolgordegroep instellen waarbij de catch weight-eenheid is gedefinieerd als de laagste voorraadeenheid (SKU).
- Een beleid voor verwerking van catch weight-artikelen instellen.

Zie voor meer informatie [instellen en beheren van catch weight-artikelen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-catch-weight-items).

## <a name="transaction-adjustments"></a>Transactiecorrecties

Omdat het gewicht van de voorraad wanneer die een magazijn binnenkomt kan afwijken van het gewicht van de voorraad wanneer die het magazijn verlaat, moet de catch weight-productverwerking de voorraad aanpassen.

> [!NOTE]
> Met activiteit van mobiel apparaat worden de transactiecorrecties alleen geactiveerd als de methode voor uitgaande gewichtafwijking van het beleid voor afhandeling van catch weight-artikelen van het artikel is ingesteld op **Afwijking van gewicht toestaan**.

**Voorbeeld 1**

In een **Gereedmelden**-productieproces is het binnenkomende gewicht van een nummerplaat met acht dozen van een catch weight-product vastgelegd als 80,1 kg. De nummerplaat wordt vervolgens opgeslagen in het gedeelte met eindproducten en gedurende de opslagperiode gaat wat gewicht aan de lucht verloren.

Het gewicht van dezelfde nummerplaat wordt later tijdens de orderverzameling in het verkoopproces vastgesteld als 79,8 kg. Daarom heeft u nu in het systeem een gewichtsverschil als onderdeel van de fysieke dimensieset.

In dit geval past het systeem automatisch het verschil aan door het boeken van een transactie voor de ontbrekende 0,3 kg.

**Voorbeeld 2**

In zijn definitie is een product ingesteld om een minimumgewicht van 8 kg en een maximumgewicht van 12 kg te tolereren voor de **Doos** catch weight-eenheid.

U hebt twee dozen van het product met een geregistreerd gewicht van 16 kg. Als een magazijnmedewerker een van de dozen ophaalt en weegt en het gewicht wordt vastgelegd als 9 kg, zal de resterende doos 7 kg wegen. Maar, omdat 7 kg lager is dan het minimumgewicht, voert het systeem een automatische correctie uit om het gewicht van de voorhanden voorraad met 1 kg te verhogen.

Om de rekeningen waarnaar deze correcties worden geboekt in te stellen, gaat u naar **Kostenbeheer \> Instellingen van grootboek-integratiebeleid \> Boeken**. Klik vervolgens op het tabblad **Voorraad** en definieer de volgende rekeningen:

- Verliesrekening variabel gewicht
- Winstrekening variabel gewicht

## <a name="catch-weight-item-handling-policy"></a>Beleid voor verwerking van catch weight-artikelen

Het afhandelingsbeleid voor het verwerken van catch weight-artikelen definieert twee primaire magazijnbeheerstromen voor de artikelen: wanneer het gewicht van de artikelen is vastgelegd en hoe dit is vastgelegd.

U kunt definiëren wanneer het gewicht wordt vastgelegd voor verkoop- en overdrachtorderverwerking. Het gewicht kan worden vastgelegd tijdens een van de volgende processen:

- **Verzamelen van** : het gewicht wordt vastgelegd tijdens het initiële verzamelingswerk van de orderverwerking.
- **pakbon** : het gewicht wordt vastgelegd tijdens het handmatig inpakken. (U moet de artikelen verzenden naar een inpakstation.)

Als het werkelijke gewicht wordt vastgelegd in het inpakstation tijdens de inpakprocessen van de container, wordt magazijnmedewerkers niet gevraagd om het gewicht vast te leggen tijdens het verzamelen. In plaats daarvan wordt het gemiddelde gewicht van de fysieke voorraad gebruikt als het gewicht van de verzamelde voorraad die naar het verpakkingsgebied gaat. Dit concept is ook van toepassing op catch weight-artikelen met labeltracering. Voor artikelen met labeltracering bepalen deze parameters wanneer het label wordt vastgelegd. Het label kan met behulp van het mobiele apparaat worden vastgelegd op het moment van het verzamelen of tijdens handmatige verpakking.

> [!NOTE]
> Omdat de optie **Inpakken** ervoor zorgt dat de voorraad wordt bijgewerkt met het gemiddelde pickgewicht, kan dit een verschil veroorzaken dat een correctie voor winst/verlies van het catch weight-artikel en/of een verschil tussen het gewicht van de voorhanden voorraad en het catch weight labelgewicht veroorzaakt.

Voor interne magazijnbeheerprocessen, zoals tellen en correcties, kunt u definiëren of het gewicht moet worden vastgelegd. Als het niet wordt vastgelegd, wordt het nominale gewicht gebruikt. Met andere opties kunt u gewicht per catch weight-eenheid en per getelde hoeveelheid vastleggen.

U kunt ook definiëren hoe het gewicht wordt vastgelegd. In een van de twee hoofdstromen worden Catch weight-labels bijgehouden en gebruikt voor het vastleggen van het gewicht. In de andere stroom worden catch weight-labels niet bijgehouden.

- **Ja** : het artikel gebruikt catch weight-labels. Elke labelnummer staat voor een catch weight-eenheid (doos) en een gewicht, en andere gegevens zijn gekoppeld aan het label. Het gewicht dat is gekoppeld aan het label wordt gebruikt voor uitgaande processen.
- **Niet** : het artikel gebruikt geen catch weight-labels. De binnenkomende en uitgaande weegprocessen zijn gebaseerd op het werkelijke gewicht dat wordt vastgelegd tijdens elk proces.

Het proces voor het bijhouden van catch weight-labels kan worden gebruikt voor artikelen waarvan het gewicht niet verandert tijdens de opslagperiode. Het gewicht wordt alleen tijdens het inkomende magazijnproces vastgelegd. Tijdens het uitgaande proces worden de catch weight-labels alleen gescand en de gewichten die gekoppeld zijn aan de labels worden voor het uitgaande transactieproces gebruikt.

Een andere belangrijke parameter met betrekking tot de verwerking van catch weight-labels is **Methode voor dimensietracering van catch weight-labels**. Labels kunnen gedeeltelijk of volledig worden getraceerd. Als een label gedeeltelijk wordt bijgehouden, worden productdimensies, traceringsdimensies en voorraadstatus bijgehouden. Als een label volledig wordt bijgehouden, worden productdimensies, traceringsdimensies en **alle** opslagdimensies bijgehouden.

En als een artikel labeltracering heeft, is er een parameter voor de **methode voor vastleggen van uitgaand gewicht**. U kunt deze parameter instellen zodat u altijd om het label wordt gevraagd voor uitgaande transacties via het mobiele apparaat. U kunt de parameter ook zo instellen dat u alleen naar labels wordt gevraagd wanneer deze nodig zijn. Stel, er zijn vijf catch weight-labels in voorraad voor een bepaald nummerplaat, en u hebt aangegeven dat u alle vijf de labels van het nummerplaat wilt verzamelen. In dit geval worden automatisch de vijf labels verzameld als de parameter **Methode voor vastleggen van uitgaand gewicht** is ingesteld op **Alleen om label vragen indien nodig**. U hoeft niet elk label te scannen. Als de parameter is ingesteld **Altijd om label vragen**, moet u elk label scannen, zelfs als alle vijf de labels worden verzameld.

> [!NOTE]
> In de regel worden labels alleen vastgelegd en bijgewerkt vanuit de menu-opdrachten van het mobiele apparaat. Er zijn echter enkele scenario's waarin labels ergens anders worden vastgelegd (bijvoorbeeld vanuit het handmatige verpakkingsstation). Als er labels worden gebruikt, moeten in het algemeen echter de menuopdrachten op de mobiele apparaten worden gebruikt voor alle magazijnactiviteiten.

### <a name="how-to-capture-catch-weight"></a>Hoe wordt catch weight vastgelegd?

**Als gebruik wordt gemaakt van het bijhouden van catch weight-labels**, moet altijd een label worden gemaakt voor elke catch weight-eenheid die wordt ontvangen, en elk label moet altijd worden gekoppeld aan een gewicht.

Bijvoorbeeld: **Doos** is de catch weight-eenheid en u ontvangt een pallet van acht dozen. In dit geval moeten acht unieke catch weight-labels worden gemaakt en aan elk label moet een gewicht worden gekoppeld. Afhankelijk van het inkomende catch weight-label, kan het totale gewicht van alle acht dozen worden vastgelegd en het gemiddelde gewicht kan vervolgens toebedeeld worden aan elke doos, of er kan een uniek gewicht voor elke doos worden vastgelegd.
Wanneer u de functie **Bestaande codes voor catch weight gebruiken bij het gereedmelden van productieorders** gebruikt terwijl het proces via een menuopdracht op een mobiel apparaat is ingeschakeld, wordt de voorraad bijgewerkt op basis van bestaande codegegevens voor catch weight. Hierdoor wordt in de magazijnbeheer-app niet gevraagd om de catch weight-codegegevens vast te leggen als onderdeel van een productielijst voor voltooide bewerkingen.

**Als geen gebruik wordt gemaakt van het bijhouden van catch weight-labels** dan kan het gewicht worden vastgelegd voor elke dimensieset (bijvoorbeeld voor elke nummerplaat en traceringsdimensie). Het gewicht kan ook worden vastgelegd op basis van een samengevoegd niveau, zoals vijf nummerplaten (pallets).

Voor de methoden voor vastleggen van uitgaand catch weight, kunt u met de optie **Per catch weight-eenheid** opgeven dat de weging moet worden uitgevoerd voor elke catch weight-eenheid (bijvoorbeeld per doos). Met de optie **Per verzameleenheid** kunt u opgeven dat het gewicht moet worden vastgelegd op basis van de hoeveelheid die wordt verzameld (bijvoorbeeld drie dozen). Houd er rekening mee dat voor het verzamelproces en het interne verplaatsingsproces in de productielijn het gemiddelde gewicht wordt gebruikt als de optie **Niet vastgelegd** wordt gebruikt.

Er zijn meer methoden voor gewichtvastlegging gedefinieerd in het beleid voor het afhandelen van catch weight-artikelen. De parameter van elke gewichtvastlegmethode wordt door diverse transacties gebruikt. De volgende tabel geeft een overzicht van welke parameters die door welke transacties worden gebruikt.

| methode                                     | Transactie                                |
|--------------------------------------------|--------------------------------------------|
| Methode voor vastleggen van uitgaand gewicht           | Orderverzamelen, doorgifteverzamelen            |
| Methode voor vastleggen van productieverzamelgewicht | Productieverzamelen, productieverbruik |
| Methode voor vastleggen van mutatiegewicht           | Mutatie                                   |
| Moment van vastlegging van gewichtscorrectie       | Correcties, Tellen                      |
| Methode voor vastleggen van tellingsgewicht           | Tellen                                   |
| Methode voor vastleggen gewicht van magazijntransfer | Magazijntransfer                         |

Om te voorkomen dat de verzamelprocessen van het magazijnbeheer tot gevolg hebben dat gewichten worden vastgelegd die resulteren in correcties voor winst/verlies van het catch weight-artikel, kunt u de methode voor uitgaande gewichtafwijking gebruiken. De methode voor uitgaande gewichtafwijking wordt toegepast tijdens de volgende processen op mobiele apparaten: orderverzamelen, doorgifteverzamelen, productieverzamelen, verplaatsingen, telling en magazijnoverdrachten. U kunt de optie **Afwijking van gewicht beperken** gebruiken als het gewicht van het catch weight-artikel niet schommelt tijdens de magazijnopslag en als er geen correcties voor winst en verlies voor het catch weight-artikel zijn vereist. U kunt de optie **Afwijking van gewicht toestaan** gebruiken als het gewicht schommelt, en als er correcties voor winst en verlies van het catch weight-artikel zijn vereist wanneer een schommeling van het gewicht wordt vastgelegd.

## <a name="unsupported-scenarios"></a>Niet-ondersteunde scenario's

Niet alle workflows ondersteunen verwerking van catch weight-producten bij magazijnbeheer. De volgende beperkingen gelden momenteel. Deze zijn van toepassing op alle catch weight-artikelen, ongeacht of ze zijn gelabeld.

### <a name="configuring-catch-weight-products-for-warehouse-management-processes"></a>Het configureren van catch weight-producten voor magazijnbeheerprocessen

- Alleen formuleverwerking wordt ondersteund voor catch weight-producten (niet-stuklijst).
- Catch weight-producten kunnen niet worden gekoppeld aan een traceringsdimensiegroep met behulp van de eigenaar-dimensie.
- Catch weight-producten kunnen niet worden gebruikt als services.
- Catch weight-producten kunnen alleen worden gebruikt als 'producten opgeslagen in voorraad' als onderdeel van de artikelmodelgroep.
- Catch weight-producten kunnen niet worden gebruikt samen met de functionaliteit voor het bijhouden van 'Actief in verkoopproces'.
- Catch weight-producten kunnen niet worden gebruikt samen met de functionaliteit voor het vastleggen van serienummers. Daarom kunnen producten niet worden overgeboekt van een 'leeg' naar een serienummer als onderdeel van het proces van verzamelen en verpakken.
- Catch weight-producten kunnen niet worden gebruikt samen met de functionaliteit voor het .registreren van serienummers voor verbruik.
- Catch weight-producten die variabel kunnen zijn, kunnen niet samen worden gebruikt met de functionaliteit voor het converteren van variabele maateenheden.
- Catch weight-producten kunnen niet worden gemarkeerd als een Commerce-productkit.
- Catch weight-producten kunnen alleen worden gebruikt met een volgordegroep voor de eenheid die catch weight-materiaalverwerkingseenheden heeft en die de catch-weight-eenheid als laagste volgnummer heeft.
- Voor catch weight-producten kan de voorraadeenheid alleen worden geconverteerd naar de catch weight-eenheid als de conversie een nominale hoeveelheid van meer dan 1 produceert.
- Het instellen van streepjescodes voor catch weight-producten ondersteunt niet een variabele gewichtsinstelling.

### <a name="order-processing"></a>Orderverwerking

- Het maken van een advance shipping notice (ASN/verpakkingsstructuren) ondersteunt geen gewichtinformatie.
- De orderhoeveelheid moet worden onderhouden gebaseerd op de catch weight-eenheid.

### <a name="inbound-warehouse-processing"></a>Inkomende magazijnverwerking

- Bij het ontvangen van nummerplaten moet gewicht worden toegewezen tijdens de registratie, omdat gewichtsinformatie niet wordt ondersteund als onderdeel van de advance shipping notice. Wanneer catch weight-labelprocessen worden gebruikt, moet het labelnummer handmatig worden toegewezen per catch weight-eenheid.
- Kwaliteitscontrole bij binnenkomst wordt niet ondersteund voor catch weight-producten. Indien geconfigureerd, wordt de kwaliteitscontrole overgeslagen.

### <a name="inventory-and-warehouse-operations"></a>Voorraad- en magazijnoperaties

- Het handmatig maken van quarantaineorders wordt niet ondersteund voor catch weight-producten.
- Handmatige voorraadverplaatsing met betrekking tot openstaand werk wordt niet ondersteund voor catch weight-producten.
- Het laden van nummerplaten voor het initialiseren van magazijnvoorraad wordt niet ondersteund voor catch weight-producten.
- Batchverdelingsprocessen worden niet ondersteund voor catch weight-producten.
- De verwerking van negatieve fysieke voorraad wordt niet ondersteund voor catch weight-producten.
- Voorraadmarkering kan niet worden gebruikt voor catch weight-producten.

### <a name="outbound-warehouse-processing"></a>Uitgaande magazijnverwerking

- De functie voor clusterverzamelen wordt niet ondersteund voor catch weight-producten.
- De magazijnverwerking verzamelen en inpakken wordt niet ondersteund voor catch weight-producten.
- Voor catch weight-producten kan werk dat is gedefinieerd in een werksjabloon niet automatisch worden uitgevoerd.
- Voor catch weight-producten biedt het systeem geen ondersteuning voor de verwerking op handmatige inpakstations waar werk voor het verzamelen uit verpakte containers wordt gecreëerd nadat containers zijn gesloten.
- De functie voor stuk voor stuk scannen wordt niet ondersteund voor catch weight-producten.

### <a name="production-processing"></a>Productieverwerking

- Voor catch weight-producten worden alleen batchorders voor formuleproducten ondersteund.
- Kanbanfunctionaliteit wordt niet ondersteund voor catch weight-producten.
- Voor catch weight-producten kunnen serienummers niet vóór verbruik worden geregistreerd.
- De functie voor het terugkeren van nummerplaten uit productie wordt niet ondersteund voor catch weight-producten.
- Voor catch weight-producten kan gereedmelding niet worden geregistreerd op serienummer.

### <a name="transportation-management-processing"></a>Transportbeheerprocessen

- Workbench voor ladingopbouwverwerking wordt niet ondersteund voor catch weight-producten.
- Transportaanvraagregels worden niet ondersteund voor catch weight-producten.

### <a name="other-restrictions-and-behaviors-for-catch-weight-product-processing-with-warehouse-management"></a>Andere beperkingen en gedragingen voor het verwerken van catch weight-producten bij magazijnbeheer

- Tijdens verzamelprocessen waarin de gebruiker niet wordt gevraagd om traceringsdimensies te identificeren, wordt de gewichtstoewijzing gedaan op basis van het gemiddelde gewicht. Dit treedt op wanneer bijvoorbeeld een combinatie van traceringsdimensies wordt gebruikt op dezelfde locatie en nadat een gebruiker het verzamelen verwerkt en er slechts één trackingsdimensiewaarde op de locatie is gebleven.
- Wanneer de voorraad wordt gereserveerd voor een catch weight-product dat is geconfigureerd voor magazijnbeheerprocessen, wordt de reservering gedaan op basis van het minimumgewicht dat is gedefinieerd, zelfs als deze hoeveelheid de laatste voorhanden verwerkingshoeveelheid is. Dit gedrag wijkt af van het gedrag voor artikelen die niet zijn geconfigureerd voor magazijnbeheerprocessen. Er is één uitzondering op deze beperking. Voor productieverzamelen wordt het werkelijke gewicht gebruikt als de laatste afhandelingshoeveelheid van een catch weight-product met serienummercontrole wordt verzameld.
- Processen die gebruikmaken van het gewicht als onderdeel van de capaciteitsberekeningen (wavedrempels, maximale werkpauzes, containermaxima, belastingscapaciteiten locatie, enzovoort) gebruiken het werkelijke gewicht van de voorraad niet. In plaats daarvan zijn de processen gebaseerd op het fysieke verwerkingsgewicht dat is gedefinieerd voor het product.
- In het algemeen wordt Commerce-functionaliteit niet ondersteund voor catch weight-producten.
- Voor catch weight-producten kan de voorraadstatus niet worden bijgewerkt vanuit **Statuswijziging van magazijn**.

### <a name="catch-weight-tags"></a>Catch weight-labels

Een catch weight-label kan worden gemaakt via een magazijnapp-proces, het kan handmatig in het formulier worden gemaakt of het kan worden gemaakt met een gegevensentiteitproces. Als een catch weight-label is gekoppeld aan een documentregel van een inkomende bron, zoals een inkooporderregel, wordt het label geregistreerd. Als de regel wordt gebruikt voor uitgaande verwerking, wordt het label bijgewerkt als verzonden.

Naast de beperkingen die momenteel van toepassing zijn op catch weight-producten hebben gelabelde catch weight-producten nog andere beperkingen die momenteel van toepassing zijn.

- Alle handmatige updates van voorraad (dat wil zeggen: updates die niet worden uitgevoerd via een mobiel apparaat) moeten de bijbehorende handmatige updates van de bijbehorende catch weight-labels bevatten. Deze worden niet automatisch uitgevoerd. Bijvoorbeeld, met handmatige correctiejournalen wordt de voorraad bijgewerkt, maar niet de bijbehorende catch weight-labels..
- U moet catch weight-labels handmatig bijwerken om verplaatsingen van aanvullingswerk weer te geven. Dit komt doordat het systeem geen gewichten kan vastleggen tijdens aanvullingswerkzaamheden en daarom in plaats daarvan het gemiddelde gewicht registreert.
- De ontvangst van gecombineerde nummerplaten wordt momenteel niet ondersteund voor gelabelde catch weight-producten.
- Met de verwerking van de ontvangst van verkoopretourorders kunt u catch weight-labels vastleggen. Het proces valideert echter niet of het geretourneerde label hetzelfde label is als het label dat oorspronkelijk voor een verkooporder is verzonden.
- Het menu-item van het mobiele apparaat dat de activiteitscode **Materiaalverbruik registreren** heeft, biedt momenteel geen ondersteuning voor het vastleggen van catch weight-labels.
- Hoewel telprocessen voor gelabelde catch weight-producten worden ondersteund, zijn deze beperkt. U kunt bijvoorbeeld de opties van het mobiele apparaat gebruiken voor het tellen van gelabelde catch weight-artikelen, in welk geval het gemiddelde gewicht wordt gebruikt. Catch weight-labels worden echter niet automatisch bijgewerkt met de teltransactie. Wanneer de teltransactie is voltooid, moeten de catch weight-labels handmatig worden bijgewerkt opdat ze de juiste voorraad aangeven. Als artikelen die oorspronkelijk niet op een locatie stonden, op die locatie worden geteld, wordt het nominale gewicht gebruikt.
- Nummerplaatconsolidatie biedt momenteel geen ondersteuning voor gelabelde catch weight-artikelen.
- De functionaliteit voor storneringswerk wordt niet ondersteund voor catch weight-artikelen met labelnummertracering.

> [!NOTE]
> Voorgaande informatie over catch weight-labels is alleen geldig als het catch weight-product een methode heeft voor dimensietracering van catch weight-labels voor volledige tracering (dat wil zeggen, als de parameter **Methode voor dimensietracering van catch weight-labels** in het beleid voor afhandeling van catch weight-producten is ingesteld op **Productdimensies, traceringsdimensies en alle opslagdimensies**). Als een artikel alleen gedeeltelijke labeltracering heeft (dus als de parameter **Methode voor dimensietracering van catch weight-labels** in het beleid voor afhandeling van catch weight-artikelen is ingesteld op **Productdimensies, traceringsdimenses en voorraadstatus**), zijn er extra beperkingen van toepassing. Omdat zichtbaarheid tussen het label en de voorraad in dit geval verloren gaat, worden sommige aanvullende scenario's niet ondersteund.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]