---
title: Uitgaande geplande intercompany-vraag weergeven
description: Deze procedure beschrijft hoe u alle geplande orders kunt weergeven die door een intercompany-leverancier worden vervuld.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqOutboundIntercompanyDemand
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f97cccc0d27d1154d8f8cb5018cf5040efcf190a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001769"
---
# <a name="view-outbound-planned-intercompany-demand"></a><span data-ttu-id="bc4d7-103">Uitgaande geplande intercompany-vraag weergeven</span><span class="sxs-lookup"><span data-stu-id="bc4d7-103">View outbound planned intercompany demand</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bc4d7-104">Deze procedure beschrijft hoe u alle geplande orders kunt weergeven die door een intercompany-leverancier worden vervuld.</span><span class="sxs-lookup"><span data-stu-id="bc4d7-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="bc4d7-105">Het demobedrijf dat wordt gebruikt om deze procedure te maken is DEMF.</span><span class="sxs-lookup"><span data-stu-id="bc4d7-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="bc4d7-106">Klik op Hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="bc4d7-106">Click Master planning.</span></span>
2. <span data-ttu-id="bc4d7-107">Typ of selecteer een waarde in het veld Plan.</span><span class="sxs-lookup"><span data-stu-id="bc4d7-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="bc4d7-108">Selecteer in het veld Plan plan 10.</span><span class="sxs-lookup"><span data-stu-id="bc4d7-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="bc4d7-109">Klik op Uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="bc4d7-109">Click Run.</span></span>
4. <span data-ttu-id="bc4d7-110">Voer een getal in het veld Aantal threads in.</span><span class="sxs-lookup"><span data-stu-id="bc4d7-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="bc4d7-111">Dit vertegenwoordigt het aantal parallelle threads dat voor de hoofdplanning moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="bc4d7-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="bc4d7-112">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="bc4d7-112">Click OK.</span></span>
    * <span data-ttu-id="bc4d7-113">Dit kan enige tijd duren.</span><span class="sxs-lookup"><span data-stu-id="bc4d7-113">This may take a while.</span></span>  
6. <span data-ttu-id="bc4d7-114">Klik op Geplande intercompany-vraag.</span><span class="sxs-lookup"><span data-stu-id="bc4d7-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="bc4d7-115">Klik op Uitgaande geplande intercompany-vraag.</span><span class="sxs-lookup"><span data-stu-id="bc4d7-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="bc4d7-116">Deze pagina biedt een overzicht van alle geplande vraag die door een interne toeleverancier wordt vervuld.</span><span class="sxs-lookup"><span data-stu-id="bc4d7-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="bc4d7-117">Vouw de sectie Details van upstream vraag uit.</span><span class="sxs-lookup"><span data-stu-id="bc4d7-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="bc4d7-118">In deze sectie ziet u de details voor de wijze waarop de vraag wordt vervuld.</span><span class="sxs-lookup"><span data-stu-id="bc4d7-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="bc4d7-119">U moet mogelijk wachten totdat de hoofdplanning is uitgevoerd in het toeleveringsbedrijf, voordat u hier aanvullende informatie kunt zien.</span><span class="sxs-lookup"><span data-stu-id="bc4d7-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  

