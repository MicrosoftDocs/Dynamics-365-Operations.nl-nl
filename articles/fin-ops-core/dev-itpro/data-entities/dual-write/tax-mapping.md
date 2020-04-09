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
ms.openlocfilehash: a4da37d45698290b40f6c72148f1500bef72127a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173080"
---
# <a name="integrated-tax"></a><span data-ttu-id="0a771-103">Geïntegreerde belasting</span><span class="sxs-lookup"><span data-stu-id="0a771-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="0a771-104">Belastinginstellingsgegevens bepalen de instellingen voor zowel indirecte belastingen (btw, GST, omzetbelasting) als bronbelasting.</span><span class="sxs-lookup"><span data-stu-id="0a771-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="0a771-105">Het beschrijft de regel voor belastingberekening, het belastingtarief, belastingboekhouding, vereffening en andere concepten.</span><span class="sxs-lookup"><span data-stu-id="0a771-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="0a771-106">Sjablonen</span><span class="sxs-lookup"><span data-stu-id="0a771-106">Templates</span></span>

<span data-ttu-id="0a771-107">Belastinggegevens omvatten een verzameling entiteitstoewijzingen die samenwerken tijdens de interactie van gegevens, zoals in de volgende tabel wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="0a771-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="0a771-108">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="0a771-108">Finance and Operations apps</span></span> | <span data-ttu-id="0a771-109">Modelgestuurde apps in Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="0a771-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="0a771-110">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="0a771-110">Description</span></span> |
-------------------------|---------------------------------
<span data-ttu-id="0a771-111">Btw-codes</span><span class="sxs-lookup"><span data-stu-id="0a771-111">Tax codes</span></span>                   | <span data-ttu-id="0a771-112">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="0a771-112">msdyn\_taxcodes.md</span></span> | 
<span data-ttu-id="0a771-113">Belastinggroepen</span><span class="sxs-lookup"><span data-stu-id="0a771-113">Tax groups</span></span>                 | <span data-ttu-id="0a771-114">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="0a771-114">msdyn\_taxgroups.md</span></span> | 
<span data-ttu-id="0a771-115">Btw-artikelengroepen</span><span class="sxs-lookup"><span data-stu-id="0a771-115">Tax item groups</span></span>             | <span data-ttu-id="0a771-116">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="0a771-116">msdyn\_taxitemgroups.md</span></span> | 
<span data-ttu-id="0a771-117">Belastingvrijstellingen</span><span class="sxs-lookup"><span data-stu-id="0a771-117">Tax Exemptions</span></span>             | <span data-ttu-id="0a771-118">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="0a771-118">msdyn\_taxexemptcodes.md</span></span> | 
<span data-ttu-id="0a771-119">Belastingdienst</span><span class="sxs-lookup"><span data-stu-id="0a771-119">Tax Authorities</span></span>             | <span data-ttu-id="0a771-120">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="0a771-120">msdyn\_taxauthorities.md</span></span> | 
<span data-ttu-id="0a771-121">Bronbelastingcodes</span><span class="sxs-lookup"><span data-stu-id="0a771-121">Withholding tax codes</span></span>       | <span data-ttu-id="0a771-122">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="0a771-122">msdyn\_withholdingtaxcodes.md</span></span> | 
<span data-ttu-id="0a771-123">Bronbelastinggroepen</span><span class="sxs-lookup"><span data-stu-id="0a771-123">Withholding tax groups</span></span>     | <span data-ttu-id="0a771-124">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="0a771-124">msdyn\_withholdingtaxgroups.md</span></span> | 
<span data-ttu-id="0a771-125">Grootboekrekeningsgroep voor belasting</span><span class="sxs-lookup"><span data-stu-id="0a771-125">Tax Ledger Account Group</span></span> | <span data-ttu-id="0a771-126">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="0a771-126">msdyn\_taxpostinggroups</span></span>     | 

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

