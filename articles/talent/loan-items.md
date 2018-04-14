---
title: Artikelen beheren die aan werknemers worden geleend
description: Leenartikelen zijn records waarmee managers de artikelen die uw bedrijf aan werknemers uitleent, bijhouden.
author: kherr75
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmLoanItem, HcmLoanType, HcmPersonLoan
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 3581
ms.assetid: b14bdddb-f10e-4619-9f91-8c88439da862
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ba1b158908ac2328c29f7efe23756248be5be33c
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---

# <a name="manage-items-lent-to-workers"></a><span data-ttu-id="2d2db-103">Artikelen beheren die aan werknemers worden geleend</span><span class="sxs-lookup"><span data-stu-id="2d2db-103">Manage items lent to workers</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="2d2db-104">Leenartikelen zijn records waarmee managers de artikelen die uw bedrijf aan werknemers uitleent, bijhouden.</span><span class="sxs-lookup"><span data-stu-id="2d2db-104">Loan items are records that help managers track the physical items that your company lends to its workers.</span></span> 

<span data-ttu-id="2d2db-105">De volgende punten zijn voorbeelden van artikelen die een bedrijf aan werknemers kan uitlenen:</span><span class="sxs-lookup"><span data-stu-id="2d2db-105">The following points list examples of items that a company might lend to workers:</span></span>
-   <span data-ttu-id="2d2db-106">Mobiele telefoons</span><span class="sxs-lookup"><span data-stu-id="2d2db-106">Mobile telephones</span></span>
-   <span data-ttu-id="2d2db-107">Auto's</span><span class="sxs-lookup"><span data-stu-id="2d2db-107">Automobiles</span></span>
-   <span data-ttu-id="2d2db-108">Computerapparatuur</span><span class="sxs-lookup"><span data-stu-id="2d2db-108">Computer equipment</span></span>

<span data-ttu-id="2d2db-109">Elke fysiek artikel moet een bijbehorend leenartikel hebben.</span><span class="sxs-lookup"><span data-stu-id="2d2db-109">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="2d2db-110">Bij elke leenartikelrecord moet worden beschreven wat er precies wordt uitgeleend, wie ervoor verantwoordelijk is en het aantal dagen dat een artikel aan een medewerker kan worden geleend.</span><span class="sxs-lookup"><span data-stu-id="2d2db-110">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can loaned to a worker.</span></span> <span data-ttu-id="2d2db-111">U kunt meerdere uitleenartikelen maken, voor artikelen zoals sleutels, toegangskaarten of uniformen.</span><span class="sxs-lookup"><span data-stu-id="2d2db-111">You can create multiple loan items, for items such as keys, access cards or uniforms, at the same time.</span></span> 

<span data-ttu-id="2d2db-112">Wanneer een artikel wordt uitgeleend, noteert u de datum waarop het artikel is opgehaald, en de datum waarop het artikel naar verwachting zal worden teruggebracht.</span><span class="sxs-lookup"><span data-stu-id="2d2db-112">When loaning an item, enter the date that the item was loaned, and the planned return date.</span></span> <span data-ttu-id="2d2db-113">Als het geleende artikel weer wordt teruggebracht, noteert u de inleverdatum.</span><span class="sxs-lookup"><span data-stu-id="2d2db-113">When the item is returned, enter the actual return date.</span></span>

<span data-ttu-id="2d2db-114">Werknemers kunnen de records van de artikelen weergeven die aan hen zijn uitgeleend met het werkgebied Selfservice werknemer.</span><span class="sxs-lookup"><span data-stu-id="2d2db-114">Employees can view the records of the items that have been loaned to them using the Employee self-service workspace.</span></span> <span data-ttu-id="2d2db-115">Ze kunnen ook de bestaande records bewerken of nieuwe leenartikelen opgeven als ze extra fysieke artikelen hebben ontvangen.</span><span class="sxs-lookup"><span data-stu-id="2d2db-115">They can also edit the existing records or enter new loan items, if they've received additional physical items.</span></span>  <span data-ttu-id="2d2db-116">Workflow kan worden ingesteld om wijzigingen te routeren naar nieuwe of bestaande leenartikelen via een goedkeuringsproces.</span><span class="sxs-lookup"><span data-stu-id="2d2db-116">Workflow can be set up to route changes to new or existing loan items through an approval process.</span></span> 

<span data-ttu-id="2d2db-117">Managers kunnen geleende artikelen voor hun directe ondergeschikten weergeven.</span><span class="sxs-lookup"><span data-stu-id="2d2db-117">Managers can view loaned items for their direct reports.</span></span> <span data-ttu-id="2d2db-118">Ze kunnen ook gemachtigd worden om nieuwe leenartikelen namens hun werknemers toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="2d2db-118">They can also be granted permission to add new loan items on behalf of their employees.</span></span>

 <a name="account-for-lost-or-misplaced-loan-items"></a><span data-ttu-id="2d2db-119">Rekening voor verloren of beschadigde leenartikelen</span><span class="sxs-lookup"><span data-stu-id="2d2db-119">Account for lost or misplaced loan items</span></span>
-----------------------------------------

<span data-ttu-id="2d2db-120">Als een artikel beschadigd is of verloren raakt, noteert u een fictieve teruggave.</span><span class="sxs-lookup"><span data-stu-id="2d2db-120">If an item becomes damaged or misplaced, enter a fictitious return record.</span></span> <span data-ttu-id="2d2db-121">Vervolgens verwijdert u het artikel of laat u het artikel in het overzicht staan, maar vermeldt u dat het artikel niet meer beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="2d2db-121">Then either delete the item or keep it in the overview and change the description to indicate that the item is not available.</span></span>


<a name="see-also"></a><span data-ttu-id="2d2db-122">Zie ook</span><span class="sxs-lookup"><span data-stu-id="2d2db-122">See also</span></span>
--------

[<span data-ttu-id="2d2db-123">Human resources</span><span class="sxs-lookup"><span data-stu-id="2d2db-123">Human resources</span></span>](index.md)




