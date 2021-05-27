---
title: Op de pagina met de creditcardinvoer wordt een fout weergegeven bij het uitchecken
description: Dit onderwerp bevat richtlijnen voor probleemoplossing die u kunnen helpen als de sectie Betalingsmethode niet wordt geladen en er een foutbericht wordt weergegeven.
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
ms.openlocfilehash: ea9105481e6c5812565f0d3604906c905bcb5443
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018501"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a><span data-ttu-id="19943-103">Op de pagina met de creditcardinvoer wordt een fout weergegeven bij het uitchecken</span><span class="sxs-lookup"><span data-stu-id="19943-103">Credit card entry page shows an error at checkout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="19943-104">Dit onderwerp bevat richtlijnen voor probleemoplossing die u kunnen helpen als de sectie **Betalingsmethode** niet wordt geladen en er een foutbericht wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="19943-104">This topic provides troubleshooting guidance that can help when the **Payment method** section isn't loaded and shows an error message.</span></span>

## <a name="description"></a><span data-ttu-id="19943-105">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="19943-105">Description</span></span>

<span data-ttu-id="19943-106">Wanneer u de uitcheckpagina van een online winkel opent, wordt de sectie **Betalingsmethode** niet geladen en wordt het volgende foutbericht weergegeven: 'Er is een fout opgetreden.</span><span class="sxs-lookup"><span data-stu-id="19943-106">When you open the checkout page of an online store, the **Payment method** section isn't loaded, and the following error message is shown: "Something went wrong.</span></span> <span data-ttu-id="19943-107">Probeer het later opnieuw.'</span><span class="sxs-lookup"><span data-stu-id="19943-107">Please try again later."</span></span>

![Fout in betalingsmodule](media/payment-module-error.jpg)

## <a name="resolution"></a><span data-ttu-id="19943-109">Oplossing</span><span class="sxs-lookup"><span data-stu-id="19943-109">Resolution</span></span>

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a><span data-ttu-id="19943-110">Wacht tot de cache van Commerce Scale Unit verloopt</span><span class="sxs-lookup"><span data-stu-id="19943-110">Wait for the Commerce Scale Unit cache to expire</span></span>

<span data-ttu-id="19943-111">De instellingen voor de betalingsservice op de uitcheckpagina van de online winkel worden in de cache opgeslagen op de Commerce Scale Unit, en het kan tot 15 minuten duren voordat deze op de e-commercesite wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="19943-111">The payment service settings on the online store's checkout page are cached on the Commerce Scale Unit and can take up to 15 minutes to appear on the e-commerce site.</span></span> <span data-ttu-id="19943-112">Deze instellingen van de betalingsservice omvatten wijzigingen in de verkopersrekening-id, de cloud-API-sleutel en verschillende configuratie-instellingen die aan de betalingsmethode zijn gerelateerd.</span><span class="sxs-lookup"><span data-stu-id="19943-112">These payment service settings include changes to the merchant account ID, cloud API key, and various configuration settings that are related to the payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="19943-113">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="19943-113">Additional resources</span></span>

[<span data-ttu-id="19943-114">Een online afzetkanaal instellen</span><span class="sxs-lookup"><span data-stu-id="19943-114">Set up an online channel</span></span>](../channel-setup-online.md)
