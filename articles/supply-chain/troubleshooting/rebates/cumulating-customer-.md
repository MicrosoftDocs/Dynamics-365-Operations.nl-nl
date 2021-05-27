---
title: De cumulatie van klantkortingen mislukt wanneer artikelkortingsgroepen worden gebruikt
description: Wanneer u klantkortingsovereenkomsten gebruikt in combinatie met artikelkortingsgroepen, worden kortingen berekend, maar mislukt de cumulatie.
author: sherry-zheng
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PdsRebateTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5222d5a52a34ecfa4a1eac96a2cb561f257f17ea
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026395"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a><span data-ttu-id="48148-103">De cumulatie van klantkortingen mislukt wanneer artikelkortingsgroepen worden gebruikt</span><span class="sxs-lookup"><span data-stu-id="48148-103">Cumulation of customer rebates fails when item rebate groups are used</span></span>

<span data-ttu-id="48148-104">KB-nummer: 4611372</span><span class="sxs-lookup"><span data-stu-id="48148-104">KB number: 4611372</span></span>

## <a name="symptoms"></a><span data-ttu-id="48148-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="48148-105">Symptoms</span></span>

<span data-ttu-id="48148-106">Wanneer u klantkortingsovereenkomsten (van het type *bedrag*) gebruikt in combinatie met artikelkortingsgroepen, worden kortingen berekend, maar mislukt de cumulatie.</span><span class="sxs-lookup"><span data-stu-id="48148-106">When you use customer rebate agreements (of the *amount* type) in combination with item rebate groups, rebates are calculated, but cumulation fails.</span></span>

## <a name="resolution"></a><span data-ttu-id="48148-107">Oplossing</span><span class="sxs-lookup"><span data-stu-id="48148-107">Resolution</span></span>

<span data-ttu-id="48148-108">Dit gedrag van het systeem is inherent aan het ontwerp.</span><span class="sxs-lookup"><span data-stu-id="48148-108">The system is behaving as designed.</span></span> <span data-ttu-id="48148-109">Artikelengroepen groeperen alleen artikelen met dezelfde drempelvoorwaarde.</span><span class="sxs-lookup"><span data-stu-id="48148-109">Item groups group only items that have the same threshold condition.</span></span> <span data-ttu-id="48148-110">De kortingsvoorwaarde (drempel) wordt ingesteld op het bedrag voor elk artikel, niet op het gecumuleerde bedrag voor een artikel in de artikelgroep.</span><span class="sxs-lookup"><span data-stu-id="48148-110">The rebate condition (threshold) is set against the amount for each item, not against the cumulated amount for any item in the item group.</span></span>
