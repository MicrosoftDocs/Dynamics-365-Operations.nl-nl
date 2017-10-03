--- 
title: Selectiecriteria voor verkoopprijs maken
description: Deze procedure laat zien hoe u een selectiecriterium voor de verkoopprijs maakt voor op kenmerk gebaseerde verkoopprijsmodellen.
author: YuyuScheller
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 633628e6250baa74df544e814ce6e9656a2f0b06
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="create-sales-price-selection-criteria"></a>Selectiecriteria voor verkoopprijs maken

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u een selectiecriterium voor de verkoopprijs maakt voor op kenmerk gebaseerde verkoopprijsmodellen. Deze procedure vereist dat er ten minste één verkoopprijsmodel beschikbaar is. Dit voorbeeld gebruikt het verkoopprijsmodel van de luidsprekeroplossing in het USMF-bedrijf met demogegevens. Gewoonlijk gebruikt een productmanager deze procedure.


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>Voeg een nieuw criterium voor een bestaand verkoopprijsmodel toe
1. Klik op Definitie van productvariantmodel.
2. Klik op Productconfiguratiemodellen.
3. Selecteer in de lijst de rij voor het productmodel van de luidsprekeroplossing, maar klik niet op de koppeling voor de modelnaam.
4. Klik in het actievenster op Model.
5. Klik op Criteria voor prijsmodel.
6. Klik op Nieuw.
7. Typ Klantengroep 10 in het veld Naam.
    * De naam van het criterium prijsmodel wordt gebruikt om de onderliggende selectiecriteria te identificeren.  
8. Typ of selecteer een waarde in het veld Prijsmodel.
9. Selecteer Verkooporder in het veld Ordertype.
    * Het ordertype bepaalt de databasevelden die voor de selectiequery beschikbaar zijn.  
10. Typ een datum in het veld Geldig vanaf.
11. Typ een datum in het veld Vervallen op.
12. Klik op Opslaan.

## <a name="create-the-query-for-the-selection-criteria"></a>Maak de query voor de selectiecriteria
1. Klik op Bewerken.
2. Selecteer Klanten in het veld Tabel. 
3. Selecteer Klantengroep in het veld Veld.
    * In dit voorbeeld wordt een specifieke klantengroep voor de selectiecriteria gebruikt.  
4. Selecteer Klantengroep 10 in het veld Criteria. 
5. Klik op OK.

