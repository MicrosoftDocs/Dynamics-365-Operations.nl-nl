---
title: Geïntegreerde belasting
description: In dit onderwerp wordt de integratie van btw-gegevens tussen Finance and Operations en Dataverse beschreven.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 7501ef21492a96c81b971e1d9077beaba9be897b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560332"
---
# <a name="integrated-tax"></a><span data-ttu-id="3bbac-103">Geïntegreerde belasting</span><span class="sxs-lookup"><span data-stu-id="3bbac-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="3bbac-104">Belastinginstellingsgegevens bepalen de instellingen voor zowel indirecte belastingen (btw, GST, omzetbelasting) als bronbelasting.</span><span class="sxs-lookup"><span data-stu-id="3bbac-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="3bbac-105">Het beschrijft de regel voor belastingberekening, het belastingtarief, belastingboekhouding, vereffening en andere concepten.</span><span class="sxs-lookup"><span data-stu-id="3bbac-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="3bbac-106">Sjablonen</span><span class="sxs-lookup"><span data-stu-id="3bbac-106">Templates</span></span>

<span data-ttu-id="3bbac-107">Belastinggegevens omvatten een verzameling tabeltoewijzingen die samenwerken tijdens de interactie van gegevens, zoals in de volgende tabel wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="3bbac-107">Tax data includes a collection of table maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="3bbac-108">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="3bbac-108">Finance and Operations apps</span></span> | <span data-ttu-id="3bbac-109">Modelgestuurde apps in Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="3bbac-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="3bbac-110">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="3bbac-110">Description</span></span> |
-------------------------|---------------------------------|----|
<span data-ttu-id="3bbac-111">Btw-groep voor artikel</span><span class="sxs-lookup"><span data-stu-id="3bbac-111">Item sales tax group</span></span> | <span data-ttu-id="3bbac-112">msdyn_taxitemgroups</span><span class="sxs-lookup"><span data-stu-id="3bbac-112">msdyn_taxitemgroups</span></span> |
<span data-ttu-id="3bbac-113">Btw-dienst</span><span class="sxs-lookup"><span data-stu-id="3bbac-113">Sales tax authorities</span></span> | <span data-ttu-id="3bbac-114">msdyn_taxauthorities</span><span class="sxs-lookup"><span data-stu-id="3bbac-114">msdyn_taxauthorities</span></span> |
<span data-ttu-id="3bbac-115">Entiteit btw-vrijstellingscode voor CDS</span><span class="sxs-lookup"><span data-stu-id="3bbac-115">Sales tax exempt code entity CDS</span></span> | <span data-ttu-id="3bbac-116">msdyn_taxexemptcodes</span><span class="sxs-lookup"><span data-stu-id="3bbac-116">msdyn_taxexemptcodes</span></span> |
<span data-ttu-id="3bbac-117">Btw-groepen</span><span class="sxs-lookup"><span data-stu-id="3bbac-117">Sales tax groups</span></span> | <span data-ttu-id="3bbac-118">msdyn_taxgroups</span><span class="sxs-lookup"><span data-stu-id="3bbac-118">msdyn_taxgroups</span></span> |
<span data-ttu-id="3bbac-119">Groepen van boekingen in btw-grootboek V2</span><span class="sxs-lookup"><span data-stu-id="3bbac-119">Sales tax ledger posting groups V2</span></span> | <span data-ttu-id="3bbac-120">msdyn_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="3bbac-120">msdyn_taxpostinggroups</span></span> |
<span data-ttu-id="3bbac-121">Bronbelastingcodes</span><span class="sxs-lookup"><span data-stu-id="3bbac-121">Withholding tax codes</span></span> | <span data-ttu-id="3bbac-122">msdyn_withholdingtaxcodes</span><span class="sxs-lookup"><span data-stu-id="3bbac-122">msdyn_withholdingtaxcodes</span></span> |
<span data-ttu-id="3bbac-123">Bronbelastinggroepen</span><span class="sxs-lookup"><span data-stu-id="3bbac-123">Withholding tax groups</span></span> | <span data-ttu-id="3bbac-124">msdyn_withholdingtaxgroups</span><span class="sxs-lookup"><span data-stu-id="3bbac-124">msdyn_withholdingtaxgroups</span></span> | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]