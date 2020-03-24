---
title: Verwijderde of afgeschafte functies in Dynamics 365 Finance
description: In dit onderwerp worden de functies beschreven die zijn verwijderd of die zijn gepland voor verwijdering uit Dynamics 365 Finance.
author: roschlom
manager: AnnBe
ms.date: 03/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: ec13076e6a05c3402af566487f7921f6971da215
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127972"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a><span data-ttu-id="5d13f-103">Verwijderde of afgeschafte functies in Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="5d13f-103">Removed or deprecated features in Dynamics 365 Finance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5d13f-104">In dit onderwerp worden de functies beschreven die zijn verwijderd of die zijn gepland voor verwijdering uit Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="5d13f-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Finance.</span></span>

- <span data-ttu-id="5d13f-105">Een *verwijderde* functie is niet langer beschikbaar in het product.</span><span class="sxs-lookup"><span data-stu-id="5d13f-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="5d13f-106">Een *afgeschafte* functie wordt niet meer actief ontwikkeld en kan in een toekomstige update worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="5d13f-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="5d13f-107">Deze lijst is bedoeld om u de mogelijkheid te bieden voor uw eigen planning rekening te houden met deze verwijderingen en afschaffingen.</span><span class="sxs-lookup"><span data-stu-id="5d13f-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="5d13f-108">Gedetailleerde informatie over objecten in Finance and Operations-apps is te vinden in de [Rapporten met technische naslaginformatie](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="5d13f-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="5d13f-109">U kunt de verschillende versies van deze rapporten vergelijken voor meer informatie over objecten die zijn gewijzigd of verwijderd in elke versie van Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="5d13f-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a><span data-ttu-id="5d13f-110">Verwijderde of verouderde functies in versie 10.0.12 van Finance</span><span class="sxs-lookup"><span data-stu-id="5d13f-110">Features removed or deprecated in the Finance 10.0.12 release</span></span>

