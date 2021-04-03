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
# <a name="refund-on-a-return-order-is-declined"></a>Restitutie voor een retourorder wordt geweigerd

[!include [banner](../../includes/banner.md)]

Dit onderwerp bevat richtlijnen voor probleemoplossing die u kunnen helpen als een restitutie voor een retourorder wordt afgewezen omdat de creditcard die wordt gebruikt voor facturering, verschilt van de kaart die is gebruikt tijdens de oorspronkelijke betalingsautorisatie.

## <a name="description"></a>Beschrijving

Een restitutie wordt afgewzen wanneer de creditcard die wordt gebruikt voor het factureren van een retourorder, afwijkt van de kaart die is gebruikt tijdens de oorspronkelijke betalingsautorisatie. Het volgende foutbericht wordt weergegeven: 'Sommige betalingen hebben niet de juiste status voor boeking. Valideer de status van alle betalingen opnieuw voordat u factureert.'

In de details van de betalingsautorisatie wordt het volgende foutbericht weergegeven: 'SendRequest() van Adyen-gateway is mislukt met de status 'InternalServerError'.22144; Leeg antwoord van Adyen.(22001);'

![Fout waardoor restitutie voor een retourorder wordt geweigerd](media/refund-order-decline.jpg)

## <a name="resolution"></a>Oplossing

### <a name="enable-blind-returns-in-adyen"></a>Blinde retourzendingen inschakelen in Adyen

Als u blinde retourzendingen wilt inschakelen, volgt u de stappen in [Problemen met Dynamics 365-betalingsconnector voor Adyen oplossen](adyen-support.md) om contact op te nemen met het Adyen-ondersteuningsteam en het inschakelen van blinde retourzendingen aan te vragen voor uw Adyen-verkopersaccount.

## <a name="additional-resources"></a>Aanvullende bronnen

[Dynamics 365-betalingsconnector voor Adyen](../dev-itpro/adyen-connector.md)

[De Adyen-betalingsconnector voor Dynamics 365 instellen](https://docs.adyen.com/plugins/microsoft-dynamics)
