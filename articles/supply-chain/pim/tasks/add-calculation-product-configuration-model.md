---
title: Een berekening toevoegen aan een productconfiguratiemodel
description: Deze procedure toont hoe u een nieuwe berekening toevoegt aan een productconfiguratiemodel.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 268baa4b518f6df52d4393f7278a79cbe1733844
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812664"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a>Een berekening toevoegen aan een productconfiguratiemodel

[!include [banner](../../includes/banner.md)]

Deze procedure toont hoe u een nieuwe berekening toevoegt aan een productconfiguratiemodel. Deze procedure toont hoe u de logische expressie maakt met de operator 'als' om een luidsprekerhoogte in te stellen op 10 voor witte luidsprekers en op 15 voor alle andere afwerkingen. De procedure gebruikt het onderdeel Geavanceerde luidspreker in het demobedrijf USMF.


## <a name="add-a-calculation"></a>Een berekening toevoegen

## <a name="create-calculation-expression"></a>Een berekeningsexpressie maken
1. Klik op Expressie bewerken.
2. Typ 'If[CabinetFinish=="White", 10, 15]' in het veld ConstraintBody.
3. Klik op Valideren.
4. Klik op Sluiten.
5. Klik op OK.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]