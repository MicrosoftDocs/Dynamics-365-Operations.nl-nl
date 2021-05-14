---
title: Op kenmerken gebaseerde prijzen instellen voor configureerbare producten
description: In dit onderwerp wordt uitgelegd hoe u op kenmerken gebaseerde prijsdetails instelt.
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0c30c520e7265c2676937f5191844f6789c364e6
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921236"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>Op kenmerken gebaseerde prijzen instellen voor configureerbare producten

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u op kenmerken gebaseerde prijsdetails instelt. Als eerste vereiste moet u een productconfiguratiemodel hebben dat een of meerdere onderdelen en kenmerken heeft. In dit voorbeeld wordt het model Geavanceerde luidspreker gebruikt in het demobedrijf USMF. Gewoonlijk gebruikt een productmanager deze procedure.


## <a name="create-a-new-price-model"></a>Eem nieuw prijsmodel maken

1. Ga naar **Productgegevensbeheer \> Producten \> Productconfiguratiemodellen**.
1. In de lijst selecteert u de regel **Geavanceerde luidspreker**, maar selecteert u niet de koppeling voor de naam.
1. Selecteer **Model** in het actievenster.
1. Selecteer **Prijsmodellen**.
1. Selecteer **Nieuw**.
1. Typ een waarde in het veld **Naam prijsmodel**. Gebruik een naam waaraan u het model gemakkelijk kunt herkennen.  
1. Typ een waarde in het veld **Beschrijving**.
1. Selecteer **Opslaan**.

## <a name="add-price-elements"></a>Prijselementen toevoegen

1. Selecteer **Bewerken**. Elke component in een productmodel kan een element van de basisprijs en elk gewenst aantal prijsexpressieregels hebben. U kunt ook prijzen in andere valuta toevoegen.  
2. Typ een waarde in het veld **Basisprijsexpressie**. Typ bijvoorbeeld 100. Een expressie van de basisprijs kan een numerieke waarde zijn of bestaan uit een rekenkundige berekening die een of meer kenmerken bevat.  
3. Selecteer **Toevoegen**.
4. Typ in het veld **Naam** `Rosewood`. De naam van de prijsexpressie helpt bij het herkennen waarvoor het prijselement staat. In dit voorbeeld wordt een prijselement gemaakt voor de rozenhouten afwerking van de luidsprekerkast.  
5. Selecteer **Voorwaarde bewerken**. Een prijsvoorwaarde zorgt ervoor dat een element van de prijsexpressie alleen in de verkoopprijs wordt opgenomen als een specifieke combinatie van kenmerken aanwezig is.  
6. In het veld **ConstraintBody** voert u `CabinetFinish=="Rosewood"` in.
7. Selecteer **OK**.
8. Typ een waarde in het veld **Expressie**. Typ bijvoorbeeld `50`. 
9. Sluit de pagina.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]