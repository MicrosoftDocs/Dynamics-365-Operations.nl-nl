---
title: Beleid voor het kopen en verkopen van verlof beheren
description: In Dynamics 365 Human Resources kunt u instellen dat werknemers verlof kunnen kopen en verkopen.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2020
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
ms.openlocfilehash: 55d29c42cc1b2d69517e2fcd458ee6a1bdf5277f
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712105"
---
# <a name="manage-buy-and-sell-leave-policies"></a><span data-ttu-id="a758b-103">Beleid voor verlof inkopen/verkopen beheren</span><span class="sxs-lookup"><span data-stu-id="a758b-103">Manage buy and sell leave policies</span></span>

<span data-ttu-id="a758b-104">U kunt werknemers in staat stellen om verlof te kopen en te verkopen door een beleid voor het kopen en verkopen van verlof te maken.</span><span class="sxs-lookup"><span data-stu-id="a758b-104">You can enable employees to buy and sell leave by creating a buy and sell leave policy.</span></span> <span data-ttu-id="a758b-105">U kunt dit beleid configureren om een werkstroom voor goedkeuringen te gebruiken, maximumbedragen en -tarieven in te stellen en tarieven voor kopen en verkopen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="a758b-105">You can configure these policies to use workflow for approvals, set maximum amounts and rates, and set rates for buying and selling.</span></span> 

## <a name="enable-employees-to-buy-and-sell-leave"></a><span data-ttu-id="a758b-106">Toestaan dat werknemers verlof kopen en verkopen</span><span class="sxs-lookup"><span data-stu-id="a758b-106">Enable employees to buy and sell leave</span></span>

1. <span data-ttu-id="a758b-107">Op de pagina **Verlof- en verzuimparameters** selecteert u **Ja** voor **Werknemers toestaan om verlof te kopen** en **Werknemers toestaan om verlof te verkopen**.</span><span class="sxs-lookup"><span data-stu-id="a758b-107">On the **Leave and absence parameters** page, select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span>

## <a name="create-a-buy-and-sell-leave-policy"></a><span data-ttu-id="a758b-108">Een beleid voor het kopen en verkopen van verlof maken</span><span class="sxs-lookup"><span data-stu-id="a758b-108">Create a buy and sell leave policy</span></span>

1. <span data-ttu-id="a758b-109">Selecteer op de pagina **Verlof en verzuim** het tabblad **Koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="a758b-109">On the **Leave and absence** page, select the **Links** tab.</span></span> 

2. <span data-ttu-id="a758b-110">Selecteer **Beleid voor kopen en verkopen van verlof**.</span><span class="sxs-lookup"><span data-stu-id="a758b-110">Select **Buy and sell leave policy**.</span></span>

3. <span data-ttu-id="a758b-111">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="a758b-111">Select **New**.</span></span>

4. <span data-ttu-id="a758b-112">Voer een **naam** en **omschrijving** voor het beleid in onder **Beleid voor kopen en verkopen van verlof**.</span><span class="sxs-lookup"><span data-stu-id="a758b-112">Enter a **Name** and **Description** for the policy under **Buy and sell leave policy**.</span></span> 

5. <span data-ttu-id="a758b-113">Selecteer een **beleidstype**.</span><span class="sxs-lookup"><span data-stu-id="a758b-113">Select a **Policy type**.</span></span> 

   <span data-ttu-id="a758b-114">De beschikbare beleidstypen zijn **Bedrag** en **Uren per week**.</span><span class="sxs-lookup"><span data-stu-id="a758b-114">The available policy types are **Amount** and **Hours per week**.</span></span> <span data-ttu-id="a758b-115">Selecteer **Bedrag** om een **vast bedrag** in te voeren voor de maximumbedragen die werknemers kunnen kopen en verkopen.</span><span class="sxs-lookup"><span data-stu-id="a758b-115">Select **Amount** to enter a **Fixed amount** for the maximum amounts employees can buy and sell.</span></span> <span data-ttu-id="a758b-116">Als u **Uren per week** selecteert, wordt de werktijd die is gedefinieerd in de toegewezen werktijdkalender van de werknemer gebruikt om het maximumbedrag van het beleid te bepalen.</span><span class="sxs-lookup"><span data-stu-id="a758b-116">If you select **Hours per week**, the working time defined in the employee's assigned working time calendar is used to determine the maximum amount of the policy.</span></span> 

6. <span data-ttu-id="a758b-117">Selecteer een **begindatum** en **einddatum** voor het beleid.</span><span class="sxs-lookup"><span data-stu-id="a758b-117">Select a **Start date** and **End date** for the policy.</span></span> <span data-ttu-id="a758b-118">Aanvragen om verlof te kopen of verkopen zijn alleen beschikbaar voor verzending tijdens dit tijdsbestek.</span><span class="sxs-lookup"><span data-stu-id="a758b-118">Requests to buy or sell leave will only be available for submission during this time frame.</span></span> 

