---
title: Problemen met Dynamics 365-betalingsconnector voor Adyen oplossen
description: Dit onderwerp bevat richtlijnen voor probleemoplossing die u kunnen helpen ondersteuning te krijgen bij problemen met de Microsoft Dynamics 365-betalingsconnector voor Adyen.
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
ms.openlocfilehash: f01db3fa670355696c094be544775a3abc557a70
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585260"
---
# <a name="troubleshoot-dynamics-365-payment-connector-for-adyen-issues"></a><span data-ttu-id="d64a8-103">Problemen met Dynamics 365-betalingsconnector voor Adyen oplossen</span><span class="sxs-lookup"><span data-stu-id="d64a8-103">Troubleshoot Dynamics 365 Payment Connector for Adyen issues</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d64a8-104">Dit onderwerp bevat richtlijnen voor probleemoplossing die u kunnen helpen ondersteuning te krijgen bij problemen met de Microsoft Dynamics 365-betalingsconnector voor Adyen.</span><span class="sxs-lookup"><span data-stu-id="d64a8-104">This topic provides troubleshooting guidance that can help you get support when you have issues with the Microsoft Dynamics 365 Payment Connector for Adyen.</span></span>

## <a name="description"></a><span data-ttu-id="d64a8-105">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="d64a8-105">Description</span></span>

<span data-ttu-id="d64a8-106">U hebt problemen met de Dynamics 365-betalingsonnector voor Adyen in de volgende gebieden en u hebt ondersteuning nodig van het Adyen-team:</span><span class="sxs-lookup"><span data-stu-id="d64a8-106">You have issues with the Dynamics 365 Payment Connector for Adyen in the following areas, and you require support from the Adyen team:</span></span>

- <span data-ttu-id="d64a8-107">Configuratie van verkooppunt (POS), Modern Point Of Sale (MPOS), callcenter of Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d64a8-107">Configuration of Point of sale (POS), Modern point of sale (MPOS), call center, or Dynamics 365 Commerce</span></span>
- <span data-ttu-id="d64a8-108">Het PSP-referentienummer (Payment Service Provider) van Adyen (bijvoorbeeld als u vragen hebt over afwijzingen, waaronder handmatige sleutelinvoer \[MKE\]-afwijzingen)</span><span class="sxs-lookup"><span data-stu-id="d64a8-108">The Adyen payment service provider (PSP) reference number (for example, if you have questions about refusals, including manual key entry \[MKE\] refusals)</span></span>
- <span data-ttu-id="d64a8-109">Alles wat niet werkt in test- of live verkopersomgevingen</span><span class="sxs-lookup"><span data-stu-id="d64a8-109">Anything that isn't working in test or live merchant environments</span></span>

## <a name="resolution"></a><span data-ttu-id="d64a8-110">Oplossing</span><span class="sxs-lookup"><span data-stu-id="d64a8-110">Resolution</span></span>

<span data-ttu-id="d64a8-111">Gebruik de volgende e-mailsjabloon om het ondersteuningsproces met het Adyen-team te starten.</span><span class="sxs-lookup"><span data-stu-id="d64a8-111">Use the following email template to start the support process with the Adyen team.</span></span> <span data-ttu-id="d64a8-112">Zorg ervoor dat het e-mailbericht alle vereiste gegevens bevat om het probleem sneller op te lossen.</span><span class="sxs-lookup"><span data-stu-id="d64a8-112">To expedite troubleshooting, make sure that the email contains all the required details.</span></span>

