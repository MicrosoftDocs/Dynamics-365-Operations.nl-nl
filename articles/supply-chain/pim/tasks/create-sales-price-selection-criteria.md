---
title: Selectiecriteria voor verkoopprijs maken
description: Deze procedure laat zien hoe u een selectiecriterium voor de verkoopprijs maakt voor op kenmerk gebaseerde verkoopprijsmodellen.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 69d22c3321beaa2667ee20bff00acd746714b993
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920526"
---
# <a name="create-sales-price-selection-criteria"></a>Selectiecriteria voor verkoopprijs maken

[!include [banner](../../includes/banner.md)]

Deze procedure laat zien hoe u een selectiecriterium voor de verkoopprijs maakt voor op kenmerk gebaseerde verkoopprijsmodellen. Deze procedure vereist dat er ten minste één verkoopprijsmodel beschikbaar is. Dit voorbeeld gebruikt het verkoopprijsmodel van de luidsprekeroplossing in het USMF-bedrijf met demogegevens. Gewoonlijk gebruikt een productmanager deze procedure.

## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>Voeg een nieuw criterium voor een bestaand verkoopprijsmodel toe

1. Ga naar **Productgegevensbeheer \> Producten \> Productconfiguratiemodellen**.
1. Selecteer in de lijst de rij voor het productmodel van de luidsprekeroplossing, maar selecteer niet de koppeling voor de modelnaam.
1. Selecteer **Model** in het actievenster.
1. Selecteer **Criteria voor prijsmodel**.
1. Selecteer **Nieuw**.
1. Typ 'Klantengroep 10' in het veld **Naam**.
    * De naam van het criterium prijsmodel wordt gebruikt om de onderliggende selectiecriteria te identificeren.  
1. Typ of selecteer een waarde in het veld **Prijsmodel**.
1. Selecteer *Verkooporder* in het veld **Ordertype**.
    * Het ordertype bepaalt de databasevelden die voor de selectiequery beschikbaar zijn.  
1. Typ een datum in het veld **Geldig vanaf**.
1. Typ een datum in het veld **Vervallen op**.
1. Selecteer **Opslaan**.

## <a name="create-the-query-for-the-selection-criteria"></a>Maak de query voor de selectiecriteria

1. Selecteer **Bewerken**.
2. Selecteer **Klanten** in het veld *Tabel*.
3. Selecteer **Klantengroep** in het veld *Veld*.
    * In dit voorbeeld wordt een specifieke klantengroep voor de selectiecriteria gebruikt.  
4. Selecteer **Klantengroep 10** in het veld *Criteria*.
5. Selecteer **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]