---
title: Een compensatiestructuur ontwikkelen
description: Dit artikel begeleidt u bij het maken van een vastecompensatieplan en het registreren van werknemers voor het plan via geschiktheidsregels.
author: andreabichsel
manager: tfehr
ms.date: 02/10/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: DefaultDashboard, HcmCompensationWorkspace, HcmCompFixedPlansPart, HRMCompFixedPlanTable, HRMCompCreateGridDialog, HRCCompGridView, HRMCompEligibility,  HRCCompGrid
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5030203877ebdf885fb55c7946bfd4ee0c883c2e
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465673"
---
# <a name="develop-a-compensation-structure"></a><span data-ttu-id="77930-103">Een compensatiestructuur ontwikkelen</span><span class="sxs-lookup"><span data-stu-id="77930-103">Develop a compensation structure</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="77930-104">Dit artikel begeleidt u bij het maken van een vastecompensatieplan en het registreren van werknemers voor het plan via geschiktheidsregels.</span><span class="sxs-lookup"><span data-stu-id="77930-104">This article walks you through creating a fixed compensation plan and enrolling employees in the plan through eligibility rules.</span></span> <span data-ttu-id="77930-105">In dit artikel, dat van toepassing is op managers voor compensatie en vergoedingen, worden de USMF-voorbeeldgegevens gebruikt.</span><span class="sxs-lookup"><span data-stu-id="77930-105">This article uses the USMF demo data and applies to Compensation and Benefits Managers.</span></span>

## <a name="create-a-fixed-compensation-plan"></a><span data-ttu-id="77930-106">Een vast compensatieplan maken</span><span class="sxs-lookup"><span data-stu-id="77930-106">Create a fixed compensation plan</span></span>

1. <span data-ttu-id="77930-107">Selecteer **Compensatiebeheer**.</span><span class="sxs-lookup"><span data-stu-id="77930-107">Select **Compensation management**.</span></span>

2. <span data-ttu-id="77930-108">Selecteer **Vastecompensatieplannen**.</span><span class="sxs-lookup"><span data-stu-id="77930-108">Select **Fixed compensation plans**.</span></span>

3. <span data-ttu-id="77930-109">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="77930-109">Select **New**.</span></span>

4. <span data-ttu-id="77930-110">Voer een waarde in het veld **Plan** in.</span><span class="sxs-lookup"><span data-stu-id="77930-110">In the **Plan** field, enter a value.</span></span>

5. <span data-ttu-id="77930-111">Voer een waarde in het veld **Beschrijving** in.</span><span class="sxs-lookup"><span data-stu-id="77930-111">In the **Description** field, enter a value.</span></span>

6. <span data-ttu-id="77930-112">Voer een datum in het veld **Begindatum** in.</span><span class="sxs-lookup"><span data-stu-id="77930-112">In the **Effective date** field, enter a date.</span></span>

7. <span data-ttu-id="77930-113">Selecteer in het veld **Type** of het vastecompensatieplan van het type **Schaal**, **Schijf** of **Stap** is.</span><span class="sxs-lookup"><span data-stu-id="77930-113">In the **Type** field, select whether the fixed compensation plan is a **Band**, **Grade**, or **Step** plan.</span></span>

8. <span data-ttu-id="77930-114">Het selectievakje **Aanbeveling toegestaan** fungeert als standaardwaarde voor eventuele acties die aan dit plan in een procesgebeurtenis worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="77930-114">The **Recommendation allowed** checkbox acts as a default value for any actions added to this plan in a Process event.</span></span> <span data-ttu-id="77930-115">Met Aanbeveling toegestaan kunt u het berekende richtlijnbedrag overschrijven bij het verwerken van de compensatie.</span><span class="sxs-lookup"><span data-stu-id="77930-115">Allowing recommendations enables you to override the calculated guideline amount when processing compensation.</span></span>

