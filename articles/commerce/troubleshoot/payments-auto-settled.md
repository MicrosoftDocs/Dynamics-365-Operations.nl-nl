---
title: Betalingen worden automatisch vereffend voordat orders worden gefactureerd of verzonden
description: Dit onderwerp bevat richtlijnen voor probleemoplossing die u kunnen helpen wanneer een betaling in de Adyen-portal direct na het plaatsen van een order wordt vereffend, zelfs als de verkooporder nog niet is gefactureerd of verzonden.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 43fe90cf99ddbe42dc89685e7fc747ded5a285c0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801646"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a><span data-ttu-id="7897a-103">Betalingen worden automatisch vereffend voordat orders worden gefactureerd of verzonden</span><span class="sxs-lookup"><span data-stu-id="7897a-103">Payments are automatically settled before orders are invoiced or shipped</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7897a-104">Dit onderwerp bevat richtlijnen voor probleemoplossing die u kunnen helpen wanneer een betaling in de Adyen-portal direct na het plaatsen van een order wordt vereffend, zelfs als de verkooporder nog niet is gefactureerd of verzonden.</span><span class="sxs-lookup"><span data-stu-id="7897a-104">This topic provides troubleshooting guidance that can help when a payment is settled in the Adyen portal immediately after an order is placed, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="description"></a><span data-ttu-id="7897a-105">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="7897a-105">Description</span></span>

<span data-ttu-id="7897a-106">Nadat een order is geplaatst, wordt de betaling onmiddeld vereffend in de Adyen-portal, zelfs als de verkooporder nog niet is gefactureerd of verzonden.</span><span class="sxs-lookup"><span data-stu-id="7897a-106">After an order is placed, the payment is immediately settled in the Adyen portal, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="resolution"></a><span data-ttu-id="7897a-107">Oplossing</span><span class="sxs-lookup"><span data-stu-id="7897a-107">Resolution</span></span>

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a><span data-ttu-id="7897a-108">Handmatig vastleggen voor e-commercebetalingen configureren in de Adyen-portal</span><span class="sxs-lookup"><span data-stu-id="7897a-108">Configure manual capture for e-commerce payments in the Adyen portal</span></span>

<span data-ttu-id="7897a-109">Voer de volgende stappen uit als u het handmatig vastleggen voor e-commercebetalingen wilt configureren in de Adyen-portal.</span><span class="sxs-lookup"><span data-stu-id="7897a-109">To configure manual capture for e-commerce payments in the Adyen portal, follow these steps.</span></span>

1. <span data-ttu-id="7897a-110">Meld u aan bij de Adyen-portal.</span><span class="sxs-lookup"><span data-stu-id="7897a-110">Sign in to the Adyen portal.</span></span>
1. <span data-ttu-id="7897a-111">Selecteer in de rechterbovenhoek uw verkoperrekening voor het e-commercekanaal.</span><span class="sxs-lookup"><span data-stu-id="7897a-111">In the upper-right corner, select your merchant account for the e-commerce channel.</span></span>
1. <span data-ttu-id="7897a-112">Selecteer op de bovenste navigatiebalk **Rekening** en vervolgens **Instellingen**.</span><span class="sxs-lookup"><span data-stu-id="7897a-112">On the top navigation, select **Account**, and then select **Settings**.</span></span>
1. <span data-ttu-id="7897a-113">Selecteer in het veld **Vertraging vastleggen** de optie **handmatig**.</span><span class="sxs-lookup"><span data-stu-id="7897a-113">In the **Capture Delay** field, select **manual**.</span></span>

    ![Instelling voor vertraging vastleggen in de Adyen-portal](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a><span data-ttu-id="7897a-115">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="7897a-115">Additional resources</span></span>

[<span data-ttu-id="7897a-116">Adyen-betaling vastleggen</span><span class="sxs-lookup"><span data-stu-id="7897a-116">Adyen payment capture</span></span>](https://docs.adyen.com/point-of-sale/capturing-payments)

[<span data-ttu-id="7897a-117">Dynamics 365-betalingsconnector voor Adyen</span><span class="sxs-lookup"><span data-stu-id="7897a-117">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="7897a-118">De Adyen-betalingsconnector voor Dynamics 365 instellen</span><span class="sxs-lookup"><span data-stu-id="7897a-118">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
