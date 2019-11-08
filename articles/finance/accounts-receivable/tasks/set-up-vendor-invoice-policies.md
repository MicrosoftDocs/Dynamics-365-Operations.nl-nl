---
title: Leveranciersfactuurbeleid instellen
description: In dit onderwerp wordt uitgelegd u beleidsregels instelt voor leveranciersfacturen.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72f017294c976dcd1b7ddda01ac9e39252f036d6
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250274"
---
# <a name="set-up-vendor-invoice-policies"></a><span data-ttu-id="61f60-103">Leveranciersfactuurbeleid instellen</span><span class="sxs-lookup"><span data-stu-id="61f60-103">Set up vendor invoice policies</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="61f60-104">In dit onderwerp wordt uitgelegd u beleidsregels instelt voor leveranciersfacturen.</span><span class="sxs-lookup"><span data-stu-id="61f60-104">This topic explains how to set up vendor invoice policies.</span></span> <span data-ttu-id="61f60-105">Beleidsregels voor leveranciersfacturen worden uitgevoerd wanneer u een leveranciersfactuur boekt met behulp van de pagina Leveranciersfactuur en wanneer u de leveranciersfactuurpagina Beleidsovertredingen opent.</span><span class="sxs-lookup"><span data-stu-id="61f60-105">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="61f60-106">U kunt tevens de workflow van de leveranciersfactuur configureren, om iedere keer wanneer u een factuur naar de workflow verzendt, leveranciersfactuurbeleid uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="61f60-106">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

