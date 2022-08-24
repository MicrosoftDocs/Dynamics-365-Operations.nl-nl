---
title: Afgedrukte klantfacturen met hashnummers archiveren
description: In dit artikel wordt uitgelegd hoe u archivering kunt inschakelen om afgedrukte klantfacturen met hekjes op te slaan.
author: mrolecki
ms.date: 09/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.custom: 539093
ms.search.form: ''
ms.openlocfilehash: 4c9bd7ead1615a4e6b0e8e672e858312ba518b56
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291664"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a>Afgedrukte klantfacturen met hashnummers archiveren

[!include [banner](../includes/banner.md)]

In sommige landen is het wettelijk verplicht om berekende hekjes in het systeem op te slaan, samen met afdrukken van bepaalde documenten. Hekjes kunnen worden gebruikt voor rapportage aan instanties en tijdens audits.

In dit artikel wordt uitgelegd hoe u archivering kunt configureren om afgedrukte klantfacturen met hekjes op te slaan.

## <a name="prerequisites"></a>Vereisten

- Schakel in de werkruimte **Functiebeheer** de functie **Afgedrukte klantfacturen met hekjes archiveren** in. Zie [Overzicht van functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) voor meer informatie.
- Configureer de afdrukbare indelingen van vereiste documenten **Afdrukbeheer**.

Deze functionaliteit is van toepassing op de volgende documenten.

**Klanten**
- Klantfactuur
- Creditnota van de klant
- Vrije-tekstfactuur
- Vrije-tekstcreditnota

**Projectbeheer en boekhouding**
- Projectfactuur
- Creditnota van project

## <a name="configure-customer-master-data"></a>Klanthoofdgegevens configureren
Voer de volgende stappen uit om de klantgegevens te configureren en schakel de mogelijkheid in om afgedrukte facturen automatisch als bijlagen op te slaan.

1. Ga naar **Klanten** > **Alle klanten**. 
2. Selecteer een klant en selecteer op het sneltabblad **Factuur en levering** in de sectie **E-FACTUUR** in het veld **eInvoice-bijlage** de optie **Ja**.

## <a name="print-invoices"></a>Facturen afdrukken
U kunt elke vrije tekst-, klant- en projectfactuur of creditnota boeken en afdrukken voor de klant die in de vorige procedure is geconfigureerd.

Open de pagina **Bijlagen** voor de afgedrukte factuur. Zoek op het sneltabblad **Bijlage** in de veldgroep **Aanvullende details** in het veld **Hekje voor document** het opgeslagen hekje op dat is berekend voor de afgedrukte factuur.

![Hekje voor bijlage.](media/attach-hash-num.jpg)

