---
title: Uitgaande geplande intercompany-vraag weergeven
description: Deze procedure beschrijft hoe u alle geplande orders kunt weergeven die door een intercompany-leverancier worden vervuld.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqOutboundIntercompanyDemand
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2e0e3a4613e5598e725c475c7dff7662bf4169a7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "333709"
---
# <a name="view-outbound-planned-intercompany-demand"></a><span data-ttu-id="c451d-103">Uitgaande geplande intercompany-vraag weergeven</span><span class="sxs-lookup"><span data-stu-id="c451d-103">View outbound planned intercompany demand</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c451d-104">Deze procedure beschrijft hoe u alle geplande orders kunt weergeven die door een intercompany-leverancier worden vervuld.</span><span class="sxs-lookup"><span data-stu-id="c451d-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="c451d-105">Het demobedrijf dat wordt gebruikt om deze procedure te maken is DEMF.</span><span class="sxs-lookup"><span data-stu-id="c451d-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="c451d-106">Klik op Hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="c451d-106">Click Master planning.</span></span>
2. <span data-ttu-id="c451d-107">Typ of selecteer een waarde in het veld Plan.</span><span class="sxs-lookup"><span data-stu-id="c451d-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="c451d-108">Selecteer in het veld Plan plan 10.</span><span class="sxs-lookup"><span data-stu-id="c451d-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="c451d-109">Klik op Uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="c451d-109">Click Run.</span></span>
4. <span data-ttu-id="c451d-110">Voer een getal in het veld Aantal threads in.</span><span class="sxs-lookup"><span data-stu-id="c451d-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="c451d-111">Dit vertegenwoordigt het aantal parallelle threads dat voor de hoofdplanning moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c451d-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="c451d-112">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c451d-112">Click OK.</span></span>
    * <span data-ttu-id="c451d-113">Dit kan enige tijd duren.</span><span class="sxs-lookup"><span data-stu-id="c451d-113">This may take a while.</span></span>  
6. <span data-ttu-id="c451d-114">Klik op Geplande intercompany-vraag.</span><span class="sxs-lookup"><span data-stu-id="c451d-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="c451d-115">Klik op Uitgaande geplande intercompany-vraag.</span><span class="sxs-lookup"><span data-stu-id="c451d-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="c451d-116">Deze pagina biedt een overzicht van alle geplande vraag die door een interne toeleverancier wordt vervuld.</span><span class="sxs-lookup"><span data-stu-id="c451d-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="c451d-117">Vouw de sectie Details van upstream vraag uit.</span><span class="sxs-lookup"><span data-stu-id="c451d-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="c451d-118">In deze sectie ziet u de details voor de wijze waarop de vraag wordt vervuld.</span><span class="sxs-lookup"><span data-stu-id="c451d-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="c451d-119">U moet mogelijk wachten totdat de hoofdplanning is uitgevoerd in het toeleveringsbedrijf, voordat u hier aanvullende informatie kunt zien.</span><span class="sxs-lookup"><span data-stu-id="c451d-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  

