---
title: Verwerking van catch weight-producten bij magazijnbeheer
description: In dit onderwerp wordt beschreven hoe werksjablonen en locatie-instructies kunnen worden gebruikt om te bepalen hoe en waar werk wordt gedaan in het magazijn.
author: perlynne
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCatchWeightTag, WHSCatchWeightItemHandlingPolicy
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-1-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: ced22a144e57b624ceacb8bb5c3032218db3a0eb
ms.sourcegitcommit: bacec397ee48ac583596be156c87ead474ee07df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/05/2019
ms.locfileid: "777267"
---
# <a name="catch-weight-product-processing-with-warehouse-management"></a>Verwerking van catch weight-producten bij magazijnbeheer

[!include [banner](../includes/banner.md)]

## <a name="feature-exposure"></a>Functieblootstelling

Als u magazijnbeheer wilt gebruiken om catch weight-producten te verwerken, moet u een licentieconfiguratiesleutel gebruiken om de functionaliteit in te schakelen. (Ga naar **Systeembeheer \> Instellingen \> Licentieconfiguratie**. Klik vervolgens op het tabblad **Configuratiesleutels**, vouw **Handel \> Magazijn en transportmanagement** uit en selecteer het selectievakje **Catch weight voor magazijn**.)

> [!NOTE]
> De licentieconfiguratiesleutel **Magazijn en transportbeheer** en de licentieconfiguratiesleutel **Procesdistributie \> catch weight** moeten ook zijn ingeschakeld.

Nadat de licentieconfiguratiesleutel is ingeschakeld en u een vrijgegeven product maakt, kunt u **Catch weight-** selecteren. U kunt ook het vrijgegeven product koppelen aan een opslagdimensiegroep waarvoor de **Magazijnanagementprocessen gebruiken**-parameter voor is geselecteerd.

Voordat u het product in magazijnbeheer kunt gebruiken, moet u enkele productspecifieke basisinstellingen voor catch weight maken:

- De nominale gewichtsconversie tussen de eenheid van catch weight (doos) en de voorraadeenheid (kilogram \[kg\]) definiëren als onderdeel van een definitie voor eenheidsconversie.
- De minimale en maximale gewichttoleranties definiëren als onderdeel van de instellingen van de catch weight-eenheid.
- Een eenheidsvolgordegroep instellen waarbij de catch weight-eenheid is gedefinieerd als de laagste voorraadeenheid (SKU).
- Een beleid voor verwerking van catch weight-artikelen instellen.

Zie voor meer informatie [instellen en beheren van catch weight-artikelen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-catch-weight-items).

## <a name="transaction-adjustments"></a>Transactiecorrecties

Omdat het gewicht van de voorraad wanneer die een magazijn binnenkomt kan afwijken van het gewicht van de voorraad wanneer die het magazijn verlaat, moet de catch weight-productverwerking de voorraad aanpassen.

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

Als het werkelijke gewicht wordt vastgelegd in het inpakstation tijdens de inpakprocessen van de container, zal aan magazijnmedewerkers niet worden gevraagd om het gewicht vast te leggen tijdens het verzamelen. In plaats daarvan wordt het gemiddelde gewicht van de fysieke voorraad gebruikt als het gewicht van de verzamelde voorraad die naar het verpakkingsgebied gaat.

Voor interne magazijnbeheerprocessen zoals tellen en correctie is het mogelijk om te definiëren of het gewicht moet worden vastgelegd of niet. Bij niet vastleggen wordt het nominale gewicht gebruikt.

U kunt ook definiëren hoe het gewicht wordt vastgelegd. In een van de twee hoofdstromen worden Catch weight-labels bijgehouden en gebruikt voor het vastleggen van het gewicht. In de andere stroom worden catch weight-labels niet bijgehouden.

- **Ja** : het artikel gebruikt catch weight-labels. Elke labelnummer staat voor een catch weight-eenheid (doos) en een gewicht, en andere gegevens zijn gekoppeld aan het label. Het gewicht dat is gekoppeld aan het label wordt gebruikt voor uitgaande processen.
- **Niet** : het artikel gebruikt geen catch weight-labels. De binnenkomende en uitgaande weegprocessen zijn gebaseerd op het werkelijke gewicht dat wordt vastgelegd tijdens elk proces.

