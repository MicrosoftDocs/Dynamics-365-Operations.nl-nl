---
title: Activiteiten tijdens uitvaltijd voor onderhoud
description: In dit onderwerp wordt uitgelegd hoe uitvaltijd voor onderhoud wordt gebruikt om een overzicht te krijgen van de capaciteit die nodig is voor het uitvoeren van onderhoudstaken voor bepaalde activa gedurende een bepaalde periode.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetMaintenanceStopCopy, EntAssetMaintenanceStopObject, EntAssetObjectProductionStop, EntAssetProductionStopType, EntAssetMaintenanceStop
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 617fca55226e216197c385c88a9d7a8e3de03b03
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425475"
---
# <a name="maintenance-downtime-activities"></a>Activiteiten tijdens uitvaltijd voor onderhoud

[!include [banner](../../includes/banner.md)]

Uitvaltijd voor onderhoud wordt gebruikt om een overzicht te krijgen van de capaciteit die nodig is voor het uitvoeren van onderhoudstaken voor bepaalde activa gedurende een bepaalde periode. U kunt bijvoorbeeld de uitvaltijd voor onderhoud registreren voor Productieregel 10 in Productiezaal 29-A op productielocatie 02. De registratie van uitvaltijd voor onderhoud heeft een begin- en eindtijd die de periode aangeeft waarin de activa voor de onderhoudsstop niet beschikbaar zijn voor productie.

**Activiteiten voor uitvaltijd voor onderhoud** is een overzicht van onderhoudsplanningsregels en onderhoudstaken voor werkorders voor gerelateerde activa gedurende een bepaalde periode. De regels met betrekking tot onderhoudstaken voor werkorders hebben allemaal een verwachte begindatum binnen de periode van de onderhoudsstop. U kunt nuttige informatie ophalen en wijzigingen in geplande onderhoudstaken aanbrengen:

- Vraag een overzicht op van de vereiste afsluitperioden van productieapparatuur (activa).  
- Vraag een overzicht op van gepland onderhoud (uren), gegroepeerd op competenties (verantwoordelijke onderhoudsmedewerkersgroepen of onderhoudsmedewerkers), bijvoorbeeld capaciteitsbelasting voor elektriciens, smeden of andere onderhoudsmedewerkersgroepen die vereist zijn voor het uitvoeren van geplande onderhoudstaken.  
- Breng aanpassingen aan in onderhoudsplanningsregels of onderhoudstaken voor de activa, wijzig bijvoorbeeld de verwachte begin- en eindtijden op een regel of selecteer andere onderhoudsmedewerkers om de workflow voor onderhoudsmedewerkers en onderhoudsmedewerkersgroepen te optimaliseren.

Wanneer activa in een registratie van uitvaltijd voor onderhoud zijn geselecteerd, worden alle openstaande onderhoudsschemaregels en onderhoudstaken voor werkorders met betrekking tot actieve werkorders opgenomen in de registratie van de uitvaltijd voor onderhoud.

## <a name="maintenance-downtime-activities"></a>Activiteiten tijdens uitvaltijd voor onderhoud

Klik op **Activabeheer** > **Algemeen** > **Activiteiten voor uitvaltijd voor onderhoud** > **Alle activiteiten voor uitvaltijd voor onderhoud** om een lijst te openen van alle activiteiten voor uitvaltijd voor onderhoud en informatie over de activiteiten te bekijken. Klik op een koppeling in de kolom **Activiteiten voor uitvaltijd voor onderhoud** om de detailweergave te openen. In de onderstaande afbeelding ziet u een voorbeeld van de lijst **Activiteiten voor uitvaltijd voor onderhoud**.

![Figuur 1](media/19-preventive-maintenance.png)


## <a name="create-a-maintenance-downtime-activity"></a>Een activiteit voor uitvaltijd voor onderhoud maken

1. Klik op **Activabeheer** > **Algemeen** > **Activiteiten voor uitvaltijd voor onderhoud** > **Alle activiteiten voor uitvaltijd voor onderhoud** of **Actieve activiteiten voor uitvaltijd voor onderhoud**.

2. Klik op **Nieuw**.

3. Geef een id op in het veld **Activiteiten voor uitvaltijd voor onderhoud** en een naam in het veld **Naam**.

