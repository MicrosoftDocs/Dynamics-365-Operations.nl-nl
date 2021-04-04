---
title: Fout bij ordersynchronisatie in verband met de standaardbetalingsservice
description: Dit onderwerp bevat richtlijnen voor probleemoplossing die u kunnen helpen bij het oplossen van een fout die kan optreden als een online order wordt gesynchroniseerd.
author: Reza-Assadi
manager: AnnBe
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
ms.openlocfilehash: dd7c400f26b6fc7fbe1d4fec43a52295eb363333
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585261"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a><span data-ttu-id="63d63-103">Fout bij ordersynchronisatie in verband met de standaardbetalingsservice</span><span class="sxs-lookup"><span data-stu-id="63d63-103">Order synchronization error related to the default payment service</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="63d63-104">Dit onderwerp bevat richtlijnen voor probleemoplossing die u kunnen helpen bij het oplossen van een fout die kan optreden als een online order wordt gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="63d63-104">This topic provides troubleshooting guidance that can help fix an error that might occur when an online order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="63d63-105">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="63d63-105">Description</span></span>

<span data-ttu-id="63d63-106">Wanneer u een online order synchroniseert, wordt het volgende foutbericht weergegeven: 'Er moet een standaardbetalingsservice zijn voor het verwerken van creditcardtransacties'.</span><span class="sxs-lookup"><span data-stu-id="63d63-106">When you sync an online order, you receive the following error message: "There must be a default payment service to process credit card transactions."</span></span>

![Fout door ontbrekende standaardbetalingsservice](media/default-payment-method-error.jpg)

## <a name="resolution"></a><span data-ttu-id="63d63-108">Oplossing</span><span class="sxs-lookup"><span data-stu-id="63d63-108">Resolution</span></span>

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a><span data-ttu-id="63d63-109">De standaardbetalingsservice bevestigen of instellen in Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="63d63-109">Confirm or set the default payment service in Commerce headquarters</span></span>

<span data-ttu-id="63d63-110">Voer de volgende stappen uit om de standaardbetalingsservice te bevestigen of in te stellen in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="63d63-110">To confirm or set the default payment service in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="63d63-111">Ga naar **Leveranciers \> Instelling van betalingen \> Betalingsservice**.</span><span class="sxs-lookup"><span data-stu-id="63d63-111">Go to **Accounts receivable \> Payment setup \> Payment services**.</span></span>
1. <span data-ttu-id="63d63-112">Zorg ervoor dat de optie **Standaardverwerker voor de nieuwe creditcard** is ingesteld op **Ja** voor één betalingsservice.</span><span class="sxs-lookup"><span data-stu-id="63d63-112">Make sure that the **Default processor for new credit cards** option is set to **Yes** for one payment service.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="63d63-113">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="63d63-113">Additional resources</span></span>

[<span data-ttu-id="63d63-114">Instelling, autorisatie en registratie van creditcards</span><span class="sxs-lookup"><span data-stu-id="63d63-114">Credit card setup, authorization, and capture</span></span>](https://docs.microsoft.com/dynamics365/finance/accounts-receivable/credit-card-authorizations)
