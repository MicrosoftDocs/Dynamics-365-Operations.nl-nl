---
title: Fout Betalingstype moet creditcard zijn op de verkooporderpagina
description: Dit artikel bevat richtlijnen voor probleemoplossing die u kunnen helpen als een foutbericht wordt weergegeven op de verkooporderpagina nadat een order is gesynchroniseerd.
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
ms.openlocfilehash: 71c5cbaf574866c74e222f4d67132004327db8fe
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285627"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a>Fout 'Betalingstype moet creditcard zijn' op de verkooporderpagina

[!include [banner](../../includes/banner.md)]

Dit artikel bevat richtlijnen voor probleemoplossing die u kunnen helpen als een foutbericht wordt weergegeven op de verkooporderpagina nadat een order is gesynchroniseerd.

## <a name="description"></a>Beschrijving

Wanneer u de verkooporderpagina opent nadat u een order hebt gesynchroniseerd, wordt het volgende foutbericht weergegeven: 'Het betalingstype moet creditcard zijn, omdat het creditcardnummer is opgegeven'.

![Fout Betalingstype moet een creditcard zijn.](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a>Oplossing

### <a name="set-the-payment-type-in-commerce-headquarters"></a>Het betalingstype instellen in Commerce Headquarters

1. Ga naar **Klanten \> Betalingsinstelling \> Betalingstermijnen**.
1. Selecteer in de linkernavigatie uw betalingsvoorwaarden.
1. Controleer in het veld **Betalingstype** of **Creditcard** is geselecteerd.

## <a name="additional-resources"></a>Aanvullende bronnen

[Online verkopen en betalingen boeken](../tasks/posting-online-sales-payments.md)
