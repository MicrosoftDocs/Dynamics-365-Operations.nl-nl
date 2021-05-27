---
title: Functionaliteit voor factuursplitsing
description: In dit onderwerp worden de instellingen en functies beschreven voor het splitsen van facturen op afleveradres en belastingrekeningnummer (TAN).
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
ms.openlocfilehash: 7dddbb9f69a9735c2a03d2b23928f5cb92d4e0fd
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023153"
---
# <a name="split-invoice-functionality"></a><span data-ttu-id="bd670-103">Functionaliteit voor factuursplitsing</span><span class="sxs-lookup"><span data-stu-id="bd670-103">Split invoice functionality</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bd670-104">In dit onderwerp worden de instellingen en functies beschreven voor het splitsen van facturen op afleveradres en belastingrekeningnummer (TAN).</span><span class="sxs-lookup"><span data-stu-id="bd670-104">This topic describes the setup and functionality for splitting invoices by delivery address and tax account number (TAN).</span></span>

<span data-ttu-id="bd670-105">Schakel op de pagina **Parameters van module Leveranciers** op het tabblad **Algemeen** het selectievakje **Productontvangstbon** of **Factuur** in om een productontvangstbon of factuur met verschillende afleveradressen en belastingrekeningnummers op de pagina **Inkooporder** te boeken en te splitsen.</span><span class="sxs-lookup"><span data-stu-id="bd670-105">On the **Accounts payable parameters** page, on the **General** tab, select the **Product receipt** or **Invoice** checkbox to post and split a product receipt or invoice that has different delivery addresses and TANs on the **Purchase order** page.</span></span> <span data-ttu-id="bd670-106">De geboekte factuur wordt dan opgesplitst per afleveradres en belastingrekeningnummer.</span><span class="sxs-lookup"><span data-stu-id="bd670-106">The posted invoice will then be split by delivery address and TAN.</span></span>

<span data-ttu-id="bd670-107">Stel op het tabblad **Overzicht bijwerken** op het sneltabblad **Splitsen op basis van** in de rij **Leveringsgegevens** de optie **Bevestiging**, **Orderverzamellijst**, **Pakbon** of **Factuur** op **Ja** in om een bevestiging, orderverzamellijst, pakbon of factuur te maken waar verschillende afleveradressen en belastingrekeningnummers zijn gedefinieerd voor verschillende factuurregels op de pagina **Verkooporder**.</span><span class="sxs-lookup"><span data-stu-id="bd670-107">On the **Summary update** tab, on the **Split based on** FastTab, in the **Delivery information** row, set the **Confirmation**, **Picking list**, **Packing slip**, or **Invoice** option to **Yes** to post and split a confirmation, picking list, packing slip, or invoice where different delivery addresses and TANs are defined for different invoice lines on the **Sales order** page.</span></span> <span data-ttu-id="bd670-108">De factuur wordt dan eerst gesplitst op afleveradres en vervolgens op belastingrekeningnummer.</span><span class="sxs-lookup"><span data-stu-id="bd670-108">The invoice will be split first by delivery address and then by TAN.</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="bd670-109">Als er geen opties voor **Leveringsgegevens** zijn ingesteld op **Ja**, wordt de factuur als één factuur geboekt.</span><span class="sxs-lookup"><span data-stu-id="bd670-109">If no options for **Delivery information** are set to **Yes**, the invoice will be posted as a single invoice.</span></span> <span data-ttu-id="bd670-110">Er vindt geen factuursplitsing plaats.</span><span class="sxs-lookup"><span data-stu-id="bd670-110">No invoice splitting will occur.</span></span>
> - <span data-ttu-id="bd670-111">Als u een pakbon wilt splitsen en boeken waarbij de factuurregels verschillende afleveradressen en belastingrekeningnummers hebben, moet u de optie **Pakbon** voor **Leveringsgegevens** instellen op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="bd670-111">To split and post a packing slip where the invoice lines have different delivery addresses and TANs, you must set the **Packing slip** option for **Delivery information** to **Yes**.</span></span>
> - <span data-ttu-id="bd670-112">Als u een factuur wilt splitsen en boeken waarbij de factuurregels verschillende afleveradressen en belastingrekeningnummers hebben, moet u de optie **Factuur** voor **Leveringsgegevens** instellen op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="bd670-112">To split and post an invoice where the invoice lines have different delivery addresses and TANs, you must set the **Invoice** option for **Delivery information** to **Yes**.</span></span>
> - <span data-ttu-id="bd670-113">Als u een factuur wilt splitsen en boeken waarbij de factuurregels verschillende afleveradressen maar hetzelfde belastingrekeningnummer hebben, moet u de optie **Factuur** voor **Leveringsgegevens** instellen op **Nee**.</span><span class="sxs-lookup"><span data-stu-id="bd670-113">To post an invoice where the invoice lines have different delivery addresses but the same TAN, set the **Invoice** option for **Delivery information** to **No**.</span></span> <span data-ttu-id="bd670-114">De factuur wordt dan gesplitst op afleveradres.</span><span class="sxs-lookup"><span data-stu-id="bd670-114">The invoice will be split by delivery address.</span></span>

