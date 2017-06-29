---
title: Productieorders maken
description: "Als een productieorder wordt gemaakt, wordt er een aanvraag geïnitieerd om te beginnen met de productie van een artikel. De productieorder bevat informatie over het artikel dat wordt geproduceerd, het aantal en de geplande einddatum. Het bevat ook informatie over de te verwerken materialen en de processen die moeten worden gevolgd om het artikel te produceren."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: annbe
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: bcbb07553d990c35057ba32fd56d26fbc9c6f71b
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="create-production-orders"></a>Productieorders maken

[!include[banner](../includes/banner.md)]


Als een productieorder wordt gemaakt, wordt er een aanvraag geïnitieerd om te beginnen met de productie van een artikel. De productieorder bevat informatie over het artikel dat wordt geproduceerd, het aantal en de geplande einddatum. Het bevat ook informatie over de te verwerken materialen en de processen die moeten worden gevolgd om het artikel te produceren.

Een productieorder doorloopt fasen van de productielevenscyclus. Bij het maken wordt aan een order de status **Gemaakt** toegewezen. Bij het voltooien wordt aan een order de status **Beëindigd** toegewezen. Met een parameterinstelling in elke fase kan een gebruiker elke stap configureren. De instelling kan worden opgegeven voor één gebruiker of voor alle gebruikers.

De productiestuklijst en de productieroute zijn de belangrijkste entiteiten van de productieorder. Ze worden naar de productieorder gekopieerd op basis van het geselecteerde artikel en de hoeveelheid die gaan worden geproduceerd. Voordat de productieorder is gestart, kunnen de productiestuklijst en route worden bewerkt.

Een productieorder kan in de volgende scenario's worden gemaakt:

-   Gemaakt door hoofdplanningsuitvoering op basis van de vraag naar materiaal.
-   Rechtstreeks gemaakt van een verkooporderregel of wanneer een productieorder van een hoger niveau wordt gemaakt en geraamd (getraceerd aanbod).
-   Handmatig gemaakt.





