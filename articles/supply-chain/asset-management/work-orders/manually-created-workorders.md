---
title: Handmatig gemaakte werkorders
description: In dit onderwerp wordt uitgelegd hoe u werkorders handmatig maakt in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderTableCreateRelated, EntAssetWorkOrderTableCreate, EntAssetWorkOrderTableCopy
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8c787dbc9889139df76b9b102deb18fce567e382
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017863"
---
# <a name="manually-created-work-orders"></a>Handmatig gemaakte werkorders

[!include [banner](../../includes/banner.md)]


U kunt werkorders op twee manieren handmatig maken:

- Op de pagina **Alle werkorders** of **Actieve werkorders** 
- Op de pagina **Alle onderhoudsverzoeken** of **Actieve onderhoudsverzoeken** of **De onderhoudsverzoeken van mijn functionele locatie** 

## <a name="create-work-order"></a>Werkorder maken

1. Selecteer **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.

2. Selecteer **Nieuw**.

3. Selecteer in het dialoogvenster **Werkorder maken** een werkordertype in het veld **Werkordertype**.

4. Selecteer zo nodig een **Beschrijving**.

5. Selecteer het activum in het veld **Activum**.

>[!NOTE]
>Wanneer u een activum selecteert, zijn er mogelijk drie tabbladen beschikbaar in de vervolgkeuzelijst **Activum**: 

- **Actieve activa**: dit tabblad bevat een lijst met alle activa met de levenscyclusstatus 'Actief' voor activa. 
- **Activaweergave**: op dit tabblad wordt een structuurweergave getoond van functionele locaties en de activa die op die locaties zijn geïnstalleerd.
- **Mijn activa**: dit tabblad bevat activa die zijn gerelateerd aan de functionele locaties die aan u (de werknemer die bij het systeem is aangemeld) kunnen worden toegewezen. (Zie [Onderhoudsmedewerkers en groepen werknemers](../setup-for-objects/workers-and-worker-groups.md) voor meer informatie over de instellingen.) Als er geen functionele locaties zijn ingesteld voor een werknemer in [Onderhoudsmedewerkers en groepen werknemers](../setup-for-objects/workers-and-worker-groups.md) is het tabblad **Mijn activa** niet beschikbaar. 

6. Selecteer een type onderhoudstaak voor de werkorder in het veld **Type onderhoudstaak**.

7. Selecteer indien nodig de **variant van type onderhoudstaak** en **Handel**.

8. Indien nodig kunt u het serviceniveau van de werkorder wijzigen in het veld **Serviceniveau**.

9. Selecteer de **verwachte begin-** en **einddatums** in de daarvoor bestemde velden.

10. Klik op **OK** om de werkorder te maken.

11. Op de lijstpagina **Alle werkorders** kunt u de werkorder naar wens bewerken.

Let op de volgende punten:

- In de detailweergave op de lijstpagina **Alle werkorders** kunt u verschillende activa aan een werkorder toevoegen. Daarvoor voegt u regels toe op het sneltabblad **Onderhoudstaken voor werkorders**. Op een activum kunt u alleen de typen onderhoudstaken selecteren die zijn gedefinieerd voor het activumtype dat voor het activum is geselecteerd.  

- Als u het serviceniveau of de kritieke eigenschappen van een activum in deze instellingen wijzigt nadat u het activum al hebt gebruikt op een werkorder, worden het serviceniveau of de kritieke eigenschappen van de werkorder niet dienovereenkomstig bijgewerkt. Zie [Serviceniveaus van activa](../setup-for-objects/object-priorities.md) en [Typen kritieke eigenschappen van activa](../setup-for-objects/object-criticalities.md) voor meer informatie over serviceniveaus en kritieke eigenschappen.

- De kritieke eigenschappen van een werkorder worden telkens opnieuw berekend wanneer een werkordertaak wordt toegevoegd aan of verwijderd uit de werkorder.

