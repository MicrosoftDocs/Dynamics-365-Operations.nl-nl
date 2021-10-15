---
title: Selectiecriteria voor verkoopprijs maken
description: Deze procedure laat zien hoe u een selectiecriterium voor de verkoopprijs maakt voor op kenmerk gebaseerde verkoopprijsmodellen.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ed7083f289948033782f74dd9ed1b3c2d2a73aea
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568442"
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