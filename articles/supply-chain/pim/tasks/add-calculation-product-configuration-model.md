---
title: Een berekening toevoegen aan een productconfiguratiemodel
description: Deze procedure toont hoe u een nieuwe berekening toevoegt aan een productconfiguratiemodel.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9754c46010e7bbdb2edef0d6e68162f344bb1257
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "343162"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a>Een berekening toevoegen aan een productconfiguratiemodel

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure toont hoe u een nieuwe berekening toevoegt aan een productconfiguratiemodel. Deze procedure toont hoe u de logische expressie maakt met de operator 'als' om een luidsprekerhoogte in te stellen op 10 voor witte luidsprekers en op 15 voor alle andere afwerkingen. De procedure gebruikt het onderdeel Geavanceerde luidspreker in het demobedrijf USMF.


## <a name="add-a-calculation"></a>Een berekening toevoegen

## <a name="create-calculation-expression"></a>Een berekeningsexpressie maken
1. Klik op Expressie bewerken.
2. Typ 'If[CabinetFinish=="White", 10, 15]' in het veld ConstraintBody.
3. Klik op Valideren.
4. Klik op Sluiten.
5. Klik op OK.