9. <span data-ttu-id="77930-116">Met het veld **Tolerantie voor buiten bereik** kunt u opgeven hoe u compensatiebedragen wilt verwerken die buiten het opgegeven bereik van de compensatiestructuur voor het opgegeven niveau vallen.</span><span class="sxs-lookup"><span data-stu-id="77930-116">The **Out of range tolerance** field allows you to specify how you want to handle compensation amounts that fall outside of the specified compensation structure range for the given level.</span></span> <span data-ttu-id="77930-117">Als u het veld **Tolerantie voor buiten bereik** instelt op **Geen**, kunt u elk gewenst compensatiebedrag gebruiken.</span><span class="sxs-lookup"><span data-stu-id="77930-117">Setting the **Out of range tolerance** field to **None** allows you to use any compensation amount.</span></span> <span data-ttu-id="77930-118">**Zachte tolerantie** waarschuwt gebruikers als het compensatiebedrag minder is dan het minimale of meer dan het maximale referentiepuntbedrag voor dat niveau.</span><span class="sxs-lookup"><span data-stu-id="77930-118">**Soft tolerance** warns users if the compensation amount is less than the minimum or greater than the maximum reference point amounts for that level.</span></span> <span data-ttu-id="77930-119">Gebruikers kunnen de waarschuwing negeren en verdergaan.</span><span class="sxs-lookup"><span data-stu-id="77930-119">Users can ignore the warning and continue.</span></span> <span data-ttu-id="77930-120">**Harde tolerantie** genereert een fout als de compensatie van een werknemer buiten de minimum- en maximumreferentiepunten voor het niveau ligt en wordt de compensatie automatisch aangepast om binnen het bereik te vallen.</span><span class="sxs-lookup"><span data-stu-id="77930-120">**Hard tolerance** generates an error if an employee's compensation is outside the minimum and maximum reference points for the level and will automatically adjust the employee's compensation to fall within the range.</span></span>

10. <span data-ttu-id="77930-121">Met het veld **Huurregel** wordt de compensatie van een werknemer tijdens een procesgebeurtenis berekend.</span><span class="sxs-lookup"><span data-stu-id="77930-121">The **Hire rule** field calculates an employee's compensation during a process event.</span></span> <span data-ttu-id="77930-122">Een **huurregel** van het type **Percentage** berekent een verhoging die evenredig is voor de duur dat de werknemer in dienst is in de cyclus.</span><span class="sxs-lookup"><span data-stu-id="77930-122">A **Hire rule** of **Percent** calculates an increase that's prorated for the length of the time the worker has been employed in the cycle.</span></span>

11. <span data-ttu-id="77930-123">Typ een waarde in het veld **Valuta**.</span><span class="sxs-lookup"><span data-stu-id="77930-123">In the **Currency** field, type a value.</span></span>

12. <span data-ttu-id="77930-124">Typ of selecteer een waarde in het veld **Conversie van loontarief**.</span><span class="sxs-lookup"><span data-stu-id="77930-124">In the **Pay rate conversion** field, enter or select a value.</span></span>

13. <span data-ttu-id="77930-125">Vouw de sectie **Bereikgebruiksmatrix** uit.</span><span class="sxs-lookup"><span data-stu-id="77930-125">Expand the **Range utilization matrix** section.</span></span> <span data-ttu-id="77930-126">Voeg desgewenst bereikgebruikrecords toe om werknemers sneller naar hun middelpunt toe te krijgen en ze af te remmen voor het bereiken van het maximum van hun bereik.</span><span class="sxs-lookup"><span data-stu-id="77930-126">Optionally, add range utilization records to get employees to their midpoint faster and slow them from reaching the maximum of their range.</span></span>

14. <span data-ttu-id="77930-127">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="77930-127">Select **Save**.</span></span> <span data-ttu-id="77930-128">Hierdoor wordt de knop **Compensatie instellen** ingeschakeld en kunt u doorgaan met het definiëren van uw compensatiestructuur voor het plan.</span><span class="sxs-lookup"><span data-stu-id="77930-128">This enables the **Set up compensation** button and continue defining your compensation structure for the plan.</span></span>

15. <span data-ttu-id="77930-129">Selecteer **Compensatie instellen**.</span><span class="sxs-lookup"><span data-stu-id="77930-129">Select **Set up compensation**.</span></span> <span data-ttu-id="77930-130">U kunt een van de volgende drie methoden gebruiken om een compensatiestructuur te maken:</span><span class="sxs-lookup"><span data-stu-id="77930-130">You can create a compensation structure by using one of these three methods:</span></span>

    - <span data-ttu-id="77930-131">Maak een geheel nieuwe structuur door een set referentiepunten te selecteren en de niveaus toe te voegen om uw eigen structuur te maken.</span><span class="sxs-lookup"><span data-stu-id="77930-131">Create a completely new structure by selecting a set of reference points and adding the levels to create your own structure.</span></span>
    - <span data-ttu-id="77930-132">Kopieer een compensatiestructuur van een bestaand plan als beginpunt en wijzig deze voor het nieuwe plan.</span><span class="sxs-lookup"><span data-stu-id="77930-132">Copy a compensation structure from an existing plan as a starting point and modify it for the new plan.</span></span>
    - <span data-ttu-id="77930-133">Selecteer een bestaand compensatieraster.</span><span class="sxs-lookup"><span data-stu-id="77930-133">Select an existing compensation grid.</span></span> <span data-ttu-id="77930-134">Als een ander plan al gebruikmaakt van het compensatieraster, worden eventuele wijzigingen in het raster ook doorgevoerd in het andere plan.</span><span class="sxs-lookup"><span data-stu-id="77930-134">If another plan already uses the compensation grid, the other plan also reflects any changes you make to the grid.</span></span>

