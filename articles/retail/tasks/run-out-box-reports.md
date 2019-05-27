---
title: Genereren en uitvoeren van kant-en-klare rapporten
description: Gebruik deze taakbegeleiding om kant-en-klare rapporten op het hoofdkantoor uit te voeren vanuit verschillende werkgebieden en query's en verkooprapporten onder Detailhandel en commerce.
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
ms.openlocfilehash: b42f86fc243312d18654b1a048f9dffb29afd187
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550065"
---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="2fcd5-103">Genereren en uitvoeren van kant-en-klare rapporten</span><span class="sxs-lookup"><span data-stu-id="2fcd5-103">Generate and run out of box reports</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="2fcd5-104">Gebruik deze taakbegeleiding om kant-en-klare rapporten op het hoofdkantoor uit te voeren vanuit verschillende werkgebieden en query's en verkooprapporten onder Detailhandel en commerce.</span><span class="sxs-lookup"><span data-stu-id="2fcd5-104">Use this task guide to run out of box reports in headquarters from different workspaces and Inquiries & Sales reports located under Retail & Commerce.</span></span>



<span data-ttu-id="2fcd5-105">Het demobedrijf dat wordt gebruikt om deze registratie te maken is USRT.</span><span class="sxs-lookup"><span data-stu-id="2fcd5-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="2fcd5-106">Deze registratie is bedoeld voor de systeembeheerdersrol.</span><span class="sxs-lookup"><span data-stu-id="2fcd5-106">This recording is intended for the System administrator role.</span></span>


## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="2fcd5-107">Rapporten starten vanuit werkgebieden</span><span class="sxs-lookup"><span data-stu-id="2fcd5-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="2fcd5-108">Ga naar Detailhandel en commerce > Producten en categorieën > Categorie- en productbeheer.</span><span class="sxs-lookup"><span data-stu-id="2fcd5-108">Go to Retail and commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="2fcd5-109">Klik op de pijl om de sectie Rapporten uit te vouwen of samen te vouwen.</span><span class="sxs-lookup"><span data-stu-id="2fcd5-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="2fcd5-110">Klik op Rapport Topproducten.</span><span class="sxs-lookup"><span data-stu-id="2fcd5-110">Click Top products report.</span></span>
4. <span data-ttu-id="2fcd5-111">Voer een datum in het veld Begindatum in.</span><span class="sxs-lookup"><span data-stu-id="2fcd5-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="2fcd5-112">Voer een datum in het veld Einddatum in.</span><span class="sxs-lookup"><span data-stu-id="2fcd5-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="2fcd5-113">Klik in het veld Kanaal op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="2fcd5-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="2fcd5-114">Selecteer in de structuur 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span><span class="sxs-lookup"><span data-stu-id="2fcd5-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="2fcd5-115">Dit toont de standaardhiërarchie voor detailhandelsorganisaties voor detailhandelrapportagedoeleinden.</span><span class="sxs-lookup"><span data-stu-id="2fcd5-115">This shows the default retail organization hierarchy for Retail reporting purpose.</span></span>   <span data-ttu-id="2fcd5-116">Ga naar Organisatiebeheer >Organisaties > Organisatiehiërarchiedoelstellingen en kies Detailhandelrapportage onder Toegewezen hiërarchieën, en controleer de hiërarchienaam waarvoor Standaardkolom is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="2fcd5-116">Go to Organization administration >Organizations >Organization hierarchy purposes and choose Retail reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span>      <span data-ttu-id="2fcd5-117">Als onderdeel van demogegevens (gebruikt voor taakregistratie) ziet u dat Detailhandelwinkels per regio de standaardorganisatiehiërarchie is voor detailhandelrapportagedoeleinden.</span><span class="sxs-lookup"><span data-stu-id="2fcd5-117">As part of demo data (used for this task recording) you would notice, Retail Stores by Region, is the default organization hierarchy for the Retail reporting purpose.</span></span>     
8. <span data-ttu-id="2fcd5-118">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="2fcd5-118">Click OK.</span></span>
9. <span data-ttu-id="2fcd5-119">Selecteer een optie in het veld Weergeven.</span><span class="sxs-lookup"><span data-stu-id="2fcd5-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="2fcd5-120">Selecteer een optie in het veld Op.</span><span class="sxs-lookup"><span data-stu-id="2fcd5-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="2fcd5-121">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="2fcd5-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports-located-under-retail--commerce-app-link"></a><span data-ttu-id="2fcd5-122">Rapporten starten vanuit de query- en verkooprapporten onder de appkoppeling Detailhandel en commerce.</span><span class="sxs-lookup"><span data-stu-id="2fcd5-122">Launch reports from the inquiries and sales reports located under Retail & Commerce app link.</span></span>
1. <span data-ttu-id="2fcd5-123">Ga naar Detailhandel en commerce > Query's en rapporten > Verkooprapporten > Rapport Verkoop van categorie.</span><span class="sxs-lookup"><span data-stu-id="2fcd5-123">Go to Retail and commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="2fcd5-124">Voer een datum in het veld Begindatum in.</span><span class="sxs-lookup"><span data-stu-id="2fcd5-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="2fcd5-125">Voer een datum in het veld Einddatum in.</span><span class="sxs-lookup"><span data-stu-id="2fcd5-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="2fcd5-126">Klik in het veld Kanaal op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="2fcd5-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="2fcd5-127">Selecteer in de structuur 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span><span class="sxs-lookup"><span data-stu-id="2fcd5-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="2fcd5-128">Dit toont de standaardhiërarchie voor detailhandelsorganisaties voor detailhandelrapportagedoeleinden.</span><span class="sxs-lookup"><span data-stu-id="2fcd5-128">This shows the default retail organization hierarchy for Retail reporting purpose.</span></span>   <span data-ttu-id="2fcd5-129">Ga naar Organisatiebeheer >Organisaties > Organisatiehiërarchiedoelstellingen en kies Detailhandelrapportage onder Toegewezen hiërarchieën, en controleer de hiërarchienaam waarvoor Standaardkolom is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="2fcd5-129">Go to Organization administration >Organizations >Organization hierarchy purposes and choose Retail reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span>      <span data-ttu-id="2fcd5-130">Als onderdeel van demogegevens (gebruikt voor taakregistratie) ziet u dat Detailhandelwinkels per regio de standaardorganisatiehiërarchie is voor detailhandelrapportagedoeleinden.</span><span class="sxs-lookup"><span data-stu-id="2fcd5-130">As part of demo data (used for this task recording) you would notice, Retail Stores by Region, is the default organization hierarchy for the Retail reporting purpose.</span></span>     
6. <span data-ttu-id="2fcd5-131">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="2fcd5-131">Click OK.</span></span>
7. <span data-ttu-id="2fcd5-132">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="2fcd5-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="2fcd5-133">Een hoofdkantoorrapport exporteren</span><span class="sxs-lookup"><span data-stu-id="2fcd5-133">Export an HQ reports</span></span>
1. <span data-ttu-id="2fcd5-134">Ga naar Detailhandel en commerce > Query's en rapporten > Verkooprapporten > Rapport Verkoop van organisatie.</span><span class="sxs-lookup"><span data-stu-id="2fcd5-134">Go to Retail and commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="2fcd5-135">Voer een datum in het veld Begindatum in.</span><span class="sxs-lookup"><span data-stu-id="2fcd5-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="2fcd5-136">Voer een datum in het veld Einddatum in.</span><span class="sxs-lookup"><span data-stu-id="2fcd5-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="2fcd5-137">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="2fcd5-137">Click OK.</span></span>
5. <span data-ttu-id="2fcd5-138">Klik op Exporteren.</span><span class="sxs-lookup"><span data-stu-id="2fcd5-138">Click Export.</span></span>
6. <span data-ttu-id="2fcd5-139">Klik op PDF.</span><span class="sxs-lookup"><span data-stu-id="2fcd5-139">Click PDF.</span></span>

