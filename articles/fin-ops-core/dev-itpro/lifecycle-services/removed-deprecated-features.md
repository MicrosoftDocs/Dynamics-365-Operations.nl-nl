---
title: Verwijderde of afgeschafte functies in Lifecycle Services (LCS)
description: In dit onderwerp worden de functies beschreven die zijn verwijderd waarvoor de verwijdering is gepland in Microsoft Dynamics Lifecycle Services (LCS).
author: sericks007
manager: AnnBe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c792d06e9b0aa42919de924bdcc9118358779b72
ms.sourcegitcommit: 75bbcff474cfb8d2f282be2b9d2d7984d1505fa3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/03/2019
ms.locfileid: "2885450"
---
# <a name="removed-or-deprecated-features-in-lifecycle-services-lcs"></a><span data-ttu-id="37d0f-103">Verwijderde of afgeschafte functies in Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="37d0f-103">Removed or deprecated features in Lifecycle Services (LCS)</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="37d0f-104">In dit onderwerp worden de functies beschreven die zijn verwijderd of afgeschaft voor Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="37d0f-104">This topic describes features that have been removed or deprecated for Microsoft Dynamics Lifecycle Services (LCS).</span></span>

- <span data-ttu-id="37d0f-105">Een *verwijderde* functie is niet langer beschikbaar in de service.</span><span class="sxs-lookup"><span data-stu-id="37d0f-105">A *removed* feature is no longer available in the service.</span></span>
- <span data-ttu-id="37d0f-106">Een *afgeschafte* functie wordt niet meer actief ontwikkeld en kan in een toekomstige update worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="37d0f-106">A *deprecated* feature isn't in active development and might be removed in a future update.</span></span>

<span data-ttu-id="37d0f-107">Deze lijst is bedoeld om u de mogelijkheid te bieden voor uw eigen planning rekening te houden met deze verwijderingen en afschaffingen.</span><span class="sxs-lookup"><span data-stu-id="37d0f-107">This list is provided so that you can consider these removals and deprecations as you do your own planning.</span></span>

## <a name="october-2019-announcements"></a><span data-ttu-id="37d0f-108">Aankondigingen van oktober 2019</span><span class="sxs-lookup"><span data-stu-id="37d0f-108">October 2019 announcements</span></span>

### <a name="flowchart-diagrams-in-business-process-modeler"></a><span data-ttu-id="37d0f-109">Stroomdiagrammen in Modelleertool bedrijfsprocessen</span><span class="sxs-lookup"><span data-stu-id="37d0f-109">Flowchart diagrams in Business process modeler</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="37d0f-110"><strong>Reden voor afschaffing/verwijdering</strong></span><span class="sxs-lookup"><span data-stu-id="37d0f-110"><strong>Reason for deprecation/removal</strong></span></span></td>
<td><span data-ttu-id="37d0f-111">We schaffen het onderdeel voor stroomdiagrammen in Modelleertool bedrijfsprocessen af omdat het verouderde ontwerp weinig werd gebruikt.</span><span class="sxs-lookup"><span data-stu-id="37d0f-111">We are deprecating the flowchart diagrams component in Business process modeler (BPM), because the legacy design caused low usage.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37d0f-112"><strong>Vervangen door een andere functie?</strong></span><span class="sxs-lookup"><span data-stu-id="37d0f-112"><strong>Replaced by another feature?</strong></span></span></td>
<td><span data-ttu-id="37d0f-113">Nee</span><span class="sxs-lookup"><span data-stu-id="37d0f-113">No</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37d0f-114"><strong>Betrokken gebieden</strong></span><span class="sxs-lookup"><span data-stu-id="37d0f-114"><strong>Areas affected</strong></span></span></td>
<td><span data-ttu-id="37d0f-115">Modelleertool bedrijfsprocessen</span><span class="sxs-lookup"><span data-stu-id="37d0f-115">Business process modeler</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37d0f-116"><strong>Status</strong></span><span class="sxs-lookup"><span data-stu-id="37d0f-116"><strong>Status</strong></span></span></td>
<td><span data-ttu-id="37d0f-117">Afgeschaft: naar verachting wordt het onderdeel voor stroomdiagrammen in BPM begin februari 2020 verwijderd.</span><span class="sxs-lookup"><span data-stu-id="37d0f-117">Deprecated: The flowchart diagrams component in BPM is expected to be removed by early February 2020.</span></span> <span data-ttu-id="37d0f-118">De volgende functionaliteit wordt verwijderd:</span><span class="sxs-lookup"><span data-stu-id="37d0f-118">The following functionality will be removed:</span></span>
<ul>
<li><span data-ttu-id="37d0f-119">Bestaande stroomdiagrammen zijn niet beschikbaar voor weergave of bewerking.</span><span class="sxs-lookup"><span data-stu-id="37d0f-119">Existing flowcharts will be unavailable for viewing or editing.</span></span> <span data-ttu-id="37d0f-120">De vormeigenschappen die aan stroomdiagramactiviteiten zijn gekoppeld, zijn dan ook niet meer beschikbaar omdat het hele tabblad <strong>Stroomdiagram</strong> wordt verwijderd.</span><span class="sxs-lookup"><span data-stu-id="37d0f-120">The shape properties that are associated with flowchart activities will also be unavailable, because the whole <strong>Flowchart</strong> tab will be removed.</span></span> <span data-ttu-id="37d0f-121">Deze stroomdiagrammen omvatten zowel standaardstroomdiagrammen die automatisch worden gegenereerd als aangepaste stroomdiagrammen die worden aangepast op basis van deze standaardstroomdiagrammen.</span><span class="sxs-lookup"><span data-stu-id="37d0f-121">These flowcharts include both the default flowcharts that are automatically generated and customized flowcharts that are modified based on those default flowcharts.</span></span></li>
<li><span data-ttu-id="37d0f-122">De verouderde functie voor geschiktheid/hiaatanalyse is niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="37d0f-122">The legacy fit/gap analysis feature will be unavailable.</span></span> <span data-ttu-id="37d0f-123">Daarom wordt er niet automatisch een hiaatlijst gemaakt of beschikbaar voor export.</span><span class="sxs-lookup"><span data-stu-id="37d0f-123">Therefore, no gap list will be automatically created or available for export.</span></span>
<p><span data-ttu-id="37d0f-124"><strong>Opmerking:</strong> deze functie was eerder afgeschaft en vervangen door Microsoft Azure DevOps-integraties.</span><span class="sxs-lookup"><span data-stu-id="37d0f-124"><strong>Note:</strong> This feature had previously been deprecated and replaced by Microsoft Azure DevOps integrations.</span></span></p>
</li>
<li><span data-ttu-id="37d0f-125">De versiegeschiedenis van het stroomdiagram is niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="37d0f-125">The version history of the flowchart will be unavailable.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>
