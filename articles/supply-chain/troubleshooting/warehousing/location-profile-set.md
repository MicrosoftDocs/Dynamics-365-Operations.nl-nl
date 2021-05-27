---
title: Door het locatieprofiel wordt negatieve voorraad niet toegestaan, maar is negatieve voorhanden voorraad wel toegestaan
description: De optie Negatieve voorraad toestaan voor het locatieprofiel is ingesteld op Nee, maar negatieve voorhanden voorraad blijft toegestaan.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 356d2dd7853bf93250e14eb9bd28a8a145794584
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026403"
---
# <a name="location-profile-disallows-negative-inventory-but-negative-on-hand-inventory-is-permitted"></a><span data-ttu-id="86252-103">Door het locatieprofiel wordt negatieve voorraad niet toegestaan, maar is negatieve voorhanden voorraad wel toegestaan</span><span class="sxs-lookup"><span data-stu-id="86252-103">Location profile disallows negative inventory, but negative on-hand inventory is permitted</span></span>

<span data-ttu-id="86252-104">KB-nummer: 4613622</span><span class="sxs-lookup"><span data-stu-id="86252-104">KB number: 4613622</span></span>

## <a name="symptoms"></a><span data-ttu-id="86252-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="86252-105">Symptoms</span></span>

<span data-ttu-id="86252-106">De optie **Negatieve voorraad toestaan** voor het locatieprofiel is ingesteld op *Nee*, maar negatieve voorhanden voorraad blijft toegestaan.</span><span class="sxs-lookup"><span data-stu-id="86252-106">The **Allow negative inventory** option for the location profile is set to *No*, but the system still allows negative on-hand inventory.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="86252-107">Voorbeeldscenario</span><span class="sxs-lookup"><span data-stu-id="86252-107">Example scenario</span></span>

<span data-ttu-id="86252-108">Voor overheidstransacties met gereguleerde transacties moet het systeem negatieve voorraad kunnen registreren om verliezen te boeken.</span><span class="sxs-lookup"><span data-stu-id="86252-108">For government-regulated transactions, the system must be able to record negative inventory to book losses.</span></span> <span data-ttu-id="86252-109">U wilt dat een artikel negatieve voorraad kan laten zien, maar alleen op bepaalde locaties, bijvoorbeeld op een bepaalde locatie, bijvoorbeeld containers.</span><span class="sxs-lookup"><span data-stu-id="86252-109">You want an item to be able to show negative inventory, but only in designated locations, such as tanks.</span></span> <span data-ttu-id="86252-110">Als de artikelmodelgroep echter negatieve voorraad toestaat, maakt het u niet uit of de locatie is ingesteld op negatieve voorraad toestaan.</span><span class="sxs-lookup"><span data-stu-id="86252-110">However, if the item model group allows negative inventory, you find that it doesn't matter whether the location is set to allow negative inventory.</span></span> <span data-ttu-id="86252-111">Als het artikel zo is ingesteld dat negatieve voorraad niet is toegestaan, maakt het niet uit hoe het locatieprofiel is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="86252-111">If the item is set up so that negative inventory isn't allowed, it doesn't matter how the location profile is set up.</span></span>

## <a name="resolution"></a><span data-ttu-id="86252-112">Oplossing</span><span class="sxs-lookup"><span data-stu-id="86252-112">Resolution</span></span>

<span data-ttu-id="86252-113">De instelling **Negatieve voorraad toestaan** vanuit het locatieprofiel is alleen van toepassing op magazijnprocessen, zoals orderverzameling.</span><span class="sxs-lookup"><span data-stu-id="86252-113">The **Allow negative inventory** setting from the location profile applies only to warehouse processes, such as picking.</span></span> <span data-ttu-id="86252-114">Als artikelmodelgroepen echter zijn ingesteld op negatieve voorraad toestaan, is dit van invloed op alle processen van de modules Voorraadbeheer en Magazijnbeheer en het locatieprofiel heeft geen voorrang.</span><span class="sxs-lookup"><span data-stu-id="86252-114">However, item model groups that are set to allow negative inventory affect all processes from the Inventory management and Warehouse management modules, and the location profile won't override the setting.</span></span>

<span data-ttu-id="86252-115">U kunt bepalen of in een magazijn negatieve voorraad is toegestaan.</span><span class="sxs-lookup"><span data-stu-id="86252-115">You can control whether a warehouse is allowed to carry negative inventory.</span></span> <span data-ttu-id="86252-116">Stel de artikelmodelgroepen in op het niet toestaan van negatieve fysieke voorraad en stel alleen het relevante magazijn in op het toestaan van negatieve voorraad.</span><span class="sxs-lookup"><span data-stu-id="86252-116">Set your item model groups to disallow negative physical inventory, and set only the relevant warehouse to allow negative inventory.</span></span>
