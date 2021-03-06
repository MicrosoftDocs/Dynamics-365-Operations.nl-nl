---
title: Afgedrukte klantfacturen met hashnummers archiveren
description: In dit onderwerp wordt uitgelegd hoe u archivering kunt inschakelen om afgedrukte klantfacturen met hekjes op te slaan.
author: ilyako
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 841e6059f5b0d70dbd1fe12a1f8910bbb31ddc86
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018973"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a>Afgedrukte klantfacturen met hashnummers archiveren

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

In sommige landen is het wettelijk verplicht om berekende hekjes in het systeem op te slaan, samen met afdrukken van bepaalde documenten. Hekjes kunnen worden gebruikt voor rapportage aan instanties en tijdens audits.

In dit onderwerp wordt uitgelegd hoe u archivering kunt configureren om afgedrukte klantfacturen met hekjes op te slaan.

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

![Hekje voor bijlage](media/attach-hash-num.jpg)

