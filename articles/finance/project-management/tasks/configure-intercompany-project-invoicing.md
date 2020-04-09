---
title: Intercompany-projectfacturering configureren
description: In dit onderwerp ziet u hoe u projectfacturen configureert tussen twee bedrijven in uw organisatie.
author: KimANelson
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 31dbae2d37aefe1841fe85cb6caf185c78596e55
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144274"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="0cd0f-103">Intercompany-projectfacturering configureren</span><span class="sxs-lookup"><span data-stu-id="0cd0f-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0cd0f-104">In dit onderwerp ziet u hoe u projectfacturen configureert tussen twee bedrijven in uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="0cd0f-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="0cd0f-105">In deze taak wordt de gegevensset van USSI gebruikt.</span><span class="sxs-lookup"><span data-stu-id="0cd0f-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="0cd0f-106">Ga in het navigatievenster naar **Modules > Leveranciers > Leveranciers > Alle leveranciers**.</span><span class="sxs-lookup"><span data-stu-id="0cd0f-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="0cd0f-107">Zoek in de lijst **Alle leveranciers** de gewenste record en selecteer deze.</span><span class="sxs-lookup"><span data-stu-id="0cd0f-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="0cd0f-108">Selecteer **Algemeen** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="0cd0f-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="0cd0f-109">Selecteer **Intercompany**.</span><span class="sxs-lookup"><span data-stu-id="0cd0f-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="0cd0f-110">Stel **Actief** in op **Ja** om handel tussen bedrijven (intercompany) in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="0cd0f-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="0cd0f-111">Typ of selecteer een waarde in het veld **Bedrijf van klant**.</span><span class="sxs-lookup"><span data-stu-id="0cd0f-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="0cd0f-112">Typ of selecteer een waarde in het veld **Mijn rekening**.</span><span class="sxs-lookup"><span data-stu-id="0cd0f-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="0cd0f-113">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="0cd0f-113">Select **Save**.</span></span>
9. <span data-ttu-id="0cd0f-114">Sluit de pagina's om terug te keren naar de startpagina.</span><span class="sxs-lookup"><span data-stu-id="0cd0f-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="0cd0f-115">Ga in het navigatievenster naar **Modules > Projectbeheer en boekhouding > Instellingen > Projectbeheer- en boekhoudingsparameters**.</span><span class="sxs-lookup"><span data-stu-id="0cd0f-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="0cd0f-116">Selecteer het tabblad **Intercompany**.</span><span class="sxs-lookup"><span data-stu-id="0cd0f-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="0cd0f-117">Verplaats de schuifregelaar naar **Ja** om Intercompany-resourceplanning en urenstaten in te schakelen</span><span class="sxs-lookup"><span data-stu-id="0cd0f-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="0cd0f-118">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="0cd0f-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="0cd0f-119">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="0cd0f-119">Select **New**.</span></span>
15. <span data-ttu-id="0cd0f-120">Typ of selecteer een waarde in het veld **Lenende rechtspersoon**.</span><span class="sxs-lookup"><span data-stu-id="0cd0f-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="0cd0f-121">Schakel het selectievakje **Opbrengst samenvoegen** in.</span><span class="sxs-lookup"><span data-stu-id="0cd0f-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="0cd0f-122">Typ of selecteer een waarde in het veld **Standaardcategorie voor urenstaat**.</span><span class="sxs-lookup"><span data-stu-id="0cd0f-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="0cd0f-123">Typ of selecteer een waarde in het veld **Standaardcategorie voor onkosten**.</span><span class="sxs-lookup"><span data-stu-id="0cd0f-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="0cd0f-124">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="0cd0f-124">Select **Save**.</span></span>
20. <span data-ttu-id="0cd0f-125">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="0cd0f-125">Close the page.</span></span>
21. <span data-ttu-id="0cd0f-126">Ga in het navigatievenster naar **Modules > Projectbeheer en boekhouding > Instellingen > Boeking > Instellingen boeking in grootboek**.</span><span class="sxs-lookup"><span data-stu-id="0cd0f-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="0cd0f-127">Selecteer een optie in het veld **Grootboekrekeningtypen**.</span><span class="sxs-lookup"><span data-stu-id="0cd0f-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="0cd0f-128">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="0cd0f-128">Select **New**.</span></span>
24. <span data-ttu-id="0cd0f-129">Geef in het veld **Hoofdrekening** van de nieuwe rij de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="0cd0f-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="0cd0f-130">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="0cd0f-130">Select **Save**.</span></span>
26. <span data-ttu-id="0cd0f-131">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="0cd0f-131">Close the page.</span></span>
27. <span data-ttu-id="0cd0f-132">Ga in het navigatievenster naar **Modules > Projectbeheer en boekhouding > Instellingen > Prijzen > Prijs overboeken**.</span><span class="sxs-lookup"><span data-stu-id="0cd0f-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="0cd0f-133">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="0cd0f-133">Select **New**.</span></span>
29. <span data-ttu-id="0cd0f-134">Voer een datum in het veld **Begindatum** in.</span><span class="sxs-lookup"><span data-stu-id="0cd0f-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="0cd0f-135">Typ of selecteer een waarde in het veld **Lenende rechtspersoon**.</span><span class="sxs-lookup"><span data-stu-id="0cd0f-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="0cd0f-136">Selecteer een optie in het veld **Overboeking prijsmodel**.</span><span class="sxs-lookup"><span data-stu-id="0cd0f-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="0cd0f-137">Voer in het veld **Prijscalculatie** een getal in.</span><span class="sxs-lookup"><span data-stu-id="0cd0f-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="0cd0f-138">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="0cd0f-138">Select **Save**.</span></span>

