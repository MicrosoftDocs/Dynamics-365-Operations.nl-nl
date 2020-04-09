---
title: Leveranciers goedkeuren voor specifieke aanschaffingscategorieën
description: In dit onderwerp wordt uitgelegd hoe u leveranciers voor specifieke inkoopcategorieën kunt goedkeuren in Dynamics 365 Supply Chain Management.
author: mkirknel
manager: AnnBe
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 135b3a6bea2c0a8940550299504139551c9c3559
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147498"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a><span data-ttu-id="24b9e-103">Leveranciers goedkeuren voor specifieke aanschaffingscategorieën</span><span class="sxs-lookup"><span data-stu-id="24b9e-103">Approve vendors for specific procurement categories</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="24b9e-104">In dit onderwerp wordt uitgelegd hoe u leveranciers voor specifieke inkoopcategorieën kunt goedkeuren in Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="24b9e-104">This topic explains how to approve vendors for specific procurement categories in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="24b9e-105">Wanneer een opdracht tot inkoop is gemaakt, kan er een vereiste zijn om een goedgekeurde leverancier of voorkeursleverancier te selecteren, afhankelijk van hoe het aanschaffingsbeleid is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="24b9e-105">When a purchase requisition is created, there may be a requirement to select an approved or preferred vendor, depending on how the purchasing policies are set up.</span></span> <span data-ttu-id="24b9e-106">Deze procedure laat zien hoe u kunt opgeven dat een leverancier is goedgekeurd of een voorkeursleverancier is voor een specifieke aanschaffingscategorie.</span><span class="sxs-lookup"><span data-stu-id="24b9e-106">This procedure shows you how to specify that a vendor is approved or preferred for a specific procurement category.</span></span> <span data-ttu-id="24b9e-107">Deze taak wordt meestal uitgevoerd door een inkoopmedewerker.</span><span class="sxs-lookup"><span data-stu-id="24b9e-107">This task would usually be carried out by a procurement professional.</span></span> <span data-ttu-id="24b9e-108">U kunt deze procedure gebruiken in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="24b9e-108">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="24b9e-109">Ga in het navigatievenster naar **Modules > Inkoopbeheer > Leveranciers > Alle leveranciers**.</span><span class="sxs-lookup"><span data-stu-id="24b9e-109">In the navigation pane, go to **Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="24b9e-110">Selecteer de leverancier die u als goedgekeurde leverancier of voorkeursleverancier voor een categorie wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="24b9e-110">Select the vendor that you want to set as an approved or preferred vendor for a category.</span></span>
3. <span data-ttu-id="24b9e-111">Selecteer **Algemeen** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="24b9e-111">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="24b9e-112">Selecteer **Categorieën**.</span><span class="sxs-lookup"><span data-stu-id="24b9e-112">Select **Categories**.</span></span>
5. <span data-ttu-id="24b9e-113">Selecteer **Categorie toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="24b9e-113">Select **Add category**.</span></span>
6. <span data-ttu-id="24b9e-114">Selecteer in het veld **Categorie** de optie **OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES)**.</span><span class="sxs-lookup"><span data-stu-id="24b9e-114">In the **Category** field, select **OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES)**.</span></span>
7. <span data-ttu-id="24b9e-115">Selecteer **Voorkeur** in het veld **Categoriestatus leverancier**.</span><span class="sxs-lookup"><span data-stu-id="24b9e-115">In the **Vendor category status** field, select **Preferred**.</span></span> <span data-ttu-id="24b9e-116">Het is mogelijk om meer dan één voorkeursleverancier voor een categorie op te geven.</span><span class="sxs-lookup"><span data-stu-id="24b9e-116">It's possible to specify more than one preferred vendor for a category.</span></span>  
8. <span data-ttu-id="24b9e-117">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="24b9e-117">Select **Save**.</span></span>
9. <span data-ttu-id="24b9e-118">Ga in het navigatievenster naar **Modules > Inkoopbeheer > Aanschaffingscategorieën**.</span><span class="sxs-lookup"><span data-stu-id="24b9e-118">In the navigation pane, go to **Modules > Procurement and sourcing > Procurement categories**.</span></span>
10. <span data-ttu-id="24b9e-119">Selecteer **CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="24b9e-119">In the tree, select **CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES**.</span></span>
11. <span data-ttu-id="24b9e-120">Vouw de sectie **Leveranciers** uit.</span><span class="sxs-lookup"><span data-stu-id="24b9e-120">Expand the **Vendors** section.</span></span> <span data-ttu-id="24b9e-121">Controleer of de geselecteerde leverancier is vermeld als voorkeursleverancier voor de categorie kantoor- en bureau-accessoires.</span><span class="sxs-lookup"><span data-stu-id="24b9e-121">Check if the vendor that you selected appears as a preferred vendor for the Office and desk accessories category.</span></span> <span data-ttu-id="24b9e-122">Als u deze procedure als taakhandleiding uitvoert, moet u mogelijk de knop **Ontgrendelen** selecteren om omlaag naar de lijst met leveranciers te kunnen bladeren.</span><span class="sxs-lookup"><span data-stu-id="24b9e-122">If you're running this procedure as a task guide, you may have to select the **Unlock** button to be able to scroll down to the list of vendors.</span></span>  <span data-ttu-id="24b9e-123">Het is ook mogelijk om voorkeursleveranciers en goedgekeurde leveranciers toe te voegen op deze pagina.</span><span class="sxs-lookup"><span data-stu-id="24b9e-123">It's also possible to add preferred and approved vendors on this page.</span></span>  
12. <span data-ttu-id="24b9e-124">Klik in de structuur op **OFFICE AND DESK ACCESSORIES** en selecteer **Scharen**.</span><span class="sxs-lookup"><span data-stu-id="24b9e-124">In the tree, expand **OFFICE AND DESK ACCESSORIES** and select **Scissors**.</span></span>
13. <span data-ttu-id="24b9e-125">Selecteer **Nee** in het veld **Leveranciers opnemen uit bovenliggende categorie:**.</span><span class="sxs-lookup"><span data-stu-id="24b9e-125">Select **No** in the **Inherit vendors from parent category:** field.</span></span>
14. <span data-ttu-id="24b9e-126">Selecteer **Ja** in het veld **Leveranciers opnemen uit bovenliggende categorie:**.</span><span class="sxs-lookup"><span data-stu-id="24b9e-126">Select **Yes** in the **Inherit vendors from parent category:** field.</span></span>

