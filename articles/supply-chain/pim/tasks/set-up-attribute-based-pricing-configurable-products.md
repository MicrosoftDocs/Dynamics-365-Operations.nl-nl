---
title: Op kenmerken gebaseerde prijzen instellen voor configureerbare producten
description: In dit onderwerp wordt uitgelegd hoe u op kenmerken gebaseerde prijsdetails instelt.
author: ShylaThompson
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 534e9c9332c107afebd814cf2090ecbdf0ec6459
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914694"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>Op kenmerken gebaseerde prijzen instellen voor configureerbare producten

[!include [task guide banner](../../includes/task-guide-banner.md)]

In dit onderwerp wordt uitgelegd hoe u op kenmerken gebaseerde prijsdetails instelt. Als eerste vereiste moet u een productconfiguratiemodel hebben dat een of meerdere onderdelen en kenmerken heeft. In dit voorbeeld wordt het model Geavanceerde luidspreker gebruikt in het demobedrijf USMF. Gewoonlijk gebruikt een productmanager deze procedure.


## <a name="create-a-new-price-model"></a>Eem nieuw prijsmodel maken
1. Selecteer **Definitie van productvariantmodel** op de startpagina.
2. Selecteer **Productconfiguratiemodellen** in de sectie **koppelingen**.
3. In de lijst selecteert u de regel **Geavanceerde luidspreker**, maar selecteert u niet de koppeling voor de naam.
4. Selecteer **Model** in het actievenster.
5. Selecteer **Prijsmodellen**.
6. Selecteer **Nieuw**.
7. Typ een waarde in het veld **Naam prijsmodel**. Gebruik een naam waaraan u het model gemakkelijk kunt herkennen.  
8. Typ een waarde in het veld **Beschrijving**.
9. Selecteer **Opslaan**.

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

