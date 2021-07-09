---
title: Kortingsbeheergroepen
description: In dit onderwerp wordt beschreven hoe u kortingsbeheergroepen instelt. Kortingsbeheergroepen kunnen worden gebruikt tijdens kortingsberekeningen en kunnen aan een hoofdrecord worden gekoppeld.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: ee5a195b3d2881ff70fb1f0d4063ed681e874648
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271072"
---
# <a name="rebate-management-groups"></a><span data-ttu-id="679d2-104">Groepen voor kortingsbeheer</span><span class="sxs-lookup"><span data-stu-id="679d2-104">Rebate management groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="679d2-105">Kortingsbeheerberekeningen kunnen worden aangedreven door groepen.</span><span class="sxs-lookup"><span data-stu-id="679d2-105">Rebate management calculations can be driven by groups.</span></span> <span data-ttu-id="679d2-106">Kortingsbeheergroepen kunnen worden gemaakt voor klanten, leveranciers en artikelen.</span><span class="sxs-lookup"><span data-stu-id="679d2-106">Rebate management groups can be created for customers, vendors, and items.</span></span> <span data-ttu-id="679d2-107">Ze kunnen aan een hoofdrecord worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="679d2-107">They can be attached to a master record.</span></span>

## <a name="rebate-management-customer-groups"></a><span data-ttu-id="679d2-108">Klantgroepen voor kortingsbeheer</span><span class="sxs-lookup"><span data-stu-id="679d2-108">Rebate management customer groups</span></span>

<span data-ttu-id="679d2-109">De berekening voor een groep klanten wordt vaak uitgevoerd voor een keten van bedrijven, zoals een supermarktketen of een franchisebedrijf.</span><span class="sxs-lookup"><span data-stu-id="679d2-109">The calculation for a group of customers is often created for a chain of companies, such as a supermarket chain or a franchise company.</span></span> <span data-ttu-id="679d2-110">Dit type berekening is meestal gerelateerd aan een korting.</span><span class="sxs-lookup"><span data-stu-id="679d2-110">This type of calculation is usually related to a rebate.</span></span>

<span data-ttu-id="679d2-111">Een inhouding wordt vaak berekend zonder na te gaan aan wie de in aanmerking komende order is verkocht.</span><span class="sxs-lookup"><span data-stu-id="679d2-111">A deduction is often calculated without considering who the qualifying order was sold to.</span></span> <span data-ttu-id="679d2-112">Er zijn echter uitzonderingen.</span><span class="sxs-lookup"><span data-stu-id="679d2-112">However, there are exceptions.</span></span> <span data-ttu-id="679d2-113">Een licentienemer kan bijvoorbeeld een inhoudingsregeling opstellen waarbij klantgroep A 4 procent ontvangt, maar klantgroep B slechts 3 procent.</span><span class="sxs-lookup"><span data-stu-id="679d2-113">For example, a licensee might create a deduction scheme where customer group A will receive 4 percent, but customer group B will receive only 3 percent.</span></span>

### <a name="set-up-customer-groups"></a><span data-ttu-id="679d2-114">Klantengroepen instellen</span><span class="sxs-lookup"><span data-stu-id="679d2-114">Set up customer groups</span></span>

<span data-ttu-id="679d2-115">Als u wilt werken met klantgroepen voor kortingsbeheer, gaat u naar **Kortingsbeheer \> Kortingsbeheergroepen instellen \> Klantgroepen**.</span><span class="sxs-lookup"><span data-stu-id="679d2-115">To work with Rebate management customer groups, go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span> <span data-ttu-id="679d2-116">U kunt de knoppen in het actiedeelvenster gebruiken om naar behoefte groepen toe te voegen en te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="679d2-116">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="679d2-117">Stel voor elke groep de volgende velden in:</span><span class="sxs-lookup"><span data-stu-id="679d2-117">For each group, set the following fields:</span></span>

- <span data-ttu-id="679d2-118">**Kortingsbeheergroep**: voer een unieke naam voor de groep in.</span><span class="sxs-lookup"><span data-stu-id="679d2-118">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="679d2-119">**Beschrijving**: voer een beschrijving van de groep in om meer informatie te geven over hoe deze moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="679d2-119">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-customer-group-assignments"></a><span data-ttu-id="679d2-120">Toewijzingen van klantgroepen beheren</span><span class="sxs-lookup"><span data-stu-id="679d2-120">Manage customer group assignments</span></span>

