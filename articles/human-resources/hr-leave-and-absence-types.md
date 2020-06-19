---
title: Verlof- en verzuimtypen configureren
description: Typen verlof instellen die werknemers kunnen aanvragen in Dynamics 365 Human Resources.
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
ms.openlocfilehash: 1802938f54a1d78e6ea60572a76177a037192ae0
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2020
ms.locfileid: "3428588"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="7afee-103">Verlof- en verzuimtypen configureren</span><span class="sxs-lookup"><span data-stu-id="7afee-103">Configure leave and absence types</span></span>

<span data-ttu-id="7afee-104">Verloftypen in Dynamics 365 Human Resources geven de typen verlof aan die werknemers kunnen rapporteren.</span><span class="sxs-lookup"><span data-stu-id="7afee-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="7afee-105">U kunt de typen verlof aanpassen op basis van de behoeften van uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="7afee-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="7afee-106">Voorbeelden van verloftypen zijn:</span><span class="sxs-lookup"><span data-stu-id="7afee-106">Examples of leave types include:</span></span>

- <span data-ttu-id="7afee-107">Betaald verlof</span><span class="sxs-lookup"><span data-stu-id="7afee-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="7afee-108">Onbetaald verlof</span><span class="sxs-lookup"><span data-stu-id="7afee-108">Unpaid leave</span></span>
- <span data-ttu-id="7afee-109">Betaalde vakantie</span><span class="sxs-lookup"><span data-stu-id="7afee-109">Paid vacation</span></span>
- <span data-ttu-id="7afee-110">Ziekteverlof</span><span class="sxs-lookup"><span data-stu-id="7afee-110">Sick leave</span></span>
- <span data-ttu-id="7afee-111">Medisch verlof</span><span class="sxs-lookup"><span data-stu-id="7afee-111">Medical leave</span></span>
- <span data-ttu-id="7afee-112">Familieverlof</span><span class="sxs-lookup"><span data-stu-id="7afee-112">Family leave</span></span>
- <span data-ttu-id="7afee-113">Kortdurende arbeidsongeschiktheid</span><span class="sxs-lookup"><span data-stu-id="7afee-113">Short-term disability</span></span>
- <span data-ttu-id="7afee-114">Verlof bij sterfgeval</span><span class="sxs-lookup"><span data-stu-id="7afee-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="7afee-115">Een verloftype toevoegen</span><span class="sxs-lookup"><span data-stu-id="7afee-115">Add a leave type</span></span>

1. <span data-ttu-id="7afee-116">Selecteer op de pagina **Verlof en verzuim** het tabblad **Koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="7afee-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="7afee-117">Selecteer onder **Instellingen** de optie **Verlof- en verzuimtypen**.</span><span class="sxs-lookup"><span data-stu-id="7afee-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="7afee-118">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="7afee-118">Select **New**.</span></span>

4. <span data-ttu-id="7afee-119">Voer een naam in voor het verloftype onder **Type**, selecteer een werkstroom bij **Werkstroom-id** en voer een beschrijving in onder **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="7afee-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="7afee-120">Selecteer bij **Algemeen** de optie **Geen**, **Gepland** of **Ongepland** in de vervolgkeuzelijst **Categorie**.</span><span class="sxs-lookup"><span data-stu-id="7afee-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="7afee-121">Selecteer een inkomstencode in de vervolgkeuzelijst **Inkomstencode**.</span><span class="sxs-lookup"><span data-stu-id="7afee-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="7afee-122">Geef onder **Redencode vereist** aan of u een redencode wilt vereisen.</span><span class="sxs-lookup"><span data-stu-id="7afee-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="7afee-123">Als u redencodes wilt vereisen, moet u deze mogelijk toevoegen.</span><span class="sxs-lookup"><span data-stu-id="7afee-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="7afee-124">Selecteer onder **Redencodes** de optie **Toevoegen**, selecteer een redencode en schakel vervolgens het selectievakje **Ingeschakeld** hiernaast in.</span><span class="sxs-lookup"><span data-stu-id="7afee-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="7afee-125">Kies onder **Toegang tot geselecteerde rollen beperken** of u de toegang wilt beperken.</span><span class="sxs-lookup"><span data-stu-id="7afee-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="7afee-126">Selecteer vervolgens de beveiligingsrollen onder **Beveiligingsrollen voor dit verloftype**.</span><span class="sxs-lookup"><span data-stu-id="7afee-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="7afee-127">De beveiligingsrollen worden gedefinieerd in de werkstroom die u onder **Werkstroom-id** eerder in deze procedure hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="7afee-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="7afee-128">Geef onder **Uitstelrelaties** op of u wilt dat dit verloftype een ander verloftype uitstelt of door een ander verloftype wordt uitgesteld.</span><span class="sxs-lookup"><span data-stu-id="7afee-128">Under **Suspension relations**, choose if you want to have this leave type either suspend another leave type or be suspended by another leave type.</span></span> <span data-ttu-id="7afee-129">Wanneer een verlofaanvraag wordt ingediend voor het uitstellende verloftype, wordt er automatisch een verlofuitstel gemaakt voor het uitgestelde verloftype.</span><span class="sxs-lookup"><span data-stu-id="7afee-129">When a leave of absence request is submitted for the suspending leave type, a leave suspension will automatically be created for the suspended leave type.</span></span> 

