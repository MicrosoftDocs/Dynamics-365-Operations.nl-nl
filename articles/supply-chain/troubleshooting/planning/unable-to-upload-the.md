---
title: U kunt de voorspelde eenheidskosten niet bijwerken wanneer u vraagprognoserecords importeert
description: Wanneer u gegevensentiteiten gebruikt om vraagprognoserecords te importeren, wordt de kostprijs voor bestaande records niet bijgewerkt, zodat deze overeenkomt met de geïmporteerde gegevens.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c8ea8322a6c7bafe2dfcaaee3e9989f753c85e2a
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026409"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a><span data-ttu-id="4fda0-103">U kunt de voorspelde eenheidskosten niet bijwerken wanneer u vraagprognoserecords importeert</span><span class="sxs-lookup"><span data-stu-id="4fda0-103">You can't update the forecasted unit cost when you import demand forecast records</span></span>

<span data-ttu-id="4fda0-104">KB-nummer: 4614109</span><span class="sxs-lookup"><span data-stu-id="4fda0-104">KB number: 4614109</span></span>

## <a name="symptoms"></a><span data-ttu-id="4fda0-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="4fda0-105">Symptoms</span></span>

<span data-ttu-id="4fda0-106">Wanneer u gegevensentiteiten gebruikt om vraagprognoserecords te importeren, wordt de waarde van **Voorspelde eenheidskosten** voor bestaande records niet bijgewerkt, zodat deze overeenkomt met de geïmporteerde gegevens.</span><span class="sxs-lookup"><span data-stu-id="4fda0-106">When you use data entities to import demand forecast records, the **Forecasted unit cost** value for existing records isn't updated so that it matches the imported data.</span></span>

## <a name="cause"></a><span data-ttu-id="4fda0-107">Oorzaak</span><span class="sxs-lookup"><span data-stu-id="4fda0-107">Cause</span></span>

<span data-ttu-id="4fda0-108">**Voorspelde eenheidskosten** is een alleen-lezenveld.</span><span class="sxs-lookup"><span data-stu-id="4fda0-108">**Forecasted unit cost** is a read-only field.</span></span> <span data-ttu-id="4fda0-109">De waarde is gebaseerd op de kosten van de producteenheid en kan niet direct worden ingesteld via importeren.</span><span class="sxs-lookup"><span data-stu-id="4fda0-109">The value is based on the product unit cost and can't be set directly through import.</span></span>

## <a name="resolution"></a><span data-ttu-id="4fda0-110">Oplossing</span><span class="sxs-lookup"><span data-stu-id="4fda0-110">Resolution</span></span>

<span data-ttu-id="4fda0-111">Omdat het veld alleen-lezen is, kunt u er geen waarden voor importeren.</span><span class="sxs-lookup"><span data-stu-id="4fda0-111">Because the field is read only, you can't import values for it.</span></span> <span data-ttu-id="4fda0-112">De waarde wordt berekend volgens de bestaande bedrijfslogica.</span><span class="sxs-lookup"><span data-stu-id="4fda0-112">The value will be calculated according to the existing business logic.</span></span>