Het proces voor het bijhouden van catch weight-labels kan worden gebruikt voor artikelen waarvan het gewicht niet verandert tijdens de opslagperiode. Het gewicht wordt alleen tijdens het inkomende magazijnproces vastgelegd. Tijdens het uitgaande proces worden de catch weight-labels alleen gescand en de gewichten die gekoppeld zijn aan de labels worden voor het uitgaande transactieproces gebruikt.

### <a name="how-to-capture-catch-weight"></a>Hoe wordt catch weight vastgelegd?

Als gebruik wordt gemaakt van het bijhouden van catch weight-labels, moet altijd een label worden gemaakt voor elke catch weight-eenheid die wordt ontvangen, en elk label moet altijd worden gekoppeld aan een gewicht.

Bijvoorbeeld: **Doos** is de catch weight-eenheid en u ontvangt een pallet van acht dozen. In dit geval moeten acht unieke catch weight-labels worden gemaakt en aan elk label moet een gewicht worden gekoppeld. Afhankelijk van het inkomende catch weight-label, kan het totale gewicht van alle acht dozen worden vastgelegd en het gemiddelde gewicht kan vervolgens toebedeeld worden aan elke doos, of er kan een uniek gewicht voor elke doos worden vastgelegd.

Als geen gebruik wordt gemaakt van het bijhouden van catch weight-labels dan kan het gewicht worden vastgelegd voor elke dimensieset (bijvoorbeeld voor elke nummerplaat en traceringsdimensie). Het gewicht kan ook worden vastgelegd op basis van een samengevoegd niveau, zoals vijf nummerplaten (pallets).

Voor de methoden voor het vastleggen van het uitgaande gewicht, kunt u opgeven of het wegen is uitgevoerd voor elke catch weight-eenheid (dat wil zeggen per doos), of dat het gewicht wordt vastgelegd op basis van de hoeveelheid die zal worden opgenomen (bijvoorbeeld drie dozen). Houd er rekening mee dat voor het verzamelproces in de productielijn het gemiddelde gewicht wordt gebruikt als de optie **Niet vastgelegd** wordt gebruikt.

## <a name="supported-scenarios"></a>Ondersteunde scenario's

Niet alle workflows ondersteunen verwerking van catch weight-producten bij magazijnbeheer. De volgende beperkingen gelden momenteel.
 
### <a name="configuring-catch-weight-products-for-warehouse-management-processes"></a>Het configureren van catch weight-producten voor magazijnbeheerprocessen

- Voor catch weight-producten, kan de opslagdimensiegroep voor artikelen niet worden gewijzigd (zodat magazijnbeheerprocessen ervoor kunnen worden gebruikt).
- Alleen formuleverwerking wordt ondersteund voor catch weight-producten (niet-stuklijst).
- Catch weight-producten kunnen niet worden gekoppeld aan een traceringsdimensiegroep met behulp van de eigenaar-dimensie.
- Catch weight-producten kunnen niet worden gebruikt als services.
- Catch weight-producten kunnen alleen worden gebruikt als 'producten opgeslagen in voorraad' als onderdeel van de artikelmodelgroep.
- Catch weight-producten kunnen niet worden gebruikt samen met de functionaliteit voor het bijhouden van 'Actief in verkoopproces'.
- Catch weight-producten kunnen niet worden gebruikt samen met de functionaliteit voor het vastleggen van serienummers. Daarom kunnen producten niet worden overgeboekt van een 'leeg' naar een serienummer als onderdeel van het proces van verzamelen en verpakken.
- Catch weight-producten kunnen niet worden gebruikt samen met de functionaliteit voor het .registreren van serienummers voor verbruik.
- Catch weight-producten die variabel kunnen zijn, kunnen niet samen worden gebruikt met de functionaliteit voor het converteren van variabele maateenheden.
- Catch weight-producten kunnen niet worden gemarkeerd als een detailhandels 'productkit'.
- Catch weight-producten kunnen alleen worden gebruikt met een volgordegroep voor de eenheid die catch weight-materiaalverwerkingseenheden heeft en die de catch-weight-eenheid als laagste volgnummer heeft.
- Voor catch weight-producten kan de voorraadeenheid alleen worden geconverteerd naar de catch weight-eenheid als de conversie een nominale hoeveelheid van meer dan 1 produceert.
- Het instellen van streepjescodes voor catch weight-producten ondersteunt niet een variabele gewichtsinstelling.
 