7. <span data-ttu-id="a758b-119">Selecteer een **Werkstroom-id** voor het beleid.</span><span class="sxs-lookup"><span data-stu-id="a758b-119">Select a **Workflow ID** for the policy.</span></span> <span data-ttu-id="a758b-120">Bij koop- en verkoopaanvragen wordt deze werkstroom gebruikt voor controle en goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="a758b-120">Any buy and sell requests will use this workflow for review and approval.</span></span> 

8. <span data-ttu-id="a758b-121">Selecteer onder **Beleid voor kopen** de optie **Fulltime-equivalentie** (FTE) om het maximumbedrag te aan te passen aan de gedefinieerde FTE voor de functie van de werknemer.</span><span class="sxs-lookup"><span data-stu-id="a758b-121">Under **Buy policy**, select **Full time equivalency** (FTE) to prorate the maximum amount based on the FTE defined on the employee's position.</span></span> <span data-ttu-id="a758b-122">Als het type beleid **Bedrag** is, voert u een **vast maximumbedrag** in.</span><span class="sxs-lookup"><span data-stu-id="a758b-122">If the policy type is **Amount**, enter a **Maximum fixed amount**.</span></span> 

9. <span data-ttu-id="a758b-123">Selecteer **Toevoegen** om de verloftypen toe te voegen die werknemers kunnen kopen.</span><span class="sxs-lookup"><span data-stu-id="a758b-123">Select **Add** to add the leave types for employees to buy leave.</span></span> <span data-ttu-id="a758b-124">U kunt meerdere verloftypen aan het beleid toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a758b-124">You can add multiple leave types to the policy.</span></span> 

10. <span data-ttu-id="a758b-125">Voer de **servicemaanden** voor het verloftype in om verschillende servicemaanden in te schakelen om het maximumbedrag te bepalen dat een werknemer kan kopen.</span><span class="sxs-lookup"><span data-stu-id="a758b-125">Enter the **Months of service** for the leave type to enable different months of service to determine the maximum amount an employee can buy.</span></span> 

11. <span data-ttu-id="a758b-126">Voer het **maximale bedrag** in voor het verloftype.</span><span class="sxs-lookup"><span data-stu-id="a758b-126">Enter the **Maximum amount** for the leave type.</span></span> 

12. <span data-ttu-id="a758b-127">Hier kunt u de **snelheid** invoeren waarmee de werknemer het verlof koopt.</span><span class="sxs-lookup"><span data-stu-id="a758b-127">Enter the **Rate** at which the employee will buy the leave.</span></span> 

13. <span data-ttu-id="a758b-128">Voer desgewenst de **inkomstencode** in die moet worden gebruikt voor het kopen van verlof.</span><span class="sxs-lookup"><span data-stu-id="a758b-128">Optionally enter the **Earning code** to be used for buying leave.</span></span> 

14. <span data-ttu-id="a758b-129">U kunt ook instellen of FTE moet worden gebruikt om het maximumbedrag voor het verloftype te bepalen.</span><span class="sxs-lookup"><span data-stu-id="a758b-129">Optionally set whether to use FTE to determine the maximum amount for the leave type.</span></span> 

15. <span data-ttu-id="a758b-130">Volg de stappen 8 tot en met 14 onder **Verkoopbeleid** om een verkoopbeleid te maken.</span><span class="sxs-lookup"><span data-stu-id="a758b-130">To create a sell policy, follow steps 8 through 14 under **Sell policy**.</span></span> 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a><span data-ttu-id="a758b-131">Het beleid voor kopen en verkopen van verlof toevoegen aan een plan voor verlof en verzuim</span><span class="sxs-lookup"><span data-stu-id="a758b-131">Add the buy and sell leave policy to a leave and absence plan</span></span>

1. <span data-ttu-id="a758b-132">Selecteer op de pagina **Verlof en verzuim** een plan voor verlof en verzuim.</span><span class="sxs-lookup"><span data-stu-id="a758b-132">On the **Leave and absence** page, select a leave and absence plan.</span></span>

2. <span data-ttu-id="a758b-133">Selecteer onder **Regels** de optie **Beleid voor kopen en verkopen van verlof**.</span><span class="sxs-lookup"><span data-stu-id="a758b-133">Under **Rules**, select **Buy and sell leave policy**.</span></span>

## <a name="see-also"></a><span data-ttu-id="a758b-134">Zie ook</span><span class="sxs-lookup"><span data-stu-id="a758b-134">See also</span></span>

[<span data-ttu-id="a758b-135">Overzicht van verlof en verzuim</span><span class="sxs-lookup"><span data-stu-id="a758b-135">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="a758b-136">Verlof- en verzuimtypen configureren</span><span class="sxs-lookup"><span data-stu-id="a758b-136">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)</br>
[<span data-ttu-id="a758b-137">Verlof- en verzuimplannen toerekenen</span><span class="sxs-lookup"><span data-stu-id="a758b-137">Accrue leave and absence plans</span></span>](hr-leave-and-absence-accrue.md)</br>
[<span data-ttu-id="a758b-138">Verlof inkopen en verkopen</span><span class="sxs-lookup"><span data-stu-id="a758b-138">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

