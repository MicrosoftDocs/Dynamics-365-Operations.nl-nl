---
title: Verlof- en verzuimtypen configureren
description: Typen verlof instellen die werknemers kunnen aanvragen in Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 06/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 39e4c4b9c83ca648c21ac20bd20b739af8a6b9ed
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271122"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="377fb-103">Verlof- en verzuimtypen configureren</span><span class="sxs-lookup"><span data-stu-id="377fb-103">Configure leave and absence types</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="377fb-104">Verloftypen in Dynamics 365 Human Resources geven de typen verlof aan die werknemers kunnen rapporteren.</span><span class="sxs-lookup"><span data-stu-id="377fb-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="377fb-105">U kunt de typen verlof aanpassen op basis van de behoeften van uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="377fb-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="377fb-106">Voorbeelden van verloftypen zijn:</span><span class="sxs-lookup"><span data-stu-id="377fb-106">Examples of leave types include:</span></span>

- <span data-ttu-id="377fb-107">Betaald verlof</span><span class="sxs-lookup"><span data-stu-id="377fb-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="377fb-108">Onbetaald verlof</span><span class="sxs-lookup"><span data-stu-id="377fb-108">Unpaid leave</span></span>
- <span data-ttu-id="377fb-109">Betaalde vakantie</span><span class="sxs-lookup"><span data-stu-id="377fb-109">Paid vacation</span></span>
- <span data-ttu-id="377fb-110">Ziekteverlof</span><span class="sxs-lookup"><span data-stu-id="377fb-110">Sick leave</span></span>
- <span data-ttu-id="377fb-111">Medisch verlof</span><span class="sxs-lookup"><span data-stu-id="377fb-111">Medical leave</span></span>
- <span data-ttu-id="377fb-112">Familieverlof</span><span class="sxs-lookup"><span data-stu-id="377fb-112">Family leave</span></span>
- <span data-ttu-id="377fb-113">Kortdurende arbeidsongeschiktheid</span><span class="sxs-lookup"><span data-stu-id="377fb-113">Short-term disability</span></span>
- <span data-ttu-id="377fb-114">Verlof bij sterfgeval</span><span class="sxs-lookup"><span data-stu-id="377fb-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="377fb-115">Een verloftype toevoegen</span><span class="sxs-lookup"><span data-stu-id="377fb-115">Add a leave type</span></span>

1. <span data-ttu-id="377fb-116">Selecteer op de pagina **Verlof en verzuim** het tabblad **Koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="377fb-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="377fb-117">Selecteer onder **Instellingen** de optie **Verlof- en verzuimtypen**.</span><span class="sxs-lookup"><span data-stu-id="377fb-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="377fb-118">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="377fb-118">Select **New**.</span></span>

4. <span data-ttu-id="377fb-119">Voer een naam in voor het verloftype onder **Type**, selecteer een werkstroom bij **Werkstroom-id** en voer een beschrijving in onder **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="377fb-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="377fb-120">Selecteer bij **Algemeen** de optie **Geen**, **Gepland** of **Ongepland** in de vervolgkeuzelijst **Categorie**.</span><span class="sxs-lookup"><span data-stu-id="377fb-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="377fb-121">Selecteer een inkomstencode in de vervolgkeuzelijst **Inkomstencode**.</span><span class="sxs-lookup"><span data-stu-id="377fb-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="377fb-122">Geef onder **Redencode vereist** aan of u een redencode wilt vereisen.</span><span class="sxs-lookup"><span data-stu-id="377fb-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="377fb-123">Als u redencodes wilt vereisen, moet u deze mogelijk toevoegen.</span><span class="sxs-lookup"><span data-stu-id="377fb-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="377fb-124">Selecteer onder **Redencodes** de optie **Toevoegen**, selecteer een redencode en schakel vervolgens het selectievakje **Ingeschakeld** hiernaast in.</span><span class="sxs-lookup"><span data-stu-id="377fb-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="377fb-125">Kies onder **Toegang tot geselecteerde rollen beperken** of u de toegang wilt beperken.</span><span class="sxs-lookup"><span data-stu-id="377fb-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="377fb-126">Selecteer vervolgens de beveiligingsrollen onder **Beveiligingsrollen voor dit verloftype**.</span><span class="sxs-lookup"><span data-stu-id="377fb-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="377fb-127">De beveiligingsrollen worden gedefinieerd in de werkstroom die u onder **Werkstroom-id** eerder in deze procedure hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="377fb-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="377fb-128">Kies onder **Agendakleur** welke kleur moet worden weergegeven agenda's voor verlof en verzuim voor dit verloftype.</span><span class="sxs-lookup"><span data-stu-id="377fb-128">Under **Calendar color**, choose what color to display on leave and absence calendars for this leave type.</span></span> 

