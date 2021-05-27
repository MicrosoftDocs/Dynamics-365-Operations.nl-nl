---
title: Opslaan voor mijn volgende betalingsoptie wordt niet weergegeven
description: Dit onderwerp biedt richtlijnen voor probleemoplossing die u kunnen helpen wanneer het selectievakje Opslaan voor mijn volgende betaling niet wordt weergegeven onder Betalingsmethode op de uitcheckpagina van een e-commercesite.
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
ms.openlocfilehash: af19a3abd78d543d82f7a8d017e2dc413115a6d8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018429"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a><span data-ttu-id="6c97c-103">Optie 'Opslaan voor mijn volgende betaling' wordt niet weergegeven</span><span class="sxs-lookup"><span data-stu-id="6c97c-103">"Save for my next payment" option doesn't appear</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6c97c-104">Dit onderwerp biedt richtlijnen voor probleemoplossing die u kunnen helpen wanneer het selectievakje **Opslaan voor mijn volgende betaling** niet wordt weergegeven onder **Betalingsmethode** op de uitcheckpagina van een e-commercesite.</span><span class="sxs-lookup"><span data-stu-id="6c97c-104">This topic provides troubleshooting guidance that can help when the **Save for my next payment** check box doesn't appear under **Payment method** on an e-commerce site's checkout page.</span></span>

## <a name="description"></a><span data-ttu-id="6c97c-105">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="6c97c-105">Description</span></span>

<span data-ttu-id="6c97c-106">Het selectievakje **Opslaan voor mijn volgende betaling** wordt niet weergegeven in de sectie **Betalingsmethode** op de uitcheckpagina van een e-commercesite.</span><span class="sxs-lookup"><span data-stu-id="6c97c-106">The **Save for my next payment** check box doesn't appear in the **Payment method** section on an e-commerce site's checkout page.</span></span>

<span data-ttu-id="6c97c-107">In de volgende afbeelding ziet u een voorbeeld van een uitcheckpagina met het selectievakje **Opslaan voor mijn volgende betaling**.</span><span class="sxs-lookup"><span data-stu-id="6c97c-107">The following illustration shows an example of a checkout page that includes the **Save for my next payment** check box.</span></span>

![Selectievakje Opslaan voor mijn volgende betaling in de module Betaling](media/payment-module-save-payment.jpg)

## <a name="resolution"></a><span data-ttu-id="6c97c-109">Oplossing</span><span class="sxs-lookup"><span data-stu-id="6c97c-109">Resolution</span></span>

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a><span data-ttu-id="6c97c-110">Controleren of de Dynamics 365-betalingsconnector voor Adyen correct is geconfigureerd in Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="6c97c-110">Verify that the Dynamics 365 Payment Connector for Adyen is correctly configured in Commerce headquarters</span></span>

<span data-ttu-id="6c97c-111">Voer deze stappen uit om te controleren of de Dynamics 365-betalingsconnector voor Adyen correct is geconfigureerd in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="6c97c-111">To verify that the Dynamics 365 Payment Connector for Adyen is correctly configured in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="6c97c-112">Ga naar **Retail en Commerce \> Afzetkanalen \> Online winkels**.</span><span class="sxs-lookup"><span data-stu-id="6c97c-112">Go to **Retail and Commerce \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="6c97c-113">Selecteer de online winkel.</span><span class="sxs-lookup"><span data-stu-id="6c97c-113">Select the online store.</span></span>
1. <span data-ttu-id="6c97c-114">Zorg ervoor op het sneltabblad **Betalingsrekeningen** dat het veld **Opslaan van betalingsgegevens toestaan in e-commerce** is ingesteld op **Waar**.</span><span class="sxs-lookup"><span data-stu-id="6c97c-114">On the **Payment accounts** FastTab, make sure that the **Allow saving payment information in e-commerce** field is set to **True**.</span></span>

![Het opslaan van betalingsgegevens toestaan in veld e-commerce in Commerce Headquarters](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a><span data-ttu-id="6c97c-116">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="6c97c-116">Additional resources</span></span>

[<span data-ttu-id="6c97c-117">Betalingsmodule</span><span class="sxs-lookup"><span data-stu-id="6c97c-117">Payment module</span></span>](../payment-module.md)

[<span data-ttu-id="6c97c-118">Online betaalmiddelen opslaan met de Adyen-connector</span><span class="sxs-lookup"><span data-stu-id="6c97c-118">Saving online payment instruments with the Adyen connector</span></span>](../dev-itpro/adyen-connector-listPI.md)
