---
title: Fout Betalingstype moet creditcard zijn op de verkooporderpagina
description: Dit onderwerp bevat richtlijnen voor probleemoplossing die u kunnen helpen als een foutbericht wordt weergegeven op de verkooporderpagina nadat een order is gesynchroniseerd.
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
ms.openlocfilehash: 20f18507dee330fd1affedeee092b3dfa7cc10bc
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585268"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a>Fout 'Betalingstype moet creditcard zijn' op de verkooporderpagina

[!include [banner](../../includes/banner.md)]

Dit onderwerp bevat richtlijnen voor probleemoplossing die u kunnen helpen als een foutbericht wordt weergegeven op de verkooporderpagina nadat een order is gesynchroniseerd.

## <a name="description"></a>Beschrijving

Wanneer u de verkooporderpagina opent nadat u een order hebt gesynchroniseerd, wordt het volgende foutbericht weergegeven: 'Het betalingstype moet creditcard zijn, omdat het creditcardnummer is opgegeven'.

![Fout Betalingstype moet een creditcard zijn](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a>Oplossing

### <a name="set-the-payment-type-in-commerce-headquarters"></a>Het betalingstype instellen in Commerce Headquarters

1. Ga naar **Klanten \> Betalingsinstelling \> Betalingstermijnen**.
1. Selecteer in de linkernavigatie uw betalingsvoorwaarden.
1. Controleer in het veld **Betalingstype** of **Creditcard** is geselecteerd.

## <a name="additional-resources"></a>Aanvullende bronnen

[Online verkopen en betalingen boeken](../tasks/posting-online-sales-payments.md)