---
title: Groepen met consolidatierekeningen en aanvullende consolidatierekeningen
description: In dit onderwerp wordt informatie gegeven over groepen met consolidatierekeningen en aanvullende consolidatierekeningen en wordt uitgelegd hoe deze worden gebruikt in Microsoft Dynamics 365 for Operations.
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 72aba47eeaab8c049016c560a9543dd2476308df
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a>Groepen met consolidatierekeningen en aanvullende consolidatierekeningen

[!include[banner](../includes/banner.md)]


In dit onderwerp wordt informatie gegeven over groepen met consolidatierekeningen en aanvullende consolidatierekeningen en wordt uitgelegd hoe deze worden gebruikt in Microsoft Dynamics 365 for Operations.

<a name="consolidation-account-groups"></a>Groepen met consolidatierekeningen
----------------------------

Met groepen consolidatierekeningen kunt u groepen maken van de rekeningen die u wilt gebruiken om gegevens te consolideren. Meestal wordt met een groep consolidatierekeningen een door de overheid voorgeschreven rekeningschema vertegenwoordigd of worden rekeningen aan een groep toegewezen die door het hoofdkantoor van het bedrijf is gedefinieerd. U vindt groepen consolidatierekeningen in het gebied **Instellen** van de module **Consolidaties**. Wanneer u een nieuwe groep toevoegt, voert u een unieke ID en een naam in voor de rekeninggroep.

## <a name="additional-consolidation-accounts"></a>Aanvullende consolidatiebedragen
Met aanvullende consolidatierekeningen kunt u een rekening vanuit een bestaand rekeningschema toewijzen aan een groep consolidatierekeningen. U kunt vervolgens een waarde en naam voor de consolidatierekening opgeven. 

U vindt aanvullende consolidatierekeningen in het gebied **Instellen** van de module **Consolidaties**. Wanneer u een nieuwe consolidatierekening maakt, moet u de volgende gegevens opgeven:

-   **Hoofdrekening** : dit veld is een zoekveld waarin de belangrijkste rekeningen worden weergegeven die zijn gebaseerd op het rekeningschema dat u hebt geselecteerd op de pagina. Wanneer u een rekening selecteert, wordt de naam automatisch ingevoerd in het veld **Naam hoofdrekening**.
-   **Groep met consolidatierekeningen** : met dit veld kunt u de groep opgeven waaraan u de rekening wilt toewijzen. Als u op twee verschillende manieren consolideert, moet u dezelfde rekening toevoegen aan alle vier de groepen consolidatierekeningen.
-   **Consolidatierekening**: voer de waarde van de consolidatierekening in. Deze waarde hoeft geen rekening van een rekeningschema te zijn. Het kan een waarde zijn die u nodig hebt.
-   **Naam van consolidatierekening**: voer de naam van de rekening in als u wilt dat deze in query´s en rapporten verschijnt.
-   **SAT-niveau**: dit veld wordt gebruikt voor aangifte van rekeningoverzichten bij de Mexicaanse belastingdienst. 

Wanneer u de groepen consolidatierekeningen en aanvullende consolidatierekeningen hebt gemaakt, kunt u de groep selecteren in het online proces Consolideren.





