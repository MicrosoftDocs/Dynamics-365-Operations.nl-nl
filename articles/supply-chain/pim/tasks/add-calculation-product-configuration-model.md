---
title: Een berekening toevoegen aan een productconfiguratiemodel
description: Deze procedure toont hoe u een nieuwe berekening toevoegt aan een productconfiguratiemodel.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6e23d33c6911310cca6aac0df4589e909568a86a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258066"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="e1f1e-103">Een berekening toevoegen aan een productconfiguratiemodel</span><span class="sxs-lookup"><span data-stu-id="e1f1e-103">Add a calculation to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e1f1e-104">Deze procedure toont hoe u een nieuwe berekening toevoegt aan een productconfiguratiemodel.</span><span class="sxs-lookup"><span data-stu-id="e1f1e-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="e1f1e-105">Deze procedure toont hoe u de logische expressie maakt met de operator 'als' om een luidsprekerhoogte in te stellen op 10 voor witte luidsprekers en op 15 voor alle andere afwerkingen.</span><span class="sxs-lookup"><span data-stu-id="e1f1e-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="e1f1e-106">De procedure gebruikt het onderdeel Geavanceerde luidspreker in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="e1f1e-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="e1f1e-107">Een berekening toevoegen</span><span class="sxs-lookup"><span data-stu-id="e1f1e-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="e1f1e-108">Een berekeningsexpressie maken</span><span class="sxs-lookup"><span data-stu-id="e1f1e-108">Create calculation expression</span></span>
1. <span data-ttu-id="e1f1e-109">Klik op Expressie bewerken.</span><span class="sxs-lookup"><span data-stu-id="e1f1e-109">Click Edit expression.</span></span>
2. <span data-ttu-id="e1f1e-110">Typ 'If[CabinetFinish=="White", 10, 15]' in het veld ConstraintBody.</span><span class="sxs-lookup"><span data-stu-id="e1f1e-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="e1f1e-111">Klik op Valideren.</span><span class="sxs-lookup"><span data-stu-id="e1f1e-111">Click Validate.</span></span>
4. <span data-ttu-id="e1f1e-112">Klik op Sluiten.</span><span class="sxs-lookup"><span data-stu-id="e1f1e-112">Click Close.</span></span>
5. <span data-ttu-id="e1f1e-113">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="e1f1e-113">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]