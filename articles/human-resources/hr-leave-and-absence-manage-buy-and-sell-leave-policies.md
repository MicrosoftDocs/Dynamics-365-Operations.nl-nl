---
title: Beleid voor het kopen en verkopen van verlof beheren
description: In Dynamics 365 Human Resources kunt u instellen dat werknemers verlof kunnen kopen en verkopen.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 859445f2b6e980b5960e512e69129f6a8fc6df2b
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429008"
---
# <a name="manage-buy-and-sell-leave-policies"></a><span data-ttu-id="e96af-103">Beleid voor het kopen en verkopen van verlof beheren</span><span class="sxs-lookup"><span data-stu-id="e96af-103">Manage buy and sell leave policies</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="e96af-104">U kunt instellen dat werknemers verlof kunnen kopen door een beleid voor het kopen van verlof te maken.</span><span class="sxs-lookup"><span data-stu-id="e96af-104">You can enable employees to buy leave by creating a buy leave policy.</span></span>  

## <a name="enable-employees-to-buy-and-sell-leave"></a><span data-ttu-id="e96af-105">Toestaan dat werknemers verlof kopen en verkopen</span><span class="sxs-lookup"><span data-stu-id="e96af-105">Enable employees to buy and sell leave</span></span>

1. <span data-ttu-id="e96af-106">Op de pagina **Verlof- en verzuimparameters** selecteert u **Ja** voor **Werknemers toestaan om verlof te kopen**.</span><span class="sxs-lookup"><span data-stu-id="e96af-106">On the **Leave and absence parameters** page, select **Yes** for **Allow employees to buy leave**.</span></span> 

## <a name="create-a-buy-leave-policy"></a><span data-ttu-id="e96af-107">Een beleid voor het kopen van verlof maken</span><span class="sxs-lookup"><span data-stu-id="e96af-107">Create a buy leave policy</span></span>

1. <span data-ttu-id="e96af-108">Selecteer op de pagina **Verlof en verzuim** het tabblad **Koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="e96af-108">On the **Leave and absence** page, select the **Links** tab.</span></span> 

2. <span data-ttu-id="e96af-109">Selecteer **Beleid voor kopen en verkopen van verlof**.</span><span class="sxs-lookup"><span data-stu-id="e96af-109">Select **Buy and sell leave policy**.</span></span>

3. <span data-ttu-id="e96af-110">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="e96af-110">Select **New**.</span></span>

4. <span data-ttu-id="e96af-111">Voer een **naam** en **omschrijving** voor het beleid in onder **Beleid voor kopen en verkopen van verlof**.</span><span class="sxs-lookup"><span data-stu-id="e96af-111">Enter a **Name** and **Description** for the policy under **Buy and sell leave policy**.</span></span> 

5. <span data-ttu-id="e96af-112">Selecteer een **beleidstype**.</span><span class="sxs-lookup"><span data-stu-id="e96af-112">Select a **Policy type**.</span></span> 

   <span data-ttu-id="e96af-113">De beschikbare beleidstypen zijn **Bedrag** en **Uren per week**.</span><span class="sxs-lookup"><span data-stu-id="e96af-113">The available policy types are **Amount** and **Hours per week**.</span></span> <span data-ttu-id="e96af-114">Selecteer **Bedrag** om een **vast bedrag** in te voeren voor de maximumbedragen die werknemers kunnen kopen en verkopen.</span><span class="sxs-lookup"><span data-stu-id="e96af-114">Select **Amount** to enter a **Fixed amount** for the maximum amounts employees can buy and sell.</span></span> <span data-ttu-id="e96af-115">Als u **Uren per week** selecteert, wordt de werktijd die is gedefinieerd in de toegewezen werktijdkalender van de werknemer gebruikt om het maximumbedrag van het beleid te bepalen.</span><span class="sxs-lookup"><span data-stu-id="e96af-115">If you select **Hours per week**, the working time defined in the employee's assigned working time calendar is used to determine the maximum amount of the policy.</span></span> 

6. <span data-ttu-id="e96af-116">Selecteer een **begindatum** en **einddatum** voor het beleid.</span><span class="sxs-lookup"><span data-stu-id="e96af-116">Select a **Start date** and **End date** for the policy.</span></span> <span data-ttu-id="e96af-117">Aanvragen om verlof te kopen of verkopen zijn alleen beschikbaar voor verzending tijdens dit tijdsbestek.</span><span class="sxs-lookup"><span data-stu-id="e96af-117">Requests to buy or sell leave will only be available for submission during this time frame.</span></span> 

