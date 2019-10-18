---
title: Prognoses voor onderhoud
description: In dit onderwerp wordt uitgelegd wat prognoses voor onderhoud zijn in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 383c910b40199f2da863144c6dc85a579d0091e9
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024494"
---
# <a name="maintenance-forecasts"></a><span data-ttu-id="10002-103">Prognoses voor onderhoud</span><span class="sxs-lookup"><span data-stu-id="10002-103">Maintenance forecasts</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="10002-104">Wanneer u een werkorder maakt, kunt u werkordertaken maken met gerelateerde activa en typen onderhoudstaken.</span><span class="sxs-lookup"><span data-stu-id="10002-104">When you create a work order, you create work order jobs with related assets and maintenance job types.</span></span> <span data-ttu-id="10002-105">Wanneer u een type onderhoudstaak selecteert dat prognoses voor onderhoud bevat, worden de prognoses automatisch naar de werkorder gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="10002-105">When you select a maintenance job type containing maintenance forecasts, the forecasts are automatically copied to the work order.</span></span>

<span data-ttu-id="10002-106">U kunt mogelijk prognoseregels toevoegen aan of verwijderen uit een werkorder.</span><span class="sxs-lookup"><span data-stu-id="10002-106">You may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="10002-107">De instelling van de levenscyclusstatus van een werkorder, het gerelateerde projecttype en de faseregels die betrekking hebben op het projecttype bepalen of u prognoseregels kunt toevoegen of bewerken.</span><span class="sxs-lookup"><span data-stu-id="10002-107">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determines if you are able to add or edit forecast lines.</span></span> 

1. <span data-ttu-id="10002-108">Klik op **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.</span><span class="sxs-lookup"><span data-stu-id="10002-108">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="10002-109">Selecteer de werkorder in de lijst en klik op **Prognose**.</span><span class="sxs-lookup"><span data-stu-id="10002-109">Select the work order in the list, and click **Forecast**.</span></span> <span data-ttu-id="10002-110">In **Prognose voor onderhoud** worden de prognoseregels van het type onderhoudstaak dat in de werkordertaak is geselecteerd, weergegeven.</span><span class="sxs-lookup"><span data-stu-id="10002-110">In **Work order maintenance forecast**, forecast lines from the maintenance job type selected on the work order job are displayed.</span></span>


## <a name="add-hours-forecast-to-a-work-order"></a><span data-ttu-id="10002-111">Urenprognose aan een werkorder toevoegen</span><span class="sxs-lookup"><span data-stu-id="10002-111">Add hours forecast to a work order</span></span>

1. <span data-ttu-id="10002-112">Selecteer de werkordertaak waaraan u een prognose wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="10002-112">Select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="10002-113">Ga naar het sneltabblad **Uren** en klik op **Toevoegen** om een nieuwe regel te maken.</span><span class="sxs-lookup"><span data-stu-id="10002-113">On the **Hours** FastTab, click **Add** to create a new line.</span></span>

3. <span data-ttu-id="10002-114">Selecteer een categorie in het veld **Categorie**.</span><span class="sxs-lookup"><span data-stu-id="10002-114">Select a category in the **Category** field.</span></span>

4. <span data-ttu-id="10002-115">Voer het aantal voorspelde uren in het veld **Uren** in.</span><span class="sxs-lookup"><span data-stu-id="10002-115">Insert number of forecasted hours in the **Hours** field.</span></span>

5. <span data-ttu-id="10002-116">Selecteer in het veld **Regeleigenschap** het toeslagtype dat op de regel moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="10002-116">In the **Line property** field, select the charge type to be used on the line.</span></span>


## <a name="add-items-forecast-to-a-work-order"></a><span data-ttu-id="10002-117">Artikelen toevoegen aan een werkorder</span><span class="sxs-lookup"><span data-stu-id="10002-117">Add items forecast to a work order</span></span>

<span data-ttu-id="10002-118">Er zijn drie manieren om artikelen aan een prognose voor werkorderonderhoud toe te voegen: u kunt regels maken voor artikelen (reserve-onderdelen) die niet zijn opgenomen in de lijst met reserve-onderdelen of activumstuklijst, u kunt reserve-onderdelen selecteren in de lijst met goedgekeurde onderdelen en u kunt artikelen selecteren in de activumstuklijst.</span><span class="sxs-lookup"><span data-stu-id="10002-118">There are three ways to add items to a work order maintenance forecast: You can create lines for items (spare parts) that are not included in the spare parts list or asset BOM, you can select spare parts from the approved spare parts list, and you can select items from the asset BOM.</span></span>

