--- 
title: Op kenmerken gebaseerde prijzen instellen voor configureerbare producten
description: Deze procedure laat zien hoe u op kenmerken gebaseerde prijsdetails instelt.
author: BibiSp
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 473d01ecddfd58aa72a972ee901673534c9d7c9c
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>Op kenmerken gebaseerde prijzen instellen voor configureerbare producten

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u op kenmerken gebaseerde prijsdetails instelt. Als eerste vereiste moet u een productconfiguratiemodel hebben dat een of meerdere onderdelen en kenmerken heeft. In dit voorbeeld wordt het model Geavanceerde luidspreker gebruikt in het demobedrijf USMF. Gewoonlijk gebruikt een productmanager deze procedure.


## <a name="create-a-new-price-model"></a>Eem nieuw prijsmodel maken
1. Klik op Definitie van productvariantmodel.
2. Klik op Productconfiguratiemodellen.
3. In de lijst selecteert u de regel van de Geavanceerde luidspreker, maar klikt u niet op de koppeling voor de naam.
4. Klik in het actievenster op Model.
5. Klik op Prijsmodellen.
6. Klik op Nieuw.
7. Typ een waarde in het veld Prijsmodel.
    * Gebruik een naam waaraan u het model gemakkelijk kunt herkennen.  
8. Typ een waarde in het veld Omschrijving.
9. Klik op Opslaan.

## <a name="add-price-elements"></a>Prijselementen toevoegen
1. Klik op Bewerken.
    * Elke component in een productmodel kan een element van de basisprijs en elk gewenst aantal prijsexpressieregels hebben. U kunt ook prijzen in andere valuta toevoegen.  
2. Typ een waarde in het veld Basisprijsexpressie.
    * Typ bijvoorbeeld 100.   Een expressie van de basisprijs kan een numerieke waarde zijn of bestaan uit een rekenkundige berekening die een of meer kenmerken bevat.  
3. Klik op Toevoegen.
4. Typ Rozenhouten in het veld Naam.
    * De naam van de prijsexpressie helpt bij het herkennen waarvoor het prijselement staat. In dit voorbeeld wordt een prijselement gemaakt voor de rozenhouten afwerking van de luidsprekerkast.  
5. Klik op Voorwaarde bewerken.
    * Een prijsvoorwaarde zorgt ervoor dat een element van de prijsexpressie alleen in de verkoopprijs wordt opgenomen als een specifieke combinatie van kenmerken aanwezig is.  
6. Typ in het veld ConstraintBody 'CabinetFinish=="Rosewood"'.
7. Klik op OK.
8. Typ een waarde in het veld Expressie.
    * Typ bijvoorbeeld 50.  
9. Sluit de pagina.
10. Sluit de pagina.