16. <span data-ttu-id="77930-135">Selecteer **Nieuwe matrix maken op basis van bestaande compensatiematrix**.</span><span class="sxs-lookup"><span data-stu-id="77930-135">Select **Create new from existing compensation matrix**.</span></span>

17. <span data-ttu-id="77930-136">Typ of selecteer een waarde in het veld **Uit raster kopiëren**.</span><span class="sxs-lookup"><span data-stu-id="77930-136">In the **Copy from grid** field, enter or select a value.</span></span> <span data-ttu-id="77930-137">Desgewenst kunt u de naam van het nieuwe compensatieraster wijzigen die u maakt door het geselecteerde raster te kopiëren.</span><span class="sxs-lookup"><span data-stu-id="77930-137">Optionally, you can change the name of the new compensation grid that you create by copying the selected grid.</span></span>

18. <span data-ttu-id="77930-138">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="77930-138">Select **OK**.</span></span>

19. <span data-ttu-id="77930-139">Selecteer **Groepsgewijs wijzigen**.</span><span class="sxs-lookup"><span data-stu-id="77930-139">Select **Mass change**.</span></span> <span data-ttu-id="77930-140">Met **Groepsgewijs wijzigen** kunt u de bedragen van de compensatiematrix onderhouden door een percentage of een vlakke bedragverhoging toe te passen op één of meerdere niveaus of referentiepunten.</span><span class="sxs-lookup"><span data-stu-id="77930-140">**Mass change** allows you to maintain the compensation matrix amounts by applying a percent or flat amount increase to one or more levels or reference points.</span></span>

20. <span data-ttu-id="77930-141">Voer in het veld **Aanpassingsbedrag** een getal in.</span><span class="sxs-lookup"><span data-stu-id="77930-141">In the **Adjustment amount** field, enter a number.</span></span>

21. <span data-ttu-id="77930-142">Selecteer of deselecteer alle rijen in de lijst.</span><span class="sxs-lookup"><span data-stu-id="77930-142">In the list, mark or unmark all rows.</span></span>

22. <span data-ttu-id="77930-143">Klik op **Toepassen op raster**.</span><span class="sxs-lookup"><span data-stu-id="77930-143">Click **Apply to grid**.</span></span>

23. <span data-ttu-id="77930-144">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="77930-144">Close the page.</span></span> <span data-ttu-id="77930-145">Nadat u de compensatiestructuur hebt gemaakt, kunt u selecteren welke referentiepunten u wilt gebruiken als controlepunt voor het vastecompensatieplan.</span><span class="sxs-lookup"><span data-stu-id="77930-145">After you create the compensation structure, you can select which of the reference points to use as the control point for the fixed compensation plan.</span></span> <span data-ttu-id="77930-146">Het controlepunt wordt gebruikt om de comparatio van een werknemer te berekenen.</span><span class="sxs-lookup"><span data-stu-id="77930-146">The control point is used to calculate an employee's Compa Ratio.</span></span>

24. <span data-ttu-id="77930-147">Typ of selecteer een waarde in het veld **Controlepunt**.</span><span class="sxs-lookup"><span data-stu-id="77930-147">In the **Control point** field, enter or select a value.</span></span>

25. <span data-ttu-id="77930-148">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="77930-148">Close the page.</span></span>

## <a name="create-an-eligibility-rule-for-the-fixed-compensation-plan"></a><span data-ttu-id="77930-149">Maak een geschiktheidsregel voor het vastecompensatieplan</span><span class="sxs-lookup"><span data-stu-id="77930-149">Create an eligibility rule for the fixed compensation plan</span></span>

<span data-ttu-id="77930-150">U kunt een vastecompensatieplan toewijzen aan een werknemer totdat u geschiktheidsregels voor het plan hebt gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="77930-150">You can't assign a fixed compensation plan to an employee until you define eligibility rules for the plan.</span></span>  