10. <span data-ttu-id="377fb-129">Geef onder **Uitstelrelaties** op of u wilt dat dit verloftype een ander verloftype uitstelt of door een ander verloftype wordt uitgesteld.</span><span class="sxs-lookup"><span data-stu-id="377fb-129">Under **Suspension relations**, choose if you want to have this leave type either suspend another leave type or be suspended by another leave type.</span></span> <span data-ttu-id="377fb-130">Wanneer een verlofaanvraag wordt ingediend voor het uitstellende verloftype, wordt er automatisch een verlofuitstel gemaakt voor het uitgestelde verloftype.</span><span class="sxs-lookup"><span data-stu-id="377fb-130">When a leave of absence request is submitted for the suspending leave type, a leave suspension will automatically be created for the suspended leave type.</span></span> 

10. <span data-ttu-id="377fb-131">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="377fb-131">Select **Save**.</span></span>

## <a name="configure-leave-type-rules"></a><span data-ttu-id="377fb-132">Regels voor verloftypen configureren</span><span class="sxs-lookup"><span data-stu-id="377fb-132">Configure leave type rules</span></span>

1. <span data-ttu-id="377fb-133">Stel afrondingsopties in voor het verloftype.</span><span class="sxs-lookup"><span data-stu-id="377fb-133">Set rounding options for the leave type.</span></span> <span data-ttu-id="377fb-134">De beschikbare opties zijn **Geen**, **Naar boven**, **Naar beneden** en **Dichtstbijzijnde**.</span><span class="sxs-lookup"><span data-stu-id="377fb-134">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="377fb-135">U kunt ook een afrondingsprecisie instellen voor het verloftype.</span><span class="sxs-lookup"><span data-stu-id="377fb-135">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="377fb-136">Stel **Feestdagcorrectie** in voor het verloftype.</span><span class="sxs-lookup"><span data-stu-id="377fb-136">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="377fb-137">Wanneer u deze optie selecteert, gebruikt Human Resources het aantal feestdagen dat op een werkdag valt om te bepalen hoe het verlof moet worden opgebouwd voor het verloftype.</span><span class="sxs-lookup"><span data-stu-id="377fb-137">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="377fb-138">Als kerstdag bijvoorbeeld op een maandag valt, trekt Human Resources een dag af van het verloftype bij het verwerken van toerekeningen.</span><span class="sxs-lookup"><span data-stu-id="377fb-138">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="377fb-139">U kunt feestdage instellen in de werktijdkalender.</span><span class="sxs-lookup"><span data-stu-id="377fb-139">You set holidays in the working time calendar.</span></span> <span data-ttu-id="377fb-140">Zie [Een werktijdenkalender maken](hr-leave-and-absence-working-time-calendar.md) voor meer informatie</span><span class="sxs-lookup"><span data-stu-id="377fb-140">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>
   
 3. <span data-ttu-id="377fb-141">Stel **Verloftype voor transporteren** in voor het verloftype.</span><span class="sxs-lookup"><span data-stu-id="377fb-141">Set **Carry-forward leave type** for the leave type.</span></span> <span data-ttu-id="377fb-142">Wanneer u deze optie selecteert, worden transportsaldi overgeboekt naar het opgegeven verloftype.</span><span class="sxs-lookup"><span data-stu-id="377fb-142">When you select this option, any carry-forward balances will be transferred to the specified leave type.</span></span> <span data-ttu-id="377fb-143">Het verloftype voor transporteren moet ook worden opgenomen in het plan voor verlof en verzuim.</span><span class="sxs-lookup"><span data-stu-id="377fb-143">The carry-forward leave type also needs to be included in the leave and absence plan.</span></span> 
 
