---
title: Restitutie voor een retourorder wordt geweigerd
description: Dit onderwerp bevat richtlijnen voor probleemoplossing die u kunnen helpen als een restitutie voor een retourorder wordt afgewezen omdat de creditcard die wordt gebruikt voor facturering, verschilt van de kaart die is gebruikt tijdens de oorspronkelijke betalingsautorisatie.
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
ms.openlocfilehash: e202c6b4b9e025d5af1cd5eb6235884aab6444e6
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585273"
---
# <a name="refund-on-a-return-order-is-declined"></a><span data-ttu-id="e48e3-103">Restitutie voor een retourorder wordt geweigerd</span><span class="sxs-lookup"><span data-stu-id="e48e3-103">Refund on a return order is declined</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e48e3-104">Dit onderwerp bevat richtlijnen voor probleemoplossing die u kunnen helpen als een restitutie voor een retourorder wordt afgewezen omdat de creditcard die wordt gebruikt voor facturering, verschilt van de kaart die is gebruikt tijdens de oorspronkelijke betalingsautorisatie.</span><span class="sxs-lookup"><span data-stu-id="e48e3-104">This topic provides troubleshooting guidance that can help when a refund on a return order is declined because the credit card that is used for invoicing differs from the card that was used during the original payment authorization.</span></span>

## <a name="description"></a><span data-ttu-id="e48e3-105">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="e48e3-105">Description</span></span>

<span data-ttu-id="e48e3-106">Een restitutie wordt afgewzen wanneer de creditcard die wordt gebruikt voor het factureren van een retourorder, afwijkt van de kaart die is gebruikt tijdens de oorspronkelijke betalingsautorisatie.</span><span class="sxs-lookup"><span data-stu-id="e48e3-106">A refund is declined when the credit card that is used to invoice a return order differs from the card that was used during the original payment authorization.</span></span> <span data-ttu-id="e48e3-107">Het volgende foutbericht wordt weergegeven: 'Sommige betalingen hebben niet de juiste status voor boeking.</span><span class="sxs-lookup"><span data-stu-id="e48e3-107">You receive the following error message: "Some payments are not in the correct status for posting.</span></span> <span data-ttu-id="e48e3-108">Valideer de status van alle betalingen opnieuw voordat u factureert.'</span><span class="sxs-lookup"><span data-stu-id="e48e3-108">Please re-validate the status of all payments prior to invoicing."</span></span>

<span data-ttu-id="e48e3-109">In de details van de betalingsautorisatie wordt het volgende foutbericht weergegeven: 'SendRequest() van Adyen-gateway is mislukt met de status 'InternalServerError'.22144; Leeg antwoord van Adyen.(22001);'</span><span class="sxs-lookup"><span data-stu-id="e48e3-109">The payment authorization details will include the following error message: "Adyen gateway SendRequest() failed with status 'InternalServerError'.22144; Empty response returned from Adyen.(22001);"</span></span>

![Fout waardoor restitutie voor een retourorder wordt geweigerd](media/refund-order-decline.jpg)

## <a name="resolution"></a><span data-ttu-id="e48e3-111">Oplossing</span><span class="sxs-lookup"><span data-stu-id="e48e3-111">Resolution</span></span>

### <a name="enable-blind-returns-in-adyen"></a><span data-ttu-id="e48e3-112">Blinde retourzendingen inschakelen in Adyen</span><span class="sxs-lookup"><span data-stu-id="e48e3-112">Enable blind returns in Adyen</span></span>

<span data-ttu-id="e48e3-113">Als u blinde retourzendingen wilt inschakelen, volgt u de stappen in [Problemen met Dynamics 365-betalingsconnector voor Adyen oplossen](adyen-support.md) om contact op te nemen met het Adyen-ondersteuningsteam en het inschakelen van blinde retourzendingen aan te vragen voor uw Adyen-verkopersaccount.</span><span class="sxs-lookup"><span data-stu-id="e48e3-113">To enable blind returns, follow the steps in [Troubleshoot Dynamics 365 Payment Connector for Adyen issues](adyen-support.md) to contact the Adyen support team and request that blind returns be enabled on your Adyen merchant account.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e48e3-114">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="e48e3-114">Additional resources</span></span>

[<span data-ttu-id="e48e3-115">Dynamics 365-betalingsconnector voor Adyen</span><span class="sxs-lookup"><span data-stu-id="e48e3-115">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="e48e3-116">De Adyen-betalingsconnector voor Dynamics 365 instellen</span><span class="sxs-lookup"><span data-stu-id="e48e3-116">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