1. <span data-ttu-id="77930-151">Selecteer **Geschiktheidsregels**.</span><span class="sxs-lookup"><span data-stu-id="77930-151">Select **Eligibility rules**.</span></span>

2. <span data-ttu-id="77930-152">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="77930-152">Select **New**.</span></span>

3. <span data-ttu-id="77930-153">Typ of selecteer een waarde in het veld **Geschiktheid**.</span><span class="sxs-lookup"><span data-stu-id="77930-153">In the **Eligibility** field, enter a value.</span></span>

4. <span data-ttu-id="77930-154">Voer een waarde in het veld **Beschrijving** in.</span><span class="sxs-lookup"><span data-stu-id="77930-154">In the **Description** field, enter a value.</span></span>

5. <span data-ttu-id="77930-155">Voer een datum in het veld **Begindatum** in.</span><span class="sxs-lookup"><span data-stu-id="77930-155">In the **Effective date** field, enter a date.</span></span> <span data-ttu-id="77930-156">Zowel vaste- als variabele-compensatieplannen maken gebruik van geschiktheidsregels.</span><span class="sxs-lookup"><span data-stu-id="77930-156">Both fixed and variable compensation plans use eligibility rules.</span></span> <span data-ttu-id="77930-157">Selecteer in het veld **Type** het type plan.</span><span class="sxs-lookup"><span data-stu-id="77930-157">In the **Type** field, select the type of plan.</span></span>

6. <span data-ttu-id="77930-158">Typ of selecteer een waarde in het veld **Plannen**.</span><span class="sxs-lookup"><span data-stu-id="77930-158">In the **Plan** field, enter or select a value.</span></span> <span data-ttu-id="77930-159">Selecteer de criteria waaraan een werknemer moet voldoen om in aanmerking te komen voor het compensatieplan.</span><span class="sxs-lookup"><span data-stu-id="77930-159">Select the criteria an employee must meet in order to be eligible for the compensation plan.</span></span> <span data-ttu-id="77930-160">Mogelijke criteria zijn:</span><span class="sxs-lookup"><span data-stu-id="77930-160">Criteria can include:</span></span>

    - <span data-ttu-id="77930-161">**Departement**</span><span class="sxs-lookup"><span data-stu-id="77930-161">**Department**</span></span>
    - <span data-ttu-id="77930-162">**Vakbond**</span><span class="sxs-lookup"><span data-stu-id="77930-162">**Labor union**</span></span>
    - <span data-ttu-id="77930-163">**Locatie** (**Compensatieregio**)</span><span class="sxs-lookup"><span data-stu-id="77930-163">**Location** (**Compensation region**)</span></span>
    - <span data-ttu-id="77930-164">**Functie**</span><span class="sxs-lookup"><span data-stu-id="77930-164">**Job**</span></span>
    - <span data-ttu-id="77930-165">**Functie**</span><span class="sxs-lookup"><span data-stu-id="77930-165">**Function**</span></span>
    - <span data-ttu-id="77930-166">**Taaktype**</span><span class="sxs-lookup"><span data-stu-id="77930-166">**Job type**</span></span>
    - <span data-ttu-id="77930-167">**Compensatieniveau**</span><span class="sxs-lookup"><span data-stu-id="77930-167">**Compensation level**</span></span>
    
    <span data-ttu-id="77930-168">De werknemer moet aan alle criteria voldoen om in aanmerking te komen voor het compensatieplan.</span><span class="sxs-lookup"><span data-stu-id="77930-168">The employee must meet all specified criteria to be eligible for the compensation plan.</span></span> <span data-ttu-id="77930-169">Als u geen criteria opgeeft, komen alle werknemers in aanmerking voor het compensatieplan.</span><span class="sxs-lookup"><span data-stu-id="77930-169">If you don't specify any criteria, all employees are eligible for the compensation plan.</span></span> <span data-ttu-id="77930-170">Als een werknemer niet voldoet aan de criteria die in de regel voor geschiktheid worden opgegeven, of er geen regel voor geschiktheid voor een compensatieplan is opgegeven, wordt het compensatieplan niet in de zoekopdracht weergegeven als u een vastecompensatierecord voor een werknemer maakt.</span><span class="sxs-lookup"><span data-stu-id="77930-170">If an employee doesn't meet the criteria specified in the eligibility rule, or an eligibility rule has not been specified for a compensation plan, the compensation plan won't appear in the lookup when you create a fixed compensation record for an employee.</span></span>

7. <span data-ttu-id="77930-171">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="77930-171">Close the page.</span></span>

8. <span data-ttu-id="77930-172">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="77930-172">Close the page.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]