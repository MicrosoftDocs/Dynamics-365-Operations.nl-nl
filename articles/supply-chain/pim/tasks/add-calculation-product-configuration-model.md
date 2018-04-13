--- 
title: Een berekening toevoegen aan een productconfiguratiemodel
description: Deze procedure toont hoe u een nieuwe berekening toevoegt aan een productconfiguratiemodel.
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2db8fb922b085a7f118822ef4fd974ac338f4d99
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="add-a-calculation-to-a-product-configuration-model"></a>Een berekening toevoegen aan een productconfiguratiemodel

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure toont hoe u een nieuwe berekening toevoegt aan een productconfiguratiemodel. Deze procedure toont hoe u de logische expressie maakt met de operator 'als' om een luidsprekerhoogte in te stellen op 10 voor witte luidsprekers en op 15 voor alle andere afwerkingen. De procedure gebruikt het onderdeel Geavanceerde luidspreker in het demobedrijf USMF.


## <a name="add-a-calculation"></a>Een berekening toevoegen

## <a name="create-calculation-expression"></a>Een berekeningsexpressie maken
1. Klik op Expressie bewerken.
2. Typ 'If[CabinetFinish=="White", 10, 15]' in het veld ConstraintBody.
3. Klik op Valideren.
4. Klik op Sluiten.
5. Klik op OK.


