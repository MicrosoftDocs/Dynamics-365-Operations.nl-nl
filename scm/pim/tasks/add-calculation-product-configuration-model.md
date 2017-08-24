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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 9ac2d9bcc316a57941136c248a0c5ff030a1fe49
ms.contentlocale: nl-nl
ms.lasthandoff: 07/28/2017

---
# <a name="add-a-calculation-to-a-product-configuration-model"></a>Een berekening toevoegen aan een productconfiguratiemodel

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure toont hoe u een nieuwe berekening toevoegt aan een productconfiguratiemodel. Deze procedure toont hoe u de logische expressie maakt met de operator 'als' om een luidsprekerhoogte in te stellen op 10 voor witte luidsprekers en op 15 voor alle andere afwerkingen. De procedure gebruikt het onderdeel Geavanceerde luidspreker in het demobedrijf USMF.


## <a name="add-a-calculation"></a>Een berekening toevoegen

## <a name="create-calculation-expression"></a>Een berekeningsexpressie maken
1. Klik op Expressie bewerken.
2. Typ 'If[CabinetFinish=="White", 10, 15]' in het veld ConstraintBody.
3. Klik op Valideren.
4. Klik op Sluiten.
5. Klik op OK.


