---
title: Betalingen worden automatisch vereffend voordat orders worden gefactureerd of verzonden
description: Dit artikel bevat richtlijnen voor probleemoplossing die u kunnen helpen wanneer een betaling in de Adyen-portal direct na het plaatsen van een order wordt vereffend, zelfs als de verkooporder nog niet is gefactureerd of verzonden.
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
ms.openlocfilehash: 6fdaf48600edc22b5423e0167177616758e2dc6e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282702"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a>Betalingen worden automatisch vereffend voordat orders worden gefactureerd of verzonden

[!include [banner](../../includes/banner.md)]

Dit artikel bevat richtlijnen voor probleemoplossing die u kunnen helpen wanneer een betaling in de Adyen-portal direct na het plaatsen van een order wordt vereffend, zelfs als de verkooporder nog niet is gefactureerd of verzonden.

## <a name="description"></a>Beschrijving

Nadat een order is geplaatst, wordt de betaling onmiddeld vereffend in de Adyen-portal, zelfs als de verkooporder nog niet is gefactureerd of verzonden.

## <a name="resolution"></a>Oplossing

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a>Handmatig vastleggen voor e-commercebetalingen configureren in de Adyen-portal

Voer de volgende stappen uit als u het handmatig vastleggen voor e-commercebetalingen wilt configureren in de Adyen-portal.

1. Meld u aan bij de Adyen-portal.
1. Selecteer in de rechterbovenhoek uw verkoperrekening voor het e-commercekanaal.
1. Selecteer op de bovenste navigatiebalk **Rekening** en vervolgens **Instellingen**.
1. Selecteer in het veld **Vertraging vastleggen** de optie **handmatig**.

    ![Instelling voor vertraging vastleggen in de Adyen-portal.](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a>Aanvullende bronnen

[Adyen-betaling vastleggen](https://docs.adyen.com/point-of-sale/capturing-payments)

[Dynamics 365 Payment Connector voor Adyen](../dev-itpro/adyen-connector.md)

[De Adyen-betalingsconnector voor Dynamics 365 instellen](https://docs.adyen.com/plugins/microsoft-dynamics)
