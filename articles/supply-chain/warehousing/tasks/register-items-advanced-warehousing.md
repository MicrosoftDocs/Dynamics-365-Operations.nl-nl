---
title: Artikelen registreren voor een artikel waarvoor geavanceerd magazijnbeheer mogelijk is met een artikelontvangstjournaal
description: Deze procedure toont hoe u artikelen registreert via het artikelontvangstjournaal wanneer u de geavanceerde magazijnbeheerprocessen gebruikt.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 392884d2a87c10a5f38bf6f51967f879c68c1ca6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558075"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a>Artikelen registreren voor een artikel waarvoor geavanceerd magazijnbeheer mogelijk is met een artikelontvangstjournaal

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure toont hoe u artikelen registreert via het artikelontvangstjournaal wanneer u de geavanceerde magazijnbeheerprocessen gebruikt. Dit wordt gewoonlijk uitgevoerd door een ontvangstadministrateur. 

U kunt deze procedure uitvoeren in het demogegevensbedrijf USMF of met uw eigen gegevens. U moet een bevestigde inkooporder met een openstaande inkooporderregel hebben voordat u deze handleiding start. Het artikel op de regel moet in voorraad zijn opgeslagen, er mogen geen productvarianten worden gebruikt en het mag geen traceringsdimensies hebben. En het artikel moet zijn gekoppeld aan een opslagdimensiegroep die gebruikmaakt van magazijnbeheerprocessen. Het magazijn dat wordt gebruikt moet zijn ingeschakeld voor magazijnbeheerprocessen en de locatie die u voor het ontvangen gebruikt moet worden gecontroleerd op nummerplaat. Als u USMF gebruikt, kunt u bedrijfsrekening 1001, Magazijn 51 en artikel M9200 gebruiken om de IO te maken. 

Noteer het nummer van de inkooporder die u maakt en noteer ook het artikelnummer en de site die u voor de inkooporderregel gebruikt.


## <a name="create-an-item-arrival-journal-header"></a>Een koptekst voor artikelontvangstjournaal maken
1. Ga naar Artikelontvangst.
2. Klik op Nieuw.
3. Typ een waarde in het veld Naam.
    * Als u USMF gebruikt, kunt u WHS typen. Als u andere gegevens gebruikt, moet het journaal waarvan u de naam kiest de volgende eigenschappen hebben: Orderverzamellocatie controleren moet zijn ingesteld op Nee en Quarantainebeheer moet zijn ingesteld op Nee.  
4. Typ een waarde in het veld Nummer.
5. Typ een waarde in het veld Locatie.
    * Selecteer de site die u voor de inkooporderregel hebt gebruikt. Dit fungeert als een standaardwaarde, die standaard wordt ingesteld op alle regels in het journaal. Als u magazijn 51 gebruikte in USMF, kiest u site 5.  
6. Typ een waarde in het veld Magazijn.
    * Selecteer een geldig magazijn voor de site die u hebt geselecteerd. Dit fungeert als een standaardwaarde, die standaard wordt ingesteld op alle regels in het journaal. Als u de voorbeeldwaarden in USMF gebruikt, selecteert u 51.  
7. Typ een waarde in het veld Locatie.
    * Selecteer een geldige locatie in het magazijn dat u hebt geselecteerd. De locatie moet aan een locatieprofiel zijn gekoppeld, waar nummerplaten worden gecontroleerd. Dit fungeert als een standaardwaarde, die standaard wordt ingesteld op alle regels in het journaal. Als u de voorbeeldwaarden in USMF gebruikt, selecteert u Bulk-008.  
8. Klik met de rechtermuisknop op de vervolgkeuzepijl in het veld Nummerplaat en selecteer vervolgens Details weergeven.
9. Klik op Nieuw.
10. Typ een waarde in het veld Nummerplaat.
    * Noteer de waarde.  
11. Klik op Opslaan.
12. Sluit de pagina.
13. Typ een waarde in het veld Nummerplaat.
    * Voer de waarde van de nummerplaat in die u zojuist hebt gemaakt. Dit fungeert als een standaardwaarde, die standaard wordt ingesteld op alle regels in het journaal.  
14. Klik op OK.

## <a name="add-a-line"></a>Een regel toevoegen
1. Klik op Regel toevoegen.
2. Typ een waarde in het veld Artikelnummer.
    * Voer het artikelnummer in dat u op de inkooporderregel hebt gebruikt.  
3. Voer in het veld Hoeveelheid een getal in.
    * Voer de hoeveelheid in die u wilt registreren.  
    * Het veld Datum bepaalt de datum waarop de voorhanden hoeveelheid van het artikel in de voorraad wordt geregistreerd.  
    * De partij-id wordt door het systeem ingevuld als deze uniek kan worden geïdentificeerd uit de opgegeven informatie. Anders moet u deze handmatig toevoegen. Dit is een verplichte veld, dat deze registratie aan een specifieke brondocumentregel koppelt.  

## <a name="complete-the-registration"></a>De registratie voltooien
1. Klik op Valideren.
    * Dit controleert of het journaal gereed is om te worden geboekt. Als validatie mislukt, kunt u de fouten bevestigen voordat u het journaal kunt boeken.  
2. Klik op OK.
    * Nadat u op OK hebt geklikt, controleert u het bericht. Er moet een bericht zijn dat meldt dat het journaal OK is.  
3. Klik op Boeken.
4. Klik op OK.
    * Nadat u op OK hebt geklikt, controleert u de berichtenbalk. Er moet een bericht zijn dat meldt dat de bewerking voltooid is.  
5. Sluit de pagina.