7. <span data-ttu-id="e96af-118">Selecteer onder **Beleid voor kopen** de optie **Fulltime-equivalentie** (FTE) om het maximumbedrag te aan te passen aan de gedefinieerde FTE voor de functie van de werknemer.</span><span class="sxs-lookup"><span data-stu-id="e96af-118">Under **Buy policy**, select **Full time equivalency** (FTE) to prorate the maximum amount based on the FTE defined on the employee's position.</span></span> <span data-ttu-id="e96af-119">Als het type beleid **Bedrag** is, voert u een **vast maximumbedrag** in.</span><span class="sxs-lookup"><span data-stu-id="e96af-119">If the policy type is **Amount**, enter a **Maximum fixed amount**.</span></span> 

8. <span data-ttu-id="e96af-120">Selecteer **Toevoegen** om de verloftypen toe te voegen die werknemers kunnen kopen.</span><span class="sxs-lookup"><span data-stu-id="e96af-120">Select **Add** to add the leave types for employees to buy leave.</span></span> <span data-ttu-id="e96af-121">U kunt meerdere verloftypen aan het beleid toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e96af-121">You can add multiple leave types to the policy.</span></span> 

9. <span data-ttu-id="e96af-122">Voer de **servicemaanden** voor het verloftype in om verschillende servicemaanden in te schakelen om het maximumbedrag te bepalen dat een werknemer kan kopen.</span><span class="sxs-lookup"><span data-stu-id="e96af-122">Enter the **Months of service** for the leave type to enable different months of service to determine the maximum amount an employee can buy.</span></span> 

10. <span data-ttu-id="e96af-123">Voer het **maximale bedrag** in voor het verloftype.</span><span class="sxs-lookup"><span data-stu-id="e96af-123">Enter the **Maximum amount** for the leave type.</span></span> 

11. <span data-ttu-id="e96af-124">Hier kunt u de **snelheid** invoeren waarmee de werknemer het verlof koopt.</span><span class="sxs-lookup"><span data-stu-id="e96af-124">Enter the **Rate** at which the employee will buy the leave.</span></span> 

12. <span data-ttu-id="e96af-125">Voer desgewenst de **inkomstencode** in die moet worden gebruikt voor het kopen van verlof.</span><span class="sxs-lookup"><span data-stu-id="e96af-125">Optionally enter the **Earning code** to be used for buying leave.</span></span> 

13. <span data-ttu-id="e96af-126">U kunt ook instellen of FTE moet worden gebruikt om het maximumbedrag voor het verloftype te bepalen.</span><span class="sxs-lookup"><span data-stu-id="e96af-126">Optionally set whether to use FTE to determine the maximum amount for the leave type.</span></span> 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a><span data-ttu-id="e96af-127">Het beleid voor kopen en verkopen van verlof toevoegen aan een plan voor verlof en verzuim</span><span class="sxs-lookup"><span data-stu-id="e96af-127">Add the buy and sell leave policy to a leave and absence plan</span></span>

1. <span data-ttu-id="e96af-128">Selecteer op de pagina **Verlof en verzuim** een plan voor verlof en verzuim.</span><span class="sxs-lookup"><span data-stu-id="e96af-128">On the **Leave and absence** page, select a leave and absence plan.</span></span>

2. <span data-ttu-id="e96af-129">Selecteer onder **Regels** de optie **Beleid voor kopen en verkopen van verlof**.</span><span class="sxs-lookup"><span data-stu-id="e96af-129">Under **Rules**, select **Buy and sell leave policy**.</span></span>

## <a name="see-also"></a><span data-ttu-id="e96af-130">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e96af-130">See also</span></span>

[<span data-ttu-id="e96af-131">Overzicht van verlof en verzuim</span><span class="sxs-lookup"><span data-stu-id="e96af-131">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="e96af-132">Verlof- en verzuimtypen configureren</span><span class="sxs-lookup"><span data-stu-id="e96af-132">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)</br>
[<span data-ttu-id="e96af-133">Verlof- en verzuimplannen toerekenen</span><span class="sxs-lookup"><span data-stu-id="e96af-133">Accrue leave and absence plans</span></span>](hr-leave-and-absence-accrue.md)</br>
[<span data-ttu-id="e96af-134">Verlof inkopen en verkopen</span><span class="sxs-lookup"><span data-stu-id="e96af-134">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

