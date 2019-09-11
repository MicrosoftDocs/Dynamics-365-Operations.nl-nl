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
ms.openlocfilehash: c89b17c09a4f145b5a4ca9cdd127b4e635447d4b
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867314"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="c76b4-103">Intercompany-projectfacturering configureren</span><span class="sxs-lookup"><span data-stu-id="c76b4-103">Configure intercompany project invoicing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c76b4-104">In dit onderwerp ziet u hoe u projectfacturen configureert tussen twee bedrijven in uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="c76b4-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="c76b4-105">In deze taak wordt de gegevensset van USSI gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c76b4-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="c76b4-106">Ga in het navigatievenster naar **Modules > Leveranciers > Leveranciers > Alle leveranciers**.</span><span class="sxs-lookup"><span data-stu-id="c76b4-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="c76b4-107">Zoek in de lijst **Alle leveranciers** de gewenste record en selecteer deze.</span><span class="sxs-lookup"><span data-stu-id="c76b4-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="c76b4-108">Selecteer **Algemeen** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="c76b4-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="c76b4-109">Selecteer **Intercompany**.</span><span class="sxs-lookup"><span data-stu-id="c76b4-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="c76b4-110">Stel **Actief** in op **Ja** om handel tussen bedrijven (intercompany) in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="c76b4-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="c76b4-111">Typ of selecteer een waarde in het veld **Bedrijf van klant**.</span><span class="sxs-lookup"><span data-stu-id="c76b4-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="c76b4-112">Typ of selecteer een waarde in het veld **Mijn rekening**.</span><span class="sxs-lookup"><span data-stu-id="c76b4-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="c76b4-113">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c76b4-113">Select **Save**.</span></span>
9. <span data-ttu-id="c76b4-114">Sluit de pagina's om terug te keren naar de startpagina.</span><span class="sxs-lookup"><span data-stu-id="c76b4-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="c76b4-115">Ga in het navigatievenster naar **Modules > Projectbeheer en boekhouding > Instellingen > Projectbeheer- en boekhoudingsparameters**.</span><span class="sxs-lookup"><span data-stu-id="c76b4-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="c76b4-116">Selecteer het tabblad **Intercompany**.</span><span class="sxs-lookup"><span data-stu-id="c76b4-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="c76b4-117">Verplaats de schuifregelaar naar **Ja** om Intercompany-resourceplanning en urenstaten in te schakelen</span><span class="sxs-lookup"><span data-stu-id="c76b4-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="c76b4-118">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c76b4-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="c76b4-119">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="c76b4-119">Select **New**.</span></span>
15. <span data-ttu-id="c76b4-120">Typ of selecteer een waarde in het veld **Lenende rechtspersoon**.</span><span class="sxs-lookup"><span data-stu-id="c76b4-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="c76b4-121">Schakel het selectievakje **Opbrengst samenvoegen** in.</span><span class="sxs-lookup"><span data-stu-id="c76b4-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="c76b4-122">Typ of selecteer een waarde in het veld **Standaardcategorie voor urenstaat**.</span><span class="sxs-lookup"><span data-stu-id="c76b4-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="c76b4-123">Typ of selecteer een waarde in het veld **Standaardcategorie voor onkosten**.</span><span class="sxs-lookup"><span data-stu-id="c76b4-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="c76b4-124">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c76b4-124">Select **Save**.</span></span>
20. <span data-ttu-id="c76b4-125">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="c76b4-125">Close the page.</span></span>
21. <span data-ttu-id="c76b4-126">Ga in het navigatievenster naar **Modules > Projectbeheer en boekhouding > Instellingen > Boeking > Instellingen boeking in grootboek**.</span><span class="sxs-lookup"><span data-stu-id="c76b4-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="c76b4-127">Selecteer een optie in het veld **Grootboekrekeningtypen**.</span><span class="sxs-lookup"><span data-stu-id="c76b4-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="c76b4-128">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="c76b4-128">Select **New**.</span></span>
24. <span data-ttu-id="c76b4-129">Geef in het veld **Hoofdrekening** van de nieuwe rij de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="c76b4-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="c76b4-130">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c76b4-130">Select **Save**.</span></span>
26. <span data-ttu-id="c76b4-131">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="c76b4-131">Close the page.</span></span>
27. <span data-ttu-id="c76b4-132">Ga in het navigatievenster naar **Modules > Projectbeheer en boekhouding > Instellingen > Prijzen > Prijs overboeken**.</span><span class="sxs-lookup"><span data-stu-id="c76b4-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="c76b4-133">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="c76b4-133">Select **New**.</span></span>
29. <span data-ttu-id="c76b4-134">Voer een datum in het veld **Begindatum** in.</span><span class="sxs-lookup"><span data-stu-id="c76b4-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="c76b4-135">Typ of selecteer een waarde in het veld **Lenende rechtspersoon**.</span><span class="sxs-lookup"><span data-stu-id="c76b4-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="c76b4-136">Selecteer een optie in het veld **Overboeking prijsmodel**.</span><span class="sxs-lookup"><span data-stu-id="c76b4-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="c76b4-137">Voer in het veld **Prijscalculatie** een getal in.</span><span class="sxs-lookup"><span data-stu-id="c76b4-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="c76b4-138">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c76b4-138">Select **Save**.</span></span>

