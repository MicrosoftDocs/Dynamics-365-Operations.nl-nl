---
title: Periodiek TDS-vereffeningsproces uitvoeren
description: In dit onderwerp wordt uitgelegd hoe u periodieke TDS (belasting ingehouden op bron) moet vereffenen.
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
ms.openlocfilehash: 6c0aca4d0a916b21ca5ac6ee14e6ab658e0bae26
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726429"
---
# <a name="run-the-periodic-tds-settlement-process"></a>Periodiek TDS-vereffeningsproces uitvoeren

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u periodieke TDS (belasting ingehouden op bron) moet vereffenen.

1. Ga naar **Belasting \> Aangiften \> Bronbelasting \> Betaling van bronbelasting**.

    [![Dialoogvenster Betaling van bronbelasting.](./media/apac-ind-TDS-47.png)](./media/apac-ind-TDS-47.png)

2. Selecteer in het dialoogvenster **Betaling van bronbelasting** de optie **TDS** in het veld **Belastingtype**.
3. Selecteer in het veld **Belastingrekeningnummer (TAN)** het belastingrekeningnummer waarvoor u het vereffeningsproces wilt uitvoeren.
4. Selecteer in het veld **Componentgroep voor bronbelasting** de TDS-componentgroep waarvoor u het vereffeningsproces wilt uitvoeren.
5. Selecteer in het veld **Vereffeningsperiode** de TDS-vereffeningsperiode waarvoor het vereffeningsproces moet worden uitgevoerd.

    > [!NOTE]
    > Het TDS-vereffeningsproces wordt uitgevoerd voor alle perioden die zijn ingesteld voor de TDS-vereffeningsperiode op het tabblad **Perioden** van de pagina **Vereffeningsperioden voor bronbelasting** (**Belasting \> Indirecte belastingen \> Bronbelasting \> Vereffeningsperioden voor bronbelasting**).

6. Selecteer in het veld **Begindatum** de begindatum waarop het TDS-vereffeningsproces moet worden uitgevoerd.

    Voor een specifieke periode binnen de vereffeningsperiode wordt de begindatum die voor de periode is gedefinieerd, beschouwd als de 'vanaf'-datum. De TDS-vereffeningsperiode heeft bijvoorbeeld twee perioden: 1 april tot en met 30 april 2009 en 1 mei tot en met 31 mei 2009. Als u **06/04/2009** (6 april 2009) selecteert als begindatum in het veld **Begindatum**, wordt het vereffeningsproces nog steeds uitgevoerd vanaf 1 april 2009.

    Als u een latere periode invoert in het veld **Begindatum**, maar zonder vereffening van een eerdere periode binnen de vereffeningsperiode, vindt de vereffening niet plaats voor eerdere perioden. De TDS-vereffeningsperiode heeft bijvoorbeeld drie perioden: 1 april tot en met 30 april 2009, 1 mei tot en met 31 mei 2009 en 1 juni tot en met 30 juni 2009. Als u **01/05/2009** (1 mei 2009) selecteert als begindatum in het veld **Begindatum**, wordt het vereffeningsproces alleen uitgevoerd van 1 mei tot en met 31 mei 2009. De vereffening vindt niet plaats van 1 april tot en met 30 april 2009.

7. Selecteer in het veld **Transactiedatum** de datum waarop de TDS-vereffeningstransactie moet worden geboekt.
8. Selecteer in het veld **Versie van bronbelastingbetaling** de versie van de TDS-vereffening.

     - **Oorspronkelijk**: gebruik deze optie om het TDS-vereffeningsproces voor de eerste keer uit te voeren. De oorspronkelijke betalingsversie wordt slechts één keer gebruikt om het TDS-vereffeningsproces uit te voeren voor een combinatie van een TAN, een groep bronbelastingcomponenten en een vereffeningsperiode voor bronbelasting.
    - **Nieuwste versies**: gebruik deze optie als het TDS-vereffeningsproces al is uitgevoerd voor de opgegeven periode. Achterstallige transacties opnemen die zijn geboekt nadat het vereffeningsproces eerder voor de periode was uitgevoerd. U kunt deze optie gebruiken om het vereffeningsproces een willekeurig aantal keren uit te voeren.

9. Schakel het selectievakje **Bijwerken** in om het TDS-vereffeningsproces uit te voeren en de bedragen naar de grootboekrekeningen te boeken. Als dit selectievakje is uitgeschakeld, wordt het vereffeningsproces niet uitgevoerd en worden de financiële posten niet gegenereerd.
10. Selecteer **OK** om het TDS-vereffeningsproces uit te voeren en het bronbelastingbetalingsrapport te genereren. De status van TDS-transacties die zijn opgenomen in het vereffeningsproces wordt weergegeven als **Vereffend** op de pagina **Vereffening** (ga naar **Leveranciers \> Betalingen \> Journaal met betalingen van leverancier**, selecteer **Regels**, selecteer **Functies** en selecteer vervolgens **Vereffening**).

### <a name="important-points"></a>Belangrijke punten

- Als er tijdens het vereffeningsproces geen bronbelastingcomponentgroep is geselecteerd, vindt de vereffening plaats voor alle bronbelastingcomponentgroepen voor de geselecteerde TAN en vereffeningsperiode. Er wordt een afzonderlijke regel gemaakt voor elke groep bronbelastingonderdelen op de pagina **Bewerken als openstaande transactie**.
- Het vereffeningsproces is gebaseerd op de soort belastingplichtige voor een vereffeningsperiode. Transacties waarbij de soort belastingplichtige **Bedrijf** is, worden vereffend en worden als één regel weergegeven op de pagina **Bewerken als openstaande transactie**. Transacties waarbij de soort belastingplichtige iets anders dan **Bedrijf** is, worden vereffend en worden als één regel weergegeven op de pagina **Bewerken als openstaande transactie**.
- De vervaldatum voor de vereffende TDS-transactieregels op de pagina **Bewerken als openstaande transactie** is gebaseerd op de betalingsvoorwaarden die zijn gedefinieerd voor de leverancier van de TDS-dienst op de pagina **Leveranciers**. Als de betalingsvoorwaarden niet zijn gedefinieerd voor de leverancier van de TDS-dienst, wordt de laatste dag van de vereffeningsperiode weergegeven als de vervaldatum.
