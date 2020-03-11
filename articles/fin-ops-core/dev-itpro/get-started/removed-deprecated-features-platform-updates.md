---
title: Verwijderde of afgeschafte Platform-functies
description: In dit onderwerp worden de functies beschreven die zijn verwijderd waarvoor de verwijdering is gepland in platformupdates van Finance and Operations-apps.
author: sericks007
manager: AnnBe
ms.date: 02/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 66e1420c7053c0df9f42b15c55aba1a8c869f02a
ms.sourcegitcommit: 2cc3b89efdd90f8d80883b7a271d7885282ba3e8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087878"
---
# <a name="removed-or-deprecated-platform-features"></a><span data-ttu-id="dece2-103">Verwijderde of afgeschafte Platform-functies</span><span class="sxs-lookup"><span data-stu-id="dece2-103">Removed or deprecated platform features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dece2-104">In dit onderwerp worden de functies beschreven die zijn verwijderd waarvoor de verwijdering is gepland in platformupdates van Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="dece2-104">This topic describes features that have been removed, or that are planned for removal in platform updates of Finance and Operations apps.</span></span>

- <span data-ttu-id="dece2-105">Een *verwijderde* functie is niet langer beschikbaar in het product.</span><span class="sxs-lookup"><span data-stu-id="dece2-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="dece2-106">Een *afgeschafte* functie wordt niet meer actief ontwikkeld en kan in een toekomstige update worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="dece2-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="dece2-107">Deze lijst is bedoeld om u de mogelijkheid te bieden voor uw eigen planning rekening te houden met deze verwijderingen en afschaffingen.</span><span class="sxs-lookup"><span data-stu-id="dece2-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="dece2-108">Gedetailleerde informatie over objecten in Finance and Operations-apps is te vinden in de [Rapporten met technische naslaginformatie](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="dece2-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="dece2-109">U kunt de verschillende versies van deze rapporten vergelijken voor meer informatie over objecten die zijn gewijzigd of verwijderd in elke versie van Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="dece2-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="platform-update-32"></a><span data-ttu-id="dece2-110">Platformupdate 32</span><span class="sxs-lookup"><span data-stu-id="dece2-110">Platform update 32</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="dece2-111">Dialoogvenster Wijziging in werkstroom aanvragen bevat niet langer een vervolgkeuzelijst voor gebruikersselectie</span><span class="sxs-lookup"><span data-stu-id="dece2-111">Workflow request change dialog box no longer includes user selection drop-down list</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="dece2-112">**Reden voor afschaffing/verwijdering**</span><span class="sxs-lookup"><span data-stu-id="dece2-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="dece2-113">Dit was een beveiligingsprobleem omdat de aanvraag voor wijziging naar een onbedoelde gebruiker kon worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="dece2-113">This was a security issue because the request for change could be sent to an unintended user.</span></span> <span data-ttu-id="dece2-114">Dit was ook een bruikbaarheidsprobleem omdat de gebruiker werd gedwongen te bepalen bij wie de werkstroom oorspronkelijk vandaan kwam en deze handmatig te selecteren.</span><span class="sxs-lookup"><span data-stu-id="dece2-114">This was also a usability issue because it forced the user to determine who the workflow originator was and manually select them.</span></span>  |
| <span data-ttu-id="dece2-115">**Vervangen door een andere functie?**</span><span class="sxs-lookup"><span data-stu-id="dece2-115">**Replaced by another feature?**</span></span>   | <span data-ttu-id="dece2-116">Nee</span><span class="sxs-lookup"><span data-stu-id="dece2-116">No</span></span> |
| <span data-ttu-id="dece2-117">**Betrokken productgebieden**</span><span class="sxs-lookup"><span data-stu-id="dece2-117">**Product areas affected**</span></span>         | <span data-ttu-id="dece2-118">Werkstroom</span><span class="sxs-lookup"><span data-stu-id="dece2-118">Workflow</span></span> |
| <span data-ttu-id="dece2-119">**Implementatieoptie**</span><span class="sxs-lookup"><span data-stu-id="dece2-119">**Deployment option**</span></span>              | <span data-ttu-id="dece2-120">Alle</span><span class="sxs-lookup"><span data-stu-id="dece2-120">All</span></span> |
| <span data-ttu-id="dece2-121">**Status**</span><span class="sxs-lookup"><span data-stu-id="dece2-121">**Status**</span></span>                         | <span data-ttu-id="dece2-122">De vervolgkeuzelijst voor gebruikersselectie werd in Platform update 32 verwijderd uit het dialoogvenster Wijziging in werkstroom aanvragen.</span><span class="sxs-lookup"><span data-stu-id="dece2-122">The user selection drop-down list was removed from the request change dialog box in Platform update 32.</span></span> <span data-ttu-id="dece2-123">Aanvragen voor verzoeken om wijzigingen worden automatisch naar de persoon verzonden bij wie de werkstroom oorspronkelijk vandaan kwam, zoals bedoeld.</span><span class="sxs-lookup"><span data-stu-id="dece2-123">Request change requests will be automatically sent to the originator as intended.</span></span> <span data-ttu-id="dece2-124">Zie [Acties in goedkeuringsprocessen voor werkstroom](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change) voor meer informatie over deze functionaliteit.</span><span class="sxs-lookup"><span data-stu-id="dece2-124">For more information about this functionality, see [Actions in workflow approval processes](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="dece2-125">Eerdere aankondigingen over verwijderde of afgeschafte functies</span><span class="sxs-lookup"><span data-stu-id="dece2-125">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="dece2-126">Zie [Verwijderde of afgeschafte functies in eerdere versies](../migration-upgrade/deprecated-features.md) voor meer informatie over functies die zijn verwijderd of vervangen in eerdere versies.</span><span class="sxs-lookup"><span data-stu-id="dece2-126">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../migration-upgrade/deprecated-features.md).</span></span>

