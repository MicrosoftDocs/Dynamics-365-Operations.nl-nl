---
title: Verwijderde of afgeschafte functies in Lifecycle Services (LCS)
description: In dit onderwerp worden de functies beschreven die zijn verwijderd waarvoor de verwijdering is gepland in Microsoft Dynamics Lifecycle Services (LCS).
author: AngelMarshall
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e583ec66f24940f44113433042f5e2340cf0f52c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748434"
---
# <a name="removed-or-deprecated-features-in-lifecycle-services-lcs"></a><span data-ttu-id="09923-103">Verwijderde of afgeschafte functies in Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="09923-103">Removed or deprecated features in Lifecycle Services (LCS)</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="09923-104">In dit onderwerp worden de functies beschreven die zijn verwijderd of afgeschaft voor Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="09923-104">This topic describes features that have been removed or deprecated for Microsoft Dynamics Lifecycle Services (LCS).</span></span>

- <span data-ttu-id="09923-105">Een *verwijderde* functie is niet langer beschikbaar in de service.</span><span class="sxs-lookup"><span data-stu-id="09923-105">A *removed* feature is no longer available in the service.</span></span>
- <span data-ttu-id="09923-106">Een *afgeschafte* functie wordt niet meer actief ontwikkeld en kan in een toekomstige update worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="09923-106">A *deprecated* feature isn't in active development and might be removed in a future update.</span></span>

<span data-ttu-id="09923-107">Deze lijst is bedoeld om u de mogelijkheid te bieden voor uw eigen planning rekening te houden met deze verwijderingen en afschaffingen.</span><span class="sxs-lookup"><span data-stu-id="09923-107">This list is provided so that you can consider these removals and deprecations as you do your own planning.</span></span>

## <a name="october-2019-announcements"></a><span data-ttu-id="09923-108">Aankondigingen van oktober 2019</span><span class="sxs-lookup"><span data-stu-id="09923-108">October 2019 announcements</span></span>

### <a name="flowchart-diagrams-in-business-process-modeler"></a><span data-ttu-id="09923-109">Stroomdiagrammen in Modelleertool bedrijfsprocessen</span><span class="sxs-lookup"><span data-stu-id="09923-109">Flowchart diagrams in Business process modeler</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="09923-110"><strong>Reden voor afschaffing/verwijdering</strong></span><span class="sxs-lookup"><span data-stu-id="09923-110"><strong>Reason for deprecation/removal</strong></span></span></td>
<td><span data-ttu-id="09923-111">We schaffen het onderdeel voor stroomdiagrammen in Modelleertool bedrijfsprocessen af omdat het verouderde ontwerp weinig werd gebruikt.</span><span class="sxs-lookup"><span data-stu-id="09923-111">We are deprecating the flowchart diagrams component in Business process modeler (BPM), because the legacy design caused low usage.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09923-112"><strong>Vervangen door een andere functie?</strong></span><span class="sxs-lookup"><span data-stu-id="09923-112"><strong>Replaced by another feature?</strong></span></span></td>
<td><span data-ttu-id="09923-113">Nee</span><span class="sxs-lookup"><span data-stu-id="09923-113">No</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09923-114"><strong>Betrokken gebieden</strong></span><span class="sxs-lookup"><span data-stu-id="09923-114"><strong>Areas affected</strong></span></span></td>
<td><span data-ttu-id="09923-115">Modelleertool bedrijfsprocessen</span><span class="sxs-lookup"><span data-stu-id="09923-115">Business process modeler</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09923-116"><strong>Status</strong></span><span class="sxs-lookup"><span data-stu-id="09923-116"><strong>Status</strong></span></span></td>
<td><span data-ttu-id="09923-117">Afgeschaft: naar verwachting wordt het onderdeel voor stroomdiagrammen in BPM in 2020 verwijderd.</span><span class="sxs-lookup"><span data-stu-id="09923-117">Deprecated: The flowchart diagrams component in BPM is expected to be removed in 2020.</span></span> <span data-ttu-id="09923-118">De volgende functionaliteit is niet beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="09923-118">The following functionality will be unavailable:</span></span>
<ul>
<li><span data-ttu-id="09923-119">Alle stroomdiagrammen zijn alleen-lezen en kunnen niet worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="09923-119">All flowcharts will be read-only and unavailable for editing.</span></span> <span data-ttu-id="09923-120">De shape-eigenschappen die aan stroomdiagramactiviteiten zijn gekoppeld, zijn eveneens niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="09923-120">The shape properties that are associated with flowchart activities will also be unavailable.</span></span> <span data-ttu-id="09923-121">Deze stroomdiagrammen omvatten zowel standaardstroomdiagrammen die automatisch worden gegenereerd als aangepaste stroomdiagrammen die worden aangepast op basis van deze standaardstroomdiagrammen.</span><span class="sxs-lookup"><span data-stu-id="09923-121">These flowcharts include both the default flowcharts that are automatically generated and customized flowcharts that are modified based on those default flowcharts.</span></span></li>
<li><span data-ttu-id="09923-122">De processtappen zijn alleen-lezen en kunnen niet worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="09923-122">The process steps will be read-only and unavailable for editing.</span></span></li>     
<li><span data-ttu-id="09923-123">De verouderde functie voor geschiktheid/hiaatanalyse is niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="09923-123">The legacy fit/gap analysis feature will be unavailable.</span></span> <span data-ttu-id="09923-124">Daarom wordt er niet automatisch een hiaatlijst gemaakt of beschikbaar voor export.</span><span class="sxs-lookup"><span data-stu-id="09923-124">Therefore, no gap list will be automatically created or available for export.</span></span>
<p><span data-ttu-id="09923-125"><strong>Opmerking:</strong> deze functie was eerder afgeschaft en vervangen door Microsoft Azure DevOps-integraties.</span><span class="sxs-lookup"><span data-stu-id="09923-125"><strong>Note:</strong> This feature had previously been deprecated and replaced by Microsoft Azure DevOps integrations.</span></span></p>
</li>
<li><span data-ttu-id="09923-126">De versiegeschiedenis van het stroomdiagram is niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="09923-126">The version history of the flowchart will be unavailable.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]