---
title: Betalingsmethoden voor retouren zonder ontvangstbewijs beperken
description: In dit onderwerp wordt beschreven hoe bepaalde betalingstypen kunnen worden beperkt voor restitutie als de retouren worden gemaakt zonder ontvangstbewijs.
author: rapraj
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.openlocfilehash: dd07c9c95639c8e69e1013fd7da283cf51b60ed0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804522"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="e75d3-103">Betalingsmethoden voor retouren zonder ontvangstbewijs beperken</span><span class="sxs-lookup"><span data-stu-id="e75d3-103">Restrict payment methods for returns without a receipt</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="e75d3-104">Elk betalingstype dat een detailhandelaar accepteert, moet worden geconfigureerd wanneer het systeem wordt ingesteld.</span><span class="sxs-lookup"><span data-stu-id="e75d3-104">Each payment type that a retailer accepts must be configured when the system is set up.</span></span> <span data-ttu-id="e75d3-105">In dit onderwerp wordt beschreven hoe bepaalde betalingstypen kunnen worden beperkt voor restitutie als de retouren worden gemaakt zonder ontvangstbewijs.</span><span class="sxs-lookup"><span data-stu-id="e75d3-105">This topic describes how certain payment types can be restricted for refund if the returns are made without a receipt.</span></span>

## <a name="set-up-payment-methods"></a><span data-ttu-id="e75d3-106">Betalingsmethoden instellen</span><span class="sxs-lookup"><span data-stu-id="e75d3-106">Set up payment methods</span></span>

<span data-ttu-id="e75d3-107">Voor het instellen van betalingsmethoden moet u de volgende taken voltooien.</span><span class="sxs-lookup"><span data-stu-id="e75d3-107">To set up payment methods, the following tasks must be completed.</span></span>
1. <span data-ttu-id="e75d3-108">Maak de betalingsmethoden die door de gehele organisatie worden geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="e75d3-108">Create the payment methods that are accepted by the entire organization.</span></span>
2. <span data-ttu-id="e75d3-109">Kaarttypen en kaartnummers voor de hele organisatie maken.</span><span class="sxs-lookup"><span data-stu-id="e75d3-109">Create organization-wide card types and card numbers.</span></span> <span data-ttu-id="e75d3-110">Als creditcards of betaalpassen worden geaccepteerd, moet u één betalingsmethode maken voor kaarten en vervolgens de typen kaarten en kaartnummers voor de organisatie maken.</span><span class="sxs-lookup"><span data-stu-id="e75d3-110">If credit cards or debit cards are accepted, you must create one payment method for cards, and then create the organization-wide card types and card numbers.</span></span>
3. <span data-ttu-id="e75d3-111">Stel betalingsmethoden voor winkel in.</span><span class="sxs-lookup"><span data-stu-id="e75d3-111">Set up store payment methods.</span></span> <span data-ttu-id="e75d3-112">Koppel betalingsmethoden aan elke winkel en voer vervolgens de winkelspecifieke instellingen in voor elke betalingsmethode.</span><span class="sxs-lookup"><span data-stu-id="e75d3-112">Associate payment methods with each store, and then enter the store-specific settings for each payment method.</span></span>
4. <span data-ttu-id="e75d3-113">Betalingsmethoden via kaart instellen voor winkels.</span><span class="sxs-lookup"><span data-stu-id="e75d3-113">Set up card payment methods for stores.</span></span> <span data-ttu-id="e75d3-114">Voltooi de kaartinstellingen voor alle kaartbetalingsmethoden die door de winkel worden geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="e75d3-114">For any card payment methods that the store accepts, complete the card setup.</span></span>

<span data-ttu-id="e75d3-115">![Winkel instellen](media/NoReceiptReturns1.png "Instellen van detailhandelwinkel")</span><span class="sxs-lookup"><span data-stu-id="e75d3-115">![Store Setup](media/NoReceiptReturns1.png "Retail Store Setup")</span></span> 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="e75d3-116">Betalingsmethoden voor retouren zonder ontvangstbewijs beperken</span><span class="sxs-lookup"><span data-stu-id="e75d3-116">Restrict payment methods for returns without a receipt</span></span>

<span data-ttu-id="e75d3-117">Stel voor elke betalingsmethode voor winkels op de pagina **Winkelbeheer** onder **Retouren zonder ontvangstbewijs** **Beperken voor restituties zonder ontvangstbewijs** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e75d3-117">For each store payment method, on the **Store management** page, under **Non receipt returns**, set **Restrict for refunds without receipt** to **Yes**.</span></span> 

<span data-ttu-id="e75d3-118">De standaardwaarde van de wisselknop is **Nee**, waarmee wordt gegarandeerd dat de betalingsmethode is toegestaan voor restituties.</span><span class="sxs-lookup"><span data-stu-id="e75d3-118">The default value of the toggle is **No**, which ensures that the payment method is allowed for refunds.</span></span> 

<span data-ttu-id="e75d3-119">Wanneer **Beperken voor restituties zonder ontvangstbewijs** is ingesteld op **Ja**, is de geselecteerde betalingsmethode niet toegestaan voor restituties.</span><span class="sxs-lookup"><span data-stu-id="e75d3-119">When **Restrict for refunds without receipt** is set to **Yes**, the selected payment method will not be allowed for refunds.</span></span> 

<span data-ttu-id="e75d3-120">![Betalingsmethode van winkel](media/NoReceiptReturns3.png "Betalingsmethode detailhandelwinkel")</span><span class="sxs-lookup"><span data-stu-id="e75d3-120">![Store payment method](media/NoReceiptReturns3.png "Retail Store Payment Method")</span></span> 

> [!NOTE]
> <span data-ttu-id="e75d3-121">Wanneer een kassamedewerker een betalingsmethode selecteert die is beperkt voor restitutie zonder ontvangstbewijs, verschijnt een bericht om de acceptabele betalingsmethoden te controleren.</span><span class="sxs-lookup"><span data-stu-id="e75d3-121">When a cashier selects a payment method that is restricted for refund without a receipt, a message displays to verify the acceptable payment methods.</span></span>

<span data-ttu-id="e75d3-122">![Acceptabele betalingsmethoden](media/NoReceiptReturns4.png "Acceptabele betalingsmethoden")</span><span class="sxs-lookup"><span data-stu-id="e75d3-122">![Acceptable payment methods](media/NoReceiptReturns4.png "Acceptable payment methods")</span></span> 

<span data-ttu-id="e75d3-123">Als een transactie zowel een retour met een ontvangstbewijs als een retour zonder een ontvangstbewijs heeft, worden de beperkingsvoorwaarden niet afgedwongen omdat de transactie een retourwerkstroom met een ontvangstbewijs is.</span><span class="sxs-lookup"><span data-stu-id="e75d3-123">If a transaction has both a receipted return and a return without a receipt, the restriction conditions will not be enforced because the transaction will be a return workflow with a receipt.</span></span> 



[!INCLUDE[footer-include](../includes/footer-banner.md)]