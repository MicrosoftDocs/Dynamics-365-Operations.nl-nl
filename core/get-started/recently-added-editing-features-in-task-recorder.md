---
title: Recentelijk toegevoegde functies in Taakregistratie
description: "Als u met Taakregistratie taak handleidingen maakt, kunt u uw bestanden meer efficiënt gebruik maakt van de functionaliteit die wordt beschreven in deze wiki."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Core
ms.custom: 266464
ms.assetid: b4640e67-4b92-4855-8041-1bfc71aadc47
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: c4f9ac515eab6ed8b194fc8985f6d3fae40ced38
ms.lasthandoff: 03/31/2017


---

# <a name="recently-added-editing-features-in-task-recorder"></a>Recentelijk toegevoegde functies in Taakregistratie

Als u met Taakregistratie taak handleidingen maakt, kunt u uw bestanden meer efficiënt gebruik maakt van de functionaliteit die wordt beschreven in deze wiki.

Deze functies zijn beschikbaar op de **instellingen &gt;Taakregistratie &gt;registratie bewerken** menu.

-   Stap invoegen zonder het gehele bestand opnieuw te registreren.
-   Verplaats stappen onder een subtaak zonder het gehele bestand opnieuw te registreren.
-   De velden naam en beschrijving opname samenvouwen.

## <a name="insert-steps-without-rerecording-the-entire-file"></a>Stap invoegen zonder het hele bestand rerecording
U kunt nu een stap toevoegen ergens in de handleiding van een taak zonder afspelen of opnemen van het gehele bestand opnieuw.

1.  Selecteer de stap die u wilt dat de nieuwe stap moet worden ingevoegd. Controleer of dat de stap is gemarkeerd.

In de volgorde voor taakregistratie een stap invoegen, moet u de juiste pagina openen hebben. De juiste pagina wordt de pagina waarop de nieuwe stap plaatsvindt. Taakregistratie is een mechanisme waarmee wordt bepaald wat de actieve pagina is en de functionaliteit wordt uitgeschakeld als de juiste pagina niet geopend is. 

[![tg1](./media/tg1.png)](./media/tg1.png) 


Wanneer u op de juiste pagina bent **invoegen stap** beschikbaar.

[![tg2](./media/tg2-231x300.png)](./media/tg2.png)

2. Klik op **invoegen stap**.

Wanneer u klikt op **invoegen stap**, Taakregistratie schakelt over naar record-modus. Elke actie uit die in de gebruikersinterface wordt nu geregistreerd en interne toegevoegd als stappen.

3. Klik op **stoppen**.

U kunt het proces herhalen zo veel stappen toevoegen of verplaatsen van alle subtaken zo nodig (Zie hieronder voor subtaken).

4. Als u klaar bent de handleiding van de taak bewerkt, klikt u op **gedaan met het bewerken van**, en kies vervolgens een van de opties die u wilt opslaan of publiceren van de handleiding van de taak.

## <a name="move-steps-under-a-subtask-without-rerecording-the-entire-file"></a>Verplaats stappen onder een subtaak zonder het hele bestand rerecording
U kunt de stappen onder een subtaak verplaatsen zonder afspelen of het gehele bestand opnieuw te registreren. U kunt ook de subtaak stap of de stap van de subtaak einde verplaatsen als u wilt groeperen van een bestaande blok van stappen.

1.  Selecteer de stap of subtaak stap die u wilt verplaatsen. Zorg ervoor dat de stap is geselecteerd.
2.  Klik op de ellips en klik vervolgens op **verplaatsen na stap**.

[![tg3](./media/tg3.png)](./media/tg3.png)

3. Selecteer de stap of subtaak stap die u wilt verplaatsen van de stap voor stap of subtaak na. Taakregistratie wordt de stap verplaatst.

4. De stap van de subtaak einde verplaatsen, selecteert u deze, klik op de ellips, **verplaatsen na stap**, en selecteer vervolgens de stap waarna u wilt dat de stap einde subtaak moet worden.

Desgewenst kunt u de eerste stap in de handleiding van de taak in een subtaak maken van een subtaak stap als tweede stap en verplaats vervolgens de eerste stap in deze. U kunt toevoegen of verplaatsen van zo veel stappen of subtaken zo nodig.

5. Als u klaar bent de handleiding van de taak bewerkt, klikt u op **gedaan met het bewerken van**, en kies vervolgens een van de opties die u wilt opslaan of publiceren van de handleiding van de taak.

## <a name="collapse-recording-name-and-description"></a>Samenvouwen opname naam en beschrijving
U kunt uitvouwen en samenvouwen de **opname naam** en **omschrijving vastleggen** velden. Als deze velden zijn samengevouwen, is meer stappen worden weergegeven in het deelvenster bewerken Taakregistratie. 

[![tg4](./media/tg4-300x252.png)](./media/tg4.png)  

<a name="see-also"></a>Zie ook
--------

[Documentatie of trainingen maken met Taakregistraties](/dynamics365/operations/dev-itpro/user-interface/task-recorder)

[Taak recorder-beknopte naslaginformatie](/dynamics365/operations/dev-itpro/user-interface/task-recorder-quick-reference)


