--- 
title: Op kenmerken gebaseerde prijzen instellen voor configureerbare producten
description: Deze procedure laat zien hoe u op kenmerken gebaseerde prijsdetails instelt.
author: YuyuScheller
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 88402bef6fd5dad38a74795cd31a4046085d6db7
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

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


