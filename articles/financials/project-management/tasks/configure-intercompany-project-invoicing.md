---
title: Intercompany-projectfacturering configureren
description: In deze procedure ziet u hoe u projectfacturen configureert tussen twee bedrijven in uw organisatie.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2fe06978d3a1c41a1133a568cca61df05b49d235
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "352753"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="e113b-103">Intercompany-projectfacturering configureren</span><span class="sxs-lookup"><span data-stu-id="e113b-103">Configure intercompany project invoicing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e113b-104">In deze procedure ziet u hoe u projectfacturen configureert tussen twee bedrijven in uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="e113b-104">This procedure shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="e113b-105">In deze taak wordt de gegevensset van USSI gebruikt.</span><span class="sxs-lookup"><span data-stu-id="e113b-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="e113b-106">Ga naar Leveranciers > Leveranciers > Alle leveranciers.</span><span class="sxs-lookup"><span data-stu-id="e113b-106">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="e113b-107">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="e113b-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="e113b-108">Klik in het actievenster op Algemeen.</span><span class="sxs-lookup"><span data-stu-id="e113b-108">On the Action Pane, click General.</span></span>
4. <span data-ttu-id="e113b-109">Klik op Intercompany.</span><span class="sxs-lookup"><span data-stu-id="e113b-109">Click Intercompany.</span></span>
5. <span data-ttu-id="e113b-110">Stel Actief in op Ja om handel tussen bedrijven (intercompany) in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="e113b-110">Set Active to Yes to enable intercompany trading.</span></span>
6. <span data-ttu-id="e113b-111">Typ of selecteer een waarde in het veld Bedrijf van klant.</span><span class="sxs-lookup"><span data-stu-id="e113b-111">In the Customer company field, enter or select a value.</span></span>
7. <span data-ttu-id="e113b-112">Typ of selecteer een waarde in het veld Mijn rekening.</span><span class="sxs-lookup"><span data-stu-id="e113b-112">In the My account field, enter or select a value.</span></span>
8. <span data-ttu-id="e113b-113">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="e113b-113">Click Save.</span></span>
9. <span data-ttu-id="e113b-114">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e113b-114">Close the page.</span></span>
10. <span data-ttu-id="e113b-115">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e113b-115">Close the page.</span></span>
11. <span data-ttu-id="e113b-116">Ga naar Projectbeheer- en boekhouding > Instellingen > Projectbeheer- en boekhoudingsparameters.</span><span class="sxs-lookup"><span data-stu-id="e113b-116">Go to Project management and accounting > Setup > Project management and accounting parameters.</span></span>
12. <span data-ttu-id="e113b-117">Klik op het tabblad Intercompany.</span><span class="sxs-lookup"><span data-stu-id="e113b-117">Click the Intercompany tab.</span></span>
13. <span data-ttu-id="e113b-118">Verplaats de schuifregelaar naar Ja om Intercompany-resourceplanning en urenstaten in te schakelen</span><span class="sxs-lookup"><span data-stu-id="e113b-118">Move the slider to Yes to enable intercompany resource scheduling and timesheets.</span></span>
14. <span data-ttu-id="e113b-119">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e113b-119">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="e113b-120">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="e113b-120">Click New.</span></span>
16. <span data-ttu-id="e113b-121">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e113b-121">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="e113b-122">Typ of selecteer een waarde in het veld Lenende rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="e113b-122">In the Borrowing legal entity field, enter or select a value.</span></span>
18. <span data-ttu-id="e113b-123">Schakel het selectievakje Opbrengst samenvoegen in.</span><span class="sxs-lookup"><span data-stu-id="e113b-123">Select the Accrue revenue check box.</span></span>
19. <span data-ttu-id="e113b-124">Typ of selecteer een waarde in het veld Standaardcategorie voor urenstaat.</span><span class="sxs-lookup"><span data-stu-id="e113b-124">In the Default timesheet category field, enter or select a value.</span></span>
20. <span data-ttu-id="e113b-125">Typ of selecteer een waarde in het veld Standaardcategorie voor onkosten.</span><span class="sxs-lookup"><span data-stu-id="e113b-125">In the Default expense category field, enter or select a value.</span></span>
21. <span data-ttu-id="e113b-126">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="e113b-126">Click Save.</span></span>
22. <span data-ttu-id="e113b-127">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e113b-127">Close the page.</span></span>
23. <span data-ttu-id="e113b-128">Ga naar Projectbeheer en boekhouding > Instellingen > Boeken > Boeking in grootboek instellen.</span><span class="sxs-lookup"><span data-stu-id="e113b-128">Go to Project management and accounting > Setup > Posting > Ledger posting setup.</span></span>
24. <span data-ttu-id="e113b-129">Selecteer een optie in het veld Grootboekrekeningtypen.</span><span class="sxs-lookup"><span data-stu-id="e113b-129">In the Ledger account types field, select an option.</span></span>
25. <span data-ttu-id="e113b-130">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="e113b-130">Click New.</span></span>
26. <span data-ttu-id="e113b-131">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e113b-131">In the list, mark the selected row.</span></span>
27. <span data-ttu-id="e113b-132">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e113b-132">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="e113b-133">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="e113b-133">In the Main account field, specify the desired values.</span></span>
29. <span data-ttu-id="e113b-134">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="e113b-134">Click Save.</span></span>
30. <span data-ttu-id="e113b-135">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e113b-135">Close the page.</span></span>
31. <span data-ttu-id="e113b-136">Ga naar Projectbeheer en boekhouding > Instellingen > Prijzen > Prijs overboeken.</span><span class="sxs-lookup"><span data-stu-id="e113b-136">Go to Project management and accounting > Setup > Prices > Transfer price.</span></span>
32. <span data-ttu-id="e113b-137">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="e113b-137">Click New.</span></span>
33. <span data-ttu-id="e113b-138">Voer een datum in het veld Begindatum in.</span><span class="sxs-lookup"><span data-stu-id="e113b-138">In the Effective date field, enter a date.</span></span>
34. <span data-ttu-id="e113b-139">Typ of selecteer een waarde in het veld Lenende rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="e113b-139">In the Borrowing legal entity field, enter or select a value.</span></span>
35. <span data-ttu-id="e113b-140">Selecteer een optie in het veld Overboeking prijsmodel.</span><span class="sxs-lookup"><span data-stu-id="e113b-140">In the Transfer price model field, select an option.</span></span>
36. <span data-ttu-id="e113b-141">Voer in het veld Prijscalculatie een getal in.</span><span class="sxs-lookup"><span data-stu-id="e113b-141">In the Pricing field, enter a number.</span></span>
37. <span data-ttu-id="e113b-142">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="e113b-142">Click Save.</span></span>

