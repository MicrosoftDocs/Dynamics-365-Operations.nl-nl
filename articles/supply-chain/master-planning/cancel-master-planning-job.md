---
title: Een taak annuleren die is gemaakt met de verouderde hoofdplanningsengine
description: In dit artikel wordt uitgelegd hoe u een actieve planningstaak kunt annuleren die gebruikmaakt van de afgeschafte hoofdplanningsengine.
author: t-benebo
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace, ReqProcessList
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7b71a43f407050dccb7550db7c4b6a98a596d589
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740872"
---
# <a name="cancel-a-job-that-was-created-using-the-deprecated-master-planning-engine"></a>Een taak annuleren die is gemaakt met de verouderde hoofdplanningsengine

[!include [banner](../includes/banner.md)]

Er zijn meerdere opties voor het annuleren van een taak die is gemaakt met de afgeschafte hoofdplanningsengine. U kunt bijvoorbeeld een hoofdplanningstaak annuleren als deze per ongeluk is gestart of langer duurt dan verwacht en u deze wilt beëindigen.

U kunt een planningstaak het beste annuleren via de de pagina **Onvoltooide planningsprocessen**. Alternatieve opties op de pagina's **Batchtaken** en **Verbeterde batchtaken** mogen alleen worden gebruikt als het annuleren van de hoofdplanningstaak via de pagina **Onvoltooide planningsprocessen** niet binnen enkele minuten is voltooid.

## <a name="preferred-cancel-option"></a>Voorkeursoptie voor annuleren

### <a name="cancel-master-planning-job-from-the-unfinished-planning-processes-page"></a>Hoofdplanningstaak annuleren via de de pagina Onvoltooide planningsprocessen

1. Ga naar **Hoofdplanning > Query's en rapporten > Hoofdplanning > Onvoltooide planningsprocessen**.
2. Selecteer de regel met het planningsproces dat u wilt annuleren.
3. Selecteer **Annuleren**.

## <a name="additional-cancel-options"></a>Overige annuleringsopties

Deze moeten alleen worden gebruikt als het annuleren van de hoofdplanningstaak via de pagina **Onvoltooide planningsprocessen** niet binnen enkele minuten is voltooid.

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a>Hoofdplanningstaak verwijderen via de pagina **Batchtaken**

1. Ga naar **Systeembeheer > Query's > Batchtaken**.
2. Selecteer de regel met de planningstaak die u wilt verwijderen.
3. Selecteer **Verwijderen**.

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a>Hoofdplanningstaak afbreken via de pagina **Verbeterde batchtaken**

1. Ga naar **Systeembeheer > Query's > Batchtaken**.
2. Als de taak-id niet in de lijst wordt weergegeven, klikt u op **Overschakelen naar uitgebreid formulier** of gaat u verder met de volgende stap.
3. Open de batchtaak. Selecteer de **taak-id** voor de batchtaak met taken die u wilt beëindigen.
4. Selecteer bij **Batchtaken** de taken die u wilt beëindigen.
5. Selecteer **Status wijzigen**, kies **Annuleren** en klik op **OK**.
6. Klik op het sneltabblad **Batchtaken** op **Afbreken**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]