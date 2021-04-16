---
title: Uitzonderingen onderzoeken of oplossen
description: Beleidsregels voor leveranciersfacturen worden uitgevoerd wanneer u een leveranciersfactuur boekt met behulp van de pagina Leveranciersfactuur en wanneer u de leveranciersfactuurpagina Beleidsovertredingen opent.
author: abruer
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: abc8dc112ab577ddcbd208f898a8d4e487bc2998
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827765"
---
# <a name="research-or-resolve-exceptions"></a><span data-ttu-id="caae8-103">Uitzonderingen onderzoeken of oplossen</span><span class="sxs-lookup"><span data-stu-id="caae8-103">Research or resolve exceptions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="caae8-104">Beleidsregels voor leveranciersfacturen worden uitgevoerd wanneer u een leveranciersfactuur boekt met behulp van de pagina Leveranciersfactuur en wanneer u de leveranciersfactuurpagina Beleidsovertredingen opent.</span><span class="sxs-lookup"><span data-stu-id="caae8-104">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="caae8-105">U kunt tevens de workflow van de leveranciersfactuur configureren, om iedere keer wanneer u een factuur naar de workflow verzendt, leveranciersfactuurbeleid uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="caae8-105">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

<span data-ttu-id="caae8-106">Beleidsregels voor leveranciersfacturen gelden niet voor facturen die in het facturenregister of facturenjournaal gemaakt zijn.</span><span class="sxs-lookup"><span data-stu-id="caae8-106">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span> 

<span data-ttu-id="caae8-107">Valideren van factuurvereffening maakt geen gebruik van beleidsregels voor leveranciersfacturen, maar is in plaats daarvan ingesteld in de pagina Parameters van module Leveranciers.</span><span class="sxs-lookup"><span data-stu-id="caae8-107">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>