## <a name="example"></a><span data-ttu-id="bd670-115">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="bd670-115">Example</span></span>

<span data-ttu-id="bd670-116">In dit voorbeeld is de optie **Factuur** voor **Leveringsgegevens** ingesteld op **Ja** op het tabblad **Overzicht bijwerken** van de pagina **Parameters van module Leveranciers**.</span><span class="sxs-lookup"><span data-stu-id="bd670-116">In this example, the **Invoice** option for **Delivery information** is set to **Yes** on the **Summary update** tab of the **Accounts payable parameters** page.</span></span> <span data-ttu-id="bd670-117">Er wordt een inkoopfactuur geboekt die de volgende instellingen heeft voor afleveradressen en belastingrekeningnummers op de regels:</span><span class="sxs-lookup"><span data-stu-id="bd670-117">A purchase invoice is posted that has the following setup for delivery addresses and TANs on the lines:</span></span>

- <span data-ttu-id="bd670-118">**Artikelregel 1:** Afleveradres 1, TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="bd670-118">**Item line 1:** Delivery address 1, TAN-ABCD12345A</span></span>
- <span data-ttu-id="bd670-119">**Artikelregel 2:** Afleveradres 1, TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="bd670-119">**Item line 2:** Delivery address 1, TAN-ABCD12345A</span></span>
- <span data-ttu-id="bd670-120">**Artikelregel 3:** Afleveradres 2, TAN-ABCE12345B</span><span class="sxs-lookup"><span data-stu-id="bd670-120">**Item line 3:** Delivery address 2, TAN-ABCE12345B</span></span>
- <span data-ttu-id="bd670-121">**Artikelregel 4:** Afleveradres 3, TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="bd670-121">**Item line 4:** Delivery address 3, TAN-ABCD12345A</span></span>

<span data-ttu-id="bd670-122">In dit geval wordt de oorspronkelijke factuur in twee facturen gesplitst en op de volgende manier geboekt:</span><span class="sxs-lookup"><span data-stu-id="bd670-122">In this case, the original invoice is split into two invoices and posted in the following way:</span></span>

- <span data-ttu-id="bd670-123">Factuur 1 wordt geboekt voor artikelregel 1 en artikelregel 2, omdat beide regels hetzelfde afleveradres en belastingrekeningnummer hebben.</span><span class="sxs-lookup"><span data-stu-id="bd670-123">Invoice 1 is posted for item line 1 and item line 2, because both lines have the same delivery address and TAN.</span></span>
- <span data-ttu-id="bd670-124">Factuur 2 wordt geboekt voor artikelregel 3.</span><span class="sxs-lookup"><span data-stu-id="bd670-124">Invoice 2 is posted for item line 3.</span></span>
- <span data-ttu-id="bd670-125">Factuur 3 wordt geboekt voor artikelregel 4.</span><span class="sxs-lookup"><span data-stu-id="bd670-125">Invoice 3 is posted for item line 4.</span></span>
