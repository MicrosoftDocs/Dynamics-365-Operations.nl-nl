---
title: Bronbelasting in inkooptransacties
description: Voor leveranciers die bronbelasting moeten betalen, kunt u de standaard **bronbelastinggroep** toewijzen op de pagina **Alle leveranciers**.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
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
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 06c18e6b0779539a6da7ae7afbe000c4cfc78d9e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256662"
---
# <a name="withholding-tax-in-purchase-transactions"></a><span data-ttu-id="81396-103">Bronbelasting in inkooptransacties</span><span class="sxs-lookup"><span data-stu-id="81396-103">Withholding tax in purchase transactions</span></span>

<span data-ttu-id="81396-104">Voor leveranciers die bronbelasting moeten betalen, kunt u de standaard **bronbelastinggroep** toewijzen op de pagina **Alle leveranciers**.</span><span class="sxs-lookup"><span data-stu-id="81396-104">For vendors who are liable to withholding tax, you can assign the default **Withholding tax group** on the **All vendors** page.</span></span>

1. <span data-ttu-id="81396-105">Ga in het navigatievenster naar **Modules > Leveranciers > Leveranciers > Alle leveranciers**.</span><span class="sxs-lookup"><span data-stu-id="81396-105">Go to **Navigation pane > Modules > Accounts payable > Vendors > All vendors**.</span></span>

2. <span data-ttu-id="81396-106">Klik op de betreffende leveranciersrekening en klik op **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="81396-106">Click the respective Vendor account, click **Edit**.</span></span>

3. <span data-ttu-id="81396-107">Stel op het tabblad **Factuur en levering** het veld **Bronbelasting berekenen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="81396-107">In **Invoice and delivery** tab, set the **Calculate withholding tax** field to **Yes**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="81396-108">Bronbelasting wordt niet berekend als **Bronbelasting berekenen** voor deze leverancier niet wordt ingeschakeld in de gegevens.</span><span class="sxs-lookup"><span data-stu-id="81396-108">Withholding tax will not be calculated if **Calculate withholding tax** is not switched on for this vendor in the data.</span></span>

4. <span data-ttu-id="81396-109">Selecteer een bronbelastinggroep in **Bronbelastinggroep**.</span><span class="sxs-lookup"><span data-stu-id="81396-109">Select a withholding tax group in **Withholding tax group**.</span></span>

5. <span data-ttu-id="81396-110">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="81396-110">Click **Save**.</span></span>

<span data-ttu-id="81396-111">Voor artikelen/services waarvoor bronbelasting moet worden betaald, kunt u de standaard **artikelbronbelastinggroep** toewijzen in **Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="81396-111">For items/services which are liable to withholding tax, you can assign the default **Item withholding tax group** in **Released Products**.</span></span>

1. <span data-ttu-id="81396-112">Ga naar **Navigatievenster > Modules > Productgegevensbeheer > Producten > Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="81396-112">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>

2. <span data-ttu-id="81396-113">Klik op het betreffende artikelnummer en klik op **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="81396-113">Click the respective Item number, click **Edit**.</span></span>

3. <span data-ttu-id="81396-114">Klik op het tabblad **Inkopen** op **Bronbelasting berekenen**.</span><span class="sxs-lookup"><span data-stu-id="81396-114">In **Purchase** tab, click **Calculate withholding tax**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="81396-115">Bronbelasting wordt niet berekend als **Bronbelasting berekenen** niet op **Ja** is ingesteld voor dit artikel op het tabblad **Inkopen** op de pagina **Vrijgegeven product**.</span><span class="sxs-lookup"><span data-stu-id="81396-115">Withholding tax will not be calculated if **Calculate withholding tax** isn't set to **Yes** for this Item in the **Purchase** tab on the **Released product** page.</span></span>

4. <span data-ttu-id="81396-116">Selecteer een artikelbronbelastinggroep in de lijst **Artikelbronbelastinggroep**.</span><span class="sxs-lookup"><span data-stu-id="81396-116">Select an item withholding tax group in **Item withholding tax group** list.</span></span>

5. <span data-ttu-id="81396-117">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="81396-117">Click **Save**.</span></span>

<span data-ttu-id="81396-118">Bronbelastinggroepen en artikelbronbelastinggroepen kunnen worden toegewezen via de volgende pagina's:</span><span class="sxs-lookup"><span data-stu-id="81396-118">Withholding tax groups and Item withholding tax groups can be assigned in pages:</span></span> 

- <span data-ttu-id="81396-119">**Inkooporder**</span><span class="sxs-lookup"><span data-stu-id="81396-119">**Purchase order**</span></span>
- <span data-ttu-id="81396-120">**Leveranciersfactuur**</span><span class="sxs-lookup"><span data-stu-id="81396-120">**Vendor invoice**</span></span>
- <span data-ttu-id="81396-121">**Facturenjournaal**</span><span class="sxs-lookup"><span data-stu-id="81396-121">**Invoice journal**</span></span>

<span data-ttu-id="81396-122">De standaard bronbelastinggroep en artikelbronbelastinggroep worden naar de regels getransporteerd wanneer u **inkooporders** en/of **leveranciersfacturen in behandeling** maakt.</span><span class="sxs-lookup"><span data-stu-id="81396-122">The default Withholding tax group and Item withholding tax group will be carried into the lines when creating **Purchase orders** and/or **Pending Vendor invoices**.</span></span> <span data-ttu-id="81396-123">Voor **Leveranciersfactuurjournaal** kunt u **Bronbelasting berekenen** inschakelen en **Artikelbronbelastinggroep** selecteren op het tabblad **Algemeen** van het journaal.</span><span class="sxs-lookup"><span data-stu-id="81396-123">For **Vendor invoice journal**, you can switch on **Calculate withholding tax** and select **Item withholding tax group** in the **General** tab in the journal.</span></span>

<span data-ttu-id="81396-124">Het tijdelijke bronbelastingbedrag is beschikbaar in het veld **Gecorrigeerde bronbelasting** van het tabblad **Totalen** op de pagina **Inkooporder**.</span><span class="sxs-lookup"><span data-stu-id="81396-124">The temporary amount of withholding tax is available in the field **Adjusted withholding tax** of the **Totals** tab on the **Purchase order** page.</span></span>

![Bronbelasting is in de inkooporder opgenomen](media/withholding-tax-adjusted.png)

<span data-ttu-id="81396-126">Er wordt bronbelasting berekend in **Journaal met betalingen van leverancier**.</span><span class="sxs-lookup"><span data-stu-id="81396-126">Withholding tax is calculated on **Vendor payment journal**.</span></span> <span data-ttu-id="81396-127">U kunt de toepasselijke bronbelastingcodes en de werkelijke bronbelastingbedragen handmatig aanpassen op het tabblad **Bronbelasting** op de pagina **Transacties vereffenen**.</span><span class="sxs-lookup"><span data-stu-id="81396-127">You can manually adjust the applicable withholding tax codes as well as the actual withholding tax amounts in the **Withholding tax** tab on the **Settle transactions** page.</span></span>

![Bronbelasting kan handmatig worden gecorrigeerd op de pagina Transacties vereffenen](media/withholding-tax-vendor-payment-tab.png)

<span data-ttu-id="81396-129">Het afgeleide bronbelastingbedrag wordt afgetrokken van de leveranciersbetaling en geboekt op de **rekening voor bronbelasting** in een gerelateerd boekstuk.</span><span class="sxs-lookup"><span data-stu-id="81396-129">The derived withholding tax amount will be deducted from the vendor payment and posted to the **Withholding tax account** in a related voucher.</span></span>

![Bronbelastingrekening met een gerelateerd boekstuk](media/withholding-tax-adjusted.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]