---
title: Schakelen tussen leveranciersontwerpen
description: ''
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 4e97ff0b0e6195b5e3703e15a0bb0de7644ef8d1
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772359"
---
# <a name="switch-between-vendor-designs"></a>Schakelen tussen leveranciersontwerpen

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a>Leveranciersgegevensstroom 

Als u andere Dynamics 365-apps wilt gebruiken voor leveranciersbeheer en u leveranciergegevens wilt isoleren van klanten, kunt u dit elementaire leveranciersontwerp gebruiken.  

![Basisleveranciersstroom](media/dual-write-switch-1.png)
 
Als u andere Dynamics 365-apps wilt gebruiken voor leveranciersbeheer en u de entiteit **Account** wilt blijven gebruiken voor het opslaan van leveranciergegevens, kunt u dit uitgebreide leveranciersontwerp gebruiken. In dit ontwerp wordt uitgebreide leveranciersinformatie, zoals de status in wachtstand voor leveranciers en het leveranciersprofiel opgeslagen in de entiteit **leveranciers** in Common Data Service. 

![Uitgebreide leveranciersstroom](media/dual-write-switch-2.png)
 
Volg de onderstaande stappen om het uitgebreide leveranciersontwerp te gebruiken: 
 
1. Het oplossingspakket **SupplyChainCommon** bevat de sjablonen voor het workflowproces zoals wordt weergegeven in de volgende afbeelding.
    > [!div class="mx-imgBorder"]
    > ![Workflowprocessjablonen](media/dual-write-switch-3.png)
2. Maak nieuwe workflowprocessen met de workflowprocessjablonen: 
    1. Maak een nieuw workflowproces voor de entiteit **Leverancier** met de workflowprocessjabloon **Leveranciers maken in entiteit Account** en klik op **OK**. Deze workflow verwerkt het scenario voor het maken van de entiteit **Account**.
        > [!div class="mx-imgBorder"]
        > ![Leveranciers maken in entiteit Account](media/dual-write-switch-4.png)
    2. Maak een nieuw workflowproces voor de entiteit **Leverancier** met de workflowprocessjabloon **Entiteit Accounts bijwerken** en klik op **OK**. Deze workflow verwerkt het scenario voor het bijwerken van de entiteit **Account**. 
        > [!div class="mx-imgBorder"]
        > ![Entiteit Accounts bijwerken](media/dual-write-switch-5.png)
    3. Nieuwe workflowprocessen maken op basis van de sjablonen die zijn gemaakt voor de entiteit **Accounts**. 
        > [!div class="mx-imgBorder"]
        > ![Leveranciers maken in entiteit Leveranciers](media/dual-write-switch-6.png)
        > [!div class="mx-imgBorder"]
        > ![Entiteit Leveranciers bijwerken](media/dual-write-switch-7.png)
    4. U kunt de workflows configureren als realtime workflows of workflows op de achtergrond op basis van uw vereisten. 
        > [!div class="mx-imgBorder"]
        > ![Converteren naar een workflow op de achtergrond](media/dual-write-switch-8.png)
    5. Activeer de workflows die u hebt gemaakt voor de entiteiten **Account** en **Leverancier** om te beginnen met het gebruiken van de entiteit **Account** van Customer Engagement voor het opslaan van leveranciersgegevens. 
 
