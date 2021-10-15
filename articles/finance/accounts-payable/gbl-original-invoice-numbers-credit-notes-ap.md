---
title: Verwijzen naar oorspronkelijke facturen in creditnota's (leveranciersfacturen)
description: In dit onderwerp wordt beschreven hoe u een verwijzing naar een oorspronkelijke factuur maakt wanneer u een creditnota maakt.
author: v-oloski
ms.date: 09/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-oloski
ms.search.validFrom: 2021-09-23
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6114ffb4d3b9e942887cbfa10c6039b0d73af7e1
ms.sourcegitcommit: 86f0574363fb869482ef73ff294f345f81d17c5b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7562221"
---
# <a name="reference-original-invoices-in-credit-notes-vendor-invoices"></a>Verwijzen naar oorspronkelijke facturen in creditnota's (leveranciersfacturen)

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een verwijzing naar een oorspronkelijke factuur maakt wanneer u een creditnota maakt.

## <a name="prerequisites"></a>Vereisten

Schakel in de werkruimte **Functiebeheer** de functie **Factuurcreditering inschakelen voor leveranciersfacturen** in. Zie [Overzicht van functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) voor meer informatie.

De functionaliteit die in dit onderwerp wordt beschreven, is van toepassing op de volgende bedrijfsdocumenten:

**Leveranciers:**

- Inkooporder
- Factuurjournaal
- Factuurregister

**Grootboek:**

- Algemeen journaal

## <a name="define-a-reference-to-an-original-invoice"></a>Een verwijzing naar een oorspronkelijke factuur definiëren

Gebruik de volgende procedures om een verwijzing naar een oorspronkelijke factuur te definiëren op basis van het documenttype.

### <a name="vendor-credit-note-purchase-order"></a>Creditnota van leverancier (inkooporder)

1. Ga naar **Leveranciers** \> **Inkooporders** \> **Alle inkooporders**.
2. Maak een nieuwe inkooporder maken of gebruik een bestaande inkooporder om een creditnota te maken.
3. Selecteer in het actievenster op het tabblad **Factuur** in de groep **Introduceren** de optie **Factuurcreditering**.
4. Voer de reden voor de correctie de verwijzing naar de oorspronkelijke factuur in.

### <a name="vendor-credit-note-ledger-journals"></a>Creditnota van leverancier (grootboekjournalen)

1. Volg één van deze stappen:

    - Ga naar **Leveranciers** \> **Factuurjournalen**.
    - Ga naar **Leveranciers** \> **Facturenregister**.
    - Ga naar **Grootboek** \> **Journaalboekingen** \> **Algemene journalen**.

2. Maak een nieuw journaal en nieuwe journaalregels.
3. Selecteer in het actievenster **Functies** \> **Factuurcreditering**.
4. Voer de reden voor de correctie de verwijzing naar de oorspronkelijke factuur in.

> [!NOTE]
> De opdracht **Factuurcreditering** is zichtbaar in een algemeen journaalboekstuk als het veld **Rekeningtype** is ingesteld op **Leverancier**.