<span data-ttu-id="679d2-121">Elke klant kan tot een willekeurig aantal kortingsbeheergroepen behoren.</span><span class="sxs-lookup"><span data-stu-id="679d2-121">Each customer can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="679d2-122">Als u groepsleden wilt weergeven en toewijzen, kunt u beginnen vanuit de groepslijst of de klantenlijst.</span><span class="sxs-lookup"><span data-stu-id="679d2-122">To view and assign group members, you can start from either the group list or the customer list.</span></span>

<span data-ttu-id="679d2-123">Volg deze stappen om klanten voor een geselecteerde groep weer te geven, toe te voegen of te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="679d2-123">To view, add, or remove customers for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="679d2-124">Ga naar **Kortingsbeheer \> Kortingsbeheergroepen instellen \> Klantgroepen**.</span><span class="sxs-lookup"><span data-stu-id="679d2-124">Go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span>
1. <span data-ttu-id="679d2-125">Selecteer de groep die u wilt beheren.</span><span class="sxs-lookup"><span data-stu-id="679d2-125">Select the group to manage.</span></span>
1. <span data-ttu-id="679d2-126">Selecteer in het actievenster de optie **Klanten**.</span><span class="sxs-lookup"><span data-stu-id="679d2-126">On the Action Pane, select **Customers**.</span></span> <span data-ttu-id="679d2-127">De pagina **Kortingsbeheergroepen** wordt weergegeven en toont een lijst met klanten die al lid zijn van de geselecteerde groep.</span><span class="sxs-lookup"><span data-stu-id="679d2-127">The **Rebate management groups** page appears and shows a list of customers that are already members of the selected group.</span></span>
1. <span data-ttu-id="679d2-128">Als u een nieuwe klant wilt toevoegen aan de groep, selecteert u **Nieuw** in het actievenster om een rij toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="679d2-128">To add a new customer to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="679d2-129">Stel daarna het volgende veld in voor de nieuwe rij:</span><span class="sxs-lookup"><span data-stu-id="679d2-129">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="679d2-130">**Klantrekening**: selecteer de klantrekening-id.</span><span class="sxs-lookup"><span data-stu-id="679d2-130">**Customer account** – Select the customer account ID.</span></span>

1. <span data-ttu-id="679d2-131">Als u een klant uit de groep wilt verwijderen, selecteert u de klant en selecteert u vervolgens **Verwijderen** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="679d2-131">To remove a customer from the group, select the customer, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="679d2-132">Volg deze stappen om groepstoewijzingen voor een geselecteerde klant weer te geven, toe te voegen of te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="679d2-132">To view, add, or remove group assignments for a selected customer, follow these steps.</span></span>

1. <span data-ttu-id="679d2-133">Ga naar **Klanten \> Klanten \> Alle klanten**.</span><span class="sxs-lookup"><span data-stu-id="679d2-133">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="679d2-134">Selecteer de klant waarmee u wilt werken.</span><span class="sxs-lookup"><span data-stu-id="679d2-134">Select the customer to work with.</span></span>
1. <span data-ttu-id="679d2-135">Selecteer vervolgens in het actievenster op het tabblad **Klant** in de groep **Kortingsbeheer** de optie **Kortingsbeheergroepen**.</span><span class="sxs-lookup"><span data-stu-id="679d2-135">On the Action Pane, on the **Customer** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="679d2-136">De pagina **Kortingsbeheergroepen** wordt weergegeven en toont een lijst met groepen waartoe de geselecteerde klant al bestaat.</span><span class="sxs-lookup"><span data-stu-id="679d2-136">The **Rebate management groups** page appears and shows a list of groups that the selected customer already belongs to.</span></span>
1. <span data-ttu-id="679d2-137">Als u de klant wilt toevoegen aan een nieuwe groep, selecteert u **Nieuw** in het actievenster om een rij toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="679d2-137">To add the customer to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="679d2-138">Stel daarna het volgende veld in voor de nieuwe rij:</span><span class="sxs-lookup"><span data-stu-id="679d2-138">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="679d2-139">**Kortingsbeheergroep**: selecteer de groep waaraan u de klant wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="679d2-139">**Rebate management group** – Select the group to add the customer to.</span></span>

