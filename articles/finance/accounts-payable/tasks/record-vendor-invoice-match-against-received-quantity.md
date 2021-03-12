---
title: Leverancierfactuur vastleggen en met ontvangen hoeveelheid matchen
description: Wanneer u een factuur ontvangt van een leverancier voor goederen of services op een inkooporder, hanteert het bedrijf misschien een beleid waarbij de goederen of services moeten zijn ontvangen voordat de factuur kan worden goedgekeurd voor betaling.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: be1e818e8a97684248c9c0b9d43c39e631f855f5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979258"
---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a><span data-ttu-id="bf806-103">Leverancierfactuur vastleggen en met ontvangen hoeveelheid matchen</span><span class="sxs-lookup"><span data-stu-id="bf806-103">Record vendor invoice and match against received quantity</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bf806-104">Wanneer u een factuur ontvangt van een leverancier voor goederen of services op een inkooporder, hanteert het bedrijf misschien een beleid waarbij de goederen of services moeten zijn ontvangen voordat de factuur kan worden goedgekeurd voor betaling.</span><span class="sxs-lookup"><span data-stu-id="bf806-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="bf806-105">Controleer voordat u begint of de configuratiesleutel Factuurvereffening is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="bf806-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="bf806-106">In de pagina van parameters voor leveranciers, moet u ervoor zorgen dat de optie Factuurvereffeningsvalidatie inschakelen is geselecteerd, het veld Factuur met verschillen boeken is ingesteld en het veld Regelovereenstemmingsbeleid is ingesteld op Drieweg-afstemming.</span><span class="sxs-lookup"><span data-stu-id="bf806-106">In the Accounts payable parameters page, ensure that the Enable invoice matching validation option is selected, the Post invoice with discrepancies field is set to Require approval, and the Line matching policy field is set to Three-way matching.</span></span>

<span data-ttu-id="bf806-107">Bij deze procedure wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="bf806-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="bf806-108">De leveranciersmanager of Accounting Manager-rol kan deze stappen uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="bf806-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="bf806-109">Inkooporder maken</span><span class="sxs-lookup"><span data-stu-id="bf806-109">Create a purchase order</span></span>
1. <span data-ttu-id="bf806-110">Ga naar Alle inkooporders.</span><span class="sxs-lookup"><span data-stu-id="bf806-110">Go to All purchase orders.</span></span>
2. <span data-ttu-id="bf806-111">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="bf806-111">Click New.</span></span>
3. <span data-ttu-id="bf806-112">Klik in het veld Leverancierrekening op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="bf806-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="bf806-113">Typ een waarde in het veld Leveranciersrekening.</span><span class="sxs-lookup"><span data-stu-id="bf806-113">In the Vendor account field, type a value.</span></span>
5. <span data-ttu-id="bf806-114">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="bf806-114">Click OK.</span></span>
6. <span data-ttu-id="bf806-115">Klik op Regel toevoegen.</span><span class="sxs-lookup"><span data-stu-id="bf806-115">Click Add line.</span></span>
7. <span data-ttu-id="bf806-116">Typ een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="bf806-116">In the Item number field, type a value.</span></span>
8. <span data-ttu-id="bf806-117">Klik in het actievenster op Inkoop.</span><span class="sxs-lookup"><span data-stu-id="bf806-117">On the Action Pane, click Purchase.</span></span>
9. <span data-ttu-id="bf806-118">Klik op Bevestigen.</span><span class="sxs-lookup"><span data-stu-id="bf806-118">Click Confirm.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="bf806-119">Een productontvangstbon boeken</span><span class="sxs-lookup"><span data-stu-id="bf806-119">Post a product receipt</span></span>
1. <span data-ttu-id="bf806-120">Klik in het actievenster op Ontvangen.</span><span class="sxs-lookup"><span data-stu-id="bf806-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="bf806-121">Klik op Productontvangstbon.</span><span class="sxs-lookup"><span data-stu-id="bf806-121">Click Product receipt.</span></span>
3. <span data-ttu-id="bf806-122">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="bf806-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="bf806-123">Typ een waarde in het veld Productontvangstbon.</span><span class="sxs-lookup"><span data-stu-id="bf806-123">In the Product receipt field, type a value.</span></span>
5. <span data-ttu-id="bf806-124">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="bf806-124">Click OK.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="bf806-125">Een leveranciersfactuur registreren en vereffenen met productontvangstbon</span><span class="sxs-lookup"><span data-stu-id="bf806-125">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="bf806-126">Klik in het actievenster op Factuur.</span><span class="sxs-lookup"><span data-stu-id="bf806-126">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="bf806-127">Klik op Factuur.</span><span class="sxs-lookup"><span data-stu-id="bf806-127">Click Invoice.</span></span>
3. <span data-ttu-id="bf806-128">Typ een waarde in het veld Nummer.</span><span class="sxs-lookup"><span data-stu-id="bf806-128">In the Number field, type a value.</span></span>
4. <span data-ttu-id="bf806-129">Klik op Standaard vanaf: Bestelde hoeveelheid om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="bf806-129">Click Default from: Ordered quantity to open the drop dialog.</span></span>
5. <span data-ttu-id="bf806-130">Selecteer een optie in het veld Standaardhoeveelheid voor regels.</span><span class="sxs-lookup"><span data-stu-id="bf806-130">In the Default quantity for lines field, select an option.</span></span>
6. <span data-ttu-id="bf806-131">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="bf806-131">Click OK.</span></span>
7. <span data-ttu-id="bf806-132">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="bf806-132">Click Yes.</span></span>
8. <span data-ttu-id="bf806-133">Klik op Productontvangstbonnen vereffenen.</span><span class="sxs-lookup"><span data-stu-id="bf806-133">Click Match product receipts.</span></span>
9. <span data-ttu-id="bf806-134">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="bf806-134">Click OK.</span></span>
10. <span data-ttu-id="bf806-135">Klik in het actievenster op Controleren.</span><span class="sxs-lookup"><span data-stu-id="bf806-135">On the Action Pane, click Review.</span></span>
11. <span data-ttu-id="bf806-136">Klik op Vereffeningsgegevens.</span><span class="sxs-lookup"><span data-stu-id="bf806-136">Click Matching details.</span></span>

