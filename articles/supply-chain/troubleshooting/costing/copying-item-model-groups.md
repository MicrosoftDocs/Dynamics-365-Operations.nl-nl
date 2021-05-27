---
title: Ontbrekende veldinstellingen wanneer artikelmodelgroepen naar een andere rechtspersoon worden gekopieerd
description: Veldinstellingen ontbreken wanneer artikelmodelgroepen naar een andere rechtspersoon worden gekopieerd.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f6fdfef0bc377418ed8a9c8830e74526a0b95eb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026400"
---
# <a name="missing-field-settings-when-item-model-groups-are-copied-to-another-legal-entity"></a><span data-ttu-id="77855-103">Ontbrekende veldinstellingen wanneer artikelmodelgroepen naar een andere rechtspersoon worden gekopieerd</span><span class="sxs-lookup"><span data-stu-id="77855-103">Missing field settings when item model groups are copied to another legal entity</span></span>

<span data-ttu-id="77855-104">KB-nummer: 4612800</span><span class="sxs-lookup"><span data-stu-id="77855-104">KB number: 4612800</span></span>

## <a name="symptoms"></a><span data-ttu-id="77855-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="77855-105">Symptoms</span></span>

<span data-ttu-id="77855-106">Wanneer u artikelmodelgroepen kopieert naar een andere rechtspersoon (bedrijf) met behulp van de entiteit *Voorraadbeleid van artikelmodelgroep*, ontbreken sommige veldinstellingen (bijvoorbeeld het voorraadmodel en de omschrijving) in de nieuwe modelgroep in de doelrechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="77855-106">When you copy item model groups to another legal entity (company) by using the *Item model group inventory policies* entity, some field settings (for example, the inventory model and description) are missing in the new model group in the destination legal entity.</span></span>

## <a name="resolution"></a><span data-ttu-id="77855-107">Oplossing</span><span class="sxs-lookup"><span data-stu-id="77855-107">Resolution</span></span>

<span data-ttu-id="77855-108">Als u een volledige kopie van een artikelmodelgroep naar een andere rechtspersoon wilt maken, moet u ook het voorraadbeleid van de artikelmodelgroep (`InventInventoryPolicyEntity`) en de beleidsregels voor kostenstroomveronderstelling (`InventCostFlowAssumptionPolicyEntity`) selecteren die aan de artikelmodelgroep zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="77855-108">To create a complete copy of an item model group to another legal entity, you must also select both the item model group inventory policies (`InventInventoryPolicyEntity`) and the cost flow assumption policies (`InventCostFlowAssumptionPolicyEntity`) that are associated with the item model group.</span></span>
