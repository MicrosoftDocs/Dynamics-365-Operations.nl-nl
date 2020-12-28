---
title: Verlof- en verzuimplannen toerekenen
description: U kunt verlof en verzuim toerekenen in Dynamics 365 Human Resources voor meerdere werknemers of voor een individu.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 43c16c5d0de91bf1f433f4fde36e7d13775f44a0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418038"
---
# <a name="accrue-leave-and-absence-plans"></a><span data-ttu-id="95321-103">Verlof- en verzuimplannen toerekenen</span><span class="sxs-lookup"><span data-stu-id="95321-103">Accrue leave and absence plans</span></span>

<span data-ttu-id="95321-104">U kunt verlof en verzuim toerekenen in Dynamics 365 Human Resources voor meerdere werknemers of voor een individu.</span><span class="sxs-lookup"><span data-stu-id="95321-104">You can accrue leave and absence in Dynamics 365 Human Resources for multiple employees or for an individual.</span></span>

## <a name="accrue-leave-and-absence-for-multiple-employees"></a><span data-ttu-id="95321-105">Verlof en verzuim toerekenen voor meerdere werknemers</span><span class="sxs-lookup"><span data-stu-id="95321-105">Accrue leave and absence for multiple employees</span></span>

1. <span data-ttu-id="95321-106">Selecteer op de pagina **Verlof en verzuim** het tabblad **Koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="95321-106">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="95321-107">Selecteer onder **Verlof beheren** de optie **Verlof- en verzuimplannen toerekenen**.</span><span class="sxs-lookup"><span data-stu-id="95321-107">Under **Manage leave**, select **Accrue leave and absence plans**.</span></span>

3. <span data-ttu-id="95321-108">Het dialoogvenster **Verlof- en verzuimplannen toerekenen** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="95321-108">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="95321-109">Selecteer bij **Toerekenen vanaf** **Datum van vandaag** of **Aangepaste datum** en voer een aangepaste datum in.</span><span class="sxs-lookup"><span data-stu-id="95321-109">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="95321-110">Als u transitorische posten voor alle bedrijven wilt uitvoeren, selecteert u **Alle bedrijven**.</span><span class="sxs-lookup"><span data-stu-id="95321-110">If you want to run accruals for all companies, select **All companies**.</span></span> <span data-ttu-id="95321-111">Als u transitorische posten voor één verlofplan wilt verwerken, selecteert u **Nee** voor **Alle plannen** en selecteert u vervolgens een **Verlofplan**.</span><span class="sxs-lookup"><span data-stu-id="95321-111">If you want to process accruals for a single leave plan, select **No** for **All plans**, and then select a **Leave plan**.</span></span> <span data-ttu-id="95321-112">Als u alle bedrijven selecteert, kunt u geen afzonderlijk verlofplan selecteren.</span><span class="sxs-lookup"><span data-stu-id="95321-112">If you select all companies, you can't select an individual leave plan.</span></span> 

5. <span data-ttu-id="95321-113">Als u het toerekeningsprocedure op de achtergrond wilt uitvoeren, selecteert u **Uitvoeren op de achtergrond** en voert u de volgende taken uit:</span><span class="sxs-lookup"><span data-stu-id="95321-113">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="95321-114">Informatie over het toerekeningsproces invoeren.</span><span class="sxs-lookup"><span data-stu-id="95321-114">Enter information for the accrual process.</span></span>

   2. <span data-ttu-id="95321-115">Als u een terugkerende taak wilt instellen, selecteert u **Terugkeerpatroon**, voert u de terugkeergegevens in en selecteert u **OK**.</span><span class="sxs-lookup"><span data-stu-id="95321-115">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="95321-116">Als u een taakwaarschuwing wilt instellen, selecteert u **Waarschuwingen**, selecteert u de waarschuwingen die u wilt ontvangen en selecteert u vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="95321-116">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="95321-117">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="95321-117">Select **OK**.</span></span> <span data-ttu-id="95321-118">Het toerekeningsproces wordt uitgevoerd met de parameters die u instelt.</span><span class="sxs-lookup"><span data-stu-id="95321-118">The accrual process will run with the parameters you set.</span></span>

## <a name="accrue-leave-and-absence-for-an-employee"></a><span data-ttu-id="95321-119">Verlof en verzuim toerekenen voor een werknemer</span><span class="sxs-lookup"><span data-stu-id="95321-119">Accrue leave and absence for an employee</span></span>

