---
title: Een hoofdplanningstaak annuleren
description: In dit onderwerp wordt uitgelegd hoe u een actieve planningstaak kunt annuleren die gebruikmaakt van ingebouwde planningsfunctionaliteit.
author: ChristianRytt
manager: tfehr
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace, ReqProcessList
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 40d657a02df0cba66918a6853ec62621501cfdfe
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989788"
---
# <a name="cancel-a-master-planning-job"></a>Een hoofdplanningstaak annuleren

[!include [banner](../includes/banner.md)]

In Microsoft Dynamics 365 Supply Chain Management zijn er meerdere opties voor het annuleren van een hoofdplanningstaak. U kunt bijvoorbeeld een hoofdplanningstaak annuleren als deze per ongeluk is gestart of langer duurt dan verwacht en u deze wilt beëindigen. U kunt een planningstaak het beste annuleren via de de pagina **Onvoltooide planningsprocessen**. Alternatieve opties op de pagina's **Batchtaken** en **Verbeterde batchtaken** mogen alleen worden gebruikt als het annuleren van de hoofdplanningstaak via de pagina **Onvoltooide planningsprocessen** niet binnen enkele minuten is voltooid.

## <a name="preferred-cancel-option"></a>Voorkeursoptie voor annuleren
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a>Hoofdplanningstaak annuleren via de de pagina **Onvoltooide planningsprocessen**
1. Ga naar **Hoofdplanning > Query's en rapporten > Hoofdplanning > Onvoltooide planningsprocessen**.
2. Selecteer de regel met het planningsproces dat u wilt annuleren.
3. Klik op **Annuleren**.

## <a name="additional-cancel-options"></a>Overige annuleringsopties
Deze moeten alleen worden gebruikt als het annuleren van de hoofdplanningstaak via de pagina **Onvoltooide planningsprocessen** niet binnen enkele minuten is voltooid.

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a>Hoofdplanningstaak verwijderen via de pagina **Batchtaken**
1. Ga naar **Systeembeheer > Query's > Batchtaken**.
2. Selecteer de regel met de planningstaak die u wilt verwijderen.
3. Klik op **Verwijderen**.

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a>Hoofdplanningstaak afbreken via de pagina **Verbeterde batchtaken**
1. Ga naar **Systeembeheer > Query's > Batchtaken**.
2. Als de taak-id niet in de lijst wordt weergegeven, klikt u op **Overschakelen naar uitgebreid formulier** of gaat u verder met de volgende stap.
3. Open de batchtaak. Klik op de **taak-id** voor de batchtaak met taken die u wilt beëindigen.
4. Selecteer bij **Batchtaken** de taken die u wilt beëindigen.
5. Klik op **Status wijzigen**, kies **Annuleren** en klik op **OK**.
6. Klik op het sneltabblad **Batchtaken** op **Afbreken**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]