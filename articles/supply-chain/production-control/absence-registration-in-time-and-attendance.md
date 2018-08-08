---
title: Verzuimregistratie in Tijd en aanwezigheid
description: In dit onderwerp wordt uitgelegd hoe u verzuimregistraties afhandelt in Tijd en aanwezigheid.
author: johanhoffmann
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 7ef244d5abf762bcaab426cf1cefb232383a8109
ms.contentlocale: nl-nl
ms.lasthandoff: 08/07/2018

---

# <a name="absence-registration-in-time-and-attendance"></a><span data-ttu-id="20584-103">Verzuimregistratie in Tijd en aanwezigheid</span><span class="sxs-lookup"><span data-stu-id="20584-103">Absence registration in Time and attendance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="20584-104">In dit onderwerp worden de concepten voor verzuim beschreven en wordt uitgelegd hoe u verzuim afhandelt in Tijd en aanwezigheid.</span><span class="sxs-lookup"><span data-stu-id="20584-104">This topic describes the concepts for absence and explains how to handle absence in Time and attendance.</span></span>

## <a name="absence-that-is-based-on-regular-work-hours"></a><span data-ttu-id="20584-105">Verzuim dat is gebaseerd op de normale kantooruren</span><span class="sxs-lookup"><span data-stu-id="20584-105">Absence that is based on regular work hours</span></span>

<span data-ttu-id="20584-106">Werknemers worden beschouwd als afwezig voor alle uren die ze niet werken tijdens hun normale werkuren.</span><span class="sxs-lookup"><span data-stu-id="20584-106">Workers are considered absent for any hours that they don't work during their regular work hours.</span></span> <span data-ttu-id="20584-107">Normale werkuren worden gedefinieerd in het standaardtijdprofiel van een werknemer.</span><span class="sxs-lookup"><span data-stu-id="20584-107">Regular work hours are defined in a worker's standard time profile.</span></span>

<span data-ttu-id="20584-108">Een werknemer kan bijvoorbeeld werken op basis van een dagprofiel met een inkloktijd van 07:00 uur en een uitkloktijd van 15:00 uur.</span><span class="sxs-lookup"><span data-stu-id="20584-108">For example, a worker is working on a day profile that has clock-in at 7:00 AM and clock-out at 3:00 PM.</span></span> <span data-ttu-id="20584-109">Als de werknemer om 09:00 uur inklokt, wordt hij van 07:00 tot 09:00 uur als afwezig beschouwd voor die dag.</span><span class="sxs-lookup"><span data-stu-id="20584-109">If the worker clocks in at 9:00 AM, he is considered absent from 7:00 AM to 9:00 AM on that day.</span></span>

<span data-ttu-id="20584-110">In dat geval dienen werknemers een reden voor hun afwezigheid in te voeren.</span><span class="sxs-lookup"><span data-stu-id="20584-110">In this case, workers are prompted to enter a reason for their absence.</span></span> <span data-ttu-id="20584-111">Ze kunnen een reden opgeven door een verzuimcode te selecteren.</span><span class="sxs-lookup"><span data-stu-id="20584-111">They can specify a reason by selecting an absence code.</span></span>

## <a name="absence-codes"></a><span data-ttu-id="20584-112">Verzuimcodes</span><span class="sxs-lookup"><span data-stu-id="20584-112">Absence codes</span></span>

<span data-ttu-id="20584-113">Verzuimcodes definiëren de verschillende verzuimtypen.</span><span class="sxs-lookup"><span data-stu-id="20584-113">Absence codes define the various types of absence.</span></span> <span data-ttu-id="20584-114">Verzuimcodes worden gedefinieerd door het bedrijf.</span><span class="sxs-lookup"><span data-stu-id="20584-114">Absence codes are defined by the company.</span></span>

<span data-ttu-id="20584-115">Verschillende regels kunnen worden toegepast op verzuimcodes.</span><span class="sxs-lookup"><span data-stu-id="20584-115">Various rules can be applied to absence codes.</span></span> <span data-ttu-id="20584-116">Een verzuimcode kan bijvoorbeeld zo worden geconfigureerd dat op basis hiervan salaris wordt ingehouden of wordt uitgekeerd.</span><span class="sxs-lookup"><span data-stu-id="20584-116">For example, an absence code can be configured to deduct or grant pay.</span></span>