10. <span data-ttu-id="7afee-130">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="7afee-130">Select **Save**.</span></span>

## <a name="configure-leave-type-rules"></a><span data-ttu-id="7afee-131">Regels voor verloftypen configureren</span><span class="sxs-lookup"><span data-stu-id="7afee-131">Configure leave type rules</span></span>

1. <span data-ttu-id="7afee-132">Stel afrondingsopties in voor het verloftype.</span><span class="sxs-lookup"><span data-stu-id="7afee-132">Set rounding options for the leave type.</span></span> <span data-ttu-id="7afee-133">De beschikbare opties zijn **Geen**, **Naar boven**, **Naar beneden** en **Dichtstbijzijnde**.</span><span class="sxs-lookup"><span data-stu-id="7afee-133">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="7afee-134">U kunt ook een afrondingsprecisie instellen voor het verloftype.</span><span class="sxs-lookup"><span data-stu-id="7afee-134">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="7afee-135">Stel **Feestdagcorrectie** in voor het verloftype.</span><span class="sxs-lookup"><span data-stu-id="7afee-135">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="7afee-136">Wanneer u deze optie selecteert, gebruikt Human Resources het aantal feestdagen dat op een werkdag valt om te bepalen hoe het verlof moet worden opgebouwd voor het verloftype.</span><span class="sxs-lookup"><span data-stu-id="7afee-136">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="7afee-137">Als kerstdag bijvoorbeeld op een maandag valt, trekt Human Resources een dag af van het verloftype bij het verwerken van toerekeningen.</span><span class="sxs-lookup"><span data-stu-id="7afee-137">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="7afee-138">U kunt feestdage instellen in de werktijdkalender.</span><span class="sxs-lookup"><span data-stu-id="7afee-138">You set holidays in the working time calendar.</span></span> <span data-ttu-id="7afee-139">Zie [Een werktijdenkalender maken](hr-leave-and-absence-working-time-calendar.md) voor meer informatie</span><span class="sxs-lookup"><span data-stu-id="7afee-139">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>
   
 3. <span data-ttu-id="7afee-140">Stel **Verloftype voor transporteren** in voor het verloftype.</span><span class="sxs-lookup"><span data-stu-id="7afee-140">Set **Carry-forward leave type** for the leave type.</span></span> <span data-ttu-id="7afee-141">Wanneer u deze optie selecteert, worden transportsaldi overgeboekt naar het opgegeven verloftype.</span><span class="sxs-lookup"><span data-stu-id="7afee-141">When you select this option, any carry-forward balances will be transferred to the specified leave type.</span></span> <span data-ttu-id="7afee-142">Het verloftype voor transporteren moet ook worden opgenomen in het plan voor verlof en verzuim.</span><span class="sxs-lookup"><span data-stu-id="7afee-142">The carry-forward leave type also needs to be included in the leave and absence plan.</span></span> 
 
 4. <span data-ttu-id="7afee-143">Definieer **vervalregels** voor het verloftype.</span><span class="sxs-lookup"><span data-stu-id="7afee-143">Define **Expiration rules** for the leave type.</span></span> <span data-ttu-id="7afee-144">Wanneer u deze optie configureert, kunt u als eenheid voor dagen of maanden kiezen en de duur instellen voor de vervaldatum.</span><span class="sxs-lookup"><span data-stu-id="7afee-144">When you configure this option, you can choose the unit of days or months and set the duration for the expiry.</span></span> <span data-ttu-id="7afee-145">U kunt ook de ingangsdatum van de verloopregel instellen.</span><span class="sxs-lookup"><span data-stu-id="7afee-145">You can also set the effective date of the expiration rule.</span></span> <span data-ttu-id="7afee-146">Alle verlofsaldi die aanwezig zijn op het tijdstip van de vervaldatum, worden afgetrokken van het verloftype en worden weergegeven in het verlofsaldo.</span><span class="sxs-lookup"><span data-stu-id="7afee-146">Any leave balances that exist at the time of expiry will be subtracted from the leave type and will be reflected in the leave balance.</span></span> 
 
 
## <a name="see-also"></a><span data-ttu-id="7afee-147">Zie ook</span><span class="sxs-lookup"><span data-stu-id="7afee-147">See also</span></span>

- [<span data-ttu-id="7afee-148">Overzicht van verlof en verzuim</span><span class="sxs-lookup"><span data-stu-id="7afee-148">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="7afee-149">Een plan voor verlof en verzuim maken</span><span class="sxs-lookup"><span data-stu-id="7afee-149">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="7afee-150">Een werktijdenkalender maken</span><span class="sxs-lookup"><span data-stu-id="7afee-150">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
- [<span data-ttu-id="7afee-151">Verlof uitstellen</span><span class="sxs-lookup"><span data-stu-id="7afee-151">Suspend leave</span></span>](hr-leave-and-absence-suspend-leave.md)

