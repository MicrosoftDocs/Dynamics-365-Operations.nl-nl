---
title: Selectiecriteria voor verkoopprijs maken
description: Deze procedure laat zien hoe u een selectiecriterium voor de verkoopprijs maakt voor op kenmerk gebaseerde verkoopprijsmodellen.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed8c60b188b7c7090546e8367455e0f58ce9359b
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147682"
---
# <a name="create-sales-price-selection-criteria"></a>Selectiecriteria voor verkoopprijs maken

[!include [banner](../../includes/banner.md)]

Deze procedure laat zien hoe u een selectiecriterium voor de verkoopprijs maakt voor op kenmerk gebaseerde verkoopprijsmodellen. Deze procedure vereist dat er ten minste één verkoopprijsmodel beschikbaar is. Dit voorbeeld gebruikt het verkoopprijsmodel van de luidsprekeroplossing in het USMF-bedrijf met demogegevens. Gewoonlijk gebruikt een productmanager deze procedure.


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>Voeg een nieuw criterium voor een bestaand verkoopprijsmodel toe
1. Klik op Definitie van productvariantmodel.
2. Klik op Productconfiguratiemodellen.
3. Selecteer in de lijst de rij voor het productmodel van de luidsprekeroplossing, maar klik niet op de koppeling voor de modelnaam.
4. Klik in het actievenster op Model.
5. Klik op Criteria voor prijsmodel.
6. Klik op Nieuw.
7. Typ 'Klantengroep 10' in het veld Naam.
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

