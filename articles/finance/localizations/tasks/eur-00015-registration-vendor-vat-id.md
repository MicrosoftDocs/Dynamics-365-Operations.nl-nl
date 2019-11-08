---
title: EUR-00015 Registratie van het btw-id van een leverancier
description: Deze procedure laat zien hoe u btw-registratie-id's en een btw-nummer toevoegt aan een leveranciersrekening.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddress, RegNumTaxIdLookup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 68475c96e7c85cc5a4c540441a4b1f3752ecf0bd
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174682"
---
# <a name="eur-00015-registration-of-vendor-vat-id"></a><span data-ttu-id="fbe62-103">EUR-00015 Registratie van het btw-id van een leverancier</span><span class="sxs-lookup"><span data-stu-id="fbe62-103">EUR-00015 Registration of vendor VAT ID</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fbe62-104">Deze procedure laat zien hoe u btw-registratie-id's en een btw-nummer toevoegt aan een leveranciersrekening.</span><span class="sxs-lookup"><span data-stu-id="fbe62-104">This procedure shows how to add VAT registration IDs and a tax except number to a vendor account.</span></span> <span data-ttu-id="fbe62-105">Dit proces is vergelijkbaar voor rechtspersonen en klanten.</span><span class="sxs-lookup"><span data-stu-id="fbe62-105">This process is similar for legal entities and customers.</span></span> 

<span data-ttu-id="fbe62-106">Voordat u deze procedure kunt uitvoeren, moet u btw-id's instellen.</span><span class="sxs-lookup"><span data-stu-id="fbe62-106">Before you can complete this procedure you must set up VAT IDs.</span></span> <span data-ttu-id="fbe62-107">Deze procedure is van toepassing op alle Europese landen/regio's.</span><span class="sxs-lookup"><span data-stu-id="fbe62-107">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="fbe62-108">De procedure is gemaakt met het demobedrijf DEMF met een primair adres in Duitsland.</span><span class="sxs-lookup"><span data-stu-id="fbe62-108">The procedure was created using the demo data company DEMF with a primary address in Germany.</span></span> <span data-ttu-id="fbe62-109">Deze procedure is bedoeld voor een beheerder van gegevensbeheer, leveranciers of klanten.</span><span class="sxs-lookup"><span data-stu-id="fbe62-109">This procedure is intended for a data management administrator, accounts payable manager, or accounts receivable manager.</span></span> <span data-ttu-id="fbe62-110">Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.</span><span class="sxs-lookup"><span data-stu-id="fbe62-110">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="fbe62-111">Ga naar Leveranciers > Leveranciers > Alle leveranciers.</span><span class="sxs-lookup"><span data-stu-id="fbe62-111">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="fbe62-112">Zoek en selecteer in de lijst klant DE-01001.</span><span class="sxs-lookup"><span data-stu-id="fbe62-112">In the list find and select vendor DE-01001</span></span>
3. <span data-ttu-id="fbe62-113">Klik op Registratie-id's</span><span class="sxs-lookup"><span data-stu-id="fbe62-113">Click Registration IDs.</span></span>
4. <span data-ttu-id="fbe62-114">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="fbe62-114">Click Add.</span></span>
5. <span data-ttu-id="fbe62-115">Selecteer Btw-id.</span><span class="sxs-lookup"><span data-stu-id="fbe62-115">Select VAT ID.</span></span>
6. <span data-ttu-id="fbe62-116">Typ een waarde in het veld Registratienummer.</span><span class="sxs-lookup"><span data-stu-id="fbe62-116">In the Registration number field, type a value.</span></span>
    * <span data-ttu-id="fbe62-117">Geef een btw-id in Duitsland op voor de geselecteerde leverancier.</span><span class="sxs-lookup"><span data-stu-id="fbe62-117">Specify a VAT ID in Germany for the selected vendor.</span></span> <span data-ttu-id="fbe62-118">De id moet overeenkomen met de opgegeven indeling van het registratietype.</span><span class="sxs-lookup"><span data-stu-id="fbe62-118">The ID must match the specified format of the registration type.</span></span>  