<span data-ttu-id="20584-117">Een bedrijf kan bijvoorbeeld een verzuimcode **Te laat** definiëren voor werknemers die zonder goede reden te laat komen.</span><span class="sxs-lookup"><span data-stu-id="20584-117">For example, a company defines a **Late** absence code that workers use if they come in late and don't have a good reason.</span></span> <span data-ttu-id="20584-118">Het bedrijf definieert ook een verzuimcode **Interne cursus** die werknemers kunnen gebruiken voor de tijd die ze besteden aan het bijwonen van interne cursussen.</span><span class="sxs-lookup"><span data-stu-id="20584-118">The company also defines an **Internal course** absence code that workers use for time that they spend attending internal courses.</span></span> <span data-ttu-id="20584-119">Deze verzuimcodes kunnen zo worden ingesteld dat met **Te laat** salaris van een werknemer wordt ingehouden en met **Interne cursus** geen salaris wordt ingehouden.</span><span class="sxs-lookup"><span data-stu-id="20584-119">These absence codes can be set up so that **Late** deducts from a worker's pay but **Internal course** doesn't deduct from a worker's pay.</span></span>

<span data-ttu-id="20584-120">U kunt automatische verzuimcodes instellen.</span><span class="sxs-lookup"><span data-stu-id="20584-120">You can set up automatic absence codes.</span></span> <span data-ttu-id="20584-121">Deze verzuimcodes kunnen worden gebruikt voor het berekenen van de gewerkte tijd door een werknemer wanneer er geen verzuim is geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="20584-121">These absence codes can be used to calculate a worker's time when no absence is registered.</span></span> <span data-ttu-id="20584-122">Het tijdprofiel van de werknemer bepaalt of de verzuimcode voor standaardtijd of flextijd wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="20584-122">The worker's time profile determines whether the absence code for standard time or flex time is used.</span></span>

### <a name="set-up-standard-time-and-flex-time"></a><span data-ttu-id="20584-123">Standaardtijd en flextijd instellen</span><span class="sxs-lookup"><span data-stu-id="20584-123">Set up standard time and flex time</span></span>

- <span data-ttu-id="20584-124">Configureer de parameters voor standaardtijd en flextijd met de opties **Verzuim automatisch invoegen** en **Flextijd automatisch invoegen-** op de pagina **Parameters in Tijd en aanwezigheid**.</span><span class="sxs-lookup"><span data-stu-id="20584-124">Configure the parameters for standard time and flex time by using the **Auto insert absence** and **Auto insert Flex-** options on the **Time and attendance parameters** page.</span></span>

## <a name="absence-groups"></a><span data-ttu-id="20584-125">Verzuimgroepen</span><span class="sxs-lookup"><span data-stu-id="20584-125">Absence groups</span></span>

<span data-ttu-id="20584-126">Verzuimcodes worden gegroepeerd in verzuimgroepen.</span><span class="sxs-lookup"><span data-stu-id="20584-126">Absence codes are grouped into absence groups.</span></span> <span data-ttu-id="20584-127">U gebruikt verzuimgroepen om groepscodes met gemeenschappelijke kenmerken te groeperen.</span><span class="sxs-lookup"><span data-stu-id="20584-127">You use absence groups to group absence codes that have common characteristics.</span></span> <span data-ttu-id="20584-128">Voorbeelden zijn onder andere verzuimcodes voor een geldig verzuim of verzuim vanwege een doktersafspraak, verlof of een ziek kind.</span><span class="sxs-lookup"><span data-stu-id="20584-128">Examples include absence codes for a legal absence, or absence because of a doctor's appointment, jury duty, or a sick child.</span></span>

## <a name="planned-absence"></a><span data-ttu-id="20584-129">Gepland verzuim</span><span class="sxs-lookup"><span data-stu-id="20584-129">Planned absence</span></span>

<span data-ttu-id="20584-130">Als u weet dat een werknemer een periode afwezig is, bijvoorbeeld vanwege een aanstaande vakantie, kunt u gepland verzuim gebruiken.</span><span class="sxs-lookup"><span data-stu-id="20584-130">If you know that a worker will be absent for a period, such as an upcoming vacation, you can use planned absence.</span></span> <span data-ttu-id="20584-131">U stelt gepland verzuim in door de verzuimcode zo te configureren dat rekening wordt gehouden met het geplande verzuim.</span><span class="sxs-lookup"><span data-stu-id="20584-131">You set up planned absence by configuring the absence code so that it considers the planned absence.</span></span> <span data-ttu-id="20584-132">Wanneer u een gepland verzuim instelt, wordt u tijdens de afwezigheidsperiode niet gevraagd om een verzuimcode wanneer gebruikerstijdregistraties worden berekend.</span><span class="sxs-lookup"><span data-stu-id="20584-132">When you set up a planned absence, you aren't prompted for an absence code during the absence period when user time registrations are calculated.</span></span> <span data-ttu-id="20584-133">Gepland verzuim kan voor één werknemer worden gedefinieerd, maar u kunt ook een batchtaak opgeven om het geplande verzuim voor werknemers bulksgewijs bij te werken.</span><span class="sxs-lookup"><span data-stu-id="20584-133">Planned absence can be defined for a single worker, or you can define a batch job to bulk update the planned absence for workers.</span></span>