4. Geef de periode voor de onderhoudsstop op in de velden **Begindatum/-tijd** en **Einddatum/-tijd**.

5. Klik op het sneltabblad **Activa voor activiteiten voor uitvaltijd voor onderhoud** op **Regel toevoegen** om activa één voor één toe te voegen aan de activiteit voor uitvaltijd voor onderhoud.

6. Klik op **Opslaan** wanneer alle activa zijn toegevoegd. In de onderstaande afbeelding ziet u een voorbeeld van een activiteit voor uitvaltijd voor onderhoud met bijbehorende activa en onderhoudstaken.

7. De onderhoudstaken voor werkorders en de openstaande onderhoudsschemaregels voor de geselecteerde activa worden weergegeven op de sneltabbladen **Resulterende onderhoudstaken voor werkorder** en **Onderhoudsschemaregels**. Op het sneltabblad **Algemeen** > groep **Werkorders** > veld **Prognose onderhoudsuren** en sneltabblad **Algemeen** >groep **Onderhoudsschema** > veld **Prognose onderhoudsuren** ziet u het totaal aantal uren dat is geraamd voor onderhoudstaken en onderhoudsschemaregels van werkorders.

In de onderstaande afbeelding ziet u een voorbeeld van de detailweergave **Activiteiten voor uitvaltijd voor onderhoud**.

![Figuur 2](media/20-preventive-maintenance.png)

>[!NOTE]
>De onderhoudstaken en onderhoudsschemaregels van werkorders voor de geselecteerde activa worden automatisch bijgewerkt als er nieuwe werkorders of onderhoudsschemaregels worden gemaakt nadat u de activiteit voor uitvaltijd voor onderhoud hebt gemaakt. Als u bijvoorbeeld twee dagen na het maken van de activiteit voor uitvaltijd voor onderhoud onderhoudsplannen of onderhoudsronden voor de betreffende activa plant, worden er automatisch nieuwe onderhoudsschemaregels aan de activiteit voor uitvaltijd voor onderhoud toegevoegd.

8. Selecteer in **Alle activiteiten voor uitvaltijd voor onderhoud** > **Activiteiten voor uitvaltijd voor onderhoud** een activiteit voor uitvaltijd voor onderhoud in de lijst en klik op **Capaciteitsbelasting** om het dialoogvenster **Capaciteitsbelasting berekenen** te openen. Gebruik dit dialoogvenster om een overzicht te krijgen van de capaciteitsbelasting voor bijvoorbeeld datums, activa, activatypen en typen onderhoudstaken. De datums die in het dialoogvenster worden weergegeven, zijn de begin- en einddatums die zijn geselecteerd in **Activiteiten voor uitvaltijd voor onderhoud**. Deze berekening bevat de activa met betrekking tot de activiteit voor uitvaltijd voor onderhoud.

9. In het dialoogvenster **Capaciteitsbelasting berekenen** kunt u de begin- en eindtijden bewerken en selecteren of u werkorders en onderhoudsschema's in de berekening wilt opnemen. Gebruik het veld **Niveau** om aan te geven hoe gedetailleerd u de capaciteitsbelasting wilt berekenen met betrekking tot functionele locaties. Als u bijvoorbeeld het getal 1 in het veld invoegt en u een structuur met meerdere niveaus voor functionele locaties hebt, worden alle activa voor een functionele locatie die in de activiteit voor uitvaltijd voor onderhoud zijn geselecteerd, weergegeven op het hoogste niveau. Het is daarom mogelijk dat de uren op een regel worden opgeteld vanuit functionele locaties die zich op een lager niveau bevinden. Als u het getal 0 in het veld **Niveau** invoegt, ziet u een gedetailleerd resultaat met alle regels voor capaciteitsbelasting op alle niveaus voor functionele locaties waarop deze betrekking hebben.

10. Klik op **OK** om de berekening te starten. Het totaal aantal uren wordt weergegeven in het overzicht **Capaciteitsbelasting**. Klik op het tabblad **Capaciteitsbelasting** > in de actievenstergroepen **Groeperen op…** op de relevante knoppen voor een gedetailleerder overzicht van de toewijzing van geraamde uren. In de onderstaande afbeelding ziet u de resultaten van de berekening van de **Capaciteitsbelasting**.

![Figuur 3](media/21-preventive-maintenance.png)