1. <span data-ttu-id="679d2-140">Als u een klant uit een groep wilt verwijderen, selecteert u de groep en selecteert u vervolgens **Verwijderen** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="679d2-140">To remove a customer from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="rebate-management-vendor-groups"></a><span data-ttu-id="679d2-141">Leveranciersgroepen voor kortingsbeheer</span><span class="sxs-lookup"><span data-stu-id="679d2-141">Rebate management vendor groups</span></span>

<span data-ttu-id="679d2-142">De berekening voor een groep leveranciers wordt vaak gemaakt voor een groep leveringspunten.</span><span class="sxs-lookup"><span data-stu-id="679d2-142">The calculation for a group of vendors is often created for a group of delivery points.</span></span> <span data-ttu-id="679d2-143">Dit type berekening is meestal gerelateerd aan een korting.</span><span class="sxs-lookup"><span data-stu-id="679d2-143">This type of calculation is usually related to a rebate.</span></span>

### <a name="set-up-vendor-groups"></a><span data-ttu-id="679d2-144">Leveranciersgroepen instellen</span><span class="sxs-lookup"><span data-stu-id="679d2-144">Set up vendor groups</span></span>

<span data-ttu-id="679d2-145">Als u wilt werken met leveranciersgroepen voor kortingsbeheer, gaat u naar **Kortingsbeheer \> Kortingsbeheergroepen instellen \> Leveranciersgroepen**.</span><span class="sxs-lookup"><span data-stu-id="679d2-145">To work with Rebate management vendor groups, go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span> <span data-ttu-id="679d2-146">U kunt de knoppen in het actiedeelvenster gebruiken om naar behoefte groepen toe te voegen en te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="679d2-146">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="679d2-147">Stel voor elke groep de volgende velden in:</span><span class="sxs-lookup"><span data-stu-id="679d2-147">For each group, set the following fields:</span></span>

- <span data-ttu-id="679d2-148">**Kortingsbeheergroep**: voer een unieke naam voor de groep in.</span><span class="sxs-lookup"><span data-stu-id="679d2-148">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="679d2-149">**Beschrijving**: voer een beschrijving van de groep in om meer informatie te geven over hoe deze moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="679d2-149">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-vendor-group-assignments"></a><span data-ttu-id="679d2-150">Toewijzingen van leveranciersgroepen beheren</span><span class="sxs-lookup"><span data-stu-id="679d2-150">Manage vendor group assignments</span></span>

<span data-ttu-id="679d2-151">Elke leverancier kan tot een willekeurig aantal kortingsbeheergroepen behoren.</span><span class="sxs-lookup"><span data-stu-id="679d2-151">Each vendor can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="679d2-152">Als u groepsleden wilt weergeven en toewijzen, kunt u beginnen vanuit de groepslijst of de leverancierslijst.</span><span class="sxs-lookup"><span data-stu-id="679d2-152">To view and assign group members, you can start from either the group list or the vendor list.</span></span>

<span data-ttu-id="679d2-153">Volg deze stappen om leveranciers voor een geselecteerde groep weer te geven, toe te voegen of te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="679d2-153">To view, add, or remove vendors for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="679d2-154">Ga naar **Kortingsbeheer \> Kortingsbeheergroepen instellen \> Leveranciersgroepen**.</span><span class="sxs-lookup"><span data-stu-id="679d2-154">Go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span>
1. <span data-ttu-id="679d2-155">Selecteer de groep die u wilt beheren.</span><span class="sxs-lookup"><span data-stu-id="679d2-155">Select the group to manage.</span></span>
1. <span data-ttu-id="679d2-156">Selecteer **Leveranciers** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="679d2-156">On the Action Pane, select **Vendors**.</span></span> <span data-ttu-id="679d2-157">De pagina **Kortingsbeheergroepen** wordt weergegeven en toont een lijst met leveranciers die al lid zijn van de geselecteerde groep.</span><span class="sxs-lookup"><span data-stu-id="679d2-157">The **Rebate management groups** page appears and shows a list of vendors that are already members of the selected group.</span></span>
1. <span data-ttu-id="679d2-158">Als u een nieuwe leverancier wilt toevoegen aan de groep, selecteert u **Nieuw** in het actievenster om een rij toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="679d2-158">To add a new vendor to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="679d2-159">Stel daarna het volgende veld in voor de nieuwe rij:</span><span class="sxs-lookup"><span data-stu-id="679d2-159">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="679d2-160">**Leveranciersrekening**: selecteer de leveranciersrekening-id.</span><span class="sxs-lookup"><span data-stu-id="679d2-160">**Vendor account** – Select the vendor account ID.</span></span>