7. <span data-ttu-id="fbe62-119">Klik op het tabblad Algemeen.</span><span class="sxs-lookup"><span data-stu-id="fbe62-119">Click the General tab.</span></span>
8. <span data-ttu-id="fbe62-120">Voer een datum in in het veld Ingangsdatum.</span><span class="sxs-lookup"><span data-stu-id="fbe62-120">In the Effective field, enter a date.</span></span>
9. <span data-ttu-id="fbe62-121">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="fbe62-121">Click Save.</span></span>
10. <span data-ttu-id="fbe62-122">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="fbe62-122">Click New.</span></span>
11. <span data-ttu-id="fbe62-123">Typ een waarde in het veld Naam of omschrijving.</span><span class="sxs-lookup"><span data-stu-id="fbe62-123">In the Name or description field, type a value.</span></span>
    * <span data-ttu-id="fbe62-124">Voer bijvoorbeeld ITA in.</span><span class="sxs-lookup"><span data-stu-id="fbe62-124">For example, enter ITA.</span></span>  
12. <span data-ttu-id="fbe62-125">Typ of selecteer een waarde in het veld Land/regio.</span><span class="sxs-lookup"><span data-stu-id="fbe62-125">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="fbe62-126">Selecteer bijvoorbeeld ITA.</span><span class="sxs-lookup"><span data-stu-id="fbe62-126">For example, select ITA.</span></span>  
13. <span data-ttu-id="fbe62-127">Selecteer Ja in het veld Primair voor land/regio.</span><span class="sxs-lookup"><span data-stu-id="fbe62-127">Select Yes in the Primary for country field.</span></span>
14. <span data-ttu-id="fbe62-128">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="fbe62-128">Click Save.</span></span>
15. <span data-ttu-id="fbe62-129">Klik op het tabblad Overzicht.</span><span class="sxs-lookup"><span data-stu-id="fbe62-129">Click the Overview tab.</span></span>
16. <span data-ttu-id="fbe62-130">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="fbe62-130">Click Add.</span></span>
17. <span data-ttu-id="fbe62-131">Typ of selecteer een waarde in het veld Registratietype.</span><span class="sxs-lookup"><span data-stu-id="fbe62-131">In the Registration type field, enter or select a value.</span></span>
    * <span data-ttu-id="fbe62-132">Selecteer bijvoorbeeld Btw-id.</span><span class="sxs-lookup"><span data-stu-id="fbe62-132">For example, select VAT ID.</span></span>  
18. <span data-ttu-id="fbe62-133">Typ een waarde in het veld Registratienummer.</span><span class="sxs-lookup"><span data-stu-id="fbe62-133">In the Registration number field, type a value.</span></span>
    * <span data-ttu-id="fbe62-134">Geef bijvoorbeeld een btw-id in italië op.</span><span class="sxs-lookup"><span data-stu-id="fbe62-134">For example, specify a VAT ID in Italy.</span></span>  <span data-ttu-id="fbe62-135">De id moet overeenkomen met de indeling van het registratietype.</span><span class="sxs-lookup"><span data-stu-id="fbe62-135">The ID must have the same format as the registration type.</span></span>  
19. <span data-ttu-id="fbe62-136">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="fbe62-136">Click Save.</span></span>
20. <span data-ttu-id="fbe62-137">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="fbe62-137">Close the page.</span></span>
21. <span data-ttu-id="fbe62-138">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="fbe62-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="fbe62-139">Selecteer bijvoorbeeld DE-01001.</span><span class="sxs-lookup"><span data-stu-id="fbe62-139">For example, select DE-01001.</span></span>  
22. <span data-ttu-id="fbe62-140">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="fbe62-140">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="fbe62-141">Vouw de sectie Factuur en levering uit.</span><span class="sxs-lookup"><span data-stu-id="fbe62-141">Expand the Invoice and delivery section.</span></span>
24. <span data-ttu-id="fbe62-142">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="fbe62-142">Click Edit.</span></span>
25. <span data-ttu-id="fbe62-143">Typ of selecteer een waarde in het veld Nummer van belastingvrijstelling.</span><span class="sxs-lookup"><span data-stu-id="fbe62-143">In the Tax exempt number field, enter or select a value.</span></span>
26. <span data-ttu-id="fbe62-144">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="fbe62-144">Click Save.</span></span>
