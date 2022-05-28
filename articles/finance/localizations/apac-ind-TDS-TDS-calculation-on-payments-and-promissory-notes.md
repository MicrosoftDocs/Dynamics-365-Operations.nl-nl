---
title: TDS-berekening op betalingen en promessen
description: Dit onderwerp biedt naslaginformatie over de verschillende betalingstransacties waarop TDS (belasting ingehouden op bron) wordt berekend.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 7f38a8c4b0416abb10bfdaf95c3379e964e9a41e
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726457"
---
# <a name="tds-calculation-on-payments-and-promissory-notes"></a>TDS-berekening op betalingen en promessen

[!include [banner](../includes/banner.md)]

Dit onderwerp biedt naslaginformatie over de verschillende betalingstransacties waarop TDS (belasting ingehouden op bron) wordt berekend.

| Serienummer | Transactietype | Transactiebedrag | Paginanaam en -pad | Rekeningtype en type tegenrekening |
|---------------|------------------|--------------------|--------------------|--------------------------------------|
| 1             | Voorschot/betaling tegen factuur (TDS te betalen) | Debet of Credit | <ul><li>Algemeen journaal (**Grootboek \> Journaalboekingen \> Algemene journalen**)</li><li>Facturenjournaal (**Leveranciers \> Facturen \> Facturenjournaal**)</li><li>Betalingsjournaal (**Leveranciers \> Betalingen \> Journaal met betalingen van leverancier**)</li></ul> | Leverancier (debet), bank (credit) |
| 2             | Voorschot/betaling tegen factuur (inkoop van klant - TDS te betalen) | Debet of Credit | <ul><li>Algemeen journaal (**Grootboek \> Journaalboekingen \> Algemene journalen**)</li><li>Facturenjournaal (**Leveranciers \> Facturen \> Facturenjournaal**)</li><li>Betalingsjournaal (**Leveranciers \> Betalingen \> Journaal met betalingen van leverancier**)</li></ul> | Klant (debet), bank (credit) |
| 3             | Promessen | Debet | Journaal met getrokken promessen (**Leveranciers \> Betalingen \> Promessen \> Journaal met getrokken promessen**) | Leverancier (debet), grootboek (credit) |
| 4             | Diverse inkomsten (TDS te ontvangen) | Debet of Credit | Algemeen journaal (**Grootboek \> Journaalboekingen \> Algemene journalen**) | Bank (debet), grootboek (credit) |
| 5             | Overige onkosten (TDS te betalen) | Debet of Credit | Algemeen journaal (**Grootboek \> Journaalboekingen \> Algemene journalen**) | Bank (debet), grootboek (credit) |

Volg deze stappen om TDS te berekenen voor betalingen en promessen.

1. Maak journaalregels op de journaalpagina's. Selecteer het rekeningtype en het tegenrekeningtype.
2. Selecteer **Functies \> Vereffening** om de pagina **Bewerken als openstaande transactie** te openen. Selecteer vervolgens een specifieke factuur die moet worden vereffend. Als TDS al op factuurniveau is berekend, geeft het veld **Oorsprong van bedrag** het basisbedrag waarop TDS is berekend. In het veld **TDS-bedrag** staat het TDS-bedrag dat voor de transactie is berekend. In het veld **Bedrag** staat het nettobetalingsbedrag. Dit is dus het betalingsbedrag nadat TDS is ingehouden.

    > [!NOTE]
    > Voor een betaling die tegen een factuur is gedaan, gelden de volgende voorwaarden:
    >
    > - Als het betalingsbedrag en het factuurbedrag hetzelfde zijn, wordt TDS niet berekend als dit al op factuurniveau is berekend.
    > - Als het factuurbedrag na inhouding van het TDS-bedrag hoger is dan het betalingsbedrag, wordt TDS niet berekend.
    > - Als het factuurbedrag na inhouding van het TDS-bedrag lager is dan het betalingsbedrag, wordt TDS berekend over het bedrag dat hoger is dan het factuurbedrag.

