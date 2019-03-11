---
title: Productieorders maken
description: Als een productieorder wordt gemaakt, wordt er een aanvraag geïnitieerd om te beginnen met de productie van een artikel. De productieorder bevat informatie over het artikel dat wordt geproduceerd, het aantal en de geplande einddatum. Het bevat ook informatie over de te verwerken materialen en de processen die moeten worden gevolgd om het artikel te produceren.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2957b387aac9e0218f88572fa605cde1a30c52e5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "324624"
---
# <a name="create-production-orders"></a>Productieorders maken

[!include [banner](../includes/banner.md)]

Als een productieorder wordt gemaakt, wordt er een aanvraag geïnitieerd om te beginnen met de productie van een artikel. De productieorder bevat informatie over het artikel dat wordt geproduceerd, het aantal en de geplande einddatum. Het bevat ook informatie over de te verwerken materialen en de processen die moeten worden gevolgd om het artikel te produceren.

Een productieorder doorloopt fasen van de productielevenscyclus. Bij het maken wordt aan een order de status **Gemaakt** toegewezen. Bij het voltooien wordt aan een order de status **Beëindigd** toegewezen. Met een parameterinstelling in elke fase kan een gebruiker elke stap configureren. De instelling kan worden opgegeven voor één gebruiker of voor alle gebruikers.

De productiestuklijst en de productieroute zijn de belangrijkste entiteiten van de productieorder. Ze worden naar de productieorder gekopieerd op basis van het geselecteerde artikel en de hoeveelheid die gaan worden geproduceerd. Voordat de productieorder is gestart, kunnen de productiestuklijst en route worden bewerkt.

Een productieorder kan in de volgende scenario's worden gemaakt:

-   Gemaakt door hoofdplanningsuitvoering op basis van de vraag naar materiaal.
-   Rechtstreeks gemaakt van een verkooporderregel of wanneer een productieorder van een hoger niveau wordt gemaakt en geraamd (getraceerd aanbod).
-   Handmatig gemaakt.