### <a name="set-up-planned-absence"></a><span data-ttu-id="20584-134">Gepland verzuim instellen</span><span class="sxs-lookup"><span data-stu-id="20584-134">Set up planned absence</span></span>

1. <span data-ttu-id="20584-135">Selecteer **HRM** &gt; **Medewerkers** &gt; **Werknemers** en selecteer een werknemer.</span><span class="sxs-lookup"><span data-stu-id="20584-135">Select **Human resources** &gt; **Workers** &gt; **Employees**, and select an employee.</span></span>
2. <span data-ttu-id="20584-136">Selecteer **Tijd** &gt; **Tijdtoewijzingen** &gt; **Registratie van tijdverzuim** en stel het geplande verzuim in.</span><span class="sxs-lookup"><span data-stu-id="20584-136">Select **Time** &gt; **Time assignments** &gt; **Time Absence registration**, and set up the planned absence.</span></span>

## <a name="interrupted-planned-absence"></a><span data-ttu-id="20584-137">Onderbroken gepland verzuim</span><span class="sxs-lookup"><span data-stu-id="20584-137">Interrupted planned absence</span></span>

<span data-ttu-id="20584-138">Als u de optie **Onderbreken** toepast tijdens het instellen van een gepland verzuim, wordt het geplande verzuim onderbroken als de werknemer zich tijdens de periode van het geplande verzuim aanmeldt.</span><span class="sxs-lookup"><span data-stu-id="20584-138">If you apply the **Interrupt** option when you set up a planned absence, the planned absence will be interrupted if the worker signs in during the planned absence period.</span></span> <span data-ttu-id="20584-139">Het geplande verzuim wordt gemarkeerd als **Onderbroken**, maar dit heeft verder geen effect op toekomstige berekeningen.</span><span class="sxs-lookup"><span data-stu-id="20584-139">The planned absence will be marked as **Interrupted** and won't have any effect on future calculations.</span></span>

### <a name="set-up-a-planned-absence-for-interruption"></a><span data-ttu-id="20584-140">Een gepland verzuim voor onderbreking instellen</span><span class="sxs-lookup"><span data-stu-id="20584-140">Set up a planned absence for interruption</span></span>

1. <span data-ttu-id="20584-141">Open de pagina **Registratie van tijdverzuim** op de wijze die wordt beschreven in de procedure voor het instellen van gepland verzuim.</span><span class="sxs-lookup"><span data-stu-id="20584-141">Open the **Time Absence registration** page as described in the procedure for setting up planned absence.</span></span>
2. <span data-ttu-id="20584-142">Selecteer **Onderbreken**.</span><span class="sxs-lookup"><span data-stu-id="20584-142">Select **Interrupt**.</span></span>

<span data-ttu-id="20584-143">De optie **Onderbreken** geldt als er tijd wordt geregistreerd via de werkvloerterminal of het werkvloerapparaat.</span><span class="sxs-lookup"><span data-stu-id="20584-143">The **Interrupt** option applies when time is registered through the shop floor terminal or the shop floor device.</span></span> <span data-ttu-id="20584-144">De optie is niet van toepassing als de registraties worden ingevoerd op de berekenings- en goedkeuringspagina's, of op de pagina **Elektronische prikkaart**.</span><span class="sxs-lookup"><span data-stu-id="20584-144">The option doesn't apply if the registrations are entered on the calculation and approval pages, or on the **Electronic timecard** page.</span></span>

## <a name="examples-of-the-use-of-absence-in-a-flex-profile"></a><span data-ttu-id="20584-145">Voorbeelden van het gebruik van verzuim in een flextijdprofiel</span><span class="sxs-lookup"><span data-stu-id="20584-145">Examples of the use of absence in a flex profile</span></span>

<span data-ttu-id="20584-146">Met de volgende drie voorbeelden wordt aangegeven hoe verzuim wordt berekend in een profiel met flexperioden.</span><span class="sxs-lookup"><span data-stu-id="20584-146">The following three examples show how absence is calculated in a profile that has flex periods.</span></span>