4. <span data-ttu-id="377fb-144">Definieer **vervalregels** voor het verloftype.</span><span class="sxs-lookup"><span data-stu-id="377fb-144">Define **Expiration rules** for the leave type.</span></span> <span data-ttu-id="377fb-145">Wanneer u deze optie configureert, kunt u als eenheid voor dagen of maanden kiezen en de duur instellen voor de vervaldatum.</span><span class="sxs-lookup"><span data-stu-id="377fb-145">When you configure this option, you can choose the unit of days or months and set the duration for the expiration.</span></span> <span data-ttu-id="377fb-146">De ingangsdatum van de vervaldatumregel wordt gebruikt om te bepalen wanneer moet worden begonnen met het uitvoeren van de batchtaak die de verlofvervaldatum verwerkt, of de datum waarop de regel van kracht wordt.</span><span class="sxs-lookup"><span data-stu-id="377fb-146">The effective date of the expiration rule is used to determine when to start running the batch job that processes the leave expiration, or the date when the rule takes effect.</span></span> <span data-ttu-id="377fb-147">De vervaldatum zelf is altijd op de begindatum van de toerekeningsperiode.</span><span class="sxs-lookup"><span data-stu-id="377fb-147">The expiration itself will always occur on the accrual period start date.</span></span> <span data-ttu-id="377fb-148">Als de begindatum van de toerekeningsperiode bijvoorbeeld 3 augustus 2021 is en de vervaldatumregel is ingesteld op 6 maanden, wordt de regel verwerkt op basis van de vervaldatumverschuiving vanaf de begindatum van de toerekeningsperiode, zodat deze wordt uitgevoerd op 3 februari 2022.</span><span class="sxs-lookup"><span data-stu-id="377fb-148">For example, if the accrual period start date is August 3, 2021, and the expiration rule was set at 6 months, the rule will be processed based on the expiration offset from the accrual period start date, so it would be executed on February 3, 2022.</span></span> <span data-ttu-id="377fb-149">Alle verlofsaldi die aanwezig zijn op het tijdstip van de vervaldatum, worden afgetrokken van het verloftype en worden weergegeven in het verlofsaldo.</span><span class="sxs-lookup"><span data-stu-id="377fb-149">Any leave balances that exist at the time of expiry will be subtracted from the leave type and will be reflected in the leave balance.</span></span>
 
## <a name="see-also"></a><span data-ttu-id="377fb-150">Zie ook</span><span class="sxs-lookup"><span data-stu-id="377fb-150">See also</span></span>

- [<span data-ttu-id="377fb-151">Overzicht van verlof en verzuim</span><span class="sxs-lookup"><span data-stu-id="377fb-151">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="377fb-152">Een plan voor verlof en verzuim maken</span><span class="sxs-lookup"><span data-stu-id="377fb-152">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="377fb-153">Een werktijdenkalender maken</span><span class="sxs-lookup"><span data-stu-id="377fb-153">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
- [<span data-ttu-id="377fb-154">Verlof uitstellen</span><span class="sxs-lookup"><span data-stu-id="377fb-154">Suspend leave</span></span>](hr-leave-and-absence-suspend-leave.md)
- [<span data-ttu-id="377fb-155">Een werkstroom maken voor het aanvragen voor het kopen en verkopen van verlof</span><span class="sxs-lookup"><span data-stu-id="377fb-155">Create a buy and sell leave request workflow</span></span>](hr-leave-and-absence-buy-sell-workflow.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
