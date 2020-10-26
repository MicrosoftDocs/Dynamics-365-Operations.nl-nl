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
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 68461f375c6d5b04f224331dc192c921cf3c4d04
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979324"
---
# <a name="integrated-tax"></a><span data-ttu-id="3e868-103">Geïntegreerde belasting</span><span class="sxs-lookup"><span data-stu-id="3e868-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="3e868-104">Belastinginstellingsgegevens bepalen de instellingen voor zowel indirecte belastingen (btw, GST, omzetbelasting) als bronbelasting.</span><span class="sxs-lookup"><span data-stu-id="3e868-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="3e868-105">Het beschrijft de regel voor belastingberekening, het belastingtarief, belastingboekhouding, vereffening en andere concepten.</span><span class="sxs-lookup"><span data-stu-id="3e868-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="3e868-106">Sjablonen</span><span class="sxs-lookup"><span data-stu-id="3e868-106">Templates</span></span>

<span data-ttu-id="3e868-107">Belastinggegevens omvatten een verzameling entiteitstoewijzingen die samenwerken tijdens de interactie van gegevens, zoals in de volgende tabel wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="3e868-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="3e868-108">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="3e868-108">Finance and Operations apps</span></span> | <span data-ttu-id="3e868-109">Modelgestuurde apps in Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="3e868-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="3e868-110">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="3e868-110">Description</span></span> |
-------------------------|---------------------------------|----|
<span data-ttu-id="3e868-111">Btw-groep voor artikel</span><span class="sxs-lookup"><span data-stu-id="3e868-111">Item sales tax group</span></span> | <span data-ttu-id="3e868-112">msdyn_taxitemgroups</span><span class="sxs-lookup"><span data-stu-id="3e868-112">msdyn_taxitemgroups</span></span> |
<span data-ttu-id="3e868-113">Btw-dienst</span><span class="sxs-lookup"><span data-stu-id="3e868-113">Sales tax authorities</span></span> | <span data-ttu-id="3e868-114">msdyn_taxauthorities</span><span class="sxs-lookup"><span data-stu-id="3e868-114">msdyn_taxauthorities</span></span> |
<span data-ttu-id="3e868-115">Entiteit btw-vrijstellingscode voor CDS</span><span class="sxs-lookup"><span data-stu-id="3e868-115">Sales tax exempt code entity CDS</span></span> | <span data-ttu-id="3e868-116">msdyn_taxexemptcodes</span><span class="sxs-lookup"><span data-stu-id="3e868-116">msdyn_taxexemptcodes</span></span> |
<span data-ttu-id="3e868-117">Btw-groepen</span><span class="sxs-lookup"><span data-stu-id="3e868-117">Sales tax groups</span></span> | <span data-ttu-id="3e868-118">msdyn_taxgroups</span><span class="sxs-lookup"><span data-stu-id="3e868-118">msdyn_taxgroups</span></span> |
<span data-ttu-id="3e868-119">Groepen van boekingen in btw-grootboek V2</span><span class="sxs-lookup"><span data-stu-id="3e868-119">Sales tax ledger posting groups V2</span></span> | <span data-ttu-id="3e868-120">msdyn_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="3e868-120">msdyn_taxpostinggroups</span></span> |
<span data-ttu-id="3e868-121">Bronbelastingcodes</span><span class="sxs-lookup"><span data-stu-id="3e868-121">Withholding tax codes</span></span> | <span data-ttu-id="3e868-122">msdyn_withholdingtaxcodes</span><span class="sxs-lookup"><span data-stu-id="3e868-122">msdyn_withholdingtaxcodes</span></span> |
<span data-ttu-id="3e868-123">Bronbelastinggroepen</span><span class="sxs-lookup"><span data-stu-id="3e868-123">Withholding tax groups</span></span> | <span data-ttu-id="3e868-124">msdyn_withholdingtaxgroups</span><span class="sxs-lookup"><span data-stu-id="3e868-124">msdyn_withholdingtaxgroups</span></span> | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

