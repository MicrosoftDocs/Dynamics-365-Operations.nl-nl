---
title: Delen van financiële gegevens tussen bedrijven configureren
description: Deze procedure laat zien hoe u conflicten configureert, inschakelt, valideert en oplost wanneer gegevens tussen bedrijven worden gedeeld.
author: aprilolson
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr, DMFExecutionHistoryWorkspace, DMFExecutionHistorySummary, DMFExecutionHistoryEntities,  SysDataSharingConfiguration, SysDataSharingDiscrepencies
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dc368351641f3e2432dfdbbaf8eed8694595bd4e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184365"
---
# <a name="configure-financial-cross-company-data-sharing"></a><span data-ttu-id="24167-103">Delen van financiële gegevens tussen bedrijven configureren</span><span class="sxs-lookup"><span data-stu-id="24167-103">Configure financial cross-company data sharing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="24167-104">Deze procedure laat zien hoe u conflicten configureert, inschakelt, valideert en oplost wanneer gegevens tussen bedrijven worden gedeeld.</span><span class="sxs-lookup"><span data-stu-id="24167-104">This procedure shows how to configure, enable, validate, and resolve conflicts when sharing data between companies.</span></span> <span data-ttu-id="24167-105">In deze procedure worden het USMF-bedrijf en de sjabloon voor het delen van financiële gegevens gebruikt.</span><span class="sxs-lookup"><span data-stu-id="24167-105">It uses the USMF company and the Financial data sharing template.</span></span>

<span data-ttu-id="24167-106">Voor deze taakbegeleiding is Dynamics AX platform 7.1 of later vereist.</span><span class="sxs-lookup"><span data-stu-id="24167-106">This task guide requires Dynamics AX platform 7.1 or later.</span></span>

1. <span data-ttu-id="24167-107">Ga naar **Navigatievenster > Modules > Systeembeheer > Werkgebieden > Gegevensbeheer**.</span><span class="sxs-lookup"><span data-stu-id="24167-107">Go to **Navigation pane > Modules > System administration > Workspaces > Data management**.</span></span>
2. <span data-ttu-id="24167-108">Klik op **Importeren**.</span><span class="sxs-lookup"><span data-stu-id="24167-108">Click **Import**.</span></span>
3. <span data-ttu-id="24167-109">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="24167-109">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="24167-110">In het veld **Brongegevensindeling** selecteert u het 'pakkettype'.</span><span class="sxs-lookup"><span data-stu-id="24167-110">In the **Source data format** field, select the 'Package' type.</span></span> <span data-ttu-id="24167-111">Klik op **Uploaden**.</span><span class="sxs-lookup"><span data-stu-id="24167-111">Click **Upload**.</span></span> <span data-ttu-id="24167-112">Navigeer naar de locatie van het sjabloonpakketbestand voor het delen van financiële gegevens en selecteer dat bestand.</span><span class="sxs-lookup"><span data-stu-id="24167-112">Navigate to the location of the Financial data sharing template package file and select that file.</span></span>
5. <span data-ttu-id="24167-113">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="24167-113">Click **Save**.</span></span>
6. <span data-ttu-id="24167-114">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="24167-114">In the list, mark the selected row.</span></span> <span data-ttu-id="24167-115">Selecteer het zojuist gemaakte beleid voor het delen van gegevens.</span><span class="sxs-lookup"><span data-stu-id="24167-115">Select the data sharing policy that was just created.</span></span>  
7. <span data-ttu-id="24167-116">Klik op **Importeren**.</span><span class="sxs-lookup"><span data-stu-id="24167-116">Click **Import**.</span></span>
8. <span data-ttu-id="24167-117">Klik op **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="24167-117">Click **Close**.</span></span>
9. <span data-ttu-id="24167-118">Vernieuw de pagina.</span><span class="sxs-lookup"><span data-stu-id="24167-118">Refresh the page.</span></span>
10. <span data-ttu-id="24167-119">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="24167-119">Close the page.</span></span>
11. <span data-ttu-id="24167-120">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="24167-120">Close the page.</span></span>
12. <span data-ttu-id="24167-121">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="24167-121">Close the page.</span></span>
13. <span data-ttu-id="24167-122">Ga naar **Navigatievenster > Modules > Systeembeheer > Instellen > Delen van gegevens tussen bedrijven configureren**.</span><span class="sxs-lookup"><span data-stu-id="24167-122">Go to **Navigation pane > Modules > System administration > Setup > Configure cross-company data sharing**.</span></span>
14. <span data-ttu-id="24167-123">Zoek en selecteer **Betalingsdagen** in de lijst.</span><span class="sxs-lookup"><span data-stu-id="24167-123">In the list, find and select **Payment days**.</span></span>
15. <span data-ttu-id="24167-124">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="24167-124">Click **Add**.</span></span>
16. <span data-ttu-id="24167-125">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="24167-125">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="24167-126">Typ 'USSI' in het veld **Bedrijf**.</span><span class="sxs-lookup"><span data-stu-id="24167-126">In the **Company** field, type 'USSI'.</span></span>
18. <span data-ttu-id="24167-127">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="24167-127">Click **Add**.</span></span>
19. <span data-ttu-id="24167-128">Typ 'USMF' in het veld **Bedrijf**.</span><span class="sxs-lookup"><span data-stu-id="24167-128">In the **Company** field, type 'USMF'.</span></span>
20. <span data-ttu-id="24167-129">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="24167-129">Click **Save**.</span></span>
21. <span data-ttu-id="24167-130">Klik op **Inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="24167-130">Click **Enable**.</span></span>
22. <span data-ttu-id="24167-131">Klik op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="24167-131">Click **Yes**.</span></span>
23. <span data-ttu-id="24167-132">Klik op **Problemen met delen zoeken**.</span><span class="sxs-lookup"><span data-stu-id="24167-132">Click **Find sharing issues**.</span></span>
24. <span data-ttu-id="24167-133">Klik op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="24167-133">Click **Yes**.</span></span>
25. <span data-ttu-id="24167-134">Klik op **Veldwaarde bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="24167-134">Click **Update field value**.</span></span>
26. <span data-ttu-id="24167-135">Klik op **Waarde van bedrijf 1** gebruiken.</span><span class="sxs-lookup"><span data-stu-id="24167-135">Click **Use value from company 1**.</span></span>
27. <span data-ttu-id="24167-136">Vernieuw de pagina.</span><span class="sxs-lookup"><span data-stu-id="24167-136">Refresh the page.</span></span>
28. <span data-ttu-id="24167-137">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="24167-137">Close the page.</span></span>
