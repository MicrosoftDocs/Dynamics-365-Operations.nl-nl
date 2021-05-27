---
title: Problemen met Dynamics 365-betalingsconnector voor Adyen oplossen
description: Dit onderwerp bevat richtlijnen voor probleemoplossing die u kunnen helpen ondersteuning te krijgen bij problemen met de Microsoft Dynamics 365-betalingsconnector voor Adyen.
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
ms.openlocfilehash: 707efeba9553b996e4e33a4754e42a9d22643e33
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019584"
---
# <a name="troubleshoot-dynamics-365-payment-connector-for-adyen-issues"></a><span data-ttu-id="696e9-103">Problemen met Dynamics 365-betalingsconnector voor Adyen oplossen</span><span class="sxs-lookup"><span data-stu-id="696e9-103">Troubleshoot Dynamics 365 Payment Connector for Adyen issues</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="696e9-104">Dit onderwerp bevat richtlijnen voor probleemoplossing die u kunnen helpen ondersteuning te krijgen bij problemen met de Microsoft Dynamics 365-betalingsconnector voor Adyen.</span><span class="sxs-lookup"><span data-stu-id="696e9-104">This topic provides troubleshooting guidance that can help you get support when you have issues with the Microsoft Dynamics 365 Payment Connector for Adyen.</span></span>

## <a name="description"></a><span data-ttu-id="696e9-105">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="696e9-105">Description</span></span>

<span data-ttu-id="696e9-106">U hebt problemen met de Dynamics 365-betalingsonnector voor Adyen in de volgende gebieden en u hebt ondersteuning nodig van het Adyen-team:</span><span class="sxs-lookup"><span data-stu-id="696e9-106">You have issues with the Dynamics 365 Payment Connector for Adyen in the following areas, and you require support from the Adyen team:</span></span>

- <span data-ttu-id="696e9-107">Configuratie van verkooppunt (POS), Modern Point Of Sale (MPOS), callcenter of Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="696e9-107">Configuration of Point of sale (POS), Modern point of sale (MPOS), call center, or Dynamics 365 Commerce</span></span>
- <span data-ttu-id="696e9-108">Het PSP-referentienummer (Payment Service Provider) van Adyen (bijvoorbeeld als u vragen hebt over afwijzingen, waaronder handmatige sleutelinvoer \[MKE\]-afwijzingen)</span><span class="sxs-lookup"><span data-stu-id="696e9-108">The Adyen payment service provider (PSP) reference number (for example, if you have questions about refusals, including manual key entry \[MKE\] refusals)</span></span>
- <span data-ttu-id="696e9-109">Alles wat niet werkt in test- of live verkopersomgevingen</span><span class="sxs-lookup"><span data-stu-id="696e9-109">Anything that isn't working in test or live merchant environments</span></span>

## <a name="resolution"></a><span data-ttu-id="696e9-110">Oplossing</span><span class="sxs-lookup"><span data-stu-id="696e9-110">Resolution</span></span>

<span data-ttu-id="696e9-111">Gebruik de volgende e-mailsjabloon om het ondersteuningsproces met het Adyen-team te starten.</span><span class="sxs-lookup"><span data-stu-id="696e9-111">Use the following email template to start the support process with the Adyen team.</span></span> <span data-ttu-id="696e9-112">Zorg ervoor dat het e-mailbericht alle vereiste gegevens bevat om het probleem sneller op te lossen.</span><span class="sxs-lookup"><span data-stu-id="696e9-112">To expedite troubleshooting, make sure that the email contains all the required details.</span></span>

| <span data-ttu-id="696e9-113">Veld</span><span class="sxs-lookup"><span data-stu-id="696e9-113">Field</span></span>        | <span data-ttu-id="696e9-114">Waarde</span><span class="sxs-lookup"><span data-stu-id="696e9-114">Value</span></span> |
|--------------|-------|
| <span data-ttu-id="696e9-115">T/m</span><span class="sxs-lookup"><span data-stu-id="696e9-115">To</span></span>           | `support@adyen.com` |
| <span data-ttu-id="696e9-116">CC</span><span class="sxs-lookup"><span data-stu-id="696e9-116">Cc</span></span>           | |
| <span data-ttu-id="696e9-117">Onderwerpregel</span><span class="sxs-lookup"><span data-stu-id="696e9-117">Subject line</span></span> | <span data-ttu-id="696e9-118">Ondersteuningsaanvraag Microsoft Dynamics</span><span class="sxs-lookup"><span data-stu-id="696e9-118">Microsoft Dynamics Support Request</span></span> |
| <span data-ttu-id="696e9-119">Hoofdtekst</span><span class="sxs-lookup"><span data-stu-id="696e9-119">Body</span></span>         | <p><span data-ttu-id="696e9-120">Hallo ondersteuning,</span><span class="sxs-lookup"><span data-stu-id="696e9-120">Hi Support,</span></span></p><p><span data-ttu-id="696e9-121">Wij vragen om ondersteuning voor het volgende probleem:</span><span class="sxs-lookup"><span data-stu-id="696e9-121">Please provide support for the following issue:</span></span></p><ul><li><span data-ttu-id="696e9-122">Verkoperrekening</span><span class="sxs-lookup"><span data-stu-id="696e9-122">Merchant account</span></span></li><li><span data-ttu-id="696e9-123">Omgeving (Test/Prod)</span><span class="sxs-lookup"><span data-stu-id="696e9-123">Environment (Test/Prod)</span></span></li><li><span data-ttu-id="696e9-124">Kanaal (POS/callcenter/Commerce e-commerce)</span><span class="sxs-lookup"><span data-stu-id="696e9-124">Channel (POS/call center/Commerce e-commerce)</span></span></li><li><span data-ttu-id="696e9-125">PSP-referentienummer als het probleem een specifieke transactie bevat (U kunt het PSP-referentienummer vinden op het ontvangstbewijs, in het Adyen-klantengebied of in het transactiemenu op de POS-terminal.)</span><span class="sxs-lookup"><span data-stu-id="696e9-125">PSP reference number, if the issue involved a specific transaction (You can find the PSP reference number on the receipt, in the Adyen Customer Area, or on the transactions menu on the POS terminal.)</span></span></li><li><span data-ttu-id="696e9-126">Schermopname of foto van het foutbericht, indien van toepassing</span><span class="sxs-lookup"><span data-stu-id="696e9-126">Screenshot or photo of the error message, if applicable</span></span></li><li><span data-ttu-id="696e9-127">Logboeken van gebeurtenisviewer (in .txt-indeling)</span><span class="sxs-lookup"><span data-stu-id="696e9-127">Event Viewer logs (in .txt format)</span></span></li><li><span data-ttu-id="696e9-128">Beschrijving van het probleem en de probleemoplossingsstappen die u hebt geprobeerd uit te voeren</span><span class="sxs-lookup"><span data-stu-id="696e9-128">Description of the issue and troubleshooting steps that you've tried</span></span></li></ul> |

## <a name="additional-resources"></a><span data-ttu-id="696e9-129">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="696e9-129">Additional resources</span></span>

[<span data-ttu-id="696e9-130">Betalingen met de Adyen-connector accepteren voor Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="696e9-130">Accept payments with the Adyen connector for Dynamics 365 Commerce</span></span>](https://www.adyen.com/partners/dynamics-365-commerce)

[<span data-ttu-id="696e9-131">Dynamics 365-betalingsconnector voor Adyen</span><span class="sxs-lookup"><span data-stu-id="696e9-131">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="696e9-132">De Adyen-betalingsconnector voor Dynamics 365 instellen</span><span class="sxs-lookup"><span data-stu-id="696e9-132">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
