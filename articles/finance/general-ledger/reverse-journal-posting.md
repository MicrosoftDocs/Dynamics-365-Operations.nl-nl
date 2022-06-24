---
title: Journaalboekingen tegenboeken
description: Dit artikel beschrijft mogelijkheden waarmee u boekstukken kunt tegenboeken uit de lijst met boekstuktransacties of vanuit financiële journalen.
author: kweekley
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: roschloma
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bec7d5d0dd64a2d89b00e2aa630a4fe670feaa2b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868397"
---
# <a name="reverse-journal-posting"></a>Journaalboekingen tegenboeken

[!include [banner](../includes/banner.md)]

In dit artikel worden mogelijkheden van Microsoft Dynamics 365 Finance beschreven waarmee u een volledig journaal kunt terugboeken of een of meer boekstukken kunt terugboeken uit de lijst met boekstuktransacties, ongeacht de oorsprong. 

Voordat u een van de in dit artikel beschreven functies kunt gebruiken, moet u deze in het systeem inschakelen. Beheerders kunnen het werkgebied **Functiebeheer** gebruiken om de status van de functie te controleren en desgewenst in te schakelen. De functie wordt daar op de volgende manier weergegeven:
 - Module: Grootboek
 - Functienaam: **massaal omkeringen voor meerdere documenten**

## <a name="reversing-journals"></a>Journalen tegenboeken

U kunt journaalregels afzonderlijk tegenboeken. Bij het terugdraaien van journaalboekingen kunt u ook een heel financieel journaal tegenboeken. Een journaal tegenboeken: 

- Filteren op de geboekte journalen en de weergave **Regels** van het journaal openen.
- Selecteer het menu **Terugboeken** bovenaan de pagina.
- Het totale aantal boekstukken en boekstukregels wordt weergegeven, evenals het totale bedrag van de regels die worden teruggeboekt
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

- Selecteer het vervolgkeuzemenu **Geheel journaal terugboeken** bovenaan de pagina.
- Het totale aantal boekstukken en boekstukregels wordt weergegeven, evenals het totale bedrag van de regels die worden teruggeboekt
- Selecteer **Ja** als u de bestaande transactiedatums wilt gebruiken of **Nee** als u een nieuwe transactiedatum wilt invoeren. In sommige gevallen wordt de periode van de oorspronkelijke transactie afgesloten en moet u een nieuwe transactiedatum invoeren om de transactie terug te boeken.
- Als u **Nee** selecteert, voert u een transactiedatum voor de terugboeking in. 
- Voer een opmerking in om de terugboektransactie te beschrijven.
- Selecteer de knop **Terugboeken**.

De transacties worden teruggeboekt. 

Als er meer dan 100 terugboekregels zijn, wordt het terugboekproces uitgevoerd met behulp van het batchproces. U kunt de resultaten controleren door de opmerkingen in de batchtaak te bekijken. Transacties die niet kunnen worden teruggeboekt, worden opgenomen in de historie van de batchtaak.

Als het aantal boekstukregels 100 regels of minder bedraagt, wordt het terugboekproces onmiddellijk uitgevoerd. De resultaten worden weergegeven in een dialoogvenster waarin een boekstuk dat niet kon worden teruggeboekt, wordt weergegeven met de reden waarom het niet kon worden teruggeboekt. Selecteer **OK** om het dialoogvenster te sluiten.

Transacties kunnen alleen worden teruggeboekt als ze voldoen aan de bedrijfsregels voor het terugboeken ervan. Leveranciersbetalingen kunnen niet worden teruggeboekt met de functie die in dit artikel wordt beschreven. Leveranciersbetalingen moeten worden teruggeboekt door de stappen te volgen in [Een leveranciersbetaling terugboeken](../accounts-payable/reverse-vendor-payment.md).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