1. <span data-ttu-id="679d2-161">Als u een leverancier uit de groep wilt verwijderen, selecteert u de leverancier en selecteert u vervolgens **Verwijderen** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="679d2-161">To remove a vendor from the group, select the vendor, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="679d2-162">Volg deze stappen om groepstoewijzingen voor een geselecteerde leverancier weer te geven, toe te voegen of te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="679d2-162">To view, add, or remove group assignments for a selected vendor, follow these steps.</span></span>

1. <span data-ttu-id="679d2-163">Ga naar **Leveranciers \> Leveranciers \> Alle leveranciers**.</span><span class="sxs-lookup"><span data-stu-id="679d2-163">Go to **Accounts payable \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="679d2-164">Selecteer de leverancier waarmee u wilt werken.</span><span class="sxs-lookup"><span data-stu-id="679d2-164">Select the vendor to work with.</span></span>
1. <span data-ttu-id="679d2-165">Selecteer vervolgens in het actievenster op het tabblad **Leverancier** in de groep **Kortingsbeheer** de optie **Kortingsbeheergroepen**.</span><span class="sxs-lookup"><span data-stu-id="679d2-165">On the Action Pane, on the **Vendor** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="679d2-166">De pagina **Kortingsbeheergroepen** wordt weergegeven en toont een lijst met groepen waartoe de geselecteerde leverancier al bestaat.</span><span class="sxs-lookup"><span data-stu-id="679d2-166">The **Rebate management groups** page appears and shows a list of groups that the selected vendor already belongs to.</span></span>
1. <span data-ttu-id="679d2-167">Als u de leverancier wilt toevoegen aan een nieuwe groep, selecteert u **Nieuw** in het actievenster om een rij toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="679d2-167">To add the vendor to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="679d2-168">Stel daarna het volgende veld in voor de nieuwe rij:</span><span class="sxs-lookup"><span data-stu-id="679d2-168">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="679d2-169">**Kortingsbeheergroep**: selecteer de groep waaraan u de leverancier wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="679d2-169">**Rebate management group** – Select the group to add the vendor to.</span></span>

1. <span data-ttu-id="679d2-170">Als u een leverancier uit een groep wilt verwijderen, selecteert u de groep en selecteert u vervolgens **Verwijderen** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="679d2-170">To remove a vendor from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="item-rebate-groups"></a><span data-ttu-id="679d2-171">Artikelkortingsgroepen</span><span class="sxs-lookup"><span data-stu-id="679d2-171">Item rebate groups</span></span>

<span data-ttu-id="679d2-172">Door artikelen te groeperen, hebt u meer flexibiliteit bij het berekenen van kortingen en inhoudingen.</span><span class="sxs-lookup"><span data-stu-id="679d2-172">By grouping items, you have more flexibility when rebates and deductions are calculated.</span></span> <span data-ttu-id="679d2-173">Deze aanpak is vaak een efficiëntere manier om kortingen en inhoudingen in te stellen voor klanten en leveranciers.</span><span class="sxs-lookup"><span data-stu-id="679d2-173">This approach is often a more efficient way to set up rebates and deductions for customers and vendors.</span></span>

### <a name="set-up-item-groups"></a><span data-ttu-id="679d2-174">Artikelgroepen instellen</span><span class="sxs-lookup"><span data-stu-id="679d2-174">Set up item groups</span></span>

