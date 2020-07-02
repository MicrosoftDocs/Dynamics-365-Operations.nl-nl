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
ms.openlocfilehash: 69521ec8c664a7025050c94105eca58f7f2c5c00
ms.sourcegitcommit: 7d943499f302298c6ff127f56cecc34af6cee289
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/08/2020
ms.locfileid: "3435555"
---
# <a name="integrated-tax"></a><span data-ttu-id="012a9-103">Geïntegreerde belasting</span><span class="sxs-lookup"><span data-stu-id="012a9-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="012a9-104">Belastinginstellingsgegevens bepalen de instellingen voor zowel indirecte belastingen (btw, GST, omzetbelasting) als bronbelasting.</span><span class="sxs-lookup"><span data-stu-id="012a9-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="012a9-105">Het beschrijft de regel voor belastingberekening, het belastingtarief, belastingboekhouding, vereffening en andere concepten.</span><span class="sxs-lookup"><span data-stu-id="012a9-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="012a9-106">Sjablonen</span><span class="sxs-lookup"><span data-stu-id="012a9-106">Templates</span></span>

<span data-ttu-id="012a9-107">Belastinggegevens omvatten een verzameling entiteitstoewijzingen die samenwerken tijdens de interactie van gegevens, zoals in de volgende tabel wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="012a9-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="012a9-108">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="012a9-108">Finance and Operations apps</span></span> | <span data-ttu-id="012a9-109">Modelgestuurde apps in Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="012a9-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="012a9-110">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="012a9-110">Description</span></span> |
-------------------------|---------------------------------|----|
<span data-ttu-id="012a9-111">Btw-groep voor artikel</span><span class="sxs-lookup"><span data-stu-id="012a9-111">Item sales tax group</span></span> | <span data-ttu-id="012a9-112">msdyn_taxitemgroups</span><span class="sxs-lookup"><span data-stu-id="012a9-112">msdyn_taxitemgroups</span></span> |
<span data-ttu-id="012a9-113">Btw-dienst</span><span class="sxs-lookup"><span data-stu-id="012a9-113">Sales tax authorities</span></span> | <span data-ttu-id="012a9-114">msdyn_taxauthorities</span><span class="sxs-lookup"><span data-stu-id="012a9-114">msdyn_taxauthorities</span></span> |
<span data-ttu-id="012a9-115">Entiteit btw-vrijstellingscode voor CDS</span><span class="sxs-lookup"><span data-stu-id="012a9-115">Sales tax exempt code entity CDS</span></span> | <span data-ttu-id="012a9-116">msdyn_taxexemptcodes</span><span class="sxs-lookup"><span data-stu-id="012a9-116">msdyn_taxexemptcodes</span></span> |
<span data-ttu-id="012a9-117">Btw-groepen</span><span class="sxs-lookup"><span data-stu-id="012a9-117">Sales tax groups</span></span> | <span data-ttu-id="012a9-118">msdyn_taxgroups</span><span class="sxs-lookup"><span data-stu-id="012a9-118">msdyn_taxgroups</span></span> |
<span data-ttu-id="012a9-119">Groepen van boekingen in btw-grootboek V2</span><span class="sxs-lookup"><span data-stu-id="012a9-119">Sales tax ledger posting groups V2</span></span> | <span data-ttu-id="012a9-120">msdyn_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="012a9-120">msdyn_taxpostinggroups</span></span> |
<span data-ttu-id="012a9-121">Bronbelastingcodes</span><span class="sxs-lookup"><span data-stu-id="012a9-121">Withholding tax codes</span></span> | <span data-ttu-id="012a9-122">msdyn_withholdingtaxcodes</span><span class="sxs-lookup"><span data-stu-id="012a9-122">msdyn_withholdingtaxcodes</span></span> |
<span data-ttu-id="012a9-123">Bronbelastinggroepen</span><span class="sxs-lookup"><span data-stu-id="012a9-123">Withholding tax groups</span></span> | <span data-ttu-id="012a9-124">msdyn_withholdingtaxgroups</span><span class="sxs-lookup"><span data-stu-id="012a9-124">msdyn_withholdingtaxgroups</span></span> | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

