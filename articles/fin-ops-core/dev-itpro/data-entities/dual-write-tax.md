---
title: Geïntegreerde belasting
description: In dit onderwerp wordt de integratie van belastinggegevens tussen Finance and Operations en Common Data Service beschreven.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ''
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 86e74086a5a74c7af5f2572d1a653a1658d729c0
ms.sourcegitcommit: d0322d1ed6c798301058e44dae76227a0e1f49ac
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2019
ms.locfileid: "2853854"
---
# <a name="integrated-tax"></a><span data-ttu-id="f99bb-103">Geïntegreerde belasting</span><span class="sxs-lookup"><span data-stu-id="f99bb-103">Integrated tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f99bb-104">Belastinginstellingsgegevens bepalen de instellingen voor zowel indirecte belastingen (btw, GST, omzetbelasting) als bronbelasting.</span><span class="sxs-lookup"><span data-stu-id="f99bb-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="f99bb-105">Het beschrijft de regel voor belastingberekening, het belastingtarief, belastingboekhouding, vereffening en andere concepten.</span><span class="sxs-lookup"><span data-stu-id="f99bb-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="f99bb-106">Sjablonen</span><span class="sxs-lookup"><span data-stu-id="f99bb-106">Templates</span></span>

<span data-ttu-id="f99bb-107">Belastinggegevens omvatten een verzameling entiteitstoewijzingen die samenwerken tijdens de interactie van gegevens, zoals in de volgende tabel wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f99bb-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="f99bb-108">Finance en Operations</span><span class="sxs-lookup"><span data-stu-id="f99bb-108">Finance and Operations</span></span>   | <span data-ttu-id="f99bb-109">Andere Dynamics 365-apps</span><span class="sxs-lookup"><span data-stu-id="f99bb-109">Other Dynamics 365 apps</span></span>
-------------------------|---------------------------------
<span data-ttu-id="f99bb-110">Belastingcodes</span><span class="sxs-lookup"><span data-stu-id="f99bb-110">Tax codes</span></span>                  | <span data-ttu-id="f99bb-111">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="f99bb-111">msdyn\_taxcodes.md</span></span>
<span data-ttu-id="f99bb-112">Belastinggroepen</span><span class="sxs-lookup"><span data-stu-id="f99bb-112">Tax groups</span></span>               | <span data-ttu-id="f99bb-113">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="f99bb-113">msdyn\_taxgroups.md</span></span>
<span data-ttu-id="f99bb-114">Btw-artikelengroepen</span><span class="sxs-lookup"><span data-stu-id="f99bb-114">Tax item groups</span></span>          | <span data-ttu-id="f99bb-115">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="f99bb-115">msdyn\_taxitemgroups.md</span></span>
<span data-ttu-id="f99bb-116">Belastingvrijstellingen</span><span class="sxs-lookup"><span data-stu-id="f99bb-116">Tax Exemptions</span></span>           | <span data-ttu-id="f99bb-117">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="f99bb-117">msdyn\_taxexemptcodes.md</span></span>
<span data-ttu-id="f99bb-118">Belastingdienst</span><span class="sxs-lookup"><span data-stu-id="f99bb-118">Tax Authorities</span></span>          | <span data-ttu-id="f99bb-119">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="f99bb-119">msdyn\_taxauthorities.md</span></span>
<span data-ttu-id="f99bb-120">Bronbelastingcodes</span><span class="sxs-lookup"><span data-stu-id="f99bb-120">Withholding tax codes</span></span>      | <span data-ttu-id="f99bb-121">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="f99bb-121">msdyn\_withholdingtaxcodes.md</span></span>
<span data-ttu-id="f99bb-122">Bronbelastinggroepen</span><span class="sxs-lookup"><span data-stu-id="f99bb-122">Withholding tax groups</span></span>   | <span data-ttu-id="f99bb-123">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="f99bb-123">msdyn\_withholdingtaxgroups.md</span></span>
<span data-ttu-id="f99bb-124">Grootboekrekeningsgroep voor belasting</span><span class="sxs-lookup"><span data-stu-id="f99bb-124">Tax Ledger Account Group</span></span> | <span data-ttu-id="f99bb-125">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="f99bb-125">msdyn\_taxpostinggroups</span></span>  

[!include [banner](../includes/dual-write-symbols.md)]

[!include [Tax groups](dual-write/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](dual-write/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](dual-write/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](dual-write/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](dual-write/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](dual-write/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](dual-write/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

