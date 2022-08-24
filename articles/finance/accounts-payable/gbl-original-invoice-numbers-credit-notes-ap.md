---
title: Verwijzen naar oorspronkelijke facturen in creditnota's (leveranciersfacturen)
description: In dit artikel wordt beschreven hoe u een verwijzing naar een oorspronkelijke factuur maakt wanneer u een creditnota maakt.
author: AdamTrukawka
ms.date: 09/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2021-09-23
ms.dyn365.ops.version: 10.0.20
ms.search.form: ''
ms.openlocfilehash: ed07ae9784da3ca721fcb25a9c5a14c4f75f2e59
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277365"
---
# <a name="reference-original-invoices-in-credit-notes-vendor-invoices"></a>Verwijzen naar oorspronkelijke facturen in creditnota's (leveranciersfacturen)

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u een verwijzing naar een oorspronkelijke factuur maakt wanneer u een creditnota maakt.

## <a name="prerequisites"></a>Vereisten

Schakel in de werkruimte **Functiebeheer** de functie **Factuurcreditering inschakelen voor leveranciersfacturen** in. Zie [Overzicht van functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) voor meer informatie.

De functionaliteit die in dit artikel wordt beschreven, is van toepassing op de volgende bedrijfsdocumenten:

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
