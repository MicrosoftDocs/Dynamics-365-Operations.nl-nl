---
title: Configureren en uitvoeren van taak om overzichten te boeken
description: Deze procedure doorloopt de configuratie en uitvoering van een terugkerende batchtaak om overzichten te boeken voor een geselecteerde winkel of groep winkels.
author: josaw1
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a24014f7e1b925e0fdb20b91bcc9594feb8f4c5c
ms.sourcegitcommit: fc40279d0e56f8a43c601bca6265fdde4c8c4c7e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/29/2019
ms.locfileid: "1792243"
---
# <a name="configure-and-run-job-to-post-statements"></a>Configureren en uitvoeren van taak om overzichten te boeken

[!include[task guide banner](../includes/task-guide-banner.md)]

Deze procedure doorloopt de configuratie en uitvoering van een terugkerende batchtaak om overzichten te boeken voor een geselecteerde winkel of groep winkels. Deze procedure gebruikt het demobedrijf USRT.

1. Ga naar Alle werkgebieden > .. > Financiën van detailhandelwinkel.
2. Klik op Overzichten in batch boeken.
    * Selecteer een organisatiehiërarchie en selecteer vervolgens in de structuur van organisatieknooppunten een individuele winkel of een knooppunt. Selecteer een knooppunt als u de batchtaak wilt maken voor een groep winkels.  
    * Klik op de pijl om uw selectie toe te voegen.  
3. Klik op het tabblad Uitvoeren op de achtergrond. ![Uitvoeren op de achtergrond](../dev-itpro/media/runbackground.png "Uitvoeren op de achtergrond") 
4. Schakel het selectievakje Batchverwerking in of uit.
![Batchverwerking](../dev-itpro/media/batchprocessing.png "Batchverwerking en Terugkeerpatroon") 
5. Klik op Terugkeerpatroon.
6. Voer een datum in het veld Startdatum in.
7. Voer een tijd in het veld Begintijd in.
    * Kies of u de herhaling wilt beëindigen na een bepaald aantal uitvoeringen, op een specifieke datum of nooit. Kies vervolgens de verschillende opties om te bepalen hoe vaak u de taak wilt uitvoeren.  
8. Klik op OK.
9. Klik op OK.

