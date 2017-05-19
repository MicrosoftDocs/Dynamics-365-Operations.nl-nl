---
title: Recentelijk toegevoegde functies in Taakrecorder
description: "Als u met Taakrecorder taakbegeleidingen maakt, kunt u uw bestanden efficiënter gebruiken door middel van de functionaliteit die wordt beschreven in dit onderwerp."
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 3be54879494948f75b192fcc22239b9064173220
ms.contentlocale: nl-nl
ms.lasthandoff: 04/25/2017


---

# <a name="recently-added-editing-features-in-task-recorder"></a>Recentelijk toegevoegde functies in Taakrecorder

[!include[banner](../includes/banner.md)]


Als u met Taakrecorder taakbegeleidingen maakt, kunt u uw bestanden efficiënter gebruiken door middel van de functionaliteit die wordt beschreven in dit onderwerp.

Deze functies zijn beschikbaar in het menu **Instellingen &gt; Taakrecorder &gt; Opname bewerken**.

-   Stappen invoegen zonder het gehele bestand opnieuw op te nemen
-   Stappen onder een subtaak plaatsen zonder het gehele bestand opnieuw op te nemen
-   De velden Naam van opname en Omschrijving van opname samenvouwen

## <a name="insert-steps-without-rerecording-the-entire-file"></a>Stappen invoegen zonder het gehele bestand opnieuw op te nemen
U kunt nu een stap overal in de taakbegeleiding toevoegen, zonder het bestand af te spelen of opnieuw op te nemen.

1.  Selecteer de stap waarna u de nieuwe stap wilt invoegen. Let erop dat de stap is gemarkeerd.

Om de taakrecorder een stap te laten invoegen, moet u de juiste pagina hebben geopend. De juiste pagina is de pagina waarop de nieuwe stap wordt uitgevoerd. Taakrecorder heeft een mechanisme waarmee wordt bepaald wat de actieve pagina is en schakelt de functionaliteit uit als de juiste pagina niet geopend is. 

[![tg1](./media/tg1.png)](./media/tg1.png) 


Wanneer u op de juiste pagina bent, wordt de optie **Stap invoegen** beschikbaar.

[![tg2](./media/tg2-231x300.png)](./media/tg2.png)

2. Klik op **Stap invoegen**.

Als u klikt op **Stap invoegen** schakelt Taakrecorder over naar de opnamemodus. Alle acties die in de gebruikersinterface worden uitgevoerd, worden nu geregistreerd en op de gewenste plaats ingevoegd als stap.

3. Klik op **Stop**.

U kunt het proces herhalen en zoveel stappen toevoegen of subtaken verplaatsen als nodig is (zie hieronder voor subtaken).

4. Als u klaar bent met het bewerken van de taakbegeleiding, klikt u op **Klaar met bewerken**. Kies vervolgens een van de opties om de taakbegeleiding op te slaan of te publiceren.

## <a name="move-steps-under-a-subtask-without-rerecording-the-entire-file"></a>Stappen onder een subtaak plaatsen zonder het gehele bestand opnieuw op te nemen
U kunt stappen onder een subtaak plaatsen zonder het gehele bestand af te spelen of opnieuw op te nemen U kunt ook de subtaak-stap of de eindstap van de subtaak verplaatsen, als u een bestaand blok van stappen wilt groeperen.

1.  Selecteer de stap of subtaakstap die u wilt verplaatsen. Let erop dat de stap is gemarkeerd.
2.  Klik op het weglatingsteken (ellips) en vervolgens op **Stap verplaatsen na**.

[![tg3](./media/tg3.png)](./media/tg3.png)

3. Selecteer de stap of subtaak stap waar u de stap voor stap of subtaakstap achter wilt plaatsen. Taakrecorder verplaatst de stap.

4. Om de eindstap van de subtaak te verplaatsen, selecteert u deze. Klik op de ellips en op **Stap verplaatsen na** en selecteer vervolgens de stap waarna u de eindstap wilt plaatsen.

Als u de eerste stap in de taakbegeleiding in een subtaak wilt hebben, maakt u een subtaakstap als de tweede stap en verplaatst u de eerste stap naar de subtaak. U kunt zoveel stappen of subtaken toevoegen of verplaatsen als nodig.

5. Als u klaar bent met het bewerken van de taakbegeleiding, klikt u op **Klaar met bewerken**. Kies vervolgens een van de opties om de taakbegeleiding op te slaan of te publiceren.

## <a name="collapse-recording-name-and-description"></a>De velden Naam van opname en Omschrijving van opname samenvouwen
U kunt de velden **Naam van opname** en **Omschrijving van opname** uit- en samenvouwen. Als deze velden zijn samengevouwen, worden meer stappen weergegeven in het bewerkingsdeelvenster van de Taakrecorder. 

[![tg4](./media/tg4-300x252.png)](./media/tg4.png)  

<a name="see-also"></a>Zie ook
--------

[Documentatie of trainingen maken met Taakregistraties](/dynamics365/operations/dev-itpro/user-interface/task-recorder)

[Snelzoekgids voor de Taakrecorder](/dynamics365/operations/dev-itpro/user-interface/task-recorder-quick-reference)