1. <span data-ttu-id="95321-120">Selecteer **Verlof** in de record van de werknemer.</span><span class="sxs-lookup"><span data-stu-id="95321-120">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="95321-121">Selecteer **Verlof en verzuim toerekenen**.</span><span class="sxs-lookup"><span data-stu-id="95321-121">Select **Accrue leave and absence**.</span></span>

3. <span data-ttu-id="95321-122">Het dialoogvenster **Verlof- en verzuimplannen toerekenen** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="95321-122">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="95321-123">Selecteer bij **Toerekenen vanaf** **Datum van vandaag** of **Aangepaste datum** en voer een aangepaste datum in.</span><span class="sxs-lookup"><span data-stu-id="95321-123">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="95321-124">Als u transitorische posten voor alle bedrijven wilt uitvoeren, selecteert u **Alle bedrijven**.</span><span class="sxs-lookup"><span data-stu-id="95321-124">If you want to run accruals for all companies, select **All companies**.</span></span> <span data-ttu-id="95321-125">Als u transitorische posten voor één verlofplan wilt verwerken, selecteert u **Nee** voor **Alle plannen** en selecteert u vervolgens een **Verlofplan**.</span><span class="sxs-lookup"><span data-stu-id="95321-125">If you want to process accruals for a single leave plan, select **No** for **All plans**, and then select a **Leave plan**.</span></span> <span data-ttu-id="95321-126">Als u alle bedrijven selecteert, kunt u geen afzonderlijk verlofplan selecteren.</span><span class="sxs-lookup"><span data-stu-id="95321-126">If you select all companies, you can't select an individual leave plan.</span></span> 

5. <span data-ttu-id="95321-127">Als u het toerekeningsprocedure op de achtergrond wilt uitvoeren, selecteert u **Uitvoeren op de achtergrond** en voert u de volgende taken uit:</span><span class="sxs-lookup"><span data-stu-id="95321-127">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="95321-128">Informatie over het toerekeningsproces invoeren.</span><span class="sxs-lookup"><span data-stu-id="95321-128">Enter information for the accrual process.</span></span>

   2. <span data-ttu-id="95321-129">Als u een terugkerende taak wilt instellen, selecteert u **Terugkeerpatroon**, voert u de terugkeergegevens in en selecteert u **OK**.</span><span class="sxs-lookup"><span data-stu-id="95321-129">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="95321-130">Als u een taakwaarschuwing wilt instellen, selecteert u **Waarschuwingen**, selecteert u de waarschuwingen die u wilt ontvangen en selecteert u vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="95321-130">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="95321-131">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="95321-131">Select **OK**.</span></span> <span data-ttu-id="95321-132">Het toerekeningsproces wordt uitgevoerd met de parameters die u instelt.</span><span class="sxs-lookup"><span data-stu-id="95321-132">The accrual process will run with the parameters you set.</span></span>

## <a name="delete-leave-and-absence-accruals-for-multiple-employees"></a><span data-ttu-id="95321-133">Verlof- en verzuimtoerekeningen verwijderen voor meerdere werknemers</span><span class="sxs-lookup"><span data-stu-id="95321-133">Delete leave and absence accruals for multiple employees</span></span>

<span data-ttu-id="95321-134">Opbouwrecords voor een specifiek plan en datumbereik verwijderen.</span><span class="sxs-lookup"><span data-stu-id="95321-134">Delete accrual records for a specific plan and date range.</span></span> <span data-ttu-id="95321-135">Toerekeningsdatums moeten vandaag of in de toekomst gedateerd zijn.</span><span class="sxs-lookup"><span data-stu-id="95321-135">Accrual dates must be dated today or in the future.</span></span>

1. <span data-ttu-id="95321-136">Selecteer op de pagina **Verlof en verzuim** het tabblad **Koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="95321-136">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="95321-137">Selecteer onder **Verlof beheren** de optie **Verlof- en verzuimtoerekeningen verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="95321-137">Under **Manage leave**, select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="95321-138">Selecteer in het dialoogvenster **Verlof- en verzuimtoerekeningen verwijderen** de optie **Verlofplan**.</span><span class="sxs-lookup"><span data-stu-id="95321-138">In the **Delete leave and absence plan accruals** dialog box, select the **Leave plan**.</span></span> 