- <span data-ttu-id="61f60-107">Beleidsregels voor leveranciersfacturen gelden niet voor facturen die in het facturenregister of facturenjournaal gemaakt zijn.</span><span class="sxs-lookup"><span data-stu-id="61f60-107">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span>  
- <span data-ttu-id="61f60-108">Valideren van factuurvereffening maakt geen gebruik van beleidsregels voor leveranciersfacturen, maar is in plaats daarvan ingesteld in de pagina Parameters van module Leveranciers.</span><span class="sxs-lookup"><span data-stu-id="61f60-108">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>  
- <span data-ttu-id="61f60-109">Bij deze registratie wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="61f60-109">This recording uses the USMF demo company.</span></span> <span data-ttu-id="61f60-110">De leveranciersmanager of Accounting Manager-rol kan deze stappen uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="61f60-110">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="61f60-111">Controleer voordat u begint of de configuratiesleutel Factuurvereffening is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="61f60-111">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="61f60-112">Voorbereiden op het maken van leveranciersfactuurbeleid</span><span class="sxs-lookup"><span data-stu-id="61f60-112">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="61f60-113">Ga naar **Navigatievenster > Modules > Leveranciers > Instellen > Parameters voor Leveranciers**.</span><span class="sxs-lookup"><span data-stu-id="61f60-113">Go to **Navigation pane > Modules > Accounts payable > Setup > Accounts payable parameters**.</span></span>
2. <span data-ttu-id="61f60-114">Selecteer het tabblad **Factuurvalidatie**.</span><span class="sxs-lookup"><span data-stu-id="61f60-114">Select the **Invoice validation** tab.</span></span>
3. <span data-ttu-id="61f60-115">Schakel het selectievakje met de status **Factuurkoptekst automatisch bijwerken** in of uit.</span><span class="sxs-lookup"><span data-stu-id="61f60-115">Select or clear the **Automatically update invoice header** status check box.</span></span>
4. <span data-ttu-id="61f60-116">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="61f60-116">Select **OK**.</span></span>
5. <span data-ttu-id="61f60-117">Selecteer een optie in het veld **Factuur met verschillen boeken**.</span><span class="sxs-lookup"><span data-stu-id="61f60-117">In the **Post invoice with discrepancies** field, select an option.</span></span>
6. <span data-ttu-id="61f60-118">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="61f60-118">Close the page.</span></span>
7. <span data-ttu-id="61f60-119">Ga naar **Navigatievenster > Modules > Leveranciers > Beleidsinstelling > Leveranciersfactuurbeleid**.</span><span class="sxs-lookup"><span data-stu-id="61f60-119">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
8. <span data-ttu-id="61f60-120">Selecteer **Parameters**.</span><span class="sxs-lookup"><span data-stu-id="61f60-120">Select **Parameters**.</span></span>
9. <span data-ttu-id="61f60-121">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="61f60-121">Select **Add**.</span></span>
10. <span data-ttu-id="61f60-122">Sluit de pagina om terug te keren naar de startpagina.</span><span class="sxs-lookup"><span data-stu-id="61f60-122">Close the page to return to the home page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="61f60-123">Typen beleidsregels voor leveranciersfacturen maken</span><span class="sxs-lookup"><span data-stu-id="61f60-123">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="61f60-124">Ga naar **Navigatievenster > Modules > Leveranciers > Beleidsinstelling > Beleidsregeltypen voor leveranciersfactuur**.</span><span class="sxs-lookup"><span data-stu-id="61f60-124">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policy rule types**.</span></span>
2. <span data-ttu-id="61f60-125">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="61f60-125">Select **New**.</span></span>
3. <span data-ttu-id="61f60-126">Typ waarden in de velden **Regelnaam** en **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="61f60-126">In the **Rule name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="61f60-127">Selecteer in het veld **Querynaam** de vervolgkeuzeknop om de zoekopdracht te openen en selecteer de gewenste record.</span><span class="sxs-lookup"><span data-stu-id="61f60-127">In the **Query name** field, select the drop-down button to open the lookup, then selec the desired record.</span></span>
5. <span data-ttu-id="61f60-128">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="61f60-128">Select **Save**.</span></span>
6. <span data-ttu-id="61f60-129">Sluit de pagina om terug te keren naar de startpagina.</span><span class="sxs-lookup"><span data-stu-id="61f60-129">Close the page to return to the home page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="61f60-130">Een leveranciersfactuurbeleid definiëren</span><span class="sxs-lookup"><span data-stu-id="61f60-130">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="61f60-131">Ga naar **Navigatievenster > Modules > Leveranciers > Beleidsinstelling > Leveranciersfactuurbeleid**.</span><span class="sxs-lookup"><span data-stu-id="61f60-131">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
2. <span data-ttu-id="61f60-132">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="61f60-132">Select **New**.</span></span>
3. <span data-ttu-id="61f60-133">Typ waarden in de velden **Naam** en **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="61f60-133">In the **Name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="61f60-134">Vouw de sectie **Beleidorganisaties** uit of samen.</span><span class="sxs-lookup"><span data-stu-id="61f60-134">Expand or collapse the **Policy organizations** section.</span></span>
5. <span data-ttu-id="61f60-135">In de structuur selecteert u **Contoso Entertainment System USA**.</span><span class="sxs-lookup"><span data-stu-id="61f60-135">In the tree, select **Contoso Entertainment System USA**.</span></span>
6. <span data-ttu-id="61f60-136">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="61f60-136">Select **Add**.</span></span>
7. <span data-ttu-id="61f60-137">Vouw de sectie **Beleidsregels** uit of samen.</span><span class="sxs-lookup"><span data-stu-id="61f60-137">Expand or collapse the **Policy rules** section.</span></span>
8. <span data-ttu-id="61f60-138">Selecteer **Beleidsregel maken**.</span><span class="sxs-lookup"><span data-stu-id="61f60-138">Select **Create policy rule**.</span></span>
9. <span data-ttu-id="61f60-139">Typ een waarde in het veld **Beschrijving beleidsregel**.</span><span class="sxs-lookup"><span data-stu-id="61f60-139">In the **Policy rule description** field, type a value.</span></span>
10. <span data-ttu-id="61f60-140">Selecteer **Filter**.</span><span class="sxs-lookup"><span data-stu-id="61f60-140">Select **Filter**.</span></span>
11. <span data-ttu-id="61f60-141">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="61f60-141">Select **Add**.</span></span> <span data-ttu-id="61f60-142">Selecteer de gewenste record.</span><span class="sxs-lookup"><span data-stu-id="61f60-142">Select the desired record.</span></span>
12. <span data-ttu-id="61f60-143">Typ of selecteer in de vervolgkeuzemenu's opties voor de velden **Tabel**, **Afgeleide tabel** en **Veld**.</span><span class="sxs-lookup"><span data-stu-id="61f60-143">In the **Table**, **Derived table**, and **Field** fields, select or enter options from the drop-down menus.</span></span>
13. <span data-ttu-id="61f60-144">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="61f60-144">Close the page.</span></span>
14. <span data-ttu-id="61f60-145">Typ een waarde in het veld **Criteria**.</span><span class="sxs-lookup"><span data-stu-id="61f60-145">In the **Criteria** field, type a value.</span></span>
15. <span data-ttu-id="61f60-146">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="61f60-146">Select **OK**.</span></span>
16. <span data-ttu-id="61f60-147">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="61f60-147">Select **OK**.</span></span>
17. <span data-ttu-id="61f60-148">Sluit de pagina's om terug te keren naar de startpagina.</span><span class="sxs-lookup"><span data-stu-id="61f60-148">Close the pages to return to the home page.</span></span>
