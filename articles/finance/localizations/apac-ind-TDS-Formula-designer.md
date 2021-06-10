---
title: Formuleontwerper voor TDS-berekeningen
description: In dit onderwerp wordt een voorbeeld beschreven van hoe TDS (Tax Ducted at Source, belasting ingehouden op bron) wordt berekend op basis van de formule die is gedefinieerd voor elke TDS-belastingcode in de TDS-groep die aan de transactie is gekoppeld.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: d0f644da640b56761a52baec9ff01c898e895d19
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023139"
---
# <a name="formula-designer-for-tds-calculations"></a><span data-ttu-id="42651-103">Formuleontwerper voor TDS-berekeningen</span><span class="sxs-lookup"><span data-stu-id="42651-103">Formula designer for TDS calculations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="42651-104">In dit onderwerp wordt een voorbeeld gegeven van hoe TDS (Tax Ducted at Source, belasting ingehouden op bron) wordt berekend op basis van de formule die voor elke TDS-belastingcode is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="42651-104">This topic provides an example of how Tax Deducted at Source (TDS) is calculated based on the formula defined for each TDS tax code.</span></span> <span data-ttu-id="42651-105">TDS-belastingcodes worden gedefinieerd in de TDS-groep die aan de transactie is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="42651-105">TDS tax codes are defined in the TDS group that's attached to the transaction.</span></span> <span data-ttu-id="42651-106">Voordat u TDS-formules ontwerpt, moet u de basisinstellingen voor TDS voltooien, zoals wordt vermeld in de volgende stappen.</span><span class="sxs-lookup"><span data-stu-id="42651-106">Before designing TDS formulas, complete the basic setup required for TDS as listed in the following steps.</span></span> 

- <span data-ttu-id="42651-107">Stel TDS-componentgroepen in met de pagina **Componentgroepen voor bronbelasting**.</span><span class="sxs-lookup"><span data-stu-id="42651-107">Set up TDS component groups using the **Withholding tax component groups** page.</span></span> 
- <span data-ttu-id="42651-108">Stel TDS-componenten in en koppel de TDS-componentgroep aan de TDS-componenten met de pagina **Bronbelastingcomponenten**.</span><span class="sxs-lookup"><span data-stu-id="42651-108">Set up TDS components and attach TDS component group to the TDS components using the **Withholding tax components** page.</span></span> 
- <span data-ttu-id="42651-109">Stel TDS-belastingcodes in en koppel de TDS-componenten aan de belastingcodes met de pagina **Bronbelastingcodes**.</span><span class="sxs-lookup"><span data-stu-id="42651-109">Set up TDS tax codes and attach TDS components to the tax codes using the **Withholding tax codes** page.</span></span> 
- <span data-ttu-id="42651-110">Stel TDS-belastinggroepen in met de pagina **Bronbelastinggroepen**.</span><span class="sxs-lookup"><span data-stu-id="42651-110">Set up TDS tax groups using the **Withholding tax groups** page.</span></span> <span data-ttu-id="42651-111">Koppel vervolgens de TDS-belastingcodes aan de belastinggroep en definieer de formule met de pagina **Formuleontwerper**.</span><span class="sxs-lookup"><span data-stu-id="42651-111">Then attach the TDS tax codes to the tax group, and define the formula, using the **Formula designer** page.</span></span> 

<span data-ttu-id="42651-112">**Voorbeeld van formule**</span><span class="sxs-lookup"><span data-stu-id="42651-112">**Example formula**</span></span>

<span data-ttu-id="42651-113">In dit voorbeeld is de TDS-groep Huur gekoppeld aan een inkoopfactuur die voor leverancier A is gemaakt. Het factuurbedrag is $ 100.000.</span><span class="sxs-lookup"><span data-stu-id="42651-113">In this example, the TDS group, Rent, is attached to a purchase invoice that's created for vendor A. The invoice amount is $100,000.</span></span> <span data-ttu-id="42651-114">Zie de volgende tabel voor de TDS-berekening voor de factuur.</span><span class="sxs-lookup"><span data-stu-id="42651-114">Refer to the following table to view the TDS calculation for the invoice.</span></span>