### <a name="polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a><span data-ttu-id="5d13f-111">Poolse SSRS-rapporten: Btw-register voor verkoop, Btw-register voor inkoop, Btw-register EU-overzicht – functieverwijzing PL-00014</span><span class="sxs-lookup"><span data-stu-id="5d13f-111">Polish SSRS reports: Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="5d13f-112">**Reden voor afschaffing/verwijdering**</span><span class="sxs-lookup"><span data-stu-id="5d13f-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="5d13f-113">Niet wettelijk vereist.</span><span class="sxs-lookup"><span data-stu-id="5d13f-113">Not legally required.</span></span>  |
| <span data-ttu-id="5d13f-114">**Vervangen door een andere functie?**</span><span class="sxs-lookup"><span data-stu-id="5d13f-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="5d13f-115">Ja (Excel-indeling voor standaardauditbestand met btw-aangifte - JPK_VDEK)</span><span class="sxs-lookup"><span data-stu-id="5d13f-115">Yes (Excel format for Standard Audit File with VAT declaration - JPK_VDEK)</span></span> |
| <span data-ttu-id="5d13f-116">**Betrokken productgebieden**</span><span class="sxs-lookup"><span data-stu-id="5d13f-116">**Product areas affected**</span></span>         | <span data-ttu-id="5d13f-117">Aanvraag</span><span class="sxs-lookup"><span data-stu-id="5d13f-117">Application</span></span> |
| <span data-ttu-id="5d13f-118">**Implementatieoptie**</span><span class="sxs-lookup"><span data-stu-id="5d13f-118">**Deployment option**</span></span>              | <span data-ttu-id="5d13f-119">Alle</span><span class="sxs-lookup"><span data-stu-id="5d13f-119">All</span></span> |
| <span data-ttu-id="5d13f-120">**Status**</span><span class="sxs-lookup"><span data-stu-id="5d13f-120">**Status**</span></span>                         | <span data-ttu-id="5d13f-121">Afgeschaft: vanaf 1 juli 2021 worden de SSRS-rapporten niet meer ondersteund: **Btw-register voor verkoop, Btw-register voor inkoop, Btw-register EU-overzicht – functieverwijzing PL-00014**.</span><span class="sxs-lookup"><span data-stu-id="5d13f-121">Deprecated: By July 1, 2021, we plan to no longer support the SSRS reports: **Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014**.</span></span> <span data-ttu-id="5d13f-122">In plaats daarvan wordt een voorbeeld van een Excel-indeling geïntroduceerd voor het standaardauditbestand met btw-aangifte (JPK_VDEK).</span><span class="sxs-lookup"><span data-stu-id="5d13f-122">Excel format example for Standard Audit File with VAT declaration (JPK_VDEK) will be introduced instead.</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a><span data-ttu-id="5d13f-123">Verwijderde of verouderde functies in versie 10.0.7 van Finance</span><span class="sxs-lookup"><span data-stu-id="5d13f-123">Features removed or deprecated in the Finance 10.0.7 release</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="5d13f-124">Dialoogvenster Wijziging in werkstroom aanvragen bevat niet langer een vervolgkeuzelijst voor gebruikersselectie</span><span class="sxs-lookup"><span data-stu-id="5d13f-124">Workflow request change dialog box no longer includes user selection drop-down list</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="5d13f-125">**Reden voor afschaffing/verwijdering**</span><span class="sxs-lookup"><span data-stu-id="5d13f-125">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="5d13f-126">Gewijzigd in de functie met selectie van rekeninggroepen.</span><span class="sxs-lookup"><span data-stu-id="5d13f-126">Changed to the feature with account groups selection.</span></span>  |
| <span data-ttu-id="5d13f-127">**Vervangen door een andere functie?**</span><span class="sxs-lookup"><span data-stu-id="5d13f-127">**Replaced by another feature?**</span></span>   | <span data-ttu-id="5d13f-128">Ja</span><span class="sxs-lookup"><span data-stu-id="5d13f-128">Yes</span></span> |
| <span data-ttu-id="5d13f-129">**Betrokken productgebieden**</span><span class="sxs-lookup"><span data-stu-id="5d13f-129">**Product areas affected**</span></span>         | <span data-ttu-id="5d13f-130">Workflow</span><span class="sxs-lookup"><span data-stu-id="5d13f-130">Workflow</span></span> |
| <span data-ttu-id="5d13f-131">**Implementatieoptie**</span><span class="sxs-lookup"><span data-stu-id="5d13f-131">**Deployment option**</span></span>              | <span data-ttu-id="5d13f-132">Alle</span><span class="sxs-lookup"><span data-stu-id="5d13f-132">All</span></span> |
| <span data-ttu-id="5d13f-133">**Status**</span><span class="sxs-lookup"><span data-stu-id="5d13f-133">**Status**</span></span>                         | <span data-ttu-id="5d13f-134">Afgeschaft: op 1 december 2020 worden Chinese boekingstypen niet meer ondersteund zonder dat rekeninggroepen zijn geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="5d13f-134">Deprecated: By December 1, 2020, we plan to no longer support Chinese voucher types setup without Account groups selection.</span></span> <span data-ttu-id="5d13f-135">Meer informatie over het nieuwe ontwerp is te vinden in [Nieuwe functies in 10.0.7](whats-new-changed-10-0-7.md).</span><span class="sxs-lookup"><span data-stu-id="5d13f-135">Find more details about the new design in [What's new in 10.0.7](whats-new-changed-10-0-7.md).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="5d13f-136">Eerdere aankondigingen over verwijderde of afgeschafte functies</span><span class="sxs-lookup"><span data-stu-id="5d13f-136">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="5d13f-137">Zie [Verwijderde of afgeschafte functies in eerdere versies](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md) voor meer informatie over functies die zijn verwijderd of vervangen in eerdere versies.</span><span class="sxs-lookup"><span data-stu-id="5d13f-137">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span></span>