### <a name="order-processing"></a>Orderverwerking

- Intercompany-orderverwerking wordt niet ondersteund.
- Het maken van een advance shipping notice (ASN/verpakkingsstructuren) ondersteunt geen gewichtinformatie.
- De orderhoeveelheid moet worden onderhouden gebaseerd op de catch weight-eenheid.
 
### <a name="inbound-warehouse-processing"></a>Inkomende magazijnverwerking

- Bij het ontvangen van nummerplaten moet gewicht worden toegewezen tijdens de registratie, omdat gewichtsinformatie niet wordt ondersteund als onderdeel van de advance shipping notice. Wanneer catch weight-labelprocessen worden gebruikt, moet het labelnummer handmatig worden toegewezen per catch weight-eenheid.
- Het ontvangen van gecombineerde nummerplaten wordt niet ondersteund voor catch weight-producten.
 
### <a name="inventory-and-warehouse-operations"></a>Voorraad- en magazijnoperaties

- Het handmatig maken van quarantaineorders wordt niet ondersteund voor catch weight-producten.
- Het handmatig muteren van voorraad dat is gerelateerd aan werk wordt niet ondersteund voor catch weight-producten.
- Het consolideren van nummerplaten wordt niet ondersteund voor catch weight-producten.
- Wijzigingen in de voorraadstatus magazijn als onderdeel van een periodieke taak worden niet voor catch weight-producten ondersteund.
- Wijzigingen in de voorraadstatus die zijn gedefinieerd door een query worden niet ondersteund voor catch weight-producten. (Wijzigingen in de voorraadstatus van de kwaliteitsorder worden ook niet ondersteund.)
- Voor catch weight-producten kan de voorraadstatus niet worden gewijzigd van de pagina **Voorhanden op locatie**.
- Voor catch weight-producten kan de voorraadstatus niet worden gewijzigd als onderdeel van het magazijnapp mutatiewerk.
- Het laden van nummerplaten voor het initialiseren van magazijnvoorraad wordt niet ondersteund voor catch weight-producten.
- Batchverdelingsprocessen worden niet ondersteund voor catch weight-producten.
- De verwerking van negatieve fysieke voorraad wordt niet ondersteund voor catch weight-producten.
- Voorraadmarkering kan niet worden gebruikt voor catch weight-producten.
 
### <a name="outbound-warehouse-processing"></a>Uitgaande magazijnverwerking

- De functie voor clusterverzamelen wordt niet ondersteund voor catch weight-producten.
- De magazijnverwerking verzamelen en inpakken wordt niet ondersteund voor catch weight-producten.
- Voor catch weight-producten kan werk niet worden voltooid van de pagina **Werk**.
- Voor catch weight-producten kan werk dat is gedefinieerd in een werksjabloon automatisch worden uitgevoerd.
- De functie voor het ongedaan maken van werk wordt niet ondersteund voor catch weight-producten.
- Voor catch weight-producten wordt het proces van het handmatige inpakstation waar werk wordt gecreëerd nadat containers zijn gesloten niet ondersteund.
- De functie voor stuk voor stuk scannen wordt niet ondersteund voor catch weight-producten.
 
### <a name="production-processing"></a>Productieverwerking

- Voor catch weight-producten worden alleen batchorders voor formuleproducten ondersteund.
- Kanbanfunctionaliteit wordt niet ondersteund voor catch weight-producten.
- Voor catch weight-producten kunnen serienummers niet vóór verbruik worden geregistreerd.
- De functie voor het ongedaan maken van nummerplaten wordt niet ondersteund voor catch weight-producten.
- Voor catch weight-producten kan gereedmelding worden geregistreerd op serienummer.

