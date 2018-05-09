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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 123ae1315c95693af09d7d7c96a071d606ac98f8
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="c02c5-103">Een berekening toevoegen aan een productconfiguratiemodel</span><span class="sxs-lookup"><span data-stu-id="c02c5-103">Add a calculation to a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c02c5-104">Deze procedure toont hoe u een nieuwe berekening toevoegt aan een productconfiguratiemodel.</span><span class="sxs-lookup"><span data-stu-id="c02c5-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="c02c5-105">Deze procedure toont hoe u de logische expressie maakt met de operator 'als' om een luidsprekerhoogte in te stellen op 10 voor witte luidsprekers en op 15 voor alle andere afwerkingen.</span><span class="sxs-lookup"><span data-stu-id="c02c5-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="c02c5-106">De procedure gebruikt het onderdeel Geavanceerde luidspreker in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="c02c5-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="c02c5-107">Een berekening toevoegen</span><span class="sxs-lookup"><span data-stu-id="c02c5-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="c02c5-108">Een berekeningsexpressie maken</span><span class="sxs-lookup"><span data-stu-id="c02c5-108">Create calculation expression</span></span>
1. <span data-ttu-id="c02c5-109">Klik op Expressie bewerken.</span><span class="sxs-lookup"><span data-stu-id="c02c5-109">Click Edit expression.</span></span>
2. <span data-ttu-id="c02c5-110">Typ 'If[CabinetFinish=="White", 10, 15]' in het veld ConstraintBody.</span><span class="sxs-lookup"><span data-stu-id="c02c5-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="c02c5-111">Klik op Valideren.</span><span class="sxs-lookup"><span data-stu-id="c02c5-111">Click Validate.</span></span>
4. <span data-ttu-id="c02c5-112">Klik op Sluiten.</span><span class="sxs-lookup"><span data-stu-id="c02c5-112">Click Close.</span></span>
5. <span data-ttu-id="c02c5-113">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c02c5-113">Click OK.</span></span>


