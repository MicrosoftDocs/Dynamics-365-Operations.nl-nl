---
title: Bronbelasting in verkooptransacties
description: Dit onderwerp bevat de stappen voor het voorkomen van de berekening van bronbelasting voor geselecteerde klanten. Voor klanten die bronbelasting opgeven in hun betalingen aan u, kunt u de standaard bronbelastinggroep toewijzen.
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
ms.openlocfilehash: c839df1b54cdb60beefa6dc6c3fc6e945a6eac85
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256638"
---
# <a name="withholding-tax-in-sales-transactions"></a><span data-ttu-id="68efb-104">Bronbelasting in verkooptransacties</span><span class="sxs-lookup"><span data-stu-id="68efb-104">Withholding tax in sales transactions</span></span>

<span data-ttu-id="68efb-105">Dit onderwerp bevat de stappen voor het voorkomen van de berekening van bronbelasting voor geselecteerde klanten.</span><span class="sxs-lookup"><span data-stu-id="68efb-105">This topic lists the steps for avoiding the calculation of withholding tax for selected customers.</span></span> <span data-ttu-id="68efb-106">Voor klanten die bronbelasting opgeven in hun betalingen aan u, kunt u de standaard **bronbelastinggroep** toewijzen op de pagina **Klanten**.</span><span class="sxs-lookup"><span data-stu-id="68efb-106">For customers who specify withholding tax in their payments to you, you can assign the default **Withholding tax group** on the **Customers** page.</span></span> 

1. <span data-ttu-id="68efb-107">Ga in het navigatiedeelvenster naar **Modules > Klanten > Klanten > Alle klanten**.</span><span class="sxs-lookup"><span data-stu-id="68efb-107">Go to **Navigation pane > Modules > Accounts receivable > Customers > All customers**.</span></span>

2. <span data-ttu-id="68efb-108">Klik op de betreffende klantrekening en klik op **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="68efb-108">Click the respective customer account, click **Edit**.</span></span>

3. <span data-ttu-id="68efb-109">Stel op het tabblad **Factuur en levering** het veld **Bronbelasting berekenen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="68efb-109">In the **Invoice and delivery** tab, set the **Calculate withholding tax** field to **Yes**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="68efb-110">Bronbelasting wordt niet berekend als **Bronbelasting berekenen** voor deze klant niet wordt ingeschakeld in de hoofdgegevens.</span><span class="sxs-lookup"><span data-stu-id="68efb-110">Withholding tax will not be calculated if **Calculate withholding tax** is not switched on for this customer in the master data.</span></span>

4. <span data-ttu-id="68efb-111">Selecteer een bronbelastinggroep in **Bronbelastinggroep**.</span><span class="sxs-lookup"><span data-stu-id="68efb-111">Select a withholding tax group in **Withholding tax group**.</span></span>

5. <span data-ttu-id="68efb-112">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="68efb-112">Click **Save**.</span></span>

<span data-ttu-id="68efb-113">Voor artikelen/services waarvoor bronbelasting moet worden betaald, kunt u de standaard **artikelbronbelastinggroep** toewijzen in **Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="68efb-113">For items/services, which are liable to withholding tax, you can assign the default **Item withholding tax group** in **Released Products**.</span></span>

1. <span data-ttu-id="68efb-114">Ga naar **Navigatievenster > Modules > Productgegevensbeheer > Producten > Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="68efb-114">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>

2. <span data-ttu-id="68efb-115">Klik op het betreffende artikelnummer en klik op **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="68efb-115">Click the respective Item number, click **Edit**.</span></span>

3. <span data-ttu-id="68efb-116">Klik op het tabblad **Verkopen** op **Bronbelasting berekenen**.</span><span class="sxs-lookup"><span data-stu-id="68efb-116">In the **Sell** tab, click **Calculate withholding tax**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="68efb-117">Bronbelasting wordt niet berekend als **Bronbelasting berekenen** niet op **Ja** is ingesteld voor dit artikel op het tabblad **Verkopen** op de pagina **Vrijgegeven product**.</span><span class="sxs-lookup"><span data-stu-id="68efb-117">Withholding tax will not be calculated if **Calculate withholding tax** is not set to **Yes** for this Item in the **Sell** tab on the **Released product** page.</span></span>

4. <span data-ttu-id="68efb-118">Selecteer een artikelbronbelastinggroep in de lijst **Artikelbronbelastinggroep**.</span><span class="sxs-lookup"><span data-stu-id="68efb-118">Select an Item withholding tax group in **Item withholding tax group** list.</span></span>

5. <span data-ttu-id="68efb-119">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="68efb-119">Click **Save**.</span></span>

<span data-ttu-id="68efb-120">Bronbelastinggroepen en artikelbronbelastinggroepen kunnen worden toegewezen via de pagina **Verkooporder**.</span><span class="sxs-lookup"><span data-stu-id="68efb-120">Withholding tax groups and Item withholding tax groups can be assigned using the **Sales order** page.</span></span> 

<span data-ttu-id="68efb-121">De standaard bronbelastinggroep en artikelbronbelastinggroep worden als standaardwaarden gebruikt op verkooporderregels wanneer u een nieuwe verkooporder maakt.</span><span class="sxs-lookup"><span data-stu-id="68efb-121">The default Withholding tax group and Item withholding tax group will be used as default entries on sales order lines when you create a new sales order.</span></span>

<span data-ttu-id="68efb-122">Bronbelasting wordt berekend en geboekt met **Journaal met betalingen van klant**.</span><span class="sxs-lookup"><span data-stu-id="68efb-122">Withholding tax is calculated and posted with **Customer payment journal**.</span></span> <span data-ttu-id="68efb-123">U kunt de toepasselijke bronbelastingcode en het werkelijke bronbelastingbedrag handmatig aanpassen op het tabblad **Bronbelasting** op de pagina **Transacties vereffenen**.</span><span class="sxs-lookup"><span data-stu-id="68efb-123">You can manually adjust the applicable withholding tax code, as well as the actual withholding tax amount in the **Withholding tax** tab on the **Settle transactions** page.</span></span>

<span data-ttu-id="68efb-124">Het berekende bronbelastingbedrag wordt afgetrokken van de klantbetaling en geboekt op de **tegenrekening voor bronbelasting** in een gerelateerd boekstuk.</span><span class="sxs-lookup"><span data-stu-id="68efb-124">The calculated withholding tax amount will be deducted from the customer payment and posted to the **Withholding tax offset** account in a related voucher.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]