---
title: Geavanceerde contracten maken voor facturering op basis van voortgang
description: In dit onderwerp wordt uitgelegd hoe u projectcontracten maakt, zodat u facturen voor klanten kunt genereren op basis van een percentage voltooid werk.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 90cae104d0abad909606ef6a0e0c45ed95e74de2
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282819"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="587f9-103">Geavanceerde contracten maken voor facturering op basis van voortgang</span><span class="sxs-lookup"><span data-stu-id="587f9-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="587f9-104">In dit onderwerp wordt uitgelegd hoe u projectcontracten maakt, zodat u facturen voor klanten kunt maken op basis van een percentage voltooid werk.</span><span class="sxs-lookup"><span data-stu-id="587f9-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="587f9-105">Factuurbedragen voor de budgetcategorieën van werkzaamheden die u voor een project instelt, worden automatisch berekend.</span><span class="sxs-lookup"><span data-stu-id="587f9-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="587f9-106">Wanneer u factureert, wordt ingesteld bij de contractonderhandeling van het project met de klant.</span><span class="sxs-lookup"><span data-stu-id="587f9-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="587f9-107">Gebruik de procedures in dit onderwerp voor het instellen van een contract, een gekoppeld project en de factureringsregels voor het berekenen van de factuurbedragen voor de budgetcategorieën van werkzaamheden die u voor het project hebt ingesteld.</span><span class="sxs-lookup"><span data-stu-id="587f9-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="587f9-108">Nadat u het contract en het project hebt gemaakt, kunt u de details van het project instellen.</span><span class="sxs-lookup"><span data-stu-id="587f9-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="587f9-109">U kunt bijvoorbeeld de activiteiten definiëren en werknemers toewijzen aan het project.</span><span class="sxs-lookup"><span data-stu-id="587f9-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="587f9-110">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="587f9-110">Example</span></span>

<span data-ttu-id="587f9-111">Uw organisatie is een bedrijf dat zich bezig houdt met het ontwikkelen van software.</span><span class="sxs-lookup"><span data-stu-id="587f9-111">Your organization is a software development firm.</span></span> <span data-ttu-id="587f9-112">U komt met een klant overeen dat u een salarisadministratiepakket zult ontwikkelen voor een totaal tarief van 20.000 Amerikaanse dollar (USD).</span><span class="sxs-lookup"><span data-stu-id="587f9-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="587f9-113">Uw organisatie stemt in met het factureren van de klant als u de specifieke percentages van de projectwerkzaamheden voltooit.</span><span class="sxs-lookup"><span data-stu-id="587f9-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="587f9-114">U stelt de volgende projectcategorieën voor het werk in, zodat u ze in het factureringsproces kunt gebruiken:</span><span class="sxs-lookup"><span data-stu-id="587f9-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="587f9-115">Advisering</span><span class="sxs-lookup"><span data-stu-id="587f9-115">Consulting</span></span>
- <span data-ttu-id="587f9-116">Ontwerpen</span><span class="sxs-lookup"><span data-stu-id="587f9-116">Design</span></span>
- <span data-ttu-id="587f9-117">Installatie</span><span class="sxs-lookup"><span data-stu-id="587f9-117">Installation</span></span>

<span data-ttu-id="587f9-118">U stelt ook factureringsregels in die automatisch de factuurbedragen berekenen voor het percentage voltooide projectwerkzaamheden in elke categorie.</span><span class="sxs-lookup"><span data-stu-id="587f9-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="587f9-119">De budgetmanager maakt een budget voor de projectcategorieën.</span><span class="sxs-lookup"><span data-stu-id="587f9-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="587f9-120">De hoeveelheid voltooid werk wordt automatisch berekend als een percentage van de werkelijke hoeveelheid werk vergeleken met de gebudgetteerde bedragen.</span><span class="sxs-lookup"><span data-stu-id="587f9-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="587f9-121">Vereisten</span><span class="sxs-lookup"><span data-stu-id="587f9-121">Prerequisites</span></span>

