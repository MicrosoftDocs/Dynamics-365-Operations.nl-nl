---
title: Verwijzingen naar oorspronkelijke facturen in creditnota's
description: In dit artikel wordt uitgelegd hoe u de oorspronkelijke factuurnummers in gerelateerde creditnota's kunt instellen en afdrukken.
author: mrolecki
ms.date: 10/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.search.form: ''
ms.openlocfilehash: f1f9ca3914aa02cc38ddfe9f8dd88eb7fc88fd4b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281230"
---
# <a name="references-to-original-invoices-in-credit-notes"></a>Verwijzingen naar oorspronkelijke facturen in creditnota's

[!include [banner](../includes/banner.md)]


In sommige landen en regio's is er een wettelijke vereiste dat afgedrukte creditnota's verwijzingen naar de oorspronkelijke facturen bevatten. In dit artikel wordt uitgelegd hoe u de oorspronkelijke factuurnummers in gerelateerde creditnota's kunt instellen en afdrukken.

## <a name="prerequisites"></a>Vereisten

- Schakel in de werkruimte **Functiebeheer** de functie **Creditfactuurindeling voor verkoop- en projectfactuurrapporten** in. Zie [Overzicht van functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) voor meer informatie.
- De afdrukbare indelingen van de vereiste documenten moeten in Afdrukbeheer worden geconfigureerd.

De functionaliteit die in dit artikel wordt beschreven, is van toepassing op de volgende documenten:

**Klanten**

- Vrije-tekstcreditnota
- Creditnota van de klant

**Projectbeheer en boekhouding**

- Creditnota van project

## <a name="configure-accounts-receivable-parameters"></a>De parameters van Klanten configureren

Volg deze stappen om de parameter in te stellen die bepaalt of verwijzingen naar de oorspronkelijke facturen worden afgedrukt in gerelateerde creditnota's.

1. Ga naar **Klanten** \> **Instellen** \> **Parameters van module Klanten**.
2. Stel op het tabblad **Updates** op het sneltabblad **Factuur** de optie **Creditfactuurindeling toepassen op verkoop- en projectfactuurrapporten** in op **Ja**.

![De parameters van Klanten configureren.](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a>Verwijzingen naar oorspronkelijke facturen definiëren

Gebruik de volgende procedures om verwijzingen naar oorspronkelijke facturen te definiëren op basis van het documenttype.

### <a name="free-text-credit-note"></a>Vrije-tekstcreditnota

1. Ga naar **Klanten** \> **Facturen** \> **Alle vrije-tekstfacturen**.
2. Maak een nieuwe creditnota of selecteer een bestaande creditnota.
3. Open de factuur.
4. Selecteer in het actievenster op het tabblad **Factuur** in de groep **Functies** de optie **Factuurcreditering**.
5. Voer de verwijzing naar de oorspronkelijke factuur in en selecteer de reden voor de correctie.

![De verwijzing voor een vrije-tekstfactuur definiëren.](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a>Creditnota van de klant

1. Ga naar **Klanten** \> **Orders** \> **Alle verkooporders**.
2. Selecteer en open de gefactureerde verkooporder die moet worden gecorrigeerd.
3. Ga in het actievenster naar het tabblad **Verkopen** in de groep **Creditnota** en klik op **Creditnota**.
4. Voer de reden voor de correctie in. De verwijzing naar de oorspronkelijke factuur wordt automatisch gemaakt.

![De verwijzing voor een verkooporder definiëren.](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a>Creditnota van project

1. Ga naar **Projectbeheer en boekhouding** \> **Projectfacturen** \> **Projectfacturen**.
2. Selecteer en open de projectfactuur die moet worden gecorrigeerd.
3. Selecteer in het actievenster op het tabblad **Projectfactuur** in de groep **Functies** de optie **Selecteren voor creditnota**.
4. Selecteer **Factuurcreditering**.
5. Voer de reden voor de correctie in. De verwijzing naar de oorspronkelijke factuur wordt automatisch gemaakt.

![De verwijzing voor een projectfactuur definiëren.](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a>Creditnota's afdrukken

Wanneer u vrije tekst, klanten en projectcreditnota's afdrukt, bevatten deze de verwijzing naar de oorspronkelijke factuur en de reden van de correctie.

![Afgedrukte creditnota.](media/credit-note-FTI.jpg)

> [!NOTE]
> Zorg ervoor dat de afdrukbare indelingen van de documenten correct zijn geconfigureerd, op basis van de veronderstelling dat verwijzingen naar oorspronkelijke facturen worden afgedrukt.

## <a name="references-to-original-invoices-in-debit-notes"></a>Verwijzingen naar oorspronkelijke facturen in debetnota's

Standaard kunnen verwijzingen naar oorspronkelijke facturen worden ingevoerd voor creditnota's. U kunt bijvoorbeeld verwijzingen invoeren wanneer u negatieve (afnemende) correcties van oorspronkelijke facturen maakt.

Als u verwijzingen wilt invoeren wanneer u positieve (verhogende) correcties van oorspronkelijke facturen maakt, moet u de functie **Verwijzingen naar oorspronkelijke facturen in debetnota's** in de werkruimte **Functiebeheer** inschakelen.  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
