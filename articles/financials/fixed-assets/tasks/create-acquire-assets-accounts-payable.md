--- 
title: Activa vanuit Leveranciers maken en aanschaffen
description: Deze taakbegeleiding doorloopt het maken en bijboeken van vaste activa met het inkoopproces.
author: saraschi2
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c483622346bf61d0805402ae4ae8d2ba7c7aed89
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---
# <a name="create-and-acquire-assets-from-accounts-payable"></a><span data-ttu-id="257aa-103">Activa vanuit Leveranciers maken en aanschaffen</span><span class="sxs-lookup"><span data-stu-id="257aa-103">Create and acquire assets from accounts payable</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="257aa-104">Deze taakbegeleiding doorloopt het maken en bijboeken van vaste activa met het inkoopproces.</span><span class="sxs-lookup"><span data-stu-id="257aa-104">This task guide will walk through creation and acquisition of a fixed asset with the purchasing process.</span></span>  <span data-ttu-id="257aa-105">Het gebruikt de accountant en Leveranciersmedewerker en het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="257aa-105">It uses the Accountant and Accounts payable clerks and the demo company USMF .</span></span>


## <a name="set-fixed-assets-parameters"></a><span data-ttu-id="257aa-106">Parameters voor vaste activa instellen</span><span class="sxs-lookup"><span data-stu-id="257aa-106">Set Fixed assets parameters</span></span>
1. <span data-ttu-id="257aa-107">Ga naar Vaste activa > Instellen > Parameters vaste activa.</span><span class="sxs-lookup"><span data-stu-id="257aa-107">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="257aa-108">Vouw de sectie Inkooporders uit of samen.</span><span class="sxs-lookup"><span data-stu-id="257aa-108">Expand or collapse the Purchase orders section.</span></span>
3. <span data-ttu-id="257aa-109">Schakel het selectievakje Bijboekingen van activa vanuit Inkoop toestaan in.</span><span class="sxs-lookup"><span data-stu-id="257aa-109">Check the Allow asset acquisition from Purchasing checkbox.</span></span>
4. <span data-ttu-id="257aa-110">Schakel het selectievakje Activum maken tijdens boeken van productontvangstbon of factuur in.</span><span class="sxs-lookup"><span data-stu-id="257aa-110">Check the Create asset during product receipt or invoice posting checkbox.</span></span>

## <a name="create-a-new-vendor-invoice"></a><span data-ttu-id="257aa-111">Een nieuwe leveranciersfactuur maken</span><span class="sxs-lookup"><span data-stu-id="257aa-111">Create a new vendor invoice</span></span>
1. <span data-ttu-id="257aa-112">Ga naar Leveranciers > Werkruimten > Leveranciersfactuurregistratie.</span><span class="sxs-lookup"><span data-stu-id="257aa-112">Go to Accounts payable > Workspaces > Vendor invoice entry.</span></span>
2. <span data-ttu-id="257aa-113">Klik op Nieuwe leveranciersfactuur.</span><span class="sxs-lookup"><span data-stu-id="257aa-113">Click New vendor invoice.</span></span>
3. <span data-ttu-id="257aa-114">Klik in het veld Factuurrekening op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="257aa-114">In the Invoice account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="257aa-115">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="257aa-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="257aa-116">Typ een waarde in het veld Nummer.</span><span class="sxs-lookup"><span data-stu-id="257aa-116">In the Number field, type a value.</span></span>
6. <span data-ttu-id="257aa-117">Voer in het veld Boekingsdatum een datum in.</span><span class="sxs-lookup"><span data-stu-id="257aa-117">In the Posting date field, enter a date.</span></span>
7. <span data-ttu-id="257aa-118">Klik op Regel toevoegen.</span><span class="sxs-lookup"><span data-stu-id="257aa-118">Click Add line.</span></span>
8. <span data-ttu-id="257aa-119">Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="257aa-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="257aa-120">Of de niet-opgeslagen artikelen of de inkoopcategorieën kunnen worden gebruikt voor bijboeking van vaste activa.</span><span class="sxs-lookup"><span data-stu-id="257aa-120">Either non-stocked items or procurement categories can be used for fixed asset acquisition.</span></span>  
9. <span data-ttu-id="257aa-121">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="257aa-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="257aa-122">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="257aa-122">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="257aa-123">Eén factuurregel maakt slechts één vast activum, ongeacht de hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="257aa-123">One invoice line will only create one fixed asset, regardless of quantity.</span></span>  <span data-ttu-id="257aa-124">De waarde van het veld voor de factuurhoeveelheid wordt overgebracht naar de vaste-activahoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="257aa-124">The invoice quantity field value will be transferred to the fixed asset quantity.</span></span>  
11. <span data-ttu-id="257aa-125">Voer in het veld Eenheidsprijs een getal in.</span><span class="sxs-lookup"><span data-stu-id="257aa-125">In the Unit price field, enter a number.</span></span>
12. <span data-ttu-id="257aa-126">Vouw de sectie Regeldetails uit of samen.</span><span class="sxs-lookup"><span data-stu-id="257aa-126">Expand or collapse the Line details section.</span></span>
13. <span data-ttu-id="257aa-127">Klik op het tabblad Vaste activa.</span><span class="sxs-lookup"><span data-stu-id="257aa-127">Click the Fixed assets tab.</span></span>
14. <span data-ttu-id="257aa-128">Schakel het selectievakje Een nieuw vast activum maken in.</span><span class="sxs-lookup"><span data-stu-id="257aa-128">Check the Create a new fixed asset checkbox.</span></span>
15. <span data-ttu-id="257aa-129">Klik in het veld Groep vaste activa op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="257aa-129">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="257aa-130">Selecteer in de lijst de groep vaste activa die moet worden gebruikt als de nieuwe vaste activa worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="257aa-130">In the list, select the fixed asset group to be used when creating the new fixed asset.</span></span>
17. <span data-ttu-id="257aa-131">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="257aa-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="257aa-132">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="257aa-132">Click Post.</span></span>
    * <span data-ttu-id="257aa-133">Het vaste activum wordt gemaakt en bijgeboekt wanneer de factuur wordt geboekt.</span><span class="sxs-lookup"><span data-stu-id="257aa-133">The fixed asset will be created and acquired when the invoice is posted.</span></span>  


