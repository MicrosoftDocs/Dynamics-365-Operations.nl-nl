---
title: Geïntegreerde belasting
description: In dit onderwerp wordt de integratie van btw-gegevens tussen Finance and Operations en Common Data Service beschreven.
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
ms.openlocfilehash: 0d32a5f7859f0200da823a73d94b9a6b2a9c8e7d
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019716"
---
# <a name="integrated-tax"></a><span data-ttu-id="d0f21-103">Geïntegreerde belasting</span><span class="sxs-lookup"><span data-stu-id="d0f21-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="d0f21-104">Belastinginstellingsgegevens bepalen de instellingen voor zowel indirecte belastingen (btw, GST, omzetbelasting) als bronbelasting.</span><span class="sxs-lookup"><span data-stu-id="d0f21-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="d0f21-105">Het beschrijft de regel voor belastingberekening, het belastingtarief, belastingboekhouding, vereffening en andere concepten.</span><span class="sxs-lookup"><span data-stu-id="d0f21-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="d0f21-106">Sjablonen</span><span class="sxs-lookup"><span data-stu-id="d0f21-106">Templates</span></span>

<span data-ttu-id="d0f21-107">Belastinggegevens omvatten een verzameling entiteitstoewijzingen die samenwerken tijdens de interactie van gegevens, zoals in de volgende tabel wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d0f21-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="d0f21-108">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d0f21-108">Finance and Operations</span></span>   | <span data-ttu-id="d0f21-109">Andere Dynamics 365-apps</span><span class="sxs-lookup"><span data-stu-id="d0f21-109">Other Dynamics 365 apps</span></span>
-------------------------|---------------------------------
<span data-ttu-id="d0f21-110">Belastingcodes</span><span class="sxs-lookup"><span data-stu-id="d0f21-110">Tax codes</span></span>                  | <span data-ttu-id="d0f21-111">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="d0f21-111">msdyn\_taxcodes.md</span></span>
<span data-ttu-id="d0f21-112">Belastinggroepen</span><span class="sxs-lookup"><span data-stu-id="d0f21-112">Tax groups</span></span>               | <span data-ttu-id="d0f21-113">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="d0f21-113">msdyn\_taxgroups.md</span></span>
<span data-ttu-id="d0f21-114">Btw-artikelengroepen</span><span class="sxs-lookup"><span data-stu-id="d0f21-114">Tax item groups</span></span>          | <span data-ttu-id="d0f21-115">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="d0f21-115">msdyn\_taxitemgroups.md</span></span>
<span data-ttu-id="d0f21-116">Belastingvrijstellingen</span><span class="sxs-lookup"><span data-stu-id="d0f21-116">Tax Exemptions</span></span>           | <span data-ttu-id="d0f21-117">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="d0f21-117">msdyn\_taxexemptcodes.md</span></span>
<span data-ttu-id="d0f21-118">Belastingdienst</span><span class="sxs-lookup"><span data-stu-id="d0f21-118">Tax Authorities</span></span>          | <span data-ttu-id="d0f21-119">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="d0f21-119">msdyn\_taxauthorities.md</span></span>
<span data-ttu-id="d0f21-120">Bronbelastingcodes</span><span class="sxs-lookup"><span data-stu-id="d0f21-120">Withholding tax codes</span></span>      | <span data-ttu-id="d0f21-121">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="d0f21-121">msdyn\_withholdingtaxcodes.md</span></span>
<span data-ttu-id="d0f21-122">Bronbelastinggroepen</span><span class="sxs-lookup"><span data-stu-id="d0f21-122">Withholding tax groups</span></span>   | <span data-ttu-id="d0f21-123">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="d0f21-123">msdyn\_withholdingtaxgroups.md</span></span>
<span data-ttu-id="d0f21-124">Grootboekrekeningsgroep voor belasting</span><span class="sxs-lookup"><span data-stu-id="d0f21-124">Tax Ledger Account Group</span></span> | <span data-ttu-id="d0f21-125">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="d0f21-125">msdyn\_taxpostinggroups</span></span>  

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

