---
title: Groepen met consolidatierekeningen en extra consolidatierekeningen
description: In dit onderwerp bevat informatie over groepen met consolidatierekeningen en extra consolidatierekeningen en wordt uitgelegd hoe ze worden gebruikt in Microsoft Dynamics 365 voor bewerkingen.
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: f9c5aaa389c9c2f85d1ab91cbf3d2222cbebef55
ms.lasthandoff: 03/31/2017


---

# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a>Groepen met consolidatierekeningen en extra consolidatierekeningen

In dit onderwerp bevat informatie over groepen met consolidatierekeningen en extra consolidatierekeningen en wordt uitgelegd hoe ze worden gebruikt in Microsoft Dynamics 365 voor bewerkingen.

<a name="consolidation-account-groups"></a>Groepen met consolidatierekeningen
----------------------------

Groepen met consolidatierekeningen kunnen u groepen van de rekeningen die u gebruiken wilt voor het consolideren van gegevens maken. De meeste gevallen een groep consolidatierekeningen vertegenwoordigt een rekeningschema overheid voorgeschreven of rekeningen wordt toegewezen aan een groep die wordt gedefinieerd door het hoofdkantoor van het bedrijf. U vindt consolidatie boekingsgroepen in de **Setup** gebied van de **consolidaties** module. Wanneer u een nieuwe groep toevoegt, kunt u een unieke identificatie invoeren voor de groep en een naam.

## <a name="additional-consolidation-accounts"></a>Aanvullende consolidatiebedragen
Aanvullende consolidatierekeningen kunnen u een rekening uit een bestaande rekeningschema toewijzen aan een groep consolidatierekeningen. U kunt vervolgens een waarde voor consolidatie van de rekening en een naam opgeven. 

U vindt extra consolidatierekeningen in de **Setup** gebied van de **consolidaties** module. Wanneer u een nieuwe consolidatierekening maakt, moet u de volgende gegevens opgeven:

-   **Hoofdrekening** : dit veld is een lookup waarop de belangrijkste accounts die zijn gebaseerd op de rekeningschema's die u hebt geselecteerd op de pagina. Wanneer u een rekening, de naam wordt automatisch ingevoerd in de **hoofdtabel rekeningnaam** veld.
-   **Groep met consolidatierekeningen** : met dit veld kunt u de groep voor het toewijzen van de rekening die u wilt opgeven. Als u op twee verschillende manieren samenvoegt, moet u dezelfde rekening toevoegen aan alle groepen met consolidatierekeningen vier.
-   **Consolidatierekening** : de waarde van de consolidatierekening invoeren. Deze waarde hoeft te zijn van een rekening in een rekeningschema. Dit is een waarde die u nodig hebt.
-   **Naam van consolidatierekening** : de naam van de rekening invoeren als u wilt weergeven in query's en rapporten.
-   **SAT niveau** : dit veld wordt gebruikt voor aangifte van rekeningoverzichten aan de Mexicaanse overheid. 

Wanneer u klaar bent met het maken van de groepen met consolidatierekeningen en extra consolidatierekeningen, selecteert u de groep in het on line proces consolideren.