<span data-ttu-id="20584-147">In de voorbeelden wordt het volgende profiel gebruikt:</span><span class="sxs-lookup"><span data-stu-id="20584-147">The examples use the following profile.</span></span>

| <span data-ttu-id="20584-148">Inklokken</span><span class="sxs-lookup"><span data-stu-id="20584-148">Clock-in</span></span> | <span data-ttu-id="20584-149">Standaardtijd</span><span class="sxs-lookup"><span data-stu-id="20584-149">Standard time</span></span>    | <span data-ttu-id="20584-150">Pauze</span><span class="sxs-lookup"><span data-stu-id="20584-150">Break</span></span>             | <span data-ttu-id="20584-151">Standaardtijd</span><span class="sxs-lookup"><span data-stu-id="20584-151">Standard time</span></span> | <span data-ttu-id="20584-152">Flextijd-</span><span class="sxs-lookup"><span data-stu-id="20584-152">Flex-</span></span>        | <span data-ttu-id="20584-153">Uitklokken</span><span class="sxs-lookup"><span data-stu-id="20584-153">Clock-out</span></span> | <span data-ttu-id="20584-154">Flextijd+</span><span class="sxs-lookup"><span data-stu-id="20584-154">Flex+</span></span>        |
|----------|------------------|-------------------|---------------|--------------|-----------|--------------|
| <span data-ttu-id="20584-155">08:00 uur</span><span class="sxs-lookup"><span data-stu-id="20584-155">8 AM</span></span>     | <span data-ttu-id="20584-156">09:00 tot 11:30 uur</span><span class="sxs-lookup"><span data-stu-id="20584-156">9 AM to 11:30 AM</span></span> | <span data-ttu-id="20584-157">11:30 tot 12:00 uur</span><span class="sxs-lookup"><span data-stu-id="20584-157">11:30 AM to 12 PM</span></span> | <span data-ttu-id="20584-158">12:00 tot 15:00 uur</span><span class="sxs-lookup"><span data-stu-id="20584-158">12 PM to 3 PM</span></span> | <span data-ttu-id="20584-159">15:00 tot 16:00 uur</span><span class="sxs-lookup"><span data-stu-id="20584-159">3 PM to 4 PM</span></span> | <span data-ttu-id="20584-160">16:00 uur</span><span class="sxs-lookup"><span data-stu-id="20584-160">4 PM</span></span>      | <span data-ttu-id="20584-161">16:00 tot 18:00 uur</span><span class="sxs-lookup"><span data-stu-id="20584-161">4 PM to 6 PM</span></span> |

### <a name="example-1-signing-out-during-a-flex--period"></a><span data-ttu-id="20584-162">Voorbeeld 1: Afmelden tijdens een periode Flextijd-</span><span class="sxs-lookup"><span data-stu-id="20584-162">Example 1: Signing out during a Flex- period</span></span>

<span data-ttu-id="20584-163">De werknemer klokt in om 08:00 uur en klokt uit om 15:30 uur.</span><span class="sxs-lookup"><span data-stu-id="20584-163">The worker clocks in at 8:00 AM and clocks out at 3:30 PM.</span></span> <span data-ttu-id="20584-164">In dit geval wordt er geen verzuim berekend omdat de werknemer uitklokt tijdens een periode Flextijd- en er wordt een half uur afgetrokken van het flexsaldo van de werknemer.</span><span class="sxs-lookup"><span data-stu-id="20584-164">In this case, because the worker clocks out during a Flex- period, no absence is calculated, and half an hour is deducted from the worker's flex balance.</span></span>

### <a name="example-2-signing-out-in-during-standard-time-period"></a><span data-ttu-id="20584-165">Voorbeeld 2: Afmelden tijdens de periode Standaardtijd</span><span class="sxs-lookup"><span data-stu-id="20584-165">Example 2: Signing out in during Standard time period</span></span>

<span data-ttu-id="20584-166">De werknemer klokt in om 08:00 uur en klokt uit om 14:30 uur.</span><span class="sxs-lookup"><span data-stu-id="20584-166">The worker clocks in at 8:00 AM and clocks out at 2:30 PM.</span></span> <span data-ttu-id="20584-167">In dit geval wordt er wel verzuim berekend omdat de werknemer uitklokt tijdens de periode Standaardtijd. Er wordt van 14:30 tot 16:00 uur verzuim berekend en er wordt een verzuimperiode van 1,5 uur geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="20584-167">In this case, because the worker clocks out during the Standard time period, absence is calculated from 2:30 PM to 4 PM, and an absence period of 1.5 hours is registered.</span></span> <span data-ttu-id="20584-168">Voor die periode is een verzuimcode vereist.</span><span class="sxs-lookup"><span data-stu-id="20584-168">An absence code for that period is required.</span></span>