| <span data-ttu-id="42651-115">TDS-groep</span><span class="sxs-lookup"><span data-stu-id="42651-115">TDS  group</span></span>                                                   | <span data-ttu-id="42651-116">TDS-belastingcodes die aan de TDS-groep zijn gekoppeld</span><span class="sxs-lookup"><span data-stu-id="42651-116">TDS tax codes attached to the TDS group</span></span> | <span data-ttu-id="42651-117">Waarde</span><span class="sxs-lookup"><span data-stu-id="42651-117">Value</span></span>              | <span data-ttu-id="42651-118">Belastbare basis (Formuleontwerper)</span><span class="sxs-lookup"><span data-stu-id="42651-118">Taxable basis  (Formula designer)</span></span> | <span data-ttu-id="42651-119">Berekeningsexpressie (Formuleontwerper)</span><span class="sxs-lookup"><span data-stu-id="42651-119">Calculation expression  (Formula designer)</span></span> | <span data-ttu-id="42651-120">Basisbedrag</span><span class="sxs-lookup"><span data-stu-id="42651-120">Base amount</span></span> | <span data-ttu-id="42651-121">Berekend TDS-bedrag</span><span class="sxs-lookup"><span data-stu-id="42651-121">Calculated TDS amount</span></span> |
| ------------------------------------------------------------ | --------------------------------------- | ------------------ | --------------------------------- | :----------------------------------------: | ----------- | --------------------- |
| <span data-ttu-id="42651-122">Huur</span><span class="sxs-lookup"><span data-stu-id="42651-122">Rent</span></span>                                                         | <span data-ttu-id="42651-123">TDS (TDS-component - TDS)</span><span class="sxs-lookup"><span data-stu-id="42651-123">TDS  (TDS component-TDS)</span></span>                | <span data-ttu-id="42651-124">10%</span><span class="sxs-lookup"><span data-stu-id="42651-124">10%</span></span>                | <span data-ttu-id="42651-125">Brutobedrag</span><span class="sxs-lookup"><span data-stu-id="42651-125">Gross amount</span></span>                      |                                            | <span data-ttu-id="42651-126">100,000</span><span class="sxs-lookup"><span data-stu-id="42651-126">100,000</span></span>      | <span data-ttu-id="42651-127">10,000</span><span class="sxs-lookup"><span data-stu-id="42651-127">10,000</span></span>                 |
| <span data-ttu-id="42651-128">Toeslag (TDS-component - Toeslag)</span><span class="sxs-lookup"><span data-stu-id="42651-128">Surcharge  (TDS component-Surcharge)</span></span>                         | <span data-ttu-id="42651-129">10%</span><span class="sxs-lookup"><span data-stu-id="42651-129">10%</span></span>                                     | <span data-ttu-id="42651-130">Excl. brutobedrag</span><span class="sxs-lookup"><span data-stu-id="42651-130">Excl. gross amount</span></span> | <span data-ttu-id="42651-131">+TDS</span><span class="sxs-lookup"><span data-stu-id="42651-131">+TDS</span></span>                              |                   <span data-ttu-id="42651-132">10000</span><span class="sxs-lookup"><span data-stu-id="42651-132">10000</span></span>                    | <span data-ttu-id="42651-133">1.000</span><span class="sxs-lookup"><span data-stu-id="42651-133">1,000</span></span>        |                       |
| <span data-ttu-id="42651-134">PE-Cess (TDS-component - PE-Cess)</span><span class="sxs-lookup"><span data-stu-id="42651-134">PE-Cess  (TDS component- PE-Cess)</span></span>                            | <span data-ttu-id="42651-135">2%</span><span class="sxs-lookup"><span data-stu-id="42651-135">2%</span></span>                                      | <span data-ttu-id="42651-136">Excl. brutobedrag</span><span class="sxs-lookup"><span data-stu-id="42651-136">Excl. gross amount</span></span> | <span data-ttu-id="42651-137">+TDS+Toeslag</span><span class="sxs-lookup"><span data-stu-id="42651-137">+TDS+Surcharge</span></span>                    |                   <span data-ttu-id="42651-138">11000</span><span class="sxs-lookup"><span data-stu-id="42651-138">11000</span></span>                    | <span data-ttu-id="42651-139">220</span><span class="sxs-lookup"><span data-stu-id="42651-139">220</span></span>         |                       |
| <span data-ttu-id="42651-140">SHE Cess (TDS-component - SHE Cess)</span><span class="sxs-lookup"><span data-stu-id="42651-140">SHE Cess  (TDS component- SHE Cess)</span></span>                          | <span data-ttu-id="42651-141">1%</span><span class="sxs-lookup"><span data-stu-id="42651-141">1%</span></span>                                      | <span data-ttu-id="42651-142">Excl. brutobedrag</span><span class="sxs-lookup"><span data-stu-id="42651-142">Excl. gross amount</span></span> | <span data-ttu-id="42651-143">+TDS+Toeslag</span><span class="sxs-lookup"><span data-stu-id="42651-143">+TDS+Surcharge</span></span>                    |                   <span data-ttu-id="42651-144">11000</span><span class="sxs-lookup"><span data-stu-id="42651-144">11000</span></span>                    | <span data-ttu-id="42651-145">110</span><span class="sxs-lookup"><span data-stu-id="42651-145">110</span></span>         |                       |
| <span data-ttu-id="42651-146">**Totale** **TDS**  **die** **voor** **de** **factuur is berekend**</span><span class="sxs-lookup"><span data-stu-id="42651-146">**Total** **TDS**  **calculated** **for** **the** **invoice**</span></span> | <span data-ttu-id="42651-147">**11,330**</span><span class="sxs-lookup"><span data-stu-id="42651-147">**11,330**</span></span>                               |                    |                                   |                                            |             |                       |