<span data-ttu-id="caae8-108">Bij deze registratie wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="caae8-108">This recording uses the USMF demo company.</span></span> <span data-ttu-id="caae8-109">De leveranciersmanager of Accounting Manager-rol kan deze stappen uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="caae8-109">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="caae8-110">Controleer voordat u begint of de configuratiesleutel Factuurvereffening is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="caae8-110">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="caae8-111">Voorbereiden op het maken van leveranciersfactuurbeleid</span><span class="sxs-lookup"><span data-stu-id="caae8-111">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="caae8-112">Ga naar Leveranciers > Instellingen > Parameters van module Leveranciers.</span><span class="sxs-lookup"><span data-stu-id="caae8-112">Go to Accounts payable > Setup > Accounts payable parameters.</span></span>
2. <span data-ttu-id="caae8-113">Klik op het tabblad Factuurvalidatie.</span><span class="sxs-lookup"><span data-stu-id="caae8-113">Click the Invoice validation tab.</span></span>
3. <span data-ttu-id="caae8-114">Selecteer het selectievakje Status factuurkoptekst automatisch bijwerken in of uit.</span><span class="sxs-lookup"><span data-stu-id="caae8-114">Select or clear the Automatically update invoice header status check box.</span></span>
4. <span data-ttu-id="caae8-115">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="caae8-115">Click OK.</span></span>
5. <span data-ttu-id="caae8-116">Selecteer een optie in het veld Factuur met verschillen boeken.</span><span class="sxs-lookup"><span data-stu-id="caae8-116">In the Post invoice with discrepancies field, select an option.</span></span>
6. <span data-ttu-id="caae8-117">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="caae8-117">Close the page.</span></span>
7. <span data-ttu-id="caae8-118">Ga naar Leveranciers > Beleidsinstelling > Leveranciersfactuurbeleid.</span><span class="sxs-lookup"><span data-stu-id="caae8-118">Go to Accounts payable > Policy setup > Vendor invoice policies.</span></span>
8. <span data-ttu-id="caae8-119">Klik op Parameters.</span><span class="sxs-lookup"><span data-stu-id="caae8-119">Click Parameters.</span></span>
9. <span data-ttu-id="caae8-120">Klik op btnAdd.</span><span class="sxs-lookup"><span data-stu-id="caae8-120">Click btnAdd.</span></span>
10. <span data-ttu-id="caae8-121">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="caae8-121">Close the page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="caae8-122">Typen beleidsregels voor leveranciersfacturen maken</span><span class="sxs-lookup"><span data-stu-id="caae8-122">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="caae8-123">Ga naar Leveranciers > Beleidsinstelling > Beleidsregeltypen voor leveranciersfactuur.</span><span class="sxs-lookup"><span data-stu-id="caae8-123">Go to Accounts payable > Policy setup > Vendor invoice policy rule types.</span></span>
2. <span data-ttu-id="caae8-124">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="caae8-124">Click New.</span></span>
3. <span data-ttu-id="caae8-125">Typ een waarde in het veld Regelnaam.</span><span class="sxs-lookup"><span data-stu-id="caae8-125">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="caae8-126">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="caae8-126">In the Description field, type a value.</span></span>
5. <span data-ttu-id="caae8-127">Klik in het veld Querynaam op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="caae8-127">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="caae8-128">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="caae8-128">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="caae8-129">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="caae8-129">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="caae8-130">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="caae8-130">Click Save.</span></span>
9. <span data-ttu-id="caae8-131">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="caae8-131">Close the page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="caae8-132">Een leveranciersfactuurbeleid definiëren</span><span class="sxs-lookup"><span data-stu-id="caae8-132">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="caae8-133">Ga naar Leveranciers > Beleidsinstelling > Leveranciersfactuurbeleid.</span><span class="sxs-lookup"><span data-stu-id="caae8-133">Go to Accounts payable > Policy setup > Vendor invoice policies.</span></span>
2. <span data-ttu-id="caae8-134">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="caae8-134">Click New.</span></span>
3. <span data-ttu-id="caae8-135">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="caae8-135">In the Name field, type a value.</span></span>
4. <span data-ttu-id="caae8-136">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="caae8-136">In the Description field, type a value.</span></span>
5. <span data-ttu-id="caae8-137">Vouw de sectie Beleidorganisaties uit of samen.</span><span class="sxs-lookup"><span data-stu-id="caae8-137">Expand or collapse the Policy organizations section.</span></span>
6. <span data-ttu-id="caae8-138">In de structuur selecteert u "Contoso-entertainmentsysteem USA".</span><span class="sxs-lookup"><span data-stu-id="caae8-138">In the tree, select 'Contoso Entertainment System USA'.</span></span>
7. <span data-ttu-id="caae8-139">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="caae8-139">Click Add.</span></span>
8. <span data-ttu-id="caae8-140">Vouw de sectie Beleidsregels uit of samen.</span><span class="sxs-lookup"><span data-stu-id="caae8-140">Expand or collapse the Policy rules section.</span></span>
9. <span data-ttu-id="caae8-141">Klik op Beleidsregel maken.</span><span class="sxs-lookup"><span data-stu-id="caae8-141">Click Create policy rule.</span></span>
10. <span data-ttu-id="caae8-142">Typ een waarde in het veld Beschrijving beleidsregel.</span><span class="sxs-lookup"><span data-stu-id="caae8-142">In the Policy rule description field, type a value.</span></span>
11. <span data-ttu-id="caae8-143">Klik op Filter.</span><span class="sxs-lookup"><span data-stu-id="caae8-143">Click Filter.</span></span>
12. <span data-ttu-id="caae8-144">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="caae8-144">Click Add.</span></span>
13. <span data-ttu-id="caae8-145">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="caae8-145">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="caae8-146">Klik in het veld Tabel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="caae8-146">In the Table field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="caae8-147">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="caae8-147">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="caae8-148">Klik in het veld Afgeleide tabel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="caae8-148">In the Derived table field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="caae8-149">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="caae8-149">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="caae8-150">Klik in het veld Veld op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="caae8-150">In the Field field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="caae8-151">Typ een waarde in het veld Veld.</span><span class="sxs-lookup"><span data-stu-id="caae8-151">In the Field field, type a value.</span></span>
20. <span data-ttu-id="caae8-152">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="caae8-152">Close the page.</span></span>
21. <span data-ttu-id="caae8-153">Typ een waarde in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="caae8-153">In the Criteria field, type a value.</span></span>
22. <span data-ttu-id="caae8-154">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="caae8-154">Click OK.</span></span>
23. <span data-ttu-id="caae8-155">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="caae8-155">Click OK.</span></span>
24. <span data-ttu-id="caae8-156">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="caae8-156">Close the page.</span></span>
25. <span data-ttu-id="caae8-157">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="caae8-157">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]