<span data-ttu-id="679d2-175">Als u wilt werken met artikelgroepen voor kortingsbeheer, gaat u naar **Kortingsbeheer \> Kortingsbeheergroepen instellen \> Artikelgroepen**.</span><span class="sxs-lookup"><span data-stu-id="679d2-175">To work with Rebate management item groups, go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span> <span data-ttu-id="679d2-176">U kunt de knoppen in het actiedeelvenster gebruiken om naar behoefte groepen toe te voegen en te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="679d2-176">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="679d2-177">Stel voor elke groep de volgende velden in:</span><span class="sxs-lookup"><span data-stu-id="679d2-177">For each group, set the following fields:</span></span>

- <span data-ttu-id="679d2-178">**Kortingsbeheergroep**: voer een unieke naam voor de groep in.</span><span class="sxs-lookup"><span data-stu-id="679d2-178">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="679d2-179">**Beschrijving**: voer een beschrijving van de groep in om meer informatie te geven over hoe deze moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="679d2-179">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-item-group-assignments"></a><span data-ttu-id="679d2-180">Toewijzingen van artikelgroepen beheren</span><span class="sxs-lookup"><span data-stu-id="679d2-180">Manage item group assignments</span></span>

<span data-ttu-id="679d2-181">Elk artikel kan tot een willekeurig aantal kortingsbeheergroepen behoren.</span><span class="sxs-lookup"><span data-stu-id="679d2-181">Each item can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="679d2-182">Als u groepsleden wilt weergeven en toewijzen, kunt u beginnen vanuit de groepslijst of de artikellijst.</span><span class="sxs-lookup"><span data-stu-id="679d2-182">To view and assign group members, you can start from either the group list or the item list.</span></span> <span data-ttu-id="679d2-183">U kunt ook artikelen toevoegen op basis van uw categoriehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="679d2-183">You can also add items based on your category hierarchy.</span></span>

<span data-ttu-id="679d2-184">Volg deze stappen om artikelen voor een geselecteerde groep weer te geven, toe te voegen of te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="679d2-184">To view, add, or remove items for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="679d2-185">Ga naar **Kortingsbeheer \> Kortingsbeheergroepen instellen \> Artikelgroepen**.</span><span class="sxs-lookup"><span data-stu-id="679d2-185">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="679d2-186">Selecteer de groep die u wilt beheren.</span><span class="sxs-lookup"><span data-stu-id="679d2-186">Select the group to manage.</span></span>
1. <span data-ttu-id="679d2-187">Selecteer **Artikelen** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="679d2-187">On the Action Pane, select **Items**.</span></span> <span data-ttu-id="679d2-188">De pagina **Kortingsbeheergroepen** wordt weergegeven en toont een lijst met artikelen die al lid zijn van de geselecteerde groep.</span><span class="sxs-lookup"><span data-stu-id="679d2-188">The **Rebate management groups** page appears and shows a list of items that are already members of the selected group.</span></span>
1. <span data-ttu-id="679d2-189">Als u een nieuw artikel wilt toevoegen aan de groep, selecteert u **Nieuw** in het actievenster om een rij toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="679d2-189">To add a new item to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="679d2-190">Stel daarna het volgende veld in voor de nieuwe rij:</span><span class="sxs-lookup"><span data-stu-id="679d2-190">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="679d2-191">**Artikelrekening**: selecteer de artikelrekening-id.</span><span class="sxs-lookup"><span data-stu-id="679d2-191">**Item account** – Select the item account ID.</span></span>

1. <span data-ttu-id="679d2-192">Als u een artikel uit de groep wilt verwijderen, selecteert u het artikel en selecteert u vervolgens **Verwijderen** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="679d2-192">To remove an item from the group, select the item, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="679d2-193">Volg deze stappen om groepstoewijzingen voor een geselecteerd artikel weer te geven, toe te voegen of te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="679d2-193">To view, add, or remove group assignments for a selected item, follow these steps.</span></span>

