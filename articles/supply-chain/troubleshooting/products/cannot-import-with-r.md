---
title: U kunt een artikel niet importeren via de entiteit Vrijgegeven producten V2
description: U kunt een artikel niet importeren via de entiteit Vrijgegeven producten V2.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended, DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8182f2f83f6a3e4cf54fe6fa64b25a2f461ff541
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026397"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a><span data-ttu-id="bd160-103">U kunt een artikel niet importeren via de entiteit Vrijgegeven producten V2</span><span class="sxs-lookup"><span data-stu-id="bd160-103">You can't import an item by using the Released products V2 entity</span></span>

<span data-ttu-id="bd160-104">KB-nummer: 4611825</span><span class="sxs-lookup"><span data-stu-id="bd160-104">KB number: 4611825</span></span>

## <a name="symptoms"></a><span data-ttu-id="bd160-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="bd160-105">Symptoms</span></span>

<span data-ttu-id="bd160-106">Wanneer u een artikel probeert te importeren met de entiteit *Vrijgegeven producten V2*, ontvangt u een foutbericht dat op het volgende voorbeeld lijkt:</span><span class="sxs-lookup"><span data-stu-id="bd160-106">When you try to import an item by using the *Released products V2* entity, you receive an error message that resembles the following example:</span></span>

> <span data-ttu-id="bd160-107">Kan geen record maken in Artikelen - traceringsdimensiegroepen (EcoResTrackingDimensionGroupItem).</span><span class="sxs-lookup"><span data-stu-id="bd160-107">Cannot create a record in Items - tracking dimension groups (EcoResTrackingDimensionGroupItem).</span></span> <span data-ttu-id="bd160-108">Artikelnummer: 2040663, Batch.</span><span class="sxs-lookup"><span data-stu-id="bd160-108">Item number: 2040663, Batch.</span></span> <span data-ttu-id="bd160-109">Het record bestaat al.</span><span class="sxs-lookup"><span data-stu-id="bd160-109">The record already exists.</span></span>

## <a name="resolution"></a><span data-ttu-id="bd160-110">Oplossing</span><span class="sxs-lookup"><span data-stu-id="bd160-110">Resolution</span></span>

<span data-ttu-id="bd160-111">Als u nieuwe vrijgegeven producten wilt importeren, moet u de entiteit *Vrijgegeven product maken V2* gebruiken in plaats van de entiteit *Vrijgegeven producten V2*.</span><span class="sxs-lookup"><span data-stu-id="bd160-111">To import new released products, you must use the *Released product creation V2* entity instead of the *Released products V2* entity.</span></span>
