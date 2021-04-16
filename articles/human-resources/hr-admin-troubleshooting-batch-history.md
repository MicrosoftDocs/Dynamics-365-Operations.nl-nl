---
title: Prestaties optimaliseren met automatische opschoningstaken
description: In dit artikel wordt uitgelegd hoe u enkele prestatieproblemen met Microsoft Dynamics 365 Human Resources kunt oplossen door de batchtaakgeschiedenis op te schonen.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 0372833c11e0919fa03d57ea258e81a89ab9ff31
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803940"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a>Prestaties optimaliseren met taken met automatische opschoning

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Uitgifte**

Microsoft Dynamics 365 Human Resources kan prestatieproblemen ondervinden als de batchtaakgeschiedenis te groot wordt.

**Oorzaak**

Batchtaken die vaak worden uitgevoerd, kunnen leiden tot een onhoudbare groei van de batchtaakgeschiedenis. Dit kan prestatieproblemen veroorzaken. 

**Oplossing**

Plan een automatische taak om de batchtaakgeschiedenis op te schonen. Het is raadzaam de taak zo in te stellen dat deze wekelijks wordt uitgevoerd, maar mogelijk moet u het opschonen meer of minder vaak uitvoeren, afhankelijk van uw omgeving. De volgende procedure bevat de aanbevolen instellingen, maar u kunt deze wijzigen op basis van uw behoeften.

1. Selecteer in Human Resources de optie **Systeembeheer**.

2. Voer in de **Zoekbalk** de optie **Batchtaakgeschiedenis opschonen** in.

   ![Zoek naar opschonen van batchtaakgeschiedenis](media/talent-batch-history-cleanup-search-bar.png)

3. Geef in **Geschiedenislimiet (dagen)** **30** in.

   ![Stel de geschiedenislimiet op 30](media/talent-batch-history-cleanup-history-limit.png)

4. Selecteer **Uitvoeren op de achtergrond** en selecteer **Terugkeerpatroon**.

   ![Stel terugkeerpatroon in](media/talent-batch-history-cleanup-recurrence.png)

5. Geef onder **Terugkeerpatroon definiëren** de **Begindatum** en **Begintijd** op die moeten plaatsvinden tijdens buitenuren of het weekend en selecteer vervolgens **GEEN EINDDATUM**. 

   ![Definieer begindatum en -tijd van het terugkeerpatroon](media/talent-batch-history-cleanup-define-recurrence.png)

6. Selecteer onder **TERUGKEERPATROON** **Dagen** en stel **HERHALEN NA OPGEGEVEN INTERVAL** in op **7**.

   ![Opschonen instellen op wekelijks herhalen](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. Selecteer **OK**.

8. Wijzig indien nodig andere parameters onder **Uitvoeren op de achtergrond** en selecteer vervolgens **OK**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]