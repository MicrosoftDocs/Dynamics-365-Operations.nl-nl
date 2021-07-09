---
title: Leverancierscode niet geautoriseerd voor een specifiek product en specifieke datum
description: Wanneer u een geplande order probeert te fiatteren of een regel aan een inkooporder wilt toevoegen, wordt een foutbericht weergegeven waarin staat dat de leverancierscode niet is geautoriseerd voor een product en datum.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO_ReqTransPoMarkFirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e6b1189e4fedfdb029f4b4503f0635133df9d87e
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294050"
---
# <a name="vendor-code-isnt-authorized-for-a-specific-product-and-date"></a><span data-ttu-id="1ef52-103">Leverancierscode niet geautoriseerd voor een specifiek product en specifieke datum</span><span class="sxs-lookup"><span data-stu-id="1ef52-103">Vendor code isn't authorized for a specific product and date</span></span>

<span data-ttu-id="1ef52-104">Foutcode: SYP4881415</span><span class="sxs-lookup"><span data-stu-id="1ef52-104">Error code: SYP4881415</span></span>

## <a name="symptoms"></a><span data-ttu-id="1ef52-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="1ef52-105">Symptoms</span></span>

<span data-ttu-id="1ef52-106">Wanneer u probeert een geplande order te fiatteren of een regel toe te voegen aan een inkooporder, wordt het volgende foutbericht weergegeven:</span><span class="sxs-lookup"><span data-stu-id="1ef52-106">When you try to firm a planned order or add a line to a purchase order, you receive the following error message:</span></span>

> <span data-ttu-id="1ef52-107">Leverancierscode %1 is niet geautoriseerd voor %2 op %3.</span><span class="sxs-lookup"><span data-stu-id="1ef52-107">Vendor code %1 is not authorized for %2 on %3.</span></span>

## <a name="cause"></a><span data-ttu-id="1ef52-108">Oorzaak</span><span class="sxs-lookup"><span data-stu-id="1ef52-108">Cause</span></span>

<span data-ttu-id="1ef52-109">De fout treedt op omdat het veld **Controlemethode voor goedgekeurde leveranciers** is ingesteld op *Alleen waarschuwing* of *Niet toegestaan* voor het opgegeven product en de leverancier op dit moment niet is geautoriseerd om dat product te leveren.</span><span class="sxs-lookup"><span data-stu-id="1ef52-109">The error occurs because the **Approved vendor check method** field is set to *Warning only* or *Not allowed* for the specified product, and the vendor isn't currently authorized to supply that product.</span></span>

## <a name="resolution"></a><span data-ttu-id="1ef52-110">Oplossing</span><span class="sxs-lookup"><span data-stu-id="1ef52-110">Resolution</span></span>

<span data-ttu-id="1ef52-111">Om dit probleem op te lossen, schakelt u de leverancierscontrole voor het relevante product uit of keurt u de leverancier goed.</span><span class="sxs-lookup"><span data-stu-id="1ef52-111">To fix this issue, either disable the vendor check for the relevant product or approve the vendor.</span></span>

<span data-ttu-id="1ef52-112">Volg deze stappen om de leverancierscontrole voor een product uit te schakelen.</span><span class="sxs-lookup"><span data-stu-id="1ef52-112">To disable the vendor check for a product, follow these steps.</span></span>

1. <span data-ttu-id="1ef52-113">Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="1ef52-113">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="1ef52-114">Open het relevante product.</span><span class="sxs-lookup"><span data-stu-id="1ef52-114">Open the relevant product.</span></span>
1. <span data-ttu-id="1ef52-115">Stel op het sneltabblad **Inkoop** het veld **Controlemethode voor goedgekeurde leveranciers** in op een andere waarde dan *Alleen waarschuwing* of *Niet toegestaan*.</span><span class="sxs-lookup"><span data-stu-id="1ef52-115">On the **Purchase** FastTab, set the **Approved vendor check method** field to a value other than *Warning only* or *Not allowed*.</span></span>

<span data-ttu-id="1ef52-116">Volg deze stappen om een leverancier voor een product goed te keuren.</span><span class="sxs-lookup"><span data-stu-id="1ef52-116">To approve a vendor for a product, follow these steps.</span></span>

1. <span data-ttu-id="1ef52-117">Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="1ef52-117">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="1ef52-118">Open het betreffende artikel.</span><span class="sxs-lookup"><span data-stu-id="1ef52-118">Open the relevant item.</span></span>
1. <span data-ttu-id="1ef52-119">Klik in het actievenster in het tabblad **Inkoop** in de groep **Goedgekeurde leverancier** op **Instellingen**.</span><span class="sxs-lookup"><span data-stu-id="1ef52-119">On the Action Pane, on the **Purchase** tab, in the **Approved vendor** group, select **Setup**.</span></span>
1. <span data-ttu-id="1ef52-120">Voeg op de lijstpagina **Goedgekeurde leverancier** een rij toe aan het raster en stel er de volgende waarden voor in:</span><span class="sxs-lookup"><span data-stu-id="1ef52-120">On the **Approved vendor** list page, add a row to the grid, and set the following values for it:</span></span>

    - <span data-ttu-id="1ef52-121">**Leverancier**: selecteer de leverancier die moet worden goedgekeurd voor het huidige product.</span><span class="sxs-lookup"><span data-stu-id="1ef52-121">**Vendor** – Select the vendor to approve for the current product.</span></span>
    - <span data-ttu-id="1ef52-122">**Ingangsdatum**: selecteer de eerste datum waarvoor de leverancier is goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="1ef52-122">**Effective date** – Select the first date that the vendor is approved for.</span></span>
    - <span data-ttu-id="1ef52-123">**Vervaldatum**: selecteer de laatste datum waarvoor de leverancier is goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="1ef52-123">**Expiration date** – Select the last date that the vendor is approved for.</span></span>

<span data-ttu-id="1ef52-124">Meer informatie over dit onderwerp vindt u in [Leveranciers goedkeuren voor specifieke producten](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).</span><span class="sxs-lookup"><span data-stu-id="1ef52-124">For more information, see [Approve vendors for specific products](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).</span></span>
