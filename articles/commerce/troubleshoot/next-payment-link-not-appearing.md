---
title: Opslaan voor mijn volgende betalingsoptie wordt niet weergegeven
description: Dit onderwerp biedt richtlijnen voor probleemoplossing die u kunnen helpen wanneer het selectievakje Opslaan voor mijn volgende betaling niet wordt weergegeven onder Betalingsmethode op de uitcheckpagina van een e-commercesite.
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
ms.openlocfilehash: 3a4fbcd522651ed1b82b72b751ff6ead44c94a71
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585269"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a>Optie 'Opslaan voor mijn volgende betaling' wordt niet weergegeven

[!include [banner](../../includes/banner.md)]

Dit onderwerp biedt richtlijnen voor probleemoplossing die u kunnen helpen wanneer het selectievakje **Opslaan voor mijn volgende betaling** niet wordt weergegeven onder **Betalingsmethode** op de uitcheckpagina van een e-commercesite.

## <a name="description"></a>Beschrijving

Het selectievakje **Opslaan voor mijn volgende betaling** wordt niet weergegeven in de sectie **Betalingsmethode** op de uitcheckpagina van een e-commercesite.

In de volgende afbeelding ziet u een voorbeeld van een uitcheckpagina met het selectievakje **Opslaan voor mijn volgende betaling**.

![Selectievakje Opslaan voor mijn volgende betaling in de module Betaling](media/payment-module-save-payment.jpg)

## <a name="resolution"></a>Oplossing

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a>Controleren of de Dynamics 365-betalingsconnector voor Adyen correct is geconfigureerd in Commerce Headquarters

Voer deze stappen uit om te controleren of de Dynamics 365-betalingsconnector voor Adyen correct is geconfigureerd in Commerce Headquarters.

1. Ga naar **Retail en Commerce \> Afzetkanalen \> Online winkels**.
1. Selecteer de online winkel.
1. Zorg ervoor op het sneltabblad **Betalingsrekeningen** dat het veld **Opslaan van betalingsgegevens toestaan in e-commerce** is ingesteld op **Waar**.

![Het opslaan van betalingsgegevens toestaan in veld e-commerce in Commerce Headquarters](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a>Aanvullende bronnen

[Betalingsmodule](../payment-module.md)

[Online betaalmiddelen opslaan met de Adyen-connector](../dev-itpro/adyen-connector-listPI.md)