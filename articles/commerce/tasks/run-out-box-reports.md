---
title: Genereren en uitvoeren van kant-en-klare rapporten
description: Gebruik deze taakbegeleider om kant-en-klare rapporten uit te voeren in Headquarters vanuit verschillende werkgebieden en query's en verkooprapporten in Commerce.
author: ashishmsft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailCategoryAndProductWorkspace, RetailOrgHierarchyTreeLookup, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d148fa36a116860af8c44043d90759b8a2d76fb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411408"
---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="f47d7-103">Genereren en uitvoeren van kant-en-klare rapporten</span><span class="sxs-lookup"><span data-stu-id="f47d7-103">Generate and run out of box reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f47d7-104">Gebruik deze taakbegeleider om kant-en-klare rapporten uit te voeren in Headquarters vanuit verschillende werkgebieden en query's en verkooprapporten in Commerce.</span><span class="sxs-lookup"><span data-stu-id="f47d7-104">Use this task guide to run out of box reports in Headquarters from different workspaces and Inquiries & Sales reports located in Commerce.</span></span>

<span data-ttu-id="f47d7-105">Het demobedrijf dat wordt gebruikt om deze registratie te maken is USRT.</span><span class="sxs-lookup"><span data-stu-id="f47d7-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="f47d7-106">Deze registratie is bedoeld voor de systeembeheerdersrol.</span><span class="sxs-lookup"><span data-stu-id="f47d7-106">This recording is intended for the System administrator role.</span></span>

## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="f47d7-107">Rapporten starten vanuit werkgebieden</span><span class="sxs-lookup"><span data-stu-id="f47d7-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="f47d7-108">Ga naar Detailhandel en commerce > Producten en categorieën > Categorie- en productbeheer.</span><span class="sxs-lookup"><span data-stu-id="f47d7-108">Go to Retail and Commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="f47d7-109">Klik op de pijl om de sectie Rapporten uit te vouwen of samen te vouwen.</span><span class="sxs-lookup"><span data-stu-id="f47d7-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="f47d7-110">Klik op Rapport Topproducten.</span><span class="sxs-lookup"><span data-stu-id="f47d7-110">Click Top products report.</span></span>
4. <span data-ttu-id="f47d7-111">Voer een datum in het veld Begindatum in.</span><span class="sxs-lookup"><span data-stu-id="f47d7-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="f47d7-112">Voer een datum in het veld Einddatum in.</span><span class="sxs-lookup"><span data-stu-id="f47d7-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="f47d7-113">Klik in het veld Kanaal op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="f47d7-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="f47d7-114">Selecteer in de structuur 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span><span class="sxs-lookup"><span data-stu-id="f47d7-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="f47d7-115">Dit toont de standaardhiërarchie voor detailhandelsorganisaties voor rapportagedoeleinden in Commerce.</span><span class="sxs-lookup"><span data-stu-id="f47d7-115">This shows the default organization hierarchy for Commerce reporting purpose.</span></span>   <span data-ttu-id="f47d7-116">Ga naar Organisatiebeheer > Organisaties > Doelstellingen voor organisatiehiërarchie, kies Commerce-rapportage en controleer onder Toegewezen hiërarchieën de hiërarchienaam waarvoor de Standaardkolom is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="f47d7-116">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="f47d7-117">Als onderdeel van demogegevens (gebruikt voor taakregistratie) ziet u dat Winkels per regio de standaardorganisatiehiërarchie is voor rapportagedoeleinden.</span><span class="sxs-lookup"><span data-stu-id="f47d7-117">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
8. <span data-ttu-id="f47d7-118">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f47d7-118">Click OK.</span></span>
9. <span data-ttu-id="f47d7-119">Selecteer een optie in het veld Weergeven.</span><span class="sxs-lookup"><span data-stu-id="f47d7-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="f47d7-120">Selecteer een optie in het veld Op.</span><span class="sxs-lookup"><span data-stu-id="f47d7-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="f47d7-121">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f47d7-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports"></a><span data-ttu-id="f47d7-122">Rapporten starten vanuit de query- en verkooprapporten</span><span class="sxs-lookup"><span data-stu-id="f47d7-122">Launch reports from the inquiries and sales reports</span></span>
1. <span data-ttu-id="f47d7-123">Ga naar Detailhandel en commerce > Query's en rapporten > Verkooprapporten > Rapport Verkoop van categorie.</span><span class="sxs-lookup"><span data-stu-id="f47d7-123">Go to Retail and Commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="f47d7-124">Voer een datum in het veld Begindatum in.</span><span class="sxs-lookup"><span data-stu-id="f47d7-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="f47d7-125">Voer een datum in het veld Einddatum in.</span><span class="sxs-lookup"><span data-stu-id="f47d7-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="f47d7-126">Klik in het veld Kanaal op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="f47d7-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="f47d7-127">Selecteer in de structuur 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span><span class="sxs-lookup"><span data-stu-id="f47d7-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="f47d7-128">Dit toont de standaardhiërarchie voor detailhandelsorganisaties voor rapportagedoeleinden in Commerce.</span><span class="sxs-lookup"><span data-stu-id="f47d7-128">This shows the default organization hierarchy for Commerce reporting purpose.</span></span> <span data-ttu-id="f47d7-129">Ga naar Organisatiebeheer > Organisaties > Doelstellingen voor organisatiehiërarchie, kies Commerce-rapportage en controleer onder Toegewezen hiërarchieën de hiërarchienaam waarvoor de Standaardkolom is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="f47d7-129">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="f47d7-130">Als onderdeel van demogegevens (gebruikt voor taakregistratie) ziet u dat Winkels per regio de standaardorganisatiehiërarchie is voor rapportagedoeleinden.</span><span class="sxs-lookup"><span data-stu-id="f47d7-130">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
6. <span data-ttu-id="f47d7-131">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f47d7-131">Click OK.</span></span>
7. <span data-ttu-id="f47d7-132">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f47d7-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="f47d7-133">Een hoofdkantoorrapport exporteren</span><span class="sxs-lookup"><span data-stu-id="f47d7-133">Export an HQ reports</span></span>
1. <span data-ttu-id="f47d7-134">Ga naar Detailhandel en commerce > Query's en rapporten > Verkooprapporten > Rapport Verkoop van organisatie.</span><span class="sxs-lookup"><span data-stu-id="f47d7-134">Go to Retail and Commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="f47d7-135">Voer een datum in het veld Begindatum in.</span><span class="sxs-lookup"><span data-stu-id="f47d7-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="f47d7-136">Voer een datum in het veld Einddatum in.</span><span class="sxs-lookup"><span data-stu-id="f47d7-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="f47d7-137">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f47d7-137">Click OK.</span></span>
5. <span data-ttu-id="f47d7-138">Klik op Exporteren.</span><span class="sxs-lookup"><span data-stu-id="f47d7-138">Click Export.</span></span>
6. <span data-ttu-id="f47d7-139">Klik op PDF.</span><span class="sxs-lookup"><span data-stu-id="f47d7-139">Click PDF.</span></span>