| <span data-ttu-id="d64a8-113">Veld</span><span class="sxs-lookup"><span data-stu-id="d64a8-113">Field</span></span>        | <span data-ttu-id="d64a8-114">Waarde</span><span class="sxs-lookup"><span data-stu-id="d64a8-114">Value</span></span> |
|--------------|-------|
| <span data-ttu-id="d64a8-115">T/m</span><span class="sxs-lookup"><span data-stu-id="d64a8-115">To</span></span>           | `support@adyen.com` |
| <span data-ttu-id="d64a8-116">CC</span><span class="sxs-lookup"><span data-stu-id="d64a8-116">Cc</span></span>           | |
| <span data-ttu-id="d64a8-117">Onderwerpregel</span><span class="sxs-lookup"><span data-stu-id="d64a8-117">Subject line</span></span> | <span data-ttu-id="d64a8-118">Ondersteuningsaanvraag Microsoft Dynamics</span><span class="sxs-lookup"><span data-stu-id="d64a8-118">Microsoft Dynamics Support Request</span></span> |
| <span data-ttu-id="d64a8-119">Hoofdtekst</span><span class="sxs-lookup"><span data-stu-id="d64a8-119">Body</span></span>         | <p><span data-ttu-id="d64a8-120">Hallo ondersteuning,</span><span class="sxs-lookup"><span data-stu-id="d64a8-120">Hi Support,</span></span></p><p><span data-ttu-id="d64a8-121">Wij vragen om ondersteuning voor het volgende probleem:</span><span class="sxs-lookup"><span data-stu-id="d64a8-121">Please provide support for the following issue:</span></span></p><ul><li><span data-ttu-id="d64a8-122">Verkoperrekening</span><span class="sxs-lookup"><span data-stu-id="d64a8-122">Merchant account</span></span></li><li><span data-ttu-id="d64a8-123">Omgeving (Test/Prod)</span><span class="sxs-lookup"><span data-stu-id="d64a8-123">Environment (Test/Prod)</span></span></li><li><span data-ttu-id="d64a8-124">Kanaal (POS/callcenter/Commerce e-commerce)</span><span class="sxs-lookup"><span data-stu-id="d64a8-124">Channel (POS/call center/Commerce e-commerce)</span></span></li><li><span data-ttu-id="d64a8-125">PSP-referentienummer als het probleem een specifieke transactie bevat (U kunt het PSP-referentienummer vinden op het ontvangstbewijs, in het Adyen-klantengebied of in het transactiemenu op de POS-terminal.)</span><span class="sxs-lookup"><span data-stu-id="d64a8-125">PSP reference number, if the issue involved a specific transaction (You can find the PSP reference number on the receipt, in the Adyen Customer Area, or on the transactions menu on the POS terminal.)</span></span></li><li><span data-ttu-id="d64a8-126">Schermopname of foto van het foutbericht, indien van toepassing</span><span class="sxs-lookup"><span data-stu-id="d64a8-126">Screenshot or photo of the error message, if applicable</span></span></li><li><span data-ttu-id="d64a8-127">Logboeken van gebeurtenisviewer (in .txt-indeling)</span><span class="sxs-lookup"><span data-stu-id="d64a8-127">Event Viewer logs (in .txt format)</span></span></li><li><span data-ttu-id="d64a8-128">Beschrijving van het probleem en de probleemoplossingsstappen die u hebt geprobeerd uit te voeren</span><span class="sxs-lookup"><span data-stu-id="d64a8-128">Description of the issue and troubleshooting steps that you've tried</span></span></li></ul> |

## <a name="additional-resources"></a><span data-ttu-id="d64a8-129">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="d64a8-129">Additional resources</span></span>

[<span data-ttu-id="d64a8-130">Betalingen met de Adyen-connector accepteren voor Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d64a8-130">Accept payments with the Adyen connector for Dynamics 365 Commerce</span></span>](https://www.adyen.com/partners/dynamics-365-commerce)

[<span data-ttu-id="d64a8-131">Dynamics 365-betalingsconnector voor Adyen</span><span class="sxs-lookup"><span data-stu-id="d64a8-131">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="d64a8-132">De Adyen-betalingsconnector voor Dynamics 365 instellen</span><span class="sxs-lookup"><span data-stu-id="d64a8-132">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