1. <span data-ttu-id="679d2-194">Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="679d2-194">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="679d2-195">Selecteer het artikel waarmee u wilt werken.</span><span class="sxs-lookup"><span data-stu-id="679d2-195">Select the item to work with.</span></span>
1. <span data-ttu-id="679d2-196">Selecteer vervolgens in het actievenster op het tabblad **Product** in de groep **Kortingsbeheer** de optie **Kortingsbeheergroepen**.</span><span class="sxs-lookup"><span data-stu-id="679d2-196">On the Action Pane, on the **Product** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="679d2-197">De pagina **Kortingsbeheergroepen** wordt weergegeven en toont een lijst met groepen waartoe het geselecteerde artikel al bestaat.</span><span class="sxs-lookup"><span data-stu-id="679d2-197">The **Rebate management groups** page appears and shows a list of groups that the selected item already belongs to.</span></span>
1. <span data-ttu-id="679d2-198">Als u het artikel wilt toevoegen aan een nieuwe groep, selecteert u **Nieuw** in het actievenster om een rij toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="679d2-198">To add the item to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="679d2-199">Stel daarna het volgende veld in voor de nieuwe rij:</span><span class="sxs-lookup"><span data-stu-id="679d2-199">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="679d2-200">**Kortingsbeheergroep**: selecteer de groep waaraan u het artikel wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="679d2-200">**Rebate management group** – Select the group to add the item to.</span></span>

1. <span data-ttu-id="679d2-201">Als u een artikel uit een groep wilt verwijderen, selecteert u de groep en selecteert u vervolgens **Verwijderen** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="679d2-201">To remove an item from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="679d2-202">Volg deze stappen om artikel toe te voegen aan een groep op basis van uw categoriehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="679d2-202">To add items to a group based on your category hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="679d2-203">Ga naar **Kortingsbeheer \> Kortingsbeheergroepen instellen \> Artikelgroepen**.</span><span class="sxs-lookup"><span data-stu-id="679d2-203">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="679d2-204">Selecteer de groep die u wilt beheren.</span><span class="sxs-lookup"><span data-stu-id="679d2-204">Select the group to manage.</span></span>
1. <span data-ttu-id="679d2-205">Selecteer **Artikelen toevoegen** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="679d2-205">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="679d2-206">Selecteer in het dialoogvenster **Artikelen toevoegen** in het veld **Categoriehiërarchie** een categorie op het hoogste niveau.</span><span class="sxs-lookup"><span data-stu-id="679d2-206">In the **Add items** dialog box, in the **Category hierarchy** field, select a top-level category.</span></span>
1. <span data-ttu-id="679d2-207">De artikelhiërarchie wordt geopend in het linkerdeelvenster.</span><span class="sxs-lookup"><span data-stu-id="679d2-207">The item hierarchy is opened in the left pane.</span></span> <span data-ttu-id="679d2-208">Selecteer het hiërarchieniveau dat u zoekt.</span><span class="sxs-lookup"><span data-stu-id="679d2-208">Select the hierarchy level that you're looking for.</span></span> 
1. <span data-ttu-id="679d2-209">Artikelen uit de geselecteerde hiërarchie en van het geselecteerde hiërarchieniveau worden nu in het rechterdeelvenster weergegeven.</span><span class="sxs-lookup"><span data-stu-id="679d2-209">Items from the selected hierarchy and hierarchy level are now listed in the right pane.</span></span> <span data-ttu-id="679d2-210">Volg deze stappen om met het deelvenster te werken:</span><span class="sxs-lookup"><span data-stu-id="679d2-210">Follow these steps to work with the pane:</span></span>

    - <span data-ttu-id="679d2-211">Schakel het selectievakje in voor elk artikel dat u wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="679d2-211">Select the check box for each item that you want to add.</span></span>
    - <span data-ttu-id="679d2-212">Schakel het selectievakje in de rasterkop in om alle artikelen te selecteren die worden vermeld.</span><span class="sxs-lookup"><span data-stu-id="679d2-212">Select the check box on the grid header to select all the items that are listed.</span></span>
    - <span data-ttu-id="679d2-213">Selecteer de knop **Selectie weergeven** om het raster te filteren, zodat alleen de artikelen worden weergegeven die u tot nu toe hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="679d2-213">Select the **Show selected** button to filter the grid so that it shows only the items that you've selected so far.</span></span> <span data-ttu-id="679d2-214">Selecteer de knop nogmaals om terug te keren naar de volledige lijst.</span><span class="sxs-lookup"><span data-stu-id="679d2-214">Select the button again to return to the full list.</span></span>

1. <span data-ttu-id="679d2-215">Selecteer **OK** om uw artikelselectie toe te passen op de geselecteerde groep.</span><span class="sxs-lookup"><span data-stu-id="679d2-215">Select **OK** to apply your item selection to the selected group.</span></span>