<span data-ttu-id="587f9-122">Voordat u een project maakt waarin factureringsregels worden gebruikt, moet u de nummerreeksen instellen voor factureringsregels en een bijzondere-kostenjournaal dat wordt gebruikt om facturering naar rato van voortgang te boeken.</span><span class="sxs-lookup"><span data-stu-id="587f9-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="587f9-123">Ga naar **Projectbeheer en boekhouding** \> **Instellingen** \> **Projectbeheer- en boekhoudingsparameters**.</span><span class="sxs-lookup"><span data-stu-id="587f9-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="587f9-124">Stel op de pagina **Projectbeheer- en boekhoudingsparameters** in het tabblad **Nummerreeksen** de nummerreeks in die u wilt gebruiken wanneer factureringsregels worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="587f9-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="587f9-125">Ga naar **Projectbeheer en boekhouding** \> **Journalen** \> **Bijzondere kosten**.</span><span class="sxs-lookup"><span data-stu-id="587f9-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="587f9-126">Selecteer **Nieuw** op de pagina **Bijzondere-kostenjournaal** en voer de journaalnaam in.</span><span class="sxs-lookup"><span data-stu-id="587f9-126">On the **Fee journal** page, select **New**, and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="587f9-127">Een contract maken voor facturering naar rato van voortgang</span><span class="sxs-lookup"><span data-stu-id="587f9-127">Create a contract for progress billings</span></span>

<span data-ttu-id="587f9-128">Gebruik deze procedure om een projectcontract voor een project met een vaste prijs te maken.</span><span class="sxs-lookup"><span data-stu-id="587f9-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="587f9-129">U maakt een projectfactuur wanneer de voltooiing van het project een opgegeven percentage bereikt.</span><span class="sxs-lookup"><span data-stu-id="587f9-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="587f9-130">Ga naar **Projectbeheer en boekhouding** \> **Projecten** \> **Projectcontracten**.</span><span class="sxs-lookup"><span data-stu-id="587f9-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="587f9-131">Selecteer **Nieuw** op de pagina **Projectcontracten**.</span><span class="sxs-lookup"><span data-stu-id="587f9-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="587f9-132">Stel in het dialoogvenster **Nieuw projectcontract** de volgende velden in:</span><span class="sxs-lookup"><span data-stu-id="587f9-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="587f9-133">**Naam**</span><span class="sxs-lookup"><span data-stu-id="587f9-133">**Name**</span></span>
    - <span data-ttu-id="587f9-134">**Type financiering**</span><span class="sxs-lookup"><span data-stu-id="587f9-134">**Funding type**</span></span>
    - <span data-ttu-id="587f9-135">**Financieringsbron**</span><span class="sxs-lookup"><span data-stu-id="587f9-135">**Funding source**</span></span>
    - <span data-ttu-id="587f9-136">**Verkoopvaluta**: deze valuta wordt standaard gebruikt voor klantfacturen die gekoppeld zijn aan het projectcontract.</span><span class="sxs-lookup"><span data-stu-id="587f9-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="587f9-137">U kunt echter de verkoopvaluta voor een bepaalde klantfactuur wijzigen.</span><span class="sxs-lookup"><span data-stu-id="587f9-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="587f9-138">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="587f9-138">Select **OK**.</span></span> <span data-ttu-id="587f9-139">De informatie wordt gekopieerd naar de koptekst van de pagina **Projectcontracten**.</span><span class="sxs-lookup"><span data-stu-id="587f9-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="587f9-140">Vul op de pagina **Projectcontracten** de rest van de vereiste informatie voor het project in.</span><span class="sxs-lookup"><span data-stu-id="587f9-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="587f9-141">Een project maken voor facturering naar rato van voortgang</span><span class="sxs-lookup"><span data-stu-id="587f9-141">Create a project for progress billings</span></span>

<span data-ttu-id="587f9-142">Volg deze stappen als u een project en eventuele subprojecten wilt maken die aan een projectcontract zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="587f9-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="587f9-143">Ga naar **Projectbeheer en boekhouding** \> **Projecten** \> **Alle projecten**.</span><span class="sxs-lookup"><span data-stu-id="587f9-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="587f9-144">Selecteer **Nieuw** op de pagina **Alle projecten**.</span><span class="sxs-lookup"><span data-stu-id="587f9-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="587f9-145">Selecteer in het dialoogvenster **Nieuw project** in het veld **Projecttype** de optie **Tijd en materiaal**.</span><span class="sxs-lookup"><span data-stu-id="587f9-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="587f9-146">Selecteer een projectgroep.</span><span class="sxs-lookup"><span data-stu-id="587f9-146">Select a project group.</span></span> <span data-ttu-id="587f9-147">Een projectgroep definieert de boekingsgegevens voor de projecten die zijn toegewezen aan de groep.</span><span class="sxs-lookup"><span data-stu-id="587f9-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="587f9-148">Selecteer **Project maken**.</span><span class="sxs-lookup"><span data-stu-id="587f9-148">Select **Create project**.</span></span>
6. <span data-ttu-id="587f9-149">Stel nadat het project is gemaakt, de projectfase in op **Onderhanden**.</span><span class="sxs-lookup"><span data-stu-id="587f9-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="587f9-150">Maak een budget voor een project.</span><span class="sxs-lookup"><span data-stu-id="587f9-150">Create a budget for a project</span></span>