4. <span data-ttu-id="95321-139">Kies **Saldocorrecties verwijderen** als dit van toepassing is.</span><span class="sxs-lookup"><span data-stu-id="95321-139">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="95321-140">Voer een **Toerekeningsdatum voor verlof** in of selecteer deze.</span><span class="sxs-lookup"><span data-stu-id="95321-140">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="95321-141">Deze datum moet vandaag zijn of in de toekomst liggen.</span><span class="sxs-lookup"><span data-stu-id="95321-141">This date has to be either today or in the future.</span></span> 

6. <span data-ttu-id="95321-142">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="95321-142">Select **OK**.</span></span> <span data-ttu-id="95321-143">Door het toerekeningsproces worden de toerekeningen met de parameters die u hebt ingesteld, verwijderd.</span><span class="sxs-lookup"><span data-stu-id="95321-143">The accrual process will delete accruals with the parameters you set.</span></span> 

## <a name="delete-leave-and-absence-accruals-for-a-single-employee"></a><span data-ttu-id="95321-144">Verlof- en verzuimtoerekeningen verwijderen voor één werknemer</span><span class="sxs-lookup"><span data-stu-id="95321-144">Delete leave and absence accruals for a single employee</span></span>

1. <span data-ttu-id="95321-145">Selecteer **Verlof** in de record van de werknemer.</span><span class="sxs-lookup"><span data-stu-id="95321-145">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="95321-146">Selecteer **Verlof- en verzuimtoerekeningen verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="95321-146">Select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="95321-147">Selecteer in het dialoogvenster **Verlof- en verzuimtoerekeningen verwijderen** de optie **Verlofplan**.</span><span class="sxs-lookup"><span data-stu-id="95321-147">In the **Delete leave and absence plan accruals** dialog box, select **Leave plan**.</span></span> 

4. <span data-ttu-id="95321-148">Kies **Saldocorrecties verwijderen** als dit van toepassing is.</span><span class="sxs-lookup"><span data-stu-id="95321-148">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="95321-149">Voer een **Toerekeningsdatum voor verlof** in of selecteer deze.</span><span class="sxs-lookup"><span data-stu-id="95321-149">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="95321-150">Deze datum moet vandaag zijn of in de toekomst liggen.</span><span class="sxs-lookup"><span data-stu-id="95321-150">This date must be either today or in the future.</span></span> 

6. <span data-ttu-id="95321-151">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="95321-151">Select **OK**.</span></span> <span data-ttu-id="95321-152">Door het toerekeningsproces worden de toerekeningen met de parameters die u hebt ingesteld, verwijderd.</span><span class="sxs-lookup"><span data-stu-id="95321-152">The accrual process will delete accruals with the parameters you set.</span></span> 

## <a name="review-leave-accrual-and-deletion-processes"></a><span data-ttu-id="95321-153">Toerekenings- en verwijderprocessen voor verlof controleren</span><span class="sxs-lookup"><span data-stu-id="95321-153">Review leave accrual and deletion processes</span></span>

<span data-ttu-id="95321-154">**Controle van toerekening van verlof** wordt steeds weergegeven als u een toerekening uitvoert of verwijdert voor een of alle werk nemers.</span><span class="sxs-lookup"><span data-stu-id="95321-154">**Leave accrual audit** displays each time you run or delete an accrual for one or all employees.</span></span> <span data-ttu-id="95321-155">De datum en de persoon die de actie heeft uitgevoerd, worden ook weer gegeven.</span><span class="sxs-lookup"><span data-stu-id="95321-155">The date and person who performed the action also displays.</span></span>

1. <span data-ttu-id="95321-156">Selecteer op de pagina **Verlof en verzuim** het tabblad **Koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="95321-156">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="95321-157">Selecteer onder **Verlof beheren** de optie **Controle van toerekening van verlof verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="95321-157">Under **Manage leave**, select **Delete leave accrual audit**.</span></span>

## <a name="see-also"></a><span data-ttu-id="95321-158">Zie ook</span><span class="sxs-lookup"><span data-stu-id="95321-158">See also</span></span>

[<span data-ttu-id="95321-159">Overzicht van verlof en verzuim</span><span class="sxs-lookup"><span data-stu-id="95321-159">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="95321-160">Een plan voor verlof en verzuim maken</span><span class="sxs-lookup"><span data-stu-id="95321-160">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
