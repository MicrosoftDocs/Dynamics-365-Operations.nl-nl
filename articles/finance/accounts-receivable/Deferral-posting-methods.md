---
title: Boekingsmethoden voor uitstel
description: In dit artikel worden de verschillen beschreven tussen de boekingsmethoden voor uitstel voor de uitstel van opbrengsten en onkosten in Facturering van abonnementen.
author: JodiChristiansen
ms.date: 6/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: c66ed1c38251140dd798c39797873ceb5f7121a4
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/15/2022
ms.locfileid: "9019093"
---
# <a name="deferral-posting-methods"></a>Boekingsmethoden voor uitstel

In dit artikel worden de verschillen beschreven tussen de boekingsmethoden voor uitstel voor de uitstel van opbrengsten en onkosten in Facturering van abonnementen.

Op de pagina **Uitstelparameters voor opbrengsten en onkosten** zijn de opties voor boekingsmethoden voor uitstel **Balans** en **Winst en verlies**. In het voorbeeld in dit artikel worden de verschillen tussen de twee methoden uitgelegd en worden de redenen gegeven waarom u de ene of de andere methode kan gebruiken.

Bij de methode **Balans** worden slechts twee rekeningen gebruikt. Er zijn dus minder instellingen nodig. Bij de methode **Winst en verlies** worden de twee extra rekeningen **Initiële toerekening** en **Tegenrekening voor toerekening** gebruikt voor opbrengst, kortingen en kosten, afhankelijk van het transactietype. Deze rekeningen worden ingesteld op de pagina **Standaardwaarden voor uitstel** (**Facturering van abonnementen \> Uitstel van opbrengsten en onkosten \> Instellen**). Hoewel het voorbeeld is gericht op uitgestelde opbrengsten, kan hetzelfde concept worden toegepast op uitgestelde kortingen en uitgestelde kosten.

## <a name="example"></a>Voorbeeld

Verkoopfactuur 1 heeft een totaal van € 3000 en heeft uitgestelde opbrengst. In de volgende tabellen worden de verdelingen weergegeven wanneer deze verkoopfactuur wordt geboekt.

**Methode Balans**

| Type | Rekening | Debet | Credit|
|---|---|---|---|
| Debet | Debiteuren | 3,000.00 | |
| Credit | Uitgestelde opbrengst | | 3,000.00 |

**Methode Winst en verlies**

| Type | Rekening | Debet | Credit |
|---|---|---|---|
| Debet | Debiteuren | 3,000.00 | |
| Debet | Tegenrekening voor toerekening van opbrengst | 3,000.00 | |
| Credit | Uitgestelde opbrengst | | 3,000.00 |
| Credit | Ongeldige opbrengsttoerekening | | 3,000.00 |

Verkoopfactuur 2 heeft een totaal van € 2000 en heeft geen uitgestelde opbrengst.

| Type | Rekening | Bedrag |
|---|---|---|
| Debet | Debiteuren | 3,000.00 |
| Credit | Omzet | 3,000.00 |

**Totalen van de methode Balans voor verkoopfactuur 1 en 2 bij elkaar**

| Rekening | Debet | Credit |
|---|---|---|
| Debiteuren | 5.000,00 | |
| Omzet | | 2,000.00 |
| Uitgestelde opbrengst | | 3,000.00 |

Wanneer de methode **Balans** wordt gebruikt, is het niet zo eenvoudig om de bruto-opbrengst voor een periode te zien. Een deel van de opbrengts wordt geboekt naar de rekening **Uitgestelde opbrengst**. Omdat er elke periode opbrengst wordt toegrekend, bevinden zich meerdere debet- en creditbedragen op de rekening **Uitgestelde opbrengst**. De bruto-opbrengst voor een bepaalde periode wordt gecombineerd met de debet- en creditbedragen van opbrengsttoerekening.

**Totalen van de methode Winst en verlies voor verkoopfactuur 1 en 2 bij elkaar**

| Rekening | Debet | Credit |
|---|---|---|
| Debiteuren | 5.000,00 | |
| Omzet | | 5.000,00 |
| Tegenrekening opbrengst | 3,000.00 | |
| Uitgestelde opbrengst | | 3,000.00 |

Alle opbrengsten gaan naar de winst-en-verliesrekening **Opbrengst**. Vervolgens wordt de uitgestelde opbrengst van het winst- en verliesoverzicht naar de balans verplaatst. Ukunt de bruto-opbrengst eenvoudig nekijken, omdat alles naar de rekening **Opbrengst** wordt geboekt. Een deel van deze bruto-opbrengst wordt echter uitgesteld. Daarom wordt deze verplaatst naar de rekening **Uitgestelde opbrengst** en later toegerekend.

In de methode **Winst en verlies** kunt u naar de rekeningen **Opbrengst** en **Tegenrekening opbrengst** kijken voor de bruto-opbrengst van € 5000 en netto-opbrengst (netto van uitgesteld) van € 2000. Hoewel de methode **Winst en verlies** rapporteren eenvoudiger kan maken, moet u meer rekeningen instellen.