1. <span data-ttu-id="10002-119">Selecteer de werkordertaak waaraan u een prognose wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="10002-119">Select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="10002-120">Selecteer het sneltabblad **Artikelen**.</span><span class="sxs-lookup"><span data-stu-id="10002-120">Select the **Items** FastTab.</span></span>

3. <span data-ttu-id="10002-121">Klik op **Toevoegen** als u een nieuwe regel wilt maken voor een reserve-onderdeel dat nog niet voorkomt in de lijst met reserve-onderdelen of de activumstuklijst.</span><span class="sxs-lookup"><span data-stu-id="10002-121">Click **Add** to create a new line for a spare part that is not on the spare parts list or the asset BOM list.</span></span>

4. <span data-ttu-id="10002-122">Selecteer het artikel in het veld **Artikelnummer**.</span><span class="sxs-lookup"><span data-stu-id="10002-122">Select the item in the **Item number** field.</span></span>

5. <span data-ttu-id="10002-123">Typ een hoeveelheid in het veld **Verkoophoeveelheid** en selecteer een hoeveelheidseenheid in het veld **Eenheid**.</span><span class="sxs-lookup"><span data-stu-id="10002-123">Insert quantity in the **Sales quantity** field, and select a quantity unit in the **Unit** field.</span></span>

6. <span data-ttu-id="10002-124">Voeg de kostprijs en valuta in de betreffende velden in en selecteer een **Regeleigenschap**.</span><span class="sxs-lookup"><span data-stu-id="10002-124">Insert cost price and currency in the relevant fields, and select a **Line property**.</span></span>

7. <span data-ttu-id="10002-125">Als u de lijst met dimensies wilt wijzigen die op de artikelregels wordt weergegeven, klikt u op **Voorraad** > **Weergavedimensies**, selecteert u de dimensies en selecteert u Ja op de wisselknop **Instellingen opslaan**.</span><span class="sxs-lookup"><span data-stu-id="10002-125">If you want to change the list of dimensions displayed on the item lines, click **Inventory** > **Display dimensions**, select the dimensions, and select "Yes" on the **Save setup** toggle button.</span></span>

8. <span data-ttu-id="10002-126">Als u een goedgekeurd reserve-onderdeel aan de prognose voor onderhoud wilt toevoegen, klikt u op **Reserve-onderdelen toevoegen**, selecteert u het reserve-onderdeel, wijzigt u indien nodig gerelateerde gegevens en klikt u op **OK**.</span><span class="sxs-lookup"><span data-stu-id="10002-126">If you want to add an approved spare part to the maintenance forecast, click **Add spare parts**, select the spare part, edit related information if required, and click **OK**.</span></span>

9. <span data-ttu-id="10002-127">Als u activumstuklijstartikelen aan de prognose wilt toevoegen, klikt u op **Stuklijstartikelen toevoegen**, selecteert u het artikel, wijzigt u gerelateerde informatie als dat nodig is en klikt u op **OK**.</span><span class="sxs-lookup"><span data-stu-id="10002-127">If you want to add asset BOM items to the forecast, click **Add BOM items**, select the item, edit related information if required, and click **OK**.</span></span>

10. <span data-ttu-id="10002-128">Klik op **Artikel waar gebruikt** voor een overzicht van waar het artikel op de geselecteerde regel in Activabeheer wordt gebruikt in relatie tot activa, standaardwaarden voor onderhoudstaaktypen, reserveonderdelen en werkorders.</span><span class="sxs-lookup"><span data-stu-id="10002-128">Click **Item where used** if you want to get an overview of where the item on the selected line is used in Asset Management in relation to assets, maintenance job type defaults, spare parts, and work orders.</span></span> 



## <a name="add-expense-forecast-to-a-work-order"></a><span data-ttu-id="10002-129">Onkostenprognose toevoegen aan een werkorder</span><span class="sxs-lookup"><span data-stu-id="10002-129">Add expense forecast to a work order</span></span>

1. <span data-ttu-id="10002-130">In dit onderwerp wordt uitgelegd hoe u een onkostenprognose aan een werkorder toevoegt.</span><span class="sxs-lookup"><span data-stu-id="10002-130">This topic explains how to add an expense forecast to a work order.</span></span> <span data-ttu-id="10002-131">Selecteer de werkordertaak waaraan u een prognose wilt toevoegen in de linkerzijde van het formulier.</span><span class="sxs-lookup"><span data-stu-id="10002-131">In the left-hand side of the form, select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="10002-132">Selecteer het sneltabblad **Onkosten**.</span><span class="sxs-lookup"><span data-stu-id="10002-132">Select the **Expense** FastTab.</span></span>

