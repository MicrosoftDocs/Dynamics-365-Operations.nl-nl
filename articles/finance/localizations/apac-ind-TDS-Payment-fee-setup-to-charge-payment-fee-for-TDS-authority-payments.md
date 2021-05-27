---
title: Bijzondere betalingskosten instellen voor betalingen aan een TDS-dienst
description: In dit onderwerp wordt uitgelegd hoe u bijzondere betalingskosten moet instellen die worden berekend voor de belasting die wordt ingehouden op de bron (TDS).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: b52331bb1c7a1bc2c764008112f3df9cc0385995
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023163"
---
# <a name="set-up-payment-fees-for-tds-authority-payments"></a>Bijzondere betalingskosten instellen voor betalingen aan een TDS-dienst

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u bijzondere betalingskosten moet instellen die worden berekend voor de belasting die wordt ingehouden op de bron (TDS).

1. Ga naar **Leveranciers \> Betalingsinstelling \> Bijzondere betalingskosten**.

    [![Pagina Bijzondere betalingskosten](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)

2. Selecteer **Nieuw** om bijzondere betalingskosten te maken en voer de vereiste gegevens in.
3. Selecteer het type bijzondere betalingskosten in het veld **Type bijzondere kosten**:

    - **None**
    - **Rente**: rente wordt in rekening gebracht over te late betalingen die zijn gedaan aan de TDS-dienstleverancier.
    - **Andere**: overige kosten worden in rekening gebracht over te late betalingen die zijn gedaan aan de TDS-dienstleverancier.

    Als u **Rente** of **Andere** selecteert, wordt het veld **Toeslag** automatisch ingesteld op **Grootboek**.

4. Als u **Rente** of **Andere** in het veld **Veldtype** hebt geselecteerd, selecteert u in het veld **Hoofdrekening** de grootboekrekening waar u de rente of andere toeslagen naar wilt boeken.
5. Voer de andere vereiste gegevens in.
6. Selecteer in het actievenster **Instellingen van bijzondere betalingskosten** om de pagina **Instellingen van bijzondere betalingskosten** te openen, waar u bijzondere betalingskosten kunt instellen voor verschillende combinaties van banken, betalingsmethoden, betalingsspecificaties, valuta's en datumintervallen.

    [![Pagina Instellingen van bijzondere betalingskosten](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)

7. Geef op het tabblad **Overzicht** in het veld **Groeperingen** op voor welke banken u de bijzondere betalingskosten wilt instellen:

    - **Tabel**: de bijzondere betalingskosten gelden voor een specifieke bankrekening.
    - **Groep**: de betalingskosten gelden voor een specifieke bankgroep.
    - **Alle**: de bijzondere betalingskosten gelden voor alle bankrekeningen.

8. Als u **Tabel** of **Groep** hebt geselecteerd in het veld **Groeperingen**, selecteert u in het veld **Bankrelatie** de specifieke bankrekening of bankgroep waar u de bijzondere betalingskosten voor in wilt stellen.
9. In het veld **Betalingsmethode** selecteert u de betalingsmethode die u wilt gebruiken voor betaling van bijzondere betalingskosten.
10. Selecteer in het veld **Betalingsspecificatie** de betalingsspecificatiecode die is gegenereerd op de pagina **Betalingsspecificatie**.
    - De betalingsspecificatie wordt gebruikt met de betalingsmethoden van EFT (Electronic Funds Transfer).
12. Selecteer in het veld **Betalingsvaluta** de valuta die de bijzondere betalingskosten activeert. Alleen transacties die de geselecteerde valuta gebruiken, kunnen de bijzondere kosten activeren. Als u dit veld leeg laat, worden de bijzondere kosten door alle valuta's geactiveerd.
13. Selecteer de berekeningsmethode in het veld **Percentage/bedrag**. De opties zijn **Bedrag**, **Percentage** en **Interval**.
14. Geef in het veld **Bedrag van bijzondere kosten** het bedrag van de bijzondere kosten op als een percentage van de betaling of als het bedrag voor één betaling.
15. Selecteer in het veld **Valuta van kosten** de valutacode voor de bijzondere kosten op.
16. Selecteer op het tabblad **Algemeen** om de details voor de geselecteerde bankrekening weer te geven of te wijzigen.

    [![Tabblad Algemeen](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)

16. Voer in het veld **Minimum** het minimumtransactiebedrag in dat de bijzondere kosten activeert.
17. Voer in het veld **Maximum** het maximumtransactiebedrag in dat de bijzondere kosten activeert.
18. Definieer in de velden **Begindatum** en **Einddatum** een datumbereik voor het berekenen van de bijzondere kosten.
19. Geef in het veld **Minimale bijzondere kosten** het bedrag van de bijzondere kosten op als een percentage van de betaling of als het bedrag voor één betaling.
20. Selecteer in het veld **Btw-groep** de btw-groep die u wilt gebruiken om de btw voor het bedrag van de bijzondere kosten te berekenen.
21. Selecteer in het veld **Btw-groep voor artikel** de artikel-btw-groep die u wilt gebruiken om de artikel-btw voor het bedrag van de bijzondere kosten te berekenen.
22. Selecteer het tabblad **Interval**. 

    [![Tabblad Interval](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)

23. Voer in het veld **Dagen** het aantal dagen in tussen de boekingsdatum (kortingsdatum) van de betaling en de vervaldatum van de promesse.
24. Selecteer in het veld **Percentage/bedrag** of de specificatie een percentage of een ingesteld bedrag is.
25. Voer in het veld **Minimale bijzondere kosten** het bedrag in van de bijzondere kosten als een percentage van de betaling of als het bedrag voor één betaling.
26. Sluit de pagina **Instellingen van bijzondere betalingskosten**.
27. Sluit de pagina **Bijzondere betalingskosten**.
