---
title: TDS-betalingen vereffenen met TDS-instantieleveranciers en Challan voor TDS genereren
description: In dit artikel wordt uitgelegd hoe u TDS-betalingen (Tax Afgetrokken belasting) kunt vereffenen met leveranciers van de TDS-dienst.
author: kailiang
ms.date: 03/12/2021
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
ms.openlocfilehash: e1ee65a555193433e6712a8caa892d7a3ad7bf61
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848505"
---
# <a name="settle-tds-payments-to-tds-authority-vendors-and-generate-tds-challan"></a>TDS-betalingen vereffenen met TDS-instantieleveranciers en Challan voor TDS genereren

[!include [banner](../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u TDS-betalingen (Tax Afgetrokken belasting) kunt vereffenen met leveranciers van de TDS-dienst.

1. Ga naar **Leveranciers \> Betalingen \> Journaal met betalingen van leverancier**.

    [![Pagina Journaal met betalingen van leverancier.](./media/apac-ind-TDS-51.png)](./media/apac-ind-TDS-51.png)

2. Selecteer **Nieuw** om een journaalregel te maken op de pagina **Journaal met betalingen van leverancier**.
3. Selecteer in het veld **Rekening** de TDS-instantieleverancier waarmee u TDS-betalingen wilt vereffenen.
4. Selecteer **Vereffeningstransacties** om de pagina **Vereffeningstransacties** te openen, waar u de vereffende TDS-transacties kunt weergeven voor de TDS-instantieleverancier.

    De vereffende TDS-transacties voor een vereffeningsperiode worden als volgt weergegeven:

    - TDS-transacties waarbij de soort belastingplichtige **Bedrijf** is, worden weergegeven als één transactieregel.
    - TDS-transacties waarbij de aard van de beoordelaarscategorie **HUF**, **Firma**, **Afzonderlijk**, **AOP**, **BOI**, **Lokale instantie** of **Andere** is, worden weergegeven als één transactieregel.
    - In het veld **Bedrag** staat het totale TDS-bedrag dat aan de TDS-instantieleverancier moet worden betaald.

5. Selecteer **Bronbelastingtransacties** om de verschillende TDS-transacties weer te geven die zijn opgenomen voor de vereffeningsrecord. U kunt op deze pagina het splitsen weergeven van elke TDS-transactie die in het vereffeningsproces voor de vereffeningsperiode is opgenomen.
6. Schakel op het tabblad **Overzicht** het selectievakje **Markeren** in voor de TDS-transacties die u met de TDS-instantieleverancier wilt vereffenen.

    Op het tabblad **Overzicht** wordt de volgende informatie voor elke openstaande TDS-transactie weergegeven:

    - **Date**: de TDS-transactiedatum.
    - **Boekstuk**: het nummer van het boekstuk.
    - **Bron**: de module waarin de TDS-transactie is geboekt.
    - **Leverancier/klant**: het rekeningnummer van de leverancier of klant van wie de TDS wordt ingehouden.
    - **Naam van degene van wie wordt ingehouden (deductee)/partij**: de naam van de leverancier of klant van wie het TDS-bedrag wordt ingehouden.
    - **Soort belastingplichtige**: de soort belastingplichtige waar de deductee bij hoort.
    - **Bedrag**: het factuurbedrag waarover de TDS is berekend.
    - **Belastingbedrag**: het TDS-bedrag dat voor de transactie is berekend.

    > [!NOTE]
    > Schakel het selectievakje **Markeren** uit voor TDS-transacties die niet moeten worden vereffend met de TDS-instantieleverancier.

    Op het tabblad **Algemeen** wordt in het veld **PAN** het permanente rekeningnummer (permanent account number, PAN) van de deductee weergegeven. Het veld **Datum** geeft de datum van de TDS-berekening weer, en in het veld **Waarde** staat het totale percentage dat is gebruikt voor de TDS-berekening.

7. Selecteer **Boekstuk** om de boekstukposten voor de TDS-transactie weer te geven.
8. Sluit de pagina.
10. Selecteer **Bronbelastingcomponenten** om de pagina **Bronbelastingcomponenten** te openen, waar u de TDS kunt bekijken die per TDS-belastingcomponent is berekend voor een specifieke TDS-belastingcode.

    Op het tabblad **Overzicht** staat in het veld **Belastingcomponent** de TDS-belastingcomponent die is gebruikt voor de transactie. In het veld **Bedrag** staat het TDS-bedrag dat is berekend voor de TDS-belastingcomponent in de basisvaluta. Het veld **Samengevoegd bedrag** geeft het totale TDS-bedrag weer dat is berekend voor de TDS-belastingcomponent voor alle vereffende transacties.

    Op het tabblad **Bedrag** staat in de sectie **Standaardvaluta** het TDS-bedrag dat is berekend voor de TDS-belastingcomponent, in de standaardvaluta. In de sectie **Secundaire valuta** ziet u het bedrag in de secundaire valuta.

11. Sluit de pagina **Bronbelastingcomponenten**.
12. Op de pagina **Bewerken als openstaande transactie** in het veld **Bedrag** ziet u dat het totaalbedrag dat met de TDS-instantieleverancier moet worden vereffend voor de vereffeningsperiode is bijgewerkt.
13. Schakel het selectievakje **Markeren** voor de transacties in om de TDS-transacties van verschillende TDS-vereffeningsperioden te vereffenen met de TDS-instantieleverancier.
14. Sluit de pagina **Bewerken als openstaande transactie**.

    > [!NOTE]
    > Als er slechts een paar transacties zijn geselecteerd voor vereffening op de pagina **Bronbelastingtransacties**, wordt het totale TDS-bedrag van de geselecteerde transacties bijgewerkt in het veld **Correctie** op de pagina **Bewerken als openstaande transactie**. Het correctiebedrag wordt bijgewerkt op de journaalregel op de pagina **Journaalboekstuk** en de pagina **Bewerken als openstaande transactie** wordt gesloten.

    Op de pagina **Journaalboekstuk** staat in het veld **Debet** het totaalbedrag dat aan de TDS-instantieleverancier moet worden betaald.

15. De details van de tegenrekening invoeren.

    > [!NOTE]
    > Als TDS-transacties verschillende belastingrekeningnummers hebben, worden er journaalregels gemaakt per belastingrekeningnummer (TAN) op de pagina **Journaalboekstuk**.

16. Selecteer op het tabblad **Bijzondere betalingskosten** in het veld **ID van bijzondere kosten** een kosten-id met het type **Rente** voor de kosten of **Andere** om de betalingskosten in rekening te brengen voor vertraagde betalingen die worden gedaan aan de leverancier van de TDS-dienst.

    Op het tabblad **Belastinginformatie** wordt in de sectie **Bedrijfsgegevens** het veld **Naam** de bedrijfsnaam weergegeven. In de sectie **Bronbelasting** staat in het veld **Belastingrekeningnummer (TAN)** het belastingrekeningnummer dat aan de transactieregel is gekoppeld.

17. Valideer en boek het journaal.
18. Selecteer **Bronbelasting \> Challan-gegevens** om Challan-gegevens in te voeren voor de transactie.

    In het veld **Boekstuk** staat het boekstuknummer van de transactie.
    
19. Schakel het selectievakje **TDS-storting via boekinvoer** in als het TDS-bedrag wordt gestort door middel van boekinvoer.
20. Voer in het veld **Challan-nummer** het Challan-nummer in dat wordt gebruikt om de betaling aan de leverancier van de TDS-dienst uit te voeren.
21. Voer in het veld **Datum** de Challan-datum in.
22. Selecteer in het veld **Banknaam** de naam van de bank waar het TDS-bedrag dat aan de leverancier van de TDS-dienst moet worden betaald, moet worden gestort. Dit veld bevat alle bankrekeningen die zijn ingesteld voor de TDS-leverancier in **Leveranciers \> Alle leveranciers \> Instellen \> Bankrekeningen**.
23. Geef in het veld **BSR-code** de BSR-code (Basic Statistical Return) van de bank op.
24. Sluit de pagina.

### <a name="example"></a>Voorbeeld

De periode 01-04-2009 wordt vereffend voor de TDS-componentgroep **Huur** met behulp van het periodieke TDS-vereffeningsproces. Het totale TDS-bedrag 141.625,00 wordt geboekt naar de rekening van de leverancier van de TDS-dienst voor de TDS-vereffeningsperiode. U kunt dit bedrag weergeven in het veld **Bedrag** op de pagina **Bewerken als openstaande transactie** voor de leverancier van de TDS-dienst.

Als u **Bronbelastingtransacties** selecteert om de verschillende TDS-transacties weer te geven die voor de periode zijn vereffend, worden de volgende gegevens weergegeven.

| TDS-bedrag |
|------------|
| 16,995.00  |
| 22,660.00  |
| 28,325.00  |
| 16,995.00  |
| 28,325.00  |
| 16,995.00  |
| 11,330.00  |

Selecteer **Bronbelastingcomponenten** om de TDS weer te geven voor een bepaald TDS-bedrag dat per TDS-belastingcomponent is berekend voor een specifieke TDS-belastingcode. U selecteert bijvoorbeeld **Bronbelastingcomponenten** voor het te betalen TDS-bedrag 16.995,00. Het belastingbedrag wordt getoond dat per component voor de transactie is berekend.

| Belastingonderdeel | Bedrag    | Samengevoegd bedrag |
|---------------|-----------|--------------------|
| TDS           | 1,5000.00 | 125,000.00         |
| Toeslag     | 1,500.00  | 12,500.00          |
| PE-Cess       | 330.00    | 2,750.00           |
| SHECess      | 165.00    | 1,375.00           |

Als u alleen de TDS-bedragen 16.995,00, 22.660,00, en 2.8325,00 voor vereffening hebt geselecteerd op de pagina **Bronbelastingtransacties**, wordt het totaalbedrag voor vereffening weergegeven als **67.980,00** in het veld **Correctie** op de pagina **Bewerken als openstaande transactie**. Als deze transactie is gemarkeerd voor vereffening en de pagina **Bewerken als openstaande transactie** wordt gesloten, wordt het bedrag **67.980,00** weergegeven in het veld **Debet** op de pagina **Journaalboekstuk**.

U kunt het journaal nu boeken en het Challan voor TDS genereren.

### <a name="adjustment-of-advance-payments-that-are-made-to-tds-authority-vendors"></a>Correctie van voorschotten die worden gedaan aan leveranciers van de TDS-dienst

Als u een voorschot dat aan de leverancier van de TDS-dienst is gedaan, wilt aanpassen aan een werkelijke betaling, gaat u naar **Leveranciers \> Leveranciers \> Alle leveranciers \> Transacties bewerken**. Als de daadwerkelijke betaling die wordt gedaan, hoger is dan de voorschotbetaling, worden er twee Challan-nummers voor de transactie gegenereerd. In de TDS-opvraag wordt echter alleen het eerste Challan-nummer weergegeven.