3. <span data-ttu-id="10002-133">Klik op **Toevoegen** om een nieuwe regel te maken.</span><span class="sxs-lookup"><span data-stu-id="10002-133">Click **Add** to create a new line.</span></span>

4. <span data-ttu-id="10002-134">Selecteer een categorie in het veld **Categorie**.</span><span class="sxs-lookup"><span data-stu-id="10002-134">Select a category in the **Category** field.</span></span>

5. <span data-ttu-id="10002-135">Voer in het veld **Hoeveelheid** een hoeveelheid in.</span><span class="sxs-lookup"><span data-stu-id="10002-135">Insert quantity in the **Quantity** field.</span></span>

6. <span data-ttu-id="10002-136">Voeg kostprijs, verkoopvaluta en verkoopprijs in de relevante velden in.</span><span class="sxs-lookup"><span data-stu-id="10002-136">Insert cost price, sales currency, and sales price in the relevant fields.</span></span>

7. <span data-ttu-id="10002-137">Selecteer in het veld **Regeleigenschap** het toeslagtype dat op de regel moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="10002-137">In the **Line property** field, select the charge type to be used on the line.</span></span>

>[!NOTE]
><span data-ttu-id="10002-138">Op het sneltabblad **Totalen van prognose voor onderhoud** kunt u een overzicht bekijken van het aantal regels dat op elk tabblad is gemaakt, voor de geselecteerde werkordertaak en voor de werkorder.</span><span class="sxs-lookup"><span data-stu-id="10002-138">On the **Maintenance forecast totals** FastTab, you can see an overview of the number of lines created on each tab, for the selected work order job and for the work order.</span></span> <span data-ttu-id="10002-139">U kunt ook een som weergeven van de voorspelde werkuren voor de werkordertaak en de werkorder.</span><span class="sxs-lookup"><span data-stu-id="10002-139">Also, you can see a sum of forecasted work hours for the work order job and for the work order.</span></span>

![Figuur 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a><span data-ttu-id="10002-141">Prognoses van werkorders automatisch bijwerken</span><span class="sxs-lookup"><span data-stu-id="10002-141">Automatic update of work order forecasts</span></span>

<span data-ttu-id="10002-142">In Activabeheer kunt u eventuele wijzigingen in prognoses voor werkorders die betrekking hebben op uurkosten, artikelkosten en onkosten, automatisch bijwerken als ze zijn bijgewerkt in andere modules.</span><span class="sxs-lookup"><span data-stu-id="10002-142">In Asset Management, you can automatically update any changes in work order forecasts regarding hour costs, item costs, and expenses, which have been updated in other modules.</span></span> <span data-ttu-id="10002-143">Op die manier worden altijd de laatste kostprijzen in uw prognoses voor werkorders gebruikt.</span><span class="sxs-lookup"><span data-stu-id="10002-143">This is done to ensure that the latest cost prices are always used in your work order forecasts.</span></span> <span data-ttu-id="10002-144">Het is ook mogelijk om soortgelijke updates te maken voor [prognoses voor onderhoudstaken](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span><span class="sxs-lookup"><span data-stu-id="10002-144">It is also possible to make similar updates for [maintenance job type forecasts](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span>

1. <span data-ttu-id="10002-145">Klik op **Activabeheer** > **Periodiek** > **Prognose** > **Prognose voor werkorder bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="10002-145">Click **Asset management** > **Periodic** > **Forecast** > **Update work order forecast**.</span></span>

2. <span data-ttu-id="10002-146">In het vervolgkeuzevenster **Prognose voor werkorder bijwerken** kunt u zo nodig selecties toevoegen met betrekking tot specifieke werkorders of werkordertaken.</span><span class="sxs-lookup"><span data-stu-id="10002-146">In the **Update work order forecast** drop-down dialog, you can add selections regarding specific work orders or work order jobs, if required.</span></span> <span data-ttu-id="10002-147">Klik op **Filter** om deze selecties te maken.</span><span class="sxs-lookup"><span data-stu-id="10002-147">Click **Filter** to make those selections.</span></span>

3. <span data-ttu-id="10002-148">Indien nodig kunt u de automatische update op het sneltabblad **Op de achtergrond uitvoeren** instellen als een batchtaak.</span><span class="sxs-lookup"><span data-stu-id="10002-148">If required, you can set up the automatic update as a batch job on the **Run in the background** FastTab.</span></span>

4. <span data-ttu-id="10002-149">Klik op **OK** om de update van de prognose te starten.</span><span class="sxs-lookup"><span data-stu-id="10002-149">Click **OK** to start the forecast update.</span></span>


![Figuur 2](media/07-work-orders.png)