### <a name="transportation-management-processing"></a>Transportbeheerprocessen

- Workbench voor ladingopbouwverwerking wordt niet ondersteund voor catch weight-producten.
- Transportaanvraagregels worden niet ondersteund voor catch weight-producten.
 
### <a name="other-restrictions-and-behaviors-for-catch-weight-product-processing-with-warehouse-management"></a>Andere beperkingen en gedragingen voor het verwerken van catch weight-producten bij magazijnbeheer

- Als catch weight-labels worden vastgelegd als onderdeel van magazijnappverwerking, kan de gebruiker niet annuleren buiten de workflow.
- Tijdens verzamelprocessen waarin de gebruiker niet wordt gevraagd om traceringsdimensies te identificeren, wordt de gewichtstoewijzing gedaan op basis van het gemiddelde gewicht. Dit treedt op wanneer bijvoorbeeld een combinatie van traceringsdimensies wordt gebruikt op dezelfde locatie en nadat een gebruiker het verzamelen verwerkt en er slechts één trackingsdimensiewaarde op de locatie is gebleven.
- Wanneer de voorraad wordt gereserveerd voor een catch weight-product dat is geconfigureerd voor magazijnbeheerprocessen, wordt de reservering gedaan op basis van het minimumgewicht dat is gedefinieerd, zelfs als deze hoeveelheid de laatste voorhanden verwerkingshoeveelheid is. Dit gedrag wijkt af van het gedrag voor artikelen die niet zijn geconfigureerd voor magazijnbeheerprocessen.
- Processen die gebruikmaken van het gewicht als onderdeel van de capaciteitsberekeningen (wavedrempels, maximale werkpauzes, containermaxima, belastingscapaciteiten locatie, enzovoort) gebruiken het werkelijke gewicht van de voorraad niet. In plaats daarvan zijn de processen gebaseerd op het fysieke verwerkingsgewicht dat is gedefinieerd voor het product.
- In het algmeen wordt retailfunctionaliteit niet ondersteund voor catch weight-producten.
 
### <a name="catch-weight-tags"></a>Catch weight-labels

De functionaliteit voor catch weight-labels wordt momenteel uitsluitend ondersteund als onderdeel van de volgende scenario's:

- Bij de verwerking van inkooporders ontvangen via magazijnapp.
- Bij de verwerking van belasting ontvangen via magazijnapp.
- Voor het ontvangen van nummerplaten dat betrekking heeft op een opdrachtorderbelasting wordt tijdens het ontvangstproces toewijzing van gewicht gevraagd. Daarentegen wordt bij het ontvangen van transferorders het gewicht van de zendingsgegevens voor de transferorder gebruikt.
- Voor transferorderartikelen en regelontvangst afkomstig van een magazijn zonder magazijnbeheerproces.
- De verwerking van de ontvangst van verkoopretourorders kan catch weight-labels registreren, maar de verwerking wordt niet gevalideerd als de labels dezelfde labels zijn die oorspronkelijk zijn verzonden voor een bepaalde verkooporderregel.
- Wanneer de verwerking van een voorraadstatus is gewijzigd met behulp van de magazijnapp.
- Wanneer een magazijnoverdracht is gedaan met behulp van de magazijnapp.
- Bij het verwerken van een in- en uitcorrectie via de magazijnapp.
- Wanneer orderverzamelen wordt verwerkt voor verkoop en overdrachtorders. (Let op dat catch weight-labels niet kunnen worden opgenomen voor het verzamelen van productiecomponenten.)
- Wanneer verzamelde hoeveelheden worden verminderd van laadlijnen, ongeacht of containers worden gebruikt.
- Wanneer producten worden verpakt in containers op een inpakstation.
- Wanneer de containers worden heropend.
- Wanneer formuleproducten worden gereedgemeld via de magazijnapp.
- Wanneer transportbelastingen worden verwerkt met behulp van de magazijnapp.
