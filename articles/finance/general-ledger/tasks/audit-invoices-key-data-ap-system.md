---
title: Facturen en hoofdgegevens controleren in leverancierssysteem
description: Wanneer u een factuur ontvangt van een leverancier voor goederen of services op een inkooporder, hanteert het bedrijf misschien een beleid waarbij de goederen of services moeten zijn ontvangen voordat de factuur kan worden goedgekeurd voor betaling.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c6e8967fe4db67ff98fc7093792bdb82b73a33d9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177107"
---
# <a name="audit-invoices-and-key-data-in-ap-system"></a><span data-ttu-id="58b39-103">Facturen en hoofdgegevens controleren in leverancierssysteem</span><span class="sxs-lookup"><span data-stu-id="58b39-103">Audit invoices and key data in AP system</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="58b39-104">Wanneer u een factuur ontvangt van een leverancier voor goederen of services op een inkooporder, hanteert het bedrijf misschien een beleid waarbij de goederen of services moeten zijn ontvangen voordat de factuur kan worden goedgekeurd voor betaling.</span><span class="sxs-lookup"><span data-stu-id="58b39-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="58b39-105">Controleer voordat u begint of de configuratiesleutel Factuurvereffening is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="58b39-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="58b39-106">In de pagina van parameters voor leveranciers, moet u ervoor zorgen dat de optie Factuurvereffeningsvalidatie inschakelen is geselecteerd, het veld Factuur met verschillen boeken is ingesteld en het veld Regelovereenstemmingsbeleid is ingesteld op Drieweg-afstemming.</span><span class="sxs-lookup"><span data-stu-id="58b39-106">In the Accounts payable parameters page, ensure that the Enable invoice matching validation option is selected, the Post invoice with discrepancies field is set to Require approval, and the Line matching policy field is set to Three-way matching.</span></span>

<span data-ttu-id="58b39-107">Bij deze procedure wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="58b39-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="58b39-108">De leveranciersmanager of Accounting Manager-rol kan deze stappen uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="58b39-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="58b39-109">Inkooporder maken</span><span class="sxs-lookup"><span data-stu-id="58b39-109">Create a purchase order</span></span>
1. <span data-ttu-id="58b39-110">Ga naar **Alle inkooporders**.</span><span class="sxs-lookup"><span data-stu-id="58b39-110">Go to **All purchase orders**.</span></span>
2. <span data-ttu-id="58b39-111">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="58b39-111">Click **New**.</span></span>
3. <span data-ttu-id="58b39-112">Typ een waarde in het veld **Leveranciersrekening**.</span><span class="sxs-lookup"><span data-stu-id="58b39-112">In the **Vendor account** field, type a value.</span></span>
4. <span data-ttu-id="58b39-113">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="58b39-113">Click **OK**.</span></span>
5. <span data-ttu-id="58b39-114">Klik op **Regel toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="58b39-114">Click **Add line**.</span></span>
6. <span data-ttu-id="58b39-115">Typ een waarde in het veld **Artikelnummer**.</span><span class="sxs-lookup"><span data-stu-id="58b39-115">In the **Item number** field, type a value.</span></span>
7. <span data-ttu-id="58b39-116">Klik in het actievenster op **Inkoop**.</span><span class="sxs-lookup"><span data-stu-id="58b39-116">On the Action Pane, click **Purchase**.</span></span>
8. <span data-ttu-id="58b39-117">Klik op **Bevestigen**.</span><span class="sxs-lookup"><span data-stu-id="58b39-117">Click **Confirm**.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="58b39-118">Een productontvangstbon boeken</span><span class="sxs-lookup"><span data-stu-id="58b39-118">Post a product receipt</span></span>
1. <span data-ttu-id="58b39-119">Klik in het actievenster op **Ontvangen**.</span><span class="sxs-lookup"><span data-stu-id="58b39-119">On the Action Pane, click **Receive**.</span></span>
2. <span data-ttu-id="58b39-120">Klik op **Productontvangstbon**.</span><span class="sxs-lookup"><span data-stu-id="58b39-120">Click **Product receipt**.</span></span>
3. <span data-ttu-id="58b39-121">Typ een waarde in het veld **Productontvangstbon**.</span><span class="sxs-lookup"><span data-stu-id="58b39-121">In the **Product receipt** field, type a value.</span></span>
4. <span data-ttu-id="58b39-122">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="58b39-122">Click **OK**.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="58b39-123">Een leveranciersfactuur registreren en vereffenen met productontvangstbon</span><span class="sxs-lookup"><span data-stu-id="58b39-123">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="58b39-124">Klik in het actievenster op **Factuur > Factuur**.</span><span class="sxs-lookup"><span data-stu-id="58b39-124">On the Action Pane, click **Invoice > Invoice**.</span></span>
2. <span data-ttu-id="58b39-125">Typ een waarde in het veld **Nummer**.</span><span class="sxs-lookup"><span data-stu-id="58b39-125">In the **Number** field, type a value.</span></span>
3. <span data-ttu-id="58b39-126">Klik op **Standaard vanaf: Bestelde hoeveelheid** om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="58b39-126">Click **Default from: Ordered quantity** to open the drop dialog.</span></span>
4. <span data-ttu-id="58b39-127">Selecteer een optie in het veld **Standaardhoeveelheid voor regels**.</span><span class="sxs-lookup"><span data-stu-id="58b39-127">In the **Default quantity for lines** field, select an option.</span></span>
5. <span data-ttu-id="58b39-128">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="58b39-128">Click **OK**.</span></span>
6. <span data-ttu-id="58b39-129">Klik op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="58b39-129">Click **Yes**.</span></span>
7. <span data-ttu-id="58b39-130">Klik op **Productontvangstbonnen vereffenen**.</span><span class="sxs-lookup"><span data-stu-id="58b39-130">Click **Match product receipts**.</span></span>
8. <span data-ttu-id="58b39-131">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="58b39-131">Click **OK**.</span></span>
9. <span data-ttu-id="58b39-132">Klik in het actievenster op **Controleren**.</span><span class="sxs-lookup"><span data-stu-id="58b39-132">On the Action Pane, click **Review**.</span></span>
10. <span data-ttu-id="58b39-133">Klik op **Vereffeningsgegevens**.</span><span class="sxs-lookup"><span data-stu-id="58b39-133">Click **Matching details**.</span></span>