<span data-ttu-id="587f9-151">Budgetcategorieën worden gebruikt voor het automatisch berekenen van de factuurbedragen voor het percentage voltooide werkzaamheden voor de afzonderlijke categorieën.</span><span class="sxs-lookup"><span data-stu-id="587f9-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="587f9-152">Volg deze stappen om budgetcategorieën te maken voor de geraamde kosten.</span><span class="sxs-lookup"><span data-stu-id="587f9-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="587f9-153">Ga naar **Projectbeheer en boekhouding** \> **Projecten** \> **Alle projecten**.</span><span class="sxs-lookup"><span data-stu-id="587f9-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="587f9-154">Selecteer op de pagina **Alle projecten** het gewenste project en open het.</span><span class="sxs-lookup"><span data-stu-id="587f9-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="587f9-155">Selecteer op de pagina **Projecten** in het actievenster op het tabblad **Plan** in de groep **Budget** de optie **Projectbudget**.</span><span class="sxs-lookup"><span data-stu-id="587f9-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="587f9-156">Voer op de pagina **Projectbudget** de geschatte kosten in voor de afzonderlijke categorieën in het project.</span><span class="sxs-lookup"><span data-stu-id="587f9-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="587f9-157">Factureringsregels maken voor facturering naar rato van voortgang</span><span class="sxs-lookup"><span data-stu-id="587f9-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="587f9-158">Ga naar **Projectbeheer en boekhouding** \> **Projecten** \> **Projectcontracten**.</span><span class="sxs-lookup"><span data-stu-id="587f9-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="587f9-159">Selecteer op de pagina **Projectcontracten** een projectcontract en open het.</span><span class="sxs-lookup"><span data-stu-id="587f9-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="587f9-160">Selecteer **Toevoegen** op de pagina Projectcontract in het sneltabblad **Factureringsregels**.</span><span class="sxs-lookup"><span data-stu-id="587f9-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="587f9-161">Selecteer op de pagina **Factureringsregel** in het veld **Regeltype** de optie **Voortgang**.</span><span class="sxs-lookup"><span data-stu-id="587f9-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="587f9-162">Voer in het sneltabblad **Regeldetails factureringsregel** in het veld **Contractwaarde** de totale waarde van het contract in.</span><span class="sxs-lookup"><span data-stu-id="587f9-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="587f9-163">Selecteer in het veld **Categorie** de categorie waarnaar de transactie moet worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="587f9-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="587f9-164">Selecteer in het veld **Project** het project waarvoor deze factureringsregel wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="587f9-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="587f9-165">Optioneel: u kunt de factureringsregel aan extra projecten toewijzen.</span><span class="sxs-lookup"><span data-stu-id="587f9-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="587f9-166">Selecteer op het sneltabblad **Project** in de sectie **Beschikbare projecten** een project en selecteer vervolgens de pijl naar rechts om het project toe te voegen aan de sectie **Geselecteerde projecten**.</span><span class="sxs-lookup"><span data-stu-id="587f9-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="587f9-167">Optioneel: bereken een percentagebedrag dat de klant inhoudt van betalingen op een factuur.</span><span class="sxs-lookup"><span data-stu-id="587f9-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="587f9-168">Selecteer op het sneltabblad **Inhoudingsvoorwaarden betalingen** de financieringsbron en vul vervolgens het veld **Inhoudingspercentage** in.</span><span class="sxs-lookup"><span data-stu-id="587f9-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="587f9-169">Herhaal deze stappen voor het maken van aanvullende factureringsregels voor het contract.</span><span class="sxs-lookup"><span data-stu-id="587f9-169">Repeat these steps to create additional billing rules for the project contract.</span></span>
