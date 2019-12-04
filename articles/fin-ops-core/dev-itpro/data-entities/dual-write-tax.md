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
ms.openlocfilehash: b6be53e9a2065373ca37c2791568a8161823803f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772405"
---
## <a name="integrated-tax"></a><span data-ttu-id="fe37d-103">Geïntegreerde belasting</span><span class="sxs-lookup"><span data-stu-id="fe37d-103">Integrated tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fe37d-104">Belastinginstellingsgegevens bepalen de instellingen voor zowel indirecte belastingen (btw, GST, omzetbelasting) als bronbelasting.</span><span class="sxs-lookup"><span data-stu-id="fe37d-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="fe37d-105">Het beschrijft de regel voor belastingberekening, het belastingtarief, belastingboekhouding, vereffening en andere concepten.</span><span class="sxs-lookup"><span data-stu-id="fe37d-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="fe37d-106">Sjablonen</span><span class="sxs-lookup"><span data-stu-id="fe37d-106">Templates</span></span>

<span data-ttu-id="fe37d-107">Belastinggegevens omvatten een verzameling entiteitstoewijzingen die samenwerken tijdens de interactie van gegevens, zoals in de volgende tabel wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="fe37d-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="fe37d-108">Finance en Operations</span><span class="sxs-lookup"><span data-stu-id="fe37d-108">Finance and Operations</span></span>   | <span data-ttu-id="fe37d-109">Customer Engagement-toepassing</span><span class="sxs-lookup"><span data-stu-id="fe37d-109">Customer Engagement application</span></span>
-------------------------|---------------------------------
<span data-ttu-id="fe37d-110">Belastingcodes</span><span class="sxs-lookup"><span data-stu-id="fe37d-110">Tax codes</span></span>                  | <span data-ttu-id="fe37d-111">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="fe37d-111">msdyn\_taxcodes.md</span></span>
<span data-ttu-id="fe37d-112">Belastinggroepen</span><span class="sxs-lookup"><span data-stu-id="fe37d-112">Tax groups</span></span>               | <span data-ttu-id="fe37d-113">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="fe37d-113">msdyn\_taxgroups.md</span></span>
<span data-ttu-id="fe37d-114">Btw-artikelengroepen</span><span class="sxs-lookup"><span data-stu-id="fe37d-114">Tax item groups</span></span>          | <span data-ttu-id="fe37d-115">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="fe37d-115">msdyn\_taxitemgroups.md</span></span>
<span data-ttu-id="fe37d-116">Belastingvrijstellingen</span><span class="sxs-lookup"><span data-stu-id="fe37d-116">Tax Exemptions</span></span>           | <span data-ttu-id="fe37d-117">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="fe37d-117">msdyn\_taxexemptcodes.md</span></span>
<span data-ttu-id="fe37d-118">Belastingdienst</span><span class="sxs-lookup"><span data-stu-id="fe37d-118">Tax Authorities</span></span>          | <span data-ttu-id="fe37d-119">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="fe37d-119">msdyn\_taxauthorities.md</span></span>
<span data-ttu-id="fe37d-120">Bronbelastingcodes</span><span class="sxs-lookup"><span data-stu-id="fe37d-120">Withholding tax codes</span></span>      | <span data-ttu-id="fe37d-121">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="fe37d-121">msdyn\_withholdingtaxcodes.md</span></span>
<span data-ttu-id="fe37d-122">Bronbelastinggroepen</span><span class="sxs-lookup"><span data-stu-id="fe37d-122">Withholding tax groups</span></span>   | <span data-ttu-id="fe37d-123">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="fe37d-123">msdyn\_withholdingtaxgroups.md</span></span>
<span data-ttu-id="fe37d-124">Grootboekrekeningsgroep voor belasting</span><span class="sxs-lookup"><span data-stu-id="fe37d-124">Tax Ledger Account Group</span></span> | <span data-ttu-id="fe37d-125">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="fe37d-125">msdyn\_taxpostinggroups</span></span>  

[!include [banner](../includes/dual-write-symbols.md)]

[!include [Tax groups](dual-write/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](dual-write/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](dual-write/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](dual-write/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](dual-write/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](dual-write/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](dual-write/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