11. Wanneer u een overzicht van de capaciteitsbelasting hebt ontvangen en wijzigingen wilt aanbrengen in de onderhoudstaken voor werkorders of de onderhoudsschemaregels, dan kunt u terugkeren naar de detailweergave **Activiteiten voor uitvaltijd voor onderhoud**. Selecteer daar de regels die u wilt corrigeren op de sneltabbladen **Resulterende onderhoudstaken voor werkorder** en **Onderhoudsschemaregels**.

12. Klik op de knop **Aanpassen** en werk verwachte begin- en einddatums, serviceniveau of verantwoordelijke onderhoudsmedewerkers voor de geselecteerde onderhoudstaken of de onderhoudsschemaregels bij.

13. Klik op **OK** wanneer u de vereiste correcties hebt aangebracht. 

>[!NOTE]
>Onderhoudstaken voor werkorders en onderhoudsschemaregels die niet zijn opgenomen in de periode voor uitvaltijd voor onderhoud nadat u correcties hebt aangebracht, worden automatisch verwijderd uit **Activiteiten voor uitvaltijd voor onderhoud**.

14. Selecteer een activiteit voor uitvaltijd voor onderhoud in de lijst in **Alle activiteiten voor uitvaltijd voor onderhoud** > **Activiteiten voor uitvaltijd voor onderhoud** en klik op **Artikelprognose** om het dialoogvenster **Artikelprognose berekenen** te openen. Gebruik dit dialoogvenster om prognoses te berekenen voor artikelen (reserve-onderdelen en andere vereiste artikelen) en deze te groeperen om een overzicht te krijgen, bijvoorbeeld op basis van datum, activum, activatype en type onderhoudstaak. De datums die in het dialoogvenster worden weergegeven, zijn de begin- en einddatums die zijn geselecteerd in **Activiteiten voor uitvaltijd voor onderhoud**. Deze berekening bevat reserve-onderdelen en artikelen voor de activa die zijn geselecteerd in de activiteit voor uitvaltijd voor onderhoud.

15. In het dialoogvenster **Artikelprognose berekenen** kunt u de begin- en eindtijden bewerken en selecteren of u werkorders en onderhoudsschema's in de berekening wilt opnemen. Gebruik het veld **Niveau** om aan te geven hoe gedetailleerd u de capaciteitsbelasting wilt berekenen met betrekking tot functionele locaties. Als u bijvoorbeeld het getal 1 in het veld invoegt en u een structuur met meerdere niveaus voor functionele locaties hebt, worden alle activa voor een functionele locatie die in de activiteit voor uitvaltijd voor onderhoud zijn geselecteerd, weergegeven op het hoogste niveau. Het is daarom mogelijk dat de uren op een regel worden opgeteld vanuit functionele locaties die zich op een lager niveau bevinden. Als u het getal 0 in het veld **Niveau** invoegt, ziet u een gedetailleerd resultaat met alle regels voor capaciteitsbelasting op alle niveaus voor functionele locaties waarop deze betrekking hebben.

16. Klik op **OK** om de berekening te starten. Het totaal aantal artikelprognoses wordt weergegeven in het overzicht **Artikelprognose**. Klik op het tabblad **Artikelprognose** > in de actievenstergroepen **Groeperen op…** op de relevante knoppen voor een gedetailleerder overzicht van de toewijzing van geraamde artikelen. In de onderstaande afbeelding ziet u de resultaten van de berekening van een **Artikelprognose**.

![Figuur 4](media/22-preventive-maintenance.png)

- U kunt activa van de ene activiteit voor uitvaltijd voor onderhoud naar een andere kopiëren. Selecteer in **Alle activiteiten voor uitvaltijd voor onderhoud** de knop **Activiteiten voor uitvaltijd voor onderhoud kopiëren** en selecteer de gewenste opties in de velden **Van activiteiten voor uitvaltijd voor onderhoud** en **Naar activiteiten voor uitvaltijd voor onderhoud** en klik op **OK**.
- Klik in **Alle activiteiten voor uitvaltijd voor onderhoud** op de knop **Onderhoudsschemaregels** of de knop **Actieve werkorders** om de gerelateerde lijsten te openen en de regels voor de geselecteerde activiteit voor uitvaltijd voor onderhoud weer te geven.

