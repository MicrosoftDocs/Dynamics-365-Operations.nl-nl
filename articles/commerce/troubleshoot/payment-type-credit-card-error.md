---
title: Fout Betalingstype moet creditcard zijn op de verkooporderpagina
description: Dit onderwerp bevat richtlijnen voor probleemoplossing die u kunnen helpen als een foutbericht wordt weergegeven op de verkooporderpagina nadat een order is gesynchroniseerd.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5be19949e9d1dbc43fdd3e6def119effa50a34d0
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018405"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a><span data-ttu-id="ae142-103">Fout 'Betalingstype moet creditcard zijn' op de verkooporderpagina</span><span class="sxs-lookup"><span data-stu-id="ae142-103">"Payment type must be credit card" error on the sales order page</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ae142-104">Dit onderwerp bevat richtlijnen voor probleemoplossing die u kunnen helpen als een foutbericht wordt weergegeven op de verkooporderpagina nadat een order is gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="ae142-104">This topic provides troubleshooting guidance that can help when an error message is shown on the sales order page after an order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="ae142-105">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="ae142-105">Description</span></span>

<span data-ttu-id="ae142-106">Wanneer u de verkooporderpagina opent nadat u een order hebt gesynchroniseerd, wordt het volgende foutbericht weergegeven: 'Het betalingstype moet creditcard zijn, omdat het creditcardnummer is opgegeven'.</span><span class="sxs-lookup"><span data-stu-id="ae142-106">When you open the sales order page after you sync an order, you receive the following error message: "The payment type must be credit card, since the credit card number has been specified."</span></span>

![Fout Betalingstype moet een creditcard zijn](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a><span data-ttu-id="ae142-108">Oplossing</span><span class="sxs-lookup"><span data-stu-id="ae142-108">Resolution</span></span>

### <a name="set-the-payment-type-in-commerce-headquarters"></a><span data-ttu-id="ae142-109">Het betalingstype instellen in Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="ae142-109">Set the payment type in Commerce headquarters</span></span>

1. <span data-ttu-id="ae142-110">Ga naar **Klanten \> Betalingsinstelling \> Betalingstermijnen**.</span><span class="sxs-lookup"><span data-stu-id="ae142-110">Go to **Accounts receivable \> Payment setup \> Terms of payment**.</span></span>
1. <span data-ttu-id="ae142-111">Selecteer in de linkernavigatie uw betalingsvoorwaarden.</span><span class="sxs-lookup"><span data-stu-id="ae142-111">In the left navigation, select your terms of payment.</span></span>
1. <span data-ttu-id="ae142-112">Controleer in het veld **Betalingstype** of **Creditcard** is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="ae142-112">In the **Payment type** field, make sure that **Credit card** is selected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ae142-113">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="ae142-113">Additional resources</span></span>

[<span data-ttu-id="ae142-114">Online verkopen en betalingen boeken</span><span class="sxs-lookup"><span data-stu-id="ae142-114">Posting of online sales and payments</span></span>](../tasks/posting-online-sales-payments.md)
