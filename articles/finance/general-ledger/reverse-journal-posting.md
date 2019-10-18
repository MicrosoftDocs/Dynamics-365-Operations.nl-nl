---
title: Journaalboekingen tegenboeken
description: Dit onderwerp beschrijft mogelijkheden waarmee u boekstukken kunt tegenboeken uit de lijst met boekstuktransacties of vanuit financiële journalen.
author: MikeFalkner
manager: AnnBe
ms.date: 08/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a5456e60f1f3cee5f83ac7f725f7e01ba5bd7a1
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248580"
---
# <a name="reverse-journal-posting"></a>Journaalboekingen tegenboeken

[!include [banner](../includes/banner.md)]

In dit onderwerp worden Microsoft Dynamics 365 Finance-mogelijkheden beschreven waarmee u een volledig journaal kunt tegenboeken of een of meer boekstukken kunt tegenboeken uit de lijst met boekstuktransacties, ongeacht de oorsprong. 

## <a name="reversing-journals"></a>Journalen tegenboeken

U kunt journaalregels afzonderlijk tegenboeken. Bij het terugdraaien van journaalboekingen kunt u ook een heel financieel journaal tegenboeken. Een journaal tegenboeken: 
- Open het financiële journaal en filter op geboekte journalen
- Klik op het menu Tegenboeken bovenaan de pagina
- Het totale aantal boekstukken en boekstukregels wordt weergegeven, evenals het totale bedrag van de regels die worden teruggeboekt.
- Selecteer Ja als u de bestaande transactiedatums wilt gebruiken of Nee als u een nieuwe transactiedatum wilt invoeren. In sommige gevallen wordt de periode van de oorspronkelijke transactie afgesloten en wilt u een nieuwe transactiedatum voor het tegenboeken invoeren.
- Als u Nee hebt geselecteerd, voert u een transactiedatum voor het tegenboeken in. 
- Voer een opmerking invoeren die u wilt toevoegen aan de tegenboektransactie
- Klik op de knop Tegenboeken.

De transacties worden teruggeboekt. 

Als het aantal boekstukregels hoger is dan 100 regels, wordt het tegenboekproces uitgevoerd met het batchproces. U kunt de resultaten van de tegenboeking bekijken door de opmerkingen in de batchtaak te bekijken die is uitgevoerd. Alle fouten worden vastgelegd in de historie van de batchtaak.

Als het aantal boekstukregels 100 regels of minder bedraagt, wordt het tegenboekproces onmiddellijk uitgevoerd. De resultaten worden weergegeven in een dialoogvenster waarin een boekstuk wordt weer gegeven dat niet kan worden teruggeboekt, en de reden waarom het niet kan worden teruggeboekt. Klik OK om het dialoogvenster te sluiten.

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a>Boekstukken tegenboeken vanuit de lijst met boekstuktransacties. 

U kunt ook boekstukken omkeren uit de **Lijst met boekstuktransacties** in alle subadministraties. Daarnaast kunt u meerdere boekstukken tegelijk tegenboeken. 

Een of meer boekstukken tegenboeken: 
- Klik op het menu Tegenboeken bovenaan de pagina
- Het totale aantal boekstukken en boekstukregels wordt weergegeven, evenals het totale bedrag van de regels die worden teruggeboekt.
- Selecteer Ja als u de bestaande transactiedatums wilt gebruiken of Nee als u een nieuwe transactiedatum wilt invoeren. In sommige gevallen wordt de periode van de oorspronkelijke transactie afgesloten en wilt u een nieuwe transactiedatum voor het tegenboeken invoeren.
- Als u Nee hebt geselecteerd, voert u een transactiedatum voor het tegenboeken in. 
- Voer een opmerking invoeren die u wilt toevoegen aan de tegenboektransactie
- Klik op de knop Tegenboeken.

De transacties worden teruggeboekt. 

Als het aantal boekstukregels hoger is dan 100 regels, wordt het tegenboekproces uitgevoerd met het batchproces. U kunt de resultaten van de tegenboeking bekijken door de opmerkingen in de batchtaak te bekijken die is uitgevoerd. Alle fouten worden vastgelegd in de historie van de batchtaak.

Als het aantal boekstukregels 100 regels of minder bedraagt, wordt het tegenboekproces onmiddellijk uitgevoerd. De resultaten worden weergegeven in een dialoogvenster waarin een boekstuk wordt weer gegeven dat niet kan worden teruggeboekt, en de reden waarom het niet kan worden teruggeboekt. Klik OK om het dialoogvenster te sluiten.