### <a name="example-3-signing-out-during-a-flex-period"></a><span data-ttu-id="20584-169">Voorbeeld 3: Afmelden tijdens een periode Flextijd+</span><span class="sxs-lookup"><span data-stu-id="20584-169">Example 3: Signing out during a Flex+ period</span></span>

<span data-ttu-id="20584-170">De werknemer klokt in om 08:00 uur en klokt uit om 16:30 uur.</span><span class="sxs-lookup"><span data-stu-id="20584-170">The worker clocks in at 8:00 AM and clocks out at 4:30 PM.</span></span> <span data-ttu-id="20584-171">In dit geval wordt er geen verzuim berekend omdat de werknemer uitklokt tijdens een periode Flextijd+ en wordt er een half uur opgeteld bij het flexsaldo van de werknemer.</span><span class="sxs-lookup"><span data-stu-id="20584-171">In this case, because the worker clocks out during a Flex+ period, no absence is calculated, and half an hour is added to the worker's flex balance.</span></span>

## <a name="absence-in-the-calculation-and-approval-process"></a><span data-ttu-id="20584-172">Verzuim in het berekenings- en goedkeuringsproces</span><span class="sxs-lookup"><span data-stu-id="20584-172">Absence in the calculation and approval process</span></span>

<span data-ttu-id="20584-173">Registraties van werknemerstijd moeten worden berekend en goedgekeurd voordat ze als salarisposten kunnen worden overgebracht naar de salarisadministratie.</span><span class="sxs-lookup"><span data-stu-id="20584-173">Worker time registrations must be calculated and approved before they can be transferred to a payroll system as pay items.</span></span>

<span data-ttu-id="20584-174">Een fiatteur kan de tijdregistraties van een werknemer wijzigen.</span><span class="sxs-lookup"><span data-stu-id="20584-174">An approver can change a worker's time registrations.</span></span> <span data-ttu-id="20584-175">De fiatteur kan zelfs het verzuim wijzigen dat de werknemer heeft geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="20584-175">The approver can even change any absence that the worker has registered.</span></span> <span data-ttu-id="20584-176">Als de fiatteur handmatig een periode met een verzuimcode invoert, wordt de verzuimcode voor die periode niet overschreven door de standaardverzuimcode uit Parameters in Tijd en aanwezigheid.</span><span class="sxs-lookup"><span data-stu-id="20584-176">If the approver manually enters a time period that has an absence code, the absence code for that period isn't overridden by the default absence code from the Time and attendance parameters.</span></span>

<span data-ttu-id="20584-177">Stel, een werknemer klokt in om 10:00 uur en selecteert een verzuimcode waarmee wordt aangegeven dat zij te laat is.</span><span class="sxs-lookup"><span data-stu-id="20584-177">For example, a worker clocks in at 10 AM and selects an absence code that indicates that she is late.</span></span> <span data-ttu-id="20584-178">Later informeert de werknemer haar supervisor dat ze van 08:00 tot 10:00 uur een doktersafspraak had.</span><span class="sxs-lookup"><span data-stu-id="20584-178">Later, the worker informs her supervisor that she had a doctor's appointment from 8 AM to 10 AM.</span></span> <span data-ttu-id="20584-179">Een doktersafspraak mag niet resulteren in het inhouden van salaris.</span><span class="sxs-lookup"><span data-stu-id="20584-179">A doctor's appointment should not cause a deduction in the worker's pay.</span></span> <span data-ttu-id="20584-180">Daarom kan de supervisor in dit geval de twee verzuimuren van 08:00 tot 10:00 uur handmatig aanpassen door een verzuimcode in te voeren die op ziekte duidt.</span><span class="sxs-lookup"><span data-stu-id="20584-180">Therefore, in this case, the supervisor can adjust the two hours of absence from 8 AM to 10 AM by manually entering an absence code that indicates illness for those two hours.</span></span>

### <a name="calculate-and-approve-absence"></a><span data-ttu-id="20584-181">Verzuim berekenen en goedkeuren</span><span class="sxs-lookup"><span data-stu-id="20584-181">Calculate and approve absence</span></span>

- <span data-ttu-id="20584-182">Selecteer **Tijd en aanwezigheid** &gt; **Controleren en goedkeuren** &gt; **Goedkeuren of berekenen**.</span><span class="sxs-lookup"><span data-stu-id="20584-182">Select **Time attendance** &gt; **Review and approve** &gt; **Approve or Calculate**.</span></span>

