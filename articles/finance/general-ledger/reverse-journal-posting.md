---
title: Journaalboekingen tegenboeken
description: Dit onderwerp beschrijft mogelijkheden waarmee u boekstukken kunt tegenboeken uit de lijst met boekstuktransacties of vanuit financiële journalen.
author: MikeFalkner
manager: AnnBe
ms.date: 10/08/2019
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
ms.openlocfilehash: bc2ff30ef5d08759af700d683c207b0f5ed65d5b
ms.sourcegitcommit: 574309903f15eeab7911091114885b5c7279d22a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/24/2019
ms.locfileid: "2658968"
---
# <a name="reverse-journal-posting"></a>Journaalboekingen tegenboeken

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit onderwerp worden mogelijkheden van Microsoft Dynamics 365 Finance beschreven waarmee u een volledig journaal kunt terugboeken of een of meer boekstukken kunt terugboeken uit de lijst met boekstuktransacties, ongeacht de oorsprong. 

## <a name="reversing-journals"></a>Journalen tegenboeken

U kunt journaalregels afzonderlijk tegenboeken. Bij het terugdraaien van journaalboekingen kunt u ook een heel financieel journaal tegenboeken. Een journaal tegenboeken: 

- Open het financiële journaal en filter op geboekte journalen.
- Selecteer het menu **Terugboeken** bovenaan de pagina.
- Het totale aantal boekstukken en boekstukregels wordt weergegeven, evenals het totale bedrag van de regels die worden teruggeboekt.
- Selecteer **Ja** als u de bestaande transactiedatums wilt gebruiken of **Nee** als u een nieuwe transactiedatum wilt invoeren. In sommige gevallen wordt de periode van de oorspronkelijke transactie afgesloten en moet u een nieuwe transactiedatum voor de terugboeking invoeren.
- Als u **Nee** selecteert, voert u een transactiedatum voor de terugboeking in. 
- Voer een opmerking in die u aan de terugboektransactie wilt toevoegen.
- Selecteer de knop **Terugboeken**.

De transacties worden teruggeboekt. 

Als het boekstuk meer dan 100 regels bevat, wordt het terugboekproces uitgevoerd met behulp van het batchproces. U kunt de resultaten controleren door de opmerkingen in de batchtaak te bekijken. Transacties die niet kunnen worden teruggeboekt, worden weergegeven in de historie van de batchtaak.

Als het boekstuk 100 regels of minder bevat, wordt het terugboekproces onmiddellijk uitgevoerd. De resultaten worden weergegeven in een dialoogvenster waarin een boekstuk dat niet kon worden teruggeboekt, wordt weergegeven met de reden waarom het niet kon worden teruggeboekt. Selecteer **OK** om het dialoogvenster te sluiten.

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a>Boekstukken tegenboeken vanuit de lijst met boekstuktransacties. 

U kunt ook boekstukken omkeren uit de **Lijst met boekstuktransacties** in alle subadministraties. Daarnaast kunt u meerdere boekstukken tegelijk tegenboeken. 

Een of meer boekstukken tegenboeken: 

- Selecteer het menu **Terugboeken** bovenaan de pagina
- Het totale aantal boekstukken en boekstukregels wordt weergegeven, evenals het totale bedrag van de regels die worden teruggeboekt
- Selecteer **Ja** als u de bestaande transactiedatums wilt gebruiken of **Nee** als u een nieuwe transactiedatum wilt invoeren. In sommige gevallen wordt de periode van de oorspronkelijke transactie afgesloten en moet u een nieuwe transactiedatum invoeren om de transactie terug te boeken.
- Als u **Nee** selecteert, voert u een transactiedatum voor de terugboeking in. 
- Voer een opmerking in om de terugboektransactie te beschrijven.
- Selecteer de knop **Terugboeken**.

De transacties worden teruggeboekt. 

Als er meer dan 100 terugboekregels zijn, wordt het terugboekproces uitgevoerd met behulp van het batchproces. U kunt de resultaten controleren door de opmerkingen in de batchtaak te bekijken. Transacties die niet kunnen worden teruggeboekt, worden opgenomen in de historie van de batchtaak.

Als het aantal boekstukregels 100 regels of minder bedraagt, wordt het terugboekproces onmiddellijk uitgevoerd. De resultaten worden weergegeven in een dialoogvenster waarin een boekstuk dat niet kon worden teruggeboekt, wordt weergegeven met de reden waarom het niet kon worden teruggeboekt. Selecteer **OK** om het dialoogvenster te sluiten.

Transacties kunnen alleen worden teruggeboekt als ze voldoen aan de bedrijfsregels voor het terugboeken ervan. Leveranciersbetalingen kunnen niet worden teruggeboekt met de functie die in dit onderwerp wordt beschreven. Leveranciersbetalingen moeten worden teruggeboekt door de stappen te volgen in [Een leveranciersbetaling terugboeken](https://docs.microsoft.com/en-us/dynamics365/finance/accounts-payable/reverse-vendor-payment).

