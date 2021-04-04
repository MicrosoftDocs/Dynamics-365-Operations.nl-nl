---
title: Op de pagina met de creditcardinvoer wordt een fout weergegeven bij het uitchecken
description: Dit onderwerp bevat richtlijnen voor probleemoplossing die u kunnen helpen als de sectie Betalingsmethode niet wordt geladen en er een foutbericht wordt weergegeven.
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
ms.openlocfilehash: f0751fc76e6eb4320f766886b4c1efcb1042e996
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585262"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a><span data-ttu-id="ad425-103">Op de pagina met de creditcardinvoer wordt een fout weergegeven bij het uitchecken</span><span class="sxs-lookup"><span data-stu-id="ad425-103">Credit card entry page shows an error at checkout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ad425-104">Dit onderwerp bevat richtlijnen voor probleemoplossing die u kunnen helpen als de sectie **Betalingsmethode** niet wordt geladen en er een foutbericht wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ad425-104">This topic provides troubleshooting guidance that can help when the **Payment method** section isn't loaded and shows an error message.</span></span>

## <a name="description"></a><span data-ttu-id="ad425-105">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="ad425-105">Description</span></span>

<span data-ttu-id="ad425-106">Wanneer u de uitcheckpagina van een online winkel opent, wordt de sectie **Betalingsmethode** niet geladen en wordt het volgende foutbericht weergegeven: 'Er is een fout opgetreden.</span><span class="sxs-lookup"><span data-stu-id="ad425-106">When you open the checkout page of an online store, the **Payment method** section isn't loaded, and the following error message is shown: "Something went wrong.</span></span> <span data-ttu-id="ad425-107">Probeer het later opnieuw.'</span><span class="sxs-lookup"><span data-stu-id="ad425-107">Please try again later."</span></span>

![Fout in betalingsmodule](media/payment-module-error.jpg)

## <a name="resolution"></a><span data-ttu-id="ad425-109">Oplossing</span><span class="sxs-lookup"><span data-stu-id="ad425-109">Resolution</span></span>

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a><span data-ttu-id="ad425-110">Wacht tot de cache van Commerce Scale Unit verloopt</span><span class="sxs-lookup"><span data-stu-id="ad425-110">Wait for the Commerce Scale Unit cache to expire</span></span>

<span data-ttu-id="ad425-111">De instellingen voor de betalingsservice op de uitcheckpagina van de online winkel worden in de cache opgeslagen op de Commerce Scale Unit, en het kan tot 15 minuten duren voordat deze op de e-commercesite wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ad425-111">The payment service settings on the online store's checkout page are cached on the Commerce Scale Unit and can take up to 15 minutes to appear on the e-commerce site.</span></span> <span data-ttu-id="ad425-112">Deze instellingen van de betalingsservice omvatten wijzigingen in de verkopersrekening-id, de cloud-API-sleutel en verschillende configuratie-instellingen die aan de betalingsmethode zijn gerelateerd.</span><span class="sxs-lookup"><span data-stu-id="ad425-112">These payment service settings include changes to the merchant account ID, cloud API key, and various configuration settings that are related to the payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ad425-113">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="ad425-113">Additional resources</span></span>

[<span data-ttu-id="ad425-114">Een online afzetkanaal instellen</span><span class="sxs-lookup"><span data-stu-id="ad425-114">Set up an online channel</span></span>](../channel-setup-online.md)
