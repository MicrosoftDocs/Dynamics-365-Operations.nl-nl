---
title: Prestaties optimaliseren met taken met automatische opschoning
description: In dit onderwerp wordt uitgelegd hoe u enkele prestatie problemen met Microsoft Dynamics 365 Talent kunt oplossen door de batchtaakgeschiedenis op te schonen.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: a053c9094151f4e12e4aadc533dd272258779540
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832577"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a>Prestaties optimaliseren met taken met automatische opschoning

[!include [banner](includes/banner.md)]

**Uitgifte**

Microsoft Dynamics 365 Talent kan prestatieproblemen ondervinden als de batchtaakgeschiedenis te groot wordt.

**Oorzaak**

Batchtaken die vaak worden uitgevoerd, kunnen leiden tot een onhoudbare groei van de batchtaakgeschiedenis. Dit kan prestatieproblemen veroorzaken. 

**Oplossing**

Plan een automatische taak om de batchtaakgeschiedenis op te schonen. Het is raadzaam de taak zo in te stellen dat deze wekelijks wordt uitgevoerd, maar mogelijk moet u het opschonen meer of minder vaak uitvoeren, afhankelijk van uw omgeving. De volgende procedure bevat de aanbevolen instellingen, maar u kunt deze wijzigen op basis van uw behoeften.

1. Selecteer **Systeembeheer**in Talent.

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

