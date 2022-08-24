---
title: Op de pagina met de creditcardinvoer wordt een fout weergegeven bij het uitchecken
description: Dit artikel bevat richtlijnen voor probleemoplossing die u kunnen helpen als de sectie Betalingsmethode niet wordt geladen en er een foutbericht wordt weergegeven.
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
ms.openlocfilehash: 25f0dde83efff7c1d9a2a456270f5d48047f44ba
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269750"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a>Op de pagina met de creditcardinvoer wordt een fout weergegeven bij het uitchecken

[!include [banner](../../includes/banner.md)]

Dit artikel bevat richtlijnen voor probleemoplossing die u kunnen helpen als de sectie **Betalingsmethode** niet wordt geladen en er een foutbericht wordt weergegeven.

## <a name="description"></a>Beschrijving

Wanneer u de uitcheckpagina van een online winkel opent, wordt de sectie **Betalingsmethode** niet geladen en wordt het volgende foutbericht weergegeven: 'Er is een fout opgetreden. Probeer het later opnieuw.'

![Fout in betalingsmodule.](media/payment-module-error.jpg)

## <a name="resolution"></a>Oplossing

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a>Wacht tot de cache van Commerce Scale Unit verloopt

De instellingen voor de betalingsservice op de uitcheckpagina van de online winkel worden in de cache opgeslagen op de Commerce Scale Unit, en het kan tot 15 minuten duren voordat deze op de e-commercesite wordt weergegeven. Deze instellingen van de betalingsservice omvatten wijzigingen in de verkopersrekening-id, de cloud-API-sleutel en verschillende configuratie-instellingen die aan de betalingsmethode zijn gerelateerd.

## <a name="additional-resources"></a>Aanvullende bronnen

[Een online afzetkanaal instellen](../channel-setup-online.md)
