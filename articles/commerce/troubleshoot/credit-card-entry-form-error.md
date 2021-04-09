---
title: Op de pagina met de creditcardinvoer wordt een fout weergegeven bij het uitchecken
description: Dit onderwerp bevat richtlijnen voor probleemoplossing die u kunnen helpen als de sectie Betalingsmethode niet wordt geladen en er een foutbericht wordt weergegeven.
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
ms.openlocfilehash: f0751fc76e6eb4320f766886b4c1efcb1042e996
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585262"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a>Op de pagina met de creditcardinvoer wordt een fout weergegeven bij het uitchecken

[!include [banner](../../includes/banner.md)]

Dit onderwerp bevat richtlijnen voor probleemoplossing die u kunnen helpen als de sectie **Betalingsmethode** niet wordt geladen en er een foutbericht wordt weergegeven.

## <a name="description"></a>Beschrijving

Wanneer u de uitcheckpagina van een online winkel opent, wordt de sectie **Betalingsmethode** niet geladen en wordt het volgende foutbericht weergegeven: 'Er is een fout opgetreden. Probeer het later opnieuw.'

![Fout in betalingsmodule](media/payment-module-error.jpg)

## <a name="resolution"></a>Oplossing

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a>Wacht tot de cache van Commerce Scale Unit verloopt

De instellingen voor de betalingsservice op de uitcheckpagina van de online winkel worden in de cache opgeslagen op de Commerce Scale Unit, en het kan tot 15 minuten duren voordat deze op de e-commercesite wordt weergegeven. Deze instellingen van de betalingsservice omvatten wijzigingen in de verkopersrekening-id, de cloud-API-sleutel en verschillende configuratie-instellingen die aan de betalingsmethode zijn gerelateerd.

## <a name="additional-resources"></a>Aanvullende bronnen

[Een online afzetkanaal instellen](../channel-setup-online.md)