- In de detailweergave **Alle werkorders** > tabblad **Koptekst** > sneltabblad **Planning** kunt u een verantwoordelijke onderhoudsmedewerkersgroep of een verantwoordelijke onderhoudsmedewerker selecteren in het veld **Verantwoordelijke groep** of **Verantwoordelijke**. Deze instellingen kunnen worden gewijzigd terwijl de werkorder actief is. Ze kunnen bijvoorbeeld worden gewijzigd als de levenscyclusstatus van de werkorder verandert. De automatische selectie tijdens het maken van de werkorder is gebaseerd op de instellingen op de pagina **Verantwoordelijke onderhoudsmedewerkers**. Als u werkordertaken toevoegt of verwijdert nadat u een werkorder hebt gemaakt, en als de velden **Verantwoordelijke groep** en **Verantwoordelijke** leeg zijn wanneer u de werkorder bijwerkt, zoekt Activabeheer naar een mogelijke overeenkomst op de instellingenpagina voor een verantwoordelijke onderhoudsmedewerkersgroep of een verantwoordelijke onderhoudsmedewerker. Als het veld **Verantwoordelijke groep** of **Verantwoordelijke** al is ingesteld wanneer u de werkorder bijwerkt, worden er geen wijzigingen aangebracht. Zie [Verantwoordelijke onderhoudsmedewerkers](../setup-for-maintenance-requests/responsible-workers.md) voor meer informatie over verantwoordelijke onderhoudsmedewerkers en onderhoudsmedewerkersgroepen.

- Op de pagina [Onderhoudsstatus](../controlling-and-reporting/maintenance-status.md) kunt u een berekening uitvoeren om een overzicht te krijgen van de werkbelasting voor inkomende en voltooide werkorders.  

- In de detailweergave van de pagina **Alle werkorders** kunt u op het sneltabblad **Regeldetails** de velden **Breedtegraad** en **Lengtegraad** gebruiken om geografische coördinaten toe te voegen voor het geselecteerde activum in de werkordertaak.  


## <a name="create-related-work-order"></a>Gerelateerde werkorder maken

U kunt een werkorder maken die betrekking heeft op een bestaande werkorder. Deze functie is handig als bijvoorbeeld wilt werken met primaire en secundaire werkorders. Een nieuwe werkorder is gebaseerd op een werkordertaak op basis van een bestaande werkorder.

1. Selecteer **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.

2. Selecteer de werkorder waarvoor u een gerelateerde werkorder wilt maken.

3. Selecteer in het actievenster op het tabblad **Werkorder** in de groep **Nieuw** de optie **Gerelateerde werkorder**.

4. Selecteer in het dialoogvenster **Gerelateerde werkorder maken** de werkordertaak waarvoor u een gerelateerde werkorder wilt maken in het veld **Werkordertaak**.

5. Selecteer in het veld **Type onderhoudstaak** het type onderhoudstaak.

6. Selecteer in de velden **Variant van type onderhoudstaak** en **Handel** de variant en handel voor het type onderhoudstaak.

7. Als deze werkorder de eerste gerelateerde werkorder is die voor de geselecteerde werkorder wordt gemaakt, voert u de volgende stappen uit:
    1. Selecteer de optie **Nieuwe werkorder**.
    2. Selecteer een type werkorder in het veld **Werkordertype**.
    3. Voer bij **Beschrijving** een beschrijving in.
    4. Indien nodig kunt u het serviceniveau van de werkorder wijzigen in het veld **Serviceniveau**.
    5. Selecteer in de velden **Verwachte begindatum** en **Verwachte einddatum** de verwachte begin- en einddatums.
    6. Selecteer **OK**. De nieuwe gerelateerde werkorder wordt weergegeven op de lijstpagina **Alle werkorders**.  

8. Als de werkorder waarvoor u deze gerelateerde werkorder maakt al gerelateerde werkorders heeft, voert u de volgende stappen uit om een nieuwe werkordertaak toe te voegen aan een bestaande gerelateerde werkorder:
    1. Selecteer de optie **Toevoegen aan gerelateerde werkorder**.
    2. Selecteer de gerelateerde werkorder waaraan u een nieuwe werkordertaak wilt toevoegen in het veld **Werkorder**.
    3. Indien nodig kunt u het serviceniveau van de werkorder wijzigen in het veld **Serviceniveau**.
    4. Wijzig zo nodig in de velden **Verwachte begindatum** en **Verwachte einddatum** de verwachte begin- en einddatums.
    5. Selecteer **OK**. De werkordertaak wordt toegevoegd aan de bestaande gerelateerde werkorder.

In de onderstaande afbeelding ziet u een voorbeeld van het dialoogvenster **Gerelateerde werkorder maken**.

![Figuur 1](media/03-work-orders.png)

>[!NOTE]
>Als u een masker voor verwante werkorders hebt ingesteld in **Parameters voor activabeheer** > **tabblad Werkorders** > veld **Verwante-werkordermasker**, worden werkorder-id's gemaakt op basis van de maskerinstellingen. Als er geen verwante-werkordermasker is ingesteld, wordt de volgende beschikbare werkorder-id gebruikt voor gerelateerde werkorders.

## <a name="copy-a-work-order"></a>Een werkorder kopiëren

U kunt snel een nieuwe werkorder maken op basis van een bestaande werkorder. Deze manier van werken met werkorders verschilt van het maken van werkorders op basis van [onderhoudsplannen](../preventive-and-reactive-maintenance/maintenance-plans.md). Het is bijvoorbeeld handig als een werkorder veel werkordertaken bevat en de verschillende taken voor verschillende activa regelmatig moeten worden voltooid.

1. Selecteer **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.

2. Selecteer de werkorder waaruit u inhoud wilt kopiëren.

3. Selecteer in het actievenster > tabblad **Werkorder** > groep **Nieuw** **Gerelateerde werkorder**.

4. De werkorderinstellingen van de geselecteerde werkorder worden weergegeven. U kunt zo nodig enkele velden bewerken.

5. Selecteer **OK** om de nieuwe werkorder te maken.

6. Op de lijstpagina **Alle werkorders** kunt u de werkorder naar wens bewerken.

>[!NOTE]
>Wanneer de nieuwe werkorder wordt gemaakt, worden bepaalde gegevens rechtstreeks uit de bestaande werkorder gekopieerd. Informatie over prognoses, hulpmiddelen, onderhoudscontrolelijsten, functionele locatie, adressen en planning wordt niet gekopieerd. Deze gegevens worden geïnitialiseerd vanuit de huidige instellingen in Activabeheer. Als deze informatie is gewijzigd tussen het tijdstip waarop de eerste werkorder is gemaakt en de tijd waarop u een kopie van de werkorder hebt gemaakt, worden de wijzigingen ook opgenomen in de nieuwe werkorder. Voorbeelden zijn wijzigingen in prognoses of updates voor onderhoudscontrolelijsten.

In de onderstaande afbeelding ziet u een voorbeeld van het dialoogvenster **Werkorder kopiëren**.

![Figuur 2](media/04-work-orders.png)


## <a name="create-a-work-order-based-on-a-maintenance-request"></a>Een werkorder maken op basis van een onderhoudsverzoek

1. Selecteer **Activabeheer** > **Algemeen** > **Onderhoudsverzoeken** > **Alle onderhoudsverzoeken** of **Actieve onderhoudsverzoeken**.

2. Selecteer het onderhoudsverzoek waarvoor u een werkorder wilt maken en klik op **Bewerken**.

3. Selecteer in het actievenster > tabblad **Onderhoudsverzoek** > groep **Nieuw** **Werkorder**.

4. Stel in het dialoogvenster **Werkorder** de velden in. Als er een type onderhoudstaak is geselecteerd in het onderhoudsverzoek, kunt u indien nodig een ander type onderhoudstaak selecteren wanneer u de werkorder maakt.

5. Selecteer **OK**. Een bericht meldt u dat de verkooporder is gemaakt.

6. Als u wilt zien welke werkorders aan een onderhoudsverzoek zijn gekoppeld, selecteert u het onderhoudsverzoek in de lijstpagina **Alle onderhoudsverzoeken** of **Actieve onderhoudsverzoeken**. Selecteer vervolgens in het actievenster op het tabblad **Onderhoudsverzoek** in de groep **Weergeven** de optie **Werkorders**.


In de onderstaande afbeelding ziet u een voorbeeld van het dialoogvenster **Werkorder maken**.

![Figuur 3](media/05-work-orders.png)


>[!NOTE]
>Als u automatisch werkorders wil maken kunt u onderhoudsplantaken plannen of 'automatisch maken' instellen voor [onderhoudsplannen](../preventive-and-reactive-maintenance/maintenance-plans.md) of [onderhoudsronden](../preventive-and-reactive-maintenance/maintenance-rounds.md) voor een activum. Werkorders die zijn gemaakt op basis van onderhoudsverzoeken in de lijstpagina **Alle onderhoudsschema's**, hebben de typen onderhoudstaken die in de onderhoudsverzoeken zijn geselecteerd.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]