---
title: "Voorraadtellingsprocessen definiëren"
description: Deze procedure leidt u door de configuratie van telprocessen voor basisvoorraad door een telgroep en een tellijst te maken.
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 62c60faafd9ad96ce636a08102bc8652f9fff870
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="define-inventory-counting-processes"></a>Voorraadtellingsprocessen definiëren

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure leidt u door de configuratie van telprocessen voor basisvoorraad door een telgroep en een tellijst te maken. Het laat u ook zien hoe u telbeleid kunt inschakelen op magazijn- en artikelniveau. Deze taken worden meestal uitgevoerd door een magazijnsupervisor. Het is een vereiste om sommige bestaande vrijgegeven producten en magazijnen te hebben. Als u een demobedrijf gebruikt, kunt u deze procedure in het bedrijf USMF uitvoeren met elk artikel dat is opgeslagen in voorraad.


## <a name="create-a-counting-group"></a>Een telgroep maken
1. Ga naar Voorraadbeheer > Instellingen > Voorraad > Telgroepen.
2. Klik op Nieuw.
3. Typ een waarde in het veld Telgroep.
4. Typ een waarde in het veld Naam.
5. Selecteer een optie in het veld Telcode.
    * Handmatig – Er worden steeds regels opgenomen wanneer u de taak uitvoert. Dit betekent dat u het tellingsinterval voor de tellingsgroep bepaalt.  Periode – Er worden regels voor de periode in de tellijst opgenomen wanneer het periode-interval is vervallen.   Nul in voorraad – als de voorhanden voorraad nul (0) wordt, worden er regels in de tellijst gegenereerd wanneer de taak wordt uitgevoerd. Als de voorhanden voorraad na een telling nul (0) wordt, worden er regels gegenereerd de volgende keer dat u de telling start.   Minimum – Hiermee worden regels in de tellijst ingevoegd als de voorhanden voorraad gelijk is aan of kleiner is dan het opgegeven minimum.  
    * Optioneel: als u Periode hebt opgegeven in het veld Telcode, moet u het interval voor de periode typen in het veld Telperiode. De intervaleenheid is dagen.  
    * Wanneer u de taak uitvoert voor het maken van nieuwe regels in de tellijst, worden nieuwe regels gemaakt met het interval dat in dit veld is opgegeven, ongeacht hoe vaak u dezelfde taak uitvoert. Als bijvoorbeeld Telperiode op 7 is ingesteld en de journaalregels voor het laatst zijn gegenereerd voor een telling op 1 januari, zijn als een andere taak op 5 januari wordt gestart, nog geen zeven dagen verstreken en worden er dus geen regels gegenereerd in het journaal voor dit periode-interval. Als u de taak opnieuw start op 8 januari, worden er wel regels voor de periode gegenereerd in de tellijst, omdat er 7 dagen zijn verstreken.  
6. Klik op Opslaan.

## <a name="create-a-counting-journal-name"></a>Een naam voor een tellijst maken
1. Ga naar Voorraadbeheer > Instellingen > Journaalnamen > Voorraad.
2. Klik op Nieuw.
3. Typ een waarde in het veld Naam.
4. Typ een waarde in het veld Omschrijving.
5. Selecteer Tellen in het veld Journaaltype.
    * Optioneel: u kunt een andere boekstukreeks-id selecteren als u een specifieke nummerreeks wilt voor de boekstukreeks-id's die worden gegenereerd bij het maken van tellijsten. Boekstukreeksen worden gemaakt op de pagina Nummerreeksen.  
6. Selecteer een optie in het veld Detailniveau.
    * Dit is het detailniveau dat wordt toegepast wanneer het journaal wordt geboekt.  
    * Optioneel: u kunt de waarde wijzigen in het veld Reservering. Dit is de methode die wordt gebruikt voor het reserveren van artikelen tijdens het tellen.   
    * Handmatig - De artikelen worden handmatig gereserveerd op het formulier Reservering.   Automatisch - De bestelhoeveelheid wordt gereserveerd in de beschikbare voorhanden voorraad voor het artikel.   Explosie - De reservering maakt deel uit van de hoofdplanning van de transactie.  
7. Klik op Opslaan.

## <a name="set-standard-counting-journal-name"></a>Standaardtellijstnaam instellen
1. Ga naar Voorraadbeheer > Instellingen > Parameters voor voorraad- en magazijnbeheer.
2. Klik op het tabblad Journalen.
3. Klik in het veld Tellen op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Selecteer het journaal dat u eerder hebt gemaakt.
    * Dit journaal is dan de standaardjournaalnaam voor voorraadjournalen van het type Tellen.  
5. Klik op het tabblad Algemeen.
    * Optioneel: selecteer deze optie om een artikel te vergrendelen tijdens het telproces om updates te voorkomen voor pakbonnen, orderverzamellijsten of orderverzamellijstregistraties.  

## <a name="set-the-counting-policy-for-an-item"></a>Het telbeleid voor een artikel instellen
1. Ga naar Productgegevensbeheer > Producten > Vrijgegeven producten.
2. Klik in de lijst op de koppeling voor het artikelnummer van het product waarvoor u telbeleid wilt instellen.
    * Merk op dat u een artikel moet selecteren dat in de voorraad wordt bijgehouden. Een product waarvoor geen voorraad wordt bijgehouden kan niet worden geteld. Als u het demobedrijf USMF gebruikt, kunt u artikel A0001 selecteren.  
3. Klik op Bewerken.
4. Schakel de uitbreiding van de sectie Voorraad beheren om.
5. Klik in het veld Telgroep op de vervolgkeuzeknop om de zoekopdracht te openen.
6. Klik in de lijst op de telgroep u eerder hebt gemaakt.
    * Dit product wordt nu opgenomen wanneer de regels van de voorraadtellijst met deze telgroep worden gemaakt.  
7. Klik op Opslaan.

## <a name="set-the-counting-policy-for-an-item-in-a-specific-warehouse"></a>Het telbeleid voor een artikel in een specifiek magazijn instellen
1. Klik in het actievenster op Voorraad beheren.
2. Klik op Magazijnartikelen.
3. Klik op Nieuw.
4. Klik in het veld Magazijn op de vervolgkeuzeknop om de zoekopdracht te openen.
5. Selecteer in de lijst het magazijn waarvoor u specifiek telbeleid wilt instellen.
6. Klik in het veld Telgroep op de vervolgkeuzeknop om de zoekopdracht te openen.
7. Selecteer een telgroep in de lijst.
    * Hier kunt u een specifieke telgroep selecteren die moet gelden voor het artikel in het opgegeven magazijn dat u hebt geselecteerd. Als het tellen wordt uitgevoerd in dat magazijn, negeert dit telbeleid het algemene telbeleid voor het artikel.  
8. Klik op Opslaan.
