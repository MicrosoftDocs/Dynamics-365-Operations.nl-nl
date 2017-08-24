--- 
title: Een expressiebeperking toevoegen aan een productconfiguratiemodel
description: Deze procedure toont hoe u een nieuwe expressie voor beperking toevoegt aan een productconfiguratiemodel.
author: YuyuScheller
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: b8286eba5c799789ebba9a501a5a0b06ccdaabb1
ms.contentlocale: nl-nl
ms.lasthandoff: 07/28/2017

---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>Een expressiebeperking toevoegen aan een productconfiguratiemodel

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure toont hoe u een nieuwe expressie voor beperking toevoegt aan een productconfiguratiemodel. Deze geeft aan hoe u kunt verplicht dat de hoekbescherming moet worden toegepast op een luidspreker als de gebruiker een grill in metaal heeft geselecteerd. De procedure gebruikt het onderdeel Geavanceerde luidspreker in het demobedrijf USMF.


## <a name="create-an-expression-constraint"></a>Maak een expressiebeperking
1. Klik op Definitie van productvariantmodel.
2. Klik op Productconfiguratiemodellen.
3. Zoek en selecteer de gewenste record in de lijst.
    * In dit voorbeeld wordt het model Geavanceerde luidspreker gebruikt.  
4. Klik in de lijst op de koppeling in de geselecteerde rij.
5. Vouw de sectie Beperkingen uit.
6. Klik op Toevoegen.
7. Klik op Maken.
8. Typ een waarde in het veld Naam.

## <a name="enter-expression"></a>Expressie invoeren
1. Klik op Expressie bewerken.
    * Als u de gebruikersinterface in de taakregistratie in deze fase ontgrendelt, kunt u IntelliSense en de lijst van symbolen gebruiken om de expressie voor de beperking te maken.  
2. Typ 'Implies[FrontGrill=="Metal", CornerProtection] ' in het veld ConstraintBody.
    * Deze expressielogica meldt: Als de grill van metaal is, moet de optie voor hoekbescherming worden geselecteerd.  
3. Klik op Valideren.
    * De validatiefunctie wordt uitgevoerd op de expressie voor de beperking en controleert op syntaxisfouten.  
4. Klik op Sluiten.
5. Klik op OK.