3. Controleer of wijzig op de pagina **Journaalboekstuk** op het tabblad **Overzicht** in het veld **TDS-groepen** de standaard-TDS-groep die voor de leverancier of klant is gedefinieerd. TDS die op journaalregels wordt berekend, is gebaseerd op de formule die is gedefinieerd voor de TDS-belastingcodes in de TDS-groep.

    > [!NOTE]
    > TDS wordt alleen berekend als de optie **Bronbelasting berekenen** is ingesteld op **Ja** voor de leverancier op de pagina **Leveranciers**.

4. Op het tabblad **Belastinginformatie** kunt u in de sectie **Bedrijfsgegevens** in het veld **Naam** een bedrijfsnaam selecteren voor alternatieve adressen die voor het bedrijf zijn ingesteld.

    In de sectie **Bronbelasting** wordt in het veld **Soort belastingplichtige** de soort belastingplichtige weergegeven waar de leverancier of klant toe hoort. In het veld **Belastingrekeningnummer (TAN)** staat het belastingrekeningnummer van het geselecteerde bedrijf.

5. Selecteer **Bronbelastingknop \> bronbelasting** om de pagina **Tijdelijke bronbelastingtransacties** te openen. Het bovenste deel van deze pagina heeft de volgende velden:

    - **Totaalbedrag bronbelasting**: het totale TDS-bedrag dat voor de transactie voor de TDS-groep is berekend.
    - **Waarde** het totale percentage dat is gebruikt om TDS voor de transactie te berekenen. Het totale percentage is gebaseerd op de formule die is gedefinieerd voor de TDS-belastingcodes en is gekoppeld aan de TDS-groep.
    - **Totaal gecorrigeerd bronbelastingbedrag**: het totale gecorrigeerde TDS-bedrag voor alle belastingcodes in de TDS-groep.
    - **TDS**: een ingeschakeld selectievakje geeft aan dat er een TDS-groep aan de transactie is gekoppeld.

    De velden op de tabbladen **Overzicht**, **Algemeen** en **Correctie** geven het berekende TDS-bedrag en details weer van het gecorrigeerde TDS-bedrag voor elke TDS-belastingcode die aan de TDS-groep is gekoppeld.

6. Selecteer **Drempel** om de pagina **Drempel** te openen, waar u de drempellimiet kunt bekijken die is gedefinieerd voor de TDS-belastingcomponent die aan een specifieke TDS-belastingcode is gekoppeld.
7. Selecteer **Formuleontwerper** om de pagina **Formuleontwerper** te openen. Hier kunt u de formule bekijken die voor een specifieke TDS-belastingcode is gedefinieerd.
8. Sluit de pagina's **Formuleontwerper** en **Tijdelijke bronbelastingtransacties** om terug te keren naar de pagina **Journaalboekstuk**.
9. Valideer en boek het journaal. Het TDS-bedrag dat is berekend, wordt geboekt naar de te betalen rekening die is gedefinieerd voor elke TDS-belastingcode in de TDS-groep. De klantenrekeningen voor TDS-belastingcodes worden gedefinieerd op de pagina **Bronbelastingcodes**.
10. Selecteer **Bronbelasting geboekt** om de pagina **Bronbelastingtransacties** te openen. In het veld **Waarde** wordt het totale percentage weergegeven dat is gebruikt om TDS voor de transactie te berekenen.

    De velden op de tabbladen **Overzicht**, **Algemeen** en **Bedrag** geven de TDS-bedragen weer die zijn berekend voor de TDS-groep die aan de transactie is gekoppeld.

11. Controleer de TDS-berekeningsgegevens voor elke TDS-belastingcode die aan de TDS-groep is gekoppeld.

## <a name="generate-payments"></a>Betalingen genereren

Volg deze stappen om betalingen te genereren:

1. Volg één van deze stappen:

    - Ga naar **Leveranciers \> Betalingen \> Journaal met betalingen van leverancier**.
    - Ga naar **Klanten \> Betalingen \> Journaal met betalingen van klant**.
    - Ga naar **Leveranciers \> Betalingen \> Promessen \> Journaal met getrokken promessen**.
    - Ga naar **Klanten \> Betalingen \> Wissel \> Journaal met getrokken wissels**.
    - Ga naar **Klanten \> Betalingen \> Wissel \> Journaal met hertrokken wissels**.

2. Selecteer **Regels**
3. Selecteer **Functies \> Betalingen genereren**.