<span data-ttu-id="42651-148">De boekstukposten worden als volgt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="42651-148">The voucher entries are created as follows.</span></span>

| <span data-ttu-id="42651-149">Rekening</span><span class="sxs-lookup"><span data-stu-id="42651-149">Account</span></span>           | <span data-ttu-id="42651-150">Debet</span><span class="sxs-lookup"><span data-stu-id="42651-150">Debit</span></span>  | <span data-ttu-id="42651-151">Krediet</span><span class="sxs-lookup"><span data-stu-id="42651-151">Credit</span></span> |
| ----------------- | ------ | ------ |
| <span data-ttu-id="42651-152">Huur</span><span class="sxs-lookup"><span data-stu-id="42651-152">Rent</span></span>              | <span data-ttu-id="42651-153">100,000</span><span class="sxs-lookup"><span data-stu-id="42651-153">100,000</span></span> |        |
| <span data-ttu-id="42651-154">Leverancier A</span><span class="sxs-lookup"><span data-stu-id="42651-154">Vendor A</span></span>          |        | <span data-ttu-id="42651-155">100,000</span><span class="sxs-lookup"><span data-stu-id="42651-155">100,000</span></span> |
| <span data-ttu-id="42651-156">Leverancier A</span><span class="sxs-lookup"><span data-stu-id="42651-156">Vendor A</span></span>          | <span data-ttu-id="42651-157">11,330</span><span class="sxs-lookup"><span data-stu-id="42651-157">11,330</span></span>  |        |
| <span data-ttu-id="42651-158">TDS te betalen</span><span class="sxs-lookup"><span data-stu-id="42651-158">TDS payable</span></span>       |        | <span data-ttu-id="42651-159">10,000</span><span class="sxs-lookup"><span data-stu-id="42651-159">10,000</span></span>  |
| <span data-ttu-id="42651-160">Toeslag te betalen</span><span class="sxs-lookup"><span data-stu-id="42651-160">Surcharge payable</span></span> |        | <span data-ttu-id="42651-161">1.000</span><span class="sxs-lookup"><span data-stu-id="42651-161">1,000</span></span>   |
| <span data-ttu-id="42651-162">PE-Cess te betalen</span><span class="sxs-lookup"><span data-stu-id="42651-162">PE-Cess payable</span></span>   |        | <span data-ttu-id="42651-163">220</span><span class="sxs-lookup"><span data-stu-id="42651-163">220</span></span>    |
| <span data-ttu-id="42651-164">SHE Cess te betalen</span><span class="sxs-lookup"><span data-stu-id="42651-164">SHE Cess payable</span></span>  |        | <span data-ttu-id="42651-165">110</span><span class="sxs-lookup"><span data-stu-id="42651-165">110</span></span>    |