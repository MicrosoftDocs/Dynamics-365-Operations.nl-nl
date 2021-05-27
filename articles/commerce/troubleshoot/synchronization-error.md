---
title: Fout bij ordersynchronisatie in verband met de standaardbetalingsservice
description: Dit onderwerp bevat richtlijnen voor probleemoplossing die u kunnen helpen bij het oplossen van een fout die kan optreden als een online order wordt gesynchroniseerd.
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
ms.openlocfilehash: fa174bbb257379f6ce906dd21180bbcb19f8bc3f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021122"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a>Fout bij ordersynchronisatie in verband met de standaardbetalingsservice

[!include [banner](../../includes/banner.md)]

Dit onderwerp bevat richtlijnen voor probleemoplossing die u kunnen helpen bij het oplossen van een fout die kan optreden als een online order wordt gesynchroniseerd.

## <a name="description"></a>Beschrijving

Wanneer u een online order synchroniseert, wordt het volgende foutbericht weergegeven: 'Er moet een standaardbetalingsservice zijn voor het verwerken van creditcardtransacties'.

![Fout door ontbrekende standaardbetalingsservice](media/default-payment-method-error.jpg)

## <a name="resolution"></a>Oplossing

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a>De standaardbetalingsservice bevestigen of instellen in Commerce Headquarters

Voer de volgende stappen uit om de standaardbetalingsservice te bevestigen of in te stellen in Commerce Headquarters.

1. Ga naar **Leveranciers \> Instelling van betalingen \> Betalingsservice**.
1. Zorg ervoor dat de optie **Standaardverwerker voor de nieuwe creditcard** is ingesteld op **Ja** voor één betalingsservice.

## <a name="additional-resources"></a>Aanvullende bronnen

[Instelling, autorisatie en registratie van creditcards](../../finance/accounts-receivable/credit-card-authorizations.md)