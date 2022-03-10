---
title: Voorraadtellingsprocessen definiëren
description: Deze onderwerp geeft een beschrijving van de configuratie van telprocessen voor basisvoorraad door een telgroep en een tellijst te maken.
author: yufeihuang
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventCountGroup, InventJournalName, InventParameters, EcoResProductDetailsExtended, InventItemLocation, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee47b04ba7ec9f3d74230b7a41b1c295eaea9313
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580835"
---
# <a name="define-inventory-counting-processes"></a>Voorraadtellingsprocessen definiëren

[!include [banner](../../includes/banner.md)]

Deze onderwerp geeft een beschrijving van de configuratie van telprocessen voor basisvoorraad door een telgroep en een tellijst te maken. Het laat u ook zien hoe u telbeleid kunt inschakelen op magazijn- en artikelniveau. Deze taken worden meestal uitgevoerd door een magazijnsupervisor. Het is een vereiste om sommige bestaande vrijgegeven producten en magazijnen te hebben. Als u een demobedrijf gebruikt, kunt u deze procedure in het bedrijf USMF uitvoeren met elk artikel dat is opgeslagen in voorraad.


## <a name="create-a-counting-group"></a>Een telgroep maken
1. Ga in het navigatievenster naar **Modules > Voorraadbeheer > Instellen > Voorraad > Telgroepen**.
2. Selecteer **Nieuw**.
3. Typ een waarde in het veld **Telgroep** van de nieuwe rij.
4. Typ een waarde in het veld **Naam**.
5. Selecteer een optie in het veld **Telcode**.

    - **Handmatig**: er worden steeds regels opgenomen wanneer u de taak uitvoert. Dit betekent dat u het tellingsinterval voor de tellingsgroep bepaalt.  
    - **Periode**: er worden regels voor de periode in de tellijst opgenomen wanneer het periode-interval is vervallen.  
    - **Nul in voorraad**: als de voorhanden voorraad nul (0) wordt, worden er regels in de tellijst gegenereerd wanneer de taak wordt uitgevoerd. Als de voorhanden voorraad na een telling nul (0) wordt, worden er regels gegenereerd de volgende keer dat u de telling start.  
    - **Minimum**: hiermee worden regels in de tellijst ingevoegd als de voorhanden voorraad gelijk is aan of kleiner is dan het opgegeven minimum.  
    - Optioneel: als u **Periode** hebt opgegeven in het veld **Telcode**, moet u het interval voor de periode typen in het veld **Telperiode**. De intervaleenheid is dagen.  
    - Wanneer u de taak uitvoert voor het maken van nieuwe regels in de tellijst, worden nieuwe regels gemaakt met het interval dat in dit veld is opgegeven, ongeacht hoe vaak u dezelfde taak uitvoert. Als bijvoorbeeld **Telperiode** op 7 is ingesteld en de journaalregels voor het laatst zijn gegenereerd voor een telling op 1 januari, zijn als een andere taak op 5 januari wordt gestart, nog geen zeven dagen verstreken en worden er dus geen regels gegenereerd in het journaal voor dit periode-interval. Als u de taak opnieuw start op 8 januari, worden er wel regels voor de periode gegenereerd in de tellijst, omdat er 7 dagen zijn verstreken.  

6. Selecteer **Opslaan**.

## <a name="create-a-counting-journal-name"></a>Een naam voor een tellijst maken
1. Ga in het navigatievenster naar **Modules > Voorraadbeheer > Instellen > Journaalnamen > Voorraad**.
2. Selecteer **Nieuw**.
3. Typ een waarde in het veld **Naam**.
4. Typ een waarde in het veld **Beschrijving**.
5. Selecteer **Tellen** in het veld **Journaaltype**. Optioneel: u kunt een andere boekstukreeks-id selecteren als u een specifieke nummerreeks wilt voor de boekstukreeks-id's die worden gegenereerd bij het maken van tellijsten. Boekstukreeksen worden gemaakt op de pagina **Nummerreeksen**.  
6. Selecteer een optie in het veld **Detailniveau**.  

    - Dit is het detailniveau dat wordt toegepast wanneer het journaal wordt geboekt.  
    - Optioneel: u kunt de waarde wijzigen in het veld Reservering. Dit is de methode die wordt gebruikt voor het reserveren van artikelen tijdens het tellen.   
    - **Handmatig**: de artikelen worden handmatig gereserveerd op het formulier Reservering.  
    - **Automatisch**: de bestelhoeveelheid wordt gereserveerd in de beschikbare voorhanden voorraad voor het artikel.   
    - **Explosie**: de reservering maakt deel uit van de hoofdplanning van de transactie.  

7. Selecteer **Opslaan**.

## <a name="set-standard-counting-journal-name"></a>Standaardtellijstnaam instellen
1. Ga in het navigatievenster naar **Modules > Voorraadbeheer > Instellen > Parameters voor voorraad- en magazijnbeheer**.
2. Selecteer het tabblad **Journalen**.
3. Selecteer in de vervolgkeuzelijst van het veld **Tellen** het journaal dat u eerder hebt gemaakt. Dit journaal is dan de standaardjournaalnaam voor voorraadjournalen van het type **Tellen**.  
4. Selecteer het tabblad **Algemeen**. Optioneel: selecteer deze optie om een artikel te vergrendelen tijdens het telproces om updates te voorkomen voor pakbonnen, orderverzamellijsten of orderverzamellijstregistraties.  

## <a name="set-the-counting-policy-for-an-item"></a>Het telbeleid voor een artikel instellen
1. Ga in het navigatievenster naar **Modules > Productgegevensbeheer > Producten > Vrijgegeven producten**.
2. Selecteer in de lijst de koppeling voor het artikelnummer van het product waarvoor u telbeleid wilt instellen. U moet een artikel selecteren dat in de voorraad wordt bijgehouden. Een product waarvoor geen voorraad wordt bijgehouden kan niet worden geteld. Als u het demobedrijf USMF gebruikt, kunt u artikel A0001 selecteren.  
3. Selecteer **Bewerken**.
4. Schakel de uitbreiding van de sectie **Voorraad beheren** in.
5. Selecteer in de vervolgkeuzelijst van het veld **Telgroep** de telgroep die u eerder hebt gemaakt. Dit product wordt nu opgenomen wanneer de regels van de voorraadtellijst met deze telgroep worden gemaakt.  
6. Selecteer **Opslaan**.

## <a name="set-the-counting-policy-for-an-item-in-a-specific-warehouse"></a>Het telbeleid voor een artikel in een specifiek magazijn instellen
1. Selecteer in het actievenster de optie **Voorraad beheren**.
2. Selecteer **Magazijnartikelen**.
3. Selecteer **Nieuw**.
4. Selecteer in de vervolgkeuzelijst van het veld **Magazijn** het magazijn waarvoor u een specifiek tellingsbeleid wilt instellen.
5. Selecteer een telgroep in het vervolgkeuzemenu van het veld **Telgroep**. U kunt een specifieke telgroep selecteren die moet gelden voor het artikel in het opgegeven magazijn dat u hebt geselecteerd. Als het tellen wordt uitgevoerd in dat magazijn, negeert dit telbeleid het algemene telbeleid voor het artikel.  
6. Selecteer **Opslaan**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]