---
title: Leveranciers goedkeuren voor specifieke aanschaffingscategorieën
description: Wanneer een opdracht tot inkoop is gemaakt, kan er een vereiste zijn om een goedgekeurde leverancier of voorkeursleverancier te selecteren, afhankelijk van hoe het aanschaffingsbeleid is ingesteld.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b783d1ce8f02ad119dc6768e6d9cd3c61ae07e70
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566428"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a><span data-ttu-id="9577e-103">Leveranciers goedkeuren voor specifieke aanschaffingscategorieën</span><span class="sxs-lookup"><span data-stu-id="9577e-103">Approve vendors for specific procurement categories</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9577e-104">Wanneer een opdracht tot inkoop is gemaakt, kan er een vereiste zijn om een goedgekeurde leverancier of voorkeursleverancier te selecteren, afhankelijk van hoe het aanschaffingsbeleid is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="9577e-104">When a purchase requisition is created, there may be a requirement to select an approved or preferred vendor, depending on how the purchasing policies are set up.</span></span> <span data-ttu-id="9577e-105">Deze procedure laat zien hoe u kunt opgeven dat een leverancier is goedgekeurd of een voorkeursleverancier is voor een specifieke aanschaffingscategorie.</span><span class="sxs-lookup"><span data-stu-id="9577e-105">This procedure shows you how to specify that a vendor is approved or preferred for a specific procurement category.</span></span> <span data-ttu-id="9577e-106">Deze taak wordt meestal uitgevoerd door een inkoopmedewerker.</span><span class="sxs-lookup"><span data-stu-id="9577e-106">This task would usually be carried out by a procurement professional.</span></span> <span data-ttu-id="9577e-107">U kunt deze procedure gebruiken in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="9577e-107">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="9577e-108">Ga naar Inkoop en sourcing > Leveranciers > Alle leveranciers.</span><span class="sxs-lookup"><span data-stu-id="9577e-108">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="9577e-109">Selecteer de leverancier die u als goedgekeurde leverancier of voorkeursleverancier voor een categorie wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="9577e-109">Select the vendor that you want to set as an approved or preferred vendor for a category.</span></span>
3. <span data-ttu-id="9577e-110">Klik in het actievenster op Algemeen.</span><span class="sxs-lookup"><span data-stu-id="9577e-110">On the Action Pane, click General.</span></span>
4. <span data-ttu-id="9577e-111">Klik op Categorieën.</span><span class="sxs-lookup"><span data-stu-id="9577e-111">Click Categories.</span></span>
5. <span data-ttu-id="9577e-112">Klik op Categorie toevoegen.</span><span class="sxs-lookup"><span data-stu-id="9577e-112">Click Add category.</span></span>
6. <span data-ttu-id="9577e-113">Selecteer in het veld Categorie de optie OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES).</span><span class="sxs-lookup"><span data-stu-id="9577e-113">In the Category field, select OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES).</span></span>
7. <span data-ttu-id="9577e-114">Selecteer 'Voorkeur' in het veld Categoriestatus leverancier.</span><span class="sxs-lookup"><span data-stu-id="9577e-114">In the Vendor category status field, select 'Preferred'.</span></span>
    * <span data-ttu-id="9577e-115">Het is mogelijk om meer dan één voorkeursleverancier voor een categorie op te geven.</span><span class="sxs-lookup"><span data-stu-id="9577e-115">It’s possible to specify more than one preferred vendor for a category.</span></span>  
8. <span data-ttu-id="9577e-116">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="9577e-116">Click Save.</span></span>
9. <span data-ttu-id="9577e-117">Ga naar Inkoop en sourcing > Inkoopcategorieën.</span><span class="sxs-lookup"><span data-stu-id="9577e-117">Go to Procurement and sourcing > Procurement categories.</span></span>
10. <span data-ttu-id="9577e-118">Selecteer 'CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="9577e-118">In the tree, select 'CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES'.</span></span>
11. <span data-ttu-id="9577e-119">Vouw de sectie Leveranciers uit.</span><span class="sxs-lookup"><span data-stu-id="9577e-119">Expand the Vendors section.</span></span>
    * <span data-ttu-id="9577e-120">Controleer of de leverancier die u hebt geselecteerd als voorkeursleverancier voor kantoor- en bureau-accessoires staat vermeld.</span><span class="sxs-lookup"><span data-stu-id="9577e-120">Check if the vendor that you selected  appears as a preferred vendor for the Office and desk accessories category.</span></span> <span data-ttu-id="9577e-121">Als u deze procedure als taakhandleiding uitvoert, moet u mogelijk op de knop Ontgrendelen klikken om omlaag naar de lijst met leveranciers te kunnen bladeren.</span><span class="sxs-lookup"><span data-stu-id="9577e-121">If you’re running this procedure as a task guide, you may have to click the Unlock button to be able to scroll down to the list of vendors.</span></span>  <span data-ttu-id="9577e-122">Het is ook mogelijk om voorkeursleveranciers en goedgekeurde leveranciers toe te voegen op deze pagina.</span><span class="sxs-lookup"><span data-stu-id="9577e-122">It’s also possible to add preferred and approved vendors on this page.</span></span>  
12. <span data-ttu-id="9577e-123">Vouw 'OFFICE AND DESK ACCESSORIES' uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="9577e-123">In the tree, expand 'OFFICE AND DESK ACCESSORIES'.</span></span>
13. <span data-ttu-id="9577e-124">Selecteer 'Scharen' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="9577e-124">In the tree, select 'Scissors'.</span></span>
14. <span data-ttu-id="9577e-125">Selecteer Nee in het veld Leveranciers opnemen uit bovenliggende categorie:.</span><span class="sxs-lookup"><span data-stu-id="9577e-125">Select No in the Inherit vendors from parent category: field.</span></span>
15. <span data-ttu-id="9577e-126">Selecteer Ja in het veld Leveranciers opnemen uit bovenliggende categorie:.</span><span class="sxs-lookup"><span data-stu-id="9577e-126">Select Yes in the Inherit vendors from parent category: field.</span></span>

