---
title: Problemen met Dynamics 365-betalingsconnector voor Adyen oplossen
description: Dit artikel bevat richtlijnen voor probleemoplossing die u kunnen helpen ondersteuning te krijgen bij problemen met de Microsoft Dynamics 365-betalingsconnector voor Adyen.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 687f2fdff5e29cc25fae911b015164f0d90aee88
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268860"
---
# <a name="troubleshoot-dynamics-365-payment-connector-for-adyen-issues"></a>Problemen met Dynamics 365-betalingsconnector voor Adyen oplossen

[!include [banner](../../includes/banner.md)]

Dit artikel bevat richtlijnen voor probleemoplossing die u kunnen helpen ondersteuning te krijgen bij problemen met de Microsoft Dynamics 365-betalingsconnector voor Adyen.

## <a name="description"></a>Beschrijving

U hebt problemen met de Dynamics 365-betalingsonnector voor Adyen in de volgende gebieden en u hebt ondersteuning nodig van het Adyen-team:

- Configuratie van verkooppunt (POS), Modern Point Of Sale (MPOS), callcenter of Dynamics 365 Commerce
- Het PSP-referentienummer (Payment Service Provider) van Adyen (bijvoorbeeld als u vragen hebt over afwijzingen, waaronder handmatige sleutelinvoer \[MKE\]-afwijzingen)
- Alles wat niet werkt in test- of live verkopersomgevingen

## <a name="resolution"></a>Oplossing

Gebruik de volgende e-mailsjabloon om het ondersteuningsproces met het Adyen-team te starten. Zorg ervoor dat het e-mailbericht alle vereiste gegevens bevat om het probleem sneller op te lossen.

| Veld        | Waarde |
|--------------|-------|
| T/m           | `support@adyen.com` |
| CC           | |
| Onderwerpregel | Ondersteuningsaanvraag Microsoft Dynamics |
| Hoofdtekst         | <p>Hallo ondersteuning,</p><p>Wij vragen om ondersteuning voor het volgende probleem:</p><ul><li>Verkoperrekening</li><li>Omgeving (Test/Prod)</li><li>Kanaal (POS/callcenter/Commerce e-commerce)</li><li>PSP-referentienummer als het probleem een specifieke transactie bevat (U kunt het PSP-referentienummer vinden op het ontvangstbewijs, in het Adyen-klantengebied of in het transactiemenu op de POS-terminal.)</li><li>Schermopname of foto van het foutbericht, indien van toepassing</li><li>Logboeken van gebeurtenisviewer (in .txt-indeling)</li><li>Beschrijving van het probleem en de probleemoplossingsstappen die u hebt geprobeerd uit te voeren</li></ul> |

## <a name="additional-resources"></a>Aanvullende bronnen

[Betalingen met de Adyen-connector accepteren voor Dynamics 365 Commerce](https://www.adyen.com/partners/dynamics-365-commerce)

[Dynamics 365-betalingsconnector voor Adyen](../dev-itpro/adyen-connector.md)

[De Adyen-betalingsconnector voor Dynamics 365 instellen](https://docs.adyen.com/plugins/microsoft-dynamics)
