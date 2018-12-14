--- 
title: Facturen en hoofdgegevens controleren in leverancierssysteem
description: Wanneer u een factuur ontvangt van een leverancier voor goederen of services op een inkooporder, hanteert het bedrijf misschien een beleid waarbij de goederen of services moeten zijn ontvangen voordat de factuur kan worden goedgekeurd voor betaling.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cc995b474e86272b49629f97e1b4d4b4fb597b9d
ms.openlocfilehash: 946076d682a10becdc2c4a8baff7f52de7893119
ms.contentlocale: nl-nl
ms.lasthandoff: 12/04/2018

---
# <a name="audit-invoices-and-key-data-in-ap-system"></a><span data-ttu-id="524c7-103">Facturen en hoofdgegevens controleren in leverancierssysteem</span><span class="sxs-lookup"><span data-stu-id="524c7-103">Audit invoices and key data in AP system</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="524c7-104">Wanneer u een factuur ontvangt van een leverancier voor goederen of services op een inkooporder, hanteert het bedrijf misschien een beleid waarbij de goederen of services moeten zijn ontvangen voordat de factuur kan worden goedgekeurd voor betaling.</span><span class="sxs-lookup"><span data-stu-id="524c7-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="524c7-105">Controleer voordat u begint of de configuratiesleutel Factuurvereffening is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="524c7-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="524c7-106">In de pagina van parameters voor leveranciers, moet u ervoor zorgen dat de optie Factuurvereffeningsvalidatie inschakelen is geselecteerd, het veld Factuur met verschillen boeken is ingesteld en het veld Regelovereenstemmingsbeleid is ingesteld op Drieweg-afstemming.</span><span class="sxs-lookup"><span data-stu-id="524c7-106">In the Accounts payable parameters page, ensure that the Enable invoice matching validation option is selected, the Post invoice with discrepancies field is set to Require approval, and the Line matching policy field is set to Three-way matching.</span></span>

<span data-ttu-id="524c7-107">Bij deze procedure wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="524c7-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="524c7-108">De leveranciersmanager of Accounting Manager-rol kan deze stappen uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="524c7-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="524c7-109">Inkooporder maken</span><span class="sxs-lookup"><span data-stu-id="524c7-109">Create a purchase order</span></span>
1. <span data-ttu-id="524c7-110">Ga naar **Alle inkooporders**.</span><span class="sxs-lookup"><span data-stu-id="524c7-110">Go to **All purchase orders**.</span></span>
2. <span data-ttu-id="524c7-111">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="524c7-111">Click **New**.</span></span>
3. <span data-ttu-id="524c7-112">Typ een waarde in het veld **Leveranciersrekening**.</span><span class="sxs-lookup"><span data-stu-id="524c7-112">In the **Vendor account** field, type a value.</span></span>
4. <span data-ttu-id="524c7-113">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="524c7-113">Click **OK**.</span></span>
5. <span data-ttu-id="524c7-114">Klik op **Regel toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="524c7-114">Click **Add line**.</span></span>
6. <span data-ttu-id="524c7-115">Typ een waarde in het veld **Artikelnummer**.</span><span class="sxs-lookup"><span data-stu-id="524c7-115">In the **Item number** field, type a value.</span></span>
7. <span data-ttu-id="524c7-116">Klik in het actievenster op **Inkoop**.</span><span class="sxs-lookup"><span data-stu-id="524c7-116">On the Action Pane, click **Purchase**.</span></span>
8. <span data-ttu-id="524c7-117">Klik op **Bevestigen**.</span><span class="sxs-lookup"><span data-stu-id="524c7-117">Click **Confirm**.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="524c7-118">Een productontvangstbon boeken</span><span class="sxs-lookup"><span data-stu-id="524c7-118">Post a product receipt</span></span>
1. <span data-ttu-id="524c7-119">Klik in het actievenster op **Ontvangen**.</span><span class="sxs-lookup"><span data-stu-id="524c7-119">On the Action Pane, click **Receive**.</span></span>
2. <span data-ttu-id="524c7-120">Klik op **Productontvangstbon**.</span><span class="sxs-lookup"><span data-stu-id="524c7-120">Click **Product receipt**.</span></span>
3. <span data-ttu-id="524c7-121">Typ een waarde in het veld **Productontvangstbon**.</span><span class="sxs-lookup"><span data-stu-id="524c7-121">In the **Product receipt** field, type a value.</span></span>
4. <span data-ttu-id="524c7-122">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="524c7-122">Click **OK**.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="524c7-123">Een leveranciersfactuur registreren en vereffenen met productontvangstbon</span><span class="sxs-lookup"><span data-stu-id="524c7-123">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="524c7-124">Klik in het actievenster op **Factuur > Factuur**.</span><span class="sxs-lookup"><span data-stu-id="524c7-124">On the Action Pane, click **Invoice > Invoice**.</span></span>
2. <span data-ttu-id="524c7-125">Typ een waarde in het veld **Nummer**.</span><span class="sxs-lookup"><span data-stu-id="524c7-125">In the **Number** field, type a value.</span></span>
3. <span data-ttu-id="524c7-126">Klik op **Standaard vanaf: Bestelde hoeveelheid** om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="524c7-126">Click **Default from: Ordered quantity** to open the drop dialog.</span></span>
4. <span data-ttu-id="524c7-127">Selecteer een optie in het veld **Standaardhoeveelheid voor regels**.</span><span class="sxs-lookup"><span data-stu-id="524c7-127">In the **Default quantity for lines** field, select an option.</span></span>
5. <span data-ttu-id="524c7-128">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="524c7-128">Click **OK**.</span></span>
6. <span data-ttu-id="524c7-129">Klik op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="524c7-129">Click **Yes**.</span></span>
7. <span data-ttu-id="524c7-130">Klik op **Productontvangstbonnen vereffenen**.</span><span class="sxs-lookup"><span data-stu-id="524c7-130">Click **Match product receipts**.</span></span>
8. <span data-ttu-id="524c7-131">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="524c7-131">Click **OK**.</span></span>
9. <span data-ttu-id="524c7-132">Klik in het actievenster op **Controleren**.</span><span class="sxs-lookup"><span data-stu-id="524c7-132">On the Action Pane, click **Review**.</span></span>
10. <span data-ttu-id="524c7-133">Klik op **Vereffeningsgegevens**.</span><span class="sxs-lookup"><span data-stu-id="524c7-133">Click **Matching details**.</span></span>


