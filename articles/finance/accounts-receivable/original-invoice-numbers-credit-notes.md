---
title: Verwijzingen naar oorspronkelijke facturen in creditnota's
description: In dit onderwerp wordt uitgelegd hoe u de oorspronkelijke factuurnummers in gerelateerde creditnota's kunt instellen en afdrukken.
author: ilkond
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 673288f04b33aa2a578f9e2e7913dbe7ac309644
ms.sourcegitcommit: 7cdec5469ff0da145ac4e01caf3287d0627ae2dc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2021
ms.locfileid: "5099997"
---
# <a name="references-to-original-invoices-in-credit-notes"></a>Verwijzingen naar oorspronkelijke facturen in creditnota's

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

In sommige landen en regio's is er een wettelijke vereiste dat afgedrukte creditnota's verwijzingen naar de oorspronkelijke facturen bevatten. In dit onderwerp wordt uitgelegd hoe u de oorspronkelijke factuurnummers in gerelateerde creditnota's kunt instellen en afdrukken.

## <a name="prerequisites"></a>Vereisten

- Schakel in de werkruimte **Functiebeheer** de functie **Creditfactuurindeling voor verkoop- en projectfactuurrapporten** in. Zie [Overzicht van functiebeheer](../../fin-and-ops/get-started/feature-management/feature-management-overview.md) voor meer informatie.
- De afdrukbare indelingen van de vereiste documenten moeten in Afdrukbeheer worden geconfigureerd.

De functionaliteit die in dit onderwerp wordt beschreven, is van toepassing op de volgende documenten:

**Klanten**

- Vrije-tekstcreditnota
- Creditnota van de klant

**Projectbeheer en boekhouding**

- Creditnota van project

## <a name="configure-accounts-receivable-parameters"></a>De parameters van Klanten configureren

Volg deze stappen om de parameter in te stellen die bepaalt of verwijzingen naar de oorspronkelijke facturen worden afgedrukt in gerelateerde creditnota's.

1. Ga naar **Klanten** \> **Instellen** \> **Parameters van module Klanten**.
2. Stel op het tabblad **Updates** op het sneltabblad **Factuur** de optie **Creditfactuurindeling toepassen op verkoop- en projectfactuurrapporten** in op **Ja**.

![De parameters van Klanten configureren](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a>Verwijzingen naar oorspronkelijke facturen definiëren

Gebruik de volgende procedures om verwijzingen naar oorspronkelijke facturen te definiëren op basis van het documenttype.

### <a name="free-text-credit-note"></a>Vrije-tekstcreditnota

1. Ga naar **Klanten** \> **Facturen** \> **Alle vrije-tekstfacturen**.
2. Maak een nieuwe creditnota of selecteer een bestaande creditnota.
3. Open de factuur.
4. Selecteer in het actievenster op het tabblad **Factuur** in de groep **Functies** de optie **Factuurcreditering**.
5. Voer de verwijzing naar de oorspronkelijke factuur in en selecteer de reden voor de correctie.

![De verwijzing voor een vrije-tekstfactuur definiëren](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a>Creditnota van de klant

1. Ga naar **Klanten** \> **Orders** \> **Alle verkooporders**.
2. Selecteer en open de gefactureerde verkooporder die moet worden gecorrigeerd.
3. Ga in het actievenster naar het tabblad **Verkopen** in de groep **Creditnota** en klik op **Creditnota**.
4. Voer de reden voor de correctie in. De verwijzing naar de oorspronkelijke factuur wordt automatisch gemaakt.

![De verwijzing voor een verkooporder definiëren](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a>Creditnota van project

1. Ga naar **Projectbeheer en boekhouding** \> **Projectfacturen** \> **Projectfacturen**.
2. Selecteer en open de projectfactuur die moet worden gecorrigeerd.
3. Selecteer in het actievenster op het tabblad **Projectfactuur** in de groep **Functies** de optie **Selecteren voor creditnota**.
4. Selecteer **Factuurcreditering**.
5. Voer de reden voor de correctie in. De verwijzing naar de oorspronkelijke factuur wordt automatisch gemaakt.

![De verwijzing voor een projectfactuur definiëren](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a>Creditnota's afdrukken

Wanneer u vrije tekst, klanten en projectcreditnota's afdrukt, bevatten deze de verwijzing naar de oorspronkelijke factuur en de reden van de correctie.

![Afgedrukte creditnota](media/credit-note-FTI.jpg)

> [!NOTE]
> Zorg ervoor dat de afdrukbare indelingen van de documenten correct zijn geconfigureerd, op basis van de veronderstelling dat verwijzingen naar oorspronkelijke facturen worden afgedrukt